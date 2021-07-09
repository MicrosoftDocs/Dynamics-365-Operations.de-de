---
title: Regulatory Configuration Service (RCS) – Löschen einer RCS-Umgebung
description: In diesem Thema wird erklärt, wie ein Systemadministrator des Regulatory Configuration Service (RCS) eine RCS-Umgebung und die zugehörigen Daten löschen kann.
author: JaneA07
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Global
audience: Application User, System Admin
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2021-01-01
ms.dyn365.ops.version: AX 10.0.15
ms.openlocfilehash: 637962cf63bfd8c2330726f33545f939ec91d58d
ms.sourcegitcommit: dbffde1944b9d037124415c28053036c9ef1ecb7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/23/2021
ms.locfileid: "6295817"
---
# <a name="regulatory-configuration-service-rcs---delete-an-rcs-environment"></a><span data-ttu-id="a6775-103">Regulatory Configuration Service (RCS) – Löschen einer RCS-Umgebung</span><span class="sxs-lookup"><span data-stu-id="a6775-103">Regulatory Configuration Service (RCS) - Delete an RCS environment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a6775-104">In diesem Thema wird erklärt, wie ein Systemadministrator des Regulatory Configuration Service (RCS) eine RCS-Umgebung und die zugehörigen Daten löschen kann.</span><span class="sxs-lookup"><span data-stu-id="a6775-104">This topic explains how a Regulatory Configuration Service (RCS) system administrator can delete an RCS environment and related data.</span></span>

<span data-ttu-id="a6775-105">Bevor Sie das Verfahren in diesem Thema ausführen können, müssen die folgenden Voraussetzungen erfüllt sein:</span><span class="sxs-lookup"><span data-stu-id="a6775-105">Before you can complete the procedure in this topic, the following prerequisites must be met:</span></span>

- <span data-ttu-id="a6775-106">Sie müssen über die Rolle **System Admin** verfügen, die Ihnen für die RCS-Umgebung zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="a6775-106">You must have the **System Admin** role assigned to you for the RCS environment.</span></span>
- <span data-ttu-id="a6775-107">Der Rolle **System Admin** muss die Rolle **RCSDeleteEnvironmentDuty** zugewiesen sein.</span><span class="sxs-lookup"><span data-stu-id="a6775-107">The **System Admin** role must have the **RCSDeleteEnvironmentDuty** role assigned to it.</span></span>

## <a name="delete-an-rcs-environment"></a><span data-ttu-id="a6775-108">Löschen einer RCS Umgebung</span><span class="sxs-lookup"><span data-stu-id="a6775-108">Delete an RCS environment</span></span>

1. <span data-ttu-id="a6775-109">Öffnen Sie RCS und wählen Sie die Kachel **Elektronisches Berichtswesen** des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="a6775-109">Open RCS, and select the **Electronic reporting** workspace tile.</span></span>
2. <span data-ttu-id="a6775-110">Wählen Sie im Abschnitt **Verwandte Links** die Rolle **RCS-Umgebung löschen**.</span><span class="sxs-lookup"><span data-stu-id="a6775-110">In the **Related links** section, select **Delete RCS environment**.</span></span>

    ![Link RCS Umgebung im Abschnitt Zugehörige Links löschen](media/01_RCS-Delete-Environ-Related-Link.PNG)

3. <span data-ttu-id="a6775-112">Überprüfen Sie im angezeigten Dialogfeld die Nachrichten über den Umfang des Löschens der Umgebung.</span><span class="sxs-lookup"><span data-stu-id="a6775-112">In the dialog box that appears, review the messages about the scope of environment deletion.</span></span>

    ![Meldungen im Dialogfeld „RCS-Umgebung löschen](media/01_RCS-Delete-Environ-Msg_noGUID.PNG)

    > [!IMPORTANT]
    > <span data-ttu-id="a6775-114">Das Löschen einer RCS-Umgebung kann nicht rückgängig gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="a6775-114">Deletion of an RCS environment can't be reversed.</span></span>
    >
    > <span data-ttu-id="a6775-115">Der Vorgang löscht die ausgewählte RCS-Umgebung und alle zugehörigen Daten, einschließlich Funktionen und Konfigurationen, die im globalen Repository gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="a6775-115">The operation deletes the selected RCS environment and any related data, including features and configurations that are stored in the Global repository.</span></span> <span data-ttu-id="a6775-116">Funktionen und Konfigurationen, die mit anderen Organisationen geteilt werden, werden nicht geteilt und gelöscht, wenn sie keine Abhängigkeiten haben.</span><span class="sxs-lookup"><span data-stu-id="a6775-116">Features and configurations that are shared with other organizations will be unshared and deleted if they have no dependencies.</span></span> <span data-ttu-id="a6775-117">Funktionen und Konfigurationen, die Abhängigkeiten haben, werden als abgekündigt markiert.</span><span class="sxs-lookup"><span data-stu-id="a6775-117">Features and configurations that have dependencies will be marked as discontinued.</span></span>

4. <span data-ttu-id="a6775-118">Geben Sie in das vorgesehene Feld den global eindeutigen Bezeichner (GUID) der RCS-Umgebung ein, um zu bestätigen, dass Sie sie löschen möchten.</span><span class="sxs-lookup"><span data-stu-id="a6775-118">In the field that is provided, enter the globally unique identifier (GUID) of the RCS environment to confirm that you want to delete it.</span></span> <span data-ttu-id="a6775-119">Die GUID der Umgebung ist in der Nachricht über das Löschen enthalten.</span><span class="sxs-lookup"><span data-stu-id="a6775-119">The environment's GUID is included in the deletion message.</span></span>
5. <span data-ttu-id="a6775-120">Wählen Sie **Umgebung löschen**.</span><span class="sxs-lookup"><span data-stu-id="a6775-120">Select **Delete environment**.</span></span>
    
<span data-ttu-id="a6775-121">Ihre RCS Umgebung und alle zugehörigen Daten werden nun gelöscht.</span><span class="sxs-lookup"><span data-stu-id="a6775-121">Your RCS environment and any related data are now deleted.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a6775-122">Nachdem Sie eine RCS Umgebung gelöscht haben, gibt es keine Möglichkeit, die Daten wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="a6775-122">After you delete an RCS environment, there is no way to recover the data.</span></span> <span data-ttu-id="a6775-123">Eine neue RCS-Umgebung kann in jeder verfügbaren RCS-Region erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="a6775-123">A new RCS environment can be created in any available RCS region.</span></span>
