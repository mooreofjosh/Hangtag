<p align="center"><img src="logo.svg" width="96" alt="HANGTAG logo"></p>

# HANGTAG

**PA prep from Soundvision files: hangs, angles and dolly tags.**

HANGTAG is a single-page web app. Import an L-Acoustics Soundvision file and it works out:

- **Inventory:** how many boxes of each model are in the design, which hangs use them, which fly bars are needed, how many dollies to prep, and how many boxes need each Panflex setting.
- **Hangs & angles:** each hang or stack, whether it's flown or ground stacked, the fly bar, which way the fly bar faces, the pickup hole, the site angle, the trim, and the splay angle and **Panflex** setting of every box. Each hang also gets a to-scale side-view drawing marked with its **centre of gravity** and approximate weight.
- **Printout:** a full prep sheet with all of the above, ready to print or save as a PDF.
- **Dolly labels:** set how many boxes of each model go on a dolly. HANGTAG then prints a label for every dolly showing:
  - which hang it belongs to (e.g. *MAIN L – DOLLY 2/3*)
  - the box numbers on that dolly, with the angle and Panflex setting for each box
  - the angle linking its top box to the dolly above
  - the fly bar, direction and hole, on the first dolly only

## Using it

Open `index.html` in Chrome, Edge, Safari or Firefox. There's nothing to install, and it works offline. Files are read in your browser and never uploaded anywhere.

1. **Import & Inventory:** drop in a **Soundvision PDF report**, or click **Load demo show** to try it out.
2. **Hangs & Angles:** check and edit anything the importer missed. Every field can be edited, and hangs can be added, duplicated and reordered.
3. **Printout:** print the prep sheet.
4. **Dolly Labels:** set the boxes per dolly for each model, choose a label size (1, 2, 4 or 6 per A4 page) and print.

Your current show is remembered in the browser. Use **Save project** and **Open project** to keep a show as a `.json` file or move it to another computer.

## About Soundvision files

Soundvision project files (`.xmlp`) are encrypted, so only Soundvision can open them. Export a **report** from Soundvision instead and drop the PDF into HANGTAG. It reads each source's:

- group, name, and whether it's flown or stacked, vertical or side by side
- fly bar and its direction (`L2-BAR hole A` = normal, `hole B` = reversed), the pickup hole on the bar (`Front pickup position: 3` = hole 3), number of motors and motor load
- box models, the site of each box (from which the angles between boxes are worked out) and Panflex settings for every module
- trim (bottom elevation), total weight and mechanical warnings

Box 1's angle to the fly bar isn't in the report, so it's set to 0°. Check it on the Hangs tab.

Site angles follow Soundvision: positive aims up.

Reading PDFs uses [pdf.js](https://mozilla.github.io/pdf.js/) (Apache 2.0), bundled in `vendor/`. If `index.html` is opened on its own without that folder, HANGTAG loads pdf.js from cdnjs instead, which needs an internet connection.

## Centre of gravity

The centre of gravity is calculated from each box's height, depth and weight and from the angles in the hang. It includes the boxes only, not the fly bar, motors or cable. The built-in sizes and weights are approximate. Check them against the current L-Acoustics spec sheets and correct them under **Box sizes & weights** on the Hangs tab. For rigging decisions, Soundvision's own mechanical data is the authority.
