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

Il plugin, installato tramite zip, si presenta con tre icone: la seconda e la terza (settings) si attivano solo dopo aver attivato il plugin (con la prima icona).

<img src="/images/icone_p2.png">

* la prima icona: '_Allows selections by relationship_' attiva la selezione figlio-padre (configurazione di default);
* la seconda icona _Select Relationship_, un menu a tendina, permette di attivare le relazioni del progetto; di default non è selezionata nessuna relazione, quindi il plugin non lavora;
* la terza icona '_settings_'ha tre opzioni:
    * Zoom to Feature to of Parent Layer (Zoom feature Padre);
    * Select Feature(s) of Child From Parent Layer (Seleziona Figli selezionando Padri);
    * Active Parent Layer (Attiva layer Padre);

<img src="/images/icona_settings2.png">