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
  <li><b>CNN</b>: Staat voor Convolutional Neural Network. Het is een vorm van een neuraal netwerk in Machine Learning terminologie.</li>
  <li><b>MFCC</b>: Staat voor Mel Frequency Cepstral Coefficient. Het is geluid omgezet naar features, floats in dit geval. Deze kunnen voor allerlei data science doeleinden gebruikt worden, zoals bijvoorbeeld data visualisatie.</li>
</ul>
<h3> Literature </h3>
<h4> Algemeeen over Afasie </h4>
<ul>
  <li>https://www.afasienet.com/mensen/afasie/over-afasie/</li>
  <li>https://www.hersenletsel-uitleg.nl/gevolgen/neurologische-gevolgen-nah/afasie-dysartrie-en-spraakapraxie-1</li>
</ul>
<h4> Sphinx en andere ASR tooling gerelateerd </h4>
<ul>
  <li>https://cmusphinx.github.io/wiki/tutoriallm/#language-models</li>
  <li>https://cmusphinx.github.io/wiki/tutorialdict/</li>
  <li>https://en.wikipedia.org/wiki/Acoustic_model</li>
  <li>ftp://m170.limsi.fr/public/csl01.pdf</li>
</ul>
<h4> Sequence to sequence models </h4>
<ul>
  <li>https://www.analyticsvidhya.com/blog/2018/03/essentials-of-deep-learning-sequence-to-sequence-modelling-with-attention-part-i/</li>
  <li>https://blog.keras.io/a-ten-minute-introduction-to-sequence-to-sequence-learning-in-keras.html</li>
  <li>https://nlp.stanford.edu/~johnhew/public/14-seq2seq.pdf</li>
</ul>
<h4> Mel Frequency Cepstral Coefficient (MFCC) </h4>
<ul>
  <li>http://practicalcryptography.com/miscellaneous/machine-learning/guide-mel-frequency-cepstral-coefficients-mfccs/</li>
  <li>https://haythamfayek.com/2016/04/21/speech-processing-for-machine-learning.html</li>
</ul>
<br>
<h2> Predictive models </h2>
<h3> G2p-seq2seq </h3>
<p>Op figuur 7 is het gebruik van het nieuw getrainde model te zien wat bij <a href="https://github.com/troley/project-aphasia/blob/master/Persoonlijke_portfolio.md#-g2p-seq2seq--1">Diagnostics of the learning process</a> toegelicht wordt. Ik schreef wat woorden op en de g2p interactive sessie genereerde de bijbehorende klanken. Deze konden vervolgens opgeslagen worden in een woordenlijst.</p>
<img src="g2p-seq2seq-new-model-usage.png" alt="Gebruik van een nieuw model met g2p-seq2seq" />
<i>Figuur 7</i>

<h3> Malaria detection CNN </h3>
<p>Naast het werken aan het project heb ik zelf ook nog een CNN gebouwd. Ik was tijdens het project veel bezig met tooling en kwam niet altijd aan het Data Science Machine Learning deel. Hiermee wil ik mijn opgedane skills bevestigen.</p>
<p>In <a href="https://github.com/troley/project-aphasia/blob/master/Malaria_detection_CNN.ipynb">dit jupyter notebook</a> bestand is het predictive model deel te vinden onder de kopjes <b>Building / training a predictive model</b> en <b>Using predictive model</b></p>
<br>
<br>
<h2> Data preparation </h2>
<h3> UvA data extractie unieke woorden </h3>
<p>Mijn collega Jesse heeft weinig coding ervaring. In het team hebben we daarom afgesproken dat we Jesse wat eenvoudigere klusjes zouden laten programmeren. Hierbij is het notebook bestand <a href="https://github.com/troley/project-aphasia/blob/master/text_files_to_dict.ipynb">waarbij uit een tal UvA bestanden unieke woorden worden geextraheerd en in een nieuw bestand worden opgeslagen</a> een voorbeeld die Jesse heeft gecodeerd. Ik gaf hem hierbij tips hoe bepaalde dingen bereikt konden worden. Samen hebben wij hieraan gewerkt om unieke data uit een UvA dataset te krijgen.</p>

<h3> Audio segment extractie en processing </h3>
<p>Het processen van Corpus Gesproken Nederlands (CGN) data voor seq2seq model training was een van mijn taken in sprint 7. Hiervoor heb ik een bestaande set aan csv bestanden (die eerder werd gemaakt door Jesse en Koray) gebruikt. Hierbij heb ik bij <a href="https://www.scrumwise.com/scrum/#/backlog-item/4298-de-meeste-voorkomende-woorden-in-de-cgn-data-in-een-nieuw-bestand-kopieren/id-84641-13034-61">deze Scrumwise ticket</a> de 15 meest voorkomende woorden in de Nederlandse taal genomen, opgezocht en gesneden uit de audio bestanden van CGN. De gesneden audiobestanden heb ik opgeslagen en gebruikt voor het trainen van het seq2seq model.</p> 
<p>De verdere details zijn in <a href="https://github.com/troley/project-aphasia/blob/master/audio_segment_extractor.ipynb">deze jupyter notebook</a> te vinden.</p>

