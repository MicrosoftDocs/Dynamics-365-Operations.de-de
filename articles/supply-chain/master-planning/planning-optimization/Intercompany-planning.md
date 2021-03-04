---
title: Intercompany-Planung
description: Dieses Thema beschreibt die Intercompany-Planung und erklärt, wie Sie die Intercompany-Planung mit der Planungsoptimierung in Microsoft Dynamics 365 Supply Chain Management konfigurieren.
author: ChristianRytt
manager: tfehr
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 25c80ce27498131c6eb92174ab14a592bfa9915a
ms.sourcegitcommit: fe21a3a98dcf6fe4eb9351941493f2c0443d8696
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/04/2020
ms.locfileid: "4672186"
---
# <a name="intercompany-planning"></a>Intercompany-Planung

[!include [banner](../../includes/banner.md)]

Für einige Organisationen hängen logistische Operationen von anderen juristischen Entitäten (Firmen) in der Organisation ab. Diese Vorgänge werden über Intercompany-Verkäufe und -Einkäufe abgewickelt, da jede juristische Entität einen eigenen Kontenplan hat.

Dieses Thema beschreibt die Intercompany-Planung und erklärt, wie Sie die Intercompany-Planung mit der Planungsoptimierung in Microsoft Dynamics 365 Supply Chain Management konfigurieren.

In diesem Thema werden die folgenden wichtigen Intercompany-Begriffe verwendet:

- **Aufwärts** - Eine relative Referenz in einer Firma oder Lieferkette. Er zeigt die Bewegung in Richtung des Rohstofflieferanten an.
- **Abwärts** - Ein relativer Verweis in einer Firma oder Lieferkette. Er zeigt die Bewegung in Richtung des Kunden an.
- **Geplanter Intercompany-Bedarf** - Geplanter Bedarf für ein Produkt in einem Unternehmen, basierend auf dem geplanten Bedarf für das Produkt von einem nachgelagerten Unternehmen.

In der Produktprogrammplanung kann ein Plan in einem Unternehmen einen geplanten Intercompany-Bedarf enthalten, der sich auf geplante Aufträge aus einem Plan in einem anderen Unternehmen bezieht. Diese Funktionalität ist nützlich, da sie einen vollständigen Überblick über die geplanten Aufträge in allen Unternehmen bietet. Sie stellt auch sicher, dass alle erforderlichen geplanten Lieferaufträge erstellt werden, ohne dass jedoch Planaufträge für den Intercompany-Bedarf umgewandelt werden müssen.

Wenn Sie die Produktprogrammplanung von einem Masterplan aus durchführen, der geplanten nachgelagerten Bedarf enthält, werden geplante Einkaufsbestellungen von den entsprechenden Intercompany-Lieferanten als Bedarf in den Plan aufgenommen.

## <a name="required-setup"></a>Erforderliches Einrichten

Um die Intercompany-Planung zu verwenden, müssen Sie Ihr System wie folgt vorbereiten:

1. Die relevanten Produkte müssen in allen relevanten Firmen freigegeben sein. Weitere Informationen finden Sie unter [Konfigurieren und verwenden Sie Intercompany-Handel in Dynamics 365 Supply Chain Management ](https://docs.microsoft.com/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) auf Microsoft Learn.
1. Der nachgelagerte Bedarf muss durch Einkäufe bei einem Lieferanten gedeckt werden, der eine Intercompany-Beziehung zum vorgelagerten Unternehmen und entsprechende Standard-Bestandsdimensionen (Standort und Lagerort) beim Kunden hat. Weitere Informationen finden Sie unter [Konfigurieren und verwenden Sie Intercompany-Handel in Dynamics 365 Supply Chain Management ](https://docs.microsoft.com/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) auf Microsoft Learn.
1. Der Masterplan im vorgelagerten Unternehmen muss den geplanten nachgelagerten Bedarf enthalten, und das entsprechende Unternehmen und der Masterplan müssen in den nachgelagerten Plänen angegeben sein.

## <a name="include-planned-downstream-demand"></a>Geplanten Downstream-Bedarf einschließen

Gehen Sie wie folgt vor, um Ihren Masterplan so zu konfigurieren, dass er den geplanten nachgelagerten Bedarf enthält.

1. Wechseln Sie zu **Produktprogrammplanung \> Einrichtung \> Pläne \> Produktprogrammpläne**.
1. Wählen oder erstellen Sie einen Masterplan.
1. Legen Sie auf dem Inforegister **Intercompany-Planung** die folgenden Felder fest:

    - **Geplanten nachgelagerten Bedarf einbeziehen** - Legen Sie diese Option auf *Ja* fest, um die Intercompany-Planung für den Masterplan zu aktivieren.
    - **Nachgelagerte Pläne** - Wenn Sie die Option **Geplanten nachgelagerten Bedarf einbeziehen** auf *Ja* festlegen, verwenden Sie die Symbolleiste und das Raster, um die gewünschten Produktprogrammplanungen von anderen Unternehmen hinzuzufügen.

## <a name="peg-across-companies-by-using-multilevel-pegging"></a>Firmenübergreifende Bedarfsverursacher mit Hilfe des mehrstufigen Bedarfsverursachers

Bei mehrstufigen Bedarfsverursachern können Sie den Bedarfsverursacher firmenübergreifend anzeigen, um die ursprüngliche Bedarfsquelle zu sehen, die durch ein Angebot abgedeckt wird.

Führen Sie die folgenden Schritte aus, um Informationen zum mehrstufigen Bedarfsverursacher anzuzeigen.

1. Gehen Sie zu **Produktprogrammplanung \> Gesamtplanung \> Geplante Aufträge**.
1. Wählen oder öffnen Sie einen Planauftrag.
1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Ansicht** in der Gruppe **Bedarf** die Option **Mehrstufiger Bedarfsverursacher**.

### <a name="intercompany-example-that-involves-two-companies"></a>Intercompany-Beispiel, an dem zwei Firmen beteiligt sind

In diesem Beispiel wird in der Firma USMF ein geplanter Fertigungsauftrag erstellt, um einen Auftrag in der Firma DEMF zu decken. In USMF ist der direkte Bedarf ein geplanter Intercompany-Bedarf. Um diesen Bedarf in USMF erscheinen zu lassen, wird die Produktprogrammplanung zuerst in DEMF und dann in USMF ausgeführt.

Die folgende Abbildung zeigt, wie dieses Beispiel auf der Seite **Multilevel Bedarfsverursacher** für den geplanten Produktionsauftrag erscheinen könnte.

![Intercompany-Beispiel, an dem zwei Firmen beteiligt sind](media/IntercompanyPlanning1.png)

### <a name="intercompany-example-that-involves-three-companies"></a>Intercompany-Beispiel, an dem drei Firmen beteiligt sind

Für dieses Beispiel wird eine geplante Einkaufsbestellung in der USMF-Firma erstellt, um einen Auftrag in der FRRT-Firma zu decken. In den Firmen DEMF und USMF ist der direkte Bedarf ein geplanter Intercompany-Bedarf. Um diesen Bedarf in USMF erscheinen zu lassen, wird die Produktprogrammplanung zuerst in FRRT, dann in DEMF und schließlich in USMF ausgeführt.

Die folgende Abbildung zeigt, wie dieses Beispiel auf der Seite **Multilevel Bedarfsverursacher** für den geplanten Produktionsauftrag erscheinen könnte.

![Intercompany-Beispiel, an dem drei Firmen beteiligt sind](media/IntercompanyPlanning2.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]