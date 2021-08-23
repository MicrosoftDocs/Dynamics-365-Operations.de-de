---
title: Struktur einer Geschäftsdokumentvorlage aktualisieren
description: In diesem Thema wird erläutert, wie Sie die Struktur einer Geschäftsdokumentvorlage mithilfe der Funktion zur Verwaltung von Geschäftsdokumenten aktualisieren.
author: NickSelin
ms.date: 11/19/2020
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
ms.search.validFrom: 2019-12-01
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 2f57e3f3a84a6e767755c69074bc194e90793e6edd79d0e07ae7449d45ec7539
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6775285"
---
# <a name="update-the-structure-of-a-business-document-template"></a>Struktur einer Geschäftsdokumentvorlage aktualisieren 

[!include[banner](../includes/banner.md)]

Im Bereich **Vorlagenstruktur** des Editors für Vorlagen zur [Verwaltung von Geschäftsdokumenten](er-business-document-management.md) können Sie eine Geschäftsdokumentvorlage durch das [Hinzufügen neuer Felder](er-bdm-add-field-to-excel-template.md) zu einer Vorlage in Microsoft Excel ändern. Die Struktur der Vorlage wird dann in Dynamics 365 Finance automatisch aktualisiert, damit sie die Änderungen widerspiegelt, die Sie im Bereich **Vorlagenstruktur** vorgenommen haben.

Sie können eine Vorlage auch mithilfe der Office 365-Onlinefunktion ändern. Beispielsweise können Sie dem bearbeitbaren Arbeitsblatt ein neues benanntes Element, beispielsweise ein Bild oder eine Form, hinzufügen. In diesem Fall wird die Struktur der Vorlage in Finance nicht automatisch aktualisiert und das von Ihnen hinzugefügte Element wird nicht im Bereich **Vorlagenstruktur** angezeigt. Aktualisieren Sie die Vorlagenstruktur in Finance manuell, indem Sie **Struktur aktualisieren** auf der Seite des Vorlagen-Editors auswählen.

Weitere Informationen über diese Funktion erhalten Sie, wenn Sie das folgende Beispiel abschließen.

## <a name="example-update-the-structure-of-a-business-document-template"></a>Beispiel: Struktur einer Geschäftsdokumentvorlage aktualisieren

Dieses Beispiel zeigt, wie ein Systemadministrator die Struktur einer Geschäftsdokumentvorlage in Finance aktualisieren kann, nachdem die Vorlage in Office Online geändert wurde. In den folgenden Abschnitten werden die damit verbundenen Schritte erläutert.

### <a name="prepare-a-business-document-template-for-editing"></a>Eine Geschäftsdokumentvorlage zur Bearbeitung vorbereiten

Führen Sie die folgenden Prozeduren in [Geschäftsdokumentverwaltung – Übersicht](er-business-document-management.md) aus.

