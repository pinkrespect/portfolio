# 이미지의 결함물 검출을 위한 grad-CAM
## 참고 논문
https://arxiv.org/abs/1610.02391
https://arxiv.org/abs/1502.03044

## 참고 코드
https://github.com/kazuto1011/grad-cam-pytorch<br>
https://github.com/leftthomas/GradCAM<br>
https://github.com/sgrvinod/a-PyTorch-Tutorial-to-Image-Captioning

## 내용
건축물의 결함 검출을 위한 2D Image Detection<br>
건축물의 결함 사진을 설명하는 Image Captioning<br>
grad-CAM 및 LSTM 모델 트레이닝 및 인퍼런싱

## 데이터셋
기존 건축물의 결함 이미지를 활용<br>
기존 건축물의 결함을 설명하는 Text 데이터셋
### 기존 건축물의 결함 Class
박락, 박리, 철근 노출, 누수, 백태
### 기존 건축물의 결함 데이터 전처리
각각의 특징만 Crop 후, 각각의 Class 이름 별로 폴더를 만들어 저장
### 건축물의 결함을 설명하는 Text 데이터셋
한 사진당 3개 이상의 Text Explain GT 데이터 필요
### 건축물의 결함을 설명하는 Text 데이터 전처리
.json 파일로 만들어 http://cs.stanford.edu/people/karpathy/deepimagesent/caption_datasets.zip 의 양식에 맞춤

## 트레이닝
- Learning rate를 0.0002부터 시작하여, 0.002까지 순차적으로 늘림
- Batch Size는 크면 좋지만 적을경우 한 Class의 이미지 갯수를 전부 포함할 정도로 설정
- GPU 사용 시 옵션을 바꿔줘야 하는 부분 있음

## 인퍼런싱
![이력서](https://user-images.githubusercontent.com/14182583/73243204-5f956380-41ea-11ea-85bf-2ac3f511a417.jpg)
