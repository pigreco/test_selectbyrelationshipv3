## Test plugin Select by relationship v3

In questo repo faremo dei test sul plugin per >= QGIS 3.0

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

## Plugin Select by Relationship v3

Il plugin consente di selezionare i record attraverso tabelle basate su **relazioni** `one-to-one` o `one-to-many` specificate all'interno di un progetto QGIS.
Dopo l'installazione apparirà una tool bar con tre bottoni:

<img src="/images/icone_p2.png">

* la prima icona: '_Allows selections by relationship_' attiva/disattiva il plugin;
* la seconda icona _Select Relationship_, un menu a tendina, permette di attivare le relazioni del progetto; di default non è selezionata nessuna relazione, quindi il plugin non lavora;
* la terza icona '_settings_' ha tre opzioni:
    * Zoom to Feature to of Parent Layer,se attivata fa lo zoom della feature padre;
    * Select Feature(s) of Child From Parent Layer, se attivata seleziona i Figli dopo la selezione dei Padri;
    * Active Parent Layer, se attivata dopo selezione rende attivo il layer padre;

<img src="/images/icona_settings2.png">

 Il plugin in 3 passaggi:
1. Carica in un progetto QGIS i tuoi strati;
2. Impostare le relazioni tra i livelli all'interno delle proprietà del progetto QGIS e salva;
3. Attivare il plugin tramite prima icona e attiva una relazione per consentire la selezione figlio-padre (configurazione di default).

Ora puoi selezionare i record tra molte tabelle correlate.
Potete vedere un esempio in questo videotutorial di **Salvatore Fiandaca**: [link](https://youtu.be/EGfFCOfAS5E)

[![Plugin SelectByRelationshipv3](https://img.youtube.com/vi/EGfFCOfAS5E/0.jpg)](https://youtu.be/EGfFCOfAS5E "SelectByRelationshipv3")


## Un po' di storia:

Il plugin è iniziato da un thread originale pubblicato da **Salvatore Fiandaca** e sviluppato da **Andrea Borruso** e **Salvatore Larosa**: [Thread originale](http://osgeo-org.1560.x6.nabble.com/QGIS-select-in-join-tabella-in-relazione-td5317093.html)

Un primo post di **Andrea Borruso**: [post](https://medium.com/tantotanto/qgis-selezionare-geometrie-da-una-tabella-di-attributi-correlata-bea37747a7e2)

La macro Python originale di **Salvatore Larosa**: [link](https://gist.github.com/slarosa/653e6d759cf0d82c2a24dcc499b094e0)

Un videotutorial di **Salvatore Fiandaca** in cui viene mostrato l'uso della macro pitone di **Salvatore Larosa**: [link](https://www.youtube.com/watch?v=PRDftcPWNg8)

Un altro videotutorial di **Salvatore Fiandaca** per testare il codice macro python incorporato nel plugin selectFromRelations: [link](https://www.youtube.com/watch?v=4lXRnsMO-qI)