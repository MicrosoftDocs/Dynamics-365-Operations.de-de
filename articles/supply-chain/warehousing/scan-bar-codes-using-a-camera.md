---
title: Strichcodes mit einer Kamera in die Warehouse Management Mobile App scannen
description: In diesem Thema wird erläutert, wie Sie die Warehouse Management Mobile App einrichten, um Strichcodes mithilfe einer Kamera auf einem mobilen Gerät zu scannen.
author: MarkusFogelberg
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 2f61f9c45b95b730a7f1743963658ec00abfbb56
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831217"
---
# <a name="scan-bar-codes-using-a-camera-in-the-warehouse-management-mobile-app"></a><span data-ttu-id="b64ad-103">Strichcodes mit einer Kamera in die Warehouse Management Mobile App scannen</span><span class="sxs-lookup"><span data-stu-id="b64ad-103">Scan bar codes using a camera in the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b64ad-104">In diesem Thema wird erläutert, wie Sie die Warehouse Management Mobile App einrichten, um Strichcodes mithilfe einer Kamera auf einem mobilen Gerät zu scannen.</span><span class="sxs-lookup"><span data-stu-id="b64ad-104">This topic explains how to set up the Warehouse Management mobile app to scan bar codes using a camera on a mobile device.</span></span>

## <a name="setup"></a><span data-ttu-id="b64ad-105">Einstellung</span><span class="sxs-lookup"><span data-stu-id="b64ad-105">Setup</span></span>

<span data-ttu-id="b64ad-106">In der Anzeige der Warehouse Management Mobile App können Sie auswählen, ob die Kamera für Scannen von Strichcodes verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b64ad-106">In the display settings of the Warehouse Management mobile app, you can select if the camera should be used for bar code scanning.</span></span> <span data-ttu-id="b64ad-107">Wenn Sie **Verwenden Sie die Kamera als Scanner** aktivieren, können Sie die Kamera auf jedem Eingabefeld verwenden, bei dem der bevorzugte Eingabemodus auf **Scannen** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="b64ad-107">If you enable **Use the camera as scanner**, you can use the camera on every input field that has the preferred input mode set to **Scanning**.</span></span>

<span data-ttu-id="b64ad-108">Um zu steuern, ob ein Eingabefeld gescannt werden soll, legen Sie auf der Seite **Feldnamen in Lagerortanwendung** **Bevorzugter Eingabemodus** auf **Scannen** fest.</span><span class="sxs-lookup"><span data-stu-id="b64ad-108">To control whether an input field should be scannable, on the **Warehouse app field names** page, set **Preferred input mode** to **Scanning**.</span></span> <span data-ttu-id="b64ad-109">Wenn diese Option aktiviert ist, kann eine Kamera für das Scannen in der Warehouse Management Mobile App verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b64ad-109">When this option is selected, a camera can be used for scanning in the Warehouse Management mobile app.</span></span> <span data-ttu-id="b64ad-110">Weitere Informationen finden Sie unter [Felder für die Warehouse Management Mobile App konfigurieren](configure-app-field-names-priorities-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="b64ad-110">For more information, see [Configure fields for the Warehouse Management mobile app](configure-app-field-names-priorities-warehouse.md).</span></span>

## <a name="supported-bar-code-formats"></a><span data-ttu-id="b64ad-111">Unterstützte Strichcodeformate</span><span class="sxs-lookup"><span data-stu-id="b64ad-111">Supported bar code formats</span></span>

<span data-ttu-id="b64ad-112">Die Formate der allgemeinsten Strichcodes einschließlich Code 128 Code 39, Codes 93, EAN-8, EAN-13, UPC-A und QR unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b64ad-112">The most common bar code formats are supported, including Code 128, Code 39, Code 93, EAN-8, EAN-13, UPC-E, UPC-A, and QR codes.</span></span>

## <a name="navigation"></a><span data-ttu-id="b64ad-113">Navigieren</span><span class="sxs-lookup"><span data-stu-id="b64ad-113">Navigation</span></span>

<span data-ttu-id="b64ad-114">Die Kameraseite wird auf jeder Seite verwendet, die im Eingabefeld einen **Bevorzugten Eingabemodus** hat, auf dem der Vorgang auf *Scannen* festgelegt ist, wenn Sie auf der Kameraseiten zu den folgenden Optionen navigieren:</span><span class="sxs-lookup"><span data-stu-id="b64ad-114">The camera page will be initiated on each page where the input field has its **Preferred input mode** set to *Scanning*, when you are on the camera page use the following options to navigate:</span></span>

- <span data-ttu-id="b64ad-115">Wählen Sie auf die Schaltfläche „Zurück“, um wieder zur Seite **Aufgaben und Details** zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="b64ad-115">Select the back button to go back to the **Task and details** page.</span></span>
- <span data-ttu-id="b64ad-116">Wählen Sie den Stift auf der Seite **Aufgabe und Details** aus, um zur Seite zu wechseln, in der Sie die Eingabe manuell eingeben können.</span><span class="sxs-lookup"><span data-stu-id="b64ad-116">Select the pencil on the **Task and details** page to go to the page where you can type input manually.</span></span>
- <span data-ttu-id="b64ad-117">Wählen Sie auf der Seite **Aufgabe und Details** die Kamera aus, um zur Kameraseite zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="b64ad-117">Select the camera on the **Task and details** page to go back to the camera page.</span></span>

<span data-ttu-id="b64ad-118">Auf der Kameraseite, wenn Sie die Kameraschaltfläche auswählen, wird sie abgeblendet angezeigt, wenn Sie versuchen, einen Strichcode zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="b64ad-118">On the camera page, when you select the camera button, it will appear dimmed while trying to identify a bar code.</span></span> <span data-ttu-id="b64ad-119">Wenn ein Strichcode nicht innerhalb von 5 Sekunden gekennzeichnet wird, wird der Prozess unterbrochen und die Kameraschaltfläche wird wieder verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b64ad-119">If a bar code is not identified within 5 seconds, the process will time out and the camera button will become available again.</span></span> <span data-ttu-id="b64ad-120">Sie können dann versuchen, den Strichcode erneut zu scannen.</span><span class="sxs-lookup"><span data-stu-id="b64ad-120">You will then be able to try to scan a bar code again.</span></span>

<span data-ttu-id="b64ad-121">Wenn Sie die Kamera auf einen Strichcode richten, halten Sie den Strichcode auf die Klammern ausgerichtet, um das beste Ergebnis zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="b64ad-121">When you aim the camera at a bar code, keep the bar code aligned within the brackets for best result.</span></span> <span data-ttu-id="b64ad-122">Wenn ein Strichcode erfolgreich gescannt wird, wird das Ergebnis verarbeitet, und Sie werden auf die nächste Stufe übernommen.</span><span class="sxs-lookup"><span data-stu-id="b64ad-122">When a bar code is scanned successfully, the result will be processed, and you will be taken to the next step.</span></span> <span data-ttu-id="b64ad-123">Wenn im nächsten Schritt ein anderes Eingabefeld den bevorzugten Eingabemodus enthält, der im Vorgang festgelegt wird, wird die Kameraseite erneut angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b64ad-123">If the next step contains another input field with the preferred input mode set to Scanning, the camera page will start again.</span></span> <span data-ttu-id="b64ad-124">Wenn der nächste Schritt kein Scan-Feld ist, wird die Kameraseite nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="b64ad-124">If the next step is not a scanning field, then the camera page will not be initiated.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]