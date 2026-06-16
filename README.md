# MAGAZINIE AI 카드뉴스 메이커 - Gemini 내장키 버전

회사 보안 프로그램 때문에 `.env.local` 또는 Vercel Environment Variables 업로드가 어려운 상황을 고려해, 개인 사용용으로 API 키를 서버 함수 파일 안에 넣은 버전입니다.

## 실행

```bash
npm install
npm run dev
```

## 배포

Vercel에 그대로 업로드하면 됩니다. 별도 API 입력 화면은 없습니다.

## 주의

- 이 버전은 개인 사용용입니다.
- 공개 GitHub 저장소에 올리지 마세요.
- 배포 URL을 외부에 공유하면 서버 함수가 호출될 수 있습니다.
- 키가 노출됐다고 판단되면 Google AI Studio와 네이버 개발자센터에서 새 키로 재발급하세요.

## 구성

```text
index.html
api/search-news.js
api/generate-cardnews.js
package.json
vercel.json
README.md
```
