# 📸 AI & OpenCV Study Repository

OpenCV와 컴퓨터 비전 학습을 위한 레포지토리입니다.

## 📂 학습 내용

### 🖼️ 이미지 처리 기초 (Jupyter Notebook)
`note/` 폴더에 OpenCV 기본 개념을 단계별로 학습한 노트북 파일들이 있습니다:

- **이미지 입출력**
  - **01_image_basic.ipynb**: 이미지 불러오기, 출력, 저장
    - 이미지 불러오기 옵션 (컬러, 그레이스케일, 투명도)
    - 이미지 속성 확인 (`shape`)
    - 파일 저장 (`imwrite`)

- **비디오 처리**
  - **02_video_basic.ipynb**: 비디오 파일 및 실시간 영상 처리
    - 비디오 파일 재생 (`VideoCapture`)
    - FPS 제어 및 프레임 처리
    - 웹캠 실시간 영상 처리
    - 화면 캡처 및 비디오 저장

- **이미지 조작**
  - **03_edit_image_basic.ipynb**: 기본적인 이미지 편집
    - NumPy 배열을 이용한 빈 화면 생성
    - 이미지 기본 조작 작업

### 🛠️ 리소스
#### `images/`
예제 이미지 파일들 (dog.jpg, cat.jpg, dog_png.png 등)

#### `videos/`
예제 비디오 파일들 (dog.mp4 등)

#### `output/`
처리된 결과물 저장 폴더

---
*마지막 업데이트: 2025-09-08*