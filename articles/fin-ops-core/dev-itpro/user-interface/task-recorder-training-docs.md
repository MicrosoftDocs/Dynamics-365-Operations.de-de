---
title: Dokumentation oder Schulung mit der Aufgabenaufzeichnung erstellen
description: In diesem Thema werden die Aufgabenaufzeichnung und Aufgabenleitfäden erläutert. Zudem erfahren Sie, wie Aufgabenaufzeichnungen angelegt werden und wie Microsoft-Aufgabenleitfäden angepasst und in die Hilfe aufgenommen werden.
author: josaw1
manager: AnnBe
ms.date: 03/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SysHelpSetup
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 25391
ms.assetid: 59bf39f8-1464-441e-8b23-9a856c73471b
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 927f6475e60b5b93aac0e0c2840cb0b4fc7f0ac8
ms.sourcegitcommit: 61f9e15c5791d27db392d0a90cd781aa8e5baa6f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3164557"
---
# <a name="create-documentation-or-training-with-task-recorder"></a>Dokumentation oder Schulung mit der Aufgabenaufzeichnung erstellen

[!include [banner](../includes/banner.md)]

In diesem Thema werden die Aufgabenaufzeichnung und Aufgabenleitfäden erläutert. Zudem erfahren Sie, wie Aufgabenaufzeichnungen angelegt werden und wie Microsoft-Aufgabenleitfäden angepasst und in die Hilfe aufgenommen werden.

> [!IMPORTANT]
> Sie können Ihre eigenen Aufgabenleitfäden für Dynamics 365 Human Resources erfassen, jedoch sind Sie noch nicht in der Lage, sie in einer Geschäftsprozessmodellierer-(BPM)-Bibliothek zu speichern oder sie vom Hilfebereich zu öffnen. Sie können sie lokal oder an einem Netzwerkspeicherort speichern und sie dann mithilfe der Aufgabenaufzeichnung öffnen und erneut wiedergeben. 

<a name="learn-about-task-recorder"></a>Mehr über die "Aufgabenaufzeichnung" erfahren
-------------------------

Die Aufgabenaufzeichnung ist ein Tool, das Sie verwenden können, um Aktivitäten aufzuzeichnen, die Sie in der Produkt-Benutzeroberfläche (UI) ausgeführt haben. Wenn Sie die Aufgabenaufzeichnung anwenden, werden alle Ereignisse, die in der Benutzeroberfläche vom Server abgerufen werden - einschließlich dem Hinzufügen von Werten, der Änderung von Einstellungen und dem Entfernen von Daten - aufgezeichnet. Die Schritte, die Sie erfassen, werden zusammenfassend als *Aufgabenaufzeichnung* bezeichnet. Aufgabenaufzeichnungen können auf unterschiedliche Weise verwendet werden:

-   **Aufgabenaufzeichnungen können als Aufgabenleitfäden wiedergegeben werden.** Aufgabenleitfäden sind ein integrierter Bestandteil der Hilfe-Erfahrung.Ein Aufgabenleitfaden ist eine kontrollierte, geführte, interaktive Erfahrung, die Sie durch die Schritte eines Geschäftsprozesses führt. Der Benutzer wird aufgefordert, jeden Schritt einer Popupeingabeaufforderung (oder "Blase") abzuschließen, die über die Benutzeroberfläche animiert wird und auf das Benutzeroberflächenelement verweist, mit dem der Benutzer interagieren soll. Die "Blase" enthält auch Informationen zur Interaktion mit Elementen, wie "Hier klicken" oder "Geben Sie in diesem Feld einen Wert ein".Ein Aufgabenleitfaden wird mit dem Datensatz des aktuellen Benutzers ausgeführt, und die Daten, die eingegeben werden, werden in der Anwenderkonfiguration gespeichert.
-   **Aufgabenaufzeichnungen können als Word-Dokumente gespeichert werden.** Dadurch wird es Ihnen ermöglicht, druckbare Trainingshandbücher einfach zu erzeugen.

Sie können eigene Aufgabenaufzeichnungen erstellen, Aufgabenaufzeichnungen wiedergeben, die von Microsoft bereitgestellt werden, oder von Microsoft zur Verfügung gestellte Aufgabenaufzeichnungen ändern, um sie Ihrer Konfiguration anzupassen.Weitere Informationen zu der Aufgabenaufzeichnung, finden Sie unter [Aufgabenaufzeichnung](task-recorder.md)

