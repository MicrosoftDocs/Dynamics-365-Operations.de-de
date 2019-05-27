---
title: Startdaten in neuen Retail-Umgebungen initialisieren
description: In diesem Artikel werden die Daten beschrieben, die im Rahmen des Initialisierungsprozesses für Microsoft Dynamics 365 for Retail erstellt werden.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 52f0c52748958f0bebb6c40df01cfac10c0ed427
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556897"
---
# <a name="initialize-seed-data-in-new-retail-environments"></a><span data-ttu-id="da2b8-103">Startwertdaten in Retail-Umgebungen initialisieren</span><span class="sxs-lookup"><span data-stu-id="da2b8-103">Initialize seed data in new Retail environments</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="da2b8-104">In diesem Artikel werden die Daten beschrieben, die im Rahmen des Initialisierungsprozesses für Microsoft Dynamics 365 for Retail erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="da2b8-104">This article describes the data that's created as part of the initialization process for Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="da2b8-105">Nachdem die Retail-Lösung über Microsoft Dynamics Lifecycle Services (LCS) bereitgestellt wurde, müssen Sie die Einzelhandelskonfiguration initialisieren, um die grundlegenden Konfigurationsdaten zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="da2b8-105">After the Retail solution has been deployed through Microsoft Dynamics Lifecycle Services (LCS), you must initialize the retail configuration to create the basic configuration data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="da2b8-106">Bevor Sie die Einzelhandelskonfiguration initialisieren, überprüfen Sie, ob Sie eine Sprache und eine Postadresse für jede juristische Person angegeben haben, für die Sie Einzelhandelsgeschäfte einrichten werden.</span><span class="sxs-lookup"><span data-stu-id="da2b8-106">Before you initialize the retail configuration, make sure that you've specified a language and a postal address for each legal entity where you will set up retail stores.</span></span> <span data-ttu-id="da2b8-107">Dieser Schritt muss für jede juristische Person abgeschlossen werden, die Sie für Einzelhandel verwenden.</span><span class="sxs-lookup"><span data-stu-id="da2b8-107">This step must be completed for each legal entity that you use for retail.</span></span>

<span data-ttu-id="da2b8-108">Um die Einzelhandelskonfiguration zu initialisieren, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="da2b8-108">To initialize the retail configuration, follow these steps.</span></span>

1. <span data-ttu-id="da2b8-109">Starten Sie den Dynamics 365 for Retail-Client.</span><span class="sxs-lookup"><span data-stu-id="da2b8-109">Start the Dynamics 365 for Retail client.</span></span>
2. <span data-ttu-id="da2b8-110">Klicken Sie auf **Einzelhandel** &gt; **Zentralverwaltungseinrichtun** &gt; **Parameter** &gt; **Einzelhandelsparamete**.</span><span class="sxs-lookup"><span data-stu-id="da2b8-110">Click **Retail** &gt; **Headquarters setup** &gt; **Parameters** &gt; **Retail parameters**.</span></span>
3. <span data-ttu-id="da2b8-111">Klicken Sie auf **Initialisieren**.</span><span class="sxs-lookup"><span data-stu-id="da2b8-111">Click **Initialize**.</span></span>

<span data-ttu-id="da2b8-112">Durch die Initialisierung werden die folgenden Standardkonfigurationsdaten erstellt:</span><span class="sxs-lookup"><span data-stu-id="da2b8-112">Initialization creates the following default configuration data:</span></span>

- <span data-ttu-id="da2b8-113">Einzelhandel-Steuerprogramm-Aufträge und -Unteraufträge</span><span class="sxs-lookup"><span data-stu-id="da2b8-113">Retail scheduler jobs and subjobs</span></span>
- <span data-ttu-id="da2b8-114">Retail Channel-Schema</span><span class="sxs-lookup"><span data-stu-id="da2b8-114">Retail channel schema</span></span>
- <span data-ttu-id="da2b8-115">Einzelhandel-Vertriebszeitpläne</span><span class="sxs-lookup"><span data-stu-id="da2b8-115">Retail distribution schedules</span></span>
- <span data-ttu-id="da2b8-116">Standard-Bildschirmlayouts mit Schaltflächenrastern, Bildern und Themen</span><span class="sxs-lookup"><span data-stu-id="da2b8-116">Default screen layouts, which include button grids, images, and themes</span></span>
- <span data-ttu-id="da2b8-117">Zeitzoneninformation</span><span class="sxs-lookup"><span data-stu-id="da2b8-117">Time zone information</span></span>
- <span data-ttu-id="da2b8-118">Verkaufsstellen(POS)-Vorgänge</span><span class="sxs-lookup"><span data-stu-id="da2b8-118">Point-of-sale (POS) operations</span></span>
- <span data-ttu-id="da2b8-119">POS-Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="da2b8-119">POS permissions</span></span>
- <span data-ttu-id="da2b8-120">Kanalberichte</span><span class="sxs-lookup"><span data-stu-id="da2b8-120">Channel reports</span></span>
- <span data-ttu-id="da2b8-121">Attributmetadaten</span><span class="sxs-lookup"><span data-stu-id="da2b8-121">Attribute metadata</span></span>
- <span data-ttu-id="da2b8-122">Entitätsprüfungsvorlagen</span><span class="sxs-lookup"><span data-stu-id="da2b8-122">Entity validation templates</span></span>
- <span data-ttu-id="da2b8-123">Batchauftrag zum Löschen der Commerce Data Exchange-Sitzungshistorie</span><span class="sxs-lookup"><span data-stu-id="da2b8-123">Batch job to purge Commerce Data Exchange session history</span></span>

<span data-ttu-id="da2b8-124">Darüber hinaus ist das Protokollieren in Zusammenhang mit der Zahlungskartenindustrie (PCI) für die Dynamics 365 for Retail-Datenbank aktiviert.</span><span class="sxs-lookup"><span data-stu-id="da2b8-124">Additionally, logging that is related to the payment card industry (PCI) is enabled for the Dynamics 365 for Retail database.</span></span>

> [!NOTE]
> <span data-ttu-id="da2b8-125">Es gibt eine Option, um das Einzelhandel-Steuerprogramm separat zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="da2b8-125">There is an option to separately configure the Retail scheduler.</span></span> <span data-ttu-id="da2b8-126">Mit dieser Option können Sie die Einzelhandel-Steuerprogramm-Konfiguration auf die Standardeinstellungen zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="da2b8-126">This option lets you reset the Retail scheduler configuration to its default settings.</span></span>

<span data-ttu-id="da2b8-127">Nachdem die Initialisierung abgeschlossen wurde, müssen Sie zusätzliche Einzelhandelsdaten konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="da2b8-127">After initialization is completed, you must configure additional retail data.</span></span> <span data-ttu-id="da2b8-128">Nachfolgend finden Sie einige Beispiele:</span><span class="sxs-lookup"><span data-stu-id="da2b8-128">Here are some examples:</span></span>

- <span data-ttu-id="da2b8-129">Einzelhandelsparameter</span><span class="sxs-lookup"><span data-stu-id="da2b8-129">Retail parameters</span></span>
- <span data-ttu-id="da2b8-130">Einzelhandel-Steuerprogramm-Parameter</span><span class="sxs-lookup"><span data-stu-id="da2b8-130">Retail scheduler parameters</span></span>
- <span data-ttu-id="da2b8-131">Retail Channels</span><span class="sxs-lookup"><span data-stu-id="da2b8-131">Retail channels</span></span>
- <span data-ttu-id="da2b8-132">Register und Geräte</span><span class="sxs-lookup"><span data-stu-id="da2b8-132">Registers and devices</span></span>
- <span data-ttu-id="da2b8-133">Sortimente</span><span class="sxs-lookup"><span data-stu-id="da2b8-133">Assortments</span></span>
