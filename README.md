# 😺 Face Character Emoji - 실시간 얼굴 필터 웹 애플리케이션

## 📌 프로젝트 소개
Face Character Emoji는 웹캠을 통해 실시간으로 사용자의 얼굴을 인식하고 재미있는 동물 캐릭터 필터를 적용할 수 있는 웹 애플리케이션입니다. MediaPipe의 얼굴 인식 기술과 Flask 웹 프레임워크를 활용하여 개발되었습니다.

## 🎯 주요 기능
- MediaPipe를 활용한 정확한 얼굴 인식
- 다양한 동물 캐릭터 필터 (고양이, 여우)
- 웹 인터페이스를 통한 간편한 필터 전환
- 실시간 이미지 오버레이 처리

## 🛠 기술 스택
- **Backend**: Python, Flask
- **AI/ML**: 
  - MediaPipe (얼굴 특징점 검출)
  - OpenCV (이미지 처리 및 변환)
- **Frontend**: HTML, JavaScript

## 📁 프로젝트 구조
```
face_character_emoji/
├── main.py               # Flask 웹 서버 및 라우팅
├── animal_overlay_filter.py  # 얼굴 인식 및 필터 처리
├── image_overlay.py      # 이미지 합성 유틸리티
├── templates/
│   └── index.html       # 웹 인터페이스
├── images/
│   ├── cat_right_ear.png
│   ├── cat_left_ear.png
│   ├── cat_nose.png
│   ├── fox_right_ear.png
│   ├── fox_left_ear.png
│   └── fox_nose.png
└── requirements.txt      # 프로젝트 의존성
```

## 🔍 시스템 아키텍처
```mermaid
graph TD
    A[웹캠] --> B[Flask 서버]
    B --> C[MediaPipe 얼굴 인식]
    C --> D[이미지 오버레이 처리]
    D --> E[필터 적용]
    E --> F[실시간 스트리밍]
    F --> G[웹 브라우저]
```

## ⚙️ 설치 방법
1. 가상환경 생성 및 활성화
```bash
python -m venv venv
.\venv\Scripts\activate  # Windows
```

2. 필요한 패키지 설치
```bash
pip install -r requirements.txt
```

3. 애플리케이션 실행
```bash
python main.py
```

4. 웹 브라우저에서 접속
```
http://localhost:5000
```

## 💻 주요 기능 상세 설명
### 1. 얼굴 인식 시스템 (`animal_overlay_filter.py`)
- MediaPipe를 활용한 얼굴 특징점 추출
- 실시간 처리 최적화
- 눈과 코 위치 자동 감지

### 2. 캐릭터 필터 처리
- 고양이와 여우 캐릭터 필터
- 실시간 필터 전환
- 얼굴 특징점 기반 필터 포지셔닝
- OpenCV를 활용한 투명도 처리 및 이미지 합성

### 3. 웹 인터페이스
- 직관적인 UI/UX
- 실시간 웹캠 피드백
- 간편한 필터 전환 버튼
- 반응형 디자인

## 🌟 핵심 구현 사항
1. **실시간 처리 시스템**
   - MediaPipe 얼굴 특징점 검출
   - OpenCV 기반 실시간 이미지 처리
   - 효율적인 메모리 관리
   - 실시간 처리를 위한 최적화

2. **사용자 경험**
   - 직관적인 필터 인터페이스
   - 실시간 피드백 제공
   - 다양한 시각적 효과

## 🔧 개발 환경
- Python 3.8+
- Windows 10
- WebCam 필요

## 🎉 프로젝트 특징
- MediaPipe를 활용한 정확한 얼굴 인식
- 사용자 친화적인 웹 인터페이스
- 실시간 처리 최적화
- 다양한 동물 캐릭터 필터 지원
