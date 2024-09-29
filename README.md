# Reflection을 이용한 RAG의 성능 향상 

<a href="https://hits.seeyoufarm.com"><img src="https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2Fkyopark2014%2Frag-with-reflection&count_bg=%2379C83D&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=hits&edge_flat=false"/></a>
<img alt="License" src="https://img.shields.io/badge/LICENSE-MIT-green">

<a href="https://hits.seeyoufarm.com"><img src="hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2Fkyopark2014%2Frag-with-reflection%2F&count_bg=%2379C83D&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=hits&edge_flat=false"></a>
<img alt="License" src="https://img.shields.io/badge/LICENSE-MIT-green">

RAG의 결과가 충분한 context를 포함하고 있지 않은 경우에 [Query Tansformation](https://github.com/kyopark2014/korean-chatbot-using-amazon-bedrock/blob/main/query-transformation.md)을 이용하면, 다양한 sub queries를 통해 풍부한 context를 가지는 결과를 얻을 수 있습니다. 그러나, query의 질문이 짧은 경우에는 query transformation으로 얻어진 결과가 늘어난 지연시간만큼 효과를 얻지 못할 수 있습니다. 또한 chatbot의 경우에 이전 history를 이용해 이미 질문을 revise하므로 query transformation이 불필요한 중복일 수 있습니다. 

여기서에서는 Reflection을 이용한 RAG의 성능 강화에 대해 설명합니다. Reflection을 통해 RAG로 얻어진 결과에서 sub-queries들을 생성하고 이를 통해 RAG로 얻어진 context를 강화합니다. 
