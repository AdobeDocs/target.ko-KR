---
solution: Target
product: target
title: Adobe Target MCP 서버 자체 호스팅
description: Python, Docker 또는 로컬 개발 환경을 사용하여 Adobe Target MCP 서버의 자체 인스턴스를 실행하는 방법을 알아봅니다.
feature: Integrations
topic: Experimentation, Personalization, Artificial Intelligence
badge: label="Beta" type="Informative"
role: Developer
level: Experienced
source-git-commit: 7b0c8b18abe2db4e07e3ef979d6d194f4c4c81d6
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 2%

---

# [!DNL Adobe Target] MCP 서버 자체 호스팅 {#target-mcp-self-hosted}


>[!AVAILABILITY]
>
>[!DNL Adobe Target] MCP 서버는 **공개 Beta**&#x200B;의 모든 고객이 사용할 수 있습니다. 현재 **클라우드 웹**, **클라우드 데스크톱**, **클라우드 코드**, **커서** 및 **ChatGPT**&#x200B;에서 지원됩니다.

이 페이지에서는 [!DNL Adobe Target] MCP 서버의 자체 인스턴스를 복제, 구성 및 실행하는 방법에 대해 설명합니다. 자체 호스팅은 로컬 개발 환경, 사용자 지정 네트워크 구성이 필요하거나 서버 코드 베이스에 기여하려는 경우 유용합니다.

>[!AVAILABILITY]
>
>자체 호스팅 배포는 [!DNL Adobe Target] MCP 서버 런타임을 완벽하게 제어해야 하는 개발자 및 고급 사용자를 위한 것입니다. 대부분의 사용자에게는 호스팅된 끝점(`https://targetmcp.adobe.io/mcp`)이 권장됩니다. [MCP 클라이언트 작업](target-mcp.md)을 참조하세요.



## 사전 요구 사항 {#self-hosted-prereqs}

시작하기 전에 다음을 확인하십시오.

* **Python 3.13 이상**
* **[uv](https://github.com/astral-sh/uv){target="_blank"}** — 빠른 Python 패키지 및 프로젝트 관리자

  ```bash
  curl -LsSf https://astral.sh/uv/install.sh | sh
  ```

* Adobe Experience Cloud 액세스가 포함된 활성 [!DNL Adobe Target] 라이선스
* **Artifactory 자격 증명**(Adobe 내부 사용자만 해당) - 내부 종속성을 설치하는 데 필요합니다.

## 설치 {#self-hosted-install}

**1. 리포지토리 복제:**

```bash
git clone https://github.com/Adobe-TnT/target-mcp.git
cd target-mcp
```

**2. 가상 환경 만들기 및 활성화:**

```bash
uv venv --python 3.13
source .venv/bin/activate
```

**3. 환경 변수 구성:**

```bash
cp env.example .env
```

`.env`을(를) 열고 자리 표시자 값을 자격 증명 및 조직 설정으로 바꿉니다.

**4. 종속성 설치:**

```bash
make uv-install
```

**5. 서버 시작:**

사용 사례와 일치하는 모드를 선택합니다.

| 모드 | 명령 | 다음의 경우에 사용 |
|---|---|---|
| StreamableHTTP(API 서버) | `make run-api-server` | HTTP를 통해 MCP 클라이언트 연결 |
| STDIO(로컬 MCP 클라이언트) | `make run-mcp-stdio` | 직접 프로세스 통신 사용 |

## MCP 클라이언트를 로컬 서버에 연결 {#self-hosted-connect}

### 커서

커서 MCP 구성에 다음 내용을 추가합니다. 자리 표시자 값을 실제 IMS 토큰 및 조직 ID로 바꿉니다.

```json
{
  "mcpServers": {
    "target-local": {
      "url": "http://localhost:8080/mcp",
      "headers": {
        "Authorization": "Bearer {IMS_USER_TOKEN}",
        "x-gw-ims-org-id": "{IMS_ORGANIZATION_ID}"
      }
    }
  }
}
```

### 클로드 코드

로컬 서버를 가리키는 클라우드 코드 MCP 구성 파일에 항목을 추가합니다.

```json
{
  "mcpServers": {
    "target-local": {
      "url": "http://localhost:8080/mcp"
    }
  }
}
```

>[!NOTE]
>
>로컬 서버에 연결할 때 위의 커서 예제에서 보듯이 인증 헤더를 수동으로 전달해야 합니다. OAuth 브라우저 흐름은 호스팅된 `https://targetmcp.adobe.io/mcp` 끝점에서만 사용할 수 있습니다.

## Docker 배포 {#self-hosted-docker}

저장소에는 컨테이너화된 배포를 위한 도커 구성 구성이 포함됩니다.

**Docker 작성으로 실행:**

```bash
make run-dc
```

**도커 이미지를 직접 빌드하고 실행합니다.**

```bash
make build
make run-docker
```

## API 엔드포인트 {#self-hosted-endpoints}

자체 호스팅 서버는 다음 HTTP 끝점을 노출합니다.

| 엔드포인트 | 설명 |
|---|---|
| `/mcp` | AI 클라이언트용 MCP 프로토콜 엔드포인트 |
| `/ping` | 라이브니스 검사 — `"Pong"` 반환 |
| `/health` | 상태 검사 — `{"status": "healthy"}` 반환 |
| `/validate` | 입력 유효성 검사 끝점 |
| `/authorize` | OAuth 인증 끝점 |
| `/token` | OAuth 토큰 엔드포인트 |

**상태 검사 예:**

```bash
curl http://localhost:8080/health
# Response: {"status": "healthy"}
```

## 문제 해결 {#self-hosted-troubleshoot}

+++서버 시작 실패

1. Python 3.13+가 설치되어 있는지 확인합니다. `python --version`
1. 가상 환경이 활성화되었는지 확인: `source .venv/bin/activate`
1. `.env`의 모든 환경 변수가 올바르게 설정되어 있는지 확인하십시오.
1. 모든 종속성이 있는지 확인하려면 `make uv-install`을(를) 다시 실행하십시오.

+++

+++MCP 클라이언트에서 연결할 수 없음

1. 서버가 실행 중이고 포트에 액세스할 수 있는지 확인합니다. `curl http://localhost:8080/ping`
1. MCP 클라이언트 구성의 서버 URL이 실행 중인 서버 주소와 일치하는지 확인합니다.
1. Cursor의 경우 `Authorization` 헤더에 만료되지 않은 올바른 IMS 토큰이 있는지 확인하십시오.

+++

+++종속성 설치 실패(Adobe 내부 사용자)

1. Artifactory 자격 증명이 올바르게 구성되었는지 확인합니다.
1. 내부 Artifactory 인스턴스에 대한 네트워크 연결을 확인합니다.
1. Artifactory 액세스는 팀의 DevOps 또는 플랫폼 엔지니어링 담당자에게 문의하십시오.

+++

## 관련 리소스 {#self-hosted-related}

* [MCP 클라이언트 작업](target-mcp.md) — 호스팅된 끝점 설정 및 도구 참조
* [모델 컨텍스트 프로토콜 설명서](https://modelcontextprotocol.io/introduction){target="_blank"}
* [[!DNL Adobe Target] 관리 API 참조](https://developers.adobe.com/target/administer/admin-api/){target="_blank"}
