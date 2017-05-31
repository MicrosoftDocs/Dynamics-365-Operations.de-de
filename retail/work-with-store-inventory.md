---
title: Shop-Lagerbestand verwalten
description: "Dieser Artikel beschreibt die Dokumentarten, die Sie zum Verwalten des Bestands verwenden können."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 5e5043d5951015fc14d29989ef4cab20a8b24f3b
ms.contentlocale: de-de
ms.lasthandoff: 05/25/2017


---

# <a name="manage-store-inventory"></a>Shop-Lagerbestand verwalten

[!include[banner](includes/banner.md)]


Dieser Artikel beschreibt die Dokumentarten, die Sie zum Verwalten des Bestands verwenden können.

Sie können die folgenden Typen von Dokumenten verwenden, um den Lagerbestand der Organisation zu verwalten.

## <a name="purchase-orders"></a>Bestellungen
Bestellungen werden in der Zentrale erstellt. Wenn ein Einzelhandelslagerort im Bestellkopf enthalten ist, kann der Auftrag im Shop mithilfe von Modern POS (MPOS) oder Cloud POS in Microsoft Dynamics 365 for Operations - Retail empfangen werden. Nachdem die Mengen, die im Shop eingehen, eingegeben wurden, können sie lokal für weitere Änderungen gespeichert werden. Alternativ können die Mengen eingerichtet und an die Zentrale gesendet werden. In der Zentrale werden die Mengen, die im Shop eingegangen sind, in Microsoft Dynamics 365 for Operations im Feld **Aktuelle Lieferung** auf der Bestellung angezeigt.

## <a name="transfer-orders"></a>Umlagerungsaufträge
Mit einem Umlagerungsauftrag kann angegeben werden, dass ein bestimmter Shop ein Lagerplatz ist, von dem Artikel versendet werden können. In diesem Fall wird der Umlagerungsauftrag im Shop als Kommissionierungsanfrage in MPOS oder Cloud POS angezeigt. Nachdem die angeforderten Mengen entnommen wurden, werden sie kommissioniert und an die Zentrale gesendet. In der Zentrale werden die Mengen, die im Shop entnommen wurden, in Microsoft Dynamics 365 for Operations im Feld **Jetzt liefern** des Umlagerungsauftrags angezeigt. Mit einem Umlagerungsauftrag kann angegeben werden, dass ein bestimmter Shop ein Lagerplatz ist, an den Artikel versendet werden können. In diesem Fall wird der Umlagerungsauftrag im Shop als Eingangsanforderung in MPOS oder Cloud POS angezeigt. Nachdem die Mengen, die im Shop eingehen, eingegeben wurden, können sie lokal für weitere Änderungen gespeichert werden. Alternativ können die Mengen eingerichtet und an die Zentrale gesendet werden. In der Zentrale werden die Mengen, die im Shop eingegangen sind, in Microsoft Dynamics 365 for Operations im Feld **Aktuelle Lieferung** auf dem Umlagerungsauftrag angezeigt.

## <a name="stock-counts"></a>Bestandsmengen
Bestandsmengen können entweder geplant oder ungeplant sein. Geplante Bestandszählungen werden in der Zentrale veranlasst, die die zu zählenden Artikel vorgibt. Von der Zentrale wird ein Inventurdokument erstellt, das im Shop empfangen werden kann und in dem die tatsächlich verfügbaren Mengen in MPOS oder Cloud POS eingegeben werden. Ungeplante Bestandsmengen werden in einem Shop initiiert, und die Mengen des tatsächlich verfügbaren Lagerbestands werden in MPOS oder Cloud POS aktualisiert. Im Gegensatz zu geplanten Bestandsmengen haben ungeplante Bestandsmengen keine vordefinierte Liste mit Artikeln. Wenn eine Bestandsmenge eines beliebigen Typs abgeschlossen wurde, wird sie kommissioniert und an die Zentrale gesendet. In der Zentrale wird die Bestandsmenge geprüft und gebucht.






