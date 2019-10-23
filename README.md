# Extending ROR on a Department Level

[ROR](https://ror.org/) currently provides identifiers with metadata on a top level, like a whole university. For some use cases, a more detailed level is interesting. Here we explore the possibility to express such department level data using [schema.org](https://schema.org/).

# Sources

Indeed the best source for department level data is the organization itself, which provides this information from their internal systems.

Yet in order to get started fast, public data can be used. Many organization provide on their websites (structured) information about their internal structures.

## The Swiss Case

Let us have a look at some organizations in Switzerland:


| Name        | ROR           | Department Data  |
| :------------- |:-------------| :-----|
|University of Bern | [https://ror.org/02k7v4d05](https://ror.org/02k7v4d05) | [Website](https://www.unibe.ch/facultiesinstitutes/index_eng.html), [IR BORIS](https://boris.unibe.ch/view/divisions/divisions.html)|
|ETHZ| [https://ror.org/05a28rw58](https://ror.org/05a28rw58)| [Organisationsstruktur](https://www.bi.id.ethz.ch/orgdb/ListePre.do?filter=1)|
|University of Zurich| [https://ror.org/02crff812](https://ror.org/02crff812)|[IR ZORA](https://www.zora.uzh.ch/view/subjectsnew/)|
|...|||

# Get the data

Let's examine further the data from the University of Bern

The University of Bern uses Eprints as repository software. So for most running instances it's possible to export the used divisions tree as XML:
http://boris.unibe.ch/cgi/export/subject/divisions/XML/divisions.xml

eg. this also works for other [EPrints instances](http://roar.eprints.org/cgi/roar_search/advanced?location_country=&software=eprints&type=&order=-recordcount/-date) like:

 - https://eprints.kingston.ac.uk/cgi/export/subject/divisions/XML/divisions.xml
 - https://archipel.uqam.ca/cgi/export/subject/divisions/XML/divisions.xml
 - http://repository.essex.ac.uk/cgi/export/subject/divisions/XML/divisions.xml

# The elements

## id
Usually the department uses an id, this may be an guid, internal number or an acronym. 

Examples:

 - dep_cish
 - DCD5A442BD4CE17DE0405C82790C4DE2
 - 914aea7a-4fbc-4287-9965-01c4adf1d84c
 - 01211
 
## label

A department has a name, may exist also in different languages

| eng | ger | fr |
| :------------- |:-------------| :-----|
| General and Historical Educational Science | Allgemeine und Historische Erziehungswissenschaft | Pédagogie générale et historique |
|Centre for Computational Finance and Economic Agents|||
|Rapid Architectural Prototyping Laboratory D-ARCH (RAPLAB)|||

there are also variations for short or extended names:

|lang| Short | Standard | Long|
| :------------- |:-------------| :-----|:-----|
| ger| Masch.u.Verf.tech. | [Dep. Maschinenbau und Verfahrenstechnik](https://www.bi.id.ethz.ch/orgdb/OrgeinheitDetailPre.do?leitzahl=02130&closeMenu=1) | Departement Maschinenbau und Verfahrenstechnik |
|eng| Mechan. Process E. |Dep. of Mechanical and Process Eng.|Department of Mechanical and Process Engineering|

## hierarchy

- A department must have one or several parent organizations.
- A department may have one or several child organizations.

## display order

If there are several departments within one level there may exist a predefined order on how to order the list.

## website / url

Usually a department has a website.

## validity / history

Departments maybe disolved, merged, renamed. 


