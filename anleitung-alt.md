# Anleitung (ALT)

### Grundsätzliches

Der (eingedeutschte) Begriff *Shownotes* ist ein Kompositum aus den englischen Wörtern *show* und *notes* und bezeichnet Begleitnotizen zu Audio- und Videoproduktionen, insbesondere Podcasts und Hörfunksendungen. Allgemein betrachtet handelt es sich um eine Mischung aus Stichpunkten, Inhaltsangaben, Zitaten und weiterführenden Informationen. Diese Notizen können aus folgenden Gründen nützlich sein:

- Jemand möchte sich vor dem Hören einer Produktion (Aufzeichnung) einen Überblick verschaffen und wissen, worum es ungefähr geht (Querlesen) – um dann zu entscheiden, ob sich ein Hören überhaupt lohnt.
- Während des Hörens kann man bequem auf gegebenenfalls eingebaute Verweise zurückgreifen und muss sich nicht selbst alles zusammensuchen (Arbeitserleichterung). Die Einteilung in Kapitel sorgt für Übersicht und Struktur.
- Hörgeschädigte werden nicht gänzlich ausgeschlossen.
- Man findet schneller etwas wieder, die Durchsuchbarkeit ist zumindest einigermaßen gegeben.

Insbesondere haben Shownotes das Ziel, der Hörerschaft das Leben angenehmer zu machen und einen Nutzen zu bieten. Dies sollte man als Autor stets im Hinterkopf behalten!

### Womit man schreiben kann

