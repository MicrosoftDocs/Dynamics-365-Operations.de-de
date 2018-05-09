--- 
title: "Konfigurationsanbieter erstellen und als aktiv für elektronische Berichterstellung (ER) markieren"
description: "In den folgenden Schritten wird erläutert, wie ein Benutzer, der der Systemadministratorrolle oder der Rolle \"Entwickler für elektronische Berichterstellung\" zugewiesen ist, einen Konfigurationsanbieter für elektronische Berichterstellung (ER) erstellen kann."
author: NickSelin
manager: AnnBe
ms.date: 11/01/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 8392e789f546e32a00736c02eccf47d00893cc8b
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-configuration-provider-and-mark-it-as-active-for-electronic-reporting-er"></a><span data-ttu-id="eb5c2-103">Konfigurationsanbieter erstellen und als aktiv für elektronische Berichterstellung (ER) markieren</span><span class="sxs-lookup"><span data-stu-id="eb5c2-103">Create a configuration provider and mark it as active for electronic reporting (ER)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="eb5c2-104">In den folgenden Schritten wird erläutert, wie ein Benutzer, der der Systemadministratorrolle oder der Rolle "Entwickler für elektronische Berichterstellung" zugewiesen ist, einen Konfigurationsanbieter für elektronische Berichterstellung (ER) erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="eb5c2-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can create a configuration provider for Electronic reporting (ER).</span></span> <span data-ttu-id="eb5c2-105">Jede Konfiguration für elektronische Berichterstellung verweist auf den Anbieter als Autor der Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="eb5c2-105">Each ER configuration will refer to the provider as the author of the configuration.</span></span> <span data-ttu-id="eb5c2-106">In diesem Beispiel erstellen Sie eine Konfiguration für das Beispielunternehmen, Litware, Inc. Diese Schritte können in einem beliebigen Unternehmen ausgeführt werden, da ER-Konfigurationsanbieter unter allen Unternehmen geteilt werden.</span><span class="sxs-lookup"><span data-stu-id="eb5c2-106">In this example, you will create a configuration provider for sample company, Litware, Inc. These steps can be performed in any company as ER configuration providers are shared among all companies.</span></span>


## <a name="create-a-provider"></a><span data-ttu-id="eb5c2-107">Anbieter erstellen</span><span class="sxs-lookup"><span data-stu-id="eb5c2-107">Create a provider</span></span>
1. <span data-ttu-id="eb5c2-108">Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.</span><span class="sxs-lookup"><span data-stu-id="eb5c2-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="eb5c2-109">Klicken Sie auf "Konfigurationsanbieter".</span><span class="sxs-lookup"><span data-stu-id="eb5c2-109">Click Configuration providers.</span></span>
3. <span data-ttu-id="eb5c2-110">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="eb5c2-110">Click New.</span></span>
    * <span data-ttu-id="eb5c2-111">Ein Anbieterdatensatz ist nach Name und URL eindeutig.</span><span class="sxs-lookup"><span data-stu-id="eb5c2-111">A provider record has a unique name and URL.</span></span> <span data-ttu-id="eb5c2-112">Überprüfen Sie den Inhalt dieser Seite und lassen Sie diese Prozedur aus, wenn bereits ein `http://www.litware.com` für Litware, Inc. besteht.</span><span class="sxs-lookup"><span data-stu-id="eb5c2-112">Review the content of this page and skip this procedure if a record for Litware, Inc. (`http://www.litware.com`) already exists.</span></span>  
4. <span data-ttu-id="eb5c2-113">Geben Sie im Feld "Name" "Litware, Inc." ein.</span><span class="sxs-lookup"><span data-stu-id="eb5c2-113">In the Name field, type 'Litware, Inc.'.</span></span>
    * <span data-ttu-id="eb5c2-114">Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="eb5c2-114">Litware, Inc.</span></span>  
5. <span data-ttu-id="eb5c2-115">Geben Sie im Feld "Internetadresse" `http://www.litware.com` ein.</span><span class="sxs-lookup"><span data-stu-id="eb5c2-115">In the Internet address field, type `http://www.litware.com`.</span></span>
6. <span data-ttu-id="eb5c2-116">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="eb5c2-116">Click Save.</span></span>
7. <span data-ttu-id="eb5c2-117">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="eb5c2-117">Close the page.</span></span>

## <a name="select-as-an-active-provider"></a><span data-ttu-id="eb5c2-118">Als aktiven Anbieter auswählen</span><span class="sxs-lookup"><span data-stu-id="eb5c2-118">Select as an active provider</span></span>
1. <span data-ttu-id="eb5c2-119">Wählen Sie den "Litware, Inc."- Anbieter.</span><span class="sxs-lookup"><span data-stu-id="eb5c2-119">Select the Litware, Inc. provider.</span></span>
2. <span data-ttu-id="eb5c2-120">Klicken Sie auf "Als aktiv festlegen"</span><span class="sxs-lookup"><span data-stu-id="eb5c2-120">Click Set active.</span></span>


