---
title: Visuelle und kollaborative Ausführung
description: Dieser Artikel beschreibt, wie Sie Ihre bedarfsgesteuerte Materialbedarfsplanung (DDMRP) mit Entkopplungspunkten, Pufferzonen, geplanten Aufträgen und Historie überwachen können.
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: EcoResProductDetailsExtended, ReqDDMRPWorkspace, ReqDecouplingPointsStatusByNetFlow, ReqDecouplingPointStatusByOnHand, ReqPlannedOrderForm, ReqItemDecoupledLeadTime
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 92e38c6ea19b60ae0a61e55f240ff52698e06933
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689775"
---
# <a name="visual-and-collaborative-execution"></a>Visuelle und kollaborative Ausführung

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Dieser Artikel beschreibt, wie Sie Ihre bedarfsgesteuerte Materialbedarfsplanung (DDMRP) mit Entkopplungspunkten, Pufferzonen, geplanten Aufträgen und Historie überwachen können.

## <a name="visually-track-buffers-and-quantities-for-a-selected-item"></a>Verfolgen Sie visuell Puffer und Mengen für einen ausgewählten Artikel

In Microsoft Dynamics 365 Supply Chain Management können Sie visuell verfolgen, wie sich Puffer, Lagerbestände und Netto-Flows im Laufe der Zeit für jedes ausgewählte freigegebene Produkt verändern. Führen Sie diese Schritte aus, um die Diagramme zu öffnen und zu überprüfen.

1. Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**.
1. Wählen Sie einen zugelassenen Artikel, der als Entkopplungspunkt festgelegt ist. (Weitere Informationen finden Sie unter [Positionierung von Beständen](ddmrp-inventory-positioning.md)).
1. Wählen Sie im Aktionsbereich auf der Registerkarte **Plan** die Option **Artikelabdeckung**.
1. Wählen Sie auf der Seite **Artikelabdeckung** einen Datensatz zur Artikelabdeckung aus, der einen Entkopplungspunkt erstellt. (In diesem Datensatz wird der Name einer Abdeckungsgruppe angezeigt, die zum Erstellen von Entkopplungspunkten festgelegt ist.)
1. Wählen Sie die Registerkarte **Lagerbestand**. Diese Registerkarte enthält ein Diagramm, das zeigt, wie sich die Lagerbestände im Laufe der Zeit verändert haben, zusammen mit dem Wert des Lagerbestands, der für einen bestimmten Zeitraum jedes Mal, wenn die Planungsoptimierung ausgeführt wird, aufgezeichnet wurde. Die Registerkarte enthält auch eine Tabelle, die zeigt, in welche der folgenden Kategorien jeder erfasste Lagerbestand fällt:

    - **Kritisch niedrig** – Weniger als die Hälfte des Minimums für den Zeitraum.
    - **Niedrig** – Zwischen der Hälfte des Minimums und dem Minimum.
    - **Durchschnittlicher Lagerbestand** – Zwischen dem Minimum und dem Minimum plus der grünen Zone.
    - **Höher als der Durchschnitt** – Höher als der Durchschnitt.

    ![Historische Lagerbestände auf der Registerkarte Lagerbestand.](media/ddmrp-on-hand-graph.png "Historische Lagerbestände auf der Registerkarte Lagerbestand")

    > [!NOTE]
    > Die Farben, die auf der Registerkarte **Lagerbestand** verwendet werden, stellen andere Bereiche dar als die ähnlichen Farben, die auf der Registerkarte **Pufferwerte** verwendet werden.

1. Um zu sehen, wie sich Ihre Pufferwerte im Laufe der Zeit verändert haben und wie sie im Vergleich zum Lagerbestand und zum Netto Flow stehen, wählen Sie die Registerkarte **Pufferwerte**.

    ![Historischer Lagerbestand und Netto-Flows auf der Registerkarte Pufferwerte:](media/ddmrp-buffer-values-graph.png "Historische Lagerbestände und Net-Flows auf der Registerkarte Pufferwerte")

## <a name="track-the-status-and-planned-orders-for-all-decoupling-points"></a>Verfolgen Sie den Status und die geplanten Aufträge für alle Entkopplungspunkte

Der **Bedarfsgesteuerte Materialbedarfsplanung** Arbeitsbereich bietet verschiedene Tools, zusammen mit Key Performance Indicators (KPIs) und Übersichten über den Status Ihrer Entkopplungspunktartikel und der dazugehörigen geplanten Aufträge. Um sie zu öffnen, gehen Sie zu **Masterprogrammplanung \> Arbeitsbereiche \> Bedarfsgesteuerte Materialbedarfsplanung**.

