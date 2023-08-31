---
layout: post
title: 기술 면접 대비 - DB 로직 최소화
subtitle: DB 로직 최소화를 하려면 어떻게 해야 할까요?
categories: 기술면접
tags: [면접대비, cs]
banner:
  image: /assets/images/jobinterview.jpeg
---

## 1. 기술 면접 대비 - DB 로직 최소화를 하려면 어떻게 해야 할까요?

DB 로직을 최소화하는 것은 시스템 성능과 유지 보수성을 높이는 중요한 작업입니다. 여기 몇 가지 방법을 소개합니다:

1. **비즈니스 로직 분리**: 데이터베이스에서 처리하는 로직은 간단하게 유지하고, 복잡한 비즈니스 로직은 애플리케이션 레벨에서 처리합니다.
2. **불필요한 쿼리 줄이기**: 필요한 데이터만 쿼리하여, 불필요한 데이터 접근을 줄입니다. `SELECT *` 대신 필요한 컬럼만 명시합니다.
3. **캐싱 사용**: 자주 사용되는 쿼리 결과나 계산 값은 애플리케이션 레벨에서 캐시하여 불필요한 DB 접근을 줄입니다.
4. **배치 처리**: 여러 작업을 묶어 한 번의 쿼리로 처리하여 DB 접근을 최소화합니다.
5. **인덱싱과 파티셔닝**: 적절한 인덱스와 데이터 파티셔닝을 사용하여 쿼리 성능을 높이고, DB 부하를 줄입니다.
6. **프리페어드 스테이트먼트**: 동일한 쿼리가 여러 번 실행될 경우, 프리페어드 스테이트먼트를 사용하여 파싱과 컴파일 시간을 줄입니다.
7. **응용 프로그램 로직의 최적화**: DB에 전달되는 데이터를 미리 검증하거나 정제하여, DB에서 이를 처리할 필요를 없애거나 줄입니다.
8. **로직 간소화**: 저장 프로시저, 트리거, 뷰 등을 과도하게 사용하는 것은 복잡성을 증가시킬 수 있으므로, 필요한 경우에만 사용합니다.

이러한 방법들은 애플리케이션과 데이터베이스의 특성, 그리고 트래픽 패턴에 따라 적용할 필요가 있습니다.

### 면접 답변 :
DB 로직을 최소화하기 위해서는 복잡한 비즈니스 로직을 애플리케이션 레벨에서 처리하고, 필요한 데이터만 쿼리해야 합니다. 자주 사용되는 쿼리 결과는 캐싱하여 DB 접근을 줄이고, 배치 처리를 통해 여러 작업을 한 번에 처리합니다. 인덱싱과 데이터 파티셔닝을 적절히 활용해 성능을 높이며, 불필요한 저장 프로시저나 트리거는 피합니다.


[1]: https://daringfireball.net/projects/markdown/
  [2]: https://www.fileformat.info/info/unicode/char/2163/index.htm
  [3]: https://www.markitdown.net/
  [4]: https://daringfireball.net/projects/markdown/basics
  [5]: https://daringfireball.net/projects/markdown/syntax