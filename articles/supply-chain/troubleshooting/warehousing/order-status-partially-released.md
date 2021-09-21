---
title: Bestellstatus bleibt nach Rechnungsstellung „Teilweise freigegeben“
description: In einigen Fällen bleibt der Freigabestatus eines Verkaufsauftrags „Teilweise freigegeben“, auch nachdem der Auftrag fakturiert wurde. Auf dieser Seite wird erklärt, warum und eine mögliche Problemumgehung wird erläutert.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 8bfe7ecfd4beb6e77e8dd1e23ccd896d067bdb51
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476454"
---
# <a name="order-status-remains-partially-released-even-after-the-sales-order-is-invoiced"></a>Auftragsstatus bleibt auch nach Fakturierung des Debitorenauftrags teilweise freigegeben

## <a name="symptoms"></a>Symptome

Ein Verkaufsauftrag ist ein Lieferauftrag, aber ein oder mehrere Elemente auf ihm haben eine andere Lieferart. Nachdem der Auftrag fakturiert wurde, hat er immer noch einen Freigabestatus von *Teilweise freigegeben*.

Ein Verkaufsauftrag hat z. B. zwei Elemente: eines zur Lieferung und eines zur Abholung. Sowohl die Lieferung als auch die Abholung sind erfolgt. Daher sind beide Zeilen fakturiert worden. Der Freigabestatus wird jedoch immer noch als *Teilweise freigegeben* angezeigt, was irreführend ist.

## <a name="workaround"></a>Problemumgehung

Der Freigabestatus gilt nur für Auftragszeilen, bei denen die Elemente für die Lagerortverwaltung freigegeben sind. Daher bleibt der Freigabestatus in diesem Szenario *Teilweise freigegeben*. Microsoft hat dieses Problem untersucht und festgestellt, dass es sich um eine Einschränkung der Funktion handelt. Im Rahmen des Lieferschein- und Fakturierungsprozesses könnte eine Erweiterung hinzugefügt werden, um den Freigabestatus zu aktualisieren.
