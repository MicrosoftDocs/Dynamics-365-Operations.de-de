---
title: Neue Benutzeroberfläche für Dokumente in der Geschäftsdokumentenverwaltung
description: Dieses Thema enthält Informationen zur Verwendung der neuen Benutzeroberfläche in der Geschäftsdokumentverwaltung-Funktion des Frameworks für elektronische Berichterstellung (ER).
author: v-anamir
manager: AnnBe
ms.date: 05/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-anamir
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4acde9703c721ab7c20d1603299a10dda91b23c4
ms.sourcegitcommit: b8f8ccab2cd9d848e5ecd71caaf0a63237e2236b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2020
ms.locfileid: "2957062"
---
# <a name="new-document-user-interface-in-business-document-management"></a>Neue Benutzeroberfläche für Dokumente in der Geschäftsdokumentenverwaltung

[!include [banner](../includes/banner.md)]

Mit der Geschäftsdokumentverwaltung können geschäftliche Benutzer Geschäftsdokumentvorlagen mit einem Microsoft Office 365-Dienst oder der entsprechenden Microsoft Office-Desktopanwendung bearbeiten. Bearbeitungen können Entwurfsänderungen oder neue Bereitstellungen umfassen. Benutzer können auch Platzhalter hinzufügen, um zusätzliche Daten aufzunehmen, ohne den Quellcode ändern zu müssen. Weitere Informationen zum Arbeiten mit der Geschäftsdokumentenverwaltung finden Sie unter [Überblick über die Geschäftsdokumentverwaltung](er-business-document-management.md).

Die neue Benutzeroberfläche für Dokumente ist übersichtlicher und benutzerfreundlicher. Der **Geschäftsdokument**-Bereich zeigt nur die Vorlagen, die für den aktuellen Anbieter verfügbar sind.

Mit der Schaltfläche **Neues Dokument** können Benutzer eine Vorlage in einer ER-Formatkonfiguration bearbeiten, die von einem anderen Anbieter bereitgestellt wird. Im Beispiel dieses Themas ist der Anbieter Microsoft.

## <a name="make-the-new-document-ui-in-business-document-management-available"></a>Neue Benutzeroberfläche für die Geschäftsdokumentverwaltung zur Verfügung stellen

Um die neue Dokument-Benutzeroberfläche in der Geschäftsdokumentverwaltung zu verwenden, müssen Sie die Funktion **Office-ähnliche UI-Erfahrung für Geschäftsdokumentverwaltung** im Arbeitsbereich **Funktionsverwaltung** aktivieren.

Befolgen Sie diese Schritte, um diese Funktion für alle juristischen Personen zu aktivieren.

1. Wählen Sie im Arbeitsbereich **Funktionsverwaltung** auf der Registerkarte **Neu** die Funktion **Office-ähnliche UI-Erfahrung für Geschäftsdokumentverwaltung** aus der Liste aus.
2. Wählen Sie **Jetzt aktivieren** aus, um die ausgewählte Fähigkeit zu aktivieren.
3. Aktualisieren Sie die Seite, um auf die neue Funktion zugreifen können.

### <a name="edit-templates-that-are-owned-by-other-providers"></a>Vorlagen anderer Anbieter bearbeiten

1. Wählen Sie im Arbeitsbereich **Geschäftsdokumentverwaltung** **Neues Dokument** aus.

    ![Arbeitsbereich Geschäftsdokumentenverwaltung](./media/BDM_overview_new_template1.png)

2. Wählen Sie im Dialogfeld das Dokument aus, das als Vorlage verwendet werden soll, und wählen Sie **Dokument erstellen** aus.

    ![Dialogfeld „Geschäftsdokumente“](./media/BDM_overview_new_template2.png)

3. Ändern Sie im neuen Dialogfeld im Feld **Titel** den Titel nach Bedarf. Der Titeltext wird zum Benennen der neuen ER-Formatkonfiguration verwendet, die automatisch erstellt wird. Die Entwurfsversion dieser Konfiguration (**Debitoren-FTI-Bericht (GER) – Kopie**) enthält die bearbeitete Vorlage und wird verwendet, um dieses ER-Format für den aktuellen Benutzer auszuführen. Die ursprüngliche Vorlage von der Basis-ER-Formatkonfiguration wird verwendet, um dieses ER-Format für jeden anderen Benutzer auszuführen.
4. Ändern Sie im Feld **Name** den Namen der ersten Überarbeitung der bearbeitbaren Vorlage, die automatisch erstellt wird.
5. Aktualisieren Sie im Feld **Kommentar** die Anmerkungen für die Überarbeitung der bearbeitbaren Vorlage, die automatisch erstellt wird.
6. Wählen Sie **OK** aus, um den Beginn des Bearbeitungsprozesses zu bestätigen.

    ![Dialogfeld zur Dokumentenerstellung](./media/BDM_overview_new_template3.png)

Die Schaltfläche **Neues Dokument** wird verwendet, um eine Vorlage in einer ER-Formatkonfiguration zu erstellen und zu bearbeiten, die von einem anderen Anbieter bereitgestellt wird. In diesem Beispiel ist der Anbieter Microsoft. Wenn Sie auf **Neues Dokument** klicken, sehen Sie alle Vorlagen, die sich im Besitz aktueller und anderer Anbieter befinden. Nachdem Sie die Vorlage ausgewählt haben, wird sie zur Bearbeitung geöffnet. Die bearbeitete Vorlage wird dann in einer neuen ER-Formatkonfiguration gespeichert, die automatisch generiert wird.

Weitere Informationen finden Sie unter [Überblick über die Geschäftsdokumentverwaltung](er-business-document-management.md).
