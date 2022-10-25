---
title: Umsatzsteuererklärung (Deutschland)
description: In diesem Artikel wird erläutert, wie Sie eine Umsatzsteuererklärung für juristische Personen in Deutschland im offiziellen XML-Format einrichten und erstellen.
author: AdamTrukawka
ms.date: 03/10/2022
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: ''
ms.openlocfilehash: 04c625b554d96f8ed28ceffef9647fe9cbf7fe2f
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689459"
---
# <a name="vat-declaration-germany"></a>Umsatzsteuererklärung (Deutschland)

[!include [banner](../includes/banner.md)]

In diesem Artikel wird erläutert, wie Sie eine Umsatzsteuererklärung für juristische Personen in Deutschland im offiziellen XML-Format einrichten und erstellen. In diesem Artikel wird auch erläutert, wie Sie eine Vorschau der Umsatzsteuererklärung in Microsoft Excel anzeigen.

Um den Bericht automatisch zu erstellen, erstellen Sie genügend Mehrwertsteuercodes, um für jedes Feld in der Mehrwertsteuervoranmeldung eine separate Mehrwertsteuerabrechnung zu führen. Verknüpfen Sie außerdem in den anwendungsspezifischen Parametern des Formats für die elektronische Berichterstellung (ER) für die Umsatzsteuervoranmeldung Mehrwertsteuercodes mit dem Ergebnis der Suche nach den Feldern in der Umsatzsteuererklärung.

