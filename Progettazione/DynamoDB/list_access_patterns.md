# List Access Patterns 

<!-- 
partition key: nometenant
sortkey: keytraduzione+ KSUID (https://www.npmjs.com/package/ksuid)
secondary key: per tenere in ordine lista dall'ultima modifica
A
--> 

## traduzione
- accedere a tutte le traduzioni del tenant(a cui le traduzioni appartengono): key e la lingua di traduzione default
- accedere ad una traduzione in dettaglio(vedere tutte le lingue, chi ha modificato, quando)
- accedere al versionamento di una traduzione(vedere lista delle 5 vecchie versioni)
- accedere al versionamento di una traduzione in dettaglio(vedere tutte le lingue, da chi e quando è stata modificata)
- (FILTRAGGIO) accedere a tutte le traduzioni che contengono una parola inserita !!!! aggiungere attributo con le parole della traduzione -> facilita ricerca
- (FILTRAGGIO) accedere a tutte le traduzioni con una certa data di creazione
- (FILTRAGGIO) accedere a tutte le traduzioni che sono pubblicate ??? aggiungere GSI per pubblicazione o fare a client side
- creare una nuova traduzione(inserisco: key traduzione, lista lingue disponibili)
    - inserire traduzioni nelle lingue disponibili
- modifica traduzione((aggiungere)lingue di traduzione, traduzioni nelle lingue)
- pubblicare una traduzione
- eliminare traduzione(elimina key e tutte le traduzioni)

## tenant
- accedere lista tenant(accedere al nome e alla traduzione di default)
- accedere al dettaglio del tenant: numero trad diponibili, numero trad usate, visualizzazione token libreria??, lista utenti
- accedere al dettaglio del utente che appartiene al tenant(email, stato: datacreazione)
- modifica tenant
- elimina tenant


## import file NoSQL
il file del db si importa con NoSQLWorkbench