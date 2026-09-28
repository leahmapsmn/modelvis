# modelvis

A browser-based tool that turns ArcGIS ModelBuilder Python exports into clean, readable workflow diagrams showing model inputs, geoprocessing tools, parameter values, and outputs.

## Why This Exists

This project was originally created as a teaching tool for **GEOG 350: Geography of Global Health** at the University of St. Thomas. Students needed a clearer way to document what they built in ModelBuilder—including the settings used inside each tool—without submitting a pile of screenshots. She also lowkey wanted it for herself, so that in the future, she could document what she did in her models with out needing to go back through geoprocessing history or writing it down on 28 sticky notes. This is a happy medium for her, okay?

The visualizer creates a shareable “model receipt” that can be included in assignments, reports, presentations, or project documentation.

## Features

- Opens Python files exported from ArcGIS ModelBuilder
- Identifies model inputs, tools, parameters, connections, and outputs
- Translates supported positional ArcPy arguments into readable ModelBuilder-style labels
- Produces horizontal or vertical workflow layouts
- Exports diagrams as PNG or SVG
- Supports transparent PNGs or a custom background color using a hex code
- Provides a print option for saving as PDF
- Runs entirely in the browser—no installation or server required

## How to Use It

1. In ArcGIS Pro, open the model in ModelBuilder.
2. Export the model to a Python file (`.py`).
3. Open the Model Workflow Visualizer.
4. Select **Open exported .py** and choose the exported file.
5. Choose a horizontal or vertical layout.
6. Export the finished workflow as PNG, SVG, or PDF.

## Privacy

The selected Python file is processed locally in the browser. It is not uploaded to GitHub, stored on a server, or transmitted elsewhere by this tool.

## Current Limitations

- The visualizer reconstructs the logical workflow and does not preserve the exact manual arrangement used inside ModelBuilder.
- ArcPy calls that use named parameters can generally be labeled automatically.
- Positional arguments require tool-specific mappings. Unsupported tools may temporarily display labels such as `Argument 1` or `Argument 2` until a mapping is added.
- Complex Python logic that was added after exporting from ModelBuilder may not be represented completely.

## AI Development Disclosure

This project was created collaboratively with **ChatGPT by OpenAI**. The human creator provided the original idea, classroom use case, requirements, testing, screenshots, bug reports, and design feedback. ChatGPT generated and iteratively refined a substantial portion of the HTML, CSS, and JavaScript.

In other words: a GIS instructor had a very specific problem, and ChatGPT was repeatedly told when the solution looked weird until it stopped looking weird.

## Esri Disclaimer

This is an independent educational utility and is not affiliated with, endorsed by, or maintained by Esri. ArcGIS, ArcGIS Pro, ModelBuilder, and ArcPy are trademarks or registered trademarks of Esri.

## License

This project is available under the [MIT License](LICENSE).

