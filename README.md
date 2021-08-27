# Brunei COVID-19 Clusters, 2021

2021 datasets and simple charts about COVID-19 clusters in Brunei in CSV/JSON/XLSX formats.

Data is generally sourced from the Ministry of Health (MOH), Brunei Darussalam, as shared on the official government channel on Telegram, [GOV.BN Official][1]. On occasion, will link to other government or media sources in Brunei, including posts on Instagram. Detailed sources are in the files.

This work is licensed under a [Creative Commons Attribution-NonCommercial 4.0 International License][2].

## Disclaimer

The datasets provided here are unofficial. This is a data collection and sharing exercise by [Hazirah M][3].

Terms used are based on my understanding as a layman. To contact me regarding any grievous errors, see "Contact" below.

The data here relies on what is provided and understood from MOH’s data. Please see an **important note on total cluster size discreprancies** below.

### Discreprancies

Generally, total sizes of clusters **cannot be verified with MOH data**, since MOH does not release total cluster sizes. So along with the following discreprancies, all numbers relating to cluster size in this project **may only be taken as estimates**.

Please also note that generally, total cluster sizes are referring to **cumulative totals for each cluster, and not current active cases for each cluster**.

* On 24 Aug 2021, MOH announced that day's total increase in cases linked to clusters but **did not specify the breakdown per cluster**. ([Situasi Jangkitan Covid-19 Di Negara Brunei Darussalam (24 Ogos 2021)](https://www.rtbgo.bn/play?scheme=205&p_type=true&id=3752&eps_id=3806), RTB GO, retrieved 25-Aug-2021)
* On 21 Aug 2021, in announcing a new cluster 1385, it was not specified whether the cases related to it were existing or new case numbers. ([Siaran Akhbar Situasi Terkini COVID-19 di Negara Brunei Darussalam (21 Ogos 2021)](https://t.me/govbnofficial/2832))
* On a specific date in August 2021, it may have been mentioned in the Question & Answer session with the media, that some previously unlinked cases may later be recategorised into existing clusters. It is also mentioned in the [footnotes](https://archive.ph/yGBU4) (archived version, retrieved 25-Aug-2021) of the Flourish public visualisation by Rayana M, [COVID-19 Brunei Daily Report](https://public.flourish.studio/visualisation/7014155/). ([Please contact me, with sources][4], if you have further info on this so that I can cite it more fully.)

## Contents

### Data about Clusters and Linked Cases

1. `local_cases` CSV/JSON - Shows _daily_ total of _new_ local cases, i.e. community spread cases, not imported.
2. `clusters` CSV/JSON - Shows _daily_ total of _new_ cases broken down by clusters, as identified and named by MOH Brunei. These will often exclude the first case of the cluster, if found on an earlier day.
3. `new_cases_breakdown` CSV/JSON - Breakdown of daily case numbers into: total new, new import cases, new local cases, new unlinked cases, and previously unlinked cases that are newly linked to a cluster or another case.
4. `new_linked` CSV/JSON - Shows on a daily basis, the cases that were previously unlinked, that on a particular date have been linked to a cluster or another case.
5. MS Excel file (XLSX) containing the above data in separate sheets. The data is filterable in Excel.

Note that new daily data is added to the top rows for each file and sheet.

### Charts

1. **Daily Charts:** For each cluster and its daily number of new cases recorded, the numbers are displayed in a bar chart. Each bar represents one day’s numbers - it may be 0 in some cases.
2. **Weekly Charts:**
	- a) Daily new community cases, by week
	- b) Weekly new community cases, by cluster
	- c) New clusters by end of week

The text-based charts are created with [Tweetable Charts][4] - more details in the “Credits” section below.

The charts being in a text form is admittedly a [no-code attitude][5] which I’m still coming to terms with. The truth is that I haven’t had time to relearn Python.

## Rationale

### Why this data

As Brunei’s second wave of COVID-19 transmission developed, starting on 7th August 2021, I wanted to:

1. Keep track of cluster growth on a daily basis
2. Keep track of the unlinked cases. I was interested particularly in seeing unlinked cases become, over time, linked to other cases or new clusters.

Though a number of (great!) citizen/unofficial visualisations of Brunei’s COVID-19 data have turned up, as of now, I haven’t seen any visualisations of the unlinked cases in the way I’ve described it above (2nd point).

