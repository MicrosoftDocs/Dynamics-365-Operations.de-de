---
title: Garantien auf Anlagen und Anlagearten
description: In diesem Abschnitt wird erläutert, wie Sie im Anlagenmanagement Garantien auf Anlagen und Anlagenarten einrichten.
author: johanhoffmann
ms.date: 08/30/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f05f5af76aeb037d606d38a368a49d011f0d2bd6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825565"
---
# <a name="warranties-on-assets-and-asset-types"></a><span data-ttu-id="e9b7f-103">Garantien auf Anlagen und Anlagearten</span><span class="sxs-lookup"><span data-stu-id="e9b7f-103">Warranties on assets and asset types</span></span>

[!include [banner](../../includes/banner.md)]

 


<span data-ttu-id="e9b7f-104">In diesem Abschnitt wird erläutert, wie Sie im Anlagenmanagement Garantien auf Anlagen und Anlagenarten einrichten.</span><span class="sxs-lookup"><span data-stu-id="e9b7f-104">This topic explains how to set up warranties on assets and asset types in Asset Management.</span></span>

## <a name="set-up-a-warranty-on-an-asset-type"></a><span data-ttu-id="e9b7f-105">Einrichten einer Garantie für eine Anlagenart</span><span class="sxs-lookup"><span data-stu-id="e9b7f-105">Set up a warranty on an asset type</span></span>

1. <span data-ttu-id="e9b7f-106">Wählen Sie **Anlageverwaltung** \> **Einstellungen** \> **Anlagentypen** \> **Anlagentypen** aus.</span><span class="sxs-lookup"><span data-stu-id="e9b7f-106">Select **Asset management** \> **Setup** \> **Asset types** \> **Asset types**.</span></span>
2. <span data-ttu-id="e9b7f-107">Wählen Sie im linken Bereich die Anlagenart aus, an die eine Garantievereinbarung des Lieferanten angehängt werden soll, und wählen Sie dann **Anlagentypvorgaben**.</span><span class="sxs-lookup"><span data-stu-id="e9b7f-107">In the left pane, select the asset type to attach a vendor warranty agreement to, and then select **Asset type defaults**.</span></span>
3. <span data-ttu-id="e9b7f-108">Wählen Sie im Feld **Allgemein** FastTab im Feld **Lieferantengarantie** die Vereinbarung aus.</span><span class="sxs-lookup"><span data-stu-id="e9b7f-108">On the **General** FastTab, in the **Vendor warranty** field, select the agreement.</span></span>

## <a name="set-up-a-warranty-on-an-asset"></a><span data-ttu-id="e9b7f-109">Einrichten einer Garantie für eine Anlage</span><span class="sxs-lookup"><span data-stu-id="e9b7f-109">Set up a warranty on an asset</span></span>

1. <span data-ttu-id="e9b7f-110">Wählen Sie **Anlagenverwaltung** \> **Allgemeines** \> **Anlagen** \> **Alle Anlagen**.</span><span class="sxs-lookup"><span data-stu-id="e9b7f-110">Select **Asset management** \> **Common** \> **Assets** \> **All assets**.</span></span>
2. <span data-ttu-id="e9b7f-111">Wählen Sie die Anlage aus und wählen Sie dann **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="e9b7f-111">Select the asset, and then select **Edit**.</span></span>
3. <span data-ttu-id="e9b7f-112">Wählen Sie auf der Registerkarte **Lieferant** FastTab im Abschnitt **Lieferantengarantie**, im Feld **Garantie** die Garantievereinbarung aus.</span><span class="sxs-lookup"><span data-stu-id="e9b7f-112">On the **Vendor** FastTab, in the **Vendor warranty** section, in the **Warranty** field, select the warranty agreement.</span></span>
4. <span data-ttu-id="e9b7f-113">Wählen Sie in den Feldern **Garantiebeginn** und **Garantieende** das Start- und Enddatum aus.</span><span class="sxs-lookup"><span data-stu-id="e9b7f-113">In the **Warranty start** and **Warranty end** fields, select the start and end dates.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="e9b7f-114">Wenn bei einem Arbeitsauftrag im Feld **Gewährleistungsbeginn** ein Datum ausgewählt wird, gilt die Garantie für den Arbeitsauftrag zu diesem Datum.</span><span class="sxs-lookup"><span data-stu-id="e9b7f-114">If a date is selected in the **Warranty start** field on a work order, the warranty becomes valid for the work order on that date.</span></span> <span data-ttu-id="e9b7f-115">Wenn Sie einen Arbeitsauftrag anlegen, wird das Feld **Garantiebeginn** automatisch auf das Erstellungsdatum gesetzt.</span><span class="sxs-lookup"><span data-stu-id="e9b7f-115">When you create a work order, the **Warranty start** field is automatically set to the date of creation.</span></span> <span data-ttu-id="e9b7f-116">Sie können das Datum jedoch so ändern, dass es z.B. dem Startdatum einer Garantievereinbarung entspricht.</span><span class="sxs-lookup"><span data-stu-id="e9b7f-116">However, you can change the date so that it corresponds to, for example, the start date of a warranty agreement.</span></span>
    >
    > ![Arbeitsauftragsseite](media/02-warranty.png)

> [!NOTE]
> <span data-ttu-id="e9b7f-118">Wenn Sie einen Arbeitsauftrag für eine Anlage anlegen, die unter eine Lieferantengarantie fällt, erhalten Sie eine Benachrichtigung über die Garantievereinbarung, wenn der Arbeitsauftrag ein voraussichtliches Startdatum innerhalb der Garantiezeit hat.</span><span class="sxs-lookup"><span data-stu-id="e9b7f-118">When you create a work order for an asset that is covered by a vendor warranty, if the work order has an expected start date during the warranty period, you receive a notification about the warranty agreement.</span></span> <span data-ttu-id="e9b7f-119">Anschließend können Sie den Arbeitsauftrag nach Bedarf stornieren.</span><span class="sxs-lookup"><span data-stu-id="e9b7f-119">You can then cancel the work order, as you require.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]