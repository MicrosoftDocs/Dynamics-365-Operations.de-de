---
title: Commerce-Analysen (Vorschau)
description: In diesem Thema wird erläutert, wie Sie die Analysefunktion in Microsoft Dynamics 365 Commerce installieren und verwenden.
author: AamirAllaq
ms.date: 02/24/2022
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: aamiral
ms.search.validFrom: 2021-11-12
ms.openlocfilehash: 63d6e5ef7e883578106495d5ec778bbd686ee92d
ms.sourcegitcommit: 722854cb0d302d01ce3d9580ac80dc7c23d19bf5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/06/2022
ms.locfileid: "8550006"
---
# <a name="commerce-analytics-preview"></a>Commerce-Analysen (Vorschauversion)

[!include [banner](includes/banner.md)]

In diesem Thema wird erläutert, wie Sie Commerce-Analyse (Vorschau) installieren, die funktionale Analysefunktion, die in Microsoft Dynamics 365 Commerce enthalten ist.

## <a name="commerce-analytics-preview-live-demo"></a>Commerce-Analysen (Vorschau) – Live-Demo

Sie können eine [Live-Demo von Commerce-Analysen (Vorschau)](https://aka.ms/CommerceAnalyticsDemo) erhalten.

![Commerce-Analysen (Vorschau) – Zusammenfassung](media/CommerceAnalytics_Summary.png)
![Commerce-Analysen (Vorschau) – Zahlungen](media/CommerceAnalytics_Payments.png)
![Commerce-Analysen (Vorschau) – Webaktivität](media/CommerceAnalytics_WebActivity.png)

## <a name="commerce-analytics-preview-system-architecture"></a>Commerce-Analysen (Vorschau) – Systemarchitektur

### <a name="key-components"></a>Schlüsselkomponenten

Commerce-Analysen (Vorschau) bestehen aus den folgenden Schlüsselkomponenten:

- Gebrauchsfertige interaktive Power BI-Berichte
- SQL-Ansichten in Azure Synapse Analytics
- Entitäts- und Ontologiedaten in Azure Data Lake
- Rohdaten in Data Lake

![Schlüsselkomponenten der Commerce-Analysen-Systemarchitektur](media/CommerceAnalyticsArchitecture_v2.png)

### <a name="data-flow"></a>Datenfluss

#### <a name="step-1-data-generation"></a>Schritt 1: Datengenerierung

Daten stammen entweder als Transaktionsdaten oder Verhaltensdaten aus einer der folgenden Quellen:

- Ein Callcenter-Mitarbeiter verwendet den Commerce HQ-Client, um Kundenaufträge zu bearbeiten.
- Ein Kassierer am Point of Sale (POS) verarbeitet Verkaufstransaktionen.
- Verkäufe werden in benutzerdefinierten Anwendungen mithilfe von monitorlosem Commerce (Commerce Scale Unit) erstellt.
- Ein E-Commerce-Käufer durchsucht Ihre E-Commerce-Website.
- Ein E-Commerce-Käufer erteilt einen Auftrag auf Ihrer E-Commerce-Website.
- Daten werden von anderen Systemen erzeugt, wie z. B. Dynamics 365 Connected Spaces.

#### <a name="step-2-ingestion-and-pre-processing"></a>Schritt 2: Aufnahme und Vorverarbeitung

Transaktionsdaten gehen entweder direkt an Commerce HQ (bei Bestellungen, die direkt im Commerce HQ-Client erfasst werden) oder über Commerce Scale Unit (bei Bestellungen, die am POS, im E-Commerce oder in benutzerdefinierten Clients erfasst werden, die Kunden verwenden).

Die Funktion „In Data Lake exportieren“ wird dann verwendet, um die Transaktionsdaten als Rohdaten in Ihren Data Lake zu kopieren. Im Data Lake werden die Rohdaten im Tabellen-Ordner gespeichert.

E-Commerce-Webaktivitätsdaten werden direkt an den Data Lake gesendet. Daten, die von anderen Systemen erzeugt werden, wie z. B. Dynamics 365 Connected Spaces, wird von diesen Systemen direkt an den Data Lake gesendet.

#### <a name="step-3-transformation-and-aggregation"></a>Schritt 3: Transformation und Aggregation

Nachdem sich die Rohdaten in Ihrem Data Lake befinden, liest der Commerce-Analysedienst sie, transformiert sie, aggregiert sie und schreibt sie in Form von logischen Entitäten (im Entitäten-Ordner) und aggregierten Metriken (im Ontologien-Ordner) zurück in den Data Lake.

#### <a name="step-4-querying"></a>Schritt 4: Abfragen

Azure Synapse Analytics wird zur Abfrage von Daten in Ihrem Data Lake über eine Transact-SQL (T-SQL) Schnittstelle verwendet. Diese Schnittstelle enthält SQL-Ansichten. SQL-Ansichten ermöglichen die föderierte Abfrage von Daten im Data Lake, entweder direkt über einen T-SQL-Client (zur Ad-hoc-Analyse) oder über ein Visualisierungstool wie Power BI.

#### <a name="step-5-modeling-and-serving"></a>Schritt 5: Modellieren und servieren

Daten, die von Azure Synapse Analytics abgefragt werden, gehen an das semantische Modell von Power BI. Je nach Art der Daten werden sie entweder regelmäßig in den Arbeitsspeicher in Power BI importiert oder direkt zur Laufzeit abgefragt.

Schließlich werden die Daten in Power BI Visuals gerendert, damit Benutzer sie anzeigen und damit interagieren können.

## <a name="commerce-analytics-preview-functional-overview"></a>Funktionsübersicht Commerce-Analysen (Vorschau)

### <a name="summary"></a>Übersicht

Die Vorlagen-App für Commerce-Analysen umfasst die folgenden Hauptberichtsseiten:

1. [Filter der obersten Ebene](#TopLevelFilters)
2. [Produkte](#ProductsPage)
3. [Kunden](#CustomersPage)
4. [Benachrichtigungskanäle](#ChannelsPage)
5. [Umsatz](#SalesPage)
6. [Ränder](#MarginsPage)
7. [Rücklieferungen](#ReturnsPage)
8. [Rabatte](#DiscountsPage)
9. [Zahlungen](#PaymentsPage)
10. [Kunden](#CustomersPage)
11. [Vergleich](#ComparisonPage)
12. [Webaktivität](#WebActivityPage)
13. [Webaktivität – Filter der obersten Ebene](#WebActivityTopLevelFilters)

#### <a name="top-level-filters"></a><a name="TopLevelFilters"></a> Filter der obersten Ebene

- Datumseinstellungen

    - Jahr
    - Quartal
    - Monat
    - Woche
    - Tag

- Kanaleinstellungen

    - Juristische Person
    - Kanaltyp
    - Debitorentyp
    - Verkaufstyp
    - Kanal
    - Organisationshierarchie

- Produkteinstellungen

    - Kategoriehierarchie
    - Kategorie

#### <a name="products"></a><a name="ProductsPage"></a> Produkte

- Vertrieb
- Rand
- Rücklieferungen

#### <a name="customers"></a><a name="CustomersPage"></a> Kunden

- Vertrieb
- Rand
- Rücklieferungen

#### <a name="channels"></a><a name="ChannelsPage"></a> Kanäle

- Vertrieb
- Rand
- Rücklieferungen

### <a name="sales"></a>Vertrieb <a name="SalesPage"></a>

- Nach Lieferort
- Nach Kanal/Geschäft/Terminal
- Nach Mitarbeiter
- Nach Datum
- Nach Stunde
- Nach Produktkategorie

### <a name="margins"></a><a name="MarginsPage"></a> Ränder

- Nach Lieferort
- Nebenprodukt
- Nach Datum

### <a name="returns"></a><a name="ReturnsPage"></a> Rücklieferungen

- Rücklieferungen nach Betrag

    - Nach Shop
    - Nebenprodukt
    - Nach Datum

- Retoure nach Buchung

    - Nach Shop
    - Nebenprodukt
    - Nach Datum

### <a name="discounts"></a><a name="DiscountsPage"></a> Rabatte

- Nach Shop
- Nebenprodukt
- Nach Datum
- Aufschlüsselung

    - Juristische Person
    - Shop
    - Rabatttyp
    - Rabattname
    - Produkt

### <a name="payments"></a><a name="PaymentsPage"></a> Zahlungen

- Nach Kanal/Terminal
- Nach Zahlungsmethode/-typ
- Nach Datum
- Aufschlüsselung

    - Juristische Person
    - Kanaltyp
    - Shop
    - Terminal
    - Zahlungsweise

### <a name="customers"></a><a name="CustomersPage"></a> Kunden

- Lebensdauerwert (LTV)

    Der LTV wird basierend auf dem Gesamtbetrag berechnet, den ein Kunde für alle Dynamics 365 Commerce-Vertriebskanäle (einschließlich POS, E-Commerce und Call Center) ausgibt.

- Aktualität

    Die Aktualität wird basierend auf der Anzahl der Tage seit der letzten Transaktionsbeziehung eines Kunden mit der Organisation berechnet. Derzeit berücksichtigt die Aktualität keine nicht-transaktionalen Interaktionssignale, wie z. B. E-Commerce-Browsing-Aktivitäten.

- Häufigkeit

    Die Häufigkeit wird basierend auf der Transaktionsbeziehung eines Kunden mit der Organisation berechnet. Derzeit berücksichtigt die Häufigkeit keine nicht-transaktionalen Interaktionssignale, wie z. B. E-Commerce-Browsing-Aktivitäten.

- Beziehungsdauer

    Die Beziehungsdauer wird basierend auf der Anzahl der Tage berechnet, seit der Kundendatensatz im System erstellt wurde.

- Transaktionszahl

### <a name="comparison"></a><a name="ComparisonPage"></a> Vergleich

- Produktvergleich nach Zeitraum

    - Vertrieb und Vertriebsdifferenz
    - Marge und Margendifferenz

- Debitorumsatz nach Zeitperiode

    - Vertrieb und Vertriebsdifferenz
    - Marge und Margendifferenz

### <a name="web-activity"></a><a name="WebActivityPage"></a> Webaktivität

#### <a name="top-level-filters"></a><a name="WebActivityTopLevelFilters"></a> Filter der obersten Ebene

- Datumsbereich
- Kanaltyp
- Kanal
- Kategoriehierarchie

#### <a name="acquisitions"></a>Anschaffungen

- Seitenansichten

    - Nach Land oder Region
    - Nebenprodukt
    - Nach Anmeldestatus des Benutzers
    - Nach Datum

- E-Commerce-Bestellungen
- Wechselkurs

    - Nach Datum

- Konversionstrichter

    - Seitenaufruf nach Seitentyp (Startseite, Kategorieseite oder Produktdetailseite)
    - In den Einkaufswagen
    - Kasse
    - Kaufen

#### <a name="sessions"></a>Sitzungen

Eine Sitzung ist eine Episode des Besuchs eines Benutzers auf Ihrer E-Commerce-Website. Eine Sitzung gilt nach 30 Minuten Inaktivität oder 24 Stunden aktiver Nutzung als beendet.

- Nach Land oder Region
- Nach Herkunft (externer Referrer)
- Nach Anmeldestatus des Benutzers
- Sitzungsanzahl

    - Nach Datum
    - Nach Eintragsseite

- Bestellung pro Sitzung

    - Nach Datum

- Absprungrate der Sitzung

    Ein Sitzungsabsprung ist eine Sitzung, bei der ein Benutzer sofort nach dem Besuch Ihrer E-Commerce-Website verlässt. Weitere Informationen finden Sie unter [Absprungrate](https://en.wikipedia.org/wiki/Bounce_rate).

- Klicks pro Sitzung

#### <a name="visitors"></a>Besucher

Ein anonymer Besucher auf Ihrer E-Commerce-Site wird anhand des spezifischen Browsers und des spezifischen Geräts, das der Benutzer verwendet, eindeutig identifiziert. Commerce-Analysen verfolgen keine anonymen Besucher über verschiedene Browser oder Geräte hinweg. Ein anonymer Besucher, der denselben Browser auf demselben Gerät verwendet, wird über mehrere Benutzersitzungen hinweg eindeutig identifiziert, bis entweder die zwischengespeicherten Daten des Browsers gelöscht werden oder ein Zeitraum (normalerweise 12 Monate) verstreicht, je nachdem, was zuerst eintritt.

Wenn Besucher Ihre E-Commerce-Site durchsuchen, während sie angemeldet sind, kann Commerce-Analysen zusätzliche Informationen über sie bereitstellen. Diese Informationen basieren auf der bestehenden Beziehung, die Ihre Organisation mit den Besuchern aufgrund ihrer früheren Einkäufe unterhält. Dynamics 365 Commerce-Vertriebskanäle (einschließlich POS, E-Commerce und Call Center). Die zusätzlichen Informationen umfassen Aktualität, Beziehungslänge, Lebensdauerwert und Häufigkeitsdaten.

- Besuchermarge
- Durchschnittliche Bestellungen der Besucher
- Durchschnittliche Verkäufe der Besucher
- Besucherzahl im E-Commerce

    - Nach Datum
    - Nach Ort

        Derzeit kann die Commerce-Analyse nur eine Granularität auf Länder-/Regionsebene für Standortinformationen für E-Commerce-Besucher bereitstellen.

    - Nach Aktualität

        Die Aktualität wird basierend auf der Anzahl der Tage seit der letzten Transaktionsbeziehung eines Kunden mit der Organisation berechnet. Derzeit berücksichtigt die Aktualität keine nicht-transaktionalen Interaktionssignale, wie z. B. E-Commerce-Browsing-Aktivitäten.

    - Nach Beziehungsdauer

        Die Beziehungsdauer wird basierend auf der Anzahl der Tage berechnet, seit der Kundendatensatz im System erstellt wurde.

    - Nach Lebensdauerwert (LTV)

        Der LTV wird basierend auf dem Gesamtbetrag berechnet, den ein Kunde für alle Dynamics 365 Commerce-Vertriebskanäle (einschließlich POS, E-Commerce und Call Center) ausgibt.

    - Nach Lohnzahlungshäufigkeit

        Die Häufigkeit wird basierend auf der Transaktionsbeziehung eines Kunden mit der Organisation berechnet. Derzeit berücksichtigt die Häufigkeit keine nicht-transaktionalen Interaktionssignale, wie z. B. E-Commerce-Browsing-Aktivitäten.

#### <a name="impressions"></a>Aufrufe

Ein Aufruf ist eine einzelne Ansicht einer Produktvisualisierung durch einen E-Commerce-Besucher. Zum Beispiel geht ein E-Commerce-Besucher auf die Startseite Ihrer E-Commerce-Website und sieht sich ein Yogamatten-Produkt in einem **Meistverkauft**-Listenmodul an. Der Besucher sieht dann das gleiche Yogamattenprodukt in einem **Entnahmen für Sie**-Listenmodul. In diesem Fall gibt es zwei Produktimpressionen.

Derzeit werden Impressionen in den folgenden Oberflächen verfolgt:

- Listen (zum Beispiel **Empfohlen**, **Meistverkauft**, **Entnahmen für Sie** und **Im Trend**)
- Einkaufswagenmodul
- Suchergebniscontainer
- Kategoriesuchergebniscontainer

Derzeit werden Produkte, die in einem Karussellmodul oder in benutzerdefinierten Visualisierungen gerendert werden, nicht in impressionsbezogenen Messwerten gezählt.

Die Seite **Impressionsbericht** enthält die folgenden Kennzahlen:

- Impressionsanzahl

    - Nach Seitentyp und Modul

        Seitentyp ist der generische Seitentyp, der für jede Seite auf Ihrer E-Commerce-Website definiert wird. Modultyp ist der Typ des visuellen E-Commerce-Moduls, in dem das Produkt angezeigt wird.

        Um Impressionen nach Modul anzuzeigen, müssen Sie möglicherweise einen Drilldown in die Seiten- und Modulvisualisierungen durchführen.

    - Nebenprodukt
    - Nach Anmeldestatus des Benutzers
    - Nach Datum

- Impressionsklickanzahl

    Ein Impression-Klick tritt auf, wenn ein E-Commerce-Besucher ein Produktvisualisierung auswählt. Normalerweise wird der Besucher dann auf die Produktdetailseite für das Produkt geleitet.

- Klickrate der Impressionen (CTR)

    Die CTR wird berechnet als die Gesamtzahl der Impression-Klicks geteilt durch die Gesamtzahl der Impressionen.

## <a name="commerce-analytics-preview-installation"></a>Commerce-Analysen (Vorschau) – Installation

> [!NOTE]
> Commerce-Analyse (Vorschau) ist in den Regionen USA, Kanada, Vereinigtes Königreich, Europa, Südostasien, Ostasien, Australien und Japan in der Vorschau verfügbar. Wenn sich Ihre Finance + Operations Umgebung in einer dieser Regionen befindet, können Sie diese Funktion in Ihrer Umgebung aktivieren, indem Sie Microsoft Dynamics Lifecycle Services (LCS) verwenden. Bevor Sie diese Funktion verwenden können, lesen Sie [Export in Azure Data Lake konfigurieren](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).

### <a name="enable-and-configure-commerce-analytics-preview"></a><a name="enableCommerceAnalytics"></a>Aktivieren und Konfigurieren von Commerce-Analysen (Vorschau)

Um Commerce-Analysen (Vorschau) zu installieren, müssen Sie über Berechtigungen zum Erstellen von Ressourcen in einem Azure-Abonnement verfügen. Sie müssen auch über Berechtigungen zum Installieren von Add-Ins in LCS verfügen.

Gehen Sie folgendermaßen vor, um Commerce Analytics (Vorschau) zu aktivieren und zu konfigurieren.

1. [Senden Sie das Vorschau-Eingangsformular für Commerce-Analysen (Vorschauversion)](#joinPreview)
2. [Aktivieren und konfigurieren Sie das Add-In Export to Data Lake](#enableExportToDataLake).
3. [Installieren und konfigurieren Sie einen Azure Synapse Workspace](#configureAzureSynapse).
4. [Hinzufügen von Geheimnissen zum Key Vault](#addSecrets).
5. [Aktivieren und Konfigurieren von Commerce-Analysen (Vorschau)](#enableCommerceAnalyticsAddin)
6. [Power BI-Vorlagen-App installieren](#powerbi).

### <a name="submit-the-preview-intake-form-for-commerce-analytics-preview"></a><a name="joinPreview"></a>Senden Sie das Vorschau-Eingangsformular für Commerce-Analysen (Vorschau).

Senden Sie das [Vorschau-Eingangsformular für Commerce-Analysen (Vorschau)](https://forms.office.com/r/vW5VLJGXZ2). Nach der Bearbeitung wird eine Bestätigungs-E-Mail an die E-Mail-Adresse gesendet, die Sie im Formular angegeben haben.

### <a name="enable-and-configure-the-export-to-data-lake-add-in"></a><a name="enableExportToDataLake"></a>Aktivieren und konfigurieren Sie das Add-In Export to Data Lake

> [!IMPORTANT]
> Wenn Sie das Add-In Export to Data Lake konfigurieren, deaktivieren Sie das Kontrollkästchen **Echtzeitdatenänderungen** auf der Einrichtungsseite des Add-Ins Export to Data Lake, um sicherzustellen, dass Echtzeitdatenänderungen nicht aktiviert sind. Die Funktion **Echtzeitdatenänderungen** befindet sich in der Vorschau und wird derzeit von Commerce Analytics nicht unterstützt. Wenn Sie die Funktion aktivieren, kann Commerce Analytics Ihre Daten im Data Lake nicht verarbeiten, und die meisten Ihrer Power BI-Berichte werden keine Daten anzeigen.

Commerce Analytics (Vorschau) verlässt sich auf die Funktion Export to Data Lake, um die Daten der Commerce-Zentrale nach Data Lake zu exportieren und die Daten aktuell zu halten. Bevor Sie Commerce-Analysen (Vorschau) konfigurieren, aktivieren und konfigurieren Sie den Export nach Data Lake, indem Sie die Schritte in [Export in Azure Data Lake konfigurieren](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md) ausführen.

Notieren Sie sich bei der Konfiguration des Add-Ins Export to Data Lake die folgenden Informationen, da Sie sie später eingeben müssen:

- <a name="keyVault"></a>Der Domain Name System (DNS) Name des Key Vault, den Sie angegeben haben.
- Die geheimen Namen, die Sie angegeben haben und die die Anwendungs-ID und das Anwendungsgeheimnis enthalten. Weitere Informationen finden Sie unter [Geheimnisse zum Schlüsseltresor hinzufügen](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#addsecrets).

### <a name="install-and-configure-an-azure-synapse-workspace"></a><a name="configureAzureSynapse"></a>Installieren und konfigurieren Sie einen Azure Synapse Workspace.

Commerce Analytics (Vorschau) erfordert, dass Synapse SQL on-demand in Ihrem Azure Synapse workspace bereitgestellt wird. Führen Sie die folgenden Schritte aus, um einen Azure Synapse Workspace zu installieren und zu konfigurieren.

1. Installieren Sie einen Azure Synapse Workspace in Ihrem Azure-Abonnement. Weitere Informationen finden Sie unter [Schnellstart: Einen Synapse Workspace erstellen](/azure/synapse-analytics/quickstart-create-workspace).
1. <a name="serverlessep"></a>Nachdem der Arbeitsbereich bereitgestellt wurde, öffnen Sie die Seite mit der Ressourcenübersicht und notieren Sie sich den Wert **Serverless SQL Endpunkt**. Im nächsten Abschnitt müssen Sie diesen Wert im Key Vault speichern.
1. Auf der Übersichtsseite wählen Sie den Link **Synapse Studio öffnen**, um das Studio Azure Synapse für Ihren Arbeitsbereich zu öffnen.
1. Wählen Sie **Verwalten** im linken Menü. Um die Menünamen zu sehen, müssen Sie eventuell den Link Erweitern im linken Menü wählen.
1. Wählen Sie unter **Sicherheitsgruppe** die Option **Zugriffssteuerung**. 
1. Wählen Sie **Hinzufügen** aus.
1. Legen Sie im Bereich **Rollenzuweisung hinzufügen** die Optionen wie in der folgenden Tabelle beschrieben fest.

    | Option | Wert |
    |--------|-------|
    | Bereich | Wählen Sie **Arbeitsbereich**. |
    | Rolle | Wählen Sie **Synapse SQL Administrator**.|
    | Benutzer auswählen | Suchen Sie nach dem Namen der Anwendung, die Sie [bei der Installation des Add-Ins Export to Data Lake erstellt haben](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#createapplication). Wenn die Anwendung in den Suchergebnissen erscheint, wählen Sie sie aus. Die Anwendung erscheint nun im Bereich **Ausgewählte(r) Benutzer, Gruppe(n) oder Dienstprinzipal(e)**. |

1. Wählen Sie **Anwenden**, um die Rollenzuweisung abzuschließen. Die Anwendung erhält die Rechte eines Synapse SQL-Administrators. Daher kann es die erforderlichen Ansichten während der Konfiguration des Commerce Analytics (Vorschau) LCS Add-Ins erstellen.

### <a name="add-secrets-to-the-key-vault"></a><a name="addSecrets"></a>Geheimnisse zum Key Vault hinzufügen

In demselben [Key Vault](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#createkeyvault), den Sie bei der Konfiguration des Add-Ins Export to Data Lake verwendet haben, müssen Sie die Geheimnisse hinzufügen, die in der folgenden Tabelle aufgeführt sind. Für jedes Geheimnis müssen Sie einen Geheimnamen und den angegebenen Wert angeben.

| Vorgeschlagener Geheimname | Geheimer Wert | Beispiel für einen geheimen Wert |
|---------|---------|---------|
| synapse-sql-server | Der Wert des serverlosen SQL-Endpunkts, den Sie bei der [Konfiguration des Azure Synapse workspace](#serverlessep) notiert haben. | `test-ondemand.sql.azuresynapse.net` |
| <a name="roUser"></a>nur-lesen-sql-pwd | Das Kennwort, das für den schreibgeschützten SQL-Benutzer festgelegt werden soll. Der Power BI-Bericht verwendet dieses Kennwort, um sich mit dem serverlosen SQL zu verbinden. Um das Kennwort festzulegen, befolgen Sie die Richtlinien Ihres Unternehmens für Kennwörter. | |

### <a name="enable-and-configure-the-commerce-analytics-preview-add-in"></a><a name="enableCommerceAnalyticsAddin"></a>Aktivieren und Konfigurieren von Commerce-Analysen (Vorschau)

Um das Commerce-Analyse-Add-In (Vorschau) in LCS zu installieren, müssen Sie ein Umgebungsadministrator in LCS für die Umgebung sein, die Sie verwenden möchten.

Um das Add-In der Commerce-Analysen (Vorschau) zu installieren und zu konfigurieren, folgen Sie diesen Schritten.

1. Melden Sie sich bei [LCS](https://lcs.dynamics.com/) an und gehen Sie zu Ihrer Umgebung.
2. Wählen Sie auf der Seite **Umgebungen** auf der Registerkarte **Umgebungs-Add-Ins** die Option **Neues Add-In installieren** aus.
3. Wählen Sie im Dialogfeld **Commerce-Analysen (Vorschau)**.
4. Geben Sie im Dialogfeld **Add-In einrichten** die folgenden Informationen ein.

    | Informationen | Grundlage | Beispielswert |
    |---|---|---|
    | Azure Active Directory (Azure AD) Mandant ID | Melden Sie sich bei beim [Azure-Portal](https://portal.azure.com/) an, und öffnen Sie den **Azure Active Directory**-Service. Öffnen Sie dann die Seite **Eigenschaften** und kopieren Sie den Wert in das Feld **Mandanten-ID**. | `72f988bf-0000-0000-00000-2d7cd011db47` |
    | DNS-Name Ihres Azure Key Vault | DNS-Namen Ihres Schlüsseltresors eingeben. Sie sollten sich diesen Wert notiert haben, während Sie [das Add-In Export to Data Lake konfiguriert haben](#keyVault). | `https://contosod365datafeedpoc.vault.azure.net/` |
    | Geheimer Name, der die Anwendungs-ID enthält | Geben Sie den geheimen Namen ein, der die Anwendungs-ID speichert. Sie sollten sich diesen Wert notiert haben, während Sie [das Add-In Export to Data Lake konfiguriert haben](#keyVault). | `app-id` |
    | Geheimer Name, der das Anwendungsgeheimnis enthält | Geben Sie den geheimen Namen ein, der das Anwendungsgeheimnis speichert. Sie sollten sich diesen Wert notiert haben, während Sie [das Add-In Export to Data Lake konfiguriert haben](#keyVault). | `app-secret` |
    | Geheimer Name, der den serverlosen SQL-Endpunkt für Azure Synapse enthält | Geben Sie den geheimen Namen ein, unter dem der serverlose SQL-Endpunkt gespeichert ist. Sie hätten das Geheimnis erstellen sollen, während Sie die [Geheimnisse zum Schlüsselwert hinzugefügt haben](#addSecrets). | `synapse-sql-server` |
    | Geheimer Name, der das Kennwort enthält, das für schreibgeschützte SQL-Benutzer in Azure Synapse festgelegt werden soll | Geben Sie den geheimen Namen ein, unter dem das Kennwort gespeichert ist, das für den schreibgeschützten SQL-Benutzer festgelegt werden soll. Dieser Benutzer wird für Sie erstellt und sollte im Bericht Power BI verwendet werden, um sich mit dem serverlosen SQL-Server zu verbinden. Sie sollten das Geheimnis erstellt haben, während Sie [Geheimnisse zum Schlüsselwert hinzugefügt haben](#addSecrets). | `readonly-sql-pwd` |

1. Akzeptieren Sie die Angebotsbedingungen, indem Sie das Kontrollkästchen aktivieren und dann **Installieren** auswählen.

    Das System installiert und konfiguriert das Commerce-Analysen (Vorschau)-Add-In für die Umgebung. Dieser Prozess kann einige Minuten in Anspruch nehmen. Nach Abschluss sollte **Commerce-Analysen (Vorschau)-** auf der **Umgebungs**-Seite aufgeführt werden, und der Status sollte **Installiert** sein.

### <a name="install-the-power-bi-template-app"></a><a name="powerbi"></a>Power BI -Vorlagen-App installieren.

Um die Power BI-Vorlagen-App für Commerce-Analysen (Vorschau) zu installieren und zu konfigurieren, folgen Sie diesen Schritten.

1. Melden Sie sich beim [Power BI-Portal](https://powerbi.microsoft.com/) an, indem Sie Ihre Organisations-ID verwenden.
1. Installieren Sie die Commerce-Analyse (Vorschau) Power BI-Vorlagen-App unter [https://aka.ms/cdireport-installapp](https://aka.ms/cdireport-installapp). Alternativ besuchen Sie die [AppSource Seite für Dynamics 365 Commerce Analytics](https://appsource.microsoft.com/product/power-bi/dynamics-365-commerce.dydnamics-365-commerce-analytics) und wählen **Jetzt holen**.
1. Wenn Sie die App zum ersten Mal neu installieren, fahren Sie mit Schritt 5 fort. Wenn Sie die App bereits installiert haben, gelten die folgenden Optionen für die Aktualisierung der App:

    - **Aktualisieren Sie den Arbeitsbereich und die App** – Aktualisieren Sie die vorhandene Vorlagen-App und überschreiben Sie Ihre vorhandenen App-Einstellungen, z. B. den Namen der App-Instanz und die Berechtigungskonfigurationen.
    - **Nur Workspace-Inhalte aktualisieren, ohne die App zu aktualisieren** – Aktualisieren Sie die vorhandene Vorlagen-App, behalten Sie jedoch Ihre vorhandenen App-Einstellungen bei. *Diese Option ist die empfohlene Option für App-Updates.*
    - **Installieren Sie eine weitere Kopie der App in einem neuen Arbeitsbereich** – Erstellen Sie einen neuen Arbeitsbereich und erstellen Sie dann eine Kopie der vorhandenen Vorlagen-App darin. Der vorhandene Arbeitsbereich bleibt erhalten.

1. Wählen Sie eine der Update-Optionen und dann **Installieren**.
1. Öffnen Sie die installierte App, indem Sie **Apps** im linken Bereich auswählen, und wählen Sie dann die App aus.
1. Verbinden Sie die App mit Ihrer Datenquelle, indem Sie **Verbinden** auswählen. Wenn Sie die App bereits installiert haben, wählen Sie den **Daten verbinden**-Link in der gelben Nachrichtenleiste.
1. Stellen Sie die folgenden Felder ein.

    | Feld | Wert |
    |---|---|
    | Server | Geben Sie den serverlosen SQL-Endpunkt ein, den Sie sich notiert haben, nachdem Sie [den Azure Synapse workspace erstellt haben](#serverlessep). |
    | Datenbank | Geben Sie **CommerceAnalytics** ein. |
    | Sprache | Wählen Sie einen Wert in der Liste aus. Dieses Feld wird für lokalisierte Produkt- und Kategorienamen verwendet. Der Wert beachtet die Groß-/Kleinschreibung. |
    | Datumsbereich | Wählen Sie einen Wert in der Liste aus. Die Daten für die ausgewählte Anzahl von Monaten werden in das Power BI-DataSet importiert. Der von Ihnen ausgewählte Wert wirkt sich auf die Größe des DataSets und die für die Synchronisierung erforderliche Zeit aus. |

1. Wählen Sie **Weiter**. Wenn Sie aufgefordert werden, die Anmeldeinformationen für die Verbindung mit der SQL-Datenbank Azure Synapse einzugeben, legen Sie die Feldwerte fest, wie in der folgenden Tabelle gezeigt.

    | Feld | Wert |
    |---|---|
    | Authentifizierungsmethode | Wählen Sie **Basic** aus. |
    | Benutzername | Geben Sie **reportreadonlyuser** ein. |
    | Kennwort | Geben Sie das Kennwort ein, das Sie [für den schreibgeschützten SQL-Benutzer im Key Vault gespeichert haben](#roUser). |

1. Wählen Sie **Anmelden und verbinden** aus.
1. Warten Sie, bis das Dataset erfolgreich aktualisiert wurde. Wählen Sie dann **App bearbeiten**, um den Arbeitsbereich für Apps zu öffnen, in dem Sie den Aktualisierungsstatus des Datasets einsehen können. Im App-Arbeitsbereich können Sie optional auch automatische Aktualisierungszeitpläne für Ihr DataSet einrichten, Berechtigungen verwalten und die App-Instanz umbenennen.

### <a name="privacy"></a><a name="privacy"></a>Vertraulichkeit

Datenschutz ist uns sehr wichtig. Weiteres erfahren Sie in unserer [Datenschutzerklärung](https://go.microsoft.com/fwlink/?LinkId=521839).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
