---
title: Anlagevermögen mit einem Mietvertrag verknüpfen
description: In diesem Thema wird erläutert, wie Sie eine vorhandene Anlage einem neuen Mietvertrag zuordnen.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseDetail
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 02a17b8c995e8aa97384d8b855afb688324017d6
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881347"
---
# <a name="associate-fixed-assets-with-leases"></a><span data-ttu-id="fcdee-103">Anlagevermögen mit einem Mietvertrag verknüpfen</span><span class="sxs-lookup"><span data-stu-id="fcdee-103">Associate fixed assets with leases</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fcdee-104">In diesem Thema wird erläutert, wie Sie eine vorhandene Anlage einem neuen Mietvertrag zuordnen.</span><span class="sxs-lookup"><span data-stu-id="fcdee-104">The topic explains how to associate an existing fixed asset with a new lease.</span></span> <span data-ttu-id="fcdee-105">Wenn Sie eine Anlage einem Mietvertrag verknüpfen, entspricht der Wert des Nutzungsrechts am Leasingobjekt bei der erstmaligen Erfassung den Anschaffungskosten der Anlage.</span><span class="sxs-lookup"><span data-stu-id="fcdee-105">When you associate a fixed asset with a lease, the right-of-use (ROU) asset value at initial recognition will be the acquisition cost of the fixed asset.</span></span>

<span data-ttu-id="fcdee-106">Bevor Sie eine Anlage einem Mietvertrag zuordnen können, müssen Sie im Anlagevermögen einen Datensatz für das Anlagevermögen erstellen.</span><span class="sxs-lookup"><span data-stu-id="fcdee-106">Before you can associate a fixed asset with a lease, you must create a record for the fixed asset in Fixed assets.</span></span> <span data-ttu-id="fcdee-107">Dann müssen Sie auf der **Mietvertragsübersicht** Seite einen Mietvertrag erstellen und die Anlage mit damit verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="fcdee-107">Then, on the **Lease summary** page, you must create a lease and link the asset to that lease.</span></span>

1. <span data-ttu-id="fcdee-108">Fügen Sie einen Mietvertrag hinzu, indem Sie die Schritte in [Mietverträge hinzufügen oder kopieren](add-lease.md) ausführen.</span><span class="sxs-lookup"><span data-stu-id="fcdee-108">Add a lease by following the steps in [Add or copy leases](add-lease.md).</span></span> <span data-ttu-id="fcdee-109">Wählen Sie auf der **Mietvertrag hinzufügen**-Seite im Feld **Anlagennnummer** die Anlage aus, die noch nicht erworben wurde.</span><span class="sxs-lookup"><span data-stu-id="fcdee-109">On the **Add lease** page, in the **Fixed asset number** field, select the asset that hasn't yet been acquired.</span></span>
2. <span data-ttu-id="fcdee-110">Wählen Sie **Bücher** und bestätigen Sie den Zahlungsplan.</span><span class="sxs-lookup"><span data-stu-id="fcdee-110">Select **Books**, and confirm the payment schedule.</span></span>
3. <span data-ttu-id="fcdee-111">Wählen Sie **Erstmalige Erfassung**.</span><span class="sxs-lookup"><span data-stu-id="fcdee-111">Select **Initial recognition**.</span></span>
4. <span data-ttu-id="fcdee-112">Wählen Sie **Erfassung für Anlagenleasing**.</span><span class="sxs-lookup"><span data-stu-id="fcdee-112">Select **Asset leasing journal**.</span></span>

    <span data-ttu-id="fcdee-113">Der Journaleintrag der erstmaligen Erfassung für den Mietvertrag belastet die Anlage mit dem Betrag, der normalerweise dem Konto für das Nutzungsrecht am Leasingobjekt belastet wird.</span><span class="sxs-lookup"><span data-stu-id="fcdee-113">The initial recognition journal entry for the lease debits the fixed asset for the amount that is usually debited to the ROU asset account.</span></span>

    <span data-ttu-id="fcdee-114">Sie können jetzt die Transaktionsart anzeigen und für die Anlage buchen.</span><span class="sxs-lookup"><span data-stu-id="fcdee-114">You can now view the transaction type and book for the fixed asset.</span></span>

