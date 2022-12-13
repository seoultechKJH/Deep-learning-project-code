# Deep-learning-project-code
Class Imbalanced Deep Learning via a Class-Balanced Ensemble 논문 저자의 코드 재현

코드 출처: https://github.com/smallcube/Class-balanced-Ensemble

# 파일 구성
-  MyEnsemble -> 실질적인 실행코드. 메인함수인 MyEnsemble을 실행함으로써 작동 가능
-  EnsembleV2 -> 메인 네트워크인 ResNext 모델과 보조분류기 생성 클래스가 정의되어 있는 코드 파일
-  FocalLossV5 -> 논문에서 제안한 BCE Loss 코드 파일
-  CifarImbalanced -> CIFAR-10 및 CIFAR-100에 불균형성을 적용한 데이터셋 제공

# 작동 프로세스
- 클래스 불균형이 존재하는 이미지 데이터셋에 대해, 메인 네트워크인 ResNext를 중심으로 5개의 보조 분류기가 달려있음
- 메인 네트워크의 레이어가 깊은 곳에 위치한 보조 분류기일수록 커널 사이즈를 작게 하여 좀 더 세부적인 정보를 학습하는 것이 주요 아이디어임
- 메인 네트워크는 3개의 Block으로 이루어져 있으며, 각 Block은 5개의 Bottleneck 레이어로 구성되어 있음
- 5개의 Bottleneck 레이어 중 첫번째 레이어에서만 출력 채널 수가 입력 채널의 2배가 되며, 나머지 레이어에서는 채널 수가 유지됨
