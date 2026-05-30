# 🍕 DoorDash Delivery Duration Prediction: Machine Learning Guessing Brain

Welcome to my second major Business Analyst project! In this case study, I built a Predictive Machine Learning model to solve a classic DoorDash challenge: **Guessing exactly how many seconds it takes for a food delivery to arrive from the moment a customer clicks "Order."**

## 🧰 The Machine Learning Toolbox
To build our guessing brain, I used Python and these high-tech tools:
* **Pandas & NumPy:** To clean raw data and manipulate datasets.
* **Scikit-Learn:** To split data into a "Study Pile" and a "Quiz Pile" (`train_test_split`), and score our results.
* **LightGBM (LGBM):** Our supercomputer AI brain that solves the prediction math at lightning speed.

---

## 🧠 Feature Engineering (Inventing Super Clues)
To make our AI brain extra smart, I combined the simple columns DoorDash gave us into **Super Clues**:
1. **Free Dashers:** Total Available Drivers minus Busy Drivers (`total_onshift_dashers - total_busy_dashers`). This tells the brain if there is a shortage of drivers on the road.
2. **Order Hour:** Extracting the exact hour from the timestamp to catch the busy Dinner Rush traffic peaks.
3. **Baseline Estimates:** Combining pre-existing kitchen prep estimates and road driving estimates to give our model a solid starting point.

---

## 🔬 Training and Evaluation (The Grading)
* **The Training Process:** We turned all text descriptions (like cuisine categories and store IDs) into numbers using a dummy-coding trick. The model evaluated **2,053 unique clues** across over **157,000 historical deliveries**!
* **The Final Score:** We tested our model on completely unseen test data (the Quiz Pile) using Mean Absolute Error (MAE).

### 🏆 Final Result: 13.71 Minutes
On average, our magic brain is able to guess the exact delivery time within **13.71 minutes** of accuracy! For a complex city network with dynamic cooking and traffic times, this forms a highly reliable baseline.

---

## 🚀 Key Business Takeaways
* **Deconstructing Delays:** Kitchen prep time handles the internal restaurant delays, while the `Free Dashers` metric perfectly handles supply and demand on the road.
* **Smart UI Expectations:** DoorDash can use this 13.71-minute baseline model to display highly accurate delivery windows, preventing customers from getting "hangry" due to unexpected delays.
