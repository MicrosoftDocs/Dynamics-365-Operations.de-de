---
title: Neuzuweisung der Umsatzerkennung
description: In diesem Artikel geht es darum, wie Unternehmen mit der Neuzuweisung die Umsatzerlöspreise neu berechnen können, wenn sich die Vertragsbedingungen für einen Verkauf ändern. Im Artikel enthaltene Links verweisen auf andere Artikel, in denen erläutert wird, wie Umsatzerlöse in verschiedenen Fällen erkennt werden.
author: kweekley
manager: aolson
ms.date: 12/21/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-21
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 45fa888508e3d9c6be1e26ebcf2896ca0b538caf
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5238279"
---
# <a name="revenue-recognition-reallocation"></a>Neuzuweisung der Umsatzerkennung

[!include [banner](../includes/banner.md)]

Durch eine Neuzuweisung können Unternehmen die Umsatzerlöspreise neu berechnen, wenn sich die Vertragsbedingungen für einen Verkauf ändern. Zum Zwecke der Umsatzerkennung gelten die Auftragsdokumente als Vertrag.

Ihre Organisation muss selbst entscheiden, ob eine Neuzuweisung erforderlich ist. Wird ein Auftrag mit einer neuen Position ergänzt oder einem Debitor ein neuer Auftrag hinzugefügt, muss dies nicht unbedingt eine Vertragsänderung nach sich ziehen. In den folgenden Fällen bedarf es eventuell einer Neuzuweisung:

- Ein Debitor hat einen Auftrag mit weiteren Artikeln ergänzt oder Artikel aus dem Auftrag gelöscht, nachdem der Auftrag ganz oder teilweise in Rechnung gestellt wurde.
- Zu einem ausgehandelten Vertrag wurden mehrere Aufträge entweder im Status „Bestätigt“ oder „In Rechnung gestellt“ eingegeben.
- Ein Debitor hat einen Artikel zurückgeschickt oder eine Gutschrift dafür erhalten, nachdem der ursprüngliche Auftrag ganz oder teilweise in Rechnung gestellt wurde.

Bei Neuzuweisungen gibt es einige wichtige Einschränkungen:

- Eine Neuzuweisung kann nur einmal ausgeführt werden. Daher darf sie erst erfolgen, nachdem alle Änderungen vorgenommen wurden.
- Eine Neuzuweisung darf nicht bei Projektaufträgen erfolgen.
- Sind mehrere Aufträge betroffen, müssen sich diese auf dasselbe Kundenkonto beziehen.
- Alle Aufträge, die neu zugewiesen werden, müssen dieselbe Transaktionswährung haben.
- Einmal erfolgt, kann eine Neuzuweisung weder storniert noch rückgängig gemacht werden.

## <a name="set-up-reallocation"></a>Neuzuweisung einrichten

Neuzuweisungen werden durch einen Parameter beeinflusst.

Weil Neuzuweisungen bei Aufträgen erfolgen können, die teilweise oder vollständig in Rechnung gestellt wurden, müssen alle vorherigen Buchhaltungseinträge zur Rechnung mithilfe der neuen, neu zugewiesenen Umsatzerlöspreise korrigiert werden. Diese Korrektur erfolgt durch Stornieren des Buchungseintrags der ursprünglichen Rechnung sowie Buchen eines neuen Eintrags, bei dem die neu zugewiesenen Umsatzerlöspreise berücksichtigt werden.

