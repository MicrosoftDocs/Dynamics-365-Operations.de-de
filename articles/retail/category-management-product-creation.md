---
title: Verwalten von Produktkategorien (Retail) und Produkten
description: In diesem Thema wird beschrieben, wie Verkaufmanager Produktkategorien (Retail) verwenden können, um Beziehungen zwischen der Produkthierarchie (Retail) und freigegebenen Produktdetails zu verwalten.
author: ashishmsft
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: ''
ms.assetid: c7ed2ba5-87c6-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 27870fe6172479b891b885d9e84ca10b250e3399
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2019
ms.locfileid: "2019506"
---
# <a name="manage-retail-product-categories-and-products"></a>Verwalten von Einzelhandelsproduktkategorien und ‑produkten

[!include [banner](./includes/banner.md)]

Dieses Thema beschreibt eine erweiterte Art, Produktkategorien und Produkte in Dynamics 365 Retail zu verwalten. Mit diesen Erweiterungen können Verkaufsmanager eine Struktur von Produkteigenschaften anzeigen, die von der Produkthierarchie und freigegebenen Produktdetails geteilt werden.

Um mehr darüber zu erfahren, wie Produktkategorien im Arbeitsbereich **Kategorie und Produktverwaltung** verwaltet werden, wählen Sie die Kachel **Produkthierarchie (Retail)** aus.

Beachten Sie die erweiterte Struktur auf der Seite **Produkthierarchie (Retail)**, die angezeigt wird. In älteren Versionen von Retail wurden Produkteigenschaften in *Produktgrundeigenschaften* und *Produkteigenschaften (Retail)*, basierend auf dem Umfang ihrer Anwendbarkeit aufgeteilt. Produkteigenschaften (Retail) sind *global* in ihrem Umfang der Anwendbarkeit. Das bedeutet, dass für eine gegebene Produkteigenschaft derselbe Wert für alle juristischen Personen verwendet wird. Produktgrundeigenschaften sind jedoch jeweils *für juristische Personen spezifisch*. Das bedeutet, dass für eine gegebene Produktgrundeigenschaft der Wert je nach juristischer Person verschieden sein kann, basierend auf den einzelne geschäftlichen Anforderungen jeder juristischen Person.

In der erweiterten Produktkategoriestruktur werden Produkteigenschaften logisch getrennt, basierend auf ihrer Anwendbarkeit in einer Gruppe, um die Struktur der Formularstruktur für freigegebene Produktdetails widerzuspiegeln.

![Felder, die auf Grundlage des Umfangs der Anwendbarkeit der Eigenschaften gruppiert sind](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

Sie können zwischen dem Verwalten von Eigenschaften, die für juristische Personen spezifisch sind, über alle juristischen Personen hinweg und dem Verwalten davon für eine bestimmte juristische Person wechseln.

Um Eigenschaften für alle juristischen Personen zu verwaltet, wählen Sie **Ansicht für alle juristischen Personen** (oder **Bearbeiten für alle juristischen Personen**) aus.

![Anzeigen/Bearbeiten für alle juristische Personen](media/ToggleBackToEditForSpecificLegalEntity.PNG)

Um Eigenschaften für eine bestimmte juristische Person zu verwalten, wählen Sie **Ansicht für eine bestimmte juristische Person** (oder **Bearbeiten für eine bestimmte juristische Person**) aus.

![Anzeigen/Bearbeiten für eine bestimmte juristische Person](media/ToggleToEditForAllLegalEntities.PNG)

In der erweiterten Produktkategoriestruktur kann darüber hinaus ein Verkaufsmanager jetzt Standardwerte für einen zusätzlichen Satz Produktattribute auf der Ebene einer einzelnen Kategorie definieren. Wenn dann die Produkte erstellt werden, erben sie die Standardwerte für ihre Produkteigenschaften basierend auf der Zuordnung dieser Eigenschaften mit einer einzelnen Kategorie in der Produkthierarchie. Diese geerbten Produkteigenschaften können auch für jedes Produkt geändert werden, um einzelnen geschäftlichen Bedarf abzudecken.

## <a name="selecting-properties-to-update-products-on-the-retail-product-hierarchy-page"></a>Auswählen von Eigenschaften zum Aktualisieren von Produkten auf der Seite „Produkthierarchie (Retail)”.

Sie können die neue erweiterte Struktur für Produkteigenschaften verwenden, um aktualisierte Produkteigenschaften auszuwählen, die an die zugeordneten Produkte mit Push übertragen werden müssen. Wählen Sie auf der Seite **Produkthierarchie (Retail)** im Aktivitätsbereich die Option **Kategorie** aus, und wählen Sie dann **Produkte aktualisieren**, um das Dialogfeld **Produkte aktualisieren** zu öffnen.

![Das Produktedialogfeld aktualisieren](media/NewUpdateProductsEnhancedView.PNG)
