---
title:  "(코딩테스트 준비) 의사코드 작성 & 장점" 

categories:
  - Algorithm
tags:
  - [Algorithm, Coding Test]

toc: true
toc_sticky: true

date: 2023-03-29
last_modified_at: 2023-03-29
---

## 🚀 서론

의사코드를 작성하기 전 연습되어야 하는 것들 

1. 문제 구조의 이해


2. 논리 문제를 풀듯이 풀 수 있어야함

<br>

### 🔥 의사코드란?


>  자연어를 이용해 만든 문장을 프로그래밍 언어와 유사하게 배치한 코드

- 이질적인 언어체계인 자연어와 프로그래밍 언어를 중계하는 역할
- 자연어의 자유로운 표현과 실제 프로그래밍과 비슷한 순서를 지니어 두 언어의 장점을 적절히 취함

비록 실제 컴파일을 할 수는 없지만 의사코드는 사람이 보라고 만드는 것이기 때문에 별 문제되지 않는다


<br>

### 🔥 의사코드를 작성하는 방법

> 처음에는 자기가 짜려고 하는 언어의 형식에다가 자연어를 넣는다는 느낌으로 만들어보면 된다


- 의사코드는 정해진 작성기준이나 문법 같은게 없다

다만 너무 일관성 없게 작성하면 작성자 개인만 알아볼 수 있게 되므로 여러번 작성해가면서 어느정도의 스타일을 확립해가면 좋다

<br>

### 🔥 의사코드의 장점

0. 자연어와 비슷한 사고 가능
    - 언어를 막 배우기 시작한 시기에 익숙한 자언어로 주어진 문제를 대할 수 있다
      <br><br> 
1. 문제 풀이의 효율성 향상
    - 문제가 복잡하거나 코드의 양이 방대할 경우 자칫하다가 헤메게 될 수 있다
    - 의사코드는 이 경우 일종의 지표로서 작동될 수 있다
      <br><br>

2. 에러 핸들링에 용이
    - 오류 발생 시 의사코드를 참조하여 다른 요소를 제외한 로직에 온전히 집중할 수 있다
      <br><br>

3. 프로그래밍 언어를 잘 모르는 인원과도 소통이 가능하다
   - 자연어로 쓰여있기 때문에 비개발자와 소통시에도 사용될 수 있다



<br>

## 🚀 실습 예제 및 구현 과정

자연어를 사용하여 코딩을 한다고 생각하면서 짜보기
<br><br>

### 🔥 실습 예제 1

> 수를 요소로 갖는 배열을 입력받아, 각 요소들이 그 이전의 요소들의 합보다 큰지를 확인해야 합니다.

```java
// 의사코드 작성

// 배열의 각 요소들이 그 이전의 요소들의 합보다 큰지 여부를 확인하는 함수
public Boolean superIncreasing(int[] arr) {

// 합계를 담을 변수를 선언하고 배열의 0번째 값을 할당

// 그 이후값부터 끝까지 배열을 순회하는 반복문을 작성

  // 만약 arr[i]가 이전의 합보다 작으면 false 리턴
  
  // 그 외의 경우엔 arr[i]를 합계에 더해준다
  
// true값 리턴
```
<br>

#### 💎 의사코드를 기반으로 실제 작성된 코드 💎

```java
// 배열의 각 요소들이 그 이전의 요소들의 합보다 큰지 여부를 확인하는 함수
public Boolean superIncreasing(int[] arr) {

  // 합계를 담을 변수를 선언하고 배열의 0번째 값을 할당
  int sum = arr[0];

  // 그 이후값부터 끝까지 배열을 순회하는 반복문을 작성
  for (int i = 1; i < arr.length; i++) {

    // 만약 arr[i]가 이전의 합보다 작거나 같으면 false 리턴
    if (arr[i] <= sum) {
      return false;
    }  
  
    // 그 외의 경우엔 arr[i]를 합계에 더해준다
    else {
      sum = sum + arr[i]
    } 
  }  
  // true값 리턴
  return true;
}
```

<br><br><br>

### 🔥 실습 예제 2

> 문자열을 입력받아 연속된 한자리 홀수 숫자 사이에 '-'를 추가한 문자열을 리턴하는 함수를 작성해야 합니다.

