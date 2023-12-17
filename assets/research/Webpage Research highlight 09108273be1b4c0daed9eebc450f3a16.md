# Webpage: Research highlight

Date Created: April 13, 2023 3:12 PM
Status: To Do

# AI-driven decision-making

My research group develops AI-driven approaches to decision-making, with a particular emphasis on robust and reliable learning methods. This requires an interdisciplinary approach spanning several fields including machine learning, operations research, and statistics. 

## Research philosophy and methodology

The standard algorithmic development paradigm for decision-making relies on theoretical performance guarantees and as a result, often ignore important operational constraints or are non-performant in practice. While theoretical insights can provide invaluable principles, their successful operationalization requires recognizing and internalizing the limitations of crude approximations and unverifiable assumptions we put in place for mathematical convenience. 

We identify central intellectual bottlenecks in real-world problems, and resolve them by building computational and data-centric foundations borne out of mathematical principles. Our research methodology aims to connect two disparate yet complementary worldviews:

- rigorous empirical benchmarking practices arising from the AI research community’s data-centric approach
- theoretical and computational tools from statistical learning, optimization, applied probability, and casual inference.

I take inspiration from Von Neumann’s perspective on mathematical sciences, which I paraphrase below.

> As a mathematical discipline travels far from its empirical source only indirectly inspired from ideas coming from 'reality', it is beset with grave dangers that it will develop along the line of least resistance and become more and more purely aestheticizing. This need not be bad if the discipline is under the influence of researchers with an exceptionally well-developed taste, but the only general remedy is the rejuvenating return to the source: the reinjection of directly empirical ideas. I am convinced that this is a necessary condition to conserve the freshness and the vitality of the subject, and that this will remain so in the future. (Click here for the full article[.](https://www.notion.so/Bon-App-tit-Foodcast-8f53b7bc2c1e472faaba18bea10e1139?pvs=21))
> 

[TheMathematician.pdf](Webpage%20Research%20highlight%2009108273be1b4c0daed9eebc450f3a16/TheMathematician.pdf)

I am extremely fortunate to be able to learn from the well-developed taste of my fabulous colleagues at Columbia and beyond. Concurrent to this ongoing personal education, I (try to) inject empirical ideas to formulate research directions to increase the impact of my research. 

## I. Robust and Responsible AI

Modern data collection systems acquire data from heterogeneous sources, and classical approaches that optimize average-case performance yield brittle AI systems. They fail to

- make good predictions on underrepresented groups
- generalize to new environments, even those similar to that seen during training
- be robust to adversarial examples and long-tailed inputs.

Yes, even the largest models trained on the entirety of the internet! 

Despite recent successes, lack of understanding on the failure modes of AI systems highlights the need for models that i) reliably work and ii) rigorous evaluation schemes and diagnostics that maintain their quality. We take a holistic “industrial engineering” view of AI systems, studying them from data collection to deployment & monitoring.

![ai-overview.png](Webpage%20Research%20highlight%2009108273be1b4c0daed9eebc450f3a16/ai-overview.png)

### Building a language defining distribution shifts

Different distribution shifts require different solutions. Understanding *why* model performance worsened is a fundamental step for informing subsequent methodological and operational interventions. Heterogeneity in data helps robustness, but the cost of data collection is often a binding constraint. We build a nuanced modeling language for quantifying data heterogeneity (or lack thereof), and use it to make optimally allocate limited resources in the AI production pipeline.

- [Cite as bitbtex; same format as publications page] T. Cai, H. Namkoong, and S. Yadlowsky. Diagnosing model performance under distribution shift. arXiv:2303.02011 [stat.ML], 2023. 
Major revision in Operations Research; conference version appeared Symposium on Foundations of Responsible Computing (FORC) 2023
- [Cite as bitbtex; same format as publications page] J. Liu, T. Wang, P. Cui, and H. Namkoong. On the need for a language describing distribution shifts: Illustrations on tabular datasets. In Advances in Neural Information Processing Systems 36, 2023.

