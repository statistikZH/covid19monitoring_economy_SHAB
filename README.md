# covid19monitoring_economy_SHAB

## Grundlage 
Die Angaben basieren auf einer Auswertung der im Schweizerischen Handelsamtsblatt (SHAB) von den kantonalen Handelsregistern publizierten Meldungen. Abgerufen werden die Meldungen via API, die von der Moneyhouse AG betrieben wird. Die Publikation im SHAB erfolgt im Normalfall mehrere Tage nach der Publikation in den kantonalen Handelsregistern. Das Datum bezieht sich auf die Publikation im SHAB.

Erfasst wird die Anzahl erstmaliger Konkursverfahrenseröffnungen gegen Firmen, die im Handelsregister eingetragen sind. Ist eine Einzelfirma (Selbständige) nicht im Handelsregister eingetragen, wird die Konkurseröffnungen nicht erfasst. Verfahrenseröffnungen aufgrund organisatorischer Mängel einer Firma (Art. 731b OR) werden separate in einem Excel-File ausgewiesen
, weil diese nicht per se mit Zahlungsschwierigkeiten in Zusammenhang stehen. 
Weil es keinen national gültigen Standard gibt, wie Meldungen zu Konkursverfahrenseröffnungen zu verfassen und  kategorisieren sind, wird für die Identifizierung der relevanten Meldungen ein maschinelles, mehrstufiges Filterverfahren eingesetzt, das unter anderem auch auf einer Stichwortsuche basiert. Aufgrund der Unterschiede bei der Datenerhebung kann es zu Abweichungen mit anderen Auswertungen kommen. Der Vorteil dieser Erhebung liegt darin, dass die Daten sehr zeitnah analysiert werden können.
<br><br>
## Datensätze
<strong>Economy_SHAB.csv </strong>: Konkurseröffnungen pro Kanton. Dies ist der Datensatz für das Gesellschaftsmonitoring-COVID19 des Statistischen Amtes.

<strong>Economy_SHAB_branchen.csv</strong>: Konkurseröffnungen pro Kanton und NOGA-Hautpabschnitt. Dies ist der Ausgangsdatensatz für die Visualisierung [hier](https://www.zh.ch/de/news-uebersicht/mitteilungen/2021/politik-staat/statistik/zeitnahe-daten-zum-konkursgeschehen.html). Um den Datensatz klein zu halten, sind nur Tage mit einer SHAB-Meldung für die entsprechende Kombination von Kanton und Branche enthalten. Nicht im Datensatz aufgeführte Tage haben den Wert 0. 

<strong>Economy_SHAB_inclorgmangel.xlsx</strong>: Konkurseröffnungen pro Kalenderwoche (inkl. Verfahren aufgrund organisatorischer Mängel).

## Methodisches
* Am 18. November 2020 werden die SHAB-Meldungen über eine neue Version der Moneyhouse-API (V2)  abgerufen. Um eine konsistente Datenreihe zu haben, wurden die Meldungen auch rückwirkend über die neue API bezogen. Weil eine identische Abfrage nicht möglich war, kommt es zu kleinen Abweichungen.
* Die Zuordnung der Firmen zu einem NOGA-Hauptabschnitt basiert auf einer Codierung der Moneyhouse AG, welche auf der NOGA-Systematik aufbaut. 
* Es wird jeweils nur die erste Eröffnung eines Konkursverfahrens seit 2015 gegen eine Firma erfasst. Dies ist dem Erhebungsverfahren geschuldet.
* Es kann zu kleinen rückwirkenden Anpassungen der Daten kommen. Etwa wenn es zu nachträglichen Erfassungen in der Datenquelle kommt.

## Visualisierung
Eine Visualisierung und weitere Informationen finden sich [hier](https://www.zh.ch/de/news-uebersicht/mitteilungen/2020/politik-staat/statistik/zeitnahe-daten-zum-konkursgeschehen.html)

## Variablen
### Economy_SHAB.csv
<strong>konk_eroeff</strong> = Anzahl erstmaliger Konkurseröffnungsverfahren gegen Firmen im jeweiligen Kanton (exkl. Verfahren aufgrund organisatorischer Mängel)

### Economy_SHAB_branchen.csv
<strong>konk_eroeff_noga_...</strong> = Anzahl erstmaliger Konkurseröffnungsverfahren gegen Firmen im jeweiligen Kanton (exkl. Verfahren aufgrund organisatorischer Mängel) in NOGA-Abschnitt ...

## Weitere Informationen 
[Projektseite: "Gesellschafsmonitoring COVID19"](https://github.com/statistikZH/covid19monitoring) <br>
[Datenbezug](https://www.web.statistik.zh.ch/covid19_indikatoren_uebersicht/#/) <br>
[Visualisierung](https://www.web.statistik.zh.ch/cms_vis/covid19_indikatoren/) <br>