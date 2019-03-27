# Avgangstider for Ruter

En Flask-applikasjon som leser et [Ruter-API](https://reisapi.ruter.no/help) og lager en avgangstabell som til forveksling ligner Ruters egne skjermer. Ved hjelp av parameterne nedenfor kan man velge hvilken stasjon, platform og linje man vil vise avganger for.


# Parametere

* `stopid`: Et tall som identifiserer holdeplassen. For å finne stopid fra linjenummer, kan du se gjennom output fra https://reisapi.ruter.no/Place/GetStopsByLineID/3 (eksempel for linje 3)
* `lines`: Et tall som identifiserer linjenummeret du fil filtrere på. Du kan evt. spesifisere flere linjer ved å gjenta denne parameteren.
* `platforms`: Et tall som identifiserer plattformen du vil filtrere på. Du kan evt. spesifisere flere platformer ved å gjenta denne parameteren.
* `rows`: Max antall avganger du ønsker å vise. Default verdi 0 viser alle avganger som returneres av API'et.

# Eksempel
URL: http://localhost:5000/?stopid=3011310&platforms=2&rows=4
Resultat: ![Screenshot](screenshot.png)
