## test_selectbyrelationshipv3

Questo repo serve a fare test 

* database spatialite per test:
    * tre tabelle:
        * regioni
        * province
        * comuni

* progetto QGIS 3.0:
    * create due relazioni:
        * tra regioni (padre) e province (figlio) - chiave "COD_REG";
        * tra province (padre) e comuni (figlio) - chiave "COD_PROV";

---

Il plugin, installato tramite [file.zip](https://github.com/pyarchinit/selectbyrelationship_repo/releases/tag/v0.3.0), si presenta con due icone: la seconda (settings) si attiva solo dopo aver attivato il plugin con la prima icona.

<img src="/images/icone_p.png">

* la prima icona: '_Allows selections by relationship_' attiva la selezione figlio-padre (configurazione di default);
* la seconda icona '_settings_'ha tre opzioni:
    * Zoom to Feature to Referenced Layer (Parent);
    * Select Feature of Referencing Layer (Child) From Referenced one;
    * Active Referenced Layer

<img src="/images/icona_settings.png">