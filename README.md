# ChatBotRasa
Il chatbot oggetto di questo progetto ha l’obiettivo di informare i consumatori sui prodotti della Mulino Bianco (e delle altre imprese ad essa legate: Pan di Stelle e Gran Cereale). Il chatbot è stato realizzato per parlare e rispondere in italiano.
Ci si è focalizzati su un set di possibili informazioni che l’utente potrebbe voler conoscere, anche in base ai dati che si avevano a disposizione nel dataset utilizzato.
Con il dataset a disposizione sono state individuate tutte le informazioni che maggiormente interessano i consumatori. Essendo molte le informazioni si è deciso di raggrupparle in più funzionalità, in maniera tale da non avere delle conversazioni troppo lunghe. Le informazioni considerate sono relative ai gusti del consumatore, come ad esempio la categoria o un certo tipo di ingredienti. Inoltre, si è tenuta in considerazione anche la salute del consumatore, inserendo tra le informazioni anche gli allergeni.
Le possibili azioni che gli utenti potranno fare sono le seguenti:
 -  Visualizzare tutte le categorie dei prodotti presenti (ad es. torte, biscotti, …);
 -  Visualizzare come è composto il packaging del prodotto (ad es. plastica, carta, …);
 -  Visualizzare un prodotto, le diverse dimensioni dei pacchi disponibili, la porzione consigliata, la categoria in cui rientra il prodotto e gli ingredienti;
 -  Visualizzare un prodotto, i suoi ingredienti, i suoi allergeni e le sue kcal;
 -  Visualizzare i vari brand presenti, e una volta selezionato uno di essi tutti i prodotti di tale brand;
 -  Visualizzare tutti i prodotti che hanno meno calorie di quelle inserite dall’utente, per porzione;
 -  Comprare un dato prodotto.
Le funzioni che abbiamo descritto prima richiedono di accedere ad un dataset che consente al chatbot di trovare le informazioni che l’utente richiede e di registrare quelle relative alle vendite dei prodotti.
Il dataset è stato memorizzato in un database con all’interno due tabelle, una per gli ingredienti e una per gli
acquisti.

## Il dataset
Ai fini del progetto si è utilizzato un database gestito con MySQL che è un relational database management system (RDBMS) composto da un client a riga di comando che permette l’interrogazione del database e un server nel quale il database è ospitato.
I dati per popolare tale database sono stati reperiti effettuando una ricerca sul sito https://it.openfoodfacts.org/ e scaricando i risultati.
Si è poi provveduto ad aggiornare il dataset così ottenuto aggiungendo i prodotti nuovi e andando a rimuovere quelli che non sono più in commercio, inoltre si è effettuato anche una fase di ETL che è consistita soprattutto nella rimozione delle colonne inutili e nella rimozione delle righe riguardanti i prodotti non esistenti in Italia.
Infine, è stata aggiunto un attributo ad ogni riga per associare ad ogni prodotto la sua immagine.

## Conclusioni e sviluppi futuri
Si è utilizzato il framework RASA (AI) per la realizzazione di un chatbot come supporto al cliente, nella fattispecie un chatbot che guidi l’utente nella scelta dei prodotti fra quelli venduti dall’azienda Mulino Bianco.
Le funzionalità implementate (descritte nel Capitolo 3 di tale relazione) del chatbot sono rivolte principalmente ai prodotti della Mulino Bianco e di alcune delle sue controllate.
Si potrebbe pensare come un possibile sviluppo futuro di ampliare il database dei prodotti, per estenderlo pure a quelli di altre aziende oltre che creare altre funzionalità più incentrate sulle informazioni nutrizionali.
