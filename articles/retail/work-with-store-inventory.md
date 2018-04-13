---
title: Shop-Lagerbestand verwalten
description: "Dieser Artikel beschreibt die Dokumentarten, die Sie zum Verwalten des Bestands verwenden können."
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 6245d37ace9f46ecce83a0cf80a014d5de898bbc
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="manage-store-inventory"></a>Shop-Lagerbestand verwalten

[!INCLUDE [banner](includes/banner.md)]

Dieser Artikel beschreibt die Dokumentarten, die Sie zum Verwalten des Bestands verwenden können.

Sie können die folgenden Typen von Dokumenten verwenden, um den Lagerbestand der Organisation zu verwalten.

## <a name="purchase-orders"></a>Bestellungen
Bestellungen werden in der Zentrale erstellt. Wenn ein Einzelhandelslagerort im Bestellkopf enthalten ist, kann der Auftrag im Shop mithilfe von Modern POS (MPOS) oder Cloud POS in Microsoft Dynamics 365 for Retail empfangen werden. Nachdem die Mengen, die im Shop eingehen, eingegeben wurden, können sie lokal für weitere Änderungen gespeichert werden. Alternativ können die Mengen eingerichtet und an die Zentrale gesendet werden. In der Zentrale werden die Mengen, die im Shop eingegangen sind, in Microsoft Dynamics 365 for Retail im Feld **Aktuelle Lieferung** auf der Bestellung angezeigt.

## <a name="transfer-orders"></a>Umlagerungsaufträge
Mit einem Umlagerungsauftrag kann angegeben werden, dass ein bestimmter Shop ein Lagerplatz ist, von dem Artikel versendet werden können. In diesem Fall wird der Umlagerungsauftrag im Shop als Kommissionierungsanfrage in MPOS oder Cloud POS angezeigt. Nachdem die angeforderten Mengen entnommen wurden, werden sie kommissioniert und an die Zentrale gesendet. In der Zentrale werden die Mengen, die im Shop entnommen wurden, in Microsoft Dynamics 365 for Retail im Feld **Jetzt liefern** des Umlagerungsauftrags angezeigt. Mit einem Umlagerungsauftrag kann angegeben werden, dass ein bestimmter Shop ein Lagerplatz ist, an den Artikel versendet werden können. In diesem Fall wird der Umlagerungsauftrag im Shop als Eingangsanforderung in MPOS oder Cloud POS angezeigt. Nachdem die Mengen, die im Shop eingehen, eingegeben wurden, können sie lokal für weitere Änderungen gespeichert werden. Alternativ können die Mengen eingerichtet und an die Zentrale gesendet werden. In der Zentrale werden die Mengen, die im Shop eingegangen sind, in Microsoft Dynamics 365 for Retail im Feld **Aktuelle Lieferung** im Umlagerungsauftrag angezeigt.

## <a name="stock-counts"></a>Bestandsmengen
Bestandsmengen können entweder geplant oder ungeplant sein. Geplante Bestandszählungen werden in der Zentrale veranlasst, die die zu zählenden Artikel vorgibt. Von der Zentrale wird ein Inventurdokument erstellt, das im Shop empfangen werden kann und in dem die tatsächlich verfügbaren Mengen in MPOS oder Cloud POS eingegeben werden. Ungeplante Bestandsmengen werden in einem Shop initiiert, und die Mengen des tatsächlich verfügbaren Lagerbestands werden in MPOS oder Cloud POS aktualisiert. Im Gegensatz zu geplanten Bestandsmengen haben ungeplante Bestandsmengen keine vordefinierte Liste mit Artikeln. Wenn eine Bestandsmenge eines beliebigen Typs abgeschlossen wurde, wird sie kommissioniert und an die Zentrale gesendet. In der Zentrale wird die Bestandsmenge geprüft und gebucht.

## <a name="inventory-lookup"></a>Bestandsuche
Die aktuelle Produktmenge für Mehrfachshops und Lagerorte kann auf der Bestandssuchenseite angezeigt werden. Neben der aktuellen verfügbaren Menge können auch künftige Verfügbarkeitszusagen-Mengen (ATP) für jede einzelne Filiale angezeigt werden. Klicken Sie hierfür auf die Filiale, für die Sie die VfZ für anzeigen möchten, und klicken Sie auf **Verfügbarkeit in Filiale anzeigen**.





