# 🎯 YouTube 조회수 예측 (영상 제목 기반, 실습 프로젝트)

## 📌 프로젝트 개요

- Kaggle **YouTube Trending Video Dataset** (US subset)을 활용한 **딥러닝 실습**
- 공개 데이터와 참고 예제 코드를 기반으로 **데이터 전처리 → 모델 설계 → 학습 → 평가** 전 과정을 재현
- **영상 제목 텍스트만**을 입력으로 조회수를 예측하는 NLP 회귀 모델 구현

---

## 📂 데이터 & 참고 자료

- **데이터 출처**: [Kaggle - Trending YouTube Video Statistics](https://www.kaggle.com/datasets/datasnaek/youtube-new)
- **참고 코드**: 공개 GitHub 예제 및 블로그 튜토리얼 일부 참고, 학습 목적에 맞게 수정·실행

---

## 🛠 사용 기술

- **Python** 3.11
- **TensorFlow / Keras** (LSTM, Embedding)
- **Pandas / NumPy**
- **Matplotlib / Seaborn**
- Google Colab Pro 환경에서 개발 및 학습

---

## 📂 프로젝트 구조

data/ # 데이터 관련 파일
experiments/ # 실험 기록 및 템플릿
notebooks/ # 학습/실험
results/ # 결과물 (손실 곡선, 모델 요약)
README.md # 프로젝트 소개 문서
requirements.txt # 의존성 패키지 목록

---

## 📊 학습 결과

- **훈련 Epochs**: 15
- **Batch Size**: 128
- **Train MSE**: 0.8564
- **Validation MSE**: 0.4359
- **Validation RMSE (역변환)**: 약 **4,972,961**

📈 **손실 곡선**  
`results/loss_curve.png` 참고

---

## 💡 학습 포인트

- NLP 기반 회귀 문제 접근 방법 이해
- 텍스트 전처리(토큰화, 패딩)와 log 변환 적용
- LSTM 구조와 하이퍼파라미터 조정 경험
- 모델 성능 평가 지표(RMSE) 계산 및 해석

---

## 🧩 나의 역할

- 제공된 데이터와 예제 코드를 바탕으로 전처리 과정 수정
- 모델 구조 및 하이퍼파라미터 일부 변경
- 학습 및 평가 실행, 결과 분석
