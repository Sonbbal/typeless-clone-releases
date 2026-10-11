# TypelessMVP releases

이 저장소는 TypelessMVP(macOS Apple Silicon 한국어 받아쓰기 앱)의 **빌드 산출물만** 게시합니다.
앱의 소스 코드는 여기에 없습니다.

## 릴리즈마다 올라가는 파일

- `TypelessMVP-<버전>-mac-arm64.zip` — 서명된 앱 번들(`TypelessMVP.app`) 하나
- `latest.json` — 버전·zip 주소·sha256·크기·ed25519 서명·릴리즈 노트 주소·게시 시각

태그에 `-` 가 들어간 버전(예: `v0.1.0-rc.1`)은 prerelease 로 게시되고, 앱의 자동 확인 대상이 아닙니다.

## 앱이 확인하는 주소

```
https://github.com/Sonbbal/typeless-clone-releases/releases/latest/download/latest.json
```

앱은 이 파일의 서명을 앱에 내장된 공개키로 확인한 뒤에만 업데이트를 설치합니다.

## 만드는 방법

`v*` 태그가 이 저장소에 push 되면 `.github/workflows/release.yml` 이 같은 태그의 소스를 받아 빌드·서명·점검한 뒤
위 두 파일로 같은 이름의 릴리즈를 만듭니다. 같은 태그의 릴리즈가 이미 있으면 아무것도 하지 않습니다.