I'm not super skilled at visualisation, and right now I can’t spend a lot of time on this project. So I decided to show the data I was interested in, in a hopefully low-effort way, while also respecting that others might want to make use of the data.

1. The daily cluster growth is shown via simple bar charts, and are also provided in CSV/JSON/XLSX format.
2. The daily linked cases are provided in CSV/JSON/XLSX format. If you have any visualizations of these as described above, I’d love to see them! (See also an explanation below, “Removal of dataset for unlinked cases”.)

### Data structure

I have kept the data structures simple because:

* I want to update it easier on an almost daily basis.
* I'm not personally planning anything ambitious with the data.
* If anyone wants to use the datasets for the same reasons, I don’t yet see that the data needs to be more detailed.
* I am out of practice with formal data collection so I want to start small!

Suggestions for improving data structure are welcome. (I'm figuring it out as I go!)

### The term “unlinked cases”

I have used the term “unlinked case” based on Singapore’s usage for cases that are not linked to any clusters.

Sources:

1.  Website - [Ministry of Health, Singapore][6]
- Screenshot below shows the website as linked above, scrolled to a section where numbers for new linked and unlinked cases are shown.
	![Screenshot of Ministry of Health Singapore website https://www.moh.gov.sg/ . Retrieved 22 Aug 2021.][image-1]
2. PDF - [ 20 August 2021 Daily Report on COVID-19 ][7]
- The document contains a table of figures, showing numbers for linked and unlinked cases. (The link shows an archived version, retrieved 22 Aug 2021.)

In MOH Brunei’s media statements, they are called cases of unknown source, or cases “where the source of infection is still being determined” (Media Statement on the Current Situation of COVID-19 in Brunei Darussalam, 21 Aug 2021).

### Removal of dataset for unlinked cases

For unlinked cases, I earlier provided a dataset `unlinked` in CSV/JSON format and in the Excel file. This was to track when **unlinked** cases **became linked** and to keep a record of them.

MOH at first shared the individual case numbers for such cases, but when the daily unlinked numbers went above 10, I noticed they stopped sharing them. So I used my own numbering system for each unlinked case.

However, I have removed these. When the daily numbers for unlinked cases climbed above 50, I realised it would become difficult to manage.

Instead, only information made available about **unlinked** cases **becoming linked** are made available, and you may find them in `new_linked`.

Here’s the old description for this:

> **unlinked** CSV/JSON - Shows _daily new_ unlinked case numbers, where MOH Brunei have not identified the source of the spread, i.e. neither imported nor connected to a known cluster or local case. More info:
> - Once a case has been linked, its cluster name will be added to the row.
> - Sometimes the unlinked case numbers are not provided, so in such cases, I will add my own numbering system in the format "?-001".

## Credits

The text-based charts in the Daily Charts and Weekly Charts are thanks to [Tweetable Charts][8], who also show you [how to make them in Python][9] in their book [Tweetable Python][10].

Data clean-up is done with [DevUtils.app][11] and [Browserling Web Developer Tools][12].

## Contact

Mini-project by **Hazirah M** under **Open Brunei**.

[Contact me here][13].

Website: [openbrunei.org][14]

[1]:	https://t.me/govbnofficial
[2]:	http://creativecommons.org/licenses/by-nc/4.0/
[3]:	https://possiblyzebra.notion.site/Contact-Me-e88daff714834f3a9fac11413ed48b6
[4]:	https://tweetable-charts.agiliq.com/
[5]:	https://en.wikipedia.org/wiki/No-code_development_platform
[6]:	https://www.moh.gov.sg/
[7]:	http://web.archive.org/web/20210822064653/https://www.moh.gov.sg/docs/librariesprovider5/local-situation-report/ceg_20210820_daily_report_on_covid-19.pdf
[8]:	https://tweetable-charts.agiliq.com/
[9]:	https://books.agiliq.com/projects/tweetable-python/en/latest/ascii-art.html#horizontal-bar-graphs
[10]:	https://books.agiliq.com/projects/tweetable-python/
[11]:	https://devutils.app/
[12]:	https://www.browserling.com/tools/
[13]:	https://possiblyzebra.notion.site/Contact-Me-e88daff714834f3a9fac11413ed48b6
[14]:	http://openbrunei.org

[image-1]:	https://github.com/openbrunei/brunei-covid19-clusters/raw/main/assets/moh-sg_unlinked_retr2021-08-22.png