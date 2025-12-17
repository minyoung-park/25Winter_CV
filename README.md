# 25Winter_CV

# html 시각화 자료가 안보이므로 주의 요함
분석 목적 및 목표

- 국내 주식 시장과 해외 주식 시장의 구조 비교
- 시장 동향 분석
- Sector를 활용하여 산업 간의 구조 파악
- 전체 산업에서의 중요 종목 및 산업 별 중요 종목 선정
- 경제 지표와 산업 및 종목 간 관계 파악

- networkx, pyvis 와 같은 네트워크 분석 라이브러리를 이용
- 각 종목을 Node, 종목 간의 관계를 Edge로 활용하여 네트워크화

- Sector 분류
=> yahoo finance, GICS 체계 활용하여 분류

=> 일일 주가 변동률을 통해 correalation matrix 새로 생성하여 분석 진행 => Sector간 관계 확보
=> 임계값 이하의 correlation Edge는 삭제 

중요 종목 선정 방법
- Degree Centrality 연결 중심성 : 이웃이 얼마나 많은가
- Closeness Centrality 근접 중심성 : 다른 노드들과 얼마나 가까운가
- Betweenness Centrality 매개 중심성: 얼마나 bridge 역할을 하는지의 정도
- Eigenvector centrality: 얼마나 central한 node들과 연결되어 있는가
- PageRank : 중요한 노드들은 또다른 중요한 노드로부터 많은 유입 링크를 가진다는 가정

(1) 국내, 해외 통합하여 전 Sector 네트워크 시각화

(2)국내, 해외 종목 구분하여 전 Sector 포함 후 중요 종목 추출

(3)주요 종목 활용하여 시각화

(4) Sector 별 산업별 평균 중요도 산출 후 누적 수익률과 비교

(5) 월 별 누적 수익률 변화 파악

(6)국내, 해외 구분하여 Sector 별 중요 종목 선정