Eigentlich braucht man keine besondere Software, um Shownotes zu verfassen. Damit mehrere Autoren gleichzeitig an einem Dokument arbeiten können, setzen wir zurzeit die Webanwendung *ShowPad* (https://shownot.es/) ein. Aus dem Kalender der *Hörsuppe* (http://hoersuppe.de) übernimmt es alle Termine von Livesendungen und bietet dafür die schnelle Erstellung eines sogenannten *Pads* an. Um das zu tun und überhaupt mit dem ShowPad arbeiten zu können, ist ein Benutzerkonto notwendig. Das gibt es nach einer schnellen Registrierung kostenlos. Zu den dem System bekannten Podcast dürfen sich die Benutzer selber Pads erstellen. Jederzeit kann man sich aber von den Mitgliedern des Shownotes-Kernteams welche für alles andere anlegen lassen. Dazu genügt es, eine Nachricht zu schreiben (team at shownot.es) oder im Chatraum (\#shownotes bei Freenode) vorbeizuschauen.

Das eben erwähnte Kernteam kümmert sich, nebenbei gesagt, hauptsächlich um Entwicklung, Administration und Betrieb.

### ShowPad in Kürze

Egal ob man ein Pad selber angelegt oder eines angelegt bekommen hat – die Adresse ist von der Form https://shownot.es/podcastname/625, im Bearbeitungsmodus um ein /edit/ ergänzt. Ruft man ein jungfräuliches Pad auf, ist außer einer Zeilennummer noch nix zu sehen. Rechts gibt es einen Chat, mit dem sich die Schreiber während der Arbeit austauschen können.

Zunächst mal sind die Namen der Podcaster einzutragen.

Am Ende dürfen sich alle Shownotes-Autoren als Helfer eintragen. Es versteht sich wohl von selbst, dass man sich der Fairness halber nur nach dem Einbringen substantieller Beiträge einträgt. Bei schließlich 200 Zeilen an acht davon beteiligt zu sein fällt eher nicht in diese Kategorie.

Man kann das Pad wie einen einfachen Editor benutzen. Jeder registrierte Benutzer kann sich bei seinen persönlichen Profil-Einstellungen eine beliebige Farbe aussuchen, mit der seine Textbeiträge (auch im Chat) hinterlegt werden, damit man erkennen kann, wer was beigetragen hat. Idealerweise sind die Farben so ausgesucht, dass man verschiedene Autoren klar voneinander unterscheiden kann und alles noch leicht lesbar ist.

Das ShowPad bietet aber mehr als simple Editorfunktionen! In Shownotes ist es nützlich, wenn man weiß, zu welchem Zeitpunkt eines Podcastes ein bestimmter Teil des Inhalts gehört. Irgendwie muss also die Zeit vermerkt werden. Standardmäßig arbeitet das ShowPad dazu mit der Unixzeit. Die aktuelle bekommt man durch Schreiben von `###` und direkt danach einem Leerzeichen. In den fertigen Shownotes werden später alle Zeitmarken relativ zur ersten im Quelltext vorkommenden Zeitangabe vor einer Überschrift berechnet.

Hinter die Zeitmarke kommt der eigentliche Inhalt. Das sieht dann etwa so aus:

`1397473197 Schloss Neuschwanstein`

Möchte man dem noch eine Information hierarchisch unterordnen, so geschieht dies mit einem Bindestrich (Viertelgeviertstrich) vor der eigentlichen Information:

`1397473197 Schloss Neuschwanstein`

`- Hohenschwangau (wo das Schloss steht)`

Die Kombination aus Zeitmarke und weiteren Informationen nennt man übrigens *Item*. Jedem Item darf höchstens eine URL zugeordnet werden. Diese gehört zwischen Vergleichszeichen hinter den Text:

`1397473197 Schloss Neuschwanstein <https://de.wikipedia.org/wiki/Schloss\_Neuschwanstein\>`

`- Hohenschwangau (wo das Schloss steht) <https://de.wikipedia.org/wiki/Hohenschwangau\>`

Hinter einzelne Worte innerhalb eines Items kann kein Verweis gelegt werden. So was hier ist also *nicht* zulässig:

`1347423137 Sebastian Krumbiegel <http://de.wikipedia.org/wiki/Sebastian\_Krumbiegel\> ist Mitglied der Prinzen`

Weiter darf ein Item durch mehrere sogenannte *Tags* kategorisiert werden (muss aber nicht). Die gängigsten Tags sind diese hier:

`#c` oder `#chapter` Damit wird ein neues Kapitel eingeleitet

`#g` oder `#glossary` Nachschlagequellen, zum Beispiel Wikipedia, Psiram, Stupipedia

`#q` oder `#quote` Zitate

`#article` Presseartikel, etwa von Zeitungen

`#shopping` Wenn auf ein Angebot verwiesen wird, bei dem es primär ums Verkaufen geht oder wenn dort hauptsächlich ein kommerzielles Produkt oder eine Dienstleistung beworben wird. Prominentes Beispiel: Amazon.

`#podcast` Podcasts, entweder Startseite oder eine bestimmte Episode

`#video` Für Verweise auf Videos, beispielsweise bei YouPorn.

`#image` Für Verweise auf Foto und andere Bilddateien, etwa bei Flickr

`#tweet` Einzelner Tweet (Twitter oder App.net) oder ein Konto allgemein

`#link` Explizit genannter URL

`#r` oder `#revison` Dieses Item muss noch überarbeitet werden – eine Markierung, die das Wiederfinden von unfertigen Stellen erleichtert, ein sparsamer Umgang ist aber anzustreben

Einige der Tags sind (offenbar) nur in Verbindung mit einer zusätzlich angegebenen URL sinnvoll.

Mit Tags könnte unser Beispiel von oben so aussehen:

`1397473197 Schloss Neuschwanstein <https://de.wikipedia.org/wiki/Schloss\_Neuschwanstein\> #g`

`- Hohenschwangau (wo das Schloss steht) <https://de.wikipedia.org/wiki/Hohenschwangau\> #g`

Man darf aber eben auch mehrere Tags setzen:

`1397473082 Köln – hält Mirko für eine "geile Stadt" <https://de.wikipedia.org/wiki/Köln\> #q #g`

Ans Ende eines Items kommt *kein* Punkt.

Zitate gehören zwischen Anführungszeichen (`"`), die später automatisch in richtige Anführungszeichen verwandelt werden. Der Urheber wird meist in Klammern dahinter geschrieben. Entweder notiert man vollständige Sätze:

`1117913729 "Vanilleeis sollte ein Grundrecht sein!" (Stefan Schneidereit) #q`

Diese Sätze sollen mit einem Punkt/Ausrufezeichen/Fragezeichen vor dem abschließenden `"` enden.

Oder Teile man schreibt nur ausgewählte Worte auf:

`0985331825 Max findet Kirschkuchen "total abgefahren" #q`

In jedem Falle sollte aber erkennbar sein, wer zitiert wird.

Noch ein technischer Hinweis: Zwischendurch sollte man schauen, ob die selbst erzeugten Zeitmarken zu denen der anderen Autoren passen. Bestehen große Abweichungen, liegt ein Problem vor, das man mit einer Korrektur der lokalen Systemzeit beheben kann.

Zwischenspeichern muss man übrigens nicht, das geschieht automatisch.

Und wenn alles fertig ist? Dann muss ein Befugter die Shownotes erst *sichten* und damit quasi freischalten. Um Shownotes zur Sichtung vorzuschlagen, gibt es oben eine eigene Schaltfläche. Nach erfolgreicher Sichtung können die Podcaster die Shownotes mittels eines Plugins in ihr Blog (WordPress) einbauen. Unabhängig davon ist das Dokument unter der anfangs genannten URL erreichbar. In beiden Fällen entsteht ein für den herkömmlichen Leser genießbarer Hypertext mit Zeitangaben in Tooltips.

Mit dem Schreiben von Shownotes verzichtest du übrigens auf sämtliche Schutzrechte und übergibst das Werk in die Gemeinfreiheit, Stichworte: CC0, Public Domain.

### Wie anfangen?

Wer sich noch nicht traut oder unsicher ist, kann sich als Zaungast zunächst mal angucken, wie Shownotes entstehen. Dazu einfach während einer Livesendung das zugehörige Pad aufrufen und verfolgen, was geschieht. Und keine Berührungsängste haben! Erst mal nur ein paar URLs beisteuern oder Rechtschreibfehler korrigieren ist für den Anfang völlig ausreichend.

Denjenigen, die erst mal noch mehr über das Schreiben guter Shownotes lernen möchten, sei die Lektüre der folgenden beiden Abschnitte empfohlen.

### Was man schreiben kann

Es gibt keine in Stein gemeißelten Regeln, nach denen man als Shownotes-Autor zu handeln hat. Was man aufschreibt, hängt von den Persönlichkeiten der Schreiber, dem Zielpublikum, eventuellen Vorgaben und Wünschen der Podcaster, der zur Verfügung stehenden Aufmerksamkeit und anderen Dingen ab. In jedem Falle sollen Shownotes – man erinnere sich an den Anfang dieses Dokuments – einen Nutzen bilden und nicht als Abladehalde für alles Mögliche dienen.

Sinnvolle Inhalte sind …

- (Komplett ausgeschriebene) Namen
	- von genannten Personen, Orten, Produkten, Filmen, …
- Anspielungen
	- »Ins Essen gequatscht.«
	- Jan traf sich mit einer jungen Frau, die er bei Facebook kennengelernt hatte, im Steigenberger-Hotel in Düsseldorf
	- »Scheiße mit der Scheiße hier.«

Freundlich ist es natürlich, kurze Erklärungen mitzuliefern.

- Fakten aus dem Leben der Podcaster
	- Annett mag Bananen mit Kakaopulver
	- Tobias ist Mitglied beim THW
	- Rüdiger besitzt eine Wohnung in der Mannheimer Innenstadt

- Fremdwörter und Redewendungen (die die breite Masse nicht unbedingt kennt)
	- your mileage may vary
	- Parallelepiped
	- coram publico
	- Suade

- Stichworte zum inhaltlichen Verlauf, durchaus auch in Satzform – die dann aber ohne Punkt am Ende, siehe oben
	- Birgit schlägt vor, in Zukunft einen anderen Raum zu benutzen
	- Tanja warnt vor grundlos erteilten Berechtigungen
	- Vernon meint, Coverversionen seien manchmal viel besser als das Original
	- Daniela hat mit Cabriolets bisher nur gute Erfahrungen gemacht
	- Steffi findet, man müsse sich sein persönliches Netzwerk aufbauen
	- Ina erklärt, wie der Bewerbungsprozess ungefähr abläuft

    (Beachte aber dazu die im nächsten Abschnitt vorgestellten Einschränkungen.)

- Korrekturen von gemachten Aussagen
	- Der von Jürgen gesuchte Komponist ist nicht Ralf Siegel, sondern Kurt Cobain
	- Entgegen Eriks Aussage wurden tatsächlich nur drei Systeme umgestellt

- Zitate

### Stilfragen – Wie man gut schreibt und was man lassen sollte

Wie so oft im Leben ist es mit dem alleinigen Angeben von Inhalten, die zum Beispiel anhand der Ideen im vorherigen Abschnitt zusammengetragen wurden, nicht getan. Für eine gute und einheitliche Präsentation braucht man weitere Regeln.

- Shownotes werden grundsätzlich im in der Gegenwartsform (Präsens) verfasst.
- Jedes Item beginnt (hinter der Zeitmarke) in der Regel mit einem Großbuchstaben.
- Bitte nicht indirekte Rede mit Zitaten mischen. (Sollte man generell nicht tun.)
- Zwischen Zollzeichen gehören nur echte Zitate, keine sinngemäßen Aussagen (eventuell hinterher nochmal genauen Wortlaut prüfen). Bei Zitaten muss man darüber hinaus darauf achten, nichts aus dem Zusammenhang zu reißen und dadurch falsch oder missverständlich darzustellen. Eventuell hilft ein kurzer Zusatz zur Klarstellung. Außerdem sollte man sich darauf beschränken, nur Wichtiges zu zitieren. Schauen wir uns ein paar weniger gute Beispiele an:
	- »Aber muss man doch mal sagen.« (Toby) – Dieses Zitat ist ohne das, was man angeblich doch mal sagen müsse, wertlos, kann also eigentlich weg.
	- »Das Wichtigste ist, zuhören.« (Toby) – Auch hier fehlt der Zusammenhang. Im Gegensatz zum ersten Punkt kann man hier bestimmt schnell was ergänzen, etwa so: (Toby über Personalführung)
	- »Ich bring dir einen Salzstreuer mit für meine Wunden.« (Holgi) – Man müsste ein Item davor einfügen, um zu erklären, wie Holgi zu seiner Aussage kommt. Irgendwas zum Draufstreuen muss Holgis Gesprächspartner ja aufgerissen haben.
	- »Wasserflaschenersatzpodcast« (Toby) – Schwer zu sagen, ob jemand gezielt nach solchen Zitaten sucht, was ja grundsätzlich schon mal ein Grund fürs Festhalten wäre. Vermutlich tut’s aber niemand, deshalb ist so ein vermeintlich lustiges Wort eher ein Fall für die Mülltonne. Es sei denn, man erklärt …

	Gut sind immer Zitate, die für sich stehen können und keiner weiteren Erklärung bedürfen:
	
	- Das Gerücht, nach dem eine Reihe schon deshalb konvergieren muss, weil die Reihenglieder den Limes 0 haben, hält sich hartnäckig, wird dadurch aber nicht wahrer. (Klaus Wirthmüller)
	- Niemand beherrscht alles gleichermaßen gut – zum Glück, sonst würden die anderen ihn erschlagen. Denn der Mensch erträgt keine Vollkommenheit. Deshalb sollte er sie bei sich selbst auch gar nicht erst vermuten. (Heiko Mell)
	- Irgendwann fängt jeder an zu stinken. (Daniel Weber)

- Nur aufschreiben, was auch verständlich und klar ist. Bei einer Aussage wie »Man kann es nie allen Recht machen« ist – abgesehen davon, dass es sich um eine Binsenweisheit handelt – zum Beispiel nicht klar, ob die Podcaster nach einer Diskussion zu dieser Erkenntnis (diesem Konsens) kamen oder ob es die Aussage eines Einzelnen ist. Im letzten Fall wäre ein Zitat (siehe oben) besser. Auch diese Stichpunkte hier (echten Shownotes entnommen) sind verbesserungswürdig:
	- »Schwierig, in diesem Thema den Überblick zu behalten«
	- »Religion befriedigt Bedürfnis nach Sicherheit«
	- »Einfluss des Königs in Thailand« – Ist zwar ein Teil der Inhaltsangabe, aber ein wenig mager.
	- »Serviceorientierter Reisepodcast« – Was soll man damit anfangen?

	Im Idealfall sind Shownotes ein von der Film- oder Tonquelle wenigstens halbwegs unabhängiges Werk, das eigenständig für sich steht und verständlich ist. Oder sie halten abschnittsweise einfach nur (mit Verweisen hinterlegte) gefallene, aber ohne weitere Erläuterung hilfreiche Schlagworte fest. Beispiel: Spiegelkabinett; Lachkabinett; Phantasialand; Geister-Rikscha; Ständige Vertretung; Hollywood Tour.

- Nicht jedes Detail aufschreiben, das über den Äther geht, sondern das, was einen konkreten Nutzen hat. Jede unspektakuläre Kleinigkeit festzuhalten (»Aileen wird verabschiedet«, »Max hat das Glas leergetrunken und schenkt sich neu ein« oder schlicht »Begrüßung«) ist unnötig und nicht zielführend. Von Telefonverbindungsabbrüchen oder Rauswürfen in Radiosendungen zu berichten ist da schon sinnvoller.

- Aussagekräftige oder wenigstens originelle Abschnittsüberschriften verwenden. Den erstes Teil einer Ausgabe mit »Intro« zu betiteln gibt nur dann Sinn, wenn er auch tatsächlich nur die Eröffnung enthält. Dauert die bei einer einstündigen Episode aber schon 15 Minuten, also ein Viertel der Gesamtzeit, ist zumindest mal zu überlegen, ob man da nicht feiner unterteilen kann. Ähnliches gilt für »Outro«.

- Relative Zeitangaben sind suboptimal, gerade bei aufgezeichneten Episoden (bei Podcasts also immer). Wenn ein Podcaster sagt, er sei »gestern« im Supermarkt gewesen, ist für die Shownotes daraus zum Beispiel »am Tag vor der Aufzeichnung« zu machen. Aus der letzten Woche wird die Vorwoche. Und so weiter.

- Wichtig ist auch, einen Podcast einigermaßen gleichmäßig abzudecken. Über eine minutenlange Diskussion nichts zu schreiben, dann aber etwas festhalten, was ein Podcaster in einem Halbsatz erwähnt hat (»Andreas hat neulich mal Curry King probiert.«), erzeugt ein falsches Bild. Natürlich kann es mal schwierig werden, Inhalte angemessen darzustellen, etwa bei schnellen Themenwechseln oder komplizierten Argumentationsketten. In solchen Fällen ist es möglich, sich durchs Beschreiben mittels Oberbegriffen abzuhelfen (siehe fünfter Punkt): Klimapolitik, Freundschaft, Jugendschutz, Maßtheorie …

- Jeder Verweistext sollte für sich selbst sprechen. (Wieder etwas, das man generell beachten sollte.) Einfache Unbeispiele: Item enthält ausschließlich den Text »in der Wikipedia« oder »der erwähnte Artikel« – danach kann man schlecht gezielt suchen. Außerdem sieht man nicht auf Anhieb, was genau gemeint ist. Und wenn im Podcast nicht explizit vom Wikipedia-Artikel die Rede ist, braucht man die Shownotes mit der Quelle nicht unnötig aufzublähen. Falls man ausnahmsweise in die Verlegenheit kommt, zu einem Namen, Stichwort oder Sachverhalt mehrere Items aufschreiben zu müssen, ist es ganz gut, erst den (immer gleichen) Text und dahinter in Klammern die unterschiedlichen Angebote zu notieren: Voll normaaal (Wikipedia); Voll normaaal (IMDb).

Jedes Item muss darüber hinaus so gestaltet sein, dass es auch noch ohne URL Sinn ergibt, zum Beispiel ausgedruckt.

- Keine URL verwenden, die möglicherweise nur kurze Zeit gültig sind. Verweise auf etwa eine Mediathek sind kritisch zu sehen, weil die Filmbeiträge nach einer Woche wieder verschwunden sein können. Wikipedia ist (bei allen Vorbehalten) eigentlich eine sichere Bank, weil die Einträge dort Bestand haben und man viele weitere Verweise (nach außen) findet. Wegen Letzterem kann man sich entsprechende Auflistungen in den Shownotes sparen – vor allem doppelte, siehe vorheriger Punkt.

Weiter kann es passieren, dass ein Angebot im Netz verschwindet. Dann hat ein Wikipedia-Artikel den Vorteil, dass er nicht automatisch ebenfalls verloren geht, sondern bestehen bleibt und Geschichte sowie das Entschwinden des im Artikel beschriebenen Dienstes erklärt, er also im Nachhinein weiterhin einen Nutzen für den Leser bietet.

Bitte keinen Gebrauch von URL-Aliase (Bit.ly, Tinyurl.com, Ow.ly, ShortURL.de, …) machen.

- Es spricht nichts dagegen, Zusatzinformation einzubauen:

	- »Diese Frage wurde in der Ausgabe des Monats Mai übrigens schon behandelt« – Dazu dann die URL zur entsprechenden Podcast-Ausgabe servieren.

	- »Das von Florian erwähnte Produkt gibt es, nebenbei bemerkt, sehr günstig bei … zu kaufen«

	Allerdings geht es nicht darum, den Lesern ein Rundum-sorglos-Paket zu schnüren. Vielmehr sollen die Shownotes Ausgangspunkt für weitergehende Recherchen und Abschweifen sein. Selber denken macht schlau.

- URLs von Produktseiten bei Amazon kann man immer auf eine kompakte Form wie bei http://www.amazon.de/dp/B000VDG3G6 bringen. Um die Übersicht zu erhöhen, sollte man das auch praktizieren.

- Jeder Item sollte pro Dokument nur einmal vorkommen. Mehrmals Andreas Gabalier oder Bauschaum aufzuführen ist unnötig.

- Auf korrekte Rechtschreibung und Zeichensetzung ist zu achten. Dummheit und Faulheit sind keine Ausreden. 

- Überhaupt empfiehlt sich eine Prüfung des Geschriebenen. Wer Zeit und Lust hat, hört sich die Podcastausgabe nochmal an und hat dazu im Idealfall einen privaten Mitschnitt sofort, vor der offiziellen Veröffentlichung vorliegen. Man glaubt gar nicht, was man alles beim ersten Mal falsch versteht oder überhört. Dabei ist zu beachten, dass man Zeitmarken hinterher manuell einsetzen muss. Denn `###` plus Leerzeichen liefert die jeweils *gerade aktuelle* Unixzeit, die unter Umständen sehr große Differenzen zu bereits vorhandenen Angaben aufweist. Wer nicht achtgibt, erhält hässliche Zeitsprünge innerhalb des Dokuments.

Sollte es bei Livesendungen zwischendurch mal Probleme mit dem Stream gegeben haben, gibt es keinen Grund, das Versäumte nicht nachzutragen – damit solche Bemerkungen wie »Streamabriss« nur vorübergehend bestehen. Denn die Podcastshörer interessieren Übertragungsprobleme nicht, wenn man in der heruntergeladenen Episode nichts davon hört. Anders ausgedrückt: Die Vollständigkeit von Shownotes soll letztlich nicht davon abhängen, wie die Autoren die jeweilige Podcastausgabe konsumiert haben.

- Um mehr Hintergrundwissen und -material (Verweise) zu haben, ist hilfreich zu verfolgen, was die Podcaster sonst so veröffentlichen, etwa in eigenen Blogs oder bei Mikroblogging-Diensten. Wenn jemand erzählt, dass sie oder er am Vortag ein lustiges Plakat gesehen hat und man als Shownotes-Autor weiß, dass es dazu einen Tweet mit Bild gibt, kann man den einbinden, damit sich alle noch Unwissenden einen Eindruck verschaffen können. Gleiches gilt für Anspielungen oder Verweise auf ältere Podcastausgaben. 

### Sonderwünsche der Podcaster oder Regeln für gewisse Podcasts

- NSFW (†), Freakshow: Anfangs- und Abschlussmusik bitte in eigene Kapitel packen, diese »Intro« bzw. »Outro« taufen. 

- Realitätsabgleich (WRINT): Nachrichtenüberschriften von Deutschlandfunk-Website kopieren (aber nicht URL hinter Überschriften legen), Wetter am Ende im Volltext übernehmen und nur mündlich vorgetragene Datumsnennung ergänzen, damit es ein echtes Zitat werden kann. Holgis Gesprächspartner darf man beim Eintragen der Podcaster ruhig Toby nennen. 

- Wrintheit (WRINT): Material bis zu den Fragen gehört üblicherweise in ein Kapitel, die weiteren Überschriften bestehen aus den Fragen. Bei zu langen Fragen wirklich nur den Kern hinschreiben (Beispiel: »Was haltet ihr davon?«), auch wenn dadurch Unklarheiten bleiben.

Erstellt von mathepauker

