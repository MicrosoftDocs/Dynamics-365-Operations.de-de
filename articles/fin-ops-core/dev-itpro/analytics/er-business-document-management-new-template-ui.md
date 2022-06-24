---
title: Microsoft Office-Benutzeroberfläche in der Verwaltung von Belegen in Unternehmen (enthält Video)
description: Dieser Artikel erklärt, wie die neue Nutzungsoberfläche in der Funktion der Geschäftsdokumentverwaltung des Frameworks für elektronische Berichterstellung (EB) verwendet wird.
author: v-anamir
ms.date: 01/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-anamir
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: bcc464a17e27393c5904c59b8439de6ca000d57a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8892224"
---
# <a name="microsoft-office-style-user-interface-in-business-document-management"></a>Benutzeroberfläche im Stil von Microsoft Office für Dokumente in der Geschäftsdokumentverwaltung

[!include [banner](../includes/banner.md)]

Mit der Geschäftsdokumentverwaltung können geschäftliche Benutzer Geschäftsdokumentvorlagen mit einem Microsoft Office 365-Dienst oder der entsprechenden Microsoft Office-Desktopanwendung bearbeiten. Bearbeitungen können Entwurfsänderungen oder neue Bereitstellungen umfassen. Benutzer können auch Platzhalter hinzufügen, um zusätzliche Daten aufzunehmen, ohne den Quellcode ändern zu müssen. Weitere Informationen zum Arbeiten mit der Geschäftsdokumentenverwaltung finden Sie unter [Überblick über die Geschäftsdokumentverwaltung](er-business-document-management.md).

