---
title: Fehlerbehebung bei Teilfreigaben und Teillieferungen
description: In diesem Thema wird beschrieben, wie Sie allgemeine Probleme beheben, die bei der Arbeit mit Teilfreigaben und Teillieferungen in Microsoft Dynamics 365 Supply Chain Management auftreten können.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 1c9246376505e163a4a41bf141a98deed0fd511f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263227"
---
# <a name="troubleshoot-partial-releases-and-partial-shipments"></a>Fehlerbehebung bei Teilfreigaben und Teillieferungen

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie allgemeine Probleme beheben, die bei der Arbeit mit Teilfreigaben und Teillieferungen in Microsoft Dynamics 365 Supply Chain Management auftreten können.

## <a name="the-release-status-of-a-sales-order-remains-partially-released-even-after-the-sales-order-is-invoiced"></a>Der Freigabestatus eines Verkaufsauftrags bleibt teilweise freigegeben, auch nachdem der Auftrag fakturiert wurde.

### <a name="issue-description"></a>Problembeschreibung

Ein Verkaufsauftrag ist ein Lieferauftrag, aber ein oder mehrere Elemente auf ihm haben eine andere Lieferart. Nachdem der Auftrag fakturiert wurde, hat er immer noch einen Freigabestatus von *Teilweise freigegeben*.

Ein Verkaufsauftrag hat z. B. zwei Elemente: eines zur Lieferung und eines zur Abholung. Sowohl die Lieferung als auch die Abholung sind erfolgt. Daher sind beide Zeilen fakturiert worden. Der Freigabestatus wird jedoch immer noch als *Teilweise freigegeben* angezeigt, was irreführend ist.

### <a name="issue-resolution"></a>Problemlösung

Der Freigabestatus gilt nur für Auftragszeilen, bei denen die Elemente für die Lagerortverwaltung freigegeben sind. Daher bleibt der Freigabestatus in diesem Szenario *Teilweise freigegeben*. Microsoft hat dieses Problem untersucht und festgestellt, dass es sich um eine Einschränkung der Funktion handelt. Im Rahmen des Lieferschein- und Fakturierungsprozesses könnte eine Erweiterung hinzugefügt werden, um den Freigabestatus zu aktualisieren.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]