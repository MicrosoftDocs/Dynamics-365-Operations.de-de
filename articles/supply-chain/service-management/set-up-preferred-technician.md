---
title: Einrichten eines bevorzugten Technikers
description: Sie können eine beliebige Arbeitskraft als bevorzugten Techniker für eine Servicevereinbarung oder einen Serviceauftrag auswählen.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable, SMADispatchBoard
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 80ea0265eb27fb5cf32f5f921caa7ac2e44a0116
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3217286"
---
# <a name="set-up-a-preferred-technician"></a><span data-ttu-id="c5935-103">Einrichten eines bevorzugten Technikers</span><span class="sxs-lookup"><span data-stu-id="c5935-103">Set up a preferred technician</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="c5935-104">Sie können eine beliebige Arbeitskraft als bevorzugten Techniker für eine Servicevereinbarung oder einen Serviceauftrag auswählen.</span><span class="sxs-lookup"><span data-stu-id="c5935-104">You can select any worker as a preferred technician for a service agreement or service order.</span></span> <span data-ttu-id="c5935-105">Es empfiehlt sich allerdings, die Arbeitskraft dem entsprechenden Einsatzteam zuzuordnen, damit sie im Modul **Einsatzplanung** berücksichtigt wird.</span><span class="sxs-lookup"><span data-stu-id="c5935-105">However, it is a good idea to add the worker to the appropriate dispatch team so that the worker is included on the **Dispatch board**.</span></span>

## <a name="assign-employee-to-a-dispatch-team"></a><span data-ttu-id="c5935-106">Zuweisen eines Mitarbeiters zu einem Einsatzteam</span><span class="sxs-lookup"><span data-stu-id="c5935-106">Assign employee to a dispatch team</span></span>

1.  <span data-ttu-id="c5935-107">Klicken Sie auf **Personalverwaltung** \> **Allgemein** \> **Arbeitskräfte** \> **Arbeitskräfte**.</span><span class="sxs-lookup"><span data-stu-id="c5935-107">Click **Human resources** \> **Common** \> **Workers** \> **Workers**.</span></span> <span data-ttu-id="c5935-108">Doppelklicken Sie auf eine Arbeitskraft, um die Seite "Details zur Arbeitskraft" zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c5935-108">Double-click a worker to open the worker details page.</span></span> <span data-ttu-id="c5935-109">Klicken im **Aktivitätsbereich** auf **Einstellungen** \>**Einsatzteam**, um das Formular **Arbeitskräfte disponieren** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c5935-109">On the **Action Pane**, click **Setup** \>**Dispatch team** to open the **Dispatch workers** form.</span></span>

2.  <span data-ttu-id="c5935-110">Wählen Sie im Feld **Einsatzteam** das Team aus, dem die Arbeitskraft zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="c5935-110">In the **Dispatch team** field, select the team to assign the worker to.</span></span>

## <a name="assign-a-preferred-technician-to-a-service-agreement"></a><span data-ttu-id="c5935-111">Zuweisen eines bevorzugten Technikers zu einer Servicevereinbarung</span><span class="sxs-lookup"><span data-stu-id="c5935-111">Assign a preferred technician to a service agreement</span></span>

1.  <span data-ttu-id="c5935-112">Klicken Sie auf den Bereichsseitenknoten: **Serviceverwaltung** \> **Gemeinsam** \> **Servicevereinbarungen** \> **Servicevereinbarungen**.</span><span class="sxs-lookup"><span data-stu-id="c5935-112">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span> <span data-ttu-id="c5935-113">Doppelklicken Sie auf eine Servicevereinbarung, um das Detailformular zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c5935-113">Double-click a service agreement to open the details form.</span></span>

2.  <span data-ttu-id="c5935-114">Aktivieren Sie auf der Registerkarte **Allgemein** das Kontrollkästchen **Bevorzugter Techniker**, und wählen Sie anschließend ein Mitglied des entsprechenden Einsatzteams als bevorzugten Techniker für die Servicevereinbarung aus.</span><span class="sxs-lookup"><span data-stu-id="c5935-114">On the **General** tab, select the **Preferred technician** field, and then select a member of the appropriate dispatch team as the preferred technician for the service agreement.</span></span>

## <a name="assign-a-preferred-technician-to-a-service-order"></a><span data-ttu-id="c5935-115">Zuweisen eines bevorzugten Technikers zu einem Serviceauftrag</span><span class="sxs-lookup"><span data-stu-id="c5935-115">Assign a preferred technician to a service order</span></span>

1.  <span data-ttu-id="c5935-116">Klicken Sie auf **Serviceverwaltung** \> **Periodisch** \> **Einsatzplanung**.</span><span class="sxs-lookup"><span data-stu-id="c5935-116">Click **Service management** \> **Periodic** \> **Dispatch board**.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="c5935-117">Geben Sie im Formular <STRONG>Einsatzplanung</STRONG> einen Datumsbereich für die anzuzeigenden Einsatzaktivitäten an.</span><span class="sxs-lookup"><span data-stu-id="c5935-117">In the <STRONG>Dispatch board</STRONG> form, specify a date range for dispatch activities to view.</span></span> <span data-ttu-id="c5935-118">Geben Sie außerdem an, ob abgeschlossene Aktivitäten angezeigt werden sollen und ob die Liste mit den Einsatzaktivitäten auf die Teams beschränkt werden soll, denen Sie selbst angehören oder die Sie selbst überwachen.</span><span class="sxs-lookup"><span data-stu-id="c5935-118">Also, specify whether to display closed activities and whether to limit the dispatch activity list to teams that you belong to or are authorized to monitor.</span></span> <span data-ttu-id="c5935-119">Klicken Sie auf <STRONG>OK</STRONG>, um das Formular <STRONG>Einsatzplanung</STRONG> zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c5935-119">Click <STRONG>OK</STRONG> to open the <STRONG>Dispatch board</STRONG>.</span></span></P>



2.  <span data-ttu-id="c5935-120">Wählen Sie die Position der Serviceaktivität aus, die Sie ändern möchten.</span><span class="sxs-lookup"><span data-stu-id="c5935-120">Select the line of the service activity to modify.</span></span>

3.  <span data-ttu-id="c5935-121">Weisen Sie auf der  **Registerkarte** mithilfe der Liste **Arbeitskraft** ein Mitglied des entsprechenden Einsatzteams als bevorzugten Techniker für den Serviceeinsatz zu.</span><span class="sxs-lookup"><span data-stu-id="c5935-121">On the **Related** tab, use the **Worker** list to assign a member of the appropriate dispatch team as the preferred technician for the service call.</span></span>

## <a name="see-also"></a><span data-ttu-id="c5935-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c5935-122">See also</span></span>

[<span data-ttu-id="c5935-123">Ausarbeiten und Festsetzen von Serviceverträge – Übersicht</span><span class="sxs-lookup"><span data-stu-id="c5935-123">Develop and establish service agreements overview</span></span>](service-agreements.md)

[<span data-ttu-id="c5935-124">Manuelles Erstellen von Serviceaufträgen</span><span class="sxs-lookup"><span data-stu-id="c5935-124">Create service orders manually</span></span>](create-service-orders-manually.md)

<span data-ttu-id="c5935-125">[Formular "Servicevereinbarungen"](https://technet.microsoft.com/library/aa617823\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="c5935-125">[Service agreements (form)](https://technet.microsoft.com/library/aa617823\(v=ax.60\))</span></span>
  


