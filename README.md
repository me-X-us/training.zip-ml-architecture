# training.zip-ml-architecture
Training.zip 서비스의 ml 모델 
트집은 웹브라우저와 웹캠만 있으면 언제 어디서든 헬스,스포츠,댄스등의 트레이닝서비스를 받을 수 있도록 하는 서비스 플랫폼입니다.

# Pose estimation model

- 모델은 HRNet  - [https://github.com/stefanopini/simple-HRNet](https://github.com/stefanopini/simple-HRNet) 를 참조하였습니다.
- HRNet 구조
- 고해상도의 이미지를 유지시키고 저해상도의 이미지를 병렬로 연결하는 방식이기 때문에, 좀 더 정밀한 특징 추출이 가능한 네트워크

    ![https://github.com/me-X-us/training.zip-ml-architecture/hrnet.png]

- video 데이터를 입력 받아서 사람의 관절 정보를 JSON 타입으로 변환

    ![https://github.com/me-X-us/training.zip-ml-architecture/oputput.png]
- 포즈 추출 모델 예시
    ![https://github.com/me-X-us/training.zip-ml-architecture/pose.gif]
# Shape estimation model

- torchvision.models.detection.maskrcnn_resnet50_fpn 모델을 사용
- 트레이너의 형상을 추출한 후 .mp4 형식으로 저장 (vp09 코덱)
- 형상 추출 모델 예시
 ![https://github.com/me-X-us/training.zip-ml-architecture/shape.gif]
