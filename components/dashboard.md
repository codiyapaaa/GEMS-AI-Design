# GEMS AI — Dashboard Design Generation

**Execution:** Claude AI + Figma MCP  
**Scope:** Dashboard UI/UX Design Generation  
**Governance:** Human-in-the-Loop  
**Instruction Priority:** Mandatory

## 1. Input & Official References

**Target Figma:** `[MASUKKAN LINK FIGMA TUJUAN]`

**Requirements / Data:** `[UPLOAD FILE / MASUKKAN LINK / TULIS TASK]`

Accepted inputs: HSD, BRD, PDF, DOCX, XLSX, CSV, Google Docs/Sheets, GitHub, ZIP, atau direct instructions.

### Official Sources

| Source | Reference |
|---|---|
| GEMS Design System | [Figma — Official Components](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System) |
| GEMS AI Repository | [GitHub](https://github.com/dgtuixexternal/GEMS-AI-Design) |
| Dashboard Guidelines | [dashboard.md](https://github.com/dgtuixexternal/GEMS-AI-Design/blob/main/guidelines/dashboard.md) |
| Design Guidelines | [design-guideline.md](https://github.com/dgtuixexternal/GEMS-AI-Design/blob/main/guidelines/design-guideline.md) |
| Component Guidelines | [components/](https://github.com/dgtuixexternal/GEMS-AI-Design/tree/main/components) |
| UX Patterns | [ux-patterns/](https://github.com/dgtuixexternal/GEMS-AI-Design/tree/main/guidelines/ux-patterns) |

**Source Priority:**

1. Approved HSD/BRD/Data → business requirements and calculations.
2. GitHub Component Guidelines → component selection, usage, variants, states, and behavior.
3. GEMS Figma Design System → official component instances and visual properties.
4. Dashboard/Design Guidelines → layout and design standards.
5. UX Patterns → interaction and CRUD flows.
6. Dashboard References → visual examples only.

AI MUST read relevant source content, not filenames or URLs alone. Load only required documentation to minimize token usage. If sources conflict or are inaccessible, STOP and request clarification. Never invent rules or data.

## 2. Official GEMS Chart Components

AI MUST inspect relevant chart components through Figma MCP and use official GEMS instances.

| Component | Figma Reference |
|---|---|
| Line and Bar Chart | [View Component](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=441-4196) |
| Pie Chart | [View Component](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=786-2005) |
| Chart Data | [View Component](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=441-3302) |
| Activity Gauge | [View Component](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=441-3540) |
| Radar Chart | [View Component](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=441-3666) |
| Vertical Bar Chart | [View Component](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=2339-19393) |
| Horizontal Bar Chart | [View Component](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=2339-19715) |
| Line Chart | [View Component](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=2339-19714) |
| Bar & Line Chart | [View Component](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=2339-18667) |
| Doughnut Chart | [View Component](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=2339-19848) |

**Chart Rules:** Choose charts based on analytical purpose and data structure. KPI Card = key values; Line = trends; Bar = comparisons; Pie/Doughnut = proportions; Gauge = valid targets; Radar = comparable dimensions; Table = detailed records.

AI MUST NOT use decorative charts, misleading scales, invented data, unsupported calculations, or custom charts when an appropriate official component exists.

## 3. Dashboard Design References

Use only relevant examples for information hierarchy, KPI Cards, Charts, Tables, Filters, and layout. References are not business requirements.

| Dashboard | Figma Reference |
|---|---|
| Fuel Management | [View](https://www.figma.com/design/NR3xLOKvfTvElF1HGgnnmM/ISS-Website?node-id=757-34567) |
| Main Dashboard | [View](https://www.figma.com/design/NR3xLOKvfTvElF1HGgnnmM/ISS-Website?node-id=4233-207299) |
| Visit | [View](https://www.figma.com/design/NR3xLOKvfTvElF1HGgnnmM/ISS-Website?node-id=3585-249006) |
| Accommodation | [View](https://www.figma.com/design/NR3xLOKvfTvElF1HGgnnmM/ISS-Website?node-id=3613-91801) |
| Meals Management | [View](https://www.figma.com/design/NR3xLOKvfTvElF1HGgnnmM/ISS-Website?node-id=3599-87213) |
| Transport | [View](https://www.figma.com/design/NR3xLOKvfTvElF1HGgnnmM/ISS-Website?node-id=3613-90610) |
| Laundry 01 | [View](https://www.figma.com/design/NR3xLOKvfTvElF1HGgnnmM/ISS-Website?node-id=3585-261583) |
| Laundry 02 | [View](https://www.figma.com/design/NR3xLOKvfTvElF1HGgnnmM/ISS-Website?node-id=3475-147760) |
| Charging Station | [View](https://www.figma.com/design/NR3xLOKvfTvElF1HGgnnmM/ISS-Website?node-id=619-23490) |
| HRGA | [View](https://www.figma.com/design/v3ggUUZOrTe6dh9wJ21Hcy/ISS-Registrasi-Asset?node-id=576-138623) |

## 4. Mandatory Execution Workflow

### Phase 01 — Data Analysis

AI MUST:

1. Analyze requirements and datasets.
2. Identify dashboard objectives, users, KPIs, metrics, calculations, trends, comparisons, data availability, and permissions.
3. Separate confirmed, proposed, and missing information.
4. Recommend relevant KPIs and visual information with brief reasoning.
5. Present a concise **Data Summary**.

**STOP — HUMAN APPROVAL #1 REQUIRED**

Do not proceed until the Data Summary is explicitly approved.

### Phase 02 — Dashboard Period Confirmation

After Approval #1, AI MUST ask:

**"Dashboard ini perlu periode apa saja: Hari Ini, Minggu Ini, Bulan Ini, Tahun Ini, dan Custom Periode? Mau semuanya atau beberapa saja? Tampilannya satu dashboard dengan filter atau dashboard terpisah?"**

Rules:

- Allow one, multiple, or all five periods.
- If user answers **"Ya, semuanya"**, include all five.
- Validate data availability and aggregation.
- Confirm filter-based or separate dashboard views.
- Record approved periods in the Design Plan.
- Never invent unavailable period data.

### Phase 03 — Design Planning & Component Mapping

AI MUST:

1. Read relevant GEMS GitHub Guidelines.
2. Identify required UI elements and their intended usage.
3. Read the corresponding `components/*.md` files before selecting components.
4. Verify documented Usage Rules, Variants, States, Behavior, and Restrictions.
5. Inspect matching official GEMS Figma components through MCP.
6. Select appropriate KPI Cards, Charts, Tables, Filters, Actions, and layouts.
7. Define information hierarchy, filter behavior, mandatory UI States, Empty States, and applicable CRUD.
8. Present a concise **Dashboard Design Plan** including component mapping, selected periods, charts, states, and interactions.

**STOP — HUMAN APPROVAL #2 REQUIRED**

Do not generate Figma designs until the Dashboard Design Plan is explicitly approved.

### Phase 04 — Figma Generation

After Approval #2, AI MUST:

1. Verify Target Figma access and MCP write capability.
2. Generate approved dashboard views directly in Target Figma.
3. Use official GEMS component instances with documented variants and states.
4. Include approved periods, UI States, Empty States, and applicable CRUD Screens.
5. Add UX Flow Diagrams above corresponding screens for CRUD or multi-step interactions.
6. Preserve existing designs unless modifications are approved.
7. Return the actual Figma design link.

If Figma MCP cannot perform an operation, report the limitation and request approval before using an alternative. Never claim unsuccessful work is completed.

## 5. Mandatory Component Guidelines Enforcement

**Official Guidelines:** [GEMS Components — GitHub](https://github.com/dgtuixexternal/GEMS-AI-Design/tree/main/components)

**GitHub determines WHICH component to use and HOW. GEMS Figma provides the official component instance.**

### 5.1 Component References

| UI Requirement | Required Guideline |
|---|---|
| Input / Search / Filter | [input.md](https://github.com/dgtuixexternal/GEMS-AI-Design/blob/main/components/input.md) |
| Status | [badge.md](https://github.com/dgtuixexternal/GEMS-AI-Design/blob/main/components/badge.md) |
| Action / CTA | [button.md](https://github.com/dgtuixexternal/GEMS-AI-Design/blob/main/components/button.md) |
| Dropdown (only when permitted) | [dropdown.md](https://github.com/dgtuixexternal/GEMS-AI-Design/blob/main/components/dropdown.md) |
| Confirmation | [modal.md](https://github.com/dgtuixexternal/GEMS-AI-Design/blob/main/components/modal.md) |
| Feedback | [alert.md](https://github.com/dgtuixexternal/GEMS-AI-Design/blob/main/components/alert.md) |
| Pagination | [pagination.md](https://github.com/dgtuixexternal/GEMS-AI-Design/blob/main/components/pagination.md) |
| Empty Data | [empty-state.md](https://github.com/dgtuixexternal/GEMS-AI-Design/blob/main/components/empty-state.md) |

### 5.2 Strict Component Selection Rules

AI MUST:

1. Identify the UI requirement before selecting any component.
2. Read the relevant GitHub Component Guideline.
3. Follow documented Usage Rules, Anatomy, Variants, States, Behavior, and Restrictions.
4. Inspect the matching official component through Figma MCP.
5. Select components based on documented usage, NOT visual similarity or generic UI conventions.
6. Apply the same rules across all dashboard views, periods, and states.
7. Request clarification when documentation is unavailable, ambiguous, or conflicting.

**Critical Rules:**

- **Filter:** AI MUST read `input.md` before designing filters. If the guideline specifies Input, AI MUST use the documented Input component and MUST NOT substitute Dropdown, Select, or custom filters.
- **Status:** AI MUST use Badge according to `badge.md`, including documented variants and states.
- **Actions:** AI MUST use Button according to `button.md`.
- **Confirmation:** AI MUST use Modal according to `modal.md`.
- **Empty Data:** AI MUST use the official Empty State component according to `empty-state.md`.

AI MUST NOT create custom replacements, invent variants, or override documented usage without Human Approval.

**Mandatory Selection Sequence:**

`Identify UI Requirement → Read GitHub Guideline → Verify Usage Rules → Inspect GEMS Figma Component → Select Correct Variant & State → Include in Design Plan`

## 6. Mandatory Dashboard Design Rules

### 6.1 Layout & Filters

AI MUST maintain clear information hierarchy, logical grouping, readable charts, consistent GEMS grid/spacing, and responsive behavior.

Filters MUST update related KPI Cards, Charts, and Tables consistently. Use only approved periods, metrics, and filter dependencies.

### 6.2 UI States & Empty States

**Every dashboard MUST include these design states:**

| State | Requirement |
|---|---|
| Default | Normal dashboard with data |
| Loading | Loading / Skeleton |
| Empty Data | No available records |
| No Results | No data matching filters |
| Error | Failed data loading |
| Filter Applied | Active filter results |
| Filter Reset | Default filter condition |

Add Hover, Focus, Selected, Disabled, Restricted, Partial Data, Success, or Confirmation states when relevant.

AI MUST distinguish Zero Value, Missing Data, Empty Data, and No Results using official GEMS components.

### 6.3 CRUD & UX Patterns

If requirements include Create, Read, Update, or Delete, AI MUST design applicable forms, details, validation, confirmation dialogs, success/error feedback, and UX Flow Diagrams according to approved permissions and GEMS UX Patterns.

AI MUST NOT introduce unsupported CRUD operations or invent business rules.

## 7. Execution Constraints

**AI MUST:**

- Follow approved Data Summary, Dashboard Periods, and Design Plan.
- Use official GEMS components according to GitHub Component Guidelines.
- Complete both Human Approval gates.
- Generate required UI States, Empty States, and applicable CRUD.
- Request approval before material changes to KPI, calculations, permissions, UX Flows, or component usage.
- Report actual Figma outputs and limitations accurately.

**AI MUST NOT:**

- Skip approval gates or assume silence means approval.
- Invent requirements, data, component rules, or calculations.
- Replace official GEMS components with unapproved custom components.
- Generate only Default State.
- Modify unrelated existing Figma designs.
- Claim Figma generation succeeded without confirmation.

### Mandatory Sequence

`Read Inputs → Analyze Data → Data Summary → Approval #1 → Confirm Periods → Read Relevant GitHub Component Guidelines → Inspect Official GEMS Figma Components → Plan Layout, States & CRUD → Dashboard Design Plan → Approval #2 → Generate in Target Figma → Share Actual Link`

**FINAL RULE: Approved requirements determine WHAT to design. GitHub Component Guidelines determine WHICH component to use and HOW. GEMS Figma determines the official component instance. Human Approval authorizes execution. Target Figma determines destination.**
