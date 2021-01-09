# The NUFORC Vitrine

#### Through the extraterrestrial looking-glass.

[<img src="http://www.nuforc.org/logo4.jpg" width="250" height="250"/>](http://www.nuforc.org/)

---

## Overview

This repository stores my data obtention methods and techniques, as well as the (as-of-yet unfinished) __Tableau__ workbook showcasing my analysis and insights.

---

## Briefing

All data was found, scraped, cleaned, polished, and validated by me.

### Data collection
I found the [data.world](https://data.world/timothyrenner/ufo-sightings) extract far too dirty. These shortcomings include, but are not limited to;
* the `Time` field has sporadic negative number entries;
* `Latitude` and `Longitude` are missing for non-U.S. locations, and even incorrect for some;
* `Country` data is _completely_ unusable for many reasons, first and foremost because it was treated as a free-text field at the point of data entry — most inconsistencies and errors have this to blame — but also due to the labelling of Canadian locations as American (that's ~96% of the dataset obsolete), and the use of outdated choronyms (e.g. _West Germany_, _Burma_, _Swaziland_, etc.).
<br/>

I found [Kiru](https://github.com/kiru)'s [analysis on the matter](https://github.com/kiru/ada_project) too involved. I achieved a near-identical result to Kiru with a more modest approach — that is; without parallelisation, by indexing the database by date rather than shape (not sure why this choice was made), using a quarter of the dependencies, and in about a fifth the number of lines.

### Data cleansing


---

## License

[Everything here is completely unlincensed](LICENSE).

---

[Back Up Top](#the-nuforc-vitrine)
