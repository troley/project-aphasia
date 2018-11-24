# Aphasia portfolio
<table>
  <tr>
    <td>Naam student</td>
    <td>Ren&eacute; Uhliar</td>
  </tr>
  <tr>
    <td>Studentnummer</td>
    <td>14036738</td>
  </tr>
  <tr>
    <td>Projectthema</td>
    <td>Aphasia</td>
  </tr>
  <tr>
    <td>Begeleidende docent</td>
    <td>Jeroen Vuurens</td>
  </tr>
  <tr>
    <td>Datum</td>
    <td>9 september 2018</td>
  </tr>
</table>

<p> Dit bestand dient als een readers’ guide van de door mij gemaakte items en behaalde resultaten tijdens het Applied Data Science Semester. </p>

<p>Deze GitHub repository zal een aantal bestanden bevatten, die als bewijsmateriaal zullen dienen bij de activiteiten genoemd in deze samenvatting. </p>

<br>

<p><i> Een referentielijst met hyperlinks naar de bewijsmateriaal is onderaan dit bestand te vinden.</i></p>

<br>

<h2> Behaalde courses </h2>
Hieronder zijn de door mij behaalde courses te vinden
<h3> Datacamp </h3>
<p>De afgeronde Datacamp is in 2 delen gesplitst, omdat het niet op 1 plaatje paste. Het eerste deel is alfabetisch van A naar Z gescreenshot en het tweede deel van Z naar A.</p>

<i>Datacamp deel 1/2</i>
<img src="Datacamp_success1.png" alt="Datacamp afgerond eerste deel" />
<i>Figuur 1</i>
<br>
<br>
<i>Datacamp deel 2/2</i>
<img src="Datacamp_success2.png" alt="Datacamp afgerond tweede deel" />
<i>Figuur 2</i>
<br>
<br>
<h3> Coursera </h3>
<p>De afgeronde Coursera courses zijn op de plaatjes hieronder te zien. De assignments die niet voldaan zijn (oranje) zijn Octave/Matlab programming oefeningen. Deze heb ik niet voldaan, omdat het geen onderdeel was van de minor.</p>
<i>Coursera week 1</i>
<img src="coursera_wk1.png" alt="Coursera week 1 afgerond" />
<i>Figuur 3</i>
<br>
<br>
<i>Coursera week 2</i>
<img src="coursera_wk2.png" alt="Coursera week 2 afgerond" />
<i>Figuur 4</i>
<br>
<br>
<i>Coursera week 3</i>
<img src="coursera_wk3.png" alt="Coursera week 3 afgerond" />
<i>Figuur 5</i>
<br>
<br>
<i>Coursera week 6</i>
<img src="coursera_wk6.png" alt="Coursera week 6 afgerond" />
<i>Figuur 6</i>
<br>
<br>
<h2> Domain Knowledge </h2>
<h3> Used jargon </h3>
<ul>
  <li><b>ASR</b>: ASR staat voor Automatic Speech Recognition. Vertaald betekent dit Automatische spraakherkenning.</li>
  <li><b>g2p-seq2seq</b>: Een <a href="https://github.com/cmusphinx/g2p-seq2seq">tool</a> dat met behulp van een bestaande woordenlijst met woorden en klanken, de lijst kan uitbreiden met nieuwe woorden en klanken. Voorafgaand dient eerst een model getraind te worden gebaseerd op de bestaande lijst.</li>
  <li><b>g2p-seq2seq interactive sessie</b>: een sessie van de g2p-seq2seq tool die met een commando opgestart kan worden, waarbij woorden in de terminal geschreven kunnen worden en de tool genereert de bijbehorende klanken.</li>
  <li><b>Loss</b>: <a href="https://stackoverflow.com/a/42076606/7804385">Loss</a> willen we zo laag mogelijk krijgen tijdens het trainen van een model. Het geeft aan hoe goed of slecht het model is geoptimaliseerd. Hogere percentage betekent slechter getraind.
  <li><b>Phoneme</b>: Een phoneme is een klank. Bijvoorbeeld in het woord "muis" zijn m ui s de phonemen.</li>
  <li><b>Diphone</b>: Een diphone is een tweeklank. Binen dit project wordt hiernaar gerefereerd bij elke combinatie van twee opeenvolgende klanken samen. Voorbeeld: "Beker" wordt Be ek ke er</li> 
  <li><b>Avatar</b>: Avatar is de naam van de uiteindelijke ASR applicatie die Afasie patienten bij het revalidatieproces zal helpen.</li>
</ul>
<h3> Literature </h3>
-	Referentie links uit eerste portfolio
<h3> Evaluation </h3>