```java
// 의사코드 작성

// 문자열을 입력받아 연속된 한자리 홀수 숫자 사이에 '-'를 추가한 문자열을 리턴하는 함수
public String insertDash(String str) {
  
  // 결과를 담을 문자열 선언하고 첫값을 담아줌

  // 문자열의 값을 1부터 끝까지 순회하면서

    // charAt(i-1)과 charAt(i)가 모두 홀수라면 결과에 '-'추가
  
    // 결과값에 charAt(i) 추가
    
  // 결과값 리턴
```

<br>

### 🔥 실습 예제 2

> 문자열을 입력받아 연속된 한자리 홀수 숫자 사이에 '-'를 추가한 문자열을 리턴하는 함수를 작성해야 합니다.

```java
// 의사코드 작성

// 문자열을 입력받아 연속된 한자리 홀수 숫자 사이에 '-'를 추가한 문자열을 리턴하는 함수
public String insertDash(String str) {
  
  // 결과를 담을 문자열 선언하고 첫값을 담아줌

  // 문자열의 값을 1부터 끝까지 순회하면서

    // charAt(i-1)과 charAt(i)가 모두 홀수라면 결과에 '-'추가
  
    // 결과값에 charAt(i) 추가
    
  // 결과값 리턴
```

<br>


#### 💎 의사코드를 기반으로 실제 작성된 코드 💎

```java
// 문자열을 입력받아 연속된 한자리 홀수 숫자 사이에 '-'를 추가한 문자열을 리턴하는 함수
public String insertDash(String str) {

  // 결과를 담을 문자열 선언하고 첫값을 담아줌
  String result = "" + str.charAt(0);
  // 문자열의 값을 1부터 끝까지 순회하면서
  for (int i = 1; i < str.length(); i++) {
    int check1 = Character.getNumericValue(str.charAt(i - 1)) % 2;
    int check2 = Character.getNumericValue(str.charAt(i)) % 2;
    // charAt(i-1)과 charAt(i)가 모두 홀수라면 결과에 '-'추가
    if(check1 != 0 && check2 != 0) {
      result = result + "-";
    }
    // 결과값에 charAt(i) 추가
    result = result + str.charAt(i);
  }
  // 결과값 리턴
  return result;
}
```
<br><br>

### 🔥 실습 예제 3

> 브라우저의 뒤로 가기, 앞으로 가기 기능을 구현해야 합니다

```java
// 의사코드 작성

// 행동순서를 입력받아 마지막 페이지와 방문했던 페이지를 반환하는 함수
public ArrayList<Stack> browserStack(String[] actions, String start) {
  
  // 마지막 페이지, 뒤로가기, 앞으로가기 스택과 이 모두를 담을 결과 변수 선언
  
  // 현재 페이지를 current에 push 

  // actions를 순회하면서 각각 케이스 해결

    // 앞으로 가기의 경우 현재 페이지를 꺼내 prevStack에 담고 nextStack을 꺼내 현재 페이지에 담음
  
    // 뒤로 가기의 경우 현재 페이지를 꺼내 nextStack에 담고 prevStack을 꺼내 현재 페이지에 담음
    
    // 그외의 경우는 현재 페이지를 꺼내 prevStack에 담고 주어진 행동을 현재 페이지에 넣음 
    
  // result에 스택 입력후 리턴
```

<br>

#### 💎 의사코드를 기반으로 실제 작성된 코드 💎



```java
// 행동순서를 입력받아 마지막 페이지와 방문했던 페이지를 반환하는 함수
public ArrayList<Stack> browserStack(String[] actions, String start) {
  
  // 마지막 페이지, 뒤로가기, 앞으로가기 스택과 이 모두를 담을 결과 변수 선언
  Stack<String> prevStack = new Stack<>();
  Stack<String> nextStack = new Stack<>();
  Stack<String> current = new Stack<>();
  ArrayList<Stack> result = new ArrayList<>();
  
  // 현재 페이지를 current에 push 
  current.push(start);
  
  // actions를 순회하면서 각각 케이스 해결
  for (String action : actions) {
    // 앞으로 가기의 경우 현재 페이지를 꺼내 prevStack에 담고 nextStack을 꺼내 현재 페이지에 담음
    if (action == "1") {
      if (nextStack.size() != 0) {
        prevStack.push(current.pop());
        current.push(nextStack.pop());
      }
    }
    // 뒤로 가기의 경우 현재 페이지를 꺼내 nextStack에 담고 prevStack을 꺼내 현재 페이지에 담음
    else if (action == "-1") {
      if (prevStack.size() != 0) {
        nextStack.push(current.pop());
        current.push(prevStack.pop());
      }
    }
    // 그외의 경우는 현재 페이지를 꺼내 prevStack에 담고 주어진 행동을 현재 페이지에 넣음 
    else {
      nextStack.clear();
      prevStack.push(current.pop());
      current.push(action);
    }
  }
  // result에 스택 입력후 리턴
  result.add(prevStack);
  result.add(current);
  result.add(nextStack);

  return result;
}
```


