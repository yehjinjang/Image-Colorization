# 🎨 Image Colorization & Restoration Project

## 📖 Overview
이 프로젝트는 VisionAI와 비즈니스 수업의 일환으로 흑백 얼굴 이미지를 컬러로 복원하고 품질을 향상시키는 시스템을 개발하기 위해 진행되었습니다. **Autoencoder**와 **GFPGAN** 모델을 활용하여 이미지 컬러화 및 복원 작업을 수행하였습니다.

---

## 🗓️ Period
- 2023년 9월 ~ 2023년 12월 (3개월)

---

## 👥 Team
- DLE 2명

---

## 🛠️ Stack
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white) ![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white) 
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white) ![Keras](https://img.shields.io/badge/Keras-D00000?style=for-the-badge&logo=keras&logoColor=white) 

---

## 🧑‍💻 Key Task
1. **데이터셋 준비**
   - CelebA 데이터셋에서 약 20,000개의 이미지 추출
   - All-Age-Faces (Asian) 데이터셋에서 15,000개의 이미지를 추가 병합하여 총 43,322개의 얼굴 데이터셋 생성

2. **전처리**
   - 이미지를 흑백(BGR → GrayScale)으로 변환 및 정규화
   - 크기를 224x184로 조정하고, 데이터 배치를 생성하여 모델에 입력 제공
   - 데이터셋을 8:2 비율로 훈련 세트와 테스트 세트로 분할

3. **모델 아키텍처**
   - **Autoencoder:** 흑백 이미지를 컬러화하는 데 사용
   - **Encoder:** 입력 이미지를 저차원으로 압축하고 공간 특징을 추출
   - **Decoder:** 저차원 표현을 활용해 원래 데이터를 복원
   - **GFPGAN:** 복원 및 품질 향상에 활용
   - 활성화 함수(ReLU, tanh), 손실 함수(MSE), 최적화 알고리즘(Adam) 적용

4. **실험 및 결과**
   - 초기 파이프라인: **복원(GFPGAN)** → **컬러화(Autoencoder)**
   - 최적 파이프라인: **컬러화(Autoencoder)** → **복원(GFPGAN)**
   - 최종 결과: 74.68%의 정확도, 0.0035의 손실로 자연스러운 컬러화를 달성

---

## 🌟 Retrospective
- **새로운 발견:** 흑백 이미지를 컬러로 변환하는 과정에서 **CV의 재미**를 느꼈습니다
- **성장:** 다양한 딥러닝 모델과 데이터 전처리 기술을 실습하며 기술 역량을 높일 수 있었습니다
- **한계:** GPU 자원 부족으로 인해 일부 한계가 있었지만, 이를 극복하며 효율적인 파이프라인을 설계할 수 있었습니다
