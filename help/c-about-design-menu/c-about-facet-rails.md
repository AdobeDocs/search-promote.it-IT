---
description: Utilizzate la barra laterale facet per riordinare gruppi di facet in una pagina Web.
seo-description: Utilizzate la barra laterale facet per riordinare gruppi di facet in una pagina Web.
seo-title: Informazioni su Facet Rail
solution: Target
subtopic: Navigation
title: Informazioni su Facet Rail
topic: Design,Site search and merchandising
uuid: 6da2bd67-8c20-4955-9836-bc8ba88546c5
translation-type: tm+mt
source-git-commit: 6b3aa733b0dfaace956f0ffc25f433fefd21e15f

---


# Informazioni su Facet Rail{#about-facet-rail}

Utilizzate la barra laterale facet per riordinare gruppi di facet in una pagina Web.

## Utilizzo della barra laterale {#concept_1FDC8BCDFFC84A0889DA670F63D5F6DB}

Un facet è una proprietà o una caratteristica, È un modo per classificare generalmente i risultati della ricerca. Ad esempio, produttore, prezzo e colore possono essere considerati un gruppo di facet. Ciascun facet può avere più vincoli o valori. Ad esempio, se il colore era una facet, i &quot;valori di facet&quot; potrebbero essere rosso, arancione, giallo, verde, blu, indigo e viola.

