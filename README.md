# Parallelization Scheme for Modeling Coagulation

## The "Big" Problem

* Modeling the time evolution of number densities of particles experiencing *coagulation* (or clumping together) is extremely computationally intensive
* The only code that exists for modeling this phenomena is **serial**
* Often takes up to several days to process on a cluster like USC CARC!

* Most famous and relevant equation for describing this evolution of coagulating particles is the **Smoluchowski Coagulation Equation**:

$$\frac{d}{d t} f_k=\frac{1}{2} \sum_{i+j=k} K(i, j) f_i f_j-\sum_i K(i, k) f_i f_k$$

* $K$ is the coefficient for coagulation between  and j (sticking coefficient)
* $f_k$ is the number density of particle with m = k.

## Importance


![](https://github.com/DylanUSC/Parallel_Coagulation_Kernel/blob/main/Interstellar_dust.jpeg)


Along with modeling coagulation of particles in the atmosphere, this equation is also crucial for aerosols and — most importantly — **interstellar dust**. Because there is no parallelized version for integrated models for this solver, this step has become a bottleneck in the modeling process for coagulation.


* $K$ is…
* $f_i$ is….
* $f_j$ is …
* $f_k$ is …

## Importance

* Equation is also crucial for aerosols and — most importantly — **interstellar dust**. 
* Since no parallelized version for integrated models for this solver exist, this step has become a _bottleneck_ in the modeling process for coagulation.
>>>>>>> aac1fcac8666aa0e43dd8d4dae0d02026cb7d80c



## Proposed Solution 

* **PARALLELIZE** the numerical solver for the Smoluchowski coagulation equation.

## Team Members

* Ziyu Huang
* Kevin Sampson

## Applications

* Interstellar Dust Coagulation


![](https://github.com/DylanUSC/Parallel_Coagulation_Kernel/blob/main/Coagulation_Figure.png)

## Sequential test case: K = 1

K = 1

$N(m, t)=\frac{N_0}{m_0}\left(\frac{2}{N_0 t}\right)^2 \exp \left[\frac{2}{N_0 t}\left(1-\frac{m}{m_0}\right)\right]$

![](https://github.com/DylanUSC/Parallel_Coagulation_Kernel/blob/main/K1_Dustpy.png)


* Cloud condensation in planetary atmospheres



