---
title: Die Menge ist bei der Registrierung eingehender Aufträge nicht gültig
description: 'Wenn die für ein Kennzeichnung zugeordnete Menge die Menge überschreitet, die für die aktuellen Dimensionen noch empfangen werden muss, wird folgender Fehler angezeigt: „Die Menge ist nicht gültig.“'
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 5099b320447bf59c72f5017564ea660f19c690a5
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476484"
---
# <a name="license-plate-quantity-is-not-valid-when-registering-inbound-orders"></a>Die Kennzeichenmenge ist bei der Registrierung eingehender Bestellungen nicht gültig.

## <a name="symptoms"></a>Symptome

Wenn Sie eingehende Aufträge registrieren, erhalten Sie möglicherweise die folgende Fehlermeldung:

> Die Menge ist ungültig.

Wenn das Feld **Kennzeichengruppierungsrichtlinie** für ein Menüelement eines mobilen Geräts, mit dem eingehende Aufträge registriert werden, auf *Benutzerdefiniert* eingestellt ist, wird dieser Fehler angezeigt und Sie können die Registrierung nicht abschließen.

## <a name="cause"></a>Ursache

Wenn *Benutzerdefiniert* als Ladungsträgergruppierungsrichtlinie verwendet wird, teilt das System den eingehenden Bestand in separate Ladungsträger auf, wie in der Nummernkreisgruppe der Einheit angegeben. Wenn Chargen- oder Seriennummern verwendet werden, um den eingehenden Artikel zu verfolgen, müssen die Mengen jeder Charge oder Seriennummer pro registrierter Kennzeichnung angegeben werden. Wenn die für eine Kennzeichnung angegebene Menge die Menge überschreitet, die für die aktuellen Dimensionen noch empfangen werden muss, wird diese Fehlermeldung angezeigt.

## <a name="resolution"></a>Lösung

Wenn Sie einen Artikel mithilfe eines Menüelements für mobile Geräte registrieren, in dem das Feld **Landungsträgergruppierungsichtlinie** auf *Benutzerdefiniert* ist, verlangt das System möglicherweise, dass Sie Kennzeichen-, Chargen- oder Seriennummern bestätigen oder eingeben.

Auf der Seite zur Bestätigung der Kennzeichnung zeigt das System die Menge an, die der aktuellen Kennzeichnung zugeordnet ist. Auf den Seiten zur Chargen- oder Serienbestätigung zeigt das System die Menge, die auf dem aktuellen Ladungsträger noch empfangen werden muss. Dazu gehört auch ein Feld, in das Sie die Menge eingeben können, die für diese Kombination aus Ladungsträger und Chargen- oder Seriennummer registriert werden soll. Stellen Sie in diesem Fall sicher, dass die Menge, die für die Kennzeichnung registriert wird, die Menge nicht überschreitet, die noch empfangen werden muss.

Wenn bei der Registrierung eingehender Bestellungen zu viele Ladungsträger generiert werden, wird alternativ der Wert des Felds **Ladungsträgergruppierungsrichtlinie** auf *Ladungsträgergruppierung* geändert werden, dem Artikel kann eine neue Nummernkreisgruppe für die Einheit zugewiesen werden oder die Option **Ladungsträgergruppierung** kann für die Nummernkreisgruppe für die Einheit deaktiviert werden.
