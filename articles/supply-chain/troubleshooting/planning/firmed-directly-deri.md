---
title: Direkt abgeleitete umgewandelte Aufträge werden von einem Workflow mit laufender Überprüfung verarbeitet
description: Direkt abgeleitete umgewandelte Aufträge werden von einem Workflow mit dem Status „Wird überprüft“ verarbeitet.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: d20f1c1d6e8fc83dd996b04bf0321a41f7b39290f306d1ac9f4fcd17514832e6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6721174"
---
# <a name="directly-derived-firmed-orders-are-processed-by-an-in-review-workflow"></a>Direkt abgeleitete umgewandelte Aufträge werden von einem Workflow mit laufender Überprüfung verarbeitet

KB-Nummer: 4612450

## <a name="symptoms"></a>Symptome

Direkt abgeleitete umgewandelte Aufträge werden von einem Workflow mit dem Status *Wird überprüft* verarbeitet.

## <a name="resolution"></a>Lösung

Wenn die Änderungsnachverfolgung aktiviert ist, wird abgeleiteten umgewandelten Aufträgen (Unterauftragsbestellung) den Status *Wird überprüft*. Wenn eine Bestellung abgeleitet wird (eine Unterauftragsbestellung), wird sie daher nur an einen Workflow gesendet. Wenn es sich bei einer Bestellung um eine umgewandelte geplante Einkaufsbestellung handelt, wird diese automatisch genehmigt, um sicherzustellen, dass die Planungs-Engine keine neuen geplanten Bestellungen erstellt, während die Bestellung den Status *Entwurf* hat.
