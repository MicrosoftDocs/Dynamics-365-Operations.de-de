---
title: Eine Umgebung für die Masterdatensuche einrichten
description: In diesem Thema wird erläutert, wie Sie Ihre Umgebung für die Verwendung der Masterdaten-Suchfunktion für die Steuerberechnung einrichten.
author: kai-cloud
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: pashao
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: eda093a75898bace2f3c7968933b83ccafa7fabb
ms.sourcegitcommit: 66095f1b7e0fd2756aa29fd7deb9ce5392b7e0b2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/08/2021
ms.locfileid: "5869067"
---
# <a name="set-up-an-environment-for-master-data-lookup"></a><span data-ttu-id="fd554-103">Eine Umgebung für die Masterdatensuche einrichten</span><span class="sxs-lookup"><span data-stu-id="fd554-103">Set up an environment for master data lookup</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="fd554-104">In diesem Thema wird erläutert, wie Sie Ihre Umgebung für die Verwendung der Masterdaten-Suchfunktion für die Steuerberechnung einrichten.</span><span class="sxs-lookup"><span data-stu-id="fd554-104">This topic explains how to set up your environment to use the Tax Calculation master data lookup functionality.</span></span>

1. <span data-ttu-id="fd554-105">Richten Sie die Integration von Power Platform in Lifecycle Services (LCS) ein.</span><span class="sxs-lookup"><span data-stu-id="fd554-105">Set up power platform integration in Lifecycle Services (LCS).</span></span> <span data-ttu-id="fd554-106">Weitere Informationen finden Sie unter [Integration von Microsoft Power Platform – Übersicht über Add-Ins](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).</span><span class="sxs-lookup"><span data-stu-id="fd554-106">For more information, see [Microsoft Power Platform integration - Add-ins overview](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).</span></span>
2. <span data-ttu-id="fd554-107">Richten Sie Dynamics 365 Finance und Microsoft Dataverse ein.</span><span class="sxs-lookup"><span data-stu-id="fd554-107">Set up Dynamics 365 Finance and Microsoft Dataverse.</span></span> <span data-ttu-id="fd554-108">Weitere Informationen finden Sie unter [Die Lösung erhalten](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) und [Authentifizierung und Autorisierung](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).</span><span class="sxs-lookup"><span data-stu-id="fd554-108">For more information, see [Getting the solution](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) and [Authentication and authorization](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).</span></span>
3. <span data-ttu-id="fd554-109">Importieren Sie die *notwendig virtuelle Entitätslösung für Steuerdienste* von der [Virtuellen Entität des Steuerdienstes](https://go.microsoft.com/fwlink/?linkid=2158160).</span><span class="sxs-lookup"><span data-stu-id="fd554-109">Import the *Prerequisite tax service virtual entity solution* from the [Tax service virtual entity](https://go.microsoft.com/fwlink/?linkid=2158160).</span></span>
4. <span data-ttu-id="fd554-110">Richten Sie den Dynamics 365 Regulatory Configuration Service (RCS) ein.</span><span class="sxs-lookup"><span data-stu-id="fd554-110">Set up the Dynamics 365 Regulatory Configuration Service (RCS).</span></span> 
5. <span data-ttu-id="fd554-111">Erstellen Sie eine Serviceanforderung für Microsoft, um das Flighting der folgenden Funktionen zu ermöglichen:</span><span class="sxs-lookup"><span data-stu-id="fd554-111">Create a service request for Microsoft to enable flighting of the following features:</span></span>

      - <span data-ttu-id="fd554-112">ERCdsFeature</span><span class="sxs-lookup"><span data-stu-id="fd554-112">ERCdsFeature</span></span>
      - <span data-ttu-id="fd554-113">TaxServiceCDSFeature</span><span class="sxs-lookup"><span data-stu-id="fd554-113">TaxServiceCDSFeature</span></span>

6. <span data-ttu-id="fd554-114">Aktivieren Sie in Finance den Arbeitsbereich **Funktionsverwaltung** und aktivieren Sie die folgenden Funktionen:</span><span class="sxs-lookup"><span data-stu-id="fd554-114">In Finance, go to the **Feature management** workspace, and enable the following features:</span></span>

      - <span data-ttu-id="fd554-115">(Vorschau) Unterstützung von Dataverse-Datenquellen der elektronischen Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="fd554-115">(Preview) Electronic reporting Dataverse datasources support</span></span>
      - <span data-ttu-id="fd554-116">(Vorschauversion) Unterstützung für Dataverse-Datenquellen des Steuerdienstes</span><span class="sxs-lookup"><span data-stu-id="fd554-116">(Preview) Tax Service Dataverse datasources support</span></span>
      - <span data-ttu-id="fd554-117">(Vorschau) Globalisierungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="fd554-117">(Preview) Globalization features</span></span>

5. <span data-ttu-id="fd554-118">Melden Sie sich mit einem Mandantenadministratorkonto bei RCS an.</span><span class="sxs-lookup"><span data-stu-id="fd554-118">Sign in to RCS using a tenant admin account.</span></span>
6. <span data-ttu-id="fd554-119">Gehen Sie zu **Elektronische Berichterstellung** > **Verbundene Anwendungen**.</span><span class="sxs-lookup"><span data-stu-id="fd554-119">Go to **Electronic reporting** > **Connected applications**.</span></span> 
7. <span data-ttu-id="fd554-120">Wählen Sie **Neu**, um einen Datensatz hinzuzufügen und geben Sie die folgenden Feldinformationen ein.</span><span class="sxs-lookup"><span data-stu-id="fd554-120">Select **New** to add a record, and enter the following field information.</span></span> 

   - <span data-ttu-id="fd554-121">Geben Sie im Feld **Name** einen Namen ein.</span><span class="sxs-lookup"><span data-stu-id="fd554-121">In the **Name** field, enter a name.</span></span>
   - <span data-ttu-id="fd554-122">Wählen Sie im Feld **Typ** die **Dataverse** aus.</span><span class="sxs-lookup"><span data-stu-id="fd554-122">In the **Type** field, select **Dataverse**.</span></span>
   - <span data-ttu-id="fd554-123">Geben Sie im Feld **Anwendung** Ihre Dataverse-URL ein.</span><span class="sxs-lookup"><span data-stu-id="fd554-123">In the **Application** field, enter your Dataverse URL.</span></span>
   - <span data-ttu-id="fd554-124">Geben Sie im Feld **Mandant** Ihren Mandanten ein.</span><span class="sxs-lookup"><span data-stu-id="fd554-124">In the **Tenant** field, enter your tenant.</span></span>
   - <span data-ttu-id="fd554-125">Geben Sie im Feld **Benutzerdefinierte URL** Ihre Dataverse-URL ein und fügen Sie „/api/data/v9.1“ an.</span><span class="sxs-lookup"><span data-stu-id="fd554-125">In the **Custom URL** field, enter your Dataverse URL and append it with "/api/data/v9.1".</span></span>

8. <span data-ttu-id="fd554-126">Wählen Sie **Verbindung prüfen** und beenden Sie den Verbindungsvorgang.</span><span class="sxs-lookup"><span data-stu-id="fd554-126">Select **Check connection**, and finish the connection process.</span></span> 

   <span data-ttu-id="fd554-127">[![Schaltfläche „Verbindung prüfen“](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)</span><span class="sxs-lookup"><span data-stu-id="fd554-127">[![Check connection button](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)</span></span>

9. <span data-ttu-id="fd554-128">Gehen Sie zu **Elektronische Berichterstellung** > **Steuerkonfigurationen** und importieren Sie Steuerkonfigurationen aus [Steuerkonfigurationen](https://go.microsoft.com/fwlink/?linkid=2158352).</span><span class="sxs-lookup"><span data-stu-id="fd554-128">Go to **Electronic reporting** > **Tax configurations**, and import tax configurations from [Tax configurations](https://go.microsoft.com/fwlink/?linkid=2158352).</span></span>

   <span data-ttu-id="fd554-129">[![Seite „Steuerkonfigurationen“, Steuerdatenmodellstruktur](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)</span><span class="sxs-lookup"><span data-stu-id="fd554-129">[![Tax configurations page, Tax data model tree](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)</span></span>

10. <span data-ttu-id="fd554-130">Gehen Sie zu **Modellzuordnung steuerpflichtiges Dokument** oder zu **Dataverse Modellzuordnung**, wenn Sie eine Microsoft-Konfiguration verwenden, und wählen Sie im Feld **Verbundene Anwendung** den Datensatz aus, den Sie in Schritt 7 erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="fd554-130">Go to the **Taxable document model mapping**, or **Dataverse Model Mapping** if you are using a Microsoft configuration, and in the **Connected application** field, select the record that you created in step 7.</span></span>
11. <span data-ttu-id="fd554-131">Legen Sie die **Standard für Modellzuordnung** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="fd554-131">Set **Default for model mapping** to **Yes**.</span></span>

   <span data-ttu-id="fd554-132">[![Seite „Modellzuordnung“](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)</span><span class="sxs-lookup"><span data-stu-id="fd554-132">[![Model mapping page](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
