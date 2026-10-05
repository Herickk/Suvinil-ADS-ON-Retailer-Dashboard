# Suvinil ADS ON – Retailer Dashboard

[🇧🇷 Português](README.md) | 🇺🇸 English

**Power BI** dashboard to track the retailers enrolled in the **Suvinil ADS ON** program: each store's activation status, contact profiles, contracted plans, geographic distribution, and access to every retailer's individual dashboard.

 🔗 **[Open the dashboard in Power BI](https://app.powerbi.com/view?r=eyJrIjoiYzE1ZjYyZWEtYWFkYi00OTg1LWEzMmUtYzlkMWQ1MDNlMTM5IiwidCI6ImFkMWExMmJkLWU1NzctNDA2NC1iOWQ1LTBhMzkwMzgwYjk0OCJ9)**








<img width="1630" height="787" alt="Captura de ecrã 2026-10-05 215724" src="https://github.com/user-attachments/assets/49f42725-88e3-4b06-8417-b7a3ef9b667a" />
<img width="1671" height="893" alt="Captura de ecrã 2026-10-05 214919" src="https://github.com/user-attachments/assets/8b0c3039-bdf1-4c67-852a-3fa30f9835eb" />


---

## 📌 Overview

The report answers questions such as:

- How many stores are registered and what stage is each one in?
- Which plans (legacy and new) are being contracted?
- Which regions and states are the retailers in?
- Who are the registered contacts (job titles)?
- Where is each store's individual dashboard?

---

## 🧭 Dashboard components

### 1. Filters (top of the page)

| Filter | Description |
|---|---|
| **Região** (Region) | Filter by Brazilian region (Southeast, South, North, etc.) |
| **Estado** (State) | Filter by state |
| **Razão Social** (Company name) | Filter by a specific store |
| **Plano Escolhido** (Chosen plan) | Filter by contracted plan |

All default to **"Todos" (All)** and affect every visual on the page.

### 2. Lojistas cadastrados (Registered retailers – donut chart)

Shows the **total number of stores (17)** and the breakdown by status:

| Status | Stores | % | Meaning |
|---|---|---|---|
| **Em Veiculação** (Live) | 12 | 71% | Campaign active and running |
| **Setup Inicial** (Initial setup) | 3 | 18% | Store being configured / onboarded |
| **Aguardando Pagamento** (Awaiting payment) | 2 | 12% | Registered, payment pending |

### 3. Cargo (Job title)

Bar chart of the **contact's job title** registered for each store (e.g., Manager 17.65%, Managing partner 11.76%, Director, Marketing director, Owner, Marketing manager – 5.88% each). Scrollable for more titles.

### 4. Planos Antigos (Legacy plans)

Matrix of **plan × billing period** (Monthly, Quarterly, Semiannual), showing the number of stores in each combination:

| Plan | Monthly | Quarterly | Semiannual |
|---|---|---|---|
| Basic | – | 1 | 2 |
| Premium | – | 1 | – |
| Business | – | – | 3 |

### 5. Planos Novos (New plans)

Number of stores per plan in the new pricing structure:

| Plan | Stores |
|---|---|
| Start | 2 |
| Basic | 4 |
| Premium | 2 |

### 6. Localização (Location map)

Map with the **states that have retailers** highlighted in orange, for a quick view of geographic coverage.

### 7. Região (Region) and Estado (State)

Bar charts with the **percentage of stores** by region and by state:

- **Region:** Southeast (52.94%), South (29.41%), North (11.76%), and others (scroll)
- **State:** São Paulo (29.41%), Rio Grande do Sul (23.53%), Minas Gerais (17.65%), and others (scroll)

### 8. Status buttons

Quick segmentation by workflow stage. Clicking one filters the whole report:

- **Selecionar tudo** (Select all)
- **Aguardando pagamento** (Awaiting payment)
- **Em veiculação** (Live)
- **Setup inicial** (Initial setup)

### 9. Retailer table

Detailed list, one row per store:

| Column | Description |
|---|---|
| **CNPJ** | Store's Brazilian company tax ID |
| **Estado** | Store's state |
| **Razão Social** | Registered company name |
| **Dashboard** | Link to the store's individual dashboard (Looker Studio), or the text **"Setup inicial"** when it has not been released yet |

---

## 🔄 Store status flow

```
Awaiting Payment  →  Initial Setup  →  Live
```

> The order above is illustrative; confirm the official flow with the responsible team.

---

## 💡 How to use

1. Use the **top filters** or the **status buttons** to segment the data.
2. Click a **bar, slice, or state** in any chart to cross-filter the other visuals.
3. In the **table**, click the link in the *Dashboard* column to open the store's individual panel.
4. To clear a selection, click the selected element again or press **Selecionar tudo**.

---

## ⚠️ Notes

- Some **CNPJs appear in scientific notation** (e.g., `1.53753E+13`). This means the column is stored as a **number** in the source. Convert it to **text** at the source to preserve the full CNPJ.
- **Legacy** and **new** plans coexist; stores migrated or signed after the change appear under the new structure.
- Retailer data (CNPJ, company names, links) is **sensitive**: do not commit it to this repository.

---

## 🛠️ Tech stack

- Power BI (Service)
- Google Looker Studio (per-store dashboards)
- Map: Microsoft Bing Maps (native Power BI visual)

---

## 📄 License / Owner

Add the report owner and internal-use policy here.
