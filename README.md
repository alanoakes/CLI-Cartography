# CLI Cartography

The purpose of this map template is to learn cartography
with command line tools and define an iterative 
mthodology. I am using an article written by Mike
Bostock and rendering SVG maps.

## Table of Contents

1. File Schema
2. Iterative Checklist
3. Analysis of CLI Methodology

## 1. File Schema



## 2. Iterative Checklist

* [ ] Part 01:
	* [ ] Setup development cartography environment
	* [ ] Determine, download and unzip maps needed
	* [ ] Locally install all CLI tools needed
* [ ] Part 02:


## 3. Analysis of CLI Methodology

- Author: Mike Bostock
- Title: "Command-Line Cartography"
- Subtitle:	"A tour of d3-geo’s new command-line interface."
- Published: Dec 9, 2016

# Overview

This multipart tutorial will teach you to make a thematic map
from the command line using d3-geo, TopoJSON and
ndjson-cli—free, open-source tools written in JavaScript.

# [[https://medium.com/@mbostock/command-line-cartography-part-1-897aa8f8ca2c|Part 1]]

The first part of this tutorial focuses on getting geometry
(polygons) and converting this geometry into a format that can
be easily manipulated on the command-line and displayed in a
web browser.

## Determine, Download & Unzip Files

The following FIP Codes are researched for the CBSA of Memphis, TN

**| FIPS   | Location Description                |**
| 473680 | Memphis-Forrest City, TN-MS-AR CBSA |
| 473282 | Memphis, TN-MS-AR Metro Area        |
| 052262 | Forrest City, AR Micro Area         |
| 05035  | Crittenden County, AR               |
| 05123  | St. Francis County, AR              |
| 28093  | Marshall County, MS                 |
| 28033  | DeSoto County, MS                   |
| 28137  | Tate County, MS                     |
| 28143  | Tunica County, MS                   |
| 28009  | Benton County, MS                   |
| 47157  | Shelby County, TN                   |
| 47047  | Fayette County, TN                  |
| 47167  | Tipton County, TN                   |

```bash
wget ftp://ftp2.census.gov/geo/tiger/TIGER2019/CBSA/tl_2019_us_cbsa.zip
wget ftp://ftp2.census.gov/geo/tiger/TIGER2019/TRACT/tl_2019_05_tract.zip
wget ftp://ftp2.census.gov/geo/tiger/TIGER2019/TRACT/tl_2019_28_tract.zip
wget ftp://ftp2.census.gov/geo/tiger/TIGER2019/TRACT/tl_2019_47_tract.zip
```




# [[https://medium.com/@mbostock/command-line-cartography-part-2-c3a82c5c0f3|Part 2]]

The command line is great for this. UNIX has a
well-established philosophy of small, decoupled tools that
allow powerful manipulation of data. To leverage the power of
the command line, we simply need to convert our data into a
format that fits a UNIX convention: lines of text. And since
JSON is already text, we just need each line of text be a
valid JSON value.

# [[https://medium.com/@mbostock/command-line-cartography-part-3-1158e4c55a1e|Part 3]]

The GeoJSON feature collection of census tracts we constructed
previously was 13.6M. That’s fine for local viewing, but a bit
large for the web! Fortunately there are ways to shrink
geometry without apparent loss of detail. We can:

1. Simplify (e.g., remove coordinates per Visvalingham).
2. Quantize (e.g., remove digits, say 224.3021507494117 to 224.3).
3. Compress (e.g., remove redundant geometry).
			
# [[https://medium.com/@mbostock/command-line-cartography-part-4-82d0d26df0cf|Part 4]]

he word choropleth comes from the Greek khôros meaning “area
or region” and plêthos meaning “a great number”. To construct
one, we apply a color encoding of the population data to the
geometry we prepared previously.


