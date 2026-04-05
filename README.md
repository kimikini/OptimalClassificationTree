# OptimalClassificationTree

**Optimal Classification Trees (OCT)** implemented in **Python** using **Gurobi mixed-integer optimization**. This project evaluates OCT on **UCI classification datasets** and compares its performance with **CART**, **Random Forest**, and **XGBoost**.

---

## **Overview**

Decision trees are widely used in machine learning because of their **interpretability**. However, traditional methods such as **CART** rely on greedy splitting rules and may fail to find globally optimal trees.  

This project implements **Optimal Classification Trees (OCT)** as a **mixed-integer optimization** problem and solves it with **Gurobi**. The project also compares OCT against **CART**, **XGBoost**, and **Random Forest** on real classification datasets.

**Contributors:** **Xiaoyan Lin**, **Zhuoqiao Ouyang**

---

## **Features**

- **Python implementation** of **Optimal Classification Trees (OCT)**
- Solved using **Gurobi**
- Supports **CART-based warm start**

- Experiments on **UCI classification datasets**
- Performance comparison with:
  - **CART**
  - **Random Forest**
  - **XGBoost**
- Includes **tree visualization** and **performance analysis**

---

## **Workflow**

The project follows the workflow below:

1. **Load and preprocess dataset**
2. Use **CART** to generate a **warm start**
   
   <img width="700" height="400" alt="CART" src="https://github.com/user-attachments/assets/8898e5b5-f5e1-4321-b732-76d5e1755397" />

4. Formulate the **OCT mixed-integer optimization model**
6. Solve the model with **Gurobi**
7. Reconstruct the tree from the optimized split variables
   <img width="700" height="400" alt="oct" src="https://github.com/user-attachments/assets/ed9cbb1d-c861-4918-b38b-6b67146299ef" />
   <img width="700" height="400" alt="octh" src="https://github.com/user-attachments/assets/792a93d0-acd9-4cb6-8092-32c7c43150b0" />

9. Evaluate training and testing performance
11. Compare results with **CART**, **Random Forest**, and **XGBoost**

---

## **Experimental Setup**

- **Solver:** Gurobi  
- **Tree depth:** 2  
- **Minimum leaf size:** \( N_{\min} = \lfloor 0.05n \rfloor \)  
- **Warm start:** CART-derived split rules  
- **Benchmarks:** CART, XGBoost, Random Forest  

---

## **Results Summary**

- **OCT** generally outperforms **CART**
- **OCT** remains competitive with **Random Forest** and **XGBoost**
- **OCT** provides strong **interpretability**
- **XGBoost** and **Random Forest** may achieve high accuracy, but they are less interpretable
<img width="800" height="500" alt="Table1" src="https://github.com/user-attachments/assets/837ffac9-6ae6-4f96-9df6-5ea8ea54205b" />

---

## **References**

1. **D. Bertsimas and J. Dunn**, “Optimal classification trees,” *Machine Learning*, vol. 106, no. 7, pp. 1039–1082, 2017.  

2. **Gurobi Optimization Inc.**, *Gurobi Optimizer Reference Manual*, 2015. Available: http://www.gurobi.com  

3. **IBM ILOG CPLEX**, *IBM ILOG CPLEX V12.1 User’s Manual*, 2014. Available: https://www-01.ibm.com/software/commerce/optimization/cplex-optimizer/  

4. **M. Lichman**, “UCI Machine Learning Repository,” 2013. Available: http://archive.ics.uci.edu/ml  

5. **S. Aghaei, A. Gómez, and P. Vayanos**, “Strong optimal classification trees,” 2021. Available: https://optimization-online.org/wp-content/uploads/2021/01/StrongOCT-1.pdf  

6. **T. P.**, “Overfitting and underfitting in machine learning,” *SuperAnnotate*, Oct. 2022. Accessed: 2025-05-02. Available: https://www.superannotate.com/blog/overfitting-and-underfitting-in-machine-learning  

7. **X. Zhao**, “Optimal classification trees: MIT implementation,” n.d. Available: https://github.com/XuanyiZhao/Optimal_classification_trees