1. [Parameter der elektronischen Berichterstellung konfigurieren](er-business-document-management.md#configure-er-parameters)
2. [Importieren von ER-Lösungen](er-business-document-management.md#import-er-solutions)
3. [Aktivieren der Geschäftsdokumentverwaltung](er-business-document-management.md#enable-business-document-management)
4. [Parameter konfigurieren](er-business-document-management.md#configure-parameters)

### <a name="edit-a-business-document-template"></a>Eine Geschäftsdokumentvorlage bearbeiten

1. Wählen Sie im Arbeitsbereich **Geschäftsdokumentverwaltung** **Neues Dokument** aus.
2. Wählen Sie auf der Seite **Neue Vorlage erstellen** die Vorlage **Freitextrechnung (EB-Beispiel) (Excel)** aus.
3. Wählen Sie **Dokument erstellen** aus.
4. Geben Sie in das Feld **Titel** den Text **FTR-Beispiel Litware** ein.
5. Wählen Sie **OK** aus, um die neue Vorlage zu erstellen.

    > [!NOTE]
    > Wenn Sie sich noch nicht bei Office Online angemeldet haben, werden Sie [zur Anmeldeseite von Office 365 weitergeleitet](er-business-document-management.md#frequently-asked-questions). Um zu Ihrer Finance-Umgebung zurückzukehren, wählen Sie die Schaltfläche **Zurück** in Ihrem Browser aus.

    Die neue Vorlage wird zur Bearbeitung in der eingebetteten Excel Online-Steuerung auf der Seite des Vorlagen-Editors geöffnet.

[![Verwenden des Arbeitsbereichs zur Geschäftsdokumentverwaltung, um mit der Bearbeitung einer Geschäftsdokumentvorlage zu beginnen.](./media/er-bdm-update-structure1.gif)](./media/er-bdm-update-structure1.gif)

### <a name="review-the-current-structure-of-the-editable-template"></a>Aktuelle Struktur der bearbeitbaren Vorlage überprüfen

1. Wählen Sie in Excel Online im Menüband auf der Registerkarte **Ansicht** in der Gruppe **Anzeigen** die Option **Rasterlinien** aus.
2. Wählen Sie in der bearbeitbaren Vorlage das Rechteck über dem Vorlagentitel aus. Dieses Rechteck ist ein Bild mit dem Namen **rptHeaderCompLogo**.
3. Wenn der Bereich **Vorlagenstruktur** ausgeblendet ist, wählen Sie **Struktur anzeigen** aus.
4. Erweitern Sie im Bereich **Vorlagenstruktur** die Struktur **Bericht \> Rechnung \> rptHeader \> rptHeaderPart1**.
5. Beachten Sie, dass in der Vorlagenstruktur in Finance das Element **rptHeaderCompLogo** als untergeordnetes Element von **Bericht \> Rechnung \> rptHeader \> rptHeaderPart1** dargestellt wird.

[![Verwenden des Arbeitsbereichs zur Verwaltung von Geschäftsdokumenten zum Überprüfen der aktuellen Struktur einer bearbeitbaren Vorlage.](./media/er-bdm-update-structure2.gif)](./media/er-bdm-update-structure2.gif)

### <a name="update-the-structure-of-a-business-document-template-by-deleting-a-picture"></a>Struktur einer Geschäftsdokumentvorlage durch Löschen eines Bilds aktualisieren

1. Wählen Sie in Excel Online in der bearbeitbaren Vorlage das Bild **rptHeaderCompLogo** aus.
2. Führen Sie einen der folgenden Schritte aus, um das ausgewählte Bild aus der bearbeitbaren Vorlage zu löschen:

    - Drücken Sie auf der Tastatur die **ENTF**-Taste.
    - Wählen Sie das Bild aus, halten Sie es gedrückt (oder klicken Sie mit der rechten Maustaste darauf) und wählen Sie dann **Ausschneiden** aus.

    > [!NOTE]
    > Das Element **rptHeaderCompLogo** ist in der Vorlagenstruktur in Finance derzeit noch vorhanden, obwohl das Bild nicht mehr in der Excel-Vorlage enthalten ist.

3. Wählen Sie **Struktur aktualisieren** aus, um die Struktur der bearbeitbaren Vorlage in Excel und Finance zu synchronisieren.
4. Erweitern Sie im Bereich **Vorlagenstruktur** die Struktur **Bericht \> Rechnung \> rptHeader \> rptHeaderPart1**.
5. Beachten Sie, dass das Element **rptHeaderCompLogo** in der Vorlagenstruktur in Finance nicht mehr enthalten ist.

[![Verwenden des Arbeitsbereichs zur Geschäftsdokumentverwaltung, um ein Bild aus einer Geschäftsdokumentvorlage zu löschen.](./media/er-bdm-update-structure3.gif)](./media/er-bdm-update-structure3.gif)

### <a name="update-the-structure-of-a-business-document-template-by-adding-a-picture"></a>Struktur einer Geschäftsdokumentvorlage durch Hinzufügen eines Bilds aktualisieren

1. Wählen Sie in Excel Online im Menüband auf der Registerkarte **Einfügen** in der Gruppe **Abbildungen** die Option **Bild** aus.
2. Wählen Sie **Datei auswählen** aus, navigieren Sie zu dem Bild, das Sie hinzufügen möchten, wählen Sie es aus und wählen Sie dann **OK** aus.
3. Wählen Sie **Einfügen** aus.
4. Verschieben Sie das neue Bild, bis es sich an der richtigen Stelle befindet. Standardmäßig wird das Bild von Excel benannt. Beispielsweise könnte das Bild den Namen **Bild 2** erhalten.
5. Wählen Sie **Struktur aktualisieren** aus, um die Struktur der bearbeitbaren Vorlage in Excel und Finance zu synchronisieren.
6. Erweitern Sie im Bereich **Vorlagenstruktur** die Struktur **Bericht \> Rechnung \> rptHeader \> rptHeaderPart1**.
7. Beachten Sie, dass das neue Bild jetzt als ein Element in der Vorlagenstruktur in Finance enthalten ist.

[![Verwenden des Arbeitsbereichs zur Geschäftsdokumentverwaltung, um ein Bild zu einer Geschäftsdokumentvorlage hinzuzufügen.](./media/er-bdm-update-structure4.gif)](./media/er-bdm-update-structure4.gif)

## <a name="related-links"></a>Zugehörige Links

[Überblick über die elektronische Berichterstellung (ER)](general-electronic-reporting.md)

[Geschäftsdokumentverwaltung – Übersicht](er-business-document-management.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]