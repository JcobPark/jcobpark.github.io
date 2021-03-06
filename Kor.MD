---
layout: page
title: 한국어
permalink: /kor/
---

# Grabity.io 백서

**초안 작성일: 2018년  9월  5일 Grabity Whitepaper Ver 1.0**

**최종 수정일: 2018년 10월 19일 Grabity Whitepaper Ver 1.1**

**초록**: 1960년대 인터넷의 탄생부터 상용화 단계에 이르기까지 30년이 넘는 시간이 걸렸다. 2009년 비트코인을 시작으로 블록체인 기술은 발전해왔지만, 상용화 되기 위해서는 기술적 성능 향상과 표준화를 거쳐야 한다. 2000년대 초 닷컴 버블 때처럼, 현재 많은 IT 기업들이 블록체인 비지니스를 만들기 위해 과도기적인 블록체인 기술에 많은 것을 융합하려고 시도를 하고 있다. 인터넷 기술이 없이 인터넷 비즈니스가 발달할 수 없듯 블록체인 기술의 발전이 있기 전까지 블록체인에 기반한 비즈니스 시장이 형성되기는 어렵다. 

Grabity는 컴퓨터 유휴 자원을 사용하는 퍼블릭 블록체인을 개발하는 일을 최우선으로 하여 표준 프로토콜이 되도록 노력하고 있다. 개발자들은 높은 비용을 내고 서버를 운영하는 대신 사용자의 디바이스를 노드로 사용하고 또한 사용자들은 수수료를 내지 않고도 DApp을 실행할 수 있도록 생태계를 구축할 것이다. 이를 위해 동시다발적인 트랜잭션 처리와 분산화 저장 기술을 상용화하고 자체적으로 개발한 Genesis Hoisting과 함수 조각모음 기술을 통해 P2P 통신에 최적화된 진정한 분산화 네트워크를 구축하고자 한다.

**주의사항: 본 백서에서 언급되는 암호화폐 토큰(GBT)은 이더리움 블록체인에 기반한 ERC-20 토큰이 아닌 Orbits Network 메인넷 상에서 사용할 수 있는 토큰을 지칭합니다.**

저작권 소유 © 2018 Grabity Pte. Ltd.

누구든지 허가 없이 원래의 출처와 해당 저작권 고지가 언급된 경우 비영리적이고 교육적인 용도 (즉, 유료 또는 상업적 목적 이외의 목적)로 본 백서의 자료를 사용, 복제 또는 배포할 수 있습니다.

 **면책 조항:** Grabity.io 백서 초안은 오직 정보 제공의 목적으로써 제공됩니다. Grabity Pte. Ltd.는 이 백서의 정확성이나 결론을 보장하지 않으며 이 백서는 "있는 그대로" 제공됩니다. Grabity Pte. Ltd.는 명시적, 묵시적, 법적 또는 기타의 모든 표현을 보증, 진술 하지 않습니다. Grabity Pte. Ltd. 및 그 계열사는 본 백서 또는 여기에 포함된 내용의 사용, 참조 또는 의존으로 인해 발생하는 어떠한 종류의 손해와 가능성에 대해 통보받은 경우에 대해서도 책임을 지지 않습니다. 어떤 경우에도 Grabity Pte. Ltd.는 직접 또는 직간접적, 결과적, 보상적, 부수적, 실제적, 모범적, 징벌적 또는 특수한 용도, 사용 또는 사용 불가능한 모든 종류의 손해, 손실, 책임, 비용 또는 지출에 대해 어떠한 개인이나 단체에게도 수익, 이익, 데이터, 사용, 영업권 또는 기타 무형의 손실을 포함해 책임을 지지 않습니다. 

