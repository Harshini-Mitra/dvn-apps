# My adaptation of the gold dashboard

**Question it helps answer:** *When* did each central bank buy or sell gold, and how do their running totals compare over a chosen period?

The original "Declared official sector" ranking sums the last 12 months into one bar per country. That makes countries easy to compare, but it hides timing and anything older than a year.

## Changes
1. **New view: "Compare countries over time"** (end of the Declared tab)
   - Choose up to four countries (default: the top buyer and the top seller) and a period.
   - Switch between **monthly change** (bars) and **running total** (lines, with end labels).
   - Reuses the dashboard's grammar: same country colours and the same event rules, and the caption states the net change over the chosen period.
   - Shows a clear message when no country is selected.
2. **Sample data clearly labelled**: a notice at the top and in the source line, so nobody reads synthetic figures as real.
3. **Maintenance**: replaced the deprecated `use_container_width` and pinned package versions in `requirements.txt` for a reproducible Streamlit Cloud deployment.
