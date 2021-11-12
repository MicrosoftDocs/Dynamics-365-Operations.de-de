---
title: Suchergebnismodul
description: Dieses Thema behandelt Suchergebnismodule und erläutert, wie diese Websiteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
ms.date: 10/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: dc4a01e520379a74ca3b21c1d588531412e762be
ms.sourcegitcommit: 9e8d7536de7e1f01a3a707589f5cd8ca478d657b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/18/2021
ms.locfileid: "7647511"
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

## <a name="enable-inventory-awareness-for-the-search-results-module"></a>Bestandserkennung für das Suchergebnismodul aktivieren

Kunden erwarten im Allgemeinen, dass eine E-Commerce-Site während des gesamten Surferlebnisses den Inventar berücksichtigt, damit sie entscheiden können, was zu tun ist, wenn für ein Produkt kein Inventar vorhanden ist. Das Suchergebnismodul kann so erweitert werden, dass es Bestandsdaten einbezieht und folgende Erfahrungen bietet:

- Zeigen Sie zusammen mit den Produkten ein Inventarverfügbarkeitsetikett an.
- Ausverkaufte Produkte ausblenden.
- Nicht vorrätige Produkte am Ende der Suchergebnisliste anzeigen.
    
Um diese Erfahrungen zu aktivieren, müssen Sie die folgenden vorausgesetzten Einstellungen in der Commerce-Zentrale konfigurieren.

### <a name="enable-the-enhanced-e-commerce-product-discovery-to-be-inventory-aware-feature"></a>Funktion „Erweiterte E-Commerce-Produktermittlung zur Bestandserfassung“ aktivieren

> [!NOTE]
> Die Funktion **Verbesserte E-Commerce-Produkterkennung, um den Bestand zu berücksichtigen** ist ab der Commerce-Version 10.0.20 verfügbar.

Um die Funktion **Verbesserte E-Commerce-Produkterkennung, um den Bestand zu berücksichtigen** in der Commerce-Zentrale zu aktivieren, führen Sie diese Schritte aus.

1. Wechseln Sie zu **Arbeitsbereiche \> Verwaltung von Funktionen**.
1. Suchen Sie nach der Funktion **Verbesserte E-Commerce-Produkterkennung, um den Bestand zu berücksichtigen** und aktivieren Sie sie.

### <a name="configure-the-populate-product-attributes-with-inventory-level-job"></a>Produktattribute mit Lagerebenenauftrag auffüllen konfigurieren

Der Job **Produktattribute mit Inventarebene auffüllen** erstellt ein neues Produktattribut, um die Inventarverfügbarkeit zu erfassen, und setzt dieses Attribut dann auf den neuesten Inventarwert für jedes Masterprodukt. Da sich die Lagerverfügbarkeit eines verkauften Produkts oder Sortiments ständig ändert, empfehlen wir dringend, den Job als Batch-Prozess einzuplanen.

Um den Job **Produktattribute mit Inventarebene auffüllen** in der Commerce-Zentrale zu konfigurieren, befolgen Sie diese Schritte.

1. Gehen Sie zu **Retail und Commerce \> Retail und Commerce IT \> Produkte und Bestand**.
1. Wählen Sie **Produktattribute mit Lagerbestand auffüllen**.
1. Befolgen Sie folgende Schritte im Dialogfeld **Produktattribute mit Inventarebene auffüllen**:

    1. Unter **Parameter** im Feld **Produktattribut und Typname**, geben Sie einen Namen für das dedizierte Produktattribut ein, das erstellt wird, um die Inventarverfügbarkeit zu erfassen.
    1. Unter **Parameter** im Feld **Inventarverfügbarkeit basierend auf** wählen Sie die Menge aus, auf der die Berechnung des Lagerbestands basieren soll (z. B. **Verfügbar physisch**).
    1. Unter **Im Hintergrund ausführen** konfigurieren Sie den Job so, dass er im Hintergrund ausgeführt wird, und aktivieren Sie optional die Option **Stapelverarbeitung**. 

> [!NOTE]
> Für eine konsistente Berechnung des Lagerbestands über PDPs und Produktlistenseiten auf Ihrer E-Commerce-Site sollten Sie für die Einstellung **Inventarverfügbarkeit basierend auf** in der Commerce-Zentrale und die Einstellung **Lagerbestand basierend auf** im Commerce Site Builder auswählen. Weitere Informationen zum Anwenden von Bestandeinstellungen in Site Builder finden Sie unter [Bestandseinstellungen anwenden](inventory-settings.md).

### <a name="configure-the-new-product-attribute"></a>Das neue Produktattribut konfigurieren

Nachdem der Job **Produktattribute mit Inventarebene auffüllen** ausgeführt wird, müssen Sie das neu erstellte Produktattribut auf der E-Commerce-Site konfigurieren, auf der Sie die Inventarerkennung für das Suchergebnismodul aktivieren möchten.

Um das neue Produktattribut in der Commerce-Zentralverwaltung zu konfigurieren, folgen Sie diesen Schritten.

1. Wählen Sie **Retail und Commerce \> Kanaleinstellung \> Kanalkategorien und Produktattribute** und wählen Sie eine e-Commerce-Seite aus.
1. Wählen und öffnen Sie eine zugehörige Attributgruppe, fügen Sie ihr das neu erstellte Produktattribut hinzu und schließen Sie dann die Seite.
1. Wählen Sie **Attributmetadaten festlegen**, wählen Sie das neu hinzugefügte Produktattribut aus und aktivieren Sie dann die Optionen **Attribut auf Kanal anzeigen**, **Abrufbar**, **Kann verfeinert werden**, und **Kann abgefragt werden**.

> [!NOTE]
> Bei Produkten, die im Suchergebnismodul angezeigt werden, wird die Bestandsebene auf Masterproduktebene anstelle der Einzelvariantenebene eingegeben. Es gibt nur zwei mögliche Werte: „verfügbar“ und „nicht auf Lager“. Der eigentliche Text für die Werte wird aus der Definition [Profil auf Lagerbestandsebene](inventory-buffers-levels.md) abgerufen. Ein Masterprodukt gilt nur dann als ausverkauft, wenn alle seine Varianten ausverkauft sind. Der Lagerbestand einer Variante wird basierend auf der Lagerbestandsprofildefinition des Produkts bestimmt. 

Nachdem alle vorherigen Konfigurationsschritte abgeschlossen sind, zeigen die Einschränkungen auf den Suchergebnisseiten einen inventarbasierten Filter an, und das Suchergebnismodul ruft Inventardaten hinter den Kulissen ab. Anschließend können Sie die Einstellung **Inventareinstellungen für Produktlistenseiten** im Commerce Site Builder konfigurieren, um zu steuern, wie das Suchergebnismodul nicht vorrätige Produkte anzeigt. Weitere Informationen finden Sie unter [Bestandeinstellungen anwenden](inventory-settings.md).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Übersicht zur Zielseite der Standardkategorie und der Suchergebnisseite](category-search-page-overview.md)

[Informationen zur Modulbibliothek](starter-kit-overview.md)

[Schnellansichtsmodul](quick-view-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
