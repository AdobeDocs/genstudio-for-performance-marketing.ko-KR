---
title: App Builder 앱 배포
description: GenStudio for Performance Marketing용 App Builder 앱 또는 추가 기능을 배포합니다.
feature: Extensibility
exl-id: 51888ab7-7772-4ac8-838d-26db3019e9b0
source-git-commit: 6fef5933421a56cf9f77c19bc198f017ee6c117e
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---

# 앱 배포

앱을 실행하면 추가 기능을 배포하기 전에 추가 기능 동작에 대한 사전 스냅숏이 제공됩니다. 이 정보는 디버깅을 용이하게 할 수 있습니다. 승인을 위해 앱을 다시 제출하지 않고 배포된 앱을 강제로 빌드 및 배포할 수 있습니다.

**앱을 실행하려면**:

`https://localhost:9080`에서 앱 실행:

```bash
aio app run
```

**앱을 배포하려면**:

1. 배포 작업 영역으로 이동합니다. 예를 들어 프로덕션 작업 공간으로 이동하려면 다음을 수행합니다.

   ```bash
   aio app use -w Production
   ```

1. 앱 배포:

   ```bash
   aio app deploy
   ```

**다시 배포하려면**:

>[!NOTE]
>
>빌드 및 배포를 강제로 수행하면 기존 배포가 덮어쓰기됩니다. 먼저 테스트 환경에서 앱을 철저히 테스트합니다.

```bash
aio app build --force-build
```

```bash
aio app deploy --force-deploy
```

**동시에 빌드하고 배포하려면**:

```bash
aio app deploy --force-build --force-deploy
```

**앱을 보려면**:

배포 후 GenStudio for Performance Marketing URL에 `query` 매개 변수를 추가하여 GenStudio for Performance Marketing에서 앱을 볼 수 있습니다.

`https://experience.adobe.com/?ext=https://<my-deployed-add-on>.adobeio-static.net/index.html#/@<ims-org>/genstudio/create`

추가 기능이 만족스러우면 `query` 매개 변수 없이 배포할 준비가 되었습니다.

이제 [앱을 배포](distribute-app.md)할 수 있습니다.
