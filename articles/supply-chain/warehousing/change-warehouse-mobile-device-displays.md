---
title: "Seite \"Anzeigeeinstellungen für das mobile Gerät für das Lager\""
description: "In diesem Thema wird beschrieben, wie die Darstellung einer Anzeige eines Mobilgeräts eingerichtet wird, und wie Tastenkombinationen den Steuerelementen, beispielsweise Schaltflächen zugeordnet werden."
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysUserSetup, WHSRFColor, WHSRFColorPicker, WHSWorkUserDisplaySettings
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 29071
ms.assetid: 931a02e8-b561-45e3-9c44-06b875ced1b4
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 799cd4a940813e39f8be6b4c127b9efabc88e909
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="warehouse-mobile-device-display-settings"></a>Seite "Anzeigeeinstellungen für das mobile Gerät für das Lager"

[!include[banner](../includes/banner.md)]


In diesem Thema wird beschrieben, wie die Darstellung einer Anzeige eines Mobilgeräts eingerichtet wird, und wie Tastenkombinationen den Steuerelementen, beispielsweise Schaltflächen zugeordnet werden. 

Dieser Artikel gilt für "erweiterte Funktionen" im Modul Lagerortverwaltung. Mobile Geräte können für viele der Aufgaben verwendet werden, die Lagerarbeiter ausführen.

## <a name="specify-styles-and-map-keyboard-shortcuts"></a>Definieren Sie die Formate und ordnen Sie Tastenkombinationen zu
Als Teil der Konfiguration des mobilen Geräts können Sie unterschiedliche Layouts für mobile Geräte definieren. Hierfür müssen Sie den Name der Designs und Stylesheets-Datei (CSS) und die Active Server Page Extension-Datei (ASPX) kennen. Standard Dateien werden als Teil der Portalinstallation der mobilen Lagerort-Geräte eingerichtet. Wenn Sie die Dateinamen nicht kennen, fragen Sie den Systemadministrator. Sie können ein neues Format auf der Seite **Anzeigeeinstellungen des mobilen Geräts** definieren:

-    Geben Sie den Dateinamen Ihrer CSS-Datei im Feld **CSS-Datei** ein. Schließen Sie die .css Dateinamenerweiterung mit ein.
-   Definieren Sie im Feld **Anzeigeeinstellungsansicht des mobilen Geräts** die ASPX-Datei. Lassen Sie die .aspx Dateinamenerweiterung **weg**.

Die CSS- und ASPX-Dateien müssen sich in einem bestimmten Verzeichnis befinden, damit die Internet Information Services-Anwendung (IIS) sie laden kann. Es kann hilfreich sein, verschiedene CSS-Dateien zu definieren, wenn Sie die mobile Gerätefunktionen in verschiedenen Browsern oder auf unterschiedlichen Arten der Hardware ausführen, die unterschiedliche Layoutsteuerelemente erfordern. Einfache Einstellungen wie die Hintergrundfarbe, die Schriftart und der Schriftgrad für Text und die Breite und das Verhalten der Schaltflächen können mithilfe einer unterschiedlichen Verwendung von CSS-Dateien leicht gesteuert werden. Die ASPX-Datei wird verwendet, um den mobilen Standort auf der serverseitigen ASP.NET-Anwendung anzuzeigen. Die Datei steuert, wie die Gesamtstruktur von HTML ausgelegt ist. Es wird empfohlen, diese Funktionen nur anzupassen, wenn Sie ernsthafte strukturelle Probleme mit HTML und JavaScript haben und diesen Code für Ihre spezifischen Geräte ändern müssen. Um die HTML-Steuerung auf der Seite des mobilen Geräts auf Tastenkombinationen zu ändern, müssen Sie auf der Seite **Anzeigeeinstellungen für mobiles Gerät** im Feld **Tastenkombination** die numerischen Codes für die Tasten zuweisen. Sie können das Menü **Codes für Tastenkombinationen ansehen** im mobilen Gerät verwenden, um die numerischen Zeichencodes zu finden. Beachten Sie, dass die Zuordnungen anders sein kann, je nach Hardware, die verwendet wird. Sie müssen die folgende Syntax verwenden, um die Zuordnung zu erstellen:

&lt;Steuerungsnam&gt;(&lt;Schlüsselname&gt;)=&lt;Schlüsselcode&gt;;

Hier ist eine Erläuterung der Teile der Syntax:

