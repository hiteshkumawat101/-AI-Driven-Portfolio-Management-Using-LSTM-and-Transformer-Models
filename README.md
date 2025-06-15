 📊 AI-Driven Portfolio Management Using LSTM and Transformer Models

This project replicates and extends the research presented in the paper:

> "Artificial Intelligence in Quantitative Finance: Leveraging Deep Learning for Smarter Portfolio Management and Asset Allocation"  
> [Original paper reference - included in ArtificialIntelligenceinQuantitativeFinance.pdf]

 🧠 Objective

To use deep learning models (LSTM and Transformer) for predicting asset returns, and leverage those predictions for dynamic asset allocation and portfolio performance evaluation.



 📁 Project Structure

| File | Description |
||-|
| Final.ipynb | Complete Jupyter Notebook with model training, prediction, portfolio simulation |
| ArtificialIntelligenceinQuantitativeFinance.pdf | Reference research paper used for methodology |



 🧱 Methodology

 1. 📥 Data Collection & Preprocessing
- Data collected using yfinance for: S&P 500, FTSE 100, Gold ETF.
- Calculated features:
  - Log returns
  - 5-day & 21-day moving averages
  - 21-day volatility
- Standardized inputs and handled missing values.

 2. 🧠 Model Design
- Implemented both LSTM and Transformer models using PyTorch.
- Trained one model per asset for multi-asset prediction.
- Used Mean Squared Error loss and early stopping.

 3. 💼 Portfolio Construction
- Combined predicted returns from all models.
- Applied mean-variance allocation strategy:  
  \( \text{weights} \propto \frac{\text{Expected Return}}{\text{Volatility}} \)
- Equal weights resulted due to similar signal strength.

 4. 📈 Performance Evaluation
Evaluated the portfolio using key financial metrics:
- Sharpe Ratio: 0.318
- Max Drawdown: -12.21%
- Annualized Return: 7.34%
- Annualized Volatility: 1.42%


 🔍 Key Observations

- The model-generated predictions were used to simulate a portfolio strategy.
- The final strategy showed moderate returns and low risk, but had a low Sharpe Ratio, indicating poor risk-adjusted performance.
- The equal asset weights suggest the models treated all assets with similar risk-return profiles.
- The project validates the paper's core idea — using deep learning to inform portfolio strategy — but additional layers like dynamic rebalancing, transaction cost modeling, or constraint-based optimization could improve realism.


 📌 Requirements

- Python 3.10+
- torch, numpy, pandas, scikit-learn, yfinance, matplotlib

Install them via:
bash
pip install -r requirements.txt
