# 🔬 여행 성향 분석 - 이론적 배경 및 연구 자료

## 📚 참고한 심리학 이론 및 연구

### 1. **Big Five 성격 이론 (Five Factor Model)**

**출처**: Costa, P. T., & McCrae, R. R. (1992). *NEO PI-R Professional Manual*

**5가지 성격 특성:**
- **개방성 (Openness)** → 모험심, 새로운 경험 추구
- **성실성 (Conscientiousness)** → 계획성, 조직력
- **외향성 (Extraversion)** → 사교성, 활동성
- **친화성 (Agreeableness)** → 협조성, 순응성
- **신경증 (Neuroticism)** → 정서적 안정성

**적용:**
- 우리의 "계획성 vs 즉흥성" 축 → 성실성
- "사교성 vs 독립성" 축 → 외향성
- "모험심 vs 안전추구" 축 → 개방성
- "정서적 안정성" 축 → 신경증 (역방향)

**참고 사이트:**
- https://www.psychologytoday.com/us/basics/big-5-personality-traits
- https://www.verywellmind.com/the-big-five-personality-dimensions-2795422

---

### 2. **여행 동기 이론 (Travel Motivation Theory)**

**출처**: Crompton, J. L. (1979). "Motivations for pleasure vacation"

**7가지 여행 동기:**
1. 일상 탈출 (Escape)
2. 휴식과 이완 (Relaxation)
3. 자아 탐색 (Self-exploration)
4. 사회적 교류 (Social interaction)
5. 명성 추구 (Prestige)
6. 새로운 경험 (Novelty)
7. 교육과 학습 (Education)

**적용:**
- 휴식 선호 → Cozy Healer
- 새로운 경험 → Free Spirit, Action Seeker
- 사회적 교류 → Easy-Going Companion
- 자아 탐색 → Lone Wanderer

**참고 논문:**
- Crompton, J. L. (1979). Annals of Tourism Research, 6(4), 408-424
- Pearce, P. L. (2005). *Tourist Behaviour: Themes and Conceptual Schemes*

---

### 3. **Plog의 여행자 성격 유형론**

**출처**: Plog, S. C. (1974). "Why Destination Areas Rise and Fall in Popularity"

**여행자 스펙트럼:**
```
Psychocentric ←――――――――――――→ Allocentric
(안전추구형)                    (모험추구형)
```

**특징:**
- **Psychocentric (내향적)**: 익숙한 장소, 계획된 여행, 안전 중시
- **Allocentric (외향적)**: 새로운 장소, 모험, 자유로운 여행

**적용:**
- Master Planner, Cozy Healer → Psychocentric
- Free Spirit, Action Seeker → Allocentric
- Easy-Going, Trend Setter → Mid-centric

**참고 자료:**
- Plog, S. C. (2001). Journal of Travel Research, 39(3), 244-252

---

### 4. **Cohen의 여행자 역할 이론**

**출처**: Cohen, E. (1972). "Toward a Sociology of International Tourism"

**4가지 여행자 유형:**
1. **Organized Mass Tourist** → Master Planner
2. **Individual Mass Tourist** → Trend Setter
3. **Explorer** → Free Spirit
4. **Drifter** → Lone Wanderer

**참고 논문:**
- Cohen, E. (1972). Social Research, 39(1), 164-182

---

### 5. **MBTI (Myers-Briggs Type Indicator)**

**출처**: Myers, I. B., & McCaulley, M. H. (1985)

**4가지 선호 지표:**
- **E (외향) vs I (내향)** → 사교성 vs 독립성
- **S (감각) vs N (직관)** → 현실적 vs 상상적
- **T (사고) vs F (감정)** → 논리적 vs 감성적
- **J (판단) vs P (인식)** → 계획적 vs 즉흥적

**여행 성향 매핑:**
- **ISTJ, ESTJ** → Master Planner
- **ENFP, ENTP** → Free Spirit
- **ISFP, INFP** → Cozy Healer
- **ESFP, ESTP** → Action Seeker

**참고 사이트:**
- https://www.16personalities.com/
- https://www.myersbriggs.org/

---

### 6. **소비자 라이프스타일 분석 (VALS Framework)**

**출처**: SRI International (Stanford Research Institute)

**8가지 소비자 유형:**
- Innovators → Trend Setter
- Thinkers → Master Planner
- Achievers → Action Seeker
- Experiencers → Free Spirit
- Believers → Easy-Going
- Strivers → Local Gourmet
- Makers → Lone Wanderer
- Survivors → Cozy Healer

**참고 사이트:**
- https://www.strategicbusinessinsights.com/vals/

---

## 🧪 실험 설계 및 검증

### 1. **질문 설계 방법론**

**참고**: Likert Scale & Semantic Differential Scale

