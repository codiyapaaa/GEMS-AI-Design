# GEMS AI — Dashboard Design Generation

**Execution:** Claude AI + Figma MCP  
**Scope:** Dashboard UI/UX Design  
**Governance:** Human-in-the-Loop  
**Instruction Priority:** Mandatory

## 1. Input & References

**Target Figma:** `[MASUKKAN LINK FIGMA TUJUAN]`

**Requirements / Data:** `[UPLOAD FILE / MASUKKAN LINK / TULIS TASK]`

Supported inputs: HSD, BRD, PDF, DOCX, XLSX, CSV, Google Docs/Sheets, GitHub, ZIP, atau direct instructions.

### Official Design System & Guidelines

- [GEMS Design System — Figma](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System)
- [Dashboard Guidelines](https://github.com/codiyapaaa/GEMS-AI-Design/blob/main/guidelines/dashboard.md)
- [Design Guidelines](https://github.com/codiyapaaa/GEMS-AI-Design/blob/main/guidelines/design-guideline.md)
- [Component Guidelines](https://github.com/codiyapaaa/GEMS-AI-Design/tree/main/components)
- [UX Patterns](https://github.com/codiyapaaa/GEMS-AI-Design/tree/main/guidelines/ux-patterns)

**Reference Rules:**

- AI MUST read actual source content, not filenames or URLs alone.
- AI MUST load only relevant component guidelines, UX patterns, and dashboard examples to minimize token usage.
- AI MUST use official GEMS components, variants, states, and design tokens.
- If a required source is inaccessible, request access or clarification. Never invent its contents.

## 2. Official GEMS Chart Components

AI MUST inspect relevant chart components through Figma MCP before selecting visualizations.

| Component | Figma Reference |
|---|---|
| Line and Bar Chart | [View](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=441-4196) |
| Pie Chart | [View](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=786-2005) |
| Chart Data | [View](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=441-3302) |
| Activity Gauge | [View](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=441-3540) |
| Radar Chart | [View](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=441-3666) |
| Vertical Bar Chart | [View](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=2339-19393) |
| Horizontal Bar Chart | [View](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=2339-19715) |
| Line Chart | [View](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=2339-19714) |
| Bar & Line Chart | [View](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=2339-18667) |
| Doughnut Chart | [View](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=2339-19848) |

**Chart Selection:** KPI Card = key values; Line = trends; Bar = comparisons; Pie/Doughnut = proportions; Gauge = valid targets; Radar = comparable dimensions; Table = detailed records.

AI MUST choose charts based on analytical purpose, data structure, and usability. Do not use unnecessary charts, misleading scales, invented data, or unsupported calculations.

## 3. Dashboard Design References

Use only relevant examples to understand layout, information hierarchy, KPI Cards, Charts, Tables, and Filters.

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

AI MUST NOT copy reference layouts blindly or treat examples as business requirements.

## 4. Mandatory Execution Workflow

### Phase 01 — Data Analysis

AI MUST:

1. Analyze provided requirements and datasets.
2. Identify dashboard objectives, users, KPI, metrics, calculations, trends, comparisons, data availability, and permissions.
3. Separate confirmed, proposed, and missing information.
4. Recommend relevant KPI and analytical information with brief reasoning.
5. Present a concise **Data Summary** for approval.

**STOP — HUMAN APPROVAL #1**

Do not proceed until the Data Summary is explicitly approved.

### Phase 02 — Dashboard Period Confirmation

After Approval #1, AI MUST ask:

**"Dashboard ini perlu periode apa saja: Hari Ini, Minggu Ini, Bulan Ini, Tahun Ini, dan Custom Periode? Mau semuanya atau hanya beberapa? Tampilannya satu dashboard dengan filter atau dashboard terpisah?"**

Rules:

- Allow one, multiple, or all five periods.
- If user says **"Ya, semuanya"**, include all five.
- Validate data availability and aggregation for selected periods.
- Confirm whether periods use filters or separate dashboard views.
- Record the decision in the Dashboard Design Plan.
- Never invent unavailable period data.

### Phase 03 — Design Planning

AI MUST:

1. Read relevant GEMS Guidelines and inspect required Figma components.
2. Select KPI Cards, Charts, Tables, Filters, Actions, and official component variants.
3. Define information hierarchy, layout, filter behavior, and responsive requirements.
4. Map each UI element to its documented GEMS Component.
5. Define all mandatory UI States, Empty States, and applicable CRUD Flows.
6. Present a concise **Dashboard Design Plan** containing layout, chart selection, component mapping, approved periods, states, and interactions.

**STOP — HUMAN APPROVAL #2**

Do not generate Figma designs until the Dashboard Design Plan is explicitly approved.

### Phase 04 — Figma Generation

After Approval #2, AI MUST:

1. Verify Figma MCP write capability and Target Figma access.
2. Generate approved dashboard views directly in Target Figma using official GEMS component instances.
3. Include all approved periods, UI States, Empty States, and applicable CRUD Screens.
4. Add UX Flow Diagrams above corresponding screens for CRUD or multi-step interactions.
5. Preserve existing designs unless modification is approved.
6. Return the actual Figma design link.

If Figma MCP cannot perform an operation, explain the limitation and request approval before using an alternative. Never claim unsuccessful work is completed.

## 5. Mandatory Dashboard Design Rules

### 5.1 Layout & Filters

AI MUST maintain clear information hierarchy, logical grouping, readable charts, consistent grid/spacing, and responsive behavior.

Filters MUST update related KPI Cards, Charts, and Tables consistently. Use only approved periods, metrics, and filter dependencies.

### 5.2 UI States & Empty States

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

AI MUST distinguish **Zero Value, Missing Data, Empty Data, and No Results**. Use official GEMS Empty State and feedback components.

### 5.3 CRUD & UX Patterns

If requirements include Create, Read, Update, or Delete, AI MUST design applicable forms, details, validation, confirmation dialogs, success/error feedback, and UX Flow Diagrams according to approved permissions and GEMS UX Patterns.

AI MUST NOT introduce unsupported CRUD operations or invent business rules.

### 5.4 Component Usage Enforcement

**Mandatory Component Mapping:**

| UI Element | Official Guideline |
|---|---|
| Status | [Badge](https://github.com/codiyapaaa/GEMS-AI-Design/blob/main/components/badge.md) |
| Actions / CTA | [Button](https://github.com/codiyapaaa/GEMS-AI-Design/blob/main/components/button.md) |
| Search / Text | [Input](https://github.com/codiyapaaa/GEMS-AI-Design/blob/main/components/input.md) |
| Selection / Filter | [Dropdown](https://github.com/codiyapaaa/GEMS-AI-Design/blob/main/components/dropdown.md) |
| Confirmation | [Modal](https://github.com/codiyapaaa/GEMS-AI-Design/blob/main/components/modal.md) |
| Feedback | [Alert](https://github.com/codiyapaaa/GEMS-AI-Design/blob/main/components/alert.md) |
| Page Navigation | [Pagination](https://github.com/codiyapaaa/GEMS-AI-Design/blob/main/components/pagination.md) |
| No Data | [Empty State](https://github.com/codiyapaaa/GEMS-AI-Design/blob/main/components/empty-state.md) |

AI MUST read relevant component documentation and follow its **Usage Rules, Anatomy, Variants, States, Behavior, and Restrictions** before selecting the component.

For example, table status MUST use Badge according to `badge.md`, not arbitrary text or custom labels.

Actual component guidelines take precedence over example mappings. If a required component or rule is unavailable, request clarification or approval rather than inventing one.

## 6. Execution Constraints

**AI MUST:**

- Follow the approved Data Summary, Dashboard Periods, and Design Plan.
- Use GEMS Design System, documented components, and approved UX Patterns.
- Complete both Human Approval gates before generating designs.
- Generate required dashboard states and applicable CRUD.
- Ask for approval before material changes to KPI, calculations, permissions, UX Flows, or components.
- Report actual output and limitations accurately.

**AI MUST NOT:**

- Skip approval gates or assume silence means approval.
- Invent requirements, data, component rules, or calculations.
- Replace official GEMS components with unapproved custom components.
- Generate only Default State.
- Modify unrelated existing Figma designs.
- Claim Figma generation succeeded without confirmation.

### Mandatory Sequence

`Read Inputs → Analyze Data → Data Summary → Approval #1 → Confirm Periods → Read Relevant GEMS Guidelines → Plan Components, Layout, States & CRUD → Dashboard Design Plan → Approval #2 → Generate in Target Figma → Share Actual Link`

**FINAL RULE: Data determines information. GEMS determines components and usage. Human Approval authorizes execution. Target Figma determines destination.**