![Bedarfsgesteuerte Materialbedarfsplanung Arbeitsbereich.](media/ddmrp-workspace.png "Bedarfsgesteuerte Materialbedarfsplanung im Arbeitsbereich")

## <a name="get-overviews-of-decoupling-points-and-planned-orders"></a>Erhalten Sie Übersichten über Entkopplungspunkte und geplante Aufträge

Zusätzlich zum **Bedarfsgesteuerten Materialbedarfsplanung** Arbeitsbereich bietet Supply Chain Management mehrere Seiten, auf denen Sie Informationen über Ihre DDMRP-Einrichtung, Entkopplungspunkte und geplanter Aufträge einsehen können. Einige dieser Seiten bieten auch praktische Schaltflächen im Aktionsbereich, mit denen Sie Puffer verwalten, die Produktprogrammplanung ausführen und andere zugehörige Ansichten öffnen können.

- Um den Status der Entkopplungspunkte nach Netto-Flows anzuzeigen, gehen Sie zu **Masterplanung \> Masterplanung \> DDMRP \> Status der Entkopplungspunkte nach Netto Flows**.
- Um den Status der Entkopplungspunkte nach Lagerbestand anzuzeigen, gehen Sie zu **Masterplanung \> Masterplanung \> DDMRP \> Status der Entkopplungspunkte nach Lagerbestand**.
- Um die geplanter Aufträge für Entkopplungspunkte anzuzeigen, gehen Sie auf **Masterplanung \> Produktprogrammplanung \> DDMRP \> Geplante Aufträge für Entkopplungspunkte**.
- Um entkoppelte Vorlaufzeiten anzuzeigen, gehen Sie zu **Masterplan \> Produktprogrammplanung \> DDMRP \> Entkoppelte Vorlaufzeit**.

## <a name="clean-up-decoupling-point-buffer-values"></a>Bereinigen Sie die Pufferwerte der Entkopplungspunkte

Im Laufe der Zeit wird Ihr System eine große Menge an historischen Daten aufbauen, die mit den laufenden Pufferberechnungen zusammenhängen. Diese historischen Daten führen zu einem Anstieg Ihres Datenvolumens und können schließlich die Leistung Ihres Systems beeinträchtigen. Daher empfehlen wir Ihnen, die alten Pufferwerte der Entkopplungspunkte gelegentlich zu bereinigen.

> [!WARNING]
> Der Bereinigungsauftrag entfernt historische Pufferwerteinstellungen und historische Informationen zum Lagerbestand/Netto-Flow. Es ist nicht umkehrbar.

Führen Sie diese Schritte aus, um Ihre Entkopplungspunkt-Pufferwerte zu bereinigen.

1. Gehen Sie zu **Masterplanung \> Masterplanung \> DDMRP \> Pufferwerte für Entkopplungspunkte bereinigen**.
1. Legen Sie in der Dialogbox **Pufferwerte für Entkopplungspunkte bereinigen** die folgenden Felder fest:

    - **Löschen von Datensätzen, die älter sind als (Tage)** – Geben Sie das Alter der jüngsten zu behaltenden Datensätze in Tagen an. Alle Datensätze mit Entkopplungspunkt-Pufferwerten, die älter als dieser Wert sind, werden gelöscht.
    - **Masterplan** – Wählen Sie einen Masterplan, der Artikel enthält, die von dieser Bereinigung betroffen sein sollen. Die Bereinigung wird auf alle Artikel im Plan angewendet, nachdem die **Filter**-Einstellungen, die Sie in diesem Dialogfeld festgelegt haben, angewendet wurden.

1. Um die Datensätze einzuschränken, die der Batch-Auftrag ausführen soll, wählen Sie auf dem Inforegister **Einzuschließende Datensätze** die Option **Filter**, um das Dialogfeld **Abfrage** zu öffnen. Dieses Dialogfeld funktioniert genauso wie bei anderen Arten von [Hintergrundaufträgen](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) im Supply Chain Management.
1. Geben Sie auf der Registerkarte **Im Hintergrund ausführen** Inforegister an, wie, wann und wie oft die Bereinigung durchgeführt werden soll. Die Felder funktionieren genauso wie bei anderen Arten von [Hintergrund-Jobs](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) im Supply Chain Management.
1. Wählen Sie **OK**, um den neuen Auftrag zur Ausführung in eine Batch-Warteschlange aufzunehmen.
