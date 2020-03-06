---
description: nulle
seo-description: nulle
seo-title: Search&amp;Promote 8.9 - Note sulla versione (19/07/2012)
solution: Target
title: Search&amp;Promote 8.9 - Note sulla versione (19/07/2012)
topic: Release Notes,Site search and merchandising
uuid: 3853c75d-19ed-4e36-9e81-dcbffe5f5b0c
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e

---


# Search&amp;Promote 8.9 Release Notes (07/19/2012){#search-promote-release-notes}

**Nuova funzionalità**

* Miglioramenti alla gestione dei metadati - Definizione di metadati dinamici dai feed dei clienti

   Create uno schema per riconfigurare dinamicamente l’account Search&amp;Promote in base alle definizioni di metadati fornite dal cliente.
* Miglioramenti delle prestazioni di indicizzazione - Caricatore indice

   Index Loader è un nuovo metodo per importare contenuto XML direttamente in un indice Search&amp;Promote. Si tratta di un sottoinsieme della funzionalità del connettore indice esistente progettata per importare rapidamente i nostri file di feed XML standard.

**Problemi risolti e miglioramenti**

* È stato aggiunto il supporto per la modifica dell&#39;opzione di ordinamento in base a una regola business.
* Nel tag del sistema di Aiuto `<search-description>` viene visualizzato il corpo invece quando il tag meta della descrizione ha contenuto vuoto.
* Possibilità di tenere traccia degli hit di tabella applicabili per i risultati aggiunti mediante azioni basate sui risultati.
* È stato aggiunto il supporto per l&#39;invio di parametri di query tramite POST
* Durante la ricerca per indicizzazione, in alcuni casi è possibile saltare un&#39;operazione mirror_account finale.
* Gli URL di Adobe Analytics non includono gli argomenti CGI e il codice Search&amp;Promote che esegue ricerche Adobe Analytics necessarie per eliminare in modo simile gli argomenti CGI dalle chiavi URL.
* Le regole di riscrittura scomparivano in modo intermittente dall&#39;interfaccia utente dopo che erano state forzate per essere live.
* Gli account Search&amp;Promote con l&#39;impostazione Did You Mean (Hai avuto senso) impostata per fare suggerimenti a causa di risultati ridotti potrebbero presentare risultati intermittenti.
* L&#39;output del test della regola di riscrittura non conteneva interruzioni di riga.
* Le pagine Regole URL di ricerca e Regole URL store elenco ricerca puntate sulla pagina Cronologia errata.
* Facendo clic su Modifica su alcuni banner, la pagina Modifica non veniva visualizzata.
* La riclassificazione del codice di aggiornamento a volte potrebbe essere straordinariamente lenta.
* La rimozione o lo spostamento di un elemento facet non funzionava se il nome del facet utilizzava maiuscole e minuscole miste.
