 GPT 여행 일정 추천 웹앱

OpenAI GPT와 Kakao/YouTube API를 활용한 **여행 일정 생성 & 장소 추천 웹 애플리케이션**입니다.  
사용자는 여행 날짜, 지역, 인원, 테마 등을 입력하면 **자동으로 여행 일정을 생성**하고,  
**맛집·카페·숙소**를 함께 추천해줍니다.

---

주요 기능

- GPT 기반 맞춤 여행 일정 자동 생성
- Kakao API를 이용한 지역 기반 장소 검색 (맛집, 카페, 숙소)
- 유튜브 추천 영상 자동 표시
- 일정 텍스트에서 장소 추출 → 지도에 마커로 시각화

---

설치 방법

```bash
# 1. 가상 환경 생성 (선택)
python -m venv venv
source venv/bin/activate   # macOS/Linux
venv\Scripts\activate      # Windows

# 2. 필요한 패키지 설치
pip install -r requirements.txt


환경변수 
OPENAI_API_KEY=your_openai_api_key
KAKAO_REST_API_KEY=your_kakao_rest_key
KAKAO_JAVASCRIPT_KEY=your_kakao_js_key
YOUTUBE_API_KEY=your_youtube_api_key


구조
├── app.py                 # 메인 Flask 애플리케이션
├── templates/             # HTML 템플릿 폴더
│   ├── index.html         # 메인 페이지
│   ├── plan.html          # 여행 일정 생성
│   ├── food.html          # 맛집 추천
│   ├── cafe.html          # 카페 추천
│   └── acc.html           # 숙소 추천
├── static/                # CSS 파일
├── .env                   # API 키 설정 파일 (비공개)
├── requirements.txt       # 필요 패키지 목록
└── README.md              # 프로젝트 설명


✅ 사용 기술 스택
Backend: Python, Flask
AI API: OpenAI GPT
지도/장소 검색: Kakao Local API
영상 검색: YouTube Data API v3
기타: markdown, dotenv, requests