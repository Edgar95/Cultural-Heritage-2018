# Cultural-Heritage-2018
# Künstliche Intelligenz und Cultural Heritage: Upper Brandberg - Im Louvre der Felsmalerei
# Gruppe Object Detection - Fritz, Fischer, Casters, Pöschel


# Ziel:
-     Grundlage: Programm soll Input in Form von Bildern/Abbildungen/JPEG etc. verarbeiten können.
-     Zwischenziel: Programm soll zwischen Objekt und Mensch differenzieren können.
-     Endziel: Programm soll Objekte erkennen, benennen und differenzieren können.


# Projektbeschreibung

Unsere Gruppe, bestehend aus Sören Pöschel, Edgar Fritz, Annika Fischer und Anna Casters, beschäftigt sich mit der Objekterkennug der Felsmalereien. Zunächst ist eine Differenzierung zwischen Mensch (human) und Objekt wichtig. Unter Objekt verstehen wir alles, was nicht menschlich ist. Hierzu gehören sowohl Waffen und Ausstattung als auch Körperschmuck und Kleidung. Der Fokus liegt also auf den unterschiedlichen Objekten, die in Verbindung zu den abgebildeten Menschen stehen.

Im ersten Schritt haben wir eine Bilderdatenbank erstellt. Hierfür wurden geeignete Figuren und Szenen aus den uns zur Verfügung gestellten Scans ausgeschnitten. Unsere Bilddatenbank beinhaltet einzelne Menschen ohne jegliche Objekte (nur der menschliche Körper), alle Objektarten als Einzelbilder und Figurszenen, also Abbildungen der Interaktionen der Menschen mit Objekten. Hierbei sind Abbildungen gemeint, auf denen Menschen Objekte zweckgemäß nutzen. Diese Bilder sind im Jpeg-Format nach einer bestimmten Struktur abgespeichert: AmisNummer_Figurnummerierung_Plate_Fix_Stichwort zur Abbildung --> Beispiel: A38_480_7_N_human/arrow. Mehrere Figuren: A34_239-245_9_M_human/Perücken. Dies ist besonders für die spätere Zuordnung von Vorteil. 
Das Programm soll lernfähig sein. Beispiel: In der Bilddatenbank befinden sich mehrere Bilder, die einen Bogen aufzeigen. Durch das Abgleichen mehrerer Bogenbilder soll ein Bogen in einem größeren Kontext wiedererkannt werden. Anhand mehrerer Bogenabbildungen lernt das Programm also wie ein Bogen aussieht und soll somit fähig sein diesen auf allen anderen Bildern (Abbildungen von Mensch mit Objekt) zu erkennen. Unsere 13 Klassen zur Objekterkennung lauten: human, arrow, bag, bow, club, instrument, stick, headdeco, penisatt, kaross, shoe, pendants und apron. Durch das Training der verschiedenen Bilder, kann unser Programm nun erknenn zu viel Prozent es sich tatsächlich um das besagte Objekt oder einen Menschen handelt. Die Ausgabe zeichnet Quadrate um die erkannten Menschen und Objekte.



# Technologien:
- Tensorflow
- LabelImg
- Python
- Jupyter


# Schwierigkeiten
Oft sind die Objekte im Menschen verwachsen und eine klare Unterscheidung von Anfang und Ende des Objekts oder des Menschen ist nicht möglich. Dies kann für das Programm und unsere Programmierung zu einem Problem werden. Gerade Kleidung oder Körperschmuck wie Perücken sind nicht klar abgrenzbar.

