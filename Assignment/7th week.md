# 7th Study Week

## Study Schedule
<br>

| 회차 | 강의 범위   | 강의 이수 여부 | 링크                                                                                                     |
|------|-------------|----------------|--------------------------------------------------------------------------------------------------------|
| 1    | 1~7강       | ✅              | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=84)    |
| 2    | 8~17강      | ✅              | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=75)    |
| 3    | 18~27강     | ✅              | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=65)    |
| 4    | 28~37강     | ✅              | [링크](https://www.youtube.com/watch?v=e6J0Ljd6h44&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=55)    |
| 5    | 38~47강     | ✅              | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=45)    |
| 6    | 48~57강     | ✅              | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=35)    |
| 7    | 58~66강     | ✅             | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=25)    |
| 8    | 67~77강     | 🍽️             | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=15)    |
| 9    | 78~85강     | 🍽️             | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=5)     |
---

<br/>

> **🧞‍♀️ 오늘은 강의보다 실습과 대시보드 직접 만들기가 더 중요하니, 기록보다는 사고하며 강의를 들어주세요.**
> **직접 실습파일을 다운로드하는 번거로움이 있어 assignment > 7th_files에 실습파일을 올려두었습니다. 활용해주세요!**


## 58. 집합값 변경

<!-- 집합값 변경 강의에서 알게 된 점을 적어주세요 -->
- 집합값 변경: 만들어진 집합에 포함되는 필드를 변경<br>
기능을 추가하기 이전에 제품 막대그래프에 있는 집합을 확인
### 제품과 수익 대시보드 만들기
```
# 제조 업체
IF [하위 범주 집합] THEN [제조업체]
ELSE '+'
END
- 하위 점주 집합에 있는 업체인 경우에만 제조업체를 표시

# 제품
IF [하위 범주 집합] AND [제조 업체 집합] THEN [제품 이름]
ELSE '+'
END
- 제품의 하위 범주와 제조 업체가 모두 집합 내에 있는 경우에만 제품 이름을 표시
```
![img](/image/6th_week_image/58_1.png)
```
빈 대시보드에 순서대로 세로 컨테이너, 빈 페이지, 제품 막대그래프 배치
```
```
선택한 제품 하위 범주에서 제조 업체를 보여주게 만드는 집합 값 변경 동작 만들기
- 대시보드>동작>동작 추가>집합 값 변경
```
![img](/image/6th_week_image/58_2.png)
```
하위 범주를 선택하면 하위 범주 집합의 유일한 값으로 설정하며 선택을 취소하면 해당 집합에서 모든 값이 제거된다.
```
![img](/image/6th_week_image/58_3.png)
```
제조 업체를 선택하면 하위 범주 집합의 유일한 값으로 설정하며 선택을 취소하면 해당 집합에서 모든 값이 제거된다.
```
![img]()
<div style="display: flex;">
  <img src="/image/6th_week_image/58_4.png" alt="이미지 1" style="margin-right: 10px;">
  <img src="/image/6th_week_image/58_5.png" alt="이미지 2">
</div>
```
하위 범주에서 의자를 선택하면 의자의 제조 업체들이, 제조 업체 중 'Harbour Creations'를 선택하면 회사의 제품들이 뜨는 것을 볼 수 있다.
```

### 수익성 대시보드와 매출과 수익 대시보드 연결하기
- 대시보드>동작>동작 추가>시트로 이동
![img](/image/6th_week_image/58_6.png)
- 탐색 버튼을 이용해 수익성 대시보드로 돌아가기
![img](/image/6th_week_image/58_7.png)
```
완성
```
![img](/image/6th_week_image/58_8.png)


## 59강. 스토리패널

<!-- 스토리패널 강의에서 알게 된 점을 적어주세요 -->
### 스토리패널로 스토리텔링 구현
- 시트, 대시보드 만드는 곳 옆에 책 모양 아이콘으로 스토리 생성
![img](/image/6th_week_image/59_1.png)
왼쪽의 스토리 패널과 오른쪽의 스토리 워크시트 페이지로 구성
- 스토리 워크시트 안에 시트를 추가하며 스토리 포인트 생성
- 스토리 포인트:  스토리 각각의 개별 시트
  - 빈 페이지/복제로 다음 스토리 포인트를 생성
