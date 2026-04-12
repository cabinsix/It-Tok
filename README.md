# **It-tok** #

It-tok è un corpus di parlato di TikTok, raccolto tra marzo e aprile 2025. Esso è composto di due sottosezioni, una di argomento politico-sociale (PolSo) e una di argomento generalista (Gen). L'obiettivo con cui il corpus è stato raccolto riguarda l'individuazione dei correlati funzionali del parlato di TikTok, da un lato, e la comparazione del parlato generalista di TikTok con quello di argomento socio-politico. 

## Accessibilità

It-tok è disponibile sotto compilazione della liberatoria allegata nella presente repository, in formato tabulare trascritto. È comunque necessario richiedere l'API ricerca di TikTok all'indirizzo: https://developers.tiktok.com/products/research-api/

L'API prende un paio di settimane.

Per la consultazione scrivetemi pure all'indirizzo : ltroncone (at) unisa (dot) it


## Il progetto
Il progetto It-tok è nato con tre obiettivi principali:

1. fornire una prima valutazione dei correlati funzionali di TikTok e, successivamente, delle modalità di comunicazione proprie di questo specifico social network;
2. mettere in evidenza le modalità con cui, su tale piattaforma, vengono trattate tematiche di rilievo per il dibattito pubblico;
3. confrontare i correlati funzionali della sezione generale con quelli della sezione tematica.


| subcorpus    |    durata totale      | n. tokens       |   
| ------------- | ------------- | ------------- |
|Gen          |       4:06:04         |      35 254      |  
|PolSo          |      3:43:49          |     32 581       |  
|          |                |            |  
|It-tok          |       7:50:54         |      67 835      |  



### Riferimento ###
Troncone, L. (2025). "Building It-tok: an Italian TikTok Corpus". Proceedings of CLiC-it 2025: Eleventh Italian Conference on Computational Linguistics, pre-print at https://www.researchgate.net/publication/396559002_Building_It-tok_an_Italian_TikTok_corpus


## **Tr-It-tok** ##

T-It-tok si riferisce alla sezione di It-tok annotata manualmente in CoNLL-U.

It-Tok project su Arborator: '(https://arborator.grew.fr/?#/projects/It-tok)'

Su Arborator le trascrizioni da cui traiamo la treebank comprendono la punteggiatura, ma l'annotazione no.

### Consultabilità ###
La sezione di It-tok in annotazione come treebank è consultabile su Arborator (https://arborator.grew.fr/?#/projects/It-tok) nella sezione Grew, con il linguaggio utilizzabile su GrewMatch. Solo i file senza "_aligned" nel nome (es. X0000_X0 invece di X0000_X0_aligned) sono completi di corretta annotazione di split in frasi, dipendenze e feature morfologiche.

### Campione e procedimento dei lavori ###

Il campione comprende 10 video di Gen_It-Tok e 10 di PolSo_It-Tok, per un totale di circa 10.000 token (=ca. 15% It-tok), selezionati randomicamente.

| Gen_It-Tok    |    status      | n. tokens       |n. frasi     | PolSo_It-Tok  |    status    | n. tokens | n. frasi |
| ------------- | ------------- | ------------- |  ------------- |-----| ------------- | ------------- | ------------- |
|G0125_D        |completo        |       153     |    11  |1024_S        | completo  | 1809 | 52
G1024_Q         | completo       | 202           |  17    |0125_U        | completo      | 355 | 17
G1224_H         | completo       |383            |  29   |1224_G        | completo     |653 | 37
G0125_O         | completo       |   897        |  30    |  1124_S       | completo    |189 | 9
G1224_M         | completo     | 321            |  18    |1224_E        |completo      |268 | 9
G1024_D         |completo       | 337            |  26   |1124_G        |completo     |340 | 9
G0125_P         |completo    |308           |   13   |1124_L         |completo     | 672 | 27
G1124_N         |completo      |560          |  22      |1024_R        |completo     | 582 | 31
G0125_1         | completo         | 265         |  20 |      0125_I | completo | 404 | 14
G0125_16        |completo         |   1214         |  43|      1025_U | completo | 274 | 20
| **TOT. completi**|**10**|**4.640**|    tot. frasi   229            | **TOT. completi** |  **10**    |           **5.546**  | tot. frasi 225
|**TOT. video annotati**  |**20** | **TOT. token annotati**    |**10.186**        |  TOT. frasi annotate  |  454






### **Appunti e problemi ** ###


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

