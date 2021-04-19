---
title: Einrichtung von dualem Schreiben aus Lifecycle Services
description: In diesem Thema wird erläutert, wie Sie eine Verbindung für duales Schreiben über Microsoft Dynamics Lifecycle Services (LCS) einrichten.
author: RamaKrishnamoorthy
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: e51b4ef1e309e5f89dc82a3776b88c505dc6593d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748540"
---
# <a name="dual-write-setup-from-lifecycle-services"></a><span data-ttu-id="2f2c8-103">Einrichtung von dualem Schreiben aus Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="2f2c8-103">Dual-write setup from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="2f2c8-104">In diesem Thema wird erläutert, wie Sie eine Dual-Schreib-Verbindung zwischen einer neuen Finance and Operations Umgebung und einer neuen Dataverse Umgebung aus Microsoft Dynamics Lifecycle Services (LCS) einrichten.</span><span class="sxs-lookup"><span data-stu-id="2f2c8-104">This topic explains how to set up a dual-write connection between a new Finance and Operations environment and a new Dataverse environment from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2f2c8-105">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="2f2c8-105">Prerequisites</span></span>

<span data-ttu-id="2f2c8-106">Sie müssen ein Administrator sein, um eine Dual-Schreib-Verbindung einzurichten.</span><span class="sxs-lookup"><span data-stu-id="2f2c8-106">You must be an admin to set up a dual-write connection.</span></span>

+ <span data-ttu-id="2f2c8-107">Sie müssen Zugriff auf den Mandant besitzen.</span><span class="sxs-lookup"><span data-stu-id="2f2c8-107">You must have access to the tenant.</span></span>
+ <span data-ttu-id="2f2c8-108">Sie müssen in beiden Bereichen Administrator sein, in Finance and Operations Umgebungen und Dataverse Umgebungen.</span><span class="sxs-lookup"><span data-stu-id="2f2c8-108">You must be an admin in both Finance and Operations environments and Dataverse environments.</span></span>

## <a name="set-up-a-dual-write-connection"></a><span data-ttu-id="2f2c8-109">Richten Sie eine Dual-Schreib-Verbindung ein</span><span class="sxs-lookup"><span data-stu-id="2f2c8-109">Set up a dual-write connection</span></span>

<span data-ttu-id="2f2c8-110">Folgen Sie diesen Schritten, um eine Dual-Schreib-Verbindung einzurichten.</span><span class="sxs-lookup"><span data-stu-id="2f2c8-110">Follow these steps to set up the dual-write connection.</span></span>

1. <span data-ttu-id="2f2c8-111">In LCS gehen Sie zu Ihrem Projekt.</span><span class="sxs-lookup"><span data-stu-id="2f2c8-111">In LCS, go to your project.</span></span>
2. <span data-ttu-id="2f2c8-112">Wählen Sie **Konfigurieren**, um eine neue Umgebung bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="2f2c8-112">Select **Configure** to deploy a new environment.</span></span>
3. <span data-ttu-id="2f2c8-113">Wählen Sie die Version.</span><span class="sxs-lookup"><span data-stu-id="2f2c8-113">Select the version.</span></span> 
4. <span data-ttu-id="2f2c8-114">Wählen Sie die Topologie aus.</span><span class="sxs-lookup"><span data-stu-id="2f2c8-114">Select the topology.</span></span> <span data-ttu-id="2f2c8-115">Wenn nur eine Topologie verfügbar ist, wird diese automatisch ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="2f2c8-115">If only one topology is available, it's automatically selected.</span></span>
5. <span data-ttu-id="2f2c8-116">Führen Sie die ersten Schritte im Assistent **Bereitstellungseinstellungen** aus.</span><span class="sxs-lookup"><span data-stu-id="2f2c8-116">Complete the first steps in the **Deployment settings** wizard.</span></span>
6. <span data-ttu-id="2f2c8-117">Folgen Sie einem dieser Schritte auf der Registerkarte **Dataverse**:</span><span class="sxs-lookup"><span data-stu-id="2f2c8-117">On the **Dataverse** tab, follow one of these steps:</span></span>

    - <span data-ttu-id="2f2c8-118">Wenn eine Dataverse Umgebung bereits für Ihren Mandanten bereitgestellt ist, können sie sie auswählen.</span><span class="sxs-lookup"><span data-stu-id="2f2c8-118">If a Dataverse environment is already provisioned for your tenant, you can select it.</span></span>

        1. <span data-ttu-id="2f2c8-119">Legen Sie die Option **Dataverse Konfigurieren** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="2f2c8-119">Set the **Configure Dataverse** option to **Yes**.</span></span>
        2. <span data-ttu-id="2f2c8-120">In der Spalte **Verfügbare Umgebungen** wählen Sie im Feld die Umgebung aus, die in Ihre Finance and Operations-Daten integriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="2f2c8-120">In the **Available environments** column, select the environment to integrate with your Finance and Operations data.</span></span> <span data-ttu-id="2f2c8-121">Die Liste enthält alle Umgebungen, in denen Sie über Administratorrechte verfügen.</span><span class="sxs-lookup"><span data-stu-id="2f2c8-121">The list includes all environments where you have admin privileges.</span></span>
        3. <span data-ttu-id="2f2c8-122">Wähle Sie das Kontrollkästchen **Zustimmen**, um anzuzeigen, dass Sie den Nutzungsbedingungen zustimmen.</span><span class="sxs-lookup"><span data-stu-id="2f2c8-122">Select the **Agree** check box to indicate that you agree to the terms and conditions.</span></span>

        ![Dataverse Registerkarte, wenn eine Dataverse Umgebung bereits für Ihren Mandanten bereitgestellt ist](../dual-write/media/lcs_setup_1.png)

    - <span data-ttu-id="2f2c8-124">Wenn Ihr Mandant noch keine Dataverse Umgebung hat, wird eine neue Umgebung bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="2f2c8-124">If your tenant doesn't already have a Dataverse environment, a new environment will be provisioned.</span></span>

        1. <span data-ttu-id="2f2c8-125">Legen Sie die Option **Dataverse Konfigurieren** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="2f2c8-125">Set the **Configure Dataverse** option to **Yes**.</span></span>
        2. <span data-ttu-id="2f2c8-126">Einen Namen für die Dataverse Umgebung eingeben.</span><span class="sxs-lookup"><span data-stu-id="2f2c8-126">Enter a name for the Dataverse environment.</span></span>
        3. <span data-ttu-id="2f2c8-127">Wählen Sie die Region aus, in der die Umgebung bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2f2c8-127">Select the region to deploy the environment in.</span></span>
        4. <span data-ttu-id="2f2c8-128">Wählen Sie die Standardsprache und -währung für die Umgebung aus.</span><span class="sxs-lookup"><span data-stu-id="2f2c8-128">Select the default language and currency for the environment.</span></span>

            > [!NOTE]
            > <span data-ttu-id="2f2c8-129">Sie können die Sprache und Währung später nicht mehr ändern.</span><span class="sxs-lookup"><span data-stu-id="2f2c8-129">You can't change the language and currency later.</span></span>

        5. <span data-ttu-id="2f2c8-130">Wähle Sie das Kontrollkästchen **Zustimmen**, um anzuzeigen, dass Sie den Nutzungsbedingungen zustimmen.</span><span class="sxs-lookup"><span data-stu-id="2f2c8-130">Select the **Agree** check box to indicate that you agree to the terms and conditions.</span></span>

        ![Dataverse Registerkarte, wenn Ihr Mandant noch keine Dataverse Umgebung hat](../dual-write/media/lcs_setup_2.png)

7. <span data-ttu-id="2f2c8-132">Führen Sie die verbleibenden Schritte im Assistent **Bereitstellungseinstellungen** aus.</span><span class="sxs-lookup"><span data-stu-id="2f2c8-132">Complete the remaining steps in the **Deployment settings** wizard.</span></span>
8. <span data-ttu-id="2f2c8-133">Nachdem die Umgebung den Status **Bereitgestellt** hat, öffnen Sie die Seite mit den Umgebungsdetails.</span><span class="sxs-lookup"><span data-stu-id="2f2c8-133">After the environment has a status of **Deployed**, open the environment details page.</span></span> <span data-ttu-id="2f2c8-134">Der Abschnitt **Power Platform-Integration** zeigt die Namen der Finance and Operations-Umgebung und der Dataverse-Umgebung, die verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="2f2c8-134">The **Power Platform Integration** section shows the names of the Finance and Operations environment and the Dataverse environment that are linked.</span></span>

    ![Abschnitt „Power Platform-Integration“](../dual-write/media/lcs_setup_3.png)

9. <span data-ttu-id="2f2c8-136">Ein Administrator der Finance and Operations Umgebung muss sich bei LCS anmelden und **Verknüpfung zu CDS für Apps** auswählen, um den Link vervollständigen.</span><span class="sxs-lookup"><span data-stu-id="2f2c8-136">An admin of the Finance and Operations environment must sign in to LCS and select **Link to CDS for Apps** to complete the link.</span></span> <span data-ttu-id="2f2c8-137">Auf der Seite mit den Umgebungsdetails werden die Kontaktinformationen des Administrators angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2f2c8-137">The environment details page shows the admin's contact information.</span></span>

    <span data-ttu-id="2f2c8-138">Nach Abschluss der Verknüpfung wird der Status auf **Umgebungsverknüpfung erfolgreich abgeschlossen** aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="2f2c8-138">After the link is completed, the status is updated to **Environment linking successfully completed**.</span></span>

10. <span data-ttu-id="2f2c8-139">Zum Öffnen des **Datenintegration** Arbeitsbereichs in der Finance and Operations wählen Sie die Umgebung aus und steuern Sie die verfügbaren Vorlagen und wählen Sie **Link zu CDS für Apps**.</span><span class="sxs-lookup"><span data-stu-id="2f2c8-139">To open the **Data integration** workspace in the Finance and Operations environment and control the templates that are available, select **Link to CDS for Apps**.</span></span>

    ![Link zur Schaltfläche „CDS für Apps“ im Abschnitt „Power Platform-Integration“](../dual-write/media/lcs_setup_4.png)

> [!NOTE]
> <span data-ttu-id="2f2c8-141">Sie können die Verknüpfung von Umgebungen mit LCS nicht aufheben.</span><span class="sxs-lookup"><span data-stu-id="2f2c8-141">You can't unlink environments by using LCS.</span></span> <span data-ttu-id="2f2c8-142">Um die Verknüpfung einer Umgebung aufzuheben, öffnen Sie den **Datenintegration** Arbeitsbereich in der Finance and Operations Umgebung und wählen Sie dann **Verknüpfung aufheben**.</span><span class="sxs-lookup"><span data-stu-id="2f2c8-142">To unlink an environment, open the **Data integration** workspace in the Finance and Operations environment, and then select **Unlink**.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]