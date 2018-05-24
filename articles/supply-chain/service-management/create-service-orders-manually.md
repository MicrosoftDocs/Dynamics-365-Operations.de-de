---
title: "Manuelles Erstellen von Serviceaufträgen"
description: "Serviceaufträge können mithilfe einer Servicevereinbarung oder mithilfe des Formulars **Serviceaufträge** manuell erstellt werden."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: a0cc6b2646929776f4efb20474de6b0fc5c4719c
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---

# <a name="create-service-orders-manually"></a><span data-ttu-id="b9ff4-103">Manuelles Erstellen von Serviceaufträgen</span><span class="sxs-lookup"><span data-stu-id="b9ff4-103">Create service orders manually</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="b9ff4-104">Serviceaufträge können mithilfe einer Servicevereinbarung oder mithilfe des Formulars **Serviceaufträge** manuell erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="b9ff4-104">You can create service orders manually by using a service agreement or by using the **Service orders** form.</span></span> <span data-ttu-id="b9ff4-105">Sie haben außerdem die Möglichkeit, einen Serviceauftrag auf der Grundlage eines Projekts zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b9ff4-105">You can also create a service order from a project.</span></span>

> [!TIP]
> <P><span data-ttu-id="b9ff4-106">Serviceaufträge können auch mithilfe automatischer Prozesse erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="b9ff4-106">You can use automated processes to create service orders.</span></span> 

## <a name="create-a-service-order-manually-from-a-service-agreement"></a><span data-ttu-id="b9ff4-107">Manuelles Erstellen eines Serviceauftrags auf der Grundlage einer Servicevereinbarung</span><span class="sxs-lookup"><span data-stu-id="b9ff4-107">Create a service order manually from a service agreement</span></span>

1.  <span data-ttu-id="b9ff4-108">Klicken Sie auf den Bereichsseitenknoten: **Serviceverwaltung** \> **Gemeinsam** \> **Servicevereinbarungen** \> **Servicevereinbarungen**.</span><span class="sxs-lookup"><span data-stu-id="b9ff4-108">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="b9ff4-109">Wählen Sie eine Servicevereinbarung aus, oder erstellen Sie eine neue Servicevereinbarung.</span><span class="sxs-lookup"><span data-stu-id="b9ff4-109">Select a service agreement or create a new service agreement.</span></span>

3.  <span data-ttu-id="b9ff4-110">Klicken Sie auf die Registerkarte **Liefern** und in der Gruppe **Erstellen** auf **Geplante Serviceaufträge** um das **Serviceaufträge erstellen**-Formular zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b9ff4-110">Click the **Deliver** tab and in the **Create** group click **Planned service orders** to open the **Create service orders** form.</span></span>

## <a name="create-a-service-order-manually-in-the-service-orders-form"></a><span data-ttu-id="b9ff4-111">Manuelles Erstellen eines Serviceauftrags im Formular "Serviceaufträge"</span><span class="sxs-lookup"><span data-stu-id="b9ff4-111">Create a service order manually in the Service orders form</span></span>

1.  <span data-ttu-id="b9ff4-112">Klicken auf **Serviceverwaltung** \> **Gemeinsam** \> **Serviceaufträge** \> **Serviceaufträge**.</span><span class="sxs-lookup"><span data-stu-id="b9ff4-112">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="b9ff4-113">Drücken Sie STRG+N, um einen neuen Serviceauftrag zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b9ff4-113">Press Ctrl+N to create a new service order.</span></span>

3.  <span data-ttu-id="b9ff4-114">Erstellen Sie Serviceauftragspositionen für den Serviceauftrag.</span><span class="sxs-lookup"><span data-stu-id="b9ff4-114">Create service order lines for the service order.</span></span>

> [!NOTE]
> <P><span data-ttu-id="b9ff4-115">Wenn das Kontrollkästchen <STRONG>Ohne Servicevertrag zulassen</STRONG> im Formular <STRONG>Serviceverwaltungsparameter</STRONG> aktiviert ist, können Sie die Buchungen der Serviceauftragspositionen vornehmen, ohne den Serviceauftrag einer Servicevereinbarung zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="b9ff4-115">If the <STRONG>Allow without service agreement</STRONG> check box in the <STRONG>Service management parameters</STRONG> form is selected, you can post the transactions from the service order lines without attaching the service order to a service agreement.</span></span> <span data-ttu-id="b9ff4-116">Wenn das Kontrollkästchen deaktiviert ist, müssen Sie den manuell erstellten Serviceauftrag einem Projekt zuordnen, bevor Sie die Serviceauftragspositionen buchen.</span><span class="sxs-lookup"><span data-stu-id="b9ff4-116">If the check box is cleared, you must attach the manually created service order to a project before posting the service order lines.</span></span></P>

