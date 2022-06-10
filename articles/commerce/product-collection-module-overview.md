---
title: Produktsammelmodule
description: Dieses Thema bietet eine Übersicht über Produktsammelmodule in Microsoft Dynamics 365 Commerce.
author: v-chgri
ms.date: 05/18/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4ff891eef79835fb4a65535ce8152e5b17023b9c
ms.sourcegitcommit: ccb39767bd3430c24f4653c26560bba2cd66553c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/19/2022
ms.locfileid: "8780408"
---
# <a name="product-collection-modules"></a>Produktsammelmodule

[!include [banner](includes/banner.md)]

Dieses Thema bietet eine Übersicht über Produktsammelmodule in Microsoft Dynamics 365 Commerce.

Die Produkterfassung ist ein wichtiges Tool, mit dem Einzelhändler ihre Kunden auf einer E-Commerce-Website ansprechen können. Produktsammelmodule helfen Einzelhändlern dabei, überzeugende Einkaufserlebnisse zu schaffen, indem sie eine intuitive visuelle Oberfläche bereitstellen, mit der Produktsammlungen schnell erstellt werden können.

Produktsammelmodule stellen physische Produkte und Dienstleistungen auf der Website dar. Ein Produktsammelmodul ist in der Regel mit einer Detailseite verknüpft, auf der Kunden ein Produkt oder eine Dienstleistung erwerben oder mehr darüber erfahren können. 

Die Quelle für Produktsammlungen kann eine der vier folgenden Listentypen sein:

- Redaktionelle Listen von Produkten, die manuell in Dynamics 365 Commerce als zugehörige Produkte für ein Produkt definiert wurden, oder Produktlisten
- Algorithmische Listen, z. B. Listen mit neuen, meistverkauften oder beliebten Produkten
- Empfehlungslisten, die auf maschinellem Lernen basieren
- Personalisierungslisten, die personalisierte Ergebnisse für einen Kunden unterstützen. Kunden müssen auf der E-Commerce-Website angemeldet sein, um personalisierte Ergebnisse zu erhalten. Gastbenutzer sehen keine personalisierten Ergebnisse. Kunden können sich von der Personalisierung abmelden [Kontoverwaltungsseite](account-management.md).

Die folgende Abbildung zeigt die verschiedenen Arten von Produktsammlungen, die auf einer E-Commerce-Site verwendet werden.

![Beispiel für die verschiedenen Arten von Produktsammlungen auf einer E-Commerce-Website.](./media/ProductCollectionsAcrossTheSiteUseProductPlacement.png)

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

## <a name="supported-modules"></a>Unterstützte Module 

Das Produktsammlungsmodul unterstützt das [Schnellansichtsmodul](quick-view-module.md), mit dem sich Benutzer Produktinformationen anzeigen lassen und Artikel über eine Produktsammlungsseite dem Warenkorb hinzufügen können.

## <a name="add-a-product-collection-module-to-a-category-page"></a>Hinzufügen eines Produktsammelmoduls zu einer Kategorieseite

Befolgen Sie diese Schritte, um ein Produktsammelmodul zu einer Kategorieseite hinzuzufügen.

1. Wechseln Sie zu **Seiten**, und wählen Sie dann **Neu** aus, um eine neue Seite zu erstellen.
1. In der Dialogbox **Eine neue Seite erstellen** geben Sie unter **Seitenname** einen passenden Seitennamen ein und wählen dann **Weiter**.
1. Wählen Sie unter **Wählen Sie eine Vorlage** dieselbe Vorlage aus, die auch von Ihrer Standard-Kategorieseite verwendet wird, und wählen Sie dann **Weiter**.
1. Wählen Sie unter **Wählen Sie ein Layout** ein Seitenlayout (z.B. **Flexibles Layout**) und wählen Sie dann **Weiter**.
1. Unter **Prüfen und beenden** überprüfen Sie die Konfiguration der Seite. Wenn Sie die Seiteninformationen bearbeiten müssen, wählen Sie **Zurück**. Wenn die Seiteninformationen korrekt sind, wählen Sie **Seite erstellen**. 
1. In der Zuteilung **Unterfußzeile** markieren Sie die Auslassungspunkte (**...**) und wählen Sie dann **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Module auswählen** das Modul **Container** und dann **OK** aus.
1. Wählen Sie im Slot **Container** die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Module auswählen** das Modul **Produktsammlung** und wählen Sie dann **OK**.  
1. Wählen Sie im Eigenschaftenbereich für das Produktsammelmodul **Produktliste hinzufügen** aus.
1. Wählen Sie im Dialogfeld **Produktlistenkonfiguration auswählen** den Typ der Liste, den Listenursprung aus und geben Sie die Anzahl der Artikel ein. Konfigurieren Sie alle anderen Optionen, die für den Listentyp verfügbar sind. Weitere Informationen zu Listentypen finden Sie in der folgenden Tabelle. 
1. Wählen Sie **OK**.
1. Wählen **Speichern** und dann **Vorschau** aus, um eine Vorschau der Seite anzuzeigen.
1. Wählen **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um sie zu veröffentlichen.

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

[Übersicht über die Modulbibliothek](starter-kit-overview.md)

[Karussellmodul](add-carousel.md)

[Umfangreiches Inhaltsblockmodul](add-content-rich-block.md)

[Containermodul](add-container-module.md)

[Kauffeldmodul](add-buy-box.md)

[Überblick über Produktempfehlungen](product-recommendations.md)

[Schnellansichtsmodul](quick-view-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
