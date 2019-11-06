---
title: Regeln in der Konsistenzprüfung von Einzelhandelsbuchungen deaktivieren
description: Dieses Thema beschreibt die Funktionalität zum Deaktivieren der Regeln für die Konsistenzprüfung von Einzelhandelsbuchungen in Microsoft Dynamics 365 Retail.
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4bf8df2fb9f8f5c33ceb13eb012fb6879f81ec66
ms.sourcegitcommit: bdbca89bd9b328c282ebfb681f75b8f1ed96e7a8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/14/2019
ms.locfileid: "2586296"
---
# <a name="disable-rules-in-the-retail-transaction-consistency-checker"></a><span data-ttu-id="e8e8e-103">Regeln in der Konsistenzprüfung von Einzelhandelsbuchungen deaktivieren</span><span class="sxs-lookup"><span data-stu-id="e8e8e-103">Disable rules in the retail transaction consistency checker</span></span> 

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="e8e8e-104">Einzelhändler können individuelle Geschäftsszenarien und -prozesse nutzen.</span><span class="sxs-lookup"><span data-stu-id="e8e8e-104">Retailers can have business scenarios and processes that are unique to them.</span></span> <span data-ttu-id="e8e8e-105">Daher sind nicht alle Regeln, die standardmäßig in der Konsistenzprüfung von Einzelhandelsbuchungen enthalten sind, für alle Einzelhändler anwendbar.</span><span class="sxs-lookup"><span data-stu-id="e8e8e-105">Therefore, not all the rules that are included by default in the retail transaction consistency checker are applicable to all retailers.</span></span> <span data-ttu-id="e8e8e-106">Um Abweichungen auszugleichen, bietet Microsoft Dynamics 365 Retail Funktionen, mit denen Sie die nicht anwendbaren Regeln deaktivieren können.</span><span class="sxs-lookup"><span data-stu-id="e8e8e-106">To accommodate differences, Microsoft Dynamics 365 Retail provides functionality that can be used to disable the rules that aren't applicable.</span></span>

<span data-ttu-id="e8e8e-107">Um die Liste der Regeln anzuzeigen, die in der Konsistenzprüfung von Einzelhandelsbuchungen in Ihrer Umgebung verfügbar sind, und um den Status jeder Regel anzuzeigen, wechseln Sie zu **Retail \> Zentralverwaltungseinrichtung \> Parameter \> Einzelhandelsparameter** und wählen Sie die Registerkarte **Buchungsprüfung** aus.</span><span class="sxs-lookup"><span data-stu-id="e8e8e-107">To view the list of rules that are available in the retail transaction consistency checker in your environment, and to see the status of each rule, go to **Retail \> Headquarters setup \> Parameters \> Retail parameters**, and select the **Transaction validation** tab.</span></span>

<span data-ttu-id="e8e8e-108">Standardmäßig wird der Status jeder Regel auf **Aktiviert** gesetzt.</span><span class="sxs-lookup"><span data-stu-id="e8e8e-108">By default, the status of every rule is set to **Enabled**.</span></span> <span data-ttu-id="e8e8e-109">Daher werden alle Regeln verwendet, um Einzelhandelstransaktionen zu prüfen, bevor sie in die Einzelhandelsaufstellungen übernommen werden.</span><span class="sxs-lookup"><span data-stu-id="e8e8e-109">Therefore, all the rules are used to validate retail transactions before they are pulled into the retail statements.</span></span> <span data-ttu-id="e8e8e-110">Um eine Regel zu deaktivieren, ändern Sie ihren Status auf **Deaktiviert**.</span><span class="sxs-lookup"><span data-stu-id="e8e8e-110">To disable a rule, change its status to **Disabled**.</span></span> <span data-ttu-id="e8e8e-111">Deaktivierte Regeln werden nicht berücksichtigt, wenn Einzelhandelstransaktionen während des Aufstellungsberechnungsprozesses geprüft werden.</span><span class="sxs-lookup"><span data-stu-id="e8e8e-111">Disabled rules aren't considered when retail transactions are validated during the statement calculation process.</span></span>

<span data-ttu-id="e8e8e-112">Um den gesamten Prüfungsprozess zu umgehen, unabhängig von den aktivierten Regeln, wechseln Sie zu **Retail \> Zentralverwaltungseinrichtung \> Parameter \> Einzelhandelsparameter**. Legen Sie dann auf der Registerkarte **Transaktionsprüfung** die Option **Konsistenzprüfung für Einzelhandelsbuchungen deaktivieren** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="e8e8e-112">To bypass the whole validation process, regardless of the rules that are enabled, go to **Retail \> Headquarters setup \> Parameters \> Retail parameters**, and then, on the **Transaction validation** tab, set the **Disable consistency checker for Retail transactions** option to **Yes**.</span></span> <span data-ttu-id="e8e8e-113">Nachdem diese Option auf **Nein** festgelegt wurde, kann sie über die Benutzeroberfläche nicht mehr auf **Ja** zurückgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="e8e8e-113">After this option is set to **No**, it can't be set back to **Yes** from the user interface (UI).</span></span>
