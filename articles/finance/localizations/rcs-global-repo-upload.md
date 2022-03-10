---
title: ER-Konfigurationen in RCS erstellen und sie in das globale Repository hochladen
description: In diesem Thema wird erläutert, wie Sie eine ER-Konfiguration (Electronic Reporting) in Microsoft Regulatory Configuration Services (RCS) erstellen und in das globale Repository hochladen.
author: JaneA07
ms.date: 01/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, RCS
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: eb04362d6d7261af56d2940b085fbc8d43c9d662
ms.sourcegitcommit: 27475081f3d2d96cf655b6afdc97be9fb719c04d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/12/2022
ms.locfileid: "7965088"
---
# <a name="create-er-configurations-in-regulatory-configuration-services-rcs-and-upload-them-to-the-global-repository"></a>ER-Konfigurationen in gesetzlichen Konfigurationsdiensten (Regulatory Configuration Services, RCS) erstellen und sie in das globale Repository hochladen

[!include [banner](../includes/banner.md)]

Mit Microsoft Regulatory Configuration Services (RCS) können Sie ER-Konfigurationen (Electronic Reporting) entwerfen und veröffentlichen, damit sie in Ihrem Unternehmen verwendet werden können.

In den folgenden Verfahren wird erläutert, wie ein Benutzer in der Rolle „Systemadministrator“ oder „Entwickler für elektronische Berichterstellung“ eine abgeleitete Version einer ER-Konfiguration erstellen kann, die in einer RCS-Instanz konfiguriert wurde, und anschließend die abgeleitete Konfiguration in das globale Repository hochlädt. 

Bevor Sie diese Prozeduren abschließen können, müssen Sie zunächst die folgende Voraussetzungen abschließen.

- Sie erlangen Zugriff auf eine RCS-Umgebung für Ihr Unternehmen.
- Sie erstellen einen aktiven Konfigurationsanbieter aktivieren ihn. Weitere Informationen finden Sie unter [Konfigurationsanbieter erstellen und als aktiv markieren](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

Sie müssen sicherstellen, dass eine RCS-Umgebung für Ihre Organisation bereitgestellt wird. Wenn Sie keine RCS-Instanz für Ihre Organisation bereitgestellt haben, können Sie dies mit den folgenden Schritten tun:

1. In der App für Finanzen und Betrieb gehen Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.
2. In **Weiterführende Links/Externe Links** wählen Sie **Regulierungsdienste – Konfiguration** und befolgen dann die Anweisungen, um zur Bereitstellung eine **Anmeldung** durchzuführen.

Wenn für Ihre Organisation bereits eine RCS-Umgebung bereitgestellt wurde, verwenden Sie die Seiten-URL, um darauf zuzugreifen und wählen die **Anmeldeoption** aus.

## <a name="create-a-derived-version-of-a-configuration-in-rcs"></a>Erstellen Sie eine abgeleitete Version einer Konfiguration in RCS

> [!NOTE]
> Wenn Sie RCS zum ersten Mal verwenden, steht Ihnen keine Konfiguration zum Ableiten zur Verfügung. Sie müssen eine Konfiguration aus dem globalen Repository importieren. Weitere Informationen finden Sie unter [Herunterladen von ER-Konfigurationen aus dem Global Repository des Konfigurationsdienstes](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

1. Führen Sie eine **Anmeldung** in RCS durch und wählen Sie den **Elektronisches Berichtswesen**-Arbeitsbereich.
2. Verifizieren Sie, dass Sie einen aktiven Konfigurationsanbieter für Ihre Organisation haben, der aktiv ist (siehe Voraussetzungen). 
3. Wählen Sie **Berichterstellungskonfigurationen** aus.
4. Wählen Sie die Konfiguration aus, von der Sie eine neue Version ableiten möchten. Sie können das Filterfeld über der Struktur verwenden, um Ihre Suche einzugrenzen.
5. Wählen Sie **Konfiguration erstellen** \> **Vom Namen ableiten**.
6. Geben Sie einen Namen und eine Beschreibung ein und wählen Sie dann **Konfiguration erstellen** aus, um eine neue abgeleitete Version mit einem Entwurfsstatus zu erstellen.
7. Wählen Sie die neu abgeleitete Konfiguration aus und nehmen Sie bei Bedarf weitere Änderungen am Konfigurationsformat vor. 
8. Nachdem Ihre Änderungen abgeschlossen sind, müssen Sie **Status ändern** festlegen, damit die Konfiguration **Abgeschlossen** werden kann, um sie im Repository veröffentlichen zu können. Wählen Sie **OK** aus.

![Neue Konfigurationsversion in RCS.](media/RCS_CompleteConfig.JPG)

> [!NOTE]
> Wenn der Konfigurationsstatus geändert wird, wird möglicherweise eine Validierungsfehlermeldung angezeigt, die sich auf die verbundenen Anwendungen bezieht. Um die Validierung zu deaktivieren, klicken Sie im Aktionsbereich auf der Registerkarte **Konfigurationen** auf **Benutzerparameter**, und setzen Sie dann **Validierung bei der Statusänderung und Neubasis der Konfiguration überspringen** auf **Ja**. 

## <a name="upload-a-configuration-to-the-global-repository"></a>Eine Konfiguration in das globale Repository hochladen

Um eine neue oder abgeleitete Konfiguration für Ihre Organisation freizugeben, können Sie sie in das globale Repository hochladen, indem Sie folgende Schritte ausführen:

1. Wählen Sie die fertige Version der Konfiguration aus und wählen Sie dann **In das Repository hochladen**.
2. Wählen Sie die Option **Global (Microsoft)** aus und dann **Hochladen**.

    ![In Repository-Optionen hochladen.](media/RCS_Upload_to_GlobalRepo_options.JPG)

3. Wählen Sie im Benachrichtigungsfeld **Ja** aus. 
4. Aktualisieren Sie die Beschreibung der Version nach Bedarf und wählen Sie dann **OK** aus. Optional können Sie die Version auch in eine verbundene Anwendung oder in ein GIT-Repository hochladen.  

Der Status der Konfiguration wird auf **Geteilt** aktualisiert, und die Konfiguration wird in das globale Repository hochgeladen. Außerdem wird eine Entwurfsversion der von Ihnen hochgeladenen Konfiguration erstellt, die bei nachträglichen Änderungen verwendet werden kann.

Nachdem die Konfiguration in das globale Repository hochgeladen wurde, können Sie dort auf folgende Weise damit arbeiten:

- Sie in die Dynamics 365-Instanz importieren Weitere Informationen finden Sie unter [Elektronische Berichterstellungskonfigurationen (ER) aus RCS importieren](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).
- Teilen Sie die Version mit Dritten oder einer externen Organisation [RCS Share Electronic Reporting (ER) -Konfigurationen mit externen Organisationen teilen](rcs-global-repo-share-configuration.md)

    ![Abgeleitete Intrastat Contoso-Konfigurationsversion im globalen Repository.](media/RCS_Config_upload_GlobalRepo.JPG)

## <a name="delete-a-configuration-from-the-global-repository"></a>Eine Konfiguration aus dem globalen Repository löschen
Führen Sie die folgenden Schritte aus, um eine von Ihrer Organisation erstellte Konfiguration zu löschen.

1. Bestätigen Sie im Arbeitsbereich **Elektronische Berichterstattung** dass Ihr Konfigurationsanbieter **Aktiv** ist. Weitere Informationen finden Sie unter [Konfigurationsanbieter erstellen und als aktiv markieren](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).
2. Wählen Sie auf Ihrem aktiven Konfigurationsanbieter **Repository**.
3. Wählen Sie den Repository-Typ **Global** und **Öffnen**.
4. Suchen Sie im Inforegister **Filter** nach der Konfiguration, die Sie löschen möchten, indem Sie die **Filter**-Funktionalität verwenden.
5. Im Inforegister **Version** wählen Sie die Version der Konfiguration aus, die Sie löschen möchten, und wählen dann **Löschen**:

    ![Konfiguration aus dem globalen Repository löschen.](media/RCS_Delete_from_GlobalRepo.JPG)

6. Wählen Sie im Benachrichtigungsfeld **Ja** aus.

    ![Bestätigungsmeldung zum Löschen der Konfigurationsversion.](media/RCS_Delete_from_GlobalRepo_Msg.JPG)
 
Die Konfigurationsversion wird gelöscht und eine Bestätigungsmeldung angezeigt. 

> [!NOTE]
> Konfigurationen können nur von dem Konfigurationsanbieter gelöscht werden, der sie erstellt hat. Wenn die Konfiguration für eine andere Organisation freigegeben wurde, muss die Freigabe der Konfiguration aufgehoben werden, bevor Sie sie löschen können.
 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
