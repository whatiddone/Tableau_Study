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
```
[Category]-[Sub_Category]-[Manufacturer] 순서로 이어지는 트리맵 생성
```
## 65. 파이 차트 드릴다운

<!-- 파일 차트 드릴다운에 대해 알게 된 점을 적어주세요 -->

## 66. 지도 드릴다운

<!-- 지도 드릴다운에 대해 알게 된 점을 적어주세요 -->

---

## 문제

오늘은 별도의 문제가 없습니다.

다만, 학술제 이후 마지막 과제(11/27~)로서 한 주 동안에는 학술제 주제 관련 데이터(없을 경우, 본인 관심 데이터)를 사용해 나만의 대시보드를 제작할 예정입니다. 또한, 학술제에서 시각화 시 태블로를 사용하기를 권장하는 안내가 나갈 예정입니다.
그 때 열심히 배운 내용을 잘 활용해주세요. 감사합니다 :)
