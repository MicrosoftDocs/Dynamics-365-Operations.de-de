--- 
title: Konfigurationsanbieter erstellen und sie als aktiv markieren
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 37957f224cb57fd9f6c5014740bcea124a99a03a
ms.contentlocale: de-de
ms.lasthandoff: 08/08/2018

---
# <a name="create-configuration-providers-and-mark-them-as-active"></a><span data-ttu-id="5ab73-103">Konfigurationsanbieter erstellen und sie als aktiv markieren</span><span class="sxs-lookup"><span data-stu-id="5ab73-103">Create configuration providers and mark them as active</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5ab73-104">In den folgenden Schritten wird erläutert, wie ein Benutzer, der der Systemadministratorrolle oder der Rolle "Entwickler für elektronische Berichterstellung" zugewiesen ist, einen Konfigurationsanbieter für elektronische Berichterstellung (ER) erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="5ab73-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can create a configuration provider for Electronic reporting (ER).</span></span> <span data-ttu-id="5ab73-105">Jede Konfiguration für elektronische Berichterstellung verweist auf den Anbieter als Autor der Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="5ab73-105">Each ER configuration will refer to the provider as the author of the configuration.</span></span> <span data-ttu-id="5ab73-106">In diesem Beispiel erstellen Sie eine Konfiguration für das Beispielunternehmen, Litware, Inc. Diese Schritte können in einem beliebigen Unternehmen ausgeführt werden, da ER-Konfigurationsanbieter unter allen Unternehmen geteilt werden.</span><span class="sxs-lookup"><span data-stu-id="5ab73-106">In this example, you will create a configuration provider for sample company, Litware, Inc. These steps can be performed in any company as ER configuration providers are shared among all companies.</span></span>


## <a name="create-a-provider"></a><span data-ttu-id="5ab73-107">Anbieter erstellen</span><span class="sxs-lookup"><span data-stu-id="5ab73-107">Create a provider</span></span>
1. <span data-ttu-id="5ab73-108">Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.</span><span class="sxs-lookup"><span data-stu-id="5ab73-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="5ab73-109">Klicken Sie auf "Konfigurationsanbieter".</span><span class="sxs-lookup"><span data-stu-id="5ab73-109">Click Configuration providers.</span></span>
3. <span data-ttu-id="5ab73-110">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="5ab73-110">Click New.</span></span>
    * <span data-ttu-id="5ab73-111">Ein Anbieterdatensatz ist nach Name und URL eindeutig.</span><span class="sxs-lookup"><span data-stu-id="5ab73-111">A provider record has a unique name and URL.</span></span> <span data-ttu-id="5ab73-112">Überprüfen Sie den Inhalt dieser Seite und lassen Sie diese Prozedur aus, wenn bereits ein Datensatz für Litware, Inc. (`http://www.litware.com`) besteht.</span><span class="sxs-lookup"><span data-stu-id="5ab73-112">Review the content of this page and skip this procedure if a record for Litware, Inc. (`http://www.litware.com`) already exists.</span></span>  
4. <span data-ttu-id="5ab73-113">Geben Sie im Feld "Name" "Litware, Inc." ein.</span><span class="sxs-lookup"><span data-stu-id="5ab73-113">In the Name field, type 'Litware, Inc.'.</span></span>
    * <span data-ttu-id="5ab73-114">Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="5ab73-114">Litware, Inc.</span></span>  
5. <span data-ttu-id="5ab73-115">Geben Sie im Feld "Internetadresse" `http://www.litware.com` ein.</span><span class="sxs-lookup"><span data-stu-id="5ab73-115">In the Internet address field, type `http://www.litware.com`.</span></span>
6. <span data-ttu-id="5ab73-116">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="5ab73-116">Click Save.</span></span>
7. <span data-ttu-id="5ab73-117">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="5ab73-117">Close the page.</span></span>

## <a name="select-as-an-active-provider"></a><span data-ttu-id="5ab73-118">Als aktiven Anbieter auswählen</span><span class="sxs-lookup"><span data-stu-id="5ab73-118">Select as an active provider</span></span>
1. <span data-ttu-id="5ab73-119">Wählen Sie den "Litware, Inc."- Anbieter.</span><span class="sxs-lookup"><span data-stu-id="5ab73-119">Select the Litware, Inc. provider.</span></span>
2. <span data-ttu-id="5ab73-120">Klicken Sie auf "Als aktiv festlegen"</span><span class="sxs-lookup"><span data-stu-id="5ab73-120">Click Set active.</span></span>


