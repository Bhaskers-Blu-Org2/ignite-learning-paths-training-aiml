# <a name="personalizer-demo"></a>Personalizer 데모

> 💡 데모를 시작하기 전에 [설정](https://github.com/microsoft/ignite-learning-paths-training-aiml/blob/master/aiml20/DEMO%20Setup.md)을 완료해야 합니다.

이 데모에서는 보충 학습 및 [Cognitive Services Personalizer](https://docs.microsoft.com/en-us/azure/cognitive-services/personalizer/?WT.mc_id=msignitethetour2019-github-aiml20)를 사용하여 웹 사이트 레이아웃이 방문자 작업에 어떻게 적용되는지 확인합니다.

Personalizer는 인터페이스를 동적으로 다시 구성하여 익명 방문자가 권장 사항 섹션에서 추천 범주를 클릭할 가능성을 최적화합니다.

1. Tailwind Traders 웹 사이트 앱 배포(`DEMO Setup.md`로 아직 수행하지 않은 경우)

2. Tailwind Traders 홈페이지 방문

3. “권장” 섹션과 추천 범주의 순서를 확인합니다.

4. 페이지를 새로 고칩니다(여러 번 수행해야 할 수 있음). 레이아웃이 변경되는지 확인합니다.

Personalizer 서비스는 익명 방문자를 추적하고 범주를 클릭할 때 사용되는 시간, 요일 및 브라우저 OS를 기록합니다. “보상”은 크게 많은 추천 섹션을 클릭했는지 여부입니다. 

일정 시간이 지나면 Personalizer는 시간, 요일 및 OS를 기반으로 가장 적합한 범주를 결정합니다. 또한 다른 방식으로는 제시되지 않는 범주를 나타내기 위해 시간의 20%를 “탐색”합니다.
