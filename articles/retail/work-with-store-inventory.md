---
title: Bestandsverwaltung im Laden
description: Dieser Artikel beschreibt die Dokumentarten, die Sie zum Verwalten des Bestands verwenden können.
author: rubencdelgado
manager: AnnBe
ms.date: 01/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
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
ms.openlocfilehash: 02f8afbe3bb6f94c66a8b5aa02531c219adc3963
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "339233"
---
# <a name="store-inventory-management"></a>Bestandsverwaltung im Laden

[!include [banner](includes/banner.md)]

Dieser Artikel beschreibt die Dokumentarten, die Sie zum Verwalten des Bestands verwenden können.

Sie können die folgenden Typen von Dokumenten verwenden, um den Lagerbestand der Organisation zu verwalten.

Bei der Arbeit mit dem Bestand in Dynamics 365 for Retail und der Verwendung der POS-Anwendung ist zu beachten, dass der POS nur begrenzte Unterstützung für Bestandsdimensionen und bestimmte Bestandsartikelarten bietet.  

Die POS-Lösung unterstützt die folgenden Artikelkonfigurationen nicht:
- Stücklistenpositionen (außer Kitprodukten, die einige Komponenten des Stücklistenrahmens verwenden)
- Artikelgewichtsartikel
- Chargengesteuerte Artikel

Die POS-Anwendung unterstützt derzeit die folgenden Tracking-Dimensionen am POS nicht:
- Dimension der Chargenverfolgung
- Eigentümerdimension

Die POS-Lösung bietet begrenzte Unterstützung für die folgenden Dimensionen. Eingeschränkte Unterstützung deutet darauf hin, dass der POS einige dieser Dimensionen automatisch in Bestandstransaktionen einbinden kann, basierend auf der Konfiguration von Lager/Geschäft. POS unterstützt die Dimensionen nicht vollständig in der Art und Weise, wie sie unterstützt werden, wenn ein Verkaufsvorgang manuell in das ERP eingegeben wird. 

- Ziel
- Ladungsträger (gilt nur, wenn der **Prozess der Lagerverwaltung für den Artikel** und das Lager aktiviert wurde).
- Seriennummer
- Bestandsstatus

> [!NOTE]
> Alle Unternehmen müssen Artikelkonfigurationen über den POS in Entwicklungs- oder Testumgebungen testen, bevor sie in der Produktion eingesetzt werden können. Testen Sie Ihre Artikel, indem Sie regelmäßige Cash and Carry-Verkaufstransaktionen durchführen und Kundenaufträge (falls vorhanden) über die POS mit Ihren Artikeln erstellen. Das Testen muss die Durchführung eines vollständigen Buchungsprozesses in Ihrer Testumgebung und die Überprüfung, ob es keine Probleme gibt, beinhalten.
> Wenn Sie Artikel ohne ordnungsgemäße Tests so konfigurieren, dass sie nicht von der POS-Anwendung unterstützt werden, kann dies dazu führen, dass Ihr Prozess der Rechnungsbuchung in der Produktion fehlschlägt, ohne dass Sie die Probleme einfach beheben können. Partner- oder Kundenanpassungen an die Anwendung können optional in Betracht gezogen werden, damit diese Buchungsprozesse erfolgreich abgeschlossen werden können. Wenn keine Anpassungen erforderlich sind, muss das Unternehmen sicherstellen, dass die Produktkonfiguration Ihrer Produkte in einer Weise erfolgt ist, die vom Standard-POS-Anwendungs-/Auftragserstellungs-/Anlagenbuchungsprozess unterstützt wird.

## <a name="purchase-orders"></a>Bestellungen

Bestellungen werden in der Zentrale erstellt. Wenn ein Einzelhandelslagerort im Bestellkopf enthalten ist, kann der Auftrag im Shop mithilfe von Modern POS (MPOS) oder Cloud POS in Microsoft Dynamics 365 for Retail empfangen werden. Nachdem die Mengen, die im Shop eingehen, eingegeben wurden, können sie lokal für weitere Änderungen gespeichert werden. Alternativ können die Mengen eingerichtet und an die Zentrale gesendet werden. In der Zentrale werden die in der Filiale eingegangenen Mengen auf Dynamics 365 for Retail im Feld **Jetzt erhalten** auf der Bestellung angezeigt.

## <a name="transfer-orders"></a>Umlagerungsaufträge

Mit einem Umlagerungsauftrag kann angegeben werden, dass ein bestimmter Shop ein Lagerplatz ist, von dem Artikel versendet werden können. In diesem Fall wird der Umlagerungsauftrag im Shop als Kommissionierungsanfrage in MPOS oder Cloud POS angezeigt. Nachdem die angeforderten Mengen entnommen wurden, werden sie kommissioniert und an die Zentrale gesendet. In der Zentrale werden die Mengen, die in der Filiale kommissioniert wurden, auf Dynamics 365 for Retail im Feld **Versand jetzt** auf dem Transportauftrag angezeigt. Mit einem Umlagerungsauftrag kann angegeben werden, dass ein bestimmter Shop ein Lagerplatz ist, an den Artikel versendet werden können. In diesem Fall wird der Umlagerungsauftrag im Shop als Eingangsanforderung in MPOS oder Cloud POS angezeigt. Nachdem die Mengen, die im Shop eingehen, eingegeben wurden, können sie lokal für weitere Änderungen gespeichert werden. Alternativ können die Mengen eingerichtet und an die Zentrale gesendet werden. In der Zentrale werden die in der Filiale eingegangenen Mengen auf Dynamics 365 for Retail im Feld **Jetzt erhalten** auf dem Transferauftrag angezeigt.

## <a name="stock-counts"></a>Bestandsmengen

Bestandsmengen können entweder geplant oder ungeplant sein. Geplante Bestandszählungen werden in der Zentrale veranlasst, die die zu zählenden Artikel vorgibt. Von der Zentrale wird ein Inventurdokument erstellt, das im Shop empfangen werden kann und in dem die tatsächlich verfügbaren Mengen in MPOS oder Cloud POS eingegeben werden. Ungeplante Bestandsmengen werden in einem Shop initiiert, und die Mengen des tatsächlich verfügbaren Lagerbestands werden in MPOS oder Cloud POS aktualisiert. Im Gegensatz zu geplanten Bestandsmengen haben ungeplante Bestandsmengen keine vordefinierte Liste mit Artikeln. Wenn eine Bestandsmenge eines beliebigen Typs abgeschlossen wurde, wird sie kommissioniert und an die Zentrale gesendet. In der Zentrale wird die Bestandsmenge geprüft und gebucht.

## <a name="inventory-lookup"></a>Bestandsuche

Die aktuelle Produktmenge für Mehrfachshops und Lagerorte kann auf der Bestandssuchenseite angezeigt werden. Neben der aktuellen verfügbaren Menge können auch künftige Verfügbarkeitszusagen-Mengen (ATP) für jede einzelne Filiale angezeigt werden. Klicken Sie hierfür auf die Filiale, für die Sie die VfZ für anzeigen möchten, und klicken Sie auf **Verfügbarkeit in Filiale anzeigen**.
