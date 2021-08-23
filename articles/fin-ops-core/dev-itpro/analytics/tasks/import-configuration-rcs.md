---
title: (ER) Konfigurationen aus RCS importieren
description: Dieses Thema enthält Informationen dazu, wie ein Benutzer eine neue Version einer ER-Konfiguration von RCS importieren kann.
author: NickSelin
ms.date: 07/03/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f5674c418baaac7817c27780e2f0137ce6e7137eb3f1665f768ad843cc5b3114
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6720783"
---
# <a name="er-import-configurations-from-rcs"></a>(ER) Konfigurationen aus RCS importieren

[!include [banner](../../includes/banner.md)]

In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Systemadministratorrolle oder der Rolle „Entwickler für elektronische Berichterstellung“ eine neue Konfiguration für „Elektronische Berichterstellung (ER)“ erstellen kann und sie nach Microsoft Regulatory Configuration Services (RCS) hochladen kann. In diesem Beispiel können Sie die Version der ER-Konfiguration, die in einer RCS-Instanz konfiguriert wurde, auswählen und in die aktuelle Instanz importieren, z. B. Unternehmen, Litware, Inc. Diese Schritte können in jedem Unternehmen durchgeführt werden, da ER-Konfigurationen unter Unternehmen freigegeben werden. Um diese Schritte auszuführen, müssen Sie zunächst die Schritte im Thema [Konfigurationsanbieter erstellen und als aktiv markieren](er-configuration-provider-mark-it-active-2016-11.md) abschließen. Um diese Schritte auszuführen, müssen Sie über Zugriff auf eine RCS-Instanz verfügen, die mindestens eine ER-Konfiguration enthält, entweder im **Abgeschlossen** oder Status **Gemeinsam genutzt** enthält.

1. Wechseln Sie zu **Organisationsverwaltung**  >  **Arbeitsbereiche**  >  **Elektronische Berichterstellung**. 
2. Überprüfen Sie, dass der Konfigurationsanbieter für Beispielunternehmen „Litware, Inc.” verfügbar und als **Aktiv** markiert ist. Wenn Sie diesen Konfigurationsanbieter nicht sehen, führen Sie die Schritte im Thema [Konfigurationsanbieter anlegen aus und markieren Sie ihn als aktiv](er-configuration-provider-mark-it-active-2016-11.md). 
3. Wenn Sie keine RCS-Umgebung haben, die beim Unternehmen bereitgestellt wurde, wählen Sie den externen Link **Regulatory services – Konfiguration** aus und folgen Sie den Anweisungen zur Bereitstellung einer RCS-Umgebung. 
4. Wählen Sie **Parameter für elektronische Berichterstellung** aus. 
5. Wählen Sie die Registerkarte **RCS** aus. 
6. Wenn die RCS-Umgebung bereits beim Unternehmen bereitgestellt worden ist, können Sie auf der Seite dargestellte URLs verwenden, um sie anzuzeigen. 
7. Schließen Sie die Seite. 

## <a name="register-a-new-er-repository"></a>Registrieren Sie ein neues ER-Repository. 
1. Markieren Sie in der Liste die ausgewählte Zeile. 
2. Anbieter Litware, Inc. auswählen. 
3. Wählen Sie Repositorys aus. 
4. Wählen Sie Hinzufügen, um das Dropdown-Dialogfeld zu öffnen. 
5. Wählen Sie im Feld "Konfigurationsrepository-Typ" die Option "RCS" aus. 
6. Wählen Sie Repository erstellen. 
7. Geben Sie im Namensfeld „RCS-Umgebungsanzeige“ einen Wert ein, oder wählen Sie einen Wert aus. 
8. Wählen Sie die gewünschte RCS-Instanz aus. Sie können mehrere hiervon haben. 
9. Wählen Sie OK. 

## <a name="import-er-configurations-from-rcs-based-repository"></a>Importieren von EB-Konfigurationen aus dem RCS-basierten Respository
1. Wählen Sie **Filter anzeigen** aus. 
2. Verwenden Sie den Filteroperator **beginnt mit**, um im Feld **Name** den Filterwert „RCS“ einzugeben. 
3. Wenn Sie das ausgewählte Repository öffnen, wählen Sie auf der Seite **Mit Regulatory Configuration Services verbinden** den Link **Hier auswählen, um eine Verbindung mit Regulatory Configuration Services herzustellen** aus. 
4. Wählen Sie **Öffnen**. 
5. Wählen Sie **Schließen** aus. 
6. Wählen Sie die gewünschte Version der EB-Konfiguration aus und wählen Sie dann **Importieren** aus, um sie in die aktuelle Instanz einzubringen.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]