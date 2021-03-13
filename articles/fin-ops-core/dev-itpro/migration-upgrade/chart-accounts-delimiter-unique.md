---
title: Erstellen eines eindeutigen Trennzeichens für den Kontenplan
description: In diesem Thema wird erläutert, wie Sie nicht die gleichen Trennzeichen für den Kontenplan und die Dimensionswerte verwenden können. Sie müssen die Trennzeichenwerte nach dem Upgrade ändern.
author: panolte
manager: AnnBe
ms.date: 03/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: 72965e9c6182bdac123feb1bc5cc4b82d91cd588
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/16/2021
ms.locfileid: "5020103"
---
# <a name="make-the-chart-of-accounts-delimiter-unique"></a><span data-ttu-id="53960-104">Erstellen eines eindeutigen Trennzeichens für den Kontenplan</span><span class="sxs-lookup"><span data-stu-id="53960-104">Make the chart of accounts delimiter unique</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="53960-105">In Microsoft Dynamics AX 2012 können Sie die gleichen Trennzeichen für den Kontenplan und Dimensionswerte verwenden.</span><span class="sxs-lookup"><span data-stu-id="53960-105">In Microsoft Dynamics AX 2012, you could use the same delimiter for your chart of accounts and dimension values.</span></span> <span data-ttu-id="53960-106">In aktuellen Versionen von Finance and Operations können Sie nicht dasselbe Trennzeichen für den Kontenplan und die Dimensionswerte verwenden.</span><span class="sxs-lookup"><span data-stu-id="53960-106">In current versions of Finance and Operations, you cannot have the same delimiter for the chart of accounts and dimension values.</span></span> <span data-ttu-id="53960-107">Wenn ein Trennzeichen doppelt vorkommt, können Sie es nach dem Upgrade ändern.</span><span class="sxs-lookup"><span data-stu-id="53960-107">If there is a duplicate delimiter, you can change it after upgrade.</span></span> 

<span data-ttu-id="53960-108">Diese Funktion ist in den folgenden Versionen nicht verfügbar:</span><span class="sxs-lookup"><span data-stu-id="53960-108">This feature is available in the following versions:</span></span>
- <span data-ttu-id="53960-109">Finance and Operations Version 8.0</span><span class="sxs-lookup"><span data-stu-id="53960-109">Finance and Operations version 8.0</span></span>
- <span data-ttu-id="53960-110">Finance and Operations Version 7.1, KB 4094701 – Die Finanzdimensionen können nicht eingegeben werden, wenn die Dimensionswerte das Trennzeichen für den Kontenplan enthalten</span><span class="sxs-lookup"><span data-stu-id="53960-110">Finance and Operations version 7.1, KB 4094701 Cannot enter the financial dimensions when the dimension values contain the chart of accounts delimiter</span></span>
- <span data-ttu-id="53960-111">Finance and Operations Version 7.2, KB 4092967 – Unterprojekt kann nicht als Dimension ausgewählt werden, wenn das Unterprojektformat das Dimensionstrennzeichen enthält</span><span class="sxs-lookup"><span data-stu-id="53960-111">Finance and Operations version 7.2, KB 4092967 Cannot choose sub-project as dimension when sub-project format contains the dimension delimiter</span></span>

## <a name="update-delimiter"></a><span data-ttu-id="53960-112">Trennzeichen aktualisieren</span><span class="sxs-lookup"><span data-stu-id="53960-112">Update delimiter</span></span>
<span data-ttu-id="53960-113">Bei einem Konflikt mit dem Kontenplan kann das Kontenplan-Trennzeichen und das Projekt-/Unterprojekt-ID-Format geändert werden.</span><span class="sxs-lookup"><span data-stu-id="53960-113">If there is a conflict with the chart of accounts, the chart of accounts delimiter and the project/subproject ID format can be changed.</span></span> <span data-ttu-id="53960-114">Keine anderen Dimensionstrennzeichen können geändert werden.</span><span class="sxs-lookup"><span data-stu-id="53960-114">No other dimension delimiters can be changed.</span></span> 
- <span data-ttu-id="53960-115">Sie können das Kontenplan-Trennzeichen nach dem Upgrade in **Hauptbuchparameter** > **Kontenplan und Dimensionen** > **Trennzeichen ändern** ändern.</span><span class="sxs-lookup"><span data-stu-id="53960-115">You can change the chart of accounts delimiter after upgrade in **General ledger parameters** > **Chart of accounts and dimensions** > **Change delimiter**.</span></span> 
- <span data-ttu-id="53960-116">Wenn es nur einen Konflikt mit dem Projekt-/Unterprojekt-ID-Format gibt, können Sie diesen Wert in **Projektverwaltung und Buchhaltungsparameter** > **Allgemein** > **Unterprojektformat ändern** ändern.</span><span class="sxs-lookup"><span data-stu-id="53960-116">If the only conflict is with the project/subproject ID format, you can change that value in **Project management and accounting parameters** > **General** > **Modify subproject format**.</span></span> 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a><span data-ttu-id="53960-117">So wird festgestellt, ob Ihre Umgebung aktualisierte Trennzeichen benötigt</span><span class="sxs-lookup"><span data-stu-id="53960-117">How to determine if your environment requires updated delimiters</span></span> 
<span data-ttu-id="53960-118">Wenn Trennzeichen in Ihrer aktualisierten Umgebung Konflikte verursachen, kommt es möglicherweise zu einer Instabilität, wenn Werte in einem segmentierten Eingabesteuerelement oder einem Dimensionseingabe-Steuerelement eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="53960-118">If delimiters in your upgraded environment are conflicting, you may experience instability when entering values in a segmented entry control or dimension entry control.</span></span> <span data-ttu-id="53960-119">Das bedeutet, dass Sie immer Suchen oder ein Flyoutmenü verwenden müssen, wenn Sie Konten- und Dimensionskombinationen eingeben.</span><span class="sxs-lookup"><span data-stu-id="53960-119">This means that you will need to always use lookups or a flyout menu when entering account and dimension combinations.</span></span>