- 스토리 패널: 대시보드, 시트 및 텍스트 설명을 스토리 시트로 가져올 수 있다. + 크기, 제목 표시 여부도 조절 가능
- 스토리 탐색기&툴 바
![img](/image/6th_week_image/59_2.png)
삭제, 되돌리기, 업데이트 적용, 생성이 가능하다.
  - 스토리 포인트에서 시트 혹은 대시보드의 동작 등의 작업을 진행한 뒤, 현재까지의 작업을 시작지점으로 지정하여 작업을 진행할 수 있다.
  - 스토리 탐색기에서 스토리 포인트 편집&구성, 탐색기를 이용해서 스토리 단계 이동 가능

## 60. 스토리
### 스토리
- 생성한 워크시트와 대시보드에 설명을 덧붙여 데이터를 설명하거나 정보를 전달.
<!-- 알게 된 점을 적고, 아래 질문에 답해보세요 :) -->

## 61. 대시보드 탐색

<!-- 대시보드 탐색 강의에서 알게 된 점을 적어주세요 -->
![img](/image/6th_week_image/61_1.png)
```
각 대시보드와 탐색 버튼 생성
```
![img]()
<div style="display: flex;">
  <img src="/image/6th_week_image/62_2.png" alt="이미지 1" style="margin-right: 10px;">
  <img src="/image/6th_week_image/62_3.png" alt="이미지 2">
</div>
```
탐색 버튼 활성화
```
![img](/image/6th_week_image/61_4.png)
```
자유롭게 대시보드 이동 가능
```

## 62. 태블로 단추

<!-- 태블로 단추 강의에서 알게 된 점을 적어주세요 -->
시트 우클릭>표시/숨기기 단추 추가: Alt 키와 단추를 같이 누르면 표시/숨기기 변환
![img](/image/6th_week_image/62_1.png)
```
각 그래프 별 표시/숨기기 단추 추가
```
![img](/image/6th_week_image/62_2.png)
```
편집 단추를 통해 표시/숨기기 별 이미지 설정
```
![img](/image/6th_week_image/62_3.png)
```
표시/숨기기 단추를 통해 표시할 그래프 설정 가능
```
![img](/image/6th_week_image/62_4.png)
```
컨테이너에 표시/숨기기 단추 적용
```

## 63. 막대그래프 드릴다운

<!-- 막대그래프 드릴다운에 대해 알게 된 점을 적어주세요 -->

### [배송 형태]-[범주]-[하위 범주] 순서로 이어지는 막대 그래프 생성
#### [배송형태]-[범주] 드릴다운 생성
![img](/image/6th_week_image/63_1.png)
```
배송형태별 매출 막대 그래프 생성
```
![img](/image/6th_week_image/63_2.png)
```
매개 변수 Level 1 생성
```
```
# 계산된 필드 생성
IF [배송 형태] = [매개 변수 Level 1]
THEN [범주]
ELSE [배송 형태]
END
```
![img](/image/6th_week_image/63_3.png)
```
매개 변수 동작을 편집하여 배송 형태를 선택하면 범주로 드릴다운이 되는 동작 생성
```
![img](/image/6th_week_image/63_4.png)
```
매출별로 내림차순 정렬
```
![img]()
<div style="display: flex;">
  <img src="/image/6th_week_image/63_5.png" alt="이미지 1" style="margin-right: 10px;">
  <img src="/image/6th_week_image/63_6.png" alt="이미지 2">
</div>

#### [배송형태]-[범주]-[하위 범주] 드릴다운 생성
![img](/image/6th_week_image/63_7.png)
```
매개 변수 Level 2 생성
```
```
# 계산된 필드 생성
IF [드릴다운 1] = [매개 변수 Level 2]
THEN [하위 범주]
ELSE ''
END
```
![img](/image/6th_week_image/63_8.png)
```
매개 변수 동작을 편집하여 배송 형태를 선택하면 범주로 드릴다운이 되는 동작 생성
```
![img](/image/6th_week_image/63_10.png)
```
매출별로 내림차순 정렬
```

