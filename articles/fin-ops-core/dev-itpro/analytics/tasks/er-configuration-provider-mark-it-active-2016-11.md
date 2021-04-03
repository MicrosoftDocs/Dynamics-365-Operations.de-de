---
title: Erstellen von Konfigurationsanbietern und Markieren als aktiv
description: In diesem Thema wird erläutert, wie ein Benutzer, der der Systemadministratorrolle oder der Rolle „Entwickler für elektronische Berichterstellung“ zugewiesen ist, einen Konfigurationsanbieter erstellen kann.
author: NickSelin
manager: AnnBe
ms.date: 07/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERVendorTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 11ff1d531b0467cf75ec98b092fe6010f4fa95c0
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569786"
---
# <a name="create-configuration-providers-and-mark-them-as-active"></a><span data-ttu-id="2e9fb-103">Erstellen von Konfigurationsanbietern und Markieren als aktiv</span><span class="sxs-lookup"><span data-stu-id="2e9fb-103">Create configuration providers and mark them as active</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2e9fb-104">In diesem Thema wird erläutert, wie ein Benutzer, der der Systemadministratorrolle oder der Rolle „Entwickler für elektronische Berichterstellung“ zugewiesen ist, einen Konfigurationsanbieter für elektronische Berichterstellung (ER) erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="2e9fb-104">This topic explains how a user assigned to the System Administrator or Electronic Reporting Developer role can create a configuration provider for Electronic reporting (ER).</span></span> <span data-ttu-id="2e9fb-105">Jede Konfiguration für elektronische Berichterstellung verweist auf den Anbieter als Autor der Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="2e9fb-105">Each ER configuration will refer to the provider as the author of the configuration.</span></span> <span data-ttu-id="2e9fb-106">In diesem Beispiel erstellen Sie eine Konfiguration für das Beispielunternehmen, Litware, Inc. Diese Schritte können in einem beliebigen Unternehmen ausgeführt werden, da ER-Konfigurationsanbieter unter allen Unternehmen geteilt werden.</span><span class="sxs-lookup"><span data-stu-id="2e9fb-106">In this example, you will create a configuration provider for sample company, Litware, Inc. These steps can be performed in any company as ER configuration providers are shared among all companies.</span></span>

## <a name="create-a-provider"></a><span data-ttu-id="2e9fb-107">Anbieter erstellen</span><span class="sxs-lookup"><span data-stu-id="2e9fb-107">Create a provider</span></span>
1. <span data-ttu-id="2e9fb-108">Wechseln Sie zum **Navigationsbereich** in der oberen linken Ecke und wählen Sie **Organisationsverwaltung** aus.</span><span class="sxs-lookup"><span data-stu-id="2e9fb-108">Go to the **navigation pane** in the upper left corner and select **Organization administration**.</span></span>
2. <span data-ttu-id="2e9fb-109">Wechseln Sie zu **Arbeitsbereiche > Elektronische Berichterstellung**.</span><span class="sxs-lookup"><span data-stu-id="2e9fb-109">Go to **Workspaces > Electronic reporting**.</span></span>
3. <span data-ttu-id="2e9fb-110">Wechseln Sie zu **Zugehörige Verknüpfungen > Konfigurationsanbieter**.</span><span class="sxs-lookup"><span data-stu-id="2e9fb-110">Go to **Related links > Configuration providers**.</span></span>
4. <span data-ttu-id="2e9fb-111">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="2e9fb-111">Select **New**.</span></span>
    - <span data-ttu-id="2e9fb-112">Ein Anbieterdatensatz ist nach Name und URL eindeutig.</span><span class="sxs-lookup"><span data-stu-id="2e9fb-112">A provider record has a unique name and URL.</span></span> <span data-ttu-id="2e9fb-113">Überprüfen Sie den Inhalt dieser Seite und lassen Sie diese Prozedur aus, wenn bereits ein Datensatz für Litware, Inc. (https://www.litware.com) besteht.</span><span class="sxs-lookup"><span data-stu-id="2e9fb-113">Review the content of this page and skip this procedure if a record for Litware, Inc. (https://www.litware.com) already exists.</span></span>  
5. <span data-ttu-id="2e9fb-114">Geben Sie im Feld „Name“ „`Litware, Inc.`“ ein.</span><span class="sxs-lookup"><span data-stu-id="2e9fb-114">In the Name field, type `Litware, Inc.`.</span></span>
6. <span data-ttu-id="2e9fb-115">Geben Sie im Feld „Internetadresse” „`https://www.litware.com`” ein.</span><span class="sxs-lookup"><span data-stu-id="2e9fb-115">In the Internet address field, type `https://www.litware.com`.</span></span>
7. <span data-ttu-id="2e9fb-116">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="2e9fb-116">Select **Save**.</span></span>
8. <span data-ttu-id="2e9fb-117">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="2e9fb-117">Close the page.</span></span>

## <a name="select-as-an-active-provider"></a><span data-ttu-id="2e9fb-118">Als aktiven Anbieter auswählen</span><span class="sxs-lookup"><span data-stu-id="2e9fb-118">Select as an active provider</span></span>
1. <span data-ttu-id="2e9fb-119">Wählen Sie den "Litware, Inc."- Anbieter.</span><span class="sxs-lookup"><span data-stu-id="2e9fb-119">Select the Litware, Inc. provider.</span></span>
2. <span data-ttu-id="2e9fb-120">Wählen Sie **Als aktiv festlegen**.</span><span class="sxs-lookup"><span data-stu-id="2e9fb-120">Select **Set active**.</span></span>

![Elektronische Berichterstellung – Seite „Arbeitsbereich“](../media/GER-Task-ActiveProvider-1.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]