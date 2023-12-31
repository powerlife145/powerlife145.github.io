---
layout: post
title: 기술 면접 대비 - 멀티 프로세스와 쓰레드
subtitle: 멀티프로세스와 멀티쓰레드의 특징에 대해 설명해주세요.
categories: 기술면접
tags: [면접대비, cs]
banner:
  image: /assets/images/jobinterview.jpeg
---

## 1. 기술 면접 대비 - 멀티프로세스와 멀티쓰레드의 특징에 대해 설명해주세요.



### 멀티프로세스 (Multi-Process)

1. **독립성**: 각 프로세스는 독립적인 메모리와 자원을 가지므로 하나의 프로세스가 실패해도 다른 프로세스에는 영향을 미치지 않습니다.
2. **보안**: 독립적인 메모리 공간 때문에 프로세스 간 데이터 접근이 제한되어, 보안성이 높습니다.
3. **통신 비용**: 프로세스 간 통신 (IPC)은 복잡하고 비용이 발생합니다.
4. **자원 소모**: 메모리와 CPU를 많이 사용하며, 생성과 소멸이 느리고 비용이 높습니다.
5. **스케줄링**: 운영 체제가 각 프로세스를 독립적으로 스케줄링합니다.



### 멀티쓰레드 (Multi-Thread)

1. **자원 공유**: 같은 프로세스 내 쓰레드들은 메모리와 자원을 공유하므로 통신이 빠르고 간단합니다.
2. **경량**: 쓰레드 생성, 소멸, 컨텍스트 스위칭이 프로세스에 비해 빠르고 경량입니다.
3. **데이터 일관성**: 자원을 공유하기 때문에 데이터 일관성을 유지하기 어렵고, 동기화가 필요합니다.
4. **영향성**: 하나의 쓰레드에서 문제가 발생하면 같은 프로세스 내의 다른 쓰레드에도 영향을 미칠 수 있습니다.
5. **스케줄링**: 멀티쓰레딩은 운영 체제 또는 사용자 레벨에서 스케줄링이 가능합니다.



멀티프로세스와 멀티쓰레드 각각의 특징은 그 사용 케이스를 결정하는 중요한 요소입니다. 예를 들어, 데이터가 많이 공유되어야 하는 작업은 멀티쓰레드가 적합할 수 있고, 독립성과 보안이 중요한 작업은 멀티프로세스가 더 적합할 수 있습니다.



### 면접 답변 :

멀티프로세스는 각각 독립된 메모리와 자원을 가지며, 보안과 안정성이 높습니다. 그러나 자원 소모가 크고 통신이 복잡합니다. 멀티쓰레드는 메모리를 공유해 자원 소모가 적고 통신이 빠르지만, 동기화 문제와 영향성이 있습니다. 어떤 모델을 사용할지는 작업의 독립성, 자원 공유 필요성, 통신 복잡도 등에 따라 달라집니다.



[1]: https://daringfireball.net/projects/markdown/
  [2]: https://www.fileformat.info/info/unicode/char/2163/index.htm
  [3]: https://www.markitdown.net/
  [4]: https://daringfireball.net/projects/markdown/basics
  [5]: https://daringfireball.net/projects/markdown/syntax
