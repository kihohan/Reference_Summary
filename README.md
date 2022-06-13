# reference_summary

### NLP
- [Distributed Representations of Sentences and Documents] (https://arxiv.org/pdf/1405.4053.pdf)
  PV-DIM:
    input: 문장ID and 문장 window사이즈  
    output: window ‘다음’에 나올 단어 예측(word vectors are shared across all)  
    문장들의 같은 단어의 wordvector는 공유된다  

  PV-DBOW:
    input: 문장ID
    output: 일정 갯수의 단어를 예측 (단어의 순서는 고려하지않음.) → randomly sampled
  해당 논문에서는 PV_DIM과 PV-DBOW을 같이 사용하는 것을 추천함.

### CV
### ETC
- [Job2Vec: Job Title Benchmarking with Collective Multi-View Representation Learning](https://arxiv.org/pdf/2009.07429.pdf)
  1. Topology Structrure Preservation (Graph Topology View)
  2. Semantics Preservation (Semantic View)
  3. Job Transition Patterns Preservation (Job Transition Balance View, Job Transition Duration View)

  크게 3가지의 input을 이용하여 Representation Learning (Multi-view Representation Fusion) 하면 직업 추천에 좋은 성능을 낸다는 결과를 제시한다. 요긱 혹은 차후 TMVC에 적용할 케이스로 바꿔보면 

    1. gig간의 지식 그래프 구축 (단어빈도수, 특정단어 기반으로..)
    2. gig JD의 의미분석을 통한 representation 방법론
    3. gig worker의 gig_change and gig_duration

  정도로 결론 내릴 수 있다.
