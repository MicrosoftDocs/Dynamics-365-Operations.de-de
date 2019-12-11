---
title: Erweitern einer Produktseite
description: In diesem Thema wird beschrieben, wie eine Produktseite in Microsoft Dynamics 365 Commerce ergänzt wird.
author: psimolin
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ef9e65b2027a41ca152afaf20ac2fb9a69cd9b96
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698141"
---
# <a name="enrich-a-product-page"></a>Erweitern einer Produktseite

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

In diesem Thema wird beschrieben, wie eine Produktseite in Microsoft Dynamics 365 Commerce ergänzt wird.

## <a name="overview"></a>Übersicht

Standardmäßig verwendet Ihr Standort eine generische Seite, um Produktdaten anzuzeigen. Diese Seite enthält die grundlegenden Informationen zu Produktpreisen und Steuerelementen, die erforderlich sind, um es zu verkaufen. Sie können jedoch die Informationen ergänzen, die über Retail Server kommen mit zusätzlichem Text oder Bildern für ein bestimmtes Produkt. Dieser Vorgang wird als Anreicherung der Produktseite bezeichnet.

In vielen Fällen möchten Sie bestimmten zusätzlichen Inhalt für Ihre Produkte verwenden. Wenn Sie zu **Einzelhandel** gehen im Erstellungstool sehen Sie eine Liste von Produkten vom Kanal, der dem Standort zugeordnet ist. In dieser Liste zeigen die Spalten **Angereichert** an, ob die Produktseite für ein Produkt angereichert wurde. Wenn ein Häkchen in der Spalte angezeigt wird, liegt eine angereicherte Produktseite für das Produkt vor. Wenn kein Häkchen angezeigt wird, werden die Standardproduktseite und -Inhalt für das Produkt verwendet. Sie können in der Vorschau angereicherte und nicht angereicherte Produktseiten anzeigen, wenn ein Produktname in der Liste ausgewählt ist.

## <a name="enrich-a-product-page"></a>Erweitern einer Produktseite

Um ein Produktseite anzureichern, führen Sie die folgenden Schritte aus.

1. Wählen Sie unter **Sites** **Fabrikam** (oder den Namen Ihrer Site) aus.
1. Wählen Sie im linken Navigationsbereich **Produkte** aus.
1. Wählen Sie ein beliebiges Produkt aus, das keine angereicherte Produktseite hat.
1. Klicken Sie im Aktivitätsbereich auf **Produktseite anreichern**.
1. Wählen Sie **PDP-Vorlage** und dann **OK** aus.
1. In der Seitengliederungsstruktur im Feld links, erweitern Sie den **Haupt-** Slot.
1. Wählen Sie die Ellipsen-Schaltfläche (**...**) für den **Haupt-** Slot und wählen Sie **Modul hinzufügen**.
1. Wählen Sie **Container 2** und dann **OK** aus.
1. Wählen Sie die Ellipsen-Schaltfläche für den **Container 2** und wählen Sie dann **Modul hinzufügen**.
1. Wählen Sie **Funktion** und dann **OK** aus.
1. Im Eigenschaftenbereich auf der rechten Seite, im Feld **Rich-Text** geben Sie die aktualisierte Beschreibung des Produkts ein.
1. Geben Sie im Feld **Kopf** eine Überschrift ein und wählen dann **OK** aus.
1. Wählen Sie **Speichern** und dann **Hochladen** aus.
1. Geben Sie im Feld **Kommentare** **Angereichertes Produkt** ein und wählen Sie dann **OK** aus.
1. Wählen Sie **Vorschau** aus, um die aktualisierte Produkteite in der Vorschau anzuzeigen. Wenn Sie fertig sind, schließen Sie die Vorschauregisterkarte, um zum Erstellungstool zurückzukehren.
1. Wählen Sie **Veröffentlichen** aus.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Bestehende Seite einer Website ändern](modify-existing-page.md)

[Neue Seite hinzufügen](add-new-page.md)

[Auswählen von Seitenlayouts](select-page-layouts.md)

[Verwalten von SEO-Metadaten](manage-seo-metadata.md)

[Speichern, Vorschau und Veröffentlichung einer Seite](save-preview-publish-page.md)

[Füllen einer Kategorie-Landingpage](enrich-category-page.md)
