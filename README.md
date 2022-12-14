# Homer in Ohio

    Ein Projekt von Mohammad Rezaei und Michael Markwart

https://user-images.githubusercontent.com/111492177/204910169-c294b6ca-6462-4ccb-9723-dcf5b354c669.mp4

- [Einführung](#einf)
- [Regeln und Ziele](#regeln)
- [Wichtige Objekte](#konzept)
- [Blogeinträge](#blog)
- [Fazit](#fazit)
- [Zu Starlogo](#starlogo)
- [Eigenständigkeitserklärung](#eigenst)

## <a name="einf"></a>Einführung

Zuhause gibt es kein Spiel, das du noch nicht durchgespielt hast, und du hast Langeweile? Dann haben wir genau das richtige Spiel für dich: „Homer in Ohio“.             Hilf Homer durch ein Stadtlabyrinth mit zahlreichen und gefährlichen Hindernissen, um seine Frau Marge aus den Flammen zu retten.

Zuerst musst du den rotierenden Sonic   überwinden und später werden drei sich bewegende gigantische Würfel versuchen deinen Weg zu versperren. Wenn du sie überwunden hast, wirst du mit zwei Wegen konfrontiert; du musst dich   entscheiden, ob es rechts oder links weitergeht. Ein Weg führt in eine Sackgasse, wo dich ein blutrünstiger Clown erwartet, der dich aus dem Spiel eliminieren will.     
Hast du dich jedoch für den richtigen Weg entschieden, stehst du jetzt vor zwei Fragen bei denen es um Leben und Tod geht. Wenn du es bis hierhin unversehrt geschafft   hast, stehst du jetzt vor einer Menge hirnloser Monster, die alles auf ihrem unwillkürlichen Weg töten wollen. Du hast jetzt die Möglichkeit sie abzuschießen und        deine Frau Marge aus den Flammen zu retten!

Viel Spaß und Erfolg!

Hier kannst du den StarlogoTNG Installer und das Homer in Ohio Projekt downloaden:
https://www.mediafire.com/folder/yhre6hm9z1wijam,b4tsycygr2izwdp/shared

## <a name="regeln"></a>Regeln und Ziele

Das Spiel "Homer in Ohio" verweist auf keine expliziten Regeln. Der Spieler ist also frei zu entscheiden, wobei er das Ziel zu überleben hat, um Marge aus dem Feuer zu retten. Wichtig ist die Anweisungen vom Info-Bär zu folgen.


## <a name="konzept"></a>Wichtige Objekte
In diesem Abschnitt werden Code und Funktion der wichtigsten Agenten des Spiels erklärt.

<details>
    <summary> Homer</summary>

Homer ist der Hauptcharakter, der vom Spieler gesteuert wird. Er muss versuchen, die Hindernisse zu überwinden und unversehrt das Labyrinth zu durchqueren, um zu seiner Frau Marge zu gelangen.
   
    
| Code | Funktion | 
| ------ | ------ |
| ![image](https://user-images.githubusercontent.com/111492177/207665527-5afd29e9-d634-4ff6-944d-b6967524de1e.png)(Abb.1) | Man steuert Homer mit den Tasten WASD, was recht selbsterklärend ist; Mit A und D kann man sich drehen und mit W und S vor- bzw. rückwärts laufen. Es wird also z.B. getestet, ob W gedrückt wird und wenn dies der Fall ist, läuft Homer vorwärts. Die Geschwindigkeit kann man ändern, indem man die Schrittanzahl vergrößert oder verkleinert. |
| ![image](https://user-images.githubusercontent.com/111492177/207668070-fef8f8f7-6e65-4f5c-8b2f-7fd252efa06b.png)(Abb.2) ![image](https://user-images.githubusercontent.com/111492177/207893848-7827bed0-91d9-4700-adc9-552583a13a30.png)(Abb.3)| Das ist der Code für das Erscheinen der Paintballs. Sobald man Leertaste drückt, wirft Homer einen Paintball, der mit der Hatch-Funktion in's Leben gerufen wird. Die Bewegung des Paintballs sieht so aus, dass er sich konstant mit einer Geschwindigkeit von 3 bewegt und zufällig entweder 2 Grad nach links oder 2 Grad nach rechts ausrichtet. |
 
</details>   
<details>
    <summary> Sonic</summary>

    
Sonic ist das erste Monster, das sich Homer in den Weg stellt, oder wohl eher läuft. Er rennt die ganze Zeit überaus schnell um einen Häuserblock herum, sodass es schwierig werden kann ihm auszuweichen.


| Code | Funktion | 
| ------ | ------ |
| ![image](https://user-images.githubusercontent.com/111492177/207672300-c8200085-afa3-48d7-81f4-b0517d4f9a13.png) (Abb.1) | Das "Forward 18" und "Left 90" werden in Dauerschleife abgespielt, sodass Sonic immer im Kreis um die beiden Häuser läuft. Es ist sehr wenig, aber effektiver Code. |
| ![image](https://user-images.githubusercontent.com/111492177/207672776-fe8188d2-5c3d-4064-b9a2-1b4b9d852ea7.png) (Abb.2) | Sobald Homer mit Sonic, also monster1, kollidiert, stirbt er. |


 </details>   
<details>
    <summary> Die drei Würfel</summary>

Die drei Würfel bewegen sich die ganze Zeit auf einer Strecke hin und her und sind sehr groß, weswegen man im richtigen Moment hindurchlaufen sollte, um nicht zermalmt zu werden.

| Code | Funktion | 
| ------ | ------ |
| ![image](https://user-images.githubusercontent.com/111492177/207937214-c7347392-90ef-4535-a414-55aca63af432.png) | Damit die Würfel sich in einer Dauerschleife hin- und herbewegen, arbeiteten wir mit der Ifelse Funktion. Als Test haben wir einen Remainder gesetzt. Dieser hat die Funktion die gezählten Schritte durch 12 zu teilen. Solange der Rest weniger als 6 ist, bewegen die Würfel sich vorwärts, wenn aber der Rest größer als 6 ist bewegen sie sich rückwärts. Der Schwierigkeitsgrad dieses Moduls kann verändert werden, indem man die Geschwindigkeit der steps bei "forward" und "back" verändert. |
|  | ![image](https://user-images.githubusercontent.com/111492177/207927163-15ee88e4-4e1d-4d67-ba75-38d1d7b8788e.png)|


 </details>      
<details>
    <summary> Der verrückte Clown</summary>    
    
Der verrückt gewordene Clown ist sehr hinterhältig. Sobald er Homer um die Ecke kommen sieht, setzt er seinen schweren Körper in Bewegung, um ihn zu zermalmen.
    
| Code | Funktion | 
| ------ | ------ |
| ![image](https://user-images.githubusercontent.com/111492177/207674089-12e6f2b1-4177-4d93-9b2c-d3c4b8cfb9f6.png) | Die Bewegung des Clowns beinhaltet genau dieselbe Funktion, wie die der Würfel, mit der Bedingung, dass der Clown sich erst in Bewegung setzt, sobald vor der Ecke mindestens einer der Grasbüschel zerstört wird. |

 </details>   
 <details>
    <summary> Die zwei Fragen</summary>

Die beiden Fragen sind vom Inhalt her sogenannte "Idiotenfragen". Es gibt zwei Fragen, jeweils drei Antworten und jeweils eine richtige Antwort. Wenn man eine falsche Antwort auswählt, stirbt Homer und wird wieder an den Anfang des Labyrinths gebracht. 
    
| Code | Funktion | 
| ------ | ------ |
| ![image](https://user-images.githubusercontent.com/111492177/207677719-b8281202-2f3e-474e-b934-e45eb0c23250.png) | Das Programm zählt, wie viele richtige Antworten es gibt. Bevor man sie ausgewählt hat, gibt es, natürlich, nur eine richtige Antwort. Sobald man diese richtige Anwort auswählt, verschwindet sie, sodass es jetzt 0 richtige Antworten gibt. Sobald dies geschieht, verschwindet das Tor. |
  
</details>
<details>
    <summary> Die Monster</summary>

Die Monster befinden sich im letzten Part des Spiels. Sie bewachen die Umgebung um das Feuer herum. Diese Umgebung ist von Wänden eingegrenzt, durch welche die Monster nicht hindurchlaufen können.
    
| Code | Funktion | 
| ------ | ------ |
| ![image](https://user-images.githubusercontent.com/111492177/207934786-f5ff3255-f8bf-4d59-a09b-9c1f08ef3fad.png) | Sobald die zweite richtige Antwort gewählt wird, setzen sich die Monster in Bewegung und laufen konstant mit einer Geschwindigkeit von 2 durch den eingegrenzten Bereich. |
| ![image](https://user-images.githubusercontent.com/111492177/207915736-9a78e24a-3783-4259-bb4b-1bf4536d725c.png) | Der spannende Teil liegt bei den Kollisionen. Hier wird bei einer Berührung der Monster mit einem Tor nur ihre Blickrichtung geändert. Um sicher zu gehen, dass die Monster sich immer um einen zufälligen Wert zwischen 170° und 190° drehen, um Einfältigkeit in der Bewegung der Masse zu vermeiden, werden auf die 180° zuerst die bereits vorhandene Blickrichtungsgradzahl und dazu ein zufälliger Wert zwischen -10° und 20° addiert. |

</details>

        
## <a name="blog"></a>Blogeinträge


<details> <summary>Stunden</summary>

| [22.08.2022](#1) | [25.08.2022](#2) | [29.08.2022](#3) | [05.09.2022](#4) | [08.09.2022](#5) |
| ------ | ------ | ------ | ------ | ------ |     
| [12.09.2022](#6) | [19.09.2022](#7) | [22.09.2022](#8) | [06.09.2022](#9) | [24.10.2022](#10) |
| [03.10.2022](#11) | [07.11.2022](#12) | [14.11.2022](#13) | [17.11.2022](#14) | [21.11.2022](#15) |
| [28.11.2022](#16) | [Die restlichen Stunden](#17) |

</details>

### <a name="1"></a>22.08.2022
Am 22.08.2022 haben wir uns in Gruppen aufgeteilt und dabei werden Michael und Mohammad bis zum Ende des Projektes zusammenarbeiten. In der ersten Doppelstunde sammelten wir einige Ideen zu unserem Projekt. Die erste Idee war, einen Roboter mit Hilfe von Lego-Bausätzen zu bauen und diesen schließlich zu programmieren. Dabei hätte er ein Muster auf den Boden malen sollen.
Die zweite Idee war es ein Spiel zu programmieren. Die grobe Idee war, dass es einen Agenten gibt, der durch ein Labyrinth geht und dabei Münzen sammelt und bis zum Ziel läuft. Nach einigen Überlegung haben wir uns für das Spiel entschieden. Danach haben wir uns die verschiedenen Programme angeschaut, um das Richtige zu finden, mit dem wir gut arbeiten können. Dabei kamen Snap, StarLogoTNG und Greenfoot in Frage. 
### <a name="2"></a>25.08.2022 
Am 25.08.2022 war Mohammad nicht anwesend. Währenddessen hat Michael sich in verschiedene Programme eingearbeitet. Später hat er sich mit den Lernaktivitäten für StarLogoTNG beschäftigt.
### <a name="3"></a>29.08.2022
Am 29.08.2022 haben wir uns für das Programm StarLogoTNG entschieden. Während Mohammads Abwesenheit hat er eine Skizze von dem Labyrinth gezeichnet. In der ersten Stunde haben wir einen genauen Plan vom Spiel aufgestellt. Dabei sollten es zwei Agenten sein, die bis zum Ziel Münzen sammeln und je mehr Münzen sie sammeln, desto schneller werden sie. Auf ihrem Weg sollten andere Agenten sie aufhalten. Im Falle einer Kollision soll das Spiel neugestartet werden. In der zweiten Stunde haben wir versucht unsere Agenten, Marge und Homer, so zu programmieren, dass man sie manuell steuern kann.
<details> <summary>Planskizze</summary>

    
![image](https://user-images.githubusercontent.com/111492177/205087623-da6c89d0-ccba-4d56-9e67-7b9e9d17882a.png)
    
    
    
</details>



### <a name="4"></a>05.09.2022
Am 5.09.2022 haben wir weiter an der manuellen Steuerung unserer Agenten gearbeitet. Zudem haben wir es geschafft, dass unsere Agenten zusammenlaufen, statt getrennt. Hierfür setzten wir einfach denselben Startort und dieselbe Steuerung für beide Agenten auf, was sich später jedoch als ein Problem herausstellen sollte.
<details> <summary>Steuerung</summary>
    
![Steuerung](https://user-images.githubusercontent.com/111492177/205107662-9aaeebb6-0458-4974-8319-fee645893445.png)

</details>



### <a name="5"></a>08.09.2022 
Am 08.09.2022 setzten wir uns das Ziel, den Anfang unseres Labyrinthes zu bauen. Die Wände des Labyrinths sollten aus Häusern bestehen. Dies haben wir bis Ende der ersten Informatikstunde geschafft. In der zweiten Stunde riefen wir unseren ersten Agenten, Sonic, der Marge und Homer hindern soll zum Ziel zu kommen, ins Leben. Dabei sollte Sonic schnell um ein Haus rennen und im Falle einer Kollision mit Marge und Homer sollte das Spiel neugestartet werden. Dies stellte sich als leichter heraus als erwartet, da Sonic die eingegebenen Koordinaten zu schnell übernahm, sodass er nicht um das Haus kam. Das lag daran, dass wir zu weit gedacht hatten und am Ende waren es nur zwei Blöcke Code.
<details> <summary>Sonic</summary>
    
![Sonic](https://user-images.githubusercontent.com/111492177/205108744-74437148-80dd-4fc4-aeee-ea78e3feb00e.png)
![Sonic](https://user-images.githubusercontent.com/111492177/205109447-8c1fb54f-1def-4f13-afc7-606b5e03abce.png)

https://user-images.githubusercontent.com/111492177/205115697-67af9d2b-ef3a-4828-92d4-fba549a7006b.mp4



</details>



### <a name="6"></a>12.09.2022
Am 12.9.2022 waren wir bis zum Ende der ersten Informatikstunde mit der Programmierung von Sonic fertig. In der zweiten Stunde versuchten wir den Code zu sortieren, damit es übersichtlicher wird.
### <a name="7"></a>19.09.2022 
Am 19.9.2022 arbeiteten wir am zweiten Hindernis. Dabei sollten die Walls (Würfel) sich auf einer gewissen Strecke hin und her bewegen. Ziel hierbei war es, dass Marge und Homer versuchen sollen hindurchzukommen, ohne die Hindernisse zu berühren. Diese Aufgabe stellte sich ebenfalls als äußerst herausfordernd heraus. Bis Ende der zweiten Stunde waren wir damit beschäftigt.
<details> <summary>Walls</summary>

![image](https://user-images.githubusercontent.com/111492177/205110731-caf57b95-c0bd-4d47-aa78-a6e10cb6eaa1.png)

</details>


### <a name="8"></a>22.09.2022
Am 22.09.2022 haben wir Herrn Buhl beim selben Problem um Hilfe gefragt. Herr Buhl erklärte uns das Vorgehen und zeigte einen möglichen Lösungsansatz. Dank seiner Erklärung konnten wir das Problem lösen. In der zweiten Stunde haben wir noch zwei weitere Walls hinzugefügt, sodass wir nun insgesamt drei Walls hatten, die sich bewegen. Kurz vor Ende des Unterrichts haben wir an Häuserblöcken gearbeitet, dabei haben wir die Abstände zwischen den Häuser optimiert.
<details> <summary>Die drei Würfel</summary>
    

https://user-images.githubusercontent.com/111492177/205116560-5059c122-3a5b-40a9-82a8-ec33d3b2a9fb.mp4


![image](https://user-images.githubusercontent.com/111492177/205127364-9ed55362-f559-4d37-9b43-248cf35989e9.png)



</details>


### <a name="9"></a>06.10.2022
Am 06.10.2022 haben wir an dem zweiten Hindernis gearbeitet. Nachdem Marge und Homer die hinderlichen Walls überquert haben, werden sie mit zwei Wegen konfrontiert. Der linke Weg führt in eine Sackgasse. Der Weg bis zur Sackgasse ist L-Förmig, sodass man nicht das Ende sehen kann, wo auf den Spieler ein verrückt gewordener Clown wartet, der herauskommen soll, sobald man um die Ecke läuft, um den Spieler auszuschalten und ihm einen Schrecken zu verleihen. Um dies umzusetzen, versuchten wir mit der Smell-Funktion zu arbeiten. Wenn Marge und Homer einen bestimmten Radius um den Clown erreichen, sollte er aktiviert werden.
<details> <summary>Unfunktionsfähige und aufwändige Smellfunktion</summary>
    
![image](https://user-images.githubusercontent.com/111492177/205112117-89c9711d-1472-48a9-baa5-1ec04070a061.png)
    
</details>


### <a name="10"></a>24.10.2022
Am 24.10.2022 haben wir weiter am Clown gearbeitet. Jedoch erwies die Smell-Funktion sich als sehr aufwändig und fehlerhaft. Deshalb haben wir uns eine andere Methode überlegt. Die Methode sollte darin bestehen, dass kurz vor der L-Ecke ein paar Grasbüschel auf dem Boden platziert sind. Wenn man über diese Grasbüschel läuft, sollte sich der Clown in Bewegung setzen, was sich als äußerst funktionsfähig herausstellte. Später machten wir uns über das nächste Hindernis Gedanken.
<details> <summary>Grasbüschelfunktion</summary>


https://user-images.githubusercontent.com/111492177/205121123-cb9ee103-9139-4064-adbd-3126f0af93e2.mp4


![image](https://user-images.githubusercontent.com/111492177/205112555-d8270e57-d66b-4677-be81-445f63dc9b42.png)

</details>


### <a name="11"></a>03.11.2022
Am 03.11.2022 haben wir gemerkt, dass die vorher programmierte Funktion von der letzten Stunde nicht gespeichert worden war. Daher verschwendeten wir leider etwas Zeit, um sie wiederherzustellen. Dabei fielen uns ein paar Ideen zur Verbesserung ein. Zum Beispiel, dass der Clown das vorgeschriebene Programm solange wiederholt bis er Marge und Homer aus dem Spiel entfernt. Später haben wir uns überlegt, wie das restliche Labyrinth gebaut werden sollte.
### <a name="12"></a>07.11.2022
Am 07.11.2022 ist der Informatik Unterricht ausgefallen und wir konnten deshalb nur eine Stunde ins Programmieren investieren. Als nächstes Hindernis sollten zwei Tore gebaut und jeweils vor einem Tor sollte eine Frage gestellt werden. Man hat drei Optionen und um die Antwort zu wählen, muss man zu der Option hinlaufen und kollidieren. Wenn man die richtige Antwort wählt, verschwindet das Tor, wenn man aber eine falsche Antwort wählt, muss man das Spiel neu starten.
<details> <summary>Das Quiz</summary>

![image](https://user-images.githubusercontent.com/111492177/205592056-5c323214-afaf-436d-b1e0-1c1b6e866b47.png)

</details>

### <a name="13"></a>14.11.2022
Am 14.11.2022 ist uns aufgefallen, dass die zwei Fragen gleichzeitig erscheinen, so dass es schwieriger wird, sie zu lesen. Deshalb änderten wir es insofern, dass die zweite Frage erst beim verschwinden des ersten Tors erscheint. Später haben wir einen begrenzten Raum im Zentrum unseres Labyrinthes erbaut. Dabei haben wir Tore  als Wände zur Begrenzung benutzt. Dort sollen sich zahlreiche Monster aufhalten und sich frei in zufällige Richtungen bewegen. Dies stellte sich als relativ einfach dar, jedoch war hier die Herausforderung, sie in diesem Gebiet zu behalten. Unser erster Lösungsansatz war, dass sie sich, im Falle einer Kollision mit der Wand, um 180° Grad drehen und weiterlaufen sollten. Dennoch konnten sie das Gebiet verlassen.

<details> <summary>Monster im Zentrum</summary>


![image](https://user-images.githubusercontent.com/111492177/205128087-f419122f-87be-4c86-8c17-8cd03ce4fe94.png)



</details>


### <a name="14"></a>17.11.2022
Am 17.11.2022 bemühten wir uns um die Bearbeitung dieses Problems. Somit war die zweite Idee, das Gebiet anhand der x- und y-Koordinaten einzugrenzen. Sollten die Monster sich der Grenze nähern, sollten sie zwei Schritte zurück gehen, um 90° Grad drehen und weiterlaufen. Wir haben ca. eine Stunde hoffnungslos daran gearbeitet und verschiedene Lösungsansätze ausprobiert. Da uns nicht mehr viel einfiel, haben wir uns auf die Paintball-Funktion fokussiert. Dabei sollen Marge und Homer in der Lage sein die Monster abzuschießen, um an das Ziel zu kommen. Dies ließ sich schnell bearbeiten, gerade weil Michael vorher die Lernaktivität dazu bearbeitet hatte.

<details> <summary> Paintballs schießen</summary>


https://user-images.githubusercontent.com/111492177/207943244-402af528-bd4a-41dd-b569-449ba1f5bdae.mp4



</details>


### <a name="15"></a>21.11.2022
Am 21.11.2022 überlegten wir uns, dass Marge und Homer die Paintball-Funktion erst erlaubt wird, nachdem sie durch das zweite Tor gegangen sind. Außerdem soll ein Agent, namens Info, sie über die Funktion am Tor informieren. Da die Paintballs nach dem Abwerfen schweben, sollen sie verschwinden, wenn sie mit den Toren kollidieren, damit sie nicht ewig weiterfliegen. Das andere Problem, welches wir am Anfang hatten war, dass Marge und Homer durch die Häuser laufen konnten. Dies wollten wir verhindern, indem wir sie, im Falle einer Kollision mit den Häusern, zwei Schritte zurückgehen lassen. Das galt jedoch oft nur für einen Agenten, da sie nebeneinander liefen und somit manchmal nur ein Agent von beiden zurückgestoßen wurde, weshalb wir uns entschieden haben, dass wir Homer als Hauptagent haben und er alleine durch das Labyrinth läuft.
### <a name="16"></a>28.11.2022
Am 28.11.2022 lösten wir das, zuerst hoffnungslose, Problem der Eingrenzung der Monster. Das Problem bestand darin, dass die Tore sich überlagerten und das Spiel den Code für die Drehbewegung der Monster zweimal ausführte, sodass sie einfach aus dem Feld liefen. Somit kann man sagen, dass dies ein Fehler auf Seiten StarLogo’s war. Außerdem haben wir zwei weitere Info-Agenten erstellt, um den Spieler durch das Spiel zu führen. Schließlich haben wir weitere Verfeinerungen durchgeführt und den Code verschönert.
### <a name="17"></a>Die restlichen Stunden
Die restlichen Stunden sind leider ausgefallen, da Herr Buhl krank war. Wir nutzten die Zeit um uns voll auf die Blogeinträge und das Erstellen der Projektseite zu fokussieren.


## <a name="fazit"></a>Fazit

Am Anfang wussten wir nicht, wie man Spiele programmiert. Im Internet gibt es unzählige komplett fertig durchgeführte Projekte und wir wollten nicht einfach irgendetwas kopieren. Eine eigene Idee musste her. Nach langer Ideensuche kam uns die Idee dieses Spieles: „Homer im Ohio“.                                             Obwohl Michael und Mohammad vorher keine Erfahrung in Informatik hatten, haben wir uns durch das Projekt gearbeitet. Es gab Momente, wo wir nicht mehr weiterkommen konnten, aber es gab auch Momente, wo alles reibungslos funktionierte. Die Probleme konnten wir meist mit einfachen und kreativen Lösungsansätzen lösen. Insgesamt lief die Arbeit gut und in den Stunden arbeiteten wir immer zusammen. So können wir beide alles verstehen. 
Der Nachteil dieser Arbeitsweise ist, dass sie viel Zeit in Anspruch nimmt und daher weniger effizient ist. 
Durch unsere grundsätzliche Arbeitsweise hatten wir immer wieder motivierende Erfolgsmomente. Das macht die ganze Arbeit viel angenehmer und trieb uns voran. So konnten wir während des Projektes viel Neues lernen und Probleme selbstständig lösen, was den Informatikunterricht interessanter machte. Obwohl der anfängliche Plan anders als das Endprodukt aussah, sind wir trotzdem sehr zufrieden. 
Das Beste ist, dass unser Projekt abgeschlossen ist und wir etwas Neues gelernt haben.

## <a name="starlogo"></a>Zu Starlogo

<details>
    <summary> Hier eine kurze Erklärung zu StarlogoTNG:</summary>

Mit "StarLogo TNG" können Sie ein oder mehrere digitale Objekte in einer wunderschönen 3D-Welt bewegen - zuerst war es eine Schildkröte. Sie müssen Aktionen mit einer speziellen Programmiersprache vorab eingeben. Diese Logo-basierte Programmiersprache ähnelt einem einfachen Prinzip der Modularität. Was zunächst schwierig erschien, wurde dank der Online-Hilfe und Tutorials schnell zum Kinderspiel, da es Unmengen an einzelnen Bausteinen gibt.
Ziehen Sie einzelne Befehlsblöcke per Drag & Drop auf die Oberfläche, verbinden Sie verschiedene Blöcke und verwenden Sie die Tastatur, um einzelne Eigenschaften zu ändern. Dank dieser innovativen grafischen Programmiersprache erstellen Sie mit wenigen Mausklicks eigene Bewegungsabläufe für Ihre Schildkröte. Auch die Umgebung kann im Geländeeditor nach Belieben verändert werden. Das Ganze sieht nicht nur hübsch aus, sondern lässt sich auch zur Berechnung von Bewegungsabläufen in dezentralen Systemen, etwa bei mehreren Autos im Verkehr, nutzen.

https://www.chip.de/downloads/StarLogo-The-Next-Generation_21024590.html#:~:text=StarLogo%20%2D%20The%20Next%20Generation%20Mit,einer%20speziellen%20Programmiersprache%20vorher%20eingeben.


</details>

## <a name="eigenst"></a>Eigenständigkeitserklärung

Hiermit bestätigen wir, Michael Markwart und Mohammad Rezaei, dass die von uns vorgelegte Arbeit selbstständig verfasst und keine anderen als die angegebenen Quellen und Hilfsmittel benutzt haben.

Ahrensburg, den 01.12.2022
