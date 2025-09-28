---
theme: default
colorSchema: light
background: https://plus.unsplash.com/premium_photo-1679917151809-8234fb676b26?q=80&w=1932&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D
title: Profitability for wind farms
class: text-center
drawings:
  persist: false
transition: slide-left
# enable MDC Syntax: https://sli.dev/features/mdc
mdc: true
---

# Profitability for wind farms

#### How to think about KPIs and economic performance of wind farms?

---
transition: fade-out
---

# Profitability of <u>any project</u>

<div class="space-y-4 text-xl">

<v-click>

### **Revenue / Benefits**
- **Direct income**: sales, generated revenue, etc.
- **Indirect benefits**: portfolio synergies, lower risk, avoided costs, etc.

</v-click>

<v-click>

### **Costs / Investments**
- **CapEx (Capital Expenditure)**: upfront investment (e.g. equipment, infrastructure)
- **OpEx (Operating Expenditure)**: recurring costs (e.g. maintenance, labor, fees)

</v-click>

<v-click>

### **Profit**
$
\text{Profit} = \text{Total Revenue} - \text{Total Costs}
$
- ✅ Positive → Profitable
- ❌ Negative → Loss-making

</v-click>

</div>

---
layout: default
transition: fade
---

# Project Finance Metrics

<v-clicks>

| Metric | Definition | Equation |
|---|---|---|
| **Net Present Value** | Present value of future cash flows minus costs. <br> ✅ NPV > 0 → project is profitable. | $NPV = \sum_{t=0}^{T} \frac{C_t}{(1 + r)^t}$ |
| **Internal Rate of Return** | Discount rate at which NPV = 0. <br> ✅ IRR > Cost of Capital → project is profitable. | $0 = \sum_{t=0}^{T} \frac{C_t}{(1 + IRR)^t}$ |
| **Payback Period** | Time for cumulative cashflow to recover initial investment. | <div style="min-width: 300px">$T_{pb}=\min \{T \; \| \sum_t^{T} \frac{C_t}{(1+r)^k} \geq 0 \}$</div> |
| **Profitability Index** | Like ROI but with time discounting. <br> ✅ PI > 1 → project is profitable. | $PI=1+\frac{NPV}{\text{Initial Investment}}$ |

</v-clicks>

---
layout: center
---

# PF metrics in summary

<div class="text-xl space-y-6">
<v-clicks>

<div>
<p><strong>Profitable</strong></p>
<div class="p-4 border-2 rounded-lg bg-white shadow">
$$
PI > 1 \;\;\;\;\; \Longleftrightarrow \;\;\;\;\; NPV > 0 \;\;\;\;\; \Longleftrightarrow \;\;\;\;\; IRR > \text{Cost of Capital}
$$
</div>
</div>

<div>
<p><strong>Breakeven</strong></p>
<div class="p-4 border-2 rounded-lg bg-white shadow">
$$
PI = 1 \;\;\;\;\; \Longleftrightarrow \;\;\;\;\; NPV = 0 \;\;\;\;\; \Longleftrightarrow \;\;\;\;\; IRR = \text{Cost of Capital}
$$
</div>
</div>

</v-clicks>
</div>

---
layout: image-right
image: https://images.unsplash.com/photo-1594389615321-4f50c5d7878c?q=80&w=1740&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D
---

# Cashflows for wind power project

<!-- helper: overlay normal+bold so width stays identical -->
<style>
.swap { display: inline-grid; }
.swap > * { grid-area: 1 / 1; }
</style>

### Capital expenditurs (CapEx)
- Development costs
- Hardware costs

<br>

### Revenues
- <span class="swap">
    <span v-click.hide="1">Power production sales</span>
    <span v-click="1" class="font-bold">Power production sales</span>
  </span>
- <span class="swap">
    <span v-click.hide="1">Flex sales</span>
    <span v-click="1" class="font-bold">Flex sales</span>
  </span>

<br>

### Operating expenditurs (OpEx)
- Land use
- Grid costs
- <span class="swap">
    <span v-click.hide="1">Operation and maintenance</span>
    <span v-click="1" class="font-bold">Operation and maintenance</span>
  </span>
- <span class="swap">
    <span v-click.hide="1">Imbalance costs</span>
    <span v-click="1" class="font-bold">Imbalance costs</span>
  </span>

---
transition: none
class: text-center
layout: center
---

$\huge R_{total} = R_{DA}+R_{ID}+R_B+R_F$

---
layout: cover
transition: none
css: ./no-transitions.css
background: https://images.unsplash.com/photo-1662332510287-d0163ac55a1f?q=80&w=870&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D
class: text-center
---

# How do you measure performance (KPIs)?

---
layout: cover
background: https://images.unsplash.com/photo-1662332510287-d0163ac55a1f?q=80&w=870&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D
class: text-center
transition: fade
---

$\Huge P_{out} = P_{in} \times \eta_1 \times \eta_2 \times \eta_3$

---
transition: fade-out
---

# Approach

