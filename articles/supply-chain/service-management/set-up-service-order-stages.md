---
title: Serviceauftragsphasen einrichten
description: Serviceauftragsphasen einrichten.
author: ShylaThompson
manager: AnnBe
ms.date: 05/07/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 30f6a6afa6ab91bed41bb19b8312dc7e25bd2478
ms.contentlocale: de-de
ms.lasthandoff: 08/07/2018

---

# <a name="set-up-service-order-stages"></a><span data-ttu-id="5e597-103">Serviceauftragsphasen einrichten</span><span class="sxs-lookup"><span data-stu-id="5e597-103">Set up service order stages</span></span> 

[!include [banner](../includes/banner.md)]


1.  <span data-ttu-id="5e597-104">Klicken auf **Serviceverwaltung** \> **Einrichtung** \> **Serviceaufträge** \> **Servicephasen**.</span><span class="sxs-lookup"><span data-stu-id="5e597-104">Click **Service management** \> **Setup** \> **Service orders** \> **Service stages**.</span></span>

2.  <span data-ttu-id="5e597-105">Drücken Sie STRG+N, um einen neuen Datensatz zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5e597-105">Press CTRL+N to create a new record.</span></span>

3.  <span data-ttu-id="5e597-106">Geben Sie in den Feldern **Servicephase** und **Beschreibung** eine Servicephasenkennung und eine Beschreibung an.</span><span class="sxs-lookup"><span data-stu-id="5e597-106">In the **Service stage** and **Description** fields, specify a service stage ID and description.</span></span>

4.  <span data-ttu-id="5e597-107">Wählen Sie die geeigneten Parameter für die Phase aus.</span><span class="sxs-lookup"><span data-stu-id="5e597-107">Select the appropriate parameters for the stage.</span></span>

5.  <span data-ttu-id="5e597-108">Wählen Sie die übergeordnete Phase für die aktuelle Phase aus, oder lassen Sie das Feld **Übergeordnet** leer, wenn es sich bei der Phase um die Anfangsphase handelt.</span><span class="sxs-lookup"><span data-stu-id="5e597-108">Select the parent stage for the current stage or leave the **Parent** field blank if the stage is the initial stage in the stage setup.</span></span>


> [!NOTE]
> <P><span data-ttu-id="5e597-109">Nach dem Speichern der Phase kann das Feld <STRONG>Übergeordnet</STRONG> nicht mehr geändert werden.</span><span class="sxs-lookup"><span data-stu-id="5e597-109">You cannot modify the <STRONG>Parent</STRONG> field after you save the stage.</span></span> <span data-ttu-id="5e597-110">Sie können den Datensatz stattdessen löschen und mit einer anderen Auswahl im Feld <STRONG>Übergeordnet</STRONG> neu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5e597-110">Instead, you can delete the record and create the record again with a different selection in the <STRONG>Parent</STRONG> field.</span></span></P>
> <P><span data-ttu-id="5e597-111">Eine Phase kann nur mit einem leeren Feld <STRONG>Übergeordnet</STRONG> erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="5e597-111">Also, you can only create one stage with a blank <STRONG>Parent</STRONG> field.</span></span> <span data-ttu-id="5e597-112">Anders ausgedrückt: Es ist immer nur eine Anfangsphase zulässig.</span><span class="sxs-lookup"><span data-stu-id="5e597-112">That is, only one initial stage is permitted.</span></span></P>


  



