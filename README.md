<p align="center"><img src="logo.svg" width="96" alt="HANGTAG logo"></p>

# HANGTAG

**PA prep from Soundvision files: hangs, angles and dolly tags.**

HANGTAG is a single-page web app. Import an L-Acoustics Soundvision file and it works out:

- **Inventory:** how many boxes of each model are in the design, which hangs use them, which fly bars are needed and how many dollies to prep.
- **Hangs & angles:** each hang or stack, whether it's flown or ground stacked, the fly bar, which way the fly bar faces, the pickup hole, the site angle, the trim and the splay angle of every box. Each hang also gets a side-view drawing.
- **Printout:** a full prep sheet with all of the above, ready to print or save as a PDF.
- **Dolly labels:** set how many boxes of each model go on a dolly. HANGTAG then prints a label for every dolly showing:
  - which hang it belongs to (e.g. *MAIN L – DOLLY 2/3*)
  - the box numbers on that dolly and the angle for each box
  - the angle linking its top box to the dolly above
  - the fly bar, direction and hole, on the first dolly only

## Using it

Open `index.html` in Chrome, Edge, Safari or Firefox. There's nothing to install, and it works offline. Files are read in your browser and never uploaded anywhere.

1. **Import & Inventory:** drop in a Soundvision file (`.xmlp`, `.xml` or zipped), or click **Load demo show** to try it out.
2. **Hangs & Angles:** check and edit anything the importer missed. Every field can be edited, and hangs can be added, duplicated and reordered.
3. **Printout:** print the prep sheet.
4. **Dolly Labels:** set the boxes per dolly for each model, choose a label size (1, 2, 4 or 6 per A4 page) and print.

Your current show is remembered in the browser. Use **Save project** and **Open project** to keep a show as a `.json` file or move it to another computer.

## About Soundvision files

L-Acoustics doesn't publish the Soundvision file format, so HANGTAG reads the file flexibly. It looks for known L-Acoustics model names, plus fields that look like angles, bumpers or fly bars, pickup points, orientation and stacked or flown. Always check the Hangs tab before printing. The **raw data explorer** on the first tab shows everything that was found in the file.

The default boxes-per-dolly numbers are only starting points. Set them to match your own dollies.