Jede Organisation muss entscheiden, ob durch die Korrektur nur das Hauptbuch aktualisiert werden soll oder auch die Debitorenkonten. Diese Entscheidung bestimmt, welche Einstellung für die Option **Rechnungskorrekturen auf Debitorenkonten buchen** auf der Registerkarte **Umsatzerkennung** der Seite **Hauptbuchparameter** (**Umsatzerkennung \> Einrichtung \> Hauptbuchparameter**) festzulegen ist. Die Einstellung richtet sich nach dem Anwendungsfall. Weitere Informationen zu möglichen Anwendungsfällen erhalten Sie an späterer Stelle in diesem Artikel über die Links im Abschnitt [Szenarien zur Neuzuweisung](#scenarios-for-reallocation).

[![Registerkarte „Umsatzerkennung“ auf der Seite „Hauptbuchparameter“](./media/01_RevRecScenarios.png)](./media/01_RevRecScenarios.png)

Ist die Option **Rechnungskorrekturen auf Debitorenkonten buchen** auf **Ja** gesetzt, führt die Neuzuweisung zu folgendem Ergebnis:

- In der Debitorenbuchhaltung wird eine Gutschrift erstellt, um die zu korrigierende Rechnung zu stornieren.

    - In der Gutschrift wird die ursprüngliche Rechnungsnummer verwendet, allerdings mit der Ergänzung „-1“.
    - Die Gutschrift wird automatisch mit der Originalrechnung verrechnet. Wurde die ursprüngliche Rechnung bereits mit einer anderen Gutschrift oder Zahlung verrechnet, wird diese Abrechnung automatisch storniert.
    - Die Gutschrift wird in das Hauptbuch gebucht, um den zur Originalrechnung gebuchten Buchhaltungseintrag zu stornieren. Die Transaktionsbuchungen zu Bestand und COGS (Wareneinsatz) werden jedoch nicht storniert.

- In der Debitorenbuchhaltung wird anhand der neu zugewiesenen neuen Preise eine neue Rechnung erstellt.

    - Für diese wird die ursprüngliche Rechnungsnummer verwendet, allerdings mit der Ergänzung „-2“.
    - Die neue Rechnung wird automatisch mit allen Gutschriften oder Zahlungen verrechnet, die zuvor mit der ursprünglichen Rechnung verrechnet wurden.
    - Die neue Rechnung wird unter Verwendung der neu zugewiesenen neuen Umsatzerlöspreise in das Hauptbuch gebucht. Sie wird nicht erneut auf die Konten für Bestand und COGS (Wareneinsatz) gebucht, weil diese Buchungen im Buchungseintrag der Originalrechnung enthalten sind.

Ist die Option **Rechnungskorrekturen auf Debitorenkonten buchen** auf **Nein** gesetzt, führt die Neuzuweisung zu folgendem Ergebnis:

- Eine Stornobuchung wird nur ins Hauptbuch gebucht. Alle Buchungen mit Bezug zur ursprünglichen Rechnung werden storniert mit Ausnahme der Buchungen zu Bestand und COGS (Wareneinsatz).
- Eine neue Buchung unter Berücksichtigung der neu zugewiesenen neuen Umsatzerlöspreise erfolgt nur im Hauptbuch. Sie wird nicht erneut auf die Konten für Bestand und COGS (Wareneinsatz) gebucht, weil diese Buchungen im Buchungseintrag der Originalrechnung enthalten sind.
- Die Rechnung auf der Seite **Debitorentransaktionen** ist weder betroffen noch wird sie geändert, sondern spiegelt nach wie vor die ursprüngliche Buchung wider. Es gibt keinen Hinweis auf Stornierung oder neue Buchungen.

Wie bereits erwähnt, kann nur das Hauptbuch oder sowohl das Hauptbuch als auch die Debitorenbuchhaltung aktualisiert werden. Beides ist mit Vor- und Nachteilen verbunden. Wir empfehlen, anhand der Anforderungen des Unternehmens zu entscheiden, welche Option verwendet werden soll. Werden sowohl das Hauptbuch als auch die Debitorenbuchhaltung aktualisiert, werden die berichtigten Buchungen in der neuen Rechnung angezeigt und können im Beleg auf der Seite **Debitorentransaktionen** eingesehen werden. Außerdem werden zur Verrechnung die aktualisierten Buchungen herangezogen, um Skonto und Gewinne oder Verluste zu buchen. Auf der anderen Seite werden die Gutschrift und die neue Rechnung, so wie bei anderen Gutschriften und Kundenrechnungen auch, in Kundenauszügen und Fälligkeitsberichten vermerkt. Aus der Beschreibung dieser Dokumente geht hervor, dass sie das Ergebnis einer Buchhaltungskorrektur sind.

## <a name="run-the-reallocation-process"></a>Neuzuweisung ausführen

Um eine Neuzuweisung auszuführen, wählen Sie in einem beliebigen Auftrag, bei dem eine Neuzuweisung erforderlich ist, die Option **Preis mit neuen Auftragspositionen erneut zuteilen** aus. Alternativ wählen Sie **Umsatzerkennung \> Periodische Aufgaben \> Preis mit neuen Auftragspositionen erneut zuteilen** aus, und geben Sie dann die entsprechenden Filter ein, z. B. das Debitorenkonto.

[![Seite „Preis mit neuen Auftragspositionen erneut zuteilen“](./media/02_RevRecScenarios.png)](./media/02_RevRecScenarios.png)

Das obere Raster auf der Seite **Preis mit neuen Auftragspositionen erneut zuteilen** heißt **Aufträge**. In ihm sind die Aufträge des Kunden aufgeführt. Wählen Sie die Aufträge aus, bei denen eine Neuzuweisung erforderlich ist. Projektaufträge können nicht ausgewählt werden, weil bei diesen keine Neuzuweisung möglich ist. Auch Aufträge, die bereits eine Neuzuweisungs-ID haben, können nicht ausgewählt werden, weil bei einem Auftrag immer nur eine Neuzuweisung möglich ist. Hat ein Auftrag eine Neuzuweisungs-ID, wurde er bereits von einem anderen Benutzer zwecks einer Neuzuweisung markiert.

Das untere Raster auf der Seite heißt **Positionen**. Nachdem Sie im Raster **Aufträge** einen oder mehrere Aufträge ausgewählt haben, werden im Raster **Positionen** die Auftragspositionen aufgeführt. Wählen Sie die Auftragspositionen aus, bei denen eine Neuzuweisung erforderlich ist. Wird nur eine Auftragsposition ausgewählt, müssen die Positionen aus demselben Auftrag neu zugewiesen werden. Dieser Fall kann auftreten, wenn eine der Auftragspositionen zuvor in Rechnung gestellt wurde und dann eine neue Position ergänzt oder eine vorhandene Position gelöscht oder storniert wurde. Gelöschte Positionen werden nicht im Raster angezeigt. Insofern können sie auch nicht ausgewählt werden. Dennoch werden sie bei der Neuzuweisung berücksichtigt.

Nach Auswahl der erforderlichen Auftragspositionen, verwenden Sie die Schaltflächen im Aktionsbereich wie folgt:

- **Neuzuweisung aktualisieren**: Für die ausgewählten Auftragspositionen werden die neuen Umsatzerlöspreise berechnet. Wurde eine Position gelöscht oder storniert, erfolgt die Neuzuweisung nur bei den vorhandenen ausgewählten Positionen. Die folgende Abbildung zeigt ein Beispiel für Auftragspositionen vor Aktualisierung der Neuzuweisung.

    [![Auftragspositionen vor Aktualisierung der Neuzuweisung](./media/03_RevRecScenarios.png)](./media/03_RevRecScenarios.png)

    Die neuen Umsatzerlöspreise werden im Raster **Positionen** in der Spalte **Neu zugewiesener Betrag** angezeigt. Zu diesem Zeitpunkt wurde die Neuzuweisung zwar verarbeitet, eine Berechnung hat aber noch nicht stattgefunden. Die folgende Abbildung zeigt ein Beispiel für Auftragspositionen nach Aktualisierung der Neuzuweisung.

    [![Auftragspositionen nach Aktualisierung der Neuzuweisung](./media/04_RevRecScenarios.png)](./media/04_RevRecScenarios.png)

- **Verarbeiten**: Die neu zugewiesenen Umsatzerlöspreise werden verarbeitet oder gebucht. Nach Betätigung dieser Schaltfläche kann die Neuzuweisung nicht mehr rückgängig gemacht werden. Wenn Sie vor Klicken auf **Verarbeiten** nicht auf **Neuzuweisung aktualisieren** geklickt haben, erfolgt die Neuzuweisung automatisch.

    - Wurde keine Auftragsposition in Rechnung gestellt, werden die Umsatzerlöspreise bei allen Aufträgen aktualisiert, die zwecks einer Neuzuweisung ausgewählt wurden.
    - Wurden eine oder mehrere Auftragspositionen in Rechnung gestellt, werden Korrekturbuchungen gebucht, und alle Angaben aus dem Umsatzerlöszeitplan, der zur in Rechnung gestellten Auftragsposition erstellt wurde, werden berichtigt.

- **Erwarteter Beleg**: Die Buchungen zu allen in Rechnung gestellten Auftragspositionen werden in einer Vorschau angezeigt. Wurden keine Positionen in Rechnung gestellt, wird nichts angezeigt. Wenn Sie vor Klicken auf **Erwarteter Beleg** nicht auf **Neuzuweisung aktualisieren** geklickt haben, erfolgt die Neuzuweisung automatisch.
- **Neuzuweisung des Umsatzerlöses**: Die Neuzuweisung des Umsatzerlöspreises aller ausgewählten Positionen wird auf einer Seite angezeigt. Die dort angegeben Informationen können nicht geändert werden. Vermerkt sind die Positionsbeträge, die zur Neuzuweisung herangezogen wurden.

    [![Positionsbeträge, die zur Neuzuweisung herangezogen wurden](./media/05_RevRecScenarios.png)](./media/05_RevRecScenarios.png)

- **Daten für ausgewählten Kunden zurücksetzen**: Wurde die Neuzuweisung begonnen, aber nicht abgeschlossen, werden die Daten aus der Neuzuweisungstabelle nur mit Bezug zum ausgewählten Kunden gelöscht. Wenn Sie beispielsweise mehrere Auftragspositionen zwecks einer Neuzuweisung markieren und die Seite ohne Auswahl von **Verarbeiten** geöffnet lassen, läuft das Zeitlimit der Seite ab. In diesem Fall bleiben die Auftragspositionen markiert, und ein anderer Benutzer kann sie nicht verwenden, um die Neuzuweisung abzuschließen. Die Seite ist beim Öffnen möglicherweise sogar leer. In diesem Fall können Sie mit der Schaltfläche **Daten für ausgewählten Kunden zurücksetzen** unverarbeitete Aufträge löschen, damit ein anderer Benutzer die Neuzuweisung beenden kann.

## <a name="scenarios-for-reallocation"></a>Anwendungsfälle von Neuzuweisungen

Im folgenden werden diverse Fälle von Umsatzerkennung aufgezeigt:

- [Neuzuweisung der Umsatzerkennung – Szenario 1](rev-rec-reallocation-scenario-1.md) – Es werden zwei Aufträge eingegeben, die aber nur bestätigt werden. Liegen mehr als zwei Aufträge mit dem Status „Bestätigt“ vor, ist das Ergebnis ähnlich.
- [Neuzuweisung der Umsatzerkennung – Szenario 2](rev-rec-reallocation-scenario-2.md) –Zwei Aufträge werden eingegeben. Nachdem der erste Auftrag in Rechnung gestellt wurde, ergänzt der Kunde den Vertrag mit einem Artikel.
- [Neuzuweisung der Umsatzerkennung – Szenario 3](rev-rec-reallocation-scenario-3.md) – Einem bestehenden und in Rechnung gestellten Auftrag wird eine neue Position hinzugefügt.
- [Neuzuweisung der Umsatzerkennung – Szenario 4](rev-rec-reallocation-scenario-4.md) – Aus einem bestehenden und teilweise in Rechnung gestellten Auftrag wird eine Position gelöscht.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]