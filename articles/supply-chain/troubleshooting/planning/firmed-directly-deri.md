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
ms.openlocfilehash: d54985707d82df2b947a7cb615fc25f90aa31702
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026549"
---
# <a name="directly-derived-firmed-orders-are-processed-by-an-in-review-workflow"></a>Direkt abgeleitete umgewandelte Aufträge werden von einem Workflow mit laufender Überprüfung verarbeitet

KB-Nummer: 4612450

## <a name="symptoms"></a>Symptome

Direkt abgeleitete umgewandelte Aufträge werden von einem Workflow mit dem Status *Wird überprüft* verarbeitet.

## <a name="resolution"></a>Lösung

Wenn die Änderungsnachverfolgung aktiviert ist, wird abgeleiteten umgewandelten Aufträgen (Unterauftragsbestellung) den Status *Wird überprüft*. Wenn eine Bestellung abgeleitet wird (eine Unterauftragsbestellung), wird sie daher nur an einen Workflow gesendet. Wenn es sich bei einer Bestellung um eine umgewandelte geplante Einkaufsbestellung handelt, wird diese automatisch genehmigt, um sicherzustellen, dass die Planungs-Engine keine neuen geplanten Bestellungen erstellt, während die Bestellung den Status *Entwurf* hat.
