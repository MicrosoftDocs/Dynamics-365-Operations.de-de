---
title: Transportverwaltung Sequenznummer
description: Dieses Thema beschreibt, wie Sie Nummernfolgen für die Transportverwaltung festlegen.
author: Henrikan
manager: tfehr
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: b7bb6c9338808828a41801a85a1b93b420e9c75b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5004735"
---
# <a name="transportation-management-number-sequence"></a><span data-ttu-id="02b54-103">Transportverwaltung Sequenznummer</span><span class="sxs-lookup"><span data-stu-id="02b54-103">Transportation management number sequence</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="02b54-104">Verwenden Sie die Seite **Nummernfolgen** im Modul Transportverwaltung, um verschiedene Pro-Nummern festzulegen.</span><span class="sxs-lookup"><span data-stu-id="02b54-104">Use the **Number sequences** page in the transportation management module to set up various pro numbers.</span></span> <span data-ttu-id="02b54-105">Pro-Nummern werden von Spediteuren verwendet, um den Fortschritt der einzelnen Sendungen zu organisieren und zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="02b54-105">Pro numbers are used by carriers to organize and track the progress of each shipment.</span></span>

## <a name="create-a-number-sequence-for-a-pro-number"></a><span data-ttu-id="02b54-106">Erstellen einer Nummernfolge für eine Pro-Nummer</span><span class="sxs-lookup"><span data-stu-id="02b54-106">Create a number sequence for a pro number</span></span>

<span data-ttu-id="02b54-107">Um eine Sequenz für eine Pro-Nummer zu erstellen, gehen Sie wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="02b54-107">To create a number sequence for a pro number, do the following:</span></span>

1. <span data-ttu-id="02b54-108">Gehen Sie zu **Transportverwaltung \> Einrichten \> Spediteure \> Nummernfolgen**.</span><span class="sxs-lookup"><span data-stu-id="02b54-108">Go to **Transportation management \> Setup \> Carriers \> Number sequences**.</span></span>
1. <span data-ttu-id="02b54-109">Wählen Sie **Neu**, um eine neue Sequenz für eine Nummer zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="02b54-109">Select **New** to create a new number sequence.</span></span>
1. <span data-ttu-id="02b54-110">Geben Sie eine eindeutige ID und einen beschreibenden Namen für die Nummernfolge ein.</span><span class="sxs-lookup"><span data-stu-id="02b54-110">Enter a unique ID and descriptive name for the number sequence.</span></span>
1. <span data-ttu-id="02b54-111">Im Feld **Nummernfolge-Typ** ist *Pro-Nummer* die einzige Option.</span><span class="sxs-lookup"><span data-stu-id="02b54-111">In the **Number sequence type** field, *Pro number* is the only option.</span></span>
1. <span data-ttu-id="02b54-112">Im Feld **Prüfziffer** ist *Prüfziffer* die einzige Option und ist als generische Engine festgelegt.</span><span class="sxs-lookup"><span data-stu-id="02b54-112">In the **Check digit** field, *Check digit* is the only option and is set up as a generic engine.</span></span>
1. <span data-ttu-id="02b54-113">Geben Sie auf dem Inforegister **Sequenz** Informationen über die Sequenz an.</span><span class="sxs-lookup"><span data-stu-id="02b54-113">On the **Sequence** FastTab, provide information about the sequence.</span></span>
1. <span data-ttu-id="02b54-114">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="02b54-114">Close the page.</span></span>

## <a name="link-a-number-sequence-to-a-shipping-carrier"></a><span data-ttu-id="02b54-115">Verknüpfen einer Sequenz mit einem Spediteur</span><span class="sxs-lookup"><span data-stu-id="02b54-115">Link a number sequence to a shipping carrier</span></span>

<span data-ttu-id="02b54-116">Um eine Sequenz mit einem Spediteur zu verknüpfen, gehen Sie wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="02b54-116">To link a number sequence to a carrier, do the following:</span></span>

1. <span data-ttu-id="02b54-117">Wechseln Sie zu **Transportverwaltung \> Einstellungen \> Spediteure \> Spediteure**.</span><span class="sxs-lookup"><span data-stu-id="02b54-117">Go to **Transportation management \> Setup \> Carriers \> Shipping carriers**.</span></span>
1. <span data-ttu-id="02b54-118">Wählen Sie einen Spediteur aus.</span><span class="sxs-lookup"><span data-stu-id="02b54-118">Select a shipping carrier.</span></span>
1. <span data-ttu-id="02b54-119">Wählen Sie **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="02b54-119">Select **Edit**.</span></span>
1. <span data-ttu-id="02b54-120">Wählen Sie auf der Inforegister-Registerkarte **Übersicht** eine Option im Feld **Pro Nummernfolge**.</span><span class="sxs-lookup"><span data-stu-id="02b54-120">On the **Overview** FastTab, select an option in the **Pro number sequence** field.</span></span>
1. <span data-ttu-id="02b54-121">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="02b54-121">Close the page.</span></span>
