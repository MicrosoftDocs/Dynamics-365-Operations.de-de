---
title: Verzögerungswert wird nicht aktualisiert, wenn Sie einen Planauftrag neu terminieren
description: Verzögerungswert wird nicht aktualisiert, wenn Sie einen Planauftrag neu terminieren
author: ChristianRytt
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 566702913774cf002ab38e367f690a479d968657
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476467"
---
# <a name="the-delay-value-isnt-updated-when-you-reschedule-a-planned-order"></a>Verzögerungswert wird nicht aktualisiert, wenn Sie einen Planauftrag neu terminieren

## <a name="symptoms"></a>Symptome

Der Verzögerungswert wird nicht aktualisiert, wenn Sie einen Planauftrag neu terminieren.

## <a name="resolution"></a>Lösung

Um die Verzögerung für Planaufträge zu aktualisieren, öffnen Sie das Dialogfeld **Umplanung** für den Planauftrag. Stellen Sie auf dem Inforegister **Auflösung** sicher, dass die Option **Auflösung nach Neuterminierung durchführen** auf *Ja* festgelegt ist.