<div class="space-y-8">
  <h2 v-click>1) "What if things were perfect?" or "How much better than?"</h2>
  <h2 v-click>2) Compare baseline to actual in every step of the chain.</h2>
  <h2 v-click>3) Compare with other projects and time frames to identify improvements.</h2>
</div>


---
layout: default
---


<!--
We can isolate performance by comparing to an ideal case at different stages of the value chain. 
-->

<v-clicks>

| Step | Definition | Equation |
|---|---|---|
| **Wind site** | How good is our wind site given no wake effects? | $\eta_{site} = \frac{N_t \cdot P_t(U_i)}{P_{w,i}}$ |
| **Wake** | How good is the wind farm layout? | $\eta_{wake} = \frac{P_f(U_i, \theta_i)}{N_t \cdot P_t(U_i)}$ |
| **Capture rate** | How good is the wind alignment with the market prices? | $\eta_{capture} = \frac{P_{f,i} \cdot S_i}{P_{f,i} \cdot \bar S}$ |
| **Power production** | How good are we at producing given the wind? | $\eta_{production} = \frac{P_{f,i}}{P_f(U_i, \theta_i)}$ | 
| **Dayahead trading** | How good are we at trading in dayahead market?  | $\eta_{DA} = \frac{R_{DA}+R_B}{P_{f,i} \cdot S_i}$ |
| **Intraday trading** | How good are we at trading in intraday markets? | $\eta_{ID} = \frac{R_{DA}+R_{ID}+R_B}{R_{DA}+R_B}$ |
| **Flex trading** | How good are we at trading in flex markets? | $\eta_F = \frac{R_{DA}+R_{ID}+R_F+R_B}{R_{DA}+R_{ID}+R_B}$ |

</v-clicks>


<!--
Power production can include availability and maintenance (not necessarily the same). 
-->

---
transition: none
css: ./no-transitions.css
class: text-center
layout: center
---
<div class="eqbox">

$R_{total} = \sum_i P_{w,i} \times \eta_{site,i} \times \eta_{wake,i} \times \eta_{capture,i} \times \bar S \times \eta_{production,i} \times \eta_{DA,i} \times \eta_{ID,i} \times \eta_{F,i}$

</div>

<style>
.eqbox {
  display: inline-block;
  border: 3px solid black;   /* thickness */
  padding: 12px 16px;        /* space around */
  border-radius: 6px;        /* optional rounded corners */
  background: white;         /* keeps it clean */
}
</style>

---
transition: none
css: ./no-transitions.css
class: text-center
layout: center
---

<div class="eqbox">

$R_{total} = \sum_i \underbrace{P_{w,i} \times \eta_{site.i} \times \eta_{wake,i} \times \eta_{capture,i} \times \bar S}_{\text{outside control}} \times \underbrace{\eta_{production,i} \times \eta_{DA,i} \times \eta_{ID,i} \times \eta_{F,i}}_{\text{inside control}}$

</div>

<style>
.eqbox {
  display: inline-block;
  border: 3px solid black;   /* thickness */
  padding: 12px 16px;        /* space around */
  border-radius: 6px;        /* optional rounded corners */
  background: white;         /* keeps it clean */
}
</style>

---
transition: none
css: ./no-transitions.css
class: text-center
layout: center
---

<div class="eqbox">

$R_{total} = \sum_i \underbrace{P_{w,i} \times \eta_{site,i} \times \eta_{wake,i} \times \eta_{capture,i} \times \bar S}_{\text{outside control}} \times \underbrace{\eta_{production,i} \times \eta_{DA,i} \times \eta_{ID,i} \times \eta_{F,i}}_{\text{inside control}} = \\ \ \\=R_{DA}+R_{ID}+R_F+R_B$

</div>

<style>
.eqbox {
  display: inline-block;
  border: 3px solid black;   /* thickness */
  padding: 12px 16px;        /* space around */
  border-radius: 6px;        /* optional rounded corners */
  background: white;         /* keeps it clean */
}
</style>

---

# Total revenue from wind farm (illustrative)

<div id="waterfall" style="width:100%; height:400px;"></div>

<script setup>
import { onMounted } from 'vue'

onMounted(() => {
  const script = document.createElement('script')
  script.src = 'https://cdn.plot.ly/plotly-latest.min.js'
  script.onload = () => {
    const data = [{
      type: "waterfall",
      x: ["Average capture", "Perfect spot", "Production", "DA trading", "ID trading", "Flex trading"],
      y: [100, -35, -8, -20, 4, 2],
    }]
    const layout = {
      margin: { t: 0, r: 20, b: 40, l: 40 }
    }
    window.Plotly.newPlot('waterfall', data, layout, {
  displayModeBar: false   // completely hide the toolbar
    })
  }
  document.body.appendChild(script)
})
</script>

---

# How to improve KPIs? 

<div class="space-y-8">
  <h2 v-click>1) Using a "perfect vs actual" approach also for ID and Flex trading?</h2>
  <h2 v-click>2) Include more aspects of the chain like availability/maintenance and merchant exposure vs bilateral (PPAs) trading?</h2>
  <h2 v-click>3) KPIs for hybrid parks?</h2>
</div>

---
transition: none
class: text-center
layout: center
---

# Thanks!