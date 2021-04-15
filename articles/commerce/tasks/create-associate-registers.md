---
title: " Register erstellen und zuordnen"
description: Diese Prozedur zeigt, wie ein Verkaufsstellen-(POS)-Register erstellt wird.
author: rubencdelgado
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailTerminalTable
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ba978a3d895394760687386197dbb3512c62ef98
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798560"
---
# <a name="create-and-associate-registers"></a><span data-ttu-id="ca2ae-103"> Register erstellen und zuordnen</span><span class="sxs-lookup"><span data-stu-id="ca2ae-103">Create and associate registers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ca2ae-104">Diese Prozedur zeigt, wie ein Verkaufsstellen-(POS)-Register erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="ca2ae-104">This procedure demonstrates how to create a point of sale (POS) register.</span></span> <span data-ttu-id="ca2ae-105">Für diese Prozedur wird das Demo-Datenunternehmen USRT verwendet.</span><span class="sxs-lookup"><span data-stu-id="ca2ae-105">This procedure uses the demo data company USRT.</span></span>

1. <span data-ttu-id="ca2ae-106">Wechseln Sie zu Einzelhandel und Handel > Kanaleinstellungen > POS-Einstellungen > Register.</span><span class="sxs-lookup"><span data-stu-id="ca2ae-106">Go to Retail and Commerce > Channel setup > POS setup > Registers.</span></span>
2. <span data-ttu-id="ca2ae-107">Klicken Sie auf Neu.</span><span class="sxs-lookup"><span data-stu-id="ca2ae-107">Click New.</span></span>
3. <span data-ttu-id="ca2ae-108">Geben Sie im Feld "Registernummer" eine Kennung für ein neues Register ein.</span><span class="sxs-lookup"><span data-stu-id="ca2ae-108">In the Register number field, type an ID for the new register.</span></span>
    * <span data-ttu-id="ca2ae-109">Die Registerkennung umfasst gewöhnlich Codes, die helfen, das Register dem Lager zuzuordnen, zu dem es gehört, sowie zum Lagerplatz innerhalb des Lagers.</span><span class="sxs-lookup"><span data-stu-id="ca2ae-109">The register ID typically includes codes that help map the register to the store to which it belongs, and the location within the store.</span></span>  
4. <span data-ttu-id="ca2ae-110">Geben Sie im Feld "Name" einen aussagekräftigen Namen für das Register ein.</span><span class="sxs-lookup"><span data-stu-id="ca2ae-110">In the Name field, type a descriptive name for the register..</span></span>
5. <span data-ttu-id="ca2ae-111">Geben Sie im Feld "Lagernummer" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="ca2ae-111">In the Store number field, enter or select a value.</span></span>
6. <span data-ttu-id="ca2ae-112">Geben Sie im Feld "Hardwareprofil" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="ca2ae-112">In the Hardware profile field, enter or select a value.</span></span>
    * <span data-ttu-id="ca2ae-113">Hardwareprofile werden zur Angabe der Peripheriegeräte verwendet, die an die Registrierkasse angeschlossen werden, wie z.B. Kassenlade und Bondrucker.</span><span class="sxs-lookup"><span data-stu-id="ca2ae-113">Hardware profiles are used to specify the peripherals that will be connected to the register, such as cash drawer and receipt printer.</span></span>  
7. <span data-ttu-id="ca2ae-114">Geben Sie im Feld "Visuelles Profil" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="ca2ae-114">In the Visual profile field, enter or select a value.</span></span>
    * <span data-ttu-id="ca2ae-115">Visuelle Profile werden verwendet, um die Bilder anzugeben, die im POS-Hintergrund und auf der Anmeldeseite sowie als Themen für das POS verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ca2ae-115">Visual profiles are used to specify the images used in the POS background and login page as well as themes for the POS.</span></span>  
8. <span data-ttu-id="ca2ae-116">Geben Sie im Feld "POS-Registernummer für elektronische Überweisung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="ca2ae-116">In the EFT POS register number field, type a value.</span></span>
    * <span data-ttu-id="ca2ae-117">Die POS-Registernummer für elektronische Überweisungen wird verwendet, um den Zahlungsprozessor darüber zu informieren, welches Zahlungsterminal Autorisierungsanforderungen sendet.</span><span class="sxs-lookup"><span data-stu-id="ca2ae-117">The EFT POS register number is used to inform the payment processor which payment terminal is sending authorization requests.</span></span> <span data-ttu-id="ca2ae-118">Dieser Wert wird häufig als „Terminalkennung“ oder „TID“ bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="ca2ae-118">This value is often called the "Terminal ID" or "TID".</span></span> <span data-ttu-id="ca2ae-119">Die TID kann allgemein auf einem Aufkleber auf dem Zahlungsgerät gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="ca2ae-119">The TID can generally be found on a sticker on the payment device.</span></span>  
9. <span data-ttu-id="ca2ae-120">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="ca2ae-120">Click Save.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]