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

   4. MaxCounters

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

   4. NumberOfDiscIntersections

      https://app.codility.com/demo/results/trainingP2ASWV-SFZ/?showingAll=1 (75/100, JAVA)

      https://app.codility.com/demo/results/trainingQF2355-865/?showingAll=1 (100/100, JAVA)

      - 이건 아직도 모르겠다
      - 다른 방식을 찾아야 할듯?
      - 일단 내가 참고한 [Stack OverFlow](https://stackoverflow.com/questions/4801242/algorithm-to-calculate-number-of-intersecting-discs#)


1