[Modeling and Exploiting Data Heterogeneity under Distribution Shifts Tutorial](https://nips.cc/virtual/2023/tutorial/73953)

### Foundations of distributional robustness

Our vision is to build robust and reliable learning procedures that make decisions with a guaranteed level of performance over its inputs. My Ph.D. thesis built the statistical~\cite{NamkoongDu16, DuchiGlNa21, DuchiNa21} and computational~\cite{NamkoongDu16} foundations of robust machine learning. As robustness is a central topic spanning across multiple fields, my subsequent works have developed robust algorithms for deep learning~\cite{SinhaNaDu18, VolpiNaSeDuMuSa18}, causal inference~\cite{YadlowskyNaBaDuTi21, JeongNa20}, reinforcement learning~\cite{NamkoongKeYaBr20}, and safety evaluation of autonomous vehicles~\cite{OKellySiNaDuTe18}. These works have led to new approaches toward fairness by characterizing fundamental connections between robustness and fairness~\cite{HashimotoSrNaLi18, DuchiHaNa21, LiNaXi21}. 

- [Cite as bitbtex; same format as publications page] J. C. Duchi and H. Namkoong. Learning models with uniform performance via distributionally robust optimization. Annals of Statistics, 49(3):1378–1406, 2021.
- [Cite as bitbtex; same format as publications page] J. C. Duchi, T. Hashimoto, and H. Namkoong. Distributionally robust losses against mixture covariate shifts. Operations Research, 2022.

[https://www.youtube.com/watch?v=DRlF5sdCkKY&ab_channel=GoogleTechTalks](https://www.youtube.com/watch?v=DRlF5sdCkKY&ab_channel=GoogleTechTalks)

## II. Computational framework for decision-making

Decision-making problems in OR/MS concerns the optimal allocation of scarce resources. We build scalable computational frameworks for learning operational decisions by leveraging i) auto-differentiable simulators, and ii) empirically rigorous benchmarking. Our goal is to build a algorithmic development paradigm based on computation rather than theoretical approximations. 

### Auto-differentiable discrete event simulation

Typical operational decision-making problems (e.g., queueing, inventory management) are often distinguished by two characteristics: i) the dynamics of the system are relatively simple and ii) action space is combinatorially large. Despite their flexibility, black-box reinforcement learning methods are unreliable and require prohibitive amounts of data. We develop auto-differentiable simulators that can directly optimize policies at scale and showcase the promise of this algorithmic development paradigm on the benchmark problems we develop.

- [Cite as bitbtex; same format as publications page] E. Che, J. Dong, and H. Namkoong. Auto-differentiable discrete event simulation for queuing network control. Working paper, 2024.

### **Adaptive experimentation at scale**

Adaptive data collection can significantly improve data efficiency. Standard algorithms are primarily designed to satisfy good upper bounds on their performance (regret bounds), but do not model important operational constraints and are challenging to implement due to infrastructural/organizational difficulties. Instead of the typical theory-driven paradigm, we leverage computational tools and empirical benchmarking for algorithm development. Our proposed framework models practical instances in online platforms and social networks involving a handful of reallocation epochs in which outcomes are measured in batches. 

- [Cite as bitbtex; same format as publications page] H. Namkoong, S. Daulton, and E. Bakshy. Distilled thompson sampling: Practical and efficient thomp- son sampling via imitation learning. arXiv:2011.14266 [cs.LG], 2021. Selected for an oral presentation at the Neurips 2020 OfflineRL Workshop.
- [Cite as bitbtex; same format as publications page]  E. Che and H. Namkoong. Adaptive experimentation at scale: A computational framework for flexible batches. arXiv:2303.11582 [cs.LG], 2023.
    
    TLDR; To model short-horizon problems, we must design algorithms that optimize instance-specific constants, instead of relying on regret bounds that only hold in the large horizon limit. We develop a computation-driven adaptive experimentation framework that can flexibly handle batching. Our main observation is that normal approximations, which are universal in statistical inference, can also guide the design of adaptive algorithms. Instead of the typical theory-driven paradigm, we leverage computational tools and empirical benchmarking for algorithm development. Our approach significantly improves statistical power over standard methods, even when compared to Bayesian bandit algorithms (e.g., Thompson sampling) that require full distributional knowledge of individual rewards. Overall, we expand the scope of adaptive experimentation to settings that are difficult for standard methods, involving limited adaptivity, low signal-to-noise ratio, and unknown reward distributions.**** 
    
    ![arm_diagram.png](Webpage%20Research%20highlight%2009108273be1b4c0daed9eebc450f3a16/arm_diagram.png)
    

