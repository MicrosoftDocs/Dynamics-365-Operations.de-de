---
title: Produktkategorieverwaltung und Erstellung
description: "In diesem Thema werden die Erweiterungen beschrieben, die für die Verwaltung von Einzelhandels-Produktkategorien gemacht wurde. Mit diesen Erweiterungen können Verkaufmanager eine Wechselbeziehung zwischen Produkthierarchie (Einzelhandel) und freigegebenen Produktdetails haben."
author: ashishmsft
manager: AnnBe
ms.date: 09/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailCategoryAndProductWorkspace, RetailCategory
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 98250062892e0c5f665616dc3944181a3ff8599a
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="product-category-management-and-creation"></a>Produktkategorieverwaltung und Erstellung

[!include[banner](./includes/banner.md)]

Mit den Erweiterungen, die für die Verwaltungserfahrung Produktkategorien für Einzelhandel erstellt wurden, können Verkaufmanager eine Wechselbeziehung zwischen Produkthierarchie (Einzelhandel) und freigegebenen Produktdetails haben. Klicken Sie zum Anzeigen dieser Erweiterungen auf den Arbeitsbereich **Kategorie und Produktverwaltung.** und wählen Sie **Produkthierarchie (Einzelhandel)** um die Seite  **Neue Struktur die Produktkategorie (Einzelhandel)** zu öffnen. 

In älteren Versionen wurden Produktattribute in Grundeigenschaften und Produktattribute Einzelhandel, basierend auf dem Bereich der Anwendbarkeit aufgeteilt. Eigenschaften für Einzelhandelsprodukte waren *global*. Das bedeutet, dass für eine gegebene Produkteigenschaft derselbe Wert für alle juristischen Personen verwendet wird. Grundprodukteigenschaften waren *entitätsspezifisch*. Das bedeutet, dass eine gegebene Produkteigenschaft in den juristischen Personen verschieden sein kann, basierend auf den einzelne geschäftlichen Anforderungen.

Mithilfe dieser Erweiterungen für Produktattribute in der Produktkategorie Einzelhandel trennen wir weiterhin die Felder, die auf der Grundlage ihrer Anwendbarkeit innerhalb einer Gruppe basieren, um die Details für freigegebene Produkte der Formularstruktur widerzuspiegeln.

Sie können zwischen dem Verwalten bestimmter Eigenschaften der Entität für alle juristischen Personen und dem Verwalten für eine bestimmte juristische Person wechseln. Wählen Sie einfach **Für alle juristischen Personen anzeigen/bearbeiten** oder **Für eine bestimmte juristische Person anzeigen/bearbeiten** aus.

Verkaufmanager können Standardwerte für einen zusätzlichen Satz Produktattribute auf der Ebene einer einzelnen Kategorie definieren. Diese Eigenschaftswerte werden durch ein Produkt, basierend auf deren Zuordnung zu einer Kategorie zum Zeitpunkt der Produkterstellung übernommen.

## <a name="select-properties-to-update-products-from-the-retail-product-category-form"></a>Wählen Eigenschaften aus, um Produkte im Formular Produktkategorie (Einzelhandel) zu aktualisieren

Sie können logische Einheiten verwenden, um auszuwählen, welche Produktattribute für die zugehörigen Produkte aktualisiert werden sollen.

Verkaufmanager können diese übernommenen Produktattribute für die einzelnen Produkte ändern, um einzelnen geschäftlichen Bedarf abzudecken.