<br><br>


### 🔥 실습 예제 4

> 박스 포장대에서 최대 몇명이 한꺼번에 나갈 수 있는지 알아내야 합니다


```java
// 의사코드 작성

// 인원순서대로 포장할 박스갯수가 담긴 배열을 받아서 동시에 나갈 수 있는 최대인원수를 반환하는 함수 
public int paveBox(Integer[] boxes) {
  
  // boxes를 입력받는 LinkedList 형태의 새로운 큐를 선언
  
  // 최대인원 수, 현재 기준 박스갯수, 현재 기준 포장인원을 담을 변수 선언  

  // 큐에 담긴 인원들이 전부 나갈때까지 반복하는 반복문 작성

    // 비교대상이 될 인원을 큐에서 꺼내 box라는 변수에 담음
    
    // 현재 포장중인 boxing보다 작을경우 현재 포장인원수 추가
    
      // 현재 포장인원수가 최대인원수보다 클경우 최대인원수 갱신
  
    // box가 더 오래걸리면 현재 기준이되는 박스갯수를 box로 교체
    
      // 교체 전 인원수가 최대 인원수보다 작거나 같을 경우 현재 포장인원 초기화 후 +1 해줌
      
      // 그외의 경우엔 현재 포장인원을 최대값으로 설정 후 초기화 후 +1 해줌
      
    // 큐가 전부 비었을 경우 마지막까지 계산된 현재 포장인원과 최대 인원수를 비교함
    
  // 계산된 최대인원수 반환
```

<br>

#### 💎 의사코드를 기반으로 실제 작성된 코드 💎

```java
// 인원순서대로 포장할 박스갯수가 담긴 배열을 받아서 동시에 나갈 수 있는 최대인원수를 반환하는 함수 
public int paveBox(Integer[] boxes) {
  
  // boxes를 입력받는 LinkedList 형태의 새로운 큐를 선언
  Queue<Integer> queue = new LinkedList<>(Arrays.asList(boxes));
  
  // 최대인원 수, 현재 기준 박스갯수, 현재 기준 포장인원을 담을 변수 선언  
  int maxPeople = 0;
  int boxing = 0;
  int boxPeople = 0;

  // 큐에 담긴 인원들이 전부 나갈때까지 반복하는 반복문 작성
  while (queue.peek() != null) {
    // 비교대상이 될 인원을 큐에서 꺼내 box라는 변수에 담음
    int box = queue.poll();
    // 현재 포장중인 boxing보다 작을경우 현재 포장인원수 추가
    if (box <= boxing) {
      boxPeople++;
      // 현재 포장인원수가 최대인원수보다 클경우 최대인원수 갱신
      if (maxPeople < boxPeople) {
        maxPeople++;
      }
    }
    // box가 더 오래걸리면 현재 기준이되는 박스갯수를 box로 교체
    if (box > boxing) {
      boxing = box;
      // 교체 전 인원수가 최대 인원수보다 작거나 같을 경우 현재 포장인원 초기화 후 +1 해줌
      if (maxPeople >= boxPeople) {
      boxPeople = 0;
      boxPeople++;
      }
      // 그외의 경우엔 현재 포장인원을 최대값으로 설정 후 초기화 후 +1 해줌
      else {
        maxPeople = boxPeople;
        boxPeople = 0;
        boxPeople++;
      }
    }
    // 큐가 전부 비었을 경우 마지막까지 계산된 현재 포장인원과 최대 인원수를 비교함
    if (queue.isEmpty()) {
      maxPeople = Math.max(maxPeople, boxPeople);
    }      
  }
  // 계산된 최대인원수 반환
  return maxPeople;
}

```


<br><br>

***
<br>

    🌜 개인 공부 기록용 블로그입니다. 오류나 틀린 부분이 있을 경우 
    언제든지 댓글 혹은 메일로 지적해주시면 감사하겠습니다! 😄

[맨 위로 이동하기](#){: .btn .btn--primary }{: .align-right}