# Streamlit 2: multipage app (official tutorial)

Built from the "Create a multipage app" tutorial: `Hello.py` is the entrypoint, and Streamlit builds the sidebar navigation from the `pages/` folder.

- `pages/1_📈_Plotting_Demo.py`: animated random-walk line chart.
- `pages/2_🌍_Mapping_Demo.py`: pydeck map with four toggleable layers.
- `pages/3_📊_DataFrame_Demo.py`: UN agricultural data with a country selector.

One change from the tutorial: `chart.add_rows()` no longer exists in current Streamlit, so the plotting demo keeps the growing series in an array and redraws it in an `st.empty()` placeholder. It looks the same.
Deploy with `Hello.py` as the main file.
