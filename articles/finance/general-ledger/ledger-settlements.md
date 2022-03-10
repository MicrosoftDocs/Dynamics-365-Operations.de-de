---
title: Sachkontoausgleiche
description: In diesem Thema wird erläutert, wie die Sachkontoausgleichseite verwendet wird, um Sachkontobuchungen und Stornierungs-Ausgleiche auszugleichen.
author: kweekley
ms.date: 01/31/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerTransSettlement
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-11-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: e98b012210338e7f18cb874eefbc8a023aa4428b
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8075323"
---
# <a name="ledger-settlements"></a>Sachkontoausgleiche

[!include [banner](../includes/banner.md)]

Die Hauptbuchabrechnung ist der Prozess des Abgleichs von Soll- und Haben-Transaktionen im Hauptbuch. Die Abrechnung der Soll- und Habenbeträge dient dazu, den Saldo des Sachkontos mit den detaillierten Transaktionen abzustimmen, aus denen sich dieser Saldo zusammensetzt.

Abgerechnete Transaktionen können von Abfragen und Berichten ausgeschlossen werden. Auf diese Weise ist es einfacher, die offenen Transaktionen des Sachkontos zu analysieren, aus denen sich der Saldo des Sachkontos zusammensetzt.

> [!IMPORTANT] 
> Die Module Accounts payable (AP) und Accounts receivable (AR) verfügen auch über die Abrechnung von Rechnungen und Zahlungen. Wenn die Abrechnung in den untergeordneten Sachkonten AR und AP erfolgt, werden die entsprechenden Ledger-Einträge nicht automatisch abgerechnet.

## <a name="ledger-settlement-features"></a>Funktionen der Sachkontoabrechnung
In Microsoft Dynamics 365 Finance Version 10.0.21 wurde die Option **Erweiterte Hauptbuchabrechnung aktivieren** von der Seite **Hauptbuchparameter** entfernt. Die erweiterte Abrechnung von Sachkonten ist jetzt immer aktiviert.
In Finance Version 10.0.25 wurde die Funktion **Wissen zwischen Sachkontoabrechnung und Jahresabschluss** eingeführt. Diese Funktion ändert die grundlegende Funktionalität sowohl der Sachkontoabrechnung als auch des Jahresabschlusses des Hauptbuchs. Bevor Sie diese Funktion im Arbeitsbereich **Funktionsverwaltung** aktivieren, siehe, [Abgleich zwischen Sachkonto und Jahresabschluss](awareness-between-ledger-settlement-year-end-close.md).

## <a name="set-up-ledger-settlement"></a>Sachkontoabrechnung festlegen
Sie müssen die Hauptkonten auswählen, für die Sie die Sachkontenabrechnung durchführen möchten. Es gibt zwei Möglichkeiten, diese Hauptkonten auszuwählen.

1. Gehen Sie zu **Hauptbuch** > **Hauptbuch-Einrichtung** > **Hauptbuch-Parameter**.
2. Wählen Sie auf der Registerkarte **Sachkontenabrechnungen** die Kontenpläne aus, aus denen Sie die Hauptkonten auswählen möchten.
3. Wählen Sie die Hauptkonten aus, für die die Sachkonten abgerechnet werden sollen. Da Kontenpläne global sind, werden für alle Firmen, denen die ausgewählten Kontenpläne zugeordnet sind, dieselben Hauptkonten für die Sachkontenabrechnung ausgewählt.

  – oder –

1. Gehen Sie zu **Hauptbuch** > **Periodische Aufgaben** > **Sachkonto Abrechnungen**.
2. Wählen Sie **Sachkonten abrechnen**.
3. Wählen Sie in dem Dialogfenster die Kontenpläne und Hauptkonten aus, für die Sie eine Sachkontoabrechnung durchführen möchten. Dieses Dialogfeld ist eine Abkürzung. Alle Hauptkonten, die Sie hier hinzufügen, werden auch auf der Seite **Hauptbuchparameter** angezeigt.

Sie können die gleichen grundlegenden Verfahren verwenden, um Hauptkonten jederzeit aus der Sachkontoabrechnung zu entfernen. Das Entfernen eines Hauptkontos hat keine Auswirkungen auf frühere Sachkontoabrechnungen. Das Hauptkonto und die Transaktionen werden jedoch nicht mehr auf der Seite **Sachkontoabrechnung** angezeigt.

## <a name="settle-transactions"></a><a name="settle-transactions"></a>Buchungen ausgleichen
Um Sachkontobuchungen auszugleichen, folgen Sie diesen Schritten.

