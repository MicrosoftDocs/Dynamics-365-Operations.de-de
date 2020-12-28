---
title: Bankauszugsabstimmung mithilfe der erweiterten Bankabstimmung
description: Mit der erweiterten Bankabstimmungsfunktion können Sie elektronische Bankauszüge importieren und diese in Microsoft Dynamics 365 Finance automatisch mit Bankbuchungen abstimmen. Dieses Thema beschreibt den Abstimmungsprozess.
author: saraschi2
manager: AnnBe
ms.date: 06/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankReconciliationWorksheet
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 98243
ms.assetid: 9df13adf-aa9d-4f6b-bde6-25a214611692
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c13203217af1788fe3b8a6f9bbf805e03b650a0d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4443575"
---
# <a name="reconcile-bank-statements-by-using-advanced-bank-reconciliation"></a>Bankauszugsabstimmung mithilfe der erweiterten Bankabstimmung

[!include [banner](../includes/banner.md)]

Mit der erweiterten Bankabstimmungsfunktion können Sie elektronische Bankauszüge importieren und diese in Dynamics 365 Finance automatisch mit Bankbuchungen abstimmen. Dieses Thema beschreibt den Abstimmungsprozess.  

<a name="import-an-electronic-bank-statement"></a>Import eines elektronischen Bankauszugs
-----------------------------------

Sie Importieren die Bankauszüge mithilfe der **Auszug importieren**-Aktivität auf der Seite **Bankauszüge**. Auf dem Bankauszug wird das Bankkonto durch eine Kombination der in den Bankkontodetails eingerichteten Werten identifiziert. Dazu gehören Bankname, Bankkontonummer, Bankleitzahl, SWIFT-Code (Society for Worldwide Interbank Financial Telecommunication) und IBAN (International Bank Account Number). 

Sie können einen Bankauszug hochladen, der Informationen für entweder ein einzelnes Konto oder mehrere Konten enthält. Wenn es mehrere Konten gibt, können sich die Konten bei unterschiedlichen juristischen Personen befinden.

-   Um eine einzelne Bankauszugsdatei für ein einzelnes Konto zu importieren, legen Sie die Option **Bankauszug für mehrere Bankkonten in allen juristischen Personen importieren** auf **Nein** fest, und wählen Sie das Bankkonto aus, dem der Auszug zugeordnet ist. Klicken Sie auf **Durchsuchen**, um die zugeordneten Bankauszugdatei auszuwählen. Klicken Sie dann auf **Hochladen**.
-   Um eine einzelne Bankauszugsdatei für mehrere Konten zu importieren, legen Sie die Option **Bankauszug für mehrere Bankkonten in allen juristischen Personen importieren** auf **Ja** fest. Klicken Sie auf **Durchsuchen**, um die zugeordneten Bankauszugdatei auszuwählen. Klicken Sie dann auf **Hochladen**.

Wenn Bankauszüge in der elektronischen Datei mithilfe der identifizierenden Felder keinem Bankkonto zugeordnet werden können oder mehreren Bankkonten zugeordnet sind, werden sie nicht importiert. Allerdings können andere Auszüge in der Datei noch importiert werden. Der Benutzer erhält dann eine Nachricht, die besagt, dass der Import von Bankauszügen für bestimmte Bankkonten nicht erfolgreich war. Beachten Sie, dass der Benutzer, der die Bankauszugsdatei importiert, Zugriff auf eine juristische Person haben muss, um Auszüge für die Bankkonten dieser juristischen Person zu importieren. 

Sie können mit einer ZIP-Datei mehrere Auszugsdateien in Finance in einem einzigen Prozess hochladen. Um mehrere Bankauszugsdateien für mehrere Konten zu importieren, fassen Sie alle Bankauszugsdateien in einer Zip-Datei zusammen. Im Dialogfeld **Bankauszüge importieren** legen Sie die Option **Bankauszug für mehrere Bankkonten in allen juristischen Personen importieren** auf **Ja** fest. Klicken Sie auf **Durchsuchen**, um die Zip-Datei mit den zugeordneten Bankauszugdateien auszuwählen. Klicken Sie dann auf **Hochladen**. Beim Importprozess wird die ZIP-Datei erkannt und jeder Auszug hochgeladen, der in ihr enthalten ist, unabhängig von der juristischen Person des Bankkontos.

Es ist eine **Nach Import abstimmen**-Option verfügbar. Wenn Sie diese Option auf **Ja** festlegen, überprüft das System automatisch den Bankauszug, erstellt eine neue Bankabstimmung und ein Arbeitsblatt und führt den standardmäßigen Abgleichsregelsatz beim Upload des Bankauszugs aus. Diese Funktionalität automatisiert den Prozess bis zu manuellen Abstimmung von Buchungen.

