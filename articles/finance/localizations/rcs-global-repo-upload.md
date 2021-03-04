---
title: ER-Konfigurationen in RCS erstellen und sie in das globale Repository hochladen
description: In diesem Thema wird erläutert, wie Sie eine ER-Konfiguration (Electronic Reporting) in Microsoft Regulatory Configuration Services (RCS) erstellen und in das globale Repository hochladen.
author: JaneA07
manager: AnnBe
ms.date: 09/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, RCS
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 5b2b8f35b9931f8fd1824c20e9045da68af33ad5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4443634"
---
# <a name="create-er-configurations-in-regulatory-configuration-services-rcs-and-upload-them-to-the-global-repository"></a>ER-Konfigurationen in gesetzlichen Konfigurationsdiensten (Regulatory Configuration Services, RCS) erstellen und sie in das globale Repository hochladen

[!include [banner](../includes/banner.md)]

Mit Microsoft Regulatory Configuration Services (RCS) können Sie ER-Konfigurationen (Electronic Reporting) entwerfen und veröffentlichen, damit sie in Ihrem Unternehmen verwendet werden können.

In den folgenden Verfahren wird erläutert, wie ein Benutzer in der Rolle „Systemadministrator“ oder „Entwickler für elektronische Berichterstellung“ eine abgeleitete Version einer ER-Konfiguration erstellen kann, die in einer RCS-Instanz konfiguriert wurde, und anschließend die abgeleitete Konfiguration in das globale Repository hochlädt. 

Bevor Sie diese Prozeduren abschließen können, müssen Sie zunächst die folgende Voraussetzungen abschließen.

- Auf eine RCS-Instanz zugreifen.
- Einen aktiven Konfigurationsanbieter erstellen. Weitere Informationen finden Sie unter [Konfigurationsanbieter erstellen und als aktiv markieren](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

Sie müssen auch sicherstellen, dass eine RCS-Umgebung für Ihr Unternehmen bereitgestellt wird.

1. Wechseln Sie in der Finance and Operations-App zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.
2. Wenn keine RCS-Umgebung für Ihr Unternehmen bereitgestellt wurde, klicken Sie auf **Regulatory services – externe Konfiguration** und folgen Sie den Anweisungen zur Bereitstellung einer RCS-Umgebung.

Wenn für Ihr Unternehmen bereits eine RCS-Umgebung bereitgestellt wurde, verwenden Sie die Seiten-URL, um darauf zuzugreifen, indem Sie die Anmeldeoption auswählen.

## <a name="create-a-derived-version-of-a-configuration-in-rcs"></a>Erstellen Sie eine abgeleitete Version einer Konfiguration in RCS

1. Stellen Sie im Arbeitsbereich **Elektronische Berichterstattung** sicher, dass Sie einen aktiven Konfigurationsanbieter für Ihre Organisation haben. 
2. Wählen Sie **Berichterstellungskonfigurationen** aus.
3. Wählen Sie die Konfiguration aus, von der Sie eine neue Version ableiten möchten. Sie können das Filterfeld über der Struktur verwenden, um Ihre Suche einzugrenzen.
4. Wählen Sie **Konfiguration erstellen** \> **Vom Namen ableiten**.
5. Geben Sie einen Namen und eine Beschreibung ein und wählen Sie dann **Konfiguration erstellen** aus, um eine neue abgeleitete Version zu erstellen.
6. Wählen Sie die neu abgeleitete Konfiguration aus, fügen Sie eine Beschreibung der Version hinzu, und wählen Sie dann **OK** aus. Der Status der Konfiguration in wird in **Abgeschlossen** geändert.

![Neue Konfigurationsversion in RCS](media/RCS_CompleteConfig.JPG)

> [!NOTE]
> Wenn der Konfigurationsstatus geändert wird, wird möglicherweise eine Validierungsfehlermeldung angezeigt, die sich auf die verbundenen Anwendungen bezieht. Um die Validierung zu deaktivieren, klicken Sie im Aktionsbereich auf der Registerkarte **Konfigurationen** auf **Benutzerparameter**, und setzen Sie dann **Validierung bei der Statusänderung und Neubasis der Konfiguration überspringen** auf **Ja**. 

## <a name="upload-a-configuration-to-the-global-repository"></a>Eine Konfiguration in das globale Repository hochladen

Um eine neue oder abgeleitete Konfiguration für Ihre Organisation freizugeben, können Sie sie in das globale Repository hochladen.

1. Wählen Sie die fertige Version der Konfiguration aus und wählen Sie dann **In das Repository hochladen**.
2. Wählen Sie die Option **Global (Microsoft)** aus und dann **Hochladen**.

    ![In Repository-Optionen hochladen](media/RCS_Upload_to_GlobalRepo_options.JPG)

3. Wählen Sie im Benachrichtigungsfeld **Ja** aus. 
4. Aktualisieren Sie die Beschreibung der Version nach Bedarf und wählen Sie dann **OK** aus. 

Der Status der Konfiguration wird auf **Teilen** aktualisiert, und die Konfiguration wird in das globale Repository hochgeladen. Hier können Sie damit auf folgende Arten arbeiten:

- Sie in die Dynamics 365-Instanz importieren Weitere Informationen finden Sie unter [Elektronische Berichterstellungskonfigurationen (ER) aus RCS importieren](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).
- Teilen Sie die Version mit Dritten oder einer externen Organisation [RCS Share Electronic Reporting (ER) -Konfigurationen mit externen Organisationen teilen](rcs-global-repo-share-configuration.md)

    ![Abgeleitete Intrastat Contoso-Konfigurationsversion im globalen Repository](media/RCS_Config_upload_GlobalRepo.JPG)

## <a name="delete-a-configuration-from-the-global-repository"></a>Eine Konfiguration aus dem globalen Repository löschen
Führen Sie die folgenden Schritte aus, um eine von Ihrer Organisation erstellte Konfiguration zu löschen.

1. Bestätigen Sie im Arbeitsbereich **Elektronische Berichterstattung** dass Ihr Konfigurationsanbieter **Aktiv** ist. Weitere Informationen finden Sie unter [Konfigurationsanbieter erstellen und als aktiv markieren](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).
2. Wählen Sie auf Ihrem aktiven Konfigurationsanbieter **Repository**.
3. Wählen Sie den Repository-Typ **Global** und **Öffnen**.
4. Suchen Sie im Inforegister **Filter** nach der Konfiguration, die Sie löschen möchten, indem Sie die **Filter**-Funktionalität verwenden.
5. Im Inforegister **Version** wählen Sie die Version der Konfiguration aus, die Sie löschen möchten, und wählen dann **Löschen**:

    ![Konfiguration aus dem globalen Repository löschen](media/RCS_Delete_from_GlobalRepo.JPG)

6. Wählen Sie im Benachrichtigungsfeld **Ja** aus.

    ![Bestätigungsmeldung zum Löschen der Konfigurationsversion](media/RCS_Delete_from_GlobalRepo_Msg.JPG)
 
Die Konfigurationsversion wird gelöscht und eine Bestätigungsmeldung angezeigt. 

> [!NOTE]
> Konfigurationen können nur von dem Konfigurationsanbieter gelöscht werden, der sie erstellt hat. Wenn die Konfiguration für eine andere Organisation freigegeben wurde, muss die Freigabe der Konfiguration aufgehoben werden, bevor Sie sie löschen können.
 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]