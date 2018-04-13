---
title: "Konvertieren von Buchhaltungs- oder Berichtswährungen"
description: "Ein Unternehmen, das die Buchhaltungswährung oder Berichtswährung ändern muss, verfügt über zwei Optionen."
author: aprilolson
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 78223
ms.assetid: 31c56f9a-9c64-40a2-90e3-1969a760614b
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: ad840f4ed2cf27615e699a13fcd8be7f3c2cd5c8
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="convert-accounting-or-reporting-currencies"></a>Konvertieren von Buchhaltungs- oder Berichtswährungen

[!INCLUDE [banner](../includes/banner.md)]

Ein Unternehmen, das die Buchhaltungswährung oder Berichtswährung ändern muss, verfügt über zwei Optionen. Die erste Option ist, ein neues Unternehmen zu erstellen und neu zu beginnen. Die zweite Option ist, den Buchhaltungs- und den Berichtswährungsumwandlungsprozess auszuführen. Dies ist ein Prozess mit sehr langer Laufzeit, der jede Buchung im System ändert. Bevor Sie den Prozess ausführen können, sind zusätzliche Einstellungen erforderlich.

## <a name="preparing-the-legal-entity-for-currency-conversion"></a>Vorbereiten einer juristische Person für eine Währungskonvertierung
Bevor Sie die Währung der juristischen Person umrechnen können, müssen Sie alle Neubewertungen der Fremdwährung für Debitoren- und Kreditorenkonten zurücksetzen und die vorherigen Geschäftsjahre schließen. Sie müssen außerdem die Datenbank auf die Umrechnung vorbereiten, und anschließend die erforderlichen Änderungen am Konto der juristischen Person vornehmen, für die eine Währungskonvertierung erfolgen soll. Nachdem Sie eine Währungskonvertierung abgeschlossen haben, müssen Sie mehrere zusätzliche Verfahren abschließen. Sie müssen Rundungsdifferenzen in umgerechneten Beträgen abstimmen, Geschäftsstatistik neu berechnen, die Sachkontobuchungen erfassen, den Datenzugriff auf das Konvertierungstool einschränken und Fremdwährungsbeträge für Debitoren- und Kreditorenkonten neu bewertet.

## <a name="setting-up-accounts-for-automatic-transactions"></a>Einrichten von Konten für automatische Buchungen
Während des Währungsumrechnungsprozesses werden Gewinne oder Verluste oder Centdifferenzen auf die Konten gebucht, die auf der Seite **Konten für automatische Buchungen** definiert werden. Hauptkonten müssen den folgenden Buchungstypen zugeordnet werden, bevor der Umrechnungsprozess ausgeführt wird:

-   Konvertierungsgewinn in der Buchhaltungswährung
-   Konvertierungsverlust in der Buchhaltungswährung
-   Centdifferenz in Buchhaltungswährung
-   Centdifferenz in Berichtswährung
-   Jahresendergebnis

## <a name="posting-rounding-differences-and-sum-recalculations"></a>Buchen von Rundungsdifferenzen und Summenneuberechnung
Die folgenden Informationen beschreiben, wo Rundungsdifferenzen auftreten können:

-   Wenn die Preise von Produkten in 0 (Null) umgerechnet worden sind, wird ein Bericht erstellt, der die Produktnummer, den Modultyp, den Preis vor der Umrechnung und die Einheit enthält.
-   Rundungsdifferenzen zwischen Mehrwertsteuer und Hauptbuch werden in der allgemeinen Erfassung gebucht.
-   Beträge von Neubewertungen der Fremdwährung werden neu berechnet, und Beträge von Debitoren- und Kreditorenbuchungen werden neu berechnet.
-   Ausgleichsbuchungen für Debitoren und Kreditoren werden für Rundungsdifferenzen jeder Debitoren- und Kreditorenbuchung erstellt.
-   Rundungsdifferenzen für Debitoren und Kreditoren werden in der allgemeinen Erfassung gebucht.
-   Ausgeglichene Einstandsbeträge und Kostenregulierungsbeträge in den geschlossenen Lagerbuchungen werden neu berechnet.
-   Rundungsdifferenzen in der Bestandsverwaltung werden in der allgemeinen Erfassung gebucht.
-   Der verfügbare Lagerbestand wird neu berechnet.
-   Die Gesamtbeträge in den Sachkontoerfassungen werden neu berechnet.
-   Sachkonto-Abschlussbögen werden neu berechnet.
-   Sachkontosalden werden neu berechnet.
-   Im Sachkonto aufgetretene Rundungsdifferenzen werden in der allgemeinen Erfassung gebucht.
-   Sachkonto-Primobuchungen werden neu berechnet.
-   Der Endbetrag in den Sachkontosalden wird berechnet.

Falls Sie die Umrechnung in eine neue Sachkonto-Buchhaltungswährung durchführen und während der Neuberechnung der Gesamtbeträge oder der Buchung von Rundungsdifferenzen ein Fehler aufgetreten ist, müssen Sie das Formular **Sachkontobuchhaltung - Währungskonvertierung** schließen. Die Gesamtbeträge werden neu berechnet, und die Rundungsdifferenzen werden gebucht.

## <a name="processing-the-currency-conversion"></a>Durchführen der Währungskonvertierung
Wenn Sie die Umrechnung der Währung starten, müssen alle Benutzer vom System abgemeldet sein. Sie müssen die neue Sachkonto- oder die Berichtswährung und die Wechselkurse definieren. Wenn Sie auf **OK** klicken, wird der Prozess ausgeführt und aktualisiert jede Buchung im System. Die Währungsumrechnung ist ein sehr langer Prozess. Wenn es ausgeführt ist, sehen Sie auf der Seite **Sachkonto**, dass die Buchhaltungs- oder Berichtswährung aktualisiert wurde.

## <a name="completing-the-currency-conversion"></a>Abschließen der Währungskonvertierung
Nach der Währungskonvertierung müssen Sie alle neu Abstimmungsberichte neu generierten, um sicherzustellen, dass alle konvertierten Beträge korrekt sind.

-   Wenn die Konvertierung von Hauptbuch-Buchhaltungswährung Rundungsdifferenzen verursacht, werden diese Differenzen nicht unter Verwendung des Belegs gebucht, der Ursache der Rundungsdifferenz ist. Stattdessen werden die Differenzen über den Beleg gebucht, die für die Konvertierungsbuchungen eingegeben wurde. Auf diese Weise werden die Rundungsdifferenzen in allen nach der Konvertierung ausgeführten Berichten ausgegeben, die auf Beleg und Datum prüfen. Dieses Verahlten ist korrekt und kann ignoriert werden.
-   Wird in den Abgleichberichten für Debitoren und Kreditoren ein abweichender Betrag angezeigt und war dies vor der Konvertierung nicht der Fall, muss dieser Differenzbetrag gebucht werden, und zwar auf dem Summenkonto für Debitoren und Kreditoren. Als Gegenkonto wird das Sachkonto für Konvertierungsverlust oder Konvertierungsgewinn verwendet.

Nachdem alle Sachkonto-Buchungserfassungen gelöscht wurden, können Sie die Sachkontobuchungen journalisieren. Klicken Sie auf **Hauptbuch** &gt; **Periodisch** &gt; **Erfassungs** &gt; **Journalisierung**. Sie können Fremdwährungsbeträge nach der Währungsumrechnung neu bewertet wenn die Neubewertung erforderlich ist. Sie bewerten Fremdwährungsbeträge neu, indem Sie **Standard** im Feld **Methode** für die Neubewertung auswählen.

Weitere Informationen finden Sie unter [Journalisieren von gebuchten Journaleinträge](tasks/journalize-posted-journal-entries.md).


