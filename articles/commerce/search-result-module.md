---
title: Suchergebnismodul
description: Dieser Artikel behandelt Suchergebnismodule und erläutert, wie diese Websiteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
ms.date: 08/31/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: eeb7cd0769fcb866a3d7dcc03e8e87daf24b2c5d
ms.sourcegitcommit: 1d5cebea3e05b6d758cd01225ae7f566e05698d2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2022
ms.locfileid: "9405292"
---
# <a name="search-results-module"></a>Suchergebnismodul

[!include [banner](includes/banner.md)]

Dieser Artikel behandelt Suchergebnismodule und erläutert, wie diese Websiteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.

Das Suchergebnismodul gibt Produktsuchergebnisse und eine Liste der anwendbaren Verfeinerungskriterien für die Produkte zurück. Suchergebnismodule auf Dynamics 365 Commerce-Websites können zum Rendern von Seiten für folgende Szenarien verwendet werden:

- Suchergebnisse, die von einer Benutzersuche initiiert werden
- Suchergebnisse, die eine bestimmte Reihe von Produkten anzeigen, z. B. „Produkte mit ähnlichem Aussehen kaufen“
- Eine Liste von Produkten, die zu einer bestimmten Kategorie gehören

Weitere Informationen zu Kategorien- und Suchergebnisseiten finden Sie unter [Übersicht zur Zielseite der Standardkategorie und der Suchergebnisseite](category-search-page-overview.md).

Die folgende Abbildung zeigt das Beispiel einer Kategorie-Suchergebnisseite auf der Fabrikam-Website.

![Beispiel einer Suchergebnisseite auf der Fabrikam-Website.](./media/SimpleCategoryLandingDressCategory.png)

## <a name="search-results-module-properties"></a>Eigenschaften des Suchergebnismoduls

In der folgenden Tabelle sind die Eigenschaften von Suchergebnismodulen mit ihren Werten und Beschreibungen aufgeführt.

| Eigenschaft | Werte | Beschreibung |
|----------|--------|-------------|
| Artikel pro Seite | Ganzzahl | Die Anzahl der Artikel, die auf jeder Seite angezeigt werden sollen. |
| Wieder auf PDP zulassen | **True** oder **False** | Ist diese Eigenschaft auf **True** gesetzt, wird in der Breadcrumb-Navigation auf der geöffneten Produktdetailseite (Product Details Page, PDP) der Link „Zurück zu Ergebnissen“ angezeigt, wenn ein Benutzer ein Produkt auf der Suchergebnisseite auswählt. |
| Einschränkungen erweitern | **Alle**, **1**, **2**, **3** oder **4** | Die Anzahl der Top-Verfeinerungskriterien, die beim Laden einer Seite erweitert werden sollen. Beispielsweise werden die ersten drei Verfeinerungskriterien auf der Seite erweitert, wenn diese Eigenschaft auf **3** gesetzt ist. |
| Kategorie-Hierarchieanzeige ausblenden | **True** oder **False** | Ist diese Eigenschaft auf **True** gesetzt, wird die Anzeige der Kategoriehierarchie auf der Seite ausgeblendet. Diese Eigenschaft sollte auf **True** gesetzt sein, wenn Sie das [Breadcrumb-Modul](add-breadcrumb.md) nutzen, um die Kategoriehierarchie anzuzeigen.|
| Produktattribute in Suchergebnisse einbeziehen | **True** oder **False** | Wenn diese Eigenschaft auf **True** gesetzt ist, werden für die Produkte in den Suchergebnissen Attribute zurückgegeben. Obwohl diese Attribute auf einer Commerce-Website angezeigt werden können, ist eine Erweiterung erforderlich.|
| Zugehörigkeitspreise anzeigen | **True** oder **False** | Ist diese Eigenschaft auf **True** gesetzt, werden in den Suchergebnissen Zugehörigkeitspreise für Produkte angezeigt, wenn ein angemeldeter Benutzer die Seite durchsucht. |
| Aktualisieren Sie den Verfeinerungs-Bereich | **True** oder **False** | Wenn diese Eigenschaft auf **Wahr** festgelegt ist, wird der Verfeinerungs-Bereich aktualisiert, wenn Verfeinerungen ausgewählt werden. In diesem Modus verhalten sich einige Mehrfachauswahl-Verfeinerungen wie Einzelauswahl-Verfeinerungen, wenn das Verfeinerungsfenster aktualisiert wird. |

> [!IMPORTANT]
> In Commerce Version 10.0.16 und später kann die Konfiguration **Zugehörigkeitspreise anzeigen** verwendet werden, um die Zugehörigkeitspreise auf der Seite anzuzeigen.
>
> In der Commerce-Version 10.0.20 und höher kann die Konfiguration **Aktualisieren Sie den Verfeinerungs-Bereich** verwendet werden, um den Verfeinerungs-Bereich während der Verfeinerungs-Auswahl zu aktualisieren.

