---
title: GenStudio Experience Selector MFE
description: GenStudio 앱 및 추가 기능에 대한 Experience Selector Micro FrontEnd를 이해하고 구현합니다.
feature: Extensibility, Extensions, Experiences
source-git-commit: d6e580763d85df6d9d295d4e87501af4b022f57b
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 6%

---

# GenStudio Experience Selector MFE

경험 선택기는 GenStudio 경험을 선택할 수 있는 `ExperienceSelectorDialog` 구성 요소를 제공하는 MFE(Micro Frontend)입니다. 독립 실행형 JavaScript 번들에서 `renderExperienceSelectorWithSUSI` 함수를 가져와서 응용 프로그램에서 구성 요소를 사용하십시오. 이 함수는 배포된 최신 Micro Frontend를 자동으로 로드하고 기본 구성 요소 인터페이스를 제공합니다.

GenStudio Experience Selector MFE를 통해 다음과 같은 작업을 수행할 수 있습니다.

- GenStudio 경험 검색 및 선택
- 다양한 기준으로 경험 필터링
- 단일 및 다중 선택 모드 모두 지원
- SUSI(Sign-Up Sign-In) 통합을 통해 인증 처리
- 다양한 프레임워크에서 일관된 UI 제공

## 통합 옵션

MFE는 두 가지 서로 다른 접근 방식을 사용하여 통합할 수 있습니다.

### ESM(ES 모듈) - 권장

```javascript
import { renderExperienceSelectorWithSUSI } from 'https://experience-stage.adobe.com/solutions/GenStudio-experience-selector-mfe/static-assets/resources/@genstudio/experience-selector/esm/standalone.js';
```

### UMD(유니버설 모듈 정의)

```html
<script src="https://experience-stage.adobe.com/solutions/GenStudio-experience-selector-mfe/static-assets/resources/@genstudio/experience-selector/umd/standalone.js"></script>
```

## 구성 속성

`renderExperienceSelectorWithSUSI` 함수는 다음 속성을 가진 구성 개체를 허용합니다.

| 속성 | 유형 | 필수 | 설명 |
|----------|------|----------|-------------|
| `apiKey` | 문자열 | 예 | GenStudio 서비스용 API 키 |
| `imsOrg` | 문자열 | 예 | IMS 조직 ID |
| `env` | 문자열 | 예 | 환경(`stage`, `prod`) |
| `susiConfig` | 오브젝트 | 예 | [SUSI 인증 구성](#susi-configuration) |
| `onSelectionConfirmed` | 함수 | 예 | 선택이 확인될 때의 콜백 |
| `onDismiss` | 함수 | 예 | 대화 상자가 해제된 경우 콜백 |
| `locale` | 문자열 | 아니요 | 언어 로케일(예: `en-US`) |
| `isOpen` | 부울 | 아니요 | 초기 대화 상자 상태 |
| `selectionType` | 문자열 | 아니요 | 선택 모드(`single` 또는 `multiple`) |
| `customFilters` | 배열 | 아니요 | 사용자 지정 필터 기준 |
| `dialogTitle` | 문자열 | 아니요 | 사용자 지정 대화 상자 제목 |

### SUSI 구성

`susiConfig` 개체는 다음을 포함할 수 있습니다.

```javascript
{
  clientId: 'genstudio',
  environment: 'stg1', // or 'prod'
  scope: 'additional_info.projectedProductContext,additional_info.ownerOrg,AdobeID,openid,session,read_organizations,ab.manage',
  locale: 'en_US',
  modalSettings: {
    width: 500,
    height: 700
  }
}
```

## 빠른 시작

1. 아래의 사용 가능한 예제에서 **프레임워크를 선택하십시오**
1. **예제 디렉터리로 이동**
1. **종속성 설치**(React/Vue 예제의 경우)
1. API 키 및 IMS 조직을 사용하여 **구성 업데이트**:

   ```javascript
   const experienceSelectorProps = {
     locale: 'en-US',
     apiKey: 'exc_app',           
     imsOrg: 'your-ims-org@AdobeOrg',  // Replace with your IMS Org
     env: 'stage', // or 'prod'
     susiConfig: {
        clientId: 'genstudio',
        environment: 'stg1', // or 'prod'
        scope: 'additional_info.projectedProductContext,additional_info.ownerOrg,AdobeID,openid,session,read_organizations,ab.manage',
        locale: 'en_US',
        modalSettings: {
          width: 500,
          height: 700,
        },
     },
     customFilters: ['genstudio-channel:email'],
     selectionType: 'single', // or 'multiple'
     dialogTitle: 'Select Email Templates'
   };
   ```

1. **개발 서버 실행**

### 예제 구현

이 저장소에는 다양한 프레임워크의 작업 예가 포함됩니다.

- [Vite 빌드 시스템과의 통합을 보여 주는 전체 React 응용 프로그램](https://github.com/adobe/genstudio-extensibility-examples/tree/main/genstudio-experience-selector-mfe/react-js).

- [컴퍼지션 API가 통합된 Vue 3 응용 프로그램](https://github.com/adobe/genstudio-extensibility-examples/tree/main/genstudio-experience-selector-mfe/vue-js).

- [두 개의 바닐라 JavaScript 구현](https://github.com/adobe/genstudio-extensibility-examples/tree/main/genstudio-experience-selector-mfe/vanilla-js):

- [이 바닐라 ESM 버전은 ES6 모듈과 최신 JavaScript을 사용합니다](https://github.com/adobe/genstudio-extensibility-examples/tree/main/genstudio-experience-selector-mfe/vanilla-js/vanilla-esm).

- [이 바닐라 UMD 버전은 스크립트 태그를 통해 로드된 UMD 번들을 사용합니다](https://github.com/adobe/genstudio-extensibility-examples/tree/main/genstudio-experience-selector-mfe/vanilla-js/vanilla-umd-global-var).

## 인증 흐름

경험 선택기는 SUSI를 통해 인증을 자동으로 처리합니다.

1. 대화 상자가 열리면 기존 인증을 확인합니다.
1. 인증되지 않으면 SUSI 로그인 플로우가 열립니다.
1. 인증에 성공하면 경험 선택기가 표시됩니다.
1. 사용자는 경험을 찾아보고 선택할 수 있습니다.
1. 선택한 경험은 `onSelectionConfirmed` 콜백을 통해 반환됩니다.
