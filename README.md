# Firmabil

Lager af materialer i firmabilen. Scan stregkoderne, der allerede sidder på pakkerne, og appen holder styr på, hvad der er i bilen – i stk og i hele kasser.

- **Tag ud**: scan → vælg *Hele kasser* eller *Stk* → vælg sag. Materialet trækkes fra lageret og skrives samtidig på sagen i **Timer-appen** (timesedlen).
- **Fyld op**: scan → antal kasser/stk lægges til lageret.
- **Ukendt stregkode**: giv varen et navn én gang (fx "Spax 5×50", 200 stk pr. kasse). Næste gang genkendes den.
- **Ting uden stregkode**: opret dem under *Lager* og find dem via søgning.
- **Skal købes**: varer under minimum (standard 20 stk) kommer på listen, med forslag til hvor mange kasser der skal købes. Listen kan kopieres eller deles.
- **Tæl op**: ret beholdningen, når du har talt efter.

Appen virker uden dækning (gemmes på telefonen) og synkroniserer med Home Assistant. Firmabil og Timer er to adskilte integrationer – Firmabil henter kun sagerne fra Timer og sender nye materialer til den. Er Timer ikke installeret, virker lageret stadig.

## Installation

1. HACS → ⋮ → **Brugerdefinerede repositories** → tilføj `https://github.com/amigoogfutte/firmabil` som type **Integration**.
2. Installer **Firmabil** og genstart Home Assistant.
3. Indstillinger → Enheder og tjenester → **Tilføj integration** → *Firmabil*.

Appen findes derefter i sidemenuen under **Firmabil** og på adressen `https://<din-home-assistant>/firmabil-app/index.html`
(kort adresse: `/firmabil-start`). På iPhone: åbn adressen i Safari → Del → **Føj til hjemmeskærm**.

Første gang du trykker *Scan stregkode*, spørger iPhone om lov til at bruge kameraet.

Stregkodelæseren er [ZXing](https://github.com/zxing-js/library) (Apache 2.0, se `www/zxing-LICENSE.txt`).
