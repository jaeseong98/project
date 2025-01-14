# KRX-Bigdata

👉 **Project Goal**  

저희팀은 1) 리츠 시장의 성장 가능성 2) 과거 미국의 사례 처럼 22년 국내 또한 리츠법 제정을 통해 시장을 키우려 하고 있다는 점
3)그러나 부동산 회계 중심의 정보 시스템은 상장리츠 성장에 따른 변동성을 설명하는데 한계가 존재함에 착안하여

신규 투자자의 입장에서 상장리츠의 특성을 제대로 반영한 투자의사결정 시스템을 구축하고자 본 프로젝트를 진행하게 되었습니다.
<img width="1018" alt="project_goal" src="https://github.com/jaeseong98/KRX-Bigdata/assets/68582889/e05a9c4a-7c8f-45c0-a1c6-203d4378c45a">

\
👉 **IDEA 01. 부동산 뉴스 심리지수**

As-is : 기존에 리츠 회계 정보는 짧게는 분기, 길게는 반기,년 단위로 회계(재무) 정보가 공시 되고 있었기 때문에 정보의 적시성이 떨어질 뿐더러
        주식 시장의 특성을 제대로 반영하지 못한다는 점예서 한계가 존재하였습니다.

To-be : 부동산의 시장 심리를 포착하기 위해, 금융 뉴스 분석에 적합한 사전 기반(Lexicon-based) 방법론을 바탕으로 [물류, 유통, 리테일, 오피스] 총 4개 섹터의 일단위 뉴스 긍부정 감성지수를 산출하여
        최종적으로 섹터별 시장 비중에 따라 가중 평균한 '심리지수_이동평균' 지수를 생성하여 실물 경제의 선행성과 모형 반영 시 예측 성능의 향상을 확인할 수 있었습니다.

\
👉 **IDEA 02. 부동산 뉴스 심리지수와 상장리츠 주가 기술지표를 반영한 등락 예측모형 구축**

이전 단계에서 생성한 부동산 뉴스 심리지수 외에도, 상장리츠 주가 데이터를 바탕으로 생성한 기술적 지표, 거시경제지표, 부동산실물경제지표 등을 종합적으로 반영하여
XGBoost 기반의 상장리츠 일주일 뒤 등락예측 모형을 구축하였습니다.
<img width="1017" alt="project_framwork" src="https://github.com/jaeseong98/KRX-Bigdata/assets/68582889/ca0e0c94-a833-4839-be74-4a8a05d28f35">

👉 **IDEA 03. 리츠가 처음인 투자자를 위한 상장리츠 정보시스템 기획**

앞서 구축한 부동산 뉴스심리 지수와 상장지수 등락예측 모형을 바탕으로 투자자에게 필요한 기능을 기획 및 구현해보았습니다.
> 기능 1. 기준 시점 일주일 후 개별 종목의 등락 예측 기능\
> 기능 2. SHAP를 이용한 등락 예측 결과의 설명결과 제시\
> 기능 3. 과거 일주일의 누적 히스토리를 바탕으로 예측 추세(강도) 제시\
> 기능 4. 전체 시장 대비 개별 종목의 예측 추세 제시

<img width="1015" alt="project_dashboard" src="https://github.com/jaeseong98/KRX-Bigdata/assets/68582889/78e8edc0-7294-4064-bdd1-0b8ccae88071">
