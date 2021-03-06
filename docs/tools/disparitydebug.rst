.. _disparitydebug:

disparitydebug
--------------

The ``disparitydebug`` program produces output images for debugging
disparity images created from ``stereo``. The ``stereo`` tool
produces several different versions of the disparity map; the most
important ending with extensions ``*-D.tif`` and ``*-F.tif``. (see
:numref:`outputfiles` for more information.) These raw disparity
map files can be useful for debugging because they contain raw
disparity values as measured by the correlator; however they cannot
be directly visualized or opened in a conventional image browser.
The ``disparitydebug`` tool converts a single disparity map file
into two normalized TIFF image files (``*-H.tif`` and ``*-V.tif``,
containing the horizontal and vertical, or line and sample, components
of disparity, respectively) that can be viewed using any image
display program.

The ``disparitydebug`` program will also print out the range of
disparity values in a disparity map, that can serve as useful summary
statistics when tuning the search range settings in the
``stereo.default`` file.

If the input images are map-projected (georeferenced), the outputs of
``disparitydebug`` will also be georeferenced.

Command-line options for disparitydebug:

-h, --help
    Display the help message.

--input-file <filename>
    Explicitly specify the input file.

-o, --output-prefix <filename>
    Specify the output file prefix.

-t, --output-filetype <type (default: tif)>
    Specify the output file type.

--float-pixels
    Save the resulting debug images as 32 bit floating point files
    (if supported by the selected file type).
