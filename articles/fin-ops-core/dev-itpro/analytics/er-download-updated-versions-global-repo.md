---
title: Importieren von aktualisierten Versionen von EB-Konfigurationen
description: In diesem Thema wird erläutert, wie Sie aktualisierte Versionen von EB-Konfigurationen (Elektronische Berichterstellung) aus dem globalen Repository des Konfigurationsdienstes importieren.
author: NickSelin
manager: AnnBe
ms.date: 06/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 897663998c6c95ff6d7172de2abc4d4dd6ec5f12
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679509"
---
# <a name="import-updated-versions-of-er-configurations"></a>Importieren von aktualisierten Versionen von EB-Konfigurationen

[!include [banner](../includes/banner.md)]

[Repositorys](general-electronic-reporting.md#Repository) für die elektronische Berichterstattung (EB) werden verwendet, um [EB-Konfigurationen](general-electronic-reporting.md#Configuration) freizugeben. [Importieren](download-electronic-reporting-configuration-lcs.md) Sie EB-Konfigurationen aus verschiedenen Repositorys in Ihre Instanz von Microsoft Dynamics 365 Finance. Wenn Sie EB-Konfigurationen importieren, können [Konfigurationsanbieter](general-electronic-reporting.md#Provider) Repositorys mit neuen [Versionen](general-electronic-reporting.md#component-versioning) veröffentlichen, damit sie freigegeben werden können.

In diesem Thema wird erläutert, wie Sie aktualisierte Versionen von EB-Konfigurationen aus dem globalen Repository des Konfigurationsdienstes importieren. Weitere Informationen finden Sie unter [Microsoft Dynamics 365 for Finance and Operations – Regulatory services](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).

## <a name="review-the-available-updated-versions"></a>Überprüfen der verfügbaren aktualisierten Versionen

1. Melden Sie sich bei Finance an, indem Sie eine der folgenden Rollen verwenden:

    - Entwickler für elektronische Berichterstellung
    - Funktionaler Berater für elektronische Berichterstellung
    - Systemadministrator

2. Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.
3. Auf der Seite **Lokalisierungskonfigurationen** wählen Sie im Bereich **Zugehörige Links** die Option **Aktualisierte Versionen von Konfigurationen importieren** aus.

    ![Seite „Lokalisierungskonfigurationen“](./media/er-download-updated-versions-global-repo1.png)

4. Wählen Sie im Dialogfeld **Aktualisierte Versionen von elektronischen Berichtskonfigurationen importieren** im Feld **Ausführungsmodus** die Option **Nur verfügbare Updates anzeigen** aus. Wählen Sie dann **OK** aus. 

    ![Feld „Ausführungsmodus“ auf „Nur verfügbare Updates anzeigen“ eingestellt](./media/er-download-updated-versions-global-repo2.png)

5. Überprüfen Sie die Meldungen, die angezeigt werden. Diese Meldungen enthalten die folgenden Informationen zu den EB-Konfigurationen in der aktuellen Finance-Instanz und zu Unterschieden zum Inhalt des globalen Repositorys:

    - Die Gesamtzahl der EB-Konfigurationen
    - EB-Konfigurationen, die nicht im globalen Repository vorhanden sind
    - EB-Konfigurationen, für die die neueste Version bereits in der aktuellen Finance-Instanz verfügbar ist (Um die vollständige Liste dieser EB-Konfigurationen anzuzeigen, wählen Sie den Link **Meldungsdetails** aus.)

        ![Meldung „Neueste Versionen der folgenden Konfigurationen sind bereits importiert“ und Meldungsdetails](./media/er-download-updated-versions-global-repo3.png)

    - EB-Konfigurationen, für die die neueste Version im globalen Repository verfügbar ist und in die aktuelle Finance-Instanz importiert werden kann (Um die vollständige Liste dieser EB-Konfigurationen anzuzeigen, wählen Sie den Link **Meldungsdetails** aus.)

        ![Meldung „Verfügbare Updates“ und Meldungsdetails](./media/er-download-updated-versions-global-repo4.png)

## <a name="import-available-updated-versions"></a>Importieren verfügbarer aktualisierter Versionen

1. Melden Sie sich bei Finance an, indem Sie eine der folgenden Rollen verwenden:

    - Entwickler für elektronische Berichterstellung
    - Funktionaler Berater für elektronische Berichterstellung
    - Systemadministrator

2. Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.
3. Auf der Seite **Lokalisierungskonfigurationen** wählen Sie im Bereich **Zugehörige Links** die Option **Aktualisierte Versionen von Konfigurationen importieren** aus.
4. Wählen Sie im Dialogfeld **Aktualisierte Versionen von elektronischen Berichtskonfigurationen importieren** im Feld **Ausführungsmodus** die Option **Neueste Updates importieren** aus, um die neuesten Versionen von EB-Konfigurationen aus dem globalen Repository in die aktuelle Finance-Instanz zu importieren.
5. Um einen Batchauftrag für den Import zu planen, legen Sie auf dem Inforegister **Im Hintergrund ausführen** die Option **Batchverarbeitung** auf **Ja** fest. Wenn Sie den Import regelmäßig wiederholen möchten, konfigurieren Sie die erforderliche Wiederholung.

    ![Feld „Ausführungsmodus“ ist auf „Neueste Updates importieren“ festgelegt](./media/er-download-updated-versions-global-repo5.png)

6. Wählen Sie **OK**.
7. Führen Sie einen der folgenden Schritte aus, um zu erfahren, welche Konfigurationsversionen importiert wurden:

    - Wenn Sie den Import interaktiv ausführen und keinen Batchauftrag verwenden, überprüfen Sie die angezeigten Meldungen.

        ![Während einer interaktiven Importausführung eingehende Meldungen](./media/er-download-updated-versions-global-repo6.png)

    - Wenn Sie den Import im Batchmodus ausführen, gehen Sie folgendermaßen vor:

        1. Wechseln Sie zu **Allgemeines** \> **Anfragen** \> **Batchaufträge** \> **Meine Batchaufträge**.
        2. Suchen Sie den Auftrag **Aktualisierte Versionen von elektronischen Berichtskonfigurationen importieren** und wählen Sie ihn aus. Wählen Sie dann im Aktivitätsbereich auf der Registerkarte **Batchauftrag** die Option **Batchauftrag-Historie** aus, um die Historie des Auftrags anzuzeigen.
        3. Wählen Sie auf der Seite **Batchauftrag-Historie** die Option **Protokoll** aus. Wählen Sie dann in der angezeigten Meldung den Link **Meldungsdetails** aus, um das Auftragsprotokoll anzuzeigen.

        ![Auftragsprotokoll](./media/er-download-updated-versions-global-repo7.png)

> [!IMPORTANT]
> Es wird nicht empfohlen, einen sich wiederholenden Batchauftrag zu planen, um aktualisierte Versionen von EB-Konfigurationen direkt aus dem globalen Repository in eine Produktionsumgebung zu importieren, da die importierten Versionen sofort zur Verwendung verfügbar sind. Verwenden Sie diesen Ansatz stattdessen, um Versionen von EB-Konfigurationen in einer Sandbox-Umgebung bereitzustellen. Sie können dann vor der Bereitstellung in einer Produktionsumgebung in der Sandbox-Umgebung ausgewertet werden.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Überblick über die elektronische Berichterstellung (ER)](general-electronic-reporting.md)
- [Laden Sie ER-Konfigurationen aus dem globalen Repository des Konfigurationsdienstes herunter](er-download-configurations-global-repo.md)
