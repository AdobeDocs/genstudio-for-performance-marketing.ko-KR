---
title: AI Assistant 연결
description: 지원되는 AI 도우미를 [!DNL GenStudio for Performance Marketing]에 연결하고 사용 가능한 도구에 대한 액세스를 확인하는 방법을 알아봅니다.
role: User
source-git-commit: 6fb7ddb7549ea6bcd66b6139fbde9ebe12ddaa22
workflow-type: tm+mt
source-wordcount: '623'
ht-degree: 0%
---

# AI 지원 연결

성능 데이터를 쿼리하거나 초안을 조합하거나 승인된 광고를 게시하기 전에 지원되는 AI 도우미를 [!DNL GenStudio for Performance Marketing]에 연결하십시오. 연결 옵션은 AI 비서 및 조직에 따라 다릅니다.

## 사전 요구 사항

연결하기 전에 다음을 확인합니다.

- [!DNL GenStudio for Performance Marketing]에 액세스할 수 있는 활성 Adobe 계정입니다.
- Claude, ChatGPT 또는 Microsoft Copilot을 사용할 때 원격 MCP 연결을 허용하는 지원 플랜. 수동으로 MCP 연결을 구성하는 방법에 대한 특정 지침은 AI 지원 설명서를 참조하십시오.

## Adobe CX Enterprise Coworker 연결

[!DNL GenStudio for Performance Marketing] 도구는 Adobe CX Enterprise Coworker에서 기본 연결로 관리됩니다. 조직은 가용성을 제어하므로 직접 MCP 서버 URL을 입력하지 않습니다.

