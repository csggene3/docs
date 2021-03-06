# 네오 노드 소개 (NEO node introduction)

풀 노드는 모든 블록체인 데이터를 저장하는 노드를 말합니다. 이 노드들은 P2P 네트워크를 통해 블록체인에 연결되어 있습니다. 블록체인 네트워크안에서, 모든 노드들은 동등하며 동시에 클라이언트와 서버로써 작동합니다..

두 가지의 풀노드 프로그램이 있습니다. 하나는 일반 유저를 위한 GUI(graphical user interface)인터페이스를 가지고 있으며, 기본적인 기능을 가진 유저 클라이언트입니다. 우리는 이 프로그램을 Neo-GUI라고 부릅니다.

다른 하나는 개발자들을 위한 프로그램이며, 커맨드 라인 인터페이스를 가지고 있으며 기본적인 지갑 기능을 하는 외부 API를 제공합니다. 이 노드 프로그램은 다른 노드들이 네트워크 상에서 컨센서스(concensus)를 이룰 수 있게 하며 새로운 블록 생성에도 기여합니다. 우리는 이 프로그램을 Neo-CLI라고 부릅니다. 

이제부터는 NEO [네트워트 프로토콜](network-protocol.md)에 대해 설명하겠습니다. 이 프로토콜은 아직 CLI에서 지원하지 않는, 지갑을 실행하지 않고 네오를 보내거나 GAS를 요청하거나 하는 등의 저 수준(low level)의 API를 제공합니다.
 
## 네오 노드 다운로드 주소

|      | Neo-GUI                        | Neo-CLI                        |
| ---- | ---------------------------------------- | ---------------------------------------- |
| 릴리즈 | [Official website](https://www.neo.org/download) or [Github](https://github.com/neo-project/neo-gui/releases) | [Github](https://github.com/neo-project/neo-cli/releases) |
| 소스코드 | [Github](https://github.com/neo-project/neo-gui) | [Github](https://github.com/neo-project/neo-cli) |

## GUI 노드와 CLI 노드 프로그램간의 기능 비교

|           | GUI  | CLI  |
| --------- | ---- | ---- |
| 그래픽 인터페이스 | ✅    |      |
| 커맨드 라인 인터페이스 |      | ✅    |
| 지갑 생성 | ✅    | ✅    |
| 지갑 실행 | ✅    | ✅  |
| 지갑 지수 재건(Wallet Index) | ✅    | ✅    |
| 모든 키 쌍(Pair) 보여주기 | ✅    | ✅    |
| 키 쌍 가져오기/내보내기 | ✅    | ✅    |
| 모든 주소 보여주기 | ✅    | ✅    |
| 모든 자산 보여주기 | ✅    | ✅    |
| 주소 생성 | ✅    | ✅    |
| 이전 | ✅    | ✅    |
| 전송 (자산 교환)  | ✅    |      |
| 다자간 서명 계약 생성 | ✅    |      |
| 사용자 설정 스마트 계약 생성 | ✅    |      |
| 서명 | ✅    |      |
| 선거 컨센서스 노드 | ✅    |      |
| 투표 | ✅    |      |
| 자산 등록 | ✅    |      |
| 자산 배분 | ✅    |      |
| NEO 추출(Extraction) | ✅    |      |
| 주소 묶음(Batch) 생성  |      | ✅    |
| JSON-RPC |      | ✅    |
| 참여하는 블록에 대한 동의(consensus) |      | ✅    |

## 포트 설명 (Port description)

만약 여러분꼐서 노드 API에 접근하는 외부 프로그램을 원하시면, 아래 포트들에 대해 방화벽을 열어두어야 합니다. 다음은 각 포트들에 대한 설명입니다.

|                    | 메인 넷 | 테스트 넷 |
| ------------------ | ------------ | ------------- |
| JSON-RPC via HTTPS | 10331        | 20331         |
| JSON-RPC via HTTP  | 10332        | 20332         |
| P2P via TCP        | 10333        | 20333         |
| P2P via WebSocket  | 10334        | 20334         |

좀 더 자세한 정보는 다음을 참고하세요 : [테스트 네트워크](testnet.md).
