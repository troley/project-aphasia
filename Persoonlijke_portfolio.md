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

<p> Dit bestand dient als een samenvatting van de door mij uitgevoerde activiteiten tijdens het Applied Data Science Semester. De activiteiten zullen per sprint (2 weken) beschreven worden. </p>

<p>Deze GitHub repository zal een aantal bestanden bevatten, die als bewijsmateriaal zullen dienen bij de activiteiten genoemd in deze samenvatting. </p>

<br>

<p><i> Een referentielijst met hyperlinks naar de bewijsmateriaal is onderaan dit bestand te vinden.</i></p>

<h2>Sprint 1 (27-08-2018 – 07-09-2018)</h2>
<p>Tijdens sprint 1 heb ik voor dit thema gekozen. Het sprak mij het meeste aan, omdat ik bij gezondheidszorg projecten, zeker bij een ernstige aandoening als deze, sterk het gevoel heb dat ik mensen die het nodig hebben wellicht kan helpen. Dat wil ik ook graag doen. </p>

<p>Ten eerste heb ik mij ingelezen over Afasie[1][2]. Ik heb daar voor dit semester van start was gegaan nooit eerder over gehoord. Daarom heb ik informatie gelezen over de aandoening zelf, waardoor het ontstaat en hoe het wordt gediagnosticeerd en behandeld. </p>

<p>Het werd bij mij snel duidelijker na het eerste gesprek met Jeroen Vuurens wat Rijndam Revalidatie centrum (de opdrachtgever) zo ongeveer van ons wil. De opdrachtgever wilt een applicatie, genaamd Avatar, hebben, waarmee patiënten interactief mee zullen kunnen communiceren. Deze applicatie zal de patiënten corrigeren nadat zij een semantiek en/of fonologische fout hebben gemaakt. Ik heb daarom mijn vooronderzoek specifieker gericht op de bestaande smartphone- en webapplicaties[3]. Daarbij ben ik tot de conclusie gekomen dat de meeste applicaties meer gericht zijn op gerubriceerde plaatjes en woorden / zinsdelen, waarbij de gebruiker zich van eenvoudige naar moeilijkere woorden en/of zinsdelen kan toewerken. </p>
<p>Tijdens deze sprint werden de taken een beetje verdeeld in het team. Ik had als eerste taak het afspelen van een geluidsbestand op de hhs datascience server op mij genomen. Hier heb ik een aantal manieren voor uitgeprobeerd, maar ze mislukte allemaal, totdat ik bij een StackOverflow artikel[4] ben gekomen waarin een tool genaamd MobaXTerm werd genoemd. Deze tool zorgde ervoor dat bestanden heel eenvoudig (in een grafische interface) afgespeeld konden worden op een Windows systeem.</p>

<p>Naast de werkzaamheden rondom het project ben ik verder gegaan met data camp en was daarnaast ook begonnen aan de coursera machine learning course. Deze heb ik tot en met het cost function deel gevolgd.</p>

<h2>Sprint 2 (10-09-2018 – 21-09-2018)</h2>
<p>Deze sprint was het voor mijn team al meer duidelijk wat Rijndam van ons verwachtte. We hebben daarom een eerste versie hoofdvraag opgesteld met een paar bijbehorende deelvragen. Hierbij heb ik mij gericht op een deelvraag rondom bestaande speech-to-text (STT) API’s en applicaties[5]. Hiervoor heb ik een vooronderzoek van Koray erbij gepakt over de bestaande 3e partij STT API’s en heb verder nog gezocht naar applicaties die STT in het Nederlands konden afhandelen. Bij de gevonden applicaties zag ik al meteen dat zij moeilijk aan ons doeleinde zouden voldoen.</p>

