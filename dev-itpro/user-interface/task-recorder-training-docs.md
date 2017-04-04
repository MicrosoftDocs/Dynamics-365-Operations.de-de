---
title: Dokumentation oder Schulungen mithilfe von&quot;Aufgabenaufzeichnungen&quot; erstellen
description: "In diesem Thema wird erläutert, welche Aufgabenleitfäden Aufgabenaufzeichnung und sind, wie Aufgabenaufzeichnungen erstellt und wie Microsoft-Aufgabenleitfäden passt und in der Hilfe enthält."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SysHelpSetup
audience: Application User, IT Pro
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 25391
ms.assetid: 59bf39f8-1464-441e-8b23-9a856c73471b
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b21fd97426b331726c12ea29f89817a46dd445c3
ms.openlocfilehash: 38bce4a843f0db575c8d1ba08b7dc2ece8366663
ms.lasthandoff: 03/31/2017


---

# <a name="create-documentation-or-training-using-task-recordings"></a>Dokumentation oder Schulungen mithilfe von"Aufgabenaufzeichnungen" erstellen
In diesem Thema wird erläutert, welche Aufgabenleitfäden Aufgabenaufzeichnung und sind, wie Aufgabenaufzeichnungen erstellt und wie Microsoft-Aufgabenleitfäden passt und in der Hilfe enthält.

<a name="learn-about-task-recorder"></a>Mehr über die "Aufgabenaufzeichnung" erfahren
-------------------------

Aufgabenaufzeichnung ist Microsoft Dynamics 365 für Arbeitsgangstool, das Sie verwenden können, um Projektvorgänge registrieren, dass Sie die Produktbenutzeroberfläche (UI) einlassen. Wenn Sie die Aufgabenaufzeichnung anwenden, werden alle Ereignisse, die in der Benutzeroberfläche vom Server abgerufen werden - einschließlich dem Hinzufügen von Werten, der Änderung von Einstellungen und dem Entfernen von Daten - aufgezeichnet. Die Schritte, die Sie erfassen, werden zusammenfassend als *Aufgabenaufzeichnung* bezeichnet. Aufgabenaufzeichnungen können auf unterschiedliche Weise verwendet werden:

-   **Aufgabenaufzeichnungen können als Aufgabenleitfäden wiedergegeben werden.** Aufgabenleitfäden sind ein ganzzahliges Stück des Dynamics 365 für Arbeitsgänge Hilfe zu erhalten. Ein Aufgabenleitfaden ist eine Lagersteuerung, geführte interaktive, Erfahrung durch die Schritte eines Geschäftsprozesses. Der Benutzer wird aufgefordert, jeden Schritt einer Popupeingabeaufforderung (oder "Blase") abzuschließen, die über die Benutzeroberfläche animiert wird und auf das Benutzeroberflächenelement verweist, mit dem der Benutzer interagieren soll. Die "Blase" bietet auch Informationen dazu, wie dem Element, wie hier "auf" interagiert, oder "in diesem Feld, geben Sie einen Wert ein." Ein Aufgabenleitfaden wird anhand den Satz der Daten des aktuellen Benutzers ausgeführt und die Daten, die eingegeben wird, werden in der Anwenderkonfiguration gespeichert.
-   ** Aufgabenaufzeichnungen können als prozedurale Schritte im Hilfebereich angezeigt werden. ** Sie können den Hilfebereich verwenden, der für die Suche und Aufgabenaufzeichnungen anzuzeigen. Sie können den Hilfebereich zugreifen, indem Sie auf klicken **? ** Symbol in der Leiste Navigationsleiste oder beim kann die Tastenkombination, Ctrl+Shift+ **? **. Auf der Schritte einer Aufgabenaufzeichnung im Hilfebereich lesen, oder Sie können entscheiden, Erfassung als Aufgabenleitfaden wiederzugeben, so, das er Sie die Benutzeroberfläche führt.
-   **Aufgabenaufzeichnungen können im BPM gespeichert werden.** Sie können Ihre Aufgabenaufzeichnungen in einer Position einer Hierarchie der Bibliothek des Geschäftsprozessmodellierers (BPM) in den Lifecycle Services (LCS) speichern. Aus der Aufzeichnung wird eine Liste von Schritten und ein Geschäftsprozessflussdiagramm generiert. Aufgabenaufzeichnungen einer BPM-Bibliothek, die gespeichert wurden, können in Dynamics 365 für Arbeitsgänge als Hilfe angezeigt werden.
-   **Aufgabenaufzeichnungen können als Word-Dokumente gespeichert werden.** Dadurch wird es Ihnen ermöglicht, druckbare Trainingshandbücher einfach zu erzeugen.

