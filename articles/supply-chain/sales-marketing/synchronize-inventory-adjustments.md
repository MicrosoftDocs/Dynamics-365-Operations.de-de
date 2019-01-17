---
title: Bestandsumlagerungen und Regulierungen von Field Service mit Finance and Operations synchronisieren
description: "Dieses Thema erläutert die Vorlagen und die zugrunde liegende Aufgabe, die verwendet wird, um Produkte aus Microsoft Dynamics 365 for Finance and Operations mit Microsoft Dynamics 365 for Field Service zu synchronisieren."
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.translationtype: HT
ms.sourcegitcommit: 8c6cb481f1a3fe48d329c5936118d8df88a4175b
ms.openlocfilehash: 79a1cfac3fa94223cc9af73e758ce95fd47065c9
ms.contentlocale: de-de
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-adjustments-from-field-service-to-finance-and-operations"></a>Bestandsumlagerungen und Regulierungen von Field Service mit Finance and Operations synchronisieren

[!include[banner](../includes/banner.md)]

Dieses Thema erläutert die Vorlagen und die zugrunde liegende Aufgabe, die verwendet wird, um Produkte aus Microsoft Dynamics 365 for Finance and Operations mit Microsoft Dynamics 365 for Field Service zu synchronisieren.

[![Synchronisierung von Geschäftsprozessen zwischen Finance and Operations und Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)

## <a name="templates-and-tasks"></a>Vorlagen und Aufgaben
Die folgende Vorlage und die zugrunde liegende Aufgabe, die verwendet wird, um Produkte aus Microsoft Dynamics 365 for Field Service mit Microsoft Dynamics 365 for Finance and Operations zu synchronisieren.

**Name der Vorlage in der Datenintegration:**
- Bestandanpassung (Field Service zu Finance and Operations)
- Bestandübertragung (Field Service zu Finance and Operations)

**Namen der Aufgaben im Datenintegrationsprojekt:**
- Lagerbestandsregulierungen
- Lagerumlagerungen

## <a name="entity-set"></a>Entitätssatz
| Field Service                     | Finance and Operations                             |
|-----------------------------------|----------------------------------------------------|
| msdyn_inventoryadjustmentproducts |   Kopfzeilen und Positionen zur CDS-Bestandsanpassungserfassung |
| msdyn_inventoryadjustmentproducts | Kopfzeilen und Positionen zur CDS-Bestandsübertragungserfassung   |

## <a name="entity-flow"></a>Entitätsfluss
Die Lagerregulierungen und Übertragungen, die im Field Service vorgenommen werden, Synchronisieren mit Finance and Operations, wenn der **Beitragsstatus** von erstellt auf buchen geändert wird. Wenn dies eroflt, wird die Regulierung oder der Umlagerungsauftrag gesperrt und wird schreibgeschützt, da  Regulierungen und Überträge in Finance and Operations gebucht werden können und deshalb nicht geändert werden können.
In Finance and Operations können Sie eine Stapelverarbeitung einrichten, die die Übergangslagererfassungen automatisch bucht, die bei der Integration generiert werden. Voraussetzung finden Sie unten, wie der Stapelverarbeitungsauftrag ausgeführt wird.

## <a name="field-service-crm-solution"></a>Field Service CRM-Lösung 
Das Feld Lagereinheit wurde der Produktentität hinzugefügt. Dieses Feld ist erforderlich, da Sales und Bestandeinheit nicht unbedingt gleich ist in Operations und für den Lagerort-Bestand in Operations benötigne wir die Lagereinheit.
Wenn Sie das Produkt in einem Lagerregulierungs-Produkt für beide Lagerregulierungen und Umlagerungen festsetzen, ruft die Einheit aus dem Produkt-Bestand den Produktwert ab. Wenn ein Wert vorhanden ist, wird das Einheitsfeld im Feld Lagerregulierungs-Produkt gesperrt

Das Beitrags-Statusfeld wurde der Lagerregulierungsentität und der Umlagerungsentität hinzugefügt. Dieses Feld dient als Filter und wird verwendet, wenn eine Niedrigerbewertung oder eine Übertragung mit Vorgängen gesendet wird. Das Feld wird als Standard auf erstellt (1) festgelegt und wird dann nicht von Operations übernommen. Wenn Sie eine Änderung machen, wird diese auf gebucht (2) an Operations gesendet, aber Sie können dann nichts mehr in der Regulierung anpassen oder Übertragen oder neue Zeilen hinzufügen.
Das Nummernsequenzfeld wurde der Bestand-Produktentität hinzugefügt. Dieses Feld ermöglicht der Integration, eine eindeutige Nummer zuzuweisen, damit die Integration weiss, wann sie erstellen und wann aktualisieren muss. Wenn Sie das Lagerregulierungs-Produkt zuerst erstellen, erstellt sie ein neuer Datensatz in der P2C-AutoWertentität, um den Präfix Nummernkreis und den verwendeten Präfix zu verwalten.

## <a name="prerequisites-and-mapping-setup"></a>Voraussetzungen und Zuordnungseinrichtung

### <a name="in-finance-and-operations"></a>In Finance and Operations
Die Integrationslagererfassungen, die bei der Integration generiert werden, können mit einem Stapelverarbeitungslauf automatisch gebucht werden. Diese wird aktiviert von: Lagerverwaltung > periodische Aufgaben > CD-Integration > Beitragsintegrationslagererfassungen

## <a name="template-mapping-in-data-integration"></a>Vorlagenzuordnung in Datenintegration

Die folgenden Abbildungen zeigen die Vorlagenzuordnung in Datenintegration.

### <a name="inventory-adjustment-field-service-to-finance-and-operations-inventory-adjustment"></a>Bestandanpassung (Field Service zu Finance and Operations): Bestandregulierung

[![Vorlagenzuordnung in Datenintegration](./media/FSAdj1.png)](./media/FSAdj1.png)


### <a name="inventory-transfer-field-service-to-finance-and-operations-inventory-transfer"></a>Bestandandübertragung (Field Service zu Finance and Operations): Bestandübertragung

[![Vorlagenzuordnung in Datenintegration](./media/FSTrans1.png)](./media/FSTrans1.png)