- [**1. 비전 (Vision)**](#1-vision)
- [**2. 도입 (Introduction)**](#2-introduction) 
  - [2.1. 인터넷 패러다임 (The Paradigm of Internet)](#21-the-paradigm-of-internet)
  - [2.2. 블록체인 기술 (Blockchain Technology)](#22-blockchain-technology)
  - [2.3. 인터넷 기반 신뢰의 진화 (The Evolution of Trust on the Internet)](#23-the-evolution-of-trust-on-the-internet)
  - [2.4. 분산원장기술의 미래 (The Future of Distributed Ledger Technology)](#24-the-future-of-distributed-ledger-technology)
- [**3. 프로젝트 (Project)**](#3-project) 
  - [3.1. 공전 네트워크 (Orbits Network)](#31-orbits-network)
    - [3.1.1. 동시다발적인 트랜잭션 (Simultaneous Transaction)](#311-simultaneous-transaction)
    - [3.1.2. 제네시스 호이스팅 (Genesis Hoisting)](#312-genesis-hoisting)
    - [3.1.3. 분산 저장 (Distributed Storage)](#314-distributed-storage)
    - [3.1.4. 함수 조각모음 (Defrag Function)](#313-defrag-function)
  - [3.2. 플래닛 지갑 (Planet Wallet)](#32-planet-wallet))
- [**4. 생태계 (Ecosystem)**](#4-ecosystem)
  - [4.1. 토큰 경제 (Token Economy)](#41-token-economy)
  - [4.2. DApp 지원 (DApps)](#42-dapps)
- [**5. 로드맵 (Roadmap)**](#5-roadmap)   
- [**6. 토큰 판매 (Token Sale)**](#6-token-sale)  
- [**참조 (Reference)**](#reference) 


    
# 1. Vision

**New Paradigm of Internet**

>**“We strives to shift Internet Paradigm from Centralized to Distributed Network.”**

누구나 이미 가지고 있는 스마트폰, 태블릿, PC와 같은 컴퓨터 자원을 공유하여 퍼블릭 블록체인을 구축하고 중앙화된 시스템에서 분산화된 구조로 인터넷 패러다임을 전환할 것이다.

Grabity는 중앙화된 시스템에서 분산화된 구조로 인터넷 패러다임을 전환하기 위한 퍼블릭 블록체인 프로젝트다. 현재 하드웨어 성능이 비약적으로 발전함에 따라 스마트폰만 하더라도 이전 서버 이상의 성능을 가지고 있다. 하지만 저장공간이나 연산능력을 100% 사용하고 있지는 않다. 누구나 이미 가지고 있는 스마트폰, 태블릿, PC와 같은 디바이스의 유휴 자원 혹은 사용하지 않는 디바이스를 활용해 컴퓨터 자원을 공유한다면 사용자는 자원을 제공한 만큼 보상을 획득하고 DApp 개발사는 공유된 컴퓨터 자원을 활용해 더욱 적은 비용으로 서비스를 운영할 수 있다. Grabity 프로젝트가 상용화 단계에 이른다면 누구나 분산된 노드를 활용하여 인터넷 패러다임의 전환을 이룰 수 있을 것이다.

# 2. Introduction

##         2.1. The Paradigm of Internet

>**“TCP/IP라는 고유한 프로토콜을 기반으로 구축된 전 세계적인 인터넷의 기술은 1960년대부터 개발되어 1990년대 상업화되었다.”**

1960년대 인터넷의 역사는 패킷 교환 네트워크의 구축으로부터 시작되었다. 현재 컴퓨터 매개 커뮤니케이션 방식인 패킷 교환 이론에 관한 최초의 논문이 MIT의 레너드 클라인록(Leonard Kleinrock)에 의해 1961년 발표되었다. 1969년에 아르파넷(ARPANET) 같은 인터네트워킹을 위한 프로토콜이 개발되었고 여기서 서로 떨어진 여러 개의 망이 하나의 네트워크로 함께 결합할 수 있었다. 

1970년대 중반 PC와 1200bps 모뎀이 등장하면서 CMC (computer-mediated communication) 네트워크의 분산화 모델이 등장한다. 한편 이더넷의 개발도 인터넷 이용자 확대에 커다란 기여를 하게 된다. 이것은 일종의 근거리통신망(Local Area Network, LAN) 개념으로서, 현재 인터넷 네트워크를 구성하는 가장 기본적인 모델이다. 1970년대까지 기본 시스템과 응용 프로그램들이 개발되고 그에 따라 네트워크의 규모가 비약적으로 확대되기 시작한다. 

하지만 1980년대 이후 인터넷의 관리 및 운용이 큰 문제가 되었다. 이에 따라 환경 변화에 대응하기 위한 시스템들이 개발되는데 하나의 예가 도메인 네임 시스템(DNS)이다. 초기에는 호스트의 수가 적어 단일한 호스트 테이블만으로도 가능했으나, 호스트 수가 늘어나면서 호스트의 이름과 주소를 기억하는 것이 곤란해지자 DNS(Domain Name System)가 개발되어 호스트 수가 1000대를 돌파하는 1984년부터 도입된다. 1983년 패킷의 전달 기능을 수행하는 IP와 흐름 통제 및 손실된 패킷의 수정 기능을 수행하는 TCP 등 두 가지 기능을 갖춘 TCP/IP가 표준화되었다.

일반인에게 본격적으로 확대되고 그에 따라 상업화가 진전된 것은 1990년대 이후이다. 1989년 10만을 돌파한 호스트 수는 불과 1년 후인 1990년에 30만을 돌파한다. 이때 최초의 인터넷 검색 엔진인 아키(Archie)가 개발되었고 최초로 지금과 같은 상업적인 인터넷 서비스 제공 업체(ISP)가 등장한다. 그러나 인터넷 상업화의 결정적 전기가 마련된 때는 월드와이드웹이 개발, 배포되기 시작한 1991년 이후이며, 웹이 발전할 수 있었던 이유는 사용자에게 편리한 브라우저의 개발 때문이었다.

1990년대 중순 이후로 사용자들의 접근이 편리한 웹의 증가와 함께 값싸고 성능 좋은 PC의 보급이 확대되고 통신 인프라가 확대, 발전하면서 인터넷은 문화와 상업에 막대한 영향을 미쳤다. 이는 전자메일, 인스턴트 메신저, 화상 통화뿐 아니라 블로그, 소셜 미디어, 온라인 쇼핑몰 등을 포함한 W3를 아우른다. 모뎀에서 광케이블, LTE 무선통신에 이르기까지 인터넷은 속도와 공간의 한계를 극복하며 발전해왔다.


##         2.2. Blockchain Technology

>**“블록체인은 누구나 열람할 수 있는 장부에 거래 내역을 투명하게 기록하고, 다수의 노드에 이를 복제하여 저장한 후 기록을 검증하는 방식으로 해킹을 막는 분산 데이터 저장 기술이다.”**

중앙집권화된 금융시스템의 문제점은 2007년 글로벌 금융위기 사태로 드러났다. 2009년 나카모토 사토시는 달러화 중심의 금융자본 권력에서 벗어나 신뢰할 수 없는 P2P 환경에서 개인 간 금융거래를 실현하게 할 수단으로 블록체인 기술을 제안했다. 
블록체인은 블록에 데이터를 담아 체인 형태로 연결, 수많은 컴퓨터에 동시에 이를 복제해 저장하는 분산형 데이터 저장 기술이며 공공 거래 장부라고도 부른다. 중앙 집중형 서버에 거래 기록을 보관하지 않고 거래에 참여하는 모든 사용자가 동일한 거래 내역을 보관하며, 거래 때마다 모든 거래 참여자들이 정보를 공유하고 이를 대조해 데이터 위조나 변조를 막는다.
이 블록체인 기술은 비트코인에 적용되어, 누구나 열람할 수 있는 장부에 비트코인의 거래 내역을 투명하게 기록하며 노드들이 10분에 한 번씩 기록을 검증하여 해킹을 막는다. 또한 비트코인은 완전한 익명으로 거래되며, 컴퓨터와 인터넷만 되면 누구나 계좌를 개설할 수 있다. 


2014년 비탈릭 부테린에 의해 이더리움이 개발되면서 블록체인은 큰 변화를 맞이하게 된다. 비트코인을 포크해 이더리움을 만든 비탈릭 부테린은 스마트 컨트렉트 기능을 구현했는데 이는 계약 조건을 블록체인에 기록하고 조건이 충족됐을 경우 자동으로 계약이 실행되게 하는 프로그램이다. 금융 거래뿐 아니라 전반적인 산업에 적용할 수 있는 스마트컨트렉트로 인해 블록체인 기술의 활용도는 높아졌다.

##         2.3. The Evolution of Trust on the Internet

>**“인터넷의 새로운 패러다임 전환을 위해서는 기술 기반의 신뢰가 필요하다. 신뢰는 중앙화된 구조에서 블록체인 기술을 통해 탈중앙화를 거쳐 분산된 구조로 진화할 것이다.”**

특정한 기술의 발달로 새로운 패러다임이 만들어졌다고 가정해보자, 패러다임 전환을 위해서 어떠한 요소들이 필요할까? 오래된 것에서 새로운 것으로 나아가게 하는 힘은 바로 신뢰이다.  

현재의 인터넷은 중앙집권화되어 있다. 또한 인터넷에서의 위조는 현실에서의 위조보다 용이하다. 하지만 우리들의 대부분은 공정한 거래를 원하고 인터넷의 가능성을 믿고 신뢰하려고 한다. 이러한 신뢰가 일부 악의 있는 사람들에 의해 무너져서는 안 되고 보다 신뢰할 수 있는 인터넷 사회를 위해 다소의 이점을 잃더라도 그러한 신뢰성을 반드시 구축해 나가야 한다.

블록체인 기술로 인해 중앙집권화된 인터넷은 탈중앙화된 구조로 바뀌고 있다. 대표적으로 암호화폐에 시도되고 있는데, 블록에 금전 거래 내역을 저장해 거래에 참여하는 모든 사용자에게 거래 내역을 보내주며 거래 때마다 이를 대조해 데이터 위조를 막는 방식을 사용한다. 이 밖에도 전자결제나 디지털 인증뿐만 아니라 화물 추적 시스템, P2P 대출, 전자투표, 차량 공유, 의료기록 관리 등 신뢰성이 요구되는 다양한 분야에 활용할 수 있다. 현재 이더리움 플랫폼을 통해 가속화되고 있지만, 플랫폼 사용료의 증가와 트랜잭션 처리 속도의 한계 등은 아직 해결해야 할 과제이다. 

하지만 현재 탈중앙화 플랫폼은 거버넌스 부분이나 토큰의 분배, 프로젝트의 운영과 관리 부분에서 중앙화 구조로 회귀하고 DApp들은 중앙화된 서버와 하이브리드 구조로 운영되고 있다. 중앙 서버나 중앙관리자의 제어 없이 분산화된 네트워크의 각 노드가 데이터베이스를 공유하고 계속 동기화하는 기술인 분산원장기술(DLT: Distributed Ledger Technology)의 발전은 현재의 서버-클라이언트 구조를 벗어나 노드들로 구성되는 진정한 분산화된 네트워크의 현실화를 가져올 것이다.


##         2.4. The Future of Distributed Ledger Technology

>**“블록체인 기술을 처음으로 적용한 비트코인이 개발된 지 9년이 지났다. 앞으로 분산원장 기술은 어떻게 발전할까? 또한 언제쯤 상업화될까? 이는 인터넷 기술의 발전과 상업화를 보면 예측할 수 있다. 분산원장기술의 기술적 한계를 극복하는 것과 표준화가 우선이고 그 후에야 상용화가 될 것으로 예측할 수 있다.”
”**

1969년 아르파넷(ARPANET)으로 시작된 인터넷은 전 세계적으로 14년 정도의 인터넷 기술 개발 이후 1983년에 TCP/IP라는 프로토콜로 표준화되었다. 그로부터 8년 후 1991년 월드와이드웹(WWW)이 개발 배포되면서 상용화되었다. 이후 1995년부터 2000년까지 닷컴 버블이 일어났으며 너도나도 인터넷 분야의 사업에 뛰어들게 되었다. 수많은 IT기업들이 시도했던 인터넷 서비스들이 과도기적인 인터넷 기술에 너무 많은 것을 융합하려다 시대를 앞서가게 되었고 결과적으로 벤처기업들이 파산하게 되었다.

현재의 블록체인 산업은 기술적인 발전과 동시에 이를 사업화하려는 시도가 맞물리면서 닷컴 버블과 같은 거품 경제 현상이 발생했다. 블록체인 기술에 대한 신뢰 없이는 사람들이 새로운 패러다임을 받아들이기 힘들고 이는 곧 시장(상업화) 형성과도 연결되기 어렵다. 초창기 인터넷 산업의 발전과 같이 분산 원장 기술 또한 비슷한 흐름으로 나아갈 것이다. 다만 분산원장 기술은 기존 인터넷 인프라를 사용하기 때문에 몇 배 더 빠르게 진행될 것으로 예측할 수 있다. 인터넷 기술 없이 인터넷 비즈니스가 존재할 수 없듯이 분산 원장 기술을 활용한 비즈니스는 실생활에 쓰일 수 있는 분산 원장 기술이 개발된 다음에 확장될 것이다. 분산 원장 기술이 상용화되기 위해 직면한 과제는 다음과 같다. 

첫 번째로 처리 속도가 빨라져야 한다(Scaling Issue). 현재 비트코인(7 TPS)과 이더리움(20 TPS)을 보면 속도의 한계를 알 수 있다. ‘Crypto Kitty 사태’와 같이 이더리움은 트래픽이 몰릴 때 낮은 처리 속도로 인해 네트워크 전체가 마비되는 현상을 몇 차례 겪었다. 실생활에서 웹처럼 사용할 수 있으려면 SegWit, Lightening, Plasma, Sharding 등의 부가적인 기술보다 좀 더 근본적인 기술 구조의 변화가 동반되어야 할 것이다.

두 번째로 사용 비용을 개선해야 한다. 대부분의 블록체인 네트워크는 사용자가 모든 비용(Gas)을 부담하고 있다. 우리가 인터넷을 사용할 때마다 사용 비용을 지불하지 않듯이 상용화를 위해서는 현재의 비용 구조를 개선할 필요가 있다.

세 번째는 데이터 저장의 효율화다. 지속적으로 생성되는 원장과 스마트 컨트랙트, 정크 데이터들은 블록체인 내에 영원히 저장되고 모든 풀 노드들은 현재 이더리움 기준 1TB가 넘는 제네시스 블록부터 쌓여온 모든 데이터를 가지고 있어야 한다. 라이트 노드의 용량조차 150GB가 넘어가면서 진입장벽이 높아지고 전체 네트워크 효율이 저하되고 있다. 데이터의 무결성은 보증하되 보다 효율적인 데이터 저장 구조가 필요하다.

네 번째는 완전히 분산된 DApp 구조를 만들어야 한다. 현재 DApp 구조는 기존의 App과 DApp(Decentralized App)의 하이브리드 어플리케이션 이다. DApp의 데이터 베이스는 블록체인에 저장되고 실행 코드는 중앙 서버에서 운영되기 때문에 블록체인을 통해 데이터는 보호될 수 있지만, 중앙 서버가 무력화되면 시스템이 무너지게 되는 취약한 구조다. 데이터베이스 뿐만 아니라 DApp의 소스 파일도 분산화 구조로 만들어야 한다.

다섯 번째는 보편적인 블록체인 개발 환경을 만드는 것이다. 이더리움은 제한된 환경에서 보급성이 떨어지는 언어(Solidity)를 채택함으로써 개발 진입 장벽이 높아졌기 때문에 보다 다양한 DApp이 출시되기 힘들다. 좀 더 보편적인 언어로 개발 환경을 제공한다면 많은 개발자들이 쉽게 참여해 Killing App이 더욱 활발히 개발될 것이다.

마지막으로 다수에 의한 무결성 검증이다. 현재의 블록체인 네트워크 구조는 완전한 탈중앙화 또는 분산화로 보기 어렵다. 작업 증명(Proof of Work)을 채택한 프로젝트는 재단과 채굴풀(Mining Pool) 운영자에 의해 컨트롤 되고, 지분 증명(Proof of Stake)은 자본에 의한 잠식 구조를 갖고 있으며, 지분 위임 증명(Delegated Proof of Stake)는 거버넌스 구성이 제대로 되지 않고 결국 소수에 의해 컨트롤 되고 있다. 즉 다수에 의해 무결성 검증과 합의가 일어나야 진정한 의미를 가지는 블록체인이 현재 중앙집권화되고 있으며 소수가 시스템을 장악하는 구조로 퇴화하고 있다. 진정한 분산화 시스템을 유지하기 위해서는 다수의 노드들이 시스템에 참여할 수 있는 구조로 발전해야 한다.

# 3. Project

##         3.1. Orbits Network

> **The truly distributed system optimized for wireless communications**

**< Concept >**

Orbits Network는 Grabity의 분산화된 메인넷으로써 유/무선으로 연결된 컴퓨터 유휴 자원을 공유하여 진정한 분산화 P2P 네트워크를 구축하고자 한다. Orbits Network의 트랜잭션은 동시다발적으로 빠르게 처리할 수 있고, 거래 내역은 Genesis Hoisting 기술을 활용하여 효율적으로 관리된다. 또한 스마트 컨트랙트 및 소스 파일은 분산 저장 기술과 Defrag Function 기술을 통해 부분적으로 나뉘어 각 노드에 저장되고, 필요할 때마다 각각의 부분을 호출하여 스트리밍 형식으로 실행할 수 있다.

**< Architecture >**

1.	네트워크 레이어: P2P기반의 오버레이 네트워크. 해당 레이어를 통해 노드 간 트랜잭션을 검증한 뒤 전파한다. 핵심은 기본 네트워크 대역폭을 최대한 활용하는 것이다.
2.	데이터 레이어: 블록체인 데이터 구조 및 물리적 저장공간이다. 머클트리, 해시함수, 데이터 블록, 디지털 사인 등이 포함되며 트랜잭션 내역을 담은 블록과 DApp 파일을 저장한다.
3.	컨센서스 레이어: 트랜잭션을 발생시킨 사용자 노드는 먼저 자신의 트랜잭션을 직접 검증하고 거래내역을 공유한 주변 노드들로부터 과반 이상의 검증을 받은 트랜잭션은 블록 생성으로 생성된다. 이는 다른 노드들에 전파되고 만약 악의적인 공격으로 판단된 노드가 있다면 거래내역이 초기화되고 무결성이 검증된 거래내역으로 동기화 된다. 
4.	어플리케이션 레이어: 블록체인 상단의 어플리케이션 인터페이스를 제공한다. 스마트 컨트렉트, 가상머신, DApp 등이 포함되며 데이터 사용자의 직접적인 연결 고리 역할을 한다.
5.	매니지먼트 레이어: 개발 생태계 형성을 위해 Toolkit과 SDK가 제공되어 3rd Party가 위치한다.  


**< Nodes >**

슈퍼 노드 : 모든 거래 내역과 소스 파일을 보유하고 있는 노드이다. 데이터 무결성을 보증하고, 마이크로 노드와 매크로 노드를 동기화하며, 스마트 컨트랙트를 호출할 때 파일의 위변조 여부를 판단할 수 있는 헤더 값을 마이크로 노드와 매크로 노드에게 전송한다. 

매크로 노드 : Orbits Network에 참여하여 GBT를 얻고자 하는 노드이다. 다른 노드의 트랜잭션을 처리 및 검증하기도 하고 소스 파일을 저장하고 제공하는 역할을 한다.

마이크로 노드 : 일부의 거래내역을 공유하며 자신의 트랜잭션과 타인의 트랜잭션을 일시적으로 처리 및 검증해주는 노드이다.

**< Feature >**

Orbits Network 의 주요 특징은 동시다발적인 트랜잭션(Simultaneous Transaction), 분산화 저장(Distributed Storage), 제네시스 호이스팅(Genesis Hoisting), 그리고 함수 조각 모음(Defragment Function) 이렇게 4가지로 구성된다.

|                |           Process             |          Storage            |
|----------------|-------------------------------|-----------------------------|
|     Ledger     |   Simultaneous Transaction    |      Genesis Hoisting       |
|    Source file   |        Defrag Function        |     Distributed Storage     |





###                   3.1.1. Simultaneous Transaction

순차적인 트랜잭션 처리 구조는 처리 속도의 한계가 있어 확장성의 문제를 초래한다. 확장성 문제를 해결할 수 있는 근본적인 방법은 동시다발적인 트랜잭션의 처리이다. Orbits Network 상에서 구현하려고 하는 동시다발적 트랜잭션의 기본 구조는 하나의 노드가 트랜잭션을 발생시키는 사용자이면서 트랜잭션을 처리하고 검증하는 생산자 구조이다. 이는 트랜잭션이 많이 발생하면 발생할수록 네트워크에 과부하가 걸리는 기존 방식과는 달리, 트랜잭션이 많이 발생하면 트랜잭션을 처리하고 검증하는 노드도 함께 증가하는 구조이기 때문에 확장성의 문제를 해결할 수 있다. 동시다발적인 트랜잭션 처리 구조로 인해 트랜잭션을 모아서 처리할 필요가 없으므로 하나의 트랜잭션 발생과 동시에 하나의 블록이 생성되고 자신과 주변 노드들에 의해 블록의 유효성이 검증되면 자신을 포함해 처리를 담당한 각 노드에 저장된다.


###                   3.1.2. Genesis Hoisting

현재 블록체인 구조는 시간이 지날수록 각 노드에 쌓인 분산 원장의 크기가 동일하게 증가하는 구조이기 때문에 전체 네트워크의 효율성이 저하되고 노드 확장성이 떨어진다. 하지만 블록체인의 상용화를 위해서는 많은 노드가 자유롭게 참여하는 것이 필수적이다. 이를 위해 고안된 것이 Genesis Hoisting이다. Genesis Hoisting은 각 노드가 가진 디바이스의 저장공간이 일정량 이상 다다르면 분산 원장 내역을 정산해 제네시스 파일에 덮어쓰고 모든 블록은 슈퍼 노드로 전송하는 기술이다. 정산 후 파일을 덮어쓰는 과정에서 기존 블록보다 하나 더 높은 블록 인덱스 번호를 부여하므로 기존의 블록을 끌어 올린다는 표현의 Genesis Hoisting이라 칭한다.


###                   3.1.3. Distributed Storage      

현재 DApp은 데이터베이스만 블록체인에 저장하고 소스 파일은 중앙 서버에서 운영되는 구조다. 블록체인 기술과 통신 기술의 근본적인 한계로 인해 하이브리드 구조로 가동되고 있다. 이는 블록체인을 통해 데이터는 보호될 수 있지만 중앙 서버가 무력화되면 시스템이 무너지게 되는 취약한 구조다. 진정한 분산화 어플리케이션은 소스 파일도 분산 저장 및 구동을 할 수 있어야 한다. 하지만 소스 파일을 블록체인에 담는다면 용량이 기하급수적으로 증가하기 때문에 효율적인 저장 시스템과 처리 시스템이 필요하다. 함수들이 메모리 안에 통째로 쌓여 있고, 특정 함수의 기능을 사용하고 싶을 때는 해당 주소로 접근해서 그 안의 내용을 읽는 기존 구조와는 달리 Orbits Network 상의 프로그램 소스는 함수를 기본 단위로 해시화하여 분산 저장한다.


###                   3.1.4. Defrag Function

분산 저장된 DApp을 실시간 스트리밍 형식으로 호출할 수 있는 기술이 Defrag Function이다. 프로그램 소스를 구성하는 함수를 기본 단위로 분산 저장하고 기본 단위인 함수를 호출할 시 다른 노드들과 함수의 해시 값을 비교 검증함으로써 위변조를 막는다. Defrag Function으로 인해 소스 파일의 원본을 모두 저장할 필요 없이 사용하지 않거나 사용 빈도가 적은 함수는 저장하지 않아도 되므로 저장 공간에 대한 부담이 줄어들고 네트워크를 효율적으로 유지할 수 있다. 


##         3.2. Planet Wallet

Planet Wallet은 Orbits Network에 노드 클라이언트이자 공식 지갑이다. 사용자를 확보하기 위해 먼저 메인넷 런칭 이전에는 토큰의 보관과 더불어 휴대폰 번호로 편리하게 토큰을 전송할 수 있는 기능과 어플리케이션 내에서 거래소가 연동되어 토큰의 구매와 판매를 할 수 있는 기능으로 출시될 것이다. 메인넷 런칭 이후에는 노드 어플리케이션 기능과 DApp Store 기능이 추가될 예정이다.


# 4. Ecosystem

Grabity 생태계는 노드, 커뮤니티, DApp, 플랫폼으로 이루어지고 각 구성 주체들은 토큰 이코노미에 기반해 생태계에 기여한다. 우리는 생태계가 잘 작동하고 성장하기 위한 토큰이코노미와 여러 필요 조건들을 다음과 같이 제시한다.


##         4.1. Token Economy

**GBT의 수요**

1. 컴퓨터 자원이 필요한 수요자는 GBT를 구매하여야 한다.
2. Orbits Network 기반 DApp이 진행하는 ICO에 참여하기 위해서는 GBT를 구매하여야 한다.
3. GBT는 DApp의 기축통화로서 DApp의 사용자가 증가한다면 수요가 증가하길 기대할 수 있다.
4. 메인넷 이후 컴퓨터 자원 제공에 따른 보상은 컴퓨터 자원 제공량과 더불어 GBT 보유량이 가산되어 결정되기 때문에 GBT의 수요가 증가하길 기대할 수 있다.


**GBT의 공급**

프로젝트의 개발과 운영을 위한 초기 10,000,000,000 개의 GBT가 이더리움 네트워크상에서 발행된다. ERC20 기반의 GBT는 메인넷 런칭 이후 Orbits Network 기반의 GBT로 교체될 것이다. 또한 메인넷 이후 GBT는 컴퓨터 자원 제공자에게 보상하기 위한 목적으로 인플레이션 비율을 고려하여 추가 발행된다. 인플레이션 비율은 유동적일 수 있지만, 토큰 보유자와 생태계 참여자를 보호하기 위해 5%를 넘지 않는 선에서 결정될 것이다.


**GBT 생태계 진입 인센티브**

컴퓨터 자원의 구매자는 기존 서버를 구축하거나 유지하는 비용보다 저렴하게 GBT를 사용해 Orbits Network를 이용할 수 있고 컴퓨터 자원의 제공자는 자신이 보유한 디바이스의 유휴 자원이나 여분의 디바이스를 Orbits Nerwork에 제공해 GBT를 획득할 수 있다.


##         4.2. DApps

메인넷의 가치는 얼마나 많은 DApp의 사용자를 확보하느냐에 달려있다. 대부분의 DApp 사용자는 기존 어플리케이션 사용자에서 유입되므로 Grabity는 기존 어플리케이션 사용자에게 익숙한 방식의 DApp Store를 제공한다. DApp을 사용하는 필수적인 요건은 토큰의 자유로운 보관과 거래이기 때문에 DApp Store는 지갑 및 거래소를 연동하여 PC와 모바일 버전으로 출시될 것이다. DApp Store의 카테고리는 게임, 금융, 소셜네트워킹, 미디어, 건강, 교육, 음악 등 다양하게 분류 되고 카테고리 내의 순위와 종합 순위는 일 평균 사용자 수, 만족도, 트랜잭션 발생량, 개발 빈도 등을 종합적으로 고려한 알고리즘에 의해 결정된다.


# 5. Roadmap

## **2018 Q4**

스마트 컨트랙트 배포(Deploy)

ERC20 기반 토큰 발행

## **2019 Q1**

네트워크 레이어 개발 (P2P 기반의 오버레이 네트워크 구축)

Planet Wallet 런칭 (Android, iOS)

## **2019 Q2**

데이터 레이어 개발

컨센서스 레이어 개발

## **2019 Q3**

Testnet 런칭

노드 클라이언트 개발

블록 익스플로러 개발




## **2019 Q4**

어플리케이션 레이어 개발

## **2020 Q1**

매니지먼트 레이어 개발

## **2020 Q2**

Orbits Network 런칭

GBT 기반 DEX, DApp Store 런칭

# 6. Token Sale

- 총 토큰 개수 : 10,000,000,000 GBT
- 총 판매 토큰 개수 : 7,000,000,000 GBT
- 총 토큰 개수 대비 판매 토큰 비율 : 70%
- 하드 캡 : 30,000,000 USD
- 소프트 캡 : 10,000,000 USD
  - 프리세일과 퍼블릭세일을 제외한 토큰은 프라이빗 라운드에서 판매된다.
  - 미판매 토큰은 소각 예정이다.

|                |           Pre Sale            |          Public Sale        |
|----------------|-------------------------------|-----------------------------|
|  토큰판매 비율  |              20%               |             30%             |
|    보너스      |              10%              |              0%             |



**< 토큰 분배 >**

|              항목             |             할당량           |
|-------------------------------|-----------------------------|
|          토큰 판매 이벤트      |             70%             |
|      파트너& 어드바이저        |              5%             |
|          Grabity 팀           |             15%             |
|         마케팅 & 홍보         |             10%             |

**< 자금 사용 >**

|              항목             |             사용량           |
|-------------------------------|-----------------------------|
|           기술 개발           |             50%             |
|            생태계             |             20%             |
|           사업 개발           |             10%             |
|             마케팅            |             10%             |
|              예비             |             10%             |



# Reference

1. Nakamoto, S. 31 October 2008. "Bitcoin: A Peer-to-Peer Electronic Cash System". Also known as the Bitcoin whitepaper. http://nakamotoinstitute.org/bitcoin/. http://bitcoin.org/bitcoin.pdf. 
2. W. Dai, "b-money," http://www.weidai.com/bmoney.txt 
3. S. Haber, W.S. Stornetta, "How to time-stamp a digital document," In Journal of Cryptology
4. D. Bayer, S. Haber, W.S. Stornetta, "Improving the efficiency and reliability of digital time-stamping," In Sequences II: Methods in Communication, Security and Computer Science
5. R.C. Merkle, "Protocols for public key cryptosystems," In Proc. 1980 Symposium on Security and Privacy, IEEE Computer Society
6. Ethereum: https://github.com/ethereum/wiki/wiki/White-Paper
7. EOS.IO: https://github.com/EOSIO/Documentation/blob/master/TechnicalWhitePaper.md
8. Smart contracts: https://en.bitcoin.it/wiki/Contracts
9. Merkle trees: http://en.wikipedia.org/wiki/Merkle_tree
10. GHOST: https://eprint.iacr.org/2013/881.pdf
11. Ethereum Merkle Patricia trees: https://github.com/ethereum/wiki/wiki/%5BEnglish%5D-Patricia-Tree
12. Elliptic-curve cryptography (ECC): https://en.wikipedia.org/wiki/Elliptic-curve_cryptography
13. IPFS: https://docs.ipfs.io/