-   **&lt;Steuername&gt;**> - Der Name des Steuerelements, beispielsweise eine Schaltfläche, die in HTML angezeigt wird.
-   **(&lt;Tastenname&gt;)**  – Der Name der Taste, für die Sie die Verknüpfung erstellen.
-   **&lt;Zeichencode&gt;**  – Der numerischen Zeichencode für die Taste, den Sie für die Tastenkombination verwenden möchten.

Hier ist ein Beispiel:

Abbrechen (ESC) =27; Voll (F2) =113

Auf allen Seiten, die eine Schaltfläche **Abbrechen** haben, wird die Schaltfläche diesen Text haben:

**(ESC) Abbrechen**

Das Drücken der ESC-TASTE auf der Tastatur wird die Schaltfläche **Abbrechen** aktivieren. Um die Format- und Tastenkombinationseinstellungen auf einem bestimmtem Gerät zu aktivieren, müssen Sie eine Zuordnung im Feld **Kriterien** erstellen. Sie müssen einen regulärer. NET-Ausdruck verwenden, um die Zuordnung zu erstellen, und der Ausdruck muss aus drei Bereichen bestehen, die durch einen senkrechten Strich (|) getrennt sind , so wie hier angezeigt:

Request.UserHostAddress=&lt;user host address&gt;|HostName=&lt;user host name&gt;|Request.UserAgent=&lt;user agent&gt;

Hier ist eine Erläuterung der Ausdrucksteile:

-   **&lt;Host-Benutzeradresse&gt;** – Ein regulärer .NET-Ausdruck, der der IP-Adresse des Anforderers entspricht
-   **&lt;Host-Benutzername&gt;**– Ein regulärer .NET-Ausdruck, der dem Netzwerknamen des Anforderers entspricht.
-   **&lt;Benutzer-Agent&gt;** – Ein regulärer. NET-Ausdruck, der der Bezeichnung des Browsers entspricht, die der Anforderer verwendet.

Das folgende Beispiel zeigt, wie der Internet Explorer 8 am besten verwendet wird:

Request.UserHostAddress=.\*|HostName=.\*|Request.UserAgent=MSIE\\s8\\.0

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
Sie können die Liste der akzeptierten Datumsformate für jede Installation erweitern. Diese Funktion kann hilfreich sein, beispielsweise wenn Sie ein Format angeben möchten, das es für eine Arbeitskraft einfacher macht, Daten auf einem mobilen Gerät einzugeben. Das Standardformat wird durch die Standardsprache des Benutzers bestimmt, die im Feld **Sprache** auf der Seite **Benutzeroptionen** definiert ist. (Die gleiche Seite wird auch verwendet, um einen Mitarbeiter einem bestimmten Lagerortarbeitsbenutzer zuzuordnen.) **Hinweis:** Das Portal Lagerort-mobiles Geräte verwendet nicht die Einstellung des Felds **Datum, Uhrzeit und Zahlenformat** auf der Seite **Sprache und Regionseinstellungen**. Um ein Datumsformat zu ändern, müssen Sie mit regulären Ausdrücken in Microsoft .NET Framework vertraut sein. Weitere Informationen finden Sie unter [.NET Reguläre Framework- Ausdrücke](http://go.microsoft.com/fwlink/?LinkId=391260). Um Datumsformate zu definieren, bearbeiten Sie die Datei Daten.ini, die sich unter Inhalt\\Einstellungen\\Daten.ini auf den Portalserver der mobilen Geräte für den Lagerort befindet. Diese Datei verwendet reguläre .NET-Ausdrücke, um das Datumsformat zu bestimmen. Der reguläre Ausdruck muss Teilausdrücke enthalten, die benannte Gruppen für Tag, Monat und Jahr (DDMMYY) erstellen, wie im folgenden Beispiel gezeigt:

^(?&lt;day&gt;\\d{2})(?&lt;month&gt;\\d{2})(?&lt;year&gt;\\d{2})$

Jeder Teilausdruck erfordert eine Zahl mit einer oder Ziffern für den Tag und den Monat und eine Zahl mit einer bis zu vier Ziffern für das Jahr. Beispielsweise definiert der nachfolgende Teilausdruck eine benannte Gruppe für ein Jahr und erfordert mindestens zwei und maximal vier Ziffern:

(?&lt;year&gt;\\d{2,4})

Sie können mehr als einen Ausdruck in der gleichen Datei angeben. Jeder Ausdruck muss sich auf einer separaten Zeile befinden. Der erste Ausdruck, der übereinstimmt, wird verwendet, um das Datum zu analysieren.

<a name="see-also"></a>Siehe auch
--------

[Konfigurieren von mobilen Geräten für Lagerarbeiten](configure-mobile-devices-warehouse.md)




