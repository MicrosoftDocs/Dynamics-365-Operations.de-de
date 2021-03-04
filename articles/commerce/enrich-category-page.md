---
title: Füllen einer Kategorie-Landingpage
description: In diesem Thema wird die Anreicherung der Kategorieseiten in Dynamics 365 Commerce abgedeckt.
author: v-chgri
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ca31ec7d2eee7d2b0c863506338341a870ff07ee
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4412565"
---
# <a name="enrich-a-category-landing-page"></a>Füllen einer Kategorie-Landingpage


[!include [banner](includes/banner.md)]

In diesem Thema wird die Anreicherung der Kategorieseiten in Dynamics 365 Commerce abgedeckt.

## <a name="overview"></a>Übersicht

Handel enthält eine Standardkategorieangebotsseite, die verwendet wird, wenn Kategoriedaten angezeigt werden. Eine obligatorische Standardkategorieseite enthält Elemente, wie Verfeinerungen, kategorisierte Produktplatzierung und sortiert Optionen, enthält eine auserlesene Zusammenfassung und Paginierungskontrollen. 

Allerdings anstatt die Standardkategorieseite zu verwenden, sollten Sie eine angereicherte Kategorieangebotsseite verwenden, die mehr Inhalt und mehr bestimmte Projekte aufweist. Eine typische Bereicherung ist möglicherweise das Hinzufügen von kategoriespezifischen Marketings-Inhalt der Kategorieseite hinzuzufügen. Dieser Inhalt kann überkreuzte Kategorieproduktplatzierungen enthalten für Cross-Sell-Zwecke, redaktionelle Listen, Bilder, Videos und anderen Text. Sie können entweder die Standardkategorieseite ändern oder eine andere Kategorieseite für eine bestimmte Kategorie definieren.

![Angereicherte Kategorie-Startseite](./media/CategoryLandingPages.png)

Im Commerce Site Builder umfasst die Seite **Produkte** eine Liste der Kategorien vom Kanal, die dem Standort zugeordnet werden. Wenn der Status **Angereichert** für eine Kategorieseite aktiviert ist, ist diese Kategorieseite angereichert worden. Andernfalls werden die Standardkategorieseite und der Inhalt für die Kategorie verwendet. Sie können in der Vorschau angereicherte und nicht angereicherte Kategorieseiten für eine Kategorie anzeigen, wenn ein Kategoriename in der Liste ausgewählt ist.

Um eine Kategorieseite anzureichern, gehen Sie folgendermaßen vor.

1. Auf der Seite **Produkte** wählen Sie den Namen der Kategorie, für die Sie die Kategorieseite anreichern möchten. Die Standardkategorieseite für die ausgewählte Kategorie ist im Seitenaufbereitungsprogramm geöffnet.
2. Wählen Sie **Kategorieseite anreichern** aus.
3. Wählen Sie eine Vorlage für die angereicherte Kategorieseite aus. Wenn Sie nur geringfügige Änderungen vornehmen, können Sie die Standardkategorieseite auswählen. Alternativ können Sie eine bestimmte Kategorieseitenvorlage auswählen. Wenn Sie die Vorlage auswählen, ist das Seitenaufbereitungsprogramm geöffnet, und die ausgewählte Vorlage wird verwendet, um eine neue Kategorieseite für die ausgewählte Kategorie zu erstellen. Die Seite wird von Ihnen ausgecheckt und Sie können nun Ihre Änderungen vornehmen.

> [!NOTE]
> Module, die Kategoriespezifikationsdaten verwenden, die Daten aus der ausgewählten Kategorie nutzen. Die Einstellungen der Vorlage, die Sie auswählen, bestimmt die Änderungen, die Sie vornehmen können.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Bestehende Seite einer Website ändern](modify-existing-page.md)

[Neue Seite hinzufügen](add-new-page.md)

[Auswählen von Seitenlayouts](select-page-layouts.md)

[Verwalten von SEO-Metadaten](manage-seo-metadata.md)

[Speichern, Vorschau und Veröffentlichung einer Seite](save-preview-publish-page.md)

[Erweitern einer Produktseite](enrich-product-page.md)

[Überprüfen der Zugänglichkeit des Seiteninhalts](verify-accessibility.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]