---
description: Un aggiornamento della sintassi e delle regole per la costruzione di espressioni regolari.
solution: Target
title: Espressioni regolari
topic-legacy: Appendices,Site search and merchandising
uuid: 369b54f6-372a-41de-bb5d-3ae0bd640199
exl-id: 6deb9385-9b17-47c2-b6d9-b63f13df8399
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '1045'
ht-degree: 0%

---

# Espressioni regolari{#regular-expressions}

Un aggiornamento della sintassi e delle regole per la costruzione di espressioni regolari.

Vedi anche [Configurazione di un indice incrementale di un sito web organizzato](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

**Sintassi delle espressioni regolari**

<table> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <b>Testo</b> </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> <p>Qualsiasi carattere singolo </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> [caratteri] </p> </td> 
   <td colname="col3"> <p> Classe di caratteri: Uno dei caratteri </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> [^caratteri] </p> </td> 
   <td colname="col3"> <p>Classe di caratteri: Nessun carattere </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> text1|text2 </p> </td> 
   <td colname="col3"> <p> Alternativa: testo1 o testo2 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Quantificatori</b> </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> ? </p> </td> 
   <td colname="col3"> <p> 0 o 1 del testo precedente </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> * </p> </td> 
   <td colname="col3"> <p> 0 o N del testo precedente (N &gt; 1) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> + </p> </td> 
   <td colname="col3"> <p>1 o N del testo precedente (N &gt; 1) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Raggruppamento</b> </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> (testo) </p> </td> 
   <td colname="col3"> <p> Raggruppamento di testo, per impostare i bordi di un'alternativa o per restituire i riferimenti quando il nth gruppo viene utilizzato sull'RHS di una RewriteRule con $N) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Ancoraggi</b> </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> ^ </p> </td> 
   <td colname="col3"> <p> Inizio ancoraggio linea. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> $ </p> </td> 
   <td colname="col3"> <p> Ancoraggio fine linea. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Fuga</b> </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </p> </td> 
   <td colname="col2"> <p>\char </p> </td> 
   <td colname="col3"> <p>Scappa il carattere particolare. Ad esempio, per specificare i caratteri ".[]()" e così via. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Regole sulle espressioni regolari**

