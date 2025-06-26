# supply-chain-attack
一个描述软件供应链攻击的技术矩阵

# Description

https://github.com/kcrio/supply-chain-attack/tree/bbf352c71338d909783d6c40dba0faf19bae5a9a/techniques

# Supply chain attack matrix
https://kcrio.github.io/supply-chain-attack/

![image](https://github.com/kcrio/supply-chain-attack/assets/96735391/3f64a6c7-1394-4e4a-a8e4-46773c262493)


# Analytic Hierarchy Process 
1. Construct the Judgment Matrix

    The indicators is placed in the SSCAs scenario to assess the degree of software supply chain risk it induces.
The higher the threat, the higher the scale value.

|value|Definition|
|-|-|
|1|Equal Threat Level|
|3|Moderate Threat Level|
|5|Strong Threat Level|
|7|Very Strong or demonstrated Threat Level|
|9|Extreme Threat Level|
|2,4,6,8|Intermediate values|
|reciprocal|If activity i has one of the above nonzero numbers as signed to it when compared with activity j, then j has the reciprocal value when compared with i.|

2. Calculate single weights and check consistency.

    Repeat the Judgment Matrix assessments until the Consistency Ratio $(CR) ≤ 0.10$, indicating acceptable consistency.

3. Calculate the final weight vector for each indicator.
   
    The final weights of the indicators are derived from the uppermost level to the lower level. For the sake of simplicity, assuming there are two-layer indicators. The weight of n indicators in the upper layer is Wi, and the weight of m indicators in the lower layer is $W_j$. Therefore, the final weight vector of indicators in the lower layer is $W=\sum_{i=1}^{n}{\(W_i\cdot W_j\)}$, where $j=1,2,3,...,m$.

4. Final step

    The calculation process is simplified as the sum of the weights of all technical indicators corresponding to the event, which serves as the technical score. Since there are five sub-indicators in the impact category, the final score is derived using the full Analytic Hierarchy Process (AHP) computation. A weighted score is calculated for each event.
    ###### TTIM indicator
    Let $T = \{t_1, t_2, ..., t_n\}$ be the set of TTIM indicators associated with an event, and let $w_i$ denote the weight of the $i$-th indicator. The **technical score** $S_{TTIM}$ is computed as: $S_{TTIM} = \sum_{i=1}^{n} w_i$

    ###### Impact indicator
    For the impact indicators, where $I = \{i_1, i_2, ..., i_5\}$ denotes the five sub-indicators, and let $w_i$ denote the weight of the $i$-th indicator, the **final weighted score** $S_T$ for each event is obtained through the complete AHP procedure, resulting in: $S_{I} = \sum_{i=1}^{5}{\(Score_i \cdot w_i\)}$

