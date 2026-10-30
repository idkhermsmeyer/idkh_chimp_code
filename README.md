# Environmental predictors of wild chimpanzee hair stable isotope values

Data and R code for: Environmental factors constrain trophic niche breadth in chimpanzees: implications for research on past and future primate ecology
Isabel D.K. Hermsmeyer, Andrew D. Somerville, Jim J. Moore, McKensey R. Miller, Gene R. Estrada, Elliot G. Greiner, Andrew W. Froehle, Carolyn M. Kurle, and Margaret J. Schoeninger
. Ecological Solutions and Evidence (2026).

## Files
- IDKH_chimp_code.Rmd: R Markdown script for all statistical analyses, model comparison, isotopic niche (SIBER) analyses, and figures. Knit with all CSV files in the same folder; figures are saved to figures/ and output tables to output/.
- Chimp_data_full_worldclim_SEA_fin.csv: Main analysis dataset. One row per hair sample (n = 279) from 17 chimpanzee communities (105 newly analyzed samples from this study and 174 from published studies; see Source column), with site-level environmental variables and isotopic niche space (SEA).
- behavioral_diversity.csv: Site-level overall and foraging behavioral diversity indices for the 10 communities with available data (from Kalan et al., 2020; Fig. 5).
- chimp_fossil_comp.csv: Enamel δ13C values (‰, corrected to a preindustrial [1750] atmospheric baseline) for modern chimpanzees and Miocene fossil hominoids, with sources (n = 57; Fig. 7).

## Usage
Place all files in the same folder and run IDKH_chimp_code.Rmd in R/RStudio.

## Column descriptions: Chimp_full_data_worldclim_fin.csv
Identifiers
- Group: Chimpanzee community
- Site: Study site (communities at Gombe and Ugalla share a site)
- Source: Data source ("This study" or original publication)
- Latitude: Site latitude (decimal degrees)
- Ecoregion: [?] ecoregion code
- Spec: Specimen ID (newly analyzed samples only)

Isotope data
- d13C: δ13C (‰, VPDB), corrected for the atmospheric Suess effect
- d15N: δ15N (‰, AIR)
- CN: Atomic C:N ratio (where available)

Vegetation (site-level)
- treeCoverMax / Mean / Median / Min / Mode: Tree canopy cover (%) [source, e.g., dataset and buffer radius]
- percEvergreen: Percent evergreen forest [source]

Climate and topography (site-level; WorldClim v2.1, 1970–2000, 30 arcsec)
- MAP: Mean annual precipitation (mm)
- Min_temp / Max_temp: [?] Minimum / maximum temperature (°C)
- MAT: Mean annual temperature (°C)
- Temp_seasonality: Temperature seasonality (SD × 100; BIO4)
- Seasonality_Precipitation: Precipitation seasonality (coefficient of variation; BIO15)
- Wettest_Month_Precip / Driest_Month_Precip: Precipitation of wettest / driest month (mm)
- Wettest_Quart_Precip / Driest_Quart_Precip / Warmest_Quart_Precip / Coldest_Quart_Precip: Precipitation of wettest / driest / warmest / coldest quarter (mm)
- Elevation: Elevation (m)

Niche metrics and projections (site-level)
- Niche_space: Standard ellipse area [?SEAc] (‰²)
- Niche_space_245, Niche_space_245_2041, Niche_space_C, Niche_space_S: [?]
- SSP245AVG_2041_precip / SSP585AVG_2041_precip: Projected precipitation [seasonality?] for 2041–2060 under SSP2-4.5 / SSP5-8.5 [?GCM ensemble]
- predicted_sd_d13C_future / predicted_sd_d15N_future: [?] Predicted SD of δ13C / δ15N under future climate

Missing values are left blank.
