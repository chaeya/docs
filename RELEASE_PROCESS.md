# Release Process

This document outlines the steps involved in the release process for the Wallet core SDK project.

## Versioning

The project follows the format `X.Y.Z` for versioning.

X (Major): In case of incompatibility with lower versions  
Y (Minor): When new features are added while being compatible with lower versions  
Z (Patch): Bug fixes and small changes while compatible with lower versions

> When the major version is changed, minor and patch are initialized to 0.  
  When the minor version is changed, the patch is initialized to 0.


## Releasing a New Version

1. Create an issue to define and track release-related activities. Choose a title that follows the
   format `X.Y.Z`.
2. Stop merging any new work into the main branch.
3. Check the release draft under the [CHANGE LOG](CHANGELOG.md) page to ensure that everything is in order.
4. Create and push the release tag in the format `X.Y.Z`:

    ```bash
    git tag -a vX.Y.Z -m "Release vX.Y.Z"
    git push origin vX.Y.Z
    ```

    As a result, the CI/CD pipeline will publish the release.



---

# Release Process

OmniOne 프로젝트는 명확한 릴리스 절차를 따릅니다.

## 버전 관리
- **X.Y.Z** 형식으로 버전을 관리합니다:
  - **X**: 주요 변경 사항 (하위 호환성 없음).
  - **Y**: 새로운 기능 추가 (하위 호환성 유지).
  - **Z**: 버그 수정 및 소규모 변경.

## 릴리스 절차
1. 릴리스 이슈 생성.
2. 새로운 코드 병합 중지.
3. CHANGELOG 검토 후 릴리스 준비.
4. 릴리스 태그 생성:
    ```bash
    git tag -a vX.Y.Z -m "Release vX.Y.Z"
    git push origin vX.Y.Z
    ```
5. CI/CD 파이프라인을 통해 릴리스 진행.
