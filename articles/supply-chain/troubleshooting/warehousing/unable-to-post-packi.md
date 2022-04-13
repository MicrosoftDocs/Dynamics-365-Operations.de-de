---
title: Lieferschein für eine gestoppte Zeile eines Verkaufsauftrags kann nicht gebucht werden
description: Sie können keinen Lieferschein für eine gestoppte Zeile eines Verkaufsauftrags buchen
author: smithanataraj
ms.date: 03/07/2022
ms.topic: article
ms.search.form: WHSLoadTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mfp
ms.search.validFrom: 2022-03-07
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 115cfe79e075eb36f73203818acdbb5e31fc0bad
ms.sourcegitcommit: c0f7ee7f8837fec881e97b2a3f12e7f63cf96882
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2022
ms.locfileid: "8462851"
---
# <a name="cant-post-packing-slip-for-a-stopped-a-sales-order-line"></a>Lieferschein für eine gestoppte Zeile eines Verkaufsauftrags kann nicht gebucht werden

Fehlercode: SYS13203

## <a name="symptoms"></a>Symptome

Wenn Sie versuchen, einen Lieferschein für eine Ladung zu buchen, zeigt das System die folgende Fehlermeldung an:

> Lieferschein kann nicht gebucht werden, wenn eine Verkaufsauftragszeile nach Bestätigung der ausgehenden Sendung angehalten wird Eine Menge kann nicht kommissioniert werden.

## <a name="cause"></a>Ursache

Eine oder mehrere der zugehörigen Verkaufsauftragszeilen können angehalten werden, was bedeutet, dass das System die weitere Verarbeitung dieses Verkaufsauftrags verhindert. Das bedeutet unter anderem, dass das System keinen Lieferschein für die Bestellung bucht.

Zum Beispiel kann ein Benutzer beschlossen haben, eine oder mehrere Bestellzeilen zu stoppen, weil der Kunde zurückgerufen und seine Bestellung storniert hat. Wenn der ausgehende Versand jedoch bereits bestätigt wurde, dann hat die Sendung, die den Verkaufsauftrag enthält, das Lager bereits physisch verlassen, was bedeutet, dass das Anhalten der Verkaufsauftragszeilen keine Auswirkungen hat. Da es nicht mehr möglich ist, die Sendung physisch zu stoppen, können Sie die Zeilen auch aufheben, um den Lieferschein zu buchen. Sie müssen dann die stornierte Bestellung als Rückgabe behandeln.

## <a name="resolution"></a>Lösung

Um den Lieferschein buchen zu können, stellen Sie sicher, dass keine der relevanten Verkaufsauftragszeilen angehalten ist, indem Sie die folgenden Schritte ausführen.

1. Gehen Sie zu **Alle Verkaufsaufträge \> Vertrieb und Marketing \> Alle Verkaufsaufträge**.
1. Suchen und öffnen Sie den Verkaufsauftrag, mit dem Sie Probleme haben.
1. Wählen Sie auf dem Inforegister **Verkaufsauftragszeilen** eine Auftragszeile aus.
1. Öffnen Sie auf der Registerkarte **Zeilendetails** das Inforegister **Allgemein** und stellen Sie sicher, dass das Feld **Abgebrochen** auf *Nein* festgelegt ist.
1. Arbeiten Sie weiter, bis alle betroffenen Zeilen nicht mehr angehalten werden.
1. Versuchen Sie erneut, den Lieferschein für die Ladung oder den Verkaufsauftrag zu buchen.
