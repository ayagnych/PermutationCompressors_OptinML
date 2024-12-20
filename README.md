# Permutation Compressors 
[View the PDF file](PermutationCompressors_OptinML/CGD+Marina.pdf)

# Problem

In our project we consider a problem where communication from workers to a server is slow. To address the communication bottleneck, we proposed using compression:

$$x^{k+1} = x^k - \frac{\gamma}{n} \sum_{i=1}^n c_i \left( \nabla f_i \left( x^k \right) \right)$$

where $C_i$ are i.i.d. non-correlated compressors. 

# Proposed solution
We can use i.i.d. RandK compressors. R. Szlendak, A. Tyurin, and P. Richtarik in (2) proposed permutation compressors, which are correlated. They show that the MARINA method provably performs better with these compressors compared to i.i.d. compressors. In this project, we implemented the main methods of (2).

## Break down of the project
1. As a preliminary step, we implemented an environment that would emulate the communication of workers with the server (Opt_project_MARINA.ipynb)
2. Then we implemented CGD in this environment with the RandK and PermK compressors (Opt_project_CGD.ipynb) and implemented MARINA from (2) within those compressors
3. With logistic and linear regression we took gradients and compared methods for different numbers of workers and different levels of compression