## <a name="supported-modules"></a>Unterstützte Module

Das Suchergebnismodul unterstützt das [Schnellansichtsmodul](quick-view-module.md), mit dem sich Benutzer Produktinformationen anzeigen lassen und Artikel über die Suchergebnisseite dem Warenkorb hinzufügen können.

## <a name="add-a-search-results-module-to-a-category-page"></a>Einer Kategorieseite ein Suchergebnismodul hinzufügen

Gehen Sie folgendermaßen vor, um einer Kategorieseite im Site Builder ein Suchergebnismodul hinzuzufügen.

1. Wechseln Sie zu **Vorlagen** und wählen Sie **Neu** aus, um eine neue Vorlage zu erstellen.
1. Geben Sie im Dialogfeld **Neue Vorlage** den Namen **Suchergebnisse** ein, und wählen Sie anschließend **OK** aus.
1. Markieren Sie im Slot **Hauptteil** die Auslassungspunkte (...) und wählen Sie dann **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Modul auswählen** das Modul **Standardseite** und dann **OK** aus.
1. Markieren Sie im Slot **Haupt** des Moduls **Standardseite** die Auslassungspunkte (...) und wählen Sie dann **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Module auswählen** das Modul **Container** und dann **OK** aus.
1. Markieren Sie im Slot **Container** die Auslassungspunkte (...) und wählen Sie dann **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Module auswählen** das Modul **Brotkrümel** und wählen Sie dann **OK**.
1. Geben Sie im **Breadcrumb**-Eigenschaftenbereich den Wert **1** für **Min. Vorkommen** ein.
1. Markieren Sie im Slot **Container** die Auslassungspunkte (...) und wählen Sie dann **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Module auswählen** das Modul **Suchergebnisse** und wählen Sie dann **OK**.
1. Geben Sie im **Suchergebnisse**-Eigenschaftenbereich den Wert **1** für **Min. Vorkommen** ein, und legen Sie dann alle anderen erforderlichen Eigenschaften für das Suchergebnismodul fest. Durch Festlegen dieser Eigenschaften in der Vorlage stellen Sie sicher, dass alle Anpassungen auf einer bestimmten Kategorieseite diese Einstellungen automatisch enthalten.
1. Wählen Sie **Bearbeiten beenden** aus, und wählen Sie dann **Veröffentlichen** aus, um die Vorlage zu veröffentlichen.
1. Wechseln Sie zu **Seiten**, und wählen Sie dann **Neu** aus, um eine neue Seite zu erstellen.
1. Im Dialogfeld **Eine neue Seite erstellen** geben Sie unter **Seitenname** **Kategorieseite** ein und wählen Sie dann **Weiter**.
1. Wählen Sie unter **Wählen Sie eine Vorlage** die Vorlage **Suchergebnisse**, die Sie erstellt haben, und wählen Sie dann **Weiter**.
1. Wählen Sie unter **Wählen Sie ein Layout** ein Seitenlayout (z.B. **Flexibles Layout**) und wählen Sie dann **Weiter**.
1. Unter **Prüfen und beenden** überprüfen Sie die Konfiguration der Seite. Wenn Sie die Seiteninformationen bearbeiten müssen, wählen Sie **Zurück**. Wenn die Seiteninformationen korrekt sind, wählen Sie **Seite erstellen**.
1. Wählen **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um sie zu veröffentlichen.

## <a name="inventory-aware-search-results-module"></a>Modul für Suchergebnisse mit Bestandserfassung

Das Suchergebnismodul kann so konfiguriert werden, dass es Bestandsdaten einbezieht und folgende Erfahrungen bietet:

- Bestandsangaben neben Produkten anzeigen.
- Nicht vorrätige Produkte aus der Produktliste ausblenden.
- Nicht vorrätige Produkte am Ende der Produktliste anzeigen.
- Bestandsbasierte Produktfilterung unterstützen.

Um diese Erfahrungen zu aktivieren, müssen Sie zuerst das Feature **Erweiterte E-Commerce-Produktermittlung zur Bestandserfassung** in Commerce headquarters aktivieren und dann die notwendigen Einstellungen konfigurieren. Weitere Informationen finden Sie unter [Produktauflistung mit Bestandserfassung](inventory-aware-product-listing.md).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Übersicht zur Zielseite der Standardkategorie und der Suchergebnisseite](category-search-page-overview.md)

[Informationen zur Modulbibliothek](starter-kit-overview.md)

[Schnellansichtsmodul](quick-view-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
