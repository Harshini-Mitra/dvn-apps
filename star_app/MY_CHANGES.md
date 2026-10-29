# AppStar: changes for the Part D exercise

1. **Metallicity slider**: `lz = st.slider("log10 metallicity", -4.0, -1.4, -1.7, step=0.05)`, `Z = 10 ** lz`, `zr = Z / 0.02`. The two marked lines (luminosity `L = M^3.5 zr^-0.1` and the remnant boundary `18 + 7 zr`) respond. A caption reports Z and the current neutron-star/black-hole boundary. The grid is cached per metallicity (`st.cache_data`).
2. **Pair-instability branch**: with Z < 0.001, stars of 140–260 suns end as "no remnant (pair instability)". Nothing is drawn in the portrait.
3. **HR diagram replaces the phase plane** (Altair):
   - Temperature on the x axis, log scale and reversed, so hot is on the left. Luminosity on the y axis, log scale, 10^-4 to 10^6 suns.
   - The main-sequence band is a swept array of masses using the same rules as `star_state`, so it shifts with metallicity too.
   - Your star is the grid row picked by the sliders, plotted at its phase-adjusted `temp_K` and `lum`. It leaves the band as a giant (up and right) or white dwarf (down and left). Supernova, neutron star, black hole and no-remnant rows have no luminosity, so they drop off, with a note.
4. **Fix to the starter**: the slider-to-grid match tolerance is now half a grid step. The default age (0.66) lies between grid ages 0.62 and 0.68, so the original showed an empty star until a slider was moved.
5. Replaced the deprecated `use_container_width` with `width="content"`.
