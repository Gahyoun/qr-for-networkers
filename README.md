# QR for networker

Express our field with a QR code :)

[Open QR for networker](https://gahyoun.github.io/qr-for-networkers/)

Turn a URL into a scannable QR code with rounded nodes and links between adjacent dark modules. Choose orthogonal neighbors, diagonal neighbors, or both. Pick a preset or enter up to eight HEX or RGB colors. You can also open `index.html` directly in a browser and use the generator offline.

## Sample the links

Open **Link sampling** to choose a model.

| Model | How it chooses links |
| --- | --- |
| Connected | Builds a spanning forest for each connected component of the candidate graph, then adds links while limiting crossings and crowding. |
| Bernoulli | Includes each eligible link independently with probability `p`. The number of selected links can vary between samples. |
| Fixed count | Draws exactly `k` distinct eligible links without replacement. The available pool sets the maximum. |

The candidate graph comes from the QR matrix and the active neighbor switches. With crossings switched off, Bernoulli and Fixed count use a fixed pool that includes at most one diagonal per grid cell. These two methods can produce disconnected networks.

Use **Resample links** to draw a new set of edges while keeping the nodes in place. Re-enter a link seed to reproduce the edge set for the same URL, neighbor switches, model, sampling settings, and randomness level. Use **Shuffle** to vary both node placement and links.

## Export and edit

Download a 1536 × 1536 PNG, SVG, vector PDF, or legacy Illustrator AI file. The SVG contains individually editable vector paths grouped as `nodes`, `nearest-neighbor-links`, and `diagonal-links`. The background, halos, and QR reference patterns have their own groups.

In Adobe Illustrator, use **File → Open** to open the SVG. Use the **Layers** panel to select a group, or **Direct Selection** (`A`) to select an individual node or link inside a group. [Adobe's guide to object selection](https://helpx.adobe.com/illustrator/desktop/manage-objects/select-objects/object-selection-methods-and-preferences.html)

## License

The application is available under the [GNU General Public License v3.0 or later](LICENSE). You can use it for any purpose. The GPL sets the terms for redistributing the code and modified versions. The bundled `qrcode-generator` library carries its MIT notice in the source.

The project's rights in generated QR artwork are dedicated to the public domain under [CC0 1.0 Universal](https://creativecommons.org/publicdomain/zero/1.0/). You can reuse or remix the artwork, including commercially, without attribution. Content linked from a QR code has its own rights.

> Why GNU? The creator is a Gyeongsang National University (GNU) alum. The acronym was too good to pass up. :)
