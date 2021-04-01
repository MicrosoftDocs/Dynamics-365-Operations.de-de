---
title: Empfehlungen für „Produkte mit ähnlicher Beschreibung kaufen“ aktivieren
description: In diesem Thema wird beschrieben, wie Sie Produktempfehlungen für „Produkte mit ähnlicher Beschreibung kaufen“ in Microsoft Dynamics 365 Commerce aktivieren.
author: bsokolov
manager: AnnBe
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: b6b397b1f21e3dfcdb4a2b7fe67ddb541d090a97
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234388"
---
# <a name="enable-shop-similar-description-recommendations"></a>Empfehlungen zu „Artikel mit ähnlicher Beschreibung kaufen“ aktivieren

[!include [banner](includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie Produktempfehlungen für „Produkte mit ähnlicher Beschreibung kaufen“ in Microsoft Dynamics 365 Commerce aktivieren.

Die Empfehlungsfunktion für „Produkte mit ähnlicher Beschreibung kaufen“ in Dynamics 365 Commerce nutzt die künstliche Intelligenz und maschinelles Lernen (KI-ML), um Kunden Empfehlungen für Produkte liefern, deren Beschreibung dem ähnelt, wonach der Kunde sucht. Durch die Bereitstellung von Empfehlungen für „Produkte mit ähnlicher Beschreibung kaufen“ für alle Einzelhandelskanäle in Commerce können Einzelhändler Kunden dabei helfen, leicht zu finden, wonach sie suchen.

Die Funktionalität für Empfehlungen für „Produkte mit ähnlicher Beschreibung kaufen“ verwendet den Produktnamen und die Beschreibung von Startproduktvarianten, um ähnliche Produkte im Produktkatalog eines Einzelhändlers zu finden und zu empfehlen.

Empfehlungen für „Produkte mit ähnlicher Beschreibung kaufen“ sind sowohl in POS‑ als auch in E-Commerce-Umgebungen verfügbar.

## <a name="example-scenarios"></a>Beispielszenarien

Die folgenden Beispielszenarien zeigen die Empfehlungstypen, die die Funktion „Produkte mit Ähnlicher Beschreibung kaufen“ bieten kann:

- Ein Kunde betrachtet eine Hornbrille im Retro-Stil und erhält eine Reihe von Empfehlungen für andere Brillen mit ähnlichem Design im Kontext der Einzelhandelsbranche.
- Ein Kunde verwendet die Empfehlungen „Produkte mit ähnlicher Beschreibung kaufen“, um Kaffeearomen zu entdecken, die einem Aroma ähneln, das er zuvor beim Einzelhändler gekauft hat.

## <a name="set-up-shop-similar-description-recommendations"></a>Empfehlungen für „Produkte mit ähnlicher Beschreibung kaufen“ einrichten

Produktempfehlungen werden nur für Commerce-Benutzer unterstützt, die ihren Speicher zu Azure Data Lake Storage Gen2 migriert haben.

### <a name="prerequisites"></a>Voraussetzungen

Bevor den Kunden Empfehlungen für „Produkte mit ähnlicher Beschreibung kaufen“ angezeigt werden können, müssen Sie die folgenden Voraussetzungen befolgen:

- [Produktempfehlungen aktivieren](enable-product-recommendations.md) in der Commerce-Zentrale.
- Stellen Sie sicher, dass der Medienserver HTTPS-Aufrufe unterstützt.

### <a name="turn-on-the-shop-similar-description-recommendations-feature"></a>Empfehlungsfunktion für „Produkte mit ähnlicher Beschreibung kaufen“ aktivieren

Führen Sie die folgenden Schritte aus, um die Empfehlungsfunktion „Produkte mit ähnlicher Beschreibung kaufen“ in der Commerce-Zentralverwaltung zu aktivieren.

1. Suchen und wählen Sie im Arbeitsbereich **Funktionsverwaltung** in der Liste der verfügbaren Funktionen **Produkte mit ähnlicher Beschreibung kaufen** aus.
1. Aktivieren Sie im rechten Bereich **Aktivieren**.

> [!NOTE]
> Wenn Sie die Funktion aktivieren, beginnt das System mit dem Generieren von Produktempfehlungslisten. Es kann bis zu einem Tag dauern, bis diese Listen online und an den POS-Terminals verfügbar und sichtbar sind.
>
> Wenn Sie die Funktion deaktivieren, sind andere Typen von Produktempfehlungen nicht betroffen. Weitere Informationen zu Produktempfehlungen finden Sie unter [Überblick über Produktempfehlungen](product-recommendations.md).

## <a name="add-a-shop-similar-description-button-to-product-details-pages"></a>Den Produktdetailseiten eine „Produkte mit ähnlicher Beschreibung kaufen“-Schaltfläche hinzufügen

Nachdem Sie die Empfehlungsfunktion „Produkte mit ähnlicher Beschreibung kaufen“ in der Commerce-Zentralverwaltung aktiviert haben, können Sie dem Kauffeld einer beliebigen Produktdetailseite (PDP) eine **Produkte mit ähnlicher Beschreibung kaufen**-Schaltfläche hinzufügen. Ein Kunde, der diese Schaltfläche auswählt, wird zu einer speziellen **Produkte mit ähnlicher Beschreibung kaufen**-Seite weitergeleitet, auf der visuell ähnliche Produkte angezeigt werden. Anschließend kann der Kunde Auswahlen verwenden, um die Produkte weiter zu filtern.

Gehen Sie folgendermaßen vor, um einer PDP eine **Produkte mit ähnlicher Beschreibung kaufen**-Schaltfläche mithilfe des Commerce-Website-Generators hinzuzufügen.

1. Öffnen Sie eine vorhandene Site Builder-Seite, die ein Kauffeld enthält.
1. Wählen Sie im linken Navigationsbereich das Kauffeld aus.
1. Aktivieren Sie im rechten Bereich das Kontrollkästchen **Link für „Produkte mit ähnlicher Beschreibung kaufen“ aktivieren**.
1. Wählen Sie **Speichern** aus.
1. Wählen **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um sie zu veröffentlichen. Nach der Veröffentlichung der Seite enthält die PDP eine **Produkte mit ähnlicher Beschreibung kaufen**-Schaltfläche.

Die folgende Abbildung zeigt das Kontrollkästchen **Link für „Produkte mit ähnlicher Beschreibung kaufen“ aktivieren**-Schaltfläche und die **Produkte mit ähnlicher Beschreibung kaufen**-Schaltfläche auf einer Beispiel-PDP im Site Builder.

![Das Kontrollkästchen „Link für Produkte mit ähnlicher Beschreibung kaufen“ und die Schaltfläche „Produkte mit ähnlicher Beschreibung kaufen“ auf einer Beispiel-PDP im Site Builder aktivieren](./media/ter_site_builder_buybox_button.png)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Überblick über Produktempfehlungen](product-recommendations.md)

[Aktivieren von Azure Data Lake Storage in einer Dynamics 365 Commerce Umgebung](enable-adls-environment.md)

[Produktempfehlungen aktivieren](enable-product-recommendations.md)

[Link „Ähnliche Outfits kaufen“ aktivieren](shop-similar-looks.md)

[Anpassung der Ergebnisse der AI-ML-Empfehlungen](modify-product-recommendation-results.md)

[Manuell kuratierte Empfehlungen erstellen](create-editorial-recommendation-lists.md)

[Produktempfehlungs-FAQs](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]