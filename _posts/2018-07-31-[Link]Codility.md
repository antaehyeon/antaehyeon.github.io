---
layout: post
title:  "[Link] Codility Link"
subtitle:   "Link"
categories: link
tags: link
comments: true
---

> Codility 에서 푼 문제 링크를 보관할 글 입니다.**

1. [**Lesson 01 Iterations**](https://app.codility.com/programmers/lessons/1-iterations/)

   1. BinaryGap

      https://app.codility.com/demo/results/trainingUKVSGG-JBD/ (60/100)

      https://app.codility.com/demo/results/trainingGNS8YW-NXK/ (100/100)

2. [**Lesson 02 Arrays**](https://app.codility.com/programmers/lessons/2-arrays/)

   1. CyclicRotation 

      https://app.codility.com/demo/results/trainingX7S2BW-Z5D/ (100/100)

      https://app.codility.com/demo/results/trainingNGPK2Z-QWP/?showingAll=1 (100/100, JAVA)

      - 기존의 배열을 인자로 전달된 횟수만큼 돌리는 것
      - 새로운 임시배열을 만들어서 인덱스를 수학적으로 구한후, 횟수만큼 돌려진 배열을 반환함

   2. OddOccurrencesInArray

      https://app.codility.com/demo/results/trainingRRVPPN-CKV/ (66/100)

      https://app.codility.com/demo/results/trainingXEP7GG-QJ6/ (100/100)

      https://app.codility.com/demo/results/trainingPYN8QV-3VS/?showingAll=1 (100/100, JAVA)

      - 배열중에서 Pair 된 녀석들을 제외한 홀로 남은 숫자를 찾는 것
      - Java 에서 HashSet 을 이용해서 풀음

3. [**Lesson 03 Time Complexity**](https://app.codility.com/programmers/lessons/3-time_complexity/) 

   1. FrogJmp

      https://app.codility.com/demo/results/training6M9K8G-E93/ (33/100)

      https://app.codility.com/demo/results/trainingC8DQU5-3XN/ (100/100)

      https://app.codility.com/demo/results/trainingSP4CVF-3SP/?showingAll=1 (100/100, JAVA)

      - 개구리가 점프할 수 있는 횟수를 구하는건데, 나눗셈과 나머지연산을 통해 간단하게 구현함

   2. PermMissingElem

      https://app.codility.com/demo/results/trainingZX2TG6-XTK/ (10/100)

      https://app.codility.com/demo/results/trainingM7YHQ2-FZS/ (100/100)

      https://app.codility.com/demo/results/training9WYS29-48S/?showingAll=1 (100/100, JAVA)

      - 2,5,1,3 이란 배열이 주어지면 중간에 빠진 값을 찾는건데
      - boolean 배열을 만들어서 각각 기록해놓고
      - 나중에 배열을 순회하면서 false가 뜨면 바로 리턴

   3. TapeEquilibrium

      https://app.codility.com/demo/results/trainingMZG8KV-THY/ (83/100)

      https://app.codility.com/demo/results/training7FAHTH-VGW/ (100/100)

      https://app.codility.com/demo/results/trainingG2BCAB-UNZ/ (100/100) 코드 최적화

      https://app.codility.com/demo/results/trainingBG9456-ZBM/?showingAll=1 (100/100, JAVA)

      - 각 배열의 사이 인덱스에서 각 차분을 구해서 가장 최솟값을 구하는 경우이다
      - Integer.MAX_VALUE 는 꽤 신박했음
      - foreach 문을 쓰면 배열을 다 탐색하기 때문에 이상한 값이 출력될 수 있다는 것을 항상 인지
      - 일단은 for 문으로?

4. [**Counting Elements**](https://app.codility.com/programmers/lessons/4-counting_elements/)

   1. PermCheck

      https://app.codility.com/demo/results/trainingXMQDSU-A5K/ (75/100)

      https://app.codility.com/demo/results/trainingZPHEFQ-KUH/ (100/100)

      https://app.codility.com/demo/results/trainingMZDVRM-C8U/?showingAll=1 (100/100, JAVA)

      - 이것 역시 boolean 을 통해서 체크할 배열을 만들어놓고 체크를 해주면 되는데
      - 약간의 조건식이 필요했다. 이 조건식이 없어서 처음에50%가 나왔는데 중간에 걸러주는 조건식들을
      - 생각하는 훈련이 필요할 듯 하다

   2. FrogRiverOne

      https://app.codility.com/demo/results/trainingDKDR66-AK3/ (18/100)

      https://app.codility.com/demo/results/training9D35XM-QQS/ (27/100)

      https://app.codility.com/demo/results/training2N78YZ-55A/ (54/100)

      https://app.codility.com/demo/results/trainingVE2UW9-XXG/ (100/100)

      https://app.codility.com/demo/results/trainingEHAKFF-F56/?showingAll=1 (100/100, JAVA)

      - 문제를 이해하기 좀 힘들었다
      - 자료구조 HashSet 을 이용해서 조건을 검사해서 간단하게 해결

   3. MissingInteger

      https://app.codility.com/demo/results/training55RTHV-YRJ/ (100/100)

      https://app.codility.com/demo/results/trainingDAWN6Q-SUD/?showingAll=1 (100/100, JAVA)

      - 인자로 들어온 배열의 길이를 가지고 새로운 배열을 생성할 때
      - 안의 인자의 값이 꼭 배열의 길이보다 낮을거란 생각은 ㄴㄴ
      - 항상 예외로 해줘야 하는지 체크하는 생각을 들이자 :)

   4. **MaxCounters**

      https://app.codility.com/demo/results/trainingQHD8ZZ-YSE/ (77/100)

      https://app.codility.com/demo/results/trainingTKYUJ2-TDG/ (100/100)

      https://app.codility.com/demo/results/trainingDZS4Z8-J7U/?showingAll=1 (100/100, JAVA)

      - 배열을 1부터 끝까지 값을 채우거나 순회하는 부분은 시간복잡도에서 걸릴 가능성이 매우 크므로
      - 따로 뺄 수 있는 부분을 변수를 통해서 저장해놓고, 나중에 그 값들만 처리할 것
      - 중간에 continue Point 만 있어도 시간복잡도가 많이 개선된다.

5. **[Prefix Sums](https://app.codility.com/programmers/lessons/5-prefix_sums/)**

   1. PassingCars

      https://app.codility.com/demo/results/training9QTZQU-JNB/ (10/100)

      https://app.codility.com/demo/results/trainingSJSTAZ-A5X/ (70/100)

      https://app.codility.com/demo/results/trainingNWTEU9-4V8/ (100/100)

      https://app.codility.com/demo/results/training4MP7HQ-HRK/?showingAll=1 (100/100, JAVA)

      - 수학적인 계산..이 빛을 발한 구간
      - 0과 1이 따로따로 더해진다면, 0의 카운트를 늘려서 1이나올때마다 0의 나온카운트를 더하는 식으로도 해결할 수 있다

   2. CountDiv

      https://app.codility.com/demo/results/trainingK7AEC2-7MY/ (50/100)

      https://app.codility.com/demo/results/trainingYCH38D-RXC/ (75/100)

      https://app.codility.com/demo/results/trainingPEYHB6-C2G/ (100/100)

      https://app.codility.com/demo/results/trainingD5JVFC-726/?showingAll=1 (100/100, JAVA)

      - 이것 역시 수학적인 계산
      - 일반적으로 생각하는 방식으로 풀었다간 시간초과 오짐 (mod 이용)
      - 시간 복잡도를 해결하려면 나머지 연산을 나눗셈으로 바꿀 수 있는 방법을 찾아야 함

   3. GenomicRangeQuery

      https://app.codility.com/demo/results/training8W6WQP-2HC/?showingAll=1 (100/100, JAVA)

      - 하.. 푸는방법은 다양하겠지만, 정말 뭣같은 문제였다
      - 맨처음에 O(N*M) 이 나오는데 시간복잡도에서 다꽝
      - 결론은 O(N+M) 구조를 만들어야함
      - 그러면 무조건, 공간복잡도에서 손해를 보던지 해서 산수로 결과를 내버려야됨
      - 그래서 String 길이만큼의 배열을 만들고 Log 형식으로 숫자를 하나씩 더한다음에
      - 범위 (A~B) 가 있으면 B-A 형식으로 빼서 최솟값을 구함
      - 이런말은 좀 그렇지만 미친놈인줄 알았음

   4. MinAvgTwoSlice

      https://app.codility.com/demo/results/trainingU6662C-BGW/?showingAll=1 (100/100, JAVA)

      - 평균은 최소 2가지의 숫자와 3가지의 숫자 이외에는 확률적으로 해당 평균보다 적게나오기가 힘듬
      - 그래서 맨 처음에 2가지의 숫자의 평균을 각각 구해서 최소 평균과 최소 인덱스값을 저장해놓고
      - 다음으로 3가의 숫자 평균을 구한다음에 위에서 구했던 최소 평균과 최소 인덱스를 또 비교
      - 단, 평균값이기 때문에 항상 Double 로 진행해야 하는것은 Point!

6. **[Sort](https://app.codility.com/programmers/lessons/6-sorting/)**

   1. Distinct

      https://app.codility.com/demo/results/trainingUANE87-8XR/?showingAll=1

      - 정렬문제라고 해서 정렬기법을 써야하나 싶었는데, 그냥 Set에 담아두고 Set.size 해주면 끝이였다.

   2. MaxProductOfThree

      https://app.codility.com/demo/results/training4YYGQ9-KWG/?showingAll=1 (44/100, JAVA)

      https://app.codility.com/demo/results/trainingMU856E-XA5/?showingAll=1 (100/100, JAVA)

      - 배열 중 임의의 3개의 숫자를 곱했을 때 가장 큰 결과값을 리턴하는 문제

      - 음수도 포함되어 있기 때문에, 정렬 후 배열 오른쪽 맨 끝 3개의 곱과

      - 배열 왼쪽 맨 끝 2개의 곱 * 배열 오른쪽 끝 1개를 곱해주는 것 중

      - 비교해서 가장 큰 값을 리턴하면 된다.

   3. Triangle

      https://app.codility.com/demo/results/trainingG5GSZ7-27A/?showingAll=1 (93/100, JAVA)

      https://app.codility.com/demo/results/trainingQ7A3VQ-XXB/?showingAll=1 (93/100, JAVA)

      https://app.codility.com/demo/results/training32EUEM-BZC/?showingAll=1 (100/100, JAVA)

      - Int 범위를 항상 생각할 것
      - OverFlow 체크를 해야한다. 최댓값과 최댓값이 더해지면 OverFlow 되서 2가 출력되기 때문이다

   4. **NumberOfDiscIntersections**

      https://app.codility.com/demo/results/trainingP2ASWV-SFZ/?showingAll=1 (75/100, JAVA)

      https://app.codility.com/demo/results/trainingQF2355-865/?showingAll=1 (100/100, JAVA)

      - 이건 아직도 모르겠다
      - 다른 방식을 찾아야 할듯?
      - 일단 내가 참고한 [Stack OverFlow](https://stackoverflow.com/questions/4801242/algorithm-to-calculate-number-of-intersecting-discs#)

7. [**Stacks and Queues**](https://app.codility.com/programmers/lessons/7-stacks_and_queues/nesting/)

   1. Nesting

      https://app.codility.com/demo/results/trainingEK39ZR-S8H/?showingAll=1 (25/100, JAVA)

      https://app.codility.com/demo/results/trainingXCRA3V-PSA/?showingAll=1 (100/100, JAVA)

      - 스택으로 하는것은 맞으나, 여기서 하나 느낀 부분이 있다.
      - 일단 split 함수는 시간복잡도가 굉장히 오래걸린다
      - String 을 배열로 만드는것은 toCharArray 메서드를 사용해서 char 배열로 담는게 낫다.
      - 아니면 toCharArray 와 forEach 문을 이용해서 바로 뽑아내도 되고
      - 그리고 맨 마지막에 stack에 남아있는 것도 판별해주어야 한다.

   2. Fish

      https://app.codility.com/demo/results/trainingT2BUYU-W98/?showingAll=1 (0/100, JAVA)

      https://app.codility.com/demo/results/trainingCNHX79-PMV/?showingAll=1 (100/100, JAVA)

      - 한쪽의 케이스를 Stack에 담고 비교
      - 문제의 조건을 잘 이해하고 그 때에 맞춰서 조건을 감소시키거나 증가시켜줄 것
        - 물고기가 일단 하류로 간다고 해서(Stack에 넣으면 일단 물고기가 증가된 것임)

   3. Brackets

      https://app.codility.com/demo/results/trainingUZD2GE-5QB/?showingAll=1 (62/100, JAVA)

      https://app.codility.com/demo/results/trainingDG93SA-MQ7/?showingAll=1 (100/100, JAVA)

      - 해당 문제도 Stack을 이용하면 간단하게 풀리는 문제
      - 조건들을 검사한 후 항상 마지막에 Stack에 데이터가 남아있는지 판별할 것

   2. StoneWall

      https://app.codility.com/demo/results/trainingXJQGM5-NS7/?showingAll=1 (100/100, JAVA)

      - 해당 문제는 벽돌을 세울 때 최소한의 벽돌 갯수를 구하는 것인데
      - 처음에 문제를 이해하기 너무 힘들었다
      - 이런 문제해결방식도 처음보고
      - 자료구조는 Stack 을 해결은 크기비교를 이용해서 답을 산출한다.
      - 이런 방식은 비슷한 문제가 나왔을 때 외워둬야할 듯

8. **Leader**

   1. **EquiLeader**

      https://app.codility.com/demo/results/trainingYCZ4HS-J2J/?showingAll=1 (100/100, JAVA)

      - 해당 문제는 가장 많이 나온 Leader 의 숫자를 가지고 비교하는 방법인데..
      - 도저히 모르겠다. 한국인 해설이 없어서 내가 알아보기 쉬운 코드를 가지고 디버깅 돌리면서 이해해보려고 해도 안된다
      - 수학적인 지식이 부족한것일까
      - counterOfrLeaderInLeft > (i/2) && counterOfrLeaderInRight > (A.length-i) / 2 이 조건이 어떻게 나오는것인지 모르겠다

   2. Dominator

      https://app.codility.com/demo/results/training2654VA-W97/?showingAll=1 (66/100, JAVA)

      https://app.codility.com/demo/results/training73CYRM-HZY/?showingAll=1 (75/100, JAVA)

      https://app.codility.com/demo/results/training5BZSQ2-P8D/?showingAll=1 (100/100, JAVA)

      - 가장 많이 나오는 숫자를 찾는 것
      - 근데 이것이 배열의 길이를 2로 나눈것보다 작거나 같으면 Dominator 이 될 수 없음
      - 이 부분만 고려해서 코드를 작성하면 됨
      - hashMap 을 통해서 구현하였음

9. **Maximum slice problem**

   1. MaxSliceSum

      https://app.codility.com/demo/results/trainingMY3MRM-BBM/?showingAll=1 (7/100, JAVA)

      https://app.codility.com/demo/results/trainingNG2MBP-9GB/?showingAll=1 (23/100, JAVA)

      https://app.codility.com/demo/results/trainingJTXNCZ-E7H/?showingAll=1 (30/100, JAVA)

      https://app.codility.com/demo/results/training3N4YWW-CTS/?showingAll=1 (53/100, JAVA)

      https://app.codility.com/demo/results/trainingPBATHS-SSE/?showingAll=1 (61/100, JAVA)

      https://app.codility.com/demo/results/trainingWQ2425-DZA/?showingAll=1 (100/100, JAVA)

      - 처음에 간단하게 풀 수 있을줄 알았던 문제
      - Pair 끼리만 비교하면 되는것인줄 알았는데, 전부 비교해야함
      - 그래서 경우의수가 굉장히 복잡해지는 줄 암
      - 하지만 2개의 변수를 잘 이용하면 간단하게 풀리는 문제
      - 0부터 배열의 끝까지 계속 누적한 값과, 현재의 배열값을 비교
      - 다른 변수에는 반복문이 돌고나서 계산결과가 끝났을 때 가장 큰 값을 기록한다
      - 마지막으로 큰 값을 리턴

   2. MaxProfit

      https://app.codility.com/demo/results/trainingWED977-PXG/?showingAll=1 (88/100, JAVA)

      https://app.codility.com/demo/results/trainingU7CPYD-DD4/?showingAll=1 (100/100, JAVA)

      - 변수를 2개 활용
      - 최소한의 값을 기억하고 있는 `nMin` 변수를 사용
      - 그리고 인덱스가 높은 배열에서 `nMin` 변수를 빼면서 가장 큰 차액 데이터를 보관함
      - 배열을 다 돌면 리턴
      - 간단하죠?

   3. **MaxDoubleSliceSum**

      https://app.codility.com/demo/results/trainingW7BRFA-W9W/?showingAll=1 (100/100, JAVA)

      - 3개의 슬라이스 포인트를 잡고, 해당 인덱스의 값은 뺀 후 사이값만 더해서 최댓값을 알아내는 것인데
      - 왼쪽부터 시작하고 하나씩 더해서 최댓값의 배열을 만들고 `maxLeft`
      - 오른쪽부터 시작하고 하나씩 더해서 최댓값의 배열을 만든다 `maxRight`
      - 서로 다른 값들을 가진 배열이 나온다. 단 0보다 큰 데이터가 들어갈 수 있도록 `Math.max` 로 판별한다.
      - 그리고 왼쪽과 오른쪽에 대한 인덱스 차이가 2씩 나므로 X,Y,Z 가 예를들어 1,2,3 이면 1과3은 2차이
      - Y 를 포인트로 잡고 maxLeft 는 -1 maxRight 는 +1 해서 최댓값을 구한다.

10. **Prime and composite numbers**

    1. **CountFactors**

       https://app.codility.com/demo/results/trainingHM7YNM-AJ3/?showingAll=1 (14/100, JAVA)

       https://app.codility.com/demo/results/training8H6PRJ-ZV2/?showingAll=1 (100/100, JAVA)

       - 약수 구하기다.
       - ~~이건 문제이해가 안되서~~ 다른 사람 코드를 참고했다.	
       - Math.sqrt 메서드도 알 수 있게되었고
       - 약수를 일반적인 O(N)의 방식대로 풀면 시간초과가 나므로
       - O(sqrt(N))정도로 줄여야한다

    2. MinPerimeterRectangle

       https://app.codility.com/demo/results/trainingX9HGQ6-J9Q/?showingAll=1 (100/100, JAVA)

       - 1번 문제를 풀었다면 쉽게 풀 수 있는 문제
       - sqrt 가 굉장히 유용하다
       - 쉬운 문제였다
       - 시간복잡도 `O(sqrt(N))`

    3. Flags

11. Sieve of Eratosthenes

12. Euclidean algorithm

    1. ChocolatesByNumbers

       https://app.codility.com/demo/results/trainingW94HVG-JDR/?showingAll=1 (25/100, JAVA)

       https://app.codility.com/demo/results/trainingH6ABRA-BNU/?showingAll=1 (66/100, JAVA)

       https://app.codility.com/demo/results/trainingNUXS8F-U8Q/?showingAll=1 (100/100, JAVA)

       - 유클리드 알고리즘을 사용하였다 (최대공약수를 구하는 알고리즘)
       - 뭐 뒤에 나누는것은 처음 알았지만
       - while 문 안에서 나머지 연산을 구한 후, swap
         - while 문 탈출 조건은 N % M == 0 일 경우

13. Fibonacci numbers

14. Binary search algorithm

15. Caterpillar method

    1. AbsDistinct

       https://app.codility.com/demo/results/trainingZ5WHXB-QYD/?showingAll=1 (100/100, JAVA)

16. Greedy algorithms

17. Dynamic programming

