<h2> Predictive models </h2>
<h3> G2p-seq2seq </h3>
<p>Op figuur 7 is het gebruik van het nieuw getrainde model te zien wat bij <a href="https://github.com/troley/project-aphasia/blob/master/Persoonlijke_portfolio.md#-g2p-seq2seq--1">Diagnostics of the learning process</a> toegelicht wordt. Ik schreef wat woorden op en de g2p interactive sessie genereerde de bijbehorende klanken. Deze konden vervolgens opgeslagen worden in een woordenlijst.</p>
<img src="g2p-seq2seq-new-model-usage.png" alt="Gebruik van een nieuw model met g2p-seq2seq" />
<i>Figuur 7</i>
<br>
<br>
<h2> Data preparation </h2>
<h3> UvA data extractie unieke woorden </h3>
<p>Mijn collega Jesse heeft weinig coding ervaring. In het team hebben we daarom afgesproken dat we Jesse wat eenvoudigere klusjes zouden laten programmeren. Hierbij is het notebook bestand <a href="https://github.com/troley/project-aphasia/blob/master/text_files_to_dict.ipynb">waarbij uit een tal UvA bestanden unieke woorden worden geextraheerd en in een nieuw bestand worden opgeslagen</a> een voorbeeld die Jesse heeft gecodeerd. Ik gaf hem hierbij tips hoe bepaalde dingen bereikt konden worden. Samen hebben wij hieraan gewerkt om unieke data uit een UvA dataset te krijgen.</p>
-	Python bestand door sprekers ingesproken woorden in een set() krijgen

<h2> Data visualization </h2>
<h3> (Py)Kaldi MFCC </h3>
<p>In latere sprints hadden we de focus gelegd op het tonen van klanken op het scherm bij een verkeerd/onbekend woord dat een Afasie patient tegen de Avatar zal uitspreken. Het uitgesproken woord wordt in dat geval op basis van geluidsfrequentie niveau's ontleed en op basis daarvan worden de klanken gegenereerd. Mijn deel hierin was naar (Py)Kaldi MFCC functionaliteit kijken. Dit heb ik gedaan en heb het <a href="https://github.com/troley/project-aphasia/blob/master/pykaldi_features.ipynb">in dit Jupyter Notebook bestand</a> uiteindelijk ook geplot.</p>

<h2> Data collection </h2>
<h3> Voxforge data </h3>
<p>Bij de <a href="https://www.scrumwise.com/scrum/#/backlog-item/4045-research-pocketsphinx-repo/id-84641-12337-0">Scrumwise ticket</a> waar ik onderzoek deed naar PocketSphinx, ben ik VoxForge tegengekomen bij het lezen over <a href="https://cmusphinx.github.io/wiki/tutorialam/#data-preparation">Data preparation</a>. Ik heb verder gekeken naar VoxForge en kwam Nederlands gesproken taal data tegen. Hieruit was voor ons de dictionary het meest zeldzame bestand. Dit bestand hebben we zowel in PocketSphinx als in latere Kaldi experimenten gebruikt. Hieronder is een plaatje van de data die de Voxforge dictionary bevat.</p>
<br>
<img src="voxforge_dict_preview.png" alt="Een voorbeeld van de Voxforge woordenlijst." />
<i>Figuur 8</i>
<br>
<br>
<h3> Kaldi data </h3>
<p>Om de <a href="kaldifordummies">Kaldi for Dummies tutorial</a> bij de <a href="https://www.scrumwise.com/scrum/#/backlog-item/4057-audio-van-10-mensen-verzamelen-voor-kaldi-example/id-84641-12493-2">Scrumwise ticket</a> te kunnen realiseren, heb ik van uiteindelijk 11 verschillende stemmen (inclusief syntetische) opnames verzameld waarin de getallen van één tot tien werden uitgesproken. Deze data heb ik volgens de tutorial verwerkt, zodat Kaldi er succesvol mee gerund kon worden.</p>
<p>Hieronder is bij figuur 9 de data die als training set gebruikt zijn te zien em bij figuur 10 de data die als test set gebruikt zijn.</p>
<img src="kaldi_dummies_training_set.png" alt="Kaldi for Dummies tutorial training data set." />
<i>Figuur 9</i>
<br>
<br>
<img src="kaldi_dummies_test_set.png" alt="Kaldi for Dummies tutorial test data set." />
<i>Figuur 10</i>
<br>
<br>
<h2> Evaluation </h2>
-	G2p-seq2seq Word Error Rate plaatje laten zien
<h2> Diagnostics of the learning process </h2>
<h3> G2p-seq2seq </h3>
<p>We hebben een dictionary gevonden met Nederlandse woorden met het formaat &lt;woord&gt; &lt;klank1&gt; &lt;klank2&gt; &lt;klank3&gt; etc. Het oorspronkelijke doel was deze uit te breiden met eigen woorden die patienten verkeerd kunnen uitspreken. Hiervoor heb ik gekeken naar de tool g2p-seq2seq die op basis van een bestaand model (Nederlandse dictionary) kon leren hoe klanken voor nieuwe woorden kunnen worden voorspeld.</p>
  
<p>Op het plaatje op figuur 8 is te zien dat het trainingsproces 16477 stappen (met groen onderstreept) had genomen en dat het model is geoptimaliseerd naar loss van 1.3% (met oranje onderstreept). De loss bleef tussen 0.9% en 1.5% schommelen en kwam niet meer tot nieuwe progressie, dus heb ik het trainigsproces gestopt op dit punt.</p>
<img src="g2p-seq2seq-model-training.jpg" alt="Het trainen van een nieuw klanken voorspel model." />
<i>Figuur 11</i>

<h2> Communication </h2>
-	Presentaties
-	E-mail naar Roelant
-	Research paper 
