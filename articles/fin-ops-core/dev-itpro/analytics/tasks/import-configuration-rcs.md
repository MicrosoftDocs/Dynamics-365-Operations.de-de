---
title: (ER) Konfigurationen aus RCS importieren
description: Dieses Thema enthält Informationen dazu, wie ein Benutzer eine neue Version einer ER-Konfiguration von RCS importieren kann.
author: NickSelin
ms.date: 07/03/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 77d637b2ec1deeabc04a6796644363b330f5756e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744890"
---
# <a name="er-import-configurations-from-rcs"></a><span data-ttu-id="16b22-103">(ER) Konfigurationen aus RCS importieren</span><span class="sxs-lookup"><span data-stu-id="16b22-103">(ER) Import configurations from RCS</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="16b22-104">In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Systemadministratorrolle oder der Rolle „Entwickler für elektronische Berichterstellung“ eine neue Konfiguration für „Elektronische Berichterstellung (ER)“ erstellen kann und sie nach Microsoft Regulatory Configuration Services (RCS) hochladen kann.</span><span class="sxs-lookup"><span data-stu-id="16b22-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can import a new version of an Electronic reporting (ER) configuration from Microsoft Regulatory Configuration Services (RCS).</span></span> <span data-ttu-id="16b22-105">In diesem Beispiel können Sie die Version der ER-Konfiguration, die in einer RCS-Instanz konfiguriert wurde, auswählen und in die aktuelle Instanz importieren, z. B. Unternehmen, Litware, Inc. Diese Schritte können in jedem Unternehmen durchgeführt werden, da ER-Konfigurationen unter Unternehmen freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="16b22-105">In this example, you will select the version of the ER configuration that has been configured in an RCS instance and import it into the current instance for sample company, Litware, Inc. These steps can be performed in any company because ER configurations are shared among companies.</span></span> <span data-ttu-id="16b22-106">Um diese Schritte auszuführen, müssen Sie zunächst die Schritte im Thema [Konfigurationsanbieter erstellen und als aktiv markieren](er-configuration-provider-mark-it-active-2016-11.md) abschließen.</span><span class="sxs-lookup"><span data-stu-id="16b22-106">To complete these steps, you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="16b22-107">Um diese Schritte auszuführen, müssen Sie über Zugriff auf eine RCS-Instanz verfügen, die mindestens eine ER-Konfiguration enthält, entweder im **Abgeschlossen** oder Status **Gemeinsam genutzt** enthält.</span><span class="sxs-lookup"><span data-stu-id="16b22-107">To complete these steps, you must also have access to an RCS instance containing at least one ER configuration in either **Completed** or **Shared** status.</span></span>

1. <span data-ttu-id="16b22-108">Wechseln Sie zu **Organisationsverwaltung**  >  **Arbeitsbereiche**  >  **Elektronische Berichterstellung**.</span><span class="sxs-lookup"><span data-stu-id="16b22-108">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="16b22-109">Überprüfen Sie, dass der Konfigurationsanbieter für Beispielunternehmen „Litware, Inc.” verfügbar und als **Aktiv** markiert ist.</span><span class="sxs-lookup"><span data-stu-id="16b22-109">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="16b22-110">Wenn Sie diesen Konfigurationsanbieter nicht sehen, führen Sie die Schritte im Thema [Konfigurationsanbieter anlegen aus und markieren Sie ihn als aktiv](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="16b22-110">If you don't see this configuration provider, complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 
3. <span data-ttu-id="16b22-111">Wenn Sie keine RCS-Umgebung haben, die beim Unternehmen bereitgestellt wurde, wählen Sie den externen Link **Regulatory services – Konfiguration** aus und folgen Sie den Anweisungen zur Bereitstellung einer RCS-Umgebung.</span><span class="sxs-lookup"><span data-stu-id="16b22-111">If you have no RCS environment provisioned to your company, select **Regulatory services – Configuration** external link and follow the instructions to provision an RCS environment.</span></span> 
4. <span data-ttu-id="16b22-112">Wählen Sie **Parameter für elektronische Berichterstellung** aus.</span><span class="sxs-lookup"><span data-stu-id="16b22-112">Select **Electronic reporting parameters**.</span></span> 
5. <span data-ttu-id="16b22-113">Wählen Sie die Registerkarte **RCS** aus.</span><span class="sxs-lookup"><span data-stu-id="16b22-113">Select the **RCS** tab.</span></span> 
6. <span data-ttu-id="16b22-114">Wenn die RCS-Umgebung bereits beim Unternehmen bereitgestellt worden ist, können Sie auf der Seite dargestellte URLs verwenden, um sie anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="16b22-114">If RCS environment has been already provisioned to your company, use presented on the page URLs to access it.</span></span> 
7. <span data-ttu-id="16b22-115">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="16b22-115">Close the page.</span></span> 

## <a name="register-a-new-er-repository"></a><span data-ttu-id="16b22-116">Registrieren Sie ein neues ER-Repository.</span><span class="sxs-lookup"><span data-stu-id="16b22-116">Register a new ER repository.</span></span> 
1. <span data-ttu-id="16b22-117">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="16b22-117">In the list, mark the selected row.</span></span> 
2. <span data-ttu-id="16b22-118">Anbieter Litware, Inc. auswählen.</span><span class="sxs-lookup"><span data-stu-id="16b22-118">Select Litware, Inc. provider.</span></span> 
3. <span data-ttu-id="16b22-119">Wählen Sie Repositorys aus.</span><span class="sxs-lookup"><span data-stu-id="16b22-119">Select Repositories.</span></span> 
4. <span data-ttu-id="16b22-120">Wählen Sie Hinzufügen, um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="16b22-120">Select Add to open the drop dialog.</span></span> 
5. <span data-ttu-id="16b22-121">Wählen Sie im Feld "Konfigurationsrepository-Typ" die Option "RCS" aus.</span><span class="sxs-lookup"><span data-stu-id="16b22-121">In the Configuration repository type field, enter 'RCS'.</span></span> 
6. <span data-ttu-id="16b22-122">Wählen Sie Repository erstellen.</span><span class="sxs-lookup"><span data-stu-id="16b22-122">Select Create repository.</span></span> 
7. <span data-ttu-id="16b22-123">Geben Sie im Namensfeld „RCS-Umgebungsanzeige“ einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="16b22-123">In the RCS environment display name field, enter or select a value.</span></span> 
8. <span data-ttu-id="16b22-124">Wählen Sie die gewünschte RCS-Instanz aus.</span><span class="sxs-lookup"><span data-stu-id="16b22-124">Select the desired RCS instance.</span></span> <span data-ttu-id="16b22-125">Sie können mehrere hiervon haben.</span><span class="sxs-lookup"><span data-stu-id="16b22-125">You can have several of them.</span></span> 
9. <span data-ttu-id="16b22-126">Wählen Sie OK.</span><span class="sxs-lookup"><span data-stu-id="16b22-126">Select OK.</span></span> 

## <a name="import-er-configurations-from-rcs-based-repository"></a><span data-ttu-id="16b22-127">Importieren von EB-Konfigurationen aus dem RCS-basierten Respository</span><span class="sxs-lookup"><span data-stu-id="16b22-127">Import ER configurations from RCS-based repository</span></span>
1. <span data-ttu-id="16b22-128">Wählen Sie **Filter anzeigen** aus.</span><span class="sxs-lookup"><span data-stu-id="16b22-128">Select **Show filters**.</span></span> 
2. <span data-ttu-id="16b22-129">Verwenden Sie den Filteroperator **beginnt mit**, um im Feld **Name** den Filterwert „RCS“ einzugeben.</span><span class="sxs-lookup"><span data-stu-id="16b22-129">Enter a filter value of "RCS" on the **Name** field using the **begins with** filter operator.</span></span> 
3. <span data-ttu-id="16b22-130">Wenn Sie das ausgewählte Repository öffnen, wählen Sie auf der Seite **Mit Regulatory Configuration Services verbinden** den Link **Hier auswählen, um eine Verbindung mit Regulatory Configuration Services herzustellen** aus.</span><span class="sxs-lookup"><span data-stu-id="16b22-130">When you open the selected repository, on the **Connect to Regulatory Configuration Services** page, select **Select here to connect to Regulatory Configuration Services** link.</span></span> 
4. <span data-ttu-id="16b22-131">Wählen Sie **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="16b22-131">Select **Open**.</span></span> 
5. <span data-ttu-id="16b22-132">Wählen Sie **Schließen** aus.</span><span class="sxs-lookup"><span data-stu-id="16b22-132">Select **Close**.</span></span> 
6. <span data-ttu-id="16b22-133">Wählen Sie die gewünschte Version der EB-Konfiguration aus und wählen Sie dann **Importieren** aus, um sie in die aktuelle Instanz einzubringen.</span><span class="sxs-lookup"><span data-stu-id="16b22-133">Select the desired version of ER configuration and select **Import** to bring it in the current instance.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]