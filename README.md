# HSCZ 웹 프로젝트(HSCODE 예측 모델 개발) - 파이썬
<div class="inline-images">
    <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=Python&logoColor=white">
</div>
<br>
<br>

> 머신러닝을 이용하여 사용자가 제품에 대한 설명을 입력하면 가장 유사한 HSCODE를 예측하여 추천하는 모델입니다.
<br>
<p>
  <img src="https://github.com/ghgrnrdud/Python_Project_HSCZ/assets/153475197/c4238cbe-fb3f-476b-99bf-51beda2a1f4e" width="500" height="300">
</p>
<br>

# 📖Description
- HSCODE를 통해 관세를 결정하기 때문에 수출입업자들에게 필수적임. 효율적으로 간편하게 HSCODE를 제공하기 위해 예측 모델 개발
- HSCODE는 부, 류, 호, 소호 총 10자리로 구성되어 있고, 4자리인 호까지 분류할 수 있도록 분류체계 설계
- 제품명 같은 간단한 단어를 입력하는 선행연구에서 더 나아가 문장으로 된 제품설명 글을 입력 받을 수 있음. 사용자는 복잡한 기계류 제품을 단어가 아닌 글로 설명 가능
<br>

# ⏱️TimeLine
### 데이터수집 > 전처리 > 모델링 > 결과
<br>

## ℹ️데이터수집
- 수집 경로 : 관세법령 정보포털
- 수집 연도 : 2012 ~ 2023
- 수집 국가 : 국내/영국/EU
- 수집 방법 : 웹 크롤링
- 총 데이터 수 : 127,332개
<br>

## 🪛전처리
1. 국내 사례 수집 데이터를 구글 API를 사용하여 번역
2. 중복행 제거
3. 호 단위까지의 분류체계에 맞게 HSCODE를 4자리로 통일
4. 소문자 변환
5. 구두점/불용어 제거
6. 품사태깅
7. 표제어 추출
8. TF-IDF 기법 활용
<br>

## 📊모델링
분류분석 모델 Logistic Regression, LSVC, RandomForestClassifier 3가지를 실행했을 때 예측 정확도가 0.914로 가장 높은 LSVC 모델 선택
<p>
  <img src="https://github.com/ghgrnrdud/Python_Project_HSCZ/assets/153475197/b28e904a-bbae-4f42-876d-cb64cb0210d5" width="500" height="300">
</p>
<br>

## 🔎결과
이 모델을 통한 최종 시스템 : 사용자가 수출입 하고자하는 제품의 설명을 입력하면 모델을 통해 제품의 설명과 가장 유사한 HS 코드 3가지를 예측하고 순위를 매겨 사용자에게 추천하는 시스템
<p>
  <img src="https://github.com/ghgrnrdud/Python_Project_HSCZ/assets/153475197/431aeee2-19ad-4ac9-8480-ce87256296ab" width="500" height="300">
</p>