## <a name="create-a-service-order-from-a-project"></a><span data-ttu-id="b9ff4-117">Erstellen eines Serviceauftrags auf der Grundlage eines Projekts</span><span class="sxs-lookup"><span data-stu-id="b9ff4-117">Create a service order from a project</span></span>

1.  <span data-ttu-id="b9ff4-118">Klicken Sie auf **Projektverwaltung und -buchhaltung** \> **Allgemein** \> **Projekte** \> **Alle Projekte**.</span><span class="sxs-lookup"><span data-stu-id="b9ff4-118">Click **Project management and accounting** \> **Common** \> **Projects** \> **All projects**.</span></span>

2.  <span data-ttu-id="b9ff4-119">Klicken Sie im Formular **Projekte** auf den **Aktivitätsbereich**, klicken Sie auf die Registerkarte **Verwalten** \> klicken Sie auf **Service** \> **Serviceaufträge**.</span><span class="sxs-lookup"><span data-stu-id="b9ff4-119">In the **Projects** form, on the **Action pane**, click the **Manage** tab \> click **Service** \> **Service orders**.</span></span>

3.  <span data-ttu-id="b9ff4-120">Führen Sie das vorherige Verfahren zur manuellen Erstellung eines Serviceauftrags über das Formular "**Serviceaufträge**" durch.</span><span class="sxs-lookup"><span data-stu-id="b9ff4-120">Follow the previous procedure to create a service order manually in the **Service orders** form.</span></span> <span data-ttu-id="b9ff4-121">Im Feld **Projektkennung** wird die Projektreferenz angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b9ff4-121">The **Project ID** field displays the project reference.</span></span>

> [!NOTE]
> <P><span data-ttu-id="b9ff4-122">Wenn das Kontrollkästchen <STRONG>Ohne Servicevertrag zulassen</STRONG> im Formular <STRONG>Serviceverwaltungsparameter</STRONG> aktiviert ist, können Sie die Buchungen der Serviceauftragspositionen vornehmen, ohne den Serviceauftrag einer Servicevereinbarung zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="b9ff4-122">If the <STRONG>Allow without service agreement</STRONG> check box in the <STRONG>Service management parameters</STRONG> form is selected, you can post the transactions from the service order lines without attaching the service order to a service agreement.</span></span> <span data-ttu-id="b9ff4-123">Wenn das Kontrollkästchen deaktiviert ist, müssen Sie den manuell erstellten Serviceauftrag einem Projekt zuordnen, bevor Sie die Serviceauftragspositionen buchen.</span><span class="sxs-lookup"><span data-stu-id="b9ff4-123">If the check box is cleared, you must attach the manually created service order to a project before posting the service order lines.</span></span></P>

## <a name="create-a-service-order-from-the-sales-order-form"></a><span data-ttu-id="b9ff4-124">Erstellen eines Serviceauftrags über das Formular "Auftrag"</span><span class="sxs-lookup"><span data-stu-id="b9ff4-124">Create a service order from the Sales order form</span></span>

<span data-ttu-id="b9ff4-125">Serviceaufträge können im Formular **Aufträge** erstellen, indem Sie den Assistenten **Neuen auftragsbasierten Serviceauftrag erstellen**.</span><span class="sxs-lookup"><span data-stu-id="b9ff4-125">You can create a service order from the **Sales orders** form by using the **Create a new service order based on the sales order** wizard.</span></span>

1.  <span data-ttu-id="b9ff4-126">Klicken auf Bereichsseitenknoten: **Vertrieb und Marketing** \> **Gemeinsam** \> **Aufträge** \> **Alle Aufträge**.</span><span class="sxs-lookup"><span data-stu-id="b9ff4-126">Click **Sales and marketing** \> **Common** \> **Sales orders** \> **All sales orders**.</span></span>

2.  <span data-ttu-id="b9ff4-127">Öffnen Sie den entsprechenden Auftrag.</span><span class="sxs-lookup"><span data-stu-id="b9ff4-127">Open the relevant sales order.</span></span>

3.  <span data-ttu-id="b9ff4-128">Klicken Sie auf der Registerkarte **Aufträge** auf **Serviceauftrag**, um den Assistenten **Neuen auftragsbasierten Serviceauftrag erstellen** zu starten.</span><span class="sxs-lookup"><span data-stu-id="b9ff4-128">On the **Sales order** tab, click **Service order** to start the **Create a new service order based on the sales order** wizard.</span></span>

