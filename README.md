
Vessel Analyzer
in MATLAB (R2021a; MathWorks\'ae), which quantifies EC and vessel morphology. \
\
Required toolboxes: Image Processing Toolbox and Curve Fitting Toolbox.\
\
For each user-selected vessel segment (here, a portion of the DA), first upload the image showing EC junction signals, followed by the image showing the EC membrane marker. Then, select the relevant portion of the DA as the ROI.\

The app automatically identifies the outer and luminal vessel boundaries and the lumen center in cross-sections orthogonal to the vessel axis. The software then maps EC junctions onto a cylindrical representation of the vessel surface and computationally unwraps them into a 2D plane. To segment junctions crossing the 0\'b0 boundary, the software displays two adjacent, distinctly colored copies of the unwrapped plane to help identify continuous junctions. \
\
The user then manually traces each cell outline along the junctional signal to generate an initial perimeter, which the software subsequently refines algorithmically using nearby junctional points. The software then projects the refined cell contours back into the original 3D vessel geometry, enabling visualization of the luminal and abluminal vessel surfaces, EC junctions, and the luminal surface and volume of individual ECs. \
\
Vessel Analyzer
EC-level morphometrics and Vessel-level morphometrics
