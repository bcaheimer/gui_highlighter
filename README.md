# gui_highlighter

## How to run
  Put *gui_highlighter.py* in the same directory as the xml/png files to be proccessed. Assure that each xml/png pair follows the naming convention *<app.package>-<screen#>.ext*. Then, run `python gui_highlighter filename1 filename2...` where *filename* corresponds to *<app.package>-<screen#>* for each xml/png pair.

## Output
 Annotated images can be found in the *gui_highlighter_output* folder of the current directory.

## Description
  *gui_highlighter.py* utilizes python's ElementTree module to parse inputted xml files and represent them as trees. It iterates through these trees to find leaf nodes, then stores the boundary coordinates of the corresponding GUI elements. Finally, it uses PIL to draw rectangles at these coordinates over the inputted png files, and saves the resulting images.

###### Note
  Per the discussion on Piazza, I fixed *com.apalon.ringtones.xml* by adding a closing `</node` tag.
