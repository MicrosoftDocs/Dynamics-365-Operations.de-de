--- 
title: Datenmodell zur Verwendung der Dokumentverwaltungsdateien in Formatausgaben vorbereiten
description: "In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Format zur Nutzung von Dokumentverwaltungsdateien (Anhänge) in ER-Berichten nutzen kann."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 9f99259056fab2d56d1ccf7487681c183551c64f
ms.contentlocale: de-de
ms.lasthandoff: 04/13/2018

---
# <a name="prepare-data-model-to-use-document-management-files-in-format-outputs"></a>Datenmodell zur Verwendung der Dokumentverwaltungsdateien in Formatausgaben vorbereiten

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Format zur Nutzung von Dokumentverwaltungsdateien (Anhänge) in ER-Berichten nutzen kann. Diese Schritte können in jedem Unternehmen ausgeführt werden.

Um diese Schritte auszuführen, müssen Sie zunächst die Schritte unter "Konfigurationsanbieter erstellen und als aktiv markieren" abschließen.

Diese Prozedur ist eine Funktion, die in Dynamics 365 for Operations, Version 1611 hinzugefügt wurde.


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a>Zugriff auf die Liste von Microsoft bereitgestellte von den Konfigurationen erhalten
1. Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.
    * Überprüfen Sie, ob "Litware, Inc." Anbieter ist verfügbar und markiert als aktiv.  
2. Wählen Sie den "Litware, Inc."- Anbieter.
3. Klicken Sie auf Repositorys.
    * Wenn ein Repository des Typs "Operations-Ressourcen" vorhanden ist, überspringen Sie die übrigen Schritte der aktuellen Unteraufgabe.  
4. Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".
5. Geben Sie im Feld "Konfigurationsrepository-Typ" die Bezeichnung "Betriebliche Ressourcen" ein.
6. Klicken Sie auf "Repository erstellen".
7. Klicken Sie auf "OK".

## <a name="get-the-customer-invoice-model-configurations-provided-by-microsoft"></a>Die Debitorenrechnungsmodell-Konfigurationen von Microsoft abrufen
1. Klicken Sie auf "Filter anzeigen".
2. Wenden Sie die nachfolgenden Filter an: Geben Sie den Filterwert "Operations-Ressourcen" im Feld " Name" ein, indem Sie den "beginnt mit"-Filteroperator verewnden; Geben Sie den Filterwert "" im Feld "Beschreibungs" ein, indem Sie den "beginnt mit"-Filteroperator verwenden.
3. Klicken Sie auf "Filter anzeigen".
4. Klicken Sie auf "Öffnen".
5. Wählen Sie in der Strukturdarstellung "Debitorenrechnungsmodell " aus.
    * Wählen Sie die Modellkonfiguration "Debitorenrechnungsmodell" aus, um sie zu importieren.  
6. Klicken Sie auf Import.
    * Klicken Sie auf "Importieren" für Version 1 der ausgewählten Konfiguration.  
7. Klicken Sie auf "Ja".
8. Schließen Sie die Seite.
9. Schließen Sie die Seite.
10. Klicken Sie auf "Berichterstellungskonfigurationen".
11. Wählen Sie in der Strukturdarstellung "Debitorenrechnungsmodell " aus.

## <a name="create-the-derived-model-to-support-access-to-the-document-management-files"></a>Erstellen Sie das abgeleitete Modell, um den Zugriff auf die Dokumentverwaltungsdateien zu unterstützen.
    * Sie erstellen eine eigene Konfiguration des Debitorenrechnungmodells, die von der Konfiguration von Microsoft abgeleitet ist. Sie verwenden diese Konfiguration, um den Zugriff auf die Dokumentverwaltungsdateien zu implementieren und diese für elektronische Dokumente bereitzustellen, die Sie auf Basis dieses Modell erstellen.  
1. Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.
2. Geben Sie im Feld "Neu" "Von Name 'Debitorenrechnungsmodell Microsoft' abgeleitet" ein.
3. Geben Sie im Feld "Name" "Debitorenrechnungsmodell (benutzerdefiniert)" ein.
    * Debitorenrechnungsmodell (benutzerdefiniert)  
4. Klicken Sie auf Konfiguration erstellen.


