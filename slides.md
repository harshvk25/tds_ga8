# Quarterly Earnings Report — Q3  
### TDS Assignment 8  

**Email:** 24ds2000078@ds.study.iitm.ac.in  
(This email appears clearly on this slide.)

---

## Agenda (Markdown Slide)

- Quarterly performance
- Key financial metrics
- Forecasting models
- Recommendations

Note:
This is your agenda slide—explain the 4 sections briefly.

---

## Key Metrics (with fragments)

- Revenue Growth: **+3.5%**
  <span class="fragment">• Driven by lending and payments</span>
  <span class="fragment">• Customer acquisition increased 11%</span>

- Net Profit Margin
  <span class="fragment">• Improved due to lower operating costs</span>

Note:
Fragments will appear one by one to control the pace.

---

## Financial Formula (Math Slide)

The Net Present Value (NPV) formula used in financial planning:

\[
NPV = \sum_{t=0}^{N} \frac{CF_t}{(1+r)^t}
\]

And the CAPM expected return formula:

\[
E(R_i) = R_f + \beta_i(E(R_m) - R_f)
\]

Note:
Emphasize that NPV is sensitive to discount rate selection.

---

## Code Example (Python)

```python
# Sample AR(1) forecasting model
import numpy as np
from statsmodels.tsa.ar_model import AutoReg

data = np.array([100, 102, 101, 104, 107, 110])
model = AutoReg(data, lags=1).fit()
forecast = model.predict(len(data), len(data)+2)

print(forecast)
