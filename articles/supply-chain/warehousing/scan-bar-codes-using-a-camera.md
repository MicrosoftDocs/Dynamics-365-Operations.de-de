---
title: Strichcodes mithilfe einer Kamera in Dynamics 365 for Finance and Operations – Lagerorte scannen
description: In diesem Thema wird erläutert, wie Sie Dynamics 365 for Finance and Operations – Warehousing einrichten, um Strichcodes mithilfe einer Kamera auf einem mobilen Gerät zu scannen.
author: MarkusFogelberg
manager: AnnBe
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: e78d0a82d3ca66a6912ea1a9517296ca241edf1c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "319430"
---
# <a name="scan-bar-codes-using-a-camera-in-dynamics-365-for-finance-and-operations--warehousing"></a><span data-ttu-id="53edb-103">Strichcodes mithilfe einer Kamera in Dynamics 365 for Finance and Operations – Lagerorte scannen</span><span class="sxs-lookup"><span data-stu-id="53edb-103">Scan bar codes using a camera in Dynamics 365 for Finance and Operations – Warehousing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="53edb-104">In diesem Thema wird erläutert, wie Sie Dynamics 365 for Finance and Operations – Warehousing einrichten, um Strichcodes mithilfe einer Kamera auf einem mobilen Gerät zu scannen.</span><span class="sxs-lookup"><span data-stu-id="53edb-104">This topic explains how to set up Dynamics 365 for Finance and Operations – Warehousing to scan bar codes using a camera on a mobile device.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="53edb-105">Erforderliche Komponenten</span><span class="sxs-lookup"><span data-stu-id="53edb-105">Prerequisites</span></span>
<span data-ttu-id="53edb-106">Damit Sie diese Funktion verwenden können, müssen Sie 1.2.0.0 Version des Warehousings eingerichtet haben, und Ihr Gerät muss eine Kamera haben.</span><span class="sxs-lookup"><span data-stu-id="53edb-106">To use this feature, you need to have version 1.2.0.0 of Warehousing installed, and your device must have a camera.</span></span> <span data-ttu-id="53edb-107">Wenn Sie die App nach der Aktualisierung öffnen, werden Sie aufgefordert, Dynamics 365 for Finance and Operations – Warehousing zu erlauben, die Kamera zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="53edb-107">When you open the app after updating, you will be prompted to allow the Dynamics 365 for Finance and Operations – Warehousing application to use the camera.</span></span> <span data-ttu-id="53edb-108">Wenn Ihr Gerät keine Kamera hat, wird keine entsprechende Meldung angezeigt, und Sie können die Kamera nicht als Scanner verwenden.</span><span class="sxs-lookup"><span data-stu-id="53edb-108">If your device doesn’t have a camera, no prompt will be shown, and you will not be able to use a camera as a scanner.</span></span> 

## <a name="setup"></a><span data-ttu-id="53edb-109">Einrichten</span><span class="sxs-lookup"><span data-stu-id="53edb-109">Setup</span></span>
<span data-ttu-id="53edb-110">In der Anzeige der Warehousing-Anwendung können Sie auswählen, ob die Kamera für Scannen von Strichcodes verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="53edb-110">In the Display settings of the Warehousing application, you can select if the camera should be used for bar code scanning.</span></span> <span data-ttu-id="53edb-111">Wenn Sie **Verwenden Sie die Kamera als Scanner** aktivieren, können Sie die Kamera auf jedem Eingabefeld verwenden, bei dem der bevorzugte Eingabemodus auf **Scannen** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="53edb-111">If you enable **Use the camera as scanner**, you can use the camera on every input field that has the preferred input mode set to **Scanning**.</span></span> 

<span data-ttu-id="53edb-112">Um zu steuern, ob ein Eingabefeld gescannt werden soll, legen Sie auf der Seite **Lagerort-App-Feldnamen** in Dynamics 365 for Finance and Operations **Bevorzugter Eingabemodus** auf **Scannen** fest.</span><span class="sxs-lookup"><span data-stu-id="53edb-112">To control whether an input field should be scannable, on the **Warehouse app field names** page in Dynamics 365 for Finance and Operations, set **Preferred input mode** to **Scanning**.</span></span> <span data-ttu-id="53edb-113">Wenn diese Option aktiviert ist, kann eine Kamera für das Scannen in der Warehousing-App verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="53edb-113">When this option is selected, a camera can be used for scanning in the Warehousing app.</span></span> <span data-ttu-id="53edb-114">Informationen darüber, wie Sie App-Feldnamen im Warehousing konfigurieren, finden Sie unter [Konfigurieren Sie App-Feldnamen in der Warehousing-App](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).</span><span class="sxs-lookup"><span data-stu-id="53edb-114">For information about how to configure app field names in Warehousing, see [Configure app field names in Warehousing app](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).</span></span>

## <a name="supported-bar-code-formats"></a><span data-ttu-id="53edb-115">Unterstützte Strichcodeformate</span><span class="sxs-lookup"><span data-stu-id="53edb-115">Supported bar code formats</span></span>
<span data-ttu-id="53edb-116">Die Formate der allgemeinsten Strichcodes einschließlich Code 128 Code 39, Codes 93, EAN-8, EAN-13, UPC-A und QR unterstützt.</span><span class="sxs-lookup"><span data-stu-id="53edb-116">The most common bar code formats are supported, including Code 128, Code 39, Code 93, EAN-8, EAN-13, UPC-E, UPC-A, and QR codes.</span></span> 

## <a name="navigation"></a><span data-ttu-id="53edb-117">Navigieren</span><span class="sxs-lookup"><span data-stu-id="53edb-117">Navigation</span></span>
<span data-ttu-id="53edb-118">Die Kameraseite wird auf jeder Seite verwendet, die im Eingabefeld einen bevorzugten Eingabemodus hat, auf der dem Vorgang festgelegt ist, wenn Sie auf der Kameraseitenverwendung zu den folgenden Optionen navigieren:</span><span class="sxs-lookup"><span data-stu-id="53edb-118">The camera page will be initiated on each page where the input field has the preferred input mode set to Scanning, when you are on the Camera page use the following options to navigate:</span></span>
- <span data-ttu-id="53edb-119">Klicken Sie auf die Schaltfläche "Zurück", um wieder zu den Aufgaben und die Detailseite zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="53edb-119">Click the back button to go back to the Task and details page.</span></span> 
- <span data-ttu-id="53edb-120">Klicken Sie auf den Stift für die Aufgabe und die Detailseite, um zur Seite zu wechseln, in der Sie die Eingabe manuell eingeben können.</span><span class="sxs-lookup"><span data-stu-id="53edb-120">Click the pencil on the Task and details page to go to the page where you can type input manually.</span></span>
- <span data-ttu-id="53edb-121">Klicken Sie auf die Kamera der Aufgabe und auf die Detailseite, um zur Kameraseite zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="53edb-121">Click the camera on the Task and details page to go back to the Camera page.</span></span> 

| <span data-ttu-id="53edb-122">Aufgabe und Detailseite</span><span class="sxs-lookup"><span data-stu-id="53edb-122">Task and details page</span></span> | <span data-ttu-id="53edb-123">Kameraseite</span><span class="sxs-lookup"><span data-stu-id="53edb-123">Camera page</span></span> | 
| :---------------------: | :--------------------: |
| ![Kamera-Scannen-Beispiel-Aufgabe-Detail-Seite](./media/camera-scanning-example-task-detail-page50.png)          | ![Kamera-Scannen-Beispiel-Kamera-Seite-kleiner](./media/camera-scanning-example-camera-page50.png)          |

<span data-ttu-id="53edb-126">Auf der Kameraseite, wenn Sie auf die Kameraschaltfläche klicken, wird sie abgeblendet angezeigt, wenn Sie versuchen, einen Strichcode zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="53edb-126">On the camera page, when you click the Camera button, it will appear dimmed while trying to identify a bar code.</span></span> <span data-ttu-id="53edb-127">Wenn ein Strichcode nicht innerhalb von 5 Sekunden gekennzeichnet wird, wird der Prozess unterbrochen und die Kameraschaltfläche wird wieder verfügbar.</span><span class="sxs-lookup"><span data-stu-id="53edb-127">If a bar code is not identified within 5 seconds, the process will time out and the Camera button will become available again.</span></span> <span data-ttu-id="53edb-128">Sie können dann versuchen, den Strichcode erneut zu scannen.</span><span class="sxs-lookup"><span data-stu-id="53edb-128">You will then be able to try to scan a bar code again.</span></span>

<span data-ttu-id="53edb-129">Wenn Sie die Kamera auf einen Strichcode richten, halten Sie den Strichcode auf die Klammern ausgerichtet, um das beste Ergebnis zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="53edb-129">When you aim the camera at a bar code, keep the bar code aligned within the brackets for best result.</span></span> <span data-ttu-id="53edb-130">Wenn ein Strichcode erfolgreich gescannt wird, wird das Ergebnis verarbeitet, und Sie werden auf die nächste Stufe übernommen.</span><span class="sxs-lookup"><span data-stu-id="53edb-130">When a bar code is scanned successfully, the result will be processed, and you will be taken to the next step.</span></span> <span data-ttu-id="53edb-131">Wenn im nächsten Schritt ein anderes Eingabefeld den bevorzugten Eingabemodus enthält, der im Vorgang festgelegt wird, wird die Kameraseite erneut angezeigt.</span><span class="sxs-lookup"><span data-stu-id="53edb-131">If the next step contains another input field with the preferred input mode set to Scanning, the camera page will start again.</span></span> <span data-ttu-id="53edb-132">Wenn der nächste Schritt kein Scan-Feld ist, wird die Kameraseite nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="53edb-132">If the next step is not a scanning field, then the camera page will not be initiated.</span></span>

