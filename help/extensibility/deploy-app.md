---
title: App Builder 앱 배포
description: GenStudio for Performance Marketing용 App Builder 앱 또는 추가 기능을 배포합니다.
feature: Extensibility
exl-id: 51888ab7-7772-4ac8-838d-26db3019e9b0
source-git-commit: 7fdd3f54a0a031bfe26b48983de9cd24baad2f62
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 0%

---

# 앱 배포

앱을 실행하면 추가 기능을 배포하기 전 동작에 대한 사전 스냅숏이 제공됩니다. 이 정보는 디버깅을 용이하게 할 수 있습니다.

**앱을 실행하려면**:

`https://localhost:9080`에서 앱 실행:

```bash
aio app run
```

**앱을 배포하려면**:

1. 배포 작업 영역으로 이동합니다.

   ```bash
   aio app use -w [deployment_workspace]
   ```

2. 앱 배포:

   ```bash
   aio app deploy
   ```

**다시 배포하려면**:

승인을 위해 다시 제출하지 않고 앱을 강제로 빌드 및 배포할 수 있습니다.

>[!NOTE]
>
>빌드 및 배포를 강제로 적용하면 기존 배포가 덮어쓰기됩니다. 먼저 테스트 환경에서 **앱을 철저히 테스트하세요**.

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

```txt
https://experience.adobe.com/?ext=https://<my-deployed-add-on>.adobeio-static.net/index.html#/@<ims-org>/genstudio/create
```

추가 기능에 만족하면 `query` 매개 변수 없이 배포할 준비가 된 것입니다.

이제 [앱을 배포](distribute-app.md)할 수 있습니다.