## <a name="plan-your-task-recording"></a>Ihre Aufgabenaufzeichnung planen
Ob Sie eine neue Aufgabenaufzeichnung erstellen oder Ihre Aufzeichnung einer Microsoft-Aufgabenaufzeichnung anpassen, berücksichtigen Sie die folgenden Informationen.

-   Planen Sie die Aufzeichnung, wie ein Video. Treffen Sie alle Ihre Entscheidungen im Voraus.
-   Durchlaufen Sie den Geschäftsprozess einmal oder zweimal, ohne ihn zu erfassen, um sich mit den Schritten vertraut zu machen.
-   Wenn Sie den Prozess vor der Aufnahme durchlaufen, achten Sie darauf, wo Sie Tastenkombinationen oder die **Eingabetaste** verwenden, damit Sie sie bei der tatsächlichen Aufzeichnung vermeiden können.
-   Legen Sie folgendes fest:
    -   Wollen Sie Schritte in Unteraufgaben gruppieren? Unteraufgaben unterteilen visuell Abschnitte eines Prozesses. Wenn Sie beispielsweise eine Aufnahme für das "Erstellen und die Freigabe eines Produkts" erstellen, sollten Sie die Schritte zusammen gruppieren, die erforderlich sind, um ein Produkt zu erstellen, und dann die Schritte gruppieren, die erforderlich sind, um das Produkt freizugeben. Außerdem erleichtern Unteraufgaben die Lesbarkeit längerer Prozesse.
    -   Möchten Sie Anmerkungen hinzufügen und wenn ja, wo? Siehe auch "Unterschiedlichen Arten von Anmerkungen verstehen" weiter unten für weitere Informationen.
    -   Welche Werte werden Sie den verschiedenen Feldern zuweisen, wenn Sie die Schritte des Geschäftsprozesses abschließen? Es wird empfohlen, sich darüber sicher zu sein, was Sie im weiteren Verlauf auswählen oder eingeben wollen , damit Sie während der Aufnahme keine Fehler rückverfolgen oder korrigieren müssen.

**Beschreibung und Anmerkungen im Voraus erstellen**

-   Zu Beginn jeder Aufgabenaufzeichnung gibt es ein Textfeld, das Ihnen gestattet, der Aufzeichnung eine Einführung hinzuzufügen. Es wird empfohlen, die Beschreibung in einem separaten Dokument im Voraus zu verfassen und zu speichern, sodass Sie sie während der Aufnahme in die Aufgabenaufzeichnung kopieren und einfügen können. So können Sie mehr Zeit auf die Textverfeinerung verwenden, wenn Sie nicht im Aufzeichnungsprozess sind. Das Schneiden und Einfügen des Texts ermöglicht einen schnelleren und problemloseren Aufzeichnungsprozess.
-   Für jeden Schritt in einer Aufgabenaufzeichnung können Sie Anmerkungen erstellen. Während der Wiedergabe eines Aufgabenleitfadens, werden Anmerkungen in der " Blase" als Hinweise über oder unter dem Text für den Schritt angezeigt. Wenn dieser als Text im Hilfebereich angezeigt wird, erscheinen Anmerkungen als Text innerhalb des Schritts. Für die Beschreibung wird empfohlen, Ihre Anmerkungen in einem separaten Dokument zu verfassen und zu speichern. Wenn Sie die Aufgabenaufzeichnung aufnehmen, sollten Sie die Anmerkungen aus diesem Dokument ausschneiden und einfügen.

**Unterschiedliche Arten von Anmerkungen verstehen** Alle Anmerkungen sind optional. Fügen Sie sie nur hinzu, wenn sie hilfreiche Informationen für den Benutzer darstellen.

-   **Titel**: Eine Titelanmerkung wird vor dem Schritt angezeigt, den die Aufgabenaufzeichnung automatisch generiert.Im Aufgabenleitfaden wird die Titelanmerkung über dem automatisch generierten Text angezeigt. Verwenden Sie diesen Typ der Anmerkung, um zu erläutern, warum der Benutzer den Schritt ausführt oder um einen zusätzlichen Kontext anzugeben.

Dies ist der Bearbeitungsbereich, den Sie sehen, wenn Sie eine Anmerkung hinzufügen, während Sie die Aufzeichnung erstellen. Geben Sie eine Titelanmerkung im Feld **Titel** ein. 

