# 여행지 체감물가 계산기 Beta 1.0

## 포함 기능
- 출발통화 선택 및 JPY 환율 자동 조회 (Frankfurter v2)
- 일본 5개 도시: 기타큐슈, 후쿠오카, 오사카, 도쿄, 삿포로
- 우동/라멘/햄버거/생맥주/초밥/타코야키/커피/기념품 대표 가격 범위
- 전철·버스 거리별 대표 요금 범위
- 도시별 거리운임 기반 택시 비용 개략 계산
- 여행일수/인원/소비스타일/교통/쇼핑/숙박을 포함한 전체 여행예산 계산
- 모바일 반응형
- API 실패 시 수동 환율 입력

## 티스토리에 넣는 권장 방법
1. 이 폴더의 `index.html`을 GitHub 저장소에 업로드합니다.
2. GitHub Pages를 활성화합니다.
3. 생성된 Pages 주소를 티스토리 HTML 모드의 iframe src에 넣습니다.

예시:

```html
<iframe
  src="https://YOUR-ID.github.io/YOUR-REPO/"
  width="100%"
  height="1700"
  style="border:0; border-radius:16px; overflow:hidden;"
  loading="lazy">
</iframe>
```

## 데이터 수정
`index.html` 내부 JavaScript의 `CITIES` 객체만 수정하면 도시별 음식/교통/택시 데이터를 바꿀 수 있습니다.

## 주의
음식·대중교통 데이터는 Beta용 대표 범위이며 실제 매장/노선/시기와 다를 수 있습니다. 택시는 거리운임 중심의 개략치로, 저속주행·정체·호출료 등이 포함되지 않습니다.
