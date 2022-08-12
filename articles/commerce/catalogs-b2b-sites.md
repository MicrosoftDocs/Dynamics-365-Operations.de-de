---
title: Commerce-Kataloge für B2B-Websites erstellen
description: In diesem Artikel wird beschrieben, wie Sie Commerce-Kataloge für Business-to-Business-Websites (B2B) in Microsoft Dynamics 365 Commerce erstellen.
author: ashishmsft
ms.date: 07/11/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-02-28
ms.openlocfilehash: 7d4ed3e2a76924c2c3c0ba55e21ba648e8da7b76
ms.sourcegitcommit: d1491362421bf2fcf72a81dc2dc2d13d3b98122b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/11/2022
ms.locfileid: "9136825"
---
# <a name="create-commerce-catalogs-for-b2b-sites"></a>Commerce-Kataloge für B2B-Websites erstellen

[!include [banner](includes/banner.md)]

In diesem Artikel wird beschrieben, wie Sie Commerce-Produktkataloge für Business-to-Business-Websites (B2B) in Microsoft Dynamics 365 Commerce erstellen. Antworten auf häufig gestellte Fragen zu Commerce-Katalogen für B2B-Websites finden Sie unter [FAQ zu Commerce-Katalogen für B2B](catalogs-b2b-sites-FAQ.md).

> [!NOTE]
> Dieser Artikel gilt für Dynamics 365 Commerce ab Version 10.0.27.

Sie können Commerce-Kataloge verwenden, um die Produkte zu identifizieren, die Sie in den B2B-Onlineshops anbieten möchten. Wenn Sie einen Katalog erstellen, kennzeichnen Sie die Onlineshops, in denen die Produkte angeboten werden, fügen Sie die Produkte hinzu, die einbezogen werden sollen, und verbessern Sie die Produktangebote, indem Sie Verkaufdetails hinzufügen. Sie können für jeden B2B-Online-Store mehrere Kataloge erstellen, wie in der folgenden Abbildung gezeigt.

![Commerce Produktkataloge in der Vorschau.](./media/Commerce_Catalogs.png)

Mit Commerce-Produktkatalogen können Sie die folgenden Informationen definieren:

- **Katalogtyp** – Konfigurieren Sie den Wert als **B2B**. Sie können B2B-katalogspezifische Eigenschaften wie eine Navigationshierarchie, eine Kundenhierarchie und Attribut-Metadaten für den Katalog definieren. 
- **Katalogspezifische Navigationshierarchie** – Organisationen können eine eindeutige Kategoriestruktur für ihren spezifischen Katalog erstellen.
- **Katalogspezifische Attributmetadaten** – Attribute enthalten Details zu einem Produkt. Indem Sie einer Kategorie der Navigationshierarchie Attribute zuweisen, können Sie Werte für diese Attribute auf der Ebene der Produkte definieren, die dieser Kategorie zugewiesen sind. Organisationen können dann diese Aufgaben durchführen:

    - Definieren Sie katalogspezifische Attributwerte.
    - Steuern Sie die Sichtbarkeit von Attributen auf Katalogebene.
    - Wählen Sie die Einschränkungen aus, die für einen einzelnen Katalog spezifisch sind.