[![Bearbeitungsbereich mit Titelanmerkung](./media/screen1.png)](./media/screen1.png) 

So sieht die Titelanmerkung in der "Blase" im Aufgabenleitfaden aus. 

[![Darstellung der Titelanmerkung im Aufgabenleitfaden](./media/screen2.png)](./media/screen2.png)

-   **Hinweise:** Eine Hinweisanmerkung, die automatisch von der Aufgabenaufzeichnung generiert wurde, wird nach dem Text zum Schritt angezeigt. Im Aufgabenleitfaden wird sie nur angezeigt, wenn der Benutzer auf den Link **Mehr anzeigen** in der Aufgabenleitfadenblase klickt. Verwenden Sie diesen Typ der Anmerkung, um alles Wissenswerte zu beschreiben, das der Benutzer benötigt, um den Schritt abzuschließen.

Dies ist der Bearbeitungsbereich, den Sie sehen, wenn Sie eine Anmerkung hinzufügen, während Sie die Aufzeichnung erstellen. Geben Sie eine Titelanmerkung im Feld **Anmerkung** ein. 

[![Bearbeitungsbereich mit Anmerkung im Hinweisfeld](./media/screen3.png)](./media/screen3.png) 

So sieht die Hinweisanmerkung in der "Blase" im Aufgabenleitfaden aus.

[![Darstellung der Hinweisanmerkung im Aufgabenleitfaden](./media/screen4.png)](./media/screen4.png)

-   **Info Schritt**: Diese Anmerkungen werden erstellt, indem man mit der rechten Maustaste auf ein Steuerelement oder irgendwo auf einem Formular &lt; klickt **Aufgabenrecorder** &lt; **Info Schritt hinzufügen.** Infoschritte werden an jeder Stelle, an der Sie sie einfügen, als nummerierter Schritt angezeigt, auch wenn keine Aktion in der Benutzeroberfläche aufgezeichnet wurde. Sie können einen Infoschritt auf Formularebene hinzufügen oder einen Infoschritt, der einem Steuerelement zugeordnet ist. Wenn ein Infoschritt einem Formular zugeordnet ist, wird die "Blase" des Aufgabenleitfadens ohne Zeiger irgendwo im Formular plaziert, wenn der Aufgabenleitfaden wiedergegeben wird. Wenn ein Infoschritt einem Steuerelement zugeordnet ist, wird die "Blase" des Aufgabenleitfadens auf das Steuerelement zeigen, wenn der Aufgabenleitfaden wiedergegeben wird.Im Hilfebereich wird ein Info-Schritt als nummerierter Schritt mit dem Text angezeigt, den Sie eingegeben haben. Verwenden Sie Infoschritte, um den Benutzer auf die nächsten Schritte vorbereiten, Schritte zu beschreiben, die außerhalb der Anwendung abgeschlossen werden müssen, oder um auf andere Aufzeichnungen zu verweisen (jedoch können Sie in den Anmerkungen keine Hyperinks erstellen.).

**Die Länge der Aufzeichnung bestimmen**

-   Im Allgemeinen liest oder spielt der Benutzer eine Aufzeichnung von Anfang bis Ende ab, darum sollten Sie Schritte oder Aufgaben nicht miteinander kombinieren, die besser separat durchgeführt werden.
-   Versuchen Sie nicht ein langes Szenario aufzuzeichnen, das mehrere Unterprozesse umfasst. Der "Erstellungsvorgang des Diensts für Debitoren" beispielsweise ist zu umfassend; unterteilen Sie ihn in kürzere Aufgaben wie "Rückgaben annehmen" und "Zu Geschenkkarte hinzufügen".
-   Wenn eine Aufgabe als Teil mehrerer verschiedener Geschäftsprozesse ausgeführt werden kann, erstellen Sie dafür eine separate Erfassung, und Sie können sich in den anderen Erfassungen darauf beziehen.
-   Wenn der Prozess mehrere Aufgaben betrifft, die die Person wahrscheinlich nicht alle auf einmal erledigt, können Sie die Aufgaben in einer Aufzeichnung beibehalten, beispielsweise "Funktionsprofile einrichten und zuweisen."
-   Wenn es sich um etwas handelt, dass nur einmalig ausgeführt werden muß (beispielsweise eine Konfiguration) und dann eine andere Aufgabe, die sofort danach, jedoch wiederholt und eigenständig, ausgeführt wird, teilen Sie sie in zwei Aufgabenaufzeichnungen auf.

