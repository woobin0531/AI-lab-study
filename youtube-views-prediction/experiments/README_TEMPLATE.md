# 유튜브 제목 기반 조회수 예측 실험

## 개요

- **목적**: 유튜브 영상 제목 텍스트만으로 조회수를 예측하는 딥러닝 모델 구현
- **데이터**: Kaggle - YouTube Trending Video Dataset (**US subset**, `USvideos.csv`)
- **방법**:
  1. **데이터 전처리**
     - `USvideos.csv`에서 제목(`title`)과 조회수(`views`)만 사용
     - 불필요한 특수문자 제거, NaN 및 중복 데이터 삭제
     - 조회수에 `log1p` 변환 적용 (데이터 스케일 안정화)
  2. **데이터 분리**
     - 학습:검증 = 8:2 비율로 분할
  3. **텍스트 토큰화**
     - TensorFlow `Tokenizer`를 이용해 단어 인덱스 변환
     - 최대 시퀀스 길이로 `pad_sequences` 적용
  4. **모델 설계**
     - Embedding Layer
     - Bidirectional LSTM Layer
     - Dense Layer → Linear Activation (회귀)
  5. **학습 설정**
     - 손실 함수: MSE
     - 옵티마이저: Adam
     - EarlyStopping & ModelCheckpoint 적용
  6. **성능 평가**
     - 예측값 역변환(`expm1`) 후 RMSE 계산
     - 학습 및 검증 손실 시각화

## 결과

- **핵심 수치**:
  - 최종 Val RMSE: _실험 실행 후 기입_
- **스크린샷/그래프**:
  - `results/loss_curve.png`
  - `results/model_summary.txt`

## 메모

- **한계**:
  - 제목만으로는 조회수 예측 정확도가 제한적
  - 썸네일, 태그, 업로드 시간, 카테고리 등 추가 메타데이터 필요
