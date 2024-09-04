# OmniOne Open DID

**OmniOne Open DID** is an open source project that aims to drive global adoption and expansion of self-sovereign identity through a secure identity system based on the technology that built the Republic of Korea's national mobile ID.

**OmniOne Open DID** is an open source decentralized identifier (DID) designed to provide developers with the tools they need to integrate self-sovereign identity management into their applications, built to be secure, scalable, and interoperable by adhering to the latest DID standards.

## Goals

- We aim to provide a digital identity authentication system through the OmniOne Open DID platform based on trust and responsibility to various members of the digital world.
- Through this, we reduce social costs and enable the socially excluded from the infrastructure to fulfill their “social responsibility for realizing human values.”

## Structure
The OmniOne Open DID system consists of a Trust Environment for establishing a trust chain between participating entities, a Wallet for storing and managing various certificates based on Digital ID, a Digital ID that includes various certificates, and Security for data protection.

- **Trust Environment**: The components of OmniOne Open DID define and develop methods for establishing a chain of trust between components to build a trust environment based on Digital IDs.
- **Wallet**: Define the lifecycle of the wallet and e-signs and develops the architecture for key management, storage management, access control management, and security management of the wallet.
- **Digital ID**: Define a data model based on W3C’s Decentralized Identifier and Verifiable Credentials specifications.
- **Security**: Ensures a level of security that ensures the authenticity, confidentiality, and integrity of data exchanged between OmniOne Open DID components.

## Getting Started

### Prerequisites

Before you begin, ensure you have met the following requirements:

- **Node.js** (version 14 or later)
- **npm** (version 6 or later)
- **Git** (for cloning the repository)
- A basic understanding of decentralized identities and blockchain technology is recommended.

### Installation

To install OmniOne, follow these steps:

1. **Clone the Repository**:

    ```bash
    git clone https://github.com/yourusername/OmniOne.git
    cd OmniOne
    ```

2. **Install Dependencies**:

    ```bash
    npm install
    ```

### Usage

OmniOne Open DID provides a set of commands to manage DIDs. Below are some basic usage examples:

- **Start the DID Service**:

    To start the OmniOne DID service:

    ```bash
    npm start
    ```

- **Create a New DID**:

    To create a new DID:

    ```bash
    npm run create-did
    # Output: did:omni:123456789abcdefghi
    ```

- **Resolve an Existing DID**:

    To resolve and retrieve details of an existing DID:

    ```bash
    npm run resolve-did did:omni:123456789abcdefghi
    # Output: { "@context": "https://www.w3.org/ns/did/v1", "id": "did:omni:123456789abcdefghi", ... }
    ```

### Examples

Here’s how you can use OmniOne Open DID in your project:

- **Integrating with a Web Application**: OmniOne can be integrated into a web application to enable users to authenticate using their DIDs.
- **Cross-Chain DID Resolution**: Utilize OmniOne's interoperability features to resolve DIDs across different blockchain networks.

### Contributing

We welcome and appreciate contributions from the community! To contribute to OmniOne Open DID:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/your-feature`).
3. Make your changes.
4. Commit your changes (`git commit -m 'Add some feature'`).
5. Push to the branch (`git push origin feature/your-feature`).
6. Open a Pull Request.

Please ensure that your code adheres to our [contribution guidelines](CONTRIBUTING.md) and is covered by tests where appropriate.

### License

This project is licensed under the Apache License 2.0. See the [LICENSE](LICENSE) file for details.
Apache License 2.0 : http://www.apache.org/licenses/LICENSE-2.0

Check out the licenses of other open sources used in the project below.

* [LICENSE-dependencies](/LICENSE-dependencies.md)

### Acknowledgments

OmniOne Open DID was made possible thanks to the contributions of the open-source community and the support of various partners.

### Contact

For further inquiries or support, please contact us at [technical@omnione.com](mailto:technical@omnione.net).

## Additional Resources

- **Documentation**: Detailed documentation is available in the [docs](docs) folder.
- **Issue Tracking**: Please report issues or request features via the [GitHub Issues](https://github.com/yourusername/OmniOne/issues) page.
- **Community Discussions**: Join our [community forum](https://community.omnione.com) to discuss OmniOne and decentralized identity.

## Roadmap

OmniOne Open DID is under active development. Here are some features we're planning to add:

- **Support for additional DID methods**
- **Enhanced privacy features**
- **Integration with more blockchain networks**
- **Improved scalability and performance**

Stay tuned for updates!


---
# OmniOne Digital ID

OmniOne Digital ID는 전 세계 자율적 신원(Self-Sovereign Identity, SSI)을 촉진하고 확산하기 위해 구축된 개방형 분산 식별자(DID) 시스템입니다. 이 프로젝트는 보안성, 확장성, 상호 운용성을 목표로 하며, 최신 DID 표준을 준수하여 설계되었습니다.

## 목표
- **신뢰성 있는 디지털 ID 인증 시스템 제공**: OPEN DID 플랫폼을 통해 디지털 세계에서 신뢰할 수 있는 인증 환경을 제공합니다.
- **사회적 포용성 증대**: 디지털 인프라에서 소외된 사회적 약자도 디지털 신원을 통해 자신의 가치를 실현할 수 있도록 지원합니다.

## 주요 구성 요소
- **Trust Environment**: 디지털 ID 기반의 신뢰 체인을 형성하는 신뢰 환경을 구축합니다.
- **Wallet**: DID 및 검증 가능한 자격증명(VC)을 저장 및 관리하는 디지털 지갑.
- **Digital ID**: W3C의 분산 식별자와 검증 가능한 자격 증명(VC) 사양을 준수하는 데이터 모델.
- **Security**: 시스템 내 데이터를 안전하게 보호하는 보안 시스템.

## 설치 방법
### 요구 사항
- **Node.js**: 버전 14 이상
- **npm**: 버전 6 이상
- **Git**: 리포지토리 클론에 필요

### 설치 절차
1. 리포지토리 클론:
    ```bash
    git clone https://github.com/yourusername/OmniOne.git
    cd OmniOne
    ```
2. 의존성 설치:
    ```bash
    npm install
    ```

3. DID 서비스 시작:
    ```bash
    npm start
    ```

### 기본 사용법
- **새로운 DID 생성**:
    ```bash
    npm run create-did
    ```

- **기존 DID 조회**:
    ```bash
    npm run resolve-did did:omni:123456789abcdefghi
    ```

### 기여 가이드
- GitHub 리포지토리를 포크하고, 브랜치를 생성한 후 Pull Request를 통해 기여할 수 있습니다.
- 문서 및 비개발 관련 기여(버그 리포트, 기능 요청 등)도 환영합니다.

### 보안
OmniOne 시스템의 보안은 데이터의 무결성과 기밀성을 보장합니다. 모든 데이터는 암호화되며, 보안 취약점 발견 시 GitHub 이슈 페이지를 통해 보고할 수 있습니다.
