# <a name="aiml40---demo-instructions"></a>AIML40 - 데모 지침

필요한 준비 사항을 포함하여 AIML40 데모에 대한 자세한 지침은 [AIML40 공개 자료](http://github.com/microsoft/ignite-learning-paths/aiml/aiml40/)를 참조하시기 바랍니다. 공개 자료에서 설명하는 단계를 중복 설명하지는 않습니다. 다만 데모 세션을 주어진 시간(45분) 안에 원활하게 끝낼 수 있도록 몇 가지 핵심 내용을 안내하고자 합니다. 데모 시나리오를 숙지하려면 먼저 공개 자료를 읽어보세요.

## <a name="demo-preparation"></a>데모 준비

[AIML40 공개 추가 정보](http://github.com/microsoft/ignite-learning-paths/aiml/aiml40/README.md)에 설명된 대로 다음과 같은 준비 단계가 있습니다.

1. Azure ML 작업 영역 만들기(Azure 템플릿 또는 CLI 명령 사용)
2. 자동화된 ML 데모에 대한 데이터 세트를 작업 영역에 업로드
3. 컴퓨팅 클러스터를 만들어 데모 가속화
4. Jupyter Notebook 환경을 설정하고 `asba.ipynb` 파일을 열어 실행을 준비합니다.

따라서 데모 이전에는 다음의 3개 페이지가 열려 있는 브라우저를 사용할 수 있습니다.
 - [Text Analytics 페이지](https://azure.microsoft.com/services/cognitive-services/text-analytics/?WT.mc_id=msignitethetour2019-github-aiml40)
 - [Azure ML 작업 영역](http://ml.azure.com)
 - `asba.ipynb`가 포함된 Jupyter Notebook

이러한 단계 외에도 빠른 데모를 위해 다음을 수행해야 합니다.

> 💡 데모를 시작하기 전에 [환경 설정](https://github.com/microsoft/ignite-learning-paths-training-aiml/blob/master/aiml40/Demo.md#demo-preparation)을 완료해야 합니다.

1. **데모 1:** [Text Analytics 페이지](https://azure.microsoft.com/services/cognitive-services/text-analytics/?WT.mc_id=msignitethetour2019-github-aiml40)가 있는 브라우저를 열고, 아래 텍스트 상자에 다음 텍스트를 입력한 후 **분석**을 누릅니다. 
> 런던 매장에서 구매한 도트 패턴 바지가 마음에 들었어요

[데모 1의 동영상 링크: Cognitive Services Text Analytics](https://youtu.be/QJxjm5BirOA)

2. **데모 2:**
   - [Azure ML 작업 영역](http://ml.azure.com)을 사용하여 페이지를 엽니다. 필요한 경우 올바른 작업 영역을 선택합니다.
   - 데이터 세트를 업로드해야 합니다.
   - Azure Machine Learning 작업 영역에서 **자동화된 ML** 탭으로 이동하고 [AIML40 공개 추가 정보](http://github.com/microsoft/ignite-learning-paths/aiml/aiml40/README.md)에 설명된 대로 자동화된 ML 실험을 수행합니다. 실행하는 데 꽤 많은 시간이 걸리기 때문에 미리 수행합니다.
   - 데모를 수행하는 동안 다시 로그인할 필요가 없도록 프레젠테이션 직전에 페이지를 새로 고쳐야 합니다.

[데모 2의 동영상 링크: 자동화된 Machine Learning](https://youtu.be/qrstXN6TLZk)

3. **데모 3:**
   - Jupyter 환경에서 `asba.ipynb`를 엽니다.
   - 코드에 올바른 구독 ID를 붙여넣었는지 확인합니다(기본값을 변경한 경우 클러스터 이름/리소스 그룹 이름도 확인).
   - 모든 단계가 올바르게 실행되는지 확인하기 위해 Notebook의 모든 셀을 실행합니다. 일부 단계는 실행하는 데 꽤 많은 시간이 걸리기 때문에 미리 준비합니다. (실험을 실행하는 데 최대 3시간 30분이 걸리므로 비용 절감을 위해 컴퓨팅 클러스터를 낮은 우선 순위로 설정하는 것이 중요함)
   - 자격 증명을 다시 입력할 필요가 없도록 데모 직전에 Notebook 작업을 완료했는지 확인합니다.

[데모 3의 동영상 링크: Azure Machine Learning SDK 및 Hyperdrive](https://youtu.be/sccNTPO3PwU)


## <a name="demo-time"></a>데모 시간

데모를 진행하면서 다음과 같은 단계를 보여주는 것이 좋습니다.

1. **데모 1.1**: [Text Analytics 페이지](https://azure.microsoft.com/services/cognitive-services/text-analytics/?WT.mc_id=msignitethetour2019-github-aiml40)가 있는 브라우저를 열고 **분석**을 클릭합니다. 페이지는 미리 로드해야 합니다.
2. **데모 1.2**: 
  - 같은 페이지에서 **예제-영어-긍정**을 클릭하여 기본 구인 *지난주에 시애틀로 여행을 가서 멋진 시간을 보냈고 스페이스 니들은 두 번이나 방문했어요*로 전환하고 **분석**을 클릭합니다.
  - 양호 긍정 점수 관찰
  - **멋진**이라는 단어를 제거합니다.
  - **분석**을 클릭하고 크게 하락하는 점수를 관찰합니다.
3. **데모 2:** Azure ML 작업 영역 및 자동화된 ML
  - [Azure ML 작업 영역](http://ml.azure.com)이 있는 브라우저를 엽니다. 이 페이지는 미리 로드되어야 합니다.
  - **데이터 세트**로 이동합니다.
  - 데이터 세트를 엽니다.
  - **개요** 탭에서 **샘플 사용량** 탭을 펼쳐서 코드를 표시합니다.
  - **탐색**으로 전환하여 데이터를 표시합니다.
  - **자동화된 ML**로 전환합니다.
  - 실험 이름을 입력하고 컴퓨팅, 데이터 세트(clothing_automl.xlsx)를 차례로 선택합니다.
  - **분류** 작업 및 **등급**을 대상 열로 선택합니다.
  - **고급 설정**을 펼쳐서 알고리즘 선택을 포함하여 사용 가능한 옵션을 표시합니다.
  - ‘시작’을 클릭합니다(시간이 많이 걸리므로 이전에 실험 실행을 준비했는지 확인하세요.) 
  - **자동화된 ML** 탭을 다시 클릭하고 준비 단계에서 이전에 수행한 실험을 가져옵니다.
  - 실행되는 다른 모델과 가장 최상의 실행을 보여주는 그래프를 설명합니다.
  - 최상의 모델을 클릭하여 **ROC**를 살펴보고, **정밀도-회수** 및 기타 메트릭 그래프를 자세히 알아봅니다.
  - **모델 배포** 단추를 사용하여 모델을 배포하는 작업이 얼마나 간단한지 보여줍니다.
4. **데모 3:** Python SDK와 함께 Azure ML 서비스 사용
  - 이 데모를 진행하는 동안에는 `absa.ipynb` Notebook의 셀을 따라 설명해야 합니다.
  - 가장 안전한 방법은 코드를 전혀 실행하지 않고 코드를 보여주는 것입니다. 그러나 라이브 데모 모드에서 코드를 실행하는 과정을 보여줄 수 없게 됩니다.
  - 더 많은 라이브 데모를 수행하려면 [absa-instuctions.ipynb](absa-instuctions.ipynb) Notebook을 참조하세요. 여기서는 데모 중에 실행해서는 ‘안 되는’ 셀과 안전하게 실행할 수 있는 셀을 설명합니다. 
  - 기본적으로 발표자가 피해야 할 작업은 실행 시간이 오래 걸리는 작업입니다.

## <a name="tear-down"></a>분해

데모는 리소스를 많이 사용하므로 다음 사항을 숙지하세요.
* 클러스터 준비 시간을 절약하기 위해 데모에서 자동 크기 조정이 꺼져 있으므로 컴퓨팅 클러스터를 삭제합니다.
* Azure Machine Learning 컴퓨팅으로 실행 중인 경우 가동 중지 시간에는 최소 노드가 0으로, 데모 실행 시간에는 1로 편집되어야 합니다. 그러면 비용이 절감됩니다.
* Azure ML 작업 영역 및 리소스 그룹을 삭제할 수도 있습니다. 지침은 [공개 추가 정보](http://github.com/microsoft/ignite-learning-paths/aiml/aiml40/README.md)에서 제공됩니다.

