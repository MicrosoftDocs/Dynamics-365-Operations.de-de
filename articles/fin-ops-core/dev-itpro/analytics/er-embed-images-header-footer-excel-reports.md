---
title: Ein EB-Format entwerfen, um einen Bericht im Excel-Format mit eingebetteten Bildern in den Kopf- oder Fußzeilen einer Seite zu erstellen
description: In diesem Thema wird erklärt, wie Sie mit Electronic Reporting (ER) geschäftliche Belege erzeugen können, die Bilder und Formen in Seitenkopf- oder Fußzeilen eingebettet haben.
author: NickSelin
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-06-01
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 20bcf26e1510634c5ee7043576a480ce15889923
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2021
ms.locfileid: "7344119"
---
# <a name="design-an-er-format-to-generate-a-report-in-excel-format-with-embedded-images-in-page-headers-or-footers"></a>Ein EB-Format entwerfen, um einen Bericht im Excel-Format mit eingebetteten Bildern in den Kopf- oder Fußzeilen einer Seite zu erstellen

[!include[banner](../includes/banner.md)]

Dieses Thema erläutert, wie ein Benutzer mit der Rolle des Systemadministrators oder des Functional Consultant für die elektronische Berichterstellung die folgenden Aufgaben ausführen kann:

- Die Parameter für das Framework für die [elektronische Berichterstellung (EB)](general-electronic-reporting.md) konfigurieren.
- EB-[Konfigurationen](general-electronic-reporting.md#Configuration) importieren, die von Microsoft [bereitgestellt](general-electronic-reporting.md#Provider) und zum Generieren von [Freitextrechnungen](../../../finance/accounts-receivable/create-free-text-invoice-new.md)auf Basis einer [Vorlage](er-fillable-excel.md#excel-file-component) im Microsoft Excel-Format verwendet werden.
- Eine [benutzerdefinierte (abgeleitete)](general-electronic-reporting.md#building-a-format-selecting-another-format-as-a-base-customization) Version einer standardmäßigen EB-Formatkonfiguration erstellen, die von Microsoft bereitgestellt wird.
- Die Konfiguration des benutzerdefinierten EB-Formats ändern, sodass ein Freitextrechnungsbericht mit einem Firmenlogo in der Fußzeile generiert wird.

Die Prozeduren in diesem Thema können im **USMF**-Unternehmen erledigt werden. Eine Codierung ist nicht erforderlich. Bevor Sie beginnen, laden Sie die folgende Datei herunter und speichern Sie sie.

| Beschreibung        | Dateiname |
|--------------------|-----------|
| Firmenlogo-Bild | [Firmenlogo.png](https://download.microsoft.com/download/8/2/e/82e6bd81-caac-4e9a-bfce-1392ce7c8616/Companylogo.png) |

## <a name="content"></a>Inhalt

- [Die juristische Person konfigurieren](#ConfigureLegalEntity)
- [Konfigurieren des EB-Frameworks](#ConfigureFramework)

    - [Parameter der elektronischen Berichterstellung konfigurieren](#ConfigureParameters)
    - [Aktivieren eines EB-Konfigurationsanbieters](#ActivateProvider)

        - [Überprüfen der Liste der EB-Konfigurationsanbieter](#ReviewProvidersList)
        - [Hinzufügen eines neuen EB-Konfigurationsanbieters](#AddProvider)
        - [Den neuen EB-Konfigurationsanbieter aktivieren](#ActivateAddedProvider)

- [Importieren der standardmäßigen EB-Formatkonfigurationen](#ImportERSolution1)

    - [Importieren der standardmäßigen EB-Konfigurationen](#ImportERFormat)
    - [Überprüfen der importierten EB-Konfigurationen](#ReviewImportedERSolution)

- [Eine Freitextrechnung im Standard-EB-Format konfigurieren](#PrintInvoice1)

    - [Druckverwaltung einrichten](#ConfigurePrintManagement1)
    - [Dient zum Drucken einer Freitextrechnung.](#ProcessInvoice1)

- [Anpassen des standardmäßigen EB-Formats](#CustomizeProvidedFormat)

    - [Erstellen eines benutzerdefinierten Formats](#DeriveProvidedFormat)
    - [Das benutzerdefinierte Format bearbeiten](#ConfigureDerivedFormat)
    - [Das benutzerdefinierte Format als ausführbar kennzeichnen](#MarkFormatRunnable)

- [Eine Freitextrechnung im benutzerdefinierten EB-Format konfigurieren](#PrintInvoice2)

    - [Druckverwaltung einrichten](#ConfigurePrintManagement2)
    - [Dient zum Drucken einer Freitextrechnung.](#ProcessInvoice2)

- [Zusätzliche Ressourcen](#References)

## <a name="configure-the-legal-entity"></a><a id="ConfigureLegalEntity"></a>Die juristische Person konfigurieren

1. Gehen Sie zu **Organisationsverwaltung** \> **Organisationen** \> **Juristische Personen**.
2. Gehen Sie auf der Seite **Juristische Personen** auf das Inforegister **Firmenlogobild für Bericht** und wählen Sie **Ändern** aus.
3. Wählen Sie im Dialogfeld **Bilddatei zum Hochladen auswählen** **Durchsuchen** und dann die **Firmenlogo.png**-Datei aus, die Sie zuvor heruntergeladen haben.
4. Wählen Sie **Speichern** aus und schließen Sie dann die Seite **Juristische Personen**.

![Auf der Seite „Juristische Personen“ ausgewähltes Firmenlogo.](./media/er-embed-images-header-footer-excel-reports-company-logo-image.png)

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
> Eine EB-Konfiguration kann nur vom Besitzer der Konfiguration bearbeitet werden. Bevor eine EB-Konfigurationen bearbeitet werden kann, muss im Arbeitsbereich **Elektronische Berichterstellung** der entsprechende EB-Konfigurationsanbieter aktiviert werden.

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a>Überprüfen der Liste der EB-Konfigurationsanbieter

1. Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.
2. Wählen Sie auf der Seite **Lokalisierungskonfigurationen** im Bereich **Zugehörige Links** die Option **Konfigurationsanbieter** aus.
3. Auf der Seite **Konfigurationsanbietertabelle** hat jeder Anbieterdatensatz einen eindeutigen Namen und eine eindeutige URL. Überprüfen Sie den Inhalt dieser Seite. Wenn bereits ein Datensatz für **Litware, Inc.** (`https://www.litware.com`) vorhanden ist, überspringen Sie die nächste Prozedur [Hinzufügen eines neuen EB-Konfigurationsanbieters](#AddProvider).

#### <a name="add-a-new-er-configuration-provider"></a><a id="AddProvider"></a>Hinzufügen eines neuen EB-Konfigurationsanbieters

1. Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.
2. Wählen Sie auf der Seite **Lokalisierungskonfigurationen** im Bereich **Zugehörige Links** die Option **Konfigurationsanbieter** aus.
3. Wählen Sie auf der Seite **Konfigurationsanbieter** die Option **Neu** aus.
4. Geben Sie im Feld **Name** **Litware, Inc.** ein.
5. Geben Sie im Feld **Internetadresse** `https://www.litware.com` ein.
6. Wählen Sie **Speichern** aus.

#### <a name="activate-the-new-er-configuration-provider"></a><a id="ActivateAddedProvider"></a>Den neuen EB-Konfigurationsanbieter aktivieren

1. Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.
2. Wählen Sie auf der Seite **Lokalisierungskonfigurationen** im Bereich **Konfigurationsanbieter** die Kachel **Litware, Inc.** aus. Wählen Sie dann **Als aktiv festlegen** aus.

Weitere Informationen zu EB-Konfigurationsanbietern finden Sie unter [Erstellen von Konfigurationsanbietern und Markieren als aktiv](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="import-the-standard-er-format-configurations"></a><a id="ImportERSolution1"></a>Importieren der standardmäßigen EB-Formatkonfigurationen

### <a name="import-the-standard-er-configurations"></a><a id="ImportERFormat"></a>Importieren der standardmäßigen EB-Konfigurationen

Um Ihrer aktuellen Instanz von Dynamics 365 Finance die standardmäßigen EB-Konfigurationen hinzuzufügen, müssen Sie sie aus dem EB-[Repository](general-electronic-reporting.md#Repository) importieren, das für diese Instanz konfiguriert wurde.

1. Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.
2. Wählen Sie auf der Seite **Lokalisierungskonfigurationen** im Bereich **Konfigurationsanbieter** die Kachel **Microsoft** aus. Wählen Sie dann **Repositorys** aus, um die Liste der Repositorys für den **Microsoft**-Anbieter anzuzeigen.
3. Wählen Sie auf der Seite **Konfigurationsrepositorys** das Repository des Typs **Global** aus. Wählen Sie dann **Öffnen** aus. Wenn Sie aufgefordert werden, das Herstellen einer Verbindung zum [Regulatory Configuration Service](../../../finance/localizations/rcs-overview.md) zu autorisieren, folgen Sie den Autorisierungsanweisungen.
4. Wählen Sie auf der Seite **Konfigurationsrepositorys** in der Konfigurationsstruktur im linken Bereich die Formatkonfiguration **Freitextrechnung (Excel)** aus.
5. Wählen Sie auf dem Inforegister **Versionen** die neueste Version (zum Beispiel **240.112**) der ausgewählten EB-Formatkonfiguration aus.
6. Wählen Sie **Importieren** aus, um die ausgewählte Version aus dem globalen Repository auf die aktuelle Finance-Instanz herunterzuladen.

![Die Standard-EB-Konfigurationen auf der Seite „Konfigurationsrepository“ importieren.](./media/er-embed-images-header-footer-excel-reports-import-solution.png)

> [!TIP]
> Wenn Sie Probleme beim Zugriff auf das [globale Repository](er-download-configurations-global-repo.md) haben, können Sie für das [Herunterladen von Konfigurationen](download-electronic-reporting-configuration-lcs.md) stattdessen Microsoft Dynamics Lifecycle Services (LCS) verwenden.

### <a name="review-the-imported-er-configurations"></a><a id="ReviewImportedERSolution"></a>Überprüfen der importierten EB-Konfigurationen

1. Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.
2. Auf der Seite **Lokalisierungskonfigurationen** im Abschnitt **Konfigurationen** wählen Sie die Kachel **Berichterstellungskonfigurationen** aus.
3. Erweitern Sie auf der Seite **Konfigurationen** in der Konfigurationsstruktur im linken Bereich den Punkt **Rechnungsmodell**.
4. Neben dem ausgewählten EB-Format **Freitextrechnung (Excel)** wurden weitere erforderliche EB-Konfigurationen importiert. Stellen Sie sicher, dass die folgenden EB-Konfigurationen in der Konfigurationsstruktur verfügbar sind:

    - **Rechnungsmodell**: Diese Konfiguration enthält die EB-Komponente [Datenmodell](general-electronic-reporting.md#data-model-and-model-mapping-components), die die Datenstruktur der Rechnungsstellungsgeschäftsdomäne darstellt.
    - **Rechnungsmodellzuordnung**: Diese Konfiguration enthält die EB-Komponente [Modellzuordnung](general-electronic-reporting.md#data-model-and-model-mapping-components), die beschreibt, wie das Datenmodell zur Laufzeit mit Anwendungsdaten gefüllt wird.
    - **Freitextrechnung (Excel)**: Diese Konfiguration enthält das [Format](general-electronic-reporting.md#FormatComponentOutbound) und die Formatzuordnung von EB-Komponenten. Die Formatkomponente legt das Berichtslayout basierend auf einer Vorlage im Excel-Format fest. Die Formatzuordnungskomponente enthält die Modelldatenquelle und legt fest, wie die Datenquelle verwendet wird, um das Berichtslayout zur Laufzeit auszufüllen.

![Importierte EB-Konfigurationen auf der Seite „Konfigurationen“.](./media/er-embed-images-header-footer-excel-reports-imported-solution.png)

## <a name="print-a-free-text-invoice-by-using-the-standard-er-format"></a><a id="PrintInvoice1"></a>Eine Freitextrechnung im Standard-EB-Format konfigurieren

### <a name="set-up-print-management"></a><a id="ConfigurePrintManagement1"></a>Druckverwaltung einrichten

1. Wechseln Sie zu **Debitoren** \> **Rechnungen** \> **Alle Freitextrechnungen**.
2. Wählen Sie auf der Seite **Freitextrechnung** die Rechnung **FTI-00000002** und dann im Aktivitätsbereich auf der Registerkarte **Rechnung** in der Gruppe **Druckverwaltung** die Option **Druckverwaltung** aus.
3. Klappen Sie auf der Seite **Druckverwaltungseinstellungen** im Baum links **Modul – Debitorenkonten \> Dokumente \> Freitextrechnung** auf und wählen Sie dann das Element **Original \<Default\>** aus.
4. Wählen Sie im Feld **Berichtsformat** **Freitextrechnung (Excel)** aus.
5. Drücken Sie **Esc** zum Verlassen der Seite **Druckverwaltungseinstellungen** und kehren Sie zurück zur Seite **Freitextrechnung**.

![Druckverwaltungseinstellungen für eine Freitextrechnung im Standard-EB-Format auf der Seite „Druckverwaltung“ einrichten.](./media/er-embed-images-header-footer-excel-reports-print-management.png)

### <a name="print-a-free-text-invoice"></a><a id="ProcessInvoice1"></a>Dient zum Drucken einer Freitextrechnung.

1. Stellen Sie sicher, dass auf der Seite **Freitextrechnung** die Rechnung **FTI-00000002** immer noch ausgewählt ist, und wählen Sie dann im Aktivitätsbereich auf der Registerkarte **Rechnung** in der Gruppe **Dokument** **Drucken** \> **Ausgewählt** aus.
2. Laden Sie die generierte Rechnung im Excel-Format herunter und öffnen Sie sie in der Vorschau.
3. Beachten Sie, dass die Fußzeile der generierten Rechnung entsprechend dem Aufbau der Excel-Vorlage für das bereitgestellte EB-Format Informationen über die aktuelle Seitenzahl und die Gesamtseitenzahl des Berichts enthält.

![Generierte Freitextrechnung.](./media/er-embed-images-header-footer-excel-reports-print-invoice1.gif)

## <a name="customize-the-standard-er-format"></a><a id="CustomizeProvidedFormat"></a>Anpassen des standardmäßigen EB-Formats

Für das Beispiel in diesem Abschnitt können Sie die von Microsoft bereitgestellten EB-Konfigurationen verwenden, um eine Freitextrechnung im Excel-Format zu erstellen. Sie müssen jedoch eine Anpassung hinzufügen, um ein Firmenlogo in die Fußzeile generierter Rechnungen einzufügen.

In diesem Fall müssen Sie als Vertreter von Litware, Inc. eine neue EB-Formatkonfiguration erstellen (ableiten), die auf der von Microsoft bereitgestellten Konfiguration **Freitextrechnung (Excel)** basiert.

### <a name="create-a-custom-format"></a><a id="DeriveProvidedFormat"></a>Erstellen eines benutzerdefinierten Formats

1. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.
2. Erweitern Sie auf der Seite **Konfigurationen** in der Konfigurationsstruktur im linken Bereich den Punkt **Rechnungsmodell** und wählen Sie dann **Freitextrechnung (Excel)** aus. Litware, Inc. verwendet die importierte Version (z. B. **240.112**) dieser EB-Formatkonfiguration als Basis für die benutzerdefinierte Version.
3. Wählen Sie **Konfiguration erstellen** aus, um das Dropdown-Dialogfeld zu öffnen. Verwenden Sie dieses Dialogfeld, um eine neue Konfiguration für ein benutzerdefiniertes Zahlungsformat zu erstellen.
4. Wählen Sie in der Feldgruppe **Neu** die Option **Von Name ableiten: Freitextrechnung (Excel), Microsoft** aus.
5. Geben Sie im Feld **Name** **Freitextrechnung (Excel) benutzerdefiniert** aus.
6. Wählen Sie **Konfiguration erstellen**.

![Eine Konfiguration für ein benutzerdefiniertes Zahlungsformat im Dropdown-Dialogfeld „Konfiguration erstellen“.](./media/er-embed-images-header-footer-excel-reports-add-derived-format.png)

Die Version 240.112.1 der EB-Formatkonfiguration **Freitextrechnung (Excel) benutzerdefinierte** wird erstellt. Diese Version hat den [Status](general-electronic-reporting.md#component-versioning) **Entwurf** und kann bearbeitet werden. Der aktuelle Inhalt Ihres benutzerdefinierten EB-Formats entspricht dem Inhalt des von Microsoft bereitgestellten Formats.

![Neue Versionen der EB-Formatkonfiguration auf der Seite „Konfigurationen“.](./media/er-embed-images-header-footer-excel-reports-derived-format-configuration1.png)

### <a name="edit-the-custom-format"></a><a id="ConfigureDerivedFormat"></a>Das benutzerdefinierte Format bearbeiten

Konfigurieren Sie Ihr benutzerdefiniertes Format so, dass auf jeder Seite des Berichts ein Firmenlogo in die Fußzeile eingefügt wird.

1. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.
2. Erweitern Sie auf der Seite **Konfigurationen** in der Konfigurationsstruktur im linken Bereich den Punkt **Zahlungsmodell** und wählen Sie dann **Freitextrechnung (Excel) benutzerdefiniert** aus.
3. Wählen Sie auf dem Inforegister **Versionen** die Version **240.112.1** der ausgewählten Konfiguration aus.
4. Wählen Sie **Designer** aus.
5. Wählen Sie auf der Seite **Formatdesigner** die Option **Details anzeigen** aus, um weitere Informationen zu den Formatelementen anzuzeigen.
6. Erweitern und überprüfen Sie die folgenden Elemente:

    - Das Element **Freitextrechnung** vom Typ **Excel**. Dieses Element wird verwendet, um eine Rechnung im Excel-Arbeitsmappenformat zu generieren.
    - Das Element **Freitextrechnung \\ Rechnung** vom Typ **Blatt**. Dieses Element wird verwendet, um ein Arbeitsblatt der generierten Excel-Arbeitsmappe zu generieren.
    - Das Element **Freitextrechnung \\ Rechnung \\ Fußzeile** vom Typ **Fußzeile**. Dieses Element wird verwendet, um eine Rechnungsfußzeile zu befüllen.

7. Wählen Sie das Element **Freitextrechnung \\ Rechnung \\ Fußzeile** aus.

    ![Fußzeilenelement im EB-Vorgangsdesigner.](./media/er-embed-images-header-footer-excel-reports-derived-format0.png)

    > [!NOTE]
    > Jede Fußzeile einer generierten Rechnung enthält Informationen über die aktuelle Seitenzahl und die Gesamtseitenzahl des Berichts. Wie Sie sehen können, enthält das Element **Freitextrechnung \\ Rechnung \\ Fußzeile** keine untergeordneten Elemente. Daher ist die verwendete Excel-Vorlage so konfiguriert, dass Angaben zur Seitennummerierung in der Mitte der Fußzeile jedes Berichts angezeigt werden.

8. Wählen Sie **Hinzufügen** und dann den Typ **Excel \\ Bild** des Formatelements aus, das Sie hinzufügen:

    1. Wählen Sie im Feld **Ausrichtung** **Rechts** aus.
    2. Wählen Sie im Feld **Höhe skalieren** **Relativ** aus.
    3. Geben Sie im Feld **In Prozent skalieren** **70** ein.
    4. Wählen Sie **OK** aus.

        > [!NOTE]
        > Das Element **Excel \\ Bild** wird verwendet, um ein Firmenlogobild hinzuzufügen und es auf der rechten Seite der Fußzeile auszurichten.

    ![Eigenschaften des Bildelements im Dialogfeld „Komponenteneigenschaften“.](./media/er-embed-images-header-footer-excel-reports-derived-format1.png)

9. Wählen Sie in der Formatstruktur links das Element **Bild**, das Sie gerade hinzugefügt haben, und klappen Sie dann auf der Registerkarte **Zuordnung** die **Modell**-Datenquelle auf.
10. Erweitern Sie **model.Payment** \> **model.InvoiceBase \> model.InvoiceBase.CompanyInfo** und wählen Sie dann das Datenquellenfeld **model.InvoiceBase.CompanyInfo.Logo** aus. Das Datenquellenfeld vom Typ [Container](er-formula-supported-data-types-composite.md#container) macht das Bild des Firmenlogos als Medieninhalt verfügbar.
11. Wählen Sie **Bindung** aus. Das Formatelement **Bild** ist jetzt mit dem Datenquellenfeld **model.InvoiceBase.CompanyInfo.Logo** verbunden. Daher wird zur Runtime ein Firmenlogobild in die Fußzeile der generierten Rechnungen eingefügt.

    ![Das Formatelement „Bild“ ist jetzt mit dem Datenquellenfeld „model.InvoiceBase.CompanyInfo.Logo“ im EB-Vorgangdesigner verbunden.](./media/er-embed-images-header-footer-excel-reports-derived-format2.png)

12. Wählen Sie **Speichern** und dann schließen Sie die Seite **Designer**.

### <a name="mark-the-custom-format-as-runnable"></a><a id="MarkFormatRunnable"></a>Das benutzerdefinierte Format als ausführbar kennzeichnen

Da die erste Version des benutzerdefinierten Formats mit dem Status **Entwurf** erstellt wurde, können Sie das Format zu Testzwecken ausführen. Um den Bericht auszuführen, verarbeiten Sie eine Kreditorenzahlung mithilfe der Zahlungsmethode, die sich auf Ihr benutzerdefiniertes EB-Format bezieht. Beim Aufrufen eines EB-Formats aus der Anwendung werden standardmäßig nur Versionen mit dem Status **Abgeschlossen** oder **Freigegeben** [berücksichtigt](general-electronic-reporting.md#component-versioning). Dieses Verhalten verhindert, dass EB-Formate mit unfertigen Designs verwendet werden. Für Ihre Testläufe können Sie die Anwendung jedoch zwingen, die Version Ihres EB-Formats mit dem Status **Entwurf** zu verwenden. Auf diese Weise können Sie die aktuelle Formatversion anpassen, falls Änderungen erforderlich sind. Weitere Informationen finden Sie unter [Anwendbarkeit](electronic-reporting-destinations.md#applicability).

Um die Entwurfsversion eines EB-Formats zu verwenden, müssen Sie das EB-Format explizit markieren.

1. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.
2. Auf der Seite **Konfigurationen** im Aktivitätsbereich, auf der Registerkarte **Konfigurationen** in der Gruppe **Erweiterte Einstellungen** wählen Sie **Benutzerparameter** aus.
3. Legen Sie im Dialogfeld **Benutzerparameter** die Option **Testlaufeinstellungen** auf **Ja** fest und wählen Sie dann **OK** aus.
4. Wählen Sie **Bearbeiten** aus, um die aktuelle Seite bearbeitbar zu machen, und wählen Sie dann in der Konfigurationsstruktur im linken Bereich **Freitextrechnung (Excel) benutzerdefiniert** aus.
5. Legen Sie die Option **Entwurf ausführen** auf **Ja** fest.

![Kennzeichnen Sie das benutzerdefinierte Format als ausführbar auf der Seite „Konfigurationen“.](./media/er-embed-images-header-footer-excel-reports-derived-format-configuration2.png)

## <a name="print-a-free-text-invoice-by-using-the-custom-er-format"></a><a id="PrintInvoice2"></a>Eine Freitextrechnung im benutzerdefinierten EB-Format konfigurieren

### <a name="set-up-print-management"></a><a id="ConfigurePrintManagement2"></a>Druckverwaltung einrichten

1. Wechseln Sie zu **Debitoren** \> **Rechnungen** \> **Alle Freitextrechnungen**.
2. Wählen Sie auf der Seite **Freitextrechnung** die Rechnung **FTI-00000002** und dann im Aktivitätsbereich auf der Registerkarte **Rechnung** in der Gruppe **Druckverwaltung** die Option **Druckverwaltung** aus.
3. Klappen Sie auf der Seite **Druckverwaltungseinstellungen** im Baum links **Modul – Debitorenkonten** \> **Dokumente** \> **Freitextrechnung** auf und wählen Sie dann das Element **Original** **\<Default\>** aus.
4. Wählen Sie im Feld **Berichtsformat** **Freitextrechnung (Excel) benutzerdefiniert** aus.
5. Wählen Sie **Esc** zum Verlassen der Seite **Druckverwaltungseinstellungen** und kehren Sie zurück zur Seite **Freitextrechnung**.

### <a name="print-a-free-text-invoice"></a><a id="ProcessInvoice2"></a>Dient zum Drucken einer Freitextrechnung.

1. Stellen Sie sicher, dass auf der Seite **Freitextrechnung** die Rechnung **FTI-00000002** immer noch ausgewählt ist, und wählen Sie dann im Aktivitätsbereich auf der Registerkarte **Rechnung** in der Gruppe **Dokument** **Drucken** \> **Ausgewählt** aus.
2. Laden Sie die generierte Rechnung im Excel-Format herunter und öffnen Sie sie in der Vorschau.
3. Beachten Sie, dass die Fußzeile der generierten Rechnung gemäß der Struktur des benutzerdefinierten EB-Formats neben den Informationen zur Seitennummerierung des Berichts ein Firmenlogo enthält.

![Generierte Freitextrechnung mit Firmenlogo in der Fußzeile.](./media/er-embed-images-header-footer-excel-reports-print-invoice2.gif)

## <a name="additional-resources"></a><a id="References"></a>Zusätzliche Ressourcen

- [Eine Konfiguration zur Generierung von Dokumenten im Excel-Format entwerfen](er-fillable-excel.md)
- [Einbetten von Bildern und Formen in generierten Dokumenten mithilfe von ER](electronic-reporting-embed-images-shapes.md)
