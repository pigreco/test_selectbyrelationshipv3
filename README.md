## test_selectbyrelationshipv3

In questo repo faremo dei test sul plugin Selectbyrelationship per >= QGIS 3.0

## Dati e progetto

* database spatialite per test:
    * tre tabelle (con geometry):
        * regioni;
        * province;
        * comuni;

* progetto QGIS 3.0:
    * create due relazioni:
        * tra regioni (padre) e province (figlio) - chiave "COD_REG";
        * tra province (padre) e comuni (figlio) - chiave "COD_PROV";

* Osservazioni
    * la tabella _regioni_ è solo padre (padre di province);
    * la tabella _province_ è padre e figlia (padre di comuni);
    * la tabella _comuni_ è solo figlia;

---

Il plugin, installato tramite [file.zip](https://github.com/pyarchinit/selectbyrelationship_repo/releases/tag/v0.3.0), si presenta con due icone: la seconda (settings) si attiva solo dopo aver attivato il plugin (con la prima icona).

<img src="/images/icone_p.png">

* la prima icona: '_Allows selections by relationship_' attiva la selezione figlio-padre (configurazione di default);
* la seconda icona '_settings_'ha tre opzioni:
    * Zoom to Feature to Referenced Layer (Parent) (Zoom feature Padre);
    * Select Feature of Referencing Layer (Child) From Referenced one (Seleziona Figli selezionando Padri);
    * Active Referenced Layer (Attiva layer Padre);

<img src="/images/icona_settings.png">