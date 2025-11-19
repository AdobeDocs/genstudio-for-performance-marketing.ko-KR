---
title: GenStudio Experience Selector MFE
description: GenStudio 앱 및 추가 기능에 대한 Experience Selector Micro FrontEnd를 이해하고 구현합니다.
feature: Extensibility, Extensions, Experiences
source-git-commit: 27e85e62f83bad391348c45da1558cd1a58204fc
workflow-type: tm+mt
source-wordcount: '522'
ht-degree: 4%

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
import { renderExperienceSelectorWithSUSI } from 'https://experience.adobe.com/solutions/GenStudio-experience-selector-mfe/static-assets/resources/@genstudio/experience-selector/esm/standalone.js';
```

### UMD(유니버설 모듈 정의)

```html
<script src="https://experience.adobe.com/solutions/GenStudio-experience-selector-mfe/static-assets/resources/@genstudio/experience-selector/umd/standalone.js"></script>
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

- [Vite 빌드 시스템과의 통합을 보여 주는 **완전한 React 응용 프로그램**](https://github.com/adobe/genstudio-extensibility-examples/tree/main/genstudio-experience-selector-mfe/react-js).

- [컴퍼지션 API가 통합된 **Vue 3 응용 프로그램**](https://github.com/adobe/genstudio-extensibility-examples/tree/main/genstudio-experience-selector-mfe/vue-js).

- [두 개의 **바닐라 JavaScript 구현**](https://github.com/adobe/genstudio-extensibility-examples/tree/main/genstudio-experience-selector-mfe/vanilla-js):

   - [이 **바닐라 ESM** 버전은 ES6 모듈과 최신 JavaScript을 사용합니다](https://github.com/adobe/genstudio-extensibility-examples/tree/main/genstudio-experience-selector-mfe/vanilla-js/vanilla-esm).

   - [이 **바닐라 UMD** 버전은 스크립트 태그를 통해 로드된 UMD 번들을 사용합니다](https://github.com/adobe/genstudio-extensibility-examples/tree/main/genstudio-experience-selector-mfe/vanilla-js/vanilla-umd-global-var).

## 인증 흐름

경험 선택기는 SUSI를 통해 인증을 자동으로 처리합니다.

1. 대화 상자가 열리면 기존 인증을 확인합니다.
1. 인증되지 않으면 SUSI 로그인 플로우가 열립니다.
1. 인증에 성공하면 경험 선택기가 표시됩니다.
1. 사용자는 경험을 찾아보고 선택할 수 있습니다.
1. 선택한 경험은 `onSelectionConfirmed` 콜백을 통해 반환됩니다.

## 선택 콜백

MFE에서 [!DNL Experience]을(를) 선택하고 **[!UICONTROL Use]** 단추를 클릭하면 콜백 함수를 호출하여 선택한 [!DNL Experience]의 세부 정보를 전달해야 합니다.

콜백은 [!DNL Experience]을(를) 나타내는 HTML 문자열을 제공합니다. 경험에 자산(예: 이미지, 비디오)이 포함된 경우 `<img>` 및 `<video>`과(와) 같은 HTML 요소에는 이러한 자산에 대한 사전 서명된 URL이 포함된 `src` 특성이 포함됩니다. 사전 서명된 URL의 만료 시간은 30분이며 이 시간 동안 클라이언트 응용 프로그램에서 [!DNL Experience]을(를) 사용해야 합니다.

### 출력 스키마

`onSelectionConfirmed` 콜백은 다음 구조의 [!DNL Experience] 개체 배열을 수신합니다.

| 속성 | 유형 | 설명 |
|----------|------|-------------|
| `id` | `string` | [!DNL Experience]의 고유 식별자(URN 형식). |
| `content` | `string` | [!DNL Experience]을(를) 나타내는 Base64로 인코딩된 HTML 문자열입니다. |
| `experienceFields` | `object` | [!DNL Experience]에서 편집 가능한 필드의 키-값 쌍입니다. `experienceFields`의 각 필드는 다음을 포함합니다. <ul><li>`fieldName`: 필드의 이름/식별자입니다.</li><li>`fieldValue`: 필드의 실제 콘텐츠/값입니다.</li></ul> |
| `metadata` | `object` | 경험에 대한 메타데이터(예: `channel`, `externalTemplateMetadata`, `externalAssetMetadata` 등) |
| `aspectVariants` | `array` | [!DNL Experience]에 대한 종횡비 변형의 배열입니다. 각 변형에는 다음이 포함됩니다. <ul><li>`aspectKey`: 변형에 대한 고유 식별자입니다.</li><li>`aspectMetadata`: `channel` 및 `aspectRatio`을(를) 포함한 메타데이터.</li><li>`content`: 이 특정 종횡비에 대해 Base64로 인코딩된 HTML 문자열입니다.</li></ul> |

### JSON 예

다음은 스키마를 보여주는 샘플 JSON 블록입니다.

```json
{
    "id": "urn:aaid:aem:d97f687f-1192-42c0-89a7-a3fee646ac2f",
    "content": "PCEtLSBGYWNlYm9vayAxOjEgQ2hyb21lIC0tPgo8IWRvY3R5cGUgaHRtbD4KPGh0bWwKICAgIHN0eWxlPSJtYXJnaW46IDA7IHBhZGRpbmc6IDA7IGJvcmRlcjogMDsgZm9udDogaW5oZXJpdDsgZm9udC1zaXplOiAxMDAlOyBib3gtc2l6aW5nOiBib3JkZXItYm94OyBtYXJnaW46IDBweDsgaGVpZ2h0OiAxMDAlOyIKPgogIDxoZWFkPgogICAgPG1ldGEgY2hhcnNldD0idXRmLTgiIC8+CiAgPC9oZWFkPgo8Ym9keQogIHN0eWxlPSJtYXJnaW46IDA7IHBhZGRpbmc6IDA7IGJvcmRlcjogMDsgZm9udDogaW5oZXJpdDsgZm9udC1zaXplOiAxMDAlOyBsaW5lLWhlaWdodDogMTsgYm94LXNpemluZzogYm9yZGVyLWJveDsgbWFyZ2luOiAwcHg7IGhlaWdodDogMTAwJTsiCj4KPGRpdgpzdHlsZT0iCiAgd2lkdGg6IDEwODBweDsKICBiYWNrZ3JvdW5kLWNvbG9yOiByZ2IoMjU1IDI1NSAyNTUpOwogIGRpc3BsYXk6IGZsZXg7CiAgZmxleC1kaXJlY3Rpb246IGNvbHVtbjsKICBmb250LXNpemU6IDQ2cHg7CiAgZm9udC1mYW1pbHk6IGluaXRpYWw7CiIKPgo8ZGl2CiAgc3R5bGU9IgogICAgZGlzcGxheTogZmxleDsKICAgIGZsZXgtZ3JvdzogMDsKICAgIGZsZXgtZGlyZWN0aW9uOiBjb2x1bW47CiAgICBib3JkZXItcmFkaXVzOiAwLjVlbTsKICAgIG92ZXJmbG93OiBoaWRkZW47CiAgIgo+CiAgPGRpdiBkYXRhLWdzLXNlY3Rpb249ImNocm9tZSI+CiAgICA8ZGl2CiAgICAgIHN0eWxlPSIKICAgICAgICBwYWRkaW5nLXRvcDogMWVtOwogICAgICAgIHBhZGRpbmctYm90dG9tOiAwLjU4M2VtOwogICAgICAgIHBhZGRpbmctbGVmdDogMWVtOwogICAgICAgIHBhZGRpbmctcmlnaHQ6IDFlbTsKICAgICAgICBnYXA6IDFlbTsKICAgICAgICBmbGV4LWdyb3c6IDA7CiAgICAgICAgZGlzcGxheTogZmxleDsKICAgICAgICBmbGV4LWRpcmVjdGlvbjogY29sdW1uOwogICAgICAgIGZvbnQtc2l6ZTogMC44NzVlbTsKICAgICAgICBsaW5lLWhlaWdodDogMS4yNWVtOwogICAgICAgIGZvbnQtZmFtaWx5OiBBcmlhbCwgc2Fucy1zZXJpZjsKICAgICAgIgogICAgPgogICAgICA8ZGl2IHN0eWxlPSJkaXNwbGF5OiBmbGV4OyBnYXA6IDAuNWVtOyBhbGlnbi1pdGVtczogY2VudGVyIj4KICAgICAgICA8aW1nCiAgICAgICAgICBzcmM9ImRhdGE6aW1hZ2UvcG5nO2Jhc2U2NCxpVkJPUncwS0dnb0FBQUFOU1VoRVVnQUFBQUVBQUFBQkNBSUFBQUNRZDFQZUFBQUFDWEJJV1hNQUFBc1RBQUFMRXdFQW1wd1lBQUFBREVsRVFWUUltV05nWjJjSEFBQXVBQmJIWkZROUFBQUFBRWxGVGtTdVFtQ0MiCiAgICAgICAgICBzdHlsZT0iCiAgICAgICAgICAgIHdpZHRoOiA4NXB4OyAKICAgICAgICAgICAgaGVpZ2h0OiA4NXB4OyAKICAgICAgICAgICAgYm9yZGVyLXJhZGl1czogOTk5OXB4OyAKICAgICAgICAgICAgcG9zaXRpb246IHN0YXRpYzsiCiAgICAgICAgLz4KICAgICAgICA8ZGl2CiAgICAgICAgICBzdHlsZT0iCiAgICAgICAgICAgIGRpc3BsYXk6IGZsZXg7CiAgICAgICAgICAgIGxpbmUtaGVpZ2h0OiAxZW07CiAgICAgICAgICAgIGZsZXgtZGlyZWN0aW9uOiBjb2x1bW47CiAgICAgICAgICAiCiAgICAgICAgPgogICAgICAgICAgPGRpdiBzdHlsZT0iZm9udC13ZWlnaHQ6IDcwMDsgZm9udC1zaXplOiAxZW07IG1hcmdpbi1ib3R0b206IDAuMmVtIj5Zb3VyIEJyYW5kPC9kaXY+CiAgICAgICAgICA8ZGl2IHN0eWxlPSJjb2xvcjogcmdiKDE1NiAxNjMgMTc1KTsgZm9udC1zaXplOiAwLjg3NWVtIj5TcG9uc29yZWQ8L2Rpdj4KICAgICAgICA8L2Rpdj4KICAgICAgPC9kaXY+CiAgICAgIDxkaXYgc3R5bGU9ImZvbnQtd2VpZ2h0OiA1MDA7IGZvbnQtc2l6ZTogMS4yZW07IGxpbmUtaGVpZ2h0OiAxLjJlbSIgZGF0YS1ncy1lZGl0LXJlZmVyZW5jZT0iYm9keSI+CiAgICAgICAgU3RlcCBpbnRvIGEgd29ybGQgb2Ygd29uZGVyIHdpdGggb3VyIHBsYXlmdWwgZmFudGFzeSByb2xlLXBsYXkuIElnbml0ZSB5b3VyIGltYWdpbmF0aW9uIGFuZCBleHBsb3JlIGVuZGxlc3MgZnVuIQogICAgICA8L2Rpdj4KICAgIDwvZGl2PgogIDwvZGl2PgogIDxkaXYgCiAgICBzdHlsZT0iIAogICAgZmxleC1zaHJpbms6IDA7IAogICAgd2lkdGg6IDEwMCU7IAogICAgaGVpZ2h0OiAxMDgwcHg7IAogICAgb3ZlcmZsb3c6IGhpZGRlbjsgCiAgICBsaW5lLWhlaWdodDogaW5pdGlhbDsgCiAgICBwb3NpdGlvbjogcmVsYXRpdmU7IiAKICAgIGlkPSJkMDk1OGViMS03Njc4LTQwN2MtYmZjNS0zOWQ1YWM4NjMzMzIiCiAgICBkYXRhLWdzLXNlY3Rpb249ImJvZHkiCiAgPgogICAgPGRpdiBzdHlsZT0id2lkdGg6IDEwODBweDsgaGVpZ2h0OiAxMDgwcHg7IG92ZXJmbG93OiBoaWRkZW47Ij48aW1nIHNyYz0iaHR0cHM6Ly9kZWxpdmVyeS1wMTA2NjUzLWUzMjY3MDUtY21zdGcuYWRvYmVhZW1jbG91ZC5jb20vYWRvYmUvYXNzZXRzL3VybjphYWlkOmFlbTpjYTM5MjQyNy03MDVkLTQ4MjctYmE2Zi1lMmI1YjYyYTA1NjAvYXMvcmVuZGVyLnBuZz90b2tlbiYjeDNEOzNhMDVmYzdlODllNWQzODJiYmM1N2YxYTljMDExNzcxNjMwNTIyZDM0ZDNhNWUzYzI4ZDlhMjQ4MDIxYTcwMmUmYW1wO2V4cGlyeVRpbWUmI3gzRDsyMDI1LTExLTE3VDIzJTNBMTclM0EwNS43NTBaIiBoZWlnaHQ9IjEwMCUiIHdpZHRoPSIxMDAlIiBzdHlsZT0ib2JqZWN0LWZpdDogY292ZXI7Ii8+PC9kaXY+CiAgPC9kaXY+CiAgPGRpdiBkYXRhLWdzLXNlY3Rpb249ImNocm9tZSI+CiAgICA8ZGl2CiAgICAgIHN0eWxlPSIKICAgICAgICBwYWRkaW5nOiAxLjEyZW0gMWVtIDFlbSAxZW07CiAgICAgICAgZ2FwOiAxZW07CiAgICAgICAganVzdGlmeS1jb250ZW50OiBzcGFjZS1iZXR3ZWVuOwogICAgICAgIGFsaWduLWl0ZW1zOiBjZW50ZXI7CiAgICAgICAgZGlzcGxheTogZmxleDsKICAgICAgICBmb250LXNpemU6IDAuODc1ZW07CiAgICAgICAgbGluZS1oZWlnaHQ6IDEuMjVlbTsKICAgICAgICBmb250LWZhbWlseTogQXJpYWwsIHNhbnMtc2VyaWY7CiAgICAgICIKICAgID4KICAgICAgPGRpdj4KICAgICAgICA8ZGl2CiAgICAgICAgICBzdHlsZT0iZm9udC1zaXplOiAxZW07IGxpbmUtaGVpZ2h0OiAxZW07IGNvbG9yOiByZ2IoMTU2IDE2MyAxNzUpOyBtYXJnaW4tYm90dG9tOiAwLjJlbSIKICAgICAgICAgIGRhdGEtZ3MtZWRpdC1yZWZlcmVuY2U9ImRpc3BsYXlfdXJsIgogICAgICAgID4KICAgICAgICAgIGV4YW1wbGUuY29tCiAgICAgICAgPC9kaXY+CiAgICAgICAgPGRpdiBzdHlsZT0ib3ZlcmZsb3ctd3JhcDogYnJlYWstd29yZDsgZm9udC13ZWlnaHQ6IDUwMDsgZm9udC1zaXplOiAxLjJlbSIgZGF0YS1ncy1lZGl0LXJlZmVyZW5jZT0iaGVhZGxpbmUiPgogICAgICAgICAgQXdha2VuIHRoZSBtYWdpYyB3aXRoaW4KICAgICAgICA8L2Rpdj4KICAgICAgPC9kaXY+CiAgICAgIDxidXR0b24KICAgICAgICBzdHlsZT0iCiAgICAgICAgICBiYWNrZ3JvdW5kLWNvbG9yOiByZ2IoMjQzLCAyNDQsIDI0Nik7CiAgICAgICAgICBwYWRkaW5nLXRvcDogMC4zNzVlbTsKICAgICAgICAgIHBhZGRpbmctYm90dG9tOiAwLjM3NWVtOwogICAgICAgICAgcGFkZGluZy1sZWZ0OiAwLjVlbTsKICAgICAgICAgIHBhZGRpbmctcmlnaHQ6IDAuNWVtOwogICAgICAgICAgbWF4LXdpZHRoOiA0NSU7CiAgICAgICAgICBjb2xvcjogcmdiKDEwNywgMTE0LCAxMjgpOwogICAgICAgICAgZm9udC1zaXplOiAxLjFlbTsKICAgICAgICAgIG92ZXJmbG93LXdyYXA6IGJyZWFrLXdvcmQ7CiAgICAgICAgICBmbGV4LXNocmluazogMDsKICAgICAgICAgIGJvcmRlcjogMDsKICAgICAgICAiCiAgICAgICAgZGF0YS1ncy1lZGl0LXJlZmVyZW5jZT0iY3RhIgogICAgICA+CiAgICAgICAgTGVhcm4gbW9yZQogICAgICA8L2J1dHRvbj4KICAgIDwvZGl2PgogIDwvZGl2Pgo8L2Rpdj4KPC9kaXY+CjwvYm9keT4KPC9odG1sPgo=",
    "experienceFields": {
        "body": {
            "fieldName": "body",
            "fieldValue": "Step into a world of wonder with our playful fantasy role-play. Ignite your imagination and explore endless fun!"
        },
        "headline": {
            "fieldName": "headline",
            "fieldValue": "Awaken the magic within"
        },
        "cta": {
            "fieldName": "cta",
            "fieldValue": "Learn more"
        },
        "display_url": {
            "fieldName": "display_url",
            "fieldValue": "example.com"
        },
        "destination_url": {
            "fieldName": "destination_url",
            "fieldValue": "https://www.adobe.com"
        },
        "description": {
            "fieldName": "description",
            "fieldValue": "description"
        },
        "image": {
            "fieldName": "image",
            "fieldValue": "https://delivery-p106653-e326705-cmstg.adobeaemcloud.com/adobe/assets/urn:aaid:aem:ca392427-705d-4827-ba6f-e2b5b62a0560/original/as/aa5d839d4e3044e582033ef953b36833.png?token=3a05fc7e89e5d382bbc57f1a9c011771630522d34d3a5e3c28d9a248021a702e&expiryTime=2025-11-17T23%3A17%3A05.750Z"
        },
        "image_name": {
            "fieldName": "image_name",
            "fieldValue": "aa5d839d-4e30-44e5-8203-3ef953b36833.png"
        }
    },
    "metadata": {
        "channel": "meta",
        // externalAssetMetadata is present only if experience has external assets
        "externalAssetMetadata": {
            "36031A56669DEACD0A49402F@AdobeOrg;acct:aem-cmstg-p106653-e326705@adobe.com;urn:aaid:aem:cf126281-c115-4f83-81d4-5fe26f04c758": {
                "assetId": "assets/man_bike_hill.png",
                "assetSignedPreviewUrl": "https://genstudio-uix-external-dam-demo.s3.us-east-1.amazonaws.com/thumbnails/man_bike_hill.jpg?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAU6GD2JLYS2TWIMO7%2F20251111%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20251111T003440Z&X-Amz-Expires=3600&X-Amz-Signature=ece36fe4147b85f2de80452cad88fea84bb215057e5c3da0e0ce00913bc3080f&X-Amz-SignedHeaders=host&x-amz-checksum-mode=ENABLED&x-id=GetObject",
                "assetSignedUrl": "https://genstudio-uix-external-dam-demo.s3.us-east-1.amazonaws.com/assets/man_bike_hill.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAU6GD2JLYS2TWIMO7%2F20251111%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20251111T003440Z&X-Amz-Expires=3600&X-Amz-Signature=a83ee4289aef1fbb057e864f15f5983fdf70ab60a934e30ca6e7ac195b3ed6a8&X-Amz-SignedHeaders=host&x-amz-checksum-mode=ENABLED&x-id=GetObject",
                "assetSourceUrl": "https://genstudio-uix-external-dam-demo.s3.us-east-1.amazonaws.com/assets/man_bike_hill.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAU6GD2JLYS2TWIMO7%2F20251111%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20251111T003440Z&X-Amz-Expires=3600&X-Amz-Signature=a83ee4289aef1fbb057e864f15f5983fdf70ab60a934e30ca6e7ac195b3ed6a8&X-Amz-SignedHeaders=host&x-amz-checksum-mode=ENABLED&x-id=GetObject",
                "extensionIconUrl": "data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0iVVRGLTgiPz4KPHN2ZyB3aWR0aD0iMjRweCIgaGVpZ2h0PSIyNHB4IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHZlcnNpb249IjEuMSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIiB4bWxuczp4bGluaz0iaHR0cDovL3d3dy53My5vcmcvMTk5OS94bGluayI+CiAgICA8IS0tIEdlbmVyYXRvcjogU2tldGNoIDY0ICg5MzUzNykgLSBodHRwczovL3NrZXRjaC5jb20gLS0+CiAgICA8dGl0bGU+SWNvbi1BcmNoaXRlY3R1cmUvMTYvQXJjaF9BbWF6b24tUzMtU3RhbmRhcmRfMTY8L3RpdGxlPgogICAgPGRlc2M+Q3JlYXRlZCB3aXRoIFNrZXRjaC48L2Rlc2M+CiAgICA8ZGVmcz4KICAgICAgICA8bGluZWFyR3JhZGllbnQgeDE9IjAlIiB5MT0iMTAwJSIgeDI9IjEwMCUiIHkyPSIwJSIgaWQ9ImxpbmVhckdyYWRpZW50LTEiPgogICAgICAgICAgICA8c3RvcCBzdG9wLWNvbG9yPSIjMUI2NjBGIiBvZmZzZXQ9IjAlIj48L3N0b3A+CiAgICAgICAgICAgIDxzdG9wIHN0b3AtY29sb3I9IiM2Q0FFM0UiIG9mZnNldD0iMTAwJSI+PC9zdG9wPgogICAgICAgIDwvbGluZWFyR3JhZGllbnQ+CiAgICA8L2RlZnM+CiAgICA8ZyBpZD0iSWNvbi1BcmNoaXRlY3R1cmUvMTYvQXJjaF9BbWF6b24tUzMtU3RhbmRhcmRfMTYiIHN0cm9rZT0ibm9uZSIgc3Ryb2tlLXdpZHRoPSIxIiBmaWxsPSJub25lIiBmaWxsLXJ1bGU9ImV2ZW5vZGQiPgogICAgICAgIDxnIGlkPSJJY29uLUFyY2hpdGVjdHVyZS1CRy8xNi9TdG9yYWdlIiBmaWxsPSJ1cmwoI2xpbmVhckdyYWRpZW50LTEpIj4KICAgICAgICAgICAgPHJlY3QgaWQ9IlJlY3RhbmdsZSIgeD0iMCIgeT0iMCIgd2lkdGg9IjI0IiBoZWlnaHQ9IjI0Ij48L3JlY3Q+CiAgICAgICAgPC9nPgogICAgICAgIDxwYXRoIGQ9Ik0xOC4xNTg5NDk1LDEzLjM1MzU3MTkgTDE4LjE4NjM2NTcsMTMuMTg3ODk1NiBDMTguMzQ4ODMyMiwxMy4yODA5MDY5IDE4LjQ4MTg1MTYsMTMuMzY0MjI5NCAxOC41ODY0MzkzLDEzLjQzMzk4NzkgQzE4LjQ2NzYzNTgsMTMuNDE1NTc5NCAxOC4zMjA0MDA2LDEzLjM4NzQ4MjIgMTguMTU4OTQ5NSwxMy4zNTM1NzE5IEwxOC4xNTg5NDk1LDEzLjM1MzU3MTkgWiBNMTEuOTIwMjM4NiwxMS43OTU2MzM2IEMxMS45MjAyMzg2LDEyLjA2MjA3MjEgMTEuNjkyNzg1NSwxMi4yODAwNjcyIDExLjQxMjUzMSwxMi4yODAwNjcyIEMxMS4xMzMyOTE4LDEyLjI4MDA2NzIgMTAuOTA0ODIzNCwxMi4wNjIwNzIxIDEwLjkwNDgyMzQsMTEuNzk1NjMzNiBDMTAuOTA0ODIzNCwxMS41MjgyMjYzIDExLjEzMzI5MTgsMTEuMzExMjAwMSAxMS40MTI1MzEsMTEuMzExMjAwMSBDMTEuNjkyNzg1NSwxMS4zMTEyMDAxIDExLjkyMDIzODYsMTEuNTI4MjI2MyAxMS45MjAyMzg2LDExLjc5NTYzMzYgTDExLjkyMDIzODYsMTEuNzk1NjMzNiBaIE0xNi4zMzgzMTAxLDE4LjE2NjkwMzUgQzE2LjI1MTk5OTgsMTguMjE0Mzc4IDE2LjA2NDE0OCwxOC4yODEyMjk4IDE1LjkwNjc1ODYsMTguMzM4MzkzIEwxNS42NDE3MzUzLDE4LjQzNTI3OTcgQzE1LjM3MDYxOTQsMTguNTM3MDEwNyAxNS4wNDg3MzI4LDE4LjYyOTA1MzEgMTQuNjgxMTUyNSwxOC43MDg1MDAyIEMxMy43NjExODYzLDE4LjkxMDk5MzQgMTIuNDg3ODU1NiwxOS4wMzExMzI5IDExLjI3NzQ4MDcsMTkuMDMxMTMyOSBDNy40Nzg4MTI0NywxOS4wMzExMzI5IDYuNTE2MTk4ODYsMTguNDAzMzA3MSA2LjQ4MTY3NDc1LDE4LjE5ODg3NjEgTDUuMjEwMzc0OTIsOC44MzQ3NzU4NyBDNi42MjY4NzkxMiw5LjUyOTQ1MzU2IDkuMDc1MDQ1MTYsOS44NTc4OTk1IDExLjQxMjUzMSw5Ljg1Nzg5OTUgQzEzLjUxMTM5NDIsOS44NTc4OTk1IDE2LjI5NTY2MjYsOS41NjA0NTczMSAxNy44ODM3NzIsOC44MTkyNzQgTDE3LjE3NjAyNzYsMTMuMTAwNjk3NiBDMTUuNjkyNTA2LDEyLjY2NTY3NjMgMTMuOTIzNjUyNywxMS44ODE4NjI4IDEyLjg3MjY5OCwxMS40MDIyNzM2IEMxMi42OTA5Mzg3LDEwLjc5MTg4NzQgMTIuMTA5MTA1OCwxMC4zNDIzMzMgMTEuNDEyNTMxLDEwLjM0MjMzMyBDMTAuNTcyNzgyNiwxMC4zNDIzMzMgOS44ODk0MDgxNSwxMC45OTM0MTE3IDkuODg5NDA4MTUsMTEuNzk1NjMzNiBDOS44ODk0MDgxNSwxMi41OTY4ODY3IDEwLjU3Mjc4MjYsMTMuMjQ4OTM0MiAxMS40MTI1MzEsMTMuMjQ4OTM0MiBDMTIuMDEyNjQxMywxMy4yNDg5MzQyIDEyLjUyNzQ1NjgsMTIuOTEyNzM3NCAxMi43NzYyMzM2LDEyLjQzMTIxMDQgQzEzLjkwNjM5MDcsMTIuOTQwODM0NSAxNS41ODY5MDI4LDEzLjY2MzYwOTQgMTcuMDE1NTkyLDE0LjA2NzYyNjkgTDE2LjMzODMxMDEsMTguMTY2OTAzNSBaIE0xMS40MTI1MzEsNS45Njg4NjcwNyBDMTUuNzQ0MjkyMiw1Ljk2ODg2NzA3IDE4LjA4Nzg3MDUsNi45OTE5OTA3IDE4LjExNTI4NjcsNy40MjAyMjk5NCBMMTguMTExMjI1LDcuNDQzNDgyNzUgQzE4LjA2MjQ4NTEsNy44NzU1OTc0NyAxNS43MjQ5OTkzLDguODg5MDMyNDIgMTEuNDEyNTMxLDguODg5MDMyNDIgQzcuMzA0MTYxMDYsOC44ODkwMzI0MiA1LjA1NDAwMDk4LDcuOTM5NTQyNjkgNS4wMjE1MDc2OSw3LjQ0MDU3NjE1IEw1LjAxOTQ3Njg2LDcuNDIxMTk4ODEgQzUuMDM3NzU0MzMsNi45MjQxNyA3LjI5MDk2MDY2LDUuOTY4ODY3MDcgMTEuNDEyNTMxLDUuOTY4ODY3MDcgTDExLjQxMjUzMSw1Ljk2ODg2NzA3IFogTTE4LjM1Njk1NTUsMTIuMTYwODk2NSBMMTkuMTI5Njg2NSw3LjUwNDUyMTM4IEwxOS4xMjk2ODY1LDcuNTAzNTUyNTEgQzE5LjEzMTcxNzMsNy40NzgzNjE5NyAxOS4xMzU3NzksNy40NTUxMDkxNiAxOS4xMzU3NzksNy40Mjg5NDk3NSBDMTkuMTM1Nzc5LDUuNjQ2MjM0MzQgMTQuNTE3NjcwNiw1IDExLjQxMjUzMSw1IEM3Ljg0MjMzMTExLDUgNCw1Ljc2MDU2MDY1IDQsNy40Mjg5NDk3NSBDNCw3LjQ1MDI2NDgyIDQuMDAzMDQ2MjUsNy40NzA2MTEwMyA0LjAwNDA2MTY2LDcuNDkwOTU3MjQgTDUuNDc3NDI5MTEsMTguMzM5MzYxOCBDNS41NDc0OTI3NiwxOC43NTAxNjE1IDUuNzYwNzI5OTUsMjAgMTEuMjc3NDgwNywyMCBDMTIuNTU5OTUwMSwyMCAxMy45MTc1NjAyLDE5Ljg3MTE0MDcgMTQuOTA4NjA1NSwxOS42NTMxNDU2IEMxNS4zMjM5MTAzLDE5LjU2MjA3MjEgMTUuNjk1NTUyMywxOS40NTU0OTY3IDE2LjAxMzM3NzIsMTkuMzM2MzI2MSBMMTYuMjY2MjE1NiwxOS4yNDQyODM3IEMxNi43OTMyMTYxLDE5LjA1NDM4NTcgMTcuMzM3NDc4NiwxOC44NTg2NzQ2IDE3LjMzMjQwMTYsMTguMzM3NDI0MSBMMTguMDAwNTQ0OCwxNC4zMTE3ODE0IEMxOC40NTQ0MzU0LDE0LjQwNTc2MTUgMTguODAxNzA3NCwxNC40NDkzNjA1IDE5LjA1MjUxNDksMTQuNDQ5MzYwNSBDMTkuNTIxNjM2NywxNC40NDkzNjA1IDE5LjcwMDM0OTgsMTQuMzE4NTYzNSAxOS44MjQyMzA1LDE0LjE3ODA3NzggQzE5Ljk3MjQ4MTEsMTQuMDA5NDk0OSAyMC4wMjkzNDQzLDEzLjc5NzMxMyAxOS45ODU2ODE1LDEzLjU4MDI4NjggQzE5Ljg5NzM0MDQsMTMuMTQ4MTcyMSAxOS40MjgyMTg1LDEyLjczNTQzNDcgMTguMzU2OTU1NSwxMi4xNjA4OTY1IEwxOC4zNTY5NTU1LDEyLjE2MDg5NjUgWiIgaWQ9IkFtYXpvbi1TMy1TdGFuZGFyZC1JY29uXzE2X1NxdWlkIiBmaWxsPSIjRkZGRkZGIj48L3BhdGg+CiAgICA8L2c+Cjwvc3ZnPg==",
                "extensionId": "genstudio-external-s3-dam",
                "extensionSource": "External S3 DAM",
                "isAssetDeliverable": false,
                "keywords": ["S3Asset"]
            }
        },
        // externalTemplateMetadata is present only if experience has external templates
        "externalTemplateMetadata": {
            "additionalMetadata": {
                "test": "test"
            },
            "extensionId": "257324-GSTemplateImport",
            "id": "two-pod-duplicate-fields",
            "mapping": {
                "btn": "cta",
                "btn1": "cta",
                "btn2": "cta",
                "content": "body",
                "content1": "body",
                "content2": "body",
                "else": "other",
                "else1": "other",
                "else2": "other",
                "head": "headline",
                "head1": "headline",
                "head2": "headline",
                "pod1_btn": "cta",
                "pod1_btn1": "cta",
                "pod1_btn2": "cta",
                "pod1_content": "body",
                "pod1_content1": "body",
                "pod1_content2": "body",
                "pod1_else": "other",
                "pod1_else1": "other",
                "pod1_else2": "other",
                "pod1_head": "headline",
                "pod1_head1": "headline",
                "pod1_head2": "headline",
                "pod1_subhead": "sub_headline",
                "pod1_subhead1": "sub_headline",
                "pod1_subhead2": "sub_headline",
                "pod2_btn": "cta",
                "pod2_btn1": "cta",
                "pod2_btn2": "cta",
                "pod2_content": "body",
                "pod2_content1": "body",
                "pod2_content2": "body",
                "pod2_else": "other",
                "pod2_else1": "other",
                "pod2_else2": "other",
                "pod2_head": "headline",
                "pod2_head1": "headline",
                "pod2_head2": "headline",
                "pod2_subhead": "sub_headline",
                "pod2_subhead1": "sub_headline",
                "pod2_subhead2": "sub_headline",
                "subhead": "sub_headline",
                "subhead1": "sub_headline",
                "subhead2": "sub_headline"
            },
            "source": "External Template App"
        },
        // externalTemplateId and externalTemplateSource are present only if experience has external templates
        "externalTemplateId": "two-pod-duplicate-fields",
        "externalTemplateSource": "External Template App"
    },
    "aspectVariants": [
        {
            "aspectKey": "Variant_meta_1x1_0",
            "aspectMetadata": {
                "channel": "meta",
                "aspectRatio": "1:1"
            },
            "content": "PCEtLSBGYWNlYm9vayAxOjEgQ2hyb21lIC0tPgo8IWRvY3R5cGUgaHRtbD4KPGh0bWwKICAgIHN0eWxlPSJtYXJnaW46IDA7IHBhZGRpbmc6IDA7IGJvcmRlcjogMDsgZm9udDogaW5oZXJpdDsgZm9udC1zaXplOiAxMDAlOyBib3gtc2l6aW5nOiBib3JkZXItYm94OyBtYXJnaW46IDBweDsgaGVpZ2h0OiAxMDAlOyIKPgogIDxoZWFkPgogICAgPG1ldGEgY2hhcnNldD0idXRmLTgiIC8+CiAgPC9oZWFkPgo8Ym9keQogIHN0eWxlPSJtYXJnaW46IDA7IHBhZGRpbmc6IDA7IGJvcmRlcjogMDsgZm9udDogaW5oZXJpdDsgZm9udC1zaXplOiAxMDAlOyBsaW5lLWhlaWdodDogMTsgYm94LXNpemluZzogYm9yZGVyLWJveDsgbWFyZ2luOiAwcHg7IGhlaWdodDogMTAwJTsiCj4KPGRpdgpzdHlsZT0iCiAgd2lkdGg6IDEwODBweDsKICBiYWNrZ3JvdW5kLWNvbG9yOiByZ2IoMjU1IDI1NSAyNTUpOwogIGRpc3BsYXk6IGZsZXg7CiAgZmxleC1kaXJlY3Rpb246IGNvbHVtbjsKICBmb250LXNpemU6IDQ2cHg7CiAgZm9udC1mYW1pbHk6IGluaXRpYWw7CiIKPgo8ZGl2CiAgc3R5bGU9IgogICAgZGlzcGxheTogZmxleDsKICAgIGZsZXgtZ3JvdzogMDsKICAgIGZsZXgtZGlyZWN0aW9uOiBjb2x1bW47CiAgICBib3JkZXItcmFkaXVzOiAwLjVlbTsKICAgIG92ZXJmbG93OiBoaWRkZW47CiAgIgo+CiAgPGRpdiBkYXRhLWdzLXNlY3Rpb249ImNocm9tZSI+CiAgICA8ZGl2CiAgICAgIHN0eWxlPSIKICAgICAgICBwYWRkaW5nLXRvcDogMWVtOwogICAgICAgIHBhZGRpbmctYm90dG9tOiAwLjU4M2VtOwogICAgICAgIHBhZGRpbmctbGVmdDogMWVtOwogICAgICAgIHBhZGRpbmctcmlnaHQ6IDFlbTsKICAgICAgICBnYXA6IDFlbTsKICAgICAgICBmbGV4LWdyb3c6IDA7CiAgICAgICAgZGlzcGxheTogZmxleDsKICAgICAgICBmbGV4LWRpcmVjdGlvbjogY29sdW1uOwogICAgICAgIGZvbnQtc2l6ZTogMC44NzVlbTsKICAgICAgICBsaW5lLWhlaWdodDogMS4yNWVtOwogICAgICAgIGZvbnQtZmFtaWx5OiBBcmlhbCwgc2Fucy1zZXJpZjsKICAgICAgIgogICAgPgogICAgICA8ZGl2IHN0eWxlPSJkaXNwbGF5OiBmbGV4OyBnYXA6IDAuNWVtOyBhbGlnbi1pdGVtczogY2VudGVyIj4KICAgICAgICA8aW1nCiAgICAgICAgICBzcmM9ImRhdGE6aW1hZ2UvcG5nO2Jhc2U2NCxpVkJPUncwS0dnb0FBQUFOU1VoRVVnQUFBQUVBQUFBQkNBSUFBQUNRZDFQZUFBQUFDWEJJV1hNQUFBc1RBQUFMRXdFQW1wd1lBQUFBREVsRVFWUUltV05nWjJjSEFBQXVBQmJIWkZROUFBQUFBRWxGVGtTdVFtQ0MiCiAgICAgICAgICBzdHlsZT0iCiAgICAgICAgICAgIHdpZHRoOiA4NXB4OyAKICAgICAgICAgICAgaGVpZ2h0OiA4NXB4OyAKICAgICAgICAgICAgYm9yZGVyLXJhZGl1czogOTk5OXB4OyAKICAgICAgICAgICAgcG9zaXRpb246IHN0YXRpYzsiCiAgICAgICAgLz4KICAgICAgICA8ZGl2CiAgICAgICAgICBzdHlsZT0iCiAgICAgICAgICAgIGRpc3BsYXk6IGZsZXg7CiAgICAgICAgICAgIGxpbmUtaGVpZ2h0OiAxZW07CiAgICAgICAgICAgIGZsZXgtZGlyZWN0aW9uOiBjb2x1bW47CiAgICAgICAgICAiCiAgICAgICAgPgogICAgICAgICAgPGRpdiBzdHlsZT0iZm9udC13ZWlnaHQ6IDcwMDsgZm9udC1zaXplOiAxZW07IG1hcmdpbi1ib3R0b206IDAuMmVtIj5Zb3VyIEJyYW5kPC9kaXY+CiAgICAgICAgICA8ZGl2IHN0eWxlPSJjb2xvcjogcmdiKDE1NiAxNjMgMTc1KTsgZm9udC1zaXplOiAwLjg3NWVtIj5TcG9uc29yZWQ8L2Rpdj4KICAgICAgICA8L2Rpdj4KICAgICAgPC9kaXY+CiAgICAgIDxkaXYgc3R5bGU9ImZvbnQtd2VpZ2h0OiA1MDA7IGZvbnQtc2l6ZTogMS4yZW07IGxpbmUtaGVpZ2h0OiAxLjJlbSIgZGF0YS1ncy1lZGl0LXJlZmVyZW5jZT0iYm9keSI+CiAgICAgICAgU3RlcCBpbnRvIGEgd29ybGQgb2Ygd29uZGVyIHdpdGggb3VyIHBsYXlmdWwgZmFudGFzeSByb2xlLXBsYXkuIElnbml0ZSB5b3VyIGltYWdpbmF0aW9uIGFuZCBleHBsb3JlIGVuZGxlc3MgZnVuIQogICAgICA8L2Rpdj4KICAgIDwvZGl2PgogIDwvZGl2PgogIDxkaXYgCiAgICBzdHlsZT0iIAogICAgZmxleC1zaHJpbms6IDA7IAogICAgd2lkdGg6IDEwMCU7IAogICAgaGVpZ2h0OiAxMDgwcHg7IAogICAgb3ZlcmZsb3c6IGhpZGRlbjsgCiAgICBsaW5lLWhlaWdodDogaW5pdGlhbDsgCiAgICBwb3NpdGlvbjogcmVsYXRpdmU7IiAKICAgIGlkPSJkMDk1OGViMS03Njc4LTQwN2MtYmZjNS0zOWQ1YWM4NjMzMzIiCiAgICBkYXRhLWdzLXNlY3Rpb249ImJvZHkiCiAgPgogICAgPGRpdiBzdHlsZT0id2lkdGg6IDEwODBweDsgaGVpZ2h0OiAxMDgwcHg7IG92ZXJmbG93OiBoaWRkZW47Ij48aW1nIHNyYz0iaHR0cHM6Ly9kZWxpdmVyeS1wMTA2NjUzLWUzMjY3MDUtY21zdGcuYWRvYmVhZW1jbG91ZC5jb20vYWRvYmUvYXNzZXRzL3VybjphYWlkOmFlbTpjYTM5MjQyNy03MDVkLTQ4MjctYmE2Zi1lMmI1YjYyYTA1NjAvYXMvcmVuZGVyLnBuZz90b2tlbiYjeDNEOzNhMDVmYzdlODllNWQzODJiYmM1N2YxYTljMDExNzcxNjMwNTIyZDM0ZDNhNWUzYzI4ZDlhMjQ4MDIxYTcwMmUmYW1wO2V4cGlyeVRpbWUmI3gzRDsyMDI1LTExLTE3VDIzJTNBMTclM0EwNS43NTBaIiBoZWlnaHQ9IjEwMCUiIHdpZHRoPSIxMDAlIiBzdHlsZT0ib2JqZWN0LWZpdDogY292ZXI7Ii8+PC9kaXY+CiAgPC9kaXY+CiAgPGRpdiBkYXRhLWdzLXNlY3Rpb249ImNocm9tZSI+CiAgICA8ZGl2CiAgICAgIHN0eWxlPSIKICAgICAgICBwYWRkaW5nOiAxLjEyZW0gMWVtIDFlbSAxZW07CiAgICAgICAgZ2FwOiAxZW07CiAgICAgICAganVzdGlmeS1jb250ZW50OiBzcGFjZS1iZXR3ZWVuOwogICAgICAgIGFsaWduLWl0ZW1zOiBjZW50ZXI7CiAgICAgICAgZGlzcGxheTogZmxleDsKICAgICAgICBmb250LXNpemU6IDAuODc1ZW07CiAgICAgICAgbGluZS1oZWlnaHQ6IDEuMjVlbTsKICAgICAgICBmb250LWZhbWlseTogQXJpYWwsIHNhbnMtc2VyaWY7CiAgICAgICIKICAgID4KICAgICAgPGRpdj4KICAgICAgICA8ZGl2CiAgICAgICAgICBzdHlsZT0iZm9udC1zaXplOiAxZW07IGxpbmUtaGVpZ2h0OiAxZW07IGNvbG9yOiByZ2IoMTU2IDE2MyAxNzUpOyBtYXJnaW4tYm90dG9tOiAwLjJlbSIKICAgICAgICAgIGRhdGEtZ3MtZWRpdC1yZWZlcmVuY2U9ImRpc3BsYXlfdXJsIgogICAgICAgID4KICAgICAgICAgIGV4YW1wbGUuY29tCiAgICAgICAgPC9kaXY+CiAgICAgICAgPGRpdiBzdHlsZT0ib3ZlcmZsb3ctd3JhcDogYnJlYWstd29yZDsgZm9udC13ZWlnaHQ6IDUwMDsgZm9udC1zaXplOiAxLjJlbSIgZGF0YS1ncy1lZGl0LXJlZmVyZW5jZT0iaGVhZGxpbmUiPgogICAgICAgICAgQXdha2VuIHRoZSBtYWdpYyB3aXRoaW4KICAgICAgICA8L2Rpdj4KICAgICAgPC9kaXY+CiAgICAgIDxidXR0b24KICAgICAgICBzdHlsZT0iCiAgICAgICAgICBiYWNrZ3JvdW5kLWNvbG9yOiByZ2IoMjQzLCAyNDQsIDI0Nik7CiAgICAgICAgICBwYWRkaW5nLXRvcDogMC4zNzVlbTsKICAgICAgICAgIHBhZGRpbmctYm90dG9tOiAwLjM3NWVtOwogICAgICAgICAgcGFkZGluZy1sZWZ0OiAwLjVlbTsKICAgICAgICAgIHBhZGRpbmctcmlnaHQ6IDAuNWVtOwogICAgICAgICAgbWF4LXdpZHRoOiA0NSU7CiAgICAgICAgICBjb2xvcjogcmdiKDEwNywgMTE0LCAxMjgpOwogICAgICAgICAgZm9udC1zaXplOiAxLjFlbTsKICAgICAgICAgIG92ZXJmbG93LXdyYXA6IGJyZWFrLXdvcmQ7CiAgICAgICAgICBmbGV4LXNocmluazogMDsKICAgICAgICAgIGJvcmRlcjogMDsKICAgICAgICAiCiAgICAgICAgZGF0YS1ncy1lZGl0LXJlZmVyZW5jZT0iY3RhIgogICAgICA+CiAgICAgICAgTGVhcm4gbW9yZQogICAgICA8L2J1dHRvbj4KICAgIDwvZGl2PgogIDwvZGl2Pgo8L2Rpdj4KPC9kaXY+CjwvYm9keT4KPC9odG1sPgo="
        },
        {
            "aspectKey": "Variant_meta_9x16_1",
            "aspectMetadata": {
                "channel": "meta",
                "aspectRatio": "9:16"
            },
            "content": "PCEtLSBGYWNlYm9vayA5OjE2IENocm9tZSAtLT4KPCFkb2N0eXBlIGh0bWw+CjxodG1sCiAgICBzdHlsZT0ibWFyZ2luOiAwOyBwYWRkaW5nOiAwOyBib3JkZXI6IDA7IGZvbnQ6IGluaGVyaXQ7IGZvbnQtc2l6ZTogMTAwJTsgYm94LXNpemluZzogYm9yZGVyLWJveDsgbWFyZ2luOiAwcHg7IGhlaWdodDogMTAwJTsiCj4KICA8aGVhZD4KICAgIDxtZXRhIGNoYXJzZXQ9InV0Zi04IiAvPgogIDwvaGVhZD4KPGJvZHkKICBzdHlsZT0ibWFyZ2luOiAwOyBwYWRkaW5nOiAwOyBib3JkZXI6IDA7IGZvbnQ6IGluaGVyaXQ7IGZvbnQtc2l6ZTogMTAwJTsgbGluZS1oZWlnaHQ6IDE7IGJveC1zaXppbmc6IGJvcmRlci1ib3g7IG1hcmdpbjogMHB4OyBoZWlnaHQ6IDEwMCU7Igo+CjxkaXYKc3R5bGU9IgogIHdpZHRoOiAxMDgwcHg7CiAgYmFja2dyb3VuZC1jb2xvcjogcmdiKDI1NSAyNTUgMjU1KTsKICBkaXNwbGF5OiBmbGV4OwogIGZsZXgtZGlyZWN0aW9uOiBjb2x1bW47CiAgZm9udC1zaXplOiA0NnB4OwogIGZvbnQtZmFtaWx5OiBpbml0aWFsOwoiCj4KPGRpdgogIHN0eWxlPSIKICAgIGRpc3BsYXk6IGZsZXg7CiAgICBmbGV4LWdyb3c6IDA7CiAgICBmbGV4LWRpcmVjdGlvbjogY29sdW1uOwogICAgYm9yZGVyLXJhZGl1czogMC41ZW07CiAgICBvdmVyZmxvdzogaGlkZGVuOwogICIKPgogIDxkaXYgZGF0YS1ncy1zZWN0aW9uPSJjaHJvbWUiPgogICAgPGRpdgogICAgICBzdHlsZT0iCiAgICAgICAgcGFkZGluZy10b3A6IDFlbTsKICAgICAgICBwYWRkaW5nLWJvdHRvbTogMC41ODNlbTsKICAgICAgICBwYWRkaW5nLWxlZnQ6IDFlbTsKICAgICAgICBwYWRkaW5nLXJpZ2h0OiAxZW07CiAgICAgICAgZ2FwOiAxZW07CiAgICAgICAgZmxleC1ncm93OiAwOwogICAgICAgIGRpc3BsYXk6IGZsZXg7CiAgICAgICAgZmxleC1kaXJlY3Rpb246IGNvbHVtbjsKICAgICAgICBmb250LXNpemU6IDAuODc1ZW07CiAgICAgICAgbGluZS1oZWlnaHQ6IDEuMjVlbTsKICAgICAgICBmb250LWZhbWlseTogQXJpYWwsIHNhbnMtc2VyaWY7CiAgICAgICIKICAgID4KICAgICAgPGRpdiBzdHlsZT0iZGlzcGxheTogZmxleDsgZ2FwOiAwLjVlbTsgYWxpZ24taXRlbXM6IGNlbnRlciI+CiAgICAgICAgPGltZwogICAgICAgICAgc3JjPSJkYXRhOmltYWdlL3BuZztiYXNlNjQsaVZCT1J3MEtHZ29BQUFBTlNVaEVVZ0FBQUFFQUFBQUJDQUlBQUFDUWQxUGVBQUFBQ1hCSVdYTUFBQXNUQUFBTEV3RUFtcHdZQUFBQURFbEVRVlFJbVdOZ1oyY0hBQUF1QUJiSFpGUTlBQUFBQUVsRlRrU3VRbUNDIgogICAgICAgICAgc3R5bGU9IgogICAgICAgICAgICB3aWR0aDogODVweDsgCiAgICAgICAgICAgIGhlaWdodDogODVweDsgCiAgICAgICAgICAgIGJvcmRlci1yYWRpdXM6IDk5OTlweDsgCiAgICAgICAgICAgIHBvc2l0aW9uOiBzdGF0aWM7IgogICAgICAgIC8+CiAgICAgICAgPGRpdgogICAgICAgICAgc3R5bGU9IgogICAgICAgICAgICBkaXNwbGF5OiBmbGV4OwogICAgICAgICAgICBsaW5lLWhlaWdodDogMWVtOwogICAgICAgICAgICBmbGV4LWRpcmVjdGlvbjogY29sdW1uOwogICAgICAgICAgIgogICAgICAgID4KICAgICAgICAgIDxkaXYgc3R5bGU9ImZvbnQtd2VpZ2h0OiA3MDA7IGZvbnQtc2l6ZTogMWVtOyBtYXJnaW4tYm90dG9tOiAwLjJlbSI+WW91ciBCcmFuZDwvZGl2PgogICAgICAgICAgPGRpdiBzdHlsZT0iY29sb3I6IHJnYigxNTYgMTYzIDE3NSk7IGZvbnQtc2l6ZTogMC44NzVlbSI+U3BvbnNvcmVkPC9kaXY+CiAgICAgICAgPC9kaXY+CiAgICAgIDwvZGl2PgogICAgICA8ZGl2IHN0eWxlPSJmb250LXdlaWdodDogNTAwOyBmb250LXNpemU6IDEuMmVtOyBsaW5lLWhlaWdodDogMS4yZW0iIGRhdGEtZ3MtZWRpdC1yZWZlcmVuY2U9ImJvZHkiPgogICAgICAgIFN0ZXAgaW50byBhIHdvcmxkIG9mIHdvbmRlciB3aXRoIG91ciBwbGF5ZnVsIGZhbnRhc3kgcm9sZS1wbGF5LiBJZ25pdGUgeW91ciBpbWFnaW5hdGlvbiBhbmQgZXhwbG9yZSBlbmRsZXNzIGZ1biEKICAgICAgPC9kaXY+CiAgICA8L2Rpdj4KICA8L2Rpdj4KICA8ZGl2IAogICAgc3R5bGU9IiAKICAgIGZsZXgtc2hyaW5rOiAwOyAKICAgIHdpZHRoOiAxMDAlOyAKICAgIGhlaWdodDogMTkyMHB4OyAKICAgIG92ZXJmbG93OiBoaWRkZW47IAogICAgbGluZS1oZWlnaHQ6IGluaXRpYWw7IAogICAgcG9zaXRpb246IHJlbGF0aXZlOyIgCiAgICBpZD0iZjI4MzM3ODUtMjZhNC00ZGQzLTk4OGEtMTM1ZDE5OTJhMzUzIgogICAgZGF0YS1ncy1zZWN0aW9uPSJib2R5IgogID4KICAgIDxkaXYgc3R5bGU9IndpZHRoOiAxMDgwcHg7IGhlaWdodDogMTkyMHB4OyBvdmVyZmxvdzogaGlkZGVuOyI+PGltZyBzcmM9Imh0dHBzOi8vZGVsaXZlcnktcDEwNjY1My1lMzI2NzA1LWNtc3RnLmFkb2JlYWVtY2xvdWQuY29tL2Fkb2JlL2Fzc2V0cy91cm46YWFpZDphZW06Y2EzOTI0MjctNzA1ZC00ODI3LWJhNmYtZTJiNWI2MmEwNTYwL2FzL3JlbmRlci5wbmc/dG9rZW4mI3gzRDszYTA1ZmM3ZTg5ZTVkMzgyYmJjNTdmMWE5YzAxMTc3MTYzMDUyMmQzNGQzYTVlM2MyOGQ5YTI0ODAyMWE3MDJlJmFtcDtleHBpcnlUaW1lJiN4M0Q7MjAyNS0xMS0xN1QyMyUzQTE3JTNBMDUuNzUwWiIgaGVpZ2h0PSIxMDAlIiB3aWR0aD0iMTAwJSIgc3R5bGU9Im9iamVjdC1maXQ6IGNvdmVyOyIvPjwvZGl2PgogIDwvZGl2PgogIDxkaXYgZGF0YS1ncy1zZWN0aW9uPSJjaHJvbWUiPgogICAgPGRpdgogICAgICBzdHlsZT0iCiAgICAgICAgcGFkZGluZzogMS4xMmVtIDFlbSAxZW0gMWVtOwogICAgICAgIGdhcDogMWVtOwogICAgICAgIGp1c3RpZnktY29udGVudDogc3BhY2UtYmV0d2VlbjsKICAgICAgICBhbGlnbi1pdGVtczogY2VudGVyOwogICAgICAgIGRpc3BsYXk6IGZsZXg7CiAgICAgICAgZm9udC1zaXplOiAwLjg3NWVtOwogICAgICAgIGxpbmUtaGVpZ2h0OiAxLjI1ZW07CiAgICAgICAgZm9udC1mYW1pbHk6IEFyaWFsLCBzYW5zLXNlcmlmOwogICAgICAiCiAgICA+CiAgICAgIDxkaXY+CiAgICAgICAgPGRpdgogICAgICAgICAgc3R5bGU9ImZvbnQtc2l6ZTogMWVtOyBsaW5lLWhlaWdodDogMWVtOyBjb2xvcjogcmdiKDE1NiAxNjMgMTc1KTsgbWFyZ2luLWJvdHRvbTogMC4yZW0iCiAgICAgICAgICBkYXRhLWdzLWVkaXQtcmVmZXJlbmNlPSJkaXNwbGF5X3VybCIKICAgICAgICA+CiAgICAgICAgICBleGFtcGxlLmNvbQogICAgICAgIDwvZGl2PgogICAgICAgIDxkaXYgc3R5bGU9Im92ZXJmbG93LXdyYXA6IGJyZWFrLXdvcmQ7IGZvbnQtd2VpZ2h0OiA1MDA7IGZvbnQtc2l6ZTogMS4yZW0iIGRhdGEtZ3MtZWRpdC1yZWZlcmVuY2U9ImhlYWRsaW5lIj4KICAgICAgICAgIEF3YWtlbiB0aGUgbWFnaWMgd2l0aGluCiAgICAgICAgPC9kaXY+CiAgICAgIDwvZGl2PgogICAgICA8YnV0dG9uCiAgICAgICAgc3R5bGU9IgogICAgICAgICAgYmFja2dyb3VuZC1jb2xvcjogcmdiKDI0MywgMjQ0LCAyNDYpOwogICAgICAgICAgcGFkZGluZy10b3A6IDAuMzc1ZW07CiAgICAgICAgICBwYWRkaW5nLWJvdHRvbTogMC4zNzVlbTsKICAgICAgICAgIHBhZGRpbmctbGVmdDogMC41ZW07CiAgICAgICAgICBwYWRkaW5nLXJpZ2h0OiAwLjVlbTsKICAgICAgICAgIG1heC13aWR0aDogNDUlOwogICAgICAgICAgY29sb3I6IHJnYigxMDcsIDExNCwgMTI4KTsKICAgICAgICAgIGZvbnQtc2l6ZTogMS4xZW07CiAgICAgICAgICBvdmVyZmxvdy13cmFwOiBicmVhay13b3JkOwogICAgICAgICAgZmxleC1zaHJpbms6IDA7CiAgICAgICAgICBib3JkZXI6IDA7CiAgICAgICAgIgogICAgICAgIGRhdGEtZ3MtZWRpdC1yZWZlcmVuY2U9ImN0YSIKICAgICAgPgogICAgICAgIExlYXJuIG1vcmUKICAgICAgPC9idXR0b24+CiAgICA8L2Rpdj4KICA8L2Rpdj4KPC9kaXY+CjwvZGl2Pgo8L2JvZHk+CjwvaHRtbD4K"
        }
    ]
}
```
