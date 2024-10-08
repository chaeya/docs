# Android Wallet Core SDK

Welcome to the Android Wallet Core SDK Repository. <br>
This repository provides an SDK for developing an Android mobile wallet.

## Folder Structure
```
opendid-core-sdk-aos
├── CHANGELOG.md
├── CLA.md
├── CODE_OF_CONDUCT.md
├── CONTRIBUTING.md
├── LICENSE.dependencies.md
├── MAINTAINERS.md
├── README.md
├── RELEASE-PROCESS.md
├── SECURITY.md
├── docs
│   ├── api
│   │   ├── DIDManager.md
│   │   ├── DIDManager_ko.md
│   │   ├── KeyManager.md
│   │   ├── KeyManager_ko.md
│   │   ├── SecureEncryptor.md
│   │   ├── SecureEncryptor_ko.md
│   │   ├── VCManager.md
│   │   ├── VCManager_ko.md
│   │   └── WalletCoreError.md
│   └── design
├── sample
└── source
    └── WalletCore
        ├── README.md
        ├── README_ko.md
        ├── build.gradle
        ├── gradle
        ├── gradle.properties
        ├── gradlew
        ├── gradlew.bat
        ├── libs
        ├── local.properties
        ├── release
        ├── settings.gradle
        └── src
```

| Name                    | Description                                     |
| ----------------------- | ----------------------------------------------- |
| source                  | SDK source code project                         |
| docs                    | Documentation                                   |
| ┖ api                   | API guide documentation                         |
| ┖ design                | Design documentation                            |
| sample                  | Samples and data                                |
| README.md               | Overview and description of the project         |
| CLA.md                  | Contributor License Agreement                   |
| CHANGELOG.md            | Version-specific changes in the project         |
| CODE_OF_CONDUCT.md      | Code of conduct for contributors                |
| CONTRIBUTING.md         | Contribution guidelines and procedures          |
| LICENSE.dependencies.md | Licenses for the project’s dependency libraries |
| MAINTAINERS.md          | General guidelines for maintaining              |
| RELEASE-PROCESS.md      | Release process                                 |
| SECURITY.md             | Security policies and vulnerability reporting   |

## Libraries

Libraries can be found in the [releases folder](source/WalletCore/release).


1. Copy the `opendid-core-sdk-aos-1.0.0.jar` file to the libs of the app project.
2. Add the following dependencies to the build.gradle of the app project.

```groovy
    implementation files('libs/opendid-core-sdk-aos-1.0.0.jar')
    implementation 'com.google.code.gson:gson:2.10.1'
    implementation 'androidx.biometric:biometric:1.1.0'

    implementation 'com.madgag.spongycastle:core:1.54.0.0'
    implementation 'com.madgag.spongycastle:prov:1.54.0.0'
    implementation 'com.madgag.spongycastle:pkix:1.54.0.0'
    implementation 'com.madgag.spongycastle:pg:1.54.0.0'
```
3. Sync `Gradle` to ensure the dependencies are properly added.

## API Reference

API Reference can be found [here](source/WalletCore/README.md)


## Contributing

Please read [CONTRIBUTING.md](CONTRIBUTING.md) and [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md) for details on our code of conduct, and the process for submitting pull requests to us.


## License
Copyright 2024 Raonsecure


---
# Android Wallet Core SDK Guide
This document is a guide for using the OmniOne Open DID Wallet Core SDK, providing functions to generate, store, and manage the keys, DID Document, and Verifiable Credential (VC) information required for OmniOne Open DID.


## S/W Specifications
| Component | Requirement                |
|------|----------------------------|
| OS  | Android 13|
| Language  | Java 17|
| IDE  | Android Studio 4|
| Build System  | Gradle 8.2 |
| Compatibility | Android API level 33 or higher  |

<br>


## Build Method
: Execute the export JAR task in the build.gradle file of this SDK project to generate a JAR file.
1. Open the project's `build.gradle` file and add the following `export JAR` task.
```groovy
ext {
    version = "1.0.0"
}

task exportJar(type: Copy){
    from('build/intermediates/aar_main_jar/release/')
    into('release/')
    include('classes.jar')
    rename('classes.jar', 'opendid-core-sdk-aos-${version}.jar')
}
```
2. Open the `Gradle` window in Android Studio, and run the `Tasks > other > exportJar` task of the project.
3. Once the execution is complete, the `opendid-core-sdk-aos-1.0.0.jar` file will be generated in the `release/` folder.