Sie können eigene Aufgabenaufzeichnungen, die Spielaufgabenaufzeichnungen erstellen, die von Microsoft bereitgestellten, oder Ändern von Microsoft-zurVerfügung bereitgestellte Aufgabenaufzeichnungen, um die Konfiguration zu entsprechen. Weitere Informationen finden Sie, Aufgabenaufzeichnung zu [Aufgabenaufzeichnung in Dynamics 365] "Arbeitsgänge für task-recorder.md).

## <a name="plan-your-task-recording"></a>Ihre Aufgabenaufzeichnung planen
Ob Sie eine neue Aufgabenaufzeichnung erstellen oder Ihre Aufzeichnung einer Microsoft-Aufgabenaufzeichnung anpassen, berücksichtigen Sie die folgenden Informationen.

-   Planen Sie die Aufzeichnung, wie ein Video. Treffen Sie alle Ihre Entscheidungen im Voraus.
-   Durchlaufen Sie den Geschäftsprozess einmal oder zweimal, ohne ihn zu erfassen, um sich mit den Schritten vertraut zu machen.
-   Wenn Sie den Prozess vor der Aufnahme durchlaufen, achten Sie darauf, wo Sie Tastenkombinationen oder die **Eingabetaste** verwenden, damit Sie sie bei der tatsächlichen Aufzeichnung vermeiden können.
-   Legen Sie folgendes fest:
    -   Wollen Sie Schritte in Unteraufgaben gruppieren? Unteraufgaben unterteilen visuell Abschnitte eines Prozesses. Wenn Sie beispielsweise eine Aufnahme für das "Erstellen und die Freigabe eines Produkts" erstellen, sollten Sie die Schritte zusammen gruppieren, die erforderlich sind, um ein Produkt zu erstellen, und dann die Schritte gruppieren, die erforderlich sind, um das Produkt freizugeben. Außerdem erleichtern Unteraufgaben die Lesbarkeit längerer Prozesse.
    -   Möchten Sie Anmerkungen hinzufügen und wenn ja, wo? Siehe auch "Unterschiedlichen Arten von Anmerkungen verstehen" weiter unten für weitere Informationen.
    -   Welche Werte werden Sie den verschiedenen Feldern zuweisen, wenn Sie die Schritte des Geschäftsprozesses abschließen? Es wird empfohlen, sich darüber sicher zu sein, was Sie im weiteren Verlauf auswählen oder eingeben wollen , damit Sie während der Aufnahme keine Fehler rückverfolgen oder korrigieren müssen.

**Beschreibung und Anmerkungen im Voraus erstellen**

