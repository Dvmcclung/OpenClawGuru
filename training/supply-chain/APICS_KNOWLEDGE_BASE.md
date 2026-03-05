# APICS Supply Chain Knowledge Base
**Source:** APICS instructor materials (CPIM Part 1, CPIM Part 2, CSCP 2018)  
**Compiled:** 2026-03-03  
**Sections:** CPIM Body of Knowledge · CSCP Body of Knowledge · Key Frameworks & Models · Metrics & KPIs · Strategic Concepts · Application Rules


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
1. [CPIM Body of Knowledge](#1-cpim-body-of-knowledge)
2. [CSCP Body of Knowledge](#2-cscp-body-of-knowledge)
3. [Key Frameworks & Models](#3-key-frameworks--models)
4. [Supply Chain Metrics & KPIs](#4-supply-chain-metrics--kpis)
5. [Strategic Concepts](#5-strategic-concepts)
6. [Application Rules](#6-application-rules)

---

## 1. CPIM Body of Knowledge

### 1A. Introduction to Supply Chain Management (Section A)

**Supply Chain Definition**
- Global network of organizations sharing destiny and benefits, synchronizing supply with demand via shared data.
- Core competencies: faster, cheaper, better.
- Supply chain management creates net value, builds competitive infrastructure, synchronizes supply with demand, and enables global performance measurement.

**Six Rights of Logistics**
Right goods · Right quantity · Right quality · Right time · Right place · Right cost

**Manufacturing Environments (by volume and variety)**
| Environment | Description | Inventory Held | Customer Involvement |
|---|---|---|---|
| ETO (Engineer-to-Order) | Unique, high complexity | None until ordered | Extensive |
| MTO (Make-to-Order) | Custom per order | Raw materials | Moderate |
| ATO (Assemble-to-Order) | Modular options | Component/module | Low (picks modules) |
| MTS (Make-to-Stock) | Standard, high volume | Finished goods | Indirect only |

**Hybrid Environments**
- **Mass customization:** Customize at near-same cost as high-volume production.
- **Configure-to-order:** Components made after order (same lead time as MTO).
- **Postponement:** Delay final differentiation to DC or point closer to customer.
- **Package-to-order:** Bulk storage until order triggers packaging.

**Process Types and Layouts**
- **Project:** Unique deliverables; fixed-position layout (workers move, not product).
- **Intermittent (job shop/batch):** Varied routings; functional layout; high WIP, long lead times.
- **Cellular:** U-shaped; reduced queue, smaller lots, immediate feedback, greater flexibility.
- **Flow (line/continuous):** Standardized products; product-based layout; low WIP, short lead times.

**Manufacturing Planning and Control (MPC) Hierarchy**
```
Strategic Plan
  → Business Plan
    → Sales & Operations Plan (S&OP) / Production Plan
      → Master Production Schedule (MPS)
        → Material Requirements Planning (MRP)
          → Production Activity Control (PAC)
```
Capacity checks run in parallel: Resource Planning → RCCP → CRP → Capacity Control

**Lean Philosophy**
- Pull rather than push; only make what customers want.
- Match production rate to demand rate (takt time).
- Zero defects, shortest lead times, no waste.
- House of Toyota: JIT + Jidoka (automation with human intelligence) on foundation of standardization and operational stability.
- **7 Wastes (Muda):** Overproduction, waiting, transport, over-processing, inventory, motion, defects.
- **Jidoka:** Automated line stop on defect; poka-yoke (mistake-proofing); andon (signal lights).
- **Heijunka:** Level scheduling by volume and mix.
- **5Ss:** Sort, Simplify, Scrub, Standardize, Sustain (+ Safety).
- **Kaizen blitz:** Focused improvement event (one week or less).
- **Hoshin planning:** Strategy deployment; align resources, remove obstacles; hansei (mindful reflection).

---

### 1B. Demand Management (Section B)

**Demand Management Processes**
1. Marketing management (4 Ps: Product, Price, Promotion, Place)
2. Customer Relationship Management (CRM) — customer first; builds loyalty
3. Order management (entry, tracking, promising)
4. Demand planning (forecasts, internal/external orders, tracking)

**Types of Demand**
- **Independent demand:** From external sources; must be forecasted; end units or service parts.
- **Dependent demand:** Derived from BOM structure; calculated, not forecasted; components.
- Items can have both (e.g., motorcycle tires sold individually and used in assembly).

**Demand Patterns:** Stable vs. dynamic; seasonality, trend, cycle, random variation.

**Forecasting Process (10 Steps)**
1. Determine purpose
2. Set aggregation level and units of measure
3. Select horizon and planning bucket
4. Gather and visualize data (chart)
5. Choose technique
6. Prepare data (deseasonalize if needed)
7. Test on historical data
8. Forecast
9. Achieve consensus
10. Continuously improve

**Forecasting Methods**
| Method | Type | Best For |
|---|---|---|
| Qualitative (Delphi, expert opinion) | Subjective | New products, long-term, no historical data |
| Extrinsic (leading indicators) | Quantitative | Detecting trend changes, long-term |
| Moving average | Time series | Stable demand, short-term |
| Exponential smoothing | Time series | All near/medium-term; α controls lag vs. smoothing |
| Regression/causal | Quantitative | Correlated relationships |

**Exponential Smoothing Formula:**  
`New Forecast = (α × Last Actual Demand) + ((1 − α) × Last Forecast)`  
- Low α (0.0–0.1): More smoothing, more lag.  
- High α (0.2–0.3): Less smoothing, less lag.

**Seasonal Index**
- Deseasonalize → forecast → multiply by seasonal index.
- Seasonal Index = Average demand for period / Overall average demand.

**Forecast Error Tracking**
- **Deviation:** Actual − Forecast (signed; positives and negatives cancel).
- **MAD (Mean Absolute Deviation):** Average of absolute deviations; measures error magnitude.
- **Tracking Signal:** Cumulative deviation / MAD. Bias detected if tracking signal drifts consistently positive or negative.
- 1 MAD ≈ 80% service level; 2 MAD ≈ 95%; 3 MAD ≈ 99%.

---

### 1C. Master Planning (Section C)

**Sales and Operations Planning (S&OP)**
- Monthly process; links business planning to tactics.
- 5 Steps: Data gathering → Demand planning → Supply planning → Pre-S&OP meeting → Executive meeting.
- Output: Single consensus plan across sales, production, finance, HR.
- Operates at product family level in monthly or weekly buckets.
- Functions: reconciles functional plans, proactive opportunity, defines short-to-medium term, enables replanning.

**Production Strategies**
| Strategy | Description | Advantage | Trade-off |
|---|---|---|---|
| Chase | Production = demand each period | Low inventory cost | High variability in workforce/capacity |
| Level | Produce at average demand | Stable workforce, setups | High inventory holding costs |
| Subcontracting | Minimum internal + outsource peaks | Leveling without added fixed cost | Lower margins, quality risk |
| Hybrid | Custom mix of above | Flexible | Complex planning |

**Production Plan Formula (MTS Level):**  
`Total Production = Total Forecast + Backorders + Ending Inventory − Opening Inventory`

**Master Production Schedule (MPS)**
- Disaggregates production plan (families → end items).
- Planned in weeks; drives MRP.
- Validates capacity via RCCP.

**Projected Available Balance (PAB):**  
`Ending PAB = Beginning PAB + MPS Receipt − Demand (orders or forecast)`  
- Before demand time fence: use customer orders only.
- After demand time fence: use greater of customer orders or forecast.

**Time Fences**
- **Demand time fence (DTF):** Inside = frozen; customer orders dominate.
- **Planning time fence (PTF):** Inside = slushy; master scheduler approves changes.
- **Liquid zone:** Beyond PTF; system can plan freely.

**Available-to-Promise (ATP)**
- First Period ATP = Beginning Inventory − Customer orders before next MPS receipt.
- Subsequent periods: MPS Receipt − Customer orders before next MPS receipt.

---

### 1D. Material Requirements Planning (Section D)

**MRP Purpose**

- Translates independent demand (MPS) into time-phased dependent demand for components.
- Controls: adapt to changing priorities, expedite/de-expedite, cancel or change orders.

**MRP Inputs**
1. Master Production Schedule (MPS)
2. Bill of Material (BOM)
3. Inventory status records (on-hand, on-order, allocated, lead times, lot sizes)

**MRP Logic (Gross-to-Net)**
```
Gross Requirements (from MPS or parent order)
− Scheduled Receipts (open orders due)
− On-Hand Inventory
= Net Requirements
→ Planned Order Receipts (due date)
→ Planned Order Releases (offset by lead time)
```

**Bill of Material (BOM) Types**
- **Single-level:** One parent-child relationship; reusable across products.
- **Multilevel (indented):** Full expansion from end item to purchased components.
- **Planning BOM (modular):** Uses historical percentages of options for ATO planning.
- **Where-used:** Lists all parents using a child (used for engineering changes).
- **Pegging:** Traces gross requirements back to specific parent orders.

**Lead-Time Offset (Offsetting):** Planned order release = due date minus lead time.

**Lot-Sizing Methods**
| Method | Description | Best For |
|---|---|---|
| Lot-for-Lot | Order exactly what's needed | Dependent demand, expensive/perishable items, lean |
| Fixed Order Quantity (FOQ) | Fixed batch size | Volume discounts, efficient production batches |
| Period Order Quantity (POQ) | EOQ expressed as number of periods | Balances ordering and holding |
| EOQ | Mathematically optimal | Independent demand with stable costs |

**Managing MRP**
- **System nervousness:** Frequent, unnecessary replanning cascades. Mitigate with time fences and firm planned orders.
- **Net change vs. regeneration:** Net change is faster; runs continuously.
- **Firm planned order:** Planner-controlled; prevents system from changing it automatically.

---

### 1E. Capacity Management (Section E)

**Capacity Planning Hierarchy**
| Level | Tool | Horizon |
|---|---|---|
| Business plan | Resource Planning (RP) | 15–18 months; long-lead resources |
| S&OP | Rough-Cut Capacity Planning (RCCP) | Medium-term; key resources only |
| MRP | Capacity Requirements Planning (CRP) | Detailed; all work centers |
| Shop floor | Production Activity Control (PAC) | Short-term; daily dispatch |

**Capacity Measurement**
- **Standard hours:** Common unit; includes setup and run time; based on time studies.
- **Rated Capacity:** Available Time × Utilization × Efficiency
  - Available Time = Workers or Equipment × Hours in period
  - Utilization = Hours Worked / Available Hours (accounts for breaks, maintenance)
  - Efficiency = Standard Hours of Work / Hours Worked
- **Demonstrated Capacity:** Historical average actual output × standard hours per item.

**Lead Time Components (SQWM)**
- **Queue:** Waiting to begin (usually largest component).
- **Setup:** Convert from last good item A to first good item B.
- **Run:** Time doing the operation.
- **Wait:** Waiting after operation ends.
- **Move:** Physical movement between operations.

**CRP Process**
1. Calculate available capacity (rated or demonstrated).
2. Back-schedule open and planned orders to create load profiles per work center.
3. Compare load (capacity required) to available capacity.
4. Resolve: adjust capacity first; alter load as fallback.

**Resolving Capacity Imbalances**
- Increase capacity: overtime, hire/lay off, add/remove shifts, subcontract, alternate routing, process improvement.
- Reduce load: alter lot sizes, split orders, change routings, reschedule.

---

### 1F. Purchasing (Section F)

**Types of Purchases**
- Capital expenditures (RFQ process)
- Regular: raw materials, services, MRO supplies
- Direct vs. indirect materials and labor

**Purchasing Objectives**
- **Conventional:** Correct goods, correct quality/quantity, lowest total cost, minimize lead time.
- **SCM objectives:** Invest in supplier partnerships (SRM), supplier certification, CSR/sustainability.

**Purchasing Process**
1. Establish specifications (form, fit, function; quality; quantity; price)
2. Select suppliers (weight and rank: capabilities, location, price, reliability, SC maturity, culture)
3. Negotiate contracts (PO, blanket PO, long-term contract)
4. Manage purchasing cycle (requisition → PO → follow-up → receive → pay)
5. Monitor and control (scorecards, metrics, feedback)

**Supplier Relationship Strategies**
- **Single-source / key suppliers:** Long-term contracts; shared destiny; lean relies on 100% quality.
- **VMI (Vendor-Managed Inventory):** Supplier manages replenishment; can mitigate bullwhip.
- **Consignment:** Supplier retains ownership until used/sold.
- **Continuous replenishment:** Regularly scheduled restocking.

**Supplier Selection Matrix**  
Strategic Impact vs. Supply Risk → determines intensity of collaboration required.
- Low risk / low strategic: transactional.
- High risk / high strategic: partnership.

---

### 1G. Inventory Management (Section G)

**Objectives of Aggregate Inventory Management**
1. Minimize inventory investment (supply chain total, not just internal).
2. Meet targeted customer service level.
3. Maximize manufacturing efficiency (smooth, uninterrupted flow).

**Functions of Inventory**
- Safety stock (protect against demand/supply variability)
- Decoupling inventory (buffers between work centers)
- Anticipation inventory (seasonal buildup)
- Lot-size / cycle stock (due to batch ordering)
- Transportation inventory (in-transit)
- Hedge inventory (against price/supply uncertainty)

**Inventory Costs**
| Cost Category | Components |
|---|---|
| Item cost | Unit price + shipping + taxes |
| Carrying cost | Capital (opportunity cost) + storage + risk (insurance, obsolescence) |
| Ordering cost | PO admin, receiving, setup/teardown, lost capacity |
| Stockout cost | Lost revenue, damaged customer perception |
| Capacity-related | Costs of adjusting capacity |

**Typical carrying cost rate:** 20–30% of inventory value per year.  
`Annual Carrying Cost = Carrying Cost Rate × Average Inventory Value`

**ABC Classification (Pareto Analysis)**
| Class | % of Items | % of Value | Control Level |
|---|---|---|---|
| A | 10–20% | 50–70% | Tight; frequent counting; precise safety stock |
| B | ~20% | ~20–45% | Average controls |
| C | 60–70% | 5–10% | Simple; two-bin, kanban; minimal counting |

**Economic Order Quantity (EOQ)**
```
EOQ = √(2 × Annual Demand (A) × Ordering Cost (S) / (Unit Cost (c) × Carrying Cost Rate (i)))
```
- EOQ is where annual ordering cost = annual carrying cost (total cost minimized).
- Assumptions: constant known demand; full lot arrives at once; costs are known and stable.
- Sensitivity: EOQ is relatively insensitive to small errors in inputs (near-optimal results still good).

**Safety Stock Calculations**
```
Safety Stock = MAD × MAD Safety Factor  (or SD × SD Safety Factor)
```
- 1 MAD ≈ 80% service level; 2 MAD ≈ 95%; 3 MAD ≈ 99%.
- Higher lead time → more safety stock (scales approximately with square root of lead time ratio).
- Reducing safety stock: shorter lead times, better forecasts, more frequent orders, less demand variability.

**Order Point Systems (Independent Demand)**
```
Order Point (OP) = Demand During Lead Time + Safety Stock
DDLT = Average Demand per Period × Lead Time
```
- **Perpetual:** ERP tracks transactions; reorder when OP is reached.
- **Two-bin / kanban:** Visual; reorder when first bin empty; suits C items.

**Periodic Review System:**
```
Target Level (T) = D × (R + L) + Safety Stock
Order Quantity (Q) = T − Current Inventory on Hand
```
Where D = daily demand, R = review period, L = lead time.

**Inventory Accuracy**
- **Cycle counting:** Count A most often, B less, C least; continuous; less disruptive.
- **Wall-to-wall count:** Counts everything at once; requires shutdown.

---

### 1H. Execution and Control (Section H)

**Theory of Constraints (TOC)**
- **Core principle (Goldratt):** Complex systems have a small number of variables limiting output. Only improvement at the constraint creates net gain.
- **Throughput:** Revenue generated per time period.
- **Bottleneck:** Work center at 100% utilization; WIP accumulates upstream; downstream waits.
- **Capacity-Constrained Resource (CCR):** Not always at 100% but close enough to need careful management.

**Five Focusing Steps**
1. **Identify** the constraint.
2. **Exploit** the constraint (maximize its output; minimize setup, preventive maintenance, pre-check inputs).
3. **Subordinate** everything else to the constraint (all other work centers pace to constraint; protective capacity is okay).
4. **Elevate** the constraint (if exploitation isn't enough: more equipment, overtime, outsourcing).
5. **Find the new constraint** and repeat.

**Drum-Buffer-Rope**
- **Drum:** Constraint sets pace (like takt time but constraint-based).
- **Buffer:** Time buffer — materials arrive before needed; allocated to specific future orders.
- **Rope:** Demand-pull signal based on constraint throughput rate; keeps buffer from shrinking or growing.

**Scheduling Methods**
| Method | Direction | Characteristic |
|---|---|---|
| Backward | From due date | Latest start date; minimizes WIP |
| Forward | From earliest date | Earliest finish; may create early WIP |
| Infinite loading | Ignores capacity | Good for planning if capacity is flexible |
| Finite loading | Respects capacity limits | Realistic; requires accurate standard hours |

**Dispatching Rules (Priority Sequencing)**
| Rule | Description |
|---|---|
| FCFS | First come, first served |
| EDD | Earliest job due date |
| ODD | Earliest operation due date |
| SPT | Shortest process time |
| Critical Ratio (CR) | Time remaining / Work remaining; <1 = behind schedule |

**Input/Output Control**
- Monitor actual vs. planned input and output at each work center.
- Backlog = Previous Backlog + Input − Output.
- Control queue times by managing input rate and output rate.

---

### 1I. Physical Distribution (Section I)

**Distribution Objectives**
- Required level of customer service at least total cost.
- Minimize materials handling (minimize number of times handled).
- Maximize turnover (cross-docking).
- Reliable delivery lead times.

**Transportation Modes Comparison**
| Mode | Cost | Speed | Best For |
|---|---|---|---|
| Air | Highest | Fastest (1–2 days) | High-value, time-sensitive, low-density |
| Road (TL) | Medium-low | Fast, flexible | End-to-end, diverse destinations |
| Rail | Low-medium | Medium | Dense, durable, low-value; long-haul |
| Water (ocean) | Lowest | Slowest | Dense, low-value bulk; long-haul |
| Pipeline | Very low (operating) | Continuous | Liquids, slurries; high fixed cost |
| Intermodal | Variable | Medium | Combines modes for line haul |

**TL vs. LTL**
- TL: Lower rate; requires full load; lot-size inventory builds.
- LTL: Higher rate; more terminal handling; suits smaller, diverse shipments.

**Factors Affecting Transportation Rate**
- Density (weight vs. volume), hazardous classification, perishability, fragility.
- Backhaul availability, detention (road) / demurrage (rail/water), expediting.

**Distribution Requirements Planning (DRP)**
- Uses MRP logic applied to distribution network.
- DC planned order releases become gross requirements at central supply / MPS.
- Provides advance visibility for production leveling (push information, pull inventory).
- `Net Requirements (with Safety Stock) = Gross Requirements − (Prior Projected Available − Safety Stock)`

**Push vs. Pull Distribution**
- **Pull:** DCs order independently; autonomous; risk of bullwhip effect; ignores other DCs.
- **Push:** Central allocation; tight inventory control; ignores local demand nuances.
- **DRP Hybrid:** DCs pull but share advance information enabling production leveling.

**Warehousing**
- Value-added functions: break-bulk, freight consolidation, cross-docking, postponement.
- More warehouses: lower transportation costs, shorter lead times, but higher total warehousing cost.
- **Picking methods:** Discrete, batch, wave, zone.
- **Storage systems:** Fixed location (~50% waste at times), floating/random location (WMS-directed, better cube utilization).
- **Public vs. private:** Public = variable cost, flexible; private = lower long-run cost if volume justifies.

**Reverse Logistics**
- Dedicated supply chain for returns, repair, remanufacture, recycling.
- Design 4 Rs into product life cycle: Reduce, Reuse, Recycle, Recover (energy).
- High cost; proactively plan and manage (or outsource to 3PL).

**Global Distribution Complexities**
- Language, culture, holidays, documentation, currency exchange, customs/duties/tariffs.
- Incoterms (2020): define obligations of exporters and importers.
- C-TPAT: Customs-Trade Partnership Against Terrorism; benefits include fewer inspections, risk-assessment factor.
- Free Trade Zones (FTZs): defer duties/taxes; reduce import costs; allows reprocessing.

---

### 1J. Continuous Improvement (Section J)

**Continuous Improvement Commonalities**
- Employee involvement and empowerment (respected, included in decisions).
- Customer as ultimate definer of quality.
- Sustainable; ongoing cycle.

**TQM and Quality Definitions**
- **User-based quality:** Meets customer expectations; features, aesthetics, conformance.
- **Manufacturing-based:** Conformance to requirements; specifications limits.
- **Value-based:** Value for money relative to competition.
- **Reliability, durability, maintainability** are key quality dimensions.

**Cost of Poor Quality**
- Prevention costs (training, design review) + Appraisal costs (inspection) + Internal failure (scrap, rework) + External failure (returns, warranty).
- Not investing in quality is more expensive in the long run.

**Basic 7 Quality Tools (B7)**
1. Check sheets
2. Pareto charts (80–20 rule)
3. Cause-and-effect (Ishikawa/fishbone) diagrams
4. Flowcharts
5. Histograms
6. Scatter diagrams
7. Control charts (SPC)

**Statistical Process Control (SPC)**
- **Specification limits (USL/LSL):** Set by customer/engineering; voice of the customer.
- **Control limits (UCL/LCL):** Set by statistical observation (±3 standard deviations); voice of the process.
- **Common (random) causes:** Inherent variation; process is in control.
- **Assignable (special) causes:** Root cause exists; process out of control; investigate.
- Normal distribution: 1σ = 68.3%, 2σ = 95.4%, 3σ = 99.7%.

**Six Sigma (DMAIC)**
- Goal: No more than 3.4 defects per million opportunities (6σ from mean).
- 1. **Define** — Customer's problem.
- 2. **Measure** — Collect data.
- 3. **Analyze** — Cause-and-effect; root cause of variation.
- 4. **Improve** — Address process variations.
- 5. **Control** — Sustain improvements; standardize; integrate.

**Quality Function Deployment (QFD)**
- Voice of the Customer (VOC) mapped to product/process requirements.
- "House of Quality" matrix manages tradeoffs among competing requirements.

**Value Stream Mapping (VSM)**
- Draw current-state value stream to identify waste (non-value-added steps).
- Draw future-state map as improvement target.
- Distinguish value-added vs. non-value-added time.

---

## 2. CSCP Body of Knowledge

### 2A. Supply Chain Design (Module 1, Section A)

**Business and SC Strategy Alignment**
- Four levels: Business strategy → Organizational strategy → Supply chain strategy → Functional strategies.
- SC strategy must align with competitive priorities: cost, quality, time, flexibility.
- **Value proposition:** Customer service + Quality + Cost, relative to competition.

**Four Types of Competitive Strategies**
1. **Responsiveness:** Agility; niche marketing; safety stocks or close warehouses.
2. **Focus:** Mass vs. niche; standardize or segment.
3. **Innovation:** R&D, time-to-market, time-to-volume.
4. **Cost leadership:** Efficiency, economies of scale.

**Functional Product vs. Innovative Product Supply Chains (Fisher Matrix)**
| Attribute | Functional Products | Innovative Products |
|---|---|---|
| Demand | Predictable, stable | Volatile, uncertain |
| Product life cycle | Long | Short |
| SC focus | Efficiency (low cost) | Responsiveness (agility) |
| Inventory | Minimal, high turns | Buffer capacity + safety stock |
| Supplier selection | Cost, quality | Speed, flexibility, quality |
| Forecast accuracy | High | Low |

**Push-Pull Frontier**
- Demand-driven SC moves push-pull boundary toward supplier.
- Retail pulls from factory (ATO) in demand-driven model.

**Supply Chain Maturity Stages**
1. **Dysfunctional enterprise:** Functional silos, reactive.
2. **Semifunctional enterprise:** Some integration internally.
3. **Integrated enterprise:** Internal + external logistics integration; combined warehousing/transportation.
4. **Extended enterprise:** Full SC collaboration; shared data, strategy, and risk.

**Stakeholder Value Creation**
- Financial value: net gains, ROI, reinvest in infrastructure.
- Customer value: invest resources in what matters most to market.
- Social value: CSR, UN Global Compact (10 Principles: human rights, labor, environment, anti-corruption).

**Three Vs of SC Strategy**
- **Velocity:** Speed of flow through SC.
- **Variety:** Breadth of product/service offering.
- **Volume:** Scale of operations.

---

### 2B. Supply Chain Network Design (Module 1, Section B)

**Network Design Considerations**
- Number, location, and capacity of warehouses.
- Plant locations and production levels.
- Transportation modes (plant→warehouse, warehouse→retailer).
- Inventory location, optimal levels, customer service balance.

**Product Design Methods**
| Method | Description |
|---|---|
| Standardization / Component commonality | Shared components across products; reduces cost, less flexibility |
| Universality | One design for multiple markets ("one size fits all") |
| Modularization | Modules combined in different ways; enables postponement |
| Mass customization | High-variety at near-mass production cost |
| Postponement | Delay differentiation until late in supply chain |
| Design for Logistics (DFL) | Design product to minimize shipping/handling cost |
| Design for Manufacture and Assembly (DFMA) | Simplify manufacturing; reduce parts count |
| Concurrent engineering | Cross-functional design team; reduces rework, time-to-market |
| Design for Six Sigma | Build quality into design from start |

**Collaborative Design Benefits**
- Fewer cost overruns; improved customer satisfaction; faster to market; higher quality.

**Supply Chain Configuration: Efficient vs. Responsive**
| | Efficient SC | Responsive SC |
|---|---|---|
| Product type | Functional | Innovative |
| Strategy | Make-to-stock | Make-to-order or ATO |
| Demand | Stable, predictable | Volatile, uncertain |
| Primary goal | Low cost, high utilization | Speed, flexibility |

---

### 2C. Technology Design (Module 1, Section B, Chapter 3)

**IT Role in Supply Chain**
- Replace push with pull; avoid bullwhip effect.
- Data entered once; data accuracy; straight-through processing (remove "friction").
- Share knowledge with SC partners; global visibility; SC velocity and agility.

**ERP Systems**
- "Framework for organizing, defining, and standardizing business processes to effectively plan and control an organization."
- Modularized suite; automated interactions; common data source.
- Modules: Sales/Order Management, Finance, HR, Purchasing, MRP/MPS/S&OP, Shop Floor Control, Inventory/WMS.
- ERP vs. best-of-breed: ERP = simpler integration, lower TCO; best-of-breed = faster innovation, niche expertise.
- Implementation rule: new system should match ≥80% of functionality goals; customize ≤20%.

**Key Technology Applications**
| System | Purpose |
|---|---|
| ERP | Enterprise-wide integration, common data |
| APS (Advanced Planning & Scheduling) | Finite scheduling, constraint-based optimization |
| SCEM (Supply Chain Event Management) | Monitor, alert, simulate, control SC exceptions |
| WMS (Warehouse Management System) | Directed picking/put-away, inventory control, automation |
| TMS (Transportation Management System) | Transportation planning, execution, visibility, cost optimization |
| CRM | Customer relationship and order history management |
| SRM (Supplier Relationship Management) | Supplier performance, scorecards, collaboration |

**SCEM Benefits**
- Faster response to supply/demand changes; exception notices on portable devices.
- Reduced inventories; improved order accuracy; greater labor efficiency; real-time communications.

**TMS Benefits**
- Lower costs (less deadheading, demurrage); collaborative shipping; aggregated volumes.
- Web-based visibility; real-time accurate costs.

**Automatic Identification Technologies**
- Bar codes (UPC, 2D/QR codes) — lightweight, inexpensive.
- RFID (Radio Frequency Identification) — passive or active tags; automated tracking without line-of-sight.
- POS (Point-of-Sale) data — capture at source; replace push with pull; reduce bullwhip.

**Data Communications**
- **EDI:** Electronic data interchange; batch-processed; requires agreed format (PO, ASN, invoice).
- **Web Services / XML:** Open standards; interchangeable building blocks; real-time.
- **SOA (Service-Oriented Architecture):** Assembled from reusable software components.
- **SaaS:** Software as a Service; lower initial cost; vendor-managed updates.
- **Cloud Computing:** Scalable, secure; internal/external clouds; current lack of standardization.

---

### 2D. Operations Planning and Control (Module 2, Section A, Chapter 2)

**Operations Planning Hierarchy**
```
Strategic Plan → Business Plan → S&OP → MPS → MRP → DRP → PAC
           ↑                           ↑         ↑
    Resource Planning              RCCP         CRP
```

**Supply-Demand Strategies and MPS Focus**
| Strategy | MPS Schedules | Typical Use |
|---|---|---|
| MTS | Finished goods | Commodity, high-volume, predictable |
| ATO | Modules/components | Many end-items, few components (computers, vehicles) |
| MTO | Raw materials | Many items, few components; custom |
| ETO | None initially | Unique, engineered products |

**Distribution Requirements Planning (DRP)**
- DRP applies MRP logic to distribution network.
- DCs originate planned orders that aggregate at central supply.
- Evaluated at supplying locations before release to determine actual need and availability.
- Prevents shortages at supplying sites and overstocking at ordering sites.

**Capacity Growth Strategies**
1. One-step lead strategy
2. Stepwise lead strategy (expand before demand)
3. Stepwise lag strategy (expand after demand confirmed)
4. Stepwise overlapping strategy

---

### 2E. Global Supply Chain Considerations (CSCP Module 1, Section C–D)

**Challenges of Global Operations**
- Language, culture, holidays, work ethics, documentation requirements.
- Currency exchange, customs duties, tariffs, quotas.
- Lead time variability; higher safety stock requirements.
- Regulatory compliance (import/export licensing, harmonized system codes).

**Trade Terms and Documentation**
- **Incoterms 2020:** Define exporter/importer obligations; not legally binding unless specified in contract.
- **Bill of Lading (B/L):** Legal contract between shipper and carrier.
- **Advance Ship Notice (ASN):** Electronic notification of shipment details.
- **Customs broker:** Certifies and clears shipments; expertise in changing regulations.
- **Freight forwarder:** Arranges transportation; consolidates shipments.
- **Free Trade Zones (FTZs):** Defer duties; reprocess/repack; avoid quotas; cost-effective storage.
- **Trading blocs (e.g., USMCA):** Reduce trade barriers among member countries.

---

### 2F. Sustainability and Risk Management (CSCP)

**UN Global Compact — 10 Principles**
- Human Rights (2): Support and protect; non-complicity.
- Labor (4): Association, collective bargaining, no forced/child labor, no discrimination.
- Environment (3): Precautionary approach, environmental responsibility, green technologies.
- Anti-Corruption (1): Work against corruption and bribery.

**Supply Chain Risk Management**
- Identify risks: supply disruption, demand volatility, geopolitical, natural disaster, regulatory, technology failure.
- Strategies: diversify suppliers, multi-sourcing, safety stock buffers, dual-sourcing, near-shoring, insurance.
- Build resilience: flexibility, visibility, collaboration, redundancy.
- SC resilience determined primarily by flexibility (not productivity or sameness).

**Sustainability Practices**
- Design for environment (DfE) — minimize environmental impact in product design.
- Reverse logistics — reclaim value; reduce landfill; green returns policy.
- 4 Rs: Reduce, Reuse, Recycle, Recover energy.
- Carbon footprint reduction in transportation (mode selection, load optimization, routing).

---

## 3. Key Frameworks & Models

### 3A. SCOR Model (Supply Chain Operations Reference)
- Standard SC framework with five domains: **Plan, Source, Make, Deliver, Return**.
- Provides standard metrics, processes, and best practices for benchmarking.
- Enables cross-company SC analysis and comparison.

### 3B. Economic Order Quantity (EOQ)
```
EOQ = √(2AS / ci)
Where:
  A = Annual demand (units)
  S = Cost per order ($)
  c = Unit cost ($)
  i = Carrying cost rate (decimal)
```
- Minimizes total of ordering + carrying costs.
- At EOQ: annual ordering cost = annual carrying cost.
- **Sensitivity:** Near-optimal results at ±20% of EOQ; small input errors have minimal impact.
- **Changing EOQ through CI:** Reduce S (ordering cost) → smaller optimal lots; supports lean.

### 3C. Safety Stock Models
**Statistical method:**
```
Safety Stock = σ × Z (service factor)
OR
Safety Stock = MAD × MAD Safety Factor
```
**Safety factors by service level:**
| Service Level | Z (SD) | MAD Factor |
|---|---|---|
| 80% | 0.84 | 1.00 |
| 90% | 1.28 | 1.60 |
| 95% | 1.65 | 2.06 |
| 97% | 2.05 | 2.35 |  
| 99% | 2.33 | 2.91 |

**Adjusting for lead time change:**
```
New SS = Old SS × √(New Lead Time / Old Lead Time)
```

### 3D. Bullwhip Effect
- Demand variability amplifies upstream in supply chain.
- Small changes in consumer demand → large swings in manufacturer/supplier orders.
- Causes: demand signal processing, order batching, price fluctuations, shortage gaming.
- Mitigations: share POS data, VMI, CPFR, reduce batch sizes, reduce lead times, reduce order cycles.

### 3E. S&OP Process (Wallace-Stahl Model)
1. Data gathering (actual vs. plan)
2. Demand planning phase meeting (demand manager chairs)
3. Supply planning phase meeting (production alternatives developed)
4. Pre-S&OP meeting (resolve conflicts before executive meeting)
5. Executive meeting (CEO + executives; consensus plan; communicate to all)

### 3F. Theory of Constraints (TOC) / Drum-Buffer-Rope
- **Goal:** Maximize throughput (revenue per time period).
- **Throughput accounting:** Revenue − Truly variable costs; do not allocate fixed overhead.
- Only constraint improvements yield net system gain.
- **Critical chain:** In projects, the longest sequence of dependent tasks (includes resource contention); protect with buffers.

### 3G. Lean / House of Toyota
```
ROOF: Eliminate Waste (Muda)
PILLAR 1: Just-In-Time          PILLAR 2: Jidoka
  - Takt time                     - Automation with human mind
  - One-piece flow                - Poka-yoke (mistake-proofing)
  - Pull systems (kanban)         - In-station quality control
  - Heijunka (level scheduling)   - Andon (signal lights)
FOUNDATION:
  - Standardized work
  - Total Productive Maintenance (TPM)
  - Operational stability
CENTER: Continuous Improvement (Kaizen) + Respect for People
```

### 3H. Product Life Cycle and SC Design
| Stage | Characteristics | SC Strategy |
|---|---|---|
| Introduction | Low volume, uncertain demand | High responsiveness; buffer capacity |
| Growth | Rising volume, improving forecast | Balance efficiency and responsiveness |
| Maturity | Stable, predictable demand | Efficiency; lean; cost reduction |
| Decline | Falling volume | Phase-out management; reduce inventory risk |

### 3I. ABC Pareto Analysis
- Rank items by annual dollar usage (units × unit cost).
- A items: 10–20% of items = 50–70% of value. Highest control.
- B items: ~20% of items = ~20–45% of value. Average control.
- C items: 60–70% of items = 5–10% of value. Minimal control; two-bin/kanban.

### 3J. Four Lean Tools in Inventory Planning
1. **Value Stream Mapping:** Identify and eliminate waste in material/information flows.
2. **Pull System (Kanban):** Replenish only what is consumed; visual signals.
3. **Reducing Setup/Changeover Time (SMED):** Smaller economic lot sizes; more frequent changeovers.
4. **Total Productive Maintenance (TPM):** Prevent downtime; workers maintain own equipment; uninterrupted flow.

### 3K. Balanced Scorecard
Four perspectives for long-term strategic focus:
1. **Financial Perspective** — Revenue, profit, ROI, cost reduction.
2. **Customer Perspective** — Satisfaction, retention, service levels, market share.
3. **Business Process Perspective** — Quality, cycle time, efficiency, defect rates.
4. **Innovation and Learning Perspective** — Employee development, systems improvement, capability building.

---

## 4. Supply Chain Metrics & KPIs

### 4A. Inventory Metrics
| Metric | Formula | Notes |
|---|---|---|
| Inventory Turnover | Annual COGS / Average Inventory | Higher = more efficient capital use |
| Days of Supply | Inventory on Hand / Average Daily Usage | Lower = less capital tied up |
| Average Inventory | (Beginning + Ending Inventory) / 2 | Used in turnover calculation |
| Fill Rate | Orders filled completely on time / Total orders | Customer service metric |
| Stockout Rate | Stockouts / Total order opportunities | 1 − Fill rate |
| Safety Stock Level | Actual SS / Calculated SS | Alignment check |

**Example inventory turnover:**  
COGS = $15M; Average Inventory = ($2.5M + $2M) / 2 = $2.25M; Turns = 6.67

### 4B. Capacity Metrics
| Metric | Formula |
|---|---|
| Rated Capacity | Available Time × Utilization × Efficiency |
| Utilization | Hours Worked / Available Hours |
| Efficiency | Standard Hours of Work Produced / Actual Hours Worked |
| Demonstrated Capacity | Historical avg output × standard hours per item |
| Throughput | Revenue generated per unit of time (TOC) |
| Critical Ratio (CR) | Time Remaining / Work Remaining |

### 4C. Customer Service Metrics
| Metric | Definition |
|---|---|
| Order fill rate | Perfect orders (complete, on-time, undamaged) / Total orders |
| On-time delivery (OTD) | Shipments delivered by committed date / Total shipments |
| Order cycle time | Elapsed time from order receipt to customer delivery |
| Perfect order rate | Orders with zero defects in all dimensions |
| Customer service ratio | % of demand satisfied from stock without delay |

### 4D. Forecast Accuracy Metrics
| Metric | Formula |
|---|---|
| MAD | Σ |Actual − Forecast| / n |
| MAPE | Σ (|Actual − Forecast| / Actual) / n × 100 |
| Tracking Signal | Cumulative Deviation / MAD |
| Bias | Cumulative (Actual − Forecast) / n |

### 4E. Financial SC Metrics
| Metric | Description |
|---|---|
| Total Cost of Ownership (TCO) | Purchase price + logistics + quality + support + end-of-life costs |
| Landed cost | Product cost + logistics costs to point of receipt |
| Cash-to-cash cycle time | Days inventory outstanding + days sales outstanding − days payable outstanding |
| COGS | Direct materials + direct labor + allocated overhead |
| Inventory carrying cost % | (Storage + capital + risk costs) / Inventory value |

### 4F. Transportation Metrics
| Metric | Description |
|---|---|
| Cost per mile / ton-mile | Efficiency of transportation spend |
| On-time pick-up and delivery | Carrier performance |
| Freight cost as % of sales | Overall transportation efficiency |
| Deadhead percentage | Empty miles as % of total miles |
| Load factor | Actual weight or volume / Capacity |

---

## 5. Strategic Concepts

### 5A. Supply Chain Network Design
- **Objectives:** Minimize total cost (transportation + inventory + warehousing + service) while meeting service level targets.
- **Tradeoffs:** More warehouses → lower transport cost, higher warehousing cost, shorter lead times.
- **Factors:** Customer locations, supplier locations, production volumes, lead time requirements, regulatory environment.
- **Tools:** Network modeling, operations research, simulation, linear programming.
- **Configuration options:** Centralized (fewer DCs) vs. decentralized (more DCs closer to customers).

### 5B. Outsourcing and Make vs. Buy
- **Make:** Control, IP protection, flexibility, core competency.
- **Buy/Outsource:** Lower cost (variable vs. fixed), partner specialization, scalability, risk transfer.
- **3PL (Third-Party Logistics):** Outsource logistics functions; expertise, scale, flexibility.
- **4PL:** Manages 3PLs on behalf of shipper; broader SC orchestration.
- Decision framework: Is this a core competency? Is the market competitive? Can quality be specified and monitored?

### 5C. Segmentation Strategies
- **Customer segmentation:** Segment by value, service requirements, geography.
- **Product segmentation:** Functional vs. innovative → different SC designs.
- **Supplier segmentation:** Strategic vs. transactional (Kraljic matrix: profit impact vs. supply risk).
- **Multiple supply chains:** Best practice; different products/customers may need different SCs.

### 5D. Risk Management
- **Risk identification:** Demand risk, supply risk, operational risk, geopolitical, regulatory, financial.
- **Risk assessment:** Probability × Impact.
- **Mitigation strategies:**
  - Diversify suppliers (dual/multi-source).
  - Safety stock buffers for critical items.
  - Geographic diversification (near-shore vs. offshore).
  - Business continuity planning.
  - SC visibility and SCEM tools for early warning.
- **Resilience attributes:** Flexibility, visibility, collaboration, redundancy, speed of recovery.

### 5E. Demand-Driven Supply Chains
- Move push-pull frontier upstream (toward supplier).
- Use actual demand signals (POS) rather than forecasts.
- VMI, CPFR (Collaborative Planning, Forecasting, Replenishment).
- Benefits: reduced bullwhip, lower inventories, better service levels.
- Challenges: requires trust, data sharing, aligned systems.

### 5F. Supplier Relationship Management (SRM)
- **Spectrum:** Transactional → Preferred → Partner → Strategic alliance.
- **Key partnership attributes:** Shared vision, trust, aligned incentives, effective communication, compatible systems.
- **Supplier certification:** Verified quality → eliminate receiving inspection → lean deliveries.
- **Benefits of strong partnerships:** Add value, improve market access, build financial strength, add technology, strengthen operations.
- **Barriers to collaboration:** Misaligned incentives, power imbalances, culture conflicts, technology barriers, working with competitors.

### 5G. Channel Master and Buyer/Seller Dynamics
- **Channel master:** Dominant SC member who sets terms and direction.
- Buyer's market: Many suppliers, customer has leverage.
- Seller's market: Scarce supply, supplier has leverage.
- SC complexity: Only as complex as needed; variety only if actually in demand.

### 5H. Corporate Social Responsibility (CSR) and Sustainability
- Voluntary effort to balance profit against social/environmental needs.
- Supply chain transparency and traceability increasingly required.
- Green SC design: reduce packaging, optimize routing, cleaner transport modes.
- Ethical sourcing: labor standards, conflict minerals, fair trade.
- Life cycle assessment (LCA): full environmental impact from raw material to end-of-life.

---

## 6. Application Rules

### 6A. How to Choose a Supply Chain Strategy
1. Classify products as functional (predictable) or innovative (unpredictable).
2. Match SC type: efficient for functional; responsive for innovative.
3. Align supplier selection accordingly (cost/quality vs. speed/flexibility).
4. Consider whether multiple SC designs are needed for different product families.
5. Evaluate make-to-stock, ATO, MTO, ETO environment fit.

### 6B. Inventory Decision Rules
- **Set safety stock:** Based on demand variability (MAD/SD) and desired service level; adjust for lead time.
- **Set order quantity:** Use EOQ as starting point; modify for constraints (supplier minimums, truckload quantities).
- **Set reorder point:** DDLT + Safety Stock.
- **Classify items first (ABC):** A items get tight controls; C items get simple visual systems.
- **Reduce safety stock by:** Improving forecast accuracy, shortening lead times, increasing order frequency, reducing lead time variability.
- **Use lot-for-lot when:** Lean environment, expensive/perishable components, accurate demand signals available.
- **Use FOQ when:** Supplier minimums, truckload economics, efficient production batch sizes.
- **Use periodic review when:** Many items reordered from same supplier; desire to consolidate orders.

### 6C. Capacity Planning Decision Rules
- Always check capacity impact before confirming MPS or committing to customer.
- Adjust capacity before changing the priority plan (load).
- Use RCCP for medium-term validation; use CRP only when detailed work center data is needed.
- Bottleneck rule: Non-bottleneck work centers should NOT run at 100% utilization (just builds WIP).
- For TOC: Schedule only the constraint with finite loading; all others use drum-buffer-rope.

### 6D. Forecasting Decision Rules
- Never forecast what you can calculate (dependent demand).
- Aggregate forecasts are more accurate than item-level forecasts.
- Shorter horizon → higher accuracy; always use shortest useful horizon.
- Track forecast bias; investigate systematic over- or under-forecasting.
- Replace forecasting with demand pull (POS data) wherever possible.
- Use qualitative methods when no reliable historical data exists (new products, new markets).

### 6E. Transportation and Distribution Decision Rules
- Always calculate total cost (not just unit transport rate) — include inventory carrying cost impact.
- Air vs. water decision: air saves inventory carrying cost; water saves transport cost; crossover at certain item value/volume.
- TL vs. LTL: TL lower rate but builds lot-size inventory; LTL higher rate but lower inventory.
- Add a DC when transportation savings exceed warehousing + inventory costs.
- Mode selection: align with product value density, lead time requirements, reliability needs.

### 6F. Supplier Selection and Management Rules
- Select suppliers for strategic fit first, then cost.
- For critical/high-risk items: prioritize reliability, quality, flexibility over cost.
- For commodity/low-risk items: prioritize cost and simplicity.
- Build partnerships with key suppliers; maintain arm's-length for transactional suppliers.
- Scorecards: track perfect orders, inventory performance, admin, problem resolution speed.
- Give feedback early; help suppliers improve rather than switching on first failure.

### 6G. Bullwhip Effect — Mitigation Rules
- Share POS or end-consumer demand data with all SC tiers.
- Reduce order batching (more frequent, smaller orders).
- Stabilize pricing (avoid promotions that cause demand spikes).
- Shorten lead times to reduce order cycle impact.
- Implement VMI or CPFR for key customers/suppliers.
- Use DRP to share visibility across distribution network.

### 6H. Continuous Improvement Rules (DMAIC / Lean / TOC)
- Start with the customer's problem; define clearly before measuring.
- Use data, not opinion, to identify root causes.
- Prioritize improvements at the system constraint (TOC), not at non-constraints.
- Sustain improvements through standardization and control charts.
- Employee involvement is mandatory; quality at the source (jidoka).
- Small, frequent improvements (kaizen) over large, infrequent overhauls.
- Benchmark against best-in-class, not just internal targets.

### 6I. MRP / S&OP Implementation Rules
- "Garbage in, garbage out" — data integrity is the #1 prerequisite for MRP.
- S&OP must produce ONE set of numbers agreed to by all functions.
- Executive meeting is mandatory; without CEO participation, S&OP is just a planning exercise.
- Time fences protect production stability; changes inside frozen zone require senior management approval.
- Firm planned orders prevent system nervousness for critical components.
- MRP nervousness signal: investigate whether demand signals or lead time data are inaccurate.

### 6J. Project Management Rules (CSCP Module 1, Section B, Ch. 4)
- Define scope clearly (what will AND will not be done).
- WBS (Work Breakdown Structure) decomposes deliverables into manageable work packages.
- Triple constraint: Scope ↔ Schedule ↔ Budget; changing one affects the others.
- Stakeholder register: identify early; gather communication requirements.
- Reserve meetings for substantive risks and issues; control change through tradeoff analysis.
- Measure and control against the plan; escalate exceptions, not just status.

---

## Appendix: Key Terms Reference

| Term | Definition |
|---|---|
| Takt time | Available production time / Customer demand rate; sets production pace |
| Heijunka | Level scheduling by volume and mix; smooths production |
| Kanban | Visual pull signal; authorizes production or replenishment |
| Poka-yoke | Mistake-proofing device or process design |
| Jidoka | Automation with human intelligence; stop on defect |
| CPFR | Collaborative Planning, Forecasting, Replenishment |
| VMI | Vendor-managed inventory; supplier manages replenishment |
| ASN | Advance Ship Notice; electronic pre-notification of shipment |
| Incoterms | International Commercial Terms; define export/import obligations |
| Bill of Lading | Legal contract between shipper and carrier |
| FTZ | Free Trade Zone; defer duties, reduce import costs |
| Cross-docking | Receive and ship without put-away; minimal storage time |
| Postponement | Delay product differentiation to reduce forecast risk |
| Mass customization | High-variety at near-mass-production cost |
| Decoupling point | Point in SC where push switches to pull |
| Order qualifier | Minimum requirements to be considered by customer |
| Order winner | Factor that actually wins the order vs. competitors |
| Channel master | SC member with greatest power to set terms |
| 3PL | Third-party logistics provider |
| ATP | Available-to-Promise; uncommitted inventory/production capacity |
| PAB | Projected Available Balance; future inventory projection in MPS |
| RCCP | Rough-Cut Capacity Planning; validates MPS against key resources |
| CRP | Capacity Requirements Planning; detailed capacity check at MRP level |
| PAC | Production Activity Control; shop-floor execution and control |
| DRP | Distribution Requirements Planning; MRP logic for distribution network |
| SCEM | Supply Chain Event Management; monitor, alert, control SC exceptions |
| TMS | Transportation Management System |
| WMS | Warehouse Management System |
| ERP | Enterprise Resource Planning |
| SaaS | Software as a Service |
| EDI | Electronic Data Interchange |
| RFID | Radio Frequency Identification |
| POS | Point of Sale |
| SOA | Service-Oriented Architecture |
| B/L | Bill of Lading |
| LCL | Less-than-Container Load |
| FCL | Full Container Load |
| TL | Truckload |
| LTL | Less-than-Truckload |
| Deadhead | Empty miles (truck returning without load) |
| Demurrage | Charge for detaining rail car or vessel beyond free time |
| Detention | Charge for detaining truck beyond free time |

---

*Knowledge base compiled from: CPIM Part 1 Module 1 Sections A–J (Fall 2018 Bootcamp), CPIM Part 2 Module 3 Sections A–C (2020), CSCP Sessions 01–06 (Spring 2018), and supplemental exam materials. Files processed: 16 PowerPoint presentations, 3 exam PDFs. Files skipped: Excel worksheets, invoices, administrative documents, images.*
