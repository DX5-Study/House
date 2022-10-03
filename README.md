# House
#### 부동산 유형별 집값을 예측해 봅시다!

## pycaret 사용법 : 참고사이트는 분류형(classification)이므로 주의!
- https://michael-fuchs-python.netlify.app/2022/01/01/automl-using-pycaret-classification/
- https://sthsb.tistory.com/31
- https://minimin2.tistory.com/137

## pycaret를 활용한 결측치 처리
- pycaret은 imputation_type으로 결측치를 처리할 수 있고, type엔 'Simple', 'IterativeImputer'이 있습니다
- simple은 fillna처럼 mean, median, most_frequent 등 결측치를 채우는 메소드를 선택해야 합니다
- IterativeImputer는 다중대체법이라고도 부릅니다. 다중대체법은 여러 개의 데이터를 새로 만들어서 머신이 결측치를 반복적으로 채워 본다고 합니다
- 다중대체법에 활용되는 모델은 lightgbm이며 이에 대한 자세한 알고리즘은 이해하지 못했습니다..ㅜㅜ
- 다중대체법 : https://continuous-development.tistory.com/160
- IterativeImputer type은 수치형 데이터 뿐 아니라 범주형 데이터까지 알아서 채워주므로 유용합니다.

## 결론
- pycaret를 활용해 결측치를 처리할 땐 매우 중요하게 매워야 할 결측치는 비지도 학습 혹은 simple imputer로 직접 채워주고, 
  애매하고 결측치 양이 적은 경우에만 imputation_tyep = 'IterativeImputer'로 시간을 절약합시다!
  
