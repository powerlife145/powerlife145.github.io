---
layout: post
title: 기술 면접 대비 - 쿼리 최적화
subtitle: 쿼리 최적화에 대해 설명해주시고 방법에 대해 설명해주세요.
categories: 기술면접
tags: [면접대비, cs]
banner:
  image: /assets/images/jobinterview.jpeg
---

## 1. 기술 면접 대비 - 쿼리 최적화에 대해 설명해주시고 방법에 대해 설명해주세요.



###  쿼리 최적화란?

쿼리 최적화는 데이터베이스에서 SQL 쿼리의 성능을 향상시키는 과정입니다. 목표는 가능한 빠른 시간 내에 결과를 얻는 것이며, 이를 위해 더 적은 자원을 사용하도록 쿼리를 수정하는 것이 일반적입니다.



### 쿼리 최적화 방법

1. **인덱스 사용**: 적절한 인덱스를 사용하여 데이터 검색 속도를 높입니다.
2. **조인 전략**: 조인에 사용되는 테이블의 크기와 순서를 최적화합니다. 작은 테이블을 먼저 조인하는 것이 유리할 수 있습니다.
3. **프로젝션 최적화**: 필요한 컬럼만 선택하여 불필요한 데이터 전송을 줄입니다.
4. **서브쿼리와 뷰 최적화**: 가능하다면 서브쿼리를 조인으로 변경하거나, 뷰를 사용하여 복잡한 쿼리를 단순화합니다.
5. **데이터 통계와 분석 함수 활용**: 데이터베이스 엔진이 제공하는 통계나 분석 함수를 활용하여 쿼리 플랜을 이해하고 최적화합니다.
6. **LIMIT과 OFFSET 사용**: 필요한 데이터만 추출하여 전체 데이터를 스캔하는 비용을 줄입니다.
7. **캐싱**: 자주 사용되는 쿼리 결과를 캐시하여 재사용합니다.
8. **배치 처리**: 여러 작업을 묶어 한 번에 처리하여 오버헤드를 줄입니다.

쿼리 최적화는 끊임없이 모니터링과 수정이 필요한 반복적인 작업입니다. 데이터의 양, 구조, 사용 패턴에 따라 최적의 쿼리 전략이 달라질 수 있으므로, 계속해서 성능을 모니터링하고 필요한 최적화를 적용해야 합니다.



### 면접 대비 :

쿼리 최적화는 데이터베이스에서 SQL 쿼리의 실행 성능을 향상시키는 과정입니다. 인덱스를 적절히 사용하고, 필요한 컬럼만 선택하여 자원을 효율적으로 사용할 수 있습니다. 조인 전략을 잘 선택하고, 서브쿼리를 최적화하여 빠른 결과를 얻을 수 있습니다. 일반적으로는 데이터베이스의 통계와 분석 함수를 활용해 쿼리 플랜을 이해하고 수정합니다. 이러한 최적화는 지속적인 모니터링과 튜닝이 필요합니다.


### 면접 답변 :

멀티프로세스는 각각 독립된 메모리와 자원을 가지며, 보안과 안정성이 높습니다. 그러나 자원 소모가 크고 통신이 복잡합니다. 멀티쓰레드는 메모리를 공유해 자원 소모가 적고 통신이 빠르지만, 동기화 문제와 영향성이 있습니다. 어떤 모델을 사용할지는 작업의 독립성, 자원 공유 필요성, 통신 복잡도 등에 따라 달라집니다.



[1]: https://daringfireball.net/projects/markdown/
  [2]: https://www.fileformat.info/info/unicode/char/2163/index.htm
  [3]: https://www.markitdown.net/
  [4]: https://daringfireball.net/projects/markdown/basics
  [5]: https://daringfireball.net/projects/markdown/syntax