새 대화를 시작하고 [연결을 확인](#verify-the-connection)합니다. 도구가 표시되지 않으면 조직의 관리자 또는 Adobe 담당자에게 문의하십시오.

## 클로드 연결

Claude는 Pro, Max, Team 또는 Enterprise 플랜이 필요합니다. 동일한 원격 커넥터가 웹의 클라우드 및 데스크탑 애플리케이션에서 작동합니다.

1. 클로드의 왼쪽 사이드바에서 **[!UICONTROL 사용자 지정]**&#x200B;을 선택합니다.
1. **[!UICONTROL 커넥터]**&#x200B;를 선택한 다음 추가 아이콘을 선택합니다.
1. **[!UICONTROL 사용자 지정 커넥터 추가]**&#x200B;를 선택합니다.
1. `https://genstudio-services.adobe.io/mcp`을(를) MCP 서버 URL로 입력하십시오.
1. Adobe ID으로 로그인합니다.
1. [!DNL GenStudio for Performance Marketing]에 액세스할 수 있는 IMS 조직을 선택하십시오.

> [!NOTE]
> 팀 또는 엔터프라이즈 플랜에서 조직 소유자는 먼저 커넥터를 추가해야 할 수 있습니다. 커넥터를 이미 사용할 수 있는 경우 대신 **[!UICONTROL 연결]**&#x200B;을 선택하십시오.

## ChatGPT 연결

ChatGPT를 사용하려면 Plus, Pro, Business, Enterprise 또는 Education 계정이 필요합니다. 사용자 지정 MCP 연결은 개발자 모드를 통해 웹에서 사용할 수 있습니다.

1. 웹 브라우저에서 [ChatGPT](https://chatgpt.com)에 로그인합니다.
1. **[!UICONTROL 설정]**&#x200B;을 연 다음 **[!UICONTROL 개발자 모드]**&#x200B;를 사용하도록 설정합니다.
1. **[!UICONTROL 설정]**&#x200B;에서 앱 또는 커넥터의 영역을 엽니다.
1. `GenStudio`(이)라는 사용자 지정 MCP 연결을 추가합니다.
1. `https://genstudio-services.adobe.io/mcp`을(를) MCP 서버 URL로 입력하십시오.
1. **[!UICONTROL OAuth]**&#x200B;을(를) 인증 방법으로 유지합니다.
1. Adobe ID으로 로그인합니다.
1. [!DNL GenStudio for Performance Marketing]에 액세스할 수 있는 IMS 조직을 선택하십시오.

> [!NOTE]
> ChatGPT는 개발자 및 커넥터 설정의 위치를 변경할 수 있습니다. 이러한 레이블이 계정과 다른 경우, 원격 MCP 커넥터 추가에 대한 현재 OpenAI 지침을 따르십시오.

## Codex 연결

Codex에는 Codex 명령줄 인터페이스와 인증된 Codex 계정이 필요합니다.

1. 모든 프로젝트에 대해 `~/.codex/config.toml`을(를) 열거나 한 프로젝트에 대해 `.codex/config.toml`을(를) 엽니다.
1. 이 구성 추가:

   ```toml
   [mcp_servers.genstudio]
   url = "https://genstudio-services.adobe.io/mcp"
   auth = "oauth"
   ```

1. `codex mcp login genstudio` 실행.
1. 열려 있는 브라우저 창에서 Adobe ID으로 로그인합니다.
1. [!DNL GenStudio for Performance Marketing]에 액세스할 수 있는 IMS 조직을 선택하십시오.

## 작성기 연결

작성기는 AI Studio에 대한 액세스 권한이 필요합니다.

1. Writer에서 **[!UICONTROL AI Studio]**&#x200B;을(를) 엽니다.
1. **[!UICONTROL 커넥터 및 도구]**&#x200B;를 선택하십시오.
1. **[!UICONTROL 사용자 지정 커넥터 만들기]**&#x200B;를 선택합니다.
1. 커넥터 유형으로 **[!UICONTROL MCP 서버]**&#x200B;를 선택하십시오.
1. 커넥터의 이름과 설명을 입력합니다.
1. `https://genstudio-services.adobe.io/mcp`을(를) MCP 서버 URL로 입력하십시오.
1. 커넥터의 팀 액세스 권한을 설정합니다.
1. 인증 방법으로 **[!UICONTROL OAuth 2.0(사용자 수준)]**&#x200B;을(를) 선택하십시오.
1. Adobe ID으로 로그인합니다.
1. **[!UICONTROL 저장]**&#x200B;을 선택합니다.

[!DNL GenStudio for Performance Marketing]개의 도구가 AI Studio 도구 라이브러리에 표시됩니다. 각 작성기 사용자는 개별 Adobe ID으로 로그인합니다.

## Microsoft Copilot 연결

Microsoft은 Copilot에서 사용자 지정 MCP 연결의 설정 플로우를 제어합니다. 현재 [Microsoft Copilot 설명서](https://learn.microsoft.com/en-us/copilot/)에 따라 원격 MCP 서버를 추가한 다음 `https://genstudio-services.adobe.io/mcp`을(를) 서버 URL로 사용합니다.

메시지가 표시되면 Adobe ID으로 로그인하고 [!DNL GenStudio for Performance Marketing]에 액세스할 수 있는 IMS 조직을 선택합니다.

## 연결 확인

설정 후 도구를 사용할 수 있는지 확인합니다.

1. AI 도우미에서 새 대화를 시작하십시오.
1. 액세스할 수 있는 [!DNL GenStudio for Performance Marketing] 도구를 도우미에게 요청하십시오.
1. 응답에 Insights, Create 및 Activate 의 도구가 나열되는지 확인합니다.
1. 연결된 유료 미디어 채널에 대한 성능 요약을 요청합니다.

도우미는 사용 가능한 성능 데이터를 반환하거나 요청과 일치하는 데이터가 없는 이유를 설명합니다.

> [!TIP]
> 인증에 실패하면 다시 연결하고 올바른 IMS 조직을 선택했는지 확인합니다. 도구가 나타나지 않으면 계정에 [!DNL GenStudio for Performance Marketing]에 대한 액세스 권한이 있는지 확인하십시오.

## 관련 기능

- [AI 지원 개요](overview.md)
- [AI 지원 사용](use-ai-assistants.md)
- [AI 지원 도구 참조](tools-reference.md)
