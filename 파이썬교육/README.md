# 파이썬 → 머신러닝 교육 자료

《파이썬 머신러닝 완벽 가이드》 1~4장을 수업하기 위한 파이썬 교재입니다. **파이썬을 처음 가르치는 강사도 코드 한 줄 한 줄을 설명할 수 있도록** 모든 줄에 주석을 달고, 실제 실행 결과와 "학생에게 이렇게 설명하세요" 포인트를 붙였습니다.

## 진행 순서

| 단계 | 문서 | 내용 |
|---|---|---|
| 1 | [01_기초.md](01_기초.md) | 자료형 · 연산자 · 문자열 처리 · 리스트 · 제어문 · 함수 · 입출력 · 클래스 (+ 꼭 필요한 추가 개념) |
| 2 | [02_심화_머신러닝코드읽기.md](02_심화_머신러닝코드읽기.md) | 책 1~4장 코드에서 학생들이 막히는 지점 — "왜 4개로 받지?", "왜 `.sum().sum()`?", "왜 괄호가 있다 없다 하지?" 등 — 을 반환 타입으로 해설 |

## 기본 커리큘럼에 추가한 개념

원래 기초 커리큘럼(자료형/연산자/문자열/리스트/제어문/함수/입출력/클래스)에 없지만, 책 코드를 이해하는 데 꼭 필요해서 [01_기초.md](01_기초.md)에 넣은 것들입니다.

| 추가 개념 | 이게 없으면 설명이 안 되는 책 코드 |
|---|---|
| 튜플 · **언패킹** | `X_train, X_test, y_train, y_test = train_test_split(...)` |
| 딕셔너리 | `GridSearchCV(param_grid={...})`, `best_params_`, hyperopt 검색 공간 |
| 집합 | `unique()`, `nunique()` 의 개념 |
| `None` | `df.drop(..., inplace=True)` 의 결과, `arr.sort()` 의 결과 |
| 리스트 컴프리헨션 · 한 줄 if | `[1 if x > 0.5 else 0 for x in pred_probs]` |
| 람다 | `df['Age'].apply(lambda x: ...)` |
| 기본값 · 키워드 인자 | `DecisionTreeClassifier(max_depth=3, random_state=156)` |
| 예외 처리 · 에러 읽는 법 | 학생 스스로 디버깅 |
| 모듈 · import · as | `import numpy as np`, `from sklearn.tree import ...` |
| 상속 | `class MyDummyClassifier(BaseEstimator):` |
| 객체 · 메서드 · 속성 · **점(.)** | `df.isna().sum().sum()`, `df.shape` vs `df.head()` |

## 실습 환경

- [Google Colab](https://colab.research.google.com/) 권장 (설치 불필요). 또는 Anaconda 의 Jupyter Notebook.
- 모든 예제는 인터넷 연결이나 별도 데이터 파일 없이 실행됩니다 (사이킷런 내장 데이터 / 코드로 만든 작은 표 사용).
- 문서의 실행 결과는 Python 3.10 · NumPy 1.26 · pandas 2.2 · scikit-learn 1.6 에서 실제로 실행해 얻은 값입니다. 버전에 따라 숫자 끝자리나 출력 모양이 조금 다를 수 있습니다.
- XGBoost · LightGBM · hyperopt 예제(심화 7장)는 `pip install xgboost lightgbm hyperopt` 가 필요합니다.
