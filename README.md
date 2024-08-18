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
  <summary>첫번째 방법(기본 제공하는 방법)</summary>
  
### 1) 신문 아카이브에서 제공하는 '신문브라우징'과 데이터 다운로드 
![image](https://github.com/user-attachments/assets/94da38e7-cdde-4906-a2a1-cc605f5ec056)
![image](https://github.com/user-attachments/assets/27b10222-93d9-4bfc-95ad-8311c1c6989b)
![제목 없음](https://github.com/user-attachments/assets/f89a93ac-d0c8-45a6-b0ce-c13856b3da5b)

  
</details>
<details>
  <summary>두번째 방법(스크래핑 코드)</summary>
  
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

<br><br>
## 2. 텍스트 데이터 분석
### 1) **왜 데이터프레임인가?** : 컴퓨터로 분석할 때에는 '정형 데이터'가 명령하기 수월하다. 
![image](https://github.com/user-attachments/assets/0b2541d5-cbfe-4ac8-b64b-58bf2a7b1668)
출처 : 유인태, 한문 고전 텍스트와 데이터 처리(한림 DH 워크숍 시리즈), 2024.7.3.
<br>
### 2) ChatGPT로 **데이터 프레임** 수정하기 
<br>
  ChatGPT 채팅창에 수정할 엑셀, csv 형태의 파일을 업로드하고, 조건에 따른 파일의 수정을 명령할 수 있다. 특정 단어(글자)가 들어간 파일을 필터링하거나 행의 배열을 바꿀 수 있다.

### 3) 영어 텍스트 전처리
**영어와 한국어 텍스트의 차이**

<br>

  "일반적으로 한 어절이 한 단어인 영문텍스트에 토픽모델링을 적용할 경우, 형태소 분석이나 어근 추출과 같은 텍스트 전처리 과정을 거치지 않는다. 공백으로 분리된 어절(token)을 텍스트 처리에 그대로 사용하고, 어근이 동일한 단어의 단수형이나 복수형, 동명사 등 한 단어의 다양한 활용형을 모두 다르게 처리하여 단어 사용의 맥락을 파악한다. **그러나 한글의 경우 한 어절에 어간에 조사가 결합되어 있는 교착어로, 영문텍스트처럼 단일 형태소로 구성되어 있지 않기 때문에 별도의 자연어처리 과정이 필요하다.**"

<br>

출처 : 정유경, 2020, 「텍스트의 계량 분석을 활용한 근대전환기 신문의 시계열적 주제 분석법 - 『황성신문』 논설을 대상으로」, 『역사문제연구』24-1, p.141.

<br>

### 4) 데이터 분석 방법 질문하기, 전처리 수행하기(대소문자 통일, 불용어 제거, 표제어 추출 작업), 말뭉치 형성하기

<br>

"업로드 한 파일이 어떤 파일인지 확인해줘"\
"content 열을 기준으로 분석하고 싶은데 어떻게 분석하면 좋을지 알려줘"\
"대소문자를 통일해주고, 내가 업로드한 파일로 불용어를 제거하고, 내가 업로드한 파일로 어간 및 표제어 추출 등을 진행해서 새로운 열에 말뭉치를 형성해줘."\
<br>

<details>
  <summary>GPT가 알려주는 분석절차</summary>
  
![image](https://github.com/user-attachments/assets/0d384bd6-dcd5-47b4-9cd6-47e7ac9175db)

</details>









