# SALES-DATA-CLEANUP

# Cleaning a Messy Sales Dataset with Power Query

I recently tackled a messy sales dataset using **Power Query**. From the start, the structure was a problem. Instead of clean, well-organized columns, the dataset had ship modes scattered across the first row. Customer segments had the same issue.

That layout makes analysis by ship mode or segment impossible.

![Step 1](https://github.com/user-attachments/assets/3022e93c-a1f8-4439-b8fe-e59d2a85659c)

## 🔍 The Problem

The dataset was **row-wise** instead of **column-wise**. In Power Query, that’s a red flag. You usually need one of these:

- **Transpose**: Flips rows into columns
- **Unpivot**: Turns column headers into values

Both are useful when data categories are trapped in the wrong orientation.

---

## 🧹 Steps I Took

**1. Deleted automatic steps**  
I removed the default `"Promoted Headers"` and `"Changed Type"` steps.

![Step 2](https://github.com/user-attachments/assets/3a5102ef-8da1-4306-8fb4-63d913ea0fb5)

**2. Transposed the dataset**  
Flipped rows and columns to correct the direction.

![Step 3](https://github.com/user-attachments/assets/9ade9fe9-37d2-4847-85d4-ff0d68b2bef2)

**3. Promoted first row to headers**

![Step 4](https://github.com/user-attachments/assets/951dc378-97f0-4e3e-b142-05f10e01934e)

**4. Filled down ship mode values**

![Step 5](https://github.com/user-attachments/assets/ee03eefb-68dc-47d6-8e1a-2dcd05b83809)

**5. Unpivoted order date columns**  
Each order now appeared as its own row.

![Step 6](https://github.com/user-attachments/assets/420c841d-7651-4022-8f3f-f42b6700f180)

**6. Cleaned the order date column**  
Extracted text before the underscore.

![Step 7](https://github.com/user-attachments/assets/5b701da7-1362-4de0-b449-a3fdfaa50493)

**7. Set final column to the correct data type**  
Used `"Date"` type to finish cleanup.

---

## ✅ Result

The final dataset was clean, structured, and ready for analysis. A simple transformation sequence with **big impact**.

---

### 📌 Tags  
`#PowerQuery` `#PowerBI` `#DataCleaning` `#BusinessIntelligence` `#DataAnalytics`
