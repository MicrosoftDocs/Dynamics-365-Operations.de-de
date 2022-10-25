---
title: Überblick über die bedarfsgesteuerte Disposition (DDMRP)
description: Dieser Artikel informiert Sie über die bedarfsgesteuerte Materialbedarfsplanung (DDMRP), eine Planungsmethode, die auf der Entkopplung von Vorrat und Bedarf basiert.
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 31b45fdb92cf8a590ff77104f0c8015fb4d329d5
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689487"
---
# <a name="demand-driven-material-requirements-planning-ddmrp-overview"></a>Überblick über die bedarfsgesteuerte Disposition (DDMRP)

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Seit Jahren verwenden Unternehmen die Materialbedarfsplanung (MRP) als ein System zur Berechnung der Materialien und Komponenten, die zur Herstellung eines Produkts benötigt werden. Allerdings haben sich die Vorräte inzwischen verändert. Teile haben längere Vorlaufzeiten, weil sie zunehmend aus Übersee bezogen werden. Viele Unternehmen haben daher von Fehl- oder Überbeständen berichtet, weil sie nicht wissen, wie viel Bestand sie vorrätig halten sollen. Es gibt auch mehr Marktschwankungen (manchmal ungenaue Planungen), und die Debitor verlangen Produkte mit kurzer Vorlaufzeit. Daher gibt es überall auf der Welt Engpässe in der Vorratskette. Darüber hinaus geben MRP Tools den Planern oft Tausende von Aktionen vor. Daher ist es schwer zu wissen, worauf man sich konzentrieren soll. Häufig besteht die Lösung für viele dieser Probleme darin, zur bedarfsgesteuerten Materialbedarfsplanung (DDMRP) zu wechseln.

DDMRP ist eine Planungsmethodik, die auf der Entkopplung von Vorrat und Bedarf beruht. Diese Entkopplung wird durch das Festlegen von Entkopplungspunktartikeln erreicht. Für diese Artikel werden Puffer verwaltet, um sicherzustellen, dass die richtige Menge an Lagerbestand vorhanden ist. Die Entkopplung von Vorrat und Bedarf trägt dazu bei, den „Bullwhip-Effekt“ zu verhindern, da die Variabilität nicht durch die Kette weitergegeben wird. (Der *Bullwhip-Effekt* bezieht sich darauf, wie kleine Nachfrageschwankungen auf der Ebene des Einzelhandels zu immer größeren Nachfrageschwankungen auf der Ebene des Großhandels, der Vertriebsunternehmen, der Hersteller und der Rohstofflieferanten führen können.) Jeder Puffer soll die durchschnittliche Nutzung eines Teils abdecken und kann auch angepasst werden, um Bedarfsspitzen abzudecken.

DDMRP hat sich als wertvolle Planungsmethode für variable Umgebungen erwiesen, in denen die Toleranzzeiten des Debitors kürzer sind als die kumulierten Vorlaufzeiten.

## <a name="the-five-components-of-ddmrp"></a>Die fünf Komponenten von DDMRP

DDMRP besteht aus fünf aufeinander folgenden Komponenten (Schritten). Die ersten drei Komponenten definieren im Wesentlichen die anfängliche und die sich entwickelnde Konfiguration eines bedarfsgesteuerten Planungsmodells für den Materialbedarf. Die letzten beiden Komponenten definieren den alltäglichen Vorgang der Methodik.

1. **[Strategische Bestandspositionierung](ddmrp-inventory-positioning.md)** – Identifizieren Sie Entkopplungspunkte im Lieferkettennetzwerk. Entkopplungspunkte sind bestimmte Punkte in Ihrer Vorratskette, an denen Sie einen Bestandspuffer anlegen, den Sie überwachen und wiederbeschaffen.
2. **[Pufferprofile und -stufen](ddmrp-buffer-profile-and-levels.md)** – Ermitteln Sie für jeden Entkopplungspunkt die Puffergrößen (Mindestmenge, Höchstmenge und Neubestellungspunkt) und die Nachbestellmenge.
3. **[Dynamische Pufferanpassungen](ddmrp-buffer-profile-and-levels.md#dynamic-adjustments)** – Passen Sie die Puffermengen an, basierend auf variierenden Betriebsparametern oder geplanten zukünftigen Ereignissen.
4. **[Bedarfsgesteuerte Planung](ddmrp-planning.md)** – Erzeugen Sie Lieferungsaufträge, wenn sie benötigt werden. Zu diesen Lieferungsaufträgen gehören Fertigungsaufträge, Bestellungen und Umlagerungsaufträge
5. **[Hochgradig kollaborative und sichtbare Ausführung](ddmrp-visual-and-collaborative-execution.md)** – Führen Sie die Lieferungsaufträge mit Hilfe der Visualisierung aus.

DDMRP wird in der Regel von Herstellern verwendet, die über eine mehrstufige Stückliste verfügen. Es kann jedoch auch auf Vertriebs- und Einzelhandelsnetzwerke angewendet werden.

## <a name="ddmrp-in-dynamics-365-supply-chain-management"></a>DDMRP in Dynamics 365 Supply Chain Management

DDMRP ist im Lieferumfang von Microsoft Dynamics 365 Supply Chain Management enthalten und erfordert keine zusätzlichen Lizenzgebühren. Im Supply Chain Management wurde die DDMRP-Funktionalität dem bestehenden Modul **Masterplan** hinzugefügt. Es erfordert jedoch, dass Sie das Add-In Planungsoptimierung verwenden. 

DDMRP ist in die bestehenden Einrichtungen für die Planung im Supply Chain Management integriert und wird zusammen mit diesen Einrichtungen verwendet, um die richtige Planungskonfiguration für Ihr Unternehmen zu finden. Er wird durch einen neuen Coverage Code gesteuert, der sich von Periode, Min/Max, Anforderung usw. völlig unterscheidet. Es handelt sich nicht um ein neues Modul, und es ersetzt auch nicht die bestehenden Planungsfunktionen. Es bietet Ihnen jedoch mehr Funktionalität.
