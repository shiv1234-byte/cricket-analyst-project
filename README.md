# 🏏 Cricket Analyst Project

This project uses data analytics to select the **best possible playing XI on the planet** based purely on performance metrics, without any prior knowledge of the opposition. The goal is to build a team that can consistently **score 180+ runs** and **defend 150 runs** on average in T20-style matches.

## 🧠 Problem Statement

“We don’t know the strengths and weaknesses of our opponents, but give me the best 11 from this planet.”

This project:
- Defines clear, **role-based KPIs** for Openers, Anchors/Middle Order, Finishers, All‑rounders, and Specialist Fast Bowlers.   
- Applies **statistical filters** on historical performance data to shortlist players for each role.  
- Assembles a **balanced playing XI** that combines explosive batting with reliable bowling.

## 🎯 Role Definitions & Criteria

Players are categorized into roles and filtered using quantitative thresholds such as **batting average, strike rate, boundary %, balls faced, bowling economy, and bowling strike rate**. [web:2][web:5]

### 🔹 Openers

Role: Provide fast, stable starts in the powerplay.

- Batting Average **> 30**  
- Strike Rate **> 140**  
- Innings Batted **> 3**  
- Boundary % **> 50**  
- Batting Position **< 4**

### 🔹 Anchors / Middle Order

Role: Stabilize the innings, build partnerships, handle pressure phases.

- Batting Average **> 40**  
- Strike Rate **> 125**  
- Innings Batted **> 3**  
- Avg. Balls Faced **> 20**  
- Batting Position **> 2**

### 🔹 Finishers / Lower Order Anchors

Role: Close out innings aggressively in fewer balls.

- Batting Average **> 25**  
- Strike Rate **> 130**  
- Innings Batted **> 3**  
- Avg. Balls Faced **> 12**  
- Batting Position **> 4**

### 🔹 All‑rounders / Lower Order

Role: Provide depth in both batting and bowling.

Batting:
- Batting Average **> 15**  
- Strike Rate **> 140**  
- Innings Batted **> 2**  
- Batting Position **> 4**

Bowling:
- Innings Bowled **> 2**  
- Economy **< 7**  
- Bowling Strike Rate **< 20**

### 🔹 Specialist Fast Bowlers

Role: Take wickets while keeping runs in check.

- Innings Bowled **> 4**  
- Economy **< 7**  
- Bowling Strike Rate **< 20**  
- Bowling Style: **Fast / Fast‑Medium**

## 📊 Summary Criteria Table

| Role                    | Key Batting Criteria                          | Key Bowling Criteria                   |
|-------------------------|-----------------------------------------------|----------------------------------------|
| Openers                 | Avg > 30, SR > 140, Boundary % > 50          | –                                      |
| Anchors / Middle Order  | Avg > 40, SR > 125, Balls Faced > 20         | –                                      |
| Finishers               | Avg > 25, SR > 130, Balls Faced > 12         | –                                      |
| All‑rounders            | Avg > 15, SR > 140                           | Econ < 7, SR < 20, Innings > 2         |
| Specialist Fast Bowlers | –                                             | Econ < 7, SR < 20, Innings > 4         | 

## 🔍 How the Analysis Works

1. **Data Ingestion**  
   - Load player batting and bowling stats from CSV/Excel (e.g., T20 leagues or international data). [web:7][web:10]

2. **Feature Engineering**  
   - Compute metrics like batting average, strike rate, boundary %, economy, bowling strike rate, etc.

3. **Role Classification & Filtering**  
   - Assign roles using batting position and bowling workload.  
   - Apply role-wise thresholds to shortlist top candidates. [web:2][web:13]

4. **Best XI Selection**  
   - Build a balanced XI with:
     - 2 Openers  
     - 2–3 Anchors / Middle Order  
     - 2 Finishers  
     - 2–3 All‑rounders  
     - 3 Specialist Fast Bowlers  

## 🛠 Tech Stack

- **Language:** Python / Power BI / Excel  
- **Python Libraries (if used):** Pandas, NumPy, Matplotlib/Seaborn  
- **Data Source:** Public cricket stats exports (not redistributed here to respect data ownership).

## 🚀 Getting Started

1. Clone the repository:
Or open the main notebook (e.g., `notebooks/cricket_analyst.ipynb`) and run all cells.

## 📌 Future Enhancements

- Context-aware metrics (venue, opposition, phase-wise stats).  
- Interactive dashboards using **Power BI / Streamlit**. 
- Advanced player ranking models using role-based indices or machine learning. 

## 📄 Disclaimer

This project is for learning, analytics, and portfolio purposes. All external cricket data remains the property of its respective owners and is not redistributed here, in respect of copyright and intellectual property.

