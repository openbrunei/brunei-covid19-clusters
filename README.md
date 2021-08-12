# Brunei COVID-19 Clusters, 2021

2021 data about COVID-19 clusters in Brunei in CSV/JSON/XLSX formats.

Data generally sourced from the Ministry of Health (MOH), Brunei Darussalam, as shared on the official government channel on Telegram, [GOV.BN Official](https://t.me/govbnofficial). On occasion, will link to other government or media sources in Brunei, including posts on Instagram. Detailed sources are in the files.

This work is licensed under a [Creative Commons Attribution-NonCommercial 4.0 International License](http://creativecommons.org/licenses/by-nc/4.0/).

## Disclaimer

The datasets provided here are unofficial. This is a data collection and sharing exercise by [Hazirah M](https://possiblyzebra.notion.site/Contact-Me-e88daff714834f3a9fac11413ed48b6).

Terms used are based on my understanding as a layman. To contact me regarding any grievous errors, see "Contact" below.

## Data Files

1. **local_cases** CSV/JSON - Shows _daily_ total of _new_ local cases, i.e. community spread cases, not imported.
2. **clusters** CSV/JSON - Shows _daily_ total of _new_ cases broken down by clusters, as identified and named by MOH Brunei. These will often exclude the first case of the cluster, if found on an earlier day.
3. **unlinked** CSV/JSON - Shows _daily new_ unlinked case numbers, where MOH Brunei have not identified the source of the spread, i.e. neither imported nor connected to a known cluster or local case. More info:
    - Once a case has been linked, its cluster name will be added to the row.
    - Sometimes the unlinked case numbers are not provided, so in such cases, I will add my own numbering system in the format "?-001".
4. MS Excel file (XLSX) containing above 3 in separate sheets. Filters available.

Note that new daily data is added to the top rows for each file and sheet.

## Rationale

### Why this data

I wanted to keep track of cluster growth on a daily basis, and also to keep track of the unlinked cases as over time some of them would become linked to other cases or new clusters. I'm not super skilled at visualisation, and can't spend a lot of time on this, so I decided to just store the daily cluster and overall figures, and a limited amount of related data. I'm sharing the data, as it still could be useful to others. 

### Data structure

I have kept the data structures simple because:

* I want to update it easier on an almost daily basis, particularly during Brunei's second wave of COVID-19 transmission that started on 7th Aug 2021
* I'm not planning anything ambitious with the data
* I am out of practice with formal data collection so I want to start small!

Suggestions for improving data structure are welcome. (I'm figuring it out as I go!)

## Contact

Mini-project by **Hazirah M** under **Open Brunei**.

[Contact me here](https://possiblyzebra.notion.site/Contact-Me-e88daff714834f3a9fac11413ed48b6).

Website: [openbrunei.org](http://openbrunei.org)
