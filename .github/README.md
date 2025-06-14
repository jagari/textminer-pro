# GitHub Pages 설정

이 디렉토리는 GitHub Pages 자동 배포를 위한 설정 파일들을 포함합니다.

## 설정된 워크플로우

1. **docs.yml** - MkDocs 문서 자동 빌드 및 GitHub Pages 배포
2. **release.yml** - 태그 생성 시 자동 GitHub Release 생성
3. **docs-update.yml** - 코드 변경 시 문서 자동 업데이트
4. **pypi.yml** - PyPI 자동 배포 (개선됨)

## GitHub Pages 활성화 방법

1. GitHub 저장소 → Settings → Pages
2. Source를 "GitHub Actions"로 설정
3. 메인 브랜치에 푸시하면 자동으로 문서가 배포됩니다

## 필요한 Secrets 설정

다음 Secrets을 GitHub 저장소에 설정해야 합니다:

- `PYPI_API_TOKEN`: PyPI API 토큰
- `TEST_PYPI_API_TOKEN`: Test PyPI API 토큰 (선택사항)