Für Deutschland müssen Sie **Nachschlagen von Berichtfeldern** konfigurieren. Weitere Informationen zum Einrichten anwendungsspezifischer Parameter finden Sie im Abschnitt [Anwendungsspezifische Parameter für Umsatzsteuererklärungsfelder einrichten](#set-up-application-specific-parameters-for-vat-declaration-fields) weiter unten in diesem Artikel.

In der folgenden Tabelle zeigt die Spalte „Suchergebnis“ das Suchergebnis, das für eine bestimmte Mehrwertsteuererklärungszeile im Mehrwertsteuererklärungsformat vorkonfiguriert ist. Verwenden Sie diese Informationen, um die Mehrwertsteuercodes dem Suchergebnis und dann der Zeile der Mehrwertsteuererklärung korrekt zuzuordnen.

### <a name="vat-declaration-overview"></a><a name="vat-declaration-overview"></a>Übersicht über die Umsatzsteuererklärung

Die Umsatzsteuervoranmeldung in Deutschland enthält folgende Informationen.

**ABSCHNITT – LIEFERUNGEN UND ANDERE DIENSTLEISTUNGEN**

**Steuerpflichtiger Umsatz**

| Zeile | Feld – Steuerbasis | Feld – Steuerbetrag | Description                                                                                                                                      | Suchergebnis                                                                             |
|-----|----------------|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| 20  | 81             | Ohne Code     | Steuerpflichtige Verkäufe mit einer Steuerrate von 19 Prozent.                                                                                                       | 20-TaxableSalesStandard</br>73-BadDebtsWriteOffStandard (81/50) – mit Minuszeichen             |
| 21  | 86             | Ohne Code     | Steuerpflichtige Verkäufe mit einer Steuerrate von 7 Prozent.                                                                                                        | 21-TaxableSalesReduced</br>73-BadDebtsWriteOffReduced (86/50) – mit Minuszeichen               |
| 22  | 35             | 36               | Steuerpflichtige Verkäufe zu anderen Steuersätzen.                                                                                                                | 22-TaxableSalesOtherRates</br>73-BadDebtsWriteOffOtherRates (35/36/50) – mit Minuszeichen      |
| 23  | 77             | *Kein Steuerbetrag*  | Lieferungen von land- und forstwirtschaftlichen Betrieben nach §24 UStG an Kunden, die über eine Umsatzsteuer-Identifikationsnummer verfügen. | 23-EUSalesAverageRate24</br>73-BadDebtsWriteOffEUSalesAverageRate24 (77/50) – mit Minuszeichen |
| 24  | 76             | 80               | Umsatzsteuerpflichtige Umsätze nach §24 UStG (Sägewerkprodukte, Getränke und alkoholische Flüssigkeiten).                                | 24-SalesAverageRate24</br>73-BadDebtsWriteOffSalesAverageRate24 (76/80/50)                    |

**Steuerfreie Umsätze mit Vorsteuerabzug**

| Zeile | Feld – Steuerbasis | Feld – Steuerbetrag | Description                                                                       | Suchergebnis                       |
|-----|----------------|------------------|-----------------------------------------------------------------------------------|-------------------------------------|
| 26  | 41             | *Kein Steuerbetrag*  | Innergemeinschaftliche Lieferungen an Kunden mit Umsatzsteuer-Identifikationsnummer.                       | 26-EUSales                          |
| 27  | 44             | *Kein Steuerbetrag*  | Innergemeinschaftliche Lieferungen von Neufahrzeugen an Käufer ohne Umsatzsteuer-Identifikationsnummer.    | 27-EUSalesNewVehicles               |
| 28  | 49             | *Kein Steuerbetrag*  | Innergemeinschaftliche Lieferungen von Neufahrzeugen außerhalb eines Unternehmens.                     | 28-EUSalesNewVehiclesOutsideCompany |
| 29  | 43             | *Kein Steuerbetrag*  | Sonstige steuerfreie Verkäufe mit Vorsteuerabzug, wie Exportlieferungen. | 29-ExportOtherTaxFreeSales          |

**Steuerfreie Umsätze ohne Vorsteuerabzug**

| Zeile | Feld – Steuerbasis | Feld – Steuerbetrag | Description                                            | Suchergebnis                           |
|-----|----------------|------------------|--------------------------------------------------------|-----------------------------------------|
| 30  | 48             | *Kein Steuerbetrag*  | Steuerfreie Verkäufe ohne Vorsteuerabzug. | 30-TaxFreeSalesWithoutInputTaxDeduction |

**Innergemeinschaftliche Anschaffungen**

| Zeile | Feld – Steuerbasis | Feld – Steuerbetrag | Description                                                                                                                   | Suchergebnis                                                    |
|-----|----------------|------------------|-------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| 33  | 91             | *Kein Steuerbetrag*  | Steuerfreier innergemeinschaftlicher Erwerb einiger Objekte und Anlagegold.                                                    | 33-TaxFreeEUPurchase                                             |
| 34  | 89             | Ohne Code     | Steuerpflichtiger innergemeinschaftlicher Erwerb mit einem Steuersatz von 19 Prozent.                                                             | 34-EUPurchaseStandard</br>34-UseTaxEUPurchaseStandard (89/61)        |
| 35  | 93             | Ohne Code     | Steuerpflichtiger innergemeinschaftlicher Erwerb mit einem Steuersatz von 7 Prozent.                                                              | 35-EUPurchaseReduced</br>35-UseTaxEUPurchaseReduced (93/61)          |
| 36  | 95             | 98               | Steuerpflichtiger innergemeinschaftlicher Erwerb mit aneren Steuersätzen.                                                                      | 36-EUPurchaseOtherRates</br>36-UseTaxEUPurchaseOtherRates (95/98/61) |
| 37  | 94             | 96               | Steuerpflichtiger innergemeinschaftlicher Erwerb von Neufahrzeugen von Lieferanten ohne Umsatzsteuer-Identifikationsnummer zum allgemeinen Steuersatz. | 37-EUPurchaseVehicles</br>37-UseTaxEUPurchaseVehicles (94/96/61)     |

**ABSCHNITT – BEGÜNSTIGTER ALS STEUERSCHULDNER**

| Zeile | Feld – Steuerbasis | Feld – Steuerbetrag | Description                                                                        | Suchergebnis                                                                                        |
|-----|----------------|------------------|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| 40  | 46             | 47               | Sonstige Dienstleistungen eines Unternehmers, bezogen auf den Rest des Gemeinschaftsgebiets.        | 40-BeneficiaryTaxDebtor</br>40-UseTaxBeneficiaryTaxDebtor (46/47/66)                                                                              |
| 41  | 73             | 74               | Verkäufe gemäß § 13b Absatz 2 Nr.3 des UStG.                               | 41-BeneficiaryTaxDebtorRealEstateTransfer</br>41-UseTaxBeneficiaryTaxDebtorRealEstateTransfer (73/74/67) |
| 42  | 84             | 85               | Andere Dienstleistungen, die unter § 13b (2) Nr.1, 2 und 4 bis 12 des UStG fallen. | 42-BeneficiaryTaxDebtorOther</br>42-UseTaxBeneficiaryTaxDebtorOther (84/85/67)                           |

**ABSCHNITT – ERGÄNZENDE INFORMATIONEN ZUM VERKAUF**

| Zeile | Feld – Steuerbasis  | Feld – Steuerbetrag | Description                                                                                                | Suchergebnis                                                                                    |
|-----|-----------------|------------------|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| 48  | 42              | *Kein Steuerbetrag*  | Lieferungen des ersten Kunden im Fall von gemeinschaftsinternen Dreieckstransaktionen.                   | 48-DeliveriesFirstCustomerEUTriangular                                                           |
| 49  | 60              | *Kein Steuerbetrag*  | Steuerpflichtiger Umsatz des ausführenden Unternehmers, für den der Dienstleistungsempfänger die Steuer schuldet. | 49-SalesServicesReverseCharge                                                                    |
| 50  | 21              | *Kein Steuerbetrag*  | Andere nicht steuerpflichtige Dienstleistungen.                                                                                | 50-OtherServicesNonTaxable                                                                       |
| 51  | 45              | *Kein Steuerbetrag*  | Sonstige nicht steuerpflichtige Verkäufe, wenn der Erfüllungsort nicht in Deutschland liegt.                                    | 51-OtherSalesNonTaxable                                                                          |
| 52  | *Kein Steuerbetrag* | *Kein Steuerbetrag*  | MwSt.                                                                                                       | Zeile 20 + Zeile 21 + Zeile 22 + Zeile 24 + Zeile 34 + Zeile 35 + Zeile 36 + Zeile 37 + Zeile 40 + Zeile 41 + Zeile 42 |

**ABSCHNITT – ABZIEHBARE VORSTEUER**

| Zeile | Feld – Steuerbetrag | Description                                                                                                | Suchergebnis                                                                                                                                                                |
|-----|------------------|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 55  | 66               | Eingangsrechnungssteuerbeträge von anderen Unternehmen, Dienstleistungen und innergemeinschaftlichen Dreiecksgeschäften.     | 55-InputTax 40-UseTaxBeneficiaryTaxDebtor (46/47/66)</br>74-BadDebtsWriteOffInputTax (66/37) – mit Minuszeichen                                                                   |
| 56  | 61               | Vorsteuerbeträge aus der innergemeinschaftlichen Warenanschaffung.                                           | 56-InputTaxEUPurchase 34-UseTaxEUPurchaseStandard (89/61)</br>35-UseTaxEUPurchaseReduced (93/61)</br>36-UseTaxEUPurchaseOtherRates (95/98/61)</br>37-UseTaxEUPurchaseVehicles (94/96/61) |
| 57  | 62               | Angefallene Einfuhrumsatzsteuer.                                                                                 | 57-InputTaxImport                                                                                                                                                            |
| 58  | 67               | Vorsteuerbeträge aus Dienstleistungen im Sinne von 13b des UStG.                                        | 58-InputTaxServices</br>41-UseTaxBeneficiaryTaxDebtorRealEstateTransfer (73/74/67)</br>42-UseTaxBeneficiaryTaxDebtorOther (84/85/67)                                                 |
| 59  | 63               | Vorsteuerbeträge, die nach allgemeinen Durchschnittssätzen berechnet werden.                                  | 59-InputTaxAverageRates</br>74-BadDebtsWriteOffInputTaxAverageRates (63/37) – mit Minuszeichen                                                                                    |
| 60  | 59               | Vorsteuerabzug für innergemeinschaftliche Lieferungen von Neufahrzeugen außerhalb eines Unternehmens und Kleinbetriebe. | 60-InputTaxEUPurchaseNewVehicles</br>74-BadDebtsWriteOffInputTaxEUPurchaseNewVehicles (59/37) – mit Minuszeichen                                                                  |
| 61  | 64               | Korrektur des Vorsteuerabzug.                                                                     | 61-InputTaxCorrection                                                                                                                                                        |
| 62  | \-               | Der Restbetrag.                                                                                      | Zeile 52 – Zeile 55 – Zeile 56 – Zeile 57 – Zeile 58 – Zeile 50 – Zeile 60 – Zeile 61                                                                                                        |

**ABSCHNITT – ANDERE STEUERBETRÄGE**

| Zeile | Feld – Steuerbetrag | Description                                                                                                                                                                                                                                                         | Suchergebnis                                 |
|-----|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| 64  | 65               | Steuern aufgrund von Änderungen in der Form der Besteuerung und zusätzlicher Steuer auf besteuerte Anzahlungen usw. aufgrund von Änderungen des Steuersatzes.                                                                                                                                        | 64-AdditionalTaxDueChangeTaxRate              |
| 65  | 69               | Unrichtige oder ungerechtfertigte Steuerbeträge, die auf Rechnungen ausgewiesen sind, sowie Steuerbeträge, die nach § 6A Abs. 4 Satz 2, § 17 Abs. 1 Satz 7 oder § 25b Abs. 2 UStG geschuldet sind oder von ein Outsourcing-Unternehmen oder Lagerhalter. | 65-TaxDecreaseCorrection                      |
| 67  | 39               | Abzug des fixen Sondervorschusses für die dauerhafte Verlängerung. Diese Zeile wird in der Regel erst mit der letzten Vorankündigung des Steuerzeitraums ausgefüllt.                                                                                                  | Benutzereingabeparameter im Berichtsdialog |
| 68  | 83               | Die verbleibende Umsatzsteuervorauszahlung und der verbleibende Selbstbehalt. Fügen Sie dem Betrag ein Minuszeichen voran.                                                                                                                                                          | Zeile 62 + Zeile 64 – Zeile 65 – Zeile 66             |

**ABSCHNITT – ERGÄNZENDE INFORMATIONEN ZU ABZÜGEN**

| Zeile | Feld – Steuerbasis | Feld – Steuerbetrag | Description                                                            | Suchergebnis                                                                                                                                                                                                    |
|-----|----------------|------------------|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 73  | 50             | \-               | Herabsetzung der Steuerbemessungsgrundlage in den Zeilen 20 bis 24.                      | 73-BadDebtsWriteOffStandard (81/50)</br>73-BadDebtsWriteOffReduced (86/50)</br>73-BadDebtsWriteOffOtherRates (35/36/50)</br>73-BadDebtsWriteOffEUSalesAverageRate24 (77/50)</br>73-BadDebtsWriteOffSalesAverageRate24 (76/80/50) |
| 74  | \-             | 37               | Kürzung der abzugsfähigen Vorsteuerbeträge in den Zeilen 55, 59 und 60. | 74-BadDebtsWriteOffInputTax (66/37)</br>74-BadDebtsWriteOffInputTaxAverageRates (63/37)</br>74-BadDebtsWriteOffInputTaxEUPurchaseNewVehicles (59/37)                                                                     |

#### <a name="purchase-reverse-charge-vat"></a>Einkaufssteuerschuldumkehr

Wenn Sie Mehrwertsteuercodes so konfigurieren, dass eingehende Verlagerung der Steuerschuld unter Verwendung der Verbrauchsteuer gebucht wird, verknüpfen Sie Ihre Mehrwertsteuercodes mit dem Suchergebnis der **Nachschlagen von Berichtfeldern**, die „UseTax“ im Namen enthält.

Alternativ können Sie zwei separate Mehrwertsteuercodes konfigurieren: einen für die fällige Mehrwertsteuer und einen für den Mehrwertsteuerabzug. Verknüpfen Sie dann jeden Code mit den entsprechenden Lookup-Ergebnissen von **Nachschlagen von Berichtfeldern**.

Für steuerpflichtige innergemeinschaftliche Erwerbe zum Standardsatz konfigurieren Sie beispielsweise das Umsatzsteuerkennzeichen **UT_S_EU** mit der Gebrauchssteuer und verbinden sie mit dem **34-UseTaxEUPurchaseStandard**-Suchergebnis von **Nachschlagen von Berichtfeldern**. In diesem Fall werden Beträge, die die **UT_S_EU**-Mehrwertsteuercodes verwenden, in den Feldern 089 und 061 (Zeilen 34 und 56) wiedergegeben.

Alternativ konfigurieren Sie zwei Umsatzsteuerkennzeichen:

  - **VAT_S_EU**, das einen Steuersatz von -19 Prozent hat
  - **InVAT_S_EU**, das einen Steuersatz von 19 Prozent hat

Verknüpfen Sie dann die Codes mit den Such-Ergebnissen von **Nachschlagen von Berichtfeldern** auf die folgende Weise:

  - Assoziieren Sie **VAT_S_EU** mit dem **34-EUPurchaseStandard**-Nachschlageergebnis.
  - Assoziieren Sie **InVAT_S_EU** mit dem **56-InputTaxEUPurchase**-Nachschlageergebnis.

In diesem Fall werden Beträge, die die **VAT_S_EU**-Mehrwertsteuercodes verwenden, im Feld 089 (Zeile 34) wiedergegeben. Beträge, die die **InVAT_S_EU**-Mehrwertsteuercodes verwenden, werden im Feld 061 (Zeile 56) wiedergegeben.

Weitere Informationen über die Konfiguration von Verlagerung der Steuerschuld finden Sie unter [Verlagerung der Steuerschuld](emea-reverse-charge.md).

## <a name="configure-system-parameters"></a>Konfigurieren von Systemparametern

Um eine Umsatzsteuererklärung zu erstellen, müssen Sie die Steuernummer Ihrer Organisation konfigurieren.

1. Gehen Sie zu **Organisationsverwaltung** > **Organisationen** > **Juristische Personen**.
2. Wählen Sie die juristische Person und dann **Registrierungskennungen** aus.
3. Wählen oder erstellen Sie die Adresse in Deutschland und dann auf dem Inforegister **Registrierungskennungen** **Hinzufügen**.
4. Im Feld **Registrierungstyp** wählen Sie die Registrierungsart aus, die für Deutschland bestimmt ist und die die **Unternehmens-ID (COID)**-Registrierungskategorie verwendet.
5. Geben Sie in das Feld **Registrierungsnummer** die Steuernummer ein.
6. Auf der **Allgemein**-Registerkarte geben Sie im Feld **In Kraft** das Datum ein, an dem die Nummer gültig wird.

Weitere Informationen zum Einrichten von Registrierungskategorien und Registrierungstypen finden Sie unter [Registrierungskennung](emea-registration-ids.md).

## <a name="set-up-a-vat-declaration-for-germany"></a>Umsatzsteuererklärung für Deutschland einrichten

### <a name="import-er-configurations"></a>ER Konfigurationen importieren

Öffnen Sie den **Elektronische Berichterstattung**-Arbeitsbereich und importieren Sie die folgenden Versionen oder höher dieser ER-Formate:

   - Mehrwertsteuererklärung Excel (DE).Version.101.16.12.xml
   - Mehrwertsteuererklärung XML (DE).Version.101.16.xml

### <a name="set-up-application-specific-parameters-for-vat-declaration-fields"></a><a name="set-up-application-specific-parameters-for-vat-declaration-fields"></a>Anwendungsspezifische Parameter für Umsatzsteuererklärungsfelder einrichten

Um automatisch eine MwSt.-Erklärung zu generieren, ordnen Sie der Anwendung Mehrwertsteuercodes zu und suchen Sie die Ergebnisse in der ER-Konfiguration.

> [!NOTE]
> Es wird empfohlen, dass Sie die Funktion **Anwendungsspezifische Parameter aus früheren Versionen von ER-Formaten verwenden** im **Funktionsverwaltung**-Arbeitsbereich aktivieren. Wenn diese Funktion aktiviert ist, gelten Parameter, die für die frühere Version eines ER-Formats konfiguriert wurden, automatisch für die spätere Version desselben Formats. Wenn diese Funktion nicht aktiviert ist, müssen Sie anwendungsspezifische Parameter explizit für jede Formatversion konfigurieren. Die **Anwendungsspezifische Parameter aus früheren Versionen von ER-Formaten verwenden**-Funktion ist ab der Finance-Version 10.0.23 im **Funktionsverwaltung**-Arbeitsbereich verfügbar. Weitere Informationen zum Einrichten der Parameter eines ER-Formats für jede juristische Person finden Sie unter [Parameter eines ER-Formats pro juristischer Person einrichten](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-set-up.md).

Führen Sie diese Schritte aus, um zu definieren, welche Mehrwertsteuercodes welche Felder in der Mehrwertsteuererklärung generieren.

1. Gehen Sie zu **Arbeitsbereiche** > **Elektronisches Berichtswesen**, und wählen Sie dann **Berichtskonfigurationen**.
2. Wählen Sie die **Umsatzsteuererklärung XML (DE)**-Konfiguration, und wählen Sie dann **Konfigurationen \> Anwendungsspezifische Parametereinstellung**.
3. Wählen Sie auf der **Anwendungsspezifische Parameter**-Seite auf dem Inforegister **Nachschlagen** **Nachschlagen von Berichtfeldern**.
4. Legen Sie auf dem Inforegister **Bedingungen** die folgenden Felder fest, um die Mehrwertsteuercodes und Berichtsfelder zuzuordnen.

    | Feld                  | Description                                                                                                                                                                                                                                                                                                          |
    |------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Suchergebnis          | Wählen Sie den Wert des Berichtsfelds aus. Weitere Informationen zu den Werten und deren Zuordnung zu den Umsatzsteuererklärungszeilen finden Sie im [Übersicht über die Umsatzsteuererklärung](#vat-declaration-overview)-Abschnitt weiter oben in diesem Artikel.                                                                                               |
    | Steuercode               | Wählen Sie den Mehrwertsteuercode aus, der mit dem Berichtsfeld verknüpft werden soll. Gebuchte Steuertransaktionen, die den ausgewählten Mehrwertsteuercode verwenden, werden im entsprechenden Deklarationsfeld erfasst. Wir empfehlen Ihnen, die Umsatzsteuerkennzeichen so zu trennen, dass ein Umsatzsteuerkennzeichen Beträge in nur einem Deklarationsfeld generiert. |
    | Transaktionsklassifizierer | Wenn Sie genügend Mehrwertsteuercodes erstellt haben, um ein Deklarationsfeld zu bestimmen, wählen Sie **\*Nicht leer\*** aus. Wenn Sie nicht genügend Mehrwertsteuercodes erstellt haben, damit ein Mehrwertsteuercode Beträge in nur einem Deklarationsfeld generiert, können Sie einen Transaktionsklassifizierer einrichten. Folgende Transaktionsklassifizierer sind verfügbar:</br>-   **Kaufen**</br>-   **PurchaseExempt** (Steuerbefreiter Einkauf)</br>-   **PurchaseReverseCharge** (Vorsteuer aus Verlagerung der Steuerschuld)</br>-   **Vertrieb**</br>-   **SalesExempt** (Steuerbefreiter Verkauf)</br>-   **SalesReverseCharge** (Vorsteuer aus Verlagerung der Steuerschuld Einkauf oder Verkauf)</br>-   **Steuer verwenden**. </br>Für jeden Transaktionsklassifizierer steht auch ein Klassifikator für die Gutschrift zur Verfügung. Einer dieser Klassifikatoren ist beispielsweise **PurchaseCreditNote** (Gutschrift kaufen).</br>Stellen Sie sicher, dass Sie für jeden Mehrwertsteuercode zwei Zeilen erstellen: eine mit dem Transaktionsklassifikatorwert und eine mit dem Transaktionsklassifikator für den Gutschriftswert. |

    > [!NOTE]
    > Verknüpfen Sie alle Mehrwertsteuercodes mit den Nachschlageergebnissen. Wenn Mehrwertsteuercodes keine Werte in der Mehrwertsteuererklärung generieren sollen, ordnen Sie sie dem **Sonstiges**-Nachschlageergebnis zu.

    ![Seite für anwendungsspezifische Parameter](media/69ecb881f12819259ca166b9b98b8303.jpg)

5. Ändern Sie im Feld **Status** den Wert in **Abgeschlossen**.
6. Wählen Sie im Aktivitätsbereich **Exportieren** aus, um die Einstellungen der anwendungsspezifischen Parameter zu exportieren.
7. Wählen Sie die **Umsatzsteuererklärung Excel (DE)**-Konfiguration aus, und wählen Sie dann im Aktivitätsbereich **Importieren** aus, um die Parameter zu importieren, die Sie für **Umsatzsteuererklärung XML (DE)** konfiguriert haben.
8. Wählen Sie im Feld **Status** die Option **Abgeschlossen** aus.

### <a name="set-up-the-vat-reporting-format-for-preview-amounts-in-excel"></a>Richten Sie das Mehrwertsteuer-Berichtsformat für Vorschaubeträge in Excel ein

1. Suchen Sie im Arbeitsbereich **Funktionsverwaltung** die Funktion **MwSt.-Abrechnungs-Formatberichte** udn aktivieren Sie sie.
2. Wechseln Sie zu **Hauptbuch** > **Einrichtung** > **Hauptbuchparameter**.
3. Auf der **Mehrwertsteuer**-Registerkarte im Inforegister **Steueroptionen** im Feld **MwSt.-Abrechnungs-Formatzuordnung** wählen Sie **Umsatzsteuererklärung Excel (DE)** aus.

   Dieses Format wird gedruckt, wenn Sie den **Mehrwertsteuer für Abrechnungszeitraum melden**-Bericht ausführen. Es wird auch gedruckt, wenn Sie **Drucken** auf der **Umsatzsteuerzahlungen**-Seite auswählen.

4. Wenn Sie die Korrekturen melden müssen, legen Sie im Abschnitt **Sonderbericht** die Option **Korrekturen einbeziehen** auf **Ja** fest.
5. Auf der Seite **Steuerbehörden** wählen Sie die Steuerbehörde aus, und wählen Sie im **Berichtslayout**-Feld **Standard**.

Wenn Sie die Mehrwertsteuererklärung in einer juristischen Person konfigurieren, die über [mehrere Umsatzsteuerregistrierungen](emea-reporting-for-multiple-vat-registrations.md) verfügt, folgen Sie diesen Schritten:

1. Wechseln Sie zu **Hauptbuch** > **Einrichtung** > **Hauptbuchparameter**.
2. Auf der **Mehrwertsteuer**-Registerkarte, auf dem Inforegister **Elektronische Berichte für Länder/Regionen** in der Zeile für **DEU** wählen Sie das **Umsatzsteuererklärung Excel (DE)**-ER-Format.

## <a name="set-up-electronic-messages"></a>Elektronische Nachrichten einrichten

### <a name="download-and-import-the-data-package-that-has-example-settings-for-electronic-messages"></a>Laden und importieren Sie das Datenpaket mit Beispieleinstellungen für elektronische Nachrichten

Das Datenpaket enthält elektronische Nachrichteneinstellungen, die verwendet werden, um die Umsatzsteuererklärung im XML-Format zu generieren und anschließend in Excel anzuzeigen. Sie können diese Einstellungen erweitern oder eigene erstellen. Weitere Informationen zum Arbeiten mit elektronischen Nachrichten und zum Erstellen eigener Einstellungen finden Sie unter [Elektronische Nachrichtenübermittlung](../general-ledger/electronic-messaging.md).

1. In [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/v2) wählen Sie in der Bibliothek für freigegebene Anlagen **Datenpaket** als Anlagentyp und laden dann das **DE Umsatzsteuererklärung EM-Paket** herunter. Der heruntergeladene Dateiname ist **DE Umsatzsteuererklärung EM-Paket.zip**.
2. In Dynamics 365 Finance wählen Sie im **Datenverwaltung**-Arbeitsbereich **Importieren** aus.
3. Geben Sie auf dem Inforegister **Importieren** im Feld **Gruppenname** einen Namen für den Auftrag ein.
4. Wählen Sie im Inforegister **Ausgewählte Entitäten** **Datei hinzufügen** aus.
5. Im **Datei hinzufügen**-Dialogfeld überprüfen Sie, ob das **Quelldatenformat**-Feld auf **Paket** gesetzt ist, wählen **Hochladen und hinzufügen** aus, und wählen dann die zuvor heruntergeladene ZIP-Datei aus.
6. Wählen Sie **Schließen** aus.
7. Nachdem die Datenentitäten hochgeladen wurden, wählen Sie im Aktivitätsbereich **Importieren**.
8. Gehen Sie zu **Steuer** > **Anfragen und Berichte** > **Elektronische Nachrichten** > **Elektronische Nachrichten**, und validieren Sie die importierte elektronische Nachrichtenverarbeitung.

### <a name="configure-electronic-messages"></a>Elektronische Nachrichten konfigurieren

1. Gehen Sie zu **Steuer** > **Einrichten** > **Elektronische Nachrichten** > **Datensatzauffüllungsaktivitäten**.
2. Wählen Sie die Zeile für **DE Umsatzsteuererklärungsdatensätze ausfüllen**, und wählen Sie dann **Abfrage bearbeiten**.
3. Verwenden Sie den Filter, um die Abrechnungszeiträume anzugeben, die in den Bericht aufgenommen werden sollen.
4. Wenn Sie Steuertransaktionen aus anderen Abrechnungszeiträumen in einer anderen Meldung melden müssen, erstellen Sie eine neue **Datensätze ausfüllen**-Aktion, und wählen Sie die entsprechenden Abrechnungszeiträume aus.

## <a name="preview-the-vat-declaration-in-excel"></a>Vorschau der Mehrwertsteuererklärung in Excel

### <a name="preview-the-vat-declaration-in-excel-from-the-report-sales-tax-for-settlement-period-periodic-task"></a>Vorschau der Mehrwertsteuererklärung in Excel aus der periodischen Aufgabe Umsatzsteuer für Abrechnungszeitraum melden

1. Wechseln Sie zu **Steuer** > **Periodische Aufgaben** > **Erklärungen** > **Mehrwertsteuer** > **Mehrwertsteuer für Abrechnungszeitraum melden**.
2. Wählen Sie im Feld **Abrechnungszeitraum** einen Wert aus.
3. Wählen Sie im Feld **Mehrwertsteuer, Zahlungsversion** einen der folgenden Werte aus:

    - **Original**: Generieren Sie einen Bericht für die Mehrwertsteuertransaktionen der ursprünglichen Mehrwertsteuerzahlung oder bevor die Mehrwertsteuerzahlung generiert wird.
    - **Korrekturen**: Einen Mehrwertsteuerbericht generieren für alle nachfolgenden Mehrwertsteuerzahlungen für das Periodenintervall.
    - **Gesamtliste**: Einen Mehrwertsteuerbericht generieren für alle Mehrwertsteuerbuchungen für das Periodenintervall, einschließlich der Originake und aller Korrekturen.

4. Wählen Sie im Feld **Von Datum** das Startdatum des Steuererklärungszeitraums aus.
5. **OK** wählen und den Excel-Bericht überprüfen.

### <a name="settle-and-post-sales-tax"></a><a name="settle-and-post-sales-tax"></a>Mehrwertsteuer abrechnen und buchen

1. Wechseln Sie zu **Steuer** > **Periodische Aufgaben** > **Meldungen** > **Mehrwertsteuer** > **Mehrwertsteuer abrechnen und buchen**.
2. Wählen Sie im Feld **Abrechnungszeitraum** einen Wert aus.
3. Wählen Sie im Feld **Mehrwertsteuer, Zahlungsversion** einen der folgenden Werte aus:

    - **Original**: Generieren Sie die ursprüngliche Mehrwertsteuerzahlung für den Abrechnungszeitraum.
    - **Letzte Korrekturen**: Generieren Sie eine Korrekturumsatzsteuerzahlung, nachdem die ursprüngliche Umsatzsteuerzahlung für den Abrechnungszeitraum erstellt wurde.

4. Wählen Sie im Feld **Von Datum** das Startdatum des Steuererklärungszeitraums aus.
5. Wählen Sie **OK** aus.

### <a name="preview-the-vat-declaration-in-excel-from-a-sales-tax-payment"></a>Vorschau der Mehrwertsteuererklärung in Excel aus einer Mehrwertsteuerzahlung

1. Gehen Sie zu **Steuer** > **Anfragen und Berichte** > **Umsatzsteueranfragen** > **Umsatzsteuerzahlungen**, und wählen Sie eine Mehrwertsteuer-Zahlungszeile aus.
2. Wählen Sie **Bericht drucken** aus, und wählen Sie dann **OK** aus.
3. Überprüfen Sie die Excel-Datei, die für die ausgewählte Mehrwertsteuerzahlungszeile generiert wird.

    > [!NOTE]
    > Der Bericht wird nur für die ausgewählte Mehrwertsteuerzahlungszeile generiert. Wenn Sie z. B. eine Korrekturmeldung mit allen Korrekturen für die Periode oder eine Ersatzmeldung mit den Originaldaten und allen Korrekturen erstellen möchten, verwenden Sie die periodische Aufgabe **Mehrwertsteuer für Abrechnungszeitraum melden**.

## <a name="generate-a-vat-declaration-from-electronic-messages"></a>Erstellen Sie eine Mehrwertsteuererklärung aus elektronischen Nachrichten

Wenn Sie elektronische Nachrichten zum Generieren des Berichts verwenden, können Sie Steuerdaten von mehreren juristischen Personen erfassen. Weitere Informationen finden Sie im Abschnitt [Mehrwertsteuererklärung für mehrere juristische Personen ausführen](#run-a-vat-declaration-for-multiple-legal-entities) weiter unten in diesem Artikel.

Das folgende Verfahren gilt für das Beispiel für die Verarbeitung elektronischer Nachrichten, das Sie aus der LCS Shared Asset Library importiert haben.

1. Wechseln Sie zu **Steuer** > **Abfragen und Berichte** > **Elektronische Nachrichten** > **Elektronische Nachrichten**.
2. Wählen Sie im linken Fensterbereich **DE Umsatzsteuererklärung**.
3. Auf dem Inforegister **Mitteilungen** wählen Sie **Neu** aus und dann im **Verarbeitung ausführen**-Dialogfeld **OK**.
4. Wählen Sie die erstellte Meldungszeile aus, geben Sie eine Beschreibung ein und geben Sie dann das Start- und Enddatum für die Meldung an.

    > [!NOTE]
    > Die Schritte 5 bis 7 sind optional.

5. Optional: Auf dem Inforegister **Mitteilungen** wählen Sie **Daten sammeln** aus, und wählen Sie dann **OK**. Die zuvor generierten Umsatzsteuerzahlungen werden der Nachricht hinzugefügt. Weitere Informationen finden Sie im Abschnitt [Mehrwertsteuer abrechnen und buchen](#settle-and-post-sales-tax) am Anfang dieses Artikels. Wenn Sie diesen Schritt überspringen, können Sie trotzdem eine Umsatzsteuererklärung erstellen, indem Sie das **Version der Steuererklärung**-Feld im **Erklärung**-Dialogfeld verwenden.
6. Optional: Auf dem Inforegister **Nachrichtenelemente** überprüfen Sie die Mehrwertsteuerzahlungen, die zur Verarbeitung übertragen werden. Standardmäßig werden alle Mehrwertsteuerzahlungen des ausgewählten Zeitraums berücksichtigt, die in keiner anderen Nachricht derselben Verarbeitung enthalten waren.
7. Optional: Wählen Sie **Originaldokument**, um die Umsatzsteuerzahlungen zu überprüfen, oder wählen Sie **Löschen**, um Umsatzsteuerzahlungen von der Verarbeitung auszuschließen. Wenn Sie diesen Schritt überspringen, können Sie trotzdem eine Umsatzsteuererklärung erstellen, indem Sie das **Version der Steuererklärung**-Feld im **Erklärung**-Dialogfeld verwenden.
8. Wählen Sie im Inforegister **Nachrichten** **Status aktualisieren** aus. Im **Status aktualisieren**-Dialogfeld wählen Sie **Bereit zum Generieren**, und wählen Sie dann **OK**. Stellen Sie sicher, dass der Nachrichtenstatus geändert wurde in **Bereit zum Generieren**.
9. Wählen Sie **Bericht generieren** aus. Um die Beträge der Mehrwertsteuererklärung in der Vorschau anzuzeigen, wählen Sie im **Verarbeitung ausführen**-Dialogfeld **Vorschaubericht**, und wählen Sie dann **OK**.
10. Legen Sie im Dialogfeld **Elektronische Berichtsparameter** die folgenden Felder fest und wählen Sie dann **OK** aus.

    | **Feld**                                   | **Beschreibung**                                                                                                                                                                                                              |
    |---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Ausgleichsperiode                           | Wählen Sie Ausgleichsperiode aus. Wenn Sie **Daten sammeln** in Schritt 5 ausgewählt haben, können Sie dieses Feld leer lassen. Der Bericht wird für die Umsatzsteuertransaktionen erstellt, die in den eingezogenen Umsatzsteuerzahlungen enthalten sind. |
    | Steuererklärungsversion                     | Wählen Sie einen der folgenden Werte aus:</br>-   **Original** – Generieren Sie einen Bericht für die Mehrwertsteuertransaktionen der ursprünglichen Mehrwertsteuerzahlung oder bevor die Mehrwertsteuerzahlung generiert wird.</br>-   **Korrekturen** – Einen Mehrwertsteuerbericht generieren für alle nachfolgenden Mehrwertsteuerzahlungen für das Periodenintervall.</br>-   **Gesamtliste** – Einen Mehrwertsteuerbericht generieren für alle Mehrwertsteuerbuchungen für das Periodenintervall, einschließlich der Originake und aller Korrekturen.|
    | Steuerbeauftragter | Wählen Sie ggf. die Partei aus, die ein Steuervertreter für die Mehrwertsteuererklärung ist. Informationen über die ausgewählte Partei werden ins **DatenLieferant**-XML-Element exportiert. |
    | Ansprechpartner | Wählen Sie eine Person in der Organisation aus, die ein Datenlieferant ist. Informationen über die ausgewählte Person werden ins **DatenLieferant**-XML-Element exportiert. |
    | Korrekturretoure | Wählen Sie **Ja** aus, wenn es sich um eine korrigierende Mehrwertsteuererklärung handelt. In diesem Fall hat das XML-Element KZ10 den Wert **1**.|
    | Weitere Dokumente | Wählen Sie **Ja**, wenn Sie auch Belege mitsenden. In diesem Fall hat das XML-Element KZ22 den Wert **1**.|
    | Die SEPA-Lastschriftmandat wird ausnahmsweise widerrufen| Wählen Sie **Ja** aus, wenn das SEPA-Lastschriftmandat ausnahmsweise für diese Voranmeldefrist widerrufen wird. Zum Beispiel wegen Verrechnungsanfragen. Ein eventueller Restbetrag ist gesondert zu begleichen. In diesem Fall hat das XML-Element KZ26 den Wert **1**. |
    | Anrechnung des gewünschten Erstattungsbetrages | Wählen Sie **Ja** aus, wenn eine Aufrechnung des Erstattungsbetrages gewünscht oder der Erstattungsbetrag abgetreten ist. In diesem Fall hat das XML-Element KZ29 den Wert **1**. |
    | Sondervorauszahlung Dauerverlängerung | Geben Sie den Abzugsbetrag des fixen Sondervorschusses für die dauerhafte Verlängerung ein. Dieser Abzugsbetrag wird in der Regel erst in der letzten Voranmeldung des Besteuerungszeitraums abgeschlossen. Der Betrag wird in Zeile 67 (Feld 39) und XML-Element KZ39 der Mehrwertsteuererklärung exportiert. |

11. Wählen Sie die Schaltfläche **Anhänge** rechts oben auf der Seite aus, und wählen Sie dann **Öffnen** aus.
12. Überprüfen Sie die Beträge im Excel-Dokument und wählen Sie dann **Bericht generieren**.
13. Um die Beträge der Mehrwertsteuererklärung im XML-Format zu generieren, wählen Sie im **Verarbeitung ausführen**-Dialogfeld **Bericht generieren**, und wählen Sie dann **OK**.
14. Legen Sie im **Elektronische Berichtsparameter**-Dialogfeld die Felder wie in Schritt 10 beschrieben fest.
15. Wählen Sie **Anhänge** in der oberen rechten Ecke der Seite aus und laden Sie Datei herunter, und verwenden Sie sie für Ihre Einreichung bei der Steuerbehörde.

## <a name="run-a-vat-declaration-for-multiple-legal-entities"></a><a name="run-a-vat-declaration-for-multiple-legal-entities"></a>Mehrwertsteuererklärung für mehrere juristische Personen ausführen

Um die Formate zum Melden der Umsatzsteuererklärung für eine Gruppe von juristischen Personen zu verwenden, müssen Sie zunächst die anwendungsspezifischen Parameter der ER-Formate für Umsatzsteuerkennzeichen aller erforderlichen juristischen Personen einrichten.

### <a name="set-up-electronic-messages-to-collect-tax-data-from-several-legal-entities"></a>Richten Sie elektronische Nachrichten ein, um Steuerdaten von mehreren juristischen Personen zu sammeln

Befolgen Sie diese Schritte, um elektronische Nachrichten einzurichten, die Daten von mehreren juristischen Personen sammeln.

1. Wechseln Sie zu **Arbeitsbereiche** > **Funktionsverwaltung**.
2. Suchen und wählen Sie die **Unternehmensübergreifende Abfragen für Aktivitäten zum Auffüllen von Datensätzen**-Funktion in der Liste und wählen Sie dann **Jetzt aktivieren**.
3. Gehen Sie zu **Steuer** > **Einrichten** > **Elektronische Nachrichten \> Datensatzauffüllungsaktivitäten**.
4. Auf der **Aktion zum Auffüllen von Datensätzen**-Seite wählen Sie die Zeile für **DE Umsatzsteuererklärungsdatensätze ausfüllen**.

   Im **Einrichtung von Datenquellen**-Raster ist ein neues **Unternehmen**-Feld vorhanden. Bei vorhandenen Datensätzen zeigt dieses Feld die Kennung der aktuellen juristischen Person an.

5. Im Raster **Einrichtung von Datenquellen** fügen Sie für jede weitere juristische Person, die in die Berichterstellung einbezogen werden muss, eine Zeile hinzu. Legen Sie für jede neue Zeile die folgenden Felder fest:

    | Feld                  | Description                                                                                                                   |
    |------------------------|-------------------------------------------------------------------------------------------------------------------------------|
    | Name                   | Geben Sie einen Wert ein, der Ihnen hilft zu verstehen, woher dieser Datensatz stammt. Geben Sie beispielsweise **Umsatzsteuerzahlung der Tochtergesellschaft 1** ein. |
    | Nachrichtenelementtyp      | Wählen Sie **Umsatzsteuererklärung**. Dieser Wert ist der einzige Wert, der für alle Datensätze verfügbar ist.                                    |
    | Kontenart           | **Alle** auswählen.                                                                                                               |
    | Mastertabellenname      | Legen Sie **TaxReportVoucher** für alle Aufzeichnungen fest.                                                                             |
    | Feld „Dokumentnummer”  | Legen Sie **Beleg** für alle Aufzeichnungen fest.                                                                                      |
    | Feld „Dokumentdatum”    | Legen Sie **TransDate** für alle Aufzeichnungen fest.                                                                                    |
    | Feld „Dokumentenkonto” | Legen Sie **TaxPeriod** für alle Aufzeichnungen fest.                                                                                    |
    | Unternehmen                | Wählen Sie die ID der juristischen Person aus.                                                                                            |
    | Benutzerabfrage             | Dieses Kontrollkästchen wird automatisch aktiviert, wenn Sie Kriterien definieren, indem Sie **Abfrage bearbeiten** auswählen.                                 |

6. Wählen Sie für jede neue Zeile **Abfrage bearbeiten** aus und geben Sie eine Ausgleichsperiode an, das für die im Feld **Unternehmen** der Zeile angegebene juristische Person spezifisch ist.

Wenn die Einrichtung abgeschlossen ist, sammelt die **Daten sammeln**-Funktion auf der **Elektronische Nachrichten**-Seite Mehrwertsteuerzahlungen von allen juristischen Personen, die Sie definiert haben.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
