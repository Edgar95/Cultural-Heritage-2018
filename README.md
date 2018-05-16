# Cultural-Heritage-2018
# Künstliche Intelligenz und Cultural Heritage: Upper Brandberg - Im Louvre der Felsmalerei
# Gruppe Fritz, Fischer, Casters, Pöschel



# Zwischenstand
# Ziel:
-     Grundlage: Programm soll Input in Form von Bildern/Abbildungen/JPEG etc. verarbeiten können.
-     Zwischenziel: Programm soll zwischen Objekt und Mensch differenzieren können.
-     Endziel: Programm soll Objekte erkennen, benennen und differenzieren können.


# Anmerkungen
Tensorflow funktioniert zurzeit nur auf unseren Windows-PCs

# Projektbeschreibung

Unsere Gruppe, bestehend aus Sören Pöschel, Edgar Fritz, Annika Fischer und Anna Casters, beschäftigt sich mit der Differenzierung zwischen Mensch (human) und Objekt. Tiere werden hierbei nicht beachtet. Unter Objekt verstehen wir alles, was nicht menschlich ist. Hierzu gehören sowohl Waffen und Ausstattung als auch Körperschmuck und Kleidung. Da der Fokus auf den unterschiedlichen Objekten liegt, ist das Geschlecht der abgebildeten Menschen unwichtig.

- Vorgehen

Im ersten Schritt haben wir eine Bilderdatenbank erstellt. Hierfür wurden geeignete Figuren und Szenen aus den uns zur Verfügung gestellten Scans ausgeschnitten. Wichtig ist die Nummerierung der einzelnen Figuren im Bild zu haben, damit die Klassifizierung und Zuordnung innerhalb der Höhlenmalereien nicht verloren geht. 
Auf den Bildern sollten bestenfalls keine Tiere zu sehen sein, da diese für unsere Arbeit irrelevant sind. Unsere Bilddatenbank beinhaltet einzelne Menschen ohne jegliche Objekte (nur der menschliche Körper), alle Objektarten als Einzelbilder und Figurszenen, also Abbildungen der Interaktionen der Menschen mit Objekten. Hierbei sind Abbildungen gemeint, auf denen Menschen Objekte zweckgemäß nutzen. Diese Bilder sind im Jpeg-Format nach einer bestimmten Struktur abgespeichert: AmisNummer_Figurnummerierung_Plate_Fix_Stichwort zur Abbildung --> Beispiel: A38_480_7_N_human/arrow
Mehrere Figuren: A34_239-245_9_M_human/Perücken
Dies ist besonders für die spätere Programmierung wichtig. Das Programm soll lernfähig sein. Beispiel: In der Bilddatenbank befinden sich mehrere Bilder, die einen Bogen aufzeigen. Durch das Abgleichen mehrerer Bogenbilder soll ein Bogen in einem größeren Kontext wiedererkannt werden. Anhand mehrerer Bogenabbildungen lernt das Programm also wie ein Bogen aussieht und soll somit fähig sein diesen auf allen anderen Bildern (Abbildungen von Mensch mit Objekt) zu erkennen. 

- Ziele

Als Grundlage muss das Programm Bilder erkennen können, also das JPEG-Format muss verarbeitet werden können. Im zweiten Schritt soll eine grobe Unterscheidung zwischen Mensch und Objekt möglich sein. Das Programm muss verstehen, dass auf den Abbildungen sowohl ein Typ „Mensch“ und ein Typ „Objekt“ zu sehen sein kann. Ebenfalls muss das Programm erkennen, dass es auf den Abbildungen Zahlen (Figurzahl) gibt, welche weder Mensch noch Objekt und für die Bildanalyse unbedeutend sind. 
Sofern dies funktioniert, versuchen wir im nächsten Schritt die einzelnen Objekte zu kategorisieren. Die Kategorien sind: Waffen, Ausstattung, Körperschmuck und Kleidung. Sofern Objekte zu den einzelnen Kategorien zugeordnet werden konnten, soll im Endziel eine genaue Definition des Objekts möglich sein. Dies wird mit einem Prozentwert dargestellt. Wenn das Programm auf einer Abbildung einen Bogen in der Kategorie „Waffen“ erkannt hat, wird das Programm ebenfalls sagen können zu wie viel Prozent es sich tatsächlich um einen Bogen handelt. 
Dies könnte dann in etwa so aussehen: 
 
(Quelle: https://github.com/tensorflow/models/tree/master/research/object_detection)

Als Endziel soll unser Programm also Objekte erkennen, vom Typ „Mensch“ differenzieren können und die Objekte einzeln erkennen, benennen und zuordnen können.
Oft konnten viele Objekte noch nicht klar definiert werden. Vielleicht ist es möglich mithilfe unseres Programms undefinierte Objekte zu definieren, bzw. mit einer Prozentangabe eine mögliche Zuordnung zu geben. 

- Technische Mittel

Für das Projekt haben wir TensorFlow ausgewählt, da es sich gerade für Künstliche Intelligenz und maschinelles Lernen sehr gut eignet. Als Programmiersprache werden wir statt C++ Python benutzen. 
Als Programmiergrundlage werden wir uns zunächst auf dieses Beispiel stützen: https://github.com/tensorflow/models/tree/master/research/object_detection

- Schwierigkeiten

Oft sind die Objekte im Menschen verwachsen und eine klare Unterscheidung von Anfang und Ende des Objekts oder des Menschen ist nicht möglich. Dies kann für das Programm und unsere Programmierung zu einem Problem werden. Gerade Kleidung oder Körperschmuck wie Perücken sind nicht klar abgrenzbar.