Consultate [I facet](../c-about-design-menu/c-about-facets.md#concept_FA912B3B41EE493DB2F492D188457FF5).

Per riordinare questi gruppi di facet in una pagina Web, usate la Barra di Facet. Ad esempio, supponiamo che sul lato sinistro di una pagina Web sia presente una sezione di risultati della ricerca. La sezione elencava, dall’alto verso il basso, un facet Categoria, un facet Marchio, un facet Prezzo e un facet Più popolare. Utilizzando una barra laterale, potete ad esempio fare in modo che il facet Più popolare venga visualizzato sopra o sotto il facet Categoria.

Il gruppo di facet da riordinare insieme appartiene a un tag di barra facet. Un facet può appartenere a una sola barra laterale. La barra laterale è un tag del modello Presentazione e racchiude una singola rappresentazione di un facet. Tutti i facet appartenenti a questa barra laterale condividono la rappresentazione di un solo facet.

Consultate [I modelli](../c-about-design-menu/c-about-templates.md#concept_06EB481B14864E18A8AE2BCD1D6EF0B5) e il facet nei tag [dei modelli di](../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64)presentazione.

## Configurazione di una barra laterale {#task_561A8FF1CAD1402B9DD33E276BBC6A0E}

Potete aggiungere una barra laterale per personalizzare il livello della presentazione. Le guide dei facet forniscono ai clienti una ricerca guidata che consente loro di approfondire i risultati della ricerca in base all’ordine dei facet nella pagina Web.

<!-- 

t_configuring_facet_rail.xml

-->

Qualsiasi modifica apportata alle barre dei facet può essere ripristinata utilizzando la funzione Cronologia.

**Per configurare una barra laterale**

1. Prima di configurare una barra laterale, accertatevi di aver già aggiunto un facet e, come parte di tale attività, di aver specificato un nome per la barra laterale facet.

   Consultate [Aggiunta di un nuovo facet](../c-about-design-menu/c-about-facets.md#task_FC07BFFA62CA4B718D6CBF4F2855C89B).
1. Nel menu del prodotto, fate clic su **[!UICONTROL Design]** > **[!UICONTROL Navigation]** > **[!UICONTROL Facet Rail.]**
1. Nella [!DNL Facet Rail] pagina, selezionate i facet da includere nella barra laterale, quindi impostate l’ **[!UICONTROL Sort Facets Method]** opzione dall’elenco a discesa.

   <!-- 
   r_facet_rail_options.xml
   -->

   | Funzionalità/Opzione | Descrizione |
   |--- |--- |
   | Nome barra laterale facet | Identifica il nome della barra laterale.  Il nome della barra laterale viene creato al momento dell’aggiunta del facet.  Consultate [Aggiunta di un nuovo facet](../c-about-design-menu/c-about-facets.md#task_FC07BFFA62CA4B718D6CBF4F2855C89B) |
   | Facet inclusi | Elenco di possibili facet che è possibile selezionare per aggiungere alla barra laterale facet.  Se si sceglie di ordinare i facet utilizzando `Custom`l&#39;ordine in cui vengono selezionati, l&#39;ordine in cui vengono visualizzati nella `Custom Facet Order` casella di testo dipende dall&#39;ordine in cui sono visualizzati. |
   | Metodo Sort Facets | Scegliere una delle tre opzioni seguenti nell&#39;elenco a discesa:<ul><li>`Alpha` I facet sono ordinati in ordine alfabetico rispetto ai loro nomi, inclusi i caratteri di punteggiatura.</li><li>`Alpha (not case sensitive)` I facet sono ordinati in ordine alfabetico rispetto ai loro nomi, ignorando le maiuscole e le minuscole dei caratteri alfabetici e includendo i caratteri di punteggiatura. </li><li>`Alpha (alphanumeric only)` I facet sono ordinati in ordine alfabetico rispetto ai loro nomi, ignorando i caratteri di punteggiatura. </li><li>`Alpha (not case sensitive, alphanumeric only)` I facet sono ordinati in ordine alfabetico rispetto ai loro nomi, ignorando le maiuscole e le minuscole dei caratteri alfabetici e ignorando i caratteri di punteggiatura. </li><li>`Count` I facet sono ordinati in base al numero. </li><li>`Custom` Apre la casella `Custom Facet Order` di testo che consente di definire l&#39;ordine dei facet immettendo il nome esatto di ciascun facet. Le etichette dei facet escluse vengono rimosse dall’ `Custom Facet Order` elenco.</li></ul> |
   | Ordine facet personalizzato | Questa opzione è disponibile solo se è stata selezionata `Custom` dall&#39;elenco a `Sort Facets Method` discesa.  Consente di elencare i nomi dei facet, uno per riga o tutti su una riga e separati da virgola. Se le etichette dei facet sono definite, vengono visualizzate nell&#39; `Facets Included` elenco, racchiuse tra parentesi.  Non includete le etichette dei facet nella `Custom Facet Order` casella di testo.  Quando selezionate o deselezionate i facet nell&#39; `Facets Included` elenco, la casella di `Custom Facet Order` testo viene aggiornata automaticamente. |

1. Clic **[!UICONTROL Save Changes]**.
1. (Facoltativo) Nella [!DNL Facet Rail] pagina, effettuare una delle seguenti operazioni:

   * Fate clic **[!UICONTROL History]** per annullare le modifiche apportate.

      Consultate [Utilizzo dell’opzione](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Cronologia.

   * Clic **[!UICONTROL Live]**.

      Consultate [Visualizzazione delle impostazioni](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)dal vivo.

   * Clic **[!UICONTROL Push Live]**.

      Consultate [Invio live](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)delle impostazioni dell’area di visualizzazione.

1. Modificate il modello Presentazione effettuando le seguenti operazioni:.

   * Create un &quot;modello di facet&quot; sul modello di presentazione.
   * Circondare il &quot;modello facet&quot; con i `<guided-facet-rail>` tag.

      Consultate Facet (Facet) nei tag [dei modelli di](../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64)presentazione.

      Esempio:

      ```
      <guided-facet-rail>
        <guided-facet>
          <guided-facet-display-name/>
          ...
          </guided-facet>
        </guided-facet-rail>
      ```

      Questi tag disegnano una sezione del modello di presentazione in modo che diventi un pattern ripetibile per ciascun facet nella barra dei facet. Ogni facet appartenente alla barra sfaccettatura utilizza questa sezione per valutarne l’output. Nel modello di presentazione finale può essere visualizzato un solo `<guided-facet-rail>` tag.

      I seguenti tag non richiedono l&#39; `gsname` attributo inside, `<guided-facet-rail>` perché il valore viene determinato in modo dinamico in fase di ricerca e viene sostituito correttamente:

      `<guided-facet>`
      `<guided-facet-display-name>`
      `<guided-facet-total-count>`
      `<guided-facet-undo-link>`
      `<guided-facet-undo-path>`
      `<guided-facet-behavior>`

   * Salvate il modello di presentazione e inviatelo live.

      Consultate [Modifica di una presentazione o di un modello](../c-about-design-menu/c-about-templates.md#task_800E0E2265C34C028C92FEB5A1243EC3)di trasporto.