--- 
title: "Hochladen einer Konfiguration nach Lifecycle Services für elektronische Berichterstellung (ER)"
description: "In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Systemadministratorrolle oder der Rolle \"Entwickler für elektronische Berichterstellung\" eine neue Konfiguration für \"Elektronische Berichterstellung (ER)\" erstellen kann und sie nach Microsoft Lifecycle Services (LCS) hochladen kann."
author: NickSelin
manager: AnnBe
ms.date: 05/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 3d9c2192bac8477e9c9376aab3e3b561da777569
ms.contentlocale: de-de
ms.lasthandoff: 03/26/2018

---
# <a name="upload-a-configuration-into-lifecycle-services-for-electronic-reporting-er"></a>Hochladen einer Konfiguration nach Lifecycle Services für elektronische Berichterstellung (ER)

[!include [task guide banner](../../includes/task-guide-banner.md)]

In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Systemadministratorrolle oder der Rolle "Entwickler für elektronische Berichterstellung" eine neue Konfiguration für "Elektronische Berichterstellung (ER)" erstellen kann und sie nach Microsoft Lifecycle Services (LCS) hochladen kann.

In diesem Beispiel erstellen Sie eine Konfiguration für das Beispielunternehmen, Litware, Inc. und laden Sie in LCS hoch. Diese Schritte können in einem beliebigen Unternehmen ausgeführt werden, da ER-Konfigurationen unter Unternehmen geteilt werden. Um diese Schritte auszuführen, müssen Sie zunächst die Schritte unter "Konfigurationsanbieter erstellen und als aktiv markieren" abschließen. Zugriff auf LCS ist auch für den Abschluss dieser Schritte erforderlich.

1. Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.
2. Wählen Sie „Litware, inc.” aus un lege es als aktiv fest.
3. Klicken Sie auf "Konfigurationen".

## <a name="create-a-new-data-model-configuration"></a>Neue Datenmodellkonfiguration erstellen
1. Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.
    * Sie erstellen eine Konfiguration, die ein Beispieldatenmodell für elektronische Dokumente enthält. Diese Datenmodellkonfiguration wird später in LCS hochgeladen.  
2. Geben Sie im Feld "Name" die Bezeichnung "Beispielmodellkonfiguration" ein.
    * Beispielmodellkonfiguration  
3. Geben Sie im Feld "Beschreibung" die Bezeichnung "Beispielmodellkonfiguration" ein.
    * Beispielmodellkonfiguration  
4. Klicken Sie auf Konfiguration erstellen.
5. Klicken Sie auf "Modelldesigner".
6. Klicken Sie auf "Neu".
7. Geben Sie im Feld "Name" die Bezeichnung "Eingangspunkt" ein.
    * Einstiegspunkt  
8. Klicken Sie auf Hinzufügen.
9. Klicken Sie auf "Speichern".
10. Schließen Sie die Seite.
11. Klicken Sie auf "Status ändern".
12. Klicken Sie auf "Abgeschlossen".
13. Klicken Sie auf "OK".

## <a name="register-a-new--repository"></a>Registrieren Sie ein neues Repository
1. Schließen Sie die Seite.
2. Klicken Sie auf Repositorys.
    * Dies ermöglicht Ihnen, die Liste der Repositorys für Litware, Inc. als Konfigurationsanbieter zu öffnen.  
3. Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".
    * Dies ermöglicht Ihnen, ein neues Repository hinzuzufügen.  
4. Wählen Sie im Feld "Konfigurationsrepository-Typ" die Option "LCS" aus.
5. Klicken Sie auf "Repository erstellen".
6. Geben Sie im Feld "Projekt" einen Wert ein, oder wählen Sie einen Wert aus.
    * Wählen Sie das gewünschte LCS-Projekt aus. Sie müssen Zugriff auf das Projekt besitzen.  
7. Klicken Sie auf "OK".
    * Schließen Sie einen neuen Repositoryeintrag ab.  
8. Markieren Sie in der Liste die ausgewählte Zeile.
    * Wählen Sie den LCS-Repository-Datensatz aus.  
    * Beachten Sie, dass ein registriertes Repository durch den aktuellen Anbieter markiert ist. Das bedeutet, dass nur Varianten, die diesem Anbieter gehören, zu diesem Repository platziert und folglich in das ausgewählte LCS-Projekt hochgeladen werden können.  
9. Klicken Sie auf "Öffnen".
    * Öffnen Sie das Repository, um die Liste der ER-Konfigurationen anzuzeigen. Es ist leer, wenn dieses Projekt noch nicht zum Freigeben von ER-Konfigurationen verwendet wurde.  
10. Schließen Sie die Seite.
11. Schließen Sie die Seite.

## <a name="upload-configuration-into-lcs"></a>Laden Sie Konfiguration in LCS hoch
1. Klicken Sie auf "Konfigurationen".
2. Wählen Sie "Beispielmodellkonfiguration" in der Struktur aus.
    * Wählen Sie eine erstellte Konfiguration aus, die bereits abgeschlossen wurden.  
3. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Wählen Sie die Version der ausgewählten Konfiguration mit dem Status "Abgeschlossen" aus.  
4. Klicken Sie auf "Status ändern".
5. Klicken Sie auf "Freigeben".
    * Der Konfigurationsstatus ändert sich von "Abgeschlossen" zu "Freigegeben", wenn er in LCS veröffentlicht wird.  
6. Klicken Sie auf "OK".
7. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Wählen Sie die Konfigurationsversion mit dem Status "Freigegeben" aus.  
    * Beachten Sie, dass sich der Status der ausgewählten Version von "Abgeschlossen" zu "Freigegeben" geändert hat.  
8. Schließen Sie die Seite.
9. Klicken Sie auf Repositorys.
    * Dies ermöglicht Ihnen, die Liste der Repositorys für Litware, Inc. als Konfigurationsanbieter zu öffnen.  
10. Klicken Sie auf "Öffnen".
    * Wählen Sie das LCS-Repository aus und öffnen Sie es.  
    * Beachten Sie, dass die ausgewählte Variante als Anlage des ausgewählten LCS-Projekts angezeigt wird.  
    * Öffnen Sie LSC mithilfe von https://lcs.dynamics.com. Öffnen Sie ein Projekt, das zuvor für Repositoryregistrierung verwendet wurde, öffnen Sie die Anlagenbibliothek dieses Projekts und erweitern Sie den Inhalt des Anlagentyps "GER-Konfiguration" – die hochgeladene ER-Konfiguration wird verfügbar sein. Beachten Sie, dass die hochgeladene LCS-Konfiguratio in eine andere Microsoft Dynamics 365 for Finance and Operations-Instanz importiert werden kann, wenn Anbieter Zugriff auf dieses LCS-Projekt haben.  


