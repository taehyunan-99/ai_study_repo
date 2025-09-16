# 📚 AI & OpenCV Study Repository

컴퓨터 비전 및 OpenCV 학습을 위한 레포지토리입니다.

## 📂 폴더 구조
```
ai_study_repo/
├── note/              # Jupyter Notebook 학습 자료
│   ├── 01_image_basic.ipynb
│   ├── 02_video_basic.ipynb
│   ├── 03_edit_image_basic.ipynb
│   ├── 04_diagram.ipynb
│   ├── 05_blur_binarization.ipynb
│   ├── 06_rotate_perspective.ipynb
│   ├── 07_edge_detection.ipynb
│   ├── 08_contour.ipynb
│   ├── 09_histogram_erode_dilate.ipynb
│   ├── 10_face_recognition.ipynb
│   ├── 11_yolo.ipynb
│   └── 12_tesseract-ocr.ipynb
├── cascade/           # Haar Cascade 분류기 파일들
├── images/            # 예제 이미지 파일들
├── videos/            # 예제 비디오 파일들
├── output/            # 처리된 결과물 저장
└── README.md          # 프로젝트 개요
```

## 📂 학습 내용

### 🖼️ 이미지 기초
#### 이미지 입출력
- **이미지 불러오기**: 컬러, 그레이스케일, 투명도 옵션
- **이미지 속성**: shape를 이용한 이미지 정보 확인
- **파일 저장**: imwrite를 이용한 이미지 저장

<br/>

#### 비디오 처리
- **비디오 파일 재생**: VideoCapture를 이용한 비디오 처리
- **FPS 제어**: 프레임 속도 조절 및 프레임 처리
- **실시간 영상**: 웹캠을 이용한 실시간 영상 처리
- **화면 캡처**: 비디오 저장 및 화면 캡처

<br/>

#### 이미지 조작
- **빈 화면 생성**: NumPy 배열을 이용한 이미지 생성
- **기본 조작**: 이미지 편집 및 변형 작업

<br/>

#### 도형 그리기
- **선 그리기**: line() 함수를 이용한 직선 그리기
- **원 그리기**: circle() 함수를 이용한 원 그리기 (속 채우기 옵션 포함)
- **타원 그리기**: ellipse() 함수를 이용한 타원 그리기
- **사각형 그리기**: rectangle() 함수를 이용한 사각형 그리기
- **다각형 그리기**: polylines(), fillPoly() 함수를 이용한 다각형 그리기
- **텍스트 그리기**: putText() 함수를 이용한 영문 텍스트 추가

<br/>

### 🔍 이미지 처리 고급
#### 블러와 이진화
- **기본 블러**: 이미지 흐릿하게 처리
- **가우시안 블러**: 자연스러운 블러 효과
- **모션 블러**: 움직임 효과 블러
- **bilateral 필터**: 경계 보존 블러

<br/>

#### 이진화 처리
- **threshold**: 임계값을 이용한 이진화
- **adaptive threshold**: 적응적 임계값 이진화
- **OTSU 이진화**: 자동 임계값 결정

<br/>

#### 이미지 회전과 원근 변환
- **회전**: 이미지 회전 변환
- **원근 변환**: Perspective Transformation
- **아핀 변환**: Affine Transformation
- **좌표 변환**: 이미지 위치 및 크기 변경

<br/>

#### 경계선 검출
- **Canny 알고리즘**: 경계선 검출을 위한 핵심 알고리즘
- **임계값 설정**: 약한 경계와 강한 경계 임계값 조절
- **트랙바 활용**: 실시간 임계값 조정으로 최적 파라미터 찾기
- **실시간 처리**: 웹캠을 이용한 실시간 경계선 검출

<br/>

#### 윤곽선
- **윤곽선 검출**: findContours를 이용한 윤곽선 찾기
- **윤곽선 그리기**: drawContours를 이용한 윤곽선 시각화
- **이진화 전처리**: Threshold와 OTSU를 이용한 전처리
- **윤곽선 분석**: 같은 색상 영역의 경계선 연결

<br/>

#### 히스토그램, 팽창과 침식
- **히스토그램**: 이미지의 색상 분포 분석
- **Erosion**: 이미지 침식 연산으로 객체 축소
- **Dilation**: 이미지 팽창 연산으로 객체 확장
- **Opening**: 침식 후 팽창으로 노이즈 제거
- **Closing**: 팽창 후 침식으로 구멍 채우기
- **Morphological Gradient**: 팽창과 침식의 차이로 경계선 강조

<br/>

### 🤖 얼굴 인식
#### Haar Cascade
- **Haar Cascade**: 전통적인 얼굴 검출 알고리즘
- **분류기 로드**: 사전 학습된 cascade 파일 사용
- **검출 파라미터**: scaleFactor, minNeighbors 조정
- **실시간 검출**: 웹캠을 이용한 실시간 얼굴 인식
- **영역 표시**: 검출된 얼굴 영역에 사각형 그리기
- **움직임 감지**: 배경제거(MOG2)를 이용한 움직임 감지 및 자동 캡처

<br/>

### 🎯 객체 탐지 (YOLO)
#### YOLO 모델
- **YOLO 모델 로드**: ultralytics YOLO 모델 사용 (yolo11n.pt)
- **이미지 객체 탐지**: 정적 이미지에서 객체 인식 및 분류
- **신뢰도 설정**: conf 파라미터를 통한 탐지 임계값 조정
- **결과 시각화**: 탐지된 객체에 바운딩 박스와 라벨 표시

<br/>

#### 동영상 객체 탐지
- **비디오 파일 처리**: 동영상에서 실시간 객체 탐지
- **웹캠 실시간 탐지**: 실시간 카메라 피드에서 객체 인식
- **다중 객체 탐지**: 한 프레임에서 여러 객체 동시 탐지

<br/>

### 📝 텍스트 인식 (Tesseract OCR)
#### OCR 기본 처리
- **Tesseract OCR**: pytesseract를 이용한 텍스트 인식

<br/>

#### 원근 변환 OCR
- **원근 변환**: getPerspectiveTransform으로 텍스트 영역 정규화
- **실시간 인식**: 변환된 영역에서 즉시 텍스트 추출
- **대화형 처리**: 사용자 인터페이스를 통한 직관적 텍스트 추출

<br/>

---
*마지막 업데이트: 2025-09-16*