#### 막대그래프의 레이블이 중복되는 것을 방지하는 계산된 필드 생성
```
# 드릴다운 1 레이블
IF [배송 형태] = [매개 변수 Level 1]
THEN [범주]
ELSE ''
END
```
![img](/image/6th_week_image/63_9.png)

## 64. 트리맵 드릴다운

<!-- 트리맵 드릴다운에 대해 알게 된 점을 적어주세요 -->
### [Category]-[Sub_Category]-[Manufacturer] 순서로 이어지는 트리맵 생성
#### [Category]-[Sub_Category] 드릴다운 생성
![img](/image/6th_week_image/64_1.png)
```
카테고리별 매출 트리맵 생성
```
![img](/image/6th_week_image/64_2.png)
```
카테고리 집합 생성
```
```
# 계산된 필드(드릴다운 1) 생성: IF 문을 활용하여 [Category 집합]일 경우 [Sub-category]로 드릴다운되고 그렇지 않을 경우 [Category]가 되는 함수 생성

IF [Category 집합] THEN [Sub-Category]
ELSE [Category]
END
```
![img](/image/6th_week_image/64_3.png)
```
집합 동작을 편집하여 [Category]를 선택하면 [Sub-Category]로 드릴다운이 되는 동작 생성
```
마크>레이블에 [드릴다운 1] 드래그&드롭
![img](/image/6th_week_image/64_4.png)

#### [Category]-[Sub_Category]-[Manufacturer] 드릴다운 생성
![img](/image/6th_week_image/64_5.png)
```
드릴다운 1에서 집합 생성
```
```
# 계산된 필드(드릴다운 2) 생성: IF 문을 활용하여 [드릴다운 1 집합]일 경우 [Manufacturer]로 드릴다운되고 그렇지 않을 경우 아무것도 출력하지 않는 함수 생성

IF [드릴다운 1 집합] THEN [Manufacturer]
ELSE ""
END
```
![img](/image/6th_week_image/64_6.png)
```
집합 동작을 편집하여 [Sub-Category]를 선택하면 [Manufacturer]로 드릴다운이 되는 동작 생성
```
마크>레이블에 [드릴다운 2] 드래그&드롭
![img](/image/6th_week_image/64_7.png)

#### 트리맵의 레이블이 중복되는 것을 방지하는 계산된 필드 생성
```
# 드릴다운 1 레이블
IF [Category 집합] THEN [Sub-Category]
ELSE ""
END
```
마크>레이블에 [드릴다운 1 레이블] 드래그&드롭
![img](/image/6th_week_image/64_8.png)

## 65. 파이 차트 드릴다운
<!-- 파일 차트 드릴다운에 대해 알게 된 점을 적어주세요 -->
### [Category]-[Sub_Category] 순서로 이어지는 파이차트 생성
![img](/image/6th_week_image/65_1.png)
```
카테고리별 매출 파이차트 생성
```
![img](/image/6th_week_image/65_2.png)
```
카테고리 집합 생성
```
```
# 계산된 필드(드릴다운 1) 생성: IF 문을 활용하여 [Category 집합]일 경우 [Sub_Category]로 드릴다운되고 그렇지 않을 경우 [Category]가 되는 함수 생성

IF [Category 집합] THEN [Sub-Category]
ELSE [Category]
END
```
![img](/image/6th_week_image/65_3.png)
```
집합 동작을 편집하여 [Category]를 선택하면 [Sub_Category]로 드릴다운이 되는 동작 생성
```
마크에서 합계(Sales) 크기 삭제>세부정보에 [드릴다운 1] 드래그&드롭>드릴다운 1을 색상으로 변경
![img]()
<div style="display: flex;">
  <img src="/image/6th_week_image/65_4.png" alt="이미지 1" style="margin-right: 10px;">
  <img src="/image/6th_week_image/65_5.png" alt="이미지 2">
</div>
```
카테고리와 드릴다운 1 내림차순 정렬
```