<p>Ik kreeg later twee API’s van Erik als tip om naar te kijken en heb mij op een van deze API’s verder op in verdiept. De eerste API die wij onderzochten was een pure Python API genaamd <b>SpeechRecognition</b>[6]. Het is een high-level API waarmee heel eenvoudig STT uitgevoerd kan worden d.m.v. verschillende spraakherkenning engins. De tweede API was <b>PocketSphinx</b>[7][8]. Deze API blijkt, na een aantal artikelen en reacties op het web te hebben gelezen, een best volwassen STT / Text-to-speech (TTS) API te zijn. De API is primair geschreven in de programmeertaal C, maar heeft ook versies naar andere programmeertalen. Tot zover lijkt dit het meest voor de hand liggende API te zijn die ons kan helpen bij het behalen van ons doel. Het zou goed kunnen dat we uiteindelijk SpeechRecognition samen met PocketSphinx zullen gebruiken, omdat SpeechRecognition ook onder andere functies voor het gebruik van PocketSphinx API bevat.</p>

<p>Naast de werkzaamheden rondom het project heb ik tijdens deze sprint de data camp volledig afgerond. Ook ben ik verder gegaan met de coursera machine learning course en heb het gradient descent deel afgerond. Ik loop hier hierbij een week achter, dus zal dit in sprint 3 z.s.m. inhalen.</p>

<h2>Sprint 3 (24-09-2018 – 05-10-2018)</h2>
<p>Voor deze sprint was het de bedoeling al wat ‘vatbare’ synthetische data te hebben gecreëerd en deze wellicht ook gebruikt te hebben. We hebben een heel Nederlandse language model[9], dictionary[10] en een acoustic model[11] gedownload[12]. Dit zijn de onderdelen waar PocketSphinx gebruik van maakt bij het herkennen van spraak.</p>

<p>Door een snelle ‘plug&play’ test[12][13] op PocketSphinx (Sphinx4, de Java versie van PocketSphinx) te hebben uitgevoerd, blijkt dat de woorden en zinnen die we uitspreken redelijk worden herkend. In een niet eens al te druk lokaal wordt de spraakherkenning al snel slechter, is ons opgevallen.</p>

<p>We hebben het dictionary bestand geopend in IntelliJ (omdat het PocketSphinx project daarin open was) en die heeft ons 40.000 woorden getoond  (uiteindelijk bleek dit 1.4 miljoen te zijn nadat we pas later het bestand met nano tekst editor geopend hebben). Dat leek ons heel weinig. We hebben daarom als doel bepaald de bestaande dictionary, acoustic model en language model uit te breiden en kijken hoe PocketSphinx zal reageren qua spraakherkenning op de door ons geproduceerde data.</p>

<p>We hebben de taken in onze groep verdeeld. Erik en ik gingen naar het acoustische model en de dictionary kijken en Koray en Jesse die hebben naar het language model gedeelte gekeken. </p>

<p>Koray en Jesse hebben eerst Nederlandse Wikipedia data verzameld, maar deze data bleken niet goed te zijn, doordat spraak met getranscribeerde tekst altijd overeenkwam. Daarna hebben zij 10 uur aan data (spraak en tekst) van UvA website gedownload en deze gebruikt voor hun taak. 

<p>De taak die Erik en ik hadden, was het kijken naar de mogelijkheden om de huidige dictionary uit te breiden met veel meer woorden, want 40.000 unieke woorden vonden wij geen representatieve dataset voor een spraakherkenningssysteem. </p>

<p>We hebben ons ten eerste verdiept in de structuur van een dictionary bestand. Erik heeft zich verdiept in de klanken, hoe die opgebouwd worden in een dictionary bestand en verschillende tussen bijv. Engelse en Nederlandse klanken in een dictionary bestand. Ik heb mij verdiept in de tools[15] <i>(hoofdstukken Dictionary, G2P tool Phonetisaurus en G2P tool g2p-seq2seq)</i> waarmee een model getraind kan worden die vervolgens gebruikt kan worden om een bestaand dictionary bestand uit te breiden.</p>

<p>We hebben uiteindelijk de tool g2p-seq2seq[16] gebruikt om het model met de Nederlandse dictionary te trainen. Samen met Jesse heb ik twee scripts[17][18] geschreven die de data in de juiste, bruikbare format processen[19].

<p>Bij het trainingsproces met g2p-seq2seq heb ik voor het eerst de mogelijkheid gehad om zelf een machine learning proces te initialiseren en te runnen. Ik heb door dit mee te maken een veel beter beeld gekregen van wat het eigenlijk betekent een ‘model trainen’ en hoeveel moeite het bedraagt om door allerlei excepties en errors heen te gaan, voordat de gebruikte tools kunnen beginnen met het trainen van een model.</p>

