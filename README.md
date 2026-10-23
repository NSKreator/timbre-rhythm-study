# Timbre & Rhythm

Interactive results from Nicholas's study of 100 songs: 50 New Age of House and 50 Tech House, grouped by the researcher.

[Open the interactive study](https://nskreator.github.io/timbre-rhythm-study/)

## Explore

Choose from six plots, search by artist or title, select individual songs, and download the current graph as a PNG image. The summary plots manual sixteenth-note swing against spectral PC1, with spectral PC2 shown by color. PCA uses the three spectral features only.

## Files

- `index.html`: the self-contained interactive page, with all 100 plotted records embedded.
- `results.csv`: measurements and methodology fields; local annotation directory paths are removed, while basenames and all measurement values are preserved.
- `pca/`: model, component weights, explained variance, and song scores.
- `PCA_INTERPRETATION.md`: component meanings, methodology, and limitations.

The model's `source_results_sha256` refers to the original local results table before removal of annotation directory paths.

## Interpretation

Groups were assigned by the researcher. PCA scores do not automatically classify genre or establish causation. Manual grid labels remain provisional as described in the study notes. Source audio and original annotation files are not part of this website.

## Hosting and updates

GitHub Pages serves the root of the `main` branch. Update these website files on that branch to publish changes. No build step or external JavaScript dependency is required.

To preview locally, serve this folder with any static HTTP server, or open `index.html` directly in a browser.
