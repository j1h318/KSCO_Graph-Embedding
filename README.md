# KSCO_Graph-Embedding
To respond to the rapidly changing labor market, a job classification system is established based on the latest job postings in Korea

## 프로젝트 목표
변화하는 채용시장에 대응: 향상된 직업 매칭을 위한 직무역량 기반 임베딩

한국표준직무분류(KSCO) 7차 개정 모델(2018)을 변화하는 채용시장에 대응할 수 있도록 개선합니다.
- Worknet API를 통해 구직공고 데이터를 MongoDB 데이터베이스에 수집
- GPT API를 통해 자연어로 기술된 구직공고의 구직역량을 처리 (직업/기술 데이터 셋)
- 직업/기술 구직 데이터를 그래프 노드로 구성하여 직업 간 유사성 확인
- 직업 유사성을 기반으로 Node2vec를 사용하여 직업 노드를 임베딩

## 그래프 기반의 직업/기술 분류모델
Neo4j Aura 직업-기술 예시용 이미지
![직업-기술 그래프 모델](https://github.com/j1h318/KSCO_Graph-Embedding/assets/57842978/aa1fb768-d4f1-4d1f-9ca3-96b5259098a3)

## 임베딩 값을 기반으로 유사 직업 탐색
직업 노드의 임베딩 결과
![embedding](https://github.com/j1h318/KSCO_Graph-Embedding/assets/57842978/a1a849d3-2d68-4ca8-aee1-ce475925b1e5)

## Installation

`pip install neo4j` <br>
`pip install neo4j-driver`
