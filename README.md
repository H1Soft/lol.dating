# 롤개팅 랜딩 페이지

Claude Design 프로젝트(`롤개팅 랜딩.dc.html`)를 그대로 가져온 정적 사이트입니다.

## 구성

- `index.html` — 페이지 본문 (디자인 원본과 동일한 dc 템플릿 + 인터랙션 스크립트)
- `support.js` — dc 런타임. 페이지 로드 시 React 18 / Babel을 unpkg CDN에서 불러와 템플릿을 렌더링합니다.

빌드 과정 없음. 두 파일을 같은 폴더에 두고 정적 서버로 서빙하면 끝입니다.
(`file://`로 직접 열면 CDN/폰트 로드가 막힐 수 있으니 HTTP로 서빙하세요.)

## 로컬 미리보기

```sh
python3 -m http.server 8000
# http://localhost:8000
```

## 호스팅

정적 호스팅이면 어디든 됩니다.

- **Netlify**: https://app.netlify.com/drop 에 이 폴더를 드래그 앤 드롭
- **Vercel**: `npx vercel` 실행 (이 폴더에서)
- **GitHub Pages**: 저장소에 push 후 Settings → Pages → 브랜치 선택
- **Cloudflare Pages**: 대시보드에서 폴더 업로드

인터넷 연결이 필요합니다 — 폰트(Pretendard, Chakra Petch, Galmuri)와 React/Babel을 CDN에서 로드합니다.
