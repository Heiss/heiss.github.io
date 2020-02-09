---
title: "Css External vs Internal"
date: 2017-12-16T02:03:40+01:00
author: PhysicX
summary: "Keine Beschreibung"
categories: []
tags: []
---

Vielleicht haben sich einige von euch schonmal mit Cascading Stylesheet (kurz CSS) für HTML beschäftigt. Dabei ist es Gang und Gäbe, die Styles in Dateien auszulagern um HTML und CSS zu modularisieren und weiterhin es leichter zu machen bei Änderungen die entsprechende Datei auf den Webserver zu schieben.

Seit einigen Jahren wird sogar CSS nicht nicht von HTML ausgegliedert, sondern auch Logisch modularisiert. Heißt, es wird versucht mehrere CSS Dateien zu haben für verschiedene Zwecke. In einer Datei wurden alle Container definiert, in der anderen alle Hintergründe und so weiter. Damit sollen vor allem sehr große Webseiten mit vielen Styles es leichter haben, die entsprechenden Anpassungen durchzuführen und dabei nur möglichst kleine Dateien an den Betrachter zusenden zu müssen.

(Fast) alle Browser dürften heutzutage einen Cache besitzen und überprüfen, ob sich am Inhalt überhaupt etwas geändert hat, sodass sie nicht jedesmal alle Dateien herunterladen zu müssen und so schnellere Zugriffszeiten zu ermöglichen.

Diese Ausgliederung macht es aber auch gleich wieder etwas langsamer, denn jede Datei, welche in der HTML-Datei verlinkt ist, muss angefragt, überprüft, entsprechend heruntergeladen und verarbeitet werden. Dies kann also wieder ein Zeitverlust bedeuten, welchen man sich eigentlich erkaufen wollte. Bei vielen kleinen Dateien wird damit dieser Zeitgewinn wieder negiert. Man sollte also möglichst große Dateien, welche innerhalb der Datei logisch aufgebaut ist, erstellen.

Falls man nur wenige Stylesheets, wie in diesem Blog, verwenden möchte, so sollte man diese sogar direkt intern in die Container definieren, sodass es nicht nötig ist eine neue Datei zu laden. Mit der heutigen Bandbreite ist ein einziger Downstream einer etwas größeren Datei teilweise schneller als mehrere Dateien, welche in der Summe aber kleiner sind. 

Man sollte also einige Tests durchführen um die besten Resultate für seine eigene Webseite zu erreichen. Es wird sicherlich irgendwo eine hübsche Formel dafür geben, aber für mich fuhr ich mit gesundem Menschenverstand für meine Projekte bisher sehr gut.

p.s. ein Mergen der Stylesheets ist auch leicht möglich. Solche Sachen kann man dann sehr gut per gZip an die Browser versenden, wenn die das verstehen. Weiterhin sollte man versuchen möglichst wenige JavaScript-Librarys verwenden und dafür lieber alle Möglichkeiten einer Bibliothek ausnutzen.