# 🍳 PyTorch Recipe Recommendation System

Neural Collaborative Filtering (NCF) 기반 AI 레시피 추천 시스템

## 📌 프로젝트 정보

- **시작일**: 2025-10-30
- **목표 완료일**: 2025-12-04 (5주)
- **모델**: Neural Collaborative Filtering (NCF)
- **데이터**: Food.com (레시피 23만 개, 리뷰 73만 개)

## 🎯 목표

이 프로젝트의 목표는:

1. **AI 모델 구축**: PyTorch로 추천 시스템 모델 만들기
2. **성능 달성**: Test AUC 0.83 이상 달성
3. **실제 배포**: FastAPI로 웹 서버 구축
4. **포트폴리오**: GitHub에 완성된 프로젝트 올리기

## 🛠️ 기술 스택

**Backend**: PyTorch + FastAPI + Python 3.13.5  
**Frontend**: TypeScript + Next.js (예정)  
**Database**: CSV 데이터 (초기), PostgreSQL (확장)  
**Deployment**: Docker (예정)

## 📁 프로젝트 구조

```
pytorch-recipe-recommendation/
├── data/              # 데이터셋
├── models/            # NCF 모델 코드
├── training/          # 학습 스크립트
├── api/              # FastAPI 서버
├── notebooks/        # Jupyter 노트북
├── configs/          # 설정 파일
├── checkpoints/      # 학습된 모델
├── requirements.txt
└── README.md
```

## 🚀 빠른 시작

### 1. 환경 설정

```bash
cd pytorch-recipe-recommendation
source venv/bin/activate
pip install -r requirements.txt
```

### 2. 데이터 준비 (예정)

```bash
kaggle datasets download -d shuyangli94/food-com-recipes-and-user-interactions -p ./data
cd data && unzip food-com-recipes-and-user-interactions.zip
```

### 3. 모델 학습 (예정)

```bash
python training/preprocess.py
python training/train.py
```

### 4. API 서버 실행 (예정)

```bash
uvicorn api.main:app --reload
```

## 📊 예상 성능

AUC(Area Under Curve) : 추천 모델이 좋아하는것과 싫어할 것을 얼마나 구분을 하는가  
NDCG@10 (Normalized Discounted Cumulative Gain) : 추천한 10개 중에서 좋은것을 사위에 배치했는가?



| 지표 | 목표 | 설명 |
|------|------|------|
| AUC | 0.83+ | 모델 분류 성능 |
| NDCG@10 | 0.38+ | 추천 순서 성능 |
| 응답 시간 | 200ms | API 서빙 속도 |

## 📚 기술 설명

### NCF (Neural Collaborative Filtering)

추천 시스템의 최신 기법으로, 두 가지 경로를 융합합니다:

- **GMF**: 전통적인 행렬 분해 방식
- **MLP**: 딥러닝 신경망 방식
- **Fusion**: 두 경로 결합

## 📅 로드맵

- [x] Week 1: 프로젝트 초기 설정 + 환경 준비
- [ ] Week 2: 데이터 수집 및 탐색 (EDA)
- [ ] Week 3: 모델 구현 및 첫 학습
- [ ] Week 4: 성능 최적화
- [ ] Week 5: API 구축 및 배포

## 🧪 테스트

```bash
python -c "import torch; print(f'PyTorch: {torch.__version__}')"
python -c "import pandas; print(f'pandas: {pandas.__version__}')"
```

## 📝 Velog 시리즈

1. 왜 레시피 추천 AI를 만드는가?
2. Python 가상환경이 필요한 이유
3. 패키지 하나하나 해석
4. 딥러닝 기법 정리

## 🤝 참고 자료

- [NCF 논문](https://arxiv.org/abs/1708.05031)
- [PyTorch 공식 문서](https://pytorch.org/docs/)
- [Food.com Dataset](https://www.kaggle.com/datasets/shuyangli94/food-com-recipes-and-user-interactions)

## 👤 작성자

- 개발 시작: 2025-10-30

---

**마지막 업데이트**: 2025-10-31
