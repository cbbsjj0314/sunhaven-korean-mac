# Sun Haven 한국어 패치 macOS 포트

**공대 남편** 님의 Sun Haven 비공식 한국어 패치를 macOS에서 사용할 수 있도록 포팅하고 있습니다.

## 현재 상태

- 원본 한국어 패치 v1.2 기본 번역의 macOS 포트 검증을 완료했습니다.
- 첫 macOS 설치 프로그램 **0.1.0 build 2**의 공개를 준비하고 있습니다.
- 대상 환경은 **Apple Silicon arm64 Mac, macOS 13.0 이상**입니다. Intel Mac은 지원하지 않습니다.
- `SunHaven.Core.dll`을 사용하는 추가 한글화는 현재 지원하지 않습니다.

## 원본 한국어 번역 및 출처

- 원본 한국어 번역 및 Windows 한국어 패치: **공대 남편** 님
- 원본 패치 페이지: [Sun Haven 한글 패치](https://hio0606.tistory.com/219)

이 macOS 포트는 공대 남편 님의 한국어 패치를 기반으로 합니다. macOS 포트의 제작·배포는 [원본 패치 페이지 댓글](https://hio0606.tistory.com/219#comment29516229)에서 출처 표기를 조건으로 허락받았습니다.

## 호환성

현재 macOS에서 검증이 완료된 기준 버전은 **원본 한국어 패치 v1.2의 기본 번역**입니다. 이는 원본 패치의 최신 버전을 의미하는 것은 아닙니다. 향후 Sun Haven이나 원본 한국어 패치가 업데이트되면, macOS용 패치도 이에 맞춰 업데이트가 필요할 수 있습니다.

이 설치 프로그램의 번역 범위도 v1.2 기본 번역으로 한정됩니다. 최신 게임이나 원본 패치 업데이트에 대한 호환성을 보장하지 않습니다. 자세한 공개 호환성 정보는 [`compatibility/upstream-v1.2.json`](compatibility/upstream-v1.2.json)에서 확인할 수 있습니다.

## 다운로드 및 실행

공개 후 [GitHub Releases](https://github.com/cbbsjj0314/sunhaven-korean-mac/releases)의 `installer-v0.1.0-build.2`에서 다음 세 Release assets를 같은 directory에 다운로드하십시오.

- `Sun-Haven-Korean-Patch-Installer-0.1.0-build.2-macos-arm64.zip`
- `release-manifest.json`
- `SHA256SUMS`

GitHub가 자동 생성하는 **Source code (zip)** 및 **Source code (tar.gz)** archives는 설치 프로그램이 아닙니다.

Terminal에서 다운로드한 세 파일이 있는 directory로 이동한 뒤 checksum을 확인하십시오.

```sh
shasum -a 256 -c SHA256SUMS
```

ZIP과 `release-manifest.json` 모두 `OK`인지 확인하십시오. 검증에 실패하면 실행하지 마십시오. ZIP은 3,593,140 bytes이며 SHA-256은 다음과 같습니다.

```text
4bd0031ba3fdce4b4d8e15cbd5f2e38a1e6ec8ab4cff6d55ca23f3cdcda8953f
```

Checksum은 파일 bytes의 동일성을 확인하며 publisher의 신원을 보증하지 않습니다.

이 app에는 **Developer ID distribution signature와 Apple notarization이 없습니다**. Publisher를 신뢰하는 경우에만 다운로드하여 실행하십시오.

ZIP을 풀고 `Sun Haven Korean Patch Installer.app`을 Finder에서 여십시오. 개발자를 확인할 수 없거나 notarization이 없어 Gatekeeper가 최초 실행을 차단할 수 있습니다. 신뢰하는 app임을 확인했다면 **System Settings → Privacy & Security → Open Anyway**를 선택하고 필요한 인증 후 **Open**으로 확인하십시오. [Apple의 Open Anyway 안내](https://support.apple.com/102445)를 참고하십시오. 경고 문구와 버튼은 macOS version에 따라 다를 수 있습니다. 악성 소프트웨어 또는 손상 경고는 일반적인 개발자 확인 경고와 다르므로 이 절차로 우회하지 마십시오.

## 권리 및 범위

Sun Haven에 관한 권리는 해당 게임 개발사와 권리자에게 있습니다. 원본 한국어 번역의 출처는 공대 남편 님이며, 이 저장소는 해당 비공식 한국어 패치의 macOS 포트 프로젝트입니다. 이 저장소는 번역이나 게임 콘텐츠에 대한 포괄적인 재라이선스를 주장하지 않습니다.