---
title: Laden Sie ER-Konfigurationen aus dem globalen Repository des Konfigurationsdienstes herunter
description: In diesem Artikel wird erläutert, wie Sie EB-Konfigurationen (Elektronische Berichterstellung) aus dem globalen Repository des Konfigurationsdienstes herunterladen.
author: NickSelin
ms.date: 06/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace, ERSolutionRepositoryTable
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 53007504f1094b69ec6578d382c451a2bf1f9059
ms.sourcegitcommit: 3289478a05040910f356baf1995ce0523d347368
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2022
ms.locfileid: "9108917"
---
# <a name="download-er-configurations-from-the-global-repository-of-configuration-service"></a>Laden Sie ER-Konfigurationen aus dem globalen Repository des Konfigurationsdienstes herunter

[!include [banner](../includes/banner.md)]

In diesem Artikel wird erläutert, wie Sie [EB-Konfigurationen (Elektronische Berichterstellung)](general-electronic-reporting.md#Configuration) aus dem globalen Repository des Konfigurationsdienstes herunterladen. Weitere Informationen finden Sie unter [Microsoft Dynamics 365 Finance – Regulatory Services, Konfigurationsdienst](/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).

## <a name="open-configurations-repository"></a>Konfigurations-Repository öffnen

1. Melden Sie sich in der Anwendung Dynamics 365 Finance an, indem Sie eine der folgenden Rollen verwenden:

    - Entwickler für elektronische Berichterstellung
    - Funktionaler Berater für elektronische Berichterstellung
    - Systemadministrator

2. Wechseln Sie zu **Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung**.
3. Wählen Sie im Abschnitt **Konfigurationsanbieter** die Kachel **Microsoft** aus.
3. Klicken Sie auf der Kachel **Microsoft** auf **Repositorys**.

    ![Elektronische Berichterstellung – Arbeitsbereich.](./media/er-download-configurations-global-repo-er-workspace.png)

4. Auf der Seite **Konfigurationsrepositorys** wählen Sie im Raster ein vorhandenes Repository vom Typ **Global** aus. Wenn dieses Repository nicht im Raster angezeigt wird, führen Sie die folgenden Schritte aus:

    1. Wählen Sie zum Hinzufügen neuer Repository **Hinzufügen**.
    2. Wählen Sie **Global** als Repository-Typ, und wählen Sie dann **Repository erstellen**.
    3. Wenn Sie aufgefordert werden, folgen Sie den Autorisierungsanweisungen.
    4. Geben Sie einen Namen und eine Beschreibung für das Repository ein und wählen Sie dann **OK**, um den neuen Repository-Eintrag zu bestätigen.
    5. Wählen Sie im Raster das neue Repository vom Typ **Global** aus.

5. Wählen Sie **Öffnen**, um die Liste der ER-Konfigurationen für das ausgewählte Repository anzuzeigen.

    ![Konfigurationsrepository-Seite.](./media/er-download-configurations-global-repo-repositories-list.png)

## <a name="import-a-single-configuration"></a>Einzelne Konfiguration importieren

1. Auf der Seite **Konfigurations-Repositorys** wählen Sie auf der Seite im Konfigurationsbaum die gewünschte ER-Konfiguration aus.
2. Wählen Sie im Inforegister **Versionen** die erforderliche Version der ausgewählten ER-Konfiguration aus.
3. Wählen Sie **Importieren**, um die ausgewählte Version vom globalen Repository auf die aktuelle Finance and Operations Instanz herunterzuladen.

    > [!NOTE]
    > Die Schaltfläche **Importieren** ist nicht für ER-Konfigurationsversionen verfügbar, die in der aktuellen Instanz bereits vorhanden sind.

    ![Seite „Konfigurations-Repository“, Inforegister „Konfigurationen“.](./media/er-download-configurations-global-repo-repository-content.png)

## <a name="import-filtered-configurations"></a>Importierte Konfigurationen filtern

1. Auf der Seite **Konfigurations-Repositorys** erweitern Sie im Konfigurationsbaum die Seite **Filter** Infiregister.
2. In dem Raster **Stichworte** fügen Sie alle benötigten Tags hinzu.
3. In dem Feld **Anwendbarkeit des Landes/der Region** wählen Sie in diesem Feld die entsprechenden Länder-/Regionalcodes aus und wählen Sie dann **Filter anwenden**.

    > [!NOTE]
    > Das Inforegister **Konfigurationen** zeigt alle Konfigurationen an, die die angegebenen Auswahlbedingungen erfüllen.

4. Auf dem Inforegister **Konfigurationen** wählen Sie **Importieren**, um die gefilterten Konfigurationen aus dem globalen Repository auf die aktuelle Instanz herunterzuladen.
5. Im Inforegister **Konfigurationen** wählen Sie **Filter zurücksetzen**, um die angegebenen Auswahlbedingungen zu bereinigen.

    ![Seite „Konfigurations-Repository“, Inforegister „Versionen“, Schaltfläche „Importieren“.](./media/er-download-configurations-global-repo-filtered-configurations.png)

> [!NOTE]
> Abhängig von den ER-Einstellungen werden Konfigurationen überprüft, nachdem diese importiert wurden. Sie werden über alle Inkonsistenz-Probleme benachrichtigt, die ermittelt werden. Sie müssen diese Probleme beheben, bevor Sie die importierten Konfigurationsversionen verwenden können. Weitere Informationen finden Sie in der Liste der zugehörigen Ressourcen.

> [!NOTE]
> ER-Konfigurationen können so konfiguriert werden, dass sie von anderen Konfigurationen abhängig sind. Daher werden möglicherweise zusammen mit einer ausgewählten Konfiguration andere Konfigurationen automatisch importiert. Weitere Informationen zu Konfigurationsabhängigkeiten finden Sie unter [Definieren Sie die Abhängigkeit von ER-Konfigurationen von anderen Komponenten](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Überblick über die elektronische Berichterstellung (ER)](general-electronic-reporting.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

