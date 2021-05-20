# KODAMA
## Re-exploring BHL's archives
---

[Biodiversity's Heritage Library](https://www.biodiversitylibrary.org)'s archives represent an enormous collection of digitized books from the 15th-21st centuries. It is the world's largest open access digital library for biodiversity literature, hosting over 59 millions pages from hundreds of thousands of volumes.
This notebooks presents an attempt to valorize this priceless heritage using computational methods and dynamic visualizations. A 3D tree of life, with leaves blooming into the stunning scientific illustrations contained in these archives, is developped to allow anyone to wander freely through this database.

The dataset used here was built upon a sample of the illustrations posted by [BHL on Flickr](https://www.flickr.com/people/biodivlibrary/) — to enrich pictural content with metadata (specie taxonomy, artist informations, ...) through crowdsourcing — via Flickr's API. The content was then augmented with taxonomic informations thanks to [NCBI](https://www.ncbi.nlm.nih.gov) database which allowed to retrieve all 6 main taxonomic ranks from the specie level (harvested from Flickr's machine tags) up to the domain (Eukarya).

---

This repository hosts two visualizations available as standalone applications, developped as a semester project for the [Cultural Data Sculpting](https://edu.epfl.ch/coursebook/en/cultural-data-sculpting-DH-404) class of EPFL (Lausanne, Switzerland). Both of them rely on the Force Graph library developped by Vasco Asturiano (vasturiano).

The [first one](https://noe-d.github.io/KODAMA), is a 3D-tree of life whose leaves bloom into the collected illustrations archived by the BHL when clicked. It is built with [3D Force-Directed Graph](https://github.com/vasturiano/3d-force-graph), which uses [d3-force-3d](https://github.com/vasturiano/d3-force-3d) for the physics of the graph and [ThreeJS](https://github.com/mrdoob/three.js/) to render it.
Possible interactions with the components of the tree are the following:
- left-click on node: focus on node
- left-click on leaf: display all illustrations that share the same taxonomic class as the clicked leaf
- right-click on leaf: display caption below the illustration (name of the artist, title of the book containing the illustration, year of publication of the book) — caveat: book title and date of publication have been harvested from Flickr's descriptions and might not be totally accurate
- cmd+click or ctrl+click on leaf: open in new window the page of the illustration within the book it originally appeared, on the archived volume hosted on BHL website (please use this command if you want more correct and more complete informations than displayed in the caption)
- left-click on link: focus on target node

The [second one](https://noe-d.github.io) is a coarse extension of the first tree into an AR module. It was implemented thanks to [3D Force-Directed Graph in AR](https://github.com/vasturiano/3d-force-graph-ar) which makes use of [AR.js](https://github.com/jeromeetienne/AR.js) with [A-frame](https://aframe.io) for rendering.

---

Use the following links to explore these propositions of visualization of BHL's archives:
1. [KODAMA — 3D tree](https://noe-d.github.io/KODAMA): https://noe-d.github.io/KODAMA
2. [KODAMA — AR extension](https://noe-d.github.io): https://noe-d.github.io

<sub>Disclairmer: the visualization window might not show the full canvas when not seen in fullscreen.<\sub>
