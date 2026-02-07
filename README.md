## 📚 Background & Acknowledgments

This repository is built upon the foundational code examples provided in *Computerized Adaptive and Multistage Testing with R - Using Packages catR and mstR* (Magis et al., 2017).

## The CAT Process (Computerized Adaptive Testing)

The Computerized Adaptive Testing process is based on Item Response Theory (IRT) and follows an iterative algorithm divided into four logical steps, as detailed by Magis et al. (2017, pp. 36-37; Fig 3.1):

<div align="center">
  <img width="800" alt="CAT Process Diagram" src="https://github.com/user-attachments/assets/b1498e18-596f-4e9f-be22-f4bccf01dcd3" />
</div>

**1. Initial Step**
* **Initialization:** The process begins with the **selection and administration of the first item** (or a small set of initial items) to initialize the CAT algorithm.

**2. Test Step (Iterative Loop)**
This is the core cycle of the adaptive test. It repeats until the stopping criteria are met:
* **Estimation:** The system calculates an **ad-interim ability estimation** ($\theta$) based on the current response pattern.
* **Selection:** Based on the current estimate, the algorithm selects and administers the next optimal item from the calibrated item bank.
* **Update:** The user's **response pattern** is updated with the new answer, and the ability estimate is re-calculated.

**3. Stopping Step**
* **Evaluation:** After each estimation, the system checks if the **stopping rule is satisfied**.
* **Criteria:** Common stopping rules include reaching a specific standard error of measurement (precision), administering a maximum number of items, or exceeding a time limit.
  * *If **NO**:* The process returns to the *Test Step* to select the next item.
  * *If **YES**:* The item administration ends.

**4. Final Step**
* **Conclusion:** Once the loop is broken, the system performs the **final ability estimation** to generate the final score and report.

  
<sub><sub>**⚠️ Recommendation:** The following is a summary of the process. For a comprehensive understanding and underlying theory, **it is strongly recommended to refer to Magis et al. (2017)**.</sub></sub>


---

### 🔗 References
* *Magis, D., Yan, D., & Von Davier, A. A. (2017). Computerized Adaptive and Multistage Testing with R. In Use R!* https://doi.org/10.1007/978-3-319-69218-0
