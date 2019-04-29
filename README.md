# Analyzing corrected votes in the EU Parliament

Contains Python notebooks with the data research for the following stories:

- [Här är de Svenska ledamöterna som oftast trycker fel i EU-parlamentet: ”Det är för mycket”](https://emanuelkarlsten.se/04/ledamoterna-som-oftast-trycker-fel-i-eu-parlamentet-det-ar-ju-for-mycket/?fbclid=IwAR14dtF36EA9gyEYtAUd9wylcqGi_W0sL2SfxbLh5gTlbgdEWqlS2EvIDLo)
- [Svenska ledamöter är näst sämst i EU på att rösta – trycker på fel knapp och rättar i efterhand](https://emanuelkarlsten.se/04/svenska-ledamoter-ar-nast-samst-i-eu-pa-att-trycka-pa-ratt-knapp-vid-votering/)

Contact jens@jplusplus.org for questions.

### 1. Collect data.ipynb

Run this notebook to scrape MEP + voting data from VoteWatch. Data will be stored locally as csv files (under `data`).

### 2. Analyze.ibynb

Does some very basic aggreagtion of the data, focusing on how often members of parliament correct their votes, a proxy for how often they "vote wrong".

The notebook exports aggregated data to csv files (`output`) containing the following columns:

- Number of votes in total
- Number of votings when MEP was present. Excludes all votings when the MEP has been absent.
- Presence (%): Share of votings when MEP was not absent.
- Particiation (%): Excludes not only absence, but also votings when MEP has been registred to not have voted.
- Number of 'wrong votes': "Wrong votes" are defined as votings where the MEP has been **present** and corrected a vote after the session.
- Share of votes that were 'wrong' (of the votings where the MEP was present)
- Number of corrected votes in total: This column also include corrected votes made after absence.
- Share of votes that were corrected (of the votings where the MEP was present)
