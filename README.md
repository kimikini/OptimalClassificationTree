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
3. Formulate the **OCT mixed-integer optimization model**
4. Solve the model with **Gurobi**
5. Reconstruct the tree from the optimized split variables
6. Evaluate training and testing performance
7. Compare results with **CART**, **Random Forest**, and **XGBoost**

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

---
