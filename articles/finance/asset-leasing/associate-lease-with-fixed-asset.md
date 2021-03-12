---
title: Anlagevermögen mit einem Mietvertrag verknüpfen
description: In diesem Thema wird erläutert, wie Sie eine vorhandene Anlage einem neuen Mietvertrag zuordnen.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 274fcc73b48282a8025a210dd488105500609d5a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971427"
---
# <a name="associate-fixed-assets-with-leases"></a><span data-ttu-id="44067-103">Anlagevermögen mit einem Mietvertrag verknüpfen</span><span class="sxs-lookup"><span data-stu-id="44067-103">Associate fixed assets with leases</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="44067-104">In diesem Thema wird erläutert, wie Sie eine vorhandene Anlage einem neuen Mietvertrag zuordnen.</span><span class="sxs-lookup"><span data-stu-id="44067-104">The topic explains how to associate an existing fixed asset with a new lease.</span></span> <span data-ttu-id="44067-105">Wenn Sie eine Anlage einem Mietvertrag verknüpfen, entspricht der Wert des Nutzungsrechts am Leasingobjekt bei der erstmaligen Erfassung den Anschaffungskosten der Anlage.</span><span class="sxs-lookup"><span data-stu-id="44067-105">When you associate a fixed asset with a lease, the right-of-use (ROU) asset value at initial recognition will be the acquisition cost of the fixed asset.</span></span>

<span data-ttu-id="44067-106">Bevor Sie eine Anlage einem Mietvertrag zuordnen können, müssen Sie im Anlagevermögen einen Datensatz für das Anlagevermögen erstellen.</span><span class="sxs-lookup"><span data-stu-id="44067-106">Before you can associate a fixed asset with a lease, you must create a record for the fixed asset in Fixed assets.</span></span> <span data-ttu-id="44067-107">Dann müssen Sie auf der **Mietvertragsübersicht** Seite einen Mietvertrag erstellen und die Anlage mit damit verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="44067-107">Then, on the **Lease summary** page, you must create a lease and link the asset to that lease.</span></span>

1. <span data-ttu-id="44067-108">Fügen Sie einen Mietvertrag hinzu, indem Sie die Schritte in [Mietverträge hinzufügen oder kopieren](add-lease.md) ausführen.</span><span class="sxs-lookup"><span data-stu-id="44067-108">Add a lease by following the steps in [Add or copy leases](add-lease.md).</span></span> <span data-ttu-id="44067-109">Wählen Sie auf der **Mietvertrag hinzufügen**-Seite im Feld **Anlagennnummer** die Anlage aus, die noch nicht erworben wurde.</span><span class="sxs-lookup"><span data-stu-id="44067-109">On the **Add lease** page, in the **Fixed asset number** field, select the asset that hasn't yet been acquired.</span></span>
2. <span data-ttu-id="44067-110">Wählen Sie **Bücher** und bestätigen Sie den Zahlungsplan.</span><span class="sxs-lookup"><span data-stu-id="44067-110">Select **Books**, and confirm the payment schedule.</span></span>
3. <span data-ttu-id="44067-111">Wählen Sie **Erstmalige Erfassung**.</span><span class="sxs-lookup"><span data-stu-id="44067-111">Select **Initial recognition**.</span></span>
4. <span data-ttu-id="44067-112">Wählen Sie **Erfassung für Anlagenleasing**.</span><span class="sxs-lookup"><span data-stu-id="44067-112">Select **Asset leasing journal**.</span></span>

    <span data-ttu-id="44067-113">Der Journaleintrag der erstmaligen Erfassung für den Mietvertrag belastet die Anlage mit dem Betrag, der normalerweise dem Konto für das Nutzungsrecht am Leasingobjekt belastet wird.</span><span class="sxs-lookup"><span data-stu-id="44067-113">The initial recognition journal entry for the lease debits the fixed asset for the amount that is usually debited to the ROU asset account.</span></span>

    <span data-ttu-id="44067-114">Sie können jetzt die Transaktionsart anzeigen und für die Anlage buchen.</span><span class="sxs-lookup"><span data-stu-id="44067-114">You can now view the transaction type and book for the fixed asset.</span></span>

