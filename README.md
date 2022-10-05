# House
#### 부동산 유형별 집값을 예측해 봅시다!

## pycaret 사용법 : 참고사이트는 분류형(classification)이므로 주의!
- https://michael-fuchs-python.netlify.app/2022/01/01/automl-using-pycaret-classification/
- https://sthsb.tistory.com/31
- https://minimin2.tistory.com/137

## pycaret를 활용한 결측치 처리
- pycaret은 imputation_type으로 결측치를 처리할 수 있고, type엔 'Simple', 'iterative'이 있습니다
- imputation_type = 'simple' or 'iterative'
- simple은 fillna처럼 mean, median, most_frequent 등 결측치를 채우는 메소드를 선택해야 합니다
- Iterative Imputer는 다중대체법이라고도 부릅니다. 다중대체법은 여러 개의 데이터를 새로 만들어서 머신이 결측치를 반복적으로 채워 본다고 합니다
- 다중대체법에 활용되는 모델은 lightgbm(디폴트)이며 이에 대한 자세한 알고리즘은 이해하지 못했습니다..ㅜㅜ
- 다중대체법 : https://continuous-development.tistory.com/160

## 다양한 모델로 Iterative imputer 활용하기
- Iterative imputer는 수치형 데이터 뿐 아니라 범주형 데이터까지 알아서 채워주므로 유용합니다.
- lightgbm이 아닌 다른 모델을 활용하고 싶다면?
- categorical_iterative_imputer='knn'
- numeric_iterative_imputer='knn'
- 수치형과 범주형 결측치를 다른 모델로 채워볼 수 있습니다.
- knn이외에도 다양한 모델이 활용될 수 있으니 다양한 모델들로 성능을 비교해 보는 것이 좋을 것 같습니다!
- https://www.linkedin.com/pulse/iterative-imputation-pycaret-22-antoni-baum

## 결론
- 조사 결과 iterative imputer와 프로젝트에서 배운 knn imputer는 결측치를 활용하는 다른 방법론입니다!
- https://medium.com/@blant.jesse/imputing-missing-values-with-the-new-knnimputer-and-iterativeimputer-methods-110270738c4
- 어쩌면 simple imputer를 활용해 결측치를 채우는 것이 중요한 데이터일 수도 있습니다.
- pycaret를 활용해 결측치를 처리할 땐 다양한 방법(simple imputer, knn imputer, iterative imputer 등)을 시도해 봐야 할 것 같습니다. 
  
