---
title: Laden Sie die elektronische Berichtskonfigurationen der Lifecycle Services herunter
description: Dieses Thema zeigt, wie Sie Konfigurationen zur elektronischen Berichterstellung (EB) von Microsoft Dynamics Lifecycle Services (LCS) herunterladen.
author: NickSelin
manager: AnnBe
ms.date: 08/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 8a18427114bddb7c72024a8d96d33f3fbf8dbe17
ms.sourcegitcommit: 9857d5cbdc0ab2fc9db049ac5ad118fc2b29bedc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/14/2020
ms.locfileid: "3810618"
---
# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a>Elektronische Berichterstellungskonfigurationen von Lifecycle Services herunterladen

[!include [banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie die neueste Version der [Konfigurationen für elektronische Berichte (EB)](general-electronic-reporting.md#Configuration) aus der [Bibliothek für freigegebene Anlagen](../lifecycle-services/asset-library.md) in den Microsoft Dynamics Lifecycle Services (LCS) herunterladen.

1. Melden Sie sich in der Anwendung an, indem Sie eine der folgenden Rollen verwenden:

    - Entwickler für elektronische Berichterstellung
    - Funktionaler Berater für elektronische Berichterstellung
    - Systemadministrator

2. Wechseln Sie zu **Organisationsverwaltung** &gt; **Arbeitsbereiche** &gt; **Elektronische Berichterstellung**.
3. Wählen Sie im Abschnitt **Konfigurationsanbieter** die Kachel **Microsoft** aus.
4. Klicken Sie auf der Kachel **Microsoft** auf **Repositorys**.

    [![Microsoft-Kachel auf der Seite für Lokalisierungskonfigurationen](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)

5. Auf der Seite **Konfigurationsrepositorys** wählen Sie im Raster ein vorhandenes Repository vom Typ **LCS** aus. Wenn dieses Repository nicht im Raster angezeigt wird, führen Sie die folgenden Schritte aus:

    1. Wählen Sie zum Hinzufügen eines Repositorys **Hinzufügen**.
    2. Aktivieren Sie **LCS** als Repository-Typ.
    3. Wählen Sie **Repository erstellen**.
    4. Wenn Sie zur Autorisierung aufgefordert werden, befolgen Sie die Anweisungen auf dem Bildschirm.
    5. Geben Sie einen Namen und eine Beschreibung für das Repository ein.
    6. Wählen Sie **OK**, um den neuen Repositoryeintrag zu bestätigen.
    7. Wählen Sie im Raster das neue Repository vom Typ **LCS** aus.

6. Wählen Sie **Öffnen**, um die Liste der ER-Konfigurationen für das ausgewählte Repository anzuzeigen.

    [![Konfigurationsrepository-Seite](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)

    > [!TIP]
    > Wenn Sie Probleme beim Zugriff auf das LCS-Repository haben, um Konfigurationen aus der Bibliothek für freigegebene Anlagen in LCS herunterzuladen, können Sie stattdessen Konfigurationen aus dem [globalen Repository](er-download-configurations-global-repo.md) herunterladen.

7. Wählen Sie in der Konfigurationsstruktur im linken Bereich die erforderliche EB-Konfiguration aus.
8. Wählen Sie im Inforegister **Versionen** die erforderliche Version der ausgewählten ER-Konfiguration aus.
9. Wählen Sie **Importieren**, um die ausgewählte Version vom LCS auf die aktuelle Instanz herunterzuladen.

    > [!NOTE]
    > Die Schaltfläche **Importieren** ist nicht für ER-Konfigurationsversionen verfügbar, die in der aktuellen Instanz bereits vorhanden sind.

    [![Konfigurationsrepository-Seite](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)

> [!NOTE]
> Abhängig von den ER-Einstellungen werden Konfigurationen überprüft, nachdem diese importiert wurden. Sie werden über alle Inkonsistenz-Probleme benachrichtigt, die ermittelt werden. Sie müssen diese Probleme beheben, bevor Sie die importierten Konfigurationsversionen verwenden können. Weitere Informationen finden Sie in der Liste der zugehörigen Themen.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Überblick über die elektronische Berichterstellung (ER)](general-electronic-reporting.md)

[Laden Sie ER-Konfigurationen aus dem globalen Repository des Konfigurationsdienstes herunter](er-download-configurations-global-repo.md)
