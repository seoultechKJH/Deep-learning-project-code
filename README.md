# Deep-learning-project-code
Class Imbalanced Deep Learning via a Class-Balanced Ensemble 논문 저자의 코드 재현

코드 출처: https://github.com/smallcube/Class-balanced-Ensemble

# 파일 구성
-  MyEnsemble.py -> 실질적인 실행코드. 메인함수인 MyEnsemble을 실행함으로써 작동 가능
-  EnsembleV2.py -> 메인 네트워크인 ResNext 모델과 보조분류기 생성 클래스가 정의되어 있는 코드 파일
-  FocalLossV5.py -> 논문에서 제안한 BCE Loss 코드 파일
-  CifarImbalanced.py -> CIFAR-10 및 CIFAR-100에 불균형성을 적용한 데이터셋 제공
