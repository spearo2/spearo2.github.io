---
layout: post
category: writings
---

# 동적 심볼릭 테스팅 개요
## On the Concolic Testing


동적 심볼릭 테스팅은 자동으로 결함을 일으키는 입력을 찾아내는 테스팅 기술 중에 하나이다. 결함이 자동으로 탐지되고 대응 가능한 입력값 생성이 가능하다면 소프트웨어 개발 및 유지 보수 단계에서의 비용이 크게 절약될 것이다.<br>
 동적 심볼릭 테스팅은 프로그램 실행 경로에서 프로그램 변수를 기호 변수로 취급하는 기호 실행과 SMT 기법을 결합하여 새로운 입력값을 생성하고 코드 커버리지를 최대화하는 기술이다. 이러한 방식은 타 테스팅 기법과 마찬가지로<br>
  완전하지만 안전하지 못하다. 따라서 프로그램의 정확성보다 실제 소프트웨어에서 결함을 찾는 것을 주요 목표로 두고 있고 실제로 기술의 뛰어남을 인정받아 산업 현장에서 활발히 사용되고 있는 기술중에 하나이다.

동적 심볼릭 테스팅에는 퍼징 기법과의 차별적인 장점이 존재한다. 동적 심볼릭 테스팅은 유사한 특징 덕분에 종종 퍼징 기법의 비교 대상이 되곤 한다. 동적 심볼릭 테스팅은 퍼징 기법이 Barton Miller 교수에 의해 1990년 처음<br>
 학계에 출현하고 약 15년 뒤인 2006에 Sen et al.에 의해 제안된 만큼 많은 면에서 더 뛰어난 성능을 보인다. 동적 심볼릭 테스팅은 퍼징 기법과 같은 무작위 테스팅과는 달리 입력 변수에 대한 조건을 고려하여 실행 경로를 탐색하므로<br>
  더 효과적으로 높은 코드 커버리지를 달성 할 수 있고 따라서 퍼징 기법이 발견하기 힘든 결함을 발견할 수 있다.

하지만 동적 심볼릭 테스팅에는 몇 가지 한계 또한 존재한다. 비결정적 동작이나 무한한 실행 경로와 같이 처리하기 어려운 경우가 있으며, 특히 암호학적인 부분과 같이 변수 상태를 다양하게 조합하는 경우에는 효율적인 테스팅이 어려울 수 있다.<br>
 또한, 입력 영역에 한정적일 수 있기 때문에 실제로 모든 종류의 소프트웨어에 적용하기에 어려움이 존재할 수 있다. 이 중 가장 도드라지는 문제는 실행 비용과 탐색 공간이다. 

동적 심볼릭 테스팅에는 여전히 개선의 여지가 많이 남아있다. 20년 된 기술임에도 불구하고 탐색 공간을 최적화하기 위한 수 많은 방법론들이 제시됐다. 대부분의 퍼징 기술과 달리 테스팅 시점에서 소스코드가 모두 공개된 상태에서 진행되기 때문에<br>
 소스코드의 분석을 통한 최적화의 여지가 남아 있는 것이다. 


Concolic Testing(Dynamic Symbolic Testing) is one of the automated testing techniques that automatically detects faulty inputs. If defects are automatically detectable and provides an<br> actionable test case, it can lead to significant cost savings in software development and maintenance phases. Concolic Testing combines symbolic execution, where program variables are<br>
 treated as symbolic variables during program execution, with SMT techniques to generate new inputs and maximize code coverage. Like other testing techniques, it is not complete but sound.<br>
  It is recognized for its ability to find faults in real-world software, making it widely used in the industry.

Concolic Testing offers distinct advantages compared to fuzzing techniques. Due to its similar features, it is often compared to fuzzing techniques. Concolic Testing outperforms fuzzing<br>
 techniques in many aspects, given that fuzzing techniques were first introduced to academia by Professor Barton Miller in 1990 and Concolic Testing was proposed by Sen et al. around <br>
 15 years later in 2006. Concolic Testing explores execution paths more effectively by considering conditions on input variables, leading to higher code coverage and thereby discovering <br>faults that may be difficult for fuzzing techniques to find.

However, Concolic Testing also has some limitations. It can be challenging to handle non-deterministic behavior or infinite execution paths (loops), especially when dealing with cryptographic<br>
 elements or cases where variable states are combined in various domains. Additionally, its applicability to all kinds of software may be limited due to constraints in the input domain.<br>
  The most prominent issues include execution costs and search space.

Concolic Testing still has room for improvement, despite being a two-decade-old technique. Numerous methodologies have been proposed to optimize exploration space since, <br>
unlike most fuzzing techniques, it operates on source code that is entirely whitebox at the testing stage, allowing for potential optimizations through source code analysis.