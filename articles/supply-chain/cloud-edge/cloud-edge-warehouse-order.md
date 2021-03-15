---
title: Lagerortaufträge für Cloud- und Edge-Skalierungseinheiten
description: Dieses Thema enthält Informationen zur Lagerortauftragsfunktion, die als Teil der Arbeitsauslastung der Lagerort-Skalierungseinheit verwendet wird.
author: perlynne
manager: tfeyr
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWarehouseOrderLine, WHSWarehouseReceiptEntry, PurchTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: c04127b9fe621d962be2d7fe06358b3bd1b78916
ms.sourcegitcommit: 289e9183d908825f4c8dcf85d9affd4119238d0c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/02/2021
ms.locfileid: "5105708"
---
# <a name="warehouse-orders-for-cloud-and-edge-scale-units"></a>Lagerortaufträge für Cloud- und Edge-Skalierungseinheiten

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> In der öffentlichen Vorschau werden nicht alle Geschäftsfunktionen vollständig unterstützt, wenn Arbeitsauslastungen von Skalierungseinheiten verwendet werden. Wenn Sie Skalierungseinheiten verwenden, achten Sie darauf, nur die Prozesse zu verwenden, die in diesem Thema ausdrücklich als unterstützt beschrieben werden.

## <a name="what-are-warehouse-orders"></a>Was sind Lagerortaufträge?

*Lagerortaufträge* sind ein Auftragstyp, der erstellt wurde, um Lagerortbereitstellungen von Hubs und Skalierungseinheiten zu unterstützen. Mit ihnen können Sie Bestand erhalten, wenn Sie eine Arbeitsauslastung des Lagerorts auf einer Skalierungseinheit ausführen. Sie werden derzeit nur bei Bestellungen verwendet.

Lagerortaufträge werden im Rahmen der Lagerverwaltungsverarbeitung verwendet, z. B. wenn die Lagerort-App zum Registrieren des physischen Lagerbestands während der Verarbeitung einer eingehenden Bestellung verwendet wird. Lagerortaufträge werden im Rahmen des Prozesses *Freigabe an Lager* erstellt, der für Bestellungen verfügbar ist, die einen Lagerort mit Skalierungseinheit angeben, und Artikel, die für die Verwendung von Lagerverwaltungsprozessen aktiviert sind.

> [!IMPORTANT]
> Lagerortaufträge sind nur in Bereitstellungen verfügbar, die [Arbeitsauslastungen in der Lagerortverwaltung für Cloud- und Edge-Skalierungseinheiten](cloud-edge-workload-warehousing.md).

## <a name="create-a-warehouse-order"></a>Einen Lagerortauftrag erstellen

Gehen Sie folgendermaßen vor, um einen Lagerortauftrag zu erstellen.

1. Melden Sie sich auf der Instanz von Microsoft Dynamics 365 Supply Chain Management an, die auf dem Hub ausgeführt wird. (Sie müssen den Prozess *Freigabe an Lager* initiieren, während Sie am Hub angemeldet sind.)
1. Wechseln Sie zu **Beschaffung \> Bestellungen \> Alle Bestellungen**.
1. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Lagerort**, in der Gruppe **Aktivitäten**, **Für Lagerort freigeben** aus.
1. Um die zugehörigen Lagerortauftragspositionen anzuzeigen, öffnen Sie die entsprechende Bestellung und wählen eine Position im Abschnitt **Bestellpositionen** und dann in der Symbolleiste die Option **Lagerort \> Lagerortauftragspositionen** aus. Um alle Positionen anzuzeigen, gehen Sie zu **Lagerortverwaltung \> Abfragen und Berichte \> Lagerauftragspositionen**.

## <a name="cancel-a-warehouse-order"></a>Stornieren eines Lagerortauftrags

Im Rahmen des Prozesses *Freigabe an Lager* werden Bestandsvorgänge für Bestellungen mit Lageraufträgen verknüpft und für die Aktualisierung durch den Hub gesperrt. Wenn Sie versehentlich in das Lager freigegeben wurden oder wenn Sie einen anderen Grund haben, die Erstellung von Lagerortauftragspositionen rückgängig zu machen, können Sie die Stornierung von Lagerortauftragspositionen anfordern.

Gehen Sie folgendermaßen vor, um Lagerortauftragspositionen zu stornieren.

1. Melden Sie sich bei der Instanz von Supply Chain Management an, die auf dem Hub ausgeführt wird.
1. Gehen Sie zu **Lagerortverwaltung \> Abfragen und Berichte \> Lagerauftragspositionen**.
1. Wählen Sie die zutreffende Position aus.
1. Wählen Sie im Aktionsbereich die Option **Lagerortauftragspositionen stornieren** aus.

> [!NOTE]
> Die Anforderung zum Stornieren von Positionen wird für alle Positionen abgelehnt, deren Stornierung bereits aussteht oder die aktiv in einem Lagerort verarbeitet werden, in dem die Arbeitslastung auf einer Skalierungseinheit ausgeführt wird.

## <a name="monitor-a-warehouse-order"></a>Überwachen eines Lagerortauftrags

In der Ansicht **Lagerortauftragspositionen** können Sie den Fortschritt des eingehenden Empfangs überwachen, indem Sie die Werte in der Spalte **Noch zu empfangende Menge** prüfen. Führen Sie einen dieser Schritte aus, um Details anzuzeigen, die sich auf Arbeiten beziehen, die mit der Lagerort-App ausgeführt werden.

- Gehen Sie zu **Lagerortverwaltung \> Abfragen und Berichte \> Lagerortauftragspositionen**, und verwenden Sie den Filter, um die gesuchten Positionen zu finden.
- Wechseln Sie zu **Beschaffung \> Bestellungen \> Alle Bestellungen**, und öffnen Sie die relevante Bestellung. In dem Abschnitt **Bestellpositionen** wählen Sie eine oder mehrere Zeilen aus, und wählen Sie dann in der Symbolleiste **Lagerort \> Lagerort-Empfangseinträge**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]