---
title: Hinzufügen neuer Felder zu einer Geschäftsdokumentvorlage in Microsoft Excel
description: In diesem Thema erfahren Sie, wie Sie mit der Funktion Geschäftsdokumentenverwaltung neue Felder zu einer Geschäftsdokumentvorlage in Microsoft Excel hinzufügen können.
author: NickSelin
ms.date: 11/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERBDTemplateEditor
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: af9f3dd81b0681579c14e0afb8281706e8aa534d
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6351793"
---
# <a name="add-new-fields-to-a-business-document-template-in-microsoft-excel"></a>Hinzufügen neuer Felder zu einer Geschäftsdokumentvorlage in Microsoft Excel

[!include[banner](../includes/banner.md)]

Sie können einer Vorlage, die zur Generierung von Geschäftsdokumenten im Format Microsoft Excel verwendet wird, neue Felder hinzufügen. Diese Felder können als Platzhalter hinzugefügt werden, mit denen generierte Dokumente mit den erforderlichen Informationen aus der Anwendung gefüllt werden. Für jedes Feld, das Sie hinzufügen, können Sie auch eine Bindung zu den Datenquellen angeben, um festzulegen, welche Anwendungsdaten in das Feld eingegeben werden, wenn die Vorlage zur Generierung von Geschäftsdokumenten verwendet wird.

Weitere Informationen über diese Funktion erhalten Sie, wenn Sie das Beispiel in diesem Thema abschließen. Dieses Beispiel zeigt, wie Sie eine Vorlage aktualisieren, um die Felder in den generierten Freitext-Rechnungsformularen auszufüllen.

## <a name="configure-business-document-management-to-edit-templates"></a>Konfigurieren Sie die Geschäftsdokumentenverwaltung, um Vorlagen zu bearbeiten.

Da die Geschäftsdokumentenverwaltung (BDM) auf dem [Überblick über die elektronische Berichterstattung (ER)](general-electronic-reporting.md) aufbaut, müssen Sie die erforderlichen ER- und BDM-Parameter konfigurieren, bevor Sie mit BDM arbeiten können.

1.  Melden Sie sich auf der Instanz von Microsoft Dynamics 365 Finance als Systemadministrator an.
2.  Führen Sie die folgenden Schritte des Beispiels im Thema [Übersicht Geschäftsdokumentenverwaltung](er-business-document-management.md) aus:

    1.  ER-Parameter konfigurieren.
    2.  Schalten Sie BDM ein.

Sie können nun mit dem BDM beginnen, um Geschäftsdokumentvorlagen zu bearbeiten.

## <a name="import-er-solutions-that-contain-a-template"></a>Importieren von ER-Lösungen, die eine Vorlage enthalten

Das Beispiel in diesem Verfahren verwendet die offiziell veröffentlichte ER-Lösung. Sie müssen die ER-Konfigurationen dieser Lösung in Ihre aktuelle Finanzinstanz importieren.

Die **Konfiguration der Freitextrechnung (Excel)** ER-Format dieser Lösung enthält die Geschäftsdokumentvorlage im Excel-Format, die mit dem BDM bearbeitet werden kann. Importieren Sie die neueste Version dieser ER-Format-Konfiguration aus Microsoft Dynamics Lifecycle Service (LCS). Die entsprechenden ER-Datenmodell- und ER-Modellzuordnungskonfigurationen werden automatisch importiert.

Weitere Informationen zum Importieren von ER-Konfigurationen finden Sie unter [Verwaltung des Lebenszyklus der ER-Konfiguration](general-electronic-reporting-manage-configuration-lifecycle.md).

![Seite LCS gemeinsame Objektbibliothek.](./media/BDM-AddFldExcel-LCS.png)

### <a name="edit-the-er-solution-template"></a>Bearbeiten der ER-Lösungsvorlage

1.  Melden Sie sich als Benutzer an, der Zugriff auf den Arbeitsbereich **Geschäftsdokumentenverwaltung** hat.
2.  Öffnen Sie den Arbeitsbereich **Geschäftsdokumentenverwaltung**.

    ![Arbeitsbereich Geschäftsdokumentenverwaltung.](./media/BDM-AddFldExcel-Workspace.png)

3.  Wählen Sie im Raster die Vorlage **Freitextrechnung (Excel)**.
4.  Wählen Sie im rechten Bereich **Neue Vorlage**, um eine neue Vorlage zu erstellen, die auf der ausgewählten Vorlage basiert.
5.  Geben Sie im Feld **Titel** als Titel der neuen Vorlage **Freitextrechnung (Excel) Contoso** ein.
6.  Wählen Sie **OK** aus, um den Beginn des Bearbeitungsprozesses zu bestätigen.

