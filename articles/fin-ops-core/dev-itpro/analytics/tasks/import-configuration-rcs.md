---
title: (ER) Konfigurationen aus RCS importieren
description: Dieses Thema enthält Informationen dazu, wie ein Benutzer eine neue Version einer ER-Konfiguration von RCS importieren kann.
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 55d548a97a2f93bffeb5aa4b0ce6b0c4ca5f8819
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769831"
---
# <a name="er-import-configurations-from-rcs"></a>(ER) Konfigurationen aus RCS importieren

[!include [task guide banner](../../includes/task-guide-banner.md)]

In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Systemadministratorrolle oder der Rolle „Entwickler für elektronische Berichterstellung“ eine neue Konfiguration für „Elektronische Berichterstellung (ER)“ erstellen kann und sie nach Microsoft Regulatory Configuration Services (RCS) hochladen kann. In diesem Beispiel können Sie die Version der ER-Konfiguration, die in einer RCS-Instanz konfiguriert wurde, auswählen und in die aktuelle Instanz importieren, z. B. Unternehmen, Litware, Inc. Diese Schritte können in jedem Unternehmen durchgeführt werden, da ER-Konfigurationen unter Unternehmen freigegeben werden. Um diese Schritte auszuführen, müssen Sie zunächst die Schritte im Thema [Konfigurationsanbieter erstellen und als aktiv markieren](er-configuration-provider-mark-it-active-2016-11.md) abschließen. Um diese Schritte auszuführen, müssen Sie über Zugriff auf eine RCS-Instanz verfügen, die mindestens eine ER-Konfiguration enthält, entweder im **Abgeschlossen** oder Status **Gemeinsam genutzt** enthält.

1. Wechseln Sie zu **Organisationsverwaltung**  >  **Arbeitsbereiche**  >  **Elektronische Berichterstellung**. 
2. Überprüfen Sie, dass der Konfigurationsanbieter für Beispielunternehmen „Litware, Inc.” verfügbar und als **Aktiv** markiert ist. Wenn Sie diesen Konfigurationsanbieter nicht sehen, führen Sie die Schritte im Thema [Konfigurationsanbieter anlegen aus und markieren Sie ihn als aktiv](er-configuration-provider-mark-it-active-2016-11.md). 
3. Wenn Sie keine RCS-Umgebung haben, die beim Unternehmen bereitgestellt wurde, klicken Sie auf den externen Link **Regulatory services – Konfiguration** und folgen Sie den Anweisungen zur Bereitstellung einer RCS-Umgebung. 
4. Klicken Sie auf **Parameter für elektronische Berichterstellung**. 
5. Klicken Sie auf die Registerkarte **RCS**. 
6. Wenn die RCS-Umgebung bereits beim Unternehmen bereitgestellt worden ist, können Sie auf der Seite dargestellte URLs verwenden, um sie anzuzeigen. 
7. Schließen Sie die Seite. 

## <a name="register-a-new-er-repository"></a>Registrieren Sie ein neues ER-Repository. 
1. Markieren Sie in der Liste die ausgewählte Zeile. 
2. Anbieter Litware, Inc. auswählen. 
3. Klicken Sie auf Repositorys. 
4. Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen". 
5. Wählen Sie im Feld "Konfigurationsrepository-Typ" die Option "RCS" aus. 
6. Klicken Sie auf "Repository erstellen". 
7. Geben Sie im Namensfeld „RCS-Umgebungsanzeige“ einen Wert ein, oder wählen Sie einen Wert aus. 
8. Wählen Sie die gewünschte RCS-Instanz aus. Beachten Sie, dass Sie mehrere hiervon haben können. 
9. Klicken Sie auf "OK". 

## <a name="import-er-configurations-from-rcs-based-repository"></a>Importieren von ER-Konfigurationen aus dem RCS-basierten Respository
1. Klicken Sie auf **Filter anzeigen.** 
2. Verwenden Sie den Filteroperator **beginnt mit**, um im Feld **Name** den Filterwert „RCS“ einzugeben. 
3. Wenn Sie das ausgewählte Repository öffnen, klicken Sie auf der Seite **Mit Regulatory Configuration Services verbinden** auf den Link **Hier klicken, um eine Verbindung mit Regulatory Configuration Services herzustellen**. 
4. Klicken Sie auf **Öffnen**. 
5. Klicken Sie auf **Schließen**. 
6. Wählen Sie die gewünschte Version der ER-Konfiguration aus und klicken Sie auf **Importieren**, um sie in die aktuelle Instanz einzubringen.