![img](/image/6th_week_image/65_6.png)
---
![img](/image/6th_week_image/65_7.png)
```
행 선반 더블클릭하여 임의의 축 생성 -> Ctrl 키 이용하여 하나 더 생성

마크에서 드릴다운 1 색상 제거 후 크기 조정
```
![img](/image/6th_week_image/65_8.png)
```
이중 축 생성
```
```
# 계산된 필드(드릴다운 1 레이블) 생성
IF [Category 집합] THEN [Sub_Category]
ELSE ""
END
```
두 번째 축의 마크>레이블에 [드릴다운 1 레이블] 드래그&드롭 <br>
행 구분선/열 구분선/0 기준선/격자선 없음 처리, 머리글 해제
![img](/image/6th_week_image/65_9.png)

## 66. 지도 드릴다운
<!-- 지도 드릴다운에 대해 알게 된 점을 적어주세요 -->
### [국가/지역]-[시/도] 순서로 이어지는 지도 그래프 생성
![img](/image/6th_week_image/65_1.png)
```
국가/지역 맵 생성
```
![img](/image/6th_week_image/65_2.png)
```
국가/지역 집합 생성
```
```
# 계산된 필드(드릴다운 1) 생성: IF 문을 활용하여 [국가/지역 집합]일 경우 [시/도]로 드릴다운되고 그렇지 않을 경우 [국가/지역]이 되는 함수 생성

IF [국가/지역 집합] THEN [시/도]
ELSE [국가/지역]
END

*계산된 필드에 [지리적 역할]>[만들기 원본]>[시/도]로 지리적 역할 부여
```
![img](/image/6th_week_image/65_3.png)
```
집합 동작을 편집하여 [국가/지역]을 선택하면 [시/도]로 드릴다운이 되는 동작 생성
```
마크>색상에 [드릴다운 1] 드래그&드롭
![img]()
<div style="display: flex;">
  <img src="/image/6th_week_image/66_4.png" alt="이미지 1" style="margin-right: 10px;">
  <img src="/image/6th_week_image/66_5.png" alt="이미지 2">
</div>
```
국가별로 색상이 구분된 것과, 국가 클릭시 시/도 별로 드릴다운이 되는 것을 확인할 수 있다.
```

### 매개변수를 이용하여 드릴다운과 선택한 [국가/지역]만 필터링 되는 작업을 동시에 진행
![img](/image/6th_week_image/66_6.png)
```
매개변수 생성
```
```
# 계산된 필드(선택된 국가/지역) 생성: IF/ELSE 문을 사용해서 [국가/지역]과 [매개 변수 국가/지역]이 일치할 경우와 [매개 변수 국가/지역]이'ALL'값일 경우에 TRUE를 출력하고, 그 이외의 경우에는 FALSE를 출력

IF [매개 변수 국가/지역] = [국가/지역] THEN TRUE
ELSEIF [매개 변수 국가/지역] = 'All' THEN TRUE
ELSE FALSE
END
```
```
매개변수 표시 이후, 매개변수 국가/지역>ALL 로 설정
```
![img](/image/6th_week_image/66_7.png)
```
선택된 국가/지역 필드로 필터 생성>참 선택
```
![img](/image/6th_week_image/66_8.png)
```
계산된 필드를 실행하는데 필요한 동작 생성
```
![img](/image/6th_week_image/66_9.png)
```
도구 설명 편집: 국가/지역 삭제
```
![img]()
<div style="display: flex;">
  <img src="/image/6th_week_image/66_10.png" alt="이미지 1" style="margin-right: 10px;">
  <img src="/image/6th_week_image/66_11.png" alt="이미지 2">
</div>
```
드롭다운을 실시할 때, 선택된 도시만 확대해서 필터링 됨과 동시에 드릴다운이 진행되며, 도구설명도 국가/지역에서 시/도로 변경되는 것을 확인
```
## 문제

오늘은 별도의 문제가 없습니다.

다만, 학술제 이후 마지막 과제(11/27~)로서 한 주 동안에는 학술제 주제 관련 데이터(없을 경우, 본인 관심 데이터)를 사용해 나만의 대시보드를 제작할 예정입니다. 또한, 학술제에서 시각화 시 태블로를 사용하기를 권장하는 안내가 나갈 예정입니다.
그 때 열심히 배운 내용을 잘 활용해주세요. 감사합니다 :)