## <a name="validate-the-bank-statement"></a>Bankauszug überprüfen
Um einen Auszug zu überprüfen, klicken Sie auf der Seite **Bankauszüge** auf **Überprüfen**. Bankauszüge müssen überprüft werden, bevor sie abgestimmt werden können. Dieser Schritt wird automatisch abgeschlossen, wenn Sie die Option **Nach Import abstimmen** beim Import auf **Ja** festlegen. 

Die Bankauszugsprüfung prüft die folgenden Details:

-   Der Bankauszug entspricht dem ausgewählten Bankkonto.
-   Die Währung des Bankauszugs entspricht der Währung des ausgewählten Bankkontos.
-   Der Anfangssaldo des Auszugs entspricht dem Abschlusssaldo des vorherigen Auszugs für das Bankkonto.
-   Das Datum überlappt nicht mit dem Datum für einen anderen Bankauszug für das selbe Bankkonto.
-   Es gibt keine Lücken in den Datumsangaben für Auszüge für das Bankkonto.
-   Daten von Auszugspositionen liegen zwischen dem Ab-Datum und dem Bis-Datum des Bankauszugs.
-   Der Anfangssaldo und die summierten Positionsbeträge entsprechen dem Abschlusssaldo.

Wenn die Überprüfung abgeschlossen ist, wird der Status des Bankauszugs auf **Überprüft** aktualisiert. Bankauszüge müssen überprüft werden, bevor sie abgestimmt werden können.

## <a name="reconcile-the-bank-statement"></a>Abstimmen von Bankauszügen
Nachdem Sie einen elektronischen Bankauszug importiert haben und den Auszug auf der Seite **Bankauszüge** geprüft haben, können Sie den Bankauszug auf den Seiten **Bankabstimmung** und **Bankabstimmungsarbeitsblatt** abstimmen. 

Auf der Seite **Bankabstimmung** klicken Sie auf **Neu**, um eine neue Abstimmung zu erstellen. Wählen sie dann das Bankkonto des importierten Auszugs. Ein Bankkonto kann nur eine geöffnete Bankabstimmung haben. Der Stichtag bestimmt, welche Bankkontoauszugsbuchungen und Operations-Bankbuchungen in einem Abstimmungsarbeitsblatt enthalten sind. Standardmäßig wird das aktuelle Systemdatum als Stichtag verwendet, aber Sie können das Datum für die Abstimmung ändern. Die verbleibenden Headerinformationen werden automatisch aus dem Auszug entnommen. Dieser Schritt wird automatisch abgeschlossen, wenn Sie die Option **Nach Import abstimmen** beim Import auf **Ja** festlegen. 

Auf der Seite **Bankabstimmung** klicken Sie auf **Arbeitsblatt**, um die Seite **Bankabstimmungsarbeitsblatt** zu öffnen. Wenn Sie die Option **Nach Import abstimmen** auf **Ja** festlegen, wird der Standard-Abgleichsregelsatz für die Abstimmung automatisch ausgeführt. Um Abgleichsregeln manuell auszuführen, klicken Sie auf **Abgleichsregeln ausführen**, um Abgleichsregelsätze oder Abgleichsregeln für Bankbuchungen auszuwählen. Haben Sie viele Transaktionen verarbeiten müssen, können Sie diesen Schritt als Stapelverarbeitungsvorgang abschließen. 

Die Seite **Bankabstimmungsarbeitsblatt** hat vier Raster mit Transaktionen. Die beiden oberen Raster zeigen Transaktionen aus dem Bankauszug sowie Vorgänge an, die noch nicht abgeglichen wurden. Die beiden unteren Raster anzeigen übereinstimmende Transaktionen Die **Bankauszug-Buchungsdetails**-Registerkarte zeigt Details für die nicht abgeglichene Bankauszugsbuchung, die im oberen Raster ausgewählt ist. 

Es gibt drei Möglichkeiten zum Abgleich oder zur Abstimmung von Bankauszugsbuchungen:

-   Gleichen Sie die Transaktionen mit Operations-Banktransaktionen ab.
-   Zuordnen der Transaktionen mit einer Rückbuchungsbankauszugsbuchung.
-   Markieren Sie die Transaktionen als **Neu**, sodass sie später als Bankbuchung in Finance gebucht werden können.

Um manuell Transaktionen zuzuordnen, wählen Sie die Transaktionen im Raster **Bankauszugbuchungen** aus, wählen Sie die entsprechenden Buchungen im Raster **Operations-Bankbuchungen** aus, und klicken Sie dann auf **Zuordnen**. Die ausgewählten Buchungen werden von den oberen Rastern für nicht zugeordnete Buchungen in die unteren Raster für zugeordnete Buchungen verschoben. Außerdem werden die Gesamtbeträge für zugeordnete und nicht zugeordnete Buchungen aktualisiert. Sie können Buchungen 1:1, 1:n und n:n zuordnen. Abgleiche müssen den Regeln für zulässigen Datumsabweichungen und Buchungstypen entsprechen. Diese Regeln werden auf der Seite **Bargeld- und Bankverwaltungsparameter** eingerichtet.

