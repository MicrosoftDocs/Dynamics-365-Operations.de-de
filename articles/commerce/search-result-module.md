---
title: Suchergebnismodul
description: Dieses Thema behandelt Suchergebnismodule und erläutert, wie diese Websiteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
manager: annbe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 3761be29955458099d01f2271057884fc1fd6f28
ms.sourcegitcommit: 872600103d2a444d78963867e5e0cdc62e68c3ec
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/01/2021
ms.locfileid: "5097177"
---
# <a name="search-results-module"></a>Suchergebnismodul

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Dieses Thema behandelt Suchergebnismodule und erläutert, wie diese Websiteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.

Das Suchergebnismodul gibt Produktsuchergebnisse und eine Liste der anwendbaren Verfeinerungskriterien für die Produkte zurück. Suchergebnismodule auf Dynamics 365 Commerce-Websites können zum Rendern von Seiten für folgende Szenarien verwendet werden:

- Suchergebnisse, die von einer Benutzersuche initiiert werden
- Suchergebnisse, die eine bestimmte Reihe von Produkten anzeigen, z. B. „Produkte mit ähnlichem Aussehen kaufen“
- Eine Liste von Produkten, die zu einer bestimmten Kategorie gehören

Weitere Informationen zu Kategorien- und Suchergebnisseiten finden Sie unter [Übersicht zur Zielseite der Standardkategorie und der Suchergebnisseite](category-search-page-overview.md).

Die folgende Abbildung zeigt das Beispiel einer Kategorie-Suchergebnisseite auf der Fabrikam-Website.

![Beispiel einer Suchergebnisseite auf der Fabrikam-Website](./media/SimpleCategoryLandingDressCategory.png)

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

> [!IMPORTANT]
> In Dynamics 365 Commerce Version 10.0.16 und später kann die Konfiguration **Zugehörigkeitspreise anzeigen** verwendet werden, um die Zugehörigkeitspreise auf der Seite anzuzeigen.

## <a name="supported-modules"></a>Unterstützte Module

Das Suchergebnismodul unterstützt das [Schnellansichtsmodul](quick-view-module.md), mit dem sich Benutzer Produktinformationen anzeigen lassen und Artikel über die Suchergebnisseite dem Warenkorb hinzufügen können.

## <a name="add-a-search-results-module-to-a-category-page"></a>Einer Kategorieseite ein Suchergebnismodul hinzufügen

Führen Sie folgende Schritte aus, um ein Suchergebnismodul einer Kategorieseite hinzuzufügen.

1. Wechseln Sie zu **Vorlagen** und wählen Sie **Neu** aus, um eine neue Vorlage zu erstellen.
1. Geben Sie im Dialogfeld **Neue Vorlage** den Namen **Suchergebnisse** ein, und wählen Sie anschließend **OK** aus.
1. Wählen Sie im Slot **Körper** die Ellipsen-Schaltfläche (...) und anschließend **Modul hinzufügen** aus.
1. Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **Standardseite** und dann **OK** aus.
1. Wählen Sie im **Haupt**-Slot auf der **Standardseite** die Ellipsen-Schaltfläche (...) und anschließend **Modul hinzufügen** aus.
1. Wählen Sie im Dialogfeld **Modul hinzufügen** wählen Sie das Modul **Container** und dann **OK** aus.
1. Wählen Sie im **Container**-Slot die Ellipsen-Schaltfläche (...) und anschließend **Modul hinzufügen** aus.
1. Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **Breadcrumb** und dann **OK** aus.
1. Geben Sie im **Breadcrumb**-Eigenschaftenbereich den Wert **1** für **Min. Vorkommen** ein.
1. Wählen Sie im **Container**-Slot die Ellipsen-Schaltfläche (...) und anschließend **Modul hinzufügen** aus.
1. Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **Suchergebnisse** und anschließend **OK** aus.
1. Geben Sie im **Suchergebnisse**-Eigenschaftenbereich den Wert **1** für **Min. Vorkommen** ein, und legen Sie dann alle anderen erforderlichen Eigenschaften für das Suchergebnismodul fest. Durch Festlegen dieser Eigenschaften in der Vorlage stellen Sie sicher, dass alle Anpassungen auf einer bestimmten Kategorieseite diese Einstellungen automatisch enthalten.
1. Wählen Sie **Bearbeiten beenden** aus, und wählen Sie dann **Veröffentlichen** aus, um die Vorlage zu veröffentlichen.
1. Wechseln Sie zu **Seiten**, und wählen Sie dann **Neu** aus, um eine neue Seite zu erstellen.
1. Wählen Sie im Dialogfeld **Vorlage auswählen** die zuvor erstellte **Suchergebnis**-Vorlage aus. Geben Sie als **Seitenname** **Kategorieseite** ein, und wählen Sie dann **OK** aus. Da alle Werte in der Vorlage festgelegt sind, kann die Seite veröffentlicht werden.
1. Wählen **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um sie zu veröffentlichen.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Übersicht zur Zielseite der Standardkategorie und der Suchergebnisseite](category-search-page-overview.md)

[Informationen zur Modulbibliothek](starter-kit-overview.md)

[Schnellansichtsmodul](quick-view-module.md)