**Legen Sie fest, wo in der Benutzeroberfläche eine Erfassung gestartet wird** Die Seite, auf der Sie sich befinden, wenn Sie mit der Aufnahme einer Aufgabenaufzeichnung starten, hat Auswirkungen darauf, für welche Seite der Aufgabenleitfaden angezeigt wird.Wenn also beispielsweise Ihre Aufgabenaufzeichnung im Hilfebereich aufgeführt werden soll, wenn ein Benutzer auf Hilfe auf der Seite "Hauptbuchparameter" klickt, müssen Sie die Aufzeichnung auf der Hauptbuchparameterseite starten. **Aufzeichnungen als .axtr-Dateien speichern** Wenn Sie das Erstellen oder Bearbeiten einer Aufgabenaufzeichnung beendet haben, werden Ihnen mehrere Optionen zum Herunterladen, oder Speichern der Aufzeichnung dargestellt. Sie können die Datei als Aufgabeaufzeichnungspaket (.axtr), als unformatierte Aufzeichnungsdatei (.xml) oder als Word-Dokument herunterladen, oder die Datei in einer LCS-Bibliothek speichern. Es wird empfohlen, Ihre Aufgabenaufzeichnung immer als Aufgabenaufzeichnungspaketdatei (.axtr) zu speichern. Dies unterstützt Sie dabei, die Verwaltung der Datei zu vereinfachen, wenn Prozeduren oder Anmerkungen später geändert werden müssen. Wenn Sie die Datei als Word-Dokument herunterladen möchten, speichern Sie sie ebenfalls als Aufgabenaufzeichnungspaketdatei.

## <a name="create-your-task-recording"></a>Ihre Aufgabenaufzeichnung erstellen
Detaillierte Durchführungsschritte finden Sie unter [Aufgabenrecorder-Ressourcen](task-recorder.md).

## <a name="copy-and-customize-microsofts-task-recordings"></a>Kopieren und Anpassen von Microsoft Aufgabenaufzeichnungen
Sie können die Microsoft Aufgabenaufzeichnungen herunterladen und bearbeiten, um sie für eine eigene Hilfedokumentation oder Trainingsmaterialien zu verwenden. Um eine Microsoft Aufgabenaufzeichnung herunterzuladen, führen Sie die folgenden Schritte aus:

1.  Aufgabenaufzeichnung öffnen. Die Aufgabenaufzeichnung finden Sie im Menü **Einstellungen**.
2.  Im klicken Sie Aufgabenaufzeichnungsbereich **Eine Aufzeichnung verwalten.**
3.  Klicken Sie unter **Wo ist die Aufzeichnung** auf **Befindet sich in einer LCS-Bibliothek**.
4.  Klicken Sie auf **LCS-Bibliothek auswählen**.
5.  Wählen Sie die globale Microsoft-Bibliothek aus.
6.  Wählen Sie in der Strukturdarstellung den Geschäftsprozessbibliotheksknoten aus, dem die Aufgabenaufzeichnung zugeordnet ist.
7.  Klicken Sie auf **OK**.
8.  Klicken Sie auf **Start**.
9.  An diesem Punkt durchlaufen Sie die Aufzeichnung und ändern dabei alle notwendigen Schritte, um sie zu überspielen.  **Hinweis**: Wenn Sie nur den Text der Aufzeichnung ändern müssen, können Sie die Aufzeichnung im Modus **Anmerkungen einer Aufzeichnung bearbeiten** öffnen und speichern ihn anschließend.
10. Nachdem die Aufzeichnung bis zum Ende abgespielt wurde, klicken Sie auf **Anhalten** in der Symbolleiste für die Aufgabenaufzeichnung am oberen Rand des Bildschirms.
11. Wählen Sie aus, wie Sie die Aufgabenaufzeichnung speichern wollen.



<a name="additional-resources"></a>Zusätzliche Ressourcen
--------

[Hilfesystem](../../fin-ops/get-started/help-overview.md)

[Das Hilfesystem verbinden](../../fin-ops/get-started/help-connect.md)

[Aufgabenaufzeichnung](task-recorder.md)

[Erstellen von umfangreicher Hilfethemen mit der Aufgabenaufzeichnung (externer Link)](https://mbspartner.microsoft.com/AX/Videos/970)
