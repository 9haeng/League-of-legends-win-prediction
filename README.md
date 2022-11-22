# League of legends win prediction
-----
![썸네일 2](https://user-images.githubusercontent.com/70729822/203340293-6b0bbe4a-74af-4859-b6cb-218c82a3ecd8.png)

[지난 프로젝트](https://github.com/9haeng/League-of-legends-data-analysis) 를 통해 얻은 결론은 다음과 같습니다.

**1. 진영 별 승리 플랜에는 어느정도 차이가 존재한다.**

  - 블루팀은 OP 챔피언을 먼저 가져올 수 있다는 장점을 활용해 초반 스노우볼링을 극대화 했을 경우 승률이 높다.
  - 레드팀은 블루팀의 초반 강점을 이해하고 초반 오브젝트를 효율적으로 내어주는 대신 `원소 드래곤`을 잘 관리했다면 게임 중후반부터 전세를 뒤집을 수 있다.

**2. 게임 시간대 별 승패에 영향을 미치는 요소**

  - 초반 시간대에 끝난 게임에서 승리하기 위해서는 `첫번째 타워 파괴`, 효과가 직관적으로 드러나는 `킬`, `골드`와 같은 지표가 중요하다.
  - 보통 시간대에 끝난 게임에서 승리하기 위해서는 높은 `미드 타워 파괴 횟수`가 가장 중요했으며, 각종 교전에서 승리를 거둬야 높은 수치를 기록할 수 있는 `KDA`, 그리고 `첫번째 억제기 파괴`가 중요하다.
  - 후반에 종료된 게임에서 승리하기 위해서는 중반 게임과 마찬가지로 높은 `미드 타워 파괴 횟수`와 `KDA`가 중요했으며, `전체 억제기 파괴 횟수` 또한 중요하다.
 
위 정보를 바탕으로 이번 프로젝트에서는 동일한 데이터 셋을 활용해 승리 예측을 해보는 시간을 가져보겠습니다.

## 프로젝트 목표
----
1. 게임 시간대 별 승/패 예측을 얼마나 정확하게 해내는가?

## 프로젝트 과정
----
- 데이터 준비를 위한 EDA 및 전처리
- 학습 준비
    - 팀 나누기
        - 수치형, 범주형 features 전처리
- 학습 시작
    - Blue team
        - Scaling
        - `Select K Best`
        - Baseline
    - Red team
        - Scaling
        - `Select K Best`
        - Baseline

----
## 미리보기

![image](https://user-images.githubusercontent.com/70729822/203346668-5ca49898-5a6c-43d4-afdb-012312510f18.png)
![image](https://user-images.githubusercontent.com/70729822/203346737-37f5848b-62de-4bdc-855e-5254f6863c21.png)

![image](https://user-images.githubusercontent.com/70729822/203347079-e03df0f0-7192-4446-b9f2-1b8c7690f519.png)
![image](https://user-images.githubusercontent.com/70729822/203347146-2a69cb10-e80a-4a1b-bfc7-d32be147122b.png)

데이터를 블루팀, 레드팀으로 나눈 후 `Select K Best`를 활용해 **feature selection**을 진행하고 **승리 예측**을 해보는 시간을 가졌습니다.

양 팀 공통으로 성능이 **가장 우수한 모델**은 `Logistic Regression`으로 총 6개의 타겟에 대한 예측을 **약 0.925**의 **정확도**로 해냈습니다.