<h3> Malaria detection CNN </h3>
<p>Naast het werken aan het project heb ik zelf ook nog een CNN gebouwd. Ik was tijdens het project veel bezig met tooling en kwam niet altijd aan het Data Science Machine Learning deel. Hiermee wil ik mijn opgedane skills bevestigen.</p>
<p>In <a href="https://github.com/troley/project-aphasia/blob/master/Malaria_detection_CNN.ipynb">dit jupyter notebook</a> bestand is het data preparation deel te vinden aan het begin onder het kopje <b>Data preparation</b></p>
<br>
<br>
<h2> Data visualization </h2>
<h3> (Py)Kaldi MFCC </h3>
<p>In latere sprints hadden we de focus gelegd op het tonen van klanken op het scherm bij een verkeerd/onbekend woord dat een Afasie patient tegen de Avatar zal uitspreken. Bij <a href="https://www.scrumwise.com/scrum/#/backlog-item/3718-split-audio-in-lesser-e-g-10-ms-bins-and-plot-this/id-84641-11740-0">deze</a> en <a href="https://www.scrumwise.com/scrum/#/backlog-item/3719-research-mfcc-of-kaldi-whether-hamming-window-is-processed-within-it/id-84641-11740-9">deze</a> Scrumwise tickets was het mijn doel om audio om te zetten naar MFCC en dit te visualiseren. Het uitgesproken woord wordt in dat geval op basis van geluidsfrequentie niveau's ontleed en op basis daarvan worden de klanken gegenereerd. Mijn deel hierin was naar (Py)Kaldi MFCC functionaliteit kijken. Dit heb ik gedaan en heb het <a href="https://github.com/troley/project-aphasia/blob/master/pykaldi_features.ipynb">in dit Jupyter Notebook bestand</a> uiteindelijk ook uitgewerkt en geplot.</p>

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
<h3>G2p-seq2seq</h3>
<p>Bij de g2p-seq2seq hoort ook de evaluatie van het geleerde model. De evaluatie die bij het framework, en bij dergelijke speech to text model frameworks gebruikt worden, is de Word Error Rate (WER) metric. Bij figuur 11 is de WER en accuracy te zien van de model evaluatie op 10% van de (test) data.</p>
<img src="https://github.com/troley/project-aphasia/blob/master/word_error_rate.png" />
<i>Figuur 11</i>
<br>
<br>
<h3> Malaria detection CNN </h3>
<p>Naast het werken aan het project heb ik zelf ook nog een CNN gebouwd. Ik was tijdens het project veel bezig met tooling en kwam niet altijd aan het Data Science Machine Learning deel. Hiermee wil ik mijn opgedane skills bevestigen.</p>
<p>In <a href="https://github.com/troley/project-aphasia/blob/master/Malaria_detection_CNN.ipynb">dit jupyter notebook</a> bestand is het evaluatie deel te vinden onder het kopje <b>Trained model evaluation</b></p>

<h2> Diagnostics of the learning process </h2>
<h3> G2p-seq2seq </h3>
<p>We hebben een dictionary gevonden met Nederlandse woorden met het formaat &lt;woord&gt; &lt;klank1&gt; &lt;klank2&gt; &lt;klank3&gt; etc. Het oorspronkelijke doel was deze uit te breiden met eigen woorden die patienten verkeerd kunnen uitspreken. Hiervoor heb ik gekeken naar de tool g2p-seq2seq die op basis van een bestaand model (Nederlandse dictionary) kon leren hoe klanken voor nieuwe woorden kunnen worden voorspeld. Dit werd gerealiseerd bij <a href="https://www.scrumwise.com/scrum/#/backlog-item/3525-train-a-g2p-model-with-dutch-language/id-84641-11280-18">deze Scrumwise ticket</a>.</p>
  
<p>Op het plaatje op figuur 12 is te zien dat het trainingsproces 16477 stappen (met groen onderstreept) had genomen en dat het model is geoptimaliseerd naar loss van 13% (met oranje onderstreept). De loss bleef tussen 9% en 15% schommelen en kwam niet meer tot nieuwe progressie, dus heb ik het trainigsproces gestopt op dit punt.</p>
<img src="g2p-seq2seq-model-training.jpg" alt="Het trainen van een nieuw klanken voorspel model." />
<i>Figuur 12</i>

<h3> Malaria detection CNN </h3>
<p>Naast het werken aan het project heb ik zelf ook nog een CNN gebouwd. Ik was tijdens het project veel bezig met tooling en kwam niet altijd aan het Data Science Machine Learning deel. Hiermee wil ik mijn opgedane skills bevestigen.</p>
<p>In <a href="https://github.com/troley/project-aphasia/blob/master/Malaria_detection_CNN.ipynb">dit jupyter notebook</a> bestand is het learning process diagnostics deel te vinden onder het kopje <b>Diagnostics of the learning process</b></p>

<h2> Communication </h2>
<h3> Presentations </h3>
<ul>
  <li>Eerste presentatie gegeven door Jesse en mij is <a href="https://github.com/troley/project-aphasia/blob/master/ppt_aphasia_week_4.pdf">hier te vinden</a> (mijn deel vanaf slide 3 t/m het eind)</li>
  <li>Tweede presentatie gegeven door Erik en mij is <a href="https://github.com/troley/project-aphasia/blob/master/ppt_aphasia_week_9.pdf">hier te vinden</a> (mijn deel vanaf slide 5 t/m het eind)</li>
  <li>Derde presentatie gegeven door Jesse en mij is <a href="https://github.com/troley/project-aphasia/blob/master/ppt_aphasia_week_16.pdf">hier te vinden</a> (mijn deel vanaf slide 5 t/m het eind)</li>
</ul>
-	E-mail naar Roelant
-	Research paper 
