# The NUFORC Vitrine

#### Through the extraterrestrial looking-glass.

[<img src="http://www.nuforc.org/logo4.jpg" width="250" height="250"/>](http://www.nuforc.org/)

---

## Overview

This repository stores my data obtention methods, as well as the (as-of-yet unfinished) __Tableau__ workbook showcasing my analysis and insights.

---

## Briefing

All data was collected (WIP), cleaned, analysed and visualised by me.


### Data collection
I found the [data.world](https://data.world/timothyrenner/ufo-sightings) extract far too dirty. These shortcomings include, but are not limited to:
* `Time` field has sporadic negative number entries.
* `Latitude` and `Longitude` are missing for non-U.S. locations, and even incorrect for some.
* `Country` data is unusable in its entirety for a few reasons. First and foremost, it was very clearly treated as a free-text field at the point of entry — most inconsistencies and errors have this to blame. Second, all Canadian locations are labelled as American — that's ~96% of the dataset obsolete since we can't discern the two. Finally, the dataset uses outdated and inconsistent choronyms (e.g. _West Germany_, _Burma_, _Caribbean Sea_ as well as _Antilles Sea_), owing to the database's age.

I found [Kiru](https://github.com/kiru)'s [take on the matter](https://github.com/kiru/ada_project) too involved. I achieved a near-identical result to Kiru with a more modest approach — that is without parallelisation, by indexing the database by date rather than shape (unsure why this choice was made), using a quarter of the dependencies, and in about a fifth the number of lines.


### Data cleansing
This is probably the dirtiest dataset I've ever seen.
Most fields are treated as freetext fields, and clearly no validation occured at the point of data entry:
1.	`Duration` is given textually (e.g. "1 second", "3 minutes") and is heavily strewn with mistakes, confused entries, and then just absolute poppycock. Syntactic analysis on this is extremely difficult.
2.	`Time` has sporadic "-1" entries.
3.	`Shape` is also clearly freetext, though after correcting spelling mistakes and capitalisation it boils down to only about 25 categories, thankfully. Many of these are similar enough though, so I've combined and renamed the categories down to 15.
4.  `Comment` text is encoded horrifically.
5.	`Country` is a mess:
    -	Nonsense entries include but are not limited to:
	    * "4 miles at sea"
		* "?!?!"
		* "dont know"
		* "military report"
		* "jacksonveil"
		* "ingerland!"
		* "between; mountain top"
		* "Viet Nam"
	  -	Misnomers and reduplicates:
		  * "Papua/New Guinea"
		* "U.K." and "United Kingdom" and "United Kingdom uk"
		* "Trinidad/Tobago" and "Trinidad and Tobago" and "Trinidad & Tobago"
		* "Brasil"
		* Many "Republic of"s and "Rep. of"s
6.	`Latitude` and `Longitude` are completely missing for countries outside of the U.S. and Canada. Cannot speak to their veracity.


### Comments on the data
* California has experienced more UFO sightings than every country outside of the U.S. combined.
* Colouring is proportional to LOG(COUNT+1). Combined with a diverging palette, countries with a COUNT of 1 are made brown and the rest are on a seemingly separate, sequential palette.
* NUFORC website launched in June 2001.
* The U.S. Defense Intelligence Agency's Advanced Aerospace Threat Identification Program ran from 2007 to 2012. After its start we observe a marked increase in reporting, even compared to the boost from the website's launch. We also see a decline in reporting shortly after its termination.
* Three days of note: July 4th and February 29th.
  * July 4		   I think this one's self-explanatory.
  * February 29	 While NUFORC vets all reports and ensures they're not pranks, this is probably exactly that.
  * November 7	 ???
* Datetime entries with missing time are imputed at midnight on the dot. There were 3,062 missing entries and no original entries at 00:00:00 exactly. All 00:00:00 entries are therefore NaTs.
* A more thorough accounting can be found [here](https://ada-nuforc-analysis.github.io/), courtesy of [kiru](https://github.com/kiru).

---

## License

Everything here is [unlincensed](LICENSE).

---

[Back Up Top](#the-nuforc-vitrine)
