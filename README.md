# ⚾ 2026 MLB Monte Carlo Season Simulator

**Live Demo → [andrewgaldys.github.io/mlb-simulator](https://andrewgaldys.github.io/mlb-simulator)**

An interactive web app that simulates the entire 2026 MLB season **thousands of times** using probability theory and real preseason projections. See every team's playoff odds, World Series chances, and win distributions — all powered by math.

---

## What It Does

- Simulates every game of the 2026 MLB season (162 games × 30 teams) up to **25,000 times**
- Calculates **playoff odds**, **division winner %**, and **World Series %** for all 30 teams
- Displays a **win distribution histogram** showing the full range of possible outcomes
- Shows **90% confidence intervals** and **standard deviation** for each team
- Lets users **adjust any team's projected wins** with sliders and re-run the simulation
- Includes a full stat guide, math explainer, and data source documentation

---

## Math Concepts Used

### 1. Bernoulli Trials (Win Probability)
Each of the 162 games is modeled as a **Bernoulli trial** — a random event with two outcomes (win or loss). A team projected for 90 wins has a win probability of 90/162 ≈ 0.556, so each game is like flipping a coin that lands "win" 55.6% of the time.

### 2. Log5 Formula (Playoff Matchups)
Invented by Bill James, the **Log5 formula** calculates the probability that Team A beats Team B based on both teams' win percentages:

```
P(A beats B) = (pA - pA × pB) / (pA + pB - 2 × pA × pB)
```

A .600 team vs a .400 team wins **~69.2%** of the time — not just 60%.

### 3. Monte Carlo Simulation
The entire season + playoffs are repeated **thousands of times** using random numbers. By counting how often each outcome occurs, we estimate probabilities. Example: if the Dodgers win the World Series in 2,340 out of 10,000 simulations, their WS odds are **23.4%**.

### 4. Standard Deviation & Confidence Intervals
- **Standard deviation (σ)** measures how spread out the results are across simulations
- **90% confidence interval** shows the range where 90% of simulated outcomes fall (5th to 95th percentile)

---

## Data Sources

Projected win totals are a composite average of multiple respected projection systems, sourced in February 2026:

| Source | Description |
|--------|-------------|
| **FanGraphs Depth Charts** | Combines Steamer + ZiPS projections with roster depth |
| **Baseball Prospectus PECOTA** | Player-level projection system using comparable players |
| **Betting Market Consensus** | Oddsmakers' over/under win totals (BetMGM, FanDuel, etc.) |

---

## How to Use

1. Visit the [live site](https://your-username.github.io/mlb-simulator)
2. Click **▶ Run Simulation** (it auto-runs on load with 5,000 sims)
3. Change the simulation count for more or less precision
4. Click **⚙ Adjust Teams** to tweak any team's projected wins
5. Toggle **By Division** / **By League** to change the view
6. Hover over any column header **ⓘ** for an explanation of that stat
7. Expand **📖 How to Read This Table** or **📐 The Math Behind This** for full details

---

## Tech Stack

- **Pure HTML/CSS/JavaScript** — no frameworks, no build tools, no dependencies
- Single `index.html` file — runs entirely in the browser
- Hosted for free on **GitHub Pages**

---

## Run Locally

Just open `index.html` in any browser. That's it — no install, no server, no setup.

---

## Disclaimer

This is an independent mathematical simulation built for **educational purposes**. It is not affiliated with MLB, FanGraphs, Baseball Prospectus, or any sportsbook. Projections are estimates and should not be used for gambling decisions.

---

## Contributors

<!-- Replace with your actual GitHub usernames -->
- [@andrewgaldys](https://github.com/andrewgaldys)
- [@TribalChief2307](https://github.com/TribalChief2307)

---

*Built with Monte Carlo simulation, the Log5 formula, and Bernoulli probability theory.*
