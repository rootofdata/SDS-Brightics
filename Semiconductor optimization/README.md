## 스마트팩토리 반도체 공정 최적화

### 프로젝트 개요 및 목적
#### 주제 : 분류 알고리즘을 통한 고장 감지 및 예측
#### 목적 : 반도체 공정 과정에서 관측한 센서 데이터를 기반으로 불량품을 분류하고 예측하여 생산 공정 및 스마트 팩토리 운영의 효율성 증대

### 결과 요약
(1) 시각화 분석
- 주어진 데이터의 Boxplot을 비교하여 직관적으로 어떠한 피처가 영향을 끼치는지에 대해 알고 이를 조절하여 수율을 높일 수 있다.  
(2) MLP 분류 모델 사용  
- 알고리즘 별 성능의 경우 Activation은 tanh를, Solver는 adam을 적용한 다층 퍼셉트론 분류 모델이 불량률 기준 f1 score가 0.884로 높은 성능을 보였다.   
(3) 피처 중요도    
- 피처 중요도에 따라 점도 차이와 밀도 차이를 줄일 수 있다면 수율과 공정 품질을 높일수 있으므로 공정4에서는 점도를, 공정1에서는 밀도의 차이를 줄이는데 노력을 가한다.   
- 공정 품질 저하를 유발하는 변수의 분포에 따라 공정 품질 저하를 조기감지하고 이에 따라 대응할 수 있는 해결책을 제시할 수 있다   
  
#### 시각화 분석의 결과와 MLP모델의 평가지표, 피처 중요도에 따라 공정 품질을 높이고 불량률을 낮추는 등을 통해 결과값을 도출한다.   


### 결론  
(1) Brightics 플랫폼을 통한 시각화 분석   
- 브라이틱스 내 시각화 툴을 이용하여 양품과 불량품의 차이를 한 눈에 알 수 있다.  
(2) 품질 비용 절감   
- 구축된 분류 알고리즘을 이용하여 불량률을 사전에 검출해 낼 경우 신뢰도를 향상시키고 품질 비용을 절감할 수 있다는 점   
(3) 반도체 공정 자동화  
- 만약 실제현장에서 모델링을 활용한다면, 반도체 공정에 브라이틱스를 적용하여 개발의 적합성과 성능 고도화를 하게 될 것으로 기대된다  
(4) 추가적인 검사 도출     
- 구축된 프로세스를 통하여 제품의 품질 상태를 확인하고 추가적으로 검사 항목을 도출함으로써 잠재적인 불량 발생률을 줄이는데 기여할 수 있을 것이다.   
  
#### 본 공정에서 뿐만 아니라 다른 공정과 검사에서도 브라이틱스의 본 프로세스를 적용하여 품질의 성능을 높일 수 있다.   

### 추후연구    
     
(1) 결측값 대치법  
- 결측값 대치법에서 KNN Imputation 외에 MVNI, MICE 등을 사용한다면 더 나은 결과값을 도출할 수 있다.   
(2) 하이퍼파라미터 최적화     
- MLP의 파라미터 중 learning rate initial, Max Iteration, Tolerance,dropout 등을 조정하며 모델의 성능을 높일 수 있다.   
(3) 변수간 상호의존성 파악    
- 공정 변수간 상관성 등 Feature learning 이나 feature engineering 등을 통하여 더 나은 예측모델을 구축할 수 있다.   
(4) 이상치 탐지       
- etching 공정에서 화학 반응물 이용해서 over etch인지 아닌지 판단하는 프로세스를 구성할 수 있다.  

![image](https://github.com/rootofdata/SDS-Brightics/assets/86711374/f2e915a5-8aaf-4f82-9484-4ed20e7342fd)
![image](https://github.com/rootofdata/SDS-Brightics/assets/86711374/d90476b9-b38b-4f06-b19e-59fd71d3e7a6)
![image](https://github.com/rootofdata/SDS-Brightics/assets/86711374/107805fd-aa38-43ab-9b95-93963c9b44e0)
![image](https://github.com/rootofdata/SDS-Brightics/assets/86711374/b4ac1787-41ce-4b44-b945-9081770d952c)
![image](https://github.com/rootofdata/SDS-Brightics/assets/86711374/8799bfda-f869-46d5-9221-73d11e1a869c)
![image](https://github.com/rootofdata/SDS-Brightics/assets/86711374/52b30367-d8de-4b0b-9ba5-c19634ef387a)
![image](https://github.com/rootofdata/SDS-Brightics/assets/86711374/0f8700c1-d431-4135-a46a-b22d55359546)
![image](https://github.com/rootofdata/SDS-Brightics/assets/86711374/af5e14c2-b27b-4d1b-aca9-fb22096166cc)
![image](https://github.com/rootofdata/SDS-Brightics/assets/86711374/2d66e4ab-4f9b-4fbe-8e35-7d13078af41d)
![image](https://github.com/rootofdata/SDS-Brightics/assets/86711374/5ce3f375-795c-4c92-9f25-adedb45919a3)
![image](https://github.com/rootofdata/SDS-Brightics/assets/86711374/efd83400-4e01-42c8-8cf4-99c8305ca1af)
![image](https://github.com/rootofdata/SDS-Brightics/assets/86711374/3722ff7a-ecb9-4605-bb04-54c422ffc17d)
![image](https://github.com/rootofdata/SDS-Brightics/assets/86711374/4a453e59-3d30-4a66-b4a8-6cb167fa5235)
![image](https://github.com/rootofdata/SDS-Brightics/assets/86711374/9de1732c-bb53-4096-b156-d910f8627ab1)
![image](https://github.com/rootofdata/SDS-Brightics/assets/86711374/5a322487-d872-42a6-9973-ef7a742528a8)
![image](https://github.com/rootofdata/SDS-Brightics/assets/86711374/1486734b-29c1-4649-955b-ba99d9fd8758)
![image](https://github.com/rootofdata/SDS-Brightics/assets/86711374/62acf0f2-2287-45b1-bdbe-617e9e470d39)
![image](https://github.com/rootofdata/SDS-Brightics/assets/86711374/e1897347-4063-49c1-821b-3d5f12ea85f0)
![image](https://github.com/rootofdata/SDS-Brightics/assets/86711374/06de716d-5530-4a1c-bc8b-9d48aad441c2)
![image](https://github.com/rootofdata/SDS-Brightics/assets/86711374/620bad2f-259c-4b77-b851-5ff4872b43c4)
![image](https://github.com/rootofdata/SDS-Brightics/assets/86711374/c35b17c8-cf36-472f-8564-6e86e67200d9)
![image](https://github.com/rootofdata/SDS-Brightics/assets/86711374/699d52a7-0364-4985-a3b2-16b9fe869aee)
![image](https://github.com/rootofdata/SDS-Brightics/assets/86711374/436cb28f-a0ce-418f-830c-89a0446c4ab1)
![image](https://github.com/rootofdata/SDS-Brightics/assets/86711374/933a4363-7d20-44ac-836e-81e37962f235)
