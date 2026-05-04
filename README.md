# Visible Human: Exploratory Visualization

## Rhetorical Design

### Purpose

For an audience familiar with polished visualizations — interactive apps, rendered videos,
publication figures — we demonstrate that visualization also has an instrumental mode: the
initial exploration of a dataset before any representational decisions have been made. The
goal here is not to communicate but to understand. Three notebooks use PyDICOM, matplotlib,
and PyVista to rapidly slice and render the
[Visible Human Project](https://www.nlm.nih.gov/research/visible/visible_human.html) CT
volume. The speed of scripting against existing libraries is the point: many representations
can be tried in an afternoon, which is what the exploratory phase requires.

### Strategy

These notebooks were the actual preliminary work behind
[visible-human-vtk](https://github.com/GalMunGral/visible-human-vtk),
[visible-human-gl](https://github.com/GalMunGral/visible-human-gl), and
[visible-human-volume](https://github.com/GalMunGral/visible-human-volume). `DICOM.ipynb`
reads the raw DICOM files and adds interactive sliders to scrub through axial, coronal,
and sagittal planes — verifying the data and developing an initial sense of its structure.
`PyVista.ipynb` produces a quick volume rendering, previewing how the dataset responds to
transfer functions before any WebGL implementation. `PNG.ipynb` converts the slices to
normalized PNG textures for use as WebGL inputs in the production demos.