---
title: "Seite &quot;Anzeigeeinstellungen für das mobile Gerät für das Lager&quot;"
description: "In diesem Thema wird beschrieben, wie die Darstellung einer Anzeige eines Mobilgeräts eingerichtet wird, und wie Tastenkombinationen den Steuerelementen, beispielsweise Schaltflächen zugeordnet werden."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SysUserSetup, WHSRFColor, WHSRFColorPicker, WHSWorkUserDisplaySettings
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 29071
ms.assetid: 931a02e8-b561-45e3-9c44-06b875ced1b4
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: afa59439e06aad9d669eb352a9837a013f447249
ms.openlocfilehash: 721b293d1f8c76458ca510732f9bb94f003ac6e3
ms.lasthandoff: 03/31/2017


---

# <a name="warehouse-mobile-device-display-settings"></a>Seite "Anzeigeeinstellungen für das mobile Gerät für das Lager"

In diesem Thema wird beschrieben, wie die Darstellung einer Anzeige eines Mobilgeräts eingerichtet wird, und wie Tastenkombinationen den Steuerelementen, beispielsweise Schaltflächen zugeordnet werden. 

Dieser Artikel gilt für "erweiterte Funktionen" im Modul Lagerortverwaltung. Mobile Geräte können für viele der Aufgaben verwendet werden, die Lagerarbeiter ausführen.

## <a name="specify-styles-and-map-keyboard-shortcuts"></a>Definieren Sie die Formate und ordnen Sie Tastenkombinationen zu
Als Teil der Konfiguration des mobilen Geräts können Sie unterschiedliche Layouts für mobile Geräte definieren. Hierfür müssen Sie den Name der Designs und Stylesheets-Datei (CSS) und die Active Server Page Extension-Datei (ASPX) kennen. Standard Dateien werden als Teil der Portalinstallation der mobilen Lagerort-Geräte eingerichtet. Wenn Sie die Dateinamen nicht kennen, fragen Sie den Systemadministrator. Sie können ein neues Format auf der Seite **Anzeigeeinstellungen des mobilen Geräts** definieren:

-    Geben Sie den Dateinamen Ihrer CSS-Datei im Feld **CSS-Datei** ein. Schließen Sie die .css Dateinamenerweiterung mit ein.
-   Definieren Sie im Feld **Anzeigeeinstellungsansicht des mobilen Geräts** die ASPX-Datei. Lassen Sie die .aspx Dateinamenerweiterung **weg**.

Die CSS- und ASPX-Dateien müssen sich in einem bestimmten Verzeichnis befinden, damit die Internet Information Services-Anwendung (IIS) sie laden kann. Es kann hilfreich sein, verschiedene CSS-Dateien zu definieren, wenn Sie die mobile Gerätefunktionen in verschiedenen Browsern oder auf unterschiedlichen Arten der Hardware ausführen, die unterschiedliche Layoutsteuerelemente erfordern. Einfache Einstellungen wie die Hintergrundfarbe, die Schriftart und der Schriftgrad für Text und die Breite und das Verhalten der Schaltflächen können mithilfe einer unterschiedlichen Verwendung von CSS-Dateien leicht gesteuert werden. Die ASPX-Datei wird verwendet, um den mobilen Standort auf der serverseitigen ASP.NET-Anwendung anzuzeigen. Die Dateikontrollen, wie die gesamte HTML-Struktur ausgebreitet wird. Es wird empfohlen, diese Funktionen nur anzupassen, wenn Sie ernsthafte strukturelle Probleme mit HTML und JavaScript haben und diesen Code für Ihre spezifischen Geräte ändern müssen. Um die HTML-Steuerung auf der Seite des mobilen Geräts auf Tastenkombinationen zu ändern, müssen Sie auf der Seite **Anzeigeeinstellungen für mobiles Gerät** im Feld **Tastenkombination** die numerischen Codes für die Tasten zuweisen. Sie können das Menü **Codes für Tastenkombinationen ansehen** im mobilen Gerät verwenden, um die numerischen Zeichencodes zu finden. Beachten Sie, dass die Zuordnungen anders sein kann, je nach Hardware, die verwendet wird. Sie müssen die folgende Syntax verwenden, um die Zuordnung zu erstellen:

&lt;Steuern Sie Name&gt;Schlüsselname&gt;(&lt;;) =key&lt;Code&gt;

Hier ist eine Erläuterung der Teile der Syntax:

-   **&lt;Steuername **&gt;– Der Name des Steuerelements (beispielsweise Gesamtlayout, eine Schaltfläche) sicher in HTML angezeigt wird.
-   ** (&lt;) Schlüsselname&gt;** – Der Name der Taste, dass Sie die Verknüpfung für erstellen.
-   **&lt;Tastencode&gt;** – Der Code des numerischen Zeichens, damit der Schlüssel als Tastenkombination verwendet.

Hier ist ein Beispiel:

Abbrechen (ESC) =27; Voll (F2) =113

Auf allen Seiten, die eine Schaltfläche **Abbrechen** haben, wird die Schaltfläche diesen Text haben:

**(ESC) Abbrechen**

Das Drücken der ESC-TASTE auf der Tastatur wird die Schaltfläche **Abbrechen** aktivieren. Um die Format- und Tastenkombinationseinstellungen auf einem bestimmtem Gerät zu aktivieren, müssen Sie eine Zuordnung im Feld **Kriterien** erstellen. Sie müssen einen regulärer. NET-Ausdruck verwenden, um die Zuordnung zu erstellen, und der Ausdruck muss aus drei Bereichen bestehen, die durch einen senkrechten Strich (|) getrennt sind , so wie hier angezeigt:

