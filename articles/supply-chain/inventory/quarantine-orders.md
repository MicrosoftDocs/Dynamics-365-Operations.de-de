---
title: Quarantäneaufträge
description: In diesem Artikel wird beschrieben, wie Quarantäneaufträge zum Sperren von Beständen verwendet werden.
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocation, InventModelGroup, InventQuarantineOrder, InventQuarantineParmEnd, InventQuarantineParmReportFinished, InventQuarantineParmStartUp, InventTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 30021
ms.assetid: d5047727-653c-49da-b489-6fd3fe50445e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 523e51c705d76b6e8624887292395f8f239bcb65
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "362578"
---
# <a name="quarantine-orders"></a>Quarantäneaufträge

[!include [banner](../includes/banner.md)]

In diesem Artikel wird beschrieben, wie Quarantäneaufträge zum Sperren von Beständen verwendet werden.

Quarantäneaufträge können verwendet werden, um Bestand zu sperren. Beispielsweise empfiehlt es sich, Artikel aus Gründen der Qualitätskontrolle unter Quarantäne zu stellen. Bestand, der unter Quarantäne gestellt wurde, wird an einen Quarantänelagerort übertragen. **Hinweis:** Wenn Sie die erweiterten Lagerortverwaltungsprozesse (in der Lagerortverwaltung) verwenden, wir die Quarantäneauftragsverarbeitung nur für Rückholaufträge verwendet.

## <a name="quarantine-on-hand-inventory-items"></a>Verfügbare Lagerartikel unter Quarantäne stellen
Wenn Sie Artikel unter Quarantäne stellen, können Sie die Quarantäneaufträge entweder manuell erstellen oder das System so einrichten, dass die Quarantäneaufträge automatisch erstellt werden. Um Quarantäneaufträge automatisch zu erstellen, wählen Sie die **Quarantäneverwaltung**-Option auf der **Richtlinien für Lagerbestand**-Registerkarte auf der **Lagersteuerungsgruppen**-Seite aus. Sie müssen außerdem im Feld **Quarantänelagerort** einen standardmäßigen Quarantänelagerort für den empfangenden Lagerort eingeben. Wenn der physisch verfügbare Lagerbestand in eine Bestellung oder einen Produktionsauftrag erfasst wird, werden Quarantäneelemente automatisch an einen Quarantänelagerort in Microsoft Dynamics 365 for Finance and Operations verschoben. Diese Verschiebung tritt auf, da der Status des Quarantäneauftrags in **Gestartet** geändert wird. Wenn Sie Quarantäneaufträge manuell erstellen, ist es nicht nötig anzufordern, dass der Artikel in der Artikelmodellgruppe für die Quarantäneverwaltung zugeordnet wird. Für diesen Vorgang müssen Sie den verfügbaren Lagerbestand, der unter Quarantäne gestellt werden soll, und den Quarantänelagerort angeben, der verwendet werden soll. Sie können den Quarantäneauftragsstatus verwenden, um die Planung des Vorgangs zu unterstützen.

## <a name="quarantine-order-statuses"></a>Status des Quarantäneauftrags
Quarantäneaufträge können folgende Status annehmen:

-   Erstellt
-   Gestartet
-   Fertig gemeldet
-   Abgeschlossen

### <a name="created"></a>Erstellt

Wenn ein Quarantäneauftrag manuell erstellt wird, aber der Artikel noch nicht im Quarantänelagerort ist, erhält der Quarantäneauftrag den Status **Erstellt**. Es werden zwei Lagerbuchungen erstellt. Eine Transaktion ist eine Problemtransaktion, die den Status **In Auftrag**, **Physisch reserviert**, oder **Entnommen** haben kann. Die andere Transaktion ist eine Empfangstransaktion, die am Quarantänelagerort den Status **Bestellt** oder **Erfasst** haben kann. Sie können Bestandsaktualisierungen mit den üblichen Prozessen reservieren, abholen oder erfassen.

### <a name="started"></a>Gestartet

Wenn ein Quarantäneauftrag den Status **Gestartet** aufweist, wird der Bestand vom regulären Lagerort an den Quarantänelagerort übertragen und es werden zwei Bestandtransaktionen erstellt. Eine Transaktion hat den Status **Entnommen** und die andere Transkation hat den Status **Erhalten**. Gleichzeitig werden zwei Lagerbuchungen für die Rückumlagerung erstellt. Diese Buchungen werden nicht mit einem Datum versehen. Eine Transaktion hat den Status **physisch reserviert** und die andere Transkation hat den Status **Bestellt**.

### <a name="reported-as-finished"></a>Fertig gemeldet

Per Klick auf **Als beendet melden** können Sie einen begonnenen Quarantäneauftrag als beendet melden. Der Artikel wird aus der Quarantäne entlassen, jedoch noch nicht an den normalen Lagerort umgelagert. Die Rückverschiebung zum normalen Lagerort kann mithilfe einer Wareneingangserfassung erfolgen, die während der Prozesses "Als beendet melden" ausgelöst werden kann.

### <a name="ended"></a>Abgeschlossen

Wenn ein Quarantäneauftrag beendet wird, wird der Artikel vom Quarantänelagerort zurück an den normalen Lagerort umgelagert. Der Status der Artikelbuchung wird am Quarantänelagerort auf **Verkauft** und am normalen Lagerort auf **Gekauft** festgelegt.

## <a name="quarantine-order-scrap"></a>Quarantäneauftrags-Ausschuss
Als Teil des Quarantäneauftragsprozesses ist es möglich, Bestand als Ausschuss kennzeichnen. Wenn Ausschuss verarbeitet wird, wird der Bestand durch eine Problemtransaktion vom Quarantänelagerort auf **Verkauft** gesetzt.

<a name="additional-resources"></a>Zusätzliche Ressourcen
--------

[Sperrung von Lagerbestand](inventory-blocking.md)