- **Kanäle** – Organisationen können einem Katalog mehr als einen B2B-Onlinekanal zuordnen. End-to-End-Support für Kataloge ist derzeit nur für B2B-Onlineshops verfügbar.
- **Kundenhierarchien** – Organisationen können für einen bestimmten B2B-Kanal ausgewählten B2B-Partnern einen bestimmten Katalog zur Verfügung stellen, indem sie diesem Katalog Kundenhierarchien zuordnen.
- **Preisgruppen** – Sie können Preise und Aktionen konfigurieren, die für einen bestimmten Katalog spezifisch sind. Diese Fähigkeit ist ein Hauptgrund für die Definition eines Katalogs für einen B2B-Kanal. Preisgruppen für Kataloge ermöglichen es Organisationen, Produkte für ihre beabsichtigten B2B-Organisationen verfügbar zu machen und ihre bevorzugten Preise und Rabatte anzuwenden. B2B-Kunden, die aus einem konfigurierten Katalog bestellen, können von Sonderpreisen und Werbeaktionen profitieren, nachdem sie sich auf einer Commerce B2B-Website angemeldet haben. Um katalogspezifische Preise zu konfigurieren, wählen Sie **Preisgruppen** auf der Registerkarte **Kataloge** aus, um eine oder mehrere Preisgruppen mit dem Katalog zu verknüpfen. Alle Handelsvereinbarungen, Preisregulierungserfassungen und Vorzugsrabatte, die mit der gleichen Preisgruppe verknüpft sind, werden bei der Bestellung aus diesem Katalog angewendet. (Erweiterte Rabatte umfassen Schwellenwert-, Mengen- und Angebots-Sortimentsrabatte.) Weitere Informationen zu Preisgruppen finden Sie unter [Preisgruppen](price-management.md#price-groups).

> [!NOTE]
> Diese Funktion ist ab der Dynamics 365 Commerce Version 10.0.27 verfügbar. Um katalogspezifische Konfigurationen wie Navigationshierarchie und Debitor-Hierarchie in der Commerce headquarters zu konfigurieren, gehen Sie in den Arbeitsbereich **Funktionsverwaltung** (**Systemadministration \> Arbeitsbereiche \> Funktionsverwaltung**), aktivieren Sie die Funktion **Verwendung mehrerer Kataloge auf Einzelhandelskanälen aktivieren** und führen Sie dann den Auftrag **1110 CDX** aus. Wenn Sie diese Funktion aktivieren, werden alle vorhandenen Kataloge, die für POS-Stores oder ein Call Center verwendet werden, auf der Seite **Kataloge** als **Katalogtyp = B2C** gekennzeichnet. Nur bestehende und neue Kataloge, die als **Katalogtyp = B2C** gekennzeichnet sind, sind für POS Stores und ein Call Center geeignet. 

## <a name="b2b-catalog-process-flow"></a>B2B-Katalog Prozess Flow

Der Prozess der Erstellung und Verarbeitung eines Katalogs besteht aus vier allgemeinen Schritten. Jeder Schritt wird im nächsten Abschnitt ausführlich erklärt.

> [!NOTE]
> Bevor Sie fortfahren, stellen Sie sicher, dass der Katalog als **Katalogtyp = B2B** markiert ist.

1. **[Variante](#configure-the-catalog)**

    - Ordnen Sie die Navigationshierarchie zu.
    - Geben Sie gegebenenfalls Gültigkeits- und Ablaufdaten an.
    - Fügen Sie Produkte hinzu und kategorisieren Sie diese.
    - Ordnen Sie Preisgruppen zu.
    - Ordnen Sie eine Kundenhierarchie zu, die für Ihre B2B-Organisationen spezifisch ist. 
    - Ordnen Sie eine standardmäßige Dimensionsattributgruppe für Einschränkungen wie Größe, Stil und Farbe zu.
    - Legen Sie Attributmetadaten fest.

1. **[Prüfung](#validate-the-catalog)** – In diesem Schritt führen Sie Prüfungsregeln aus, die ein bestimmtes Verhalten erzwingen. Im Folgenden finden Sie einige Beispiele hierfür:

    - Stellen Sie sicher, dass keine nicht kategorisierten Produkte vorhanden sind.
    - Stellen Sie sicher, dass alle Artikel, die jedem Kanal zugeordnet sind, einem Katalog zugeordnet sind.

1. **[Genehmigung](#approve-the-catalog)**
1. **[Veröffentlichung](#publish-the-catalog)**

## <a name="set-up-the-catalog"></a>Den Katalog einrichten

Verwenden Sie die Informationen in diesem Abschnitt, um Ihren Katalog einzurichten.

### <a name="configure-the-catalog"></a>Den Katalog konfigurieren

Gehen Sie in der Commerce-Zentrale zu **Einzelhandel und Handel \> Kataloge und Sortimente \> Alle Kataloge**, um Ihren Katalog zu konfigurieren.

Wenn Sie einen neuen Katalog anlegen, müssen Sie ihn zunächst einem oder mehreren Kanälen zuordnen. Nur Artikel, die mit Ihrem ausgewählten Kanal [Sortimente](/dynamics365/unified-operations/retail/assortments) verknüpft sind, können bei der Erstellung des Katalogs verwendet werden. Um den Katalog einem oder mehreren Kanälen zuzuordnen, wählen Sie **Hinzufügen** auf dem Inforegister **Commerce-Kanäle** der Seite **Katalog einrichten** aus. Stellen Sie sicher, dass der Katalog als **Katalogtyp = B2B** gekennzeichnet ist.

#### <a name="associate-the-navigation-hierarchy"></a>Die Navigationshierarchie zuordnen

Um Produkte in einen Katalog aufzunehmen, müssen Sie eine Navigationshierarchie auswählen. Die Navigationshierarchie unterstützt die Kategoriestruktur für den Katalog. Sie müssen eine der Navigationshierarchien auswählen, die den auf dem Inforegister **Commerce-Kanäle** der Seite **Katalogeinrichtung** ausgewählten Kanälen zugeordnet sind. Um jedem Ihrer Kanäle eine Standardnavigationshierarchie zuzuordnen, gehen Sie zu **Einzelhandel und Handel \> Kanaleinstellungen \> Kanalkategorien und Produktattribute**.

#### <a name="specify-time-effective-and-expiration-dates"></a>Gültigkeits- und Ablaufdaten angeben

Um Gültigkeits- und Ablaufdaten für einen Katalog anzugeben, wählen Sie den obersten Knoten der Kataloghierarchie aus, um zur Kopfansicht des Hauptkatalogs zurückzukehren. Konfigurieren Sie dann das Gültigkeits- und Ablaufdatum nach Bedarf auf dem Inforegister **Allgemein**.

#### <a name="add-and-categorize-products"></a>Produkte hinzufügen und kategorisieren

Um Produkte zum Hinzufügen zum Katalog zu konfigurieren, gehen Sie in der Commerce-Zentrale zu **Einzelhandel und Handel \> Kataloge und Sortimente \> Alle Kataloge**. Wählen Sie auf der Registerkarte **Kataloge** dann **Produkte hinzufügen** aus.

Wählen Sie alternativ einen Knoten in der Navigationshierarchie aus. Sie können dann Produkte direkt zu einer Kategorie im Katalog hinzufügen.

#### <a name="associate-price-groups"></a>Preisgruppen zuordnen

Um Produkte zum Hinzufügen zum Katalog zu konfigurieren, gehen Sie in der Commerce-Zentrale zu **Einzelhandel und Handel \> Kataloge und Sortimente \> Alle Kataloge**. Wählen Sie auf der Registerkarte **Kataloge** dann **Produkte hinzufügen** aus. 

Produkte, die einem Katalog über den Wurzelknoten der Navigationshierarchie durch Auswahl von **Produkte hinzufügen** im Aktionsbereich hinzugefügt wurden, erben ihre Kategorien, wenn die Quellnavigationshierarchie ebenfalls mit dem Katalog verknüpft ist. Änderungen an Kategorien, die in der Quellnavigationshierarchie vorgenommen werden, werden sofort in den Katalogen übernommen. Sie müssen die Kataloge neu veröffentlichen, um die Channels zu aktualisieren.

Alternativ können Sie auch einen Knoten in der Navigationshierarchie auswählen und Produkte direkt zu einer ausgewählten Kategorie im Katalog hinzufügen. 

Wenn Sie Produkte hinzufügen, wird die Option **Automatisch alle Varianten einbeziehen, wenn nur Produktstamm ausgewählt ist** verfügbar sein. Um die Einbeziehung aller Varianten zu verhindern, wählen Sie mindestens eine Variante für den Produktstamm aus. 

> [!NOTE]
> Wenn Sie sich dafür entscheiden, automatisch alle Varianten in eine große Produktstammauswahl aufzunehmen, kann es zu längeren Verarbeitungszeiten kommen. Bei großen Auswahlen empfehlen wir Ihnen, im Aktionsbereich der Seite Kataloge die Option **Alle Varianten einbeziehen** zu wählen, um den Vorgang im Batch-Modus auszuführen. Wenn Sie nur den Produktstamm in den Katalog aufgenommen und keine Varianten hinzugefügt haben, ist die Variantenauswahl möglicherweise nicht verfügbar, wenn Sie zu einer Produktdetailseite navigieren. 

Um katalogspezifische Preise zu konfigurieren, müssen Sie eine oder mehrere Preisgruppen mit dem Katalog verknüpfen. Um einem Katalog Preisgruppen zuzuordnen, gehen Sie in der Commerce-Zentrale zu **Einzelhandel und Handel \> Kataloge und Sortimente \> Alle Kataloge**. Wählen Sie auf der Registerkarte **Kataloge** unter **Preisgestaltung** dann **Preisgruppen** aus. Alle Handelsvereinbarungen, Preisregulierungserfassungen und Vorzugsrabatte (Schwellenwert-, Mengen- und Angebots-Sortimentsrabatte), die mit der gleichen Preisgruppe verknüpft sind, werden bei der Bestellung aus dem Katalog angewendet.

Weitere Informationen zu Preisgruppen finden Sie unter [Preisgruppen](price-management.md#price-groups).

> [!NOTE]
> Sie können keine neue Preisgruppe über die Seite **Alle Kataloge** erstellen. Stattdessen müssen Sie sie über die Seite **Alle Preisgruppen** erstellen. Sie müssen sie dann dem Katalog auf der Seite **Alle Kataloge** zuordnen.

#### <a name="associate-a-customer-hierarchy"></a>Eine Kundenhierarchie zuordnen

Gehen Sie in der Commerce-Zentrale zu **Einzelhandel und Handel \> Kataloge und Sortimente \> Alle Kataloge**, um Kundenhierarchien zuzuordnen. Wählen Sie auf der Registerkarte **Kataloge** unter **Kundenhierarchie** dann **Hierarchien zuweisen** aus, um eine oder mehrere Kundenhierarchien mit dem Katalog zu verknüpfen.

> [!NOTE]
> Sie können keine neue Kundenhierarchie über die Seite **Alle Kataloge** erstellen. Stattdessen müssen Sie sie über die Seite **Kundenhierarchien** erstellen. Sie müssen sie dann dem Katalog auf der Seite **Alle Kataloge** zuordnen.

#### <a name="associate-default-dimension-attribute-group-for-refiners-such-as-size-style-and-color"></a>Standardmäßige Dimensionsattributgruppe für Einschränkungen wie Größe, Stil und Farbe zuordnen

Um eine Standard-Dimensionsattributgruppe für Einschränkungen wie Größe, Stil und Farbe zuzuordnen, gehen Sie in der Commerce-Zentrale zu **Einzelhandel und Handel \> Kataloge und Sortimente \> Alle Kataloge**. Wählen Sie auf der Registerkarte **Kataloge** unter **Attribute** dann **Attributgruppen** aus.

#### <a name="set-attribute-metadata"></a>Attributmetadaten festlegen

Gehen Sie in der Commerce-Zentrale zu **Einzelhandel und Handel \> Kataloge und Sortimente \> Alle Kataloge**, um Attributmetadaten zu konfigurieren. Wählen Sie auf der Registerkarte **Kataloge** unter **Attribute** dann **Attributmetadaten festlegen** aus. Um die Attribute auszuwählen, die sichtbar und verfeinerbar sein sollen, wählen Sie eine Kategorie in der zugeordneten katalogspezifischen Navigationshierarchie aus und wählen dann unter **Katalogproduktattribute** ein Attribut aus. Wählen Sie dann **Attribut für Kanal anzeigen** aus. Standardmäßig sind alle sichtbaren Attribute auch durchsuchbar. Um Attribute optional verfeinerbar zu machen, wählen Sie **Kann verfeinert werden** aus.

### <a name="validate-the-catalog"></a>Katalog überprüfen

Bevor ein neuer Katalog verwendet werden kann, muss er überprüft und veröffentlicht werden.

Führen Sie folgende Schritte aus, um einen Katalog zu überprüfen.

1. Auf der Registerkarte **Kataloge** auf der Seite **Alle Kataloge** unter **Überprüfen** wählen Sie **Katalog überprüfen** aus, um eine Überprüfung auszuführen. Dieser Schritt ist notwendig. Er überprüft, dass die erforderliche Einstellung korrekt ist.
1. Wählen Sie **Ergebnisse anzeigen** aus, um die Details der Prüfung anzusehen. Wenn Fehler gefunden werden, müssen Sie die Daten korrigieren und die Prüfung dann erneut durchführen, bis sie bestanden wurde.

> [!NOTE]
> Wenn **Katalogtyp = B2B**, schlägt die Validierung fehl, wenn Sie dem Katalog POS Stores oder ein Call Center hinzugefügt haben. B2B-Kataloge dürfen nur mit B2B-Online-Kanälen verknüpft sein. Die Validierung schlägt auch fehl, wenn keine Debitor-Hierarchie mit einem B2B-Katalog verknüpft ist. 

### <a name="approve-the-catalog"></a>Katalog genehmigen

Nachdem ein Katalog überprüft wurde, muss er genehmigt werden.

Gehen Sie folgendermaßen vor, um den Workflow für die Kataloggenehmigung zu starten.

1. Wählen Sie im Aktivitätsbereich der **Alle Kataloge**-Seite **Workflow \> Senden** aus.
1. Wechseln Sie zu **Einzelhandel und Handel \> Zentralverwaltungseinrichtung \> Handels-Workflows**, um die Schritte und berechtigten Benutzer für den Workflow zu konfigurieren. Der Workflow definiert die Schritte, die erforderlich sind, um den Katalog in den Status **Genehmigt** zu bringen.

### <a name="publish-the-catalog"></a>Den Katalog veröffentlichen

Nachdem ein Katalog den Status **Genehmigt** erhalten hat, können Sie ihn veröffentlichen, indem Sie **Veröffentlichen** im Menü **Kataloge** auswählen. Nachdem der Katalog in einem Status **Veröffentlicht** ist, kann er in der Callcenterauftragserfassung verwendet werden und Katalogprozesse senden. Sie können einen Katalog entweder manuell oder mithilfe eines Stapelverarbeitungsvorgangs veröffentlichen. Das Gültigkeitsdatum, das Sie für den Katalog definiert haben, bestimmt, wann die Produkte im Onlineshop verfügbar sind. Das Ablaufdatum, das Sie definiert haben, bestimmt, wann die Produkte aus dem Onlineshop entfernt werden.

> [!NOTE]
> Sie können einen Katalog veröffentlichen, der Produkte enthält, für die Warnungen vorhanden sind. Diese Produkte werden jedoch nicht im Onlineshop angezeigt.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Auswirkung der Erweiterbarkeit von Commerce-Katalogen auf B2B-Anpassungen](catalogs-b2b-sites-dev.md)

[FAQ zu Commerce-Katalogen für B2B](catalogs-b2b-sites-FAQ.md)

[Katalog-Picker-Modul](catalog-picker.md)
