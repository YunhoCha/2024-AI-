# 2024년 8월 19일 한양대학교 사학과 '초보자를 위한 AI툴 활용법'
요약 : 'ChatGPT를 활용한 텍스트마이닝 및 통계분석 입문하기'의 강의자료, 코드, 사용법\
발표자 : 한양대학교 사학과 석사과정 차윤호
<br><br>

## 0. 개요(학습목표)
  
- 국립중앙도서관 신문아카이브 https://www.nl.go.kr/newspaper/index.do 에서 자료 수집하는 법, 스크래핑 코드 사용법 학습하기.
- ChatGPT를 활용하여 신문 영어 텍스트 분석하기(텍스트마이닝)
- ChatGPT를 활용하여 역사 수치 데이터 분석하기(통계분석)

<br><br>
## 1. 신문 아카이브에서 자료수집
<details>
  <summary>첫번째 방법</summary>
  
### 1) 신문 아카이브에서 제공하는 '신문브라우징'과 데이터 다운로드 
![image](https://github.com/user-attachments/assets/94da38e7-cdde-4906-a2a1-cc605f5ec056)
![image](https://github.com/user-attachments/assets/27b10222-93d9-4bfc-95ad-8311c1c6989b)
![제목 없음](https://github.com/user-attachments/assets/f89a93ac-d0c8-45a6-b0ce-c13856b3da5b)

  
</details>
<details>
  <summary>두번째 방법</summary>
  
### 2) 스크래핑 코드 사용법 
1. 본 깃허브 페이지 상단의 file 중 '신문아카이브_스크래핑_코드.ipynb' 클릭<br><br>
2. **'open in colab'** 클릭<br><br>
3. 좌측 파일 마크 클릭
- ![image](https://github.com/user-attachments/assets/3966fb80-75ec-4ca2-8700-bf466fd840a7)<br><br>
4. 차례대로 셀 실행 버튼 클릭(셀 하나가 완료되면 다음 셀 실행)
- ![image](https://github.com/user-attachments/assets/35c518c5-0637-40b2-96dc-62a17939dad7)<br><br>
5. 세 번째 셀에서 ID 입력할 때 스크래핑 할 신문 기사의 첫 아이디 입력 후 엔터, 마지막 아이디 입력 후 엔터

<div style="margin: 0 auto; width: fit-content;">

| 신문 제목 | 처음 아이디 | 마지막 아이디 |
|----------|----------|----------|
| 독립신문 영문판 | 00093088662 | 00093105675 |
| 대한매일신보 영문판 | 00093087842 | 00093088661 |
| Row 3, Column 1 | Row 3, Column 2 | Row 3, Column 3 |
| Row 4, Column 1 | Row 4, Column 2 | Row 4, Column 3 |

</div>

</details>
