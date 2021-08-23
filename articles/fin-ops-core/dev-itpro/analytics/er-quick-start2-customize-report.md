---
title: Anpassen eines EB-Formats, um ein benutzerdefiniertes elektronisches Dokument zu generieren
description: In diesem Thema wird erläutert, wie Sie ein von Microsoft bereitgestelltes EB-Format (Elektronische Berichterstellung) so anpassen, dass ein benutzerdefiniertes elektronisches Dokument generiert wird.
author: NickSelin
ms.date: 06/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERParameters, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner, ERVendorTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom:
- "220314"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2ec7f5bcf9f01512d22f502a4b512f2919b3caf348eb1f5c4365238d6fd3f476
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6770019"
---
# <a name="adjust-an-er-format-to-generate-a-custom-electronic-document"></a>Anpassen eines EB-Formats, um ein benutzerdefiniertes elektronisches Dokument zu generieren

[!include[banner](../includes/banner.md)]

Die Prozeduren in diesem Thema erläutern, wie ein Benutzer mit der Rolle des Systemadministrators oder des funktionalen Beraters für die elektronische Berichterstellung die folgenden Aufgaben ausführen kann:

- Konfigurieren der Parameter für das [Framework für elektronische Berichterstellung (EB)](general-electronic-reporting.md).
- Importieren von EB-Konfigurationen, die von Microsoft bereitgestellt und zum Generieren einer Zahlungsdatei verwendet werden, während eine [Kreditorenzahlung](../../../finance/cash-bank-management/tasks/vendor-payment-overview.md) verarbeitet wird.
- Erstellen einer benutzerdefinierten Version einer standardmäßigen EB-Formatkonfiguration, die von Microsoft bereitgestellt wird.
- Ändern der benutzerdefinierten EB-Formatkonfiguration, sodass Zahlungsdateien generiert werden, die den Anforderungen einer bestimmten Bank entsprechen.
- Übernehmen von Änderungen, die an der standardmäßigen EB-Formatkonfiguration vorgenommen wurden, in die benutzerdefinierte EB-Formatkonfiguration.

Alle der folgenden Prozeduren können im **GBSI**-Unternehmen ausgeführt werden. Eine Codierung ist nicht erforderlich.

