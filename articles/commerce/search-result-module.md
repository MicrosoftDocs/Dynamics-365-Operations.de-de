---
title: Suchergebnismodul
description: Dieser Artikel behandelt Suchergebnismodule und erläutert, wie diese Websiteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
ms.date: 05/18/2022
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
ms.openlocfilehash: d026de098ec182e3f7631c1c19e54b3b36db341f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886957"
---
# <a name="search-results-module"></a>Suchergebnismodul

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

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

## <a name="enable-inventory-awareness-for-the-search-results-module"></a>Bestandserkennung für das Suchergebnismodul aktivieren

Kunden erwarten im Allgemeinen, dass die E-Commerce-Website während des gesamten Surferlebnisses den Inventar berücksichtigt, damit sie entscheiden können, was zu tun ist, wenn für ein Produkt kein Inventar vorhanden ist. Das Suchergebnismodul kann so konfiguriert werden, dass es Bestandsdaten einbezieht und folgende Erfahrungen bietet:

- Inventarverfügbarkeitsetikett zusammen mit dem Produkt anzeigen.
- Nicht vorrätige Produkte aus der Produktliste ausblenden.
- Nicht vorrätige Produkte am Ende der Produktliste anzeigen.
- Produkte in den Suchergebnissen nach Lagerbestand filtern.

Um diese Erfahrungen zu aktivieren, müssen Sie zuerst die Funktion **Erweiterte E-Commerce-Produktermittlung zur Bestandserfassung** im Arbeitsplatz **Funktionsverwaltung** aktivieren.

> [!NOTE]
> Die Funktion **Verbesserte E-Commerce-Produkterkennung, um den Bestand zu berücksichtigen** ist in Commerce-Version 10.0.20 und höher verfügbar.

Die bestandsbezogene Produktsuche verwendet Produktattribute, um Informationen zur Bestandsverfügbarkeit zu erhalten. Als Voraussetzung für das Feature müssen dedizierte Produktattribute angelegt, Bestandsdaten dazu erfasst und dem Online-Kanal hinzugefügt werden. 

Führen Sie die folgenden Schritte aus, um dedizierte Produktattribute zur Unterstützung des Suchergebnismoduls mit Bestandserfassung zu erstellen.

1. Gehen Sie in der Zentralverwaltung zu **Retail und Commerce \> Retail und Commerce IT \> Produkte und Bestand**.
1. Wählen und öffnen Sie **Produktattribute mit Lagerbestand auffüllen**.
1. Geben Sie im Dialogfeld die folgenden Informationen ein:

    1. Geben Sie im Feld **Produktattribut und Typname** einen Namen für das dedizierte Produktattribut ein, das erstellt wird, um die Inventardaten zu erfassen.
    1. Wählen Sie im Feld **Inventarverfügbarkeit basierend auf** den Mengentyp aus, auf dem die Berechnung des Lagerbestands basieren soll (z. B. **Verfügbar physisch**). 

1. Führen Sie den Einzelvorgang im Hintergrund aus. Da sich der Produktbestand in einer Omnichannel-Umgebung ständig ändert, empfehlen wir dringend, diesen Job als Batch-Prozess einzuplanen.

> [!NOTE]
> Für eine konsistente Berechnung des Lagerbestands über Seiten und Module auf Ihrer E-Commerce-Website sollten Sie denselben Mengentyp für die Einstellung **Inventarverfügbarkeit basierend auf** in der Commerce-Zentralenverwaltung und die Einstellung **Lagerbestand basierend auf** im Commerce Site Builder auswählen. Weitere Informationen zum Anwenden von Bestandeinstellungen in Site Builder finden Sie unter [Bestandseinstellungen anwenden](inventory-settings.md).

Gehen Sie folgendermaßen vor, um die Produktattribute für einen Online-Kanal zu konfigurieren. 

1. Gehen Sie in der Zentralverwaltung zu **Einzelhandel und Handel \> Kanaleinstellungen \> Kanalkategorien und Produktattribute**.
1. Wählen Sie einen Online-Kanal aus, für den das Suchergebnismodul mit Bestandserfassung aktiviert werden soll.
1. Wählen und öffnen Sie eine zugehörige Attributgruppe und fügen Sie ihr dann das neu erstellte Produktattribut hinzu.
1. Wählen Sie in Versionen vor der Commerce-Version 10.0.27 **Attributmetadaten festlegen**, wählen Sie das neu hinzugefügte Produktattribut aus und aktivieren Sie dann die Optionen **Attribut auf Kanal anzeigen**, **Abrufbar**, **Kann verfeinert werden**, und **Kann abgefragt werden**.
1. Gehen Sie zu **Einzelhandel und Handel \> IT für Einzelhandel und Handel \> Vertriebsplan**, und führen Sie den Einzelvorgang **1150 (Katalog)** aus. Wenn Sie den Einzelvorgang **Produktattribute mit Lagerbestand auffüllen** als Batch-Prozess ausführen, empfehlen wir, den 1150-Einzelvorgang auch als Batch-Prozess einzuplanen, der mit der gleichen Häufigkeit ausgeführt wird.

> [!NOTE]
> Bei Produkten, die im Suchergebnismodul angezeigt werden, wird die Bestandsebene auf Masterproduktebene anstelle der Einzelvariantenebene angezeigt. Es gibt nur zwei mögliche Werte: „verfügbar“ und „nicht auf Lager“. Das eigentliche Etikett für den Wert wird aus der Definition [Profil auf Lagerbestandsebene](inventory-buffers-levels.md) abgerufen. Ein Masterprodukt gilt nur dann als ausverkauft, wenn alle seine Varianten ausverkauft sind.

Nachdem alle vorherigen Konfigurationsschritte abgeschlossen sind, zeigen die Einschränkungen auf den Suchergebnisseiten einen inventarbasierten Filter an, und das Suchergebnismodul ruft Inventardaten hinter den Kulissen ab. Anschließend können Sie die Einstellung **Inventareinstellungen für Produktlistenseiten** im Commerce Site Builder konfigurieren, um zu steuern, wie das Suchergebnismodul nicht vorrätige Produkte anzeigt. Weitere Informationen finden Sie unter [Bestandeinstellungen anwenden](inventory-settings.md).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Übersicht zur Zielseite der Standardkategorie und der Suchergebnisseite](category-search-page-overview.md)

[Informationen zur Modulbibliothek](starter-kit-overview.md)

[Schnellansichtsmodul](quick-view-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
