---
title: Planzahlenmodelle für Projektbudgets erstellen
description: In diesem Thema wird beschrieben, wie ein Planzahlenmodell für verbleibende Budgets erstellt wird.
author: RadhikaRS
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 07e540f23a668b40a54906a67d87552fe991825a
ms.sourcegitcommit: 5de75c61c33e57c813944f1ab6100aceb020d432
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2020
ms.locfileid: "3321778"
---
# <a name="create-forecast-models-for-project-budgets"></a><span data-ttu-id="66f9e-103">Planzahlenmodelle für Projektbudgets erstellen</span><span class="sxs-lookup"><span data-stu-id="66f9e-103">Create forecast models for project budgets</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="66f9e-104">In diesem Thema wird beschrieben, wie ein Planzahlenmodell für verbleibende Budgets erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="66f9e-104">This topic describes how to create a forecast model for remaining budgets.</span></span> <span data-ttu-id="66f9e-105">Für Projekte, die der Budgetsteuerung unterliegen, werden zwei Arten von Budgets verwendet: ursprünglich und verbleibend.</span><span class="sxs-lookup"><span data-stu-id="66f9e-105">A project that is subject to budget control uses two types of budgets: original and remaining.</span></span> <span data-ttu-id="66f9e-106">Beim Erstellen eines Projektbudgets müssen Sie die Planzahlenmodelle für das ursprüngliche Budget und das Restbudget angeben, die auf der Seite **Prognosemodelle** erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="66f9e-106">When you create a project budget, you must specify the original and remaining budget forecast models that were created in the **Forecast models** page.</span></span> <span data-ttu-id="66f9e-107">Projektbudgets basierend auf den angegebenen Modellen werden erstellt, wenn Sie das Projektbudget bestimmen.</span><span class="sxs-lookup"><span data-stu-id="66f9e-107">Project budgets based on the specified models are created when you commit the project budget.</span></span>

> [!NOTE]
> <span data-ttu-id="66f9e-108">Ein Planzahlenmodell, das für die Budgetsteuerung verwendet wird, kann kein Teilmodell enthalten oder kann nicht als Teilmodell verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="66f9e-108">A forecast model that is used for budget control can’t have a submodel or be used as a submodel.</span></span>

1. <span data-ttu-id="66f9e-109">Wählen Sie **Projektmanagement und Buchhaltung** > **Setup** > **Prognosen**  > **Planzahlenmodelle** aus.</span><span class="sxs-lookup"><span data-stu-id="66f9e-109">Select **Project management and accounting** > **Setup** > **Forecasts**  > **Forecast models**.</span></span>
2. <span data-ttu-id="66f9e-110">Wählen Sie **Neu** aus, um ein neues Planzahlenmodell zu erstellen, und geben Sie dann die Modellkennungsnummer und einen Namen für das neue Modell ein.</span><span class="sxs-lookup"><span data-stu-id="66f9e-110">Select **New** to create a new forecast model, and then enter a model ID number and name for the new model.</span></span> 
3. <span data-ttu-id="66f9e-111">Legen Sie die Option **Beendet** auf **Ja** fest, um Änderungen an den Prognosepositionen für das Planzahlenmodell zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="66f9e-111">Set the **Stopped** option to **Yes** to prevent any changes to the forecast lines for the forecast model.</span></span> 
4. <span data-ttu-id="66f9e-112">Wenn die Prognosepositionen, denen das Modell zugeordnet ist, Cashflow-Prognosen im Hauptbuch erstellen sollen, legen Sie **In Cashflow-Prognosen einbeziehen** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="66f9e-112">If the forecast lines that the model is associated with should generate cash flow forecasts in the general ledger, set **Include in Cash flow forecasts** to **Yes.**</span></span> 
5. <span data-ttu-id="66f9e-113">Um das Projektdatum als Rechnungsdatum zu verwenden, legen Sie **Prognose-Rechnungsdatum** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="66f9e-113">To use the project date as the invoice date, set **Forecast Invoice date** to **Yes**.</span></span> 
6. <span data-ttu-id="66f9e-114">Wählen Sie im Feld **Budgettyp** einen der folgenden Modelltypen aus:</span><span class="sxs-lookup"><span data-stu-id="66f9e-114">In the **Budget type** field, select one of the following model types:</span></span>

   - <span data-ttu-id="66f9e-115">**Ursprüngliches Budget**: Verwenden Sie die ursprünglichen Budgetbeträge, die zugesagt wurden, als das anfängliche Budget erstellt und genehmigt wurde.</span><span class="sxs-lookup"><span data-stu-id="66f9e-115">**Original budget**: Use the original budget amounts that are committed when the initial budget is created and approved.</span></span>
   - <span data-ttu-id="66f9e-116">**Restbudget**: Verwenden Sie die verbleibenden Budgetbeträge während des Verlaufs des Projekts.</span><span class="sxs-lookup"><span data-stu-id="66f9e-116">**Remaining budget**: Use the remaining budget amounts during the life of the project.</span></span> <span data-ttu-id="66f9e-117">Die Salden im Planzahlenmodell werden durch die tatsächlichen Buchungen reduziert und durch Budgetüberarbeitungen erhöht oder verringert.</span><span class="sxs-lookup"><span data-stu-id="66f9e-117">The balances in this forecast model are reduced by actual transactions and increased or decreased by budget revisions.</span></span>
   - <span data-ttu-id="66f9e-118">**Vortrag**: Verwenden Sie die Vortragsbudget-Beträge für das Projekt.</span><span class="sxs-lookup"><span data-stu-id="66f9e-118">**Carry-forward**: Use the carry-forward budget amounts for the project.</span></span> <span data-ttu-id="66f9e-119">Ein Vortrag ist ein optionaler Prozess, mit dem nicht verbrauchte Budgetbeträge auf ein anderes Geschäftsjahr übertragen werden können.</span><span class="sxs-lookup"><span data-stu-id="66f9e-119">Carry-forward is an optional process that can be run to transfer unused budget amounts from one fiscal year to another.</span></span>

7. <span data-ttu-id="66f9e-120">Legen Sie die folgenden Optionen nach Bedarf fest:</span><span class="sxs-lookup"><span data-stu-id="66f9e-120">Set the following options as required:</span></span>

   - <span data-ttu-id="66f9e-121">Aktivieren Sie **Prognose-Rechnungsdatum**, um das Projektdatum als Rechnungsdatum zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="66f9e-121">Enable **Forecast invoice date** to use the project date as the invoice date.</span></span>
   - <span data-ttu-id="66f9e-122">Aktivieren Sie **Prognose mit RIF**, um eine Prognose anhand der laufenden Arbeit (RIF) zu treffen, und wählen Sie dann den RIF-Typ aus.</span><span class="sxs-lookup"><span data-stu-id="66f9e-122">Enable **Forecast with WIP** to forecast based on work in progress (WIP), and then select the type of WIP.</span></span> 
   - <span data-ttu-id="66f9e-123">Sie können den standardmäßigen **Budgettyp** als **Keiner** beibehalten oder einen neuen Typ eingeben.</span><span class="sxs-lookup"><span data-stu-id="66f9e-123">You can keep the default **Budget type** as **None** or enter a new type.</span></span> <span data-ttu-id="66f9e-124">Der Budgettyp kann nicht geändert werden, nachdem Sie einen Datensatz geändert haben.</span><span class="sxs-lookup"><span data-stu-id="66f9e-124">The budget type can't be changed after you change a record.</span></span>     
    > [!NOTE]
    > <span data-ttu-id="66f9e-125">Wenn Sie den Standardbudgettyp ändern, stehen alle anderen Optionen nicht mehr für Updates zur Verfügung, und Sie können dieses Planzahlenmodell nicht wiederverwenden.</span><span class="sxs-lookup"><span data-stu-id="66f9e-125">If you change the default budget type, all other options will become unavailable for updates, and you can't reuse this forecast model.</span></span> 
   


 

