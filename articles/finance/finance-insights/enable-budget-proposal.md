---
title: Budgetvorschläge aktivieren (Vorschau)
description: In diesem Thema wird erläutert, wie Sie die Funktion „Budgetvorschlag“ in Finance Insights aktivieren.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 59cf40e8bf69734c5f3645997ff0b07c29d4f40e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995139"
---
# <a name="enable-budget-proposals-preview"></a>Budgetvorschläge aktivieren (Vorschau)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

In diesem Thema wird erläutert, wie Sie die Funktion „Budgetvorschlag“ in Finance Insights aktivieren.

1. Verwenden Sie Informationen von der Umgebungsseite in Microsoft Dynamics Lifecycle Services (LCS), um eine Verbindung mit der primären Instanz von Azure-SQL für diese Umgebung herzustellen. Führen Sie den folgenden Transact-SQL-Befehl (T-SQL) aus, um Flights für die Sandboxumgebung zu aktivieren. (Möglicherweise müssen Sie den Zugriff für Ihre IP-Adresse in LCS aktivieren, bevor Sie eine Remoteverbindung mit Application Object Server \[AOS\] herstellen können.)

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BudgetIntelligentBudgetRegisterProposalFeature', 1)`

    > [!NOTE]
    > Wenn es sich bei Ihrer Bereitstellung von Microsoft Dynamics 365 Finance um eine Service Fabric-Bereitstellung handelt, können Sie diesen Schritt überspringen. Das Finance Insights-Team sollte das Flight bereits für Sie aktiviert haben. Wenn Sie die Funktion im **Funktionsverwaltung**-Arbeitsbereich nicht sehen oder wenn beim Versuch, ihn einzuschalten, Probleme auftreten, senden Sie eine E-Mail an das [Finance Insights App Preview-Team](mailto:fiap@microsoft.com).

2. Öffnen Sie den **Funktionsverwaltung**-Arbeitsbereich, und befolgen Sie diese Schritte:

    1. Wählen Sie **Nach Updates suchen**.
    2. Suchen Sie nach **Budgetvorschlag** und aktivieren Sie diese Funktion.

3. Gehen Sie zu **Budgetierung \> Einrichten \> Grundlegende Budgetierung \> Budgetvorschlag (Vorschau)** und wählen Sie **Funktion aktivieren**.

#### <a name="privacy-notice"></a>Datenschutzhinweis
Vorschauen (1) wenden möglicherweise weniger Datenschutz- und Sicherheitsmaßnahmen an als der Dynamics 365 Finance and Operations-Dienst, (2) sind nicht in der Service Level Agreement (SLA) für diesen Dienst enthalten, (3) sollten nicht zur Verarbeitung personenbezogener Daten oder anderer Daten verwendet werden, die gesetzlichen oder behördlichen Compliance-Anforderungen unterliegen, und (4) hat begrenzten Support.