Bei der Abstimmung können Centdifferenzen auftreten. Sie können eine einzelne Bankauszugsbuchung und eine einzelne Operations-Bankbuchung zuordnen, die Centdifferenzen aufweisen, wenn diese Centdifferenzen innerhalb der über das Feld **Zulässige Centdifferenz** des Bankkontos definierten Toleranz liegen. Der Betrag wird im Feld **Korrekturbetrag** auf der abgeglichenen Operations-Bankbuchung angezeigt. Wenn die Bankabstimmung als abgestimmt markiert ist, werden Korrekturen mithilfe des im zugeordneten Bankbchungstyps definierten Hauptkontos automatisch gebucht. Korrekturen werden für die Dokumenttypen **Scheck** und **Einzahlung** nicht unterstützt. 

Rückbuchungen für Bankauszugsbuchungen werden über das Abstimmungsarbeitsblatt zugeordnet. Zwei Auszugspositionen können zugeordnet werden, wenn sich die Beträge ausgleichen und wenn eine der Transaktionen als Rückbuchung markiert ist. Sie können auch eine Abgleichsregel für die **Rückbuchungsauszugspositionen löschen**-Aktion festlegen.

Zurückgebuchte Operations-Bankbuchungen müssen über die Seite **Operations-Bankbuchungen** abgestimmt werden. Sie können zwei Operations-Bankbuchungen gemeinsamen abstimmten, wenn bei den Dokumenten Bankkonto, Dokumenttyp und Zahlungsreferenz übereinstimmen und wenn sich die Beträge miteinander ausgleichen. Sie können auch einen einzelnen stornierten Scheck abstimmen, um die Anzeige dieser Transaktionen auf dem Abstimmungsarbeitsblatt zu verhindern. 

Wenn es neue von der Bank initiierte Transaktionen gibt (z. B. Zinsen, Gebühren und Abgaben), die noch nicht in Finance enthalten sind, können Sie diese in einer Erfassung hinzufügen, die der ausgewählten Bankauszugsabstimmung zugeordnet ist. Wählen Sie eine Bankauszugsbuchung im Raster **Bankauszugsbuchung** für nicht abgeglichene Transaktionen und klicken Sie dann auf **Als neu markieren**. Der Status der Transaktion wird auf **Neu** festgelegt, und die Buchung wird zum Raster **Bankauszugsbuchungen** für zugeordnete Transaktionen verschoben. Als **Neu** markierte Transaktionen buchen Sie später über die Seite **Bankauszug**. 

Sie können den Abgleich bei falsch zugeordneten Transaktionen aufheben. Wählen Sie die zugeordnete Bankauszugsbuchung, und klicken Sie dann auf **Abgleich aufheben**. Alle zugeordneten Transaktionen werden in die oberen Raster für nicht abgeglichene Transaktionen zurück verschoben, und die Gesamtbeträge werden aktualisiert. 

Nach Abschluss des Abstimmungsprozesses sollten Sie das Bankabstimmungsarbeitsblatt als abgestimmt markieren  Durch diesen Prozess werden automatisch Korrekturbeträge mithilfe der Konten gebucht, die auf der Seite **Bankbuchungsart** festlegt sind.  Die Bankabstimmung für einen Auszug kann als abgestimmt markiert werden, auch wenn Bankauszugspositionen vorhanden sind, die noch nicht abgestimmt wurden.  Die nicht abgestimmten Buchungen werden automatisch auf das nächste Abstimmungsarbeitsblatt als nicht abgestimmte Bankauszugsbuchungen, die abgestimmt werden müssen, übertragen.  Beachten Sie, dass die Kennzeichnung einer Bankauszugsabstimmung als abgestimmt nicht rückgängig gemacht werden kann.  Die Abstimmung kann nicht mehr bearbeitet werden und auch nicht mehr aktualisiert werden.

## <a name="post-new-transactions-that-are-associated-with-the-reconciliation"></a>Buchen neuer Transaktionen, die der Abstimmung zugeordnet sind
Bankauszugsbuchungen, die Sie auf dem Abstimmungsarbeitsblatt als **Neu** gekennzeichnet haben, werden über die Seite **Bankauszug** gebucht. Auf der Seite **Bankauszug** wählen Sie Auszugskennung, um die Abstimmungsdetails anzuzeigen. Im **Buchhaltung**-Menü können Sie die Optionen **Verteilung anzeigen** und **Buchung anzeigen** nutzen, um die Details hinter den neuen Transaktionen und die zugeordneten Hauptbucheinträge anzuzeigen. Wählen Sie die Option **Buchen**, um die Bankauszugspositionen zu buchen, die im Hauptbuch als **Neu** markiert sind. Beachten Sie, dass die Buchung nur einmal pro Bankauszug durchgeführt werden kann.



