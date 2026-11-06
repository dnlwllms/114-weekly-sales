# 주간분양 (114-weekly-sales)

매주 분양 카드뉴스 페이지. `main`에 푸시하면 GitHub Pages(https://dnlwllms.github.io/114-weekly-sales/)로 배포된다.

## 매주 업데이트 시 반드시 유지: GTM 스크립트

`index.html`의 `<head>` 안, `<meta charset="utf-8">` 바로 아래에 아래 스크립트가 있어야 한다.
내용을 고치든 `index.html`을 새로 만들어 통째로 덮어쓰든, 이 블록은 빠지면 안 된다.

```html
<script async src="https://www.googletagmanager.com/gtm.js?id=GTM-MPMHDCW3"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
</script>
```

- GTM 컨테이너 `GTM-MPMHDCW3`가 GA4 속성 `G-JCXQDVF0XZ`로 데이터를 보낸다.
- 커밋 전에 `grep -c "GTM-MPMHDCW3" index.html` 결과가 1인지 확인한다.