-   Zu Beginn jeder Aufgabenaufzeichnung gibt es ein Textfeld, das Ihnen gestattet, der Aufzeichnung eine Einführung hinzuzufügen. Es wird empfohlen, die Beschreibung in einem separaten Dokument im Voraus zu verfassen und zu speichern, sodass Sie sie während der Aufnahme in die Aufgabenaufzeichnung kopieren und einfügen können. So können Sie mehr Zeit auf die Textverfeinerung verwenden, wenn Sie nicht im Aufzeichnungsprozess sind. Das Schneiden und Einfügen des Texts ermöglicht einen schnelleren und problemloseren Aufzeichnungsprozess.
-   Für jeden Schritt in einer Aufgabenaufzeichnung können Sie Anmerkungen erstellen. Während der Wiedergabe eines Aufgabenleitfadens, werden Anmerkungen in der " Blase" als Hinweise über oder unter dem Text für den Schritt angezeigt. Wenn sie als Text im Hilfebereich angezeigt werden, werden inline Anmerkungen als Text im Schritt. Für die Beschreibung wird empfohlen, Ihre Anmerkungen in einem separaten Dokument zu verfassen und zu speichern. Wenn Sie die Aufgabenaufzeichnung aufnehmen, sollten Sie die Anmerkungen aus diesem Dokument ausschneiden und einfügen.

**Unterschiedliche Arten von Anmerkungen verstehen** Alle Anmerkungen sind optional. Fügen Sie sie nur hinzu, wenn sie hilfreiche Informationen für den Benutzer darstellen.

-   ** Titel **: Eine Titelanmerkung wird vor dem Schritttext Aufgabenaufzeichnung, dass automatisch generiert. Im Aufgabenleitfaden wird die Titelanmerkung über dem automatisch generierten Text. Verwenden Sie diesen Typ der Anmerkung, um zu erläutern, warum der Benutzer den Schritt ausführt oder um einen zusätzlichen Kontext anzugeben.

Dies ist der Bearbeitungsbereich, den Sie sehen, wenn Sie eine Anmerkung hinzufügen, während Sie die Aufzeichnung erstellen. Geben Sie eine Titelanmerkung im Feld **Titel** ein. 

![screen1 ([]. /media/screen1.png)]". /media/screen1.png) 

So sieht die Titelanmerkung in der "Blase" im Aufgabenleitfaden aus. 

![screen2 ([]. /media/screen2.png)]". /media/screen2.png)

-   **Hinweise:** Eine Hinweisanmerkung, die automatisch von der Aufgabenaufzeichnung generiert wurde, wird nach dem Text zum Schritt angezeigt. Im Aufgabenleitfaden wird sie nur angezeigt, wenn der Benutzer auf den Link **Mehr anzeigen** in der Aufgabenleitfadenblase klickt. Verwenden Sie diesen Typ der Anmerkung, um alles Wissenswerte zu beschreiben, das der Benutzer benötigt, um den Schritt abzuschließen.

Dies ist der Bearbeitungsbereich, den Sie sehen, wenn Sie eine Anmerkung hinzufügen, während Sie die Aufzeichnung erstellen. Geben Sie eine Titelanmerkung im Feld **Anmerkung** ein. 

![screen3 ([]. /media/screen3.png)]". /media/screen3.png) 

Dies ist, was die Hinweisanmerkungsaussehung wie in der " Blase "im Aufgabenleitfaden.

![screen4 ([]. /media/screen4.png)]". /media/screen4.png)

-   ** Informationensschritt **: Diese Anmerkungen werden, indem auf einem Steuerelement oder an beliebiger Stelle auf ein Formular mit der rechten Maustaste klickt ** &lt; Aufgabenaufzeichnung ** ** &lt; hinzufügen Informationensschritt erstellt. ** Informationensschritte werden für ein numerierter Schritt an, was Punkt Sie ihn einfügen, obwohl keine Aktivitäten in der Benutzeroberfläche erfasst wurde. Sie können einen Infoschritt auf Formularebene hinzufügen oder einen Infoschritt, der einem Steuerelement zugeordnet ist. Wenn ein Infoschritt einem Formular zugeordnet ist, wird die "Blase" des Aufgabenleitfadens ohne Zeiger irgendwo im Formular plaziert, wenn der Aufgabenleitfaden wiedergegeben wird. Wenn ein Informationensschritt mangelhafte Konfiguration einer Kontrolle hin zugeordnet ist, wird die Aufgabenleitfaden "Blase" auf dem Steuerelement, wenn der Aufgabenleitfaden wiedergegeben wird. Der Hilfebereich wird eine Informationensschrittanmerkung als numerierter, was mit Schritt eingegebenen Text. Verwendungsinformationensschritte, z des Benutzers für die nächsten Schritte vorbereiten, der Schritte beschreiben, die außerhalb von Microsoft Dynamics 365 fertig für Arbeitsgänge werden müssen, oder andere Buchungen beziehen (in den hyperinks doch können Sie Anmerkungen nicht erstellen können.).

