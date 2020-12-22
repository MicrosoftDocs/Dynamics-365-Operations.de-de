---
title: Regeln in der Konsistenzprüfung von Einzelhandelsbuchungen deaktivieren
description: Dieses Thema beschreibt die Funktionalität zum Deaktivieren der Regeln für die Konsistenzprüfung von Buchungen in Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 37209f1c1de19335f5f9fa6636ab55dd8b2fccc1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4459087"
---
# <a name="disable-rules-in-the-retail-transaction-consistency-checker"></a><span data-ttu-id="06c9a-103">Regeln in der Konsistenzprüfung von Einzelhandelsbuchungen deaktivieren</span><span class="sxs-lookup"><span data-stu-id="06c9a-103">Disable rules in the retail transaction consistency checker</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="06c9a-104">Einzelhändler können individuelle Geschäftsszenarien und -prozesse nutzen.</span><span class="sxs-lookup"><span data-stu-id="06c9a-104">Retailers can have business scenarios and processes that are unique to them.</span></span> <span data-ttu-id="06c9a-105">Daher sind nicht alle Regeln, die standardmäßig in der Konsistenzprüfung von Handelsbuchungen enthalten sind, für alle Einzelhändler anwendbar.</span><span class="sxs-lookup"><span data-stu-id="06c9a-105">Therefore, not all the rules that are included by default in the commerce transaction consistency checker are applicable to all retailers.</span></span> <span data-ttu-id="06c9a-106">Um Abweichungen auszugleichen, bietet Microsoft Dynamics 365 Commerce Funktionen, mit denen Sie die nicht anwendbaren Regeln deaktivieren können.</span><span class="sxs-lookup"><span data-stu-id="06c9a-106">To accommodate differences, Microsoft Dynamics 365 Commerce provides functionality that can be used to disable the rules that aren't applicable.</span></span>

<span data-ttu-id="06c9a-107">Um die Liste der Regeln anzuzeigen, die in der Konsistenzprüfung von Einzelhandelsbuchungen in Ihrer Umgebung verfügbar sind, und um den Status jeder Regel anzuzeigen, wechseln Sie zu **Retail und Commerce \> Zentralverwaltungseinrichtung \> Parameter \> Handelsparameter**, und wählen Sie die Registerkarte **Buchungsprüfung** aus.</span><span class="sxs-lookup"><span data-stu-id="06c9a-107">To view the list of rules that are available in the transaction consistency checker in your environment, and to see the status of each rule, go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters**, and select the **Transaction validation** tab.</span></span>

<span data-ttu-id="06c9a-108">Standardmäßig wird der Status jeder Regel auf **Aktiviert** gesetzt.</span><span class="sxs-lookup"><span data-stu-id="06c9a-108">By default, the status of every rule is set to **Enabled**.</span></span> <span data-ttu-id="06c9a-109">Daher werden alle Regeln verwendet, um Einzelhandelstransaktionen zu prüfen, bevor sie in die Handelsaufstellungen übernommen werden.</span><span class="sxs-lookup"><span data-stu-id="06c9a-109">Therefore, all the rules are used to validate transactions before they are pulled into the commerce statements.</span></span> <span data-ttu-id="06c9a-110">Um eine Regel zu deaktivieren, ändern Sie ihren Status auf **Deaktiviert**.</span><span class="sxs-lookup"><span data-stu-id="06c9a-110">To disable a rule, change its status to **Disabled**.</span></span> <span data-ttu-id="06c9a-111">Deaktivierte Regeln werden nicht berücksichtigt, wenn Transaktionen während des Aufstellungsberechnungsprozesses geprüft werden.</span><span class="sxs-lookup"><span data-stu-id="06c9a-111">Disabled rules aren't considered when transactions are validated during the statement calculation process.</span></span>

<span data-ttu-id="06c9a-112">Um den gesamten Prüfungsprozess zu umgehen, unabhängig von den aktivierten Regeln, wechseln Sie zu **Retail und Commerce \> Zentralverwaltungseinrichtung \> Parameter \> Handelsparameter**. Legen Sie dann auf der Registerkarte **Transaktionsprüfung** die Option **Konsistenzprüfung für Handelsbuchungen deaktivieren** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="06c9a-112">To bypass the whole validation process, regardless of the rules that are enabled, go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters**, and then, on the **Transaction validation** tab, set the **Disable consistency checker for Commerce transactions** option to **Yes**.</span></span> <span data-ttu-id="06c9a-113">Nachdem diese Option auf **Nein** festgelegt wurde, kann sie über die Benutzeroberfläche nicht mehr auf **Ja** zurückgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="06c9a-113">After this option is set to **No**, it can't be set back to **Yes** from the user interface (UI).</span></span>