4.  <span data-ttu-id="b9ff4-129">Klicken Sie auf **Weiter \>** und schließen Sie dann die folgenden Schritte auf der Seite **Vereinbarung für Serviceauftrag auswählen** ab:</span><span class="sxs-lookup"><span data-stu-id="b9ff4-129">Click **Next \>**, and then complete the following steps on the **Select agreement for service order** page:</span></span>
    
      - <span data-ttu-id="b9ff4-130">Wählen Sie im Feld **Servicevertrag** die Servicevereinbarung aus, der der neue Serviceauftrag zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b9ff4-130">Use the **Service agreement** field to select the service agreement with which the new service order should be associated.</span></span>
    
      - <span data-ttu-id="b9ff4-131">Optional: Ordnen Sie diesen Serviceauftrag im Feld **Projektkennung** einem bestimmten Projekt zu.</span><span class="sxs-lookup"><span data-stu-id="b9ff4-131">Optional: Use the **Project ID** field to associate this service order with a particular project.</span></span>

5.  <span data-ttu-id="b9ff4-132">Klicken Sie auf **Weiter \>** und schließen Sie dann die folgenden Schritte auf der Seite **Serviceauftrag erstellen** ab:</span><span class="sxs-lookup"><span data-stu-id="b9ff4-132">Click **Next \>**, and then complete the following steps on the **Create service order** page:</span></span>
    
      - <span data-ttu-id="b9ff4-133">Geben Sie im Feld **Bevorzugte Servicezeit** ein Datum und eine Uhrzeit für den Beginn des Serviceeinsatzes ein.</span><span class="sxs-lookup"><span data-stu-id="b9ff4-133">Enter a date and time for the service call to begin in the **Preferred service time** field.</span></span>
    
      - <span data-ttu-id="b9ff4-134">Optional: Ändern Sie den Text im Feld **Beschreibung**.</span><span class="sxs-lookup"><span data-stu-id="b9ff4-134">Optional: Modify the text in the **Description** field.</span></span> <span data-ttu-id="b9ff4-135">Dieses Feld enthält standardmäßig die Beschreibung der auf der vorherigen Seite ausgewählten Servicevereinbarung.</span><span class="sxs-lookup"><span data-stu-id="b9ff4-135">By default, this field contains the description of the service agreement that you selected on the previous page.</span></span>
    
      - <span data-ttu-id="b9ff4-136">Wählen Sie im Feld **Verantwortlich** die Kennung des für die Vereinbarung zuständigen Mitarbeiters und ggf. die Kennung des vom Debitor bevorzugten Technikers für den Serviceeinsatz aus.</span><span class="sxs-lookup"><span data-stu-id="b9ff4-136">In the **Responsible** field, select the ID of the employee who is responsible for the agreement, and if you know what it is, enter the ID of the customer's preferred technician for the service call.</span></span>
    
      - <span data-ttu-id="b9ff4-137">Wählen Sie im Feld **Kontaktkennung** die Person im Unternehmen des Debitors aus, die im Zusammenhang mit diesem Serviceauftrag kontaktiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b9ff4-137">In the **Contact ID** field, select the person in the customer's company who should be contacted regarding this service order.</span></span>

6.  <span data-ttu-id="b9ff4-138">Klicken Sie auf **Weiter\>** und anschließend auf **Abschließen**.</span><span class="sxs-lookup"><span data-stu-id="b9ff4-138">Click **Next \>**, and then click **Finish**.</span></span>


## <a name="see-also"></a><span data-ttu-id="b9ff4-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b9ff4-139">See also</span></span>

[<span data-ttu-id="b9ff4-140">Serviceaufträge</span><span class="sxs-lookup"><span data-stu-id="b9ff4-140">Service orders</span></span>](service-orders.md)

[<span data-ttu-id="b9ff4-141">Automatische Erstellung von Serviceaufträgen</span><span class="sxs-lookup"><span data-stu-id="b9ff4-141">Create service orders automatically</span></span>](create-service-orders-automatically.md)

<span data-ttu-id="b9ff4-142">[Klassenformular "Serviceaufträge erstellen"](https://technet.microsoft.com/en-us/library/aa553901\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="b9ff4-142">[Create service orders (class form)](https://technet.microsoft.com/en-us/library/aa553901\(v=ax.60\))</span></span> 