**Die Länge der Aufzeichnung bestimmen**

-   Im Allgemeinen liest oder spielt der Benutzer eine Aufzeichnung von Anfang bis Ende ab, darum sollten Sie Schritte oder Aufgaben nicht miteinander kombinieren, die besser separat durchgeführt werden.
-   Versuchen Sie nicht ein langes Szenario aufzuzeichnen, das mehrere Unterprozesse umfasst. Der "Erstellungsvorgang des Diensts für Debitoren" beispielsweise ist zu umfassend; unterteilen Sie ihn in kürzere Aufgaben wie "Rückgaben annehmen" und "Zu Geschenkkarte hinzufügen".
-   Wenn eine Aufgabe als Teil mehrerer verschiedener Geschäftsprozesse ausgeführt werden kann, erstellen Sie dafür eine separate Erfassung, und Sie können sich in den anderen Erfassungen darauf beziehen.
-   Wenn der Prozess mehrere Aufgaben betrifft, die die Person wahrscheinlich nicht alle auf einmal erledigt, können Sie die Aufgaben in einer Aufzeichnung beibehalten, beispielsweise "Funktionsprofile einrichten und zuweisen."
-   Wenn es sich um etwas handelt, dass nur einmalig ausgeführt werden muß (beispielsweise eine Konfiguration) und dann eine andere Aufgabe, die sofort danach, jedoch wiederholt und eigenständig, ausgeführt wird, teilen Sie sie in zwei Aufgabenaufzeichnungen auf.

** Legen Sie fest, wo in der Benutzeroberfläche, um eine Erfassung zu starten ** die Seite, dass Sie sich befinden, wenn Sie das Erfassen von wirkt einer Aufgabenaufzeichnung starten, die der Aufgabenleitfaden für Seite angezeigt wird. Wenn Sie z die Aufgabenaufzeichnung im Hilfebereich aufgeführt werden soll, wenn ein Benutzer auf Hilfe auf die Hauptbuchparameter Seite können, müssen Sie die Erfassung auf der Hauptbuchparameterseite starten. **Aufzeichnungen als .axtr-Dateien speichern** Wenn Sie das Erstellen oder Bearbeiten einer Aufgabenaufzeichnung beendet haben, werden Ihnen mehrere Optionen zum Herunterladen, oder Speichern der Aufzeichnung dargestellt. Sie können die Datei als Aufgabeaufzeichnungspaket (.axtr), als unformatierte Aufzeichnungsdatei (.xml) oder als Word-Dokument herunterladen, oder die Datei in einer LCS-Bibliothek speichern. Es wird empfohlen, Ihre Aufgabenaufzeichnung immer als Aufgabenaufzeichnungspaketdatei (.axtr) zu speichern. Dies unterstützt Sie dabei, die Verwaltung der Datei zu vereinfachen, wenn Prozeduren oder Anmerkungen später geändert werden müssen. Wenn Sie die Datei als Word-Dokument herunterladen möchten, speichern Sie sie ebenfalls als Aufgabenaufzeichnungspaketdatei.

## <a name="create-your-task-recording"></a>Ihre Aufgabenaufzeichnung erstellen
Ausführliche Anweisungen finden der exemplarischen Vorgehensweise Sie [Aufgabenaufzeichnung erstellt wie eine task-recorder.md] ().

