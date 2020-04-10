---
title: ER Import einer Konfiguration von Lifecycle Services
description: In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Systemadministratorrolle oder der Rolle "Entwickler für elektronische Berichterstellung" eine neue Konfiguration für "Elektronische Berichterstellung (ER)" erstellen kann und sie nach Microsoft Lifecycle Services (LCS) hochladen kann.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable,  ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 67e09e3187ac49e12727116f55066b64a386e2de
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142385"
---
# <a name="er-import-a-configuration-from-lifecycle-services"></a>ER Import einer Konfiguration von Lifecycle Services

[!include [banner](../../includes/banner.md)]

In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Systemadministratorrolle oder der Rolle "Entwickler für elektronische Berichterstellung" eine neue Konfiguration für "Elektronische Berichterstellung (ER)" erstellen kann und sie nach Microsoft Lifecycle Services (LCS) hochladen kann.

In diesem Beispiel wählen Sie die gewünschte Version der ER-Konfiguration und importieren das Beispielunternehmen, Litware, Inc. Diese Schritte können in einem beliebigen Unternehmen ausgeführt werden, da ER-Konfigurationsanbieter unter allen Unternehmen geteilt werden. Um diese Schritte abzuschließen, müssen Sie zunächst die Schritte in der Prozedur „Eine ER-Konfiguration nach Lifecycle Services hochladen“ abschließen. Zugriff auf LCS ist auch für den Abschluss dieser Schritte erforderlich.

1. Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.
2. Klicken Sie auf "Konfigurationen".

## <a name="delete-a-shared-version-of-data-model-configuration"></a>Löschen Sie eine freigegebene Version der Datenmodellkonfiguration
1. Wählen Sie "Beispielmodellkonfiguration" in der Struktur aus.
    * Die erste Version einer Beispieldaten-Modellkonfiguration wurde erstellt und nach LCS veröffentlicht während der Prozedur „Hochladen einer ER-Konfiguration nach Lifecycle Services“. In dieser Prozedur löschen Sie diese Version der ER-Konfiguration. Diese Version einer Beispieldatmodellkonfiguration wird später von LCS importiert.  
2. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Wählen Sie die Version dieser Konfiguration aus, die sich im Status „Freigegeben“ befindet. Dieser Status gibt an, dass die Konfiguration nach LCS veröffentlicht wurde.  
3. Klicken Sie auf "Status ändern".
4. Klicken Sie auf "Nicht fortsetzen".
    * Ändern Sie den Status der ausgewählten Version von „Freigegeben“ zu „Nicht mehr verfügbar“, um sie zur Löschung bereitzustellen.  
5. Klicken Sie auf "OK".
6. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Wählen Sie die Version dieser Konfiguration aus, die den Status „Nicht mehr verfügbar“ hat.  
7. Klicken Sie auf Löschen.
8. Klicken Sie auf „Ja“.
    * Beachten Sie, dass die einzige Entwurfsversion 2 der ausgewählten Datenmodellkonfiguration verfügbar ist.  
9. Schließen Sie die Seite.

## <a name="import-a-shared-version-of-data-model-configuration-from-lcs"></a>Importieren Sie eine freigegebene Version der Datenmodellkonfiguration von LCS
1. Markieren Sie in der Liste die ausgewählte Zeile.
    * Öffnen Sie die Liste von Repositorys für den Konfigurationsanbieter „Litware, Inc.“ zu öffnen Konfigurationsanbieter.  
2. Klicken Sie auf Repositorys.
3. Klicken Sie auf "Öffnen".
    * Wählen Sie das LCS-Repository aus und öffnen Sie es.  
4. Markieren Sie in der Liste die ausgewählte Zeile.
    * Wählen Sie die erste Version der "Beispielmodellkonfiguration" in der Versionsliste aus.  
5. Klicken Sie auf Import.
6. Klicken Sie auf "Ja".
    * Bestätigen Sie den Import der ausgewählten Version von LCS.  
    * Beachten Sie, dass die Informationsmeldung (über dem Formular) den erfolgreichen Abschluss des Importvorgangs der ausgewählten Version bestätigt.  
7. Schließen Sie die Seite.
8. Schließen Sie die Seite.
9. Klicken Sie auf "Konfigurationen".
10. Wählen Sie "Beispielmodellkonfiguration" in der Struktur aus.
11. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Wählen Sie die Version dieser Konfiguration aus, die den Status „Freigegeben“ hat.  
    * Beachten Sie, dass die freigegebene Version 1 der ausgewählten Datenmodellkonfiguration jetzt verfügbar ist.  

