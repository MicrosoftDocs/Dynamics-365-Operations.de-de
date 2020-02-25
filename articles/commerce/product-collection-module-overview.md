---
title: Produktsammelmodule
description: Dieses Thema bietet eine Übersicht über Produktsammelmodule in Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 01/07/2020
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
ms.openlocfilehash: 069fa1cb6acad4b8d6618cebb754cbc0892ca9cf
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025947"
---
# <a name="product-collection-modules"></a>Produktsammelmodule


[!include [banner](includes/banner.md)]

Dieses Thema bietet eine Übersicht über Produktsammelmodule in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Übersicht

Die Produkterfassung ist ein wichtiges Tool, mit dem Einzelhändler ihre Kunden auf einer E-Commerce-Website ansprechen können. Produktsammelmodule helfen Einzelhändlern dabei, überzeugende Einkaufserlebnisse zu schaffen, indem sie eine intuitive visuelle Oberfläche bereitstellen, mit der Produktsammlungen schnell erstellt werden können.

Produktsammelmodule stellen physische Produkte und Dienstleistungen auf der Website dar. Ein Produktsammelmodul ist in der Regel mit einer Detailseite verknüpft, auf der Kunden ein Produkt oder eine Dienstleistung erwerben oder mehr darüber erfahren können. 

Die Quelle für Produktsammlungen kann eine der vier folgenden Listentypen sein:

- Redaktionelle Listen von Produkten, die manuell in Dynamics 365 Commerce als zugehörige Produkte für ein Produkt definiert wurden, oder Produktlisten
- Algorithmische Listen, z. B. Listen mit neuen, meistverkauften oder beliebten Produkten
- Empfehlungslisten, die auf maschinellem Lernen basieren
- Personalisierungslisten, die personalisierte Ergebnisse für einen Kunden unterstützen. Kunden müssen auf der E-Commerce-Website angemeldet sein, um personalisierte Ergebnisse zu erhalten. Gastbenutzer sehen keine personalisierten Ergebnisse. Kunden können sich von der Personalisierung abmelden [Kontoverwaltungsseite](account-management.md).

Die folgende Abbildung zeigt die verschiedenen Arten von Produktsammlungen, die auf einer E-Commerce-Site verwendet werden.

![Beispiel für die verschiedenen Arten von Produktsammlungen auf einer E-Commerce-Website](./media/ProductCollectionsAcrossTheSiteUseProductPlacement.png)

> [!NOTE]
> Verwenden Sie immer Produktsammelmodule, um eine Gruppe von Produkten eines ähnlichen Typs anzuzeigen.

## <a name="product-collection-modules-and-types"></a>Produktsammelmodule und -typen

In der folgenden Tabelle werden verschiedene Arten von Produktsammelmodulen in Dynamics 365 Commerce beschrieben.

| Produktsammelmodul  | Typ | Beschreibung |
|----------------------------|------|-------------|
| Kategorie                   | Kategorie | In diesem Modul wird eine Liste der Produkte in einer Kategorie angezeigt, die durch die Navigationskategoriehierarchie definiert ist, die der Einzelhändler für einen Kanal erstellt hat. |
| Zugehörige Produkte           | Redaktion | Diese Art eines Produktsammelmoduls zeigt eine Liste der Produkte an, die ein Manager Verkaufsförderung für den vom Autor ausgewählten Relationstyp als verwandte Produkte in Commerce konfiguriert hat. |
| Suchergebnisse             | Suchabfrage | Diese Art eines Produktsammelmoduls zeigt eine Liste der Produkte an, die der vom Kunden eingegebenen Suchanfrage am besten entsprechen. |
| Kuratierte Produktlisten      | Redaktion | Dieses Modul zeigt eine benutzerdefinierte Liste, die Merchandiser und Redakteure in Commerce erstellt haben. |
| Neue                        | Algorithmisch | Dieses Modul zeigt eine Liste der neuesten Produkte, die nach Kanälen und Katalogen sortiert wurden. Diese Liste kann personalisierte Ergebnisse für einen angemeldeten Benutzer anzeigen, wenn der Site-Autor diese Option auswählt. |
| Bestseller               | Algorithmisch | Dieses Modul zeigt eine Liste der Produkte, die nach der höchsten Anzahl an Verkäufen sortiert sind. Diese Liste kann personalisierte Ergebnisse für einen angemeldeten Benutzer anzeigen, wenn der Site-Autor diese Option auswählt. |
| Populär                   | Algorithmisch | Dieses Modul zeigt eine Liste der leistungsstärksten Produkte für einen bestimmten Zeitraum. Diese Liste kann personalisierte Ergebnisse für einen angemeldeten Benutzer anzeigen, wenn der Site-Autor diese Option auswählt. |
| Wird häufig zusammen gekauft | Künstliche Intelligenz/Maschinelles Lernen | Dieses Modul verwendet maschinelles Lernen, um Kaufmuster von Verbrauchern zu analysieren und verwandte Artikel zu empfehlen, die häufig zusammen mit einem bestimmten Produkt gekauft werden. Diese Liste kann personalisierte Ergebnisse für einen angemeldeten Benutzer anzeigen, wenn der Site-Autor diese Option auswählt. |
| Personen gefällt auch           | Künstliche Intelligenz/Maschinelles Lernen | Dieses Modul verwendet maschinelles Lernen, um Kaufmuster von Verbrauchern zu analysieren und verwandte Artikel zu empfehlen, die sich auf ein bestimmtes Produkt beziehen. Diese Liste kann personalisierte Ergebnisse für einen angemeldeten Benutzer anzeigen, wenn der Site-Autor diese Option auswählt. |
| Entnahmen für Sie              | Künstliche Intelligenz/Maschinelles Lernen | Dieses Modul verwendet maschinelles Lernen, um die Kaufmuster des angemeldeten Benutzers zu analysieren und personalisierte Empfehlungen bereitzustellen, die auf diesen Kaufmustern basieren. Für einen Gastbenutzer wird diese Liste reduziert. |

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

