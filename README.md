# covid19monitoring_economy_SHAB

## Grundlage 
Die Angaben basieren auf einer Auswertung der im Schweizerischen Handelsamtsblatt (SHAB) publizierten Meldungen. Abgerufen werden die Meldungen via API, die von der Moneyhouse AG betrieben wird. Die Publikation im SHAB erfolgt im Normalfall mehrere Tage nach der Publikation in den kantonalen Handelsregistern. Das Datum bezieht sich auf die Publikation im SHAB.

Erfasst wird die Anzahl erstmaliger Konkursverfahrenseröffnungen gegen Firmen. Verfahrenseröffnungen aufgrund organisatorischer Mängel einer Firma (Art. 731b OR) werden nicht erfasst, weil diese nicht per se mit Zahlungsschwierigkeiten in Zusammenhang stehen. 
Weil es keinen national gültigen Standard gibt, wie Meldungen zu Konkursverfahrenseröffnungen zu verfassen und  kategorisieren sind, wird für die Identifizierung der relevanten Meldungen ein maschinelles, mehrstufiges Filterverfahren eingesetzt, das unter anderem auch auf einer Stichwortsuche basiert. Aufgrund der Unterschiede bei der Datenerhebung kann es zu Abweichungen mit anderen Auswertungen kommen. Der Vorteil dieser Erhebung liegt darin, dass die Daten fast in Echtzeit analysiert werden können.
<br><br>

## Methodisches
* Es wird jeweils nur die erste Eröffnung eines Konkursverfahrens seit 2015 gegen eine Firma erfasst. Dies ist dem Erhebungsverfahren geschuldet.
* Es kann zu kleinen rückwirkenden Anpassungen der Daten kommen.

## Variablen 
<strong>konk_eroeff</strong> = Anzahl erstmaliger Konkurseröffnungsverfahren gegen Firmen im jeweiligen Kanton (exkl. Verfahren aufgrund organisatorischer Mängel)

## Weitere Informationen 
[Projektseite: "Gesellschafsmonitoring COVID19"](https://github.com/statistikZH/covid19monitoring) <br>
[Datenbezug](https://www.web.statistik.zh.ch/covid19_indikatoren_uebersicht/#/) <br>
[Visualisierung](https://www.web.statistik.zh.ch/cms_vis/covid19_indikatoren/) <br>