**우리의 접근:**
- 각 질문은 2-3개의 선택지 제공
- 극단적 선택지로 명확한 성향 파악
- 상황 기반 질문으로 실제 행동 예측

**검증 방법:**
```
1. 파일럿 테스트 (N=50)
2. 신뢰도 분석 (Cronbach's Alpha)
3. 타당도 검증 (요인 분석)
4. 재검사 신뢰도 (Test-Retest Reliability)
```

---

### 2. **유형 분류 알고리즘**

**참고**: K-Means Clustering, Decision Tree

**우리의 방법:**
1. **점수 집계**: 각 축별 점수 합산
2. **우선순위 규칙**: 특정 조건 만족 시 즉시 분류
3. **가중치 적용**: 주요 특성에 2배 가중치
4. **최종 판별**: 가장 높은 점수의 유형 선택

**정확도 목표:**
- 분류 일관성: 85% 이상
- 사용자 만족도: 80% 이상

---

### 3. **추천 시스템 기준**

**참고**: Collaborative Filtering, Content-Based Filtering

**추천 로직:**
```javascript
1. 유형별 선호 카테고리 매핑
2. 지역별 장소 필터링
3. 평점 기반 정렬
4. 다양성 보장 (카테고리 균형)
```

---

## 📊 벤치마크 사이트 및 서비스

### 1. **16Personalities (MBTI 기반)**
- URL: https://www.16personalities.com/
- 특징: 5가지 성격 특성 측정, 시각화 우수
- 참고 요소: UI/UX, 결과 표현 방식

### 2. **Airbnb 여행 스타일 퀴즈**
- 특징: 간단한 질문으로 여행 추천
- 참고 요소: 질문 설계, 추천 알고리즘

### 3. **Expedia 여행자 유형 테스트**
- 특징: 여행 선호도 기반 분류
- 참고 요소: 유형 분류 체계

### 4. **TripAdvisor 여행 성향 분석**
- 특징: 리뷰 데이터 기반 추천
- 참고 요소: 데이터 활용 방식

### 5. **Booking.com 여행 스타일 매칭**
- 특징: 숙소 선호도와 연계
- 참고 요소: 실용적 추천 시스템

---

## 🎯 우리 시스템의 차별점

### 1. **한국 여행 특화**
- 국내 여행지 데이터베이스
- 한국인 여행 패턴 반영
- 지역별 특성 고려

### 2. **실용적 추천**
- 실제 장소 데이터 연동
- 예산, 교통수단 고려
- 일정 자동 생성

### 3. **AI 기반 최적화**
- 성향 기반 일정 자동 생성
- 실시간 추천 업데이트
- 학습 기반 개선

---

## 📖 추가 참고 문헌

### 학술 논문
1. Leiper, N. (1990). "Tourist attraction systems". *Annals of Tourism Research*, 17(3), 367-384.
2. Gnoth, J. (1997). "Tourism motivation and expectation formation". *Annals of Tourism Research*, 24(2), 283-304.
3. Iso-Ahola, S. E. (1982). "Toward a social psychological theory of tourism motivation". *Annals of Tourism Research*, 9(2), 256-262.

### 서적
1. Pine, B. J., & Gilmore, J. H. (1999). *The Experience Economy*
2. Urry, J. (2002). *The Tourist Gaze*
3. MacCannell, D. (1976). *The Tourist: A New Theory of the Leisure Class*

### 온라인 리소스
1. **Psychology Today** - https://www.psychologytoday.com/
2. **Verywell Mind** - https://www.verywellmind.com/
3. **Simply Psychology** - https://www.simplypsychology.org/
4. **한국관광공사 관광지식정보시스템** - https://know.tour.go.kr/

---

## 🔄 지속적 개선 계획

### Phase 1: 데이터 수집 (현재)
- 사용자 응답 데이터 수집
- 추천 만족도 조사
- A/B 테스트 실시

### Phase 2: 알고리즘 개선
- 머신러닝 모델 도입
- 개인화 추천 강화
- 정확도 향상

### Phase 3: 확장
- 해외 여행 지원
- 다국어 지원
- 소셜 기능 추가

---

## 📝 연구 윤리

### 데이터 수집 원칙
1. **투명성**: 사용자에게 데이터 사용 목적 명시
2. **동의**: 명시적 동의 후 데이터 수집
3. **익명성**: 개인 식별 정보 제거
4. **보안**: 안전한 저장 및 전송

### 편향 방지
1. 다양한 연령대, 성별, 지역 고려
2. 문화적 편견 배제
3. 정기적 검토 및 업데이트

---

## 🤝 기여 및 피드백

연구 자료 추가, 알고리즘 개선 제안을 환영합니다!

**Contact**: 프로젝트 메인 README 참조

---

**Version**: 1.0.0  
**Last Updated**: 2026-05-20  
**Compiled by**: 떠나GO Research Team
