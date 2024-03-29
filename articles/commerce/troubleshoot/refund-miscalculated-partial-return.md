---
title: Rückerstattungsfähige Belastungen werden auf der Grundlage der zurückgegebenen Menge falsch berechnet
description: Dieser Artikel enthält Hinweise zur Problembehandlung, die Ihnen helfen können, wenn Kassierer am Point of Sale (POS) falsche erstattungsfähige Belastungen für die Menge der zurückgegebenen Artikel sehen.
author: gvrmohanreddy
ms.date: 03/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 7a84207f587a826b9acdfd818c64220c5327bde1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890242"
---
# <a name="refundable-charges-are-miscalculated-based-on-the-quantity-returned"></a>Rückerstattungsfähige Belastungen werden auf der Grundlage der zurückgegebenen Menge falsch berechnet

[!include [banner](../../includes/banner.md)]

Dieser Artikel enthält Hinweise zur Problembehandlung, die Ihnen helfen können, wenn Kassierer am Point of Sale (POS) falsche erstattungsfähige Belastungen für die Menge der zurückgegebenen Artikel sehen.

## <a name="description"></a>Description

Ein Kunde gibt eine Teilmenge der Artikel zurück, die für einen Verkaufsauftrag mit zeilenweise erstattungsfähigen Belastungen gekauft wurden. Anstatt einer teilweisen Rückerstattung zeigt POS jedoch alle Belastungen als erstattungsfähig an.

Ein Beispiel: Ein Kunde kauft eine Menge von fünf Artikeln zu $5 pro Artikel, was Gesamtbelastungen von $25 ergibt. Der Kunde schickt dann drei der fünf Elemente zurück. Allerdings wird dem Kassierer an der Kasse eine erstattungsfähige Gebühr in Höhe von 25 $ angezeigt, anstatt der erwarteten erstattungsfähigen Gebühr von 15 $ für die drei zurückgegebenen Artikel.

## <a name="resolution"></a>Lösung

### <a name="turn-on-the-enable-refunding-charges-based-on-the-refunded-quantity-feature"></a>Aktivieren Sie die Funktion Rückerstattung von Belastungen auf Basis der rückerstatteten Menge aktivieren

Ab Microsoft Dynamics 365 Commerce Version 10.0.26 ermöglicht die Funktion **Erstattung von Belastungen auf Basis der zurückerstatteten Menge aktivieren** die Berechnung von erstattungsfähigen Belastungen auf Zeilenebene auf der Grundlage der Menge der zurückgegebenen Artikel.

So aktivieren Sie die Funktion **Rückerstattung von Belastungen auf Basis der erstatteten Menge** in der Commerce Zentrale.

1. Öffnen Sie den Arbeitsbereich **Funktionsverwaltung** (**Systemadministrator \> Arbeitsbereiche \> Funktionsverwaltung**).
1. Suchen Sie in der Liste der verfügbaren Funktionen nach der Funktion **Erstattung von Belastungen auf Basis der erstatteten Menge aktivieren** und wählen Sie sie aus.
1. Wählen Sie im rechten Fensterbereich **Jetzt aktivieren**.
