# ROMS-CSTMS
(Nechad Model – Bay of Bengal)

The semi-empirical turbidity algorithm developed by Benoît Nechad is widely applied for estimating suspended sediment concentration (SSC) in optically complex coastal waters. The model establishes a nonlinear relationship between water-leaving reflectance in the red or near-infrared wavelengths and suspended particulate matter, using calibration coefficients derived from in situ measurements. It has been successfully adapted for sensors such as Sentinel-2 and Landsat-8 through atmospheric correction frameworks like ACOLITE, enabling robust SSC retrieval in highly turbid environments.

In the Bay of Bengal, characterized by intense riverine sediment discharge, strong monsoonal forcing, and highly stratified waters, the Nechad model performs particularly well due to the high optical signal associated with suspended sediments. However, its accuracy depends strongly on regional calibration of coefficients (A and C), as default values may not capture the variability in sediment composition and optical properties. Additionally, the model exhibits limitations at very high turbidity levels, where reflectance saturation can lead to underestimation or instability in SSC retrieval.

Overall, the Nechad model provides a reliable and computationally efficient approach for mapping sediment plumes and validating numerical models such as ROMS-CSTMS, especially when combined with in situ observations and regional tuning.

1. Nechad Model

✅ Works well in moderate–high turbidity

✅ Simple single-band approach

❌ Needs regional calibration

❌ Saturation at extreme SSC

2. Dogliotti Model

Uses band switching (Red → NIR)

Better for:

Extremely turbid waters

Often preferred when:

River plume is very dense

👉 Studies show it switches methods at high turbidity, improving performance where Nechad struggles

3. Semi-analytical / multi-band models

More physics-based

Better in:

Mixed optical waters (CDOM + chlorophyll)

But:

More complex

Requires more inputs

🌊 Why Nechad is Still Preferred for Bay of Bengal

Despite limitations, Nechad is widely used because:

🔹 High sediment load region

Bay receives massive sediment input

Reflectance signal is strong → model stable

🔹 Data availability

Works with:

Sentinel-2

Landsat

Easy integration with your workflow

🔹 Computational efficiency

Ideal for:

Large spatial maps

Time-series analysis

 Key Scientific Insight 

In the Bay of Bengal, the Nechad model is most effective when used as part of an integrated framework, combining river discharge (rating curves) and numerical models (ROMS), rather than as a standalone SSC estimator.

“Although the Nechad model provides reliable SSC estimates in turbid coastal waters, its performance in the Bay of Bengal is enhanced when combined with hydrological forcing and numerical modeling, highlighting the importance of multi-source integration in sediment dynamics studies.”
