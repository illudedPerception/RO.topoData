# Railroads Online Raster and CSV topographical data
* Raster based data is missing CRS and does not contain ingame Z height needs to be manipulated in QGIS
* CSV based data allready has inverted X cordinates, what are now outdated because of the rotated maps in RO, also why the rasters generated from the cordinates need to be rotated to match the new Railroads online maps
# "Template/ikea instructions" friend not needed
background color:		ffffec

line color 1:		808080 (lighter dash dot)
line color 2:		363636 (darker solid line)
line opacity:		75%
line width:			0.05mm
line 1:			solid
line 2:			dash dot dot dash

label text size:		1.8 points 
font:					open sans


buffer size:		0.2mm
buffer style:		bevel
buffer color:		ffffec

label text color 1:		808080 (lighter dash dot)
label text color 2:		363636 (darker solid line)


placement repeat:		50mm
Placement: 				on line (Mode: parallel)
anchor:			center of text

water stroke style: 		solid line
water stroke size: 		0.4mm
water stroke color:		377eb8
water fill color:		377eb8
==============================
grid opacity:		75%
line color 1:		363636 1km
line color 2:		808080  500m
line color 3:		808080 100m

line 1 stroke width:		0.1mm
line 2 stroke width:		0.08mm
line 3 stroke width:		0.05mm
line 3 style:		dash line

1000m
grid dot size:		1mm
grid dot opacity:		75%
grid dot type:		diamond
grid dot fill color:		363636
grid dot stroke color:	363636
grid dot stroke width:	0.4mm

500m
grid dot size:		0.5mm
grid dot opacity:		75%
grid dot type:		topo pop house
grid dot fill color:		808080
grid dot stroke color:	808080
grid dot stroke width:	0.2mm
==============================
relief			edit .tif for artifacts
Z factor:			100
transparency:		20%
singleband pseudocolor
color ramp:		grays / civids / mako (the best)

map extent what ever gives square output px
export DPI 470


Field calculator (might need editing)
To make index:					if("ELEV"//100%10=0, 1, NULL)
To make index 2:				if("ELEV"//100%10=0, NULL, 2)
To make label:					round("index"*"elev"/100,0)
To make label 2:				round("index2"/2*"elev"/100,0)
