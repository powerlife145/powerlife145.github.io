---
layout: post
title: 기술 면접 대비 - AWS S3, EC2
subtitle: AWS S3, EC2를 사용하는 이유와 사용 경험에 대해서 답변해주세요.
categories: 기술면접
tags: [면접대비, cs]
banner:
  image: /assets/images/jobinterview.jpeg
---

## 1. 기술 면접 대비 - AWS S3, EC2를 사용하는 이유와 사용 경험에 대해서 답변해주세요.

### AWS S3와 EC2의 사용 이유

1. AWS S3 (Simple Storage Service)
  - **확장성**: 대용량 데이터를 손쉽게 저장하고 관리할 수 있습니다.
  - **내구성과 가용성**: 데이터는 여러 물리적 위치에 분산 저장되므로 높은 내구성과 가용성을 보장합니다.
2. AWS EC2 (Elastic Compute Cloud)
  - **유연성**: 다양한 인스턴스 타입과 사용자 정의가 가능합니다.
  - **자동 스케일링**: 트래픽에 따라 자동으로 리소스를 조절할 수 있습니다.

### 사용 경험

제가 작업한 프로젝트에서는 AWS S3를 파일 저장소로, EC2를 메인 서버로 사용했습니다. 초기에는 단일 EC2 인스턴스로 충분했으나 트래픽이 증가함에 따라 성능 이슈가 발생했습니다. 이를 해결하기 위해 AWS의 로드 밸런서를 도입하여 여러 EC2 인스턴스에 트래픽을 분산시켰습니다. 이렇게 해서 시스템의 가용성과 처리 능력을 향상시켰고, S3의 확장성을 활용하여 데이터 저장도 효율적으로 관리할 수 있었습니다.

### 면접용 5줄 요약

AWS S3는 확장성 높은 스토리지 서비스로, EC2는 유연하고 자동 스케일링이 가능한 컴퓨팅 서비스입니다. 저는 프로젝트에서 S3를 파일 저장소, EC2를 메인 서버로 사용했습니다. 트래픽 증가로 인한 부하를 처리하기 위해 AWS 로드 밸런서를 도입하여 EC2 인스턴스를 확장했습니다. 이를 통해 시스템의 성능과 가용성을 향상시켰습니다.

[1]: https://daringfireball.net/projects/markdown/
[2]: https://www.fileformat.info/info/unicode/char/2163/index.htm
[3]: https://www.markitdown.net/
[4]: https://daringfireball.net/projects/markdown/basics
[5]: https://daringfireball.net/projects/markdown/syntax
