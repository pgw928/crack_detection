# 공모전 프로젝트



## Task

* 미세 Crack 검출 모델 
  * 타일 생성 공정 중에 발생되는 여러 종류의 미세 Crack에 대해서 식별(True/False)하고 자동 검출 가능한 모형
* 기대 효과 
  * 타일은 타 제조업에 비해 불량률이 높아 AI를 통해 타일의 불량률을 낮추고 사용 중 하자를 방지해 품질 향상과 비용절감이 가능하다.



## 모델 학습 예측을 위한 실행 방법 및 코드 소개

> 데이터는 비공개로 제공된 데이터이며, 코드 또한 미실행 파일입니다.

1. 활용 데이터 전처리 방법 활용 모델들에 대한 간략한 설명
   * train/validation : `train.csv`를 기준으로 8 : 2로 분류
   * 전처리 과정 없음
   * Augmentation : model 별 `tensorflow.keras.preprocessing.image.ImageDataGenerator`를 사용함 (`1.train`에 있는 파일 별로 각각 적혀있음)
   *  `2.train`에 있는 모델들(전이학습 후 미세조정)을 이용해 데이터를 학습하고 `3.predict`에서 앙상블을 통해 결과 제출
2. 디렉토리
   * `1.data분류`
   * `2.train`
   * `3.predict`
3.  코드 
   * data분류 : train/validation 및 test 원본 파일을 저희가 지정한 폴더로 복사해 오는 코드 입니다.
   * train
     * DenseNet169.ipynb
     * efficientnet_b7.ipynb
     * InceptionResNetV2.ipynb
     * InceptionV3_244_244.ipynb
     * ResNet101V2.ipynb
     * resnet50v2.ipynb
     * X-inception.ipynb
   * predict
     * Ensemble_Predict.ipynb :  학습한 모델들을 앙상블 방법의 Soft Voting을 통해 test dataset을 예측 후 제출 하는 코드

## 팀 구성 및 역할

* 한현도 : 데이터 분리 및 모델 학습
* 장수이 : 모델 학습, 하이퍼파라미터 최적화
* 박근웅 : 데이터 분리 및 학습, 모델 구성, 모델 학습
* 양진상 : 모델 학습, 모델 성능 향상





## 결과

* Public Test set : 0.947
* Private Test set : 0.95

* **1위** **수상**

