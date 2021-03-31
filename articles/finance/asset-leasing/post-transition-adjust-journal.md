---
title: Journaleinträge für die Übergangsregulierung im Anlagenleasing
description: In diesem Thema werden die Funktionen beschrieben, mit denen Sie ein Leasingportfolio auf die neuen Leasing-Rechnungslegungsstandards, des Themas 842 zur Kodifizierung von Rechnungslegungsstandards(ASC 842) und den International Financial Reporting Standard 16 (IFRS 16) umstellen können.
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
ms.openlocfilehash: 7ed62f52753a6697a7547ada0317041669cf3506
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207204"
---
# <a name="post-transition-adjustment-journal-entries-in-asset-leasing"></a><span data-ttu-id="e7448-103">Journaleinträge für die Übergangsregulierung im Anlagenleasing</span><span class="sxs-lookup"><span data-stu-id="e7448-103">Post transition adjustment journal entries in Asset leasing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e7448-104">In diesem Thema werden die Funktionen beschrieben, mit denen Sie ein Leasingportfolio auf die neuen Leasingbuchhaltungsstandards umstellen können: Thema 842 zur Kodifizierung von Rechnungslegungsstandards (ASC 842), der Standard in den allgemein anerkannten Rechnungslegungsgrundsätzen in den USA (US-GAAP), und International Financial Reporting Standard 16 (IFRS 16).</span><span class="sxs-lookup"><span data-stu-id="e7448-104">This topic describes the functionality that lets you transition a lease portfolio to the new lease accounting standards: Accounting Standards Codification Topic 842 (ASC 842), which is the standard in Generally Accepted Accounting Principles in the US (US GAAP), and International Financial Reporting Standard 16 (IFRS 16).</span></span>

<span data-ttu-id="e7448-105">Informationen zum Einrichten eines Buches für den Übergang zu den neuen Standards finden Sie unter [Leasingbücher einrichten](set-up-lease-books.md).</span><span class="sxs-lookup"><span data-stu-id="e7448-105">For information about how to set up a book for the transition to the new standards, see [Set up lease books](set-up-lease-books.md).</span></span>

<span data-ttu-id="e7448-106">Wenn Sie einen Journaleintrag für die Übergangsregulierung erstellen, wird ein Journaleintrag generiert.</span><span class="sxs-lookup"><span data-stu-id="e7448-106">When you create a transition adjustment journal entry, a journal entry is generated.</span></span> <span data-ttu-id="e7448-107">Dieser Eintrag spiegelt die Auswirkungen der Erfassung des Mietvertrags auf die Bilanzberichte nach den neuen Standards zu diesem Zeitpunkt wider.</span><span class="sxs-lookup"><span data-stu-id="e7448-107">This entry reflects the balance sheet impact of recording the lease under the new standards on that date.</span></span> <span data-ttu-id="e7448-108">Das entsprechende Aktivkonto wird an diesem Tag mit dem Buchwert belastet, und das Passivkonto wird gutgeschrieben.</span><span class="sxs-lookup"><span data-stu-id="e7448-108">The appropriate asset account is debited for the carrying amount on that date, and the liability account is credited.</span></span> <span data-ttu-id="e7448-109">Die Differenz wird entweder belastet oder den Gewinnrücklagen gutgeschrieben.</span><span class="sxs-lookup"><span data-stu-id="e7448-109">The difference is either debited or credited to retained earnings.</span></span>

<span data-ttu-id="e7448-110">Führen Sie die folgenden Schritte aus, um eine Übergangsregulierung gemäß den neuen Rechnungslegungsstandards vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="e7448-110">To post a transition adjustment in compliance with the new accounting standards, follow these steps.</span></span>

1. <span data-ttu-id="e7448-111">Auf der **Mietvertragsübersicht**-Seite, wählen Sie den Mietvertrag und dann **Bücher**.</span><span class="sxs-lookup"><span data-stu-id="e7448-111">On the **Lease summary** page, select the lease, and then select **Books**.</span></span>
2. <span data-ttu-id="e7448-112">Wählen Sie im Buch **Zahlungsplan**.</span><span class="sxs-lookup"><span data-stu-id="e7448-112">In the book, select **Payment schedule**.</span></span>
3. <span data-ttu-id="e7448-113">In dem **Zahlungsplan**-Dialogfeld wählen Sie **Bestätigen**.</span><span class="sxs-lookup"><span data-stu-id="e7448-113">In the **Payment schedule** dialog box, select **Confirm**.</span></span> <span data-ttu-id="e7448-114">Schließen Sie dann das Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="e7448-114">Then close the dialog box.</span></span>
4. <span data-ttu-id="e7448-115">Wählen Sie **Übergangsregulierung**.</span><span class="sxs-lookup"><span data-stu-id="e7448-115">Select **Transition adjustment**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e7448-116">Eine Übergangsregulierung kann nur für Leasingbücher erstellt werden, die einem Buch zugeordnet sind, in dem das **Übergangsbuch**-Feld ist verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e7448-116">A transition adjustment can be created only for lease books that are assigned to a book where the **Transition book** field is available.</span></span> <span data-ttu-id="e7448-117">Wenn der Wert im **Mietbeginn**-Feld später als das Übergangsdatum liegt, wird der Wert im Feld **Übergangsregulierung** nicht aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="e7448-117">If the value in the **Lease commencement** field is later than the transition date, the value in the **Transition adjustment** field won't be updated.</span></span>

5. <span data-ttu-id="e7448-118">Um den Journaleintrag anzuzeigen, wählen Sie **Anlagenleasingerfassungen** aus.</span><span class="sxs-lookup"><span data-stu-id="e7448-118">To view the journal entry, select **Asset leasing journals**.</span></span>
6. <span data-ttu-id="e7448-119">Wählen Sie die neuen Erfassung aus dann **Buchen**.</span><span class="sxs-lookup"><span data-stu-id="e7448-119">Select the new journal, and then select **Post**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]