| Typ                       | Beschreibung | Nutzung | Seitenkontext | Spezifischer Kontext | Personalisierung |
|----------------------------|-------------|-------|--------------|------------------|-----------------|
| Produkte nach Kategorie       | Eine Liste von Produkten, die zu einer bestimmten Kategorie gehören. Diese Kategorie wird entweder über den Seitenkontext oder über dem vom Autor bereitgestellten Kontext bestimmt. | Diese Art von Liste kann auf jeder Seite verwendet werden (z. B. einer Homepage, Kategorieseite, Marketing-Seite oder Produktdetailseite \[PDP\]), um eine bestimmte Produktkategorie zu fördern. | Kategorie aus dem Seitenkontext, sofern verfügbar (z. B. eine Kategorieseite) | Der Autor kann eine bestimmte Kategorie als Kontext für die Liste angeben. | Nicht zutreffend |
| Zugehörige Produkte           | Eine Liste der Produkte, die ein Manager Verkaufsförderung als verwandte Produkte in Commerce für den Relationstyp konfiguriert hat. | Diese Art von Liste wird hauptsächlich auf PDPs verwendet, kann jedoch auf jeder Seite verwendet werden, wenn ein übergeordnetes Produkt bereitgestellt wird. | Produkt von der Seite, Beziehungstyp (obligatorisch) | Das Produkt kann im Picker ausgewählt werden und der Beziehungstyp wird verwendet. | Nicht zutreffend |
| Zusammengestellt                    | Eine benutzerdefinierte Liste, die Merchandiser und Redakteure in Commerce erstellt haben. | Erweitern von Kategorieseiten, Startseiten, Auscheck- und Einkaufskorbseiten sowie Produktseiten | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend |
| Algorithmisch                | <ul><li>**Neu** – Eine Liste der neuesten Produkte, die nach Kanälen und Katalogen sortiert wurden.</li><li>**Bestseller** – Eine Liste der Produkte, die nach der höchsten Anzahl an Verkäufen sortiert sind.</li><li>**Populär** – Eine Liste der leistungsstärksten Produkte für einen bestimmten Zeitraum.</li></ul> | Startseite, Kategorieseite und Bezahl- und Warenkorbseiten erweitern | Kategorie aus dem Seitenkontext (z. B. eine Kategorieseite) | Die vom Site-Autor festgelegte Kategorie | Unterstützt |
| Wird häufig zusammen gekauft | Eine Liste, die maschinelles Lernen verwendet, um Kaufmuster von Verbrauchern zu analysieren und verwandte Artikel zu empfehlen, die häufig zusammen mit einem bestimmten Produkt gekauft werden. | Diese Art von Liste gilt nur für die Warenkorbseite. | Einkaufskorb | Nicht zutreffend | Unterstützt |
| Personen gefällt auch           | Eine Liste, die maschinelles Lernen verwendet, um Kaufmuster von Verbrauchern zu analysieren und verwandte Artikel zu empfehlen, die sich auf ein bestimmtes Produkt beziehen. | Diese Art von Liste wird auf PDPs verwendet, um Produkte anzuzeigen, die andere Kunden gekauft haben. | Produktkontext von der Seite | Das vom Site-Autor bereitgestellte Produkt | Unterstützt |
| Entnahmen für Sie              | Eine Liste, die maschinelles Lernen verwendet, um Kundenpräferenzen zu ermitteln. | Diese Art von Liste kann auf jeder Seite verwendet werden. | Nicht zutreffend| Nicht zutreffend | Unterstützt | 

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Starterkit-Übersicht](starter-kit-overview.md)

[Karussellmodul](add-carousel.md)

[Umfangreiches Inhaltsblockmodul](add-content-rich-block.md)

[Containermodul](add-container-module.md)

[Kauffeldmodul](add-buy-box.md)

[Überblick über Produktempfehlungen](product-recommendations.md)
