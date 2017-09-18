---
title: "Statistische Dimensionselement und statistischen Maßnahmenanbieter-Vorlagen"
description: "Dieses Thema enthält Informationen über statische Dimensionselemente und statistische Maßnahmenanbieter-Vorlagen Statistische Dimensionswerte können als Verrechnungsgrundlage in den Richtlinien wie Kostenaufteilung und Prozentsatz verwendet werden. Sie können auch verwendet werden, um nicht-monetären Verbrauch durch Kosten zu melden."
author: AndersGirke
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMCostAccountingLedgerSourceEntryProvider, CAMStatisticalDimension, CAMAXStatisticalMeasureProviderTemplate
audience: Application User
ms.reviewer: yuyus
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: YuyuScheller
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: 180863b5c3b8fe7870ab58f3849e52583f5880c1
ms.contentlocale: de-de
ms.lasthandoff: 06/20/2017

---

# <a name="statistical-dimension-members-and-statistical-measure-provider-templates"></a>Statistische Dimensionselement und statistischen Maßnahmenanbieter-Vorlagen

[!include[banner](../includes/banner.md)]

Eine statistischen Dimension und seine Mitgliedern werden verwendet, um nicht monetäre Einträge in der Kostenrechnung zu erfassen und zu steuern. Statistische Dimensionswerte können für beide Zwecke verwendet werden:

- Als Verrechnungsgrundlage in den Richtlinien wie Kostenaufteilung oder Kostenzuweisung
- Für die Angabe des nicht-monetären Verbrauchs

## <a name="statistical-dimension"></a>Statistische Dimension

Eine statistische Dimension enthält einen eindeutigen Namen und einem Satz eindeutige Dimensionswerte. Die Anzeige statistischer Dimension wird einem Kostenrechnungssachkonto Kennung zugewiesen. Diese Beziehung bindet alle entsprechenden statistischen Dimensionswerte an das Kostensachkonto. Daher werden alle Einträge im Kontext des statistischen Kostenrechnungssachkontos erstellt.

> [!NOTE]
> Die Anzeige statistischer Dimension kann mehr als einem Kostensachkonto zugewiesen werden.

Dies ist ein Beispiel einer Dimensionshierarchie.

| Name                        | Datenkonnektor für Dimensionsmitglieder |
|-----------------------------|--------------------------------------|
| Freigegebene statistische Elemente | Importierte Dimensionsmitglieder           |

Hier ist ein Beispiel einer statistischen Dimension, die einem Kostenrechnungssachkonto zugewiesen wurde.

| Name                  | Buchhaltungswährung | Wechselkurstyp | Steuerkalender | Kostenelementdimension | Statistische Dimension       |
|-----------------------|---------------------|--------------------|-----------------|------------------------|-----------------------------|
| Führungs-Buchhaltung | USD                 | Konstante Währung  | Finanzzeitraum   | Budgetkostenelemente   | Freigegebene statistische Elemente |

## <a name="statistical-dimension-members"></a>Mitglieder der statistischen Dimension

Statistisches Dimensionsmitglied stellt eine Entität dar, für die sie nicht monetäre Kennzahlen erfassen möchten. Diese Einheiten können entweder als Verrechnungsgrundlage verwendet werden oder einfach dazu, nicht monetäre Werte zu melden.

Statistische Dimensionswerte können manuell erstellt werden. Alternativ können sie aus einer Datei importiert werden, indem Sie das Datenverwaltungsimport-/-exporttool verwenden.

Statistisches Dimensionsmitglied wird automatisch einer vordefinierten Verrechnungsgrundlage. Sie kann als Verrechnungsgrundlage in den Richtlinien verwendet werden, z oder in anderen Typen Verrechnungsgrundlagen eingegeben wurde.

Nachfolgend sind einige Beispiele von typischen statistischen Dimensionsmitgliedern.

| Name der statistischen Dimension  | Statistische Elemente | Beschreibung             | Einheit |
|-----------------------------|----------------------|-------------------------|------|
| Freigegebene statistische Elemente | FTE                  | Vollzeitmitarbeiter     | Ea.  |
| Statistische Elemente | Elektrizität          | Stromverbrauch | kWh  |
| Freigegeben statistische Elemente | CC Pack              | Kostenstelle Verpackung   | Hrs. |

## <a name="statistical-measure-provider-template"></a>Anbietervorlagen für statistische Maßnahmen

Statistische Kennzahlen können aus mehreren Quellen stammen. Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition ist eine hervorragende Quelle, um  statistischen Kennzahlen zu extrahieren. Sie können eine Anbietervorlage verwenden, statistische Kennzahl der statistischen Kennzahlen leicht zu konfigurieren, die zum Extrahieren möchten.

Die Definition einer statistischen Anbietervorlage ist generisch und kann in verschiedenen statistischen Dimensionsmitgliedern wiederverwendet werden.

> [!NOTE]
> Alle Tabellen, die Finanzdimensionen enthalten, können als Quellen für statistische Maßnahmen verwendet werden.

**Beispiel: Anzahl Mitarbeiter pro Kostenstelle**

Die Anzahl der Mitarbeiter pro Kostenstelle ist ein statistischer Maßstab, der für verschiedene Zwecke verwendet werden kann, die Verwaltungseinblicke enthalten:

- Eine statistische Berichterstellungskennzahl nach Kostenstelle
- Eine Verrechnungsgrundlage für unterschiedliche Arten von Ausgaben
- Interne Verrechnungssätze nach Kostenstelle:

    - Kosten nach Mitarbeiter
    - Einnahmen nach Mitarbeiter

Die HcmEmployment-Tabelle enthält eine Liste aller Mitarbeiter in der Instanz. Diese Tabelle ist eine globale Tabelle. Daher werden die Datensätze nicht einer bestimmten Datenbereich-Kennung zugeordnet.

Das folgende Beispiel der Mitarbeiter in der HcmEmployment-Tabelle.

| Name       | Kostenstelle | Beschreibung   | Arbeitskrafttyp |
|------------|-------------|----|-------------|
| Mitarbeiter 1 | CC001       | Personalverwaltung | Mitarbeiter    |
| Mitarbeiter 2 | CC002       | FI | Mitarbeiter    |
| Mitarbeiter 3 | CC002       | FI | Mitarbeiter    |
| Mitarbeiter 4 | CC003       | LU | Mitarbeiter    |
| Mitarbeiter 5 | CC003       | LU | Mitarbeiter    |
| Mitarbeiter 6 | CC002       | FI | Auftragnehmer  |

Wenn Sie einen Datensatz **Statistische Anbietervorlage** erstellen, müssen Sie entscheiden, welche Funktionen Sie nutzen möchten:

- **Anzahl** – Eine Anzahl von Datensätzen pro Kostenträger wird übertragen.
- **Summe** – Eine Summe von Datensätzen pro Kostenträger wird übertragen. Das Feld ( **Summe** und **Datum** sind Pflichtfelder.)

## <a name="using-the-count-function"></a>Verwenden der Anzahlfunktion

So kann eine Anbietervorlage für statistische Kennzahl wie folgt eingerichtet werden.

| Name  | Funktion | Quelltabelle  | Summenfeld      | Datumsfeld     |
|-------|----------|---------------|----------------|----------------|
| FTEs  | Anzahl    | HcmEmployment | Nicht zutreffend | Nicht zutreffend |

Sie können mindestens einen oder mehrere Bereiche hinzufügen, um die Kennzahlen der Quelltabelle einzugrenzen.

Wenn Sie wie in diesem Beispiel die Anzahl aller Vollzeitangestellten (FTEs) möchten, können Sie einen Bereich  **Arbeitskrafttyp** hinzufügen. Wählen Sie im Feld **Kriterien** **Mitarbeiter**, um den Ausgabebereich wie folgt eingeschränkt.

**Bereiche**

| Quelltabelle  | Feld       | Kriterien |
|---------------|-------------|----------|
| HcmEmployment | Arbeitskrafttyp | Mitarbeiter |

Bevor Sie statistische Kennzahlen in der Kostenrechnung verwenden können, müssen Sie die Beziehung zwischen der statistischen Kennzahl und den Anbietervorlage im statistischen Dimensionsmitglied einrichten. Diese Beziehung wird pro Kostenrechnungssachkonto und -Version erstellt. Die Beziehung besteht aus einem Datenkonnektor und einem Datenanbieter. Sie können mehrere Datenkonnektoren und Datenanbieter pro statistisches Dimensionsmitglied haben.

> [!NOTE]
> In diesem Beispiel wird eine Beziehung nur für die **Tatsächliche Version** erstellt.

Gehen Sie zu **Kostenrechnungssachkonto** \> **Tatsächliche Version** \> **Verwalten** \> **Statistische Kennzahlen**, um die Beziehung einzurichten. Für dieses Szenario wählen Sie **Dynamics 365 für Finanzen und Arbeitsgänge, Enterprise Edition – Kennzahlen statistischen** aus Datenkonnektor, da diese Daten aus der erhaltenen Finanzierung und Arbeitsgängen extrahiert werden sollen.

**Datenquelle**

| Name        | Datenkonnektor                                                                     | Statistisches Dimensionselement |
|-------------|------------------------------------------------------------------------------------|------------------------------|
| FTEs D365FO | Auf Dynamics 365 for Finance and Operations, Enterprise-Editionsinstanzen zugreifen | FTEs                         |

**Daten-Konfigurationsanbieter**

| Der Name der statistischen Vorlage |
|---------------------------|
| FTEs                      |

Nachdem die Quelldaten für statistische Maßnahmen verarbeitet wurden, werden die folgenden Einträge in der Kostenrechnung erstellt.

**Erfassung**

| Erfassung | Journaltyp                       | Steuerkalenderperiode | Jahr   |  Periode  |  Version | Datenkonnektor für Quelleinträge|
|---------|------------------------------------|------------------------|--------|----------|----------|------------------------------|
| 00001   | Statistischer Umlagerungserfassungseintrag | Steuerlich                 | 2017   | Periode 1 | Sachkonto USMF | FTEs                   |

**Statistischer Eintrag für Umlagerungserfassungseinträge**

| Abschlussstichtag | Größe | Statistisches Element |   Beschreibung       | Kostenstelle |
|-----------------|-----------|---------------------|---------------------|-------------|
| 31-01-2017      | 1,00      | FTEs                | Vollzeitmitarbeiter | CC001       |
| 31-01-2017      | 2.00      | FTEs                | Vollzeitmitarbeiter | CC002       |
| 31-01-2017      | 2.00      | FTEs                | Vollzeitmitarbeiter | CC003       |

**Statistische Einträge**

| Kostenobjekt |    | Abschlussstichtag | Statistisches Dimensionselement |  Beschreibung        | Größe |
|-------------|----|-----------------|------------------------------|---------------------|-----------|
| CC001       | Personalverwaltung | 31-01-2017      | FTEs                         | Vollzeitmitarbeiter | 1,00      |
| CC002       | FI | 31-01-2017      | FTEs                         | Vollzeitmitarbeiter | 2.00      |
| CC003       | LU | 31-01-2017      | FTEs                         | Vollzeitmitarbeiter | 2.00      |

Wenn die Dimensionsmitglieds-Zuweisungsgrundlage Vollzeitbeschäftigte als vordefinierte Verrechnungsgrundlage in einer Kostenaufteilungsregel zugewiesen wird, werden die Kosten aufgeteilt, indem Sie den folgenden Zuweisungsfaktor verwenden.

| Kostenobjekt | Beschreibung    | Größe | Zuweisungsfaktor |
|-------------|----|-----------|-------------------|
| CC001       | Personalverwaltung | 1,00      | (1/5) × Betrag    |
| CC002       | FI | 2.00      | (2/5) × Betrag    |
| CC003       | LU | 2.00      | (2/5) × Betrag    |

## <a name="using-the-sum-function"></a>Verwenden der Summenfunktion

Ein Produktionskostencenter, CC010 (Verpackung ), ist für das Verpacken der Produkte zuständig, bevor sie an Debitoren versendet werden. Die direkten Arbeitskosten werden zu Produkten zur Stückliste (BOM) und Arbeitsplan hinzugefügt. Die indirekten Kostenkomponenten der Ausführung der Kostenstelle müssen den hergestellten Produkten auch zugewiesen werden. Oft ist die beste statistischen Kennzahl für eine solche Zuweisung die Anzahl der erfassten Produktionsstunden pro Produkt innerhalb der angegebenen Periode.

Die ProdRouteTrans-Tabelle enthält alle Produktionsarbeitsbuchungen pro juristische Person DataAreadID angezeigt.

Hier ist ein Beispiel für die ProdRouteTrans-Tabelle.

| Referenz        | Anzahl | Arbeitsgang | Typ | Zeit  | Physisches Datum | Name der Produktdimensionsgruppe (Finanzdimension) | Juristische Person |
|------------------|--------|-----------|------|-------|---------------|-------------------------------------|--------------|
| Produktionsauftrag | P0001  | Verpackung | Zeit | 8,00  | 01-01-2017    | Orangensaft B2B                    | USMF         |
| Produktionsauftrag | P0001  | Verpackung | Zeit | 8,00  | 02-01-2017    | Orangensaft B2B                    | USMF         |
| Produktionsauftrag | P0002  | Verpackung | Zeit | 4,00  | 03-01-2017    | Orangensaft Verbraucher               | USMF         |
| Produktionsauftrag | P0003  | Verpackung | Zeit | 4,00  | 03-01-2017    | Orangensaft Verbraucher               | USMF         |
| Produktionsauftrag | P0004  | Reconst.  | Zeit | 10,00 | 03-01-2017    | Orangensaft Verbraucher               | USMF         |

Wenn Sie einen Datensatz **Statistische Anbietervorlage** erstellen, müssen Sie entscheiden, welche Funktionen Sie nutzen möchten:

- **Anzahl** – Eine Anzahl von Datensätzen pro Kostenträger wird übertragen.
- **Summe** – Eine Summe von Datensätzen pro Kostenträger wird übertragen. Das Feld ( **Summe** und **Datum** sind Pflichtfelder.)

So kann eine Anbietervorlage mit statistischen Kennzahl wie folgt eingerichtet werden.

| Name    | Funktion | Quelltabelle   | Summenfeld | Datumsfeld    |
|---------|----------|----------------|-----------|---------------|
| CC Pack | Summe      | ProdRouteTrans | Stunden     | Physisches Datum |

Sie können mindestens einen Bereich hinzufügen, um die Kennzahlen der Quelltabelle einzugrenzen.

Wenn Sie wie in diesem Beispiel die Summe der Stunden wollen, die auf die Kostenstelle der Verpackung CC010 zugeordnet sind, können Sie einen Bereich auf dem Feld **Vorgang** hinzufügen. Wählen Sie im Feld **Kriterien** **Verpackung**, um den Ausgabebereich wie folgt einzuschränken.

**Bereiche**

| Quelltabelle   | Feld     | Kriterien  |
|----------------|-----------|-----------|
| ProdRouteTrans | Arbeitsgang | Verpackung |

Bevor Sie statistische Kennzahlen in der Kostenrechnung verwenden können, müssen Sie die Beziehung zwischen der statistischen Kennzahl und den Anbietervorlage im statistischen Dimensionsmitglied einrichten. Diese Beziehung wird pro Kostenrechnungssachkonto und -Version erstellt. Die Beziehung besteht aus einem Datenkonnektor und einem Datenanbieter. Sie können mehrere Datenkonnektoren und Datenanbieter pro statistisches Dimensionsmitglied haben.

> [!NOTE]
> In diesem Beispiel wird eine Beziehung nur für die **Tatsächliche Version** erstellt.

Gehen Sie zu **Kostenrechnungssachkonto** \> **Tatsächliche Version** \> **Verwalten** \> **Statistische Kennzahlen**, um die Beziehung einzurichten. Für dieses Szenario wählen Sie **Dynamics 365 für Finanzen und Arbeitsgänge, Enterprise Edition – Kennzahlen statistischen** aus Datenkonnektor, da diese Daten aus der erhaltenen Finanzierung und Arbeitsgängen extrahiert werden sollen.

**Datenquelle**

| Name           | Datenkonnektor                                                                     | Statistisches Dimensionselement |
|----------------|------------------------------------------------------------------------------------|------------------------------|
| Pack CC D365FO | Auf Dynamics 365 for Finance and Operations, Enterprise-Editionsinstanzen zugreifen | CC Pack                      |

Das System erkennt, dass ProdRouteTrans eine Tabelle ist, bei der jeder Datensatz zu einer juristischen Person einem separaten Datensatz gehört. Aus diesem Grund werden Sie gefragt, die juristische Person auszuwählen, für die die Buchungen importiert werden soll.

**Daten-Konfigurationsanbieter**

| Der Name der statistischen Vorlage | Juristische Person |
|---------------------------|--------------|
| CC Paket                   | USMF         |

Nachdem die Quelldaten für statistische Maßnahmen verarbeitet wurden, werden die folgenden Einträge in der Kostenrechnung erstellt.

**Erfassung**

| Erfassung | Journaltyp                     | Steuerkalenderperiode | Jahr   | Periode | Version   |   Datenkonnektor für Quelleinträge  |
|---------|----------------------------------|------------------------|--------|---------|----------------|---------|
| 00002   | Statistischer Umlagerungserfassungseintrag | Steuerlich               | 2017    | Periode 1  | Sachkonto USMF | CC Pack |

**Statistischer Eintrag für Umlagerungserfassungseinträge**

| Abschlussstichtag | Größe | Statistisches Element |  Beschreibung          | Produktgruppe         |
|-----------------|-----------|---------------------|-----------------------|-----------------------|
| 31-01-2017      | 16,00     | CC Pack             | Kostenstellendimension | Orangensaft B2B      |
| 31-01-2017      | 8,00      | CC Pack             | Kostenstellendimension | Orangensaft Verbraucher |

**Statistische Einträge**

| Kostenobjekt           | Abschlussstichtag | Statistisches Dimensionselement |    Beschreibung        | Größe |
|-----------------------|-----------------|------------------------------|-----------------------|-----------|
| Orangensaft B2B      | 31-01-2017      | CC Pack                      | Kostenstellendimension | 16,00     |
| Orangensaft Verbraucher | 31-01-2017      | CC Pack                      | Kostenstellendimension | 8,00      |

Wenn die Dimensionsmitglieds-Zuweisungsgrundlage Vollzeitbeschäftigte als vordefinierte Verrechnungsgrundlage in einer Kostenaufteilungsregel zugewiesen wird, werden die Kosten aufgeteilt, indem Sie den folgenden Zuweisungsfaktor verwenden.

| Kostenobjekt           | Größe | Zuweisungsfaktor  |
|-----------------------|-----------|--------------------|
| Orangensaft B2B      | 16,00     | (16 ÷ 24) × Betrag |
| Orangensaft Verbraucher | 8,00      | (8 ÷ 24) × Betrag  |

## <a name="imported-statistical-measures"></a>Importierte statistische Maßnahmen

Sie können statistische Kennzahlen in die Kostenrechnung importieren, indem Sie das Datenverwaltungsimport-/-exporttool verwenden.

Die Datenentität, die für den Import verwendet wird, werden importierte statistischen Kennzahlen benannt.

> [!NOTE]
> Diese Datenentität wurde so entworfen, dass maximal fünf eindeutigen Dimensionswerte pro Eintrag möglich sind.

Der Stromverbrauch wird in Microsoft Excel mithilfe des vordefinierten Format der Datenentität erfasst. Hier ist ein Beispiel.

| Abschlussstichtag | Dimensionsmitgliedsname1 | Dimensionsmitgliedsname2 | Dimensionsmitgliedsname5 | Größe  | Quellenbezeichner |
|-----------------|------------------------|------------------------|------------------------|------------|-------------------|
| 31-01-2017      | CC001                  |                        |                        | 2,450.00   | Elektrizität       |
| 31-01-2017      | CC002                  |                        |                        | 4,100.00   | Elektrizität       |
| 31-01-2017      | CC003                  |                        |                        | 15.000,00  | Elektrizität       |

Wenn Sie Ihre Daten zur Datenverwaltung importiert haben, werden die Daten in einer Kostenrechnungsstagingtabelle gespeichert. Daher können die importierten Daten in mehreren Kostenrechnungssachkonten verwendet werden. Ein erneutes Laden von Daten ist nicht erforderlich.

Um die Daten zu importieren, gehen Sie zu **Importierte Daten** \> **Datenentität** \> **Importierte statistischen Kennzahlen**.

| Quellenbezeichner | Abschlussstichtag | Größe  | Dimensionsmitgliedsname1 | Dimensionsmitgliedsname2 | Dimensionsmitgliedsname5 |
|-------------------|-----------------|------------|------------------------|------------------------|------------------------|
| Elektrizität       | 31-01-2017      | 2,450.00   | CC001                  |                        |                        |
| Elektrizität       | 31-01-2017      | 4,100.00   | CC002                  |                        |                        |
| Elektrizität       | 31-01-2017      | 15.000,00  | CC003                  |                        |                        |

Bevor Sie statistische Kennzahlen in der Kostenrechnung erhalten, müssen Sie die Beziehung zwischen der statistischen Kennzahl und den Anbietervorlagen des statistischen Dimensionsmitglied einrichten. Diese Beziehung wird pro Kostenrechnungssachkonto und -Version erstellt. Die Beziehung besteht aus einem Datenkonnektor und einem Datenanbieter. Sie können mehrere Datenkonnektoren und Datenanbieter pro statistisches Dimensionsmitglied haben.

> [!NOTE]
> In diesem Beispiel wird eine Beziehung nur für die **Tatsächliche Version** erstellt.

Gehen Sie zu **Kostenrechnungssachkonto** \> **Tatsächliche Version** \> **Verwalten** \> **Statistische Kennzahlen**, um die Beziehung einzurichten. Für dieses Szenario wählen Sie **Importierte statistischen Kennzahlen** aus Datenkonnektor, weil sich Daten von einem System eines Fremdanbieters in Kostenrechnung über Excel importiert wurden.

**Datenquelle**

| Name        | Datenkonnektor                | Statistisches Dimensionselement |
|-------------|-------------------------------|------------------------------|
| Elektrizität | Importierte statistische Maßnahmen | Elektrizität                  |

**Daten-Konfigurationsanbieter**

| Quellenbezeichner importieren | Funktion | Dimension1   | Dimension2 | Dimension5 |
|--------------------------|----------|--------------|------------|------------|
| Elektrizität              | Summe      | Kostenstellen |            |            |

> [!NOTE]
> Wenn Sie die Datenanbieterkonfiguration definieren, müssen Sie angeben, welche Kostenträgerdimension mit der importierten Buchungen übereinstimmen soll. Nachdem die Quelldaten für statistische Maßnahmen verarbeitet wurden, werden die folgenden Einträge in der Kostenrechnung erstellt.

**Erfassung**

| Erfassung | Journaltyp                       | Steuerkalenderperiode | Jahr  | Perid  |Version      |Datenkonnektor für Quelleinträge |
|---------|------------------------------------|------------------------|-------|--------|---------------|-------------|
| 00002   | Statistischer Umlagerungserfassungseintrag | Steuerlich                 | 2017  | Periode 1 | Sachkonto USMF | Elektrizität |

**Statistischer Eintrag für Umlagerungserfassungseinträge**

| Abschlussstichtag | Größe  | Kostenelement |   Beschreibung           | Kostenstelle |
|-----------------|------------|--------------|-------------------------|-------------|
| 31-01-2017      | 2,450.00   | Elektrizität  | Stromverbrauch | CC001       |
| 31-01-2017      | 4,100.00   | Elektrizität  | Stromverbrauch | CC002       |
| 31-01-2017      | 15.000,00  | Elektrizität  | Stromverbrauch | CC003       |

**Statistische Einträge**

| Kostenobjekt |    | Abschlussstichtag | Statistisches Dimensionselement |      Beschreibung                   | Größe  |
|-------------|----|-----------------|------------------------------|-------------------------|------------|
| CC001       | Personalverwaltung | 31-01-2017      | Elektrizität                  | Stromverbrauch | 2,450.00   |
| CC002       | FI | 31-01-2017      | Elektrizität                  | Stromverbrauch | 4,100.00   |
| CC003       | LU | 31-01-2017      | Elektrizität                  | Stromverbrauch | 15.000,00  |

Wenn die vordefinierte Dimensionsmitgliedzuweisungsbasis Elektrizität als Verrechnungsgrundlage einer Kostenaufteilungsregel zugewiesen wird, werden die Kosten aufgeteilt, indem Sie den folgenden Zuweisungsfaktor verwenden.

| Kostenobjekt |    | Größe | Zuweisungsfaktor          |
|-------------|----|-----------|----------------------------|
| CC001       | Personalverwaltung | 2,450.00  | (2.450 ÷ 21.550) × Betrag  |
| CC002       | FI | 4,100.00  | (4.100 ÷ 21.550) × Betrag  |
| CC003       | LU | 15.000,00 | (15.000 ÷ 21.550) × Betrag |

## <a name="see-also"></a>Siehe auch

[Zuteilungsbasen](allocation-bases.md)