Die neue Benutzeroberfläche ist übersichtlicher und benutzerfreundlicher. Der Bereich **Geschäftsbelege** zeigt nur die Vorlagen an, die dem aktuellen [aktiven](tasks/er-configuration-provider-mark-it-active-2016-11.md) [Anbieter](general-electronic-reporting.md#Provider) gehören und sich in der aktuellen Instanz von Dynamics 365 Finance befinden. In der vorherigen Benutzeroberfläche waren auf der Registerkarte **Vorlage** alle Vorlagen aufgelistet, die für einen beliebigen Anbieter verfügbar waren. Außerdem wurden alle Vorlagen angezeigt, die von Benutzern mit derselben Rolle erstellt und bearbeitet wurden.

Mit der Schaltfläche **Neuer Beleg** im Arbeitsbereich **Geschäftsdokumentenverwaltung** können Sie eine Vorlage im Format [Elektronisches Reporting (ER)](general-electronic-reporting.md) [Konfiguration](general-electronic-reporting.md#Configuration) erstellen und bearbeiten, die von einem anderen Anbieter bereitgestellt wird und sich in der aktuellen Finance-Instanz befindet, oder eine neue Vorlage aus einer Excel-Arbeitsmappe hochladen. Außerdem können Sie ab Version 10.0.25 mit der Schaltfläche **Neuer Beleg** eine Vorlage in einer ER-Formatkonfiguration erstellen und bearbeiten, die im [Globalen Repository](general-electronic-reporting.md#Repository) gespeichert ist.

In den Beispielen in diesem Artikel ist der aktive Anbieter Contoso, und Sie erstellen damit eine Vorlage, die auf einer von Microsoft bereitgestellten Vorlage basiert. Alternativ können Sie eine Vorlage erstellen, indem Sie Ihre eigene Vorlage im Excel-Format hochladen.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RWAVQg]

Das Video [Erstellen eines neuen Belegs mit Unternehmensbelegmanagement](https://youtu.be/gAIYl-mM_pw) (oben gezeigt) ist in der Playlist [Finance und Operations](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) enthalten, die auf YouTube verfügbar ist.

## <a name="make-the-new-document-ui-in-business-document-management-available"></a>Neue Benutzeroberfläche für die Geschäftsdokumentverwaltung zur Verfügung stellen

Um die neue Dokument-Benutzeroberfläche in der Geschäftsdokumentverwaltung zu verwenden, müssen Sie die Funktion **Office-ähnliche UI-Erfahrung für Geschäftsdokumentverwaltung** im Arbeitsbereich **Funktionsverwaltung** aktivieren.

Befolgen Sie diese Schritte, um diese Funktion für alle juristischen Personen zu aktivieren.

1. Wählen Sie im Arbeitsbereich **Funktionsverwaltung** auf der Registerkarte **Alle** die Funktion **Office-ähnliche UI-Erfahrung für Geschäftsdokumentverwaltung** aus der Liste aus.
2. Wählen Sie **Jetzt aktivieren** aus, um die ausgewählte Fähigkeit zu aktivieren.
3. Aktualisieren Sie die Seite, um auf die neue Funktion zugreifen können.

## <a name="add-or-activate-a-provider"></a>Hinzufügen oder Aktivieren eines Anbieters

Jede Vorlage eines geschäftlichen Belegs wird in einer ER-Formatkonfiguration gespeichert, die als Eigentum eines bestimmten Konfigurationsanbieters gekennzeichnet ist. Wenn Sie eine neue Vorlage erstellen, wird eine neue ER-Formatkonfiguration erstellt, die diese Vorlage enthält. Daher muss ein Anbieter für diese Konfiguration identifiziert werden. Hierfür wird der aktive Provider des ER Frameworks verwendet. Wenn es keinen Anbieter in ER gibt, können Sie einen erstellen. Wenn es keinen *aktiven* Anbieter gibt, können Sie einen der vorhandenen Anbieter aktivieren. Ein Dialog zum Hinzufügen oder Aktivieren eines Anbieters wird geöffnet, wenn dies erforderlich ist, während Sie mit dem Hinzufügen einer neuen Vorlage beginnen.

### <a name="add-a-new-provider"></a>Neuen Anbieter hinzufügen

Um einen neuen Provider zu erstellen, folgen Sie diesen Schritten im Dialog **Konfiguration Provider**:

1.  Geben Sie auf der Registerkarte **Konfigurationsanbieter wählen** in das Feld **Name** den Namen des neuen Anbieters ein.
2.  Geben Sie in das Feld **Internetadresse** die Internetadresse (URL) des neuen Anbieters ein. 
3.  Wählen Sie **OK** aus.

    ![Erstellen eines neuen Belegs in Unternehmensbelegmanagement.](./media/bdm_create_provider.png)

Der hinzugefügte Anbieter wird automatisch aktiviert.

### <a name="activate-a-provider"></a>Aktivieren eines Providers

Um einen Anbieter zu aktivieren, folgen Sie diesen Schritten im Dialog **Konfiguration Anbieter**:

1.  Wählen Sie auf der Registerkarte **Konfigurationsanbieter auswählen** im Feld **Konfigurationsanbieter** den Anbieter aus.
2.  Wählen Sie **OK** aus.

    ![Aktivieren eines Providers in Unternehmensbelegmanagement.](./media/bdm_choose_provider.png)

Der ausgewählte Anbieter wird aktiviert.

> [!NOTE]
> Jede Vorlage für die Verwaltung von Geschäftsdokumenten befindet sich in einer Konfiguration im ER-Format, die auf den Anbieter als Autor der Konfiguration verweist. Daher ist für jede Vorlage ein aktiver Anbieter erforderlich.

## <a name="edit-a-template-that-is-owned-by-another-provider"></a>Bearbeiten Sie eine Vorlage, die einem anderen Anbieter gehört

Dieses Beispiel zeigt, wie Sie die Schaltfläche **Neuer Beleg** im Arbeitsbereich **Unternehmensbelegmanagement** verwenden, um eine Vorlage in einer ER-Formatkonfiguration zu erstellen und zu bearbeiten, die von einem anderen Anbieter bereitgestellt wird und sich in der aktuellen Finance-Instanz befindet. In diesem Beispiel ist der aktive Anbieter Contoso, der die von Microsoft zur Verfügung gestellte ER-Format-Konfiguration verwendet. Nachdem Sie **Neuer Beleg** ausgewählt haben, zeigt die Registerkarte **Auswählen** auf der Seite **Eine neue Vorlage erstellen** alle Vorlagen der aktuellen Finance-Instanz an, die dem aktuellen Anbieter und anderen Anbietern gehören. Wählen Sie eine Vorlage, um sie zu öffnen. Sie können dann eine neue bearbeitbare Kopie der Vorlage erstellen. Die bearbeitete Vorlage wird in einer neuen ER-Formatkonfiguration gespeichert, die automatisch erstellt wird.

1. Wählen Sie im Arbeitsbereich **Geschäftsdokumentverwaltung** **Neues Dokument** aus.

    ![Arbeitsbereich Geschäftsdokumentenverwaltung.](./media/BDM_overview_new_template1.png)

2. Auf der Seite **Erstellen einer neuen Vorlage** wählen Sie auf der Registerkarte **Auswählen** den Beleg aus, der als Vorlage verwendet werden soll, und wählen Sie dann **Dokument erstellen**.

    ![Dialogfeld „Geschäftsdokumente“.](./media/BDM_overview_new_template2.png)

3. Ändern Sie im neuen Dialogfeld im Feld **Titel** den Titel nach Bedarf. Der Titeltext wird zum Benennen der neuen ER-Formatkonfiguration verwendet, die automatisch erstellt wird. Die Entwurfsversion dieser Konfiguration (**Debitoren-FTI-Bericht (GER) – Kopie**) enthält die bearbeitete Vorlage und wird verwendet, um dieses ER-Format für den aktuellen Benutzer auszuführen. Die ursprüngliche Vorlage von der Basis-ER-Formatkonfiguration wird verwendet, um dieses ER-Format für jeden anderen Benutzer auszuführen.
4. Ändern Sie im Feld **Name** den Namen der ersten Überarbeitung der bearbeitbaren Vorlage, die automatisch erstellt wird.
5. Aktualisieren Sie im Feld **Kommentar** die Anmerkungen für die Überarbeitung der bearbeitbaren Vorlage, die automatisch erstellt wird.
6. Wählen Sie **OK** aus, um den Beginn des Bearbeitungsprozesses zu bestätigen.

    ![Dialogfeld zur Dokumentenerstellung.](./media/BDM_overview_new_template3.png)

## <a name="upload-a-template-that-uses-an-existing-excel-workbook"></a>Eine Vorlage hochladen, die eine vorhandene Excel-Arbeitsmappe verwendet

Dieses Beispiel zeigt, wie Sie mit der Schaltfläche **Neuer Beleg** im Arbeitsbereich **Unternehmensbelegmanagement** eine Vorlage in einer ER-Formatkonfiguration erstellen und bearbeiten, die auf der verfügbaren Excel-Arbeitsmappe basiert. In diesem Beispiel ist der aktive Anbieter Contoso und Sie verwenden die Konfigurationen ER [Datenmodell](er-overview-components.md#data-model-component) und ER [Modellzuordnung](er-overview-components.md#model-mapping-component), die von Microsoft bereitgestellt werden. Nachdem Sie **Neuer Beleg** gewählt haben, wählen Sie die Registerkarte **Hochladen** auf der Seite **Erstellen einer neuen Vorlage**. Dort können Sie die Details für den Upload einer Excel-Arbeitsmappe angeben. Nachdem Sie die Excel-Arbeitsmappe hochgeladen haben, wird sie in eine Vorlage für einen Geschäftsbeleg umgewandelt, die zur Bearbeitung geöffnet wird. Die bearbeitete Vorlage wird in einer neuen ER-Formatkonfiguration gespeichert, die automatisch generiert wird.

Gehen Sie wie folgt vor, um die erforderlichen Informationen bereitzustellen, bevor Sie eine Vorlage hochladen.

1. Wählen Sie im Arbeitsbereich **Geschäftsdokumentverwaltung** **Neues Dokument** aus.
2. Wählen Sie auf der Seite **Neue Vorlage erstellen** die Registerkarte **Hochladen**, dann die Registerkarte **Vorlage** und schließlich **Durchsuchen** aus, um die Excel-Datei zu finden und auszuwählen, die Sie als Vorlage verwenden möchten. Im Abschnitt **Vorlage** werden die Felder **Titel** und **Beschreibung** automatisch ausgefüllt. Sie geben den Namen und die Beschreibung der neuen EB-Formatkonfiguration an, die automatisch erstellt wird. Sie können diese Felder bei Bedarf bearbeiten.
3. Im Abschnitt **Dokumenttyp** geben Sie im Feld **Name** den Typ des Geschäftsdokuments an. Dieser Wert wird verwendet, um die richtige Datenquelle (d. h. die EB-Modellkonfiguration) zu suchen.

    ![Registerkarte „Vorlage“ auf der Registerkarte „Upload“ der Seite „Eine neue Vorlage erstellen“.](./media/BDM_overview_new_UI_import_21.jpg)

4. Wählen Sie auf der Registerkarte **Datenquelle** das Inforegister **Filter** und dann **Filter anwenden** aus. Im Abschnitt **Datenquelle** wird das Feld **Name** automatisch ausgefüllt oder Sie können einen Wert manuell auswählen. Mit dem Filter können Sie nach der entsprechenden Datenquelle nach Name, Beschreibung, Länder-/Regionscode und Geschäftsdokumenttyp filtern.

    ![Datenquelle auf der Registerkarte Upload der Seite Eine neue Vorlage erstellen.](./media/BDM_overview_new_UI_import_31.jpg)

    > [!NOTE]
    > Das Inforegister **Filter** wird verwendet, um die richtige Datenquelle (d. h. die EB-Modellkonfiguration) zu suchen. Sie können alle Filterfelder bearbeiten, um die am besten geeignete Datenquelle für das Dokument zu finden, das Sie hochladen.
    > 
    > Die Bedingungen auf dem Inforegister **Filter** werden als **ODER**-Bedingungen verwendet.

5. Auf der Registerkarte **Zuordnung** wählen Sie **Automatische Erkennung** aus. Das Feld **Stammdefinition** wird automatisch ausgefüllt oder Sie können einen Wert manuell auswählen. Diese Registerkarte zeigt die Endzuordnung für die Elemente aus der Vorlage und dem Modell.

    ![Zuordnung auf der Registerkarte „Upload“ der Seite „Neue Vorlage erstellen“.](./media/BDM_overview_new_UI_import_41.jpg)

    > [!NOTE]
    > Die Zuordnung im Abschnitt **Vorlagenstruktur** verwendet die vollständige Übereinstimmung der Beschriftungen oder Beschreibungen in der Datenquelle in der Sprache des Benutzers und im Zellennamen in der Vorlage.

6. Wählen Sie **Dokument erstellen** aus, um zu bestätigen, dass Sie eine Vorlage erstellen und den Bearbeitungsprozess starten möchten.

Weitere Informationen finden Sie unter [Überblick über die Geschäftsdokumentverwaltung](er-business-document-management.md).

## <a name="upload-a-template-from-the-global-repository"></a>Hochladen einer Vorlage aus dem Global Repository

Dieses Beispiel zeigt, wie Sie über die Schaltfläche **Neuer Beleg** im Arbeitsbereich **Geschäftsdokumentenverwaltung** eine Vorlage in einer ER-Formatkonfiguration erstellen und bearbeiten, die von Microsoft bereitgestellt wird und sich im Global Repository befindet. In diesem Beispiel ist der aktive Anbieter Contoso, der die von Microsoft zur Verfügung gestellte ER-Format-Konfiguration verwendet. Nachdem Sie **Neues Dokument** ausgewählt haben, zeigt die Registerkarte **Importieren aus dem globalen Repository** auf der Seite **Erstellen einer neuen Vorlage** alle Vorlagen für Geschäftsdokumente an, die im globalen Repository gespeichert sind, aber in der aktuellen Finance-Instanz fehlen. Nachdem Sie eine Vorlage ausgewählt haben, wird sie aus dem globalen Repository in die aktuelle Finance-Instanz importiert, um eine neue bearbeitbare Kopie zu erstellen. Die bearbeitete Vorlage wird in einer neuen ER-Formatkonfiguration gespeichert, die automatisch erstellt wird.

1. Wählen Sie im Arbeitsbereich **Geschäftsdokumentverwaltung** **Neues Dokument** aus.
2. Wählen Sie auf der Seite **Erstellen einer neuen Vorlage** auf der Registerkarte **Import aus globalem Repository** den Beleg aus, der als Vorlage verwendet werden soll, und wählen Sie dann **Dokument erstellen**.

    ![Importieren Sie von der Registerkarte Globales Repository auf der Seite Eine neue Vorlage erstellen.](./media/BDM_overview_new_template22.png)

3. Wählen Sie im Nachrichtenfeld **Ja**, um zu bestätigen, dass Sie den ausgewählten Beleg aus dem globalen Repository in die aktuelle Finance-Instanz importieren möchten. Wenn Sie zur Autorisierung aufgefordert werden, folgen Sie den Anweisungen auf dem Bildschirm.
4. Ändern Sie im neuen Dialogfeld im Feld **Titel** den Titel nach Bedarf. Der Titeltext wird zum Benennen der neuen ER-Formatkonfiguration verwendet, die automatisch erstellt wird. Die Entwurfsversion dieser Konfiguration (**Sammlung Briefnotiz (Excel) Kopie**) enthält die bearbeitete Vorlage und wird verwendet, um dieses ER-Format für den aktuellen Benutzer auszuführen. Die ursprüngliche Vorlage von der Basis-ER-Formatkonfiguration wird verwendet, um dieses ER-Format für jeden anderen Benutzer auszuführen.
5. Ändern Sie im Feld **Name** den Namen der ersten Überarbeitung der bearbeitbaren Vorlage, die automatisch erstellt wird.
6. Aktualisieren Sie im Feld **Kommentar** die Anmerkungen für die Überarbeitung der bearbeitbaren Vorlage, die automatisch erstellt wird.
7. Wählen Sie **OK** aus, um den Beginn des Bearbeitungsprozesses zu bestätigen.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
