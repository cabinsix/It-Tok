# **It-tok** #

It-tok è un corpus di parlato di TikTok, raccolto tra marzo e aprile 2025. Esso è composto di due sottosezioni, una di argomento politico-sociale (PolSo) e una di argomento generalista (Gen). L'obiettivo con cui il corpus è stato raccolto riguarda l'individuazione dei correlati funzionali del parlato di TikTok, da un lato, e la comparazione del parlato generalista di TikTok con quello di argomento socio-politico. 

It-tok sarà presto disponibile nella forma trascritta sul presente github. Per consultare le trascrizioni annotate con sistema CLIPS (Savy 2006) o i file audio, scrivetemi pure all'indirizzo : ltroncone (at) unisa (dot) it

Il progetto It-tok è nato con tre obiettivi principali:

1. fornire una prima valutazione dei correlati funzionali di TikTok e, successivamente, delle modalità di comunicazione proprie di questo specifico social network;
2. mettere in evidenza le modalità con cui, su tale piattaforma, vengono trattate tematiche di rilievo per il dibattito pubblico;
3. confrontare i correlati funzionali della sezione generale con quelli della sezione tematica.


# **T-It-tok** #

T-It-tok è il progetto in corso per costruire una treebank di una parte del corpus It-tok.

**N.B.** I file CoNLL-U corrispondenti, che pure saranno messi a disposizione, sono stati manualmente controllati solo per le colonne riguardanti la lemmatizzazione e il PoS tagging. Le colonne riguardanti le informazioni morfosintattiche riportano i risultati dell'annotazione automatica fornita da spacy. Per alcuni specifici file, estratti casualmente (riportati nella sezione successiva) si avrà una treebank manualmente annotata. Come si vede, nei file CoNLL-U non controllati per le colonne con annotazione morfosintattica, si ha comunque un unico sent_id per tutto il turno, poiché la divisione in *frasi* è una delle questioni da affrontare caso per caso.

Dal momento che si tratta di annotazione morfosintattica di un corpus di parlato informale, l'annotazione della treebank riporta diverse questioni, anche di implicazione teorica, che annoto sotto.

# *Sample* #

Treebank of the It-Tok (T-It-tok) corpus subsection: sample made up of 15 videos from Gen_It-Tok and 15 videos from PolSo_It-Tok, randomly selected.

| Gen_It-Tok    |    status     | reviewed     |
| ------------- | ------------- | ------------- |
|G0125_D   |OK|
G1024_Q | in progress
G1224_Q
G0125_U
G1224_M
G1024_D
G0125_P
G1124_N
G0125_1 | OK
G1224_O
G1124_Q
G1124_F
G1224_I
G0125_11
G1024_S

|PolSo_It-Tok|    status     | reviewed     |
| ------------- | ------------- | ------------- |
|1024_E| |
0125_B
1224_U
1124_N
1224_E
1124_G
1224_F
0125_P
1024_N
1024_R
0125_C
0125_M
0125_Q
1224_V
0125_G


It-Tok project on Arborator: '(https://arborator.grew.fr/?#/projects/It-tok)'



# **Appunti e problemi irrisolti** #


| fenomeni    |    scelte     | es.     | status |
| ------------- | ------------- | ------------- |
| pronomi personali    |    ogni persona ha il suo lemma     | io -> io; lei -> lei | 
| pronomi personali in casi   |    ogni caso ha il suo lemma     | io -> io ; suo -> suo  |non implementato, da capire|
| dipendenza SD|    testa dello scope?| |OK|
| dipendenza delle pause piene e vuote | testa successiva | | BOH|


* Questione pronomi ancora irrisolta: usare 'io' come pronome lemma di tutti (tuo = io, 2 persona, sing, gen) o usare lemmi specifici? Ho visto che KIPARLA forest li separano. 

    "fargli" : fare (= inf) + gli (= lo dat?)

Non so sono ancora molto in dubbio sulla questione pronomi, clitici e casi...

* "chi è del mestiere sicuramente starò sbagliando" ellissi "per"(?)

* Problemi SD

* che polivalente

* pause piene, da chi dipendono? testa successiva? come fossero tutte processing forse? "scrivi la tua opinione **eeh** nei **commenti**"

