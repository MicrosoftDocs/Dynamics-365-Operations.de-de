---
title: Commerce-Analysen (Vorschau)
description: In diesem Thema wird erläutert, wie Sie die Analysefunktion in Microsoft Dynamics 365 Commerce installieren und verwenden.
author: AamirAllaq
ms.date: 11/23/2021
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: aamiral
ms.search.validFrom: 2021-11-12
ms.openlocfilehash: 8cfe2af756315b5be3eb22d99376a96166fffc52
ms.sourcegitcommit: f9fca3d55b47e615e5ef64669dab184e057ec234
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/23/2021
ms.locfileid: "7862772"
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
- SQL-Ansichten in Azure Synapse-Analysen
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

Azure Synapse Analytics wird verwendet, um Daten in Ihrem Data Lake über eine Transact-SQL (T-SQL)-Schnittstelle abzufragen. Diese Schnittstelle enthält SQL-Ansichten. SQL-Ansichten ermöglichen die föderierte Abfrage von Daten im Data Lake, entweder direkt über einen T-SQL-Client (zur Ad-hoc-Analyse) oder über ein Visualisierungstool wie Power BI.

#### <a name="step-5-modeling-and-serving"></a>Schritt 5: Modellieren und servieren

Daten, die von Azure Synapse Analytics abgefragt werden gehen an das semantische Power BI-Modell. Je nach Art der Daten werden sie entweder regelmäßig in den Arbeitsspeicher in Power BI importiert oder direkt zur Laufzeit abgefragt.

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

####  <a name="top-level-filters"></a><a name="TopLevelFilters"></a> Filter der obersten Ebene

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

####  <a name="products"></a><a name="ProductsPage"></a> Produkte

- Vertrieb
- Rand
- Rücklieferungen

####  <a name="customers"></a><a name="CustomersPage"></a> Kunden

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
> Commerce-Analyse (Vorschau) ist in den Regionen USA, Kanada, Vereinigtes Königreich, Europa, Südostasien, Ostasien, Australien und Japan in der Vorschau verfügbar. Wenn Ihre Finance and Operations-Umgebung in einer dieser Regionen befindet, können Sie diese Funktion in Ihrer Umgebung aktivieren, indem Sie Microsoft Dynamics Lifecycle Services (LCS) verwenden. Bevor Sie diese Funktion verwenden können, lesen Sie [Export in Azure Data Lake konfigurieren](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).

### <a name="enable-and-configure-commerce-analytics-preview"></a><a name="enableCommerceAnalytics"></a>Aktivieren und Konfigurieren von Commerce-Analysen (Vorschau)

Um Commerce-Analysen (Vorschau) zu installieren, müssen Sie über Berechtigungen zum Erstellen von Ressourcen in einem Azure-Abonnement verfügen. Sie müssen auch über Berechtigungen zum Installieren von Add-Ins in LCS verfügen. Hier ein Überblick über die Schritte:

1. [Senden Sie das Vorschau-Eingangsformular für Commerce-Analysen (Vorschau)](#joinPreview).
2. [Export in Data Lake Add-in aktivieren und konfigurieren](#enableExportToDataLake).
3. [Aktivieren und Konfigurieren von Commerce-Analysen (Vorschau)](#enableCommerceAnalyticsAddin)
4. [Generieren Sie ein Shared Access Signature (SAS)-Token für Ihr Speicherkonto](#getSASToken).
5. [Laden Sie die Bereitstellungsskripte für Azure Synapse-Ansichten herunter](#downloadSynapseDeploymentScripts).
6. [Installieren und konfigurieren Sie einen Azure Synapse Workspace](#configureAzureSynapse).
7. [Power BI-Vorlagen-App installieren](#powerbi).

### <a name="submit-the-preview-intake-form-for-commerce-analytics-preview"></a><a name="joinPreview"></a>Senden Sie das Vorschau-Eingangsformular für Commerce-Analysen (Vorschau).

Senden Sie das [Vorschau-Eingangsformular für Commerce-Analysen (Vorschau)](https://forms.office.com/r/vW5VLJGXZ2). Die Bearbeitung des Formulars kann bis zu drei Werktage dauern. Nach der Bearbeitung wird eine Bestätigungs-E-Mail an die E-Mail-Adresse gesendet, die Sie im Formular angegeben haben.

### <a name="enable-and-configure-export-to-data-lake"></a><a name="enableExportToDataLake"></a>Export in Data Lake Add-in aktivieren und konfigurieren.

Commerce-Analysen (Vorschau) basieren auf der Export nach Data Lake-Funktion, um Commerce HQ-Daten nach Data Lake zu exportieren und die Daten aktuell zu halten. Bevor Sie Commerce-Analysen (Vorschau) konfigurieren, aktivieren und konfigurieren Sie den Export nach Data Lake, indem Sie die Schritte in [Export in Azure Data Lake konfigurieren](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md) ausführen.

Notieren Sie sich beim Konfigurieren von Export nach Data Lake die folgenden Informationen, da Sie diese später eingeben müssen:

- <a name="keyVault"></a>Der Domain Name System (DNS)-Name des Schlüsseltresors und die geheimen Namen, in denen Sie die Anwendungs-ID und das Anwendungsgeheimnis speichern. Weitere Informationen finden Sie unter [Geheimnisse zum Schlüsseltresor hinzufügen](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#addsecrets).
- <a name="storageAccount"></a>Der Name des Speicherkontos für die Data Lake-Instanz. Weitere Informationen finden Sie unter [Erstellen Sie ein Data Lake Storage (Gen2)-Konto in Ihrem Abonnement](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#createsubscription).

### <a name="enable-and-configure-the-commerce-analytics-preview-add-in"></a><a name="enableCommerceAnalyticsAddin"></a>Aktivieren und Konfigurieren von Commerce-Analysen (Vorschau)

Um das Commerce-Analyse-Add-In (Vorschau) in LCS zu installieren, müssen Sie ein Umgebungsadministrator in LCS für die Umgebung sein, die Sie verwenden möchten.

Um das Add-In der Commerce-Analysen (Vorschau) zu installieren und zu konfigurieren, folgen Sie diesen Schritten.

1. Melden Sie sich bei [LCS](https://lcs.dynamics.com/) an und gehen Sie zu Ihrer Umgebung.
2. Wählen Sie auf der Seite **Umgebungen** auf der Registerkarte **Umgebungs-Add-Ins** die Option **Neues Add-In installieren** aus.
3. Wählen Sie im Dialogfeld **Commerce-Analysen (Vorschau)**.

    Wenn **Commerce-Analysen (Vorschau)** nicht aufgeführt ist, vergewissern Sie sich, dass Sie dem Insider-Programm beigetreten sind.

4. Geben Sie im Dialogfeld **Add-In einrichten** die folgenden Informationen ein.

    | Informationen | Grundlage | Beispielswert |
    |---|---|---|
    | Azure AD-Mandanten-ID für Ihre Umgebung | Melden Sie sich bei beim [Azure-Portal](https://portal.azure.com/) an, und öffnen Sie den **Azure Active Directory**-Service. Öffnen Sie dann die **Eigenschaften**-Seite und kopieren Sie den Wert in das **Verzeichnis-ID**-Feld. | 72f988bf-0000-0000-00000-2d7cd011db47 |
    | DNS-Name Ihres Schlüsseltresors | [DNS-Namen](#keyVault) Ihres Schlüsseltresors eingeben. Diesen Wert hätten Sie sich im vorherigen Abschnitt notieren müssen. | `https://contosod365datafeedpoc.vault.azure.net/` |
    | Geheimnis, das die Anwendungs-ID enthält | Geben Sie den [geheimen Namen ein, der die Anwendungs-ID speichert](#keyVault). Diesen Wert hätten Sie sich im vorherigen Abschnitt notieren müssen. | app-id |
    | Geheimnis, das das Anwendungsgeheimnis enthält | Geben Sie den [geheimen Namen ein, der das Anwendungsgeheimnis speichert](#keyVault). Diesen Wert hätten Sie sich im vorherigen Abschnitt notieren müssen. | app-secret |

5. Akzeptieren Sie die Angebotsbedingungen, indem Sie das Kontrollkästchen aktivieren und dann **Installieren** auswählen.

    Das System installiert und konfiguriert das Commerce-Analysen (Vorschau)-Add-In für die Umgebung. Dieser Prozess kann einige Minuten in Anspruch nehmen. Nach Abschluss sollte **Commerce-Analysen (Vorschau)-** auf der **Umgebungs**-Seite aufgeführt werden, und der Status sollte **Installiert** sein.

### <a name="generate-a-sas-token-for-your-storage-account"></a><a name="getSASToken"></a>Generieren Sie ein SAS-Token für Ihr Speicherkonto

Ein SAS-Token ermöglicht externen Entitäten den Zugriff auf Ihr Speicherkonto und verfügt über einen bestimmten Satz von Berechtigungen für einen begrenzten Zeitraum. Azure Synapse verwendet das SAS-Token, um auf die zugrunde liegenden Daten in Data Lake zuzugreifen.

> [!NOTE]
> Aufgrund einer bekannten Einschränkung der Commerce-Analyse (Vorschau) verliert die Azure Synapse-Instanz den Zugriff auf den Data Lake, wenn das SAS-Token abläuft. Daher sollten Sie beim Generieren des SAS-Tokens das maximale Ablaufdatum festlegen, das die Sicherheitsrichtlinien Ihrer Organisation zulassen.

Gehen Sie wie folgt vor, um ein SAS-Token zu generieren.

1. Wechseln Sie im Azure-Portal zum [Speicherkonto](#storageAccount), das Sie erstellt haben, während Sie den Export nach Data Lake konfiguriert haben.
2. Wählen Sie im linken Bereich unter dem Speicherkonto **Gemeinsame Zugriffssignatur**.
3. Auf der Seite **SAS-Optionen** setzen Sie die folgenden Felder fest.

    | Feld | Wert |
    |---|---|
    | Zulässige Dienste | Wählen Sie **Blob**. |
    | Zulässige Ressourcentypen | Wählen Sie **Service**, **Container** und **Objekt** aus. |
    | Zulässige Berechtigungen | Wählen Sie **Lesen**, **Schreiben**, **Löschen**, **Auflisten**, **Hinzufügen** und **Erstellen**. |
    | Berechtigungen für die Blob-Versionsverwaltung | Wählen Sie **Ermöglicht das Löschen von Versionen**. |
    | Start- und Ablaufdatum/-zeit | Legen Sie ein Start- und Enddatum sowie eine entsprechende Uhrzeit für das SAS-Token fest. |
    | Zulässige IP-Adressen | Lassen Sie dieses Feld leer. |
    | Zulässige Protokolle | Wählen Sie **Nur HTTPS**. |
    | Bevorzugte Routing-Stufe | Wählen Sie **Basis (Standard)**. |
    | Signaturschlüssel | Wählen Sie **Schlüssel1** oder **Schlüssel2** nach Bedarf. |

4. Wählen Sie **SAS und Verbindungszeichenfolge generieren**.
5. Kopieren Sie den Wert ins **SAS-Token**-Feld und fügen Sie es in einen Texteditor wie Notepad ein.

### <a name="download-the-deployment-scripts-for-azure-synapse-views"></a><a name="downloadSynapseDeploymentScripts"></a>Laden Sie die Bereitstellungsskripte für Azure Synapse-Ansichten herunter.

Zum Erstellen und Veröffentlichen der erforderlichen Ansichten in einem Azure Synapse Workspace müssen Sie eine Reihe von Skripts ausführen. Befolgen Sie diese Schritte, um die Skripts herunterzuladen.

1. Gehen Sie auf GitHub zum [microsoft/Dynamics365Commerce.Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions)-Repository (repo).
2. Laden Sie die Skripts auf Ihren lokalen Computer herunter, indem Sie das Repository klonen oder als ZIP-Datei herunterladen.

### <a name="install-and-configure-an-azure-synapse-workspace"></a><a name="configureAzureSynapse"></a>Installieren und konfigurieren Sie einen Azure Synapse Workspace.

Führen Sie die folgenden Schritte aus, um einen Azure Synapse Workspace zu installieren und zu konfigurieren.

1. Installieren Sie einen Azure Synapse Workspace in Ihrem Azure-Abonnement. Weitere Informationen finden Sie unter [Schnellstart: Einen Synapse Workspace erstellen](/azure/synapse-analytics/quickstart-create-workspace).
2. Öffnen Sie in Notepad oder einem anderen Texteditor die **SetupSynapse.sql**-Skriptdatei aus dem Ordner auf Ihrem lokalen Computer, in den Sie das Dynamics365Commerce.Solutions-Repository im vorherigen Abschnitt geklont oder heruntergeladen haben. Die Skriptdatei befindet sich im Ordner /Pipeline/CommerceAnalyticsSynapse/. Ersetzen Sie im Skript Platzhaltertext durch Werte, wie in der folgenden Tabelle gezeigt.

    | Platzhaltertext | Wiederbeschaffungswert |
    |---|---|
    | placeholder_storageaccount | Der Name des [Speicherkontos](#storageAccount), das Sie erstellt haben, während Sie den Export nach Data Lake konfiguriert haben. |
    | <a name="phContainer"></a>placeholder_container | Der Name des Speichercontainers, der in Ihrer Data Lake-Instanz erstellt wurde, nachdem Sie das Export nach Data Lake-Add-In in LCS erfolgreich installiert haben. Um den Containernamen abzurufen, müssen Sie den Speicher-Explorer im Azure-Portal verwenden, um Ihr Speicherkonto zu durchsuchen. |
    | placeholder_sastoken | Die [SAS-Token](#getSASToken), die Sie generiert haben. Achten Sie darauf, das Fragezeichen (**?**) vom Anfang des SAS-Token-Werts zu entfernen. |
    | <a name="phUserPwd"></a>placeholder_password | Ein starkes Passwort Ihrer Wahl. Notieren Sie das Passwort. Es wird als Passwort für das neue **reportreadonlyuser**-Konto festgelegt, das das Skript erstellt. Geben Sie **nicht** das Passwort des **sqladminuser**-Kontos an. |

3. Kopieren Sie den aktualisierten Inhalt der Skriptdatei.
4. Navigieren Sie im Azure-Portal zum neuen Azure Synapse Workspace. Auf der **Überblick**-Seite wählen Sie **Synapse Studio öffnen**.
5. Wählen Sie in Synapse Studio **Neu \> SQL-Skript**, und fügen Sie den Inhalt der Skriptdatei in den SQL-Skripteditor ein.
6. Stellen Sie sicher, dass das Feld **Datenbank verwenden** auf **Master** eingestellt ist.
7. Wählen Sie **Ausführen**, und warten Sie, bis die Ausführung des Skripts abgeschlossen ist. Bei erfolgreicher Ausführung des Skripts werden die Datenbank für Commerce-Analysen, Anmeldeinformationen für den Zugriff auf den Data Lake und ein schreibgeschütztes Benutzerkonto erstellt, das Power BI verwendet, um eine Verbindung zur Azure Synapse-Instanz herzustellen.
8. Öffnen Sie auf Ihrem lokalen Computer Windows PowerShell im Administratormodus, und wechseln Sie zum Ordner /Pipeline/CommerceAnalyticsSynapse/ unter dem Ordner, in den Sie das Dynamics365Commerce.Solutions-Repository geklont oder heruntergeladen haben.
9. Richten Sie die Windows PowerShell-Ausführungsrichtlinie ein, indem Sie den folgenden Befehl ausführen.

    ```powershell
    Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
    ```

10. Wenn das SQL Server PowerShell-Modul noch nicht installiert ist, installieren Sie es, indem Sie den folgenden Befehl ausführen.

    ```powershell
    Install-Module sqlserver
    ```

    > [!NOTE]
    > Während der Installation des Moduls werden Sie möglicherweise zur Installation eines NuGet-Anbieters aufgefordert. Wählen Sie in diesem Fall **Ja**, um einen NuGet-Anbieter zu installieren. Möglicherweise werden Sie auch aufgefordert, zu bestätigen, dass Sie Module aus einem nicht vertrauenswürdigen Repository neu installieren. Wählen Sie in diesem Fall **Ja**, um mit der Installation fortzufahren. Sie können optional das **Set-PSRepository**-Cmdlet ausführen, um dem **PSGallery**-Repository zu vertrauen.

11. Veröffentlichen Sie die Azure Synapse-Ansichten, indem Sie den folgenden Befehl ausführen.

    ```powershell
    .\PublishSynapseViews.ps1 -serverName SERVER_NAME -password PASSWORD -storageAccount STORAGE_ACCOUNT -containerName CONTAINER_NAME -datarootpath DATA_ROOT_PATH
    ```

    Wenn Sie diesen Befehl ausführen, ersetzen Sie die Platzhalterwerte, wie in der folgenden Tabelle gezeigt.

    | Platzhalterwert | Wiederbeschaffungswert |
    |---|---|
    | SERVER_NAME | Der Name des Azure Synapse Serverless-SQL-Endpunkts. Sie können diesen Wert von der **Überblick**-Seite für den Azure Synapse Workspace im Azure-Portal abrufen. |
    | KENNWORT | Das Passwort für das **sqladminuser**-Konto. |
    | STORAGE_ACCOUNT | Der Name des Speicherkontos für den Data Lake. |
    | CONTAINER_NAME | Der Name des Containers, der von der Funktion „Export nach Data Lake“ erstellt wurde. Dieser Container ist derselbe Container, den Sie als [placeholder_container](#phContainer)-Wert in Schritt 2 angegeben haben. |
    | DATA_ROOT_PATH | Der Ordnername unter dem Container, der alle Daten enthält. |

    > [!NOTE]
    > Sie finden den Speicherkontonamen, den Containernamen und den Datenstammpfad mithilfe des Azure Storage-Browsers und Ihres Data Lake-Speicherkontos im Azure-Portal.

12. Warten Sie, bis die Ausführung des Skripts abgeschlossen ist. Bei erfolgreicher Ausführung des Skripts werden SQL-Ansichten in der Azure Synapse Serverless-SQL-Instanz erstellt.

### <a name="install-the-power-bi-template-app"></a><a name="powerbi"></a>Power BI -Vorlagen-App installieren.

Um die Power BI-Vorlagen-App für Commerce-Analysen (Vorschau) zu installieren und zu konfigurieren, folgen Sie diesen Schritten.

1. Melden Sie sich beim [Power BI-Portal](https://powerbi.microsoft.com/) an, indem Sie Ihre Organisations-ID verwenden.
2. Installieren Sie die Commerce-Analyse (Vorschau) Power BI-Vorlagen-App unter [https://aka.ms/cdireport-installapp](https://aka.ms/cdireport-installapp). Möglicherweise erhalten Sie eine Warnung, die besagt, dass die App nicht auf AppSource aufgeführt ist. Wählen Sie **Installieren**.
3. Wenn Sie die App zum ersten Mal neu installieren, fahren Sie mit Schritt 5 fort. Wenn Sie diese App bereits installiert haben, werden die folgenden Optionen zum Aktualisieren der App angezeigt:

    - **Aktualisieren Sie den Arbeitsbereich und die App** – Aktualisieren Sie die vorhandene Vorlagen-App und überschreiben Sie Ihre vorhandenen App-Einstellungen, z. B. den Namen der App-Instanz und die Berechtigungskonfigurationen.
    - **Nur Workspace-Inhalte aktualisieren, ohne die App zu aktualisieren** – Aktualisieren Sie die vorhandene Vorlagen-App, behalten Sie jedoch Ihre vorhandenen App-Einstellungen bei. *Diese Option ist die empfohlene Option für App-Updates.*
    - **Installieren Sie eine weitere Kopie der App in einem neuen Arbeitsbereich** – Erstellen Sie einen neuen Arbeitsbereich und erstellen Sie dann eine Kopie der vorhandenen Vorlagen-App darin. Der vorhandene Arbeitsbereich bleibt erhalten.

4. Wählen Sie eine der Update-Optionen und dann **Installieren**.
5. Öffnen Sie die installierte App, indem Sie **Apps** im linken Bereich auswählen, und wählen Sie dann die App aus.
6. Verbinden Sie die App mit Ihrer Datenquelle, indem Sie **Verbinden** auswählen. Wenn Sie die App bereits installiert haben, wählen Sie den **Daten verbinden**-Link in der gelben Nachrichtenleiste.
7. Stellen Sie die folgenden Felder ein.

    | Feld | Wert |
    |---|---|
    | Server | Geben Sie den Namen des Azure Synapse Serverless-SQL-Endpunkts ein, den Sie im vorherigen Abschnitt erstellt haben. Sie können diesen Wert von der **Überblick**-Seite für den Azure Synapse Workspace im Azure-Portal abrufen. |
    | Datenbank | Geben Sie **CommerceAnalytics** ein. |
    | Sprache | Wählen Sie einen Wert in der Liste aus. Dieses Feld wird für lokalisierte Produkt- und Kategorienamen verwendet. Der Wert beachtet die Groß-/Kleinschreibung. |
    | Datumsbereich | Wählen Sie einen Wert in der Liste aus. Die Daten für die ausgewählte Anzahl von Monaten werden in das Power BI-DataSet importiert. Der von Ihnen ausgewählte Wert wirkt sich auf die Größe des DataSets und die für die Synchronisierung erforderliche Zeit aus. |

8. Wählen Sie **Weiter**. Sie werden aufgefordert, die Anmeldeinformationen für die Verbindung mit der Azure Synapse SQL-Datenbank einzugeben. Legen Sie dann die Felder wie in der folgenden Tabelle angezeigt fest.

    | Feld | Wert |
    |---|---|
    | Authentifizierungsmethode | Wählen Sie **Basic** aus. |
    | Benutzername | Geben Sie **reportreadonlyuser** ein. |
    | Kennwort | Geben Sie den Wert ein, mit dem Sie den [placeholder_password](#phUserPwd)-Platzhalter innerhalb des SetupSynapse.sql-Skripts ersetzt haben. Dieses Passwort ist das Passwort für das **reportreadonlyuser**-Konto. |

9. Wählen Sie **Anmelden und verbinden** aus.
10. Warten Sie, bis das DataSet erfolgreich aktualisiert wurde. Wählen Sie dann **App bearbeiten**-Schaltfläche, um den App-Arbeitsbereich zu öffnen, in dem Sie den Aktualisierungsstatus des DataSets anzeigen können. Im App-Arbeitsbereich können Sie optional auch automatische Aktualisierungszeitpläne für Ihr DataSet einrichten, Berechtigungen verwalten und die App-Instanz umbenennen.

### <a name="privacy"></a><a name="privacy"></a>Vertraulichkeit

Datenschutz ist uns sehr wichtig. Weiteres erfahren Sie in unserer [Datenschutzerklärung](https://go.microsoft.com/fwlink/?LinkId=521839).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