Die Seite mit dem Editor für BDM-Vorlagen wird angezeigt. Mit Microsoft 365 können Sie die ausgewählte Vorlage online in der eingebetteten Steuerung bearbeiten.

![BDM-Vorlagen-Editor-Seite.](./media/BDM-AddFldExcel-EditableTemplate.png)

### <a name="add-the-label-for-a-new-field-to-the-template"></a>Hinzufügen der Bezeichnung für ein neues Feld zur Vorlage

1.  Aktivieren Sie auf der Seite des BDM-Vorlageneditors, in der Excel-Leiste, auf der Registerkarte **Ansicht** die Kontrollkästchen **Überschriften und Rasterlinien** für die editierbare Excel-Vorlage.

    ![Aktivierte Kontrollkästchen für Überschriften und Rasterlinien.](./media/BDM-AddFldExcel-EditableTemplate2.png)

2.  Zellen auswählen **E8:F8**.
3.  Wählen Sie in der Excel-Leiste auf der Registerkarte **Start** **Zusammenführen & Zentrieren**, um die ausgewählten Zellen zu einer neuen zusammengeführten **E8:F8** Zelle zusammenzuführen.
4.  Geben Sie in der zusammengeführten Zelle **E8:F8** **URL** ein.
5.  Wählen Sie zusammengeführte Zelle **E7:F7**, wählen Sie **Formatkopie**, und wählen Sie dann zusammengeführte Zelle **E8:F8**, um sie genauso zu formatieren wie zusammengeführte Zelle **E7:F7**.

    ![Neue Feldbezeichnung in der Vorlage hinzugefügt.](./media/BDM-AddFldExcel-EditableTemplate3.png)

### <a name="format-the-template-to-reserve-space-for-a-new-field"></a>Formatieren Sie die Vorlage, um Platz für ein neues Feld zu reservieren.

1.  Wählen Sie auf der Seite des BDM-Vorlageneditors die zusammengeführte Zelle **G8:H8**.
2.  Wählen Sie in der Excel-Leiste auf der Registerkarte **Start** **Zusammenführen & Zentrieren**, um die ausgewählten Zellen zu einer neuen zusammengeführten **G8:H8** Zelle zusammenzuführen.
3.  Wählen Sie zusammengeführte Zelle **G7:H7**, wählen Sie **Formatkopie**, und wählen Sie dann zusammengeführte Zelle **G8:H8**, um sie genauso zu formatieren wie zusammengeführte Zelle **G7:H7**.

    ![Platz für das neue Feld reserviert.](./media/BDM-AddFldExcel-EditableTemplate4.png)

4.  Wählen Sie im Feld **Name** **CompanyInfo**.

    Der Bereich **CompanyInfo** der aktuellen Excel-Vorlage enthält alle Felder, die verwendet werden, um den Kopf eines generierten Berichts mit den Details der aktuellen Firma als Verkäuferpartei zu füllen.

    ![CompanyInfo Bereich ausgewählt.](./media/BDM-AddFldExcel-SelectCompanyInfoRange.png)

### <a name="add-a-new-field-to-the-template"></a>Ein neues Feld zur Vorlage hinzufügen

1.  Wählen Sie auf der Seite **BDM-Vorlageneditor**, im Aktivitätsbereich **Format anzeigen**.
2.  Wählen Sie im Bereich **Vorlagenstruktur** **Hinzufügen**.

    > [!NOTE]
    > Sie müssen den Abschnitt der Vorlage, den Sie als neues Feld verwenden möchten, anpassen. Sie haben diese Anpassung bereits vorgenommen, indem Sie die zusammengeführte Zelle **G8:H8** formatiert haben.

    ![Hinzufügen eines neuen Feldes zur Vorlage.](./media/BDM-AddFldExcel-AddCell.png)

3.  Wählen Sie **Excel\Zelle**, um ein neues Feld als Zelle in der Vorlage hinzuzufügen.

    Sie können **Excel\Bereich** wählen, wenn Sie der Vorlage einen neuen Bereich hinzufügen möchten. Der eingegebene Bereich kann mehrere Zellen enthalten. Sie können diese Zellen später hinzufügen.
    
    Beachten Sie, dass die Vorlagenkomponente **CompanyInfo** automatisch im Bereich **Vorlagenstruktur** ausgewählt wird, da sie die am besten geeignete übergeordnete Komponente in der aktuellen Vorlagenstruktur für das Feld ist, das Sie hinzufügen.
    
