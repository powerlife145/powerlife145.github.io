---
layout: post
title: 기술 면접 대비 - 정렬 알고리즘
subtitle: 정렬 알고리즘에 대해서 아는대로 설명해주세요.
categories: 기술면접
tags: [면접대비, cs]
banner:
  image: /assets/images/jobinterview.jpeg
---

## 1. 기술 면접 대비 - 정렬 알고리즘에 대해서 아는대로 설명해주세요.

### 정렬 알고리즘

정렬 알고리즘은 데이터를 특정 순서대로 나열하는 알고리즘입니다. 일반적으로 오름차순 또는 내림차순으로 데이터를 정렬합니다. 여러 가지 정렬 알고리즘이 있고, 각각의 알고리즘은 특정 상황에서 장점과 단점을 가집니다.

#### 대표적인 정렬 알고리즘들

1. 버블 정렬 (Bubble Sort)
  - 간단하나 비효율적, 인접한 두 원소를 비교하여 정렬
  - 시간 복잡도: O*(*n*2)
2. 선택 정렬 (Selection Sort)
  - 가장 작은(또는 큰) 원소를 선택하여 앞으로 옮김
  - 시간 복잡도: O*(*n*2)
3. 삽입 정렬 (Insertion Sort)
  - 각 원소를 알맞은 위치에 삽입
  - 시간 복잡도: O*(*n*2), 이미 정렬된 데이터에 대해서는 O*(*n*)
4. 퀵 정렬 (Quick Sort)
  - 피벗을 기준으로 분할하고 재귀적으로 정렬
  - 시간 복잡도: O(nlogn)*O*(*n*log*n*) ~ O*(*n*2)
5. 병합 정렬 (Merge Sort)
  - 데이터를 분할하고 병합하면서 정렬
  - 시간 복잡도: O(nlog⁡n)*O*(*n*log*n*)
6. 힙 정렬 (Heap Sort)
  - 힙 자료구조를 이용하여 정렬
  - 시간 복잡도: O(nlog⁡n)*O*(*n*log*n*)

#### 선택 기준

- **데이터의 크기와 상태**: 작은 데이터셋에는 단순한 알고리즘이 유용할 수 있습니다.
- **안정성**: 안정 정렬(stable sort)이 필요한지 여부도 고려해야 합니다.
- **메모리 사용**: 제자리 정렬(in-place sort)가 필요한 경우도 있습니다.

### 면접용 5줄 요약

정렬 알고리즘은 데이터를 특정 순서로 배열하는 방법입니다. 버블, 선택, 삽입 정렬은 기본적이지만 비효율적인 방법입니다. 퀵 정렬과 병합 정렬은 �(�log⁡�)*O*(*n*log*n*)의 시간 복잡도로 더 빠르며, 대용량 데이터에 적합합니다. 힙 정렬은 힙 자료구조를 사용해 효율적으로 정렬합니다. 알고리즘 선택 시 데이터의 크기, 상태, 안정성 요구사항을 고려해야 합니다.

[1]: https://daringfireball.net/projects/markdown/
[2]: https://www.fileformat.info/info/unicode/char/2163/index.htm
[3]: https://www.markitdown.net/
[4]: https://daringfireball.net/projects/markdown/basics
[5]: https://daringfireball.net/projects/markdown/syntax
