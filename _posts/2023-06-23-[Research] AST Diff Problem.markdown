---
layout: post
category: research
---

# 추상 구문 트리 수정 문제
## AST Diff Problem

The problem of editing a general ordered tree is a deterministic problem in <br>polynomial time, which is formulated as the minimum edit operation cost <br>problem between two arbitrary trees. The problem was proven to be solvable <br>by Tai in 1979, with a complexity of O(V * V'L * L'). However, such <br>algorithms cannot always be deterministic in abstract syntax trees that <br>use syntactic features instead of labels because the algorithm deviced by <br>Tai assumes that as both trees use a common ordered label.

<br>The edit operation problem in abstract syntax trees is a non-deterministic problem in polynomial time. <br> In 1996, Chawathe et al. presented an <br>algorithm that transformed the edit operation problem in information <br>structure trees into isomorphism problems, and several abstract syntax <br>tree edit operation algorithms based on this approach were proposed since <br>then. However, the edit operation problem in abstract syntax trees holds <br>significance in analyzing differences in concrete-level source code <br>structures. Therefore, it has been proven that certain substitutions can <br>be made between graphs as isomorphism problems at a higher level, where <br>information is lost through abstraction, and node labels in trees at a <br>concrete level arise from differences in strings allowed by the grammar. <br>These problems have been proven to be NP-hard.

Nevertheless, researchers have continued their efforts to achieve higher accuracy in abstract syntax tree edit operation algorithms.<br> In 2007, Fluri et al. proposed an algorithm that applied various heuristics to extract four types of transformations: insertion, deletion, update, and move of abstract syntax tree nodes. <br>This algorithm improved the accuracy compared to previous methods by approximately twofold. Then, in 2014, Martin Monperrus and his research team proposed the Gumtree algorithm that distinguishes<br> between nodes and subtrees in abstract syntax trees and calculates the four transformations with an average accuracy approximately 20% higher than that of Fluri et al.'s method.<br>  Gumtree have demonstrated excellent performance and are widely used in source code analysis research to this day.

Despite the advancements in the proposed methods from recent research, there are several limitations. <br>These include the convergence of time complexity to the cube of the number of nodes, even with imperfect accuracy, and the possibility of accuracy variations based on various syntactic features<br> provided by different programming language domains.

By understanding these theoretical issues, it becomes possible to gain a precise understanding of the patch extraction problem,<br> which is a subset of the abstract syntax tree edit operation problem and a part of my current research.
<br>
일반적인 순서 트리의 수정 문제는 임의의 트리 두 개간의 최소 수정 비용 문제로 다항 시간에 결정론적인 <br>문제이다. 해당 문제는 1979년에 Tai에 의해 O(V * V’ * L * L’) 에 풀 수 있는 문제로 증명된 <br>바 있다. 하지만 이러한 알고리즘은 두 트리에 공통으로 사용되는 순서 라벨이 사용된다는 가정이 <br>존재하기 떄문에 라벨 대신에 구문적 특징을 사용하는 추상 구문 트리에서 항상 결정론적일 수 없다.
<br>추상 구문 트리의 수정문제는 다항시간에 비결정론적인 문제이다. 1996년에 Chawathe et al.에 <br>의해 정보 구조 트리에서의 수정 문제를 서로 동형 문제로 치 환하여 풀 수 있는 알고리즘이 <br>제시되었고, 이를 이용한 여러 추상 구문 트리 수정 알고리즘이 제시되었다. 하지만 추상 구문 트리 <br>수정 문제는 더 높은 단계에서 구 체적 소스 코드의 차이를 분석하는 데에 의의가 있다. 따라서 <br>추상화를 거치면서 정보를 잃어버리는 점, 그리고 구체적 단계에서는 트리의 노드 라벨이 문법이 허락 <br>하는 내에서 문자열의 차이로 발생한다는 점에서 그래프의 서로 동형 문제로 일부 치환이 가능하며 다항 <br>시간 비결정론적 문제(NP-hard)로 증명된 바 있다.
<br>그럼에도 불구하고 추상 구문 트리의 수정 알고리즘의 더 높은 정확도를 위한 연구자들의 노력은 <br>계속되었다. 2007년 Fluri et al.은 여러 방법론을 적용하여 추상 구문 트리 노드의 삽입, 삭제, <br>수정, 이동 네 가지의 변화를 추출하는 알고리즘을 제안하였다. 해당 알고리즘은 기존의 방식의 <br>정확도를 2배 정도 향상했다. 이후 2014년에 마틴 몬페러스 교수의 연구실에서 추상 구문 트리의 <br>노드와 서브트리를 구분하여 네 가지 변화를 Fluri et al.의 방식보다 평균적으로 20% 정도 높은 <br>정 확도로 계산하는 일명 검트리 알고리즘을 제안하였다. 검트리는 훌륭한 성능으로 현재까지도 소스 <br>코드 분석 연구에 많이 사용되고 있다.
<br>이러한 최신 연구에서 제안된 방식에도 여러 가지 제한점이 존재한다. 완벽하 지 않은 정확도에도 <br>불구하고 시간 복잡도가 노드 개수의 세제곱에 수렴한다는 점, 프로그래밍 언어의 여러 구문적 특징에 <br>따라 정확도가 달라질 수 있다는 점 등이 이에 해당한다.
<br>이러한 이론적인 문제를 파악함으로써 현재 연구의 일부인 추상 구문 트리 수정 문제의 부분 집합인 <br>패치 추출 문제를 정확히 이해할 수 있을것이다.
