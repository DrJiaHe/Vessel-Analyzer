{\rtf1\ansi\ansicpg1252\cocoartf2870
\cocoatextscaling0\cocoaplatform0{\fonttbl\f0\fswiss\fcharset0 Arial-ItalicMT;\f1\fswiss\fcharset0 ArialMT;\f2\fswiss\fcharset0 Arial-BoldMT;
}
{\colortbl;\red255\green255\blue255;\red0\green0\blue0;}
{\*\expandedcolortbl;;\cssrgb\c0\c0\c0;}
\margl1440\margr1440\vieww23060\viewh10660\viewkind0
\deftab720
\pard\pardeftab720\qj\partightenfactor0

\f0\i\fs29\fsmilli14667 \cf2 \expnd0\expndtw0\kerning0
Vessel Analyzer
\f1\i0 \'a0app in MATLAB (R2021a; MathWorks\'ae), which quantifies EC and vessel morphology. \
\
Required toolboxes: Image Processing Toolbox and Curve Fitting Toolbox.\
\
\pard\pardeftab720\sl337\sa213\partightenfactor0
\cf2 For each user-selected vessel segment (here, a portion of the DA), first upload the image showing EC junction signals, followed by the image showing the EC membrane marker. Then, select the relevant portion of the DA as the ROI.\
\pard\pardeftab720\qj\partightenfactor0
\cf2 The app automatically identifies the outer and luminal vessel boundaries and the lumen center in cross-sections orthogonal to the vessel axis. The software then maps EC junctions onto a cylindrical representation of the vessel surface and computationally unwraps them into a 2D plane. To segment junctions crossing the 0\'b0 boundary, the software displays two adjacent, distinctly colored copies of the unwrapped plane to help identify continuous junctions. \
\
The user then manually traces each cell outline along the junctional signal to generate an initial perimeter, which the software subsequently refines algorithmically using nearby junctional points. The software then projects the refined cell contours back into the original 3D vessel geometry, enabling visualization of the luminal and abluminal vessel surfaces, EC junctions, and the luminal surface and volume of individual ECs. \
\
\pard\pardeftab720\qj\partightenfactor0

\f0\i \cf2 Vessel Analyzer
\f1\i0 \'a0provides two classes of outputs.\'a0\
(
\f2\b 1
\f1\b0 )
\f2\b  EC-level morphometrics
\f1\b0 , measured at the luminal surface, including\'a0\ul perimeter\ulnone \'a0(cell boundary length),\'a0\ul length\ulnone \'a0(maximum longitudinal span of the cell within its perimeter),\'a0\ul width\ulnone \'a0(maximum transverse distance within the cell perimeter, measured perpendicular to the length),\'a0\ul area\ulnone \'a0(the total luminal surface area occupied by the cell, obtained by surface integration),\'a0\ul elongation
\f2\b \ulnone  
\f1\b0 (length/width ratio), and\'a0\ul volume\ulnone \'a0(computed by integrating cell area with the distance between luminal and basal surfaces). To assess EC alignment within the vessel, the app estimates the vessel\'92s central axis by linearly fitting the inner-wall center points and then calculates each cell\'92s\'a0\ul alignment angle\ulnone \'a0(\uc0\u952 ), defined as the angle between the cell\'92s long axis and the vessel longitudinal axis. \
\
(
\f2\b 2
\f1\b0 )
\f2\b  Vessel-level morphometrics
\f1\b0 , calculated for each cross-section, including\'a0\ul maximum luminal diameter\ulnone ,\'a0\ul minimum luminal diameter\ulnone , and\'a0\ul caliber\ulnone \'a0(approximate luminal cross-sectional area enclosed by the luminal perimeter). The app also quantifies\'a0\ul vessel tortuosity\ulnone \'a0for the analyzed vessel segment, defined as the average deviation of inner-wall center points from the estimated vessel central axis.\'a0}