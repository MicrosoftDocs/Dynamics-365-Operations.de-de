---
title: Hauptkontokategorien einrichten
description: In diesem Thema wird erläutert, wie Sie unter Dynamics 365 Finance die Hauptkontokategorien einrichten.
author: aprilolson
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: MainAccountCategory, MainAccountCategoryLink
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c2dcaa27f20ca050d278aa378e90946b8cb40449
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815115"
---
# <a name="set-up-main-account-categories"></a><span data-ttu-id="596d4-103">Hauptkontokategorien einrichten</span><span class="sxs-lookup"><span data-stu-id="596d4-103">Set up main account categories</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="596d4-104">In diesem Thema wird erläutert, wie Sie unter die Hauptkontokategorien einrichten.</span><span class="sxs-lookup"><span data-stu-id="596d4-104">This topic explains how to set up main account categories.</span></span> <span data-ttu-id="596d4-105">Hauptkontokategorien werden für die Standardberichte in der Finanzberichterstellung und in Power BI verwendet.</span><span class="sxs-lookup"><span data-stu-id="596d4-105">Main account categories are used for the default reports in financial reporting and in Power BI.</span></span> <span data-ttu-id="596d4-106">Hauptkontokategorien, die standardmäßig erstellt werden, können umbenannt jedoch nicht gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="596d4-106">Main account categories that are created by default can be renamed but not deleted.</span></span> <span data-ttu-id="596d4-107">Zusätzliche Kontokategorien können den erstellt und für Berichts- und Analysezwecke verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="596d4-107">Additional account categories can be created and used for reporting and analysis purposes.</span></span> <span data-ttu-id="596d4-108">Dieses Thema verwendet die USMF-Demofirma.</span><span class="sxs-lookup"><span data-stu-id="596d4-108">This topic uses the USMF demo company.</span></span>

## <a name="create-a-main-account-category"></a><span data-ttu-id="596d4-109">Erstellen einer Hauptkontokategorie</span><span class="sxs-lookup"><span data-stu-id="596d4-109">Create a main account category</span></span>
1. <span data-ttu-id="596d4-110">Gehen Sie im Navigationsbereich zu **Module > Hauptbuch > Kontenplan > Kontenplan > Konten > Hauptkontenkategorien**.</span><span class="sxs-lookup"><span data-stu-id="596d4-110">In the navigation pane, go to **Modules > General Ledger > Chart of accounts > Accounts > Main account categories**.</span></span>
2. <span data-ttu-id="596d4-111">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="596d4-111">Select **New**.</span></span>
3. <span data-ttu-id="596d4-112">Geben Sie im Feld **Hauptkontokategorie** einen eindeutigen Namen ein.</span><span class="sxs-lookup"><span data-stu-id="596d4-112">In the **Main account category** field, enter a unique name.</span></span>
4. <span data-ttu-id="596d4-113">Geben Sie im Feld **Beschreibung** eine Beschreibung für die Hauptkontotypen ein.</span><span class="sxs-lookup"><span data-stu-id="596d4-113">In the **Description field**, enter a description for the main account category.</span></span>
5. <span data-ttu-id="596d4-114">Wählen Sie im Feld **Hauptkontoart** die Hauptkontoart aus, die mit der Kategorie verknüpft werden soll.</span><span class="sxs-lookup"><span data-stu-id="596d4-114">In the **Main account type** field, select the main account type that will be linked to the category.</span></span>

## <a name="link-main-accounts-to-account-category"></a><span data-ttu-id="596d4-115">Verknüpfen von Hauptkonten mit Kontokategorien</span><span class="sxs-lookup"><span data-stu-id="596d4-115">Link main accounts to account category</span></span>
1. <span data-ttu-id="596d4-116">Klicken Sie auf **Hauptkonten verlinken**.</span><span class="sxs-lookup"><span data-stu-id="596d4-116">Click **Link main accounts**.</span></span>
2. <span data-ttu-id="596d4-117">Wählen Sie in der Liste die Hauptkonten aus, die der Hauptkontokategorie zugeordnet werden sollen, indem Sie die Kontrollkästchen in der Spalte **Verknüpft** markieren.</span><span class="sxs-lookup"><span data-stu-id="596d4-117">In the list, select the main accounts to assign to the main account category by checking the boxes in the **Linked** column.</span></span> <span data-ttu-id="596d4-118">Das Zuweisen von Hauptkonten zu einer Hauptkontokategorie fasst die Salden der Konten zusammen wenn diese Kategorie für die Finanzberichte und Analysen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="596d4-118">Assigning main accounts to a main account category will aggregate the balances of the accounts when that category is used for financial reporting and analysis.</span></span>  
3. <span data-ttu-id="596d4-119">Wählen oder deaktivieren Sie die Option **Verknüpft**, um die Hauptkonten auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="596d4-119">Select or clear the **Linked** option to choose the main accounts.</span></span>
4. <span data-ttu-id="596d4-120">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="596d4-120">Select **OK**.</span></span>
5. <span data-ttu-id="596d4-121">Wählen Sie **Ja** aus.</span><span class="sxs-lookup"><span data-stu-id="596d4-121">Select **Yes**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]