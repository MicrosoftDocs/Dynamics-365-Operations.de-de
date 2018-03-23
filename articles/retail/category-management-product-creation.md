---
title: Produktkategorieverwaltung
description: "In diesem Thema wird beschrieben, wie Verkaufmanager Produktkategorien (Einzelhandel) verwenden können, um Beziehungen zwischen Produkthierarchie (Einzelhandel) und freigegebenen Produktdetails zu verwalten."
author: ashishmsft
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 
ms.assetid: c7ed2ba5-87c6-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 25fa39dc81fc721d7593a25a102ce47041ebc5f0
ms.openlocfilehash: 4b7ef962b777a31e1da238a8ec1be9a42ec5bb5f
ms.contentlocale: de-de
ms.lasthandoff: 03/13/2018

---


# <a name="enhanced-product-and-category-management"></a>Verbesserte Kategorie- und Produktverwaltung

[!include[banner](./includes/banner.md)]

Dieses Thema beschreibt eine erweiterte Art, Produktkategorien (Einzelhandel) und Produkte in Dynamics 365 for Retail zu verwalten. Mit diesen Erweiterungen können Verkaufmanager eine Wechselbeziehung zwischen Produkthierarchie (Einzelhandel) und freigegebenen Produktdetails haben.

Um mehr über das Verwalten von Produktkategorien (Retail) zu ermitteln, gehen sie zu**Produkthierarchie (Retail)** im Arbeitsbereich **Kategorie und Produktverwaltung** und beachten die erweiterte Struktur der Seite **Produktkategorie (Retail)**.

![Kategorie- und Produktverwaltungs-Areitsbereich](media/LaunchRetailProductHierarchy.png)

In älteren Versionen wurden Produktattribute in **Grundeigenschaften** und P**roduktattribute Einzelhandel**, basierend auf dem Bereich der Anwendbarkeit aufgeteilt. **Einzelhandelsprodukteigenschaften** sind nach Bereich *global* der Anwendbarkeit, was bedeutet, dass für eine gegebene **Produkteigenschaft Einzelhandel** der gleiche Wert für alle juristischen Personen verwendet wird. **Grundprodukteigenschaften** sind *juristische Personen spezifisch*. Das bedeutet, dass eine gegebene **Grund-Produkteigenschaft** in den juristischen Personen verschieden sein kann, basierend auf den einzelne geschäftlichen Anforderungen.

Mithilfe dieser Erweiterungen für Produktattribute in der Produktkategorie Einzelhandel trennen wir weiterhin die Felder, die auf der Grundlage ihrer Anwendbarkeit innerhalb einer Gruppe basieren, um die Details für freigegebene Produkte der Formularstruktur widerzuspiegeln.

![Gruppierung der Felder auf der Grundlage ihres jeweiligen Bereich der Anwendbarkeit](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

Sie können zwischen dem Verwalten bestimmter Eigenschaften der Entität für alle juristischen Personen und dem Verwalten für eine bestimmte juristische Person wechseln. Wählen Sie einfach **Für alle juristischen Personen anzeigen/bearbeiten** oder **Für eine bestimmte juristische Person anzeigen/bearbeiten** aus.

![Toggle-Ansicht zwischen einer Person und allen juristischen Personen](media/ToggleBackToEditForSpecificLegalEntity.PNG)

![Toggle-Ansicht zwischen einer Person und allen juristischen Personen](media/ToggleToEditForAllLegalEntities.PNG)  

Verglichen zu älteren Versionen können in der neuen Produktkategorie-Struktur ein Verkaufsmanager Standardwerte für einen zusätzlichen Satz Produktattribute für eine einzelne Kategorien auch definieren. Zum Zeitpunkt der Produkterstellung werden diese Standardprodukteigenschaftswerte durch ein Produkt, basierend auf deren Zuordnung zu einer bestimmten Kategorie in der Produkthierarchie (Einzelhandel) übernommen. Verkaufmanager können diese übernommenen Produktattribute für die einzelnen Produkte ändern, um einzelnen geschäftlichen Bedarf abzudecken.

## <a name="select-properties-to-update-products-from-the-retail-product-category-form"></a>Wählen Eigenschaften aus, um Produkte im Formular Produktkategorie (Einzelhandel) zu aktualisieren 
 
Sie können diese neue erweiterte Struktur für Produktattribute verwenden, um auszuwählen, welche aktualisierten Produktattribute für die zugehörigen Produkte aktualisiert werden müssen. 

![Neue erweiterte Ansicht von Aktualisierungsprodukten](media/NewUpdateProductsEnhancedView.PNG) 

Verkaufmanager können diese übernommenen Produktattribute für die einzelnen Produkte ändern, um einzelnen geschäftlichen Bedarf abzudecken.


