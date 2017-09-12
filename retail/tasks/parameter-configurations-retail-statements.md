--- 
title: " Parameterkonfigurationen für Einzelhandelsauszüge"
description: "Diese Prozedur zeigt Konfigurationen für Einzelhandelsparameter, die sich darauf auswirken, wie Einzelhandelsauszüge erstellt und gebucht werden."
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 731a3ec06efa103ba663df83240c77dfe78bb7cd
ms.contentlocale: de-de
ms.lasthandoff: 08/29/2017

---
# <a name="parameter-configurations-for-retail-statements"></a><span data-ttu-id="8d74e-103"> Parameterkonfigurationen für Einzelhandelsauszüge</span><span class="sxs-lookup"><span data-stu-id="8d74e-103">Parameter configurations for Retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="8d74e-104">Diese Prozedur zeigt Konfigurationen für Einzelhandelsparameter, die sich darauf auswirken, wie Einzelhandelsauszüge erstellt und gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="8d74e-104">This procedure demonstrates configurations for Retail parameters that affect how Retail statements get created and posted.</span></span> <span data-ttu-id="8d74e-105">Für diese Prozedur wird das Demo-Unternehmen USRT verwendet.</span><span class="sxs-lookup"><span data-stu-id="8d74e-105">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="8d74e-106">Navigieren Sie zu "Einzelhandel und Handel" > "Hauptsitz einrichten" > "Parameter" > "Einzelhandelsparameter".</span><span class="sxs-lookup"><span data-stu-id="8d74e-106">Go to Retail and commerce > Headquarters setup  > Parameters > Retail parameters.</span></span>
2. <span data-ttu-id="8d74e-107">Klicken Sie auf die Registerkarte "Buchung".</span><span class="sxs-lookup"><span data-stu-id="8d74e-107">Click the Posting tab.</span></span>
    * <span data-ttu-id="8d74e-108">Wählen Sie "Ja" aus, wenn Sie die periodischen Rabattbeträge speziell buchen möchten.</span><span class="sxs-lookup"><span data-stu-id="8d74e-108">Select "Yes" if you want to post the periodic discount amounts specifically.</span></span>  
    * <span data-ttu-id="8d74e-109">Wählen Sie "Standard" aus, um Standardkonten zu verwenden, oder "Periodisch", wenn Sie definieren möchten, welches Konto für jeden periodischen Rabatt zu verwenden ist.</span><span class="sxs-lookup"><span data-stu-id="8d74e-109">Select "Standard" to use default accounts, or select "Periodic" if you want to define which account to use for each periodic discount.</span></span>  
    * <span data-ttu-id="8d74e-110">Wählen Sie "Zusammenfassung" aus, wenn Bestandspositionen aggregiert werden sollen, wann immer möglich.</span><span class="sxs-lookup"><span data-stu-id="8d74e-110">Select "Summary" if inventory lines should get aggregated whenever possible.</span></span>  
    * <span data-ttu-id="8d74e-111">Wählen Sie "Ja" aus, wenn Rechnungen und Zahlungen als Teil des Auszugsbuchungsprozesses automatisch ausgeglichen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8d74e-111">Select "Yes" if Invoices and Payments should get automatically settled as part of the Statement posting process.</span></span>  
    * <span data-ttu-id="8d74e-112">Wählen Sie "Ja" aus, wenn Ablage in Tresor-Buchungen aggregiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8d74e-112">Select "Yes" if Safe drop transactions should get aggregated.</span></span>  
    * <span data-ttu-id="8d74e-113">Wählen Sie "Ja" aus, wenn Bankeinzahlungs-Buchungen aggregiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8d74e-113">Select "Yes" if Bank drop transactions should get aggregated.</span></span>  
    * <span data-ttu-id="8d74e-114">Wählen Sie "Ja" aus, um eine Aggregation für Auszugsbuchung zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="8d74e-114">Select "Yes" to turn aggregation on for Statement posting.</span></span>  
    * <span data-ttu-id="8d74e-115">Wählen Sie "Ja" aus, um Aufträge parallel zu erstellen und zu verarbeiten, wenn Aufstellungen gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="8d74e-115">Select "Yes" to create and process orders in parallel when statements are posted.</span></span>  
    * <span data-ttu-id="8d74e-116">Geben Sie die Höchstmenge der Aufträge ein, die in jeder Stapelverarbeitungsaufgabe bearbeitet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8d74e-116">Enter the maximum orders to be processed in each batch job task.</span></span>  
3. <span data-ttu-id="8d74e-117">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="8d74e-117">Click Save.</span></span>


