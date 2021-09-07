---
title: Budgetvorschläge aktivieren
description: In diesem Thema wird erläutert, wie Sie die Funktion „Budgetvorschlag“ in Finance Insights aktivieren.
author: ShivamPandey-msft
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: ab65d1b0e366bfe6bdb07688f89d440662165063
ms.sourcegitcommit: 822aea26c5da259efe11ff3b3dc4cf1598425689
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/16/2021
ms.locfileid: "7386485"
---
# <a name="enable-budget-proposals"></a>Budgetvorschläge aktivieren

[!include [banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie die Funktion „Budgetvorschlag“ in Finance Insights aktivieren.

1. Verwenden Sie Informationen von der Umgebungsseite in Microsoft Dynamics Lifecycle Services (LCS), um eine Verbindung mit der primären Instanz von Azure-SQL für diese Umgebung herzustellen. Führen Sie den folgenden Transact-SQL-Befehl (T-SQL) aus, um Flights für die Sandboxumgebung zu aktivieren. (Möglicherweise müssen Sie den Zugriff für Ihre IP-Adresse in LCS aktivieren, bevor Sie eine Remoteverbindung mit Application Object Server \[AOS\] herstellen können.)

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BudgetIntelligentBudgetRegisterProposalFeature', 1)`

    > [!NOTE]
    > Überspringen Sie diesen Schritt, wenn Sie Version 10.0.20 oder höher verwenden oder wenn Sie eine Service Fabric-Bereitstellung verwenden. Das Finance Insights-Team sollte das Flight bereits für Sie aktiviert haben. Wenn die Funktion nicht im **Funktionsverwaltung**-Arbeitsbereich angezeigt wird, oder wenn Sie Probleme beim Aktivieren haben, wenden Sie sich an <fiap@microsoft.com>.

2. Öffnen Sie den **Funktionsverwaltung**-Arbeitsbereich, und befolgen Sie diese Schritte:

    1. Wählen Sie **Nach Updates suchen**.
    2. Suchen Sie nach **Budgetvorschlag** und aktivieren Sie diese Funktion.

3. Gehen Sie zu **Budgetierung \> Einrichten \> Grundlegende Budgetierung \> Budgetvorschlag (Vorschau)** und wählen Sie **Funktion aktivieren**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
