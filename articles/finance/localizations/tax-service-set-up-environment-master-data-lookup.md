---
title: Eine Umgebung für die Masterdatensuche einrichten
description: In diesem Thema wird erläutert, wie Sie Ihre Umgebung für die Verwendung der Masterdaten-Suchfunktion für die Steuerberechnung einrichten.
author: kai-cloud
ms.date: 04/21/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: e4aa941c57e8c31793d6db8ae87140cd1bb1a82b
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021343"
---
# <a name="set-up-an-environment-for-master-data-lookup"></a><span data-ttu-id="32525-103">Eine Umgebung für die Masterdatensuche einrichten</span><span class="sxs-lookup"><span data-stu-id="32525-103">Set up an environment for master data lookup</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="32525-104">In diesem Thema wird erläutert, wie Sie Ihre Umgebung für die Verwendung der Masterdaten-Suchfunktion für die Steuerberechnung einrichten.</span><span class="sxs-lookup"><span data-stu-id="32525-104">This topic explains how to set up your environment to use the Tax Calculation master data lookup functionality.</span></span>

1. <span data-ttu-id="32525-105">Richten Sie die Integration von Power Platform in Lifecycle Services (LCS) ein.</span><span class="sxs-lookup"><span data-stu-id="32525-105">Set up power platform integration in Lifecycle Services (LCS).</span></span> <span data-ttu-id="32525-106">Weitere Informationen finden Sie unter [Integration von Microsoft Power Platform – Übersicht über Add-Ins](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).</span><span class="sxs-lookup"><span data-stu-id="32525-106">For more information, see [Microsoft Power Platform integration - Add-ins overview](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).</span></span>
2. <span data-ttu-id="32525-107">Richten Sie Dynamics 365 Finance und Microsoft Dataverse ein.</span><span class="sxs-lookup"><span data-stu-id="32525-107">Set up Dynamics 365 Finance and Microsoft Dataverse.</span></span> <span data-ttu-id="32525-108">Weitere Informationen finden Sie unter [Die Lösung erhalten](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) und [Authentifizierung und Autorisierung](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).</span><span class="sxs-lookup"><span data-stu-id="32525-108">For more information, see [Getting the solution](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) and [Authentication and authorization](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).</span></span>
3. <span data-ttu-id="32525-109">Legen Sie die folgenden Entitäten fest.</span><span class="sxs-lookup"><span data-stu-id="32525-109">Set up the following entities.</span></span> <span data-ttu-id="32525-110">Weitere Informationen finden Sie unter [Aktivieren von virtuellen Entitäten](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#enabling-virtual-entities).</span><span class="sxs-lookup"><span data-stu-id="32525-110">For more information, see [Enabling virtual entities](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#enabling-virtual-entities).</span></span>
      - <span data-ttu-id="32525-111">CompanyInfoEntity</span><span class="sxs-lookup"><span data-stu-id="32525-111">CompanyInfoEntity</span></span>
      - <span data-ttu-id="32525-112">CurrencyEntity</span><span class="sxs-lookup"><span data-stu-id="32525-112">CurrencyEntity</span></span>
      - <span data-ttu-id="32525-113">CustCustomerV3Entity</span><span class="sxs-lookup"><span data-stu-id="32525-113">CustCustomerV3Entity</span></span>
      - <span data-ttu-id="32525-114">DeliveryTermsEntity</span><span class="sxs-lookup"><span data-stu-id="32525-114">DeliveryTermsEntity</span></span>
      - <span data-ttu-id="32525-115">EcoResProductCategoryEntity</span><span class="sxs-lookup"><span data-stu-id="32525-115">EcoResProductCategoryEntity</span></span>
      - <span data-ttu-id="32525-116">EcoResReleasedProductV2Entity</span><span class="sxs-lookup"><span data-stu-id="32525-116">EcoResReleasedProductV2Entity</span></span>
      - <span data-ttu-id="32525-117">LogisticsAddressCityEntity</span><span class="sxs-lookup"><span data-stu-id="32525-117">LogisticsAddressCityEntity</span></span>
      - <span data-ttu-id="32525-118">LogisticsAddressCountryRegionTranslationEntity</span><span class="sxs-lookup"><span data-stu-id="32525-118">LogisticsAddressCountryRegionTranslationEntity</span></span>
      - <span data-ttu-id="32525-119">LogisticsAddressStateEntity</span><span class="sxs-lookup"><span data-stu-id="32525-119">LogisticsAddressStateEntity</span></span>
      - <span data-ttu-id="32525-120">PurchProcurementChargeCDSEntity</span><span class="sxs-lookup"><span data-stu-id="32525-120">PurchProcurementChargeCDSEntity</span></span>
      - <span data-ttu-id="32525-121">SalesChargeCDSEntity</span><span class="sxs-lookup"><span data-stu-id="32525-121">SalesChargeCDSEntity</span></span>
      - <span data-ttu-id="32525-122">TaxGroupEntity</span><span class="sxs-lookup"><span data-stu-id="32525-122">TaxGroupEntity</span></span>
      - <span data-ttu-id="32525-123">TaxItemGroupHeadingEntity</span><span class="sxs-lookup"><span data-stu-id="32525-123">TaxItemGroupHeadingEntity</span></span>
      - <span data-ttu-id="32525-124">VendVendorV2Entity</span><span class="sxs-lookup"><span data-stu-id="32525-124">VendVendorV2Entity</span></span>
4. <span data-ttu-id="32525-125">Richten Sie den Dynamics 365 Regulatory Configuration Service (RCS) ein.</span><span class="sxs-lookup"><span data-stu-id="32525-125">Set up the Dynamics 365 Regulatory Configuration Service (RCS).</span></span> 
5. <span data-ttu-id="32525-126">Erstellen Sie eine Serviceanforderung für Microsoft, um das Flighting der folgenden Funktionen zu ermöglichen:</span><span class="sxs-lookup"><span data-stu-id="32525-126">Create a service request for Microsoft to enable flighting of the following features:</span></span>

      - <span data-ttu-id="32525-127">ERCdsFeature</span><span class="sxs-lookup"><span data-stu-id="32525-127">ERCdsFeature</span></span>
      - <span data-ttu-id="32525-128">TaxServiceCDSFeature</span><span class="sxs-lookup"><span data-stu-id="32525-128">TaxServiceCDSFeature</span></span>

6. <span data-ttu-id="32525-129">Gehen Sie in den Arbeitsbereich **Funktionsverwaltung** und aktivieren Sie die folgenden Funktionen:</span><span class="sxs-lookup"><span data-stu-id="32525-129">Go to the **Feature management** workspace, and enable the following features:</span></span>

      - <span data-ttu-id="32525-130">(Vorschau) Unterstützung von Dataverse-Datenquellen der elektronischen Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="32525-130">(Preview) Electronic reporting Dataverse datasources support</span></span>
      - <span data-ttu-id="32525-131">(Vorschauversion) Unterstützung für Dataverse-Datenquellen des Steuerdienstes</span><span class="sxs-lookup"><span data-stu-id="32525-131">(Preview) Tax Service Dataverse datasources support</span></span>
      - <span data-ttu-id="32525-132">(Vorschau) Globalisierungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="32525-132">(Preview) Globalization features</span></span>

5. <span data-ttu-id="32525-133">Melden Sie sich mit einem Mandantenadministratorkonto bei RCS an.</span><span class="sxs-lookup"><span data-stu-id="32525-133">Sign in to RCS using a tenant admin account.</span></span>
6. <span data-ttu-id="32525-134">Gehen Sie zu **Elektronische Berichterstellung** > **Verbundene Anwendungen**.</span><span class="sxs-lookup"><span data-stu-id="32525-134">Go to **Electronic reporting** > **Connected applications**.</span></span> 
7. <span data-ttu-id="32525-135">Wählen Sie **Neu**, um einen Datensatz hinzuzufügen und geben Sie die folgenden Feldinformationen ein.</span><span class="sxs-lookup"><span data-stu-id="32525-135">Select **New** to add a record, and enter the following field information.</span></span> 

   - <span data-ttu-id="32525-136">Geben Sie im Feld **Name** einen Namen ein.</span><span class="sxs-lookup"><span data-stu-id="32525-136">In the **Name** field, enter a name.</span></span>
   - <span data-ttu-id="32525-137">Wählen Sie im Feld **Typ** die **Dataverse** aus.</span><span class="sxs-lookup"><span data-stu-id="32525-137">In the **Type** field, select **Dataverse**.</span></span>
   - <span data-ttu-id="32525-138">Geben Sie im Feld **Anwendung** Ihre Dataverse-URL ein.</span><span class="sxs-lookup"><span data-stu-id="32525-138">In the **Application** field, enter your Dataverse URL.</span></span>
   - <span data-ttu-id="32525-139">Geben Sie im Feld **Mandant** Ihren Mandanten ein.</span><span class="sxs-lookup"><span data-stu-id="32525-139">In the **Tenant** field, enter your tenant.</span></span>
   - <span data-ttu-id="32525-140">Geben Sie im Feld **Benutzerdefinierte URL** Ihre Dataverse-URL ein und fügen Sie „/api/data/v9.1“ an.</span><span class="sxs-lookup"><span data-stu-id="32525-140">In the **Custom URL** field, enter your Dataverse URL and append it with "/api/data/v9.1".</span></span>

8. <span data-ttu-id="32525-141">Wählen Sie **Verbindung prüfen** und beenden Sie den Verbindungsvorgang.</span><span class="sxs-lookup"><span data-stu-id="32525-141">Select **Check connection**, and finish the connection process.</span></span> 

   <span data-ttu-id="32525-142">[![Schaltfläche „Verbindung prüfen“](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)</span><span class="sxs-lookup"><span data-stu-id="32525-142">[![Check connection button](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)</span></span>

9. <span data-ttu-id="32525-143">Gehen Sie zu **Elektronische Berichterstellung** > **Steuerkonfigurationen** und importieren Sie Steuerkonfigurationen aus [Steuerkonfigurationen](https://go.microsoft.com/fwlink/?linkid=2158352).</span><span class="sxs-lookup"><span data-stu-id="32525-143">Go to **Electronic reporting** > **Tax configurations**, and import tax configurations from [Tax configurations](https://go.microsoft.com/fwlink/?linkid=2158352).</span></span>

   <span data-ttu-id="32525-144">[![Seite „Steuerkonfigurationen“, Steuerdatenmodellstruktur](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)</span><span class="sxs-lookup"><span data-stu-id="32525-144">[![Tax configurations page, Tax data model tree](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)</span></span>

10. <span data-ttu-id="32525-145">Gehen Sie zu **Modellzuordnung steuerpflichtiges Dokument** oder zu **Dataverse Modellzuordnung**, wenn Sie eine Microsoft-Konfiguration verwenden, und wählen Sie im Feld **Verbundene Anwendung** den Datensatz aus, den Sie in Schritt 7 erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="32525-145">Go to the **Taxable document model mapping**, or **Dataverse Model Mapping** if you are using a Microsoft configuration, and in the **Connected application** field, select the record that you created in step 7.</span></span>
11. <span data-ttu-id="32525-146">Legen Sie die **Standard für Modellzuordnung** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="32525-146">Set **Default for model mapping** to **Yes**.</span></span>

   <span data-ttu-id="32525-147">[![Seite „Modellzuordnung“](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)</span><span class="sxs-lookup"><span data-stu-id="32525-147">[![Model mapping page](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
