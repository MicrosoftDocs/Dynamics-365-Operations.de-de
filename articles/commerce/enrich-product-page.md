---
title: Erweitern einer Produktseite
description: In diesem Artikel wird beschrieben, wie eine Produktseite in Microsoft Dynamics 365 Commerce ergänzt wird.
author: josaw1
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: f01dcc2518fe861339b4984522582ed3de7aa6ad
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282133"
---
# <a name="enrich-a-product-page"></a>Erweitern einer Produktseite

[!include [banner](includes/banner.md)]

In diesem Artikel wird beschrieben, wie eine Produktseite in Microsoft Dynamics 365 Commerce ergänzt wird.

Standardmäßig verwendet Ihr Standort eine generische Seite, um Produktdaten anzuzeigen. Diese Seite enthält die grundlegenden Informationen zu Produktpreisen und Steuerelementen, die erforderlich sind, um es zu verkaufen. Sie können jedoch die Informationen, die über die Commerce-Skalierungseinheit kommen, durch zusätzliche Bilder oder Texte für ein bestimmtes Produkt ergänzen. Dieser Vorgang wird als Anreicherung der Produktseite bezeichnet.

In vielen Fällen möchten Sie bestimmten zusätzlichen Inhalt für Ihre Produkte verwenden. Wenn Sie zu **Einzelhandel und Handel** im Erstellungstool wechseln, sehen Sie eine Liste von Produkten von dem Kanal, der der Site zugeordnet ist. In dieser Liste zeigen die Spalten **Angereichert** an, ob die Produktseite für ein Produkt angereichert wurde. Wenn ein Häkchen in der Spalte angezeigt wird, liegt eine angereicherte Produktseite für das Produkt vor. Wenn kein Häkchen angezeigt wird, werden die Standardproduktseite und -Inhalt für das Produkt verwendet. Sie können in der Vorschau angereicherte und nicht angereicherte Produktseiten anzeigen, wenn ein Produktname in der Liste ausgewählt ist.

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
1. Wählen Sie **Speichern** und dann **Bearbeiten beenden** aus.
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

[Überprüfen der Zugänglichkeit des Seiteninhalts](verify-accessibility.md)

[Dynamische E-Commerce-Seiten basierend auf URL-Parametern erstellen](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
