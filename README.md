# 떠나GO (TteonaGO) ✈️

![Uploading 떠나고 데모 영상 (30초이하).gif…]

> AI 기반 개인 맞춤형 여행 일정 플래너

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![Node.js](https://img.shields.io/badge/Node.js-14+-green.svg)](https://nodejs.org/)
[![React](https://img.shields.io/badge/React-18.2-blue.svg)](https://reactjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.2-blue.svg)](https://www.typescriptlang.org/)

## 📋 프로젝트 소개

**떠나GO**는 사용자의 여행 성향을 분석하여 맞춤형 여행 일정을 추천하는 AI 기반 여행 플래너입니다. 
Big Five 성격 이론과 Plog의 여행자 성향 이론을 기반으로 사용자에게 최적화된 여행지와 일정을 제안합니다.

### 🎬 데모

웹 애플리케이션을 실행하면 다음 기능들을 사용할 수 있습니다:
- 실시간 성향 분석 및 여행 유형 진단
- 지역/카테고리별 맞춤 장소 추천
- 드래그 앤 드롭 방식의 직관적 일정 편집
- 작성한 일정 라이브러리 관리
- 즐겨찾기 및 AI 챗봇 기능

### ✨ 주요 기능

#### 1. 🎯 여행 성향 분석
- 12문항의 심리 테스트로 8가지 여행 유형 분석
- Big Five 기반 성향 프로파일 생성
- 실시간 성향 변화 감지 및 추적

#### 2. 🤖 AI 맞춤 추천
- 성향에 맞는 여행지, 맛집, 카페, 숙소 추천
- 지역별/카테고리별 필터링
- 가격대별 검색 및 평점 기반 정렬
- 계절별, 테마별 추천 섹션

#### 3. 📅 스마트 일정 관리
- 직관적인 일정 작성 인터페이스
- 날짜별 슬롯 기반 일정 구성
- AI 자동 장소 추천 기능
- 시간대 설정 및 카테고리별 구분
- 메모 및 교통수단 정보 저장

#### 4. 📚 라이브러리
- 작성한 일정 자동 저장
- 일정 목록 조회 및 검색
- 카드 클릭으로 상세 정보 팝업
- 일정 수정 및 삭제 기능
- localStorage 기반 영구 저장

#### 5. ⭐ 즐겨찾기
- 마음에 드는 장소 북마크
- 여행 일정 즐겨찾기
- 즐겨찾기 페이지에서 통합 관리
- 라이브러리와 연동

#### 6. 💬 AI 챗봇 (개발 중)
- 실시간 여행지 추천
- 자연어 질문 응답
- 맞춤형 일정 생성 지원

## 🎨 8가지 여행 유형

1. **🛋️ 코지 힐러** - 편안한 휴식 중심
2. **🍜 로컬 미식가** - 현지 음식 탐험
3. **🏛️ 역사 탐험가** - 문화유산 방문
4. **🌄 액션 시커** - 스릴 넘치는 활동
5. **📸 감성 수집가** - 인생샷 명소
6. **🚶 론 원더러** - 혼자만의 여행
7. **🎉 프리 스피릿** - 즉흥적 모험
8. **👨‍👩‍👧‍👦 패밀리 플래너** - 가족 여행 최적화

## 🏗️ 아키텍처

### 프로젝트 구조

```
떠나GO/
├── cmd/
│   └── server/
│       └── main.py              # Python 데모 실행 파일
├── internal/                    # Python 백엔드 모듈
│   ├── models/                  # 데이터 모델 (User, TravelItem, Preference 등)
│   │   ├── user.py
│   │   ├── preference.py
│   │   ├── travel_item.py
│   │   └── itinerary.py
│   ├── preference/              # 성향 분석 AI
│   │   ├── analyzer.py          # 성향 프로파일 생성/업데이트
│   │   └── clustering.py        # 유사 사용자 클러스터링
│   ├── recommendation/          # 추천 AI
│   │   ├── query_parser.py      # 자연어 쿼리 파싱
│   │   ├── ranker.py            # 다중 점수 기반 랭킹
│   │   ├── filter.py            # 필터링 로직
│   │   └── summarizer.py        # 리뷰 요약
│   └── planning/                # 일정 생성 AI
│       ├── generator.py         # 일정 자동 생성
│       ├── optimizer.py         # 동선 최적화 (TSP)
│       └── scheduler.py         # 시간 슬롯 배치
├── web/                         # 프론트엔드
│   ├── public/                  # 메인 웹 애플리케이션 (Vanilla JS)
│   │   ├── index.html           # 메인 페이지
│   │   ├── app-simple.js        # 핵심 로직 (2800+ 줄)
│   │   ├── data.js              # 장소 데이터베이스
│   │   └── style.css            # 스타일시트
│   ├── personality-analysis/    # 성향 분석 React 모듈
│   │   ├── src/
│   │   │   ├── App.tsx          # 메인 컴포넌트
│   │   │   ├── components/      # Quiz, Result 컴포넌트
│   │   │   ├── data/            # 질문/유형 데이터
│   │   │   └── utils/           # 분석 알고리즘
│   │   └── package.json
│   ├── scripts/                 # Python-Node.js 연동 스크립트
│   │   ├── preference_init.py
│   │   ├── recommend_search.py
│   │   └── plan_generate.py
│   ├── server.js                # Express 서버
│   └── package.json
├── .gitignore
├── README.md
├── ARCHITECTURE.md              # 상세 아키텍처 문서
├── SPECIFICATION.md             # 기능 명세
└── IMPLEMENTATION.md            # 구현 가이드
```

### 기술 스택

#### 프론트엔드
- **메인 앱**: Vanilla JavaScript (ES6+)
  - 커스텀 토스트 알림 시스템
  - 드래그 앤 드롭 일정 관리
  - localStorage 기반 상태 관리
- **성향 분석 모듈**: React 18.2 + TypeScript 5.2
  - Vite 빌드 시스템
  - 컴포넌트 기반 아키텍처
- **스타일링**: 순수 CSS3
  - CSS Variables (다크모드 대응)
  - Flexbox/Grid 레이아웃
  - 반응형 디자인

#### 백엔드
- **언어**: Python 3.8+
- **웹 서버**: Node.js Express 4.18
- **API**: RESTful API (Python-Node.js 연동)
- **데이터**: JSON 기반 (추후 DB 확장 예정)

## 🚀 시작하기

### 필수 요구사항

- **Python**: 3.8 이상
- **Node.js**: 14 이상
- **패키지 관리자**: pip, npm

### 설치 방법

#### 1. 저장소 클론
```bash
git clone https://github.com/yourusername/tteonago.git
cd tteonago
```

#### 2. Python 환경 설정

**방법 A: 가상환경 사용 (권장)**
```bash
# Windows
python -m venv .venv
.venv\Scripts\activate

# macOS/Linux
python3 -m venv .venv
source .venv/bin/activate
```

**방법 B: Anaconda 사용**
```bash
conda create -n go python=3.8
conda activate go
```

#### 3. Python 패키지 설치
```bash
pip install python-dotenv
```

**필요한 주요 패키지:**
- `python-dotenv`: 환경 변수 관리
- 추후 확장 시: `numpy`, `scikit-learn`, `pandas`

#### 4. Node.js 패키지 설치
```bash
cd web
npm install
```

**설치되는 패키지:**
- `express`: 웹 서버
- `cors`: CORS 처리

#### 5. 환경 변수 설정 (선택사항)
```bash
# 프로젝트 루트에 .env 파일 생성
# API 키 등 필요한 경우 추가
```

### 실행 방법

#### 방법 1: 웹 애플리케이션 실행 (권장)

```bash
cd web
npm start
```

웹 브라우저에서 `http://localhost:3000` 접속

**실행되는 기능:**
- ✅ 성향 분석 (프론트엔드)
- ✅ 장소 추천 (프론트엔드 데이터)
- ✅ 일정 관리
- ✅ 라이브러리
- ✅ 즐겨찾기
- 🔄 AI 챗봇 (Python 연동 필요)

#### 방법 2: Python AI 데모 실행

```bash
# 프로젝트 루트에서
python cmd/server/main.py
```

**데모 내용:**
- Preference AI (성향 분석)
- Recommendation AI (추천 알고리즘)
- Planning AI (일정 생성)
- User Clustering (유사 사용자 찾기)

### 개발 모드

#### React 성향 분석 모듈 개발
```bash
cd web/personality-analysis
npm run dev
```

#### React 빌드
```bash
cd web/personality-analysis
npm run build
```

빌드 결과물은 `web/public/web/personality-analysis/`에 생성됩니다.

## 📖 사용 방법

### 1️⃣ 성향 분석 시작하기

1. **홈페이지 접속**
   - 네비게이션에서 "성향 분석" 클릭

2. **퀴즈 응답**
   - 12개의 질문에 성향에 맞게 답변
   - 진행률 표시바로 현재 위치 확인
   - "이전" 버튼으로 답변 수정 가능

3. **결과 확인**
   - 8가지 유형 중 본인의 여행 성향 확인
   - 성향 축 막대 그래프로 세부 특성 파악
   - 같은 유형 추천 장소 확인

4. **추천 활용**
   - "여행 계획 작성하기" 버튼으로 일정 페이지 이동
   - 또는 "다시 검사하기"로 재진단

### 2️⃣ 장소 추천 탐색하기

1. **추천 섹션 둘러보기**
   - 나와 비슷한 유형 추천
   - 계절별 추천 (봄/여름/가을/겨울 테마)
   - 테마별 추천 (힐링/액티비티/감성/맛집)

2. **검색 및 필터**
   - 상단 검색창에 키워드 입력
   - 필터 버튼으로 상세 조건 설정:
     - 카테고리: 관광지/맛집/카페/숙소/액티비티
     - 지역: 8개 광역권 + 세부 도시
     - 가격: 슬라이더로 범위 설정

3. **장소 상세 보기**
   - 카드 클릭으로 팝업 열기
   - 평점, 주소, 태그 등 상세 정보 확인
   - "즐겨찾기" 버튼으로 북마크

### 3️⃣ 여행 일정 작성하기

1. **기본 정보 입력**
   - 일정 제목
   - 목적지
   - 여행 날짜 (시작일~종료일)
   - 인원 수
   - 교통수단
   - 메모

2. **세부 일정 작성**
   - "세부 일정 작성하기" 클릭
   - 각 Day별로 장소 추가:
     - **AI 추천**: 목적지 기반 자동 추천
     - **직접 추가**: 장소명, 시간, 카테고리 입력
     - **추천에서 추가**: 다중 선택 모드 활성화

3. **일정 편집**
   - 시간 설정: 각 슬롯의 시간 입력
   - 순서 변경: 드래그 앤 드롭 (개발 예정)
   - 슬롯 삭제: X 버튼 클릭

4. **자동 저장**
   - 모든 변경사항 자동으로 localStorage 저장
   - 페이지 새로고침해도 유지

### 4️⃣ 라이브러리 관리하기

1. **일정 목록 보기**
   - "일정" 페이지 → "라이브러리" 탭
   - 저장된 모든 일정 카드로 표시
   - 제목, 목적지, 날짜 정보 확인

2. **일정 상세 보기**
   - 카드 클릭 → 팝업 열림
   - 전체 일정표 확인
   - 일정 정보 및 메모 확인

3. **일정 수정**
   - 팝업에서 "수정하기" 클릭
   - 자동으로 "일정 작성" 탭 전환
   - 현재 작업 중이던 일정은 자동 저장
   - 폼에 데이터 로드되어 수정 가능

4. **일정 삭제**
   - 팝업에서 "삭제" 버튼
   - 확인 후 영구 삭제

### 5️⃣ 즐겨찾기 활용하기

1. **장소 즐겨찾기**
   - 추천 페이지에서 장소 상세 팝업
   - "⭐ 즐겨찾기" 버튼 클릭
   - 즐겨찾기 페이지에서 모아보기

2. **일정 즐겨찾기**
   - 라이브러리에서 일정 상세 팝업
   - "⭐ 즐겨찾기" 토글
   - 즐겨찾기 페이지에서 빠른 접근

3. **라이브러리 이동**
   - 즐겨찾기 페이지 → 여행 일정 섹션
   - "라이브러리 보기" 버튼
   - 일정 페이지의 라이브러리 탭으로 이동

### 6️⃣ AI 챗봇 사용하기 (개발 중)

1. **챗봇 열기**
   - 우측 하단 "💬" 플로팅 버튼 클릭

2. **질문하기**
   - "부산 3박 4일 힐링 여행 추천해줘"
   - "가족 여행하기 좋은 곳은?"
   - "예산 50만원으로 갈 수 있는 곳은?"

3. **장소 추가**
   - 챗봇 추천 결과에서 장소 선택
   - "선택한 장소 일정에 추가" 버튼
   - 자동으로 일정에 반영

## 🔧 핵심 기술

### AI 알고리즘

#### 1. Preference AI (성향 분석)
```python
# 성향 벡터 정규화
preference[tag] = preference[tag] + α × weight × tag_base_weight

# 코사인 유사도 기반 변화 감지
similarity = (vec1 · vec2) / (||vec1|| × ||vec2||)
```

**특징:**
- Big Five 기반 다차원 성향 분석
- 행동 데이터 기반 동적 업데이트
- K-Nearest Neighbors 클러스터링

#### 2. Recommendation AI (추천)
```python
# 다중 점수 기반 랭킹
final_score = 0.4 × similarity +
              0.2 × rating +
              0.2 × preference +
              0.2 × popularity
```

**특징:**
- 자연어 쿼리 파싱 (NER)
- RAG 기반 벡터 검색 (예정)
- TF-IDF 장소 매칭
- 다단계 필터링

#### 3. Planning AI (일정 생성)
```python
# TSP 기반 동선 최적화
distance = Haversine(location1, location2)

# 성향 기반 일정 밀도 조절
density = 0.5 + 0.3 × (1 - healing_score)
```

**특징:**
- Greedy Nearest Neighbor 알고리즘
- 지리적 클러스터링
- 시간 슬롯 자동 배치
- 성향 맞춤 일정 밀도

### 데이터 관리

#### 클라이언트 (localStorage)
```javascript
// 저장 키
- tteonago_plan: 현재 작성 중인 일정
- tteonago_library: 저장된 일정 목록
- tteonago_favorites_places: 즐겨찾기 장소
- tteonago_favorites_plans: 즐겨찾기 일정
```

#### 서버 (향후 확장)
- PostgreSQL: 사용자 데이터, 일정 데이터
- Redis: 세션, 캐싱
- Vector DB (Pinecone/Weaviate): 장소 임베딩

## 📊 알고리즘

### 성향 분석 알고리즘
```python
# K-means 클러스터링 기반
1. 사용자 응답 수집 (12개 질문)
2. 벡터화 및 정규화
3. 사전 학습된 클러스터 중심과 비교
4. 가장 가까운 클러스터 (여행 유형) 반환
```

### 추천 알고리즘
```python
# TF-IDF + 협업 필터링
1. 사용자 성향 태그 추출
2. 장소 태그와 유사도 계산
3. 평점, 거리, 계절성 가중치 적용
4. 상위 N개 추천
```

### 일정 최적화
```python
# 휴리스틱 기반 스케줄링
1. 지역별 장소 그룹화
2. 이동 거리 최소화
3. 카테고리 균형 유지 (관광지, 맛집, 휴식)
4. 시간대 고려 (오전 관광, 점심, 오후 관광, 저녁)
```

## 📝 라이선스

이 프로젝트는 MIT 라이선스 하에 배포됩니다. 자세한 내용은 [LICENSE](LICENSE) 파일을 참조하세요.

## � 주요 파일 설명

### 프론트엔드

| 파일 | 설명 | 라인 수 |
|------|------|---------|
| `web/public/index.html` | 메인 HTML 페이지 | ~800 |
| `web/public/app-simple.js` | 핵심 로직 (상태 관리, 이벤트 처리) | ~2,800 |
| `web/public/data.js` | 장소 데이터베이스, 성향 유형 정의 | ~1,500 |
| `web/public/style.css` | 전체 스타일시트 | ~1,200 |

### 백엔드 (Python)

| 파일 | 설명 |
|------|------|
| `cmd/server/main.py` | AI 시스템 데모 실행 파일 |
| `internal/models/*.py` | 데이터 모델 정의 |
| `internal/preference/analyzer.py` | 성향 분석 알고리즘 |
| `internal/recommendation/ranker.py` | 추천 랭킹 알고리즘 |
| `internal/planning/optimizer.py` | 동선 최적화 (TSP) |

### 문서

| 파일 | 설명 |
|------|------|
| `ARCHITECTURE.md` | 3개 AI 에이전트 상세 설명 |
| `SPECIFICATION.md` | 기능 명세서 |
| `IMPLEMENTATION.md` | 구현 가이드 |

## 💡 트러블슈팅

### 웹 서버가 시작되지 않을 때
```bash
# 포트 3000이 이미 사용 중인 경우
# server.js의 PORT 변수 수정

# 또는 프로세스 종료 (Windows)
netstat -ano | findstr :3000
taskkill /PID <PID> /F
```

### Python 모듈 import 오류
```bash
# sys.path에 프로젝트 루트 추가 확인
# cmd/server/main.py에 이미 구현되어 있음

# 또는 PYTHONPATH 설정
set PYTHONPATH=%CD%  # Windows
export PYTHONPATH=$(pwd)  # macOS/Linux
```

### localStorage 데이터 초기화
```javascript
// 브라우저 개발자 도구 콘솔에서
localStorage.removeItem('tteonago_plan');
localStorage.removeItem('tteonago_library');
localStorage.removeItem('tteonago_favorites_places');
localStorage.removeItem('tteonago_favorites_plans');
```

## �🙏 감사의 말

이 프로젝트는 다음의 이론과 기술을 기반으로 개발되었습니다:

### 학술 이론
- **Big Five 성격 이론** - Costa & McCrae (1992)
- **Plog의 여행자 성향 이론** - Stanley Plog (1974)
- **Crompton의 여행 동기 이론** - John Crompton (1979)
- **Cohen의 여행자 분류** - Erik Cohen (1972)

### 오픈소스 기여
- React Team - UI 라이브러리
- Vite - 빌드 도구
- Express.js - 웹 서버
- Python Community - 과학 컴퓨팅 생태계

### 데이터 출처
- 국내 여행지 정보
- 공공 데이터 포털
- 사용자 생성 콘텐츠

---