5. <span data-ttu-id="44067-115">Wählen Sie **Erfassungsdetails**.</span><span class="sxs-lookup"><span data-stu-id="44067-115">Select **Journal details**.</span></span>
6. <span data-ttu-id="44067-116">Wählen Sie **Zeilen**, um die einzelnen Zeilen für den Journaleintrag anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="44067-116">Select **Lines** to view the individual lines for the journal entry.</span></span>
7. <span data-ttu-id="44067-117">Wählen Sie die Erfassungszeile aus, die die Anlage enthält, und wählen Sie dann die Registerkarte **Anlagevermögen** aus.</span><span class="sxs-lookup"><span data-stu-id="44067-117">Select the journal line that contains the asset, and then select the **Fixed Assets** tab.</span></span>

    <span data-ttu-id="44067-118">Die Registerkarte **Anlagevermögen** zeigt die Transaktionsart und das Buch.</span><span class="sxs-lookup"><span data-stu-id="44067-118">The **Fixed assets** tab shows the transaction type and the book.</span></span> <span data-ttu-id="44067-119">Standardmäßig ist das **Transaktionart**-Feld auf **Anschaffung** festgelegt, und das **Buch**-Feld wird auf das aktuelle Buch für die Anlage gesetzt.</span><span class="sxs-lookup"><span data-stu-id="44067-119">By default, the **Transaction type** field is set to **Acquisition**, and the **Book** field is set to the current book for the fixed asset.</span></span>

<span data-ttu-id="44067-120">Nachdem Sie den Journaleintrag der erstmaligen Erfassung gebucht haben, wird die Transaktion als Anschaffungstransaktion für die Anlage angezeigt.</span><span class="sxs-lookup"><span data-stu-id="44067-120">After you post the initial recognition journal entry, the transaction appears as an acquisition transaction for the fixed asset.</span></span> <span data-ttu-id="44067-121">Um die Transaktionstabelle anzuzeigen, gehen Sie zu **Anlagevermögen \> Anlagevermögen \> Anlagevermögen**, wählen Sie die entsprechende Anlage und dann **Bewertungen** aus.</span><span class="sxs-lookup"><span data-stu-id="44067-121">To view the transaction table, go to **Fixed assets \> Fixed assets \> Fixed assets**, select the appropriate asset, and then select **Valuations**.</span></span> <span data-ttu-id="44067-122">Sie sollte sehen, dass der Journaleintrag der erstmaligen Erfassung eine Anschaffungstransaktion für die angegebene Anlage erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="44067-122">You should see that the initial recognition journal entry has created an acquisition transaction for the specified fixed asset.</span></span>

<span data-ttu-id="44067-123">Die Anlage kann jetzt mithilfe der Standardabschreibungsfunktion im Anlagevermögen abgeschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="44067-123">The fixed asset can now be depreciated by using the standard depreciation functionality in Fixed assets.</span></span> <span data-ttu-id="44067-124">Weitere Informationen zur Abschreibung finden Sie untere [Abschreibungsmethoden und - konventionen](../fixed-assets/depreciation-methods-conventions.md).</span><span class="sxs-lookup"><span data-stu-id="44067-124">For more information about depreciation, see [Depreciation methods and conventions](../fixed-assets/depreciation-methods-conventions.md).</span></span>

> [!NOTE]
> <span data-ttu-id="44067-125">Wenn Sie eine Anlage mit einem Mietvertrag verknüpfen, wird die **Anlagenabschreibung** und **Leasingminderung** Schaltflächen im Anlagenvermögen deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="44067-125">If you associate a fixed asset with a lease, the **Asset depreciation** and **Lease impairment** buttons are disabled in Asset leasing.</span></span> <span data-ttu-id="44067-126">Sie können Transaktionen zur Anlagenabschreibung und zur Leasingminderung im Anlagevermögen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="44067-126">You can view asset depreciation and lease impairment transactions from Fixed assets.</span></span> <span data-ttu-id="44067-127">Die **Anlagentransaktionen**-Schaltfläche, mit der ein Anfrageformular geöffnet wird, ist ebenfalls deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="44067-127">The **Asset transactions** button, which opens an inquiry form is also disabled.</span></span> <span data-ttu-id="44067-128">Sie können auch das **Anlagentransaktionen** -Anfrageformular im Anlagevermögen öffnen.</span><span class="sxs-lookup"><span data-stu-id="44067-128">You can also open the **Asset transactions** inquiry form in Fixed assets.</span></span>  
