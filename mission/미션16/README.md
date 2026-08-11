# 미션16 - 영화 박스오피스 데이터 수집 및 분석

씨네21 웹 스크래핑과 KOBIS 오픈API로 박스오피스 데이터를 수집·분석한 프로젝트

### 사용 기술
- Python (requests, BeautifulSoup, pandas)
- KOBIS Open API
- KoNLPy, WordCloud, matplotlib

### 데이터 수집
- 씨네21 랭킹 65위 영화의 상세정보·전문가 리뷰를 BeautifulSoup으로 수집
- 랭킹 목록은 JS 렌더링 페이지라 개발자도구로 실제 데이터 요청을 찾아 API 방식으로 우회 수집
- KOBIS 14일치 일별 박스오피스 수집

### 분석 과정
- 개봉 요일 vs 관객수, 전문가 평점 vs 관객수 상관관계 분석
- 전문가 리뷰 텍스트 분석 (형태소 분석, 키워드 빈도, 워드클라우드)

### 파일 구성
- `미션16_1팀_김륜영.ipynb` : 수집 및 분석 코드
- `cine21_movie_info.csv` : 영화 상세정보
- `cine21_reviews.csv` : 전문가 리뷰
- `kobis_boxoffice.csv` : 일별 박스오피스

### 주요 인사이트
- 수요일 개봉작이 편수·흥행 모두 압도적으로 우세
- 전문가 평점과 흥행은 거의 무관 (상관계수 -0.08)
