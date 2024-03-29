---
description: Scopri come utilizzare i tag presentazione e modello in Search&amp;Promote.
solution: Target
title: Modelli
topic-legacy: Appendices,Site search and merchandising
uuid: 78299032-dc23-4dfe-b68f-cd57b2b6d7d8
exl-id: f8cc4b5c-4e75-426b-8234-76af8bb0f4c5
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '15148'
ht-degree: 2%

---

# Modelli{#templates}

## Modelli {#concept_A5CFB6BD805D49459A96219AF1B17842}

## Tag del modello di presentazione {#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64}

Elenco di tag e attributi di ricerca/merchandising del sito per i modelli di presentazione.


Un modello di presentazione è un file HTML che include i tag del modello di presentazione definiti da site search/merchandising. Questi tag indicano come vengono formattati i risultati della ricerca visualizzati dai clienti.

Consulta [Informazioni sui modelli](../c-about-design-menu/c-about-templates.md#concept_06EB481B14864E18A8AE2BCD1D6EF0B5).

È possibile selezionare tra i seguenti gruppi di tag di presentazione:

* [Dichiarazioni](../c-appendices/c-templates.md#section_82C5CA734D2941EB858FEFE3B695D2EC)
* [Risultati](../c-appendices/c-templates.md#section_06F249C9F6AE4B0F8C32117E19DCC905)
* [Facet](../c-appendices/c-templates.md#section_EA4C5678D5864B89BAB4D0DFE62A4624)
* [Breadcrumb](../c-appendices/c-templates.md#section_9B39B71FA6EC49FA8D88AD8A3BA987F7)
* [Menu](../c-appendices/c-templates.md#section_1D489ADF041F4351A66E5D5742125CA8)
* [Pagenav](../c-appendices/c-templates.md#section_2EE397635C514BBC8D668278EA314F35)
* [Ricerche recenti](../c-appendices/c-templates.md#section_8CD907521F584257B475595B01A5964B)
* [Voleva Dire?](../c-appendices/c-templates.md#section_C1EB3B9D8E1242798A6E04609D1E3543)
* [Autocompletamento](../c-appendices/c-templates.md#section_897316BEE1454E839A56B565CA4AF018)
* [Store](../c-appendices/c-templates.md#section_A33E25DB5E67404A823BD9618665B773)
* [Zone](../c-appendices/c-templates.md#section_B9B3179E000C42D492E1541F2FE44CB5)
* [Indicatori di loop](../c-appendices/c-templates.md#section_387322CA0AA843A2ACF2795C328673E9)
* [Lingua varie](../c-appendices/c-templates.md#section_BFE8DC98E26F4D7BB60FEC54D9A5DC6C)

## Dichiarazioni {#section_82C5CA734D2941EB858FEFE3B695D2EC}

Le dichiarazioni sono speciali tag di dichiarazione guidata che è possibile impostare nella parte superiore di un modello di presentazione di livello superiore. Tutte le dichiarazioni successive vengono ignorate, incluse quelle nei modelli inclusi.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Tag </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-content-type-header content="content-type"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Per impostazione predefinita, il modello di presentazione viene inviato nuovamente con un tipo mime di text/html. Puoi modificare il tipo di contenuto utilizzato con questo tag. </p> <p>Dichiara questo tag il più in alto possibile nel modello di presentazione. Non aggiungere altro testo sulla stessa riga con questo tag. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-xml-declare&gt; </span> </p> </td> 
   <td colname="col2"> <p> Se si restituisce un file XML, è possibile utilizzare questo tag per creare la dichiarazione XML. Crea questo tag come prima riga nel modello di presentazione. Quando utilizzi questo tag, il tipo di contenuto viene impostato automaticamente su text/xml, a meno che non venga sovrascritto con <span class="codeph"> &lt;guidato-content-type-header&gt; </span> nella prima riga. Se non si specifica un set di caratteri, viene impostato automaticamente su UTF-8. Questo tag genera il seguente output nel documento XML: </p> <p> <span class="codeph"> &lt;?xml version="1.0" encoding="charset-name" standalone="yes" ?&gt; </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Risultati {#section_06F249C9F6AE4B0F8C32117E19DCC905}

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Tag </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng 1/31/13--> <span class="codeph"> &lt;guided-results&gt;&lt;/guided-results&gt; </span> </p> </td> 
   <td colname="col2"> <p>Il tag dei risultati guidati definisce i limiti di un ciclo di risultati. È possibile accedere a qualsiasi set di risultati specificando un attributo <span class="codeph"> gsname </span> . Se non viene fornito alcun <span class="codeph"> gsname </span>, vengono visualizzati i risultati di ricerca predefiniti. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng 1/31/13--> <span class="codeph"> &lt;guided-result-link&gt;&lt;/guided-result-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Per creare un collegamento a un dato risultato, utilizza il tag <span class="codeph"> guidato-result-link </span> . Definendo un attributo <span class="codeph"> gsname </span>, è possibile utilizzare un campo dall'indice invece del tag "loc" standard che fa riferimento all'"url di ricerca". Possono essere passati anche tutti gli altri attributi, ad esempio class e target, che vengono generati nel tag di ancoraggio risultante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng 1/31/13--> <span class="codeph"> &lt;guided-result-img gsname="fieldname"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Il tag <span class="codeph"> &lt;guide-result-img&gt; </span> consente di creare tag immagine anziché incorporare variabili all’interno di un tag <span class="codeph"> img </span> non elaborato. </p> <p>Specifica il campo da utilizzare per il percorso dell'immagine nell'attributo <span class="codeph"> gsname </span> . Il risultato è un tag <span class="codeph"> img </span> con tutti gli attributi HTML standard definiti e trasmessi. Quindi, l'esempio seguente: </p> <p> <code class="syntax html"> &lt;guided-result-img&nbsp;gsname="thumbnail" 
      &nbsp;class="thumb"&nbsp;border="0"/&gt; </code> </p> <p>diventa: </p> <p> <code class="syntax html"> &lt;img&nbsp;src="prod8172.jpg"&nbsp;class="thumb" 
      &nbsp;border="0"/&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 1/31/13; search-eng version does not have [escape...] Added ijson on 8/28/2015--> <span class="codeph"> &lt;guided-result-field gsname="fieldname"&gt; </span> </p> </td> 
   <td colname="col2"> <p> Tutte le informazioni da presentare nei risultati vengono visualizzate come tag <span class="codeph"> &lt;campo-risultato-guidato&gt; </span> (tranne quando si utilizzano tag di generazione automatica come <span class="codeph"> &lt;tag-risultato-img&gt; </span> ). </p> <p>Specifica il nome del campo dell'indice di ricerca in <span class="codeph"> gsname </span>. La stringa esatta passata viene emessa nel modello. </p> <p>Puoi specificare un’opzione di escape se desideri che questo campo sia preceduto da una sequenza di escape diversa da quella specificata nel modello di trasporto. </p> <p>Questa codifica viene applicata oltre a qualsiasi codifica specificata nel modello di trasporto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> 
     <span class="codeph"> &lt;guided-if&gt;&lt;/guided-if-result-field&gt; </span> </p> </td> 
   <td colname="col2"> <p>Questo set di tag condizionali è true se nel campo specifico è presente del contenuto da visualizzare. Se non esiste alcun contenuto, la condizione è false. È possibile utilizzare i tag per decidere se l’HTML circostante viene visualizzato o meno se non esiste un valore, se viene visualizzata un’immagine diversa e così via. </p> <p> <code class="syntax html"> &lt;guided-if-result-field&nbsp;gsname="thumbnail"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-result-img&nbsp;gsname="thumbnail"&nbsp;class="thumb"&nbsp;/&gt; 
      &lt;guided-else-result-field&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;img&nbsp;src="nothumb.jpg"&nbsp;class="nothumb"&nbsp;/&gt; 
      &lt;/guided-if-result-field&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> 
     <code> &lt;guided-if[-not]-result-wrap&gt; 
      &lt;guided-else-result-wrap&gt; 
      &lt;/guided-if[-not]-result-wrap&gt; </code> </p> </td> 
   <td colname="col2"> <p>Quando si visualizzano i risultati in colonne, questo tag viene utilizzato per identificare se il risultato corrente segna la fine di una colonna. </p> <p>Quando la condizione booleana è true, l’HTML viene aggiunto alla fine del risultato per terminare la riga e avviarne una nuova. Quando è l’ultima, non viene avviata una nuova riga. </p> <p>Per ulteriori informazioni su tale tag, consulta <span class="codeph"> &lt;guidato-if-not-last&gt; </span> . </p> <p> <code class="syntax html"> &lt;guided-if-result-wrap&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/div&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-not-last&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;div&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-not-last&gt; 
      &nbsp;&lt;/guided-if-result-wrap&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng version, 1/31/13--> <span class="codeph"> &lt;guided-results-found&gt; </span> </p> </td> 
   <td colname="col2"> <p>Restituisce un 1 se la richiesta di ricerca back-end ha restituito risultati e 0 se non lo ha fatto. Se non viene specificato alcun nome gsname </span> <span class="codeph">, il tag considera la ricerca primaria. Questo tag è utile per passare la logica alle routine JavaScript. </span></p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng version 1/31/13--> <span class="codeph"> &lt;guided-results-total&gt; </span> </p> </td> 
   <td colname="col2"> <p>Restituisce il numero totale di risultati nell'insieme di risultati specificato. Presuppone la ricerca predefinita quando non viene fornito alcun nome gsname </span>.<span class="codeph"> </span></p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng version 1/31/13--> <span class="codeph"> &lt;guided-results-lower&gt; </span> </p> </td> 
   <td colname="col2"> <p>Restituisce il numero di risultato del risultato inferiore nella pagina per il set di risultati specificato. Presuppone la ricerca predefinita quando non viene fornito alcun nome gsname </span>.<span class="codeph"> </span></p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng version 1/31/13--> <span class="codeph"> &lt;guided-results-upper&gt; </span> </p> </td> 
   <td colname="col2"> <p>Restituisce il numero di risultato del risultato superiore nella pagina per il set di risultati specificato. Presuppone la ricerca predefinita quando non viene fornito alcun nome gsname </span>.<span class="codeph"> </span></p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>11 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version 1/31/13--> 

    &amp;lt;/guidato-if[-not]-results-found&amp;gt;   &lt;/p>  &lt;/td>
<td colname="col2"> <p>Mostra il contenuto quando vengono trovati i risultati. Oppure, non mostra alcun risultato HTML quando i risultati non vengono trovati. </p> <p> <code class="syntax html"> &lt;guided-if-results-found&nbsp;gsname="products"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-results&nbsp;gsname="products"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;... 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-results&gt; 
      &lt;guided-else-results-found&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;No&nbsp;results&nbsp;were&nbsp;found. 
      &lt;/guided-if-results-found&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>12 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-result-title /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Il tag <span class="codeph"> &lt;driven-result-title&gt; </span> fornisce il valore del campo del modello di trasporto del titolo specificato con il tag di trasporto <span class="codeph"> &lt;title&gt; </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>13 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-result-description /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Il tag <span class="codeph"> &lt;guidate-result-description&gt; </span> fornisce il valore del campo del modello di trasporto della descrizione specificato con il tag di trasporto <span class="codeph"> &lt;description&gt; </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>14 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-result-loc /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Il tag &lt; <span class="codeph"> guidato-result-loc&gt; </span> fornisce il valore del campo del modello di trasporto loc specificato con il tag di trasporto <span class="codeph"> &lt;loc&gt; </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>15 </p> </td> 
   <td colname="col1"> <p> 

    &amp;lt;/guidato-if-result-field&amp;gt;   &lt;/p>  &lt;/td>
<td colname="col2"> <p>True se nel campo specifico è presente del contenuto da visualizzare. Se non esiste alcun contenuto, la condizione è false. Utilizza i tag per decidere se l’HTML circostante viene visualizzato o meno se non esiste un valore, se viene visualizzata un’immagine diversa e così via. </p> <p> <code class="syntax html"> &lt;guided-if-result-field&nbsp;gsname="thumbnail"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-result-img&nbsp;gsname="thumbnail"&nbsp;class="thumb"/&gt; 
      &lt;guided-else-result-field&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;img&nbsp;src="nothumb.jpg"&nbsp;class="nothumb"/&gt; 
      &lt;/guided-if-result-field&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>16 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-result-attribute-table gsname="tablename"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Questo tag fornisce una tabella di attributi a ciclo continuo definita nel modello di trasporto con tag di trasporto <span class="codeph"> &lt;attribute_table&gt; </span> . Per visualizzare i valori dei campi della tabella attributi è disponibile il tag <span class="codeph"> &lt;guide-result-attribute-table-field&gt; </span> . È inoltre possibile utilizzare tag <span class="codeph"> campi-risultati guidati </span> all'interno del ciclo per visualizzare altri campi risultato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>17 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-result-attribute-table-field gsname="fieldname"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Visualizza il campo della tabella attributi come definito nel modello di trasporto. </p> <p> 

    ...
    
    &amp;lt;ul&amp;gt;
    
    &amp;lt;guidato-risultato-attributo-tabella&amp;nbsp;gsname=&quot;download&quot;&amp;gt;
    &amp;nbsp;&amp;nbsp;&amp;lt;li&amp;gt;
    &amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;lt;a&amp;nbsp;href=&quot;&amp;lt;guidato-risultato-attributo-tabella-campo&amp;nbsp;gsname=&quot;download_link&quot;&amp;nbsp;/&amp;gt;&quot;&amp;gt;
    &amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;lt;campo-tabella dei risultati guidati bsp;gsname=&quot;download_title&quot;&amp;nbsp;/&amp;gt;
    &amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;lt;/a&amp;gt;&amp;nbsp;(&amp;lt;guidato-result-field&amp;nbsp;gsname=&quot;title&quot;/&amp;gt;)
    &amp;nbsp; sp;&amp;lt;/li&amp;gt;
    &amp;lt;/guidato-result-attribute-table&amp;gt;
    
    &amp;lt;/ul&amp;gt;
    
    ..
    
    &amp;lt;/risultati guidati&amp;gt;   &lt;/p>  &lt;/td>
</tr> 
  <tr> 
   <td colname="col01"> <p>18 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW for S&P 8.17.0 release in October 2014--> <span class="codeph"> &lt;guided-trace&gt; </span> </p> </td> 
   <td colname="col2"> <p>Invia le informazioni di traccia trovate all’interno dei dati di traccia nella sezione generale dell’output di dati JSON dal modello di trasporto per la ricerca specificata. </p> <p>Se non viene specificato alcun nome di ricerca, viene assunto <span class="codeph"> il valore predefinito </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>19 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW for S&P 8.17.0 release on October 30, 2014)--> <span class="codeph"> &lt;guided-result-trace /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Invia il contenuto JSON trovato all’interno dei risultati &gt; informazioni di traccia dell’output di dati JSON dal modello di trasporto per il risultato della ricerca corrente. </p> <p>Questo tag è valido solo nel ciclo <span class="codeph"> &lt;Guidata-results&gt;&lt;/Wizard-results&gt; </span> . </p> </td> 
  </tr> 
 </tbody> 
</table>

## Facet {#section_EA4C5678D5864B89BAB4D0DFE62A4624}

I facet sono componenti di navigazione che consentono di approfondire i risultati della ricerca. È possibile utilizzare i tag facet per visualizzare vari facet nel modello di presentazione. Fate riferimento ai facet per nome.

Consultare [Informazioni sui facet](../c-about-design-menu/c-about-facets.md#concept_FA912B3B41EE493DB2F492D188457FF5).

Consulta [Informazioni sulla barra laterale](../c-about-design-menu/c-about-facet-rails.md#concept_1FDC8BCDFFC84A0889DA670F63D5F6DB).

Consulta [Informazioni sui facet dinamici](../c-about-design-menu/c-about-dynamic-facets.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899).

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Tag </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW 02/27/2014--> <span class="codeph"> &lt;guided-dynamic-facets&gt;&lt;/guided-dynamic-facets&gt; </span> </p> </td> 
   <td colname="col2"> 
    <!--NEW 2/2/2014--> <p>Un contesto di looping per tutti i facet dinamici per una determinata ricerca. </p> <p>Il tag del modello di presentazione <span class="codeph"> &lt;facet-guidato&gt; </span> viene modificato in modo che l'attributo gsname venga fornito automaticamente dal contesto di ciclo <span class="codeph"> &lt;facet-dynamic-guidato&gt; </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-display-name gsname=" <span class="varname"> facetname </span>" /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Restituisce l’etichetta di visualizzazione del facet. </p> <p>Se il facet utilizza il tag <span class="codeph"> &lt;display-name&gt; </span> sul modello di trasporto, il contenuto del tag diventa l’etichetta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng version 1/31/13--> <span class="codeph"> &lt;guided-facet-rail&gt;&lt;/guided-facet-rail&gt; </span> </p> </td> 
   <td colname="col2"> <p> Definisce una sezione del modello di presentazione utilizzata come pattern ripetuto per ciascun facet nella barra dei facet. </p> <p> Ogni facet appartenente alla barra dei facet utilizza questa sezione per valutarne l’output. </p> <p>Esempio di barra facet: </p> <p> <code class="syntax html"> &lt;guided-facet-rail&gt; 
      &nbsp;&nbsp;&lt;guided-facet&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-display-name/&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;... 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet&gt; 
      &nbsp;&nbsp;&lt;/guided-facet-rail&gt; </code> </p> <p>Tieni presente che i seguenti tag non richiedono l’attributo <span class="codeph"> gsname </span> quando si trovano all’interno del tag <span class="codeph"> &lt;guide-facet-rail&gt; </span> , in quanto il valore viene determinato dinamicamente al momento della ricerca e viene sostituito correttamente: </p> 
    <ul id="ul_5B5ACAFD2B8848DDB27471AB9DA7BE6E"> 
     <li id="li_5A07E78D51FE4708879DD742C877FFFF">facet guidato </li> 
     <li id="li_B875DCACD7AB4FC890A456A6939AB657">nome-visualizzazione-facet-guidato </li> 
     <li id="li_B70450749E864DE7BA401E3CD6EF5EB3">conteggio totale facet-guidato </li> 
     <li id="li_DECDF5EF6FF7454F86C236D322F2BFEA">collegamento-facet-undo-link guidato </li> 
     <li id="li_176949227AC14E8CA643A419E10F7B5A">facet-undo-path guidato </li> 
     <li id="li_B32D981281744462BC680F6EFEAC0069">comportamento-facet-guidato </li> 
    </ul> <p>I criteri di ordinamento nella pagina <span class="wintitle"> Barra dei facet </span> determinano la posizione dei facet. È possibile scegliere l'ordinamento dall'elenco a discesa Ordina facet Metodo. </p> <p> 
     <!--NEW 02/27/2014-->Facoltativamente, questo tag può accettare un valore di attributo gsname di  <span class="codeph"> _dynamic_facets  </span>, che fornisce un contesto di looping per qualsiasi facet dinamico per questa ricerca. Questa barra dei facet predefinita è inoltre esposta nell’interfaccia utente delle Regole aziendali per l’azione <span class="codeph"> facet push X nella barra dei facet '_dynamic_facets' per la posizione Y </span>". </p> <p>Consulta <a href="../c-about-design-menu/c-about-facet-rails.md#concept_1FDC8BCDFFC84A0889DA670F63D5F6DB" format="dita" scope="local"> Informazioni sulla barra laterale </a>. </p> <p>Vedere anche <a href="../c-about-design-menu/c-about-dynamic-facets.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899" format="dita" scope="local"> Informazioni sui facet dinamici </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match current search-eng version 1/31/13--> <span class="codeph"> &lt;guided-facet gsname=" <span class="varname"> facetname </span>" height=" <span class="varname"> 60px </span>" width=" <span class="varname"> 120px </span>"&gt;&lt;/guided-facet&gt; </span> </p> </td> 
   <td colname="col2"> <p>Utilizza il tag <span class="codeph"> facet guidato </span> per definire un’area all’interno della quale tutti i tag facet si riferiscono a un facet specifico. Questo tag è anche un tag booleano che nasconde tutto il contenuto se non esistono valori nel facet. In tal caso, non ha senso trasmettere i valori dei facet). </p> <p>Gli attributi di altezza e larghezza sono facoltativi e le dimensioni sono specificate in pixel (px). Il Generatore di regole visive (VRB) utilizza questi due attributi e visualizza una casella punteggiata come segnaposto interattivo quando il facet è nascosto. </p> <p> Quando il nome visualizzato è nel facet e il facet è nascosto, anche il nome è nascosto. Tuttavia, se il nome è all’esterno del facet, puoi nasconderlo solo se intorno a esso è racchiuso un tag <span class="codeph"> zona </span> o un tag <span class="codeph"> guidato-if-facet-visible </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW, brought in from search-eng version, 1/31/13--> <span class="codeph"> &lt;guided-if&gt;&lt;/guided-if&gt; </span> </p> </td> 
   <td colname="col2"> <p>Questo tag condizionale è true quando il numero di valori di facet supera la soglia di lunghezza definita nella configurazione. Utilizzalo per visualizzare un facet come elemento dell’interfaccia diverso (ad esempio un elenco troncato o una casella di scorrimento) quando l’elenco è troppo lungo. </p> <p> <code class="syntax xml"> &lt;guided-facet&nbsp;name="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-long&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;select&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-option&nbsp;/&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/select&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-long&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-value-link&gt;&lt;guided-facet-value&nbsp;/&gt;&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-long&gt; 
      &lt;/guided-facet&gt; </code> </p> <p>Puoi anche utilizzare questa condizione al di fuori del contesto di un blocco <span class="codeph"> di facet guidato </span> facendo riferimento a un facet specifico direttamente tramite l'utilizzo dell'attributo <span class="codeph"> gsname </span> . </p> <p> <code class="syntax html"> &lt;guided-if-facet-long&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;The&nbsp;category&nbsp;facet&nbsp;is&nbsp;very&nbsp;long! 
      &lt;/guided-if-facet-long&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW, brought in from search-eng version, 1/31/13--> <span class="codeph"> &lt;guided-if&gt;&lt;/guided-if&gt; </span> </p> </td> 
   <td colname="col2"> <p>Questo tag condizionale è true quando si fa clic almeno una volta sul facet e si seleziona attualmente un valore di facet. Viene utilizzato per mostrare o nascondere i tag HTML o gs a seconda che sia stato fatto clic su un facet. </p> <p> <code class="syntax html"> &lt;guided-facet&nbsp;name="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;This&nbsp;facet&nbsp;has&nbsp;been&nbsp;selected.&nbsp;&nbsp;You&nbsp;can&nbsp;no&nbsp;longer&nbsp;refine&nbsp;it. 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-value-link&gt;&lt;guided-facet-value&nbsp;/&gt;&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-selected&gt; 
      &lt;/guided-facet&gt; </code> </p> <p>Puoi anche utilizzare questa condizione al di fuori del contesto di un blocco <span class="codeph"> di facet guidato </span> facendo riferimento a un facet specifico direttamente tramite l'utilizzo dell'attributo <span class="codeph"> gsname </span> . </p> <p> <code> &lt;guided-if-facet-selected&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;The&nbsp;category&nbsp;facet&nbsp;is&nbsp;selected! 
      &lt;/guided-if-facet-selected&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW, brought in from search-eng version, 1/31/13--> <span class="codeph"> &lt;guided-if&gt;&lt;/guided-if&gt; </span> </p> </td> 
   <td colname="col2"> <p>Questo tag condizionale è true quando esiste un solo valore di facet. Utilizza il tag per modificare la visualizzazione del facet quando non è in grado di perfezionare i risultati. </p> <p> <code class="syntax html"> &lt;guided-facet&nbsp;name="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-single&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Facet&nbsp;is&nbsp;not&nbsp;refinable. 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-single&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-value-link&gt;&lt;guided-facet-value&nbsp;/&gt;&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-single&gt; 
      &lt;/guided-facet&gt; </code> </p> <p>Puoi anche utilizzare questa condizione al di fuori del contesto di un blocco <span class="codeph"> di facet guidato </span> facendo riferimento a un facet specifico direttamente tramite l'utilizzo dell'attributo <span class="codeph"> gsname </span> . </p> <p> <code class="syntax html"> &lt;guided-if-facet-single&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;There&nbsp;is&nbsp;only&nbsp;one&nbsp;value&nbsp;in&nbsp;the&nbsp;category&nbsp;facet! 
      &lt;/guided-if-facet-single&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> 
     <!--Added 7/15/2014--> <span class="codeph"> &lt;guided-if&gt;&lt;/guided-if&gt; </span> </p> </td> 
   <td colname="col2"> <p>Questo tag condizionale è true quando il facet è a selezione multipla. Utilizza il tag per modificare la visualizzazione del facet all’interno dei tag <span class="codeph"> &lt;guide-facet-rail&gt; </span> o <span class="codeph"> &lt;guide-dynamic-facet&gt; </span> . </p> <p> 

    &amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;lt;guidato-if-facet-multiselect&amp;gt;
    &amp;nbsp;..
    &amp;nbsp;&amp;lt;guidato-else-facet-multiselect&amp;gt;
    &amp;nbsp;..
    &amp;nbsp;&amp;lt;/guidato-if-facet-multiselect&amp;gt;
    &amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;...
    &amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;lt;/guide-facet&amp;gt;
    &amp;nbsp;&amp;nbsp;&amp;lt;/guide-facet-rail&amp;gt;   &lt;/p>  &lt;/td>
</tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng version 1/31/13--> <span class="codeph"> &lt;guided-facet-values&gt; facetname  </span>"]&gt;&lt;/guided-facet-values&gt; </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>Questo è il tag iteratore del ciclo di valori facet. Puoi definirlo nel contesto di un blocco <span class="codeph"> a facet guidato </span> , nel qual caso puoi omettere il <span class="codeph"> <span class="varname"> gsname </span> </span>. Oppure, puoi definirlo al di fuori di qualsiasi blocco <span class="codeph"> di facet guidato </span>, ma richiederebbe l'attributo <span class="codeph"> <span class="varname"> gsname </span> </span> per identificare quale set di valori di facet viene visualizzato. </p> <p>Puoi inoltre utilizzare questo tag per visualizzare i valori dei facet al di fuori del contesto di un blocco <span class="codeph"> a facet guidato </span> denominato . Fai riferimento direttamente a un facet specifico utilizzando l'attributo <span class="codeph"> <span class="varname"> gsname </span> </span> . </p> <p> <code class="syntax html"> &lt;script&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;registerFacetValues('category',&nbsp;'&lt;guided-facet-values&nbsp;gsname="category"&gt;&lt;guided-facet-value/&gt;,&lt;/guided-facet-values&gt;'); 
      &lt;/script&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version 1/31/13--> <span class="codeph"> &lt;guided-facet-value&gt; </span> </p> </td> 
   <td colname="col2"> <p>Invia la stringa del valore del facet corrente. </p> <p>Per impostazione predefinita, il valore è un escape HTML. Puoi utilizzare l’opzione escape per modificare la modalità di escape del valore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>11 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng version 1/31/13--> <span class="codeph"> &lt;guided-facet-count /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Visualizza il numero di risultati che corrispondono al valore del facet corrente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>12 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW, brought in from search-eng version, 1/31/13--> <span class="codeph"> &lt;guided-facet-value-link&gt;&lt;/guided-facet-value-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Crea un collegamento intorno alla stringa del valore del facet su cui il visitatore del sito può fare clic. Il percorso viene generato automaticamente per limitare i risultati in base al valore del facet corrente. Supporta il passaggio di qualsiasi attributo direttamente al tag di ancoraggio. </p> <p> <code class="syntax html"> &lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-value-link&nbsp;class="facetlink"&gt;&lt;guided-facet-value&nbsp;/&gt;&lt;/guided-facet-value-link&gt; 
      &lt;/guided-facet-values&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>13 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version 1/31/13--> <code> &lt;guided-if-facet-value-selected&gt; 
      &lt;guided-else-facet- 
      value-selected&gt; 
      &lt;/guided-if-facet-value-selected&gt; </code> </p> </td> 
   <td colname="col2"> <p>Modifica la visualizzazione del valore del facet quando è attualmente selezionato. Se è già stato scelto, nella maggior parte dei casi non è più collegabile. </p> <p> <code class="syntax html"> &lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-value-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;b&gt;&lt;guided-facet-value/&gt;&lt;/b&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-value-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-link&gt;&lt;guided-facet-value/&gt;&lt;/guided-facet-link&gt;&nbsp;&nbsp;&nbsp; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-value-selected&gt; 
      &lt;/guided-facet-values&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>14 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version 1/31/13--> 

    &amp;lt;/guidato-if[-not]-facet-value-fantasma&amp;gt;   &lt;/p>  &lt;/td>
<td colname="col2"> <p>Modifica la visualizzazione del valore facet quando è un valore fantasma. Quando un valore facet è un valore fantasma, in genere viene visualizzato in corsivo per indicare che il valore è mancante o "fantasma". </p> <p>Il seguente estratto di codice è un esempio di blocco di facet: </p> <p> <code class="syntax html"> &lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-value-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;b&gt;&lt;guided-facet-value&nbsp;/&gt;&nbsp;(&lt;guided-facet-count&nbsp;/&gt;)&lt;/b&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-value-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-value-ghost&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;i&gt;&lt;guided-facet-value&nbsp;/&gt;&nbsp;(0)&lt;/i&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-value-ghost&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-link&nbsp;class="link"&gt;&lt;guided-facet-value&nbsp;/&gt;&lt;/guided-facet-link&gt;&nbsp;(&lt;guided-facet-count&nbsp;/&gt;) 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-value-ghost&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-value-selected&gt; 
      &lt;/guided-facet-values&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>15 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version 1/31/13--> <span class="codeph"> &lt;guided-facet-undo-link gsname=" <span class="varname"> facetname </span>"&gt;&lt;/guided-facet-undo-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Visualizza un collegamento di annullamento per un dato facet. Se sono presenti facet di selezione multipla, questo collegamento deseleziona tutti i valori del facet specificato. Dai un nome alla faccia. Se il facet non è attualmente selezionato, il collegamento è il percorso corrente. </p> <p>Di seguito è riportato un esempio di utilizzo di questo tag: </p> <p> <code class="syntax html"> &lt;guided-if-facet-selected&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-undo-link&nbsp;gsname="category"&gt;Undo&nbsp;Category&lt;/guided-facet-undo-link&gt; 
      &lt;/guided-if-facet-selected&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>16 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if-facet-long [gsname="facetname"]&gt; 
      &lt;guided-else-facet-long&gt;&lt;/guided-if-facet-long&gt; </code> </p> </td> 
   <td colname="col2"> <p>Questo tag condizionale è true quando il numero di valori di facet supera la soglia di lunghezza definita nella configurazione. Utilizzalo per visualizzare un facet come elemento dell’interfaccia utente diverso (ad esempio un elenco troncato o una casella di scorrimento) quando l’elenco è troppo lungo. </p> <p> <code class="syntax html"> &lt;guided-facet&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-long&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;div&nbsp;class="long_facet"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-link&gt;&lt;guided-facet-value/&gt;&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/div&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-long&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;div&nbsp;class="facet"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-link&gt;&lt;guided-facet-value/&gt;&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/div&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-long&gt; 
      &nbsp;&lt;/guided-facet&gt; </code> </p> <p>Puoi anche utilizzare questa condizione al di fuori del contesto di un blocco di facet guidato </span> denominato facendo riferimento a un facet specifico direttamente tramite l'utilizzo dell'attributo <span class="codeph"> <span class="varname"> gsname </span> </span> .<span class="codeph"> </span></p> <p> <code class="syntax html"> &lt;guided-if-facet-long&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The&nbsp;category&nbsp;facet&nbsp;is&nbsp;very&nbsp;long! 
      &lt;/guided-if-facet-long&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>17 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if-facet-selected [gsname="facetname"]&gt; 
      &lt;guided-else-facet-selected&gt;&lt;/guided-if-facet-selected&gt; </code> </p> </td> 
   <td colname="col2"> <p>Questo tag condizionale è true quando si fa clic almeno una volta sul facet e si seleziona attualmente un valore di facet. Può essere utilizzato per mostrare o nascondere i tag HTML o gs a seconda che venga fatto clic su un facet. </p> <p> <code class="syntax html"> &lt;guided-facet&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;This&nbsp;facet&nbsp;has&nbsp;been&nbsp;selected.&nbsp;&nbsp;You&nbsp;can&nbsp;no&nbsp;longer&nbsp;refine&nbsp;it. 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-link&gt;&lt;guided-facet-value/&gt;&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-selected&gt; 
      &lt;/guided-facet&gt; </code> </p> <p>Puoi anche utilizzare questa condizione al di fuori del contesto di un blocco <span class="codeph"> di facet guidato </span> facendo riferimento a un facet specifico direttamente tramite l'utilizzo dell'attributo <span class="codeph"> gsname </span> . </p> <p> <code class="syntax html"> &lt;guided-if-facet-selected&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The&nbsp;category&nbsp;facet&nbsp;is&nbsp;selected! 
      &lt;/guided-if-facet-selected&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>18 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if-facet-single [gsname="facetname"]&gt; 
      &lt;guided-else-facet-single&gt;&lt;/guided-if-facet-single&gt; </code> </p> </td> 
   <td colname="col2"> <p>Questo tag condizionale è true quando esiste un solo valore di facet. Può essere utilizzato per modificare la visualizzazione del facet quando non è in grado di perfezionare i risultati. </p> <p> <code class="syntax html"> &lt;guided-facet&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-single&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Facet&nbsp;is&nbsp;not&nbsp;refinable. 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-single&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-link&gt;&lt;guided-facet-value/&gt;&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-single&gt; 
      &lt;/guided-facet&gt; </code> </p> <p>Puoi anche utilizzare questa condizione al di fuori del contesto di un blocco di facet guidato </span> denominato facendo riferimento a un facet specifico direttamente tramite l'utilizzo dell'attributo <span class="codeph"> <span class="varname"> gsname </span> </span> .<span class="codeph"> </span></p> <p> <code class="syntax html"> &lt;guided-if-facet-single&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;There&nbsp;is&nbsp;only&nbsp;one&nbsp;value&nbsp;in&nbsp;the&nbsp;category&nbsp;facet! 
      &lt;/guided-if-facet-single&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>19 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if-facet-has-values [gsname="facetname"]&gt; 
      &lt;guided-else-facet-has-values&gt;&lt;/guided-if-facet-has-values&gt; </code> </p> </td> 
   <td colname="col2"> <p>Questa condizione ti consente di verificare se il facet specificato ha alcun valore. Puoi usarlo per mostrare un altro facet invece di uno vuoto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>20 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-total-count gsname=" <span class="varname"> facetname </span>" /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Trasmette il numero totale di risultati che si trovano all’interno del facet specificato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>21 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-value gsname=" <span class="varname"> associated custom facet value </span>"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Invia la stringa di un valore associato al facet. Puoi avere 0 o più campi associati a un facet. Avere campi associati è raro e per supportare tale operazione è possibile configurare il modello di trasporto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>22 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-facet-value gsname=" <span class="varname"> associated custom facet value </span>" /&gt;&lt;guided-else-facet-value&gt;&lt;/guided-if-facet-value&gt; </span> </p> </td> 
   <td colname="col2"> <p>Verifica se al valore facet è associato un valore di campo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>23 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-link&gt; value  </span>"]+&gt;&lt;/guided-facet-link&gt; </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>Crea un collegamento intorno alla stringa del valore del facet su cui il cliente può fare clic. Il percorso viene generato automaticamente per limitare i risultati in base al valore del facet corrente. Supporta il passaggio di qualsiasi attributo direttamente al tag di ancoraggio. </p> <p> <code class="syntax html"> &lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-link&nbsp;class="facetlink"&gt;&lt;guided-facet-value/&gt;&lt;/guided-facet-link&gt; 
      &lt;/guided-facet-values&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>24 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-value-path&gt; </span> </p> </td> 
   <td colname="col2"> <p>Crea un collegamento personalizzato a un valore di facet. </p> <p> <code class="syntax html"> &lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-lt/&gt;a&nbsp;href="&lt;guided-facet-value-path/&gt;"&lt;guided-gt/&gt;&lt;guided-facet-value/&gt;&lt;/a&gt; 
      &lt;/guided-facet-values&gt; </code> </p> <p>Per impostazione predefinita, il valore è un escape URL. È tuttavia possibile aggiungere un altro livello di codifica specificando quale modalità di escape si desidera utilizzare tramite il parametro escape. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>25 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-value-children&gt;&lt;/guided-facet-value-children&gt; </span> </p> </td> 
   <td colname="col2"> <p>Poiché <span class="codeph"> &lt;valori-facet-guidati&gt; </span> esegue l’iterazione attraverso ogni valore di facet, questo tag esegue l’iterazione di tutti i valori figlio di un facet nidificato. All’interno di questo tag, utilizza i tipici tag facet per creare collegamenti, creare collegamenti di annullamento e visualizzare i valori dei facet. Questo tag deve trovarsi all’interno di <span class="codeph"> &lt;Valore facet-guidato&gt; </span> perché esegue il looping nidificato. </p> <p>Un esempio di utilizzo di questo tag è il seguente: </p> <p> <code class="syntax html"> &lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&lt;guided-facet-link&nbsp;title='&lt;guided-facet-value&nbsp;/&gt;'&gt;&lt;guided-facet-value&nbsp;/&gt;&nbsp;(&lt;guided-facet-count&nbsp;/&gt;)&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&lt;guided-if-facet-value-has-children&gt; 
      &nbsp;&nbsp;&nbsp;&lt;guided-facet-value-children&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-link&nbsp;title='&lt;guided-facet-value&nbsp;/&gt;'&gt;&lt;guided-facet-value&nbsp;/&gt;&nbsp;(&lt;guided-facet-count&nbsp;/&gt;)&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&lt;/guided-facet-value-children&gt; 
      &nbsp;&nbsp;&lt;/guided-if-facet-value-has-children&gt; 
      &lt;/guided-facet-values&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>26 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if-facet-value-has-children&gt; 
      &lt;guided-else-facet- 
      value-has-children&gt; 
      &lt;/guided-if-facet-value-has-children&gt; </code> </p> </td> 
   <td colname="col2"> <p>Verifica se il valore del facet corrente ha valori secondari. Consigliato da utilizzare prima di utilizzare i tag <span class="codeph"> &lt;guide-facet-value-children&gt; </span> . La clausola "else" è facoltativa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>27 </p> </td> 
   <td colname="col1"> <p> 

    &amp;lt;guidato-else[-not]-facet-value-above-length-soglia&amp;gt;
    
    &amp;lt;/guidato-if[-not]-facet-value-over-length-soglia&amp;gt;   &lt;/p>  &lt;/td>
<td colname="col2"> <p>Determina se il valore del facet corrente all'interno del ciclo facet-values è al di sopra della soglia di lunghezza. In genere viene utilizzato per visualizzare solo i valori al di sotto della soglia su un lato lungo (a meno che l’utente non abbia selezionato in precedenza un collegamento "Ulteriori informazioni" visualizzato sotto il facet). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>28 </p> </td> 
   <td colname="col1"> <p> 

    &amp;lt;guidato-else[-not]-facet-value-equals-length-soglia&amp;gt;
    
    &amp;lt;/guidato-if[-not]-facet-value-equals-length-soglia&amp;gt;   &lt;/p>  &lt;/td>
<td colname="col2"> <p>Determina se il valore del facet corrente all'interno del ciclo facet-values, è uguale alla soglia di lunghezza. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>29 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-value-undo-link&gt;&lt;/guided-facet-value-undo-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Visualizza un collegamento di annullamento per un dato valore di facet selezionato. Utilizzalo per visualizzare un collegamento di annullamento accanto a un valore di facet selezionato. Poiché questo collegamento di annullamento annulla solo il valore selezionato, è diverso da <span class="codeph">  &lt;guide-facet-undo-link&gt; </span> che deseleziona tutti i valori selezionati. </p> <p> <p>Nota:  Se il facet non ha un comportamento di selezione multipla, i due collegamenti di annullamento hanno lo stesso comportamento. In altre parole, il facet può avere un solo valore selezionato. </p> </p> <p>Se il facet non è attualmente selezionato, il collegamento è il percorso corrente. Utilizza questo tag solo all'interno di un ciclo <span class="codeph"> guidati-facet-values </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>30 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-value-undo-path /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Crea un collegamento per annullare il valore del facet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>31 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-undo-path gsname=" <span class="varname"> facetname </span>" /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Crea un collegamento di annullamento facet personalizzato. </p> <p> Simile al tag <span class="codeph"> &lt;guide-facet-undo-link&gt; </span> , ma fornisce il percorso non elaborato per creare il collegamento di annullamento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>32 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if-facet-value-matches facetname="facetname" value="value"&gt;&lt;guided-else-facet-value-matches&gt; 
      &lt;/guided-if-facet-value-matches&gt; </code> </p> </td> 
   <td colname="col2"> <p>Visualizza l’HTML in modo condizionale quando il facet specificato ha il valore selezionato o singolo "value". Questo set di tag viene spesso utilizzato per visualizzare un facet in base al valore selezionato in un altro facet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>33 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-behavior gsname=" <span class="varname"> facetname </span>" /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Determina il comportamento di un facet, ad esempio normale, fisso o a selezione multipla. È utile per i clienti che ricevono i risultati XML e desiderano modificare dinamicamente il modo in cui il facet viene visualizzato in base al suo comportamento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>34 </p> </td> 
   <td colname="col1"> <p> 

    &amp;lt;/guidato-if-facet[-not]-visible&amp;gt;   &lt;/p>  &lt;/td>
<td colname="col2"> <p>Il contenuto racchiuso da questo tag viene nascosto o rivelato in base allo stato di visibilità del facet. Se una regola business nasconde o rivela direttamente il facet, qualsiasi contenuto all’interno del facet viene nascosto o rivelato. Non è necessario che questi tag avvolgano il facet. </p> <p> Questo tag viene utilizzato in genere per nascondere il nome visualizzato quando il nome è all’esterno del facet. Racchiudendo questo tag intorno al nome visualizzato, il nome scompare quando il facet è nascosto. </p> <p>Questo tag sostituisce la zona e presenta molti degli stessi vantaggi in termini di prestazioni dell’utilizzo delle aree. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Breadcrumb {#section_9B39B71FA6EC49FA8D88AD8A3BA987F7}

Consultare [Informazioni sulle breadcrumb](../c-about-design-menu/c-about-breadcrumbs.md#concept_FB8A943C594A4A1593B118141DA61F03).

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Tag </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-breadcrumb&gt; breadcrumbname  </span>"]&gt;&lt;/guided-breadcrumb&gt; </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>Tag del ciclo per la breadcrumb. Qualsiasi contenuto compreso tra i tag di apertura e chiusura viene ripetuto per ogni numero di query dello stato corrente. </p> <p>Se <span class="codeph"> <span class="varname"> gsname </span> </span> viene omesso, viene utilizzata la breadcrumb denominata "default". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-breadcrumb-link&gt;&lt;/guided-breadcrumb-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Crea un collegamento nel breadcrumb. Il comportamento predefinito è il comportamento "goto". Se il collegamento si comporta in modo diverso, utilizza l’attributo opzionale <span class="codeph"> <span class="varname"> gsname </span> </span> per specificare "remove" o "drop". Qualsiasi attributo incluso nel tag viene trasmesso al tag di ancoraggio risultante. </p> <p> <code class="syntax html"> &lt;guided-breadcrumb&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-link&nbsp;gsname="remove"&nbsp;class="bc_link"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-value/&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-breadcrumb-link&gt; 
      &lt;/guided-breadcrumb&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-breadcrumb-value /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Il tag valore stampa il valore trasformato dell’iterazione di breadcrumb corrente. Viene utilizzato solo nel contesto di un blocco <span class="codeph"> breadcrumb guidato </span>. </p> <p> <code class="syntax html"> &lt;guided-breadcrumb&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-value/&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-breadcrumb-link&gt; 
      &lt;/guided-breadcrumb&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-breadcrumb-label /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Il tag dell’etichetta restituisce un’etichetta per un valore di breadcrumb che specifica il facet selezionato per generare l’elemento di breadcrumb. Viene utilizzato solo nel contesto di un blocco <span class="codeph"> guide-breadcrumb </span>. </p> <p> <code class="syntax html"> &lt;guided-breadcrumb&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-label/&gt;:&nbsp;&lt;guided-breadcrumb-value/&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-breadcrumb-link&gt; 
      &lt;/guided-breadcrumb&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to search-eng version, 2/1/2013--> <code> &lt;guided-if-breadcrumb-label&gt; 
      &lt;guided-else- 
      breadcrumb-label&gt; 
      &lt;guided-if-breadcrumb-label /&gt; </code> </p> </td> 
   <td colname="col2"> <p>Questo tag condizionale viene utilizzato per visualizzare il contenuto in modo condizionale se il valore di breadcrumb corrente ha un’etichetta. Viene utilizzato per visualizzare solo le etichette e i contenuti correlati quando esiste effettivamente un’etichetta. Viene utilizzato solo nel contesto di un blocco <span class="codeph"> guide-breadcrumb </span>. </p> <p> <code class="syntax html"> &lt;guided-breadcrumb&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-breadcrumb-label&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-label/&gt;: 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-breadcrumb-label&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-value/&gt;&lt;/guided-breadcrumb-link&gt; 
      &lt;/guided-breadcrumb&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-breadcrumb-path&gt; </span> </p> </td> 
   <td colname="col2"> <p>Utilizzato per creare un collegamento di breadcrumb personalizzato. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Menu {#section_1D489ADF041F4351A66E5D5742125CA8}

Consultare [Informazioni sui menu](../c-about-design-menu/c-about-menus.md#concept_68123CE5CF4447B59217B5D721424E32).

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Tag </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-menu gsname="menuname"&gt;&lt;/guided-menu&gt; </span> </p> </td> 
   <td colname="col2"> <p>Questo è il tag iteratore del ciclo di valori del menu. Utilizza l'attributo <span class="codeph"> gsname </span> per identificare quale set di voci di menu viene visualizzato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-menu-item-link&gt;&lt;/guided-menu-item-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Fornisce l’URL per perfezionare la ricerca corrente per la voce di menu. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-menu-item-option&gt; </span> </p> </td> 
   <td colname="col2"> <p>In genere, un menu viene visualizzato in un controllo di selezione su un modello. Questo tag semplifica la costruzione del controllo di selezione perché genera l’HTML per generare l’opzione per il controllo selezionato. </p> <p>Ad esempio, il seguente blocco di codice: </p> <p> <code class="syntax html"> &lt;select&nbsp;name="sort"&nbsp;onchange="gcGo(this);"&gt; 
      &lt;guided-menu&nbsp;gsname="sort"&gt; 
      &lt;guided-menu-item-option/&gt; 
      &lt;/guided-menu&gt; 
      &lt;/select&gt; </code> </p> <p>Può generare HTML come segue: </p> <p> <code class="syntax html"> &lt;select&nbsp;name="sort"&nbsp;onchange="gcGo(this);"&gt; 
      &nbsp;&nbsp;&lt;option&nbsp;value="?sort=relevance;sp_sfvl_field=product-type|category|size;"&nbsp;selected="selected"&gt;Sort&nbsp;by&nbsp;Relevance&lt;/option&gt; 
      &nbsp;&nbsp;&lt;option&nbsp;value="?sort=avail-code;sp_sfvl_field=product-type|category|size;"&gt;Sort&nbsp;by&nbsp;Availability&lt;/option&gt; 
      &nbsp;&nbsp;&lt;option&nbsp;value="?sort=price;sp_sfvl_field=product-type|category|size;"&gt;Sort&nbsp;by&nbsp;Price&lt;/option&gt; 
      &lt;/select&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-menu-item-value /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Restituisce la stringa del valore associato al menu. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-menu-item-label /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Restituisce la stringa dell'etichetta associata al menu. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-menu-item-path /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Restituisce la stringa del percorso. Utilizza il tag se desideri aggiungere un parametro al percorso e creare un collegamento personalizzato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if-menu-item-selected&gt; 
      &lt;guided-else-menu- 
      item-selected&gt; 
      &lt;/guided-if-menu-item-selected&gt; </code> </p> </td> 
   <td colname="col2"> <p>Restituisce un valore 1 o 0 che indica se la voce di menu corrente è selezionata. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Pagenav {#section_2EE397635C514BBC8D668278EA314F35}

I tag di navigazione della pagina possono essere utilizzati per creare un set di collegamenti che consentono all’utente di passare alla pagina attraverso i risultati della ricerca.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Tag </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-pages&gt;&lt;/guided-pages&gt; </span> </p> </td> 
   <td colname="col2"> <p>Il tag loop per la navigazione della pagina. Qualsiasi contenuto tra i tag di apertura e chiusura viene ripetuto per ogni pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-page-link&gt;&lt;/guided-page-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Crea un collegamento nella navigazione della pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-page-link gsname="first|prev|next|last|viewall|viewpages"&gt;&lt;/guided-page-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Crea un collegamento alla prima, alla pagina precedente, alla pagina successiva o all’ultima pagina. Può anche creare un collegamento per visualizzare tutte le pagine su una sola pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-page-number /&gt; </span> </p> </td> 
   <td colname="col2"> <p> Restituisce una stringa con il numero di pagina corrente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if-page-selected&gt; 
      &lt;guided-else-page- 
      selected&gt; 
      &lt;/guided-if-page-selected&gt; </code> </p> </td> 
   <td colname="col2"> <p>Questo set di tag condizionali è true se è selezionata la pagina attualmente iterata. Generalmente viene utilizzato per visualizzare in modo diverso il numero di pagina nel controllo di navigazione della pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-page-prev&gt; 
      &lt;guided-else-page- 
      prev&gt; 
      &lt;/guided-if[-not]-page-prev&gt; </code> </p> </td> 
   <td colname="col2"> <p> Questo set di tag condizionali è true se la pagina corrente ha una pagina precedente. Generalmente viene utilizzato per visualizzare un collegamento precedente nella navigazione delle pagine, quando ha senso. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-page-next&gt; 
      &lt;guided-else-page- 
      next&gt; 
      &lt;/guided-if[-not]-page-next&gt; </code> </p> </td> 
   <td colname="col2"> <p> Questo set di tag condizionali è true se la pagina corrente ha una pagina successiva. Generalmente viene utilizzato per visualizzare un collegamento precedente nella navigazione delle pagine, quando ha senso. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-page-viewall&gt; 
      &lt;guided-else-page- 
      viewall&gt; 
      &lt;/guided-if[-not]-page-viewall&gt; </code> </p> </td> 
   <td colname="col2"> <p> Quando una ricerca restituisce un set di risultati di grandi dimensioni, è possibile che non si desideri offrire la possibilità di visualizzare tutti i risultati. Pertanto, puoi utilizzare questo set di tag condizionali per determinare quando visualizzare il collegamento Visualizza tutto . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-page-viewpages&gt; 
      &lt;guided-else-page- 
      viewpages&gt; 
      &lt;/guided-if[-not]-page-viewpages&gt; </code> </p> </td> 
   <td colname="col2"> <p>Puoi utilizzare questo set di tag condizionali per determinare quando visualizzare il collegamento Visualizza pagine. In genere viene utilizzato per consentire al cliente di visualizzare determinate pagine. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> 

    &amp;lt;guidato-else-page-link&amp;gt;
    &amp;lt;/guidato-if[-not]-page-link&amp;gt;   &lt;/p>  &lt;/td>
<td colname="col2"> <p>Verifica se la navigazione della pagina include una prima pagina, una pagina precedente, una pagina successiva e così via. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>11 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-page-total /&gt; </span> </p> </td> 
   <td colname="col2"> <p> Restituisce una stringa con il numero totale di pagine dei risultati di ricerca. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>12 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-pagination gsname= 
      "pagination_name"&gt;&lt;/guided-pagination&gt; </code> </p> </td> 
   <td colname="col2"> <p>Utilizza il tag <span class="codeph"> impaginazione guidata </span> per definire un’area in cui tutti i tag di impaginazione si riferiscono a un’impostazione di impaginazione specifica nel caso in cui siano definite poche impostazioni di navigazione della pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>13 </p> </td> 
   <td colname="col1"> <p> 

    next|last|viewall|viewpages]/&amp;gt;   &lt;/p>  &lt;/td>
<td colname="col2"> <p>Crea un collegamento personalizzato nella navigazione della pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>14 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if-page-high-eq-last&gt; 
      &lt;guided-else-page- 
      high-eq-last&gt; 
      &lt;/guided-if-page-high-eq-last&gt; </code> </p> </td> 
   <td colname="col2"> <p>Verifica se la pagina più alta nella navigazione delle pagine è uguale al numero totale di pagine. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>15 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if-page-low-eq-first&gt; 
      &lt;guided-else-page-low-eq-first&gt; &lt;/guided-if-page-low-eq-first&gt; </code> </p> </td> 
   <td colname="col2"> <p>Verifica se la pagina più bassa nella navigazione delle pagine è uguale a quella. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>16 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-page-is-multipage&gt; &lt;guided-else-page-is-multipage&gt; &lt;/guided-if-page-is-multipage&gt; </span> </p> </td> 
   <td colname="col2"> <p>Verifica se è presente una singola pagina di risultati o più pagine di risultati. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Ricerche recenti {#section_8CD907521F584257B475595B01A5964B}

Puoi utilizzare i tag di ricerca recenti per creare un set di collegamenti che consentono a un utente di eseguire rapidamente una ricerca precedente, come nell’esempio seguente:

```
<guided-if-recent-searches> 
    <span>Recent Searches</span><br/> 
    <guided-recent-searches> 
        <guided-recent-searches-link><guided-recent-searches-value></guided-recent-searches-link><br/> 
    </guided-recent-searches> 
    <guided-recent-searches-clear-link>Clear Recent Searches</guided-recent-searches-clear-link> 
</guided-if-recent-searches>
```

Consulta [Configurazione delle ricerche recenti](../c-about-design-menu/t-configuring-recent-searches.md#task_E9E8ACA04C90484F8AFD5262167B2562).

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Tag </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-recent-searches&gt;&lt;/guided-recent-searches&gt; </span> </p> </td> 
   <td colname="col2"> <p>Tag del ciclo per ricerche recenti. Qualsiasi contenuto tra i tag di apertura e chiusura viene ripetuto per ogni pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-recent-searches-link [attr="value"]+&gt; 
      &lt;/guided-recent-searches-link&gt; </code> </p> </td> 
   <td colname="col2"> <p>Consente di creare un collegamento a una ricerca recente. Supporta il passaggio di eventuali attributi HTML direttamente al tag di ancoraggio. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-recent-searches-path /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Consente di acquisire il percorso URL relativo per una ricerca recente, all’interno di un ciclo <span class="codeph"> guidato-recenti-ricerche </span>. In genere si utilizza il collegamento di ricerca guidato <span class="codeph"> </span>. Tuttavia, se desideri creare un collegamento personalizzato, puoi utilizzare questo tag . Ecco un esempio: </p> <p> <code class="syntax html"> &lt;guided-lt/&gt;a&amp;nbsp;href="&lt;guided_recent_searches_path&gt;"&gt;&lt;guided-recent-searches-value&gt;&lt;/a&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-recent-searches-value&gt; </span> </p> </td> 
   <td colname="col2"> <p>Consente di acquisire il termine di query associato a una ricerca recente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-recent-searches-clear-link&gt;&lt;/guided-recent-searches-clear-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Consente ai clienti di cancellare le ricerche salvate di recente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-recent-searches-clear-path /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Restituisce il percorso utilizzato da <span class="codeph"> &lt;guidato-Recent-Search-clear-link&gt; </span> in modo da poter creare un collegamento personalizzato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> 

    &amp;lt;/guidato-se-recenti ricerche&amp;gt;   &lt;/p>  &lt;/td>
<td colname="col2"> <p>Consente di visualizzare le ricerche recenti quando un cliente ha eseguito una ricerca recente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Intendi {#section_C1EB3B9D8E1242798A6E04609D1E3543}

È possibile utilizzare i tag Did You Mean per creare un set di collegamenti ai suggerimenti quando una ricerca non restituisce risultati e il termine Search non è presente nel dizionario dell&#39;account. Di seguito è riportato un esempio di utilizzo dei tag Did You Mean :

```
<guided-if-suggestions> 
    <span>Did You Mean?</span><br/> 
    <guided-suggestions> 
        <guided-suggestion-link><guided-suggestion/></guided-suggestion-link><br/> 
    </guided-suggestions> 
</guided-if-suggestions>
```

Consultare [Informazioni su intendete](../c-about-linguistics-menu/c-about-did-you-mean.md#concept_7D4F3C29EF184B538B8AE2ECAE0CDC5E).

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Tag </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matches search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-suggestions&gt;&lt;/guided-suggestions&gt; </span> </p> </td> 
   <td colname="col2"> <p>Questo è il tag del ciclo per sovrapporre i suggerimenti. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matches search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-suggestion-link&gt;&lt;/guided-suggestion-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Crea un collegamento al suggerimento specificato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--Newly added from search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-suggestion-value /&gt; </span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-suggestions&gt;&lt;guided-else[-not]- 
      suggestions&gt;&lt;/guided-if[-not]-suggestions&gt; </code> </p> </td> 
   <td colname="col2"> <p>Consente di verificare se sono presenti suggerimenti. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-suggestion-path /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Restituisce la stringa del percorso al suggerimento. Puoi usarlo per creare un tag di ancoraggio personalizzato. In genere, si utilizza invece <span class="codeph"> guidato-suggestione-link </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-suggestion /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Un suggerimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-suggestion-result-count /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Conteggio dei risultati per il suggerimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-suggestion-autosearch&gt; 
      &lt;guided-else[-not]-suggestion-autosearch&gt; 
      &lt;/guided-if[-not]-suggestion-autosearch&gt; </code> </p> </td> 
   <td colname="col2"> <p>Consente di verificare se è stata eseguita la ricerca automatica per suggerimento su zero risultati, nel caso in cui questa funzione sia attiva. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-suggestion-original-query /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Restituisce la query originale se è stata eseguita una ricerca automatica. </p> <p>Esempio di utilizzo: </p> <p> <code class="syntax html"> &lt;guided-if-suggestion-autosearch&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;Search&nbsp;for&nbsp;&lt;guided-query-param&nbsp;gsname="q"&nbsp;/&gt;&nbsp;instead&nbsp;of&nbsp;&lt;guided-suggestion-original-query&nbsp;/&gt; 
      &lt;/guided-if-suggestion-autosearch&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-suggestion-low-results&gt; 
      &lt;guided-else[-not]-suggestion-low-results&gt; 
      &lt;/guided-if[-not]-suggestion-low-results&gt; </code> </p> </td> 
   <td colname="col2"> <p>Questa condizione è vera se ci sono suggerimenti a causa di un conteggio basso dei risultati, nel caso in cui questa funzione sia attivata. </p> <p>Di seguito è riportato un esempio di utilizzo di questo tag: </p> <p> <code class="syntax html"> &lt;guided-if-suggestion-low-results&gt; 
      &nbsp;&nbsp;&nbsp;You&nbsp;have&nbsp;a&nbsp;low&nbsp;result&nbsp;count&nbsp;for&nbsp;&lt;guided-query-param&nbsp;gsname="q"&nbsp;/&gt;. 
      &nbsp;&nbsp;&nbsp;Did&nbsp;you&nbsp;mean:&nbsp;&lt;guided-suggestions&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-suggestion-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-suggestion&nbsp;/&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-suggestion-link&gt;&lt;guided-if-not-last&gt;,&nbsp;&lt;/guided-if-not-last&gt; 
      &nbsp;&nbsp;&nbsp;&lt;/guided-suggestions&gt; 
      &lt;/guided-if-suggestion-low-results&gt; </code> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Autocompletamento {#section_897316BEE1454E839A56B565CA4AF018}

I seguenti tag possono essere utilizzati per aggiungere il completamento automatico al modulo di ricerca. I tag head-content e form-content sono necessari per rendere correttamente la funzione di completamento automatico. Si consiglia di utilizzare i tag anziché codificare in modo rigido i codici JavaScript e CSS automatici nel modello di presentazione. Il motivo è che i tag consentono ai modelli di raccogliere qualsiasi nuovo ID cache di eliminazione ogni volta che si modificano le impostazioni di completamento automatico senza la necessità di aggiornare manualmente il modello.

Consultare [Informazioni sul completamento automatico](../c-about-auto-complete.md#concept_093A9CD754864BA79B456FE4BEB64578).

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Tag </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-autocomplete&gt; &lt;guided-else-autocomplete&gt; &lt;/guided-if-autocomplete&gt; </span> </p> </td> 
   <td colname="col2"> <p>Rileva se la funzione di completamento automatico è abilitata. È possibile utilizzare i tag per raccogliere facoltativamente il contenuto principale e il contenuto del modulo necessari per il completamento automatico. A sua volta, questo consente di attivare e disattivare la funzione e non deve modificare i modelli di presentazione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-ac-css /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Utilizzato nella parte superiore del modello di presentazione e sostituito dallo script CSS appropriato include per il completamento automatico. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-ac-form-content /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Utilizzato nel modulo di ricerca (tra i tag <span class="codeph"> &lt;form&gt; </span> e <span class="codeph"> &lt;/form&gt; </span>) del modello di presentazione, anziché codificare i tag di completamento automatico all’interno del modulo. I tag vengono sostituiti con l’HTML appropriato necessario per il funzionamento automatico. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-ac-javascript /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Genera i collegamenti al JavaScript di completamento automatico. Per ottenere le migliori prestazioni, è consigliabile posizionare questo tag vicino alla parte inferiore della pagina prima del tag "body" di chiusura. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Store {#section_A33E25DB5E67404A823BD9618665B773}

Utilizza i seguenti tag per testare e visualizzare l&#39;archivio in cui si trova attualmente un utente.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Tag </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-store /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Visualizza lo store corrente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-store-defined&gt; &lt;guided-else-store-defined&gt; &lt;/guided-if-store-defined&gt; </span> </p> </td> 
   <td colname="col2"> <p>Rileva se l'utente si trova in un negozio. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-store gsname="store"&gt; &lt;guided-else-store&gt; &lt;/guided-if-store&gt; </span> </p> </td> 
   <td colname="col2"> <p>Rileva se l'utente è nell'archivio specificato dal parametro <span class="codeph"> gsname </span> . </p> </td> 
  </tr> 
 </tbody> 
</table>

## Zone {#section_B9B3179E000C42D492E1541F2FE44CB5}

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Tag </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-zone gsname="zone area"&gt; </span> </p> </td> 
   <td colname="col2"> <p>È possibile racchiudere qualsiasi contenuto nei tag di zona per creare una zona all’esterno di tale area. Questo consente di utilizzare le regole business per visualizzare la zona in base alle esigenze. Per impostazione predefinita, le aree vengono sempre visualizzate. Puoi utilizzare i parametri di ricerca e facet facoltativi per indicare quale ricerca o facet è associato alla zona. Questa funzionalità consente al software di saltare ricerche o facet quando una zona è nascosta, migliorando le prestazioni in fase di ricerca. Gli attributi relativi all'altezza e alla larghezza sono facoltativi e vengono utilizzati per configurare la modalità di visualizzazione del segnaposto nel Generatore di regole di visualizzazione quando viene rimossa una zona. </p> <p> Utilizza il tag <span class="codeph"> guidato-if-facet[-not]-visible </span> invece della zona, se possibile. Semplifica il modello di presentazione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-zone gsname="zone area"&gt; &lt;guided-else-zone&gt; &lt;/guided-if-zone&gt; </span> </p> </td> 
   <td colname="col2"> <p>Questo insieme di tag consente di verificare se è attualmente visualizzata una zona. È utile quando altrove nella pagina sono presenti contenuti che si desidera visualizzare solo quando la zona è visualizzata. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Indicatori di loop {#section_387322CA0AA843A2ACF2795C328673E9}

È possibile utilizzare ciascuno dei seguenti indicatori di loop in uno qualsiasi dei seguenti blocchi di loop:

* risultati guidati
* valori facet-guidati
* breadcrumb guidato
* voci di menu guidate
* pagine guidate

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Tag </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-first&gt;&lt;guided-else[-not]-first&gt; 
      &lt;/guided-if[-not]-first&gt; </code> </p> </td> 
   <td colname="col2"> <p>Questa condizione è vera quando l'iterazione corrente è la prima iterazione del ciclo. Questo non significa necessariamente il primo risultato o la prima pagina, ma il primo mostrato. Se il visitatore del sito si trova a pagina 2 di un set di risultati che è 10 per pagina, la prima iterazione è il risultato 11. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-last&gt;&lt;guided-else[-not]-last&gt; 
      &lt;/guided-if[-not]-last&gt; </code> </p> </td> 
   <td colname="col2"> <p>Questa condizione è vera quando l'iterazione corrente è l'ultima iterazione del ciclo. Questo non significa necessariamente l’ultimo risultato o l’ultima pagina, ma l’ultima mostrata nel contesto corrente (pagina). Se il visitatore del sito si trova a pagina 1 di un set di risultati che contiene 200 risultati ma ha solo 10 risultati per pagina, l’ultima iterazione è il risultato 10 invece del risultato 200. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-odd&gt;&lt;guided-else[-not]-odd&gt; 
      &lt;/guided-if[-not]-odd&gt; </code> </p> </td> 
   <td colname="col2"> <p>Questa condizione è vera quando l'iterazione corrente è un'iterazione dispari del ciclo (rispetto a un'iterazione pari). È utile per visualizzare diversi colori delle righe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-even&gt;&lt;guided-else[-not]-even&gt; 
      &lt;/guided-if[-not]-even&gt; </code> </p> </td> 
   <td colname="col2"> <p>Questa condizione è vera quando l'iterazione corrente è un'iterazione pari del ciclo (rispetto a un'iterazione dispari). È utile per visualizzare diversi colori delle righe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-alt&gt;&lt;guided-else[-not]-alt&gt; 
      &lt;/guided-if[-not]-alt&gt; </code> </p> </td> 
   <td colname="col2"> <p>Questa condizione è vera quando l'iterazione corrente è un'iterazione pari del ciclo. È utile per visualizzare diversi colori delle righe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-inner&gt;&lt;guided-else[-not]-inner&gt; 
      &lt;/guided-if[-not]-inner&gt; </code> </p> </td> 
   <td colname="col2"> <p>Include il testo tra di essi se l’iterazione corrente non è né la prima né l’ultima. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-outer&gt;&lt;guided-else[-not]-outer&gt; 
      &lt;/guided-if[-not]-outer&gt; </code> </p> </td> 
   <td colname="col2"> <p>Include il testo tra di essi se l’iterazione corrente è la prima o l’ultima. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-loop-index&gt; </span> </p> </td> 
   <td colname="col2"> <p>Un numero intero (a partire da 0) il cui valore viene incrementato per ogni iterazione del ciclo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-loop-counter&gt; </span> </p> </td> 
   <td colname="col2"> <p>Un numero intero (a partire da 1) il cui valore viene incrementato per ogni iterazione del ciclo. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Lingua vari {#section_BFE8DC98E26F4D7BB60FEC54D9A5DC6C}

Sono disponibili i seguenti tag per consentire di eseguire operazioni più avanzate con il modello, ad esempio per creare un proprio mini-facet.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Tag </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng, 2/1/2013--> <span class="codeph"> &lt;guided-current-path&gt; </span> </p> </td> 
   <td colname="col2"> <p>Fornisce il percorso corrente utilizzato. In genere viene utilizzato per creare un collegamento che viene aggiunto a un nuovo parametro alla ricerca esistente. Per impostazione predefinita, il percorso è con URL di escape. È possibile specificare quale modalità di escape si desidera utilizzare tramite il parametro escape . </p> <p>Esempio: </p> <p> <code class="syntax html"> &lt;a&nbsp;href="&lt;guided-current-path&nbsp;/&gt;&amp;lang=fr"&gt; 
      French&nbsp;Version </code> </p> <p>In questo esempio, una regola di elaborazione della ricerca utilizza lang per selezionare la versione francese. </p> <p>Il percorso corrente ha sempre almeno un parametro di query. Se non esistono altri parametri di query, viene impostato su <span class="codeph"> q=* </span> per facilitare l’aggiunta di altri parametri. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> Percorso di base  </span> </p> </td> 
   <td colname="col2"> <p> Se desideri creare un collegamento utilizzando il percorso base, utilizza <span class="codeph"> / </span> all'inizio del <span class="codeph"> href </span> e aggiungi i parametri. </p> <p> <code class="syntax html"> &lt;a&nbsp;href="/"&gt;All&nbsp;Products&lt;/a&gt; 
      Would&nbsp;create&nbsp;a&nbsp;link&nbsp;"All&nbsp;Products"&nbsp;to&nbsp;your 
      basepath,&nbsp;for&nbsp;example&nbsp;https://search.mycompany.com/ 
       </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng, 2/1/2013--> <span class="codeph"> &lt;guided-query-param gsname="query_parameter"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Consente di acquisire il valore esistente di un parametro di query sull’URL. Se il parametro non esiste, questo tag restituisce una stringa vuota. Se non si specifica un'opzione di escape, la stringa restituita è un escape HTML automatico, è possibile specificare l'escape HTML o URL. </p> <p>Esempio: </p> <p> 

    &amp;lt;query-guidata-param&amp;nbsp;gsname=&quot;q&quot;&amp;nbsp;/&amp;gt;
    dà&amp;nbsp;you&amp;nbsp;the&amp;nbsp;value&amp;nbsp;pantaloni
    
    &amp;lt;guidato-query-param&amp;nbsp;gsname=&quot;lang&quot;&amp;nbsp;/&amp;gt;
    assegna&amp;nbsp;te&amp;nbsp;the&amp;nbsp;value&amp;nbsp;en
    
    &amp;lt;guidato-query-param&amp;nbsp;gsname=&quot;test&quot;&amp;nbsp;/&amp;gt;
    given&amp;nbsp;you&amp;nbsp;an&amp;nbsp;empty&amp;nbsp;string
    &amp;nbsp;
    &amp;nbsp;&amp;nbsp; nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;   &lt;/p>  &lt;/td>
</tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-query-param-name gsname="param#" offset="offset_number" /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Ricerca guidata ha la nozione di numero di query, utilizzato nel controllo breadcrumb. <span class="codeph"> guidato-query-param-name  </span> consente di definire parametri come parte di un collegamento nel modello di presentazione in cui la funzione Ricerca guidata indica il numero di query corretto. Il <span class="codeph"> gsname </span> contiene una "x", che viene sostituita dalla funzione Ricerca guidata con il numero corretto. Il valore di offset può essere compreso tra 0 e 15, dove 0 indica che viene utilizzato il successivo numero di query disponibile. Un 1 indica che desideri aggiungergli 1 e così via. </p> <p>Combinato con <span class="codeph"> percorso-corrente-guidato </span>, puoi creare un collegamento mini facet personalizzato o consentire un livello di drill-down aggiuntivo. </p> <p>Esempio: </p> <p> <code class="syntax html"> &lt;a&nbsp;href="&lt;guided-current-path 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/&gt;&amp;&lt;guided-query-param-name&nbsp;gsname="q#"&nbsp;offset="0" 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/&gt;=mens&amp;&lt;guided-query-param-name&nbsp;gsname="x#"&nbsp;offset="0" 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/&gt;=category"&nbsp;&gt;Category:Men&lt;/a&gt;&nbsp; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </code> </p> <p> <code class="syntax html"> &lt;a&nbsp;href="&lt;guided-current-path 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/&gt;&amp;&lt;guided-query-param-name&nbsp;gsname="sp_q_exact_#"&nbsp;offset="0" 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/&gt;=mens&amp;&lt;guided-query-param-name&nbsp;gsname="sp_x_#"&nbsp;offset="0" 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/&gt;=category&amp;&lt;guided-query-param-name&nbsp;gsname="sp_q_exact_#"&nbsp;offset="1" 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/&gt;=Jeans&amp;&lt;guided-query-param-name&nbsp;gsname="sp_x_#"&nbsp;offset="1" 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/&gt;=product-type"&nbsp;&gt;Cat:Men&nbsp;-&nbsp;Product:Jeans&lt;/a&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-include gsfile="filename" /&gt; </span> </p> </td> 
   <td colname="col2"> <p> Consente di includere altri file modello. Questa funzionalità consente di creare più modelli utilizzando sotto-modelli come moduli. </p> <p>Nell’esempio seguente, i file <span class="filepath"> breadcrumb </span> e <span class="filepath"> facet </span> sono inclusi: </p> <p> <code class="syntax html"> &lt;guided-include&nbsp;gsfile='breadcrumbs.tmpl'&nbsp;/&gt; 
      &lt;guided-include&nbsp;gsfile='facets.tmpl'&nbsp;/&gt; </code> </p> <p>Le inclusioni dinamiche non sono supportate. In altre parole, <span class="codeph"> gsfile </span> non può essere una variabile. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW 1/17/2013--> <span class="codeph"> &lt;guided-search-time&gt; </span> </p> </td> 
   <td colname="col2"> <p> Identifica il tempo impiegato dalla ricerca. Il valore del tempo di ricerca restituito è specificato in ms. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW 1/17/2013--> <span class="codeph"> &lt;guided-fall-through-searches&gt; </span> </p> </td> 
   <td colname="col2"> <p> Restituisce il numero di ricerche core utilizzate per creare la pagina dei risultati di ricerca. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW 1/17/2013--> <span class="codeph"> &lt;guided-if-fall-through-search&gt;&lt;/guided-if-fall-through-search&gt; </span> </p> </td> 
   <td colname="col2"> <p>Verifica se il conteggio delle ricerche principali è maggiore di uno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-even&gt;&lt;guided-else[-not]-even&gt; 
      &lt;/guided-if[-not]-even&gt; </code> </p> </td> 
   <td colname="col2"> <p>Questa condizione è vera quando l'iterazione corrente è un'iterazione pari del ciclo (rispetto a un'iterazione dispari). È utile per visualizzare diversi colori delle righe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-alt&gt;&lt;guided-else[-not]-alt&gt; 
      &lt;/guided-if[-not]-alt&gt; </code> </p> </td> 
   <td colname="col2"> <p>Questa condizione è vera quando l'iterazione corrente è un'iterazione pari del ciclo. È utile per visualizzare diversi colori delle righe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>11 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-inner&gt;&lt;guided-else[-not]-inner&gt; 
      &lt;/guided-if[-not]-inner&gt; </code> </p> </td> 
   <td colname="col2"> <p>Include il testo tra di essi se l’iterazione corrente non è né la prima né l’ultima. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>12 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-outer&gt;&lt;guided-else[-not]-outer&gt; 
      &lt;/guided-if[-not]-outer&gt; </code> </p> </td> 
   <td colname="col2"> <p>Include il testo tra di essi se l’iterazione corrente è la prima o l’ultima. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>13 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if-first-search&gt;&lt;guided-else-first-search&gt; 
      &lt;/guided-if-first-search&gt; </code> </p> </td> 
   <td colname="col2"> <p>Consente di verificare se si è nella ricerca iniziale o meno (la query è il risultato di una ricerca dalla casella di ricerca). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>14 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-search-url /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Puoi utilizzare questo tag nel modello per salvarti dalla codifica fissa dell’azione del modulo di ricerca. Rileva quando ti trovi nell’ambiente Staged o Live e cambia di conseguenza. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>15 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-query-param-defined gsname="query_parameter"&gt; &lt;guided-else-query-param-defined&gt; &lt;/guided-if-query-param-defined&gt; </span> </p> </td> 
   <td colname="col2"> <p>Questo insieme di tag consente di verificare quali parametri CGI sono definiti nel percorso di ricerca. Puoi verificare i valori dei parametri solo se sono definiti. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>16 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-next-query-number&gt; </span> </p> </td> 
   <td colname="col2"> <p>Il motore di ricerca guidata che guida il modello ha la nozione di numeri di query mobili in cui ogni nuovo collegamento generato dal motore utilizza il successivo numero di query disponibile. Questo tag consente di acquisire il numero o gli offset della query successiva in modo da poter creare collegamenti personalizzati che consentono di eseguire il drill-through del set di risultati. Offset consente di effettuare l'offset nel numero di query successivo. Ad esempio, se hai selezionato un facet, il numero di query successivo è 2, con un offset pari a 1 il numero di query restituito è 3. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>17 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-custom-var gsname="custom_variable"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Consente di acquisire il valore esistente di una variabile personalizzata definita dalle regole di elaborazione. Se non si specifica un'opzione di escape, la stringa restituita è un escape HTML automatico, è possibile specificare <span class="codeph"> html </span>, <span class="codeph"> url </span>, <span class="codeph"> js </span> o <span class="codeph"> 0 </span>. Se utilizzi una regola di elaborazione per copiare un parametro CGI in entrata in una variabile personalizzata e quindi visualizzarlo o utilizzarlo nel modello con escape impostato su none o js, puoi creare una vulnerabilità XSS nella ricerca. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>18 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-custom-var-defined gsname="custom_variable"&gt; &lt;guided-else-custom-var-defined&gt; &lt;/guided-if-custom-var-defined&gt; </span> </p> </td> 
   <td colname="col2"> <p>Abilita il test se una variabile personalizzata è definita nelle regole di elaborazione (pulizia delle query, elaborazione pre-ricerca ed elaborazione post-ricerca). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>19 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-general-field gsname="searchname" field="fieldname"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Consente di visualizzare il contenuto di un campo generale definito nel modello di trasporto. Se non si specifica un'opzione escape, la stringa restituita viene codificata nel formato specificato nel modello di trasporto per quel campo. La specificazione di un’opzione di escape si applica al formato che stai codificando nel campo come nel modello di trasporto. È possibile specificare <span class="codeph"> html </span>, <span class="codeph"> url </span>, <span class="codeph"> js </span>, <span class="codeph"> json </span> o <span class="codeph"> 0 </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>20 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-general-field gsname="searchname" field="fieldname"&gt; &lt;guided-else-general-field&gt; &lt;/guided-if-general-field&gt; </span> </p> </td> 
   <td colname="col2"> <p>Abilita il test se esiste il contenuto di un campo generale, come definito nel modello di trasporto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>21 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-cookie-value gsname="cookie_name"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Consente di acquisire il valore di un cookie, supponendo che il cookie sia disponibile. Se non si specifica un'opzione di escape, la stringa restituita è un escape HTML automatico, è possibile specificare <span class="codeph"> html </span>, <span class="codeph"> url </span>, <span class="codeph"> js </span>, <span class="codeph"> json </span> o <span class="codeph"> 0 </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>22 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-cookie gsname="cookie_name"&gt; &lt;guided-else-cookie&gt; &lt;/guided-if-cookie&gt; </span> </p> </td> 
   <td colname="col2"> <p>Abilita il test se esiste un cookie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>23 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-banner gsname="banner area"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Invia il banner per una determinata area. Gli attributi facoltativi di larghezza e altezza vengono utilizzati nel Generatore di regole visive per consentire la visualizzazione di un segnaposto significativo che consenta agli utenti di selezionare un banner. Per impostazione predefinita, i banner non sono preceduti da escape. Si desidera invece inserire l'HTML nel modello di presentazione. Tuttavia, se stai creando un modello JSON, considera l’utilizzo dell’opzione di escape js. </p> <p>Esempio: </p> <p> <code class="syntax html"> &lt;guided-banner&nbsp;gsname="top"&nbsp;width="400px" 
      &nbsp;height="50px"/&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>24 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-banner-set gsname="banner area"&gt; &lt;guided-else-banner-set&gt; &lt;/guided-if-banner-set&gt; </span> </p> </td> 
   <td colname="col2"> <p>Abilita il test se è impostata un'area banner. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>25 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-simulator-mode&gt; &lt;guided-else-simulator-mode&gt; &lt;/guided-if-simulator-mode&gt; </span> </p> </td> 
   <td colname="col2"> <p>Consente di rilevare quando si visualizza la ricerca in Simulatore o nel Generatore di regole visive. Viene normalmente utilizzato per visualizzare ulteriori informazioni di debug. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>26 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-tnt-business-rules&gt; &lt;guided-else-tnt-business-rules&gt; &lt;/guided-if-tnt-business-rules&gt; </span> </p> </td> 
   <td colname="col2"> <p>Consente di rilevare se sono presenti regole di business che fanno riferimento a una campagna <span class="keyword"> Adobe Target </span>. Viene normalmente utilizzato come parte dell'integrazione con <span class="keyword"> Adobe Target </span> per impedire di colpire i server <span class="keyword"> Target </span> quando non è necessario. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>27 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-redirect /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Per impostazione predefinita, i reindirizzamenti vengono eseguiti automaticamente. Tuttavia, se hai configurato la ricerca/merchandising del sito per restituire una risposta XML o JSON all'applicazione web, puoi scegliere di analizzare la risposta 302/301 nell'applicazione web o far passare il reindirizzamento all'utente come parte del set di risultati. Se trasmetti il reindirizzamento come parte del set di risultati, puoi utilizzare questo tag nel modello per generare la posizione di reindirizzamento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>28 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-redirect&gt; &lt;guided-else-redirect&gt; &lt;/guided-if-redirect&gt; </span> </p> </td> 
   <td colname="col2"> <p>Dopo aver configurato la ricerca/merchandising del sito per restituire i reindirizzamenti nel set di risultati, questo set di tag può essere utilizzato per determinare se è presente un reindirizzamento all'output. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>29 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-lt /&gt; &lt;guided-gt /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Questo set di tag consente di incorporare tag modello guidato all’interno degli attributi HTML. </p> <p>Esempio: </p> <p> <code class="syntax html"> &lt;guided-lt/&gt;div&nbsp;&lt;guided-if-facet-long&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;style="height:&nbsp;125px;&nbsp;overflow: 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;auto;"&lt;/guided-if-facet-long&gt;&lt;guided-gt/&gt; </code> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Tag dei modelli di trasporto {#reference_227D199F5A7248049BE1D405C0584751}

I modelli di trasporto sono modelli XML che trasmettono i dati dalla ricerca back-end al livello di presentazione Guided Search.

<!-- 

r_transport_template_tags.xml

 -->

Nel livello di presentazione, è possibile avere un singolo modello di presentazione che presenti i risultati di più ricerche. Ogni ricerca può utilizzare lo stesso modello di trasporto o un modello di trasporto personalizzato per passare i dati al livello di presentazione.

Poiché il modello di trasporto viene utilizzato solo per trasmettere i dati al livello della presentazione, non dispone di alcun codice HTML che si occupa della visualizzazione dei risultati della ricerca. Il modello di trasporto utilizza i tag XML del modello di trasporto per trasmettere i risultati della ricerca per la compilazione dei componenti di ricerca guidata, ad esempio facet, breadcrumb e menu. All’interno di questi tag vengono utilizzati i tag modello di ricerca standard per visualizzare i valori effettivi.

Vedere [Modifica di una presentazione o di un modello di trasporto](../c-about-design-menu/c-about-templates.md#task_800E0E2265C34C028C92FEB5A1243EC3).

Consulta [Ricerca tag modello](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4).

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Tag del modello di trasporto </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-xml&gt;&lt;/guided-xml&gt; </span> </p> </td> 
   <td colname="col2"> <p>I tag XML principali utilizzati dal livello di presentazione per rilevare ciò che viene analizzato dal modello di trasporto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;general&gt;&lt;/general&gt; </span> </p> </td> 
   <td colname="col2"> <p>I tag racchiudono i tag dei modelli di ricerca che forniscono dati di riepilogo in base al set di risultati. In genere, questi tag contengono tag di ricerca per il numero totale di risultati, risultati inferiori e risultati più elevati. Puoi definire un numero qualsiasi di campi globali aggiuntivi desiderati con il tag <span class="codeph"> general-field </span> , come nell’esempio seguente: </p> <p> <code class="syntax html"> &lt;general&gt; 
      &nbsp;&nbsp;&lt;total&gt;&lt;search-total&nbsp;/&gt;&lt;/total&gt; 
      &nbsp;&nbsp;&lt;lower&gt;&lt;search-lower&nbsp;/&gt;&lt;/lower&gt; 
      &nbsp;&nbsp;&lt;upper&gt;&lt;search-upper&nbsp;/&gt;&lt;/upper&gt; 
      &nbsp;&nbsp;&lt;general-field&nbsp;name="my_custom_field"&gt;Some&nbsp;global&nbsp;content&lt;/general-field&gt; 
      &lt;/general&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;results&gt;&lt;/results&gt; </span> </p> </td> 
   <td colname="col2"> <p>I tag sono racchiusi tra i risultati della ricerca, in modo che la funzione Ricerca guidata sappia dove cercarli. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;result&gt;&lt;/result&gt; </span> </p> </td> 
   <td colname="col2"> <p>I tag sono racchiusi intorno a ciascun risultato di ricerca, in modo che la funzione Ricerca guidata riconosca dove inizia e termina il contenuto di un singolo risultato di ricerca, come nell’esempio seguente: </p> <code class="syntax html"> &lt;results&gt; 
     &nbsp;&nbsp;&lt;search-results&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;result&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;index&gt;&lt;search-index&nbsp;/&gt;&lt;/index&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;loc&gt;&lt;search-cdata&gt;&lt;search-url&nbsp;length="500"&nbsp;/&gt;&lt;/search-cdata&gt;&lt;/loc&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;/result&gt; 
     &nbsp;&nbsp;&lt;/search-results&gt; 
     &lt;/results&gt; </code> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;attribute-table name="tablename"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Consente di scorrere in sequenza ogni elemento di un elenco con più valori per un singolo risultato. Utilizza questo tag solo all’interno di un risultato. Lo scopo è quello di consentire l’iterazione degli attributi che appartengono a un campo risultato, come nell’esempio seguente: </p> <code class="syntax html"> &lt;results&gt; 
     &nbsp;&nbsp;&lt;search-results&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;result&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;index&gt;&lt;search-index&nbsp;/&gt;&lt;/index&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;loc&gt;&lt;search-url&nbsp;/&gt;&lt;/loc&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;title&gt;&lt;search-title&nbsp;/&gt;&lt;/title&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;attribute-table&nbsp;name="downloads"&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;field&nbsp;name="download_title"&gt;&lt;search-display-field&nbsp;name="download_title"&nbsp;/&gt;&lt;/field&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;field&nbsp;name="download_link"&nbsp;delimiter="|"&gt;&lt;search-display-field&nbsp;name="download_link"&nbsp;/&gt;&lt;/field&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/attribute-table&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;/result&gt; 
     &nbsp;&nbsp;&lt;/search-results&gt; 
     &lt;/results&gt; </code> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;facets&gt;&lt;/facets&gt; </span> </p> </td> 
   <td colname="col2"> <p>Passa i risultati che popolano i facet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 
     <!--NEW 2/27/2014--> <span class="codeph"> &lt;dynamic-facet&gt;&lt;/dynamic-facet&gt; </span> </p> </td> 
   <td colname="col2"> <p> È possibile designare un facet come sia un facet dinamico che come membro di una barra dei facet. Tuttavia, il loro trattamento è indipendente rispetto ai relativi tag modello di presentazione. </p> <p>In altre parole, non è consentita la nidificazione di un contesto di looping della barra dei facet all’interno di un contesto di looping dei facet dinamici o viceversa. </p> <p>Per i facet sia dinamici che con ringhiere, solo i facet dinamici restituiti per una determinata ricerca sono visibili nel contesto di looping della barra sfaccettatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;facet name="name"&gt;&lt;/facet&gt; </span> </p> </td> 
   <td colname="col2"> <p> Ogni facet ha i propri tag facet in cui il parametro name corrisponde al nome del facet. I tag di ricerca vengono utilizzati all’interno dei tag facet per i valori dei facet, come nell’esempio seguente: </p> <code class="syntax html"> &lt;facets&gt; 
     &nbsp;&nbsp;&lt;facet&nbsp;name="brand"&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;values&gt;&lt;search-field-value-list&nbsp;name="brand"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="values"&nbsp;sortby="values"&nbsp;/&gt;&lt;/values&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;counts&gt;&lt;search-field-value-list&nbsp;name="brand"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="counts"&nbsp;sortby="values"&nbsp;/&gt;&lt;/counts&gt; 
     &nbsp;&nbsp;&lt;/facet&gt; 
     &nbsp;&nbsp;&lt;facet&nbsp;name="category"&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;values&gt;&lt;search-field-value-list&nbsp;name="category"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="values"&nbsp;sortby="values"&nbsp;/&gt;&lt;/values&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;counts&gt;&lt;search-field-value-list&nbsp;name="category"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="counts"&nbsp;sortby="values"&nbsp;/&gt;&lt;/counts&gt; 
     &nbsp;&nbsp;&lt;/facet&gt; 
     &lt;/facets&gt; </code> <p> Gli account che utilizzano facet con slotted possono utilizzare il tag dinamico e il tag dei nomi visualizzati. Entrambi questi tag facilitano la mappatura tra facet inclinati e facet reali durante la creazione di regole aziendali. </p> <code class="syntax html"> &lt;facets&gt; 
     &nbsp;&nbsp;&lt;facet&nbsp;name="facet_values01"&gt; 
     &nbsp;&lt;dynamic&gt;1&lt;/dynamic&gt; 
     &nbsp;&lt;display-names&gt;&lt;search-field-value-list&nbsp;name="facet_names01"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="values"&nbsp;sortby="values"&nbsp;/&gt;&lt;/display-names&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;values&gt;&lt;search-field-value-list&nbsp;name="facet_values01"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="values"&nbsp;sortby="values"&nbsp;/&gt;&lt;/values&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;counts&gt;&lt;search-field-value-list&nbsp;name="facet_values01"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="counts"&nbsp;sortby="values"&nbsp;/&gt;&lt;/counts&gt; 
     &nbsp;&nbsp;&lt;/facet&gt; </code> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-display-field separator=","&gt; </span> </p> </td> 
   <td colname="col2"> <p>L'attributo <span class="codeph"> separatore </span> consente di modificare il delimitatore utilizzato quando si producono dati del campo di ricerca per gli elenchi. Il valore predefinito è una virgola. </p> <p>In genere, il delimitatore utilizzato dovrebbe essere qualcosa che non appare facilmente nel contenuto del campo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;suggestions&gt;&lt;/suggestions&gt; </span> </p> </td> 
   <td colname="col2"> <p> Racchiudi i tuoi suggerimenti con tag in modo che Ricerca guidata riconosca quali nodi XML contengono suggerimenti. </p> <p>Consulta <a href="../c-about-linguistics-menu/c-about-did-you-mean.md#concept_7D4F3C29EF184B538B8AE2ECAE0CDC5E" type="concept" format="dita" scope="local"> Informazioni su intendete</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;suggestion&gt;&lt;/suggestion&gt; </span> </p> </td> 
   <td colname="col2"> <p>Racchiudi ogni suggerimento con tag, come nell’esempio seguente: </p> <code class="syntax html"> &lt;search-if-suggestions&gt; 
     &nbsp;&nbsp;&lt;suggestions&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;search-suggestions&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;suggestion&gt;&lt;search-suggestion-text&nbsp;/&gt;&lt;/suggestion&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;/search-suggestions&gt; 
     &nbsp;&nbsp;&lt;/suggestions&gt; 
     &lt;/search-if-suggestions&gt; </code> <p>Consulta <a href="../c-about-linguistics-menu/c-about-did-you-mean.md#concept_7D4F3C29EF184B538B8AE2ECAE0CDC5E" type="concept" format="dita" scope="local"> Informazioni su intendete</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Tag del modello di ricerca {#reference_F7AA3FF602314E42842BBC740D2CA1A4}

Un modello di ricerca è un file HTML che include i tag modello definiti da site search/merchandising. Questi tag indicano come vengono formattati i risultati della ricerca. Il riferimento seguente contiene una breve descrizione di ciascun tag del modello di ricerca e dei relativi attributi.

<!-- 

r_search_template_tags.xml

 -->

>[!NOTE]
>
>Utilizza solo i tag modello di ricerca nei file modello di trasporto (.tpl).

È possibile selezionare tra i seguenti gruppi di tag del modello di ricerca e il materiale di riferimento.

I tag validi solo all’interno del ciclo dei risultati includono quanto segue:

* [Informazioni sui tag loop dei risultati](../c-appendices/c-templates.md#section_D4DC7B4560144663972E8DBC3369C629)
* [Tag della stringa del ciclo di risultati](../c-appendices/c-templates.md#section_80D68334E8D04A33937A6E58ABAAA320)
* [Tag condizionali del ciclo di risultati](../c-appendices/c-templates.md#section_35C367969E384A06A9865E388F1F9360)
* [Tag di collegamento loop dei risultati](../c-appendices/c-templates.md#section_C5FAEF520E9E42ADAD1F90651922AA02)
* [Tag condizionali per posizione di loop](../c-appendices/c-templates.md#section_E0C29DDA09E043C9A396F36334F05EBB)

I tag validi in tutto il modello includono quanto segue:

* [Tag dell’elenco dei valori dei campi](../c-appendices/c-templates.md#section_D3298B5F976447DBA0032B883DCC91B1)
* [Tag dell&#39;elenco di valori campo](../c-appendices/c-templates.md#section_0717FA09F0FC449CB916883B0500A60E)
* [Tag consigliati](../c-appendices/c-templates.md#section_C28EB8B4F7DC4E278A0F143BCFEEB1AC)
* [Tag stringa modello](../c-appendices/c-templates.md#section_67E3D529661F4F03A1FF469D9D658CAF)
* [Tag dei collegamenti di ancoraggio del modello](../c-appendices/c-templates.md#section_3A51D27616C541E2B818CC52B2B856BA)
* [Tag condizionali del modello](../c-appendices/c-templates.md#section_18D9BC66DE484881932FD2F7EA9D170D)
* [Tag del modulo modello](../c-appendices/c-templates.md#section_45AFC414ACA74825B72FEAA8456F8DD2)

Argomenti di riferimento per i modelli di ricerca

* [Stringhe formato data](../c-appendices/c-templates.md#section_4BBDBBEF2B96414497617CD4B52D96E4)
* [Identificatori di lingua](../c-appendices/c-templates.md#section_0490DECC00E34691ADE5A9ED90A6D911)
* [Specifica dell’intestazione HTTP di tipo contenuto](../c-appendices/c-templates.md#section_AEED823E9938448A9EDB2F286D9CFD90)
* [Specifica di un set di caratteri in un modello HTML](../c-appendices/c-templates.md#section_E0D1816ABB5846BEBE9C26D5980CCBE6)
* [Specifica di un set di caratteri in un modello XML](../c-appendices/c-templates.md#section_17DC31CDCC104F5F8081466B41A96E9D)
* [Inclusione di un modello di ricerca in un altro](../c-appendices/c-templates.md#section_7D1FCD3D9E2340C291E354C9720E8BC0)

## Informazioni sui tag loop dei risultati {#section_D4DC7B4560144663972E8DBC3369C629}

Il tag loop dei risultati è il motore di lavoro del sistema dei modelli. Quando il tag viene rilevato durante una ricerca, l’HTML viene ripetuto e altri tag tra i tag di ciclo dei risultati iniziale e finale, sostituendo qualsiasi altro tag con i risultati della ricerca.

`<search-results> ... </search-results>`

I tag loop dei risultati circondano l’HTML che mostra i risultati della ricerca. L’HTML tra i tag viene ripetuto per ogni risultato e viene visualizzato sulla pagina.

I seguenti tag sono validi solo all&#39;interno del ciclo dei risultati:

* [Tag della stringa del ciclo di risultati](../c-appendices/c-templates.md#section_80D68334E8D04A33937A6E58ABAAA320)
* [Tag condizionali del ciclo di risultati](../c-appendices/c-templates.md#section_35C367969E384A06A9865E388F1F9360)
* [Tag di collegamento loop dei risultati](../c-appendices/c-templates.md#section_C5FAEF520E9E42ADAD1F90651922AA02)
* [Tag condizionali per posizione di loop](../c-appendices/c-templates.md#section_E0C29DDA09E043C9A396F36334F05EBB)

## Tag stringa ciclo risultati {#section_80D68334E8D04A33937A6E58ABAAA320}

I seguenti tag restituiscono una stringa.

Vedere [Informazioni sui tag loop dei risultati](../c-appendices/c-templates.md#section_D4DC7B4560144663972E8DBC3369C629).

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Tag </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-index&gt; </span> </p> </td> 
   <td colname="col2"> <p>Restituisce l'indice numerico del risultato corrente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-title length="XX"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Restituisce il titolo della pagina del risultato corrente. L’attributo di lunghezza opzionale viene utilizzato per limitare la lunghezza delle stringhe visualizzate, con un valore predefinito di 80 caratteri. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-bodytext length="XX" encoding="html/javascript/json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Restituisce il testo del corpo che inizia dalla parte superiore della pagina. I termini pertinenti sono in grassetto. L’attributo di lunghezza opzionale viene utilizzato per limitare la lunghezza delle stringhe visualizzate, con un valore predefinito di 80 caratteri. L’attributo encoding è facoltativo e può codificare i caratteri di output con codifica HTML (predefinita), codifica JavaScript, codifica Perl o nessuna. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-description length="XX" encoding="html/javascript/json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> <p> Restituisce la descrizione del risultato corrente. Se il tag meta description esiste e l'attributo content non è vuoto, viene visualizzato il testo specificato. In caso contrario, viene visualizzata l’inizio del corpo del testo della pagina. L’attributo di lunghezza opzionale viene utilizzato per limitare la lunghezza delle stringhe visualizzate, con un valore predefinito di 80 caratteri. </p> <p>L'attributo opzionale <span class="codeph"> encoding </span> controlla se l'output è codificato in HTML, codificato JavaScript, codificato in Perl, codificato o meno nell'URL, per l'output nella pagina dei risultati. Il valore predefinito della codifica <span class="codeph"> </span> è <span class="codeph"> html </span>. Normalmente, non è necessario specificare l'attributo di codifica. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-score rank="dynamic/static/dynamic-raw/static-raw/final-raw" precision="XX"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Restituisce il punteggio del risultato corrente, che è un numero da 0 a 100. Se hai definito un campo di classificazione in <span class="uicontrol"> Opzioni </span> &gt; <span class="uicontrol"> Metadati </span> &gt; <span class="uicontrol"> Definizioni </span>, puoi visualizzare il rango dinamico della pagina impostando l’attributo di classificazione su dinamico ( <span class="codeph"> &lt;search-score rank="dynamic"&gt; </span>). Puoi visualizzare la classificazione statica della pagina impostando l’attributo di classificazione su static ( <span class="codeph"> &lt;search-score rank="static"&gt; </span>). È possibile utilizzare l’attributo di precisione facoltativo per specificare il numero di posizioni decimali da visualizzare. Il valore predefinito è 0, che visualizza il punteggio intero). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-date length="XX" none="text" date-format="date-format-string" gmt="yes/no" language="0/2/language-id"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Restituisce la data del risultato corrente. Il valore di testo facoltativo "none" viene visualizzato se non è presente una data associata al risultato corrente. Se il valore facoltativo "none" non è specificato, viene visualizzato il testo "No Date" se non è associata alcuna data al risultato corrente. </p> <p>L'attributo "formato data" utilizza una stringa in formato data stile UNIX come "%A, %B %d, %Y" (per "lunedì 25 luglio 2016"). Per impostazione predefinita, "gmt" viene impostato su "yes" e controlla se la parte dell’ora della stringa di data deve essere restituita in GMT ("yes") o nel fuso orario dell’account ("no"). </p> <p>L’attributo "language" controlla le convenzioni relative alla lingua e alle impostazioni internazionali della stringa della data di output. "0" (impostazione predefinita) significa "Usa lingua account". "2" significa "Usa lingua documento". Il valore "language" "1" è riservato per utilizzi futuri. Qualsiasi altro valore "language" viene interpretato come un identificatore specifico della lingua, ad esempio, "en_US" significa "Inglese (Stati Uniti)". </p> <p>L’attributo di lunghezza opzionale viene utilizzato per limitare la lunghezza delle stringhe visualizzate, con un valore predefinito di 80 caratteri. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-size&gt; </span> </p> </td> 
   <td colname="col2"> <p>Restituisce la dimensione del risultato corrente in byte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-url length="XX" encoding="html/javascript/json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Restituisce l’URL del risultato corrente. </p> <p>Utilizza l'attributo opzionale <span class="codeph"> length </span> per limitare la lunghezza delle stringhe visualizzate, con un valore predefinito di caratteri illimitati. </p> <p>L'attributo <span class="codeph"> encoding </span> è facoltativo e può codificare i caratteri di output con codifica HTML, codifica Javascript, codifica Perl o nessuno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-url-path-query length="XX"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Restituisce il percorso e le porzioni di query, compreso il punto interrogativo dell'URL del risultato corrente. </p> <p>Utilizza l'attributo opzionale <span class="codeph"> length </span> per limitare la lunghezza delle stringhe visualizzate, con un valore predefinito di caratteri illimitati. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-context length="XX" encoding="html/javascript/json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Restituisce la riga di contesto successiva per il termine di ricerca. I termini pertinenti sono in grassetto. Chiama ripetutamente questo tag per visualizzare più di una riga del contesto per il risultato corrente. </p> <p>Utilizza l'attributo opzionale <span class="codeph"> length </span> per limitare la lunghezza delle stringhe visualizzate, con un valore predefinito di 80 caratteri. L'attributo <span class="codeph"> length </span> viene ignorato se il tag è racchiuso tra i set di tag <span class="codeph"> &lt;search-if-context&gt; </span> o <span class="codeph"> &lt;search-if-any-context&gt; </span> che contengono un attributo length. </p> <p>L’attributo <span class="codeph"> encoding </span> è facoltativo e può codificare i caratteri di output con codifica HTML (impostazione predefinita), codifica Javascript, codifica Perl o nessuna. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>11 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-display-field name="field-name" length="XX" none="text" date-format="date-format-string" gmt="yes/no" language="0/2/language-id" encoding="html/javascript/json/perl/url/none" quotes="yes/no" commas="yes/no" units="miles/kilometers" separator="|"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Questo tag avanzato visualizza il contenuto del campo metadati (url, titolo, desc, chiavi, target, corpo, alt, data, set di caratteri e lingua o dei campi definiti in <span class="uicontrol"> Opzioni </span> &gt; <span class="uicontrol"> Metadati </span> &gt; Definizioni) specificato nell'attributo <span class="codeph"> name </span> per il risultato corrente. Ad esempio: </p> <p> <span class="codeph"> &lt;search-display-field name="title" length="70" none="no title"&gt; </span> </p> <p>Invia il titolo della pagina per un risultato della ricerca. Se è specificato l’attributo facoltativo <span class="codeph"> none </span> , il relativo valore viene visualizzato nella pagina dei risultati solo se non è presente alcun contenuto associato al campo. </p> <p>Gli attributi del formato data <span class="codeph"> </span>, <span class="codeph"> gmt </span> e <span class="codeph"> lingua </span> sono rilevanti solo se il tipo di contenuto del campo specificato è <span class="codeph"> data </span>. </p> <p>L'attributo <span class="codeph"> formato data </span> utilizza una stringa formato data stile UNIX come <span class="codeph"> %A, %B %d, %Y </span> (per lunedì 25 luglio 2016). <span class="codeph"> gmt  </span> imposta il valore predefinito su  <span class="codeph"> yes  </span> e controlla se la parte dell’ora della stringa di data viene restituita in GMT (  <span class="codeph"> yes  </span>) o nel fuso orario dell’account (  <span class="codeph"> no  </span>). </p> <p>Vedere <a href="../c-appendices/c-templates.md#section_4BBDBBEF2B96414497617CD4B52D96E4" type="section" format="dita" scope="local"> Stringhe del formato della data</a>. </p> <p>L'attributo <span class="codeph"> language </span> controlla le convenzioni relative alla lingua e alle impostazioni internazionali della stringa della data di output. <span class="codeph"> 0  </span> (impostazione predefinita) significa "Usa lingua account". <span class="codeph"> 2  </span> significa "Usa lingua documento". Il valore <span class="codeph"> language </span> <span class="codeph"> 1 </span> è riservato per utilizzi futuri). Qualsiasi altro valore <span class="codeph"> della lingua </span> viene interpretato come un identificatore specifico della lingua, ad esempio <span class="codeph"> en_US </span> significa "Inglese (Stati Uniti)". </p> <p>Consultare <a href="../c-appendices/c-templates.md#section_0490DECC00E34691ADE5A9ED90A6D911" type="section" format="dita" scope="local"> Identificatori di lingua</a>. </p> <p>L'attributo facoltativo <span class="codeph"> length </span> viene utilizzato per limitare la lunghezza delle stringhe visualizzate, con un valore predefinito di 80 caratteri. </p> <p>L'attributo opzionale <span class="codeph"> encoding </span> controlla se l'output è codificato in HTML, codificato JavaScript, codificato in Perl, codificato o meno nell'URL, per l'output nella pagina dei risultati. Il valore predefinito della codifica <span class="codeph"> </span> è <span class="codeph"> html </span>. Normalmente, non è necessario specificare l'attributo di codifica. </p> <p>L'attributo opzionale <span class="codeph"> virgolette </span> controlla se i singoli elementi di output sono circondati da virgolette doppie (o virgolette singole, se <span class="codeph"> encoding=perl </span>). Il valore predefinito di <span class="codeph"> virgolette </span> è <span class="codeph"> no </span>. </p> <p>L'attributo facoltativo <span class="codeph"> virgola </span> controlla se i singoli elementi in uscita sono separati da virgole. Il valore predefinito di <span class="codeph"> virgole </span> è <span class="codeph"> sì </span>. L’attributo <span class="codeph"> virgole </span> viene ignorato per i campi non di tipo elenco. </p> <p>L'attributo opzionale <span class="codeph"> unità </span> controlla le unità di distanza applicate a un campo di output di ricerca di prossimità. Il valore predefinito delle unità <span class="codeph"> </span> è determinato dall'impostazione "Unità predefinite" del campo di tipo posizione associato al campo di output della ricerca di prossimità specificato. </p> <p>Vedere <a href="../c-appendices/r-about-proximity-search.md#reference_45AC6BB50609431ABD31DA46EE65360D" type="reference" format="dita" scope="local"> Informazioni sulla ricerca di prossimità</a>. </p> <p>L'attributo <span class="codeph"> separatore opzionale </span> definisce il carattere singolo, o delimitatore, inserito tra i valori dell'output per i campi di tipo elenco. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>12 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-display-field-values name="field-name"&gt; ...&lt;search-display-field-values&gt; </span> </p> </td> 
   <td colname="col2"> <p>Questo tag crea un ciclo per l’enumerazione dei valori dei campi di metadati (url, titolo, desc, chiavi, target, corpo, alt, data, set di caratteri e lingua o campi definiti in <span class="uicontrol"> Opzioni </span> &gt; <span class="uicontrol"> Metadati </span> &gt; <span class="uicontrol"> Definizioni </span>) per il risultato corrente. Non nidificare questo tag all’interno di un altro tag <span class="codeph"> &lt;search-display-field-values&gt; </span> . L'attributo <span class="codeph"> name </span> specifica il nome del campo contenente i valori da enumerare. Questo tag è particolarmente utile nei campi in cui è selezionato l’attributo <span class="uicontrol"> Elenchi consentiti </span> (in <span class="uicontrol"> Opzioni </span> &gt; <span class="uicontrol"> Metadati </span> &gt; <span class="uicontrol"> Definizioni </span>). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>13 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-display-field-value date-format="date-format-string" gmt="yes/no" language="0/language-id" encoding="html/javascript/json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Questo tag restituisce il valore del campo metadati (url, titolo, desc, chiavi, target, corpo, alt, data, set di caratteri e lingua o i campi definiti in <span class="uicontrol"> Opzioni </span> &gt; <span class="uicontrol"> Metadati </span> &gt; <span class="uicontrol"> Definizioni </span>) per l'iterazione del ciclo <span class="codeph">  &lt;search-display-field-values&gt; </span>. Questo tag è valido solo all'interno di un ciclo <span class="codeph"> &lt;search-display-field-values&gt; </span> . Gli attributi del <span class="codeph"> formato data </span>, <span class="codeph"> gmt </span> e <span class="codeph"> linguaggio </span> sono pertinenti solo se il tipo di contenuto del nome campo specificato nel tag <span class="codeph">  </span> di inclusione è <span class="codeph"> data </span>. L'attributo <span class="codeph"> formato data </span> utilizza una stringa formato data stile UNIX come <span class="codeph"> "%A </span>, <span class="codeph"> %B </span> <span class="codeph"> %d </span>, <span class="codeph"> %Y </span>" (per "lunedì 25 luglio 2016"). L'attributo <span class="codeph"> gmt </span> viene impostato automaticamente su <span class="codeph"> yes </span> e controlla se la porzione di ora della stringa di data viene restituita in GMT ( <span class="codeph"> yes </span>) o nel fuso orario dell'account ( <span class="codeph"> no </span>). </p> <p>L'attributo <span class="codeph"> language </span> controlla le convenzioni relative alla lingua e alle impostazioni internazionali della stringa della data di output. <span class="codeph"> 0  </span> (impostazione predefinita) significa "Usa lingua account". Qualsiasi altro valore <span class="codeph"> della lingua </span> viene interpretato come un identificatore specifico della lingua, ad esempio <span class="codeph"> en_US </span> significa "Inglese (Stati Uniti)". </p> <p>L'attributo opzionale <span class="codeph"> encoding </span> controlla se l'output è codificato in HTML, codificato JavaScript, codificato in Perl, codificato o meno nell'URL, per l'output nella pagina dei risultati. Il valore predefinito della codifica <span class="codeph"> </span> è <span class="codeph"> html </span>. Normalmente, non è necessario specificare l'attributo di codifica. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>14 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-display-field-value-count name="field-name"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Trasmette il numero totale di valori nel risultato corrente per il campo metadati (url, title, desc, keys, target, body, alt, date, charset e lingua o campi definiti in <span class="uicontrol"> Opzioni </span> &gt; <span class="uicontrol"> Metadati </span> &gt; <span class="uicontrol"> Definizioni </span> specificate con l'attributo name. Questo tag può essere visualizzato in qualsiasi punto del ciclo dei risultati. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>15 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-display-field-value-counter&gt; </span> </p> </td> 
   <td colname="col2"> <p>Invia il contatore ordinale (1, 2, 3 e così via) per l'iterazione del ciclo <span class="codeph"> &lt;search-display-field-values&gt; </span> corrente. Questo tag è valido solo all'interno di un ciclo <span class="codeph"> &lt;search-display-field-values&gt; </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>16 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-dynamic-facet-fields&gt; </span> </p> </td> 
   <td colname="col2"> <p>Inizia un contesto di ciclo per tutti i campi-facet dinamici restituiti per questa ricerca. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>17 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-dynamic-facet-field-name&gt; </span> </p> </td> 
   <td colname="col2"> <p>Invia il nome del campo dinamico-facet-field corrente per questa iterazione del ciclo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>18 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW for S&P 8.17.0 release on October 30 2014--> <span class="codeph"> &lt;search-result-trace encoding="html/javascript/ json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Trasmette informazioni relative al posizionamento del risultato corrente, ad esempio qualsiasi azione basata su risultati che ha influenzato la posizione del risultato. </p> <p>Il formato di output di questo tag è JSON, come nell’esempio seguente: </p> <p> <code> { 
      &nbsp;&nbsp;"sliceID":&nbsp;5, 
      &nbsp;&nbsp;"indexID":&nbsp;5894, 
      &nbsp;&nbsp;"finalScore":&nbsp;98.5, 
      &nbsp;&nbsp;"dynamicScore":&nbsp;15.3, 
      &nbsp;&nbsp;"staticScore":&nbsp;55.456, 
      &nbsp;&nbsp;"position":&nbsp;1, 
      &nbsp;&nbsp;"rbtaActionListID":&nbsp;117, 
      &nbsp;&nbsp;"rbtaActionID":&nbsp;57 
      } </code> </p> 
    <!--<p> Results added to the results set by way of <codeph>rbta</codeph> have a "naturalPosition" value of -1. </p>--> <p>L'attributo <span class="codeph"> encoding </span> è facoltativo; il valore predefinito è <span class="codeph"> html </span>. </p> <p> <p>Nota:  Questo tag ha output solo se <span class="codeph"> sp_trace=1 </span> è specificato con i parametri della query di ricerca di base. </p> </p> <p>Vedi la riga 48 nella tabella riportata in <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" format="dita" scope="local"> Parametri CGI di ricerca back-end</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Tag condizionali loop risultati {#section_35C367969E384A06A9865E388F1F9360}

I seguenti tag includono l’HTML tra di loro in modo condizionale.

Vedere [Informazioni sui tag loop dei risultati](../c-appendices/c-templates.md#section_D4DC7B4560144663972E8DBC3369C629).

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Tag </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-title&gt; ...  &lt;/search-if-title&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-title&gt; ...  &lt;/search-if-not-title&gt; </span> </p> </td> 
   <td colname="col2"> <p>Questi tag includono l'HTML tra di loro se la successiva chiamata a <span class="codeph"> &lt;search-title&gt; </span> restituisce (o non restituisce) il testo dal titolo del documento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-description length="XX"&gt; ... /search-if-description&gt;  </span> </p> <p> <span class="codeph"> &lt;search-if-not-description&gt; ...  &lt;/search-if-not-description&gt; </span> </p> </td> 
   <td colname="col2"> <p> Questi tag includono l'HTML tra di loro se la successiva chiamata a <span class="codeph"> &lt;search-description&gt; </span> restituisce (o non restituisce) il testo dalla descrizione del documento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-bodytext&gt; ...  &lt;/search-if-bodytext&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-bodytext&gt; ...  &lt;/search-if-not-bodytext&gt; </span> </p> </td> 
   <td colname="col2"> <p>Questi tag includono l'HTML tra di loro se la successiva chiamata a <span class="codeph"> &lt;search-bodytext&gt; </span> restituisce (o non restituisce) il testo dal corpo del documento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-context length="XX"&gt; ...  &lt;/search-if-context&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-context&gt; ...  &lt;/search-if-not-context&gt; </span> </p> </td> 
   <td colname="col2"> <p>Questi tag includono l'HTML tra di loro se la chiamata successiva a <span class="codeph"> &lt;search-context&gt; </span> restituisce (o non restituisce) una stringa di contesto non vuota. L’attributo length sostituisce l’attributo length su qualsiasi tag racchiuso <span class="codeph"> &lt;search-context&gt; </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-any-context length="XX"&gt; ... /search-if-any-context&gt;  </span> </p> <p> <span class="codeph"> &lt;search-if-not-any-context&gt; ...  &lt;/search-if-not-any-context&gt; </span> </p> </td> 
   <td colname="col2"> <p>Questi tag includono l'HTML tra di loro se è presente (o meno) una stringa di contesto associata al risultato. L’attributo length sostituisce l’attributo length su qualsiasi tag racchiuso <span class="codeph"> &lt;search-context&gt; </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-score lower="XX" upper="yy" rank="dynamic/static/dynamic-raw/static-raw/final-raw"&gt; ...  &lt;/search-if-score&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-score lower="XX" upper="yy" rank="dynamic/static"&gt; ...  &lt;/search-if-not-score&gt; </span> </p> </td> 
   <td colname="col2"> <p>Questi tag includono l’HTML tra di loro se il punteggio del risultato corrente è (o non è) compreso tra XX e AA. Utile per aggiungere punti elenco o elementi grafici per mostrare l’importanza del risultato. Se hai definito un campo di tipo rango in <span class="uicontrol"> Opzioni </span> &gt; <span class="uicontrol"> Metadati </span> &gt; <span class="uicontrol"> Definizioni </span>, puoi controllare il rango dinamico della pagina impostando l’attributo di rango su dinamico ( <span class="codeph"> &lt;search-if-score rank="dynamic" lower=XX Upper=YY&gt; </span>). Puoi controllare la classificazione della pagina statica impostando l’attributo di classificazione su static ( <span class="codeph"> &lt;search-if-score rank="static" lower=XX up=YY&gt; </span>). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-field name="field-name" value="value"&gt; ...  &lt;/search-if-field&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-field name="field-name" value="value"&gt; ...  &lt;/search-if-not-field&gt; </span> </p> </td> 
   <td colname="col2"> <p>Questi tag avanzati includono l’HTML tra di loro in base al fatto che il campo specificato nell’attributo "name" abbia o meno contenuto. Se è specificato l'attributo opzionale "value", i tag includono l'HTML tra di loro in base al fatto che il valore specificato corrisponda o meno al valore del campo nel risultato corrente. Questi tag funzionano solo all’interno del ciclo dei risultati (tra i tag <span class="codeph"> &lt;search-results&gt; </span> e <span class="codeph"> &lt;/search-results&gt; </span> ). </p> </td> 
  </tr> 
 </tbody> 
</table>

## Tag di collegamento di ancoraggio del ciclo dei risultati {#section_C5FAEF520E9E42ADAD1F90651922AA02}

Vedere [Informazioni sui tag loop dei risultati](../c-appendices/c-templates.md#section_D4DC7B4560144663972E8DBC3369C629).

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Tag </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-link target="frame-name" hbx-enable="yes/no" hbx-linkid-name="field-name" hbx-linkid-none="text" hbx-linkid-length="XX"&gt; ...  &lt;/search-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Questa coppia di tag crea un collegamento di ancoraggio intorno all’HTML che li circonda. Quando fai clic sul collegamento, viene visualizzata la pagina dei risultati. Un attributo di destinazione facoltativo specifica la finestra denominata in cui i browser compatibili con frame devono visualizzare la pagina dei risultati. </p> <p>Imposta l'attributo hbx-enable su "yes" per sfruttare l'analisi disponibile tramite HBX. Imposta hbx-linkid-name sul nome di un campo Meta-data che desideri monitorare. Ad esempio, per tenere traccia dei risultati della ricerca in base al numero SKU, imposta hbx-linkid-name sul nome del campo Meta-data contenente le informazioni SKU. </p> <p>I campi tipo data non sono attualmente supportati. Il valore di hbx-linkid-name viene aggiunto all'ID del collegamento nell'ancoraggio generato. Il valore dell'attributo hbx-linkid-none viene aggiunto all'ID del collegamento ogni volta che il campo dei metadati denominato è vuoto. Il valore di hbx-linboy-length limita il numero di caratteri recuperati e visualizzati dal tag Meta . Il numero predefinito di caratteri è 12. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-smart-link target="frame-name" hbx-enable="yes/no" hbx-linkid-name="field-name" hbx-linkid-none="text" hbx-linkid-length="XX"&gt; ...  &lt;/search-smart-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Questa coppia di tag è simile ai tag <span class="codeph"> &lt;search-link&gt; ... &lt;/search-link&gt; </span> . Quando fai clic sui collegamenti di ancoraggio generati, viene visualizzata la pagina dei risultati, ma con la pagina scorrevole fino al tag di ancoraggio più vicino prima del risultato. Per i collegamenti PDF, nel visualizzatore Acrobat viene visualizzata la pagina contenente il risultato. Un attributo di destinazione facoltativo specifica la finestra denominata in cui i browser compatibili con frame devono visualizzare la pagina dei risultati. </p> <p>Imposta l'attributo hbx-enable su "yes" per sfruttare l'analisi disponibile tramite HBX. Imposta hbx-linkid-name sul nome di un campo Meta-data che desideri monitorare. Ad esempio, per tenere traccia dei risultati della ricerca in base al numero SKU, imposta hbx-linkid-name sul nome del campo Meta-data contenente le informazioni SKU. </p> <p>I campi tipo data non sono attualmente supportati. Il valore di hbx-linkid-name viene aggiunto all'ID del collegamento nell'ancoraggio generato. Il valore dell'attributo hbx-linkid-none viene aggiunto all'ID del collegamento ogni volta che il campo dei metadati denominato è vuoto. Il valore di hbx-linboy-length limita il numero di caratteri recuperati e visualizzati dal tag Meta . Il numero predefinito di caratteri è 12. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-link-extension&gt; ...  &lt;/search-if-link-extension&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-link-extension&gt; ...  &lt;/search-if-not-link-extension&gt; </span> </p> </td> 
   <td colname="col2"> <p>Questi tag includono l'HTML tra di loro se un attributo value specifica un'estensione che corrisponde alla fine dell'URL per il risultato. Questo tag è utile per includere un elemento grafico nei risultati della ricerca in base all’estensione del collegamento. L'attributo value è un elenco di una o più estensioni (separate da spazi) come segue: VALUE=".pdf" o VALUE=".html .htm". </p> </td> 
  </tr> 
 </tbody> 
</table>

## Tag condizionali per posizione di loop {#section_E0C29DDA09E043C9A396F36334F05EBB}

I seguenti tag includono in modo condizionale il testo tra di essi. Possono essere visualizzati solo all’interno dei tag di &quot;looping&quot;: &lt; `search-results>` e `<search-field-values>`. Vengono utilizzati per verificare la posizione del risultato corrente all’interno del set di risultati.

Vedere [Informazioni sui tag loop dei risultati](../c-appendices/c-templates.md#section_D4DC7B4560144663972E8DBC3369C629).

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Tag </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-first&gt; ...  &lt;/search-if-first&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-first&gt; ...  &lt;/search-if-not-first&gt; </span> </p> </td> 
   <td colname="col2"> <p>Questi tag includono il testo tra di essi se il risultato corrente è (o non è) il primo risultato della pagina (quando utilizzato all'interno di <span class="codeph"> &lt;search-results&gt; </span>) o il primo valore del campo (se utilizzato all'interno di <span class="codeph"> &lt;search-field-values&gt; </span>). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-last&gt; ...  &lt;/search-if-last&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-last&gt; ...  &lt;/search-if-not-last&gt; </span> </p> </td> 
   <td colname="col2"> <p>Questi tag includono il testo tra di essi se il risultato corrente è (o non è) l'ultimo risultato della pagina (quando utilizzato all'interno di <span class="codeph"> &lt;search-results&gt; </span>) o l'ultimo valore del campo (se utilizzato all'interno di <span class="codeph"> &lt;search-field-values&gt; </span>). Questo tag può essere utilizzato per inserire un separatore tra i risultati. Ad esempio, questo inserisce un tag <span class="codeph"> &lt;hr&gt; </span> tra i risultati: </p> <p> <code class="syntax html"> &lt;search-results&gt; 
      &nbsp;&nbsp;&nbsp;&lt;search-lt&gt;tr&lt;search-if-alt&gt;&nbsp;class="alt"&lt;/search-if-alt&gt;&lt;search-gt&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;td&gt;&lt;search-url&gt;&lt;/td&gt; 
      &nbsp;&nbsp;&nbsp;&lt;/tr&gt; 
      &lt;/search-results&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-inner&gt; ...  &lt;/search-if-inner&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-inner&gt; ...  &lt;/search-if-not-inner&gt; </span> </p> </td> 
   <td colname="col2"> <p>Questi tag includono il testo tra di essi se il risultato corrente non è né il primo né l'ultimo risultato della pagina (se utilizzato all'interno di <span class="codeph"> &lt;search-results&gt; </span>) o non è il primo né l'ultimo valore del campo (se utilizzato all'interno di <span class="codeph"> &lt;search-field-values&gt; </span>). La versione non del tag verifica se il risultato è il primo o l’ultimo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-alt&gt; ...  &lt;/search-if-alt&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-alt&gt; ...  &lt;/search-if-not-alt&gt; </span> </p> </td> 
   <td colname="col2"> <p>Questi tag includono il testo tra di essi se il risultato corrente è (o non è) un risultato alternativo nella pagina (se utilizzato all'interno di <span class="codeph"> &lt;search-results&gt; </span>) o un valore di campo alternativo (se utilizzato all'interno di <span class="codeph"> &lt;search-field-values&gt; </span>). I risultati "alternativi" sono il secondo, il quarto, il sesto e così via, sulla pagina. In questo esempio viene applicata una classe diversa alle righe di tabella alternative. Tieni presente l’uso di <span class="codeph"> &lt;search-lt&gt; </span> e <span class="codeph"> &lt;search-gt&gt; </span> per consentire al tag <span class="codeph"> &lt;search-if-alt&gt; </span> di essere posizionato "all’interno" del tag <span class="codeph"> &lt;tr&gt; </span>. </p> <p> <code class="syntax html"> &nbsp;&nbsp;&nbsp;&nbsp;&lt;search-results&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;search-lt&gt;tr&lt;search-if-alt&gt;&nbsp;class="alt"&lt;/search-if-alt&gt;&lt;search-gt&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;td&gt;&lt;search-url&gt;&lt;/td&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/tr&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/search-results&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-even&gt; ...  &lt;/search-if-even&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-even&gt; ...  &lt;/search-if-not-even&gt; </span> </p> </td> 
   <td colname="col2"> <p>Questi tag includono il testo tra di essi se il risultato corrente è (o non è) un risultato pari (se utilizzato all'interno di <span class="codeph"> &lt;search-results&gt; </span>) o un valore di campo pari (se utilizzato all'interno di <span class="codeph"> &lt;search-field-values&gt; </span>). Un risultato di ricerca è numerato pari se il relativo valore <span class="codeph"> &lt;search-index&gt; </span> è pari. In altre parole, se la sua posizione all'interno dell'intero set di risultati è pari. Questo può essere diverso da <span class="codeph"> &lt;search-if-alt&gt; </span> che verifica la posizione di un risultato sulla pagina e non all’intero set di risultati. Le due tabelle seguenti illustrano la differenza: </p> </td> 
  </tr> 
 </tbody> 
</table>

### Prima pagina, sp_n=1

<table>  
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Indice </p> </th> 
   <th colname="col2" class="entry"> <p>Risultato </p> </th> 
   <th colname="col3" class="entry"> <p>Anche? </p> </th> 
   <th colname="col4" class="entry"> <p>Alt? </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>3 </p> </td> 
   <td colname="col2"> <p>Primo risultato </p> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>No </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2 </p> </td> 
   <td colname="col2"> <p>Secondo risultato </p> </td> 
   <td colname="col3"> <p>Sì </p> </td> 
   <td colname="col4"> <p>Sì </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>3 </p> </td> 
   <td colname="col2"> <p>Terzo risultato </p> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>No </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4 </p> </td> 
   <td colname="col2"> <p>Quarto risultato </p> </td> 
   <td colname="col3"> <p>Sì </p> </td> 
   <td colname="col4"> <p>Sì </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>5 </p> </td> 
   <td colname="col2"> <p>Quinto risultato </p> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>No </p> </td> 
  </tr> 
 </tbody> 
</table>

### Pagina successiva, sp_n=10

<table>  
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Indice </p> </th> 
   <th colname="col2" class="entry"> <p>Risultato </p> </th> 
   <th colname="col3" class="entry"> <p>Anche? </p> </th> 
   <th colname="col4" class="entry"> <p>Alt? </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>10 </p> </td> 
   <td colname="col2"> <p>Decimo risultato </p> </td> 
   <td colname="col3"> <p>Sì </p> </td> 
   <td colname="col4"> <p>No </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>11 </p> </td> 
   <td colname="col2"> <p>Undicesimo risultato </p> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Sì </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>12 </p> </td> 
   <td colname="col2"> <p>Dodicesimo risultato </p> </td> 
   <td colname="col3"> <p>Sì </p> </td> 
   <td colname="col4"> <p>No </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>13 </p> </td> 
   <td colname="col2"> <p>Tredicesimo risultato </p> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Sì </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>14 </p> </td> 
   <td colname="col2"> <p>Quattordicesimo risultato </p> </td> 
   <td colname="col3"> <p>Sì </p> </td> 
   <td colname="col4"> <p>No </p> </td> 
  </tr> 
 </tbody> 
</table>

Infine, tieni presente che `<search-if-even>` è sempre lo stesso di `<search-if-alt>` per i valori dei campi di ricerca, in quanto i valori dei campi non vengono impaginati.

## Tag dell&#39;elenco dei valori dei campi {#section_D3298B5F976447DBA0032B883DCC91B1}

I seguenti tag avanzati restituiscono valori di campo e dati correlati dall’intero set di risultati di ricerca. Questi tag producono solo output per i campi specificati dai parametri `sp-sfvl-field` CGI nella query di ricerca.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Tag </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-field-value-list name="field-name" quotes="yes/no" commas="yes/no" data="values/counts/results" separator="X" sortby="none/values/counts/results" max-items="XX" date-format="date-format-string" gmt="yes/no" language="0/language-id" encoding="html/javascript/json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Questo tag visualizza un elenco di valori di campo univoci, conteggi di valori o conteggi di risultati all’interno dell’intero set di risultati. </p> <p>Questo tag genera solo l’output dei campi specificati dai parametri <span class="codeph"> sp_sfvl_field </span> CGI nella query di ricerca. L’attributo opzionale "virgolette" controlla se i singoli elementi in uscita sono circondati da virgolette doppie (o virgolette singole, se encoding=perl). Il valore predefinito di "quote" è "sì". L'attributo "virgola" facoltativo controlla se i singoli elementi in uscita sono separati da virgole. Il valore predefinito di "virgole" è "sì". L’attributo opzionale "data" controlla se ogni valore di campo univoco viene restituito (data="values"), il conteggio totale di ciascun valore di campo univoco viene restituito (data="count") o il numero di risultati contenenti ciascun valore univoco (data="results"). Il valore predefinito di "data" è "values". Per i campi non di tipo elenco, data="conteggi" e data="risultati" sono equivalenti. L'attributo separatore definisce il carattere singolo o delimitatore da inserire tra i valori dell'output. L'attributo "sortby" facoltativo controlla l'ordine del risultato; sortby="none" significa nessun ordine particolare, sortby="values" significa ordinamento per valori di campo (in ordine crescente o decrescente in base alla proprietà Ordinamento del campo), sortby="conteggi" significa ordinamento in ordine decrescente dei conteggi dei valori di campo e sortby="results" significa ordinamento in ordine decrescente del numero di risultati contenenti ciascun valore. </p> <p>Sortby="conteggi" e sortby="risultati" sono equivalenti per i campi non di tipo elenco. L’attributo opzionale "max-items" limita il numero di elementi da restituire. Il valore predefinito di "max-items" è -1, il che significa "output all items". </p> <p>Esiste un limite assoluto di 100 per gli elementi massimi. Gli attributi "formato data", "gmt" e "lingua" sono rilevanti solo se il tipo di contenuto del campo specificato è "data". L'attributo "formato data" utilizza una stringa in formato data stile UNIX come "%A, %B %d, %Y" (per "lunedì 25 luglio 2016"). Per impostazione predefinita, "gmt" viene impostato su "yes" e controlla se la parte dell’ora della stringa di data deve essere restituita in GMT ("yes") o nel fuso orario dell’account ("no"). </p> <p>Vedere <a href="../c-appendices/c-templates.md#section_4BBDBBEF2B96414497617CD4B52D96E4" type="section" format="dita" scope="local"> Stringhe del formato della data</a>. </p> <p>L’attributo "language" controlla le convenzioni relative alla lingua e alle impostazioni internazionali della stringa della data di output. "0" (impostazione predefinita) significa "Usa lingua account". Qualsiasi altro valore "language" viene interpretato come un identificatore specifico della lingua, ad esempio, "en_US" significa "Inglese (Stati Uniti)". L’attributo "encoding" facoltativo controlla se i caratteri della stringa di output sono codificati in HTML, codificati JavaScript, codificati Perl, codificati o meno nell’URL, per l’output sulla pagina dei risultati. Il valore predefinito di "encoding" è "html". </p> <p>Consultare <a href="../c-appendices/c-templates.md#section_0490DECC00E34691ADE5A9ED90A6D911" type="section" format="dita" scope="local"> Identificatori di lingua</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-field-value-list-count name="field-name" value="field-value" results="yes/no"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Questo tag visualizza le informazioni sul conteggio per un dato elenco di valori-campo di ricerca. Per questo tag sono disponibili tre utilizzi distinti. Se viene fornito solo l’attributo "name", questo tag restituisce il numero di valori univoci per il campo denominato all’interno dell’intero set di risultati. Se vengono forniti entrambi gli attributi "name" e "value", questo tag restituisce il conteggio totale del valore dato all’interno dell’intero set di risultati (per result="no") oppure il conteggio totale dei risultati contenenti il valore dato nell’intero set di risultati (per results="yes"). Il valore predefinito di "results" è "no". Nota: Per i campi non di tipo elenco, result="yes" e results="no" sono equivalenti. Il valore di "results" viene ignorato se l'attributo "value" non è specificato. Questo tag genera solo l’output dei campi specificati dai parametri <span class="codeph"> sp-sfvl-field </span> CGI nella query di ricerca. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-field-value-list-count name="field-name" value="field-value"&gt; ...  &lt;/search-if-field-value-list-count&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-field-value-list-count name="field-name" value="field-value"&gt; ...  &lt;/search-if-not-field-value-list-count&gt; </span> </p> </td> 
   <td colname="col2"> <p>Questi tag visualizzano il codice HTML tra di loro se la chiamata equivalente a <span class="codeph">  &lt;search-field-value-list-count name="field-name" value="field-value"&gt; </span> con gli attributi specificati restituirà (o non restituirà) un valore maggiore di zero. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-single-field-value-list-count name="field-name"&gt; ...  &lt;/search-if-single-field-value-list-count&gt; </span> </p> </td> 
   <td colname="col2"> <p>Questi tag visualizzano il contenuto tra di loro se la chiamata equivalente a <span class="codeph">  &lt;search-field-value-list-count name="field-name" value="field-value"&gt; </span> con gli attributi specificati restituirebbe (o meno) un singolo valore. Questo viene generalmente utilizzato quando un account utilizza slot per facet. Con gli slot per facet, in genere si desidera visualizzare lo slot per valori solo quando lo slot per nomi associato ha un singolo elemento. Eseguire questo controllo nel modello di trasporto è più efficiente rispetto a farlo nel livello di presentazione. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Tag dell&#39;elenco di valori dei campi {#section_0717FA09F0FC449CB916883B0500A60E}

I seguenti tag avanzati enumerano e producono i valori dei campi e i dati correlati dall’intero set di risultati di ricerca utilizzando un costrutto di ripetizione. Questi tag producono solo output per i campi specificati dai parametri `sp-sfvl-field` CGI nella query di ricerca.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Tag </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-field-values name="field-name" sortby="none/values/counts/results" max-items="XX"&gt; ...  &lt;/search-field-values&gt; </span> </p> </td> 
   <td colname="col2"> <p>Questo tag crea un ciclo per l’enumerazione dei valori dei campi e dei dati correlati per un particolare campo nell’intero set di risultati. Non nidificare questo tag all’interno di un altro tag <span class="codeph"> &lt;search-field-values&gt; </span> . L'attributo "name" specifica il nome del campo contenente i valori da enumerare. L’attributo "sortby" facoltativo controlla l’ordine di enumerazione: "nessuno" significa nessun ordine particolare, "valori" significa ordinamento per valori di campo (in ordine crescente o decrescente in base alla proprietà Ordinamento del campo), sortby="conteggi" significa ordinamento in ordine decrescente dei conteggi dei valori dei campi e sortby="results" significa ordinamento in ordine decrescente del numero di risultati contenenti ciascun valore. </p> <p>Sortby="conteggi" e sortby="risultati" sono equivalenti per i campi non di tipo elenco. . L’attributo opzionale "max-items" limita il numero di iterazioni al valore specificato. Il valore predefinito per "max-items" è -1, il che significa "enumerare tutti i valori". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-field-value date-format="date-format-string" encoding="html/javascript/json/perl/url/none" gmt="yes/no" language="0/language-id"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Questo tag restituisce il valore del campo per l'iterazione del ciclo &lt;search-field-values&gt; corrente. Questo tag è valido solo all'interno di un ciclo <span class="codeph"> &lt;search-field-values&gt; </span> . Gli attributi "date-format", "gmt" e "language" sono rilevanti solo se il tipo di contenuto del nome del campo specificato nel tag &lt;search-field-values&gt; che racchiude i valori &lt;search-field-values&gt; è "date". L'attributo "formato data" utilizza una stringa in formato data stile UNIX come "%A, %B %d, %Y" (per "lunedì 25 luglio 2020"). </p> <p>Vedere <a href="../c-appendices/c-templates.md#section_4BBDBBEF2B96414497617CD4B52D96E4" type="section" format="dita" scope="local"> Stringhe del formato della data</a>. </p> <p>L’attributo "encoding" facoltativo controlla se i caratteri della stringa di output sono codificati in HTML, codificati JavaScript, codificati Perl, codificati o meno nell’URL, per l’output sulla pagina dei risultati. Il valore predefinito di "encoding" è "none". Normalmente, non è necessario specificare l'attributo di codifica. Per impostazione predefinita, "gmt" viene impostato su "yes" e controlla se la parte dell’ora della stringa di data deve essere restituita in GMT ("yes") o nel fuso orario dell’account ("no"). L’attributo "language" controlla le convenzioni relative alla lingua e alle impostazioni internazionali della stringa della data di output. "0" (impostazione predefinita) significa "Usa lingua account". Qualsiasi altro valore "language" viene interpretato come un identificatore specifico della lingua, ad esempio, "en_US" significa "Inglese (Stati Uniti)". </p> <p>Consultare <a href="../c-appendices/c-templates.md#section_0490DECC00E34691ADE5A9ED90A6D911" type="section" format="dita" scope="local"> Identificatori di lingua</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-field-value-count results="yes/no"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Questo tag genera il conteggio associato all'iterazione del ciclo <span class="codeph"> </span> &lt;search-field-values&gt;  corrente. Il conteggio di output è il numero di risultati nell'intero set di risultati contenente il valore del campo (result="yes"), oppure il conteggio totale del valore del campo nell'intero set di risultati. Il valore predefinito di "results" è "no". </p> <p>Per i campi non di tipo elenco, result="yes" e results="no" sono equivalenti. Questo tag è valido solo all'interno di un ciclo <span class="codeph"> &lt;search-field-values&gt; </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-field-value-counter&gt; </span> </p> </td> 
   <td colname="col2"> <p>Questo tag genera il contatore ordinale per l'iterazione del ciclo <span class="codeph"> &lt;search-field-values&gt; </span> corrente. Questo tag è valido solo all'interno di un ciclo <span class="codeph"> &lt;search-field-values&gt; </span> . </p> </td> 
  </tr> 
 </tbody> 
</table>

## Suggerisci tag {#section_C28EB8B4F7DC4E278A0F143BCFEEB1AC}

Suggest fornisce un user friendly &quot;Intende?&quot; servizio per suggerire termini di ricerca alternativi. Se un utente ha digitato erroneamente un termine di ricerca, ad esempio, Suggerisci può aiutare l’utente a trovare i risultati suggerendo un’ortografia corretta. Il sistema può anche suggerire parole chiave correlate che possono aiutare un utente a scoprire i risultati. Durante la generazione dei suggerimenti, il servizio Suggerisci utilizza due dizionari: uno basato sulla lingua dell&#39;account (impostato in **[!UICONTROL Indexing]** > **[!UICONTROL Words and Languages]** > **[!UICONTROL Language]**) e l&#39;altro che è generato in modo univoco dalle parole chiave nell&#39;indice dell&#39;account.

>[!NOTE]
>
>Il servizio Suggerisci non funziona per cinese, giapponese o coreano.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Tag </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-suggestions&gt; ...  &lt;/search-if-suggestions&gt; </span> </p> </td> 
   <td colname="col2"> <p>Racchiudi questi tag con qualsiasi tag modello "Suggerisci", ad esempio <span class="codeph"> &lt;search-sugal&gt; </span>, <span class="codeph"> &lt;search-suggestione-link&gt; </span> e così via. Se la ricerca genera suggerimenti, il motore di ricerca genera ed elabora tutti gli elementi tra il tag aperto e quello chiuso. Se la ricerca non genera suggerimenti, non viene emesso alcun contenuto nidificato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-suggestions&gt; ...  &lt;/search-suggestions&gt; </span> </p> </td> 
   <td colname="col2"> <p>Questo tag genera il ciclo "Suggerisci", che contiene un elenco di termini di ricerca suggeriti (ad esempio, "intendete", "intenzionale" e "intende", per una query originariamente inserita come "intendds"). Quando si genera l’elenco di termini, il motore di ricerca ripete tutti i tag HTML e/o modello nidificati fino a cinque volte, che è il numero massimo di suggerimenti. Utilizza l’attributo count per specificare il numero di suggerimenti generati (tra 0 e 5). </p> <p>Il tag <span class="codeph"> &lt;search-suggestione&gt; </span> può essere visualizzato più volte sulla pagina per ripetere l’elenco di suggerimenti. I suggerimenti multipli vengono ordinati in base al numero di risultati ottenuti. </p> <p>Nidifica il tag <span class="codeph"> &lt;search-Sugers&gt; </span> tra i tag aperti e chiusi <span class="codeph"> &lt;search-if-sugg&gt; </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-suggestion-link&gt; ...  &lt;/search-suggestion-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Questo tag genera un collegamento alla query di ricerca originale utilizzando il termine di ricerca suggerito selezionato invece del termine originale. Il tag accetta e stampa semplicemente qualsiasi attributo HTML, ad esempio classe, destinazione e stile. Il tag può anche accettare un attributo URL, il cui valore è utilizzato come URL di base per il collegamento generato. I tag possono essere visualizzati solo all'interno del ciclo <span class="codeph"> &lt;search-suggerimenti&gt; </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-suggestion-text /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Questo tag stampa il termine di query attualmente suggerito (ad esempio, "intendete" per una query originariamente inserita come "intendds"). Il tag non ha attributi e può essere visualizzato solo all'interno del ciclo <span class="codeph"> &lt;search-suggerimenti&gt; </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-not-suggestions&gt; ...  &lt;/search-if-not-suggestions&gt; </span> </p> </td> 
   <td colname="col2"> <p>Se la ricerca non genera alcun suggerimento, il motore di ricerca genera ed elabora tutti gli elementi tra il tag aperto e quello chiuso. Se la ricerca genera suggerimenti, non viene emesso alcun contenuto nidificato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if&gt; ...  &lt;/search-if&gt; </span> </p> </td> 
   <td colname="col2"> <p>Questi tag condizionali includono l'HTML tra di loro in base al fatto che il termine suggerito sia il primo termine nel ciclo Suggerisci . I tag devono essere visualizzati tra i tag <span class="codeph"> &lt;search-sugal&gt; </span> aperti e chiusi. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if&gt; ...  &lt;/search-if&gt; </span> </p> </td> 
   <td colname="col2"> <p>Questi tag condizionali includono l'HTML tra di loro in base al fatto che il termine suggerito sia o meno l'ultimo termine nel ciclo Suggerisci . I tag devono essere visualizzati tra i tag <span class="codeph"> &lt;search-sugal&gt; </span> aperti e chiusi. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-suggestion-index&gt; </span> </p> </td> 
   <td colname="col2"> <p>Questo tag restituisce l'indice numerico del termine di ricerca suggerito corrente. Il tag deve essere visualizzato tra i tag <span class="codeph"> &lt;search-sugal&gt; </span> aperti e chiusi. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-suggestion-total&gt; </span> </p> </td> 
   <td colname="col2"> <p>Questo tag restituisce il numero totale di termini di ricerca suggeriti generati. Il tag deve essere visualizzato tra i tag <span class="codeph"> &lt;search-sugal&gt; </span> aperti e chiusi. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-suggestion-result-count&gt; </span> </p> </td> 
   <td colname="col2"> <p>Questo tag restituisce il numero totale di risultati per il termine di ricerca suggerito. Il tag deve essere visualizzato tra i tag <span class="codeph"> &lt;search-sugal&gt; </span> aperti e chiusi. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Tag stringa modello {#section_67E3D529661F4F03A1FF469D9D658CAF}

I tag seguenti producono una stringa nell&#39;HTML in quel punto del modello.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Tag </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-body&gt; </span> </p> </td> 
   <td colname="col2"> <p>Tag HTML body con le impostazioni di colore dei collegamenti di ricerca impostate dalla sezione Look base sotto il collegamento Modello. Aggiungi un attributo di sfondo a questo tag per visualizzare le immagini di sfondo nella pagina dei risultati. Qualsiasi attributo di colore aggiunto al tag sovrascrive le impostazioni di Colore collegamento ricerca impostate nella sezione Aspetto di base. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-header&gt; </span> </p> </td> 
   <td colname="col2"> <p>L’HTML per l’intestazione dei risultati di ricerca, come impostato nella sezione Aspetto di base, sotto il collegamento Modello. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-cdata&gt; ...  &lt;/search-cdata&gt; </span> </p> </td> 
   <td colname="col2"> <p>I tag dei dati di ricerca vengono sostituiti con i rispettivi equivalenti XML: <span class="codeph"> &lt;search-data&gt; </span> è sostituito da <span class="codeph"> &lt;![CDATA[" e il tag &lt;/search-data&gt; </span> è sostituito da " <span class="codeph"> ]]&gt; </span>". Un parser XML non analizza alcuna informazione tra il tag open e close. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-query query-number="XX" encoding="html/javascript/json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Query inserita dal visitatore. L'attributo "numero-query" avanzato e facoltativo controlla quale stringa di query numerata viene generata da questo tag. Ad esempio, <span class="codeph"> &lt;search-query query-number=1&gt; </span> restituisce il contenuto del parametro cgi <span class="codeph"> sp_q_1 </span> . Se non si specifica "numero-query" o se il numero-query è "0", viene generata la query principale ( <span class="codeph"> sp_q </span>). L’attributo opzionale "encoding" controlla se l’output è codificato in HTML, codificato JavaScript, codificato in Perl, codificato o meno nell’URL, per l’output sulla pagina dei risultati. Il valore predefinito di "encoding" è "html". Normalmente, non è necessario specificare l'attributo di codifica. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-total&gt; </span> </p> </td> 
   <td colname="col2"> <p>Totale dei risultati della ricerca. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-count&gt; </span> </p> </td> 
   <td colname="col2"> <p>Il conteggio dei risultati segnalati per questa pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-lower&gt; </span> </p> </td> 
   <td colname="col2"> <p>Numero del primo risultato segnalato per questa pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-upper&gt; </span> </p> </td> 
   <td colname="col2"> <p>Il numero dell'ultimo risultato segnalato per questa pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-prev-count&gt; </span> </p> </td> 
   <td colname="col2"> <p>Il numero di risultati segnalati per la pagina precedente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-next-count&gt; </span> </p> </td> 
   <td colname="col2"> <p>Il numero di risultati segnalati per la pagina successiva. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>11 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-time&gt; </span> </p> </td> 
   <td colname="col2"> <p>Tempo in secondi per la ricerca. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>12 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-logo&gt; </span> </p> </td> 
   <td colname="col2"> <p>L’HTML del logo Ricerca configurato per l’account, se presente. Questo logo è l'immagine che attribuisce credito alla ricerca/merchandising del sito </p> <p>Al momento la maggior parte degli account non dispone di un logo Ricerca associato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>13 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-collection all="name"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Raccolta dei risultati della ricerca. L’attributo opzionale "all" viene utilizzato per indicare il nome della raccolta che rappresenta l’intero sito web. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>14 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-form&gt; ...&lt;/search-form&gt; </span> </p> </td> 
   <td colname="col2"> <p>Inserisce i tag modulo iniziale e finale. Inserisce gli attributi del metodo e dell’azione nel tag modulo iniziale. Accetta attributi aggiuntivi, tra cui l’attributo dir="RTL" per il linguaggio e gli attributi "name" e "onSubmit" relativi a JavaScript. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>15 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-input-account&gt; </span> </p> </td> 
   <td colname="col2"> <p>Inserisce un tag di input del modulo che specifica il numero di account. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>16 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-input-gallery&gt; </span> </p> </td> 
   <td colname="col2"> <p>Inserisce un tag di input del modulo che specifica il numero della raccolta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>17 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-input-query query-number="XX"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Inserisce un tag di input del modulo che specifica la stringa di interrogazione. L’attributo "numero query" avanzato e facoltativo controlla quale query numerata viene utilizzata per il tag di input del modulo. Ad esempio, <span class="codeph"> &lt;search-input-query query query-number=1&gt; </span> restituisce un tag di input del modulo per la query <span class="codeph"> sp_q_1 </span>. Se non viene specificato "numero-query" o se "numero-query" è "0", viene inserito un tag di input per la query <span class="codeph"> sp_q </span> principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>18 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-input-collections all="name"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Inserisce un tag di selezione modulo e un codice HTML associato che visualizza il menu di selezione delle raccolte. L’attributo opzionale "all" viene utilizzato per indicare il nome della raccolta che rappresenta l’intero sito web. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>19 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-lt&gt; </span> </p> </td> 
   <td colname="col2"> <p>Inserisce l’output da uno dei tag modello di ricerca all’interno di altri tag HTML o modello nella pagina dei risultati. <span class="codeph"> &lt;search-lt&gt; </span> inserisce un carattere minore di . L’utilizzo di <span class="codeph"> &lt;search-lt&gt; </span> e <span class="codeph"> &lt;search-gt&gt; </span> offre un modo per sfuggire alla definizione di un tag in modo da poter utilizzare i tag dei modelli di ricerca come valori di attributo. Quando viene eseguito il rendering del modello in risposta a una ricerca, un segno di minore (&lt;) sostituisce il tag <span class="codeph"> &lt;search-lt&gt; </span> . Ad esempio, <span class="codeph"> &lt;search-link&gt; </span> equivale a <span class="codeph"> &lt;search-lt&gt;a href="&lt;search-url&gt;"&lt;search-gt&gt; </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>20 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-gt&gt; </span> </p> </td> 
   <td colname="col2"> <p>Inserisce l’output da uno dei tag modello di ricerca all’interno di altri tag HTML o modello nella pagina dei risultati. <span class="codeph"> &lt;search-gt&gt; </span> inserisce un carattere maggiore di . L’utilizzo di <span class="codeph"> &lt;search-lt&gt; </span> e <span class="codeph"> &lt;search-gt&gt; </span> offre un modo per sfuggire alla definizione di un tag in modo da poter utilizzare altri tag modello come valori di attributo. Quando viene eseguito il rendering del modello in risposta a una ricerca, un segno di maggiore (&gt;) sostituisce il tag <span class="codeph"> &lt;search-gt&gt; </span> . Ad esempio, <span class="codeph"> &lt;search-link&gt; </span> equivale a <span class="codeph"> &lt;search-lt&gt;a href="&lt;search-url&gt;"&lt;search-gt&gt; </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>21 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-param name="param-name" length="XX" encoding="html/javascript/json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Restituisce il valore del parametro cgi denominato "param-name" dalla richiesta di ricerca corrente. L’attributo opzionale "encoding" controlla se l’output è codificato in HTML, codificato JavaScript, codificato in Perl, codificato o meno nell’URL, per l’output sulla pagina dei risultati. Il valore predefinito di "encoding" è "html". Normalmente, non è necessario specificare l'attributo di codifica. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>22 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW for S&P 8.17.0 release on October 30 2014--> <span class="codeph"> &lt;search-trace encoding="html/javascript/ json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> 
    <!--<p>This global core search template tag outputs a representation of the submitted core search query, including any "fuzzy-search" query term expansions that happen by way of synonyms, sound-alikes, and so forth. </p>--> <p>L'attributo <span class="codeph"> encoding </span> è facoltativo; il valore predefinito è <span class="codeph"> json </span>. </p> <p> <p>Nota:  Questo tag ha output solo se <span class="codeph"> sp_trace=1 </span> è specificato con i parametri della query di ricerca di base. </p> </p> <p>Vedi la riga 48 nella tabella riportata in <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" format="dita" scope="local"> Parametri CGI di ricerca back-end</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Tag di collegamento di ancoraggio modello {#section_3A51D27616C541E2B818CC52B2B856BA}

Di seguito sono riportati i tag che consentono a un collegamento di ancoraggio di racchiudere l’HTML tra di loro. Quando fai clic su , il collegamento di ancoraggio richiede la visualizzazione di un’altra pagina di risultati. Il &quot;conteggio&quot; facoltativo dell’attributo richiede la visualizzazione di molti risultati nella pagina. Se non viene specificato, viene utilizzato il conteggio richiesto nella pagina corrente. L’attributo &quot;URL&quot; avanzato e facoltativo controlla il dominio a cui è diretto il collegamento associato. Per impostazione predefinita il dominio è `https://search.atomz.com/search/`, ma puoi modificarlo utilizzando l’attributo URL.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Tag </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-next URL="https://search.yourdomain.com/search/"&gt; ...  &lt;/search-next&gt; </span> </p> <p> <span class="codeph"> &lt;search-prev URL="https://search.yourdomain.com/search/"&gt; ...  &lt;/search-prev&gt; </span> </p> </td> 
   <td colname="col2"> <p>Visualizza la pagina successiva o precedente dei risultati. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-sort-by-date URL="https://search.yourdomain.com/search/"&gt; ...  &lt;/search-sort-by-date&gt; </span> </p> <p> <span class="codeph"> &lt;search-sort-by-score URL="https://search.yourdomain.com/search/"&gt; ...  &lt;/search-sort-by-score&gt; </span> </p> </td> 
   <td colname="col2"> <p>Ordina i risultati per data o per rilevanza. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-show-summaries URL="https://search.yourdomain.com/search/"&gt; ...  &lt;/search-show-summaries&gt; </span> </p> <p> <span class="codeph"> &lt;search-hide-summaries URL="https://search.yourdomain.com/search/"&gt; ...  &lt;/search-hide-summaries&gt; </span> </p> </td> 
   <td colname="col2"> <p>Mostra o nasconde i riepiloghi. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Tag condizionali del modello {#section_18D9BC66DE484881932FD2F7EA9D170D}

Tag che consentono di includere tra di essi un HTML condizionale.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Tag </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-results&gt; ...  &lt;/search-if-results&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-results&gt; ...&lt;/search-if-not-results&gt; </span> </p> </td> 
   <td colname="col2"> <p>Questi tag includono HTML se la pagina corrente contiene risultati di ricerca (o no). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-prev-count&gt; ...  &lt;/search-if-prev-count&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-prev-count&gt; ...  &lt;/search-if-not-prev-count&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-next-count&gt; ...  &lt;/search-if-next-count&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-next-count&gt; ...  &lt;/search-if-not-next-count&gt; </span> </p> </td> 
   <td colname="col2"> <p>Questi tag includono l’HTML se alla pagina precedente o a quella successiva sono associati dei risultati (o nessuno). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-sort-by-score&gt; ...  &lt;/search-if-sort-by-score&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-sort-by-score&gt; ...  &lt;/search-if-not-sort-by-score&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-sort-by-date&gt; ...  &lt;/search-if-sort-by-date&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-sort-by-date&gt; ...  &lt;/search-if-not-sort-by-date&gt; </span> </p> </td> 
   <td colname="col2"> <p>Questi tag includono HTML se la pagina corrente è o non è ordinata per rilevanza o per data. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-show-summaries&gt; ...  &lt;/search-if-show-summaries&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-hide-summaries&gt; ...  &lt;/search-if-hide-summaries&gt; </span> </p> </td> 
   <td colname="col2"> <p>Questi tag includono HTML se la pagina corrente mostra o nasconde i riepiloghi. Puoi utilizzare questi tag per includere o escludere qualsiasi parte del risultato della ricerca. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-input-collections&gt; ...  &lt;/search-if-input-collections&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-input-collections&gt; ...  &lt;/search-if-not-input-collections&gt; </span> </p> </td> 
   <td colname="col2"> <p>Questi tag includono HTML se è stata specificata una raccolta nella generazione dei risultati di ricerca per la pagina corrente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-advanced&gt; ...  &lt;/search-if-advanced&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-advanced&gt; ...  &lt;/search-if-not-advanced&gt; </span> </p> </td> 
   <td colname="col2"> <p>Questi tag includono HTML se per la query di ricerca è stato specificato il parametro <span class="codeph"> sp_advanced=1 </span> CGI . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-bad-param name="parameter-name"&gt; ...  &lt;/search-if-bad-param&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-bad-param name="parameter-name"&gt; ...  &lt;/search-if-not-bad-param&gt; </span> </p> </td> 
   <td colname="col2"> <p>Questi tag includono o escludono l'HTML tra di loro se il parametro specificato non è valido o non è valido. </p> <p>Attualmente è supportato solo il parametro <span class="codeph"> sp_q_location[_#] </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-param name="param-name" value="param-value"&gt; ...  &lt;/search-if-param&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-param name="param-name" value="param-value"&gt; ...  &lt;/search-if-not-param&gt; </span> </p> </td> 
   <td colname="col2"> <p>Questi tag avanzati includono l’HTML tra di loro in base al fatto che il parametro CGI specificato nell’attributo "name" abbia il valore specificato nell’attributo "value". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-sort-by-field name="field-name"&gt; ...  &lt;/search-if-sort-by-field&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-sort-by-field name="field-name"&gt; ...  &lt;/search-if-not-sort-by-field&gt; </span> </p> </td> 
   <td colname="col2"> <p>Questi tag avanzati includono l’HTML tra di loro se la pagina corrente è o meno ordinata in base al nome del campo specificato. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Tag per il controllo dei moduli modello {#section_45AFC414ACA74825B72FEAA8456F8DD2}

Tag che consentono di controllare lo stato di selezione predefinito per le caselle di controllo, i pulsanti di scelta e le caselle di riepilogo all’interno di un `<form>` nel modello di ricerca.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Tag </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-input&gt; </span> </p> </td> 
   <td colname="col2"> <p>Utilizzato in un modello al posto di un tag <span class="codeph"> &lt;input&gt; </span> . Quando il tag viene scritto nel browser, la parola <span class="codeph"> input </span> sostituisce <span class="codeph"> search-input </span> e tutte le altre informazioni nel tag vengono inviate così come sono. Inoltre, se il <span class="codeph"> nome </span> specificato nel tag è elencato come parametro CGI e se il valore <span class="codeph"> </span> specificato nel tag è il valore di quel parametro CGI, alla fine del tag viene aggiunta la parola <span class="codeph"> selezionata </span>. In questo modo, è possibile impostare automaticamente lo stato predefinito del pulsante di scelta o della casella di controllo nel risultato della ricerca allo stesso modo della query corrente. </p> <p>Ad esempio, il codice HTML di una casella di controllo potrebbe avere un aspetto simile al seguente: </p> <p> <span class="codeph"> &lt;input type="checkbox" name="sp_w" value="exact"&gt;Nessuna corrispondenza audio-simile  </span> </p> <p>Il codice modello corrispondente per quella casella di controllo è il seguente: </p> <p> <span class="codeph"> &lt;search-input type="checkbox" name="sp_w" value="exact"&gt;Nessuna corrispondenza audio-simile  </span> </p> <p>Se la stringa del parametro CGI per la query contiene <span class="codeph"> sp_w=esatto </span>, il tag scritto nel browser con i risultati della ricerca sarà simile al seguente (la parola <span class="codeph"> selezionata </span> viene inserita alla fine del tag): </p> <p> <span class="codeph"> &lt;input type="checkbox" name="sp_w" value="exact" checked=""&gt;Nessuna corrispondenza audio-simile  </span> </p> <p>Se la stringa del parametro CGI per la query non contiene <span class="codeph"> sp_w=esatto </span>, il tag scritto nel browser con i risultati della ricerca sarà simile al seguente (la parola <span class="codeph"> selezionata </span> non è elencata nel tag ): </p> <p> <span class="codeph"> &lt;input type="checkbox" name="sp_w" value="exact"&gt;Nessuna corrispondenza audio-simile  </span> </p> <p>Il tag <span class="codeph"> &lt;search-input&gt; </span> è utile per inserire caselle di controllo e pulsanti di scelta nel modello di ricerca. Se nel modello di ricerca sono presenti caselle di controllo o pulsanti di scelta che si desidera aggiungere a <span class="codeph"> &lt;form&gt; </span>, utilizzare <span class="codeph"> &lt;search-input...&gt; </span> al posto di <span class="codeph"> &lt;input..&gt; </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-select&gt; ...  &lt;/search-select&gt; </span> </p> <p> <span class="codeph"> &lt;search-option&gt; ...  &lt;/search-option&gt; </span> </p> </td> 
   <td colname="col2"> <p>Le caselle di riepilogo a discesa in un tag <span class="codeph"> &lt;form&gt; </span> iniziano con un tag <span class="codeph"> &lt;select&gt; </span> e terminano con un tag <span class="codeph"> &lt;/select&gt; </span> . Il nome <span class="codeph"> </span> per il parametro CGI associato è elencato all'interno del tag <span class="codeph"> &lt;select&gt; </span> . Dopo il tag <span class="codeph"> &lt;select&gt; </span> è riportato un elenco di tag <span class="codeph"> &lt;option&gt; </span> che specificano i valori da visualizzare all’interno della casella di riepilogo. </p> <p>I tag <span class="codeph"> &lt;search-select&gt; </span>, <span class="codeph"> &lt;/search-select&gt; </span>, <span class="codeph"> &lt;search-option&gt; </span> e <span class="codeph"> &lt;/search-option&gt; </span> forniscono funzionalità simili al tag <span class="codeph"> &lt;search-input&gt; </span> . In altre parole, la parola <span class="codeph"> selezionata </span> viene aggiunta automaticamente alla fine del tag <span class="codeph"> &lt;option&gt; </span> inviato al browser se il <span class="codeph"> nome </span> nel tag <span class="codeph"> &lt;search-select&gt; </span> è elencato come parametro CGI e se il <span class="codeph"> valore </span> di tale parametro CGI è elencato come valore <span class="codeph"> </span> in un tag specifico <span class="codeph"> &lt;search-option&gt; </span> . In questo modo, è possibile impostare automaticamente la scelta predefinita della casella di riepilogo nel risultato della ricerca come la query corrente. </p> <p>Ad esempio, una casella di riepilogo tipica avrà un aspetto simile al seguente: </p> <p> <code class="syntax html"> &lt;select&nbsp;name="sp_x"&nbsp;size=1&gt; 
      &lt;option&nbsp;value="any"&nbsp;selected&gt;Anywhere&lt;/option&gt; 
      &lt;option&nbsp;value="title"&gt;Title&lt;/option&gt; 
      &lt;option&nbsp;value="desc"&gt;Description&lt;/option&gt; 
      &lt;option&nbsp;value="keys"&gt;Keywords&lt;/option&gt; 
      &lt;option&nbsp;value="body"&gt;Body&lt;/option&gt; 
      &lt;option&nbsp;value="alt"&gt;Alternate&nbsp;text&lt;/option&gt; 
      &lt;option&nbsp;value="url"&gt;URL&lt;/option&gt; 
      &lt;option&nbsp;value="target"&gt;Target&lt;/option&gt; 
      &lt;/select&gt; </code> </p> <p>Il codice modello corrispondente per la casella di riepilogo è il seguente: </p> <p> <code class="syntax html"> &lt;search-select&nbsp;name="sp_x"&nbsp;size=1&gt; 
      &lt;search-option&nbsp;value="any"&gt;Anywhere&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="title"&gt;Title&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="desc"&gt;Description&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="keys"&gt;Keywords&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="body"&gt;Body&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="alt"&gt;Alternate&nbsp;text&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="url"&gt;URL&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="target"&gt;Target&lt;/search-option&gt; 
      &lt;/search-select&gt; </code> </p> <p>Se nel modello di ricerca sono presenti caselle di riepilogo da aggiungere a <span class="codeph"> &lt;form&gt; </span>, utilizzare <span class="codeph"> &lt;search-select...&gt; </span> al posto di <span class="codeph"> &lt;select...&gt; </span>, <span class="codeph"> &lt;/search-select&gt; </span> al posto di <span class="codeph"> &lt;/select&gt; </span>/&gt;, <span class="codeph"> &lt;search-option..&gt; </span> al posto di <span class="codeph"> &lt;option..&gt; </span> e <span class="codeph"> &lt;/search-option&gt; </span> al posto di <span class="codeph"> &lt;/option&gt; </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-sort-by-field name="field-name" count="XX"&gt; ...  &lt;/search-sort-by-field&gt; </span> </p> </td> 
   <td colname="col2"> <p>Questi tag avanzati creano un collegamento di ancoraggio intorno all’HTML che li circonda. Quando fai clic su questo ancoraggio, viene visualizzata una pagina di risultati ordinati nel campo specificato. L'attributo <span class="codeph"> count </span> facoltativo specifica il numero di risultati da visualizzare nella pagina dei risultati. Se viene omesso il conteggio <span class="codeph"> </span>, viene utilizzato il conteggio utilizzato nella pagina corrente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Stringhe del formato della data {#section_4BBDBBEF2B96414497617CD4B52D96E4}

È possibile utilizzare le seguenti specifiche di conversione nelle stringhe di formato data:

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Stringa formato data </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>%A </p> </td> 
   <td colname="col2"> <p> Corrisponde alla rappresentazione nazionale del nome completo del giorno feriale, ad esempio "Lunedì". L'impostazione in <span class="uicontrol"> LinguStatistics </span> &gt; <span class="uicontrol"> Words &amp; Languages </span> &gt; <span class="uicontrol"> Language </span> determina la rappresentazione nazionale. </p> <p>Consulta <a href="../c-about-linguistics-menu/c-about-words-and-language.md#concept_CEB4B9576F3C4E2EB87B352EEC738D79" type="concept" format="dita" scope="local"> Informazioni su parole e lingua</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%a </p> </td> 
   <td colname="col2"> <p> Corrisponde alla rappresentazione nazionale del nome abbreviato del giorno feriale, dove l'abbreviazione è costituita dai primi tre caratteri, ad esempio "Luna". L'impostazione in <span class="uicontrol"> LinguStatistics </span> &gt; <span class="uicontrol"> Words &amp; Languages </span> &gt; <span class="uicontrol"> Language </span> determina la rappresentazione nazionale. </p> <p>Consulta <a href="../c-about-linguistics-menu/c-about-words-and-language.md#concept_CEB4B9576F3C4E2EB87B352EEC738D79" type="concept" format="dita" scope="local"> Informazioni su parole e lingua</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%B </p> </td> 
   <td colname="col2"> <p> Corrisponde alla rappresentazione nazionale del nome completo del mese, ad esempio "Giugno". L'impostazione in <span class="uicontrol"> LinguStatistics </span> &gt; <span class="uicontrol"> Words &amp; Languages </span> &gt; <span class="uicontrol"> Language </span> determina la rappresentazione nazionale. </p> <p>Consulta <a href="../c-about-linguistics-menu/c-about-words-and-language.md#concept_CEB4B9576F3C4E2EB87B352EEC738D79" type="concept" format="dita" scope="local"> Informazioni su parole e lingua</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%b </p> </td> 
   <td colname="col2"> <p> Corrisponde alla rappresentazione nazionale del nome del mese abbreviato, dove l'abbreviazione è i primi tre caratteri, ad esempio "Giu". L'impostazione in <span class="uicontrol"> LinguStatistics </span> &gt; <span class="uicontrol"> Words &amp; Languages </span> &gt; <span class="uicontrol"> Language </span> determina la rappresentazione nazionale. </p> <p>Consulta <a href="../c-about-linguistics-menu/c-about-words-and-language.md#concept_CEB4B9576F3C4E2EB87B352EEC738D79" type="concept" format="dita" scope="local"> Informazioni su parole e lingua</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%D </p> </td> 
   <td colname="col2"> <p>Equivalente a "%m/%d/%y", ad esempio "07/25/13". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%d </p> </td> 
   <td colname="col2"> <p> Corrisponde al giorno del mese come numero decimale (01-31). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%e </p> </td> 
   <td colname="col2"> <p> Corrisponde al giorno del mese come numero decimale (1-31). Un valore vuoto precede le singole cifre. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%H </p> </td> 
   <td colname="col2"> <p> Corrisponde all’orologio da 24 ore come numero decimale (00-23). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%h </p> </td> 
   <td colname="col2"> <p> Corrisponde alla rappresentazione nazionale del nome del mese abbreviato, dove l'abbreviazione è costituita dai primi tre caratteri, ad esempio "Jun" (uguale a %b). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%I </p> </td> 
   <td colname="col2"> <p> Corrisponde all’orologio da 12 ore come numero decimale (01-12). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%j </p> </td> 
   <td colname="col2"> <p> Corrisponde al giorno dell’anno come numero decimale (001-366). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%k </p> </td> 
   <td colname="col2"> <p> Corrisponde al (24 ore come numero decimale (0-23). Un valore vuoto precede le singole cifre. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%l </p> </td> 
   <td colname="col2"> <p> Corrisponde all’ora 12 ore di orologio come numero decimale (1-12). Un valore vuoto precede le singole cifre. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%M </p> </td> 
   <td colname="col2"> <p> Corrisponde al minuto come numero decimale (00-59). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%m </p> </td> 
   <td colname="col2"> <p> Corrisponde al mese come numero decimale (01-12). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%p </p> </td> 
   <td colname="col2"> <p> Corrisponde alla rappresentazione nazionale di "ante meridiem" o "post meridiem" a seconda dei casi, ad esempio "PM". L'impostazione in <span class="uicontrol"> LinguStatistics </span> &gt; <span class="uicontrol"> Words &amp; Languages </span> &gt; <span class="uicontrol"> Language </span> determina la rappresentazione nazionale. </p> <p>Consulta <a href="../c-about-linguistics-menu/c-about-words-and-language.md#concept_CEB4B9576F3C4E2EB87B352EEC738D79" type="concept" format="dita" scope="local"> Informazioni su parole e lingua</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%R </p> </td> 
   <td colname="col2"> <p>Equivalente a "%H:%M", ad esempio, "13:23". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%r </p> </td> 
   <td colname="col2"> <p>Equivalente a "%I:%M:%S %p", ad esempio, "01:23:45 PM". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%S </p> </td> 
   <td colname="col2"> <p> Corrisponde al secondo come numero decimale (00-60). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%T </p> </td> 
   <td colname="col2"> <p>Equivalente a "%H:%M:%S", ad esempio, "13:26:47". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%U </p> </td> 
   <td colname="col2"> <p> Corrisponde al numero della settimana dell’anno (domenica come primo giorno della settimana) come numero decimale (00-53). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%v </p> </td> 
   <td colname="col2"> <p>Equivalente a "%e-%b-%Y", ad esempio, "25-lug-2013". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%Y </p> </td> 
   <td colname="col2"> <p> Corrisponde all’anno con un numero decimale, ad esempio "2013". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%y </p> </td> 
   <td colname="col2"> <p> Corrisponde all'anno senza secolo come numero decimale (00-99). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%Z </p> </td> 
   <td colname="col2"> <p> Corrisponde al nome del fuso orario. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>% </p> </td> 
   <td colname="col2"> <p> Corrisponde a "%". </p> </td> 
  </tr> 
 </tbody> 
</table>

## Identificatori di lingua {#section_0490DECC00E34691ADE5A9ED90A6D911}

La tabella seguente contiene gli identificatori della lingua per ogni lingua supportata. Puoi utilizzare questi identificatori come valori per l&#39;attributo opzionale &quot;language&quot; nei seguenti tag modello:

* `search-date` e `search-display-field`.

   Vedere [Tag della stringa del ciclo di risultati](../c-appendices/c-templates.md#section_80D68334E8D04A33937A6E58ABAAA320).

* `search-field-value-list` Consultare Tag dell’elenco dei valori dei  [campi](../c-appendices/c-templates.md#section_D3298B5F976447DBA0032B883DCC91B1).

* `search-field-value` Consultare Tag del ciclo di elenchi di valori  [dei campi](../c-appendices/c-templates.md#section_0717FA09F0FC449CB916883B0500A60E).

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Lingua </p> </th> 
   <th colname="col2" class="entry"> <p>Identificatore lingua </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Bulgaro (Bulgaria) </p> </td> 
   <td colname="col2"> <p> bg_BG </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Cinese (Cina) </p> </td> 
   <td colname="col2"> <p> zh_CN </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Cinese (Hong Kong) </p> </td> 
   <td colname="col2"> <p> zh_HK </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Cinese (Singapore) </p> </td> 
   <td colname="col2"> <p>zh_SG </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Cinese (Taiwan) </p> </td> 
   <td colname="col2"> <p> zh_TW </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Ceco (Repubblica ceca) </p> </td> 
   <td colname="col2"> <p> cs_CZ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Danese (Danimarca) </p> </td> 
   <td colname="col2"> <p> da_DK </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Olandese (Belgio) </p> </td> 
   <td colname="col2"> <p> nl_BE </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Olandese (Paesi Bassi) </p> </td> 
   <td colname="col2"> <p> nl_NL </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Inglese (Australia) </p> </td> 
   <td colname="col2"> <p> en_AU </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Inglese (Canada) </p> </td> 
   <td colname="col2"> <p> en_CA </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Inglese (Gran Bretagna) </p> </td> 
   <td colname="col2"> <p> en_GB </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Inglese (Stati Uniti) </p> </td> 
   <td colname="col2"> <p> en_US </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Francese (Belgio) </p> </td> 
   <td colname="col2"> <p> fr_BE </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Francese (Canada) </p> </td> 
   <td colname="col2"> <p>fr_CA </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Finlandese (Finlandia) </p> </td> 
   <td colname="col2"> <p> fi_FI </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Francese (Francia) </p> </td> 
   <td colname="col2"> <p> fr_FR </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Francese (Svizzera) </p> </td> 
   <td colname="col2"> <p> fr_CH </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Tedesco (Austria) </p> </td> 
   <td colname="col2"> <p> de_AT </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Tedesco (Germania) </p> </td> 
   <td colname="col2"> <p> de_DE </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Tedesco (Svizzera) </p> </td> 
   <td colname="col2"> <p> de_CH </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Greco (Grecia) </p> </td> 
   <td colname="col2"> <p> el_GR </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Gaelico irlandese (Irlanda) </p> </td> 
   <td colname="col2"> <p> ga_IE </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Italiano (Italia) </p> </td> 
   <td colname="col2"> <p> it_IT </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Giapponese (Giappone) </p> </td> 
   <td colname="col2"> <p> ja_JP </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Coreano (Corea) </p> </td> 
   <td colname="col2"> <p> ko_KR </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Norvegese (Norvegia) </p> </td> 
   <td colname="col2"> <p> no_NO </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Polacco (Polonia) </p> </td> 
   <td colname="col2"> <p> pl_PL </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Portoghese (Brasile) </p> </td> 
   <td colname="col2"> <p> pt_BR </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Portoghese (Portogallo) </p> </td> 
   <td colname="col2"> <p> pt_PT </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Russo (ex Unione Sovietica) </p> </td> 
   <td colname="col2"> <p> ru_SU </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Slovacco (Slovacchia) </p> </td> 
   <td colname="col2"> <p> sk_SK </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Slovacco (Slovenia) </p> </td> 
   <td colname="col2"> <p>sl_SI </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Spagnolo (Messico) </p> </td> 
   <td colname="col2"> <p> es_MX </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Spagnolo (Spagna) </p> </td> 
   <td colname="col2"> <p> es_ES </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Svedese (Svezia) </p> </td> 
   <td colname="col2"> <p> sv_SE </p> </td> 
  </tr> 
 </tbody> 
</table>

## Specifica dell&#39;intestazione HTTP del tipo di contenuto {#section_AEED823E9938448A9EDB2F286D9CFD90}

Puoi specificare l&#39;intestazione di risposta HTTP Content-Type utilizzando il seguente tag:

`<search-content-type-header [content="MIME-type"] [charset="charset-name"]>`

Gli attributi `content` e `charset` sono facoltativi. Questo tag deve essere visualizzato il prima possibile nel modello. Si consiglia inoltre di visualizzarlo prima di `<search-html-meta-charset>` o `<search-xml-decl>`, in quanto influisce sul comportamento di tali tag.

Se non si specifica l&#39;attributo `content`, il valore di `MIME-type` viene impostato automaticamente sul valore impostato in **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**. Se specifichi un attributo `content`, viene utilizzato come attributo predefinito `content` per il tag `<search-html-meta-charset>` .

Se non si specifica l&#39;attributo `charset`, nessun valore `charset` viene scritto nell&#39;intestazione `content-type`.

Se si specifica `charset="1"`, il valore effettivo per `charset-name` è il valore del parametro `sp_f` CGI. Se non viene inviato alcun parametro CGI `sp_f` con la ricerca, il valore effettivo per `charset-name` viene letto dalle impostazioni del tuo account. Puoi visualizzare o modificare il set di caratteri associato all’account in **[!UICONTROL Settings]** > **[!UICONTROL My Profile]** > **[!UICONTROL Personal Information]** > **[!UICONTROL Character Encoding]**.

Consulta [Configurazione delle informazioni utente personali](../c-about-settings-menu/c-about-my-profile-menu.md#task_A11A3BE2527B4204B896E04303B04AA6).

Puoi scegliere un nome specifico per il set di caratteri elencandolo come valore `charset`, ad esempio `charset="iso-8859-1"` o `charset="Shift-JIS"`.

Se si specifica un attributo `charset`, questo viene utilizzato come attributo predefinito `charset` per i tag `<search-html-meta-charset>` e `<search-xml-decl>`, nonché come output nell&#39;intestazione `content-type`.

## Specifica di un set di caratteri in un modello HTML {#section_E0D1816ABB5846BEBE9C26D5980CCBE6}

I modelli di risultati di ricerca HTML predefiniti specificano il set di caratteri associato all’account corrente tramite il seguente tag:

`<search-html-meta-charset [content="MIME-type"] [charset="charset-name"]>`

Gli attributi del contenuto e del set di caratteri sono facoltativi. Questo tag deve essere visualizzato nella sezione HTML `<head>` del modello. Questo tag genera il seguente tag nella pagina HTML generata dal modello:

`<meta http-equiv="content-type" content="MIME-type; charset=charset-name">`

Se non si specifica l’attributo di contenuto, il valore effettivo di `MIME-type` viene impostato automaticamente su uno dei due valori. Se il tag `<search-content-type-header>` ha specificato un attributo `content`, viene utilizzato tale valore. In caso contrario, il valore utilizzato è quello impostato nella scheda **[!UICONTROL Templates]** > **[!UICONTROL Settings]** > **[!UICONTROL Content Type]** .

Se non si specifica l&#39;attributo `charset` , il valore effettivo di `charset-name` viene impostato automaticamente su uno dei due valori. Se il tag `<search-content-type-header>` ha specificato un attributo `charset`, viene utilizzato tale valore. In caso contrario, il valore effettivo di `charset-name` viene letto dalle impostazioni del tuo account. Puoi visualizzare o modificare il set di caratteri associato all’account in **[!UICONTROL Settings]** > **[!UICONTROL My Profile]** > **[!UICONTROL Personal Information]** > **[!UICONTROL Character Encoding]**.

Consulta [Configurazione delle informazioni utente personali](../c-about-settings-menu/c-about-my-profile-menu.md#task_A11A3BE2527B4204B896E04303B04AA6).

Se si specifica `charset="1"`, il valore effettivo per `charset-name` è il valore del parametro `sp_f` CGI. Se non viene inviato alcun parametro CGI `sp_f` con la ricerca, il valore effettivo per `charset-name` è il valore impostato nel tag `<search-content-type-header>` se specificato oppure il valore impostato nelle impostazioni dell&#39;account.

È possibile specificare un nome specifico per il set di caratteri, come in `charset="charset-name"`. Ad esempio, `charset="iso-8859-1"` o `charset="Shift-JIS"`.

Il tag `<search-html-meta-charset>` è facoltativo. Se lo rimuovi, il browser assume i valori predefiniti per `content-type`, ovvero quanto segue: `content="text/html; charset=ISO-8859-1"`. Puoi anche scegliere di sostituire il tag `<search-html-meta-charset>` con il tag `http-equiv` personalizzato.

## Specifica di un set di caratteri in un modello XML {#section_17DC31CDCC104F5F8081466B41A96E9D}

Il modello di risultato della ricerca XML predefinito specifica il set di caratteri associato al conto corrente tramite il seguente tag:

`<search-xml-decl [charset="charset-name"]>`

L&#39;attributo `charset` è facoltativo. Questo tag deve essere visualizzato nella parte superiore del modello, ma dopo eventuali tag `<search-content-type-header>` . Questo tag determina il seguente tag nel documento XML generato dal modello:

`<?xml version="1.0" encoding="charset-name" standalone="yes" ?>`

Se non si specifica il valore `charset`, il valore effettivo di `charset-name` viene impostato automaticamente su uno dei due valori. Se `<search-content-type-header>` ha specificato un attributo `charset`, viene utilizzato tale valore. In caso contrario, il valore effettivo di `charset-name` viene letto dalle impostazioni del tuo account. Puoi visualizzare o modificare il set di caratteri associato all’account in **[!UICONTROL Settings]** > **[!UICONTROL My Profile]** > **[!UICONTROL Personal Information]** > **[!UICONTROL Character Encoding]**.

Consulta [Configurazione delle informazioni utente personali](../c-about-settings-menu/c-about-my-profile-menu.md#task_A11A3BE2527B4204B896E04303B04AA6).

Se si specifica `charset="1"`, il valore effettivo per `charset-name` è il valore del parametro `sp_f` CGI. Se non viene inviato alcun parametro CGI `sp_f` con la ricerca, il valore effettivo per `charset-name` è il valore impostato nel tag `<search-content-type-header>` se specificato oppure il valore impostato nelle impostazioni dell&#39;account.

Se lo desideri, puoi specificare un nome specifico per il set di caratteri, come in `charset="charset-name"`. Ad esempio, `charset="iso-8859-1" or charset="Shift-JIS"`.

Puoi scegliere di sostituire il tag `<search-xml-decl>` con il tag `?xml` personalizzato.

## Inclusione di un modello di ricerca in un altro {#section_7D1FCD3D9E2340C291E354C9720E8BC0}

Per includere un modello di ricerca in un altro, utilizza il tag `<search-include>` , impostando l’attributo di file sul nome del file modello che desideri includere come nell’esempio seguente:

`<search-include file="seo/seo_search_title.tpl" />`

I segmenti dei modelli di ricerca SEO si trovano nella sottocartella `seo/` e i normali modelli di ricerca si trovano nella sottocartella `templates/` . Solo i file .tpl sono significativi da includere in questo contesto.

## Gestione di più modelli di trasporto per il sito web {#reference_12AAB3B9F4C74C11956F1DBA95714C2F}

Puoi controllare l’aspetto dei risultati della ricerca nel sito web utilizzando diversi modelli di trasporto della ricerca per ogni area.

<!-- 

r_managing_multiple_templates.xml

 -->

Per eseguire questo tipo di funzionalità di ricerca, puoi gestire i modelli di trasporto in ricerca/merchandising sul sito. In alternativa, puoi gestire i modelli di trasporto in Pubblica. Come per la ricerca/merchandising del sito, l’opzione Pubblica consente di modificare, visualizzare in anteprima e pubblicare più modelli di trasporto di ricerca.

Per impostare i moduli di ricerca in modo che utilizzino un modello di trasporto specifico (diverso da quello predefinito), utilizzare il parametro di query `sp_t`. Ad esempio, supponiamo che tu abbia un modello di ricerca denominato &quot;autorizzazione&quot; per l’area vendite contrassegnata del tuo sito web. È possibile utilizzare il modulo di ricerca HTML standard con il seguente codice modulo aggiuntivo:

`<input type=hidden name="sp_t" value="clearance">`

Quando un cliente fa clic su un modulo standard che contiene questa riga di codice, viene visualizzato il modello di trasporto di ricerca &quot;libero&quot; insieme ai relativi risultati di ricerca.

Vedere [Uso delle raccolte nei moduli di ricerca](../c-appendices/c-searchforms.md#reference_5A079AEEEFB84457892EF0870D0605C3).

Vedere [Uso dei frame con forms](../c-appendices/c-searchforms.md#reference_82CDDDA1E37042E4849EBF7EA05407C5).

Consultare [Esempio di modulo di ricerca avanzato](../c-appendices/c-searchforms.md#reference_82E1051918744EBA88A01E9E6AE42C4A).
