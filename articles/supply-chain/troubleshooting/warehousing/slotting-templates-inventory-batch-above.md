---
title: Verfügbarer Lagerbestand für „Charge oberhalb“-Artikel nicht berücksichtigt
description: Gewisse Vorlagen berücksichtigen den aktuellen verfügbaren Bestand für Charge oberhalb-Artikel nicht. Die Chargen- oder Seriennummer muss im Bedarfsauftrag angegeben werden.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: df5642b32f5e053144230eab3dbcf633f526279a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476444"
---
# <a name="slotting-templates-dont-consider-on-hand-inventory-for-batch-above-items"></a>Vorlagen für die Zuteilung von Zeitfenstern berücksichtigen nicht den Lagerbestand für „Charge oberhalb“-Artikel

## <a name="symptoms"></a>Symptome

Vorlagen für die Zuteilung von Zeitfenstern mit dem Zeitfensterkriterium *Vorhandenes berücksichtigen* berücksichtigen nicht den aktuellen Bestand von *Charge oberhalb*-Artikeln. Sie berücksichtigen es nur, wenn die Chargennummer in der Auftragsposition angegeben ist.

Wenn Sie jedoch *Chargen unterhalb*-Artikel verwenden, wird der aktuelle Bestand wie erwartet angesehen.

Weitere Informationen finden Sie unter [Zeitfenster für Lagerort zuweisen](/dynamics365/supply-chain/warehousing/warehouse-slotting).

## <a name="resolution"></a>Lösung

Die Kopfzeile der Vorlage für die Zuteilung von Zeitfenstern kann für die Bedarfsstrategie *Bestellt*, *Reserviert* oder *Freigegeben* definiert werden. Für die Bedarfsstrategie *Bestellt* gelten dieselben Anforderungen an die Reservierungshierarchie wie für die Prozesse zur Reservierung oder Freigabe an Lagerorte. Für Artikel mit der Reservierungshierarchie *Charge oberhalb* und *Serie unterhalb* muss die Chargen- oder Seriennummer auf dem Bedarfsauftrag (Verkauf oder Übertragung) angegeben werden.

Alternativ kann die Bedarfsstrategie *Reserviert* verwendet werden, um die Chargen- oder Seriennummer auszuwählen, bevor der Bedarf zur Zuteilung eines Zeitfensters am Lagerort generiert wird.
