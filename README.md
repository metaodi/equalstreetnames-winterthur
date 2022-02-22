# Welcome to EqualStreetNames Winterthur :heart: 🤍

# How to
The aim of this section is to provide a guideline on how to collect, store and link the required data so it can be used by equalstreetnames.

Basic steps are:
1. Identifiy a Street named after a Person
2. Find the Wikidata-Item of this street
3. Find the Wikidata-Item of the Person
4. Link the Street-Wikidata-Item with the Person-Wikidata-Item

See following sections to find out more about the work that can be done.

## Identify Streets named after a Person
1. Find a street on the [TODO list of Winterthur](https://equalstreetnames-todo.herokuapp.com?city=winterthur) and try to find the person on Wikidata.

## Find the Wikidata-Item of this street

* Search at [Wikidata.org](https://www.wikidata.org)

Example: [Emilie-Kempin-Spyri-Weg](https://www.wikidata.org/wiki/Q27329833)

## Find the Wikidata-Item of the Person

This is the most tricky part...
1. Check this PDF of winterthur-glossar.ch: https://www.winterthur-glossar.ch/upload/documents/2018/03/05/2481.pdf
2. Search at [Wikidata.org](https://www.wikidata.org) for this Person.
3. Note the Q-Number of the Person

Example: Q119636 for [Emilie Kempin-Spyri](https://www.wikidata.org/wiki/Q119636)

## Link the Street-Wikidata-Item with the Person-Wikidata-Item
1. Return to the Wikidata-Entry of the street
2. Click "add statement" (At the End of all Statements)
3. Choose as Property: "named after"
4. Add as the value the Q-Number of the person and choose the Name as the value
5. Click "add reference"
6. Choose as property: "stated in" and as value "Winterthur Glossar" (Q60432730)
7. Click "add" (to add an additional reference)
8. Choose as property: "retrieved" and as value the Date of Today eg. "13.05.2006"
9. Click "add" (to add an additional reference)
10. Choose as property: "reference URL" and as value the URL of the Winterthur Glossar with information about the person
11. Click "publish"

Done :muscle:

# Advanced Section

## Identify Wikidata entries of a person
The named streets can be categorised by:
* Named after a person with an existing Wikidata entry.
  * Example: [Else Züblin-Spiller](https://www.wikidata.org/wiki/Q1333744)
* Named after a person without a Wikidata entry. Usually citizens of Zurich. eg.:
  * Laura-Hezner-Weg
* Named after a historical person, not 100% sure if they exist. eg.:
  * Flobotstrasse
  * Woloweg
  * Wibichstrasse
* Named after a certain person's occupation, because they were working at this street eg.:
  * Eisengasse
  * Drehergasse
  * Feilengasse
* Named after a goddess. eg.:
  * Freyastrasse
  * Florastrasse
  * Fortunagasse

## Add Information to Wikidata
### Basic Wikidata Entry
To make the map of equalstreetnames work, a wikidata entry needs following:
* `label` (in English)
* `description` (in English)
* Statements:
  * `instance of` (P31) = `human` (Q5)
  * `sex or gender` (P21) with following possible values according to Propertydefinition:
    * `femal` (Q6581072)
    * `intersex` (Q1097630)
    * `male` (Q6581097)
    * `transgender female` (Q1052281)
    * `transgender male` (Q2449503)

### Advanced Wikidata Entry
If you know more about a Person and you feel like to share this with Wikidata. Here are some suggestions what you could add additionaly:
* `label` (in German)
* `description` (in German)
* Statements:
  * `image` (P18)
  * `date of birth` (P569)
  * `place of birth` (P19)
  * `date of death` (P570)
  * `place of death` (P20)
* Identifiers:
  * `HDS ID` (P902). Link to the HLS-article-Nr of this person. Example: [Annemarie Schwarzenbach](https://www.wikidata.org/wiki/Q123368)

### :warning: Declare Sources on Wikidata :warning:

If you add Information to Wikidata, don't forget to cite your source.

#### Information from HLS to Wikidata
Adding Information from the HLS to a Statement
* click `add reference` 
* choose:
  * `stated in` = `Historical Dictionary of Switzerland` (Q642074)
  * `retrieved` = Date of Day you entered the Information (Usualy Today)
  * `reference URL` = URL to the article like https://hls-dhs-dss.ch/de/articles/009370/2012-09-11/
* Example: `place of birth` of [Erika Rikli](https://www.wikidata.org/wiki/Q96489752)

### Wikipedia article

If there is no existing Wikipedia Articel, the "Historische Lexikon der Schweiz (HLS)" alows to copy there complete Inofmration to Wikipedia. See: [Nutzungshinweise](https://hls-dhs-dss.ch/de/about/usage)

### :warning: Declare Sources on Wikipedia :warning:

If you add Information to Wikipedia, don't forget to cite your source.
* If you create an Article completly baed on HLS add `{{HLS-Text|202356100}}` or even better `{{HLS-Text|Artikel=026515/2011-12-28|Version=190573009|Autor=Stefanie Spirig-Bülte}}` according [Vorlage:HLS-Text](https://de.wikipedia.org/wiki/Vorlage:HLS-Text)
* If only some Texts are form HLS, add a Weblink according [Vorlage:HLS](https://de.wikipedia.org/wiki/Vorlage:HLS)

# Data

## Winterthur Glossar

There is a lot of information about Winterthur on [Winterthur Glossar](https://www.winterthur-glossar.ch).

## Historisches Lexikon der Schweiz (HLS)
More about [HLS on Wikipedia](https://de.wikipedia.org/wiki/Historisches_Lexikon_der_Schweiz).

[HLS](https://hls-dhs-dss.ch) is published under [Creative Commons BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/). See also Nutzungsbedingungen of HLS: [Urheberrechte und Verwendung der HLS-Inhalte](https://hls-dhs-dss.ch/de/about/usage#HUrheberrechteundVerwendungderHLS-Inhalte)

You may use HLS to add Information on Wikidata / Wikipedia and even create a Wikipedia-article entirely based on an HLS-article. 
:warning: If you do so, Cite all Informations! See section on How to.



# ToDo
- [ ] Add Wikidata entries for all streets in Winterthur, use GWR as source? see https://qa.poole.ch/addresses/ch/
- [ ] Check the copyright of Winterthur Glossar
- [x] Create a TODO app for Winterthur (similar to the one for Zurich)
