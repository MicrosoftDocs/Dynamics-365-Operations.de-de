---
title: Produktsammelmodule
description: Dieses Thema bietet eine Übersicht über Produktsammelmodule in Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 10/01/2019
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
ms.openlocfilehash: 44f78b55b8e67b7358be75aa63c40a0147507e26
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785466"
---
# <a name="product-collection-modules"></a>Produktsammelmodule  

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dieses Thema bietet eine Übersicht über Produktsammelmodule in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Übersicht

Die Produkterfassung ist ein wichtiges Tool, mit dem Einzelhändler ihre Kunden auf einer E-Commerce-Website ansprechen können. Produktsammelmodule helfen Einzelhändlern dabei, überzeugende Einkaufserlebnisse zu schaffen, indem sie eine intuitive visuelle Oberfläche bereitstellen, mit der Produktsammlungen schnell erstellt werden können.

Produktsammelmodule stellen physische Produkte und Dienstleistungen auf der Website dar. Ein Produktsammelmodul ist in der Regel mit einer Detailseite verknüpft, auf der Kunden ein Produkt oder eine Dienstleistung erwerben oder mehr darüber erfahren können. 

Die Quelle für Produktsammlungen kann eine der drei folgenden Listentypen sein:

- Redaktionelle Listen von Produkten, die manuell in Dynamics 365 Retail als zugehörige Produkte für ein Produkt definiert wurden, oder Produktlisten
- Algorithmische Listen, z. B. Listen mit neuen, meistverkauften oder beliebten Produkten
- Empfehlungslisten, die auf maschinellem Lernen basieren

Die folgende Abbildung zeigt die verschiedenen Arten von Produktsammlungen, die auf einer E-Commerce-Site verwendet werden.

![Beispiel für die verschiedenen Arten von Produktsammlungen auf einer E-Commerce-Website](./media/ProductCollectionsAcrossTheSiteUseProductPlacement.png)

> [!NOTE]
> Verwenden Sie immer Produktsammelmodule, um eine Gruppe von Produkten eines ähnlichen Typs oder Themas anzuzeigen.

## <a name="product-collection-modules-and-types"></a>Produktsammelmodule und -typen

In der folgenden Tabelle werden verschiedene Arten von Produktsammelmodulen in Dynamics 365 Commerce beschrieben.

| Produktsammelmodul  | Typ | Beschreibung |
|----------------------------|------|-------------|
| Durchsuchte Kategorie            | Redaktion | Diese Art von Produktsammelmodulen verwendet die Navigationskategoriehierarchie, die der Einzelhändler für einen Retail Channel erstellt hat, um einen Suchlauf für Produkte anzuzeigen, die in einer bestimmten Websitekategorie angeboten werden. |
| Suchergebnisse             | Suchabfrage | Diese Art eines Produktsammelmoduls zeigt eine Liste der Produkte an, die der vom Kunden eingegebenen Suchanfrage am besten entsprechen. |
| Zugehörige Produkte           | Redaktion | Diese Art eines Produktsammelmoduls zeigt eine Liste der Produkte an, die ein Manager Verkaufsförderung für den vom Autor ausgewählten Relationstyp als verwandte Produkte im Einzelhandel konfiguriert hat. |
| Kuratierte Produktlisten      | Redaktion | Diese Art eines Produktsammelmoduls zeigt benutzerdefinierte Listen an, die Merchandiser und Redakteure im Einzelhandel erstellt haben. |
| Neue                        | Algorithmisch | Diese Art eines Produktsammelmoduls zeigt eine Liste der neuesten Produkte an, die nach Kanälen und Katalogen sortiert wurden. |
| Bestseller               | Algorithmisch | Diese Art eines Produktsammelmoduls zeigt eine Liste von Produkten an, die nach der höchsten Anzahl von Verkäufen geordnet sind. |
| Populär                   | Algorithmisch | Diese Art eines Produktsammelmoduls zeigt eine Liste der leistungsstärksten Produkte für einen bestimmten Zeitraum an. |
| Wird häufig zusammen gekauft | Künstliche Intelligenz/Maschinelles Lernen | Diese Art eines Produktsammelmoduls verwendet maschinelles Lernen, um Kaufmuster von Verbrauchern zu analysieren und verwandte Artikel zu empfehlen, die häufig zusammen mit einem bestimmten Produkt gekauft werden. |
| Personen gefällt auch           | Künstliche Intelligenz/Maschinelles Lernen | Diese Art eines Produktsammelmoduls verwendet maschinelles Lernen, um Kaufmuster von Verbrauchern zu analysieren und Artikel zu empfehlen, die sich auf ein bestimmtes Produkt beziehen. |

## <a name="add-a-product-collection-module-to-a-category-page"></a>Hinzufügen eines Produktsammelmoduls zu einer Kategorieseite

