---
title: ER-Konfigurationen in RCS/dem globalen Repository mit externen Organisationen teilen
description: In diesem Artikel wird erläutert, wie Sie eine ER-Konfiguration (Electronic Reporting) in Microsoft Regulatory Configuration Services (RCS) /im globalen Repository mit externen Organisationen teilen.
author: kfend
ms.date: 05/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.custom: 97423
ms.assetid: ''
ms.search.form: ERSolutionTable, ERWorkspace, RCS
ms.openlocfilehash: d9400ffcede9924a01391a433b570651d3f0c5e4
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284814"
---
# <a name="share-electronic-reporting-er-configurations-in-regulatory-configuration-services-rcs-global-repository-with-external-organizations"></a>ER-Konfigurationen (Electronic Reporting) in Microsoft Regulatory Configuration Services (RCS) /im globalen Repository mit externen Organisationen teilen

[!include [banner](../includes/banner.md)]

Mit Microsoft Regulatory Configuration Services (RCS) können Sie ER-Konfigurationen (Electronic Reporting) freigeben und für externe Organisationen veröffentlichen.

In den folgenden Verfahren wird erläutert, wie ein RCS-Benutzer eine Version einer ER-Konfiguration, die in einer RCS-Instanz konfiguriert wurde, für eine externe Organisation freigeben kann. Bevor Sie diese Prozeduren abschließen können, müssen Sie zunächst die folgende Voraussetzungen abschließen.

- Auf eine RCS-Instanz zugreifen.
- Einen aktiven Konfigurationsanbieter erstellen. Weitere Informationen finden Sie unter [Konfigurationsanbieter erstellen und als aktiv markieren](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).
- Erstellen Sie eine neue Version einer ER-Konfiguration und laden Sie sie hoch. Weitere Informationen finden Sie unter [Eine neue Version einer ER-Konfiguration (Electronic Reporting) erstellen und hochladen](rcs-global-repo-upload.md).

Sie müssen auch sicherstellen, dass eine RCS-Umgebung für Ihr Unternehmen bereitgestellt wird.

1. Gehen Sie in einer Finanz- und Betriebs-App zu **Verwaltung der Organisation** \> **Arbeitsbereiche** \> **Elektronisches Reporting**.
2. Wenn keine RCS-Umgebung für Ihr Unternehmen bereitgestellt wurde, klicken Sie auf **Regulatory services – externe Konfiguration** und folgen Sie den Anweisungen zur Bereitstellung einer RCS-Umgebung.

Wenn für Ihr Unternehmen bereits eine RCS-Umgebung bereitgestellt wurde, verwenden Sie die Seiten-URL, um darauf zuzugreifen, indem Sie die Anmeldeoption auswählen.

## <a name="verify-the-configuration-that-you-want-to-share"></a>Konfiguration überprüfen, die Sie freigeben möchten

Führen Sie die folgenden Schritte aus, um sicherzustellen, dass die Konfiguration, die Sie freigeben möchten, bereits in das globale Repository hochgeladen wurde.

1. Wählen Sie im Arbeitsbereich **Elektronische Berichterstattung** **Repositorys** für Ihren Konfigurationsanbieter aus.

    ![Konfigurationsanbieter.](media/1_RCS_Repo_for_config_provider.JPG)

2. Wählen Sie **Globales Repository** \> **Öffnen**.
3. Konfiguration suchen, die Sie freigeben möchten Sie können das Filterfeld verwenden, um Ihre Suche einzugrenzen. Wenn Sie die Konfiguration nicht im globalen Repository finden können, führen Sie die Schritte in [Eine neue Version einer ER-Konfiguration (Electronic Reporting) erstellen und hochladen](rcs-global-repo-upload.md) aus.

## <a name="share-er-configurations-with-external-organizations"></a>EB-Konfigurationen für externe Organisationen freigeben

Nachdem eine Konfiguration unter Ihrem Konfigurationsanbieter erstellt wurde, können Sie sie direkt für externe Organisationen über das Inforegister **Geteilt mit** auf der Seite **Globales Konfigurations-Repository** freigeben.

1. Wählen Sie im Arbeitsbereich **Elektronische Berichterstattung** **Repositorys** für Ihren Konfigurationsanbieter aus.
2. Wählen Sie **Globales Repository** \> **Öffnen**. 
3. Konfiguration auswählen, die Sie freigeben möchten
4. Wählen Sie auf dem Inforegister **Geteilt mit** eine **Organisation** aus.

    ![Inforegister „Geteilt mit“.](media/1_RCS_Repo_for_Share_with_org.JPG)

5. Geben Sie im Dialogfeld den Domänennamen für die externe Organisation ein und wählen Sie dann **OK**.

    ![Dialogfeld „Konfigurationsversion für externes Organisation freigeben“.](media/1_RCS_Repo_for_Share_with_form.JPG)

Die Konfiguration wird für die externe Organisation freigegeben und steht dieser Organisation im globalen Repository zur Verfügung. Von dort aus kann es in die RCS-Instanz des Unternehmens oder in seine Instanzen der Finanz- und Betriebs-Apps importiert werden.

6. Um die Freigabe einer Konfiguration aufzuheben, die zuvor für eine externe Organisation freigegeben wurde, wählen Sie die Konfiguration aus und klicken Sie auf **Freigabe aufheben** und dann **OK**


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
