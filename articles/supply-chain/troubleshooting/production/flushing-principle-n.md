---
title: Die Einstellungen für das Stücklisten-Bezugsprinzip in Stücklistenpositionen werden nicht berücksichtigt
description: Die Einstellungen für das Stücklisten-Bezugsprinzip in Stücklistenpositionen werden nicht berücksichtigt.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PurchTable,ProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ee40eff53efd920ebe43a7b2dd28129f01e6ebb5e75bd480a91f758529f77fc5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6716955"
---
# <a name="flushing-principle-settings-on-bom-lines-arent-respected"></a>Die Einstellungen für das Stücklisten-Bezugsprinzip in Stücklistenpositionen werden nicht berücksichtigt

KB-Nummer: 4612725

## <a name="symptoms"></a>Symptome

Dieses Problem tritt auf, wenn das Feld **Automatischer Stücklistenverbrauch** in der Registerkarte **Automatisches Update** auf der Seite **Produktionssteuerungsparameter** ist auf *Stücklisten-Bezugsprinzip* eingestellt. Diese Einstellung gibt an, dass alle Stücklistenpositionen beim Eingang einer Bestellung automatisch verbraucht werden sollen. Wenn das Feld **Stücklisten-Bezugsprinzip** bei Stücklistenpositionen nicht explizit auf *Manuell* gesetzt ist, wäre zu erwarten, dass die Stücklistenpositionen nicht automatisch verbraucht werden. Wenn dieses Problem auftritt, werden in Stücklistenpositionen, in denen das Feld **Stücklisten-Bezugsprinzip** auf *Manuell* gesetzt ist, jedoch automatisch verbraucht.

## <a name="resolution"></a>Lösung

Wenn dieses Problem auftritt, sind Ihre Produktionssteuerungsparameter möglicherweise so eingerichtet, dass sie die **Stücklisten-Bezugsprinzip**-Einstellung auf Stücklistenpositionen überschreiben. Überprüfen Sie auf der Seite **Produktionssteuerungsparameter** auf der Registerkarte **Automatisches Update** den Wert des Felds **Automatischer Stücklistenverbrauch**. Wenn es auf *Immer* eingestellt ist, ignoriert das System die **Stücklisten-Bezugsprinzip**-Einstellung auf allen Stücklistenpositionen und leert die Positionen immer. Damit das System **Stücklisten-Bezugsprinzip**-Einstellung respektiert, andern Sie in den Stücklistenpositionen den Wert des Felds **Automatischer Stücklistenverbrauch** auf *Stücklisten-Bezugsprinzip*.
