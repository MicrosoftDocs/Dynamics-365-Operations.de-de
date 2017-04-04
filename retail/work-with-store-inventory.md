---
title: Shop-Lagerbestand verwalten
description: "In diesem Artikel wird beschrieben die Dokumenttypen, die Sie verwenden können, um den Bestand verwalten."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: fbe9945799f1e65ed6ad624a3df270fa4eb72b88
ms.lasthandoff: 03/31/2017


---

# <a name="manage-store-inventory"></a>Shop-Lagerbestand verwalten

In diesem Artikel wird beschrieben die Dokumenttypen, die Sie verwenden können, um den Bestand verwalten.

Sie können die folgenden Typen von Dokumenten verwenden, um den Lagerbestand der Organisation zu verwalten.

## <a name="purchase-orders"></a>Bestellungen
Bestellungen werden in der Zentrale erstellt. Wenn ein Kleinlagerort im Bestellkopf enthalten ist, kann der Auftrag in Ihrem Unternehmen eingehen, indem modernes POS MPOS () oder Cloud POS in Microsoft Dynamics 365 für Einzelhandel - Arbeitsgänge verwendet. Nachdem die Mengen, die im Shop eingehen, eingegeben wurden, können sie lokal für weitere Änderungen gespeichert werden. Alternativ können die Mengen eingerichtet und an die Zentrale gesendet werden. In der Firmenzentrale werden die Mengen, die in Ihrem Unternehmen empfangen wurden, in Dynamics 365 für Arbeitsgänge, im ** erhalten Sie nun ** Feld der Bestellung angezeigt.

## <a name="transfer-orders"></a>Umlagerungsaufträge
Mit einem Umlagerungsauftrag kann angegeben werden, dass ein bestimmter Shop ein Lagerplatz ist, von dem Artikel versendet werden können. In diesem Fall wird der Umlagerungsauftrag im Unternehmen als Entnahmeanforderung in MPOS oder in der Cloud POS. Nachdem die angeforderten Mengen entnommen wurden, werden sie kommissioniert und an die Zentrale gesendet. In der Firmenzentrale werden die Mengen, die entnommen wurden im Unternehmen, in Dynamics 365 für Arbeitsgänge, im ** Versand- nun ** Feld auf im Umlagerungsauftrag angezeigt. Mit einem Umlagerungsauftrag kann angegeben werden, dass ein bestimmter Shop ein Lagerplatz ist, an den Artikel versendet werden können. In diesem Fall wird der Umlagerungsauftrag im Unternehmen als Eingangsformular Anforderung in MPOS oder in der Cloud POS. Nachdem die Mengen, die im Shop eingehen, eingegeben wurden, können sie lokal für weitere Änderungen gespeichert werden. Alternativ können die Mengen eingerichtet und an die Zentrale gesendet werden. In der Firmenzentrale werden die Mengen, die in Ihrem Unternehmen empfangen wurden, in Dynamics 365 für Arbeitsgänge, im ** erhalten Sie nun ** Feld auf im Umlagerungsauftrag angezeigt.

## <a name="stock-counts"></a>Bestandsmengen
Bestandsmengen können entweder geplant oder ungeplant sein. Geplante Bestandszählungen werden in der Zentrale veranlasst, die die zu zählenden Artikel vorgibt. Von der Zentrale wird ein Inventurdokument erstellt, das in Ihrem Unternehmen eingehen kann, wo die tatsächlichen Mengen des verfügbaren Bestands in MPOS POS eingegeben oder bewölken werden. Ungeplante Bestandszählungen werden zu einem Shop initiiert, und die tatsächlichen Mengen des verfügbaren Bestands werden entweder in MPOS aktualisiert oder bewölken POS. Im Gegensatz zu geplanten Bestandsmengen haben ungeplante Bestandsmengen keine vordefinierte Liste mit Artikeln. Wenn eine Bestandsmenge eines beliebigen Typs abgeschlossen wurde, wird sie kommissioniert und an die Zentrale gesendet. In der Zentrale wird die Bestandsmenge geprüft und gebucht.