* Un carattere comune, non uno dei caratteri speciali descritti di seguito, è un&#39;espressione regolare a un carattere che corrisponde a se stessa.
* Una barra rovesciata (\) seguita da qualsiasi carattere speciale è un&#39;espressione regolare a un carattere che corrisponde al carattere speciale stesso. I caratteri speciali includono quanto segue:

   * `.` (punto),  `*` (asterisco),  `?` (punto interrogativo),  `+` (segno più),  `[` (parentesi quadra sinistra),  `|` (barra verticale) e  `\` (barra rovesciata) sono sempre caratteri speciali, tranne quando compaiono tra parentesi quadre.
   * `^` (accento circonflesso) è speciale all&#39;inizio di un&#39;espressione regolare, o quando segue immediatamente la sinistra di una coppia di parentesi quadre.
   * `$` (simbolo del dollaro) è speciale alla fine di un&#39;espressione regolare.
   * `.` (punto) è un&#39;espressione regolare a un carattere che corrisponde a qualsiasi carattere, inclusi i caratteri del set di codici supplementari ad eccezione di new-line.
   * Una stringa non vuota di caratteri racchiusi tra `[ ]` (parentesi quadre sinistra e destra) è un&#39;espressione regolare di un carattere che corrisponde a un carattere, inclusi i caratteri del set di codici supplementari, in quella stringa.

      Se, tuttavia, il primo carattere della stringa è un carattere `^` (cirflex), l&#39;espressione regolare a un carattere corrisponde a qualsiasi carattere, inclusi i caratteri del set di codici supplementari, ad eccezione di new-line e dei caratteri rimanenti nella stringa.

      Il `^` ha questo significato speciale solo se si verifica per primo nella stringa. È possibile utilizzare `-` (segno meno) per indicare un intervallo di caratteri consecutivi, inclusi i caratteri del set di codici supplementari. Ad esempio, [0-9] equivale a [0123456789].

      I caratteri che specificano l&#39;intervallo devono provenire dallo stesso set di codici. Quando i caratteri provengono da set di codice diversi, uno dei caratteri che specificano l’intervallo corrisponde. Il `-` perde questo significato speciale se si verifica per primo (dopo un `^` iniziale, se presente) o per ultimo nella stringa. La `]` (parentesi quadra destra) non termina una stringa di questo tipo quando si tratta del primo carattere al suo interno, dopo un `^` iniziale, se presente. Ad esempio, `[]a-f]` corrisponde a una `]` (parentesi quadra destra) o a una delle lettere ASCII da a a a f inclusive. I quattro caratteri elencati come caratteri speciali sopra si trovano all’interno di una stringa di caratteri di questo tipo.

**Regole per la costruzione di espressioni regolari da espressioni regolari con un carattere**

Puoi utilizzare le seguenti regole per creare espressioni regolari a partire da espressioni regolari a un carattere:

* Un&#39;espressione regolare con un carattere è un&#39;espressione regolare che corrisponde a qualsiasi tipo di corrispondenza dell&#39;espressione regolare con un carattere.
* Un&#39;espressione regolare a un carattere seguita da un `*` (asterisco) è un&#39;espressione regolare che corrisponde a zero o più occorrenze dell&#39;espressione regolare a un carattere, che può essere un carattere aggiuntivo del set di codici. In caso di scelta, viene scelta la stringa più a sinistra più lunga che consente una corrispondenza.
* Un&#39;espressione regolare a un carattere seguita da un `?` (punto interrogativo) è un&#39;espressione regolare che corrisponde a zero o a una occorrenza dell&#39;espressione regolare a un carattere, che può essere un carattere aggiuntivo del set di codici. In caso di scelta, viene scelta la stringa più a sinistra più lunga che consente una corrispondenza.
* Un&#39;espressione regolare a un carattere seguita da un `+` (segno più) è un&#39;espressione regolare che corrisponde a una o più occorrenze dell&#39;espressione regolare a un carattere, che può essere un carattere di set di codici supplementare. In caso di scelta, viene scelta la stringa più a sinistra più lunga che consente una corrispondenza.
* Un&#39;espressione regolare a un carattere seguita da `{m}`, `{m,}` o `{m,n}` è un&#39;espressione regolare che corrisponde a un intervallo di occorrenze dell&#39;espressione regolare a un carattere. i valori di m e n devono essere numeri interi non negativi inferiori a 256; `{m}` corrisponde esattamente a m occorrenze; `{m,}` corrisponde ad almeno m occorrenze; `{m,n}` corrisponde a qualsiasi numero di occorrenze tra m e n inclusive. Ogni volta che esiste una scelta, l&#39;espressione regolare corrisponde al maggior numero possibile di occorrenze.
* La concatenazione di espressioni regolari è un’espressione regolare che corrisponde alla concatenazione delle stringhe abbinate a ciascun componente dell’espressione regolare.
* Un&#39;espressione regolare racchiusa tra le sequenze di caratteri ( e ) è un&#39;espressione regolare che corrisponde a qualsiasi corrispondenza dell&#39;espressione regolare non adornata.
* Un&#39;espressione regolare seguita da una `|` (barra verticale) seguita da un&#39;espressione regolare è un&#39;espressione regolare che corrisponde alla prima espressione regolare (prima della barra verticale) o alla seconda espressione regolare (dopo la barra verticale).

Puoi anche vincolare un’espressione regolare affinché corrisponda solo a un segmento iniziale o finale di una riga, oppure a entrambi.

* Un `^` (circonflex) all&#39;inizio di un&#39;espressione regolare vincola tale espressione regolare affinché corrisponda a un segmento iniziale di una riga.
* Un `$` (simbolo del dollaro) alla fine di un&#39;intera espressione regolare vincola tale espressione regolare affinché corrisponda a un segmento finale di una riga.
* La costruzione ^espressione regolare$ vincola l&#39;espressione regolare affinché corrisponda all&#39;intera riga.

Esistono alcuni nomi di classe di caratteri predefiniti che è possibile utilizzare al posto di complesse espressioni regolari tra parentesi quadre. Ad esempio, una cifra può essere rappresentata dall&#39;espressione regolare a un carattere [0-9] o dall&#39;espressione regolare a un carattere della classe di caratteri [[:cifra:]].

Le classi di caratteri predefinite e il loro significato sono i seguenti:

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Classe carattere </p> </th> 
   <th colname="col2" class="entry"> <p>Significato </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> [[:alnum:]] </p> </td> 
   <td colname="col2"> <p> Un carattere alfabetico o una cifra. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:alpha:]] </p> </td> 
   <td colname="col2"> <p>Un carattere alfabetico. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:vuoto:]] </p> </td> 
   <td colname="col2"> <p>Uno spazio o una scheda. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:cntrl:]] </p> </td> 
   <td colname="col2"> <p> un codice di controllo; carattere non stampabile. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:cifra:]] </p> </td> 
   <td colname="col2"> <p>Una cifra. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:graph:]] </p> </td> 
   <td colname="col2"> <p> Qualsiasi carattere di stampa tranne lo spazio. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:lower:]] </p> </td> 
   <td colname="col2"> <p>Carattere alfabetico minuscolo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:print:]] </p> </td> 
   <td colname="col2"> <p> Qualsiasi carattere di stampa, compreso lo spazio. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:punct:]] </p> </td> 
   <td colname="col2"> <p> Punteggiatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:space:]] </p> </td> 
   <td colname="col2"> <p> Spazio vuoto, ad esempio uno spazio, una scheda o una fine riga. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:high:]] </p> </td> 
   <td colname="col2"> <p> Carattere alfabetico maiuscolo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:xcifra:]] </p> </td> 
   <td colname="col2"> <p> Una cifra esadecimale, maiuscola o minuscola. </p> </td> 
  </tr> 
 </tbody> 
</table>

Due nomi di classe di caratteri speciali corrispondono allo spazio null all&#39;inizio e alla fine di una parola. In altre parole, non corrispondono a un carattere effettivo. Una parola è considerata una qualsiasi sequenza di caratteri alfabetici, cifre o caratteri di sottolineatura (_).

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Classe carattere </p> </th> 
   <th colname="col2" class="entry"> <p>Significato </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> [[:&lt;:]] </p> </td> 
   <td colname="col2"> <p> inizio di una parola </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:&gt;:]] </p> </td> 
   <td colname="col2"> <p>fine di una parola </p> </td> 
  </tr> 
 </tbody> 
</table>
