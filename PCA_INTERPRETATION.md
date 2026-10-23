# Spectral PCA interpretation — Analyze TA Nicholas

PCA was fitted to z-standardized mean spectral centroid, spectral bandwidth,
and 85% spectral rolloff for 100 songs. Eighth and sixteenth swing
ratios are displayed separately and have **no input to PC1 or PC2**.

| Input feature | PC1 score weight | PC2 score weight |
|---|---:|---:|
| Centroid | +0.573773 | -0.645118 |
| Bandwidth | +0.566906 | +0.757476 |
| Rolloff (85%) | +0.591102 | -0.100264 |

PC1 explains **94.38%** of spectral variance. Overall spectral brightness and high-frequency extent. Higher PC1 means higher centroid, bandwidth, and rolloff together; lower PC1 means a darker, less extended spectrum.

PC2 explains **5.14%** of spectral variance. A secondary spectral-spread contrast: positive PC2 emphasizes bandwidth relative to centroid. Read it as a contrast after the overall brightness represented by PC1 is accounted for. PC2 = -0.645118 × z(centroid) +0.757476 × z(bandwidth) -0.100264 × z(rolloff). z means subtracting this study's mean and dividing by its standard deviation. Yellow is higher PC2; purple is lower PC2. Zero is the centered spectral-contrast score, not a straight rhythm. PC2 does not measure swing or song quality.

Together these components retain **99.53%** of variation in
the three standardized spectral measurements. Weights apply to
`z = (feature - study_mean) / population_SD`; scores are unitless.

In the summary, x is manual sixteenth-note swing, y is spectral PC1, and color
is spectral PC2. Purple is low PC2; yellow is high PC2. Color is not a swing
measurement. The website and PNG/SVG use the same viridis palette and score range.
The website also takes its axis limits and color ticks from the exported figure;
the horizontal legend and dark background do not change the measurements.

This matches the old chart's **spectral-only PCA method**. Values can differ
from that automated study because spectra now cover the first-to-last manual
annotation extent, rather than its automatic beat-grid passage. Refitting on
different passages can change means, weights, and variance shares. The old
study's 93.78% and 5.75% are not reused as if they described this run.

Manual timing uses nearest-sixteenth placement and the mean of individual
offbeat ratios against fixed boundaries. A ratio of 1 means an exact midpoint;
values above 1 indicate later placement, and below 1 earlier placement. Overall
delay relative to the grid also affects this metric. Confirm that annotation
tempo and audio origin describe the same export when using these in the thesis.
Automatically inferred note positions remain provisional until reviewed.

PCA scores do not define genre or prove causation. Component signs are a
reproducible convention; reversing a component changes no relationships.
Full-precision weights, scaling, and scores are saved in `pca/`.

## Suggested thesis wording

Principal component analysis was applied to the standardized means of spectral
centroid, spectral bandwidth, and 85% spectral rolloff across 100
manually annotated song passages. PC1 explained 94.38% of spectral
variance and was interpreted as overall spectral brightness and high-frequency
extent. PC2 explained 5.14% and represented a secondary contrast in
spectral spread. These components explained 99.53% together.
Manual sixteenth-note timing was plotted alongside the spectral PCA scores and
was not used to fit either component.
