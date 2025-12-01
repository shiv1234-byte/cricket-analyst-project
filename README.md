🏏 Cricket Analyst Project
This project uses data analytics to select the best possible playing XI on the planet based purely on performance metrics, without any prior knowledge of the opposition. The aim is to build a team that can consistently score 180+ runs and defend 150 runs on average in T20-style matches.​

🧠 Problem Statement
“We don’t know the strengths and weaknesses of our opponents, but give me the best 11 from this planet.”

The project solves this by:

Defining clear role-based KPIs (Openers, Anchors/Middle Order, Finishers, All‑rounders, Specialist Fast Bowlers).​

Applying statistical filters on historical performance data to shortlist players for each role.

Assembling a balanced playing XI capable of both high scoring and strong defense.

🎯 Role Definitions & Selection Criteria
Players are classified into roles and filtered using quantitative thresholds like batting average, strike rate, boundary percentage, balls faced, bowling economy, and bowling strike rate.​

Openers
Must give fast, solid starts.

Key metrics:

Batting Average > 30

Strike Rate > 140

Innings Batted > 3

Boundary % > 50

Batting Position < 4

Anchors / Middle Order
Stabilize the innings and build partnerships.

Key metrics:

Batting Average > 40

Strike Rate > 125

Innings Batted > 3

Avg. Balls Faced > 20

Batting Position > 2

Finishers / Lower Order Anchors
Close out innings aggressively in fewer balls.

Key metrics:

Batting Average > 25

Strike Rate > 130

Innings Batted > 3

Avg. Balls Faced > 12

Batting Position > 4

All‑rounders / Lower Order
Contribute with both bat and ball for balance.

Batting criteria:

Batting Average > 15

Strike Rate > 140

Innings Batted > 2

Batting Position > 4

Bowling criteria:

Innings Bowled > 2

Economy < 7

Bowling Strike Rate < 20

Specialist Fast Bowlers
Primary job is to take wickets economically.

Key metrics:

Innings Bowled > 4

Economy < 7

Bowling Strike Rate < 20

Bowling Style: Fast / Fast‑Medium

🔍 How the Analysis Works
Data Ingestion

Load player batting and bowling records from CSV/Excel (e.g., T20 internationals or league data).​

Feature Engineering

Calculate derived stats like batting average, boundary %, economy, bowling strike rate, etc.

Role Classification & Filtering

Assign roles based on batting position and bowling involvement.

Apply the above thresholds to filter top candidates per role.​

Best XI Selection

Pick a balanced combination of:

2 Openers

2–3 Anchors/Middle Order

2 Finishers

2–3 All‑rounders

3 Specialist Fast Bowlers

🛠 Tech Stack
Language: Python / Power BI / Excel (update as per your build)

Libraries: Pandas, NumPy, Matplotlib/Seaborn (if Python-based)​

Data Source: Public cricket scorecards / Cricinfo‑style datasets (not included to respect data ownership).​

🚀 Getting Started
Clone the repo

bash
git clone https://github.com/<your-username>/cricket-analyst-project.git
cd cricket-analyst-project
Install dependencies (if Python)

bash
pip install -r requirements.txt
Add data

Place your raw player stats file in the data/ folder (e.g., players_stats.csv).

Run the analysis

bash
python main.py
or open the notebook (e.g., notebooks/cricket_analyst.ipynb) and run all cells.

📊 Outputs
Shortlisted players per role with all KPIs.

Final Best XI with a balance of batting depth and bowling strength.

Optional charts: distributions of strike rate, economy, and contributions by role.​

📌 Future Improvements
Incorporate match context (venue, opposition, phase-wise stats).

Add dashboard using Power BI / Streamlit for interactive selection.​

Use advanced models (e.g., role-based performance indices or deep learning ranking).​

📄 License
anyone can use this project and give stars to my project
