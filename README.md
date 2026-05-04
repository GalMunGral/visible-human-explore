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

`DICOM.ipynb` loads the raw DICOM slices and implements interactive reslicing along all three
axes — a first check that the data loaded correctly and that the spatial orientation is as
expected. `PyVista.ipynb` renders the volume directly, establishing what the data looks like
under volume rendering before implementing it from scratch in WebGL. `PNG.ipynb` is a
conversion step that follows exploration: it normalizes the DICOM slices to PNG textures,
which is the format the browser can load directly in
[visible-human-gl](https://github.com/GalMunGral/visible-human-gl) and
[visible-human-volume](https://github.com/GalMunGral/visible-human-volume).