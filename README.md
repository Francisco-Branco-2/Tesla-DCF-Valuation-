# Tesla (TSLA) Valuation - Discounted Cash Flow (DCF) Model

## 1. Repository Objective
The central objective of this project is to calculate the **Intrinsic Value** of Tesla shares (TSLA) using the **Discounted Cash Flow (DCF)** method. The code seeks to determine if the stock is undervalued or overvalued in the current market, based on fundamental assumptions rather than just the stock exchange price.

## 2. The Model Stages (The "Core" of the Exercise)
The repository divides the valuation exercise into the following phases:

### A. Data Collection and Assumptions
The code defines the critical input variables, which is essential given Tesla's volatility:
* **Revenue Growth Rate:** Aggressive vs. conservative projections for the next 5-10 years.
* **Operating Margins (EBIT):** The evolution of profitability as the company scales.
* **Tax Rate:** Future tax adjustments.

### B. WACC Calculation (Weighted Average Cost of Capital)
We calculate the discount rate used to bring future cash flows to their present value:
* **Cost of Debt:** Interest paid by Tesla.
* **Cost of Equity (Ke):** Based on the *Risk-Free Rate* (usually US T-Bonds) and Tesla's *Beta* (systemic risk).

### C. Cash Flow Projection (FCFF)
The exercise projects the **Free Cash Flow to the Firm**. The central formula used in the code is:

$$
FCFF = EBIT \times (1 - Tax Rate) + Depreciation - Capex - \Delta WorkingCapital
$$

### D. Terminal Value and Present Value
The code calculates Tesla's value in perpetuity (after the explicit projection period, usually 10 years) and discounts everything to the present day:

$$
Present Value = \sum_{t=1}^{n} \frac{FCFF_t}{(1 + WACC)^t} + \frac{Terminal Value}{(1 + WACC)^n}
$$

## 4. Final Output
At the end of the notebook, the repository presents:
1.  **Target Price per Share:** The fair value calculated by the model.
2.  **Margin of Safety:** The percentage difference between the calculated value and the current market price.
3.  **Sensitivity Analysis:** Tables showing how the stock price changes if growth is lower or if WACC is higher.

---

## How to Run
1.  Just download the Excel file and open it in the Office app on your desktop.
