---
source-git-commit: 8ed1e6853c9f844c72431dc692b556ece9c215a8
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 0%

---
## 목적

AI 코딩 도우미가 GenStudio for Performance Marketing 설명서 리포지토리를 작고 안전하게 편집할 수 있도록 지원합니다.

## 높은 수준 아키텍처(짧음)- 이 리포지토리는 `help/` 아래의 Markdown으로 구성된 문서 사이트로, `help/_includes/`에 공유 포함 및 `help/_includes/assets/`에 조정된 이미지가 있습니다.- 릴리스 정보, 사용 안내서 및 확장성 콘텐츠가 `help/`에서 라이브로 제공됩니다. 큰 콘텐츠 변경 사항은 프론트맨트와 기존 제목 구조를 유지해야 합니다.- 사이트는 Jekyll을 사용하여 빌드되고 GitHub 페이지에서 호스팅됩니다. 빌드 프로세스는 일부 사용자 지정 플러그인과 함께 표준 Jekyll 규칙을 사용합니다.

## 프로젝트별 규칙- 커서 규칙: 사용자 지정 자동화 및 지침은 `.cursor/rules/*.mdc`에 있습니다. 예: `.cursor/rules/docs-lint.mdc`(lint 프로세스), `.cursor/rules/generate-release-notes.mdc`(릴리스 노트 형식). 자동화된 작업에 대해서는 다음 단계를 따르십시오.- 파일 이름 및 주요 내용:   - 릴리스 노트에는 특정 프론트마크가 필요합니다(`.cursor/rules/generate-release-notes.mdc` 참조).   - 규칙 파일 및 `.mdc` 확장명에 kebab-case를 사용합니다.- 서식 지정 규칙: 문서에서는 GitHub 버전의 Markdown을 사용합니다. 제목은 일반적으로 문장과 짧은 문단을 따릅니다. 릴리스 노트의 목록은 `*`개, 기능 섹션은 `###`개를 선호합니다.

## 설명서 스타일 지침- 기술 설명서 모범 사례를 보려면 [Microsoft 작성 스타일 안내서](https://learn.microsoft.com/en-us/style-guide/)를 따르십시오.   - 사용자 작업에 초점을 맞춘 명확하고 간결한 문장 작성   - 활성 음성 및 현재 시제 사용   - 텍스트를 짧고 훑어볼 수 있는 청크로 나누기   - 기술적인 정확도를 유지하면서 따뜻하고 직접적인 어조 유지- Markdown 작성   - 머리글에 대소문자 구분 사용(첫 번째 단어만 대문자로 변환)   - 가독성을 위해 단락을 짧게 유지(2~3문장)   - 제목 및 목록 앞과 뒤에 빈 줄 추가   - UI 요소, 파일 경로 및 코드에 대해 백틱 사용   - 모든 이미지에 대체 텍스트 포함   - 설명 텍스트를 사용하여 특정 섹션에 연결

## 편집 시 안전 규칙(AI가 수행해야 하는 작업)- 공개 문서에 Jira ID, 내부 링크 또는 기업 전용 참조를 추가하지 마십시오. `generate-release-notes.mdc` &quot;문제 추적&quot; 섹션을 참조하십시오.- YAML이 포함된 파일을 편집할 때 YAML을 정확하게 유지하십시오. 많은 템플릿 및 릴리스 노트는 고정 키(제목, 설명, 역할, exl-id)에 의존합니다.- Lint 수정의 경우 `.cursor/rules/docs-lint.mdc`에서 자동화된 idempotent 편집을 선호합니다(후행 공백을 제거하고 최종 새 행을 확인하십시오). 사람이 사용하는 명령 예:

```sh
sed -i '' 's/ $//' <file>
sed -i '' '$ { /^$/d; }' <file> && echo "" >> <file>
```

## 예제(변경 사항 및 방법)- 작은 복사본 수정: `help/` Markdown 파일 내의 텍스트를 업데이트하고, 머리글과 앵커를 그대로 유지합니다.- 이미지 업데이트: `help/_includes/assets/` 아래의 참조 이미지입니다. 모든 참조를 업데이트하지 않고 이미지를 이동하거나 이름을 바꾸지 마십시오.

## 우선 살펴볼 위치- `help/_includes/` — 공유된 조각 및 이미지- `.cursor/rules/` — 자동화 및 린팅 지침입니다. 서식 및 프로세스에 대한 신뢰할 수 있는 규칙으로 사용하십시오.- `markdownlint_custom.json` — 로컬 markdownlint 재정의.- `.github/pull_request_template.md` — PR 예상

## 인간에게 물어봐야 할 때- 변경 사항에 도커 기반 도구 실행 또는 수정이 필요하거나(lint 규칙에서 도커 언급) 사이트 빌드 파이프라인에 영향을 주는 경우입니다.- 파일이 알 수 없는 외부 구성을 참조하는 경우(예: `markdownlint.json`이(가) 누락됨) - 만들지 여부를 묻습니다.

## 인간을 위한 최소한의 명령

```sh
# Install linter (if not present)
npm install -g markdownlint-cli

# Run lint locally using project config
markdownlint --config markdownlint_custom.json "help/**/*.md"

# Project lint via yarn (preferred if available in environment)
yarn lint
```

&#x200B;---
원한다면 리포지토리의 `.github/copilot-instructions.md`에 병합하거나 단어/길이를 조정할 수 있습니다. 무엇을 변경하거나 추가해야 합니까?
