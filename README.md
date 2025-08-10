# Visual Calculation Examples in Power BI

## 📌 Overview
This repository contains examples of using **Visual Calculations** in Power BI to simplify traditional DAX logic.  
The goal is to demonstrate how new built-in functions like `RANK`, `LOOKUP`, `LOOKUPWITHTOTALS`, and `COLLAPSE` reduce complexity, avoid repetitive patterns, and make calculations easier for users with limited DAX experience.

The examples are implemented in the `.pbix` file and explained in the accompanying `.docx` file.

---

## 📂 Files Included
- **Visual Calculation Examples.pbix** – Power BI file with implemented examples.
- **Visual Calculation Examples.docx** – Detailed explanation of each example, including old vs new method.

---

## 📝 Examples

### 1. **Rank Function**
**Purpose:** Rank items based on a measure used in the visual.

- **Old Way:** Required `RANKX` with `ALL()` or `ALLSELECTED()` — intimidating for beginners.
- **Visual Calculation:** `RANK` visual calculation is simpler — just provide the measure and order, no extra filter context handling needed.

---

### 2. **LookUP Value & LookUPWithTotals**
**Purpose:** Retrieve specific values or benchmarks directly in the visual.

- **LookUP Value:** Gets a single value from another row without complex `LOOKUPVALUE` or `CALCULATE` logic.
- **LookUPWithTotals:** Gets a value from a specified row (e.g., `"Control"` customer) **and** its corresponding total in one step.
- **Old Way:** Would require `CALCULATE` with multiple filters and `ALL()` to remove row context.
- **Visual Calculation:** Built-in `LOOKUP()` and `LOOKUPWITHTOTALS()` functions make it a one-line calculation.

---

### 3. **Percent of Parent (Collapse)**
**Purpose:** Show the percentage contribution of each child item to its parent total.

- **Old Way:** Needed `CALCULATE` with `REMOVEFILTERS` or `ALL()` to get parent totals.
- **Visual Calculation:** `COLLAPSE()` automatically calculates at a higher hierarchy level — no manual filter removal required.

---

## 🚀 How to Use
1. Download and open **Visual Calculation Examples.pbix** in the latest version of Power BI Desktop (with Visual Calculations enabled).
2. Navigate to each example page:
   - **Page 1:** Rank Function
   - **Page 2:** LookUP & LookUPWithTotals
   - **Page 3:** Percent of Parent (Collapse)
3. Compare the **Old Way** DAX measures with the **Visual Calculation** formulas in the visual calculation editor.

---

## 💡 Key Benefits of Visual Calculations
- Eliminates the need for `ALL()`, `ALLSELECTED()`, and `REMOVEFILTERS` in many cases.
- Shorter, more readable formulas.
- Beginner-friendly and easier to maintain.
- Calculations are evaluated at the visual level, automatically respecting filters and slicers.

---

---

**Author:** *Your Name*  
**Date:** *YYYY-MM-DD*
