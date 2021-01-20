# The NUFORC Vitrine

#### Through the extraterrestrial looking-glass.

[<img src="http://www.nuforc.org/logo4.jpg" width="250" height="250"/>](http://www.nuforc.org/)

---

## Overview

This repository stores my data obtention methods, as well as the (as-of-yet unfinished) __Tableau__ workbook showcasing my analysis and insights.

---

## Briefing

All data was found, scraped, cleaned, polished, and validated by me.


### Data collection
I found the [data.world](https://data.world/timothyrenner/ufo-sightings) extract far too dirty. These shortcomings include, but are not limited to;
* `Time` field has sporadic negative number entries;
* `Latitude` and `Longitude` are missing for non-U.S. locations, and even incorrect for some;
* `Country` data is unusable in its entirety for a few reasons. First and foremost, it was very clearly treated as a free-text field at the point of entry — most inconsistencies and errors have this to blame. Second, all Canadian locations are labelled as American — that's ~96% of the dataset obsolete since we can't discern the two. Finally, the dataset uses outdated choronyms (e.g. _West Germany_, _Burma_, _Swaziland_, etc.), owing to the database's age.

I found [Kiru](https://github.com/kiru)'s [take on the matter](https://github.com/kiru/ada_project) too involved. I achieved a near-identical result to Kiru with a more modest approach — that is without parallelisation, by indexing the database by date rather than shape (unsure why this choice was made), using a quarter of the dependencies, and in about a fifth the number of lines.


### Data cleansing
Cleanup, as per, consumed the majority of my time with this project.


### Complementary data
To support some of my findings and hypotheses I needed several auxiliary datasets.

---

## License

Everything here is wholly [unlincensed](LICENSE).

---

[Back Up Top](#the-nuforc-vitrine)
