---
title: Anlagendarlehen
description: In diesem Thema wird beschrieben, wie Anlagendarlehen in der Anlagenverwaltung erfasst werden.
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 07472188051aea7084142cc417c6d725462cf4f9
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205252"
---
# <a name="asset-loans"></a><span data-ttu-id="dcb09-103">Anlagendarlehen</span><span class="sxs-lookup"><span data-stu-id="dcb09-103">Asset loans</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="dcb09-104">Wenn Ihr Unternehmen Anlagen für Reparatur- oder Wartungsaufträge von internen Standorten oder Kunden erhält und Sie vorübergehend Anlagen an diese Standorte oder Kunden ausleihen, kann die Anlagenverwaltung die Anlagendarlehen verfolgen.</span><span class="sxs-lookup"><span data-stu-id="dcb09-104">If your company receives assets for repair or maintenance jobs from either internal locations or customers, and if you temporarily loan assets to those locations or customers, Asset Management can track the asset loans.</span></span>

## <a name="register-asset-loans-on-a-maintenance-request"></a><span data-ttu-id="dcb09-105">Anlagendarlehen in einer Wartungsanfrage erfassen</span><span class="sxs-lookup"><span data-stu-id="dcb09-105">Register asset loans on a maintenance request</span></span>

1. <span data-ttu-id="dcb09-106">Wählen Sie **Anlagenverwaltung** \> **Allgemein** \> **Wartungsanfragen** \> **Alle Wartungsanfragen** oder **Aktive Wartungsanfragen** aus.</span><span class="sxs-lookup"><span data-stu-id="dcb09-106">Select **Asset management** \> **Common** \> **Maintenance requests** \> **All maintenance requests** or **Active maintenance requests**.</span></span>
2. <span data-ttu-id="dcb09-107">Wählen Sie die Wartungsanfrage aus, um ein Anlagendarlehen zu erfassen, und wählen Sie dann **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="dcb09-107">Select the maintenance request to register an asset loan on, and then select **Edit**.</span></span>
3. <span data-ttu-id="dcb09-108">Wählen Sie auf der Seite **Anforderung** die Option **Anlagenausleihe senden** aus.</span><span class="sxs-lookup"><span data-stu-id="dcb09-108">On the **Request** page, select **Send loan asset**.</span></span>
4. <span data-ttu-id="dcb09-109">Wählen Sie die Anlage aus, und geben Sie das voraussichtliche Rückgabedatum ein.</span><span class="sxs-lookup"><span data-stu-id="dcb09-109">Select the asset, and enter the expected return date.</span></span>
5. <span data-ttu-id="dcb09-110">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="dcb09-110">Select **OK**.</span></span>

> [!NOTE]
> - <span data-ttu-id="dcb09-111">Sie können eine Anlagenausleihe nur senden, wenn eine Anlage des gleichen Anlagentyps verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="dcb09-111">You can send a loan asset only if an asset of the same asset type is available.</span></span>
> - <span data-ttu-id="dcb09-112">Die Anlage, die Sie ausleihen werden, muss über einen Anlagenlebenszyklusstatus verfügen, der es ermöglicht, dass sie als Ausleiheanlage verwendet werden kann, z. B. **Im Lager**.</span><span class="sxs-lookup"><span data-stu-id="dcb09-112">The asset that you loan must have an asset lifecycle state that allows it to be used as a loan asset, such as **InStorage**.</span></span> <span data-ttu-id="dcb09-113">Wenn die Anlagenausleihe erfasst ist, wird der Anlagenlebenszyklusstatus der Anlage automatisch aktualisiert, z. B. in **In Ausleihe**.</span><span class="sxs-lookup"><span data-stu-id="dcb09-113">When the asset loan is registered, the asset lifecycle state of the asset is automatically updated to, for example, **OnLoan**.</span></span>

<span data-ttu-id="dcb09-114">Um eine Liste mit allen Anlagen anzuzeigen, die Sie an andere Standorte oder an Kunden ausgeliehen haben, wählen Sie **Anlagenverwaltung** \> **Allgemeines** \> **Anlagendarlehen** \> **Alle Anlagendarlehen** aus.</span><span class="sxs-lookup"><span data-stu-id="dcb09-114">To view a list of all the assets that you've loaned to other locations or customers, select **Asset management** \> **Common** \> **Asset loan** \> **All asset loans**.</span></span> <span data-ttu-id="dcb09-115">Wenn das Kontrollkästchen **Beendet** für eine Anlage aktiviert ist, wurde die Anlage als Ihrem Unternehmen zurückgegeben erfasst.</span><span class="sxs-lookup"><span data-stu-id="dcb09-115">If the **Ended** check box is selected for an asset, the asset has been registered as returned to your company.</span></span>

![Wartungsanfragen verwalten](media/06-manage-maintenance-requests.png)

<span data-ttu-id="dcb09-117">Auf der Seite **Aktive Anlagendarlehen** können Sie eine Liste aller Anlagendarlehen anzeigen, die noch nicht an Ihr Unternehmen zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="dcb09-117">On the **Active asset loans** page, you can view a list of all the loan assets that haven't yet been returned to your company.</span></span>

## <a name="register-loan-assets-as-returned"></a><span data-ttu-id="dcb09-118">Anlagendarlehen als zurückgegeben erfassen</span><span class="sxs-lookup"><span data-stu-id="dcb09-118">Register loan assets as returned</span></span>

1. <span data-ttu-id="dcb09-119">Wählen Sie **Anlagenverwaltung** \> **Allgemeines** \> **Anlagendarlehen** \> **Aktive Anlagendarlehen** aus.</span><span class="sxs-lookup"><span data-stu-id="dcb09-119">Select **Asset management** \> **Common** \> **Asset loan** \> **Active asset loans**.</span></span>
2. <span data-ttu-id="dcb09-120">Wählen Sie das Anlagendarlehen aus, das als zurückgegeben erfasst werden soll, und wählen Sie dann **Anlagendarlehen zurückgeben** aus.</span><span class="sxs-lookup"><span data-stu-id="dcb09-120">Select the asset loan to register as returned, and then select **Return asset loan**.</span></span>
3. <span data-ttu-id="dcb09-121">Geben Sie im Feld **Zurückgegeben** das Datum und die Uhrzeit ein.</span><span class="sxs-lookup"><span data-stu-id="dcb09-121">In the **Returned** field, enter the date and time.</span></span>
4. <span data-ttu-id="dcb09-122">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="dcb09-122">Select **OK**.</span></span>
5. <span data-ttu-id="dcb09-123">Aktualisieren Sie die Listenseite **Aktive Anlagendarlehen**. Sie sehen, dass das Anlagendarlehen nicht mehr in der Liste angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="dcb09-123">Refresh the **Active asset loans** list page, and notice that the asset loan no longer appears in the list.</span></span>
