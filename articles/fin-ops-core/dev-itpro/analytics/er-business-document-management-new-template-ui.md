---
title: Microsoft Office-Benutzeroberfläche in der Verwaltung von Belegen in Unternehmen (enthält Video)
description: Dieses Thema erklärt, wie die neue Benutzeroberfläche in der Geschäftsdokumentverwaltung-Funktion des Frameworks für elektronische Berichterstellung (EB) verwendet wird.
author: v-anamir
ms.date: 04/12/2021
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
ms.openlocfilehash: b0c481e73daf74803d3582e4089e76dcd383e8a4
ms.sourcegitcommit: ef0dd4245fc499907ffe00e2a32f59a6cd96e45d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/18/2021
ms.locfileid: "7937555"
---
# <a name="microsoft-office-style-user-interface-in-business-document-management"></a>Benutzeroberfläche im Stil von Microsoft Office für Dokumente in der Geschäftsdokumentverwaltung

[!include [banner](../includes/banner.md)]

Mit der Geschäftsdokumentverwaltung können geschäftliche Benutzer Geschäftsdokumentvorlagen mit einem Microsoft 365-Dienst oder der entsprechenden Microsoft Office-Desktopanwendung bearbeiten. Bearbeitungen können Entwurfsänderungen oder neue Bereitstellungen umfassen. Benutzer können auch Platzhalter hinzufügen, um zusätzliche Daten aufzunehmen, ohne den Quellcode ändern zu müssen. Weitere Informationen zum Arbeiten mit der Geschäftsdokumentenverwaltung finden Sie unter [Überblick über die Geschäftsdokumentverwaltung](er-business-document-management.md).

Die neue Benutzeroberfläche ist übersichtlicher und benutzerfreundlicher. Der **Geschäftsdokument**-Bereich zeigt nur die Vorlagen, die für den aktuellen Anbieter verfügbar sind. In der vorherigen Benutzeroberfläche wurden auf der Registerkarte **Vorlage** alle Vorlagen aufgelistet, die für Anbieter verfügbar waren. Außerdem wurden alle Vorlagen angezeigt, die von Benutzern mit derselben Rolle erstellt und bearbeitet wurden.

Sie können die Schaltfläche **Neues Dokument** verwenden, um eine Vorlage in einer Formatkonfiguration der elektronischen Berichtserstellung (EB) zu erstellen und zu bearbeiten, die von einem anderen Anbieter bereitgestellt wird. Im Beispiel dieses Themas ist der Anbieter Microsoft. Alternativ können Sie eine Vorlage erstellen, indem Sie Ihre eigene Vorlage im Excel-Format hochladen.


> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RWAVQg]

Das Video zum Thema [ein neues Geschäftsdokument mit der Geschäftsdokumentverwaltung erstellen](https://youtu.be/gAIYl-mM_pw) (siehe oben) ist in der [Finance and Operations-Wiedergabeliste](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) YouTube verfügbar.

## <a name="make-the-new-document-ui-in-business-document-management-available"></a>Neue Benutzeroberfläche für die Geschäftsdokumentverwaltung zur Verfügung stellen

Um die neue Dokument-Benutzeroberfläche in der Geschäftsdokumentverwaltung zu verwenden, müssen Sie die Funktion **Office-ähnliche UI-Erfahrung für Geschäftsdokumentverwaltung** im Arbeitsbereich **Funktionsverwaltung** aktivieren.

Befolgen Sie diese Schritte, um diese Funktion für alle juristischen Personen zu aktivieren.

1. Wählen Sie im Arbeitsbereich **Funktionsverwaltung** auf der Registerkarte **Alle** die Funktion **Office-ähnliche UI-Erfahrung für Geschäftsdokumentverwaltung** aus der Liste aus.
2. Wählen Sie **Jetzt aktivieren** aus, um die ausgewählte Fähigkeit zu aktivieren.
3. Aktualisieren Sie die Seite, um auf die neue Funktion zugreifen können.

## <a name="edit-templates-that-are-owned-by-other-providers"></a>Vorlagen anderer Anbieter bearbeiten

1. Wählen Sie im Arbeitsbereich **Geschäftsdokumentverwaltung** **Neues Dokument** aus.

    ![Arbeitsbereich Geschäftsdokumentenverwaltung.](./media/BDM_overview_new_template1.png)

2. Wählen Sie in der Registerkarte **Auswählen** das Dokument aus, das als Vorlage verwendet werden soll, und wählen Sie **Dokument erstellen** aus.

    ![Dialogfeld „Geschäftsdokumente“.](./media/BDM_overview_new_template2.png)

3. Ändern Sie im neuen Dialogfeld im Feld **Titel** den Titel nach Bedarf. Der Titeltext wird zum Benennen der neuen ER-Formatkonfiguration verwendet, die automatisch erstellt wird. Die Entwurfsversion dieser Konfiguration (**Debitoren-FTI-Bericht (GER) – Kopie**) enthält die bearbeitete Vorlage und wird verwendet, um dieses ER-Format für den aktuellen Benutzer auszuführen. Die ursprüngliche Vorlage von der Basis-ER-Formatkonfiguration wird verwendet, um dieses ER-Format für jeden anderen Benutzer auszuführen.
4. Ändern Sie im Feld **Name** den Namen der ersten Überarbeitung der bearbeitbaren Vorlage, die automatisch erstellt wird.
5. Aktualisieren Sie im Feld **Kommentar** die Anmerkungen für die Überarbeitung der bearbeitbaren Vorlage, die automatisch erstellt wird.
6. Wählen Sie **OK** aus, um den Beginn des Bearbeitungsprozesses zu bestätigen.

    ![Dialogfeld zur Dokumentenerstellung.](./media/BDM_overview_new_template3.png)

Die Schaltfläche **Neues Dokument** wird verwendet, um eine Vorlage in einer ER-Formatkonfiguration zu erstellen und zu bearbeiten, die von einem anderen Anbieter bereitgestellt wird. In diesem Beispiel ist der Anbieter Microsoft. Wenn Sie auf **Neues Dokument** klicken, sehen Sie alle Vorlagen, die sich im Besitz aktueller und anderer Anbieter befinden. Nachdem Sie die Vorlage ausgewählt haben, wird sie zur Bearbeitung geöffnet. Die bearbeitete Vorlage wird dann in einer neuen ER-Formatkonfiguration gespeichert, die automatisch generiert wird.

## <a name="upload-a-template-that-uses-an-existing-excel-format"></a>Eine Vorlage hochladen, die ein vorhandenes Excel-Format verwendet
Gehen Sie wie folgt vor, um die erforderlichen Informationen bereitzustellen, bevor Sie eine Vorlage hochladen.

1. Wählen Sie im Arbeitsbereich **Geschäftsdokumentverwaltung** **Neues Dokument** aus.

    ![Arbeitsbereich Geschäftsdokumentenverwaltung.](./media/BDM_overview_new_template1.png)
    
2. Wählen Sie auf der Seite **Neue Vorlage erstellen** die Registerkarte **Hochladen**, dann die Registerkarte **Vorlage** und schließlich **Durchsuchen** aus, um die Excel-Datei zu finden und auszuwählen, die Sie als Vorlage verwenden möchten. Im Abschnitt **Vorlage** werden die Felder **Titel** und **Beschreibung** automatisch ausgefüllt. Sie geben den Namen und die Beschreibung der neuen EB-Formatkonfiguration an, die automatisch erstellt wird. Sie können diese Felder bei Bedarf bearbeiten.
3. Im Abschnitt **Dokumenttyp** geben Sie im Feld **Name** den Typ des Geschäftsdokuments an. Dieser Wert wird verwendet, um die richtige Datenquelle (d. h. die EB-Modellkonfiguration) zu suchen.

    ![Registerkarte „Vorlage“.](./media/BDM_overview_new_UI_import_21.jpg)

4. Wählen Sie auf der Registerkarte **Datenquelle** das Inforegister **Filter** und dann **Filter anwenden** aus. Im Abschnitt **Datenquelle** wird das Feld **Name** automatisch ausgefüllt oder Sie können einen Wert manuell auswählen. Mit dem Filter können Sie nach der entsprechenden Datenquelle nach Name, Beschreibung, Länder-/Regionscode und Geschäftsdokumenttyp filtern.

    ![Registerkarte „Datenquelle“.](./media/BDM_overview_new_UI_import_31.jpg)
    
    > [!NOTE]
    > Das Inforegister **Filter** wird verwendet, um die richtige Datenquelle (d. h. die EB-Modellkonfiguration) zu suchen. Sie können alle Filterfelder bearbeiten, um die am besten geeignete Datenquelle für das Dokument zu finden, das Sie hochladen.
    > 
    > Die Bedingungen auf dem Inforegister **Filter** werden als **ODER**-Bedingungen verwendet.
    
5. Auf der Registerkarte **Zuordnung** wählen Sie **Automatische Erkennung** aus. Das Feld **Stammdefinition** wird automatisch ausgefüllt oder Sie können einen Wert manuell auswählen. Diese Registerkarte zeigt die Endzuordnung für die Elemente aus der Vorlage und dem Modell.

    ![Registerkarte „Zuordnung“.](./media/BDM_overview_new_UI_import_41.jpg)
    
   > [!NOTE]
   > Die Zuordnung im Abschnitt **Vorlagenstruktur** verwendet die vollständige Übereinstimmung der Beschriftungen oder Beschreibungen in der Datenquelle in der Sprache des Benutzers und im Zellennamen in der Vorlage.

6. Wählen Sie **Dokument erstellen** aus, um zu bestätigen, dass Sie eine Vorlage erstellen und den Bearbeitungsprozess starten möchten.

Weitere Informationen finden Sie unter [Überblick über die Geschäftsdokumentverwaltung](er-business-document-management.md).

Wenn es in der elektronischen Berichterstellung keinen Anbieter gibt, können Sie einen erstellen. Wenn es keinen aktiven Anbieter gibt, können Sie einen aktivieren.

- Um einen Anbieter zu erstellen, ändern Sie den Namen des Anbieters im Feld **Name**, aktualisieren Sie die Internetadresse des neuen Anbieters im Feld **Internetadresse** und bestätigen Sie mit **OK**.

    ![Einen neuen Anbieter in BDM erstellen.](./media/bdm_create_provider.png)
    
- Um einen vorhandenen Anbieter zu aktivieren, wählen Sie den Namen des Anbieters im Feld **Konfigurationsanbieter** aus und aktivieren Sie den Anbieter dann mit **OK**.

    ![Einen Anbieter in BDM aktivieren.](./media/bdm_choose_provider.png)

> [!NOTE]
> Jede BDM-Vorlage verweist auf den Anbieter als Autor der Konfiguration. Aus diesem Grund ist für die Vorlage ein aktiver Anbieter erforderlich.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
