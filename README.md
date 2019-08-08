# 메디블록 기술백서v0.3

## 개요
메디블록 메인넷의 정식 명칭은 패너시어(Panacea)로 만병통치약의 의미를 담고 있습니다. 메디블록은 ‘환자 중심의 의료정보 솔루션 개발을 통해 의료계에 혁신적인 패러다임을 제시하고, 모든 사람이 건강한 삶을 살 수 있는 세상을 만들어간다’는 사명 아래, [환자 중심의 의료정보/ 신뢰할 수 있는 의료정보/ 개인 맞춤형 의료정보]를 제공하는 블록체인 기반의 의료정보 플랫폼을 개발하고 있습니다. 패너시어는 메디블록의 사명을 실현시킬 핵심기술로, 환자 중심의 헬스데이터 수집, 관리 및 활용이 이루어지는 생태계를 만들게 됩니다. 그 동안 환자가 겪었던 문제점은 패너시어를 통해 개선 및 해결되고, 환자의 의료경험은 완벽하게 재창조 될 것입니다. 페너시어(Panacea)는 의료정보 프로토콜로 독립된 네트워크를 가진 퍼블릭 블록체인입니다. 패너시어 블록체인 상에서는 노드들의 합의를 바탕으로 내용을 기록, 검증하기 때문에 한 번 성공적으로 기록된 내용은 위조 및 변조가 불가능합니다. 의료정보의 해시값을 패너시어에 기록하고 이를 통해 의료데이터에 대한 무결성 및 소유권 검증을 할 수 있는 것이 패너시어의 핵심 기능입니다. 이는 패너시어 생태계의 경제적 바탕이 되는 독자적인 암호화폐(MED 코인)를 기반으로 원활하게 활용될 수 있습니다.