5. <span data-ttu-id="fcdee-115">Wählen Sie **Erfassungsdetails**.</span><span class="sxs-lookup"><span data-stu-id="fcdee-115">Select **Journal details**.</span></span>
6. <span data-ttu-id="fcdee-116">Wählen Sie **Zeilen**, um die einzelnen Zeilen für den Journaleintrag anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="fcdee-116">Select **Lines** to view the individual lines for the journal entry.</span></span>
7. <span data-ttu-id="fcdee-117">Wählen Sie die Erfassungszeile aus, die die Anlage enthält, und wählen Sie dann die Registerkarte **Anlagevermögen** aus.</span><span class="sxs-lookup"><span data-stu-id="fcdee-117">Select the journal line that contains the asset, and then select the **Fixed Assets** tab.</span></span>

    <span data-ttu-id="fcdee-118">Die Registerkarte **Anlagevermögen** zeigt die Transaktionsart und das Buch.</span><span class="sxs-lookup"><span data-stu-id="fcdee-118">The **Fixed assets** tab shows the transaction type and the book.</span></span> <span data-ttu-id="fcdee-119">Standardmäßig ist das **Transaktionart**-Feld auf **Anschaffung** festgelegt, und das **Buch**-Feld wird auf das aktuelle Buch für die Anlage gesetzt.</span><span class="sxs-lookup"><span data-stu-id="fcdee-119">By default, the **Transaction type** field is set to **Acquisition**, and the **Book** field is set to the current book for the fixed asset.</span></span>

<span data-ttu-id="fcdee-120">Nachdem Sie den Journaleintrag der erstmaligen Erfassung gebucht haben, wird die Transaktion als Anschaffungstransaktion für die Anlage angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fcdee-120">After you post the initial recognition journal entry, the transaction appears as an acquisition transaction for the fixed asset.</span></span> <span data-ttu-id="fcdee-121">Um die Transaktionstabelle anzuzeigen, gehen Sie zu **Anlagevermögen \> Anlagevermögen \> Anlagevermögen**, wählen Sie die entsprechende Anlage und dann **Bewertungen** aus.</span><span class="sxs-lookup"><span data-stu-id="fcdee-121">To view the transaction table, go to **Fixed assets \> Fixed assets \> Fixed assets**, select the appropriate asset, and then select **Valuations**.</span></span> <span data-ttu-id="fcdee-122">Sie sollte sehen, dass der Journaleintrag der erstmaligen Erfassung eine Anschaffungstransaktion für die angegebene Anlage erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="fcdee-122">You should see that the initial recognition journal entry has created an acquisition transaction for the specified fixed asset.</span></span>

<span data-ttu-id="fcdee-123">Die Anlage kann jetzt mithilfe der Standardabschreibungsfunktion im Anlagevermögen abgeschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="fcdee-123">The fixed asset can now be depreciated by using the standard depreciation functionality in Fixed assets.</span></span> <span data-ttu-id="fcdee-124">Weitere Informationen zur Abschreibung finden Sie untere [Abschreibungsmethoden und - konventionen](../fixed-assets/depreciation-methods-conventions.md).</span><span class="sxs-lookup"><span data-stu-id="fcdee-124">For more information about depreciation, see [Depreciation methods and conventions](../fixed-assets/depreciation-methods-conventions.md).</span></span>

> [!NOTE]
> <span data-ttu-id="fcdee-125">Wenn Sie eine Anlage mit einem Mietvertrag verknüpfen, wird die **Anlagenabschreibung** und **Leasingminderung** Schaltflächen im Anlagenvermögen deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="fcdee-125">If you associate a fixed asset with a lease, the **Asset depreciation** and **Lease impairment** buttons are disabled in Asset leasing.</span></span> <span data-ttu-id="fcdee-126">Sie können Transaktionen zur Anlagenabschreibung und zur Leasingminderung im Anlagevermögen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="fcdee-126">You can view asset depreciation and lease impairment transactions from Fixed assets.</span></span> <span data-ttu-id="fcdee-127">Die **Anlagentransaktionen**-Schaltfläche, mit der ein Anfrageformular geöffnet wird, ist ebenfalls deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="fcdee-127">The **Asset transactions** button, which opens an inquiry form is also disabled.</span></span> <span data-ttu-id="fcdee-128">Sie können auch das **Anlagentransaktionen** -Anfrageformular im Anlagevermögen öffnen.</span><span class="sxs-lookup"><span data-stu-id="fcdee-128">You can also open the **Asset transactions** inquiry form in Fixed assets.</span></span>  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
