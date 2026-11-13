# Earth Information Jukebox

NASA Space Apps 2026 · The Earth Information Jukebox  
Data snapshot taken 13 November 2026 UTC

## Run it

1. Extract `earth-information-jukebox.zip`.
2. Open `index.html` in Chrome or Edge. Keep the `assets` folder beside it.
3. Choose a companion and start in Earth Orbit & Lab. Select **Ocean Currents**, then **Play**. Use **Hear this moment** to play the note shown in the telemetry.

The animations, maps, GISTEMP readings and audio synthesis are bundled and run offline. Source links need an internet connection. If a browser restricts local media, run `py -m http.server 8000` in the extracted folder on Windows, or `python3 -m http.server 8000` on macOS or Linux. Open [http://localhost:8000](http://localhost:8000).

The [hosted demo](https://earth-information-jukebox-eco-quest.anaselloussi2006.chatgpt.site/) is private and uses the owner’s ChatGPT sign-in. For a judges’ link, upload `index.html` and `assets/` to the root of a static site configured for judge access. No build step, API key, or Earthdata login is required. The ZIP includes the untouched original in `backup/`. Use only the updated page and its assets for hosting.

## 90-second judges’ demo

| Time | Action | What to point out |
| --- | --- | --- |
| 0:00 | Select a companion and open Earth Orbit & Lab. Choose **Ocean Currents** and press **Play**. | These are frames from NASA’s Earth Information Center. The Jukebox measures how much the current pixels change and uses that to set the musical pulse. |
| 0:20 | Pause, move the slider to a different part of the clip, and press **Hear this moment**. Open **Source and how it becomes music**. | The screen shows frame statistics and the actual note, tempo, filter cutoff, and stereo pan. The displayed model date is approximate. |
| 0:40 | Choose **Climate Through Time**. On a keyboard, select the year slider and use **Home** for 1880. Press **Hear this moment**. Move to a recent year and listen again. | NASA GISTEMP reports −0.18 °C in 1880 and +1.28 °C in 2024 relative to 1951–1980. A higher anomaly produces a higher note. The January–October 2026 point is a partial mean. |
| 1:00 | Press **Compare this year in Simulator**, raise CO₂ and watch the modeled warming change. | The NASA reading in the timeline keeps its original value. |
| 1:15 | Enter the **16-Bit Eco-Quest RPG** and press **E** to open Spark’s renewable grid quest, or use **Quests** to visit Flora and open her GEDI track from the room HUD. | The game links to NASA science, while restoration rewards change the educational scenario and soundtrack. |

## Verified resource inventory

The [public challenge description](https://www.spaceappschallenge.org/2026/challenges/the-earth-information-jukebox/) asks teams to pair EIC visual frames with dynamically generated sonification. The [official Resources tab](https://www.spaceappschallenge.org/2026/challenges/the-earth-information-jukebox/?tab=resources) returned HTTP 503 during direct retrieval and failed to load in the browser. A staging version exposed an unrelated exoplanet resource list. That list was excluded, and no entries were attributed to the production Resources tab. NASA’s [Earth Information Center gallery](https://svs.gsfc.nasa.gov/gallery/earth-information-center/) independently verifies that ECCO2 and GEDI are EIC visualizations.

| Track or guide | Verified source and bundled material | Coverage and units |
| --- | --- | --- |
| Ocean Currents | NASA SVS 3912, *Global Sea Surface Currents and Temperature*. Bundled H.264 animation and sampled frame features. [NASA product and credits](https://svs.gsfc.nasa.gov/3912/) · [Exact source movie](https://svs.gsfc.nasa.gov/vis/a000000/a003900/a003912/ecco2_sst_flow.m4v) | Global ocean surface, 25 March 2007 at 12:00 UTC to 3 March 2008 at 12:00 UTC. ECCO2 combines observations with an ocean model. The frames depict currents colored by sea-surface temperature. Jukebox inputs are image statistics in percent. |
| Forest Canopy | NASA SVS 4950, *GEDI Forest Height*. Bundled globe rotation, preview and sampled frame features. [NASA product and credits](https://svs.gsfc.nasa.gov/4950/) · [Exact source movie](https://svs.gsfc.nasa.gov/vis/a000000/a004900/a004950/GEDI_global_w_colorbar_1080p60.webm) | Global rendering of GEDI lidar observations collected April 2019–April 2020. The source color bar shows height above ground in meters. The camera rotates through one survey, with exaggerated heights. The audio uses vegetation brightness and its spread. |
| Soil & Water | Seven NASA GIBS maps from the enhanced daytime SMAP Level 3 product. The application links directly to the dated WMS image currently on screen. [SPL3SMP_E v6](https://doi.org/10.5067/M20OXIZHY3RJ) · [Example bundled map](https://gibs.earthdata.nasa.gov/wms/epsg4326/best/wms.cgi?SERVICE=WMS&VERSION=1.3.0&REQUEST=GetMap&LAYERS=SMAP_L3_Passive_Enhanced_Day_Soil_Moisture&STYLES=&FORMAT=image%2Fpng&TRANSPARENT=TRUE&CRS=EPSG%3A4326&BBOX=-60,-180,85,180&WIDTH=900&HEIGHT=362&TIME=2024-06-04) · [NASA GIBS legend](https://gibs.earthdata.nasa.gov/legends/SMAP_Soil_Moisture_H.png) | 6 January, 12 February, 15 April, 4 June, 5 August, 7 October and 9 December 2024. Enhanced estimates are posted to a 9 km grid. The bundled maps span 85° N to 60° S and use a legend in cm³/cm³. Blue Marble supplies the basemap. Blank swaths indicate missing visible retrievals. |
| Climate Through Time | NASA GISS GISTEMP v4 global Land–Ocean Temperature Index. The original CSV and the browser’s compact derivative are both bundled. [Data documentation](https://data.giss.nasa.gov/gistemp/data_v4.html) · [Exact global CSV](https://data.giss.nasa.gov/gistemp/tabledata_v4/GLB.Ts+dSST.csv) | Annual values for 1880–2025, plus available monthly values for January–October 2026. All anomalies are in °C relative to 1951–1980. |
| Ocean Color | NASA SVS 5690, PACE apparent visible wavelength (AVW). Six NASA renderings converted to browser-ready JPGs. The app links each map to its exact original EXR. [NASA product](https://svs.gsfc.nasa.gov/5690/) · [Original dated frames](https://svs.gsfc.nasa.gov/vis/a000000/a005600/a005690/frames/4096x2048_2x1_30p/avw/) | 30-day composites dated 1 June, 15 August and 1 October 2024, 1 February and 1 July 2025, and 1 October 2026. The NASA maps report AVW in nanometers. The audio uses the share of green-dominant pixels. |
| Industrial Outskirts guide | NASA SVS DYAMOND CO₂ transport preview with OCO-2 mission context. [NASA SVS product](https://svs.gsfc.nasa.gov/5196/) · [Exact preview](https://svs.gsfc.nasa.gov/vis/a000000/a005100/a005196/dyamondPointCloud_12-1-2023b_dyamond_co2_anim_globe_orbit_3x3Hyperwall.00200_web.png) · [NASA OCO-2](https://science.nasa.gov/mission/oco-2/) | The preview depicts modeled global CO₂ in ppm from January–March 2020. OCO-2 retrieves column-averaged atmospheric CO₂ in ppm. The mini-game changes the scenario’s grid. |
| Coral Coastline guide | NASA SWOT mission explanation and link from the quest. [NASA SWOT](https://science.nasa.gov/mission/swot/) | SWOT measures water-surface elevation. The shoreline cleanup is an educational quest. |

**SMAP citation.** P. E. O’Neill, S. Chan, E. G. Njoku, T. Jackson, R. Bindlish, J. Chaubell & A. Colliander (2023), *SMAP Enhanced L3 Radiometer Global and Polar Grid Daily 9 km EASE-Grid Soil Moisture*, SPL3SMP_E v6. NASA NSIDC DAAC. Subset is the seven dated GIBS maps listed above. Accessed 13 November 2026. [DOI 10.5067/M20OXIZHY3RJ](https://doi.org/10.5067/M20OXIZHY3RJ)

Visuals are credited in the app to NASA’s Scientific Visualization Studio, the visualization teams and the underlying missions. The source pages retain their full credit lists. The project is an independent hackathon entry. [NASA media guidance](https://www.nasa.gov/nasa-brand-center/images-and-media/)

## How the sound is generated

The application reuses its Web Audio oscillators, sequencer, filters, and spectrum. In NASA Observations it passes data from the selected track into those nodes. The simulator and RPG use the original rendered scenes and game state for their soundtrack.

| Input | Audio mapping |
| --- | --- |
| ECCO2 | Mean absolute RGB change over current-colored pixels between adjacent samples sets tempo. A fixed 1.0–3.2% span maps to 68–140 BPM, with clamping at the endpoints. The red/yellow pixel share maps 48–56% to MIDI 49–65. The brightness-weighted horizontal center pans the notes. |
| GEDI | Mean brightness of vegetation-colored pixels maps 25–45% to MIDI 48–67. Brightness spread maps 10–20 percentage points to an 850–3300 Hz low-pass cutoff. |
| SMAP | Blue/cyan share of colored valid pixels maps 20–30% to 74–116 BPM and a 700–3200 Hz low-pass cutoff. |
| GISTEMP | The anomaly maps linearly from −0.60 to +1.80 °C to MIDI 48–76, rounded to a semitone. Tempo is fixed at 96 BPM. |
| PACE | Green-dominant share maps 22–32% to MIDI 48–65 and a 900–3700 Hz low-pass cutoff. |

Musical ranges are artistic choices. The browser samples available ECCO2 and GEDI video frames on a 96 × 48 grid, four times per playback second. The bundled `assets/observations.json` contains corresponding samples computed from the same videos. A seek can use the bundled adjacent-frame difference until the browser has consecutive frames. If a clip fails to decode, the app shows its first NASA frame and uses the matching bundled sample. Maps use the same grid, with missing/gray cells and map overlays excluded by color, alpha, or position masks. The app computes pitch, tempo and filter from those features as the visitor changes the date.

The ocean date cursor linearly estimates date within the published range from clip progress. Pixel change is a visual motion proxy, so it can vary with rendering, compression and sampling. The GEDI camera rotation changes which region and lighting are visible. PACE and SMAP color shares reflect imagery and available coverage. The image statistics are expressed in percent or percentage points. Physical units remain on the product legends and in the GISTEMP record.

The GISTEMP derivative copies published January–December values from the `J-D` column and retains available months where the annual field is missing. The January–October 2026 point is the arithmetic mean of the ten published months, rounded for display. The app displays the individual monthly readings in the climate track. The record contains no filled annual value for 2026. The CSV and processed data are bundled together for audit.

The ocean clip is remuxed from NASA’s source. GEDI was resized to 896 × 504 and encoded at 24 fps. PACE EXR maps were converted to sRGB JPEGs at 1024 × 512 with their dates and legends retained. SMAP renders are the dated GIBS PNGs. No media soundtrack is bundled.

## Simulator and RPG methodology

The original timeline spans 1750–2100. Its gas concentrations are illustrative, piecewise linear inputs, with separate post-2026 trajectories for the two intervention settings. The 2100 baseline ends at 700 ppm CO₂ and 3.00 ppm CH₄. Intervention ends at 360 ppm CO₂ and 1.50 ppm CH₄. For the effective CO₂ input c, the toy model calculates an initial response of `1.35 × log₂(c / 280) + 0.35 × (CH₄ − 0.72)`, followed by a bounded ice index and a simple feedback term. Grid choice shifts the effective CO₂ proxy in this formula. The O₂ slider is a scenario input used as a proxy in the fish-health illustration.

Reef, fish, soil, forest, ice, air stress and biodiversity values are game or scenario indices. Sea-level change is an illustrative response calculated from the warming and ice indices. The toy temperature response is referenced to a nominal pre-industrial input of 280 ppm and has a different reference from GISTEMP. Read the scenario and NASA baseline labels when comparing a year. Before 1880 and after the observation snapshot, the timeline displays scenario values and explains where GISTEMP coverage ends.

The simulator illustrates greenhouse warming, ice reflectivity and the direction of ocean acidification. Coral bleaching can occur during prolonged heat stress. Acidification affects carbonate chemistry and can make it harder for organisms to build shells and skeletons. The Paris temperature goal describes long-term warming above pre-industrial levels. The reef cauldron’s pH target is a game mechanic. Switching modes or completing a quest leaves the NASA source data intact.

## Verification and limits

- Checked all eight companion selections, custom naming, both entry modes, five simulator biome views, grid controls, year bounds, and the intervention toggle.
- Cross-checked 1880, 2024 and 2025 against the NASA CSV and verified the separate 2026 partial mean. Confirmed that changing simulated CO₂ or restoring an RPG room leaves GISTEMP unchanged.
- Checked playback, pausing and seeking, mapped note and filter changes on the NASA tracks, mute controls, visible spectrum output, Kharita, and a 390 px layout in Chromium.
- Verified movement through a room portal, fast travel to all five rooms, spirit interaction, and completion of all five restoration mini-games in Chromium.
- The production challenge resource list could not be verified. This build uses the official NASA EIC gallery and documented NASA/NSIDC products. OCO-2 and SWOT are field-guide references. No raw OCO-2 or SWOT layer is bundled.
