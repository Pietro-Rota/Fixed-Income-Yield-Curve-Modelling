# Yield Curve Modelling: JGBs vs. Toyota Corporate Bonds

This project explores the term structure of interest rates and credit risk within the Japanese fixed-income market. Using the **Nelson-Siegel-Svensson (NSS)** model, we estimate and compare the spot and forward rate curves for Japanese Government Bonds (JGBs) and Toyota corporate bonds.

## Project Overview
The goal of this analysis is to identify the implied forward credit spread and assess how investors price time value, liquidity, and credit risk across different maturities in a unique macroeconomic environment (Japan's transition away from ultra-low interest rates).

### Key Features:
*   **Data Source:** Bloomberg Terminal (Data as of March 10, 2026).
*   **Dataset:** 326 Japanese Government Bonds (JGBs) and 37 Toyota corporate bonds.
*   **Model:** Nelson-Siegel-Svensson (NSS) to capture level, slope, and curvature (plus an additional curvature term for a better fit).
*   **Optimization:** The model parameters were optimized by minimizing the **Root Mean Square Error (RMSE)** of the yields.

## Methodology
We opted for the amplified NSS model over the simplified Nelson-Siegel version to better capture the complexities of the Japanese yield curve.

### 1. Spot Rate Estimation
The NSS model uses six parameters ($\beta_0, \beta_1, \beta_2, \beta_3, \tau_1, \tau_2$) to derive a smooth spot rate curve. By penalizing large deviations through RMSE, the model ensures a stable fit for illiquid or long-maturity bonds.

### 2. Forward Rate Derivation
Forward rates were calculated by reversing the relationship between spot rates and forward rates

### 3. Credit Spread Analysis
The forward credit spread was calculated as the difference between the Toyota forward rate and the JGB forward rate to isolate corporate-specific risk premiums.

## Key Findings
*   **Upward Sloping Curves:** Both sovereign and corporate spot curves show a steady increase with maturity, reflecting a return to "normal" market pricing following the Bank of Japan's exit from negative interest rates.
*   **Forward Credit Spread:** 
    *   **Short-End:** A sensible positive premium (approx. 0.6%) for Toyota over JGBs.
    *   **Long-End:** The spread turns negative after the 10-year horizon. 
*   **Analysis of Distortions:** The negative long-end spread is interpreted not as a "true" negative credit premium, but as a result of market distortions caused by years of Yield Curve Control (YCC) and the high sensitivity of the NSS model at ultra-long maturities.

## 👥 Contributors
*   Paul Delalande
*   Ngoc Minh Khue Nguyen
*   Tien Thanh Doan
*   Pietro Rota

---
*This project was completed as part of the **Fixed Income (SMM149)** module at **Bayes Business School**.*
