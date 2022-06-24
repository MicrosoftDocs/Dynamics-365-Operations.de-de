---
title: Quarantäneaufträge
description: Dieser Artikel beschreibt, wie Sie Quarantäneaufträge verwenden, um Bestände zu sperren.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventLocation, InventModelGroup, InventQuarantineOrder, InventQuarantineParmEnd, InventQuarantineParmReportFinished, InventQuarantineParmStartUp, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30021
ms.assetid: d5047727-653c-49da-b489-6fd3fe50445e
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3ee1ba338d90c6ee9cdc37948061f518040ae1a1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869661"
---
# <a name="quarantine-orders"></a>Quarantäneaufträge

[!include [banner](../includes/banner.md)]

Dieser Artikel beschreibt, wie Sie Quarantäneaufträge verwenden, um Bestände zu sperren.

Mit Quarantäneaufträgen können Sie Bestände sperren. Beispielsweise empfiehlt es sich, Artikel aus Gründen der Qualitätskontrolle unter Quarantäne zu stellen. Bestand, der unter Quarantäne gestellt wurde, wird an einen Quarantänelagerort übertragen.

> [!NOTE]
> Wenn Sie erweiterte Lagerortverwaltungsprozesse (in der Lagerortverwaltung) verwenden, wird die Quarantäneauftragsverarbeitung nur für Rücklieferungen von Verkaufsaufträgen verwendet.

## <a name="quarantine-on-hand-inventory-items"></a>Verfügbare Lagerartikel unter Quarantäne stellen

Wenn Sie Artikel unter Quarantäne stellen, können Sie die Quarantäneaufträge entweder manuell erstellen oder das System so einrichten, dass sie bei der eingehenden Verarbeitung automatisch erstellt werden.

Um das System so festzulegen, dass es automatisch Quarantäneaufträge erzeugt, folgen Sie diesen Schritten.

1. Gehen Sie zu **Inventarverwaltung \> Einrichten \> Bestand \> Element-Modellgruppen**.
1. Wählen Sie eine relevante Modellgruppe im Listenbereich aus oder erstellen Sie eine neue Modellgruppe.
1. Aktivieren Sie auf der Registerkarte **Inventarrichtlinien** das Kontrollkästchen **Quarantäneverwaltung**.
1. Schließen Sie die Seite.
1. Geben Sie im Feld **Quarantänelager** für die empfangenden Lagerorte ein Standard-Quarantänelager an.

Wenn ein Element, das als im Lagerort eingegangen registriert ist, zu einer Modellgruppe gehört, in der das Kontrollkästchen **Quarantäneverwaltung** aktiviert ist, erzeugt das System einen Quarantäneauftrag für dieses Element. Der Quarantäneauftrag weist die Arbeitskräfte an, das Element in das Quarantäne-Lagerort zu bringen.

Wenn Sie Quarantäne-Aufträge manuell auf der Seite **Quarantäne-Aufträge** erstellen, muss das Element nicht in der zugehörigen Artikelmodellgruppe für die Quarantäne-Verwaltung festgelegt werden. Für diesen Vorgang müssen Sie den verfügbaren Lagerbestand, der unter Quarantäne gestellt werden soll, und den Quarantänelagerort angeben, der verwendet werden soll. Sie können den Quarantäneauftragsstatus verwenden, um die Planung des Vorgangs zu unterstützen.

## <a name="quarantine-order-statuses"></a>Status des Quarantäneauftrags

Quarantäneaufträge können folgende Status annehmen:

- Erstellt
- Gestartet
- Fertig gemeldet
- Abgeschlossen

### <a name="created"></a>Erstellt

Wenn ein Quarantäneauftrag manuell erstellt wird, aber der Artikel noch nicht im Quarantänelagerort ist, erhält der Quarantäneauftrag den Status **Erstellt**. Es werden zwei Lagerbuchungen erstellt. Eine Transaktion ist eine Problemtransaktion, die den Status **In Auftrag**, **Physisch reserviert**, oder **Entnommen** haben kann. Die andere Transaktion ist eine Empfangstransaktion, die am Quarantänelagerort den Status **Bestellt** oder **Erfasst** haben kann. Sie können Bestandsaktualisierungen mit den üblichen Prozessen reservieren, abholen oder erfassen.

### <a name="started"></a>Gestartet

Wenn ein Quarantäneauftrag den Status **Gestartet** aufweist, wird der Bestand vom regulären Lagerort an den Quarantänelagerort übertragen und es werden zwei Bestandtransaktionen erstellt. Eine Transaktion hat den Status **Entnommen** und die andere Transkation hat den Status **Erhalten**. Gleichzeitig werden zwei Lagerbuchungen für die Rückumlagerung erstellt. Diese Buchungen werden nicht mit einem Datum versehen. Eine Transaktion hat den Status **physisch reserviert** und die andere Transkation hat den Status **Bestellt**.

### <a name="reported-as-finished"></a>Als fertig gemeldet

Um einen gestarteten Quarantäneauftrag als beendet zu melden, öffnen Sie den Auftrag und wählen Sie **Als beendet melden** im Aktivitätsbereich. Das Element wird aus der Quarantäne freigegeben, aber noch nicht zurück in den regulären Lagerort verschoben. Die Bewegung zurück zum regulären Lagerort kann über eine Wareneingangserfassung verarbeitet werden, die während des Berichts als abgeschlossener Prozess initialisiert werden kann.

### <a name="ended"></a>Beendet

Wenn ein Quarantäneauftrag beendet wird, wird der Artikel vom Quarantänelagerort zurück an den normalen Lagerort umgelagert. Der Status der Artikelbuchung wird am Quarantänelagerort auf *Verkauft* und am normalen Lagerort auf *Gekauft* festgelegt.

## <a name="quarantine-order-scrap"></a>Quarantäneauftrags-Ausschuss

Als Teil des Quarantäneauftragsprozesses ist es möglich, Bestand als Ausschuss kennzeichnen. Wenn Sie Ausschuss verarbeiten, wird der Status des Bestandes durch eine Ausgabe-Transaktion aus dem Quarantäne-Lagerort auf *Verkauft* festgelegt.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Sperrung von Lagerbestand](inventory-blocking.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
