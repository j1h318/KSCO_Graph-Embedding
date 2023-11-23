# QUERIES
  각 직업 노드에 임베딩 좌표 입력
  ```CALL gds.graph.project('mygraph', ['OCCUPATION', 'SKILL'],'JACCARD');

  CALL gds.beta.node2vec.stream('mygraph', {embeddingDimension: 2})
  YIELD nodeId, embedding
  RETURN nodeId, embedding;

  CALL gds.beta.node2vec.write(
   'mygraph',
    {embeddingDimension: 2,
     writeProperty:'embedding'
    }
   )
  ```
## 직업코드 단위로 값 확인 
  ```MATCH (n:OCCUPATION) RETURN n.occu1Cd As jobco, n.occu2Cd AS jobs, n.embedding AS embedding ```
