
지속적인 시스템 튜닝을 위해 간단한 test set 구성 (biomarker - explanation (requirements))
- 이를 바탕으로 evaluation을 G-Eval 등으로 자동화할 수도 있겠으나 test set 사이즈도 작고 우선순위가 낮으므로 일단 보류

Entrez와 PMC를 조합해서 query에 대해 논문 pdf들을 fetch해올 수 있는 기본적인 파이프라인 구축
- License 문제: open-access만 사용하도록 filter

Abstract text 등 esummary가 제공하는 summary info만 사용한 ranking-based search 테스트 (biomarker에 대한 정보를 잘 포함하고 있는 논문을 찾아낼 수 있는가?)
- Abstract-based search -> pdf text-based search의 2-step을 일단 상정하고 있음
- pdf parsing 방식에 따라 하나로 합치는 것도 가능할 듯함 (text block 단위라든지)

pdf parser
- speed performance를 위해 가급적 static 방식을 채택하고 싶으나 현실적으로 LLM-based를 사용할 듯
- 방문한 적 있는 pdf에 대한 parsing result는 caching하는 식으로 실제 performance를 개선할 수 있을 것으로 보임
- 필요한 정보만 뽑아서 구조화하는 작업
