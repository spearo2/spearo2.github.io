---
layout: post
category: writings
---

[paper]({{site.url}}/assets/docs/automatic_verfication.pdf)

## Automatic Software Verification

In 2008, D. Silva et al. published a comprehensive research paper that extensively investigated three software verification techniques. The authors selected and examined three verification techniques: program static analysis, model checking, and bounded model checking, based on their scalability and automation in ensuring the quality of software and handling its complexity. This article provides a brief summary of the concepts learned from reading the following paper.

Program summarization static analysis is a technique that effectively analyzes the structure of a program by summarizing it using predefined information. In the big picture, static analysis analyzes programs effectively by trading accuracy for efficiency. The summarization process occurs during the integration summary of states. Therefore, the summarization process in static analysis implies the possibility of information loss depending on the domain in which the summarization was performed and its insensitivity to execution flow and paths. On the other hand, static analysis is widely used in various fields as the technique guarantees soundness and automation.

Model checking is a method that represents a program as a graph composed of states and transitions and verifies if the graph satisfies correctness specifications. Here, correctness refers to a pre-defined logical formula, and each state represents program counters, variable values, heap, and stack values depending on the type. In other words, model checking proves that a program does not access incorrect states by checking if it satisfies the correctness specifications. The distinctive feature of model checking is its ability to provide counterexamples for program correctness by manually constructing a finite state model and applying it to the program, which enables more precise analysis that is insensitive to execution flow and paths. Although model checking does not have false positives, its performance greatly depends on the refinement strategy, and there is a possibility that the summarized refinement cycle may not terminate. Ultimately, model checking lacks determinism. Therefore, there is a proposition summarization method that applies the summarization approach of static analysis, but it also has limitations in scalability since it relies on parameter-based summarization. Model checking, leveraging its precision, continues to be used in device drivers and other applications.

While reading this paper, I gained a more intuitive understanding of the overall picture in the verification field. I learned not only the concepts I already knew but also the background and initial purposes behind the development of these techniques, which sparked my interest. However, considering that the paper is over 10 years old and contains outdated information, I plan to engage in more diverse studies to further expand my knowledge.

2008년 D.Silva et al.은 소프트웨어 검증 기법 세 가지 기술에 대해 폭 넓게 조사한 논문을 투고하였다. 저자는 검증 방식이 소프트웨어의 품질을 보장할 수 있는지와 소프트웨어의 복잡도에 대해서 확장성과 자동성이 존재하는지에 따라 프로그램 정적분석, 모델 검증, 바운디드 제한 모델 검증 세가지의 검증 기법을 선정하고 기술에 대한 개요를 조사하였다. 본 글은 다음의 논문을 읽고 배운 개념을 간단히 정리한다.

프로그램 요약 정적 분석은 사전의 정의된 정보를 이용해 효과적으로 프로그램의 구조를 요약하여 분석하는 기법이다. 큰 그림에서 정적분석은 정확도와 효율을 교환함으로서 효과적으로 프로그램을 분석한다. 요약 과정은 상태를 통합 요약하는 과정에서 일어난다. 따라서 정적 분석의 요약 과정은 어떠한 도메인에서 요약을 진행했는지와 실행 흐름와 경로에 둔감한지에 따라 정보 손실이 일어날 수 있음을 뜻한다. 반면에 정적 분석은 확정성과 자동성이 보장되기 때문에 기술이 발전하면서 여러분야에 더욱 널리 쓰이고 있다.

모델 검증은 프로그램을 상태와 이행으로 이루어진 그래프로 표현하고 해당 그래프가 정확성 명세를 만족하는지 검증하는 방법이다. 이때 정확성이란 미리 정의한 논리식을 뜻하며 각 상태는 종류에 따라 프로그램 카운터, 변숫값, 힙과 스택의 값 등을 뜻한다. 즉 모델 체킹은 프로그램이 정확성 명세를 만족하는지 검사함으로서 옳바르지 않은 상태에 접근하지 않는다는 것을 증명한다. 모델 검증의 차별점은 프로그램 정확성에 대한 반례를 제공할 수 있다는 것으로 수동으로 유한 상태 모델을 만들어 프로그램에 적용함으로서 반례가 되는 트레이스를 뽑아 내어 실행 흐름와 경로에 민감하지 않은 보다 정밀한 분석이 가능하다. 모델검증은 가양성이 없지만 정제 전략에 따라 크게 성능이 좌우되며 요약된 정제 사이클이 종료되지 않을 가능성이 존재한다. 결정적으로 모델 검증은 확정성이 떨어진다. 때문에 요약 정적 분석의 요약 방식을 적용한 명제 요약 방식이 있지만 해당 방식 또한 매개변수를 활용한 요약이므로 확장성에 제약이 있다. 모델 검증은 정밀성에 강점을 살려 디바이스 드라이버 등에서 지속해서 사용되고 있다.

해당 논문을 읽으며 검증 분야의 큰 그림을 좀 더 직관적으로 배우게 되었다. 이미 배운 내용도 있지만 기술이 만들어진 배경이나 초기 사용 목적등 이론적인 것 이외의것들을 배워 흥미를 얻을 수 있었다. 다만 논문이 10년이상 되었고 오래된 내용을 담고 있을 것을 감안하여 감안하여 더욱 다양한 공부를 할 예정이다.

