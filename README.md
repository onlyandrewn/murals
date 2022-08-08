## Collecting the data
- Manually collected the points of murals in three neighborhoods
- The three neighborhoods were: Old North St. Louis, Covenant Blu Grand Center, Forest Park Southeast
- Used [geojson.io](https://geojson.io/) to plot the relative locations of the murals

## Datawrapper
- Downloaded a shpfile containing the neighborhoods boundaries from the [City of St. Louis' open data portal](https://www.stlouis-mo.gov/data/datasets/dataset.cfm?id=85)
- Exported a separate geojson of each of the three neighborhoods in QGIS
- Imported the neighborhood boundaries and the points for each neighborhood into their own graphic in Datawrapper: [1](https://www.datawrapper.de/_/KNFLG/), [2](https://www.datawrapper.de/_/Wufjq/), [3](https://www.datawrapper.de/_/8tsDQ/)
- Created the bike route in [Google My Maps](https://www.google.com/maps/d/edit?mid=10uNCcgNwTWhCbZIn19hxpQc0OinCvHk&usp=sharing) and exported as a KML, save to geojson 
- Each part of the route in Google My Maps needed to be its own individual segment
- Export the [chart](https://www.datawrapper.de/_/NgQuz/) without headers or background from Datawrapper into Illustrator

## Illustrator
- Imported SVG file from Datawrapper
- Ungrouped all the layers
- Re-organized the contents into four layers: ai2html-settings, interactions:svg, furniture and basemap
- Export the artboard using ai2html
- Add the following settings to ai2html export: `inline_svg: true`, `png_transparent: yes`
- For static graphics, added the SVG output to the story
- For the scrollytelling portion, copy and pasted ai2html output into story and used Scrollama to animate features

## Data analysis
- Analysis used in the story can be found in `analysis.ipynb`
- Crime data scraped from the [St. Louis Post-Dispatch's crime tracker](https://graphics.stltoday.com/apps/crime/st-louis-city/) using Selenium
- Census data scraped from the [City of St. Louis](https://www.stlouis-mo.gov/government/departments/planning/research/census/data/neighborhoods/index.cfm) using BeautifulSoup
- Walkability data scraped from [Walk Score](https://www.walkscore.com/MO/St._Louis) using BeautifulSoup
- Percent of race in a neighborhood: ((pct_group - total population of neighborhood) / total population of neighborhood ) * 100
- Murals per capita: (num_murals / total population of neighborhood)