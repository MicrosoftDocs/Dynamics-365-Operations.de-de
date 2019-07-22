---
title: (ER) Konfigurationen aus RCS importieren
description: Dieses Thema enthält Informationen dazu, wie ein Benutzer eine neue Version einer ER-Konfiguration von RCS importieren kann.
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c458cf815837fb7e4688c4c0443b7962cac403a5
ms.sourcegitcommit: 287d78e6afdaf40c499e5db6c4531f2b26dbaca0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/04/2019
ms.locfileid: "1727005"
---
# <a name="er-import-configurations-from-rcs"></a><span data-ttu-id="ce2f5-103">(ER) Konfigurationen aus RCS importieren</span><span class="sxs-lookup"><span data-stu-id="ce2f5-103">(ER) Import configurations from RCS</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ce2f5-104">In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Systemadministratorrolle oder der Rolle „Entwickler für elektronische Berichterstellung“ eine neue Konfiguration für „Elektronische Berichterstellung (ER)“ erstellen kann und sie nach Microsoft Regulatory Configuration Services (RCS) hochladen kann.</span><span class="sxs-lookup"><span data-stu-id="ce2f5-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can import a new version of an Electronic reporting (ER) configuration from Microsoft Regulatory Configuration Services (RCS).</span></span> <span data-ttu-id="ce2f5-105">In diesem Beispiel können Sie die Version der ER-Konfiguration, die in einer RCS-Instanz konfiguriert wurde, auswählen und in die aktuelle Finance and Operations-Instanz importieren, z. B. Unternehmen, Litware, Inc. Diese Schritte können in jedem Unternehmen durchgeführt werden, da ER-Konfigurationen unter Unternehmen freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ce2f5-105">In this example, you will select the version of the ER configuration that has been configured in an RCS instance and import it into the current Finance and Operations instance for sample company, Litware, Inc. These steps can be performed in any company because ER configurations are shared among companies.</span></span> <span data-ttu-id="ce2f5-106">Um diese Schritte auszuführen, müssen Sie zunächst die Schritte im Thema [Konfigurationsanbieter erstellen und als aktiv markieren](er-configuration-provider-mark-it-active-2016-11.md) abschließen.</span><span class="sxs-lookup"><span data-stu-id="ce2f5-106">To complete these steps, you must first complete the steps in the topic, [Create a configuration provider and mark it as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="ce2f5-107">Um diese Schritte auszuführen, müssen Sie über Zugriff auf eine RCS-Instanz verfügen, die mindestens eine ER-Konfiguration enthält, entweder im **Abgeschlossen** oder Status **Gemeinsam genutzt** enthält.</span><span class="sxs-lookup"><span data-stu-id="ce2f5-107">To complete these steps, you must also have access to an RCS instance containing at least one ER configuration in either **Completed** or **Shared** status.</span></span>

1. <span data-ttu-id="ce2f5-108">Wechseln Sie zu **Organisationsverwaltung**  >  **Arbeitsbereiche**  >  **Elektronische Berichterstellung**.</span><span class="sxs-lookup"><span data-stu-id="ce2f5-108">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="ce2f5-109">Überprüfen Sie, dass der Konfigurationsanbieter für Beispielunternehmen „Litware, Inc.” verfügbar und als **Aktiv** markiert ist.</span><span class="sxs-lookup"><span data-stu-id="ce2f5-109">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="ce2f5-110">Wenn Sie diesen Konfigurationsanbieter nicht sehen, müssen Sie zunächst die Schritte im Thema [Konfigurationsanbieter erstellen und als aktiv markieren](er-configuration-provider-mark-it-active-2016-11.md) abschließen.</span><span class="sxs-lookup"><span data-stu-id="ce2f5-110">If you don’t see this configuration provider, complete the steps in the topic, [Create a configuration provider and mark it as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 
3. <span data-ttu-id="ce2f5-111">Wenn Sie keine RCS-Umgebung haben, die beim Unternehmen bereitgestellt wurde, klicken Sie auf den externen Link **Regulatory services – Konfiguration** und folgen Sie den Anweisungen zur Bereitstellung einer RCS-Umgebung.</span><span class="sxs-lookup"><span data-stu-id="ce2f5-111">If you have no RCS environment provisioned to your company, click **Regulatory services – Configuration** external link and follow the instructions to provision an RCS environment.</span></span> 
4. <span data-ttu-id="ce2f5-112">Klicken Sie auf **Parameter für elektronische Berichterstellung**.</span><span class="sxs-lookup"><span data-stu-id="ce2f5-112">Click **Electronic reporting parameters**.</span></span> 
5. <span data-ttu-id="ce2f5-113">Klicken Sie auf die Registerkarte **RCS**.</span><span class="sxs-lookup"><span data-stu-id="ce2f5-113">Click the **RCS** tab.</span></span> 
6. <span data-ttu-id="ce2f5-114">Wenn die RCS-Umgebung bereits beim Unternehmen bereitgestellt worden ist, können Sie auf der Seite dargestellte URLs verwenden, um sie anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ce2f5-114">If RCS environment has been already provisioned to your company, use presented on the page URLs to access it.</span></span> 
7. <span data-ttu-id="ce2f5-115">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="ce2f5-115">Close the page.</span></span> 

## <a name="register-a-new-er-repository"></a><span data-ttu-id="ce2f5-116">Registrieren Sie ein neues ER-Repository.</span><span class="sxs-lookup"><span data-stu-id="ce2f5-116">Register a new ER repository.</span></span> 
1. <span data-ttu-id="ce2f5-117">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="ce2f5-117">In the list, mark the selected row.</span></span> 
2. <span data-ttu-id="ce2f5-118">Anbieter Litware, Inc. auswählen.</span><span class="sxs-lookup"><span data-stu-id="ce2f5-118">Select Litware, Inc. provider.</span></span> 
3. <span data-ttu-id="ce2f5-119">Klicken Sie auf Repositorys.</span><span class="sxs-lookup"><span data-stu-id="ce2f5-119">Click Repositories.</span></span> 
4. <span data-ttu-id="ce2f5-120">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="ce2f5-120">Click Add to open the drop dialog.</span></span> 
5. <span data-ttu-id="ce2f5-121">Wählen Sie im Feld "Konfigurationsrepository-Typ" die Option "RCS" aus.</span><span class="sxs-lookup"><span data-stu-id="ce2f5-121">In the Configuration repository type field, enter 'RCS'.</span></span> 
6. <span data-ttu-id="ce2f5-122">Klicken Sie auf "Repository erstellen".</span><span class="sxs-lookup"><span data-stu-id="ce2f5-122">Click Create repository.</span></span> 
7. <span data-ttu-id="ce2f5-123">Geben Sie im Namensfeld „RCS-Umgebungsanzeige“ einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="ce2f5-123">In the RCS environment display name field, enter or select a value.</span></span> 
8. <span data-ttu-id="ce2f5-124">Wählen Sie die gewünschte RCS-Instanz aus.</span><span class="sxs-lookup"><span data-stu-id="ce2f5-124">Select the desired RCS instance.</span></span> <span data-ttu-id="ce2f5-125">Beachten Sie, dass Sie mehrere hiervon haben können.</span><span class="sxs-lookup"><span data-stu-id="ce2f5-125">Note that you can have several of them.</span></span> 
9. <span data-ttu-id="ce2f5-126">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="ce2f5-126">Click OK.</span></span> 

## <a name="import-er-configurations-from-rcs-based-repository"></a><span data-ttu-id="ce2f5-127">Importieren von ER-Konfigurationen aus dem RCS-basierten Respository</span><span class="sxs-lookup"><span data-stu-id="ce2f5-127">Import ER configurations from RCS based repository</span></span>
1. <span data-ttu-id="ce2f5-128">Klicken Sie auf **Filter anzeigen.**</span><span class="sxs-lookup"><span data-stu-id="ce2f5-128">Click **Show filters**.</span></span> 
2. <span data-ttu-id="ce2f5-129">Verwenden Sie den Filteroperator **beginnt mit**, um im Feld **Name** den Filterwert „RCS“ einzugeben.</span><span class="sxs-lookup"><span data-stu-id="ce2f5-129">Enter a filter value of "RCS" on the **Name** field using the **begins with** filter operator.</span></span> 
3. <span data-ttu-id="ce2f5-130">Wenn Sie das ausgewählte Repository öffnen, klicken Sie auf der Seite **Mit Regulatory Configuration Services verbinden** auf den Link **Hier klicken, um eine Verbindung mit Regulatory Configuration Services herzustellen**.</span><span class="sxs-lookup"><span data-stu-id="ce2f5-130">When you open the selected repository, on the **Connect to Regulatory Configuration Services** page, click **Click here to connect to Regulatory Configuration Services** link.</span></span> 
4. <span data-ttu-id="ce2f5-131">Klicken Sie auf **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="ce2f5-131">Click **Open**.</span></span> 
5. <span data-ttu-id="ce2f5-132">Klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="ce2f5-132">Click **Close**.</span></span> 
6. <span data-ttu-id="ce2f5-133">Wählen Sie die gewünschte Version der ER-Konfiguration aus und klicken Sie auf **Importieren**, um sie in die aktuelle Finance and Operations-Instanz einzubringen.</span><span class="sxs-lookup"><span data-stu-id="ce2f5-133">Select the desired version of ER configuration and click **Import** to bring it in the current Finance and Operations instance.</span></span>
