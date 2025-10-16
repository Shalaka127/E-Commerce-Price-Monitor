# E-Commerce Price Monitor 

> A compact, easy-to-run pipeline for loading, cleaning and visualizing product prices from a small sample dataset.
> Built for quick demonstration in **Google Colab** or locally — uses the provided `clean_books_data.csv`.

---

## 📌 Project Summary

This repository contains a minimal, well-documented notebook and helper scripts to:

* Load a provided CSV (`clean_books_data.csv`).
* Perform light cleaning and normalize price values.
* Produce a short statistical summary and simple visualizations (histogram + boxplot).
* Save a cleaned CSV for submission or further analysis.

Designed to be simple and readable so it’s ideal for coursework, demos, or quick reviews.

---

## 🔍 What’s different in this “Friend’s Edition”

* Keeps the pipeline intentionally short and focused — fewer cells, straightforward logic.
* Uses slightly different variable names, output filename and plotting style so it looks distinct from other versions.
* Uses the **same CSV** that’s included in the repository (`clean_books_data.csv`), so there’s no need to run the scraper to produce outputs.

---

## 📁 Repository Layout

```
├── README-FRIEND.md               # (this file) Friend-friendly README
├── clean_books_data.csv           # Provided sample data (source for the notebook)
├── notebooks/
│   └── friend_price_monitor.ipynb # Colab-ready notebook (simple, cell-by-cell)
└── outputs/                       # (optional) cleaned CSVs and plots will be saved here
```

---

## ▶️ Quick Start (Google Colab)

1. Open `notebooks/friend_price_monitor.ipynb` in Google Colab.
2. Upload `clean_books_data.csv` to the Colab session (or place it in the working directory).
3. Run the cells in order:

   * Load CSV → Clean/normalize price → Summary table → Visualize → Save cleaned CSV.
4. The notebook will save a cleaned CSV as `friend_clean_books_export.csv` in the working directory.

> Tip: In Colab you can use the left sidebar ▶️ **Files** to upload `clean_books_data.csv` before running the notebook.

---

## 💡 Usage Notes

* The notebook detects the first column name containing `"price"` (case-insensitive) and attempts to parse values by stripping common currency symbols (e.g., `£`) and commas.
* It drops rows where a numeric price cannot be parsed.
* Visualizations are basic and intentionally uncluttered to make quick comparisons easy.

---

## 📊 Outputs

* `friend_clean_books_export.csv` — cleaned dataset (prices parsed to numeric `price_gbp`).
* A short printed summary (count, mean, median, min, max) and a small table of counts by price range.
* Two simple plots: histogram and horizontal boxplot of prices.

---

## 🛠️ Customization Ideas

If you want to extend the notebook later (not required for current submission), consider:

* Adding more price buckets or changing bin ranges.
* Parsing additional fields (rating, category) if they exist in the CSV.
* Saving results to Google Drive for persistent storage.
* Adding a small README cell inside the Colab that documents the parameters used (bins, filename, etc.).

---

## ⚖️ Ethical Considerations

* This edition is meant to work with a **pre-provided dataset** only. It does not perform live scraping.
* If you adapt the code to scrape real websites, **always** respect `robots.txt` and the site’s Terms of Service.
* Use polite scraping practices (minimal request rates, proper User-Agent, retries). For production monitoring use official APIs where available.
* Do not publish or distribute personal or proprietary data without permission.

---

## 🤝 Contributing & Contact

* This project is intentionally small; if you want changes (e.g., slightly different charts, alternate bucket choices, or saving to Drive), submit a small pull request or open an issue describing the tweak.
* For direct help or a custom tweak before submission, contact the repository owner (or just ask me and I’ll make the edit).

---

## 📝 License

This project is provided for educational use. Use or adapt under the MIT License (or replace with your preferred license).

---

*Last updated: 2025-10-14*
