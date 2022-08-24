---
title: Entwerfen Sie ein ER-Format, um Zeilen auf derselben Excel-Seite zusammenzuhalten.
description: In diesem Artikel wird erklärt, wie Sie ein elektronisches Berichtsformat (EB) entwerfen, bei dem die Zeilen auf derselben Microsoft Excel-Seite zusammenbleiben.
author: kfend
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2022-03-01
ms.dyn365.ops.version: Version 10.0.26
ms.custom: 220314
ms.assetid: ''
ms.search.form: EROperationDesigner
ms.openlocfilehash: 7ecc4358a0d4d9ae9e729393bd3ac4cefbf15ad2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287957"
---
# <a name="design-an-er-format-to-keep-rows-together-on-the-same-excel-page"></a>Entwerfen Sie ein ER-Format, um Zeilen auf derselben Excel-Seite zusammenzuhalten.

[!include [banner](../includes/banner.md)]


Dieser Artikel erklärt, wie Benutzer mit der Rolle „Systemadministrator“ oder „Electronic Reporting Functional Consultant“ ein [Elektronische Berichterstellung (EB)](general-electronic-reporting.md)-[Format](er-overview-components.md#format-component) konfigurieren können, das ausgehende Belege in Microsoft Excel generiert und die Paginierung der Belege so verwaltet, dass erstellte Zeilen auf derselben Seite bleiben.

In diesem Beispiel ändern Sie das von Microsoft bereitgestellte ER-Format, das zum Drucken von Rechnungen mit freiem Text in Excel verwendet wird. Mit Ihren Änderungen können Sie die Paginierung eines generierten Freitext-Rechnungsberichts so verwalten, dass alle Zeilen einer einzelnen Rechnungszeile nach Möglichkeit auf derselben Seite stehen.

Die Verfahren in diesem Artikel können im **USMF**-Unternehmen abgeschlossen werden. Eine Codierung ist nicht erforderlich.

In diesem Beispiel erstellen Sie die erforderlichen ER [Konfigurationen](general-electronic-reporting.md#Configuration) für die Beispielfirma **Litware, Inc.**. Stellen Sie sicher, dass der Konfigurationsanbieter für die Beispielfirma **Litware, Inc.** (`http://www.litware.com`) für das ER Framework aufgeführt und als **Aktiv** markiert ist. Wenn dieser Konfigurationsanbieter nicht aufgeführt ist oder nicht als **Aktiv** markiert ist, folgen Sie den Schritten unter [Erstellen Sie einen Konfigurationsanbieter und markieren Sie ihn als aktiv](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="enter-a-new-free-text-invoice"></a>Geben Sie eine neue Freitext-Rechnung ein

1. Folgen Sie den Schritten in [Erstellen Sie eine Freitextrechnung](../../../finance/accounts-receivable/create-free-text-invoice-new.md#create-a-free-text-invoice-1), um eine Freitextrechnung hinzuzufügen.

    1. Fügen Sie der Rechnung eine einzelne Zeile hinzu.
    2. Fügen Sie fünf Notizen für die Rechnungszeile hinzu.

    ![Überprüfung der Rechnungszeilen-Notizen auf der Seite Anhänge.](./media/er-keep-excel-rows-together-notes.png)

2. Folgen Sie den Schritten unter [Zeilen kopieren](../../../finance/accounts-receivable/create-free-text-invoice-new.md#copy-lines), um fünf zusätzliche Rechnungszeilen zu erstellen, die Kopien der Rechnungszeile sind, die Sie im vorherigen Schritt hinzugefügt haben.

    ![Überprüfung der Zeilen einer Freitextrechnung auf der Seite Freitextrechnung.](./media/er-keep-excel-rows-together-invoice.png)

## <a name="configure-the-er-framework"></a>Konfigurieren des EB-Frameworks

Befolgen Sie die Schritte in [ER-Framework konfigurieren](er-quick-start2-customize-report.md#ConfigureFramework), um den minimalen Satz von ER-Parametern einzurichten. Sie müssen diese Einrichtung abschließen, bevor Sie mit der Verwendung des ER-Frameworks beginnen, um eine benutzerdefinierte Version eines standardmäßigen ER-Formats zu entwerfen.

## <a name="import-the-standard-er-format-configuration"></a>Die standardmäßige ER-Formatkonfiguration importieren

Befolgen Sie die Schritte in [ER-Standard-Formatkonfiguration importieren](er-quick-start2-customize-report.md#ImportERSolution1), um die ER-Standardkonfigurationen Ihrer aktuellen Instanz von Dynamics 365 Finance hinzuzufügen. Importieren Sie zum Beispiel die Version **252.116** der Konfiguration des Formats **Freitext-Rechnung (Excel)**. Die Basisversion **252** der Basis-**Rechnungsmodell**-Konfiguration wird automatisch aus dem Repository importiert, zusammen mit der erforderlichen **Rechnungsmodell-Zuordnung**-Konfiguration.

## <a name="set-up-print-management-to-use-the-standard-er-format"></a>Druckmanagement für die Verwendung des Standard-ER-Formats festlegen

Folgen Sie den Schritten in [Druckverwaltung einrichten](er-embed-images-header-footer-excel-reports.md#ConfigurePrintManagement1), um die Druckverwaltung für das Modul **Debitoren** so zu konfigurieren, dass das Standard-ER-Format für den Druck von Freitext-Rechnungen verwendet wird.

## <a name="configure-a-format-destination-for-the-standard-er-format"></a>Konfigurieren Sie ein Formatziel für das Standard-ER-Format

Führen Sie die Schritte unter [Konfigurieren Sie ein Formatziel für die Bildschirmvorschau](er-quick-start1-new-solution.md#ConfigureDestination) aus, um das Ziel [Screen](er-destination-type-screen.md) ER des Standard-ER-Formats so zu konfigurieren, dass die generierten Berichte in das PDF-Format konvertiert und in einer neuen Browser-Registerkarte in der Vorschau angezeigt werden.

## <a name="print-a-free-text-invoice-by-using-the-standard-er-format"></a>Eine Freitextrechnung im Standard-EB-Format konfigurieren

1. Führen Sie die Schritte unter [Drucken einer Freitextrechnung](er-embed-images-header-footer-excel-reports.md#ProcessInvoice1) aus, um das Standard-ER-Format zu verwenden, um einen Freitext-Rechnungsbericht im Excel-Format für die hinzugefügte Rechnung zu erstellen.
2. Laden Sie die generierte Excel-Arbeitsmappe herunter und überprüfen Sie sie in der Excel-Desktop-Anwendung.

    Beachten Sie, dass die sechste Zeile der Rechnung auf der ersten Seite des Berichts beginnt und auf der zweiten Seite fortgesetzt wird. Die letzte Notiz erscheint auf der zweiten Seite, und es ist nicht offensichtlich, dass sie zur sechsten Zeile der Rechnung gehört. Daher erschwert der Seitenumbruch in der Mitte des Inhalts für die Rechnungszeile die Lesbarkeit dieses Dokuments.

    ![Überprüfung der Paginierung der generierten Freitext-Rechnung in der Excel-Desktop-Anwendung.](./media/er-keep-excel-rows-together-invoice1.gif)

Die übrigen Verfahren in diesem Artikel zeigen, wie Sie das Standard-EB-Format anpassen können, um das Aussehen und die Lesbarkeit des Rechnungsberichts zu verbessern, indem Sie den gesamten Inhalt für eine einzelne Rechnungszeile auf derselben Seite behalten.

## <a name="create-a-custom-format"></a>Erstellen eines benutzerdefinierten Formats

Führen Sie die Schritte unter [Ein benutzerdefiniertes Format erstellen](er-embed-images-header-footer-excel-reports.md#DeriveProvidedFormat) aus, um ein Format aus dem importierten ER-Format abzuleiten und eine **Benutzerdefinierte ER-Konfiguration für Freitextrechnungen (Excel)** zu erstellen, die Sie bearbeiten und ändern können.

## <a name="edit-the-custom-format"></a>Das benutzerdefinierte Format bearbeiten

1. Folgen Sie den Schritten in [Ein angepasstes Format erstellen](er-embed-images-header-footer-excel-reports.md#ConfigureDerivedFormat), um das abgeleitete ER-Format zur Bearbeitung im ER-Formatdesigner zu öffnen.
2. Erweitern Sie auf der Seite **Formatdesigner** im Baum der Formatkomponenten im linken Fensterbereich **Freitext Rechnung \> Blatt \> InvoiceLines** und wählen Sie die Komponente **InvoiceLines_Values**.
3. Legen Sie auf der Registerkarte **Format** die Option **Zeilen zusammenhalten** auf **Ja** fest.

    ![Festlegen der Option Zeilen zusammenhalten für das editierbare ER-Format auf der Seite Formatdesigner.](./media/er-keep-excel-rows-together-format.png)

4. Klicken Sie auf **Speichern** und schließen Sie die Seite.

## <a name="mark-the-custom-format-as-runnable"></a>Das benutzerdefinierte Format als ausführbar kennzeichnen

Führen Sie die Schritte unter [Markieren Sie das angepasste Format als lauffähig](er-embed-images-header-footer-excel-reports.md#MarkFormatRunnable) aus, um die modifizierte Version des angepassten ER-Formats lauffähig zu machen.

## <a name="set-up-print-management-to-use-the-custom-er-format"></a>Legen Sie die Druckverwaltung so fest, dass das angepasste ER-Format verwendet wird.

Folgen Sie den Schritten in [Druckverwaltung einrichten](er-embed-images-header-footer-excel-reports.md#ConfigurePrintManagement2), um die Druckverwaltung für das Modul **Debitoren** so zu konfigurieren, dass das angepasste ER-Format für den Druck von Freitext-Rechnungen verwendet wird.

## <a name="configure-a-format-destination-for-the-custom-er-format"></a>Konfigurieren Sie ein Formatziel für das angepasste ER-Format

Folgen Sie den Schritten in [Konfigurieren Sie ein Formatziel für die Bildschirmvorschau](er-quick-start1-new-solution.md#ConfigureDestination), um das **Bildschirm** ER-Ziel des angepassten ER-Formats so zu konfigurieren, dass generierte Berichte in das PDF-Format konvertiert und in einer neuen Browser-Registerkarte in der Vorschau angezeigt werden.

## <a name="print-a-free-text-invoice-by-using-the-custom-er-format"></a>Eine Freitextrechnung im benutzerdefinierten EB-Format konfigurieren

1. Führen Sie die Schritte unter [Drucken einer Freitextrechnung](er-embed-images-header-footer-excel-reports.md#ProcessInvoice2) aus, um mit dem angepassten ER-Format einen Freitext-Rechnungsbericht im Excel-Format für die hinzugefügte Rechnung zu erstellen.
2. Laden Sie die generierte Excel-Arbeitsmappe herunter und überprüfen Sie sie in der Excel-Desktop-Anwendung.

    Beachten Sie, dass die sechste Zeile der Rechnung auf der zweiten Seite beginnt und alle Excel-Zeilen, die diese Rechnungszeile darstellen, zusammen auf dieser Seite erscheinen.

    ![Überprüfung der aktualisierten Paginierung der generierten Freitext-Rechnung in der Excel-Desktop-Anwendung.](./media/er-keep-excel-rows-together-invoice2.gif)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Eine Konfiguration zur Generierung von Dokumenten im Excel-Format entwerfen](er-fillable-excel.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
