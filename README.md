# Kyle's Travel Cost Calculator v1.1

모바일 대응 및 Tistory iframe 자동 높이 조절 기능을 추가한 버전입니다.

## GitHub 업데이트
기존 repository의 루트에 있는 `index.html`을 이 버전의 `index.html`로 교체하세요.

## Tistory 권장 삽입 코드

```html
<div style="width:100%; margin:24px 0;">
  <iframe
    id="kddTravelCalculator"
    src="https://capstonedrone.github.io/travel-cost-calculator/"
    title="여행지 체감물가 계산기"
    width="100%"
    height="1800"
    frameborder="0"
    scrolling="no"
    loading="lazy"
    style="display:block;width:100%;max-width:100%;border:0;overflow:hidden;">
  </iframe>
</div>
<script>
(function(){
  var frame = document.getElementById('kddTravelCalculator');
  if (!frame) return;
  window.addEventListener('message', function(e){
    if (e.origin !== 'https://capstonedrone.github.io') return;
    if (!e.data || e.data.type !== 'kdd-travel-calculator-resize') return;
    var h = Number(e.data.height);
    if (!Number.isFinite(h)) return;
    frame.style.height = Math.max(700, Math.min(6000, h + 8)) + 'px';
  });
})();
</script>
```

Tistory 본문에서 script가 제거되는 경우에는 iframe만 유지하고 CSS 미디어쿼리로 모바일 높이를 넉넉히 주거나, 리스너 스크립트를 스킨 HTML에 한 번 추가하세요.


## v1.2 변경점
- Tistory iframe 자동 높이 계산을 문서 scrollHeight가 아닌 `.wrap` 실제 콘텐츠 높이 기준으로 수정했습니다.
- 큰 초기 iframe 높이에서 하단 빈 공간이 남는 문제를 해결합니다.