Befolgen Sie diese Schritte, um ein Produktsammelmodul zu einer Kategorieseite hinzuzufügen.

1. Navigieren Sie in Dynamics 365 Commerce zu Ihrer Website und erstellen Sie eine Seite, die dieselben Vorlagen wie Ihre Standardkategorieseite verwendet.
1. Wählen Sie im Seitenüberblick den Slot **Unterfußzeile**, dann die Ellipsen-Schaltfläche (**...**) und anschließend **Modul hinzufügen** aus.
1. Wählen Sie im Dialogfeld **Modul hinzufügen** **Container** und dann **OK** aus.
1. Wählen Sie im Containermodul die Ellipsen-Schaltfläche und dann **Modul hinzufügen** aus.
1. Wählen Sie im Dialogfeld **Modul hinzufügen** **Produktsammlung** und dann **OK** aus.
1. Konfigurieren Sie die Einstellungen, indem Sie eine geeignete Datenquelle und Eingaben für die Produktsammlung auswählen.
1. Wählen Sie im Eigenschaftenbereich für das Produktsammelmodul **Produktliste hinzufügen** aus.
1. Wählen Sie im Dialogfeld **Produktlistenkonfiguration auswählen** den Typ der Liste aus, geben Sie die Anzahl der Artikel ein und wählen Sie andere Optionen aus, die für den Listentyp verfügbar sind. Weitere Informationen zu Listentypen finden Sie in der folgenden Tabelle. 
1. Wählen Sie **OK**.
1. Speichern Sie die Seite und laden Sie es hoch.

In der folgenden Tabelle sind die Listentypen aufgeführt, die im Dialogfeld **Produktlistenkonfiguration auswählen** verfügbar sind.
   
| Typ                       | Beschreibung | Allgemeine Methode | Kontext, der aus dem Seitenkontext abgeleitet werden kann | Kontext, mit dem der Autor den Seitenkontext überschreiben kann |
|----------------------------|-------------|------------------|-------------------------------------|-----------------------------------------------|
| Produkte nach Kategorie       | Eine Liste von Produkten, die zu einer bestimmten Kategorie gehören. Diese Kategorie wird entweder über den Seitenkontext oder über dem vom Autor bereitgestellten Kontext bestimmt. | Erweitern von Kategorieseiten, Startseiten, Auscheck- und Einkaufskorbseiten sowie Produktseiten | Kategorie | Vom Autor festgelegte Kategorie |
| Zugehörige Produkte           | Eine Liste der Produkte, die ein Manager Verkaufsförderung als verwandte Produkte im Einzelhandel für den Relationstyp konfiguriert hat. | Produktseiten, Auscheck- und Einkaufskorbseiten, Wunschlistenseite und Debitorenkontoseite | Produkt, Relationstyp (obligatorisch)  | Produkt, Relationstyp |
| Zusammengestellt                    | Eine benutzerdefinierte Liste, die Merchandiser und Redakteure im Einzelhandel erstellt haben. | Erweitern von Kategorieseiten, Startseiten, Auscheck- und Einkaufskorbseiten sowie Produktseiten | Nicht zutreffend | Listenauswahl |
| Algorithmisch                | <ul><li>**Neu** – Eine Liste der neuesten Produkte, die nach Kanälen und Katalogen sortiert wurden.</li><li>**Bestseller** – Eine Liste der Produkte, die nach der höchsten Anzahl an Verkäufen sortiert sind.</li><li>**Populär** – Eine Liste der leistungsstärksten Produkte für einen bestimmten Zeitraum.</li></ul> | Startseite, Kategorieseite und Bezahl- und Warenkorbseiten erweitern | Kategorie | Vom Autor festgelegte Kategorie |
| Wird häufig zusammen gekauft | Eine Liste, die maschinelles Lernen verwendet, um Kaufmuster von Verbrauchern zu analysieren und verwandte Artikel zu empfehlen, die häufig zusammen mit einem bestimmten Produkt gekauft werden. | Produktseiten und Bezahl- und Warenkorbseiten | Produkt, Einkaufskorb | Einkaufskorb einbeziehen |
| Personen gefällt auch           | Eine Liste, die maschinelles Lernen verwendet, um Kaufmuster von Verbrauchern zu analysieren und verwandte Artikel zu empfehlen, die sich auf ein bestimmtes Produkt beziehen. | Produktseiten und Bezahl- und Warenkorbseiten | Produkt, Einkaufskorb | Nicht zutreffend |

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Starterkit-Überblick](starter-kit-overview.md)

[Karussellmodul](add-carousel.md)

[Umfangreiches Inhaltsblockmodul](add-content-rich-block.md)

[Inhaltsplatzierungsmodul](add-content-placement-modules.md)

[Containermodul](add-container-module.md)

[Kauffeldmodul](add-buy-box.md)

