---
layout: post
category: writings
---

# Future Research Direction of APR

## Abstract

프로그램 자동 수정 문제는 전통적으로 수정 재료 탐색, 수정 동작 추출, 적용의 3가지 문제로 나뉜다. 이러한 고전 모델은 한계점에 도달한 것으로 보인다. 프로그램 수정 기술에는 다양한 개선 가능성이 있고 여러 최신 연구들이 다양한 방식으로 접근하고 있다.

The problem of automatic program repair is traditionally divided into three main problems: searching for repair ingredients, extracting repair actions, and applying them. However, these classic models appear to have reached their limits. There are various possibilities for improvement in program repair techniques, and recent research is approaching the problem from different angles.


The problem of automatic program repair is traditionally divided into three main problems: search for repair ingredients, extraction of repair actions, and application. Generally, automatic program repair aims to make previously failing test cases pass by applying these three methods to the program location obtained using fault localization techniques. The search for repair ingredients is the problem of identifying which modifications should be made to a given fault. It has been researched through search-based repair techniques that adopt approaches to reduce the search space and semantic repair techniques that transform the search problem into a satisfiability problem, producing semantically equivalent repairs. The extraction of repair actions typically involves computing the changes between two abstract syntax trees, and the application involves replacing the namespaces of the searched repair ingredients from the previous stage with the namespaces of the program that needs repair, followed by estimating the exact location of the repair.

However, the classic models for automatic program repair seem to have reached their limits. According to a paper submitted by Yang et al. at last year's Automated Software Engineering conference (ASE), which focused on experiments with automatic program repair techniques using the Defect4J benchmark, the number of bugs that the latest techniques were able to fix increased by 8% annually from 2016 to 2019. However, since 2020, the increase has stagnated, with an average annual growth rate of only 1%.

A common characteristic of bugs that existing approaches fail to fix is their high complexity in terms of repair ingredients. Repair ingredients with numerous lines of code, various types of variables, and multiple repair actions pose challenges to all three classic problem areas. As the complexity of bug fixes increases, the search for repair ingredients becomes more difficult, defining repair actions incurs exponentially higher costs, and applying repairs becomes much more challenging when dealing with a variety of custom types.

In addition, there are various possibilities for improvement in program repair techniques, and recent research has approached the problem from different angles. The automatic patch transplantation problem introduced by Shariffdeen et al. in 2020 simplifies the existing problem. Patch transplantation involves preparing repair ingredients from donor programs in advance and applying the patches only to programs with the same bug, eliminating the need for fault localization techniques used in traditional program repair. However, this approach still relies on test cases. In contrast, our approach does not require test cases, but it incurs the same complexity burden when dealing with intricate repairs. Therefore, it is believed that future directions in program repair techniques should focus on finding solutions for handling more complex repairs.

프로그램 자동 수정 문제는 전통적으로 수정 재료 탐색, 수정 동작 추출, 적용의 3가지 문제로 나뉜다. 일반적인 자동 프로그램 수정은 결함 위치 추정 기술을 사용하여 얻어낸 프로그램상의 위치에 위 3가지 방법을 적용하여 적용 전에 실패했던 테스트 케이스를 성공하게 하는 것을 목적으로 한다. 먼저 수정 재료 탐색 문제는 어떤 결함에 어떤 수정을 해야 하는지 탐색하는 문제로 탐색 공간을 줄이는 방식을 채택한 탐색 기반 수정 기술과 탐색 문제를 충족 가능성 문제로 바꾸어 의미적으로 동일한 수정을 만드는 의미 수정 기술로 분기되어 연구되었다. 수정 동작 추출은 일반적으로 두 개의 추상 구문 트리의 변화를 계산하여 이루어지며 적용은 이전 단계에서 탐색 된 수정 재료의 이름공간을 수정이 필요한 프로그램의 이름공간으로 교환한 뒤 정확한 수정의 위치를 추정하여 이루어진다.  

이러한 프로그램 자동 수정 문제의 고전 모델은 한계점에 도달한 것으로 보인다. Yang et al.의 지난해 자동 소프트웨어 공학 학회(ASE)에 투고된 논문에 따르면 프로그램 자동 수정 기술 실험에 주로 사용하는 Defect4J 밴치마크에서 당시 최신 기술들이 고칠 수 있었던 결함의 양이 2016년부터 2019년도까지는 매년 8\% 증가했던것에 반해 2020년 이후로는 매년 평균 1\% 증가하여 성능 증가의 폭이 고착되었다는 것을 알 수 있다.

기존의 방식들이 고치지 못한 결함들의 공통점은 수정 재료의 복잡도가 높다는 것이다. 많은 라인과 다양한 타입의 변수 및 수정 동작을 가진 수정 재료는 3가지의 고전 문제에 모두 도전이 될 수밖에 없다. 결함 수정이 복잡할수록 수정 재료 탐색이 힘들고, 수정 동작을 정의하는데 기하급수적으로 비용이 증가하며 사용자 정의된 타입이 다양하다면 적용이 매우 힘들게 된다.

이 외에도 프로그램 수정 기술에는 다양한 개선 가능성이 있고 여러 최신 연구가 다양한 방식으로 접근하고 있다. 2020년에 Shariffdeen et al. 의해 소개된 자동 패치 이식 문제는 기존의 문제를 단순화하였다. 패치 이식 문제는 수정 재료를 기증자 프로그램으로부터 미리 준비하고 동일한 결함을 가진 프로그램에만 패치를 진행함으로써 기존의 프로그램 수정 기술에서 사용했던 결함 위치 추정 기술이 필요하지 않게 된다. 하지만 해당 연구는 여전히 테스트케이스에 의존적이다. 이에 반해, 우리의 방식은 테스트케이스가 필요하지 않다는 이점이 있지만, 복잡한 수정에 대한 부담이 동일하게 지어진다. 따라서 프로그램 수정 기술의 향후 방향으로 더욱 복잡한 수정을 고치는 것에 대한 해결책이 필요할 것으로 생각된다.

## Reference

[Shariffdeen, Ridwan Salihin, et al. "Automated patch transplantation." ACM Transactions on Software Engineering and Methodology (TOSEM) 30.1 (2020): 1-36.]({{site.url}}/assets/docs/transplantation.pdf)
[Tai, Kuo-Chung. "The tree-to-tree correction problem." Journal of the ACM (JACM) 26.3 (1979): 422-433.]({{site.url}}/assets/docs/tree_to_tree.pdf)
[Yang, Deheng, et al. "TransplantFix: Graph Differencing-based Code Transplantation for Automated Program Repair." 37th IEEE/ACM International Conference on Automated Software Engineering. 2022.]({{site.url}}/assets/docs/TransplantationFix.pdf)