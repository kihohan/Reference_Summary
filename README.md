# reference_summary

### NLP
- [Distributed Representations of Sentences and Documents](https://arxiv.org/pdf/1405.4053.pdf)  
  * PV-DIM:  
    + input: 문장ID and 문장 window사이즈  
    + output: window ‘다음’에 나올 단어 예측(word vectors are shared across all)  
    + 문장들의 같은 단어의 wordvector는 공유된다  

  * PV-DBOW:  
    + input: 문장ID  
    + output: 일정 갯수의 단어를 예측 (단어의 순서는 고려하지않음.) → randomly sampled  
  
  해당 논문에서는 PV_DIM과 PV-DBOW을 같이 사용하는 것을 추천함.  
  
- [Supervised Paragraph Vector: Distributed
Representations of Words, Documents
and Class Labels](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=8653834)  

  * 추후 요긱 리뷰데이터로 많은 걸 해 볼 수있는 방법론이라고 생각됨.
  * 해당 논문에서 Interpretability, Discriminative Power, Computational Efficiency을 강조함.
  * 라벨을 일거리양, 일거리 난이도 등 요긱 데이터에 맞는 다양한 클래스를 넣어서 임베딩하여 클래스 별 Word Representation을 할 수 있음. → 잘 되면 설명력이 굉장히 높은 AI모델이 될 수 있음.

- [A Survey of Data Augmentation Approaches for NLP](https://arxiv.org/pdf/2105.03075.pdf)  

 * SR(Synonym Replacement): 문장에서 랜덤으로 stop words가 아닌 n 개의 단어들을 선택해 임의로 선택한 동의어들 중 하나로 바꾸는 기법. ex) 배달 참 쉽네. → 배송 참 쉽네.  

 * RI(Random Insertion): 문장 내에서 stop word를 제외한 나머지 단어들 중에서, 랜덤으로 선택한 단어의 동의어를 임의로 정한다. 그리고 동의어를 문장 내 임의의 자리에 넣는걸 n번 반복한다. ex) 돈이 잘 벌려요 → 돈이 너무 잘 벌려요.  

 * RS(Random Swap): 무작위로 문장 내에서 두 단어를 선택하고 위치를 바꾼다. 이것도 n번 반복 ex) 인형탈 알바 너무 쉬워요. → 인형탈 너무 알바 쉬워요.  

 * RD(Random Deletion): 확률 p를 통해 문장 내에 있는 각 단어들을 랜덤하게 삭제한다. ex) 일이 참 편해요. → 일이 편해요.  

 * KoEDA, KorEDA  

### CV
- [Learning a Similarity Metric Discriminatively, with Application to Face
Verification](http://yann.lecun.com/exdb/publis/pdf/chopra-05.pdf)

  *  One-shot learning
  *  다양한 이미지와 rgb벡터를 가진 이미지를 학습하게 되면 이미지를 잘 생성하지 못한다는 문제점이 있음.

- [AN IMAGE IS WORTH 16X16 WORDS:
TRANSFORMERS FOR IMAGE RECOGNITION AT SCALE](https://arxiv.org/pdf/2010.11929.pdf)

  * a
  * b  


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