1. Gehen Sie zu **Hauptbuch** > **Periodische Aufgaben** > **Sachkonto Abrechnungen**.
2. Setzen Sie die Filter oben auf der Seite fest:

    - Wählen Sie einen Datumsbereich. Alternativ können Sie auch einen Code für ein Datumsintervall auswählen, um den Datumsbereich automatisch auszufüllen. Wir raten Ihnen davon ab, Sachkonten für Transaktionen abzurechnen, die sich über mehrere Geschäftsjahre erstrecken.
    - Ändern Sie die Buchungsebene nach Bedarf. Sie können keine Transaktionen abrechnen, die sich in verschiedenen Buchungsebenen befinden.
    - Um das Hauptkonto und die Dimensionen separat anzuzeigen, wählen Sie ein Finanzdimensionen-Set.

3. Wählen Sie **Buchungen anzeigen**, um alle Buchungen anzuzeigen, die mit den Filtern und den  Kontenlisten übereinstimmen, die Sie festgelegt haben, als Sie die Kontenplanliste im vorherigen Abschnitt eingerichtet haben.

    - Wenn Sie Filter- oder Dimensionseinstellungen ändern, müssen Sie **Buchungen anzeigen** wieder aktivieren.
    - Um die Transaktionen nach einem einzelnen Hauptkonto zu filtern, verwenden Sie den Filter im Feld **Sachkonto**. Wir raten Ihnen davon ab, Sachkonten für Transaktionen abzurechnen, die auf verschiedene Hauptkonten gebucht werden.

4. Wählen Sie Zeilen für die Abrechnung. Der Wert im Feld **Ausgewählter Betrag** oben auf der Seite erhöht oder verringert sich, um den Gesamtbetrag der ausgewählten Zeilen wiederzugeben.
5. Wenn Sie die Auswahl der Transaktionen abgeschlossen haben, wählen Sie **Ausgewählte markieren**. Für jede ausgewählte Transaktion erscheint ein Häkchen in der Spalte **Markiert**. Außerdem erhöht oder verringert sich der Wert im Feld **Markierter Betrag** oberhalb des Rasters, um den Gesamtbetrag auf den markierten Zeilen wiederzugeben.
6. Wenn der Wert im Feld **Markierte Menge** **0** (Null) ist, wählen Sie **Markierte Transaktionen ausgleichen**. Der Status der markierten Transaktionen wird auf **Ausgeglichen** geändert.

    > [!IMPORTANT]
    > Alle Transaktionen, die Sie für die aktive juristische Entität zur Abrechnung markiert haben, werden abgerechnet, auch wenn sie derzeit nicht auf der Abrechnungsseite des Sachkontos angezeigt werden, weil Sie einen Filter angewendet haben.

## <a name="make-transactions-easier-to-find"></a>Suchen Sie Transkaktionen einfacher
Die Seite **Sachkontoabrechnungen** enthält Funktionalitäten, die es Ihnen erleichtern, die Transaktionen anzuzeigen, die Sie für die Abrechnung benötigen.

- Verwenden Sie den Filter **Markiert**, um Transaktionen danach zu filtern, ob das Kontrollkästchen **Markiert** für sie aktiviert ist.
- Verwenden Sie den Filter **Status**, um Transaktionen nach ihrem Status zu filtern.
- Wählen Sie **Sortieren nach absolutem Betrag**, um die Beträge nach absolutem Wert zu sortieren. Auf diese Weise können Sie Belastungen und Gutschriften, die denselben Betrag haben, gruppieren.

## <a name="reverse-a-settlement"></a>Ausgleich stornieren
Sie können einen Ausgleich stornieren, die versehentlich vorgenommen wurde.

1. Führen Sie die Schritte 1 bis 3 im Abschnitt [Transaktionen abrechnen](#settle-transactions) aus, um die Transaktionen anzuzeigen, an denen Sie interessiert sind.
2. Wählen Sie im Feld **Status** die Option **ausgeglichen** aus.
3. Wählen Sie Zeilen für die Umkehrung aus.
4. Wählen Sie **Markierte Transaktionen rückgängig machen**. Der Status aller Transaktionen, die dieselbe Abrechnungs-ID haben, wird auf **Nicht abgerechnet** aktualisiert.

    > [!IMPORTANT]
    > Alle Transaktionen, die die gleiche Abrechnungs-ID haben, werden storniert, auch wenn sie nicht markiert sind. Zum Beispiel wurden vier Zeilen markiert und abgerechnet. Alle vier Zeilen haben die gleiche Abwicklungs-ID. Wenn Sie eine dieser vier Zeilen markieren und dann **Markierte Transaktionen stornieren** wählen, werden alle vier Zeilen storniert.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