4.  Geben Sie im Feld **Excel-Bereich** **CompanyURL_Value** ein.
5.  Wählen Sie **OK** aus.

    ![CompanyURL_Wertfeld in der Vorlagenstruktur hinzugefügt.](./media/BDM-AddFldExcel-EditableTemplate5.png)

6.  Wählen Sie im Bereich **Vorlagenstruktur** die Schaltfläche Ellipsis (...) und dann **Bindungen anzeigen**.

    ![Ausgewählte Bindungen anzeigen.](./media/BDM-AddFldExcel-ShowBindings.png)

    Der Bereich **Vorlagenstruktur** zeigt nun die Datenquellen an, die im zugrunde liegenden ER-Format verfügbar sind.

7.  Wählen Sie **CompanyInfo_Value** als Feld, das Sie an eine Datenquelle des zugrunde liegenden ER-Formats binden möchten.
8.  Erweitern Sie im Abschnitt **Datenquellen** des Bereichs **Vorlagenstruktur** **Modell \> InvoiceBase \> CompanyInfo**.
9.  Wählen Sie unter **CompanyInfo** den Eintrag **WebsiteURI**.

    ![WebsiteURI Artikel ausgewählt.](./media/BDM-AddFldExcel-BindURL.png)

10. Wählen Sie **Bindung** aus.
11. Wählen Sie im Bereich **Vorlagenstruktur** **Speichern**, und schließen Sie dann die Seite des BDM-Vorlageneditors.

Im Arbeitsbereich **Geschäftsdokumentenmanagement** zeigt die Registerkarte **Vorlage** im rechten Bereich die aktualisierte Vorlage an. Beachten Sie im Raster, dass das Feld **Status** für die bearbeitete Vorlage in **Entwurf** geändert wurde und das Feld **Revision** nicht mehr leer ist. Diese Änderungen zeigen an, dass der Prozess der Bearbeitung dieser Vorlage gestartet wurde.

![Bearbeitete Vorlage im Arbeitsbereich Geschäftsdokumentenmanagement.](./media/BDM-AddFldExcel-Workspace2.png)

## <a name="review-company-settings"></a>Überprüfen der Unternehmenseinstellungen

1.  Gehen Sie zu **Organisationsverwaltung \> Organisationen \> Juristische Personen**.
2.  Überprüfen Sie unter **Kontaktinformationen** Inforegister, ob die Firmen-URL eingegeben wurde.

![Firmen-URL, die auf der Seite Juristische Personen eingegeben wurde.](./media/BDM-AddFldExcel-CompanyInfo.png)

## <a name="generate-business-documents-to-test-the-updated-template"></a>Generieren Sie Geschäftsdokumente, um die aktualisierte Vorlage zu testen.

1.  Ändern Sie in der Anwendung die Firma auf **USMF** und gehen Sie zu **Forderung \> Rechnungen \> Alle Freitextrechnungen**.
2.  Wählen Sie Rechnung **FTI-00000002**, und wählen Sie dann **Druckverwaltung**.
3.  Erweitern Sie im linken Bereich **Modul - Debitorenbuchhaltung \> Dokumente \> Freitextrechnung**.
4.  Wählen Sie unter **Freitextrechnung** die Ebene **Originalbeleg**, um den Umfang der zu bearbeitenden Rechnungen festzulegen.
5.  Wählen Sie im rechten Bereich im Feld **Berichtsformat** die Vorlage **Freitextrechnung (Excel) Contoso** für die angegebene Dokumentebene.

    ![Freitextrechnung (Excel) Contoso-Vorlage ausgewählt.](./media/BDM-AddFldExcel-PrintMngtSetting.png)

6.  Drücken Sie **Esc**, um die aktuelle Seite zu schließen.
7.  Wählen Sie **Drucken \> Ausgewählt**.
8.  Laden Sie das generierte Dokument herunter und öffnen Sie es in Excel.

    ![Freitextrechnung in Excel.](./media/BDM-AddFldExcel-PreviewReport.png)

Die geänderte Vorlage wird verwendet, um den Freitextrechnungsbericht für den ausgewählten Artikel zu generieren. Um zu analysieren, wie sich Änderungen, die Sie an der Vorlage vornehmen, auf diesen Bericht auswirken, führen Sie den Bericht in einer Anwendungssitzung unmittelbar nach der Änderung der Vorlage in einer anderen Anwendungssitzung aus.

## <a name="related-links"></a>Zugehörige Links

[Überblick über die elektronische Berichterstellung (Electronic reporting, ER)](general-electronic-reporting.md)

[Geschäftsdokumentverwaltung – Übersicht](er-business-document-management.md)

[Entwerfen einer Konfiguration für das Erstellen von Berichten im OPENXML-Format](tasks/er-design-reports-openxml-2016-11.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]