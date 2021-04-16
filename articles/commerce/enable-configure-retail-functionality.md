---
title: Startdaten in neuen Commerce-Umgebungen initialisieren
description: In diesem Artikel werden die Daten beschrieben, die im Rahmen des Initialisierungsprozesses für Dynamics 365 Commerce erstellt werden.
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 9f534410b21fd97554f4e038bb14eebd5f887130
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792582"
---
# <a name="initialize-seed-data-in-new-commerce-environments"></a><span data-ttu-id="d2b8f-103">Startdaten in neuen Commerce-Umgebungen initialisieren</span><span class="sxs-lookup"><span data-stu-id="d2b8f-103">Initialize seed data in new Commerce environments</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d2b8f-104">In diesem Artikel werden die Daten beschrieben, die im Rahmen des Initialisierungsprozesses für Dynamics 365 Commerce erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="d2b8f-104">This article describes the data that's created as part of the initialization process for Dynamics 365 Commerce.</span></span>

<span data-ttu-id="d2b8f-105">Nachdem die Commerce-Lösung über Microsoft Dynamics Lifecycle Services (LCS) bereitgestellt wurde, müssen Sie die Commerce-Konfiguration initialisieren, um die grundlegenden Konfigurationsdaten zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d2b8f-105">After the Commerce solution has been deployed through Microsoft Dynamics Lifecycle Services (LCS), you must initialize the Commerce configuration to create the basic configuration data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d2b8f-106">Bevor Sie die Commerce-Konfiguration initialisieren, überprüfen Sie, ob Sie eine Sprache und eine Postadresse für jede juristische Person angegeben haben, für die Sie Geschäfte einrichten werden.</span><span class="sxs-lookup"><span data-stu-id="d2b8f-106">Before you initialize the commerce configuration, make sure that you've specified a language and a postal address for each legal entity where you will set up stores.</span></span> <span data-ttu-id="d2b8f-107">Dieser Schritt muss für jede juristische Person abgeschlossen werden, die Sie für Commerce verwenden.</span><span class="sxs-lookup"><span data-stu-id="d2b8f-107">This step must be completed for each legal entity that you use for commerce.</span></span>

<span data-ttu-id="d2b8f-108">Um die Konfiguration zu initialisieren, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="d2b8f-108">To initialize the configuration, follow these steps.</span></span>

1. <span data-ttu-id="d2b8f-109">Starten Sie den Commerce-Client.</span><span class="sxs-lookup"><span data-stu-id="d2b8f-109">Start the Commerce client.</span></span>
2. <span data-ttu-id="d2b8f-110">Klicken Sie auf **Einzelhandel und Handel** &gt; **Zentralverwaltungseinrichtung** &gt; **Parameter** &gt; **Commerce-Parameter**.</span><span class="sxs-lookup"><span data-stu-id="d2b8f-110">Click **Retail and Commerce** &gt; **Headquarters setup** &gt; **Parameters** &gt; **Commerce parameters**.</span></span>
3. <span data-ttu-id="d2b8f-111">Klicken Sie auf **Initialisieren**.</span><span class="sxs-lookup"><span data-stu-id="d2b8f-111">Click **Initialize**.</span></span>

<span data-ttu-id="d2b8f-112">Durch die Initialisierung werden die folgenden Standardkonfigurationsdaten erstellt:</span><span class="sxs-lookup"><span data-stu-id="d2b8f-112">Initialization creates the following default configuration data:</span></span>

- <span data-ttu-id="d2b8f-113">Aufträge und Unteraufträge für Commerce-Steuerprogramm</span><span class="sxs-lookup"><span data-stu-id="d2b8f-113">Commerce scheduler jobs and subjobs</span></span>
- <span data-ttu-id="d2b8f-114">Handelskanalschema</span><span class="sxs-lookup"><span data-stu-id="d2b8f-114">Commerce channel schema</span></span>
- <span data-ttu-id="d2b8f-115">Vertriebszeitpläne für Commerce</span><span class="sxs-lookup"><span data-stu-id="d2b8f-115">Commerce distribution schedules</span></span>
- <span data-ttu-id="d2b8f-116">Standard-Bildschirmlayouts mit Schaltflächenrastern, Bildern und Themen</span><span class="sxs-lookup"><span data-stu-id="d2b8f-116">Default screen layouts, which include button grids, images, and themes</span></span>
- <span data-ttu-id="d2b8f-117">Zeitzoneninformation</span><span class="sxs-lookup"><span data-stu-id="d2b8f-117">Time zone information</span></span>
- <span data-ttu-id="d2b8f-118">Verkaufsstellen(POS)-Vorgänge</span><span class="sxs-lookup"><span data-stu-id="d2b8f-118">Point-of-sale (POS) operations</span></span>
- <span data-ttu-id="d2b8f-119">POS-Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="d2b8f-119">POS permissions</span></span>
- <span data-ttu-id="d2b8f-120">Kanalberichte</span><span class="sxs-lookup"><span data-stu-id="d2b8f-120">Channel reports</span></span>
- <span data-ttu-id="d2b8f-121">Attributmetadaten</span><span class="sxs-lookup"><span data-stu-id="d2b8f-121">Attribute metadata</span></span>
- <span data-ttu-id="d2b8f-122">Entitätsprüfungsvorlagen</span><span class="sxs-lookup"><span data-stu-id="d2b8f-122">Entity validation templates</span></span>
- <span data-ttu-id="d2b8f-123">Batchauftrag zum Löschen der Commerce Data Exchange-Sitzungshistorie</span><span class="sxs-lookup"><span data-stu-id="d2b8f-123">Batch job to purge Commerce Data Exchange session history</span></span>

<span data-ttu-id="d2b8f-124">Darüber hinaus ist das Protokollieren in Zusammenhang mit der Zahlungskartenindustrie (PCI) für die Commerce-Datenbank aktiviert.</span><span class="sxs-lookup"><span data-stu-id="d2b8f-124">Additionally, logging that is related to the payment card industry (PCI) is enabled for the Commerce database.</span></span>

> [!NOTE]
> <span data-ttu-id="d2b8f-125">Es gibt eine Option, um das Commerce-Steuerprogramm separat zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="d2b8f-125">There is an option to separately configure the Commerce scheduler.</span></span> <span data-ttu-id="d2b8f-126">Mit dieser Option können Sie die Commerce-Steuerprogramm-Konfiguration auf die Standardeinstellungen zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="d2b8f-126">This option lets you reset the Commerce scheduler configuration to its default settings.</span></span>

<span data-ttu-id="d2b8f-127">Nachdem die Initialisierung abgeschlossen wurde, müssen Sie zusätzliche Commerce-Daten konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="d2b8f-127">After initialization is completed, you must configure additional commerce data.</span></span> <span data-ttu-id="d2b8f-128">Im Folgenden finden Sie einige Beispiele hierfür:</span><span class="sxs-lookup"><span data-stu-id="d2b8f-128">Here are some examples:</span></span>

- <span data-ttu-id="d2b8f-129">Handelsparameter</span><span class="sxs-lookup"><span data-stu-id="d2b8f-129">Commerce parameters</span></span>
- <span data-ttu-id="d2b8f-130">Handelsplanungsparameter</span><span class="sxs-lookup"><span data-stu-id="d2b8f-130">Commerce scheduler parameters</span></span>
- <span data-ttu-id="d2b8f-131">Commerce-Kanäle</span><span class="sxs-lookup"><span data-stu-id="d2b8f-131">Commerce channels</span></span>
- <span data-ttu-id="d2b8f-132">Register und Geräte</span><span class="sxs-lookup"><span data-stu-id="d2b8f-132">Registers and devices</span></span>
- <span data-ttu-id="d2b8f-133">Sortimente</span><span class="sxs-lookup"><span data-stu-id="d2b8f-133">Assortments</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]