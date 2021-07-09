---
title: Aktivieren von Power BI für die Globale Bestandsbuchhaltung
description: Dieses Thema beschreibt, wie Sie Microsoft Power BI für die Globale Bestandsbuchhaltung aktivieren.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d7979ed18b98ee6133774cd91bc866d6fca92d5f
ms.sourcegitcommit: eceae470f4ae58000ec33fea34db34b7a7a1af43
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/18/2021
ms.locfileid: "6273161"
---
# <a name="enable-power-bi-for-global-inventory-accounting"></a><span data-ttu-id="68fc1-103">Aktivieren von Power BI für die Globale Bestandsbuchhaltung</span><span class="sxs-lookup"><span data-stu-id="68fc1-103">Enable Power BI for Global Inventory Accounting</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="68fc1-104">Sie können Kacheln, Dashboards und Berichte von Ihrem [PowerBI.com](https://powerbi.com/)-Konto an Ihren Arbeitsbereich der Microsoft Dynamics 365-Anwendung anheften.</span><span class="sxs-lookup"><span data-stu-id="68fc1-104">You can pin tiles, dashboards, and reports from your [PowerBI.com](https://powerbi.com/) account to your Microsoft Dynamics 365 application workspace.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="68fc1-105">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="68fc1-105">Prerequisites</span></span>

<span data-ttu-id="68fc1-106">Die folgenden Voraussetzungen müssen vorhanden sein, bevor Sie das Power BI-Reporting aktivieren können:</span><span class="sxs-lookup"><span data-stu-id="68fc1-106">The following prerequisites must be in place before you can enable Power BI reporting:</span></span>

- <span data-ttu-id="68fc1-107">Sie müssen ein Systemadministrator in der Dynamics 365-Anwendung sein.</span><span class="sxs-lookup"><span data-stu-id="68fc1-107">You must be a system administrator in the Dynamics 365 application.</span></span>
- <span data-ttu-id="68fc1-108">Sie müssen ein [PowerBI.com](https://powerbi.com/)-Konto haben.</span><span class="sxs-lookup"><span data-stu-id="68fc1-108">You must have a [PowerBI.com](https://powerbi.com/) account.</span></span>
- <span data-ttu-id="68fc1-109">Sie müssen mindestens ein Dashboard und einen Bericht in Ihrem Power BI-Konto haben.</span><span class="sxs-lookup"><span data-stu-id="68fc1-109">You must have at least one dashboard and one report in your Power BI account.</span></span>
- <span data-ttu-id="68fc1-110">Sie müssen ein Administrator für Ihr Azure Active Directory-Konto (Azure AD) sein.</span><span class="sxs-lookup"><span data-stu-id="68fc1-110">You must be an administrator for your Azure Active Directory (Azure AD) account.</span></span>
- <span data-ttu-id="68fc1-111">Die Azure AD-Domäne muss die gleiche Domäne sein, die Sie für Ihr [PowerBI.com](https://powerbi.com/)-Konto verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="68fc1-111">The Azure AD domain must be the same domain that you used for your [PowerBI.com](https://powerbi.com/) account.</span></span>

## <a name="setup"></a><span data-ttu-id="68fc1-112">Einstellung</span><span class="sxs-lookup"><span data-stu-id="68fc1-112">Setup</span></span>

<span data-ttu-id="68fc1-113">Um die Power BI-Integration festzulegen, folgen Sie diesen Schritten.</span><span class="sxs-lookup"><span data-stu-id="68fc1-113">To set up the Power BI integration, follow these steps.</span></span>

1. <span data-ttu-id="68fc1-114">Melden Sie sich bei [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) an.</span><span class="sxs-lookup"><span data-stu-id="68fc1-114">Sign in to [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index).</span></span>
1. <span data-ttu-id="68fc1-115">Gehen Sie zu **Gemeinsame Anlagenbibliothek**, wählen Sie **Power BI Berichtsmodell** als Anlagentyp und laden Sie das Paket **Globale Bestandsbuchhaltung** herunter.</span><span class="sxs-lookup"><span data-stu-id="68fc1-115">Go to **Shared asset library**, select **Power BI report model** as the asset type, and download the **Global Inventory Accounting** package.</span></span> 
1. <span data-ttu-id="68fc1-116">Melden Sie sich bei [PowerBI.com](https://app.powerbi.com/) an und laden Sie die Berichtsdatei **Globale Bestandsbuchhaltung** Power BI hoch, indem Sie die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="68fc1-116">Sign in to [PowerBI.com](https://app.powerbi.com/), and upload the **Global Inventory Accounting** Power BI report file by following these steps:</span></span>

    1. <span data-ttu-id="68fc1-117">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="68fc1-117">Select **New**.</span></span>
    1. <span data-ttu-id="68fc1-118">Wählen Sie **Hochladen einer Datei**.</span><span class="sxs-lookup"><span data-stu-id="68fc1-118">Select **Upload a file**.</span></span>
    1. <span data-ttu-id="68fc1-119">Wählen Sie die Berichtsdatei **Globale Bestandsbuchhaltung** Power BI.</span><span class="sxs-lookup"><span data-stu-id="68fc1-119">Select the **Global Inventory Accounting** Power BI report file.</span></span>

1. <span data-ttu-id="68fc1-120">Konfigurieren Sie den Bericht **Globale Bestandsbuchhaltung** Power BI, indem Sie die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="68fc1-120">Configure the **Global Inventory Accounting** Power BI report by following these steps:</span></span>

    1. <span data-ttu-id="68fc1-121">Gehen Sie zu **Mein Arbeitsbereich**, suchen Sie das Dataset für Globale Bestandsbuchhaltung und wählen Sie dann im Menü **Optionen** die Option **Einstellungen**.</span><span class="sxs-lookup"><span data-stu-id="68fc1-121">Go to **My workspace**, find the dataset for Global Inventory Accounting, and then, on the **Options** menu, select **Settings**.</span></span>
    1. <span data-ttu-id="68fc1-122">Erweitern Sie in **Einstellungen für Globale Bestandsbuchhaltung** die Option **Parameter** und aktualisieren Sie alle Parameter wie gewünscht.</span><span class="sxs-lookup"><span data-stu-id="68fc1-122">In **Settings for Global inventory accounting**, expand **Parameters**, and update all parameters as required.</span></span>

1. <span data-ttu-id="68fc1-123">Registrieren Sie die Anwendung wie in [Konfigurieren der PowerBI.com-Integration](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md#registration-process) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="68fc1-123">Register the application as described in [Configure PowerBI.com integration](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md#registration-process).</span></span>
1. <span data-ttu-id="68fc1-124">Integrieren Sie die Berichtsdatei **Globale Bestandsbuchhaltung** Power BI in Dynamics 365 Supply Chain Management, indem Sie die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="68fc1-124">Integrate the **Global Inventory Accounting** Power BI report file into Dynamics 365 Supply Chain Management by following these steps:</span></span>

    1. <span data-ttu-id="68fc1-125">Gehen Sie zu **Systemverwaltung \> Einrichten \> PowerBI.com-Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="68fc1-125">Go to **System administration \> Setup \> PowerBI.com configuration**.</span></span>
    1. <span data-ttu-id="68fc1-126">Wählen Sie **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="68fc1-126">Select **Edit**.</span></span>
    1. <span data-ttu-id="68fc1-127">Wählen Sie **PowerBI.com-Integration aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="68fc1-127">Select **Enable PowerBI.Com integration**.</span></span>
    1. <span data-ttu-id="68fc1-128">Geben Sie in das Feld **Anwendungs-ID** die Anwendungs-ID ein.</span><span class="sxs-lookup"><span data-stu-id="68fc1-128">In the **Application ID** field, enter the application ID.</span></span>
    1. <span data-ttu-id="68fc1-129">Geben Sie in das Feld **Anwendungsschlüssel** den Anwendungsschlüssel ein.</span><span class="sxs-lookup"><span data-stu-id="68fc1-129">In the **Application key** field, enter the application key.</span></span>
    1. <span data-ttu-id="68fc1-130">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="68fc1-130">Select **Save**.</span></span>

1. <span data-ttu-id="68fc1-131">Aktualisieren Sie die Seite, so dass das Dialogfeld Power BI zur Anmeldung erscheint.</span><span class="sxs-lookup"><span data-stu-id="68fc1-131">Refresh the page so that the Power BI sign-in dialog box appears.</span></span>
1. <span data-ttu-id="68fc1-132">Wählen Sie auf der Registerkarte **Optionen** die Option **Berichtskatalog öffnen** und wählen Sie dann die Berichtsdatei **Globale Bestandsbuchhaltung** Power BI, die Sie zuvor hochgeladen haben.</span><span class="sxs-lookup"><span data-stu-id="68fc1-132">On the **Options** tab, select **Open report catalog**, and then select the **Global Inventory Accounting** Power BI report file that you uploaded earlier.</span></span>
1. <span data-ttu-id="68fc1-133">Aktualisieren Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="68fc1-133">Refresh the page.</span></span> <span data-ttu-id="68fc1-134">Sie sollten sehen, dass Ihr Bericht hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="68fc1-134">You should see that your report has been added.</span></span>
1. <span data-ttu-id="68fc1-135">Wählen Sie unter **Power BI Berichte** den Link **Globale Bestandsbuchhaltung**.</span><span class="sxs-lookup"><span data-stu-id="68fc1-135">Under **Power BI reports**, select the **Global Inventory Accounting** link.</span></span>

<span data-ttu-id="68fc1-136">Weitere Informationen finden Sie unter [Konfigurieren der PowerBI.com-Integration](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md).</span><span class="sxs-lookup"><span data-stu-id="68fc1-136">For more information, see [Configure PowerBI.com integration](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md).</span></span>
