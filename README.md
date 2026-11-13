# freecad-resources

Macros, a colour scheme and a spreadsheet template for FreeCAD.

## Macros

Each macro hides helper geometry so a model or assembly can be looked at or
screenshotted without it. They set `Visibility` to false and nothing shows the
objects again; select them in the tree and press Space to bring them back.

| Macro                         | Hides in the active document                | Hides in linked documents          |
| ----------------------------- | ------------------------------------------- | ---------------------------------- |
| `scripts/hide_lcs.py`         | objects labelled `LCS_*`                    | objects labelled `LCS_*`           |
| `scripts/hide_sketches.py`    | sketches                                    | sketches                           |
| `scripts/hide_linked_axes.py` | nothing                                     | objects labelled `Axis_*`          |
| `scripts/hide_all.py`         | objects labelled `LCS_*`, and sketches      | `LCS_*`, `Axis_*` and sketches     |

"Linked documents" are the documents that the `App::Link` objects in the
active document point to. The macros hide matching objects throughout those
documents, not only the linked object. A link with no target is skipped.

To install, copy the files into your user macro folder (Macro → Macros…
shows where it is), then run them from that dialog or add them to a toolbar
under Tools → Customize → Macros.

## Colour scheme

Based on Flowwie's FreeCAD 0.19 colour scheme (March 2021) by Florian of
[Flowwie's Corner](https://youtube.com/flowwiescorner) /
[FreeCAD Academy](https://youtube.com/freecadacademy), with my own changes.

### Sketcher, working colours

| Setting         | Hex       |
| --------------- | --------- |
| Creating line   | `#cccccc` |
| Coordinate text | `#0000ff` |
| Cursor cross    | `#ffffff` |

### Sketcher, geometric elements

| Setting                 | Constrained | Unconstrained |
| ----------------------- | ----------- | ------------- |
| Edge                    | `#86f963`   | `#0f2873`     |
| Vertex                  | `#ff9580`   | `#aa0000`     |
| Construction geometry   | `#8fa9fd`   | `#2240a0`     |
| Internal alignment edge | `#dedec8`   | `#b2b27f`     |

| Setting                  | Hex       |
| ------------------------ | --------- |
| External geometry        | `#cd3273` |
| Fully constrained sketch | `#00c800` |
| Invalid sketch           | `#ff6d00` |

### Sketcher, constraints

| Setting                         | Hex       |
| ------------------------------- | --------- |
| Constraint symbols              | `#aa0000` |
| Dimensional constraint          | `#aa0000` |
| Reference constraint            | `#2240a0` |
| Expression dependent constraint | `#cd3273` |
| Deactivated constraint          | `#7f7f7f` |

### Outside the Sketcher

| Setting | Hex       |
| ------- | --------- |
| Edge    | `#ffffff` |
| Vertex  | `#ffffff` |

### Display

| Setting                          | Hex       |
| -------------------------------- | --------- |
| Enable preselection highlighting | `#e1e114` |
| Enable selection highlighting    | `#005500` |

## Dimension spreadsheet template

`templates/FreeCAD_dimension_template_mm` is a blank table of named dimensions
with columns for the name, the value in millimetres, the value in inches
(computed from the millimetres), an expression and notes. It has 500 rows. The
`.ods` is for LibreOffice and the `.xlsx` is for FreeCAD's spreadsheet import.

## License

MIT. See [LICENSE](./LICENSE).
