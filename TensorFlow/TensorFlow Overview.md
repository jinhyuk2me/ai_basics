## TL;DR
- TensorFlow 전체 구조를 빠르게 훑고, 세부 노트의 학습 순서를 제시하는 허브입니다.
- 설치 확인 → Tensor 기본기 → 데이터 파이프라인 → Keras 모델링 → 학습/분산 → 배포 순으로 로드맵을 안내합니다.
- PyTorch 노트와 병행 학습할 수 있도록 비교 포인트와 활용 경로를 제공합니다.

## 언제 쓰나
- TensorFlow를 처음 접하고 전체 생태계 흐름을 파악하고 싶을 때
- Keras 중심 모델링에서 분산 학습, 배포까지 어떤 노트를 참고해야 할지 한눈에 보고 싶을 때
- PyTorch와 기능을 비교하며 프레임워크를 선택하거나 병행 학습할 때

## 주요 포인트
- 설치 & 버전 확인, GPU 설정, 기본 리소스 정리
- Tensor/Autograph, tf.data, Keras Functional API, 분산 전략, TFLite 등 핵심 모듈 소개
- 각 섹션별 핵심 노트 링크와 다음 학습 단계 안내

## 실습 예제
```python
import tensorflow as tf

print(tf.__version__)
print(tf.config.list_physical_devices('GPU'))

a = tf.constant([[1., 2.], [3., 4.]], dtype=tf.float32)
b = tf.matmul(a, tf.transpose(a))
print(b)
```

## 실수 주의
- GPU 버전 설치 시 CUDA/cuDNN 버전 호환성을 반드시 확인하세요.
- eager 실행과 그래프 모드가 혼용될 때 Autograph 변환이 예상과 다르게 동작할 수 있습니다.

## 관련 노트
- [[TensorFlow/Tensor/TF Tensor Basics]]
- [[TensorFlow/Data/tf.data Overview]]
- [[TensorFlow/Modeling/Keras Functional API]]
- [[TensorFlow/Training/Training Loop (fit vs custom)]]
- [[TensorFlow/Deployment/TensorFlow Serving]]
