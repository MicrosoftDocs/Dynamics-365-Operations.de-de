---
title: Verwalten von Produktkategorien (Retail) und Produkten
description: "In diesem Thema wird beschrieben, wie Verkaufmanager Produktkategorien (Retail) verwenden können, um Beziehungen zwischen der Produkthierarchie (Retail) und freigegebenen Produktdetails zu verwalten."
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
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 19c972164474c972aab642c3cccc67cf396a6cb2
ms.contentlocale: de-de
ms.lasthandoff: 08/08/2018

---

# <a name="manage-retail-product-categories-and-products"></a>Verwalten von Produktkategorien (Retail) und Produkten

[!include [banner](./includes/banner.md)]

Dieses Thema beschreibt eine erweiterte Art, Produktkategorien (Retail) und Produkte in Microsoft Dynamics 365 for Retail zu verwalten. Mit diesen Erweiterungen können Verkaufsmanager eine Struktur von Produkteigenschaften anzeigen, die von der Produkthierarchie (Retail) und freigegebenen Produktdetails geteilt werden.

Um mehr darüber zu erfahren, wie Produktkategorien (Retail) im Arbeitsbereich **Kategorie und Produktverwaltung** verwaltet werden, wählen Sie die Kachel **Produkthierarchie (Retail)** aus.

Beachten Sie die erweiterte Struktur auf der Seite **Produkthierarchie (Retail)**, die angezeigt wird. In älteren Versionen von Retail wurden Produkteigenschaften in *Produktgrundeigenschaften* und *Produkteigenschaften (Retail)*, basierend auf dem Umfang ihrer Anwendbarkeit aufgeteilt. Produkteigenschaften (Retail) sind *global* in ihrem Umfang der Anwendbarkeit. Das bedeutet, dass für eine gegebene Produkteigenschaft (Retail) derselbe Wert für alle juristischen Personen verwendet wird. Produktgrundeigenschaften sind jedoch jeweils *für juristische Personen spezifisch*. Das bedeutet, dass für eine gegebene Produktgrundeigenschaft der Wert je nach juristischer Person verschieden sein kann, basierend auf den einzelne geschäftlichen Anforderungen jeder juristischen Person.

In der erweiterten Produktkategoriestruktur (Retail) werden Produkteigenschaften logisch getrennt, basierend auf ihrer Anwendbarkeit in einer Gruppe, um die Struktur der Formularstruktur für freigegebene Produktdetails widerzuspiegeln.

![Felder, die auf Grundlage des Umfangs der Anwendbarkeit der Eigenschaften gruppiert sind](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

Sie können zwischen dem Verwalten von Eigenschaften, die für juristische Personen spezifisch sind, über alle juristischen Personen hinweg und dem Verwalten davon für eine bestimmte juristische Person wechseln.

Um Eigenschaften für alle juristischen Personen zu verwaltet, wählen Sie **Ansicht für alle juristischen Personen** (oder **Bearbeiten für alle juristischen Personen**) aus.

![Anzeigen/Bearbeiten für alle juristische Personen](media/ToggleBackToEditForSpecificLegalEntity.PNG)

Um Eigenschaften für eine bestimmte juristische Person zu verwalten, wählen Sie **Ansicht für eine bestimmte juristische Person** (oder **Bearbeiten für eine bestimmte juristische Person**) aus.

![Anzeigen/Bearbeiten für eine bestimmte juristische Person](media/ToggleToEditForAllLegalEntities.PNG)

In der erweiterten Produktkategoriestruktur kann darüber hinaus ein Verkaufsmanager jetzt Standardwerte für einen zusätzlichen Satz Produktattribute auf der Ebene einer einzelnen Kategorie definieren. Wenn dann die Produkt erstellt werden, erben sie die Standardwerte für ihre Produkteigenschaften basierend auf der Zuordnung dieser Eigenschaften mit einer einzelnen Kategorie in der Produkthierarchie (Retail). Diese geerbten Produkteigenschaften können auch für jedes Produkt geändert werden, um einzelnen geschäftlichen Bedarf abzudecken.

## <a name="selecting-properties-to-update-products-on-the-retail-product-hierarchy-page"></a>Auswählen von Eigenschaften zum Aktualisieren von Produkten auf der Seite „Produkthierarchie (Retail)”.

Sie können die neue erweiterte Struktur für Produkteigenschaften verwenden, um aktualisierte Produkteigenschaften auszuwählen, die an die zugeordneten Produkte mit Push übertragen werden müssen. Wählen Sie auf der Seite **Produkthierarchie (Retail)** im Aktivitätsbereich die Option **Kategorie** aus, und wählen Sie dann **Produkte aktualisieren**, um das Dialogfeld **Produkte aktualisieren** zu öffnen.

![Das Produktedialogfeld aktualisieren](media/NewUpdateProductsEnhancedView.PNG)

