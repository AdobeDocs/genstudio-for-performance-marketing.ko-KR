---
title: App Builder 앱 만들기
description: 앱 또는 추가 기능 빌드를 시작하여 GenStudio for Performance Marketing을 확장합니다.
feature: Extensibility
exl-id: 4e757dd4-a02d-472c-bc13-6f27dffa48f2
source-git-commit: 04a4f6432c5db87489e39f9396a7782c86441695
workflow-type: tm+mt
source-wordcount: '453'
ht-degree: 0%

---

# App Builder 앱 개발

GenStudio for Performance Marketing의 기본 기능을 확장하는 개발자는 [Adobe App Builder](https://developer.adobe.com/app-builder/)을(를) 사용하여 확장 가능한 앱 또는 추가 기능을 만들고, 제출하고, 배포합니다.

>[!BEGINSHADEBOX]

**필수 구성 요소**:

* Node.js(버전 20.x 이상)

* npm(Node.js와 함께 패키지됨)

* Adobe Developer 명령줄 인터페이스(CLI). npm으로 설치하려면 다음을 실행하십시오. `npm install -g @adobe/aio-cli`

>[!ENDSHADEBOX]

## 앱 구조

GenStudio for Performance Marketing 추가 기능은 App Builder 앱이며 다른 App Builder 앱과 동일한 기본 구성 요소를 포함합니다.

### 빌드 및 구성 파일

App Builder 앱의 주요 구성 요소에는 이러한 빌드 및 구성 파일이 포함됩니다. 이 목록에는 모든 빌드 및 구성 파일이 포함되어 있지 않습니다.

* `README.md`: 앱에 대한 일반 정보를 포함합니다.

* TS 앱 파일:

   * `package.json`
   * `package-lock.json`
   * `eslint`
   * `tsconfig`
   * `jest test up`

* App Builder 구성 파일:

   * `app.config.yaml`
   * `ext.config.yaml`: 추가 기능에 대한 구성 파일입니다.
   * `app.config.yaml`: 추가 기능에 대한 구성 파일(앱을 GenStudio for Performance Marketing 추가 기능으로 정의 포함).
   * `.aio`
   * `.env`: `.env` 파일을 소스 제어에 커밋하지 마십시오.

### Source 코드

```
- src/
    - genstudiopem/
        - web-src/
            - src/
                - components/
                - utils/
                - Constants.ts
                - index.tsx
                - index.css
                - utils.ts
        - index.html
```

### Source 코드 구성 요소

* `ExtensionRegistration.tsx`: 호스트 앱(GenStudio for Performance Marketing)에서 추가 기능을 로드하고 표시하는 데 필요한 API를 정의합니다.

* `App.tsx`: 다른 구성 요소로의 라우팅을 정의하는 기본 앱 구성 요소입니다.

* `AdditionalContextDialog.tsx`: 추가 컨텍스트 추가 기능을 표시하기 위한 대화 상자 구성 요소입니다.

* `RightPanel.tsx`: 유효성 검사 추가 기능에 대한 대화 상자 구성 요소입니다.

* `Helper`개 구성 요소: `ClaimsChecker`개 포함.

## 기존 앱에서 App Builder 앱 만들기

예제 앱을 사용하여 추가 기능 만들기를 바로 시작할 수 있습니다.

**기존 앱에서 App Builder 앱을 만들려면**:

1. [GenStudio UIX 예제](https://github.com/adobe/genstudio-uix-examples) 리포지토리에서 예제 앱을 다운로드합니다.

1. [Adobe Developer Console](https://developer.adobe.com/console/)의 App Builder 프로젝트 작업 영역에서 [!UICONTROL 모두 다운로드]를 선택하여 프로젝트 세부 정보를 다운로드합니다.

1. 선호하는 IDE(통합 개발 환경)에서 로컬로 예제 앱을 엽니다.

1. Adobe Developer 명령줄 인터페이스를 사용하여 인증:

   ```bash
   aio login
   ```

1. JSON 파일을 다운로드한 다음 앱을 만듭니다.

   ```bash
   aio app use '/path/to/your/downloaded/app-builder/project/details/config.json'
   ```

## 추가 기능에 사용자 지정 코드 추가

`AdditionalContextDialog.tsx` 및 `RightPanel.tsx` 파일에 추가 기능 코드를 정의합니다. 이 두 파일은 사용자가 추가 기능에 액세스할 때 팝업 모양과 동작을 정의합니다.

* `AdditionalContextDialog.tsx`: _컨텍스트 추가_ 추가 기능을 사용하려면 이 구성 요소를 정의하십시오. 사용자가 _의 프롬프트 창에서_&#x200B;추가 기능[!DNL Create]을(를) 클릭하면 이 구성 요소와 상호 작용합니다.

* `RightPanel.tsx`: _오른쪽 패널_ 추가 기능(경험 유효성 검사)을 사용하려면 이 구성 요소를 정의하십시오. 사용자가 [!DNL Create] 경험 초안의 오른쪽 패널에서 유효성 검사 추가 기능을 클릭하면 이 구성 요소와 상호 작용합니다.

## 앱 개발 우수 사례

개발 환경을 유지 관리하면 앱 개발 및 배포 오류를 방지하는 데 도움이 될 수 있습니다.

* 이전 버전의 샘플 앱을 사용하는 경우 종속성을 다시 설치하여 업그레이드합니다.

  ```bash
  rm -rf node_modules package-lock.json && npm i
  ```

* GenStudio UIX SDK을 업그레이드합니다. [GenStudio UIX SDK](https://github.com/adobe/genstudio-uix-sdk)의 최신 버전을 사용 중인지 확인하십시오. 최신 SDK 변경 내용을 사용하는 방법에 대해 알아보려면 [GenStudio UIX 예제 저장소](https://github.com/adobe/genstudio-uix-examples)를 참조하십시오.

이제 [앱을 배포](deploy-app.md)할 준비가 되었습니다.
