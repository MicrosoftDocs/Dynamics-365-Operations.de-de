---
title: Die Reservierung von Inventar in einer Auftragsposition kann nicht aufgehoben werden
description: Wenn für eine Verkaufszeile offene Aufträge vorhanden sind und Sie versuchen, die Reservierung von Inventar in der Zeile aufzuheben, erhalten Sie eine Fehlermeldung. Vervollständigen oder löschen Sie die Arbeit, um die Reservierung freizugeben.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 1a042065dc4cd637aff58e55cf16179b7022f6ca
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476453"
---
# <a name="cant-unreserve-inventory-on-a-sales-order-line"></a>Die Reservierung von Inventar in einer Auftragsposition kann nicht aufgehoben werden

## <a name="symptoms"></a>Symptome

Wenn für eine Verkaufszeile offene Aufträge vorhanden sind und Sie versuchen, die Reservierung von Inventar in der Zeile aufzuheben, erhalten Sie folgende Fehlermeldung:

> Reservierungen können nicht entfernt werden, da von diesen Reservierungen abhängige Arbeit erstellt wird.

## <a name="resolution"></a>Lösung

Untersuchen Sie, ob offene Packgruppenarbeit existiert, um das Element von einem Packplatz zu einem anderen Lagerplatz zu bringen (z. B. *Baydoor*). Überprüfen Sie die Datensätze auf den Seiten **Arbeitserstellungsprotokoll** und **Arbeitsdetails**, um festzustellen, was den Bestand physisch reserviert, und schließen Sie dann die Arbeit ab oder löschen Sie sie, um die Reservierung freizugeben.
