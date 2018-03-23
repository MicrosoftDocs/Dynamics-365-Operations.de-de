---
title: "SQL Server Reporting Services für eine lokale Bereitstellung konfigurieren"
description: "Dieses Thema liefert Informationen über die Konfiguration von SQL Server Reporting Services (SSRS) für eine lokale Bereitstellung."
author: sarvanisathish
manager: AnnBe
ms.date: 06/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 55651
ms.assetid: 
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 7be3e9970e2599c159e7c9d414b54876d0116350
ms.openlocfilehash: 2b5abc98f5788c5091e5be61688cfd0d4076a510
ms.contentlocale: de-de
ms.lasthandoff: 03/09/2018

---
# <a name="configure-sql-server-reporting-services-for-an-on-premises-deployment"></a><span data-ttu-id="7b66e-103">SQL Server Reporting Services für eine lokale Bereitstellung konfigurieren</span><span class="sxs-lookup"><span data-stu-id="7b66e-103">Configure SQL Server Reporting Services for an on-premises deployment</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="7b66e-104">Gehen Sie nach den Schritten in diesem Thema vor, um SQL Server Reporting Services (SSRS) für ihre Bereitstellung von Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (lokal), zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="7b66e-104">Use the steps in this topic to configure SQL Server Reporting Services (SSRS) for your Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (on-premises) deployment.</span></span>

1. <span data-ttu-id="7b66e-105">Öffnen Sie die Applikation Reporting Services-Konfigurations-Manager.</span><span class="sxs-lookup"><span data-stu-id="7b66e-105">Open the Reporting Services Configuration Manager application.</span></span>
2. <span data-ttu-id="7b66e-106">Verwenden Sie den standardmäßigen **Servernamen**, das ist der Name der aktuellen Maschine, und die standardmäßige **Berichtsserverinstanz**, **MSSQLSERVER**.</span><span class="sxs-lookup"><span data-stu-id="7b66e-106">Leave the default **Server name**, which should be the name of the current machine, and the **Report Server Instance**, **MSSQLSERVER**.</span></span> 
3. <span data-ttu-id="7b66e-107">Klicken Sie auf **Verbinden**.</span><span class="sxs-lookup"><span data-stu-id="7b66e-107">Click **Connect**.</span></span>
   
   <span data-ttu-id="7b66e-108">[![Reporting Services-Konfigurationsverbindung](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)</span><span class="sxs-lookup"><span data-stu-id="7b66e-108">[![Reporting services configuration connection](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)</span></span>
   
4. <span data-ttu-id="7b66e-109">Klicken Sie auf die Registerkarte **Dienstkonto** und stellen Sie sicher, dass die Einstellungen mit der folgenden Graphik übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7b66e-109">Click the **Service Account** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="7b66e-110">[![Registerkarte Dienstkonto](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)</span><span class="sxs-lookup"><span data-stu-id="7b66e-110">[![Service account tab](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)</span></span>
    
5. <span data-ttu-id="7b66e-111">Klicken Sie auf die Registerkarte **Webdienst-URL** und stellen Sie sicher, dass die Einstellungen mit der folgenden Graphik übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7b66e-111">Click the **Web Service URL** tab and verify that the settings match the following graphic.</span></span> 

    <span data-ttu-id="7b66e-112">[![Registerkarte Webdienst-URL](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png)</span><span class="sxs-lookup"><span data-stu-id="7b66e-112">[![Web service URL tab](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png)</span></span> 
    
6. <span data-ttu-id="7b66e-113">Klicken Sie auf die Registerkarte **Datenbank** und stellen Sie sicher, dass die Einstellungen für **Datenbankname** und **Berechtigungseinstellungen** mit der folgenden Graphik übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7b66e-113">Click the **Database** tab and verify that the **Database Name** and **Credential settings** match the following graphic.</span></span> <span data-ttu-id="7b66e-114">**Hinweis:** Sie müssen eine neue Datenbank erstellen.</span><span class="sxs-lookup"><span data-stu-id="7b66e-114">**Note:** You will need to create a new database.</span></span> <span data-ttu-id="7b66e-115">Dazu klicken Sie auf **Datenbank ändern** und stellen sicher, dass der Name der neuen Datenbank **DynamicsAxReportServer** lautet.</span><span class="sxs-lookup"><span data-stu-id="7b66e-115">To do this, click **Change Database**, and then verify that the new database name is: **DynamicsAxReportServer**.</span></span>

    <span data-ttu-id="7b66e-116">[![Registerkarte Datenbank](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)</span><span class="sxs-lookup"><span data-stu-id="7b66e-116">[![database tab](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)</span></span>
    
7. <span data-ttu-id="7b66e-117">Klicken Sie auf die Registerkarte **Webportal-URL** und stellen Sie sicher, dass die Einstellungen mit der folgenden Graphik übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7b66e-117">Click the **Web Portal URL** tab and verify that the settings match the following graphic.</span></span> <span data-ttu-id="7b66e-118">**Hinweis:** Sie müssen auf **Übernehmen** klicken, um das Portal ordnungsgemäß zu erstellen und zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="7b66e-118">**Note:** You must click **Apply** to create and properly configure the Portal.</span></span>

    <span data-ttu-id="7b66e-119">[![Registerkarte Webportal-URL](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)</span><span class="sxs-lookup"><span data-stu-id="7b66e-119">[![web portal url tab](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)</span></span>
    
  <span data-ttu-id="7b66e-120">Nachdem das Portal konfiguriert ist, sieht die Registerkarte **Webportal-URL** aus, wie in der folgenden Graphik gezeigt.</span><span class="sxs-lookup"><span data-stu-id="7b66e-120">After the Portal is configured, the **Web Portal** tab will match the following graphic.</span></span>
    <span data-ttu-id="7b66e-121">[![Registerkarte Webportal](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)</span><span class="sxs-lookup"><span data-stu-id="7b66e-121">[![web portal tab](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)</span></span>
    
8. <span data-ttu-id="7b66e-122">Klicken Sie auf die Berichts-URL, um das SQL Server Reporting Services-Webportal anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="7b66e-122">Click the reports URL to view the SQL Server Reporting Services web portal.</span></span> 
9.  <span data-ttu-id="7b66e-123">Im Portal erstellen Sie den neuen Ordner **Dynamics**.</span><span class="sxs-lookup"><span data-stu-id="7b66e-123">When you are in the portal, create a new folder named **Dynamics**.</span></span>

    <span data-ttu-id="7b66e-124">[![Ordner Dynamics](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)</span><span class="sxs-lookup"><span data-stu-id="7b66e-124">[![dynamics folder](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)</span></span>
    
10. <span data-ttu-id="7b66e-125">Klicken Sie auf die Registerkarte **Reporting Services-Konfigurations-Manager**, klicken Sie auf die Registerkarte **E-Mail-Einstellungen** und stellen Sie sicher, dass die Einstellungen mit der folgenden Graphik übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7b66e-125">In the **Reporting Services Configuration Manager**, click the **E-mail Settings** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="7b66e-126">[![Registerkarte E-Mail-Einstellungen](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)</span><span class="sxs-lookup"><span data-stu-id="7b66e-126">[![email settings tab](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)</span></span>
    
11. <span data-ttu-id="7b66e-127">Klicken Sie auf die Registerkarte **Ausführungskonto** und stellen Sie sicher, dass die Einstellungen mit der folgenden Graphik übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7b66e-127">Click the **Execution Account** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="7b66e-128">[![Registerkarte Ausführungskonto](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)</span><span class="sxs-lookup"><span data-stu-id="7b66e-128">[![execution account tab](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)</span></span>
    
  <span data-ttu-id="7b66e-129">Ändern Sie die Standardeinstellungen auf der Registerkarte **Verschlüsselungs-Schlüssel** nicht. [![Registerkarte Verschlüsselungs-Schlüssel](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)</span><span class="sxs-lookup"><span data-stu-id="7b66e-129">Don’t change the default settings on the **Encryption Keys** tab. [![encryption keys tab](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)</span></span>
    
12. <span data-ttu-id="7b66e-130">Klicken Sie auf die Registerkarte **Abonnementeinstellungen** und stellen Sie sicher, dass die Einstellungen mit der folgenden Graphik übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7b66e-130">Click the **Subscription Settings** tab, and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="7b66e-131">[![Registerkarte Abonnementeinstellungen](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)</span><span class="sxs-lookup"><span data-stu-id="7b66e-131">[![subscription settings tab](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)</span></span>
    
  <span data-ttu-id="7b66e-132">Ändern Sie die Standardeinstellungen auf der Registerkarte **Bereitstellung für horizontales Skalieren** nicht. [![Registerkarte Bereitstellung für horizontales Skalieren](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)</span><span class="sxs-lookup"><span data-stu-id="7b66e-132">Don’t change the default settings on the **Scale-out Deployment** tab. [![scale-out deployment tab](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)</span></span>
    
  <span data-ttu-id="7b66e-133">Ändern Sie die Standardeinstellungen auf der Registerkarte **Power BI-Integration** nicht. [![Registerkarte Power BI Integration](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png)</span><span class="sxs-lookup"><span data-stu-id="7b66e-133">Don’t change the default settings on the **Power BI Integration** tab. [![power bi integration tab](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png)</span></span> 
    
13. <span data-ttu-id="7b66e-134">Klicken Sie auf **Beenden**, um den **Reporting Services-Konfigurations-Manager** zu schließen.</span><span class="sxs-lookup"><span data-stu-id="7b66e-134">Click **Exit** to close the **Reporting Services Configuration Manager**.</span></span>

    <span data-ttu-id="7b66e-135">[![Reporting Services-Konfigurations-Manager schließen](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)</span><span class="sxs-lookup"><span data-stu-id="7b66e-135">[![close reporting services configuration manager](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)</span></span>
    


