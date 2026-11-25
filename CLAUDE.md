# RawfiRoom 작업 규칙

- 저장소: https://github.com/rawfi-rgb/RawfiRoom (공개, 계정 `rawfi-rgb`). 푸시 전에 `gh auth status`로 활성 계정이 `rawfi-rgb`인지 확인한다 (`gh auth switch -u rawfi-rgb`).
- **모든 작업은 끝나면 자동으로 커밋하고 `main`에 푸시한다** (사용자가 매번 요청하지 않아도 됨). 푸시 후 `gh run list --limit 1`로 GitHub Actions `build` 성공을 확인하고 결과를 알린다.
- 배포: Render가 `render.yaml`로 `main` 푸시마다 자동 배포한다. GitHub Pages는 WebSocket 서버를 못 돌리므로 쓰지 않는다.
- 공개 저장소이므로 `data/`(방 키·업로드·녹화), `.env`, 토큰은 절대 커밋하지 않는다.
- 폴더는 iCloud Drive에 있다. `node_modules`는 `node_modules.nosync`로 가는 심볼릭 링크(iCloud 동기화 제외)이니 지우거나 실제 폴더로 바꾸지 않는다.
- 디자인: 시그니처 컬러는 레드(`--accent: #ff3b4e`). 새 UI에도 레드 포인트를 적용한다.
- 로컬 실행: `npm start` → http://localhost:8787 (미리보기 설정은 `.claude/launch.json`).
