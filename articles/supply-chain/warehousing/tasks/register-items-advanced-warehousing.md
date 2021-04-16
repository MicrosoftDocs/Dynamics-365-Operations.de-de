---
title: Artikel für einen für die erweiterte Lagerhaltung aktivierten Artikel mithilfe einer Wareneingangserfassung registrieren
description: Dieses Thema stellt ein Szenario vor, wie Artikel mithilfe der Wareneingangserfassung erfasst werden, wenn Sie die erweiterte Lagerortverwaltung verwenden.
author: ShylaThompson
ms.date: 03/24/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WMSJournalTable, WMSJournalCreate, WHSLicensePlate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c58aa1cec6c0bfe33fa1ef90267dcd8ac1218157
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830833"
---
# <a name="register-items-for-an-advanced-warehousing-enabled-item-using-an-item-arrival-journal"></a>Artikel für einen für die erweiterte Lagerhaltung aktivierten Artikel mithilfe einer Wareneingangserfassung registrieren

[!include [banner](../../includes/banner.md)]

Dieses Thema stellt ein Szenario vor, wie Artikel mithilfe der Wareneingangserfassung erfasst werden, wenn Sie die erweiterte Lagerortverwaltung verwenden. Dies wird in der Regel von einem Sachbearbeiter für Zugänge ausgeführt.

## <a name="enable-sample-data"></a>Beispieldaten aktivieren

Um dieses Szenario mit den in diesem Thema angegebenen Beispieldatensätzen und -werten zu bearbeiten, müssen Sie ein System verwenden, auf dem die Standarddemodaten installiert sind, und Sie müssen die juristische Person *USMF* auswählen, bevor Sie beginnen.

Sie können dieses Szenario stattdessen durcharbeiten, indem Sie Werte aus Ihren eigenen Daten nutzen, sofern die folgenden Daten verfügbar sind:

- Sie müssen eine bestätigte Bestellung mit einer offenen Bestellposition haben.
- Der Artikel für die Position muss gelagert sein. Es dürfen keine Produktvarianten verwendet werden und es dürfen keine Rückverfolgungsangaben vorhanden sein.
- Der Artikel muss einer Lagerdimensionsgruppe zugeordnet werden, die für den Lagerortverwaltungsprozess aktiviert ist.
- Der Lagerort, der verwendet wird, muss für Lagerortverwaltungsprozesse aktiviert sein und der Lagerplatz, der für den Eingang verwendet wird, muss über Ladungsträger gesteuert werden.

## <a name="create-an-item-arrival-journal-header-that-uses-warehouse-management"></a>Erstellen Sie eine Wareneingangserfassungs-Kopfzeile, die die Lagerortverwaltung verwendet

Das folgende Szenario zeigt, wie Sie eine Wareneingangserfassungs-Kopfzeile erstellen, die die Lagerortverwaltung verwendet:

1. Stellen Sie sicher, dass Ihr System eine bestätigte Bestellung enthält, die die im vorherigen Abschnitt beschriebenen Anforderungen erfüllt. In diesem Szenario wird eine Bestellung für das Unternehmen *USMF* verwendet, Kreditorenkonto *1001*, Lagerort *51*, mit einer Bestellposition für *10 PL* (10 Paletten) der Artikelnummer *M9200*.
1. Notieren Sie sich die Bestellnummer, die Sie benutzen werden.
1. Wechseln Sie zu **Bestandsverwaltung \> Erfassunseinträge \> Wareneingang \> Wareneingang**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Das Dialogfeld **Lagerortverwaltungserfassung erstellen** öffnet sich. Wählen Sie im Feld **Name** eine Erfassung aus.
    - Wenn Sie die *USMF*-Demodaten verwenden, wählen Sie *WHS* aus.
    - Wenn Sie Ihre eigenen Daten verwenden, muss die von Ihnen ausgewählte Erfassung bei **Entnahmeort prüfen** auf *Nein* und bei **Quarantäneverwaltung** auf *Nein* gestellt sein.
1. Setzten Sie **Referenz** auf *Bestellung*.
1. Setzen Sie **Kontonummer** auf *1001*.
1. Setzen Sie **Nummer** auf die Nummer der Bestellung, die Sie für diese Übung ausgewählt haben.

    ![Wareneingangserfassung](../media/item-arrival-journal-header.png "Wareneingangserfassung")

1. Wählen Sie **OK**, um die Erfassungkopfzeile zu erstellen.
1. Im Abschnitt **Erfassungspositionen** wählen Sie **Position hinzufügen** aus und geben Sie folgende Daten ein:
    - **Artikelnummer** – *M9200*. **Standort**, **Lagerort** und **Menge** werden basierend auf den Bestandstransaktionsdaten für die 10 Paletten (1.000 Stück) festgelegt.
    - **Standort** – Stellen Sie *001* ein. Dieser spezielle Standort verfolgt Ladungsträger nicht nach.

    ![Wareneingangserfassungsposition](../media/item-arrival-journal-line.png "Wareneingangserfassungsposition")

    > [!NOTE]
    > Das Feld **Datum** bestimmt das Datum, an dem die verfügbare Menge dieses Artikels im Bestand erfasst wird.  
    >
    > Die **Loskennung** wird vom System ausgefüllt, wenn sie über die bereitgestellten Informationen eindeutig identifiziert werden kann. Andernfalls müssen Sie sie manuell eingeben. Dies ist ein Pflichtfeld, das diese Erfassung mit einer bestimmten Quelldokumentposition verknüpft.  

1. Wählen Sie im Aktivitätsbereich **Überprüfen** aus. Dies überprüft, ob die Erfassung für die Buchung bereit ist. Wenn die Prüfung fehlschlägt, müssen Sie die Fehler korrigieren, bevor Sie die Erfassung buchen können.  
1. Das Dialogfeld **Erfassung überprüfen** öffnet sich. Wählen Sie **OK**.
1. Überprüfen Sie die Meldungsleiste. Es sollte eine Meldung geben, die darauf hinweist, dass der Vorgang abgeschlossen wurde.  
1. Wählen Sie im Aktivitätsbereich **Buchen** aus.
1. Das Dialogfeld **Erfassung buchen** öffnet sich. Wählen Sie **OK**.
1. Überprüfen Sie die Meldungsleiste. Es sollte eine Meldung geben, die darauf hinweist, dass der Vorgang abgeschlossen wurde.
1. Wählen Sie im Aktivitätsbereich **Funktionen > Produktzugang**, um die Bestellposition zu aktualisieren und einen Produktzugang zu buchen.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
