# Mean-Reverting-Statistical-Arbitrage-Strategy
This project focuses on developing a statistical arbitrage strategy to identify and capitalize on temporary price divergences between pairs of technology stocks from the S&amp;P 500. The approach uses backtesting and optimization techniques, along with dynamic enhancements like adaptive leverage and stop-loss adjustments.

### Objective
- Identify pairs of tech stocks with strong historical relationships.
- Exploit temporary price divergences using a mean-reversion approach.
- Systematically backtest and optimize the trading strategy for robust, consistent returns.
- Manage risk through dynamic adjustments in leverage and stop-loss thresholds.

### Data
- **Scope**: Historical daily data for the top 50 tech stocks in the S&P 500 (2015–2024).
- **Source**: Adjusted closing prices ensuring comparability across stocks.

### Methodology

#### 1. **Pair Selection**
   - Focus on identifying tech stock pairs with strong historical correlations.
   - Emphasize high liquidity and frequent inefficiencies, making tech stocks ideal candidates for statistical arbitrage.

#### 2. **Trade Signal Generation**
   - **Z-Score**: Generated from the spread between paired stocks.
   - **Entry Signal**: Open position when absolute z-score > 1.5.
   - **Exit Signal**: Close position when z-score returns to 0.

#### 3. **Backtesting Framework**
   - Evaluated under three conditions:
     - **Without Optimization**: Baseline strategy with static parameters.
     - **Grid Search Optimization**: Fine-tuned parameters using grid search.
     - **Dynamic Adjustments**: Enhanced strategy with adaptive features.
     
#### 4. **Dynamic Enhancements**
   - **Dynamic Leverage**: Scales based on market conditions, increasing in stable markets and decreasing in volatile ones.
   - **Dynamic Stop-Loss**: Adjusts thresholds using rolling volatility, tightening during low volatility periods and widening during high volatility.

### Performance Optimization

#### 1. **Without Optimization**: 
   - Static strategy tested with fixed parameters:
     - Lookback = 20 days, Entry Threshold = 1.5, Stop-Loss Factor = 2.0.

#### 2. **With Grid Search Optimization**:
   - Optimized parameters for better signal detection:
     - Lookback period.
     - Entry threshold.
     - Stop-loss factor.

#### 3. **With Bayesian Optimization**:
   - Applied probabilistic optimization for faster convergence and better parameter tuning.

### Best Pair
- **Salesforce vs Amazon**
  - **Sharpe Ratio**: 1.42
  - **Annualized Return**: 5.7%
  - **Max Drawdown**: -19%

#### Requirements
- Python 3.x
- Pandas, NumPy, SciPy for data processing and analysis.
- Matplotlib/Seaborn for visualization.
- Scikit-learn for machine learning models.
- Backtrader or similar for backtesting.

#### How to Run
1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/statistical-arbitrage-tech-stocks.git
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the backtest:
   ```bash
   python backtest.py
   ```

#### Contributing
Feel free to fork this repository and submit pull requests for improvements or suggestions!