[https://youtu.be/CLzRcOw9eyk?si=Y3CRCBMeVxK-PKdU](https://youtu.be/CLzRcOw9eyk?si=Y3CRCBMeVxK-PKdU)

## III. Robust off-policy learning

Engineered approaches to off-policy learning---based on deep learning and simulation optimization---have recently achieved substantial empirical progress but often produce unreliable policies due to their heuristic nature. For these methods to bear fruit and transform applications where experimentation is costly, it is important to avoid deploying policies whose safety cannot be verified. While prediction models can be easily evaluated on previously collected data, assessing decision-making performance requires counterfactual reasoning. Traditional modeling assumptions that allow adjusting prediction models to learn counterfactuals rarely hold in practice. The growth in the nominal volume of data is no panacea: observed data typically only covers a portion of the state-action space, posing challenges in counterfactual learning. Concomitant to unseen data sparsity, shifts in the data distribution are common. Observed decisions depend on unrecorded confounders, and learning good policies requires causal reasoning. Marginalized demographic groups are severely underrepresented; for example, among 10000+ cancer clinical trials the National Cancer Institute funds, fewer than 5% of participants were non-white. 

Our existing statistical language falls woefully short as it relies on unverifiable (and often false) assumptions, and we lack diagnostics that can identify failure modes. We develop data analysis tools that can i) guarantee robust scientific findings and perhaps more importantly, ii) fail in expected ways by highlighting the fundamental epistemic uncertainty in the data.

### External validity

While large-scale randomized studies offer a “gold standard” for internal validity, their external validity can be called into question over spatiotemporal changes in the population, particularly when the treatment effect is heterogeneous across the population. The ACCORD and SPRINT trials offer a prominent example: they studied the effect of treatments to lower blood pressure on cardiovascular disease, but reached opposite conclusions despite exceptionally large sample sizes (5-10K). The mechanism behind the difference could not be explained by experts even ex-post. 

We develop new methods to assess and improve the external validity of RCTs. In particular, we develop sensitivity analysis frameworks that allows researchers to assess the extent to which existing experiments inform the treatment effect in a new target site and quantify an expected range of the policy effect for each new site. 

- [Cite as bitbtex; same format as publications page] S. Jeong and H. Namkoong. Robust causal inference under covariate shift via worst-case subpopulation treatment effect. arXiv:2007.02411 [[stat.ML](http://stat.ml/)], 2022. Short version appeared in Conference on Learning Theory 2020.

### **Unobserved confounding**

Off-policy methods can learn decision policies using the rich reservoir of previously collected (observational) data. A universal assumption that enable counterfactual reasoning requires observed decisions do not depend on any unrecorded confounders that simultaneously affect future states/rewards. This condition is frequently violated in medicine, e-commerce, and public policy, e.g., emergency department patients often do not have an existing record in the hospital’s electronic health system, leaving essential patient-specific information unobserved in subsequent counterfactual analysis. In the presence of unobserved confounding, even with large samples, it is impossible to precisely estimate the performance of the evaluation policy. To guard against spurious counterfactual evaluations, we propose a worst-case approach where we first posit a realistic notion of bounded unobserved confounding that limits the influence of unrecorded variables on observed decisions and develop corresponding worst-case bounds on the reward. 

- [Cite as bitbtex; same format as publications page] S. Yadlowsky, H. Namkoong, S. Basu, J. Duchi, and L. Tian. Bounds on the conditional and average treatment effect with unobserved confounding factors. Annals of Statistics, 50(5):2587–2615, 2022.

![confounding.png](Webpage%20Research%20highlight%2009108273be1b4c0daed9eebc450f3a16/confounding.png)

### **Unforeseen data sparsity**

A central challenge in observational analysis is that the effective sample size is difficult to gauge. Even when a nominally large dataset is collected, the effective sample size may be prohibitively small when there is little overlap between trajectories seen under the data-generating and proposed policies. Data sparsity becomes more pronounced in modern problems that involve high-dimensional covariates representations; causal identification becomes difficult on parts of the covariate space with limited effective sample size. Existing observational methods are only valid in the large sample limit and silently fail in practical instances, where the effective sample size is limited. 

We propose a new inferential framework that provides always-valid uncertainty quantification. Unlike asymptotic methods, we quantify instance-specific uncertainty that accurately scales with the level of overlap Our proposed counterfactual evaluation paradigm i) provides always-valid uncertainty estimates, spurring engineering progress through rigorous empirical evaluations, and ii) guides the optimal design of experiments based on previously collected (observational) data.

[https://youtu.be/FqdH75RazNQ](https://youtu.be/FqdH75RazNQ)