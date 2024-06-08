# INU Machine Learning Final Project
## Female-Male Classification Challenge 
1. 실행 설명서 `README.md`
2. 학습용 코드 `FMCC_Train.ipynb`
3. 테스트용 코드 `FMCC_Test.ipynb`
4. 학습된 모델 `voting_classifier.pkl`
5. 테스트 결과 파일 `과탑_test_results.txt`
6. 논문 형식 결과 보고서 

## Explaination of FMCC_Test.ipynb
- `FMCC_Test.ipynb` 파일과 데이터셋 디렉토리인 `raw16k` 를 같은 디렉토리에 위치시킨다.
### 0. Install required library
### 1. Preprocess data
- `raw16k` 안의 `fmcc_test.ctl` 파일을 읽어 데이터 전처리 과정을 거친다. 
### 2. Load trained model
- `FMCC_Train.ipynb` 파일을 통해 저장된 모델을 로드한다.
### 3. Predict & Create result file
- 로드된 모델로 테스트 데이터를 추론하고 perl 스크립트 파일을 실행하기 위한 result file 을 생성한다.
## Required library
> pickle\
> Train 후 파이썬 객체 파일로 저장된 모델을 불러와 Test에 이용한다.

> librosa\
> 오디오 분석을 위한 라이브러리로 mfcc 를 이용한 특징 추출에 이용한다.

> numpy\
> 배열 및 행렬 연산에 최적화된 기능을 포함하고 있어 배열 연산을 빠르고 효율적으로 실행할 수 있다.

> noisereduce\
> 오디오 신호에서 노이즈를 제거하는 데 이용한다.

> sklearn\
> 머신 러닝 라이브러리로, 데이터 전처리와 다양한 머신 러닝 알고리즘을 제공한다.\
> SVM, KNN, RF를 ensemble한 VotingClassifer를 분류기 모델로 이용한다.

> tqdm\
> 반복 작업 시 진행 상태를 보여준다. 코드의 실행 상태를 모니터링하기 위해 이용한다.