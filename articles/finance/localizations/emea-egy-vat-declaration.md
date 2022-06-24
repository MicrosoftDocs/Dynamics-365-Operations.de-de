---
title: MwSt.-Erklärung für Ägypten
description: In diesem Artikel wird erläutert, wie Sie das MwSt.-Rückgabeformular für Ägypten konfigurieren und generieren.
author: sndray
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: sndray
ms.search.validFrom: 2017-06-20
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 1d5788b2328a49f4725a6c689e29a7e784032fae
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870034"
---
#  <a name="vat-declaration-for-egypt-eg-00002"></a>MwSt.-Erklärung für Ägypten (EG-00002)

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/banner.md)]

In diesem Artikel wird erläutert, wie Sie das MwSt.-Rückgabeformular sowie Verkaufs- und Kaufbücher für juristische Personen in Ägypten einrichten und generieren.

Das MwSt.-Rückgabeformular für Ägypten ist das offizielle Dokument, in dem der gesamte fällige Ausgangssteuerbetrag, der gesamte erstattungsfähige Vorsteuerbetrag und die damit verbundene Steuerschuld zusammengefasst sind. Das Formular wird für alle Arten von Steuerzahlern verwendet und sollte manuell über das Steuerbehördenportal ausgefüllt werden. Das MwSt.-Rückgabeformular wird üblicherweise als Umsatzsteuererklärung bezeichnet.

Das MwSt.-Rückgabeformular in Dynamics 365 Finance enthält die folgenden Berichte:

- Das MwSt.-Rückgabeformular Nr. 10 enthält eine Aufschlüsselung der Beträge, Anpassungen und des Umsatzsteuerbetrags pro Position im MwSt.-Rückgabeformular, wie in der Gesetzgebung beschrieben.
- Verkaufstransaktionsbuch
- Einkauftransaktionsbuch

## <a name="prerequisites"></a>Voraussetzungen
Die primäre Adresse der juristischen Person muss in Ägypten liegen.
Aktivieren Sie im Arbeitsbereich **Funktionsverwaltung** die folgende Funktion:

   - (Ägypten) Kategoriehierarchie für Umsatz- und Einkaufssteuerbericht.

Weitere Informationen zur Aktivierung von Funktionen finden Sie unter [Funktionsverwaltungsüberblick](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Importieren Sie im Arbeitsbereich **Elektronische Berichterstattung** das folgende elektronische Berichtsformat aus dem Repository:

- MwSt.-Erklärung Excel (EG)

> [!NOTE]
> Das obige Format basiert auf dem **Steuererklärungsmodell** und verwendet die **Zuordnung des Steuererklärungsmodells**. Zusätzliche Konfigurationen werden automatisch importiert.

Weitere Informationen zum Importieren von Konfigurationen für elektronische Berichte finden Sie unter [Elektronische Berichterstellungskonfigurationen von Lifecycle Services herunterladen](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

## <a name="download-electronic-reporting-configurations"></a>Elektronische Berichtskonfigurationen herunterladen

Die Implementierung der MwSt.-Rückgabeformulare für Ägypten basiert auf Konfigurationen für die elektronische Berichterstattung (ER). Weitere Informationen zu den Funktionen und Konzepten der konfigurierbaren Berichterstellung finden Sie unter [Elektronische Berichterstattung](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).

Für Produktions- und UAT-Umgebungen (User Acceptance Testing) siehe [Elektronische Berichterstellungskonfigurationen von Lifecycle Services herunterladen](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

Laden Sie die folgenden Konfigurationen hoch, um das MwSt.-Rückgabeformular und die zugehörigen Berichte in einer juristischen Person in Ägypten zu erstellen:

- Steuererklärung model.version.70.xml oder eine neuere Version
- Steuererklärung model.mapping.version.70.120.xml oder eine neuere Version
- MwSt.-Erklärung Excel (EG).version.70.32 oder eine neuere Version

Führen Sie die folgenden Schritte aus, nachdem Sie die ER-Konfigurationen von Lifecycle Services (LCS) oder dem globalen Repository heruntergeladen haben.

1. Wechseln Sie in den Arbeitsbereich **Elektronische Berichterstellung** und wählen Sie die Kachel **Berichterstellungskonfigurationen** aus.
1. Wählen Sie auf der Seite **Konfigurationen** im Aktionsbereich **Austausch** > **Aus XML-Datei laden** aus.
1. Laden Sie die Dateien in der Reihenfolge hoch, in der sie oben aufgeführt sind. Nachdem alle Konfigurationen hochgeladen wurden, sollte der Konfigurationsbaum in Finance vorhanden sein.

## <a name="set-up-application-specific-parameters"></a>Anwendungsspezifische Parameter einrichten

Mit den anwendungsspezifischen Parametern können Sie die Kriterien festlegen, nach denen Steuertransaktionen bei der Erstellung des Berichts in jeder Zeile klassifiziert und berechnet werden. Die Ermittlung basiert auf der Konfiguration der Artikel-Mehrwertsteuergruppe, Mehrwertsteuergruppe, dem Mehrwertsteuercode und anderen in der Suchdefinition festgelegten Kriterien.

Die Verkaufs- und Einkaufsbuchberichte für Ägypten enthalten eine Reihe von Spalten, die bestimmten Transaktionsklassifizierungen als Arten von Vorgängen, Produkten und Dokumenten entsprechen, die für Ägypten spezifisch sind. Anstatt diese neuen Klassifizierungen als neue Eintragsdaten einzuschließen, wenn die Transaktionen gebucht werden, werden die Klassifizierungen basierend auf den verschiedenen in **Konfigurationen** > **Anwendungsspezifische Parameter einrichten** > **Einrichten** eingeführten Suchvorgängen bestimmt, um die Anforderungen der Mehrwertsteuerberichte für Ägypten zu erfüllen. 

![Seite für anwendungsspezifische Parameter.](media/egypt-vat-declaration-setup1.png)

Diese folgenden Suchkonfigurationen werden verwendet, um die Transaktionen in Berichten über Vorsteuer- und Ausgangssteuerbücher zu klassifizieren:

- **PurchaseItemTypeLookup** > Spalte O: Artikeltyp
- **VATRateTypeLookup** > Spalte B: Steuertyp
- **VATRateTypeLookup** > Spalte C: Tabellenartikeltyp
- **PurchaseOperationTypeLookup** > Spalte A: Dokumenttyp
- **CustomerTypeLookup** > Spalte A: Dokumenttyp
- **SalesOperationTypeLookup** > Spalte N: Vorgangstyp
- **SalesItemTypeLookup** > Spalte O: Artikeltyp

Führen Sie die folgenden Schritte aus, um die verschiedenen Suchvorgänge einzurichten, die zum Generieren der MwSt.-Erklärung und der zugehörigen Buchberichte verwendet werden. 

1. In dem Arbeitsbereich **Elektronische Berichterstattung** wählen Sie **Konfigurationen** > **Einrichten** aus, um die Regeln zur Identifizierung der Steuertransaktion im entsprechenden Feld des MwSt.-Rückgabeformulars einzurichten.
2. Wählen Sie die aktuelle Version aus und wählen Sie im Inforegister **Suchvorgänge** den Suchnamen. Zum Beispiel **SalesItemTypeLookup**. Diese Suche identifiziert die Liste der Klassifizierungen im Ausgangssteuerbuch, die von der Steuerbehörde verlangt werden.
3. Im Inforegister **Bedingungen** wählen Sie **Hinzufügen** aus und in der neuen Zeile in der Spalte **Suchergebnis** wählen Sie die zugehörige Zeile aus, die die Klassifizierung in der **Spalte O** darstellt.
4. In der Spalte **Mehrwertsteuergruppe** wählen Sie die Mehrwertsteuergruppe aus, mit der die Klassifizierung identifiziert wird. Zum Beispiel **Inlandsverkaufsrechnung**. Sie können auch die Artikel-Mehrwertsteuergruppe, den Steuercode oder die Kombination von Baumattributen verwenden, wenn die Konfiguration auf andere Weise definiert ist. 
5. In der Spalte **Name** wählen Sie die Steuertransaktionsklassifizierung aus.
6. Wiederholen Sie die Schritte 3 bis 5 für alle verfügbaren Suchvorgänge.
7. Wählen Sie **Hinzufügen** aus, um die letzte Belegzeile aufzunehmen, und in der **Suchergebnis**-Spalte wählen Sie **Unzutreffend** aus. 
8. Wählen Sie in den restlichen Spalten **Nicht leer** aus. 
9. Wählen Sie im Feld **Status** die Option **Abgeschlossen** aus.
10. Wählen Sie **Speichern** aus und schließen Sie dann die Seite **Anwendungsspezifische Parameter**.

> [!NOTE]
> Wenn Sie den letzten Datensatz **Unzutreffend** hinzufügen, definieren Sie die folgende Regel: Wenn die Mehrwertsteuergruppe, Artikel-Mehrwertsteuergruppe, der Steuercode und Name, die/der als Argument übergeben werden, keine der vorherigen Regeln erfüllen, werden die Transaktionen nicht in das Ausgangssteuerbuch aufgenommen. Obwohl diese Regel beim Generieren des Berichts nicht verwendet wird, hilft die Regel, Fehler bei der Berichterstellung zu vermeiden, wenn eine Regelkonfiguration fehlt.

Die folgenden Tabellen stellen ein Beispiel für eine vorgeschlagene Konfiguration für die beschriebenen Suchkonfigurationen dar. 

**SalesItemTypeLookup**

| Suchergebnis         | Position | Mehrwertsteuergruppe    | Artikel-Mehrwertsteuergruppe    | Steuercode (Code) | Name                  |
|-----------------------|------|--------------------|-------------------------|-----------------|-----------------------|
| Eigen              | 1    | VAT_LOCAL          | *Nicht leer*             | *Nicht leer*     | Verk.                 |
| Eigen              | 2    | VAT_LOCAL          | *Nicht leer*             | *Nicht leer*     | SalesCreditNote       |
| Eigen              | 3    | VAT_FINALC         | *Nicht leer*             | *Nicht leer*     | Verk.                 |
| Eigen              | 4    | VAT_FINALC         | *Nicht leer*             | *Nicht leer*     | SalesCreditNote       |
| Eigen              | 5    | VAT_PUBLIO         | *Nicht leer*             | *Nicht leer*     | Verk.                 |
| Eigen              | 6    | VAT_PUBLIO         | *Nicht leer*             | *Nicht leer*     | SalesCreditNote       |
| Warenexport                | 7    | VAT_EXPORT         | *Nicht leer*             | *Nicht leer*     | Verk.                 |
| Warenexport                | 8    | VAT_EXPORT         | *Nicht leer*             | *Nicht leer*     | SalesCreditNote       |
| Maschine und Ausrüstung | 9    | *Nicht leer*        | VAT_M&E                 | *Nicht leer*     | Verk.                 |
| Maschine und Ausrüstung | 10   | *Nicht leer*        | VAT_M&E                 | *Nicht leer*     | SalesCreditNote       |
| Teilemaschinen        | 11   | *Nicht leer*        | VAT_PARTS               | *Nicht leer*     | Verk.                 |
| Teilemaschinen        | 12   | *Nicht leer*        | VAT_PARTS               | *Nicht leer*     | SalesCreditNote       |
| Befreiungen            | 13   | VAT_EXE            | *Nicht leer*           | *Nicht leer*     | SaleExempt            |
| Befreiungen            | 14   | VAT_EXE            | *Nicht leer*           | *Nicht leer*     | SalesExemptCreditNote |
| Nicht zutreffend        | 15   | *Leer*            | *Leer*                 | VAT_ADJ         | *Nicht leer*           |
| Nicht zutreffend        | 16   | *Nicht leer*        | *Nicht leer*             | *Nicht leer*     | *Nicht leer*           |

 **SalesOperationTypeLookup**

| Suchergebnis  | Position | Artikel-Mehrwertsteuergruppe    | MwSt.-Code    | Name                  |
|----------------|------|-------------------------|-------------|-----------------------|
| Waren          | 1    | VAT_GOODS               | *Nicht leer* | Verk.                 |
| Waren          | 2    | VAT_GOODS               | *Nicht leer* | SalesCreditNote       |
| Waren          | 3    | VAT_GOODS               | *Nicht leer* | SaleExempt            |
| Waren          | 4    | VAT_GOODS               | *Nicht leer* | SalesExemptCreditNote |
| Dienste       | 5    | VAT_SERV                | *Nicht leer* | Verk.                 |
| Dienste       | 6    | VAT_SERV                | *Nicht leer* | SalesCreditNote       |
| Dienste       | 7    | VAT_SERV                | *Nicht leer* | SaleExempt            |
| Dienste       | 8    | VAT_SERV                | *Nicht leer* | SalesExemptCreditNote |
| Regulierungen    | 9    | *Leer*                 | VAT_ADJ     | Verk.                 |
| Regulierungen    | 10   | *Leer*                 | VAT_ADJ     | SalesCreditNote       |
| Nicht zutreffend | 11   | *Nicht leer*             | *Nicht leer* | *Nicht leer*           |

**PurchaseItemTypeLookup**

| Suchergebnis          | Position | Artikel-Mehrwertsteuergruppe    | MwSt.-Code    | Name                     |
|------------------------|------|-------------------------|-------------|--------------------------|
| Waren                  | 1    | VAT_GOODS               | *Nicht leer* | Einkauf                 |
| Waren                  | 2    | VAT_GOODS               | *Nicht leer* | PurchaseCreditNote       |
| Dienste               | 3    | VAT_SERV                | *Nicht leer* | Einkauf                 |
| Dienste               | 4    | VAT_SERV                | *Nicht leer* | PurchaseCreditNote       |
| Maschine und Ausrüstung  | 5    | VAT_M&E                 | *Nicht leer* | Einkauf                 |
| Maschine und Ausrüstung  | 6    | VAT_M&E                 | *Nicht leer* | PurchaseCreditNote       |
| Teilemaschinen         | 7    | VAT_PARTS               | *Nicht leer* | Einkauf                 |
| Teilemaschinen         | 8    | VAT_PARTS               | *Nicht leer* | PurchaseCreditNote       |
| Befreiungen             | 9    | VAT_EXE                 | *Keine Bank*  | PurchaseExempt           |
| Befreiungen             | 10   | VAT_EXE                 | *Nicht leer* | PurchaseExemptCreditNote |
| Nicht zutreffend         | 11   | *Nicht leer*             | *Nicht leer* | *Nicht leer*              |

**PurchaseOperationTypeLookup**

| Suchergebnis  | Position | Mehrwertsteuergruppe  | MwSt.-Code    | Name                     |
|----------------|------|------------------|-------------|--------------------------|
| Eigen       | 1    | VAT_LOCAL        | *Nicht leer* | Einkauf                 |
| Eigen       | 2    | VAT_LOCAL        | *Nicht leer* | PurchaseCreditNote       |
| Eigen       | 3    | VAT_LOCAL        | *Nicht leer* | PurchaseExempt           |
| Eigen       | 4    | VAT_LOCAL        | *Nicht leer* | PurchaseExemptCreditNote |
| Importiert       | 5    | VAT_IMPORT       | *Nicht leer* | Einkauf                 |
| Importiert       | 6    | VAT_IMPORT       | *Nicht leer* | PurchaseCreditNote       |
| Importiert       | 7    | VAT_IMPORT       | *Nicht leer* | PurchaseExempt           |
| Importiert       | 8    | VAT_IMPORT       | *Nicht leer* | PurchaseExemptCreditNote |
| Regulierungen    | 9    | *Leer*          | VAT_ADJ     | PurchaseCreditNote       |
| Regulierungen    | 10   | *Leer*          | VAT_ADJ     | Kaufen                 |
| Nicht zutreffend | 11   | *Nicht leer*      | *Nicht leer* | *Nicht leer*              |

**CustomerTypeLookup**

|    Suchergebnis    | Position | Mehrwertsteuergruppe |
|---------------------|------|-----------------|
| Organisation        |  1   | VAT_LOCAL       |
| Organisation        |  2   | VAT_EXPORT      |
| Organisation        |  3   | VAT_EXE         |
| Endverbraucher      |  4   | VAT_FINALC      |
| Öffentliche Organisation |  5   | VAT_PUBLIO      |
| Nicht zutreffend      |  6   | *Nicht leer*     |

**VATRateTypeLookup**

| Suchergebnis  | Position | Steuercode (Code) |
|----------------|------|-----------------|
| GeneralGoods   | 1    | VAT_ST          |
| GeneralGoods   | 2    | VAT_RD          |
| FirstTable     | 3    | *Nicht leer*     |
| SecondTable    | 4    | *Nicht leer*     |
| Nicht zutreffend | 5    | *Nicht leer*     |


## <a name="set-up-general-ledger-parameters"></a>Einrichten der Hauptbuchparameter

Um den MwSt.-Rückgabeformularbericht im Microsoft Excel-Format zu generieren, definieren Sie ein ER-Format auf der **Hauptbuchparameter**-Seite.

1. Gehen Sie zu **Steuer** > **Einrichten** > **Hauptbuchparameter**.
2. Auf der **Mehrwertsteuer**-Registerkarte im Abschnitt **Steueroptionen** im Feld **MwSt.-Abrechnungs-Formatzuordnung** wählen Sie **MwSt.-Erklärung Excel (EG)** aus. Wenn Sie das Feld leer lassen, wird der Standardmehrwertsteuerbericht im SSRS-Format erstellt.
3. Wählen Sie die **Kategoriehierarchie** aus. Diese Kategorie aktiviert den Warencode in Transaktionen auf der Außenhandel-Registerkarte , damit Benutzer Waren und Dienstleistungen auswählen und klassifizieren können. Die Beschreibung dieser Klassifizierung finden Sie in Verkaufs- und Einkaufstransaktionsberichten. Diese Konfiguration ist optional.

![Erklärungsformular.](media/egypt-vat-declaration-setup2.png)


## <a name="generate-a-vat-return-report"></a>MwSt.-Rückgabebericht generieren
Der Prozess zum Erstellen und Einreichen eines MwSt.-Rückgabeberichts für einen Zeitraum basiert auf Mehrwertsteuerzahlungstransaktionen, die während der Mehrwertsteuerabrechnung und -buchung gebucht wurden. Weitere Informationen über die Mehrwertsteuerabrechnung und -berichterstellung finden Sie im [Mehrwertsteuerüberblick](../general-ledger/indirect-taxes-overview.md).

Führen Sie die folgenden Schritte zum Generieren des Steuererklärungsberichts aus:

1. Gehen Sie zu **Steuer** > **Erklärungen** > **Mehrwertsteuer** > **Mehrwertsteuer für Abrechnungszeitraum melden** oder **Mehrwertsteuer abrechnen und buchen**.
2. Wählen Sie **Ausgleichsperiode** aus.
3. Wählen Sie das Anfangsdatum und dann die Version der Mehrwertsteuerzahlung aus.
5. Wählen Sie **OK**. 
6. Geben Sie ggf. den Kreditbetrag aus der Vorperiode ein oder belassen Sie den Betrag bei Null.
7. Wählen Sie im Feld **Berichtsdetails** eine der folgenden verfügbaren Optionen aus. 
   - **Vorsteuerbuch**: Generieren Sie den Bericht mit den Details zu Vorsteuertransaktionen.
   - **Ausgangssteuerbuch**: Generieren Sie den Bericht mit den Details zu Mehrwertsteuertransaktionen.
   - **MwSt.-Erklärung**: Generieren Sie nur das Formular zur Rückgabe der Mehrwertsteuererklärung.
8. Geben Sie den Namen der Person ein, die registriert ist, um das Formular zuzuweisen.
9. Wählen Sie die Sprache aus. Alle Berichte werden in **en-us** und **ar-eg** übersetzt.
  
[!INCLUDE[footer-include](../../includes/footer-banner.md)]


