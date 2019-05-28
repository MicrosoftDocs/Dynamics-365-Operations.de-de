---
title: Laden Sie die elektronische Berichtskonfigurationen der Lifecycle Services herunter
description: Dieses Thema zeigt, wie Sie Konfigurationen zur elektronischen Berichterstellung (EB) von Microsoft Dynamics Lifecycle Services (LCS) herunterladen.
author: NickSelin
manager: AnnBe
ms.date: 06/20/2017
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
ms.openlocfilehash: 8686d2639a3ab7f2e79944cc5eed51571d463261
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550421"
---
# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a>Elektronische Berichterstellungskonfigurationen von Lifecycle Services herunterladen

[!include [banner](../includes/banner.md)]

Dieses Thema zeigt, wie Sie Konfigurationen zur elektronischen Berichterstellung (EB) von Microsoft Dynamics Lifecycle Services (LCS) herunterladen.

Dieses Lernprogramm erläutert das Herunterladen der aktuellen Version der Konfigurationen zur elektronischen Berichterstellung (EB) von Microsoft Dynamics Lifecycle Services (LCS).

1. Melden Sie sich für Finance and Operations an, indem Sie eine der folgenden Rollen verwenden:

    - Entwickler für elektronische Berichterstellung
    - Funktionaler Berater für elektronische Berichterstellung
    - Systemadministrator

2. Wechseln Sie zu **Organisationsverwaltung**&gt; **Elektronische Berichterstellung**..
3. Wählen Sie im Abschnitt **Konfigurationsanbieter** die Kachel **Microsoft** aus.
4. Klicken Sie auf der Kachel **Microsoft** auf **Repositorys**.

    [![Aktualisieren von ER über LCS für MS - MS Repositorys-Liste öffnen](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)

5. Auf der Seite **Konfigurationsrepositorys** wählen Sie im Raster ein vorhandenes Repository vom Typ **LCS** aus. Wenn dieses Repository nicht im Raster angezeigt wird, führen Sie die folgenden Schritte aus:

    1. Klicken Sie zum Hinzufügen neuer Repository auf **Hinzufügen**.
    2. Aktivieren Sie **LCS** als Repository-Typ.
    3. Klicken Sie auf **Repository erstellen**.
    4. Wenn Sie aufgefordert werden, folgen Sie den Autorisierungsanweisungen.
    5. Geben Sie einen Namen und eine Beschreibung für das Repository ein.
    6. Klicken Sie auf **OK**, um den neuen Repositoryeintrag zu bestätigen.
    7. Wählen Sie im Raster das neue Repository vom Typ **LCS** aus.

6. Klicken Sie auf **Öffnen**, um die Liste der ER-Konfigurationen für das ausgewählte Repository anzuzeigen.

    [![update-er-from-lcs-for-ms-make-lcs-repository](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)

7. Wählen Sie in der Konfigurationsstruktur im linken Bereich die ER-Konfiguration aus, die Sie benötigen.
8. Wählen Sie im Inforegister **Versionen** die erforderliche Version der ausgewählten ER-Konfiguration aus.
9. Klicken Sie auf **Importieren**, um die ausgewählte Version vom LCS auf die aktuelle Finance and Operations Instanz herunterzuladen.

    > [!NOTE]
    > Die Schaltfläche **Importieren** ist nicht für ER-Konfigurationsversionen verfügbar, die in der aktuellen Finance and Operations-Instanz bereits vorhanden sind.

    [![update-er-from-lcs-for-ms-download-configuration](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)

> [!NOTE]
> Abhängig von den ER-Einstellungen werden Konfigurationen überprüft, nachdem diese importiert wurden. Sie werden über alle Inkonsistenz-Probleme benachrichtigt, die ermittelt werden. Sie müssen diese Probleme beheben, bevor Sie die importierten Konfigurationsversionen verwenden können. Weitere Informationen finden Sie in der Liste der zugehörigen Artikel.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Überblick über die elektronische Berichterstellung](general-electronic-reporting.md)
