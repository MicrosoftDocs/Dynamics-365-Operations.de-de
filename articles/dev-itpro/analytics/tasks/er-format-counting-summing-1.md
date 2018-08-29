--- 
title: "Elektronische Berichterstellungsformate zur Zählung und Summierung erstellen"
description: "In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Format zur Inventarisierung und Summierung basierend auf der bereits generierten Textausgabe."
author: NickSelin
manager: AnnBe
ms.date: 11/02/2017
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 7261a2324b61cacfca8d69ad52762aa545b70220
ms.contentlocale: de-de
ms.lasthandoff: 08/08/2018

---
# <a name="create-electronic-reporting-er-formats-to-do-counting-and-summing"></a>Formate der elektronischen Berichterstellung (EB) zur Zählung und Summierung erstellen

[!include [task guide banner](../../includes/task-guide-banner.md)]

In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Format zur Inventarisierung und Summierung basierend auf der bereits generierten Textausgabe. Diese Schritte können in jedem Unternehmen ausgeführt werden.

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

## <a name="get-the-intrastat-configurations-provided-by-microsoft"></a>Intrastat-Konfigurationen von Microsoft erhalten
1. Klicken Sie auf "Öffnen".
2. Wählen Sie in der Strukturdarstellung "Intrastatmodel\Intrastat (DE)" aus.
3. Klicken Sie auf Import.
    * Klicken Sie auf "Importieren" für Version 1.1 der ausgewählten Konfiguration.  
4. Klicken Sie auf "Ja".
5. Schließen Sie die Seite.
6. Schließen Sie die Seite.
7. Klicken Sie auf "Berichterstellungskonfigurationen".
8. Erweitern Sie 'Intrastatmodell' in der Struktur.
9. Wählen Sie in der Strukturdarstellung "Intrastatmodel\Intrastat (DE)" aus.


