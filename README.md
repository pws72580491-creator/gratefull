# 🌿 Grateful — 감사노트

매일 감사한 것을 기록하는 감성 PWA 앱

## 배포 방법 (GitHub Pages)

1. 이 폴더의 모든 파일을 GitHub 저장소에 올리기
2. `Settings → Pages → Source: main branch / root` 설정
3. 배포 완료 후 `https://<username>.github.io/<repo>/` 접속
4. Chrome/Safari에서 **"홈 화면에 추가"** → 앱 설치 완료

## 파일 구조

```
/
├── index.html          # 메인 HTML
├── app.css             # 스타일시트
├── app.js              # 앱 로직
├── firebase-init.js    # Firebase 설정 + 초기화
├── sw.js               # 서비스 워커 (오프라인 + 알림)
├── manifest.json       # PWA 메타정보
├── apple-touch-icon.png
├── favicon.png
└── icons/              # PWA 아이콘 모음
    ├── icon-192x192.png
    └── icon-512x512.png
    └── ...
```

## 기능

- ✦ 매일 감사 노트 기록 (최대 5가지)
- 🙏 기도노트 (기도 중 / 응답받음)
- 📅 챌린지 (7일 → 21일 → 30일)
- 🌿 그룹 피드 공유 (Firebase)
- 🔔 매일 리마인더 알림 (Service Worker)
- 🎨 테마 / 폰트 / 배경 패턴 커스터마이징
- ☁️ Firebase 클라우드 동기화
