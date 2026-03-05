# LSS Supply Chain Knowledge Base

**Purpose:** Reference knowledge base synthesized from Lean Six Sigma and Supply Chain training materials.  
**Sources:** ~48 documents (PowerPoints, PDFs, Word docs) processed from training library.  
**Last Updated:** 2026-03-03

## Pre-flight Checklist

Before starting any supply chain analysis, answer these 5 questions:

1. **What type of problem is this?** Strategic / Operational / Tactical — which level?
2. **What data is available?** Quantitative, qualitative, anecdotal? How reliable?
3. **What decision needs to be made?** If no decision follows from this, why are we analyzing it?
4. **What is the time horizon?** Short-term fix, quarterly plan, or multi-year strategy?
5. **Which framework is most relevant?** APICS/CPIM, Gartner, LSS — or a hybrid?

> Mismatching time horizon and framework is the #1 cause of off-target SC analysis.

---


---

## Table of Contents

1. [Lean Six Sigma Foundations](#1-lean-six-sigma-foundations)
2. [Statistical Tools & Methods](#2-statistical-tools--methods)
3. [LSS in Supply Chain](#3-lss-in-supply-chain)
4. [Supply Chain Specific Content](#4-supply-chain-specific-content)
5. [Key Frameworks & Templates](#5-key-frameworks--templates)
6. [Application Rules](#6-application-rules)

---

## 1. Lean Six Sigma Foundations

*Sources: D02 Intro to Lean Six Sigma, D03 Define, D04 VSM, D05 5S, D06 SMED, D07 Flow, D08 Kanban, D09 Mistake Proofing, D10 Measure, D11 Analyze, D12 Improve, D13 Control, D14 Non-Mfg Lean*


### 1.1 What is Lean Six Sigma?

Lean Six Sigma (LSS) is the integration of two complementary improvement methodologies:

**Lean** — Focuses on eliminating waste (non-value-added activities) and improving flow. Derived from the Toyota Production System (TPS).  
**Six Sigma** — Focuses on reducing process variation and defects using data-driven methods. Target: fewer than 3.4 defects per million opportunities (DPMO).

**Combined goal:** Deliver value to customers faster, cheaper, and with higher quality by reducing waste AND variation simultaneously.

**Key concept — Value:** Anything the customer is willing to pay for. Everything else is waste.

**Sigma Levels:**
| Sigma Level | DPMO | Yield |
|-------------|------|-------|
| 1σ | 691,462 | 30.9% |
| 2σ | 308,538 | 69.1% |
| 3σ | 66,807 | 93.3% |
| 4σ | 6,210 | 99.4% |
| 5σ | 233 | 99.977% |
| 6σ | 3.4 | 99.9997% |


### 1.2 DMAIC — Define, Measure, Analyze, Improve, Control

DMAIC is the core Six Sigma problem-solving methodology for **improving existing processes**.

**DEFINE**
- Identify the problem, customer requirements, and project scope
- Tools: Project Charter, VOC (Voice of Customer), SIPOC, CTQ Tree, Value Stream Map (current state)
- Output: Defined problem statement, project scope, team, timeline

**MEASURE**
- Establish baseline performance; quantify the problem
- Tools: Data collection plan, MSA/Gage R&R, control charts (baseline), process capability (Cp, Cpk), DPMO calculation
- Output: Validated measurement system, baseline sigma level, process map with data

**ANALYZE**
- Identify root causes of defects/variation
- Tools: Fishbone (Ishikawa), 5 Whys, Pareto, hypothesis testing, regression, ANOVA, scatter plots, FMEA
- Output: Validated root causes with data evidence

**IMPROVE**
- Develop, pilot, and implement solutions to root causes
- Tools: Brainstorming, DOE (Design of Experiments), solution selection matrix, pilot plan, mistake-proofing (Poka-Yoke)
- Output: Implemented solution with demonstrated improvement

**CONTROL**
- Sustain improvements; prevent regression
- Tools: Control charts (ongoing), control plan, SOPs, mistake-proofing, visual controls, response plan
- Output: Control plan, trained operators, handoff to process owner


### 1.3 DMADV — Define, Measure, Analyze, Design, Verify

DMADV (also called DFSS — Design for Six Sigma) is used when **designing new processes or products** from scratch, or when existing processes are so broken that redesign is needed rather than improvement.

**DEFINE:** Project goals, customer needs, CTQs  
**MEASURE:** Customer specifications, benchmarks, product capabilities  
**ANALYZE:** Process design options; identify best design concept  
**DESIGN:** Develop detailed design, pilot  
**VERIFY:** Test design performance; validate against CTQs  


### 1.4 The 8 Wastes (DOWNTIME / TIM WOODS)

Lean identifies 8 types of waste (non-value-added activities). Remembered by acronym **DOWNTIME**:

| Waste | Description | Supply Chain Example |
|-------|-------------|----------------------|
| **D**efects | Errors requiring rework or scrapping | Wrong shipment, damaged goods, billing errors |
| **O**verproduction | Making more than needed, sooner than needed | Overordering inventory, excess production runs |
| **W**aiting | People or materials idle between steps | Trucks waiting at dock, orders waiting approval |
| **N**on-utilized talent | Underusing people's skills/knowledge | Drivers doing admin work, analysts doing data entry |
| **T**ransportation | Unnecessary movement of materials | Redundant handling, cross-docking without purpose |
| **I**nventory | Excess inventory beyond what's needed | Dead stock, safety stock above calculated level |
| **M**otion | Unnecessary movement of people | Warehouse picker travel, office searches for info |
| **E**xtra processing | Doing more work than customer requires | Redundant reports, over-packaging, multiple approvals |

**Original TPS 7 wastes** (Muda): Transportation, Inventory, Motion, Waiting, Overproduction, Overprocessing, Defects (TIM WOOD).


### 1.5 Value Stream Mapping (VSM)

Value Stream Mapping (VSM) is a Lean tool for visualizing the **entire flow** of materials and information from supplier to customer. Used to identify waste and design the future state.

**VSM Process:**
1. Select a product family
2. Draw **current state** map (walk the process; collect actual data)
3. Analyze: identify waste, bottlenecks, push vs. pull, wait times, inventory locations
4. Design **future state** map (target state)
5. Create implementation plan

**Key VSM metrics collected at each step:**
- Cycle time (C/T) — time to complete one unit
- Change-over time (C/O) — time to switch between products  
- Uptime (% available)
- Number of operators
- Inventory (# pieces or days)

**VSM symbols:**
- Boxes = process steps
- Triangles = inventory accumulation
- Push arrow = material pushed regardless of downstream need
- Pull/Kanban arrow = material pulled by downstream demand
- Timeline = alternates between value-added time and wait time

**Information flows:** Shown at top of map. Distinguish customer orders, production schedules, supplier purchase orders.

**Value-Added Time (VAT) vs. Total Lead Time (TLT):** The ratio (VAT/TLT) is typically very low (< 5% in most processes). Improvement opportunity = reduce non-value-added wait time.


### 1.6 5S — Workplace Organization

5S is a systematic approach to workplace organization. Foundation for all Lean improvement.

| S | Japanese | English | Meaning |
|---|----------|---------|---------|
| **S1** | Seiri | Sort | Remove everything not needed; red-tag items |
| **S2** | Seiton | Set in Order | A place for everything; everything in its place |
| **S3** | Seiso | Shine | Clean and inspect; surfaces, equipment, tools |
| **S4** | Seiketsu | Standardize | Create standards for the first 3 S's; visual controls |
| **S5** | Shitsuke | Sustain | Maintain; audit; make 5S a habit |

**Visual Controls:** Make the status of a process visible without asking anyone. Examples:
- Shadow boards (tools)
- Floor tape marking storage locations
- Kanban cards
- Andon lights (red/yellow/green status)
- Color-coded inventory zones

**In Supply Chain / Logistics:**
- Standardized dock layouts
- Labeled storage locations in warehouse
- Visual truck status boards
- Driver documentation organized by route


### 1.7 SMED — Single Minute Exchange of Dies

SMED is a Lean technique for **rapidly reducing changeover/setup time** (target: under 10 minutes = "single digit").

**The SMED Method:**
1. **Observe** current changeover (video if possible)
2. **Separate** Internal vs. External activities:
   - **Internal** = must be done while process is stopped
   - **External** = can be done while process is running
3. **Convert** internal activities to external (move prep work offline)
4. **Streamline** all activities (eliminate, simplify, standardize)
5. **Document** new standard; train; repeat

**SMED in Logistics/Supply Chain:**
- Truck loading/unloading time reduction
- Dock door changeover
- Route planning preparation (done before driver arrives)
- Order processing prep work
- Warehouse shift changeover

**Typical results:** 50-80% reduction in changeover time


### 1.8 Flow and Pull Systems

**Flow** = moving product/information through the value stream without interruption, batching, or waiting.

**Push vs. Pull:**
- **Push:** Produce based on forecast/schedule regardless of downstream demand. Creates inventory buffers.
- **Pull:** Produce/move only when downstream signals a need (Kanban). Reduces inventory and overproduction.

**Little's Law:** Lead Time = Work in Process (WIP) ÷ Throughput Rate  
- To reduce lead time: reduce WIP or increase throughput  
- Batch reduction directly reduces lead time

**Batch size reduction:** Smaller batches = faster flow, less WIP, faster feedback on quality problems. Move toward single-piece flow where possible.

**Takt Time:** Available production time ÷ Customer demand rate. Sets the pace of production to match customer pull.  
Formula: Takt = (Available Work Time per Period) / (Customer Demand per Period)

**Bottleneck identification:** The step with the lowest capacity (longest cycle time relative to takt) constrains system output. Focus improvement there first (Theory of Constraints — TOC).


### 1.9 Kanban

Kanban is a visual pull system for controlling inventory and production flow.

**Kanban Types:**
- **Production Kanban:** Signal to produce a quantity when triggered
- **Withdrawal/Move Kanban:** Signal to move material from one location to another
- **Supplier Kanban:** Signal to replenish from supplier

**Kanban Calculation:**
Number of Kanban cards = (Average Daily Demand × Lead Time × Safety Factor) ÷ Container Size

**Two-bin system:** Simplest kanban. When front bin is empty, use back bin and reorder front bin quantity.

**Electronic Kanban (eKanban):** Digital signals replace physical cards. Common in ERP/WMS systems.

**In Supply Chain:**
- VMI (Vendor Managed Inventory) is a supplier kanban concept
- Min-max inventory levels = simplified kanban logic
- Reorder points in ERP systems implement kanban digitally


### 1.10 Mistake Proofing (Poka-Yoke)

Poka-Yoke (mistake-proofing) prevents defects by designing out the possibility of error.

**Mistake-Proofing Levels (hierarchy, best to worst):**
1. **Elimination** — redesign process to eliminate step where error can occur
2. **Prevention** — design so error is impossible (wrong part won't fit)
3. **Detection at source** — detect error before it passes to next step
4. **Detection at next operation** — catch error before reaching customer
5. **Detection at final inspection** — weakest; errors can escape

**Types of Controls:**
- **Contact methods:** Physical shape, size, weight prevents wrong action
- **Fixed value methods:** Counters, checklists ensure correct quantity
- **Sequence methods:** Steps can only be done in correct order

**In Supply Chain:**
- Barcode scanning at pick/pack (prevents wrong item)
- Weight verification at shipping (catches missing items)
- Electronic BOL pre-population (prevents data entry errors)
- Trailer seal checklists (sequence control)
- Hazmat placarding checklists



---

## 2. Statistical Tools & Methods

*Sources: D10 Measure, D11 Analyze, D13 Control, forecasting.pdf*


### 2.1 Types of Data

**Continuous (Variable) Data:** Measured on a continuous scale. Examples: weight, time, temperature, distance.  
- More information per data point  
- Use: X-bar & R charts, Histograms, Process Capability

**Discrete (Attribute) Data:** Counted. Examples: defect count, pass/fail, on-time/late.  
- Requires larger samples for same statistical power  
- Use: P-charts, C-charts, np-charts, U-charts


### 2.2 Measurement System Analysis (MSA) / Gage R&R

MSA validates that your measurement system is capable before collecting process data.

**Gage R&R (Repeatability & Reproducibility):**
- **Repeatability:** Same operator, same part, same gage — variation due to gage itself
- **Reproducibility:** Different operators, same part, same gage — variation due to operators
- **Part-to-Part:** The variation you actually want to measure

**Acceptability Criteria (% Study Variation or % Tolerance):**
| % R&R | Interpretation |
|-------|----------------|
| < 10% | Excellent — measurement system acceptable |
| 10-30% | Marginal — may be acceptable depending on application |
| > 30% | Unacceptable — measurement system needs improvement |

**Number of Distinct Categories (NDC):** Must be ≥ 5 to effectively distinguish between parts.

**In Supply Chain:** Weigh scales at docks, dimensional scanners, ELD mileage tracking, fuel sensor calibration.


### 2.3 Process Capability

Process capability measures how well a process meets customer specifications.

**Key Indices:**
- **Cp** = (USL - LSL) / (6σ) — Measures potential capability (assumes centered process)
- **Cpk** = min[(USL - μ)/3σ, (μ - LSL)/3σ] — Measures actual capability (accounts for centering)
- **Pp / Ppk** = Same as Cp/Cpk but using overall (long-term) standard deviation

**Benchmarks:**
| Cpk | Interpretation |
|-----|----------------|
| < 1.0 | Incapable — process produces defects |
| 1.0 - 1.33 | Minimally capable |
| 1.33 - 1.67 | Capable (4-5σ) |
| ≥ 1.67 | Highly capable (5-6σ) |

**Supply Chain examples:**
- On-time delivery % → capability against customer window (e.g., ±1 day)
- Order fulfillment accuracy → capability against 100% target
- Transit time consistency → Cp/Cpk on lane transit times


### 2.4 Control Charts

Control charts distinguish between **Common Cause** (normal process variation) and **Special Cause** (assignable, abnormal) variation.

**Control Limits:** Calculated at ±3σ from the mean. NOT specification limits.

**Chart Selection:**
| Data Type | Subgroup Size | Chart |
|-----------|---------------|-------|
| Continuous | n = 1 | I-MR (Individuals & Moving Range) |
| Continuous | 2 ≤ n ≤ 8 | Xbar-R |
| Continuous | n ≥ 9 | Xbar-S |
| Attribute (defectives) | Variable n | P-chart |
| Attribute (defectives) | Constant n | np-chart |
| Attribute (defects/unit) | Variable n | U-chart |
| Attribute (defect count) | Constant area | C-chart |

**Western Electric Rules (Special Cause signals):**
1. One point beyond ±3σ control limits
2. 2 of 3 consecutive points beyond ±2σ
3. 4 of 5 consecutive points beyond ±1σ
4. 8 consecutive points on same side of centerline
5. 6 consecutive points trending up or down
6. 15 points in a row within ±1σ (stratification)

**In Supply Chain:** OTD rates, transit times, damage rates, fuel consumption, order cycle time.


### 2.5 Hypothesis Testing

Hypothesis testing uses data to make statistically valid decisions about process differences.

**Structure:**
- **Null Hypothesis (H₀):** No difference / no effect (default position)
- **Alternative Hypothesis (H₁):** There IS a difference/effect

**Key Concepts:**
- **α (alpha):** Significance level — probability of wrongly rejecting H₀ (Type I error). Typically 0.05.
- **p-value:** Probability of observing results as extreme as the data if H₀ is true. If p < α → reject H₀.
- **β (beta):** Probability of failing to reject a false H₀ (Type II error). Power = 1 - β.

**Test Selection Guide:**
| Question | Data Type | Test |
|----------|-----------|------|
| Is mean different from target? | Continuous | 1-sample t-test |
| Are two means different? | Continuous | 2-sample t-test |
| Are multiple means different? | Continuous | ANOVA (One-way) |
| Is proportion different from target? | Discrete | 1-proportion test |
| Are two proportions different? | Discrete | 2-proportion test |
| Are two variables related? | Continuous | Correlation / Regression |
| Is there distribution difference? | Any | Chi-square |

**Null Hypothesis Key (from training materials):**
- H₀: μ₁ = μ₂ (two means are equal)
- H₀: σ₁² = σ₂² (two variances are equal)
- H₀: ρ = 0 (no correlation)
- Decision rule: p < 0.05 → Reject H₀; conclude difference is statistically significant


### 2.6 ANOVA (Analysis of Variance)

ANOVA tests whether means of 3+ groups are statistically different.

**One-Way ANOVA:** One factor (e.g., compare transit times across 3 carriers)  
**Two-Way ANOVA:** Two factors simultaneously (e.g., carrier × lane)  
**ANOVA with interactions:** Tests whether factor effects depend on each other

**F-statistic:** Ratio of between-group variance to within-group variance. High F → more likely groups differ.  
**p-value < 0.05 → At least one group mean is significantly different.**

**Follow-up:** If ANOVA is significant, use Tukey's HSD or Bonferroni post-hoc to identify which pairs differ.

**Supply Chain use:** Carrier performance comparison, warehouse productivity by shift, lane cost differences.


### 2.7 Regression Analysis

Regression quantifies the relationship between input variables (X's) and output variable (Y).

**Simple Linear Regression:** Y = β₀ + β₁X + ε  
**Multiple Regression:** Y = β₀ + β₁X₁ + β₂X₂ + ... + ε  

**Key Statistics:**
- **R²:** Proportion of variation in Y explained by X's. R² = 0.75 → model explains 75% of variation.
- **Adjusted R²:** Penalizes for adding non-significant predictors.
- **p-value for coefficients:** Is each predictor statistically significant?
- **Residual analysis:** Check for patterns — curved residuals suggest non-linear relationship.

**Supply Chain applications:**
- Fuel cost vs. mileage + load weight
- Transit time vs. distance + weather + carrier
- Damage rate vs. load type + handling frequency
- Inventory turns vs. forecast error + lead time variability


### 2.8 Design of Experiments (DOE)

DOE systematically varies multiple input factors to understand their effects on output.

**Key Designs:**
- **Full Factorial:** All combinations of all factors — most information, most expensive
- **Fractional Factorial:** Subset of combinations — efficient screening
- **Response Surface:** Optimizes a continuous response variable
- **Taguchi:** Robust design against noise factors

**Terminology:**
- **Factor:** Input variable being tested (e.g., carrier, route, warehouse)
- **Level:** Value of the factor (e.g., Carrier A vs. B)
- **Response:** Output being measured (e.g., transit time)
- **Main Effect:** Effect of a single factor on response
- **Interaction:** Effect of one factor depends on level of another

**When to use DOE vs. OFAT (One Factor at a Time):**
- DOE detects interactions; OFAT cannot
- DOE is more efficient for multiple factors
- Use OFAT only when factors are truly independent and few in number


### 2.9 Forecasting Methods

**Qualitative Methods (no historical data):**
- Delphi method (expert panel)
- Market research
- Historical analogy

**Quantitative Methods:**

**Time Series:**
- **Naive:** Next period = last period
- **Moving Average:** Average of last N periods. Simple smoothing.
- **Weighted Moving Average:** More weight to recent periods
- **Exponential Smoothing (SES):** F(t+1) = α·A(t) + (1-α)·F(t). α = smoothing constant (0-1)
  - High α = more responsive to recent data (more volatile)
  - Low α = smoother, slower to react
- **Holt's (Double Exponential):** Adds trend component
- **Holt-Winters (Triple Exponential):** Adds trend + seasonality
- **ARIMA:** Autoregressive Integrated Moving Average — powerful statistical model for complex time series

**Causal/Regression Methods:**
- Demand forecasted as function of leading indicators (economic index, orders, weather)
- Multiple regression forecasting

**Forecast Error Metrics:**
- **MAD (Mean Absolute Deviation):** Average |actual - forecast|
- **MSE (Mean Square Error):** Average of squared errors — penalizes large errors
- **MAPE (Mean Absolute Percentage Error):** MAD as % of actual — good for comparison across products
- **Tracking Signal:** Cumulative error / MAD — detects forecast bias. Target: -4 to +4

**Supply Chain Forecasting Hierarchy:**
- Aggregate → family → SKU level
- Consensus process: Sales + Operations + Finance alignment (S&OP)
- CPFR (Collaborative Planning, Forecasting & Replenishment) with customers/suppliers



---

## 3. LSS in Supply Chain

*Sources: D14 Non-Mfg Lean, Supply Chain Management.pptx, Warehouse Optimization, manh-demand-chain-optimization*


### 3.1 Applying Lean to Non-Manufacturing / Service / Supply Chain

Lean was originally designed for manufacturing but applies directly to supply chain and service environments.

**Key adaptation principles:**
- "Product" in SC = order, shipment, information, or decision
- "Machine" = a process step (order entry, route planning, loading)
- "Inventory" = orders in queue, shipments in transit, information waiting action
- "Defect" = late shipment, wrong delivery, damaged goods, billing error

**Where Lean tools apply in logistics:**

| Lean Tool | SC Application |
|-----------|---------------|
| VSM | Map order-to-cash, tender-to-deliver, quote-to-bill |
| 5S | Dock layout, driver check-in area, dispatch office |
| SMED | Truck turn time, dock door changeover, shift handoff |
| Kanban | Reorder triggers, driver assignment, load board |
| Poka-Yoke | Barcode scan at loading, pre-trip checklist, ELD alerts |
| Flow/Pull | Load sequencing, wave picking, just-in-time delivery |
| Standard Work | Driver SOPs, dock procedures, order entry protocols |

**LSS Project Selection in SC:** Focus on high-volume, high-cost, high-defect-rate processes:
- On-time delivery improvement
- Freight damage reduction
- Order accuracy improvement
- Invoice accuracy / billing cycle time
- Carrier/lane cost reduction


### 3.2 Transportation & Logistics Improvement

**Key metrics to improve using LSS:**
- **OTD (On-Time Delivery):** % shipments delivered within customer window
- **Transit Time:** Mean and standard deviation by lane — consistency matters as much as speed
- **Freight Cost per Mile / per CWT / per Shipment**
- **Truck Utilization:** Load factor, empty miles %, cube utilization
- **Dock-to-Dock Time:** Total time asset is engaged per load
- **Turn Time:** Time from arrival to departure at facility
- **Damage Rate:** % shipments with damage claims

**Common root causes (from LSS analysis in transport):**
- Route suboptimization → excess mileage (Waste: Transportation)
- Wait time at shipper/receiver → driver and asset idle time (Waste: Waiting)
- Appointment scheduling gaps → bunching at docks (Waste: Waiting, Overprocessing)
- Manual tender processes → delays in load assignment (Waste: Motion, Waiting)
- Inaccurate weight/cube data → carrier rejections, re-tendering (Waste: Defects)

**Improvement tools:**
- TMS (Transportation Management System) — automated tendering, routing, track/trace
- Lane performance scorecards — Cpk by carrier/lane
- Driver time-at-facility analysis — identify outlier shippers/receivers
- Fuel consumption regression modeling (mileage, weight, terrain, driver behavior)


### 3.3 Inventory Management Using LSS

**Core inventory concepts:**

**EOQ (Economic Order Quantity):**  
EOQ = √(2·D·S / H)  
Where: D = annual demand, S = ordering cost per order, H = holding cost per unit per year

**Reorder Point (ROP):**  
ROP = (Average Daily Demand × Lead Time) + Safety Stock

**Safety Stock:**  
Safety Stock = Z × σ_demand × √Lead Time  
Where: Z = service level factor (Z=1.65 for 95%, Z=2.05 for 98%, Z=2.33 for 99%)

**ABC Analysis:** Classify inventory by value (A=top 20% of items = ~80% of value; B=next 30%; C=bottom 50%)  
**XYZ Analysis:** Classify by demand variability (X=stable, Y=variable, Z=irregular/lumpy)  
**ABC-XYZ Matrix:** Combined classification drives service level and replenishment strategy per SKU class

**DII (Days of Inventory on Hand):**  
DII = (Average Inventory Value / Annual COGS) × 365

**Inventory Turns:**  
Turns = Annual COGS / Average Inventory Value

**Lot Sizing Techniques:**
- Fixed Order Quantity (FOQ)
- Lot for Lot (L4L) — order exactly what's needed per period
- Period Order Quantity (POQ) — order to cover N periods
- Wagner-Whitin algorithm — optimal dynamic lot sizing

**Excess Stock / Obsolete Inventory:**
- Excess = inventory above maximum desired level (demand × coverage horizon)
- Identification: compare current stock vs. projected consumption
- Resolution strategies: promotions, transfers, write-downs, supplier returns


### 3.4 Warehouse Optimization

**Key warehouse metrics:**
- Order fulfillment accuracy
- Pick productivity (lines/hour)
- Storage utilization (% of capacity)
- Inbound/outbound throughput
- Put-away and retrieval time

**Lean warehouse improvement areas:**

**Slotting optimization:**
- Place high-velocity (A-items) near shipping docks
- Ergonomic placement (best picking height for high-frequency items)
- Reduce picker travel distance — primary driver of non-value-added motion

**Flow design:**
- U-shaped layout vs. straight-through: U-shape typically better for small operations; straight-through for high throughput
- Cross-docking: eliminate put-away/storage for flow-through freight
- Zone picking, batch picking, wave picking to optimize labor

**Warehouse DMAIC example:**
- **Define:** Reduce order pick errors (currently 0.8%, target < 0.2%)
- **Measure:** Track errors by picker, SKU, time of day, location
- **Analyze:** Pareto of errors — top 20% of SKUs drive 80% of errors; 3rd shift has 2× error rate
- **Improve:** Add barcode scan verification, improve lighting in problem zones, targeted training
- **Control:** SPC chart on daily error rate; response plan when control limits exceeded



---

## 4. Supply Chain Specific Content

*Sources: Supply Chain Management.pptx, 4PL-White-Paper, Resilinc SCRP, Risk and Gain Sharing, Shippers Port Selection, EBook SCD, manh demand chain, Accenture Shell Logistics, Warehouse Optimization*


### 4.1 Supply Chain Strategy Frameworks

**Supply Chain Strategic Objectives:**
- Cost efficiency
- Service reliability / responsiveness
- Risk resilience
- Sustainability

**Porter's Value Chain:** Primary activities (inbound logistics, operations, outbound logistics, marketing/sales, service) + Support activities. SC spans multiple companies' value chains.

**SCOR Model (Supply Chain Operations Reference):**
- Plan → Source → Make → Deliver → Return → Enable
- Five levels of process detail
- Standardized metrics at each level (performance attributes: reliability, responsiveness, agility, cost, assets)

**Supply Chain Network Design considerations:**
- Number and location of DCs (distribution centers)
- Make vs. Buy decisions
- Nearshore vs. offshore sourcing tradeoffs
- Network resilience vs. optimization tradeoff

**Impact of Number of Warehouses on Inventory (Square Root Law):**
When consolidating/expanding warehouses, safety stock scales as:  
New Safety Stock = Old Safety Stock × √(n_new / n_old)  
Where n = number of warehouses serving same demand. Consolidating warehouses significantly reduces total safety stock needed.


### 4.2 3PL, 4PL, and Logistics Service Models

**Logistics Service Provider Tiers:**

| Tier | Description |
|------|-------------|
| **1PL** | Company handles its own logistics |
| **2PL** | Asset-based carrier (trucking, rail, air) |
| **3PL** | Third-Party Logistics: manages logistics on behalf of shipper; may own assets or broker them; provides operational execution |
| **4PL** | Fourth-Party Logistics: lead logistics provider; manages the entire supply chain including 3PLs; typically non-asset; focuses on optimization and visibility |

**4PL Value Proposition** (from white paper):
- Single point of accountability across entire supply chain
- Technology-led optimization across all modes and providers
- Strategic outsourcing of entire logistics function
- Better for complex, global, multi-modal supply chains

**Shell/Accenture 4PL Case:**
- Shell outsourced entire logistics to Accenture-led 4PL solution
- Achieved step-change in performance through network consolidation
- Centralized TMS, standardized KPIs, continuous improvement framework
- Key to success: governance model, data transparency, shared risk/gain

**3PL vs 4PL Selection criteria:**
- Operational complexity
- Asset intensity preference
- Technology capability needs
- Control retention requirements
- Risk tolerance


### 4.3 Supply Chain Risk Management

*Source: Resilinc Ultimate Guide to Supply Chain Risk*

**Supply Chain Risk Categories:**
- **Demand risk:** Forecast error, demand volatility, customer concentration
- **Supply risk:** Supplier failure, capacity constraints, quality issues, single-source dependency
- **Process risk:** Internal operational failures, quality escapes
- **Environmental risk:** Natural disasters, geopolitical events, pandemics
- **Cyber/information risk:** Data breaches, ERP failures, misinformation

**SCRP (Supply Chain Resilience Program) Framework:**
1. **Map** the supply chain — n-tier supplier mapping, geographic concentration
2. **Monitor** risk events — real-time disruption intelligence
3. **Mitigate** proactively — dual sourcing, safety stock, geographic diversification
4. **Respond** — playbooks, crisis command structure, alternative routing
5. **Recover** — speed of recovery as key metric

**Key Risk Metrics:**
- TTFN (Time to First Notice) — how fast you learn of a disruption
- TTFR (Time to First Response)
- TTFK (Time to Full Krisis Recovery)
- Risk Exposure Index = Probability × Impact × Detectability

**Supplier Risk Scoring:**
- Financial health (Dun & Bradstreet scores, financial ratios)
- Geographic concentration (% of spend in high-risk regions)
- Single-source dependency (% of critical components from single supplier)
- Lead time and flexibility

**Business Continuity Planning (BCP):**
- Identify critical supply paths
- Define minimum viable supply requirements
- Establish pre-qualified alternates
- Test via tabletop exercises


### 4.4 Demand Chain Optimization

*Source: Manhattan Associates Demand Chain Optimization white paper*

**Traditional push model problems:**
- Forecast error compounds through supply chain (bullwhip effect)
- Each tier adds safety stock independently
- Response to demand signals is slow (batched orders)

**Demand Chain Optimization principles:**
- Sense actual demand (POS data, RFID, real-time consumption)
- Shape demand (promotions, price, availability)
- Respond with flexible supply
- Collaborate across the network (CPFR)

**Demand Sensing:**
- Use short-range (1-14 day) statistical demand sensing vs. traditional 12-week forecast
- Higher accuracy at SKU-location level
- Triggers faster replenishment adjustments

**Inventory Optimization:**
- Multi-echelon inventory optimization (MEIO): jointly optimize inventory at all tiers
- Better than local optimization at each tier
- Reduces total network inventory while maintaining or improving service

**S&OP (Sales & Operations Planning):**
- Monthly cycle: demand review → supply review → pre-S&OP → executive S&OP
- Aligns commercial plans with supply capability
- Outputs: consensus demand plan, supply plan, financial reconciliation

**SIOP / IBP (Integrated Business Planning):**
- Extended S&OP linking financial plans, strategic plans, and operational plans
- Rolling 18-24 month horizon
- More strategic than traditional S&OP


### 4.5 Risk and Gain Sharing in Logistics

*Source: Risk and Gain Sharing White Paper; White Paper - Coupling Gain Sharing with Risk Sharing*

**Traditional transactional model problems:**
- Adversarial shipper-carrier relationship
- Short-term pricing focus sacrifices service and cost innovation
- Carrier takes all downside risk (volatile rates) → risk premium in pricing
- No incentive for carrier to invest in service improvements

**Gain Sharing model:**
- Carrier and shipper share financial upside from improvements
- Carrier invests in optimization (routing, fuel, asset utilization) with confidence of reward
- Shipper benefits from cost reduction without having to manage it
- Requires: open book costing, trusted relationship, clearly defined metrics

**Risk Sharing model:**
- Shipper absorbs some demand/volume volatility risk
- Carrier provides lower rates in exchange for volume commitment
- Both parties protected from extreme outcomes

**Coupled Risk + Gain Sharing:**
- Most sophisticated model
- Symmetric treatment of downside and upside
- Creates aligned incentives across contract period
- Requires detailed cost modeling and contract structure

**Key implementation requirements:**
- Transparent cost data (fuel, driver wages, maintenance, overhead)
- Agreed performance baseline
- Clear measurement framework
- Governance process for disputes and adjustments
- Multi-year commitment (3-5 years minimum)


### 4.6 Port and Mode Selection

*Source: Shippers Port Selection Decision study*

**Port Selection Decision Factors (ranked by shipper priority):**
1. Port congestion/reliability
2. Cost (port charges, drayage, inland transport)
3. Geographic proximity to origin/destination
4. Service frequency
5. Port facilities and capabilities
6. Relationship/history with port authority
7. Intermodal connectivity

**Mode Selection Framework:**
- **Truckload (TL):** Best for full loads, time-sensitive, point-to-point. Higher cost/mile, fastest.
- **Less-than-Truckload (LTL):** Pooled freight, lower cost for small shipments, more handling = more damage risk.
- **Intermodal (Rail + Truck):** Lower cost for long haul (>500 miles). Slower, less flexible.
- **Air Freight:** Emergency or high-value, low-weight. Very high cost.
- **Ocean:** International. Low cost, high lead time variability.
- **Pipeline:** Liquids/gases only. High volume, low unit cost.

**Total Landed Cost Analysis:** True comparison must include:
- Freight cost
- Drayage and accessorials
- Customs/duties (international)
- Transit time cost (inventory in transit)
- Insurance
- Damage rate × average claim value
- Handling costs


### 4.7 Supplier Relationship Management (SRM)

**SRM Definition:** The systematic process for developing and managing partnerships with suppliers who are critical to business success.

**SRM Segmentation:**
- **Strategic:** Critical, sole/preferred source, high value, long-term partnership
- **Preferred:** Regular business, performance requirements, periodic review
- **Transactional:** Commodity, price-driven, easy to switch

**Key SRM Activities:**
- Supplier scorecarding (cost, quality, delivery, responsiveness)
- Joint business planning for strategic suppliers
- Innovation sharing
- Risk monitoring (financial health, geopolitical)
- Development plans for underperforming suppliers

**Supplier Performance Metrics:**
- OTIF (On-Time In-Full) delivery
- Quality defect rate (PPM — parts per million)
- Cost competitiveness vs. market
- Responsiveness (quote turnaround, issue resolution time)
- Financial stability score

**OVM (Order/Volume Management):**
- Collaborative forecasting with suppliers
- Commitment horizon (frozen zone vs. flexible zone)
- Supplier capacity reservation


### 4.8 Supply Chain Development Planning

*Source: EBook_SCD_Development_Plan*

**Supply Chain Capability Maturity:**
- Stage 1: Reactive — firefighting, no visibility
- Stage 2: Functional Excellence — each function optimized independently
- Stage 3: Internal Integration — end-to-end internal processes connected
- Stage 4: External Integration — linked with customers and suppliers
- Stage 5: Demand-Driven Network — fully synchronized, sensing and responding

**Development Plan Components:**
- Current state assessment (maturity level by domain)
- Gap analysis vs. desired state
- Prioritized initiative roadmap (quick wins → strategic)
- Technology enablement plan
- Talent and capability development
- Governance and metrics framework

**Key Development Areas:**
- Planning capability (demand, supply, S&OP)
- Procurement and sourcing
- Transportation and logistics execution
- Warehousing and distribution
- Reverse logistics
- Technology (TMS, WMS, ERP, visibility platforms)
- Analytics and data



---

## 5. Key Frameworks & Templates

*Sources: D03 Define, project charter templates, SIPOC, fishbone, FMEA from training materials*


### 5.1 Project Charter

The Project Charter is the foundational document for any LSS project. It defines scope, justification, and governance.

**Project Charter Elements:**

| Element | Description |
|---------|-------------|
| **Project Title** | Short descriptive name |
| **Problem Statement** | What is wrong? How do we know? (data-based) — no blame, no solution |
| **Goal Statement** | What is the target? Measurable, time-bound (SMART) |
| **Business Case** | Why does this matter? Financial or strategic impact |
| **Scope** | What is IN and OUT of scope (process start/stop points) |
| **Project Timeline** | Key milestones with dates (DMAIC phases) |
| **Team Members** | Champion, Black Belt, Green Belt, team members, process owner |
| **CTQs** | Critical-to-Quality requirements from customer VOC |
| **Resources Required** | Budget, time commitments |
| **Quick Wins** | Identified early improvements to implement immediately |

**SMART Goals:**
- **S**pecific — clearly defined what will be improved
- **M**easurable — quantified with data
- **A**chievable — realistic given resources
- **R**elevant — aligned to business objectives
- **T**ime-bound — deadline stated

**Example (supply chain):**  
*"Reduce average truck turn time at Company X facility from 4.2 hours to 2.0 hours by December 31, 2026, reducing driver wait costs by approximately $150K annually."*


### 5.2 SIPOC Diagram

SIPOC (Suppliers, Inputs, Process, Outputs, Customers) provides a high-level process view during Define phase.

**SIPOC Structure:**

| Suppliers | Inputs | Process | Outputs | Customers |
|-----------|--------|---------|---------|-----------|
| Who provides inputs? | What goes into the process? | High-level steps (4-7) | What comes out? | Who receives outputs? |

**Example — Freight Tendering Process:**

| Suppliers | Inputs | Process | Outputs | Customers |
|-----------|--------|---------|---------|-----------|
| Customer | Purchase order | 1. Receive order | Tendered load | Carrier |
| TMS | Rate data | 2. Enter into TMS | BOL | Driver |
| Rate guide | Carrier list | 3. Tender to carrier | Tender confirmation | Shipper/Customer |
| Carrier | Acceptance | 4. Confirm capacity | Load details | Operations team |
| | | 5. Assign driver/equipment | | |

**Key rules:**
- Keep process to 5-7 high-level steps — not a detailed flow map
- Used during Define to bound scope, not to analyze
- CTQs (Critical to Quality) are identified from the Customers column


### 5.3 Fishbone Diagram (Ishikawa / Cause & Effect)

The fishbone diagram visually organizes potential causes of a problem by category. Used in Analyze phase.

**Standard categories (6M's for manufacturing):**
- **Man** (People)
- **Machine** (Equipment)
- **Method** (Process)
- **Material**
- **Measurement**
- **Mother Nature** (Environment)

**4P's (for service/transactional — more applicable to SC):**
- **People**
- **Procedures**
- **Plant** (equipment/technology)
- **Policies**

**How to build:**
1. Write the problem (effect) at the "head" of the fish
2. Draw major category "bones"
3. Brainstorm causes for each category
4. For each cause, ask "Why?" to drill down (5 Whys)
5. Circle/vote on most likely root causes
6. Validate with data (Analyze phase tools)

**Example — High Damage Rate on Chemical Tanker Deliveries:**
- People: Driver training gaps, improper connection technique
- Equipment: Worn fittings, non-calibrated gauges
- Method: No standardized loading sequence SOP
- Material: Incompatible hose material, wrong pressure ratings
- Measurement: Pre-trip inspection not verified/recorded
- Environment: Wet docks, poor lighting at night loading


### 5.4 FMEA (Failure Mode and Effects Analysis)

FMEA is a systematic risk analysis tool used in Analyze and Improve phases to identify and prioritize failure risks.

**FMEA Structure:**

| Process Step | Potential Failure Mode | Potential Effect | Severity (S) | Potential Cause | Occurrence (O) | Current Controls | Detection (D) | RPN | Recommended Action |
|---|---|---|---|---|---|---|---|---|---|
| | What can go wrong? | Impact on customer | 1-10 | Why does it occur? | 1-10 | What prevents/detects? | 1-10 | S×O×D | |

**RPN (Risk Priority Number) = Severity × Occurrence × Detection**
- Scale 1-10 for each (10 = worst)
- RPN range: 1-1000
- Prioritize highest RPN items for action
- **No hard cutoff for RPN** — also consider Severity ≥ 9 regardless of RPN

**Key FMEA rules:**
- Detection score reflects **current** controls (not planned)
- High severity with low detection = high priority even if occurrence is low
- After implementing improvements, recalculate RPN to verify reduction

**Supply Chain FMEA examples:**
- Load tendering process
- Carrier onboarding
- Dangerous goods handling
- Warehouse receiving


### 5.5 5 Whys

5 Whys is a simple root cause analysis technique — ask "Why?" iteratively until you reach the fundamental cause.

**Rules:**
- Must be data-driven — don't accept assumptions; verify each "why"
- Keep asking until reaching a process/system cause (not blaming people)
- Often takes more or fewer than 5 iterations
- Can branch (multiple causes at same level)

**Example — Shipment Delivered Late:**
1. Why late? → Driver departed facility 2 hours behind schedule
2. Why departed late? → Load was not ready when driver arrived
3. Why load not ready? → Warehouse didn't receive load building instructions until 30 min before departure
4. Why instructions late? → Order was confirmed in TMS but notification to warehouse failed
5. Why notification failed? → TMS–WMS interface has known bug when order is same-day add

**Root cause:** Software integration bug in TMS-WMS interface for same-day orders.  
**Solution:** Fix integration; add manual backup notification protocol until fixed.


### 5.6 Pareto Analysis

Pareto analysis applies the 80/20 rule to prioritize: 20% of causes typically drive 80% of problems.

**How to build:**
1. Collect defect/problem data by category
2. Calculate frequency and cumulative %
3. Sort descending by frequency
4. Plot bar chart + cumulative line
5. Focus improvement efforts on the "vital few" (left side of chart)

**Supply Chain applications:**
- Damage claims by carrier → focus on top 2-3 carriers
- Late deliveries by lane → focus on top lanes
- Invoice errors by error type → eliminate top error type first
- Inventory excess by product family

**Common mistake:** Pareto by count only — should also do Pareto by cost/impact. A low-frequency problem with high cost per occurrence may warrant attention despite low count.


### 5.7 Control Plan

The Control Plan documents how improved process will be monitored and controlled after DMAIC.

**Control Plan Elements:**

| Process Step | What to Control | How Measured | Sample Size/Freq | Who Monitors | Spec/Target | What to Do If Out of Control |
|---|---|---|---|---|---|---|

**Elements of a complete Control Plan:**
- All critical process inputs (X's) and outputs (Y's)
- Control method for each (SPC chart, checklist, audit, automated alert)
- Response plan for each out-of-control condition
- Ownership assigned (specific role, not "team")
- Review cadence

**Control methods (weakest to strongest):**
1. Procedure/SOP (relies on human compliance)
2. Training (relies on human memory)
3. Checklist / form
4. Visual control
5. SPC / control chart with alerts
6. Automated stop / poka-yoke (strongest)



---

## 6. Application Rules

*How to apply LSS tools to real supply chain problems*


### 6.1 Selecting the Right LSS Project

**Criteria for a good LSS project:**
- **Measurable:** Must have quantifiable current performance and target
- **Scoped appropriately:** Can be completed in 3-6 months (GB) or 6-9 months (BB)
- **Not predetermined solution:** If you already know the answer, it's implementation — not LSS
- **Significant enough:** Justifies the rigor; small problems don't need DMAIC
- **Supported:** Champion engaged, process owner cooperative

**Not a good LSS project if:**
- Solution is already known (just do it)
- Problem is entirely political/organizational behavior
- Requires massive capital before any analysis
- Process is already being eliminated/replaced

**Example good SC projects (from training materials):**
- Reduce truck turn time at customer facilities
- Improve OTD performance on specific lane cluster
- Reduce freight invoice error rate
- Reduce warehouse picking errors
- Optimize safety stock levels to reduce excess without service loss
- Improve carrier onboarding cycle time
- Reduce RFQ-to-award cycle time in procurement


### 6.2 DMAIC Phase Decision Rules

**Define Phase Gates (must have before proceeding to Measure):**
- [ ] Problem statement: data-based, no cause/solution embedded
- [ ] SMART goal established
- [ ] SIPOC completed — scope bounded
- [ ] VOC/CTQs identified
- [ ] Champion signed charter
- [ ] Team assembled

**Measure Phase Gates (before proceeding to Analyze):**
- [ ] MSA completed — measurement system validated (R&R < 30%)
- [ ] Baseline data collected (at minimum 20-30 data points)
- [ ] Process capability (Cp/Cpk) or baseline sigma calculated
- [ ] Current state process map with data
- [ ] Data proves problem is real and measurable

**Analyze Phase Gates (before proceeding to Improve):**
- [ ] Root causes validated with data (not just hypothesized)
- [ ] Hypothesis testing completed where applicable
- [ ] Fishbone/5 Whys narrowed to vital few root causes
- [ ] Pareto confirms which root causes drive majority of problem
- [ ] FMEA completed (risk assessment)

**Improve Phase Gates (before proceeding to Control):**
- [ ] Solutions address validated root causes (traceability)
- [ ] Pilot data shows improvement
- [ ] ROI / benefit quantified
- [ ] Risk analysis of new process (FMEA updated)
- [ ] Implementation plan complete

**Control Phase Gates (project closure):**
- [ ] Control plan in place and owned
- [ ] SPC charts (or equivalent) running
- [ ] SOPs updated and operators trained
- [ ] Response plan for out-of-control conditions
- [ ] Financial benefit validated
- [ ] Lessons learned documented
- [ ] Project handed off to process owner


### 6.3 Matching Statistical Tools to SC Problems

**Problem: Is Carrier A faster than Carrier B on this lane?**
→ 2-sample t-test on transit time (continuous data)
→ If non-normal distribution: Mann-Whitney U test

**Problem: Are all 5 carriers performing the same on OTD?**
→ One-way ANOVA on OTD % (or Kruskal-Wallis if non-normal)

**Problem: Is our damage rate different between warehouses?**
→ 2-proportion test (discrete: damaged / not damaged)

**Problem: What drives freight cost per mile?**
→ Multiple regression (Y = cost/mile; X's = distance, weight, fuel price, carrier, season)

**Problem: Is our OTD measurement system reliable?**
→ Gage R&R / Attribute Agreement Analysis (do different analysts classify the same shipment consistently?)

**Problem: Is our OTD process in statistical control?**
→ P-chart (discrete: on-time / late) or I-MR chart on OTD % by week

**Problem: Is our process capable of meeting the customer's ±2 hour delivery window?**
→ Process capability (Cp/Cpk) on delivery time variance

**Problem: Do weather events affect transit time?**
→ ANOVA (weather category) + Regression (temperature, precipitation as continuous)

**Problem: Which factors most affect fuel consumption?**
→ DOE or Multiple Regression (load weight, route terrain, driver, speed, weather)


### 6.4 Lean vs. Six Sigma — When to Use Which

**Use Lean tools when:**
- The problem is clearly waste-related (waiting, excess motion, overprocessing)
- Root causes are visible through observation (not hidden in variation)
- Quick improvements can be made without extensive data collection
- Process is chaotic and needs structure before measuring
- 5S, SMED, flow, or pull implementation is the primary need

**Use Six Sigma tools when:**
- Problem involves variation (inconsistent results, unpredictable performance)
- Root causes are not obvious — data analysis required
- Customer specifications exist and capability must be measured
- Statistical validation of improvements needed
- Measurement system reliability is in question

**Use both (LSS) when:**
- Complex process with both waste AND variation problems (most SC problems)
- Systematic approach needed across DMAIC
- Problem requires both operational redesign AND statistical validation

**Heuristic:**
- Visible waste → start with Lean tools (often no data needed)
- Hidden variation → start with Six Sigma tools (MSA, baseline capability, hypothesis testing)
- Most real supply chain problems → use both, within DMAIC structure


### 6.5 Common LSS Mistakes in Supply Chain Contexts

1. **Skipping MSA:** Collecting weeks of OTD data before verifying that "on-time" is consistently defined and measured. Different systems, different definitions → meaningless baseline.

2. **Jumping to solutions in Define:** Charter says "implement TMS" instead of defining the problem. LSS is problem-first, solution-last.

3. **Too broad scope:** "Improve supply chain cost" — not a DMAIC project. Scope to a specific process, specific metric, specific improvement target.

4. **Confusing common and special cause variation:** Reacting to every data point (tampering) when process is in control. Control charts prevent this.

5. **Analysis paralysis in Analyze:** Over-collecting data without focus. Use Pareto, 5 Whys, and fishbone to prioritize before running advanced statistics.

6. **Piloting vs. full implementation in Improve:** Skipping pilot and implementing broadly — then failing. Always pilot first.

7. **No Control Plan in Control:** Declaring victory after improvement, handing off without controls. Improvements regress within 6-12 months without control plan.

8. **Over-reliance on averages:** Mean OTD of 94% looks good — but if Cpk is 0.8, the process is regularly generating late shipments in tails. Report variation, not just average.

9. **Ignoring measurement in supply chain:** Carrier-reported on-time vs. customer-reported on-time vs. system-captured on-time can differ significantly. Validate measurement source.

10. **Not closing the loop with the process owner:** LSS team leaves, process owner reverts to old ways. Ownership transfer is a project deliverable.


### 6.6 LSS Roles and Responsibilities

| Role | Responsibility |
|------|---------------|
| **Executive Sponsor** | Sets strategic direction, removes organizational barriers, approves resources |
| **Champion** | Owns the business problem; accountable for results; removes roadblocks; approves charter |
| **Master Black Belt (MBB)** | LSS expert; trains/coaches BBs and GBs; drives program deployment |
| **Black Belt (BB)** | Full-time LSS practitioner; leads complex DMAIC projects; advanced statistical proficiency |
| **Green Belt (GB)** | Part-time LSS practitioner; leads focused DMAIC projects; basic-to-intermediate statistical proficiency |
| **Yellow Belt (YB)** | Team member support; understands LSS basics; participates in project teams |
| **Process Owner** | Owns the process being improved; accepts handoff; maintains control plan |
| **Team Members** | Subject matter experts (SMEs); provide process knowledge; implement changes |

**Belt Project Complexity:**
- Green Belt: 3-6 months, departmental scope, $50K-$250K impact typical
- Black Belt: 6-12 months, cross-functional, $250K+ impact typical
- MBB: Program-level, mentoring BBs, enterprise deployment



---

## Appendix: Source Documents Index

| File | Type | Key Content |
|------|------|-------------|
| D02 Intro to Lean Six Sigma 2014 New.pptx | PPTX | LSS overview, sigma levels, waste, overview of methodology |
| D03 Define 2014 New.pptx | PPTX | Define phase tools: charter, VOC, SIPOC, CTQ |
| D04 Value Stream Mapping 2014 New.pptx | PPTX | VSM methodology, current/future state, metrics |
| D05 5S Visual Controls 2014 New.pptx | PPTX | 5S methodology, visual controls |
| D06 SMED 2014 New.pptx | PPTX | Changeover reduction methodology |
| D07 Understanding Flow 2014 New.pptx | PPTX | Flow principles, takt time, batch reduction |
| D08 Kanban 2014 New.pptx | PPTX | Pull systems, kanban types and calculation |
| D09 Mistake Proofing 2014 New.pptx | PPTX | Poka-yoke hierarchy and examples |
| D10 Measure 2014 New.pptx | PPTX | MSA, Gage R&R, process capability, data collection |
| D11 Analyze 2014 New.pptx | PPTX | Root cause analysis, hypothesis testing, statistical tools |
| D12 Improve 2014 New.pptx | PPTX | Solution development, DOE, pilot planning |
| D13 Control 2014 New.pptx | PPTX | Control charts, control plans, sustaining improvement |
| D14 Non Mfg Uses of Lean 2014 New.pptx | PPTX | Lean in service/SC environments |
| Supply Chain Management.pptx | PPTX | Comprehensive SC management framework |
| Warehouse Optimization Presentation.pptx | PPTX | Warehouse design, metrics, optimization |
| 4PL-White-Paper.pdf | PDF | 4PL model, comparison to 3PL |
| Accenture-Shell-Achieving-Step-Change-Logistics-Prformance.pdf | PDF | Shell 4PL case study |
| EBook_SCD_Development_Plan.pdf | PDF | Supply chain capability maturity model |
| forecasting.pdf | PDF | Forecasting methods, time series, error metrics |
| Impace of number of warehouses on inventory.pdf | PDF | Square root law for inventory consolidation |
| manh-demand-chain-optimization-white-paper-en-us.pdf | PDF | Demand sensing, S&OP, MEIO |
| Resilinc-SCRP-Ultimate-Guide-03-26-2015.pdf | PDF | Supply chain risk management framework |
| Risk and Gain Sharing White Paper.pdf | PDF | Shipper-carrier risk/gain sharing models |
| Shippers Port Selection Decision.pdf | PDF | Port and mode selection framework |
| Sustaining Sustainability_JTRF.pdf | PDF | Sustainability in supply chain |
| White Paper - Coupling Gain Sharing with Risk Sharing.docx | DOCX | Advanced gain/risk sharing model |
| Shippers Port Selection Decision.docx | DOCX | Port selection research (extended) |

---
*Knowledge base built by Thea (OpenClaw agent) — 2026-03-03*