<br>

## SDK Application Method
1. Copy the `opendid-core-sdk-aos-1.0.0.jar` file to the libs of the app project.
2. Add the following dependencies to the build.gradle of the app project.

```groovy
    implementation files('libs/opendid-core-sdk-aos-1.0.0.jar')
    implementation 'com.google.code.gson:gson:2.10.1'
    implementation 'androidx.biometric:biometric:1.1.0'

    implementation 'com.madgag.spongycastle:core:1.54.0.0'
    implementation 'com.madgag.spongycastle:prov:1.54.0.0'
    implementation 'com.madgag.spongycastle:pkix:1.54.0.0'
    implementation 'com.madgag.spongycastle:pg:1.54.0.0'
```
3. Sync `Gradle` to ensure the dependencies are properly added.

<br>

## API Specification
| Classification | API Document Link |
|------|----------------------------|
| KeyManager  | [Wallet Core SDK - KeyManager API](docs/api/KeyManager.md) |
| DIDManager  | [Wallet Core SDK - DIDManager API](docs/api/DIDManager.md) |
| VCManager  | [Wallet Core SDK - VCManager API](docs/api/VCManager.md)  |
| SecureEncryptor | [Wallet Core SDK - SecureEncryptor API](docs/api/SecureEncryptor.md)  |
| ErrorCode      | [Error Code](docs/api/WalletCoreError.md) |

### KeyManager
KeyManager provides the functionality to generate and manage key pairs for signing and store them securely.<br>The main features are as follows:

* <b>Key Generation</b>: Generates a new key pair.
* <b>Key Storage</b>: Securely stores the generated key.
* <b>Key Retrieval</b>: Retrieves the stored key.
* <b>Key Deletion</b>: Deletes the stored key.

### DIDManager
DIDManager provides the functionality to generate and manage DID Documents.<br>The main features are as follows:

* <b>DID Generation</b>: Generates a new DID.
* <b>DID Document Management</b>: Creates, updates, and deletes DID Documents.
* <b>DID Document Retrieval</b>: Retrieves information about DID Documents.

### VCManager
VCManager provides the functionality to manage and store Verifiable Credentials (VC).<br>The main features are as follows:

* <b>VC Storage</b>: Securely stores the generated VC.
* <b>VC Retrieval</b>: Retrieves the stored VC.
* <b>VC Deletion</b>: Deletes the stored VC.

### SecureEncryptor
SecureEncryptor provides the functionality to encrypt and decrypt data using the Keystore.<br>The main features are as follows:

* <b>Data Encryption</b>: Securely encrypts the data.
* <b>Data Decryption</b>: Decrypts the encrypted data.

---
# Android Wallet Core SDK

Android Wallet Core SDK는 Android 환경에서 DID(분산 식별자)와 검증 가능한 자격증명(VC)을 관리하는 데 필요한 기능을 제공합니다.

## 설치 방법
### 요구 사항
- **OS**: Android 13 이상
- **Language**: Java 17
- **IDE**: Android Studio 4
- **Build System**: Gradle 8.2 이상

### 설치 절차
1. 프로젝트에 SDK 추가:
    ```gradle
    implementation files('libs/opendid-core-sdk-aos-1.0.0.jar')
    ```

2. Gradle 동기화:
    ```bash
    ./gradlew sync
    ```

## 주요 API 설명
### KeyManager
- **키 생성**: 새로운 키 쌍을 생성합니다.
- **키 저장**: 생성된 키를 안전하게 저장합니다.
- **키 검색**: 저장된 키를 검색합니다.
- **키 삭제**: 저장된 키를 삭제합니다.

### DIDManager
- **DID 생성**: 새로운 DID를 생성합니다.
- **DID 관리**: DID 문서를 생성, 업데이트, 삭제합니다.
- **DID 검색**: 기존 DID 정보를 검색합니다.

### VCManager
- **VC 저장**: 생성된 검증 가능한 자격 증명을 저장합니다.
- **VC 검색**: 저장된 자격 증명을 검색합니다.
- **VC 삭제**: 자격 증명을 삭제합니다.

## 고급 기능
- **보안 암호화**: SecureEncryptor API를 통해 데이터를 안전하게 암호화하고 복호화할 수 있습니다.
