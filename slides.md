# Quarterly Earnings Report — Q3

**Prepared by:** Technical Consulting Team  
**Contact:** <span class="email">24ds2000078@ds.study.iitm.ac.in</span>

---

## Agenda

- Overview of performance
- Key financial metrics
- Forecast and models
- Q&A

Note:
This slide is shown as an agenda; speaker should call out the three main sections.

---

## Overview (Markdown slide)

We present **quarterly earnings highlights** and comparison to prior quarter.

- Revenue: $R_{t}$
- Net Income: $NI_{t}$
- YoY Growth: 12%

---

## Key Metrics (with fragments)

- Total Revenue: $R_{t}$  
  <span class="fragment">• Revenue growth vs last quarter: +3.5%</span>  
  <span class="fragment">• Revenue drivers: Core Banking, Lending</span>

- Net Profit Margin: $M_{t}$  
  <span class="fragment">• Margin improvement due to cost optimization</span>

Note:
Use these bullets to sequentially reveal talking points.

---

## Financial Formula (Math)

We use the basic NPV formula for investment evaluation:

\[
\mathrm{NPV} = \sum_{t=0}^{N} \frac{CF_t}{(1+r)^t}
\]

and CAPM for expected return:

\[
E(R_i) = R_f + \beta_i (E(R_m) - R_f)
\]

Note:
Explain discount rate selection and beta estimation briefly.

---

## Code: Simple forecast example (Python)

```python
# A minimal AR(1) forecast example (for demonstration)
import numpy as np
from statsmodels.tsa.ar_model import AutoReg

y = np.array([100, 102, 101, 105, 107, 110])
model = AutoReg(y, lags=1).fit()
pred = model.predict(start=len(y), end=len(y)+2)
print(pred)