### 패너시어 합의방식(Panacea Consensus Mechanism)
패너시어 블록체인은 DPOS(Delegated Proof of Stake, 위임지분증명)에 PBFT(Practical Byzantine Fault Tolerance, 프랙티컬 비잔틴 장애 허용) 알고리즘을 활용해 구축된 블록체인입니다. DPOS 방식에서는 사용자들의 투표로 결정된 블록생성자가 효율적으로 블록 동기화를 하면서 빠른 속도로 새 블록을 생성합니다. 패너시어는 PBFT방식으로 구현한 DPOS 방식을 채택하여 노드를 구성합니다. 패너시어에서 노드로 선정되어 블록검증과 블록생성을 수행하는 집단을 검증자(Validator 이하 검증자)라고 지칭하며, 검증자는 검증자로서 역할을 수행할 시 MED 메인넷 코인을 득표 비율만큼 보상으로 지급받습니다. 검증자로 채택되지 못한 MED 메인넷 코인 보유자는 본인의 MED 메인넷 코인으로 검증자에게 투표를 하여 블록 확정프로세스에 기여하고 블록 생성 완료마다 보상을 받습니다. 

 ![Image of Simplified Panacea Architecture](https://github.com/medibloc/whitepaper/blob/master/Simplified%20Panacea%20Architecture.png) 
 
 ### 패너시어 합의방식의 특징 
강제 소각(Slashing)  
패너시어는 DPoS(위임지분증명)와 PBFT(프랙티컬 비잔틴 장애 허용)알고리즘을 사용하는데, 이 알고리즘은 불성실한 검증자를 걸러내는데에도 탁월한 기능이 있습니다. 블록 검증에 성실하게 임하지 않거나 악의적인 행동을 하는 경우, 검증자는 보유 MED 메인넷 코인의 일부를 페널티로 강제 소각(Slashing) 당하며, 이러한 부적합 검증자에게 투표를 한 사용자가 스테이킹 한 코인 수량도 일정부분 자동 소각됩니다. 즉, 검증자가 옳은 행동을 하는 것이 중요할 뿐만 아니라, 사용자가 옳은 검증자를 선택하는 것 역시 매우 중요한 역할이 됩니다. 이로써 사용자들은 적합한 검증자에게 투표를 하기 위해 노력할 동기가 생기며, 궁극적으로 블록체인이 선순환 구조를 가질 수 있도록 유도합니다. 이는 의료 블록체인이 반드시 가져야 할 데이터 검증과 보안성, 안정성을 더욱 강화하는 알고리즘이며, 패너시어의 강력한 강점이 될 것입니다.
 
원블록 파이널리티(One Block Finality)
패너시어의 원블록 파이널리티(One Block Finality)메커니즘은 기존 블록체인의 취약점을 보완합니다. 기존 블록체인이 '선-블록 생성, 후 합의' 메커니즘으로 작동되어 여러 가지 공격 위험에 항상 노출되어 있었다면, 패너시어는 '선-합의, 후-블록생성'의 원블록 파이널리티 메커니즘을 통해 100%의 신뢰성을 가진 합의 알고리즘이 됩니다. 그리고 이러한 합의 메커니즘 덕분에 포크가 절대 발생하지 않는 것도 하나의 특징입니다. 

### 보상체계(Incentives)
사용자의 투표를 많이 받은 검증자는 블록 생성 순서가 더 자주 돌아오고, 득표를 많이 할 수록 가중치가 늘어나 검증자로 선정될 확률이 높아집니다. 검증자는 메디블록 코인의 인플레이션과 Gas Fee를 통해 보상을 받습니다. 검증자 본인은 스스로 자신의 수수료율을 설정할 수 있으며 해당 검증자에게 투표한 사용자(위임자)에게는 이렇게 책정한 수수료를 제외한 후 투표 비율대로 보상을 배분합니다. 투표한 사용자(위임자)는 검증자의 정보와 블록생성 수수료를 토큰스왑 이후 검증자 선출시 패너시어 익스플로러에서 확인할 수 있습니다. 패너시어 상에 스테이킹(Staking)된 비율에 따라 인플레이션 비율은 조정됩니다. 스테이킹한 코인의 비율이 상대적으로 낮아지면 인플레이션 비율이 높아지고, 반대로 스테이킹한 코인 비율이 상대적으로 높아지면 인플레이션 비율은 낮아집니다. 따라서 패너시어의 검증자들이 스테이킹을 많이 할수록 시중에 유통되는 메디블록 코인의 수량이 줄어들고, 가치를 유지하게 됩니다. 

### 패너시어의 노드구성 
향후 패너시어 검증자(validator)는 사용자들의 참여 투표를 통해 선정됩니다. 후보로 출마할 수 있는 참여자는 일반 사용자, 의료사업체 또는 의료기관 등으로 구분될 예정입니다. 일부 노드는 메디블록과 협력하고 있는 의료사업체 혹은 의료기관이 될 수 있습니다. QRC20 및 ERC20 기반 토큰을 메인넷 코인으로 스왑하기 전까지 메디블록이 패너시어 검증자의 역할을 100% 우선 수행하며, 토큰 스왑과 검증자 선정이 성공적으로 완료된 후, 메디블록이 검증자 역할 수행으로 받은 MED 메인넷 코인 보상은 소각 혹은 에어드랍할 예정입니다.

### 검증가능한 의료정보 해시
메디블록 플랫폼 내에서 헬스케어 데이터는 머클 트리(Merkle tree)의 형태로 가공되어 관리됩니다. 특정 형식의 헬스케어 데이터(e.g. HL7 FHIR)를 활용하는 서비스는 해당 데이터를 머클 트리로 만드는 과정을 진행하며, 메디블록은 이를 활용하는 서비스가 패너시어를 통해 데이터 쉽게 활용할 수 있도록 소프트웨어 도구와 가이드를 제공할 예정입니다. 데이터를 머클트리 형태로 관리할 때의 장점은 데이터 내용을 일부만 공유하는 것이 가능하다는 것입니다. 블록체인에는 데이터 소유자가 머클 트리의 루트 해시(Root hash)를 기록합니다. 머클 트리의 특성 상 데이터의 일부만 공개하더라도 루트 해시를 포함하는 머클 증명(Merkle proof)을 제공하면 그것이 전체 원본에 포함된 값이 맞는지 검증할 수 있습니다. 이를 이용해 데이터 전달시 개인 정보를 제외함으로써 데이터를 비식별화 하는것도 가능하며, 요청자의 요구에 따라 작성자의 서명과 같은 특정 데이터만을 공개해 데이터 거래 전에 해당 데이터에 대한 신뢰성을 먼저 입증할 수 있습니다. 머클 트리로 변환된 데이터 원본은 일차적으로 사용자의 스마트폰 디바이스에 저장됩니다. 블록체인에는 데이터 원본을 바탕으로 추출한 루트 해시를 기록하기 때문에 데이터 저장 및 공유 과정에서 사용하는 암호화 방식에도 아무런 제약이 없습니다. 컴퓨팅 파워의 증가로 인해 원래의 암호화 방식이 안전성을 잃더라도 블록체인에 기록된 내용과 충돌하는 것 없이 서비스 단계에서 새로운 암호화 방식을 적용할 수 있습니다.

### 패너시어의 역할 
패너시어 상의 모든 활동은 트랜잭션으로 확인 가능(개인 의료정보 자체는 해시값만 저장)
웹사이트나 모바일 앱 등에서 환자의 데이터 수집을 지원하는 역할
환자들에게 의료데이터 활용 동의를 받는 역할
환자가 수집한 의료데이터에 대해 환자가 통제권을 행사를 할 수 있도록 지원하는 역할
의료 유관 기업들이 환자들의 데이터를 신뢰할 수 있도록 하는 역할
환자의 동의를 받은 데이터를 활용할 수 있도록 하는 역할

