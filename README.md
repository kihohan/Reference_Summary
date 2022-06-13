# reference_summary

### NLP
[Job2Vec: Job Title Benchmarking with Collective Multi-View Representation Learning](https://arxiv.org/pdf/2009.07429.pdf)
### CV
### ETC
-- [Job2Vec: Job Title Benchmarking with Collective Multi-View Representation Learning](https://arxiv.org/pdf/2009.07429.pdf)
  1. Topology Structrure Preservation (Graph Topology View)
  2. Semantics Preservation (Semantic View)
  3. Job Transition Patterns Preservation (Job Transition Balance View, Job Transition Duration View)

  크게 3가지의 input을 이용하여 Representation Learning (Multi-view Representation Fusion) 하면 직업 추천에 좋은 성능을 낸다는 결과를 제시한다. 요긱 혹은 차후 TMVC에 적용할 케이스로 바꿔보면 

    1. gig간의 지식 그래프 구축 (단어빈도수, 특정단어 기반으로..)
    2. gig JD의 의미분석을 통한 representation 방법론
    3. gig worker의 gig_change and gig_duration

  정도로 결론 내릴 수 있다.