## <a name="copy-and-customize-microsofts-task-recordings"></a>Kopieren und Anpassen von Microsoft Aufgabenaufzeichnungen
Sie können von Microsoft Aufgabenaufzeichnungen herunterladen und bearbeitet, um sie für Ihre eigene -Trainingsmaterialien Hilfedokumentation oder zu verwenden. Um eine Microsoft Aufgabenaufzeichnung herunterzuladen, führen Sie die folgenden Schritte aus:

1.  In Dynamics 365 für Arbeitsgänge, öffnen Sie Aufgabenaufzeichnung. Die Aufgabenaufzeichnung finden Sie im Menü **Einstellungen**.
2.  Im klicken Sie Aufgabenaufzeichnungsbereich **Eine Aufzeichnung verwalten.**
3.  Klicken Sie unter **Wo ist die Aufzeichnung** auf **Befindet sich in einer LCS-Bibliothek**.
4.  Klicken Sie auf **LCS-Bibliothek auswählen**.
5.  Hier wählen Sie die globale Bibliothek Microsoft aus.
6.  Wählen Sie in der Strukturdarstellung den Geschäftsprozessbibliotheksknoten aus, dem die Aufgabenaufzeichnung zugeordnet ist.
7.  Klicken Sie auf **OK**.
8.  Klicken Sie auf **Start**.
9.  An diesem Punkt Schritt durch die Aufzeichnung, eine vor geändert wird, z, fahren Sie sie zu überspielen. ** Hinweis **: Wenn Sie nur den Text einer Erfassung ändern müssen, können Sie die Erfassung unter öffnen ** Bearbeiten der Anmerkungen einer Aufzeichnung ** Modus und ihn dann speichern.
10. Nachdem die Aufzeichnung bis zum Ende abgespielt wurde, klicken Sie auf **Anhalten** in der Symbolleiste für die Aufgabenaufzeichnung am oberen Rand des Bildschirms.
11. Wählen Sie aus, wie Sie die Aufgabenaufzeichnung speichern wollen.

## <a name="include-your-task-recordings-in-the-help-pane"></a>Führen Sie die im Aufgabenaufzeichnungen Hilfebereich ein
Wenn Sie Ihre benutzerdefinierten im eigenen Aufgabenaufzeichnungen Hilfebereich anzuzeigen dass sie die wiedergegebene Rückseite als Aufgabenleitfäden oder Text angezeigt werden können, müssen Sie Ihre Aufgabenaufzeichnungen zu Ihrer eigenen BPM-Bibliothek speichern und aktualisieren anschließend die Hilfesystemparameter die auf der BPM-Bibliothek zu verweisen. Weitere Informationen finden Sie [schließen Sie im Hilfesystem.] angezeigt. ". /get-started/help-connect.md)

<a name="see-also"></a>Siehe auch
--------

Dynamics für Arbeitsgangs-Hilfe [365] ". \ \ anfangen help-overview.md)

Führen [] (die Hilfe an. \ \ anfangen help-connect.md)

[Aufgabenaufzeichnung in Dynamics 365 für Arbeitsgänge task-recorder.md] ()

[Vor kurzem hinzugefügte Aufgabenaufzeichnungsfunktionen] (\\ fangen Kernsatz an, Neu-hinzugefügte-Bearbeitung-Funktion-in-AufgabeRekorder \ "

[Neue Trainingsbibliotheken für Dynamics AX in der Lebenszyklus- mithilfe der Aufgabenaufzeichnung (externer Link) Erstellen]https://docs.com/mufife/163372c6-f366-4c5a-94fa-93e2c25f878a/creating-new-training-libraries-for-dynamics-ax) "

[Erstellen Sie Ihr Hilfethemen mit Aufgabenerfassung "externen Link)]https://mbspartner.microsoft.com/AX/Videos/970) "


