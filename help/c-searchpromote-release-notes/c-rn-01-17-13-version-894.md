---
description: nulle
seo-description: nulle
seo-title: Search&amp;Promote 8.9.4 - Note sulla versione (17/01/2013)
solution: Target
title: Search&amp;Promote 8.9.4 - Note sulla versione (17/01/2013)
topic: Release Notes,Site search and merchandising
uuid: a9d550f6-0a23-4c71-b123-c31b997e7384
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e

---


# Search&amp;Promote 8.9.4 Release Notes (01/17/2013){#search-promote-release-notes}

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nuove funzioni e miglioramenti </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Regole </p> </td> 
   <td colname="col2"> <p> Aggiunta la possibilità di creare note in linea quando si creano regole di pulizia query, regole di pre-ricerca e regole post-ricerca. Il campo Note consente di documentare e spiegare le regole. </p> <p>Vedere <a href="../c-about-rules-menu/c-about-query-cleaning-rules.md#concept_17F3CDDC3C8A4128AF092A82B777B86C" format="dita" scope="local"> Informazioni sulle regole</a>di pulizia delle query. </p> <p>Consultate <a href="../c-about-rules-menu/c-about-pre-search-rules.md#concept_5BF84BB6FACB4645BA9CB7496A01CD1F" format="dita" scope="local"> Le Regole</a>Di Pre-Ricerca. </p> <p>Consultate <a href="../c-about-rules-menu/c-about-post-search-rules.md#concept_AF6ADFCC0ADF4A788003964939917FDE" format="dita" scope="local"> Le Regole</a>Post-Ricerca. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Ricerca guidata </p> </td> 
   <td colname="col2"> <p> Sono stati aggiunti tag di ricerca guidata per indicare il tempo totale impiegato dalla ricerca. </p> <p> <span class="codeph"> &lt;tempo di ricerca guidata&gt;</span> - Indica per quanto tempo è durata la ricerca. Il valore restituito per l'ora di ricerca è specificato in ms. </p> <p> <span class="codeph"> &lt;ricerca guidata-fall-through&gt;</span> - Restituisce il numero di ricerche core utilizzate per creare la pagina dei risultati di ricerca. </p> <p> <span class="codeph"> &lt;search-if-fall-through-search&gt;</span> - Consente di verificare se il conteggio delle ricerche di base è maggiore di 1. </p> <p>Consultate anche Lingua diversa nei tag <a href="../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64" format="dita" scope="local"> dei modelli di</a>presentazione. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Problemi risolti**

* Il rapporto Termini ora ignora il carattere asterisco.

   Consultate [Visualizzazione del rapporto Termini o dei termini di ricerca Null...](../c-about-reports-menu/c-about-reports-menu.md#task_53B7ED1582DD4B0E8376546A7AFC789A).

* Aprite Rapporti > Rapporto termini ricerca Null, selezionate un intervallo di tempo e visualizzate il rapporto. Fate clic su una parola nel rapporto per aprire la ricerca, quindi fate di nuovo clic su Visualizza rapporto. Il numero di ricerche per la parola chiave selezionata è aumentato due volte. Questo problema è stato adesso risolto.

   Consultate [Visualizzazione del rapporto Termini o dei termini di ricerca Null...](../c-about-reports-menu/c-about-reports-menu.md#task_53B7ED1582DD4B0E8376546A7AFC789A).

* È stata eseguita un&#39;ottimizzazione delle prestazioni quando si inviano live le Regole aziendali.

   Vedere [Informazioni sulle regole](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD)aziendali.

* La capacità di rimuovere in Breadcrumb non funzionava sempre.

   Consultate [Le Breadcrumb](../c-about-design-menu/c-about-breadcrumbs.md#concept_FB8A943C594A4A1593B118141DA61F03).

* A meno che non sia stato utilizzato Rigenera, la funzione Ri-classifica non consentiva l&#39;entrata in vigore di eventuali regole di classificazione modificate nei risultati della ricerca.

   Vedere [Informazioni sulle regole](../c-about-rules-menu/c-about-ranking-rules.md#concept_F555C076759B4E81B925441CFE707397)di classificazione.

   Vedere [Informazioni Sull&#39;Indice](../c-about-index-menu/c-about-re-rank-index.md#concept_147B0A9FCD51451787DA898E06F7C692)Rank.
