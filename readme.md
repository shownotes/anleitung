# Anleitung

### Grundsätzliches

Der Begriff *Shownotes* ist ein Kompositum aus den englischen Wörtern *show* und *notes* und bezeichnet Begleitnotizen zu Audio- und Videoproduktionen, insbesondere Podcasts und Hörfunksendungen.
Allgemein betrachtet handelt es sich um eine Mischung aus Stichpunkten, Inhaltsangaben, Zitaten und weiterführenden Informationen.
Diese Notizen können aus folgenden Gründen nützlich sein:

- Während des Hörens kann man bequem auf eingebaute Verweise zurückgreifen und muss nicht selbst suchen.
- Ein Podcast mit Shownotes kann von Suchmaschinen besser gefunden und eingeordnet werden.
- Die Einteilung einer Sendung in Kapitel sorgt für Übersicht und Struktur.
- Jemand möchte sich vor dem Hören einen Überblick verschaffen, um dann zu entscheiden, ob sich ein Hören überhaupt lohnt.
- Hörgeschädigte werden nicht gänzlich ausgeschlossen.

### Womit man schreiben kann

Damit mehrere Autoren gleichzeitig an einem Dokument arbeiten können, muss der Podcast von allen Shownotern gleichzeitig gehört werden, beispielsweise wenn er Live oder als ReLive über Xenim ausgestrahlt wird.
Die Startseite von shownot.es zeigt alle Live-Podcasts an, die im Kalender der *Hörsuppe* (http://hoersuppe.de) eingetragen sind und bietet dafür die schnelle Erstellung eines sogenannten *ShowPads* an.

Um das zu tun und überhaupt mit dem ShowPad arbeiten zu können, ist ein Benutzerkonto notwendig.
Das gibt es nach einer Registrierung kostenlos. Zu den dem System bekannten Podcasts dürfen sich die Benutzer selber Pads erstellen. Man sich jederzeit vom Shownotes-Team für noch nicht im Hörsuppenkalender vorhandene Podcasts ShowPads anlegen lassen. Dazu genügt es, im Chatraum (\#shownotes bei Freenode) vorbeizuschauen.

Das eben erwähnte Kernteam kümmert sich, nebenbei gesagt, hauptsächlich um Entwicklung, Administration und Betrieb der Plattform.

### ShowPad in Kürze

*****

Egal ob man ein Pad selber angelegt oder eines angelegt bekommen hat – die Adresse ist von der Form https://shownot.es/podcastname/625, im Bearbeitungsmodus um ein /edit/ ergänzt. Ruft man ein jungfräuliches Pad auf, ist außer einer Zeilennummer noch nix zu sehen. Rechts gibt es einen Chat, mit dem sich die Schreiber während der Arbeit austauschen können.

Zunächst sollte man die Namen der Podcaster einzutragen. Wenn man mitgeholfen hat, kann man sich als Shownoter eintragen.

Man kann das Pad wie einen einfachen Editor benutzen. Jeder registrierte Benutzer kann sich bei seinen persönlichen Profil-Einstellungen eine beliebige Farbe aussuchen, mit der seine Textbeiträge (auch im Chat) hinterlegt werden, damit man erkennen kann, wer was beigetragen hat. Idealerweise sind die Farben so ausgesucht, dass man verschiedene Autoren klar voneinander unterscheiden kann und alles noch leicht lesbar ist.

Das ShowPad bietet aber mehr als simple Editorfunktionen! In Shownotes ist es nützlich, wenn man weiß, zu welchem Zeitpunkt eines Podcastes ein bestimmter Teil des Inhalts gehört. Irgendwie muss also die Zeit vermerkt werden. Standardmäßig arbeitet das ShowPad dazu mit der Unixzeit. Die aktuelle bekommt man durch Schreiben von `###` und direkt danach einem Leerzeichen. In den fertigen Shownotes werden später alle Zeitmarken relativ zur ersten im Quelltext vorkommenden Zeitangabe vor einer Überschrift berechnet.

Hinter die Zeitmarke kommt der eigentliche Inhalt. Das sieht dann etwa so aus:

`1397473197 Schloss Neuschwanstein`

Möchte man dem noch eine Information hierarchisch unterordnen, so geschieht dies mit einem Bindestrich vor der eigentlichen Information:

`1397473197 Schloss Neuschwanstein`

`- Hohenschwangau (wo das Schloss steht)`

Die Kombination aus Zeitmarke und weiteren Informationen heißt übrigens *Item*. Jedem Item darf höchstens eine URL zugeordnet werden. Diese gehört zwischen Vergleichszeichen hinter den Text:

`1397473197 Schloss Neuschwanstein <https://de.wikipedia.org/wiki/Schloss\_Neuschwanstein\>`

`- Hohenschwangau (wo das Schloss steht) <https://de.wikipedia.org/wiki/Hohenschwangau\>`

Hinter einzelne Worte innerhalb eines Items kann kein Verweis gelegt werden. So was hier ist also nicht zulässig:

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

`#r` oder `#revison` Dieses Item muss noch überarbeitet werden. 

Einige der Tags sind nur in Verbindung mit einer zusätzlich angegebenen URL sinnvoll.

Die Tags sind nochmal in der [Referenz](https://github.com/shownotes/anleitung/blob/master/referenz.md) zusammengefasst.

Mit Tags könnte unser Beispiel von oben so aussehen:

`1397473197 Schloss Neuschwanstein <https://de.wikipedia.org/wiki/Schloss\_Neuschwanstein\> #g`

`- Hohenschwangau (wo das Schloss steht) <https://de.wikipedia.org/wiki/Hohenschwangau\> #g`

Man darf aber eben auch mehrere Tags setzen:

`1397473082 Köln-Urlaub <https://de.wikipedia.org/wiki/Köln\> #g #c`

Ans Ende eines Items kommt kein Punkt.

Zitate gehören zwischen Anführungszeichen (`"`), die später automatisch in richtige Anführungszeichen verwandelt werden. Der Urheber wird meist in Klammern dahinter geschrieben. Entweder notiert man vollständige Sätze:

`1117913729 "Vanilleeis sollte ein Grundrecht sein!" (Stefan Schneidereit) #q`

Diese Sätze sollen mit einem Punkt/Ausrufezeichen/Fragezeichen vor dem abschließenden `"` enden.

Oder man schreibt nur ausgewählte Worte auf:

`0985331825 Max findet Kirschkuchen "total abgefahren" #q`

In jedem Falle sollte aber erkennbar sein, wer zitiert wird.

Bitte nur dann Zitate einfügen, wenn sowohl der Urheber als auch der genaue(!) Wortlaut sicher feststehen. Die Nachbearbeitung falscher Zitate ist äußerst zeitaufwändig.

Noch ein technischer Hinweis: Zwischendurch sollte man schauen, ob die selbst erzeugten Zeitmarken zu denen der anderen Autoren passen. Bestehen große Abweichungen, liegt ein Problem vor, das man mit einer Korrektur der lokalen Systemzeit beheben kann.

Zwischenspeichern muss man übrigens nicht, das geschieht automatisch.

Und wenn alles fertig ist? Dann muss ein Befugter die Shownotes erst *sichten* und damit quasi freischalten. Um Shownotes zur Sichtung vorzuschlagen, gibt es oben eine eigene Schaltfläche. Nach erfolgreicher Sichtung können die Podcaster die Shownotes mittels eines Plugins in ihr Blog (WordPress) einbauen. Unabhängig davon ist das Dokument unter der anfangs genannten URL erreichbar. In beiden Fällen entsteht ein für den herkömmlichen Leser genießbarer Hypertext mit Zeitangaben in Tooltips.

Mit dem Schreiben von Shownotes verzichtest du übrigens auf sämtliche Schutzrechte und übergibst das Werk in die Gemeinfreiheit, Stichworte: CC0, Public Domain.

### Wie anfangen?

Wer sich noch nicht traut oder unsicher ist, kann sich gerne angucken, wie Shownotes entstehen. Dazu einfach während einer Livesendung das zugehörige Pad aufrufen und verfolgen, was geschieht. Und keine Berührungsängste haben! Erst mal nur ein paar URLs beisteuern oder Rechtschreibfehler korrigieren hilft ungemein.

Bitte keinen Gebrauch von URL-Aliase (Bit.ly, Tinyurl.com, Ow.ly, ShortURL.de, …) machen.

Gekürzte und geänderte Version des Textes von mathepauker
