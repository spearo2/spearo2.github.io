---
layout: post
category: writings
---
## 도움이 되는 기술
## Tech that does actually help


디버깅 자동화는 중요한 문제이다. 디버깅은 프로그램의 결함을 발견하고 제거하는
행동으로서 결함 탐색, 결함 분석, 결함 재생산, 수정, 수정 검증의 단계로 진행된
다. 2022년 Maddev에서 진행한 조사에 따르면 미국의 소프트웨어 기업이 매년
프로그램 유지 보수에 사용하는 비용은 개발 비용에 10배에 달하며 그중 절반이
넘는 비용이 디버깅에 사용된다. 또한 Haystack의 조사에 따르면 소프트웨어의 복
잡도가 증가함에 따라 전체 82%의 소프트웨어 개발자가 증가하는 업무량에 따른
무기력감을 경험하고 있다고 한다. 만약 이렇게 값비싼 디버깅 과정의 일부라도 자
동화할 수 있다면 소프트웨어의 신뢰성 향상은 물론 더욱 적극적인 개발로 이어질
것이다. 이러한 이유 때문에 자동 디버깅의 세부 단계에 해당하는 수많은 공학적인
시도들이 약 40년의 시간 동안 활발히 연구되며 발전하고 있다. 소프트웨어 공학의
관점에서 프로그램 분석, 검증, 결함 위치 추정, 결함 예측, 테스팅, 자동 수정 등의
기술이 모두 이에 해당된다고 볼 수 있다.
반면에 실제 현업에서 사용되고 있는 기술은 실제 연구된 기술들의 극히 일부에
불과하다. 과거 Chris Parnin은 직접 현업 개발자로부터 이러한 이유를 조사하였
고 소프트웨어 공학에서 다양한 문제를 탐색 문제로 치환하는 방식이 실제 사람이
디버깅하는 방식과 다른 점을 지적했다. 이론적으로 접근 했을 때 이러한 현상은
기술의 안전함과 완전함으로 설명될 수 있다. 실제로 사용되는 기술과 사용되지
않는 기술들을 비교해보면 탐색 기반이나 기계 학습 기술을 활용하여 확률적으로
주어진 작업에 성공하는 안전하지도 완전하지도 않은 기술들은 주로 사용되지 않으
며 안전한 정적 분석기나 완전한 테스팅 기반의 기술이 사용되는 것을 알 수 있다.
또한 마이크로소프트의 조사에 따르면 오탐이 20%이상인 기술은 개발자가 현업에
서 사용하기 어렵다는 것을 알 수 있다. 따라서, 실제 현업 환경에서는 안전하거나
완전한 기술이 그리고 완전한 기술이 선호된다는 것을 알 수 있다.
발전된 프로그래밍 시스템을 꿈꾸는 연구자로서 이러한 현실적인 문제 또한
진지하게 고민해 봐야 하는 문제라고 생각한다. 지금의 연구 그리고 이후의 연구
에서 내 손으로 만들어낼 기술들이 현업에 기여하고 많은 사람에게 도움이 되기를
희망한다.


Automating debugging is an important problem. Debugging involves the process of discovering and eliminating defects in a program, progressing through phases such as defect identification, defect analysis, defect reproduction, correction, and validation of correction. According to a 2022 survey conducted by Maddev, US software companies spend ten times more on annual software maintenance costs compared to development costs, with over half of that cost attributed to debugging. Additionally, based on Haystack's research, as software complexity increases, 82% of software developers experience feelings of helplessness due to the rising workload. If even a portion of this costly debugging process could be automated, it would lead to improved software reliability and more proactive development.

For these reasons, numerous engineering attempts corresponding to the various stages of automated debugging have been actively researched and developed over about 40 years. From a software engineering perspective, techniques such as program analysis, verification, defect localization, defect prediction, testing, and automated correction all fall under this umbrella.

On the other hand, the technologies actually used in practical industry settings are only a small subset of the technologies that have been researched. In the past, Chris Parnin directly investigated these reasons with input from industry developers. He pointed out that the approach of transforming various problems in software engineering into exploration problems differs from how humans debug. Theoretically, this phenomenon can be explained by the safety and completeness of the approach. In practice, when comparing the technologies that are used versus those that are not, it can be seen that probabilistic and incomplete techniques, such as search-based or machine learning-based methods, are not predominantly used. Instead, safer static analysis tools or comprehensive testing-based techniques are more common. Additionally, according to Microsoft's research, technologies with false positive rates of over 20% are difficult for developers to use in real-world settings. Therefore, in actual industry environments, safe or comprehensive technologies are preferred.

As a researcher aspiring for advanced programming systems, I believe that these practical issues must also be seriously considered. I hope that the technologies I develop in the current and future research efforts will contribute to the industry and provide assistance to many individuals.