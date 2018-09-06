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

