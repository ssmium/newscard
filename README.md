# MAGAZINIE 카드뉴스 메이커 - 실제 네이버 뉴스 검색 연결 버전

이 프로젝트는 단일 HTML 목업이 아니라 Vercel 서버리스 API를 포함한 버전입니다.

## 왜 HTML 파일만으로 실제 검색이 안 되나요?

네이버 뉴스 검색 API는 `X-Naver-Client-Id`, `X-Naver-Client-Secret` 헤더가 필요합니다.
Client Secret을 HTML/JS에 직접 넣으면 브라우저 개발자도구에서 바로 노출되므로 서버에서만 호출해야 합니다.

## 배포 방법

1. 네이버 개발자센터에서 애플리케이션을 만들고 `검색` API를 활성화합니다.
2. Client ID / Client Secret을 발급받습니다.
3. 이 폴더를 GitHub에 올립니다.
4. Vercel에서 Import Project 합니다.
5. Vercel > Project Settings > Environment Variables에 아래 값을 넣습니다.

```txt
NAVER_CLIENT_ID=네이버에서 받은 Client ID
NAVER_CLIENT_SECRET=네이버에서 받은 Client Secret
```

6. 다시 Deploy 합니다.
7. 배포된 주소에서 `뷰티 검색`, `패션 검색`을 누르면 실제 네이버 뉴스 검색 결과가 표시됩니다.

## 로컬 테스트

Vercel CLI가 있다면:

```bash
npm i -g vercel
vercel dev
```

그 다음 표시되는 localhost 주소로 접속하세요.
`index.html`을 더블클릭으로 열면 `/api/search`가 없어서 실제 검색은 동작하지 않습니다.
