# 🌿 Grateful — 감사노트 PWA

매일 감사한 것을 기록하는 감성 노트 앱

## 파일 구조

```
grateful-pwa/
├── index.html          # 메인 HTML
├── app.css             # 전체 스타일
├── app.js              # 앱 로직 (메인 JavaScript)
├── firebase-init.js    # Firebase 설정 및 초기화
├── sw.js               # 서비스 워커 (오프라인 캐시, 알림)
├── manifest.json       # PWA 매니페스트
├── icons/
│   ├── icon-192x192.png
│   └── icon-512x512.png
├── favicon.png
└── apple-touch-icon.png
```

## GitHub Pages 배포 방법

1. 이 폴더 전체를 GitHub 저장소에 push
2. Settings → Pages → Branch: `main`, Folder: `/ (root)` 선택 → Save
3. `https://{username}.github.io/{repo}/` 로 접속
4. 브라우저에서 "홈 화면에 추가" 또는 주소창 설치 아이콘으로 PWA 설치

## 아이콘 파일 추가 필요

`icons/icon-192x192.png`, `icons/icon-512x512.png`, `favicon.png`, `apple-touch-icon.png`  
파일이 없으면 PWA 설치 시 기본 아이콘이 사용됩니다.  
(기존 아이콘 파일이 있다면 그대로 복사하세요)

## Firebase 규칙

Firebase Console → Realtime Database → 규칙 탭:

```json
{
  "rules": {
    "grateful-users": {
      "$uid": {
        ".read": true,
        ".write": true
      }
    },
    "grateful-feed": {
      ".read": true,
      ".write": true
    }
  }
}
```
