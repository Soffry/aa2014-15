Argomenti:

1. riprendere le funzioni composte: modello di valutazione ad alberi -> visibilità delle variabili
2. riprendere i problemi proposti la settimana scorsa, ed introdurre i costrutti condizionali
3. varie ed eventuali 

#I costrutti condizionali

Finora si è visto come eseguire espressioni all'interno di una funzione utilizzando semplici operazioni aritmetiche (addizione, sottrazione, moltiplicazione e divisione rappresentate rispettivamente, nel linguaggio Python -e non solo-, dai simboli +, -, *, /), in modo che, assegnato un valore a un'incognita della funzione essa possa essere gestita all'interno dell'espressione, che "returnerà" il risultato della stessa.

Esempio [Python]

    def f(x):
       return (3*(x+2))/4

Spesso nella programmazione succede di trovarsi di fronte a un "bivio" a cui il programma deve porre una "scelta" di fronte a diverse "opzioni". Per esempio, per capire se un numero intero x è pari o dispari, con le conoscenze finora acquisite si potrebbe ricorrere a un'espressione. Essa restituirà come valori 0 se il numero immesso è pari, x se il numero immesso è dispari. Prima di procedere è bene introdurre un ulteriore operatore matematico: il modulo (simbolo %). Differentemente dal "omonimo" matematico |x|, il modulo informatico è un operatore che "returna"/restituisce il resto della divisione tra due numeri interi. Per esempio 4 % 2 restituirà il valore 0, in quanto il resto della divisione tra i numeri 4 e 2 dà resto 0.
Invece 5 % 3 darà come risultato 2, visto che il resto della divisione tra 5 e 3 è appunto 2. Attenzione a non confondere il modulo (%) con la divisione (/) in quanto i due operatori danno risultati differenti. Vediamo il modulo in azione:

    def f(x):
        return x%2

Con questa funzione avremo come risultato il resto della divisione tra il nostro numero x e il numero 2.
Vediamo ora, ignorando l'esistenza dell'operatore modulo, come è possibile sviluppare una funzione che ci dica se il numero immesso è pari o dispari.

//FUNZIONE DA AGGIUNGERE

Nella programmazione esiste un modo molto più immediato per sapere quale strada il programma deve prendere quando si trova di fronte a un simile bivio. Qui entrano in gioco i costrutti condizionali.

    def f(x):
        if (x%2) == 0:
            return 0
        else:
            return x
        
Analizziamo il codice linea per linea.
1.	def f(x):    dichiarazione della nostra funzione e della variabile con cui lavora
2.	if (x%2) == 0:  proviamo a tradurlo in parole. Se (if) il resto della divisione tra il mio numero x e 2 (x%2) è uguale a zero (== 0) allora (:)
3.	return 0    restituiscimi il valore 0 (che per noi significa che il numero è pari, in quanto il resto della divisione con 2 è 0)
4.	else:    altrimenti (ossia se il resto della divisione tra x e 2 NON risulta 0)
5.	return x    restituiscimi x tale e quale (che per noi significa che il numero è dispari)

In poche parole, i costrutti condizionali verificano se una condizione da noi imposta sussiste. Se esiste, il programma agirà in un modo, se non esiste il programma prenderà un'altra strada.

Oltre a if ed else, abbiamo incontrato un nuovo tipo di operatore, ==, che rappresenta un operatore di confronto. Come dice il nome, un operatore di confronto mette in paragone due valori. Ne esistono diversi:
== uguale   (es. 2 == 2)
!= diverso  (es. 2 != 3)
</>  minore/maggiore   (es. 3 < 5, 7 > 4)
<=/>= minore o uguale/maggiore o uguale

    Modificato l'ultima volta da Alberto Soffritti
