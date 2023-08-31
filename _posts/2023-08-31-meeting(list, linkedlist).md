---
layout: post
title: 기술 면접 대비 - Array, LinkedList
subtitle: Array, LinkedList에 대해 설명해주시고 각각 어떻게 사용하는지 말씀해주세요.
categories: 기술면접
tags: [면접대비, cs]
banner:
  image: /assets/images/jobinterview.jpeg
---

## 1. 기술 면접 대비 - Array, LinkedList에 대해 설명해주시고 각각 어떻게 사용하는지 말씀해주세요.

### Array (배열)

**정의**: 배열은 메모리에서 연속적으로 할당된 공간에 동일한 타입의 데이터를 저장하는 데이터 구조입니다.

**장점**:

- 빠른 조회 속도: 인덱스를 통해 O(1) 시간에 접근 가능
- 메모리 효율성: 연속된 메모리 공간을 사용하므로 공간 효율성이 높음

**단점**:

- 크기가 고정: 크기를 미리 정해야 하며, 크기 변경이 어려움
- 삽입/삭제 비효율: 중간에 요소를 삽입하거나 삭제할 경우 O(n) 시간이 소요됨

**사용법**:

```java
javaCopy code
int[] arr = new int[5];
arr[0] = 1;
arr[1] = 2;
// ... 등
```

### LinkedList (연결 리스트)

**정의**: 연결 리스트는 노드들이 포인터를 통해 서로 연결되어 있는 데이터 구조입니다.

**장점**:

- 동적 크기: 노드를 동적으로 할당하여 크기 변경이 용이함
- 삽입/삭제 효율: O(1) 시간에 삽입과 삭제 가능

**단점**:

- 조회 속도: 특정 인덱스의 요소에 접근하기 위해서는 O(n) 시간이 소요됨
- 메모리 비효율: 포인터에 대한 추가 메모리가 필요함

**사용법**:

```java
javaCopy code
LinkedList<Integer> linkedList = new LinkedList<>();
linkedList.add(1);
linkedList.add(2);
// ... 등
```

### 요약

- 배열은 빠른 조회가 필요하거나, 메모리를 효율적으로 사용해야 할 때 유용합니다.
- 연결 리스트는 자주 삽입/삭제 작업이 일어나거나, 크기를 동적으로 변경해야 할 때 유용합니다.



### 면접답변 :

배열은 연속적인 메모리 공간에 데이터를 저장하며, 빠른 데이터 조회가 가능하지만 크기가 고정되어 있습니다. 연결 리스트는 노드들이 포인터로 연결되어 있어, 크기가 동적이고 삽입/삭제가 유연하지만 조회 속도가 느립니다. 배열은 빠른 조회가 중요할 때, 연결 리스트는 자주 데이터를 삽입/삭제해야 할 때 사용합니다. 예를 들어, 자바에서는 배열은 `int[] arr = new int[5];`로, 연결 리스트는 `LinkedList<Integer> linkedList = new LinkedList<>();`로 사용할 수 있습니다.

[1]: https://daringfireball.net/projects/markdown/
[2]: https://www.fileformat.info/info/unicode/char/2163/index.htm
[3]: https://www.markitdown.net/
[4]: https://daringfireball.net/projects/markdown/basics
[5]: https://daringfireball.net/projects/markdown/syntax