Request.UserHostAddress=user-&lt;host address&gt;_=_HostName=user-&lt;Hostname&gt;_=_Request.UserAgent=user-&lt;Agent&gt;

Hier ist eine Erläuterung der Ausdrucksteile:

-   **&lt;Benutzerhost address&gt;** – Ein regulärer. NET-Ausdruck, der, die Bittsteller IP-Adresse übereinstimmt.
-   **&lt;Benutzerhostname **&gt;– Ein regulärer. NET-Ausdruck, der den Netzwerknamen des Bittstellers übereinstimmt.
-   **&lt;Benutzer-Agent&gt;** – Ein regulärer. NET-Ausdruck, der, die Kennung des Browsers übereinstimmt, der den Bittsteller verwendet.

Das folgende Beispiel zeigt, wie der Internet Explorer 8 am besten verwendet wird:

Request.UserHostAddress=.\*_=_HostName=.\*_=_Request.UserAgent=MSIE\\\\s8 .0

Sie können das Menü **Serverkonfiguration für Anzeigeeinstellungen ansehen** auf dem mobilen Gerät verwenden, um die Informationen zu den Einstellungen zu suchen.

## <a name="define-text-colors-for-messages"></a>Definieren Sie Textfarben für Nachrichten
Sie können die Seite **Textfarben des mobilen Geräts** verwenden, um die verschiedenen Farben, die in den vom System generierten Nachrichten verwendet werden, wie beispielsweise Fehlermeldungen zu steuern. Beispielsweise kann hier die Textfarbe den Zweck oder den Schweregrad der Nachricht angeben. Folgende Nachrichtentypen werden gezeigt.

| Meldungstyp | Beschreibung                                                                                                                                                                            |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Standard      | Standardnachrichten verwenden die standardmäßige Farbeinstellungen für alle Nachrichten, wie sie in der CSS-Datei für das mobile Geräteportal des Lagerorts definiert wurden.                                                   |
| Fehler        | Fehlermeldungen geben ein Problem an, das der Benutzer lösen muss, bevor er oder sie fortfahren kann.                                                                                             |
| Erfolgreich      | Erfolgsmeldungen bestätigen, dass eine Aktivität erfolgreich war.                                                                                                                                |
| Warnung      | Warnmeldungen informieren die Arbeitskraft, dass ein Problem vorhanden oder dass es ein Problem geben könnte, wenn die Arbeitskraft fortfährt. Allerdings muss die Arbeitskraft das Problem nicht lösen, um fortzufahren. |

Um die Farbe zu wählen, klicken Sie auf der Seite **Farbe wählen** auf die Palette oder geben einen hexadezimalen Farbcode ein.

## <a name="define-the-date-format-to-use-on-mobile-devices"></a>Definieren des Datumsformats, das auf mobilen Geräten verwendet werden soll
Sie können die Liste der akzeptierten Datumsformate für jede Installation erweitern. Diese Funktion kann hilfreich sein, beispielsweise wenn Sie ein Format angeben möchten, das es für eine Arbeitskraft einfacher macht, Daten auf einem mobilen Gerät einzugeben. Das Standardformat wird durch die Standardsprache des Benutzers bestimmt, die im Feld **Sprache** auf der Seite **Benutzeroptionen** definiert ist. (Die gleiche Seite wird auch verwendet, um einem Mitarbeiter mit einem bestimmten Lagerortarbeitsbenutzer zuzuordnen.) ** Hinweis: ** Die Portal verwendet Lagerort-mobilenGeräte nicht die Einstellung des ** Datums-/Uhrzeit und Zahlenformat ** Feldes in der Sprachen- ** und Regionseinstellungen ** Seite. Um ein Datumsformat zu ändern, müssen Sie mit regulären Ausdrücken in Microsoft .NET Framework vertraut sein. Weitere Informationen finden Sie unter [.NET Reguläre Framework- Ausdrücke](http://go.microsoft.com/fwlink/?LinkId=391260). Um Datumsformat definieren, bearbeiten Sie die Dates.ini-Datei die an das Content \\\\Dates.ini Einstellungen im Feld Portalserver der Lagerort- Geräte befindet. Diese Datei verwendet reguläre .NET-Ausdrücke, um das Datumsformat zu bestimmen. Der reguläre Ausdruck muss Teilausdrücke enthalten, die benannte Gruppen für Tag, Monat und Jahr (DDMMYY) erstellen, wie im folgenden Beispiel gezeigt:

^ (?&lt;Tag&gt;\\d {2}) (?&lt;Monat&gt;\\d {2}) (?&lt;Jahr&gt;\\d {2}) $

Jeder Teilausdruck erfordert eine Zahl mit einer oder Ziffern für den Tag und den Monat und eine Zahl mit einer bis zu vier Ziffern für das Jahr. Beispielsweise definiert der nachfolgende Teilausdruck eine benannte Gruppe für ein Jahr und erfordert mindestens zwei und maximal vier Ziffern:

(?&lt;Jahr&gt;\\d {2,4})

Sie können mehr als einen Ausdruck in der gleichen Datei angeben. Jeder Ausdruck muss sich auf einer separaten Zeile befinden. Der erste Ausdruck, der übereinstimmt, wird verwendet, um das Datum zu analysieren.

<a name="see-also"></a>Siehe auch
--------

[Configuration of mobile devices for warehouse work](configure-mobile-devices-warehouse.md)