- [Konfigurieren des EB-Frameworks](#ConfigureFramework)

    - [Parameter der elektronischen Berichterstellung konfigurieren](#ConfigureParameters)
    - [Aktivieren eines EB-Konfigurationsanbieters](#ActivateProvider)

        - [Überprüfen der Liste der EB-Konfigurationsanbieter](#ReviewProvidersList)
        - [Hinzufügen eines neuen EB-Konfigurationsanbieters](#ActivateProvider)
        - [Aktivieren eines EB-Konfigurationsanbieters](#ActivateAddedProvider)

- [Importieren der standardmäßigen EB-Formatkonfigurationen](#ImportERSolution1)

    - [Importieren der standardmäßigen EB-Konfigurationen](#ImportERFormat1)
    - [Überprüfen der importierten EB-Konfigurationen](#ReviewImportedERSolution)

- [Vorbereiten einer Kreditorenzahlung zur Verarbeitung](#PrepareVendorPayment)

    - [Hinzufügen von Bankdaten für ein Kreditorenkonto](#AddBankAccount)
    - [Eingeben einer Kreditorenzahlung](#EnterVendorPayment)

- [Verarbeiten einer Kreditorenzahlung durch Verwendung des standardmäpigen EB-Formats](#ProcessVendorPayment1)

    - [Einrichten der elektronischen Zahlungsmethode](#ConfigureMethodOfPayment1)
    - [Verarbeiten einer Kreditorenzahlung](#ProcessPayment1)

- [Anpassen des standardmäßigen EB-Formats](#CustomizeProvidedFormat)

    - [Erstellen eines benutzerdefinierten Formats](#DeriveProvidedFormat)
    - [Bearbeiten eines benutzerdefinierten Formats](#ConfigureDerivedFormat)
    - [Markieren eines benutzerdefinierten Formats als ausführbar](#MarkFormatRunnable)

- [Verarbeiten einer Kreditorenzahlung durch Verwendung des benutzerdefinierten EB-Formats](#ProcessVendorPayment2)

    - [Einrichten der elektronischen Zahlungsmethode](#ConfigureMethodOfPayment2)
    - [Verarbeiten einer Kreditorenzahlung](#ProcessPayment2)

- [Importieren neuer Versionen der standardmäßigen EB-Formatkonfigurationen](#ImportERSolution2)

    - [Importieren neuer Versionen der standardmäßigen EB-Konfigurationen](#ImportERFormat2)
    - [Überprüfen der importierten EB-Formatkonfigurationen](#ReviewImportedERFormat)

- [Übernehmen der Änderungen in der neuen Version eines importierten Formats in ein benutzerdefiniertes Format](#AdoptNewBaseVersion)

    - [Vervollständigen der aktuellen Entwurfsversion eines benutzerdefinierten Formats](#CompleteDerivedFormat)
    - [Zurücksetzen eines benutzerdefinierten Formats auf eine neue Basisversion](#RebaseDerivedFormat)
    - [Verarbeiten einer Kreditorenzahlung durch Verwendung eines zurückgesetzten EB-Formats](#ProcessPayment3)

- [Zusätzliche Ressourcen](#References)

## <a name="configure-the-er-framework"></a><a id="ConfigureFramework"></a>Konfigurieren des EB-Frameworks

Als Benutzer mit der Rolle des funktionalen Beraters für die elektronische Berichterstellung müssen Sie den minimalen Satz von EB-Parametern konfigurieren, bevor Sie das EB-Framework zum Entwerfen einer benutzerdefinierten Version eines standardmäßigen EB-Formats verwenden können.

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a>Parameter der elektronischen Berichterstellung konfigurieren

1. Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.
2. Wählen Sie auf der Seite **Lokalisierungskonfigurationen** im Bereich **Zugehörige Links** die Option **Parameter für elektronische Berichterstellung** aus.
3. Auf der Seite **Parameter für elektronische Berichterstellung** legen Sie auf der Registerkarte **Allgemein** die Option **Entwurfsmodus aktivieren** auf **Ja** fest.
4. Legen Sie auf der Registerkarte **Anhänge** die folgenden Parameter fest:

    - Wählen Sie im Feld **Konfigurationen** den **Dateityp** für das **USMF**-Unternehmen aus.
    - Wählen Sie in den Feldern **Einzelvorgangsarchiv**, **Temporär**, **Grundlage** und **Andere** den **Dateityp** aus.

Weitere Informationen zu EB-Parametern finden Sie unter [Konfigurieren des EB-Frameworks](electronic-reporting-er-configure-parameters.md).

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a>Aktivieren eines EB-Konfigurationsanbieters

Jede hinzugefügte EB-Konfiguration wird als Eigentum eines EB-Konfigurationsanbieters markiert. Der EB-Konfigurationsanbieter, der im Arbeitsbereich **Elektronische Berichterstellung** aktiviert ist, wird zu diesem Zweck verwendet. Daher müssen Sie im Arbeitsbereich **Elektronische Berichterstellung** einen EB-Konfigurationsanbieter aktivieren, bevor Sie mit dem Hinzufügen oder Bearbeiten von EB-Konfigurationen beginnen.

> [!NOTE]
> Nur der Besitzer einer EB-Konfiguration kann diese bearbeiten. Daher muss im Arbeitsbereich **Elektronische Berichterstellung** der entsprechende EB-Konfigurationsanbieter aktiviert werden, bevor eine EB-Konfigurationen bearbeitet werden kann.

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a>Überprüfen der Liste der EB-Konfigurationsanbieter

1. Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.
2. Wählen Sie auf der Seite **Lokalisierungskonfigurationen** im Bereich **Zugehörige Links** die Option **Konfigurationsanbieter** aus.
3. Auf der Seite **Konfigurationsanbietertabelle** hat jeder Anbieterdatensatz einen eindeutigen Namen und eine eindeutige URL. Überprüfen Sie den Inhalt dieser Seite. Wenn bereits ein Datensatz für **Litware, Inc.** (`https://www.litware.com`) vorhanden ist, überspringen Sie die nächste Prozedur [Hinzufügen eines neuen EB-Konfigurationsanbieters](#ActivateProvider).

#### <a name="add-a-new-er-configuration-provider"></a><a id="ActivateProvider"></a>Hinzufügen eines neuen EB-Konfigurationsanbieters

1. Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.
2. Wählen Sie auf der Seite **Lokalisierungskonfigurationen** im Bereich **Zugehörige Links** die Option **Konfigurationsanbieter** aus.
3. Wählen Sie auf der Seite **Konfigurationsanbieter** die Option **Neu** aus.
4. Geben Sie im Feld **Name** **Litware, Inc.** ein.
5. Geben Sie im Feld **Internetadresse** `https://www.litware.com` ein.
6. Wählen Sie **Speichern** aus.

#### <a name="activate-an-er-configuration-provider"></a><a id="ActivateAddedProvider"></a>Aktivieren eines EB-Konfigurationsanbieters

1. Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.
2. Wählen Sie auf der Seite **Lokalisierungskonfigurationen** im Bereich **Konfigurationsanbieter** die Kachel **Litware, Inc.** aus. Wählen Sie dann **Als aktiv festlegen** aus.

Weitere Informationen zu EB-Konfigurationsanbietern finden Sie unter [Erstellen von Konfigurationsanbietern und Markieren als aktiv](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="import-the-standard-er-format-configurations"></a><a id="ImportERSolution1"></a>Importieren der standardmäßigen EB-Formatkonfigurationen

### <a name="import-the-standard-er-configurations"></a><a id="ImportERFormat1"></a>Importieren der standardmäßigen EB-Konfigurationen

Um Ihrer aktuellen Instanz von Microsoft Dynamics 365 Finance die standardmäßigen EB-Konfigurationen hinzuzufügen, müssen Sie sie aus dem EB-[Repository](general-electronic-reporting.md#Repository) importieren, das für diese Instanz konfiguriert wurde.

1. Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.
2. Wählen Sie auf der Seite **Lokalisierungskonfigurationen** im Bereich **Konfigurationsanbieter** die Kachel **Microsoft** aus. Wählen Sie dann **Repositorys** aus, um die Liste der Repositorys für den Microsoft-Anbieter anzuzeigen.
3. Wählen Sie auf der Seite **Konfigurationsrepositorys** das Repository des Typs **Global** aus. Wählen Sie dann **Öffnen** aus. Wenn Sie aufgefordert werden, das Herstellen einer Verbindung zum Regulatory Configuration Service zu autorisieren, folgen Sie den Autorisierungsanweisungen.
4. Wählen Sie auf der Seite **Konfigurationsrepositorys** in der Konfigurationsstruktur im linken Bereich die Formatkonfiguration **BACS (UK)** aus.
5. Wählen Sie auf dem Inforegister **Versionen** die Version **1.1** der ausgewählten EB-Formatkonfiguration aus.
6. Wählen Sie **Importieren** aus, um die ausgewählte Version aus dem globalen Repository auf die aktuelle Finance-Instanz herunterzuladen.

![Konfigurationsrepository-Seite.](./media/er-quick-start2-import-solution1.png)

> [!TIP]
> Wenn Sie Probleme beim Zugriff auf das [globale Repository](er-download-configurations-global-repo.md) haben, können Sie für das [Herunterladen von Konfigurationen](download-electronic-reporting-configuration-lcs.md) stattdessen Microsoft Dynamics Lifecycle Services (LCS) verwenden.

### <a name="review-the-imported-er-configurations"></a><a id="ReviewImportedERSolution"></a>Überprüfen der importierten EB-Konfigurationen

1. Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.
2. Auf der Seite **Lokalisierungskonfigurationen** im Abschnitt **Konfigurationen** wählen Sie die Kachel **Berichterstellungskonfigurationen** aus.
3. Erweitern Sie auf der Seite **Konfigurationen** in der Konfigurationsstruktur im linken Bereich den Punkt **Zahlungsmodell**.
4. Beachten Sie, dass zusätzlich zum ausgewählten EB-Format **BACS (UK)** weitere erforderliche EB-Konfigurationen importiert wurden. Stellen Sie sicher, dass die folgenden EB-Konfigurationen in der Konfigurationsstruktur verfügbar sind:

    - **Zahlungsmodell**: Diese Konfiguration enthält die EB-Komponente [Datenmodell](general-electronic-reporting.md#data-model-and-model-mapping-components), die die Datenstruktur der Zahlungsgeschäftsdomäne darstellt.
    - **Zahlungsmodellzuordnung 1611**: Diese Konfiguration enthält die EB-Komponente [Modellzuordnung](general-electronic-reporting.md#data-model-and-model-mapping-components), die beschreibt, wie das Datenmodell zur Laufzeit mit Anwendungsdaten gefüllt wird.
    - **BACS (UK)**: Diese Konfiguration enthält die EB-Komponenten [Format](general-electronic-reporting.md#FormatComponentOutbound) und Formatzuordnung. Die Formatkomponente legt das Berichtslayout fest. Die Formatzuordnungskomponente enthält die Modelldatenquelle und legt fest, wie das Berichtslayout mithilfe dieser Datenquelle zur Laufzeit ausgefüllt wird.

![Seite „Konfigurationen“.](./media/er-quick-start2-imported-solution1.png)

## <a name="prepare-a-vendor-payment-for-processing"></a><a id="PrepareVendorPayment"></a>Vorbereiten einer Kreditorenzahlung zur Verarbeitung

### <a name="add-bank-information-for-a-vendor-account"></a><a id="AddBankAccount"></a>Hinzufügen von Bankdaten für ein Kreditorenkonto

Sie müssen Bankdaten für ein Kreditorenkonto hinzufügen, auf die später in einer registrierten Zahlung verwiesen wird.

1. Wechseln Sie zu **Kreditorenkonten** \> **Kreditoren** \> **Alle Kreditoren**.
2. Wählen Sie auf der Seite **Alle Kreditoren** das Kreditorenkonto **GB_SI_000001** aus. Wählen Sie dann im Aktivitätsbereich auf der Registerkarte **Kreditor** in der Gruppe **Einrichtung** die Option **Bankkonten** aus.
3. Wählen Sie auf der Seite **Kreditoren-Bankkonten** die Option **Neu** aus und geben Sie dann die folgenden Informationen ein:

    1. In das Feld **Bankkonto** geben Sie **GBP OPER** ein.
    2. Wählen Sie im Feld **Bankgruppen** die Option **BankGBP** aus.
    3. Im Feld **Bankkontonummer** geben Sie **202015** ein.
    4. Im Feld **SWIFT-Code** geben Sie <a id="DefineSWIFTCode"></a>**CHASDEFXXXX** ein.
    5. Im Feld **IBAN** geben Sie **GB33BUKB20201555555555** ein.
    6. Im Feld **Bankleitzahl** können Sie den Standardwert <a id="DefineRoutingNumber"></a>**123456** beibehalten.

    ![Seite „Kreditoren-Bankkonten“.](./media/er-quick-start2-bank-account.png)

4. Wählen Sie **Speichern** aus.
5. Schließen Sie die Seite.
6. Öffnen Sie auf der Seite **Alle Kreditoren** das Kreditorenkonto **GB_SI_000001**.
7. Wählen Sie auf der Seite mit den Kreditorendetails **Bearbeiten** aus, um die Seite bei Bedarf bearbeiten zu können.
8. Wählen Sie auf dem Inforegister **Zahlung** im Feld **Bankkonto** die Option **GBP OPER** aus.

    ![Seite „Kreditorendetails“.](./media/er-quick-start2-bank-account-reference.png)

9. Wählen Sie **Speichern** aus.
10. Schließen Sie die Seite.

### <a name="enter-a-vendor-payment"></a><a id="EnterVendorPayment"></a>Eingeben einer Kreditorenzahlung

Sie müssen eine neue Kreditorenzahlung eingeben, indem Sie einen [Zahlungsvorschlag](../../../finance/accounts-payable/create-vendor-payments-payment-proposal.md) verwenden.

1. Wechseln Sie zu **Kreditorenkonten** \> **Zahlungen** \> **Kreditorenzahlungserfassung**.
2. Wählen Sie auf der Seite **Kreditorenzahlungserfassung** die Option **Neu** aus.
3. Wählen Sie im Feld **Name** die Option **VendPay** aus.
4. Wählen Sie **Positionen** aus.
5. Wählen Sie **Zahlungsvorschlag** \> **Zahlungsvorschlag erstellen** aus.
6. Konfigurieren Sie im Dialogfeld **Kreditorenzahlungsvorschlag** Bedingungen, um ausschließlich nach Datensätzen für das Kreditorenkonto **GB_SI_000001** zu filtern, und wählen Sie dann **OK** aus.
7. Wählen Sie die Zeile für die Rechnung **00000007_Inv** aus und wählen Sie dann **Zahlung erstellen** aus.

    ![Dialogfeld „Kreditorenzahlungsvorschlag“.](./media/er-quick-start2-payment-proposal.png)

8. Überprüfen Sie, ob die eingegebene Zahlung für die Verwendung der Zahlungsmethode **Elektronisch** konfiguriert ist.

    ![Seite für Kreditorenzahlungen.](./media/er-quick-start2-payment-line.png)

## <a name="process-a-vendor-payment-by-using-the-standard-er-format"></a><a id="ProcessVendorPayment1"></a>Verarbeiten einer Kreditorenzahlung durch Verwendung des standardmäpigen EB-Formats

### <a name="set-up-the-electronic-payment-method"></a><a id="ConfigureMethodOfPayment1"></a>Einrichten der elektronischen Zahlungsmethode

Sie müssen die elektronische Zahlungsmethode so konfigurieren, dass sie die importierte EB-Formatkonfiguration verwendet.

1. Wechseln Sie zu **Kreditorenkonten** \> **Zahlungseinstellungen** \> **Zahlungsmethoden**.
2. Wählen Sie auf der Seite **Zahlungsmethoden – Kreditoren** im linken Bereich die Zahlungsmethode **Elektronisch** aus.
3. Wählen Sie **Bearbeiten** aus.
4. Legen Sie auf dem Inforegister **Dateiformate** die Option **Allgemeines elektronisches Exportformat** auf **Ja** fest.
5. Wählen Sie im Feld **Formatkonfiguration exportieren** die Formatkonfiguration **BACS (UK)** aus.

    ![Seite „Zahlungsmethoden – Kreditoren“.](./media/er-quick-start2-method-of-payment1.png)

6. Wählen Sie **Speichern** aus.

### <a name="process-a-vendor-payment"></a><a id="ProcessPayment1"></a>Verarbeiten einer Kreditorenzahlung

1. Wechseln Sie zu **Kreditorenkonten** \> **Zahlungen** \> **Kreditorenzahlungserfassung**.
2. Wählen Sie auf der Seite **Kreditorenzahlungserfassung** die Zahlungserfassung aus, die Sie zuvor hinzugefügt haben, und wählen Sie dann **Positionen** aus.
3. Wählen Sie auf der Seiite **Kreditorenzahlungen** die Option **Zahlungen generieren** aus.
4. Geben Sie im Dialogfeld **Zahlungen generieren** die folgenden Informationen ein:

    - Wählen Sie im Feld **Zahlungsmethode** die Option **Elektronisch** aus.
    - Wählen Sie im Feld **Bankkonto** die Option **GBSI OPER** aus.

5. Wählen Sie **OK**.
6. Legen Sie im Dialogfeld **Elektronische Berichtsparameter** die Option **Kontrollbericht drucken** auf **Ja** fest und wählen Sie dann **OK** aus.

    ![Dialogfeld „Elektronische Berichtsparameter“.](./media/er-quick-start2-payment-dialog1.png)

    > [!NOTE]
    > Zusätzlich zur Zahlungsdatei können Sie jetzt den Kontrollbericht generieren.

7. Laden Sie die ZIP-Datei herunter und entpacken Sie daraus die folgenden Dateien:

    - Den Kontrollbericht im Excel-Format
    - Die Zahlungsdatei im TXT-Format

        Beachten Sie, dass in Übereinstimmung mit der [Struktur](#PositionRoutingNumber) des angegebenen EB-Formats die Zahlungsposition in der generierten Datei mit der Bankleitzahl beginnt, die für das konfigurierte Bankkonto [definiert](#DefineRoutingNumber) wurde.

        ![Zahlungsdatei im TXT-Format.](./media/er-quick-start2-payment-file1.png)

## <a name="customize-the-standard-er-format"></a><a id="CustomizeProvidedFormat"></a>Anpassen des standardmäßigen EB-Formats

Für das Beispiel in diesem Abschnitt verwenden Sie die von Microsoft bereitgestellten EB-Konfigurationen, um Kreditorenzahlungsdateien im BACS-Format zu generieren. Sie müssen jedoch eine Anpassung vornehmen, um die Anforderungen einer bestimmten Bank zu unterstützen. Sie möchten außerdem Ihr benutzerdefiniertes Format aktualisieren können, wenn neue Versionen von EB-Konfigurationen verfügbar sind. Dieses Upgrade sollte jedoch möglichst wenig kosten.

In diesem Fall müssen Sie als Vertreter von Litware, Inc. eine neue EB-Formatkonfiguration erstellen (ableiten), indem Sie die von Microsoft bereitgestellte Konfiguration **BACS (UK)** als Basis verwenden.

### <a name="create-a-custom-format"></a><a id="DeriveProvidedFormat"></a>Erstellen eines benutzerdefinierten Formats

1. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.
2. Erweitern Sie auf der Seite **Konfigurationen** in der Konfigurationsstruktur im linken Bereich den Punkt **Zahlungsmodell** und wählen Sie dann **BACS (UK)** aus. Litware, Inc. verwendet Version 1.1 dieser EB-Formatkonfiguration als Basis für die benutzerdefinierte Version.
3. Wählen Sie **Konfiguration erstellen** aus, um das Dropdown-Dialogfeld zu öffnen. Sie können dieses Dialogfeld verwenden, um eine neue Konfiguration für ein benutzerdefiniertes Zahlungsformat zu erstellen.
4. Wählen Sie in der Feldgruppe **Neu** die Option **Von Name ableiten: BACS (UK), Microsoft** aus.
5. In das Feld **Name** geben Sie **BACS (UK, benutzerdefiniert)** ein.

    ![Konfigurations-Dropdown-Dialogfeld erstellen.](./media/er-quick-start2-add-derived-format.png)

6. Wählen Sie **Konfiguration erstellen**.

Version 1.1.1 der EB-Formatkonfiguration **BACS (UK, benutzerdefiniert)** wird erstellt. Diese Version hat den [Status](general-electronic-reporting.md#component-versioning) **Entwurf** und kann bearbeitet werden. Der aktuelle Inhalt Ihres benutzerdefinierten EB-Formats entspricht dem Inhalt des von Microsoft bereitgestellten Formats.

![Seite „Konfigurationen“.](./media/er-quick-start2-derived-format-configuration1.png)

### <a name="edit-a-custom-format"></a><a id="ConfigureDerivedFormat"></a>Bearbeiten eines benutzerdefinierten Formats

Sie müssen Ihr benutzerdefiniertes Format so konfigurieren, dass es den bankspezifischen Anforderungen entspricht. Beispielsweise kann eine Bank verlangen, dass generierte Zahlungsdateien den SWIFT-Code (Society for Worldwide Interbank Financial Telecommunication) einer Bank enthalten, der in der verarbeiteten Kreditorenzahlung die Agentenrolle zugewiesen ist. SWIFT-Codes sind internationale Bankleitzahlen, die bestimmte Banken weltweit identifizieren. Sie werden auch als Bank Identifier Codes (BICs) bezeichnet. Der SWIFT-Code muss 11 Zeichen lang sein und am Anfang jeder Zahlungsposition in eine generierte Zahlungsdatei eingegeben werden.

1. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.
2. Erweitern Sie auf der Seite **Konfigurationen** in der Konfigurationsstruktur im linken Bereich den Punkt **Zahlungsmodell** und wählen Sie dann **BACS (UK, benutzerdefiniert)** aus.
3. Wählen Sie auf dem Inforegister **Versionen** die Version **1.1.1** der ausgewählten Konfiguration aus.
4. Wählen Sie **Designer** aus.
5. Wählen Sie auf der Seite **Formatdesigner** die Option **Details anzeigen** aus, um weitere Informationen zu den Formatelementen anzuzeigen.
6. Erweitern und überprüfen Sie die folgenden Elemente:

    - Das Element **BACSReportsFolder** vom Typ **Ordner**. Dieses Element wird verwendet, um eine Ausgabe im ZIP-Format zu generieren.
    - Das Element **file** vom Typ **Datei**. Dieses Element wird verwendet, um eine Zahlungsdatei im TXT-Format zu generieren.
    - Das Element **transactions** vom Typ **Sequenz**. Dieses Element wird verwendet, um eine einzelne Zahlungsposition in einer Zahlungsdatei zu generieren.
    - Das Element **transaction** vom Typ **Sequenz**. Dieses Element wird verwendet, um die einzelnen Felder einer Zahlungsposition zu generieren.

7. Wählen Sie das Element **transaction** aus.

    ![Transaktionselement im EB Operation Designer.](./media/er-quick-start2-derived-format0.png)

    > [!NOTE]
    > Der bereitgestellte Bericht ist so konfiguriert, dass <a id="PositionRoutingNumber"></a>jede Zahlungsposition mit der Bankleitzahl beginnt. Das Formatelement **vendBankRouteNum** wird zu diesem Zweck verwendet. 

8. Wählen Sie **Hinzufügen** und dann den Typ **Text\\Zeichenfolge** des Formatelements aus, das Sie hinzufügen:

    1. In das Feld **Name** geben Sie **vendBankSWIFT** ein.
    2. In das Feld **Mindestlänge** geben Sie **11** ein.
    3. In das Feld **Höchstlänge** geben Sie **11** ein.
    4. Wählen Sie **OK**.

    > [!NOTE]
    > Das Element **vendBankSWIFT** wird verwendet, um den SWIFT-Code einer Kreditorenbank in generierte Dateien einzugeben.

9. Wählen Sie in der Formatstruktur den Punkt **vendBankSWIFT** aus.
10. Wählen Sie **Nach oben verschieben** aus, um das ausgewählte Formatelement um eine Ebene nach oben zu verschieben. Wiederholen Sie diesen Schritt, bis das Element **vendBankSWIFT** das <a id="PositionSWIFTCode"></a>erste Element unter dem übergeordneten Element **transaction** ist.

    ![VendBankSWIFT als erstes Element unter „Transaktion“ im EB Operation Designer.](./media/er-quick-start2-derived-format1.png)

11. Während **vendBankSWIFT** in der Formatstruktur ausgewählt ist, wählen Sie die Registerkarte **Zuordnung** aus und erweitern Sie dann die **Modelldatenquelle**.
12. Erweitern Sie **model.Payment** \> **model.Payment.CreditorAgent** und wählen Sie das Datenquellenfeld **model.Payment.CreditorAgent.BICFI** aus. Dieses Datenquellenfeld stellt den SWIFT-Code einer Kreditorenbank bereit, der die Agentenrolle in der verarbeiteten Kreditorenzahlung zugewiesen ist.
13. Wählen Sie **Bindung** aus. Das Formatelement **vendBankSWIFT** ist jetzt an das Datenquellenfeld **model.Payment.CreditorAgent.BICFI** gebunden, sodass SWIFT-Codes in generierte Zahlungsdateien eingegeben werden.

    ![Formatelement „vendBankSWIFT“ ist an das Datenquellenfeld „model.Payment.CreditorAgent.BICFI“ im EB Operations Designer gebunden.](./media/er-quick-start2-derived-format2.png)

14. Wählen Sie **Speichern** aus.
15. Schließen Sie die Designerseite.

### <a name="mark-a-custom-format-as-runnable"></a><a id="MarkFormatRunnable"></a>Markieren eines benutzerdefinierten Formats als ausführbar

Nachdem die erste Version Ihres benutzerdefinierten Formats mit dem Status **Entwurf** erstellt wurde, können Sie es zu Testzwecken ausführen. Um den Bericht auszuführen, müssen Sie eine Kreditorenzahlung mithilfe der Zahlungsmethode verarbeiten, die sich auf Ihr benutzerdefiniertes EB-Format bezieht. Beim Aufrufen eines EB-Formats aus der Anwendung werden standardmäßig nur Versionen mit dem Status **Abgeschlossen** oder **Freigegeben** [berücksichtigt](general-electronic-reporting.md#component-versioning). Dieses Verhalten verhindert, dass EB-Formate mit unfertigen Designs verwendet werden. Für Ihre Testläufe können Sie die Anwendung jedoch zwingen, die Version Ihres EB-Formats mit dem Status **Entwurf** zu verwenden. Auf diese Weise können Sie die aktuelle Formatversion anpassen, falls Änderungen erforderlich sind. Weitere Informationen finden Sie unter [Anwendbarkeit](electronic-reporting-destinations.md#applicability).

Um die Entwurfsversion eines EB-Formats zu verwenden, müssen Sie das EB-Format explizit markieren.

1. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.
2. Auf der Seite **Konfigurationen** im Aktivitätsbereich, auf der Registerkarte **Konfigurationen** in der Gruppe **Erweiterte Einstellungen** wählen Sie **Benutzerparameter** aus.
3. Legen Sie im Dialogfeld **Benutzerparameter** die Option **Testlaufeinstellungen** auf **Ja** fest und wählen Sie dann **OK** aus.
4. Wählen Sie **Bearbeiten** aus, um die aktuelle Seite bei Bedarf bearbeiten zu können.
5. Wählen Sie in der Konfigurationsstruktur im linken Bereich den Punkt **BACS (UK, benutzerdefiniert)** aus.
6. Legen Sie die Option **Entwurf ausführen** auf **Ja** fest.

    ![Option „Entwurf ausführen“ auf der Konfigurationsseite.](./media/er-quick-start2-derived-format-configuration2.png)

## <a name="process-a-vendor-payment-by-using-the-custom-er-format"></a><a id="ProcessVendorPayment2"></a>Verarbeiten einer Kreditorenzahlung durch Verwendung des benutzerdefinierten EB-Formats

### <a name="set-up-the-electronic-payment-method"></a><a id="ConfigureMethodOfPayment2"></a>Einrichten der elektronischen Zahlungsmethode

Sie müssen die elektronische Zahlungsmethode so konfigurieren, dass Ihr benutzerdefiniertes EB-Format zur Verarbeitung von Kreditorenzahlungen verwendet wird.

1. Wechseln Sie zu **Kreditorenkonten** \> **Zahlungseinstellungen** \> **Zahlungsmethoden**.
2. Wählen Sie auf der Seite **Zahlungsmethoden – Kreditoren** im linken Bereich die Zahlungsmethode **Elektronisch** aus.
3. Wählen Sie **Bearbeiten** aus.
4. Legen Sie auf dem Inforegister **Dateiformate** die Option **Allgemeines elektronisches Exportformat** auf **Ja** fest.
5. Wählen Sie im Feld **Formatkonfiguration exportieren** die Formatkonfiguration **BACS (UK, benutzerdefiniert)** aus.

    ![Seite „Zahlungsmethoden – Kreditoren“.](./media/er-quick-start2-method-of-payment2.png)

6. Wählen Sie **Speichern** aus.

### <a name="process-a-vendor-payment"></a><a id="ProcessPayment2"></a>Verarbeiten einer Kreditorenzahlung

1. Wechseln Sie zu **Kreditorenkonten** \> **Zahlungen** \> **Kreditorenzahlungserfassung**.
2. Wählen Sie auf der Seite **Kreditorenzahlungserfassung** die Zahlungserfassung aus, die Sie zuvor erstellt haben.
3. Wählen Sie **Positionen** aus.
4. Wählen Sie auf der Seite **Kreditorenzahlungen** über dem Raster **Zahlungsstatus** \> **Kein** aus.
5. Wählen Sie **Zahlung generieren** aus.
6. Geben Sie im Dialogfeld **Zahlungen generieren** die folgenden Informationen ein:

    - Wählen Sie im Feld **Zahlungsmethode** die Option **Elektronisch** aus.
    - Wählen Sie im Feld **Bankkonto** die Option **GBSI OPER** aus.

7. Wählen Sie **OK**.
8. Legen Sie im Dialogfeld **Elektronische Berichtsparameter** die Option **Kontrollbericht drucken** auf **Ja** fest und wählen Sie dann **OK** aus.

    > [!NOTE]
    > Zusätzlich zur Zahlungsdatei können Sie nur den Kontrollbericht generieren.

9. Laden Sie die ZIP-Datei herunter und entpacken Sie daraus die folgenden Dateien:

    - Den Kontrollbericht im Excel-Format
    - Die Zahlungsdatei im TXT-Format

        Beachten Sie, dass gemäß der Struktur Ihres benutzerdefinierten EB-Formats die Zahlungsposition in der generierten Datei jetzt mit dem SWIFT-Code [beginnt](#PositionSWIFTCode), der für das Bankkonto des Kreditors [eingegeben](#DefineSWIFTCode) wurde, dessen Zahlung verarbeitet wurde.

        ![Zahlungsdatei im TXT-Format.](./media/er-quick-start2-payment-file2.png)

## <a name="import-new-versions-of-the-standard-er-format-configurations"></a><a id="ImportERSolution2"></a>Importieren neuer Versionen der standardmäßigen EB-Formatkonfigurationen

Für das Beispiel in diesem Abschnitt erhalten Sie eine Benachrichtigung über den Knowledge Base-Artikel [KB3763330](https://fix.lcs.dynamics.com/Issue/Details?kb=3182046). Diese Benachrichtigung informiert Sie über die neue Version des EB-Formats **BACS (UK)**, das von Microsoft veröffentlicht wurde. Zusätzlich zum Kontrollbericht können Benutzer mit dieser neuen Version noch den Zahlungsavisbericht und den Begleitzettel-Bericht erstellen, während eine Kreditorenzahlung verarbeitet wird. Sie möchten diese Funktion jetzt nutzen.

### <a name="import-new-versions-of-the-standard-er-configurations"></a><a id="ImportERFormat2"></a>Importieren neuer Versionen der standardmäßigen EB-Konfigurationen

Um neue Versionen der EB-Konfigurationen zur aktuellen Finance-Instanz hinzuzufügen, müssen Sie sie aus dem EB-[Repository](general-electronic-reporting.md#Repository) importieren, das Sie konfiguriert haben.

1. Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.
2. Wählen Sie auf der Seite **Lokalisierungskonfigurationen** im Bereich **Konfigurationsanbieter** die Kachel **Microsoft** aus. Wählen Sie dann **Repositorys** aus, um die Liste der Repositorys für den Microsoft-Anbieter anzuzeigen.
3. Wählen Sie auf der Seite **Konfigurationsrepositorys** das Repository des Typs **Global** aus. Wählen Sie dann **Öffnen** aus. Wenn Sie aufgefordert werden, das Herstellen einer Verbindung zum Regulatory Configuration Service zu autorisieren, folgen Sie den Autorisierungsanweisungen.
4. Wählen Sie auf der Seite **Konfigurationsrepositorys** in der Konfigurationsstruktur im linken Bereich die Formatkonfiguration **BACS (UK)** aus.
5. Wählen Sie auf dem Inforegister **Versionen** die Version **3.3** der ausgewählten EB-Formatkonfiguration aus.
6. Wählen Sie **Importieren** aus, um die ausgewählte Version aus dem globalen Repository auf die aktuelle Finance-Instanz herunterzuladen.

![Konfigurationsrepository-Seite.](./media/er-quick-start2-import-solution2.png)

> [!TIP]
> Wenn Sie Probleme beim Zugriff auf das [globale Repository](er-download-configurations-global-repo.md) haben, können Sie für das [Herunterladen von Konfigurationen](download-electronic-reporting-configuration-lcs.md) stattdessen LCS verwenden.

### <a name="review-the-imported-er-format-configurations"></a><a id="ReviewImportedERFormat"></a>Überprüfen der importierten EB-Formatkonfigurationen

1. Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.
2. Auf der Seite **Lokalisierungskonfigurationen** im Abschnitt **Konfigurationen** wählen Sie die Kachel **Berichterstellungskonfigurationen** aus.
3. Erweitern Sie auf der Seite **Konfigurationen** in der Konfigurationsstruktur im linken Bereich den Punkt **Zahlungsmodell** und wählen Sie dann **BACS (UK)** aus.
4. Wählen Sie im Inforegister **Versionen** die Version **3.3** aus.
5. Wählen Sie **Designer** aus.
6. Erweitern Sie auf der Seite **Formatdesigner** das Formatelement **BACSReportsFolder**.
7.  Beachten Sie, dass Version 3.3 das Formatelement **PaymentAdviceReport** enthält, das zum Generieren eines Zahlungsavisberichts verwendet wird, wenn eine Kreditorenzahlung verarbeitet wird.

    ![Formatelement „PaymentAdviceReport“ im EB Operations Designer.](./media/er-quick-start2-imported-solution2.png)

8. Schließen Sie die Designerseite.

## <a name="adopt-the-changes-in-the-new-version-of-an-imported-format-in-a-custom-format"></a><a id="AdoptNewBaseVersion"></a>Übernehmen der Änderungen in der neuen Version eines importierten Formats in ein benutzerdefiniertes Format

### <a name="complete-the-current-draft-version-of-a-custom-format"></a><a id="CompleteDerivedFormat"></a>Vervollständigen der aktuellen Entwurfsversion eines benutzerdefinierten Formats

Wenn Sie den aktuellen Status Ihres benutzerdefinierten Formats beibehalten möchten, vervollständigen Sie den Entwurf von Version 1.1.1, indem Sie ihren Status von **Entwurf** zu **Abgeschlossen** ändern.

1. Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.
2. Auf der Seite **Lokalisierungskonfigurationen** im Abschnitt **Konfigurationen** wählen Sie die Kachel **Berichterstellungskonfigurationen** aus.
3. Erweitern Sie auf der Seite **Konfigurationen** in der Konfigurationsstruktur im linken Bereich zunächst den Punkt **Zahlungsmodell** und dann den Punkt **BACS (UK, benutzerdefiniert)**. Wählen Sie dann **BACS (UK, benutzerdefiniert)** aus.
4. Wechseln Sie auf dem Inforegister **Versionen** zu **Status ändern** \> **Abgeschlossen** und wählen Sie dann **OK** aus.

Der Status von Version 1.1.1 wird von **Entwurf** zu **Abgeschlossen** geändert und die Version ist jetzt schreibgeschützt. Eine neue bearbeitbare Version 1.1.2 mit dem Status **Entwurf** wurde hinzugefügt. Mit dieser Version können Sie weitere Änderungen an Ihrem benutzerdefinierten EB-Format vornehmen.

### <a name="rebase-a-custom-format-to-a-new-base-version"></a><a id="RebaseDerivedFormat"></a>Zurücksetzen eines benutzerdefinierten Formats auf eine neue Basisversion

Um die neuen Funktionen von Version 3.3 des Formats **BACS (UK)** in Ihrer Anpassung nutzen zu können, müssen Sie die Basiskonfigurationsversion für die benutzerdefinierte Konfiguration ändern, **BACS (UK, benutzerdefiniert)**. Dieser Prozess wird als [Rebasierung](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase) bezeichnet. Verwenden Sie anstelle von Version 1.1 von **BACS (UK)** Version 3.3.

1. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.
2. Erweitern Sie auf der Seite **Konfigurationen** in der Konfigurationsstruktur im linken Bereich den Punkt **Zahlungsmodell** und wählen Sie dann **BACS (UK, benutzerdefiniert)** aus.
3. Wählen Sie auf dem Inforegister **Versionen** Version **1.1.2** und dann **Zurücksetzen** aus.
4. Wählen Sie im Dialogfeld **Zurücksetzen** im Feld **Zielversion** Version **3.3** der Basiskonfiguration aus, um sie als neue Basis anzuwenden und zum Aktualisieren der Konfiguration zu verwenden.

    ![Dialogfeld zurücksetzen.](./media/er-quick-start2-rebase1.png)

5. Wählen Sie **OK** aus.
6. Beachten Sie, dass die Nummer der Entwurfsversion von **1.1.2** zu **3.3.2** geändert wurde, um die Änderung in der Basisversion widerzuspiegeln.

    Wenn die benutzerdefinierte Version und eine neue Basisversion zusammengeführt werden, können aufgrund von Formatänderungen, die nicht automatisch zusammengeführt werden können, einige Konflikte auftreten.

    ![Zurückgesetzte Konfiguration mit Konflikten auf der Konfigurationsseite.](./media/er-quick-start2-rebase2.png)

    Wenn Konflikte auftreten, müssen sie im Formatdesigner manuell gelöst werden.

7. Wählen Sie im Inforegister **Versionen** die Version **3.3.2** aus.
8. Wählen Sie **Designer** aus.
9. Wählen Sie auf der Seite **Formatdesigner** auf dem Inforegister **Details** einen durch das Zurücksetzen verursachten Konfliktdatensatz aus und wählen Sie dann **Basiswert anwenden** aus.

    ![Durch Zurücksetzen verursachter Konfliktdatensatz im EB Operation Designer.](./media/er-quick-start2-rebase3.png)

10. Wählen Sie **Speichern** aus.

    Der durch das Zurücksetzen verursachte Konfliktdatensatz sollte auf dem Inforegister **Details** nicht mehr angezeigt werden.

    ![Konflikt gelöst im EB Operation Designer.](./media/er-quick-start2-rebase4.png)

    > [!NOTE]
    > Sie haben den Konflikt gelöst, indem Sie bestätigt haben, dass in diesem EB-Format Version 3 des Basismodells verwendet werden muss.

11. Erweitern Sie **BACSReportsFolder** \> **file** \> **transactions** \> **transaction**.
12. Beachten Sie auf der Registerkarte **Zuordnung**, dass Version 3.3.2 Ihres benutzerdefinierten EB-Formats sowohl Ihre Anpassung (das Formatelement **vendBankSWIFT** und seine Bindung) als auch die neuen Funktionen von Version 3.3 des von Microsoft bereitgestellten Basis-EB-Formats (das Formatelement **PaymentAdviceReport** zusammen mit seinen verschachtelten Elementen und konfigurierten Bindungen) enthält. Mit nur wenigen Mausklicks haben Sie die Änderungen einer neuen Basisversion übernommen, indem Sie sie mit Ihrer Anpassung zusammengeführt haben.

    ![Zusammengeführtes Format im EB Operation Designer.](./media/er-quick-start2-rebase5.png)

13. Schließen Sie die Designerseite.

> [!NOTE]
> Das Zurücksetzen kann nicht rückgängig gemacht werden. Um das Zurücksetzen abzubrechen, wählen Sie Version **1.1.1** des Formats **BACS (UK, benutzerdefiniert)** auf dem Inforegister **Versionen** aus und wählen Sie dann **Diese Version abrufen** aus. Version 3.3.2 wird dann in 1.1.2 umnummeriert und der Inhalt der Entwurfsversion 1.1.2 stimmt mit dem Inhalt von Version 1.1.1 überein.

### <a name="process-a-vendor-payment-by-using-a-rebased-er-format"></a><a id="ProcessPayment3"></a>Verarbeiten einer Kreditorenzahlung durch Verwendung eines zurückgesetzten EB-Formats

1. Wechseln Sie zu **Kreditorenkonten** \> **Zahlungen** \> **Kreditorenzahlungserfassung**.
2. Wählen Sie auf der Seite **Kreditorenzahlungserfassung** die Zahlungserfassung aus, die Sie zuvor erstellt haben.
3. Wählen Sie **Positionen** aus.
4. Wählen Sie auf der Seite **Kreditorenzahlungen** über dem Raster **Zahlungsstatus** \> **Kein** aus.
5. Wählen Sie **Zahlung generieren** aus.
6. Geben Sie im Dialogfeld **Zahlungen generieren** die folgenden Informationen ein:

    - Wählen Sie im Feld **Zahlungsmethode** die Option **Elektronisch** aus.
    - Wählen Sie im Feld **Bankkonto** die Option **GBSI OPER** aus.

7. Wählen Sie **OK**.
8. Geben Sie im Dialogfeld **Elektronische Berichtsparameter** die folgenden Informationen ein:

    - legen Sie die **Kontrollbereicht drucken** auf **Ja** fest.
    - Legen Sie die Option **Zahlungsavis drucken** auf **Ja** fest.

    ![Dialogfeld für elektronische Berichtsparameter.](./media/er-quick-start2-payment-dialog2.png)

    > [!NOTE]
    > Zusätzlich zur Zahlungsdatei können Sie jetzt sowohl den Kontrollbericht als auch den Zahlungsavisbericht erstellen.

9. Wählen Sie **OK**.
10. Laden Sie die ZIP-Datei herunter und entpacken Sie daraus die folgenden Dateien:

    - Den Kontrollbericht im Excel-Format
    - Den Zahlungsavisbericht im Excel-Format

        ![Zahlungsavisbericht im Excel-Format.](./media/er-quick-start2-payment-advice-report.png)

    - Die Zahlungsdatei im TXT-Format

        Beachten Sie, dass die Zahlungsposition in der generierten Datei mit dem SWIFT-Code beginnt, der für das Bankkonto eines Kreditors eingegeben wurde, dessen Zahlung verarbeitet wurde.

        ![Zahlungsdatei im TXT-Format.](./media/er-quick-start2-payment-file3.png)

## <a name="additional-resources"></a><a id="References"></a>Zusätzliche Ressourcen

- [Überblick über die elektronische Berichterstellung](general-electronic-reporting.md)
- [Herunterladen elektronischer Berichterstellungskonfigurationen von Lifecycle Services](download-electronic-reporting-configuration-lcs.md)
- [Herunterladen von EB-Konfigurationen aus dem globalen Repository des Konfigurationsdienstes](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]