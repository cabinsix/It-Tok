# **It-tok** #

It-tok è un corpus di parlato di TikTok, raccolto tra marzo e aprile 2025. Esso è composto di due sottosezioni, una di argomento politico-sociale (PolSo) e una di argomento generalista (Gen). L'obiettivo con cui il corpus è stato raccolto riguarda l'individuazione dei correlati funzionali del parlato di TikTok, da un lato, e la comparazione del parlato generalista di TikTok con quello di argomento socio-politico. 

It-tok sarà presto disponibile nella forma trascritta sul presente github. Per consultare le trascrizioni annotate con sistema CLIPS (Savy 2006) o i file audio, scrivetemi pure all'indirizzo : ltroncone (at) unisa (dot) it

Il progetto It-tok è nato con tre obiettivi principali:

1. fornire una prima valutazione dei correlati funzionali di TikTok e, successivamente, delle modalità di comunicazione proprie di questo specifico social network;
2. mettere in evidenza le modalità con cui, su tale piattaforma, vengono trattate tematiche di rilievo per il dibattito pubblico;
3. confrontare i correlati funzionali della sezione generale con quelli della sezione tematica.


**N.B.** I file CoNLL-U corrispondenti, che pure saranno messi a disposizione, sono stati manualmente controllati solo per le colonne riguardanti la lemmatizzazione e il PoS tagging. Le colonne riguardanti le informazioni morfosintattiche riportano i risultati dell'annotazione automatica fornita da spacy. Per alcuni specifici file, estratti casualmente (riportati nella sezione successiva) si avrà una treebank manualmente annotata. Come si vede, nei file CoNLL-U non controllati per le colonne con annotazione morfosintattica, si ha comunque un unico sent_id per tutto il turno, poiché la divisione in *frasi* è una delle questioni da affrontare caso per caso.


### Riferimento ###
Troncone, L. (in press). "Building It-tok: an Italian TikTok Corpus". Proceedings of CLiC-it 2025: Eleventh Italian Conference on Computational Linguistics, pre-print at https://www.researchgate.net/publication/396559002_Building_It-tok_an_Italian_TikTok_corpus


## **Tr-It-tok** ##

T-It-tok è il progetto in corso per costruire una treebank di una parte del corpus It-tok.
Dal momento che si tratta di annotazione morfosintattica di un corpus di parlato informale, l'annotazione della treebank riporta diverse questioni, anche di implicazione teorica, che annoto sotto.

It-Tok project su Arborator: '(https://arborator.grew.fr/?#/projects/It-tok)'

Su Arborator le trascrizioni da cui traiamo la treebank comprendono la punteggiatura. Alla fine del lavoro di annotazione la punteggiatura verrà rimossa con le sue relative annotazioni, tenendo cura di traslare gli allineamenti che eventualmente portano tali token ai token adiacenti.

### Consultabilità ###
La sezione di It-tok in annotazione come treebank è consultabile su Arborator (https://arborator.grew.fr/?#/projects/It-tok) nella sezione Grew, con il linguaggio utilizzabile su GrewMatch. Solo i file senza "_aligned" nel nome (es. X0000_X0 invece di X0000_X0_aligned) sono completi di corretta annotazione di split in frasi, dipendenze e feature morfologiche.

### Campione e procedimento dei lavori ###

Sottosezione di It-Tok di cui si stanno annotando le treebank (T-It-tok) : il campione sarà di video di Gen_It-Tok e  di PolSo_It-Tok, per un totale di circa 10.000 token (=ca. 15% It-tok), selezionati randomicamente.

| Gen_It-Tok    |    status      | n. tokens       |     | PolSo_It-Tok  |    status       | | n. tokens |
| ------------- | ------------- | ------------- |  ------------- |-----| ------------- | ------------- |  ------------- |
|G0125_D        |completo        |       390     |      |1024_S        | completo  | 1992
G1024_Q         | completo       | 216           |      |0125_U        | completo      | 378
G1224_H         | completo       |414            |     |1224_G        | completo     |733
G0125_O         | completo       |   974        |      |  1124_S       | completo    |213
G1224_M         | completo     | 345            |      |1224_E        |completo      |307
G1024_D         |completo       | 170            |     |1124_G        |allineato     |ca. 350
G0125_P         |completo    |337           |      |1124_L         |completo     | 735
G1124_N         |completo      |609          |        |1024_R        |completo     | 643
G0125_1         | completo         | 358         |        
G0125_16        |completo         |   1318         |        
| **TOT. completi**|**10**|**5.131**|                   | **TOT. completi** |  **7**    |           **5.001**  
|**TOT. video annotati** ||**17** | |**TOT. token annotati**            |                |**10.131**        |                                                                   |






### **Appunti e problemi irrisolti** ###


| fenomeni    |    scelte     | es.     | status | 
| ------------- | ------------- | ------------- | ------------- |
| pronomi personali   |  ogni persona ha il suo lemma    | _io_ -> io; _lei_ -> lei | OK |
| pronomi personali in casi   |    ogni caso ha il suo lemma     | ho dovuto aggiungere nei FEATS ma solo per i pronomi al genitivo **PronNumber**: _suo_ = 3.SG.GEN.**SG**; _vostro_ = 2.**PL**.GEN.SG; _suoi_= 3.SG.GEN.**PL**|ho deciso di tenere per ogni pronome il suo lemma, ma specificando sempre caso, persona, numero come se si rifacessero allo stesso lemma|
| dipendenza SD|    testa dello scope| _ |OK|
| dipendenza delle pause piene e vuote | testa precedente | _ |  OK |
| pause | lemma = "pause" | _{sp},{lp},{/}, {eeh},{emh}_|OK|
|interruzioni e prolungamenti| MISC| _andare{ee}_= lemma "andare" + MISC: Prolonged=Yes|OK

* E fai x e sei Y, e fai z e se k... l'ho annotati come congiunti(?)

* G0125_P: "l'anno scorso "->appos o parataxis

* "chi è del mestiere sicuramente starò sbagliando" ellissi "per"(?)

* Problemi SD

* che polivalente