<p>Na een gesprek te hebben gevoerd met Jeroen Vuurens de laatste dag van de sprint, zijn we er samen achter gekomen dat PocketSphinx waarschijnlijk wel een doodlopend einde zal zijn bij dit project. PocketSphinx heeft de spraak data nodig in het dictionary bestand om op basis daarvan een voorspelling te doen over wat de spreker zegt. Dit komt niet zo goed van pas bij patiënten met Afasie, omdat zij vaak nonsens uitspreken, en deze woorden zullen niet in het dictionary bestand voorkomen.</p>

<p>We hebben samen met Jeroen naar nieuwe mogelijkheden gekeken. Zo hebben we nieuwe ideeën voor de volgende sprint en we zullen moeten onderzoeken of het haalbaar is en wat de voorgaande onderzoeken te zeggen hebben over de methoden.</p>

<h2>Sprint 4 (8-10-2018 – 19-10-2018)</h2>
<p>Sprint 4 begon met een gesprek met onze opdrachtgever Ineke van der Meulen en een expert op het gebied van Afasie Roelant Ossewaarde. Ik heb dit gesprek helaas niet kunnen bijwonen wegens een ziekte, maar ik heb de besproken punten meegekregen van mij groepsgenoten.[20]</p>

<p>Ik ben mij na het gesprek met Roelant gaan focussen op de spraakherkenningstool Kaldi. We hebben deze tool in eerste instantie voorbij zien komen, maar besteedden er niet veel aandacht aan, doordat wij het doodlopende pad met PocketSphinx namen.</p>

<p>We hebben een stappenplan gemaakt waarbij we stap voor stap gingen kijken naar Mel Frequenciy Cepstral Coefficient (MFCC), WIndow Framing en  Fourier Transformatie. Hierbij hebben we de taken verdeeld. Ik ging kijken naar de mogelijkheid om Mel Frequencies te kunnen genereren met behulp van Kaldi. Hierbij heb ik ook uitgezocht of Kaldi MFCC functionaliteit ook van de Window Framing functie gebruik maakte[21]. Dit bleek wel het geval te zijn. Snel heb ik een test opgezet die op basis van een 4 seconden audio die Mel Frequencies genereerde. De Mel Frequencies zijn float getallen. 

<h1>Referentielijst</h1>
[1] https://www.afasienet.com/mensen/afasie/over-afasie/ 
[2] https://www.hersenletsel-uitleg.nl/gevolgen/neurologische-gevolgen-nah/afasie-dysartrie-en-spraakapraxie-1 
[3] <h2>Verwijs naar het word document met vooronderzoek Afasie applicaties</h2>
[4] https://stackoverflow.com/a/39188790/7804385
[5] <h2>Verwijs naar het word document met onderzoek naar s2t API’s en applicaties</h2>
[6] https://pypi.org/project/SpeechRecognition/ 
[7] https://github.com/cmusphinx/pocketsphinx 
[8] https://cmusphinx.github.io/wiki/tutorial/ 
[9] https://cmusphinx.github.io/wiki/tutoriallm/#language-models
[10] https://cmusphinx.github.io/wiki/tutorialdict/ 
[11] https://en.wikipedia.org/wiki/Acoustic_model 
[12] <h2> Verwijs naar Voxforge_nl download pagina </h2>
[13] https://cmusphinx.github.io/wiki/tutorialsphinx4/#basic-usage 
[14] https://cmusphinx.github.io/wiki/tutorialsphinx4/#livespeechrecognizer 
[15] <h2> Verwijs naar het document over G2P tools </h2>
[16] https://github.com/cmusphinx/g2p-seq2seq 
[17] <h2> Verwijs naar het script dat UvA zinnen split in woorden en in new_dict opslaat </h2>
[18] <h2> Verwijs naar het script dat lege wit-regels verwijderd uit het new_dict bstand </h2>
[19] <h2> Verwijs naar het document Beschrijving_UvA_data_processing.docx (dropbox) </h2>
[20] <h2> Verwijs naar het document gesprek met Roelant Ossewaarde over Afasie </h2>
[21] <h2> Verwijs naar het document op drive over Kaldi window framing </h2>
