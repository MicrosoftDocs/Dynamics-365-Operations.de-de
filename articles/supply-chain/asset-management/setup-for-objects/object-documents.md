---
title: Anlagendokumente
description: In diesem Thema werden Anlagendokumente in Asset Management erläutert.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectDocument
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8458c302b506f9f048b7886f55a392d9afceb446
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808375"
---
# <a name="asset-documents"></a><span data-ttu-id="eeb72-103">Anlagendokumente</span><span class="sxs-lookup"><span data-stu-id="eeb72-103">Asset documents</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="eeb72-104">In diesem Thema werden Anlagendokumente in Asset Management erläutert.</span><span class="sxs-lookup"><span data-stu-id="eeb72-104">This topic explains asset documents in Asset Management.</span></span>

<span data-ttu-id="eeb72-105">In Asset Management können Sie Dokumente beispielsweise so einrichten, dass diese automatisch zu den Einzelvorgangstypen, den Anlagenherstellern, den Anlagentypen oder Anlagen zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="eeb72-105">In Asset Management, you can set up documents so that they are automatically related to job types, asset manufacturers, asset types, or assets, for example.</span></span> <span data-ttu-id="eeb72-106">Diese Funktion ist hilfreich, wenn aktualisierte Dokumentversionen freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="eeb72-106">This functionality is useful when updated document versions are released.</span></span> <span data-ttu-id="eeb72-107">In diesem Fall müssen Sie einfach das aktualisierte Dokument im Standardspeicherort ablegen, den Sie für Supply Chain Management-Dokumente verwenden, und Sie müssen das Dokument dem Anlagendokumentdatensatz zuordnen, den Sie erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="eeb72-107">In that case, you just have to put the updated document in the standard location that you use for your Supply Chain Management documents, and attach the document to the asset document record that you've created.</span></span> <span data-ttu-id="eeb72-108">Auf das aktualisierte Dokument kann dann über **Alle Anlagen**, **Aktive Anlagen**, **Meine aktiven Anlagen**, **Alle Arbeitsaufträge** und **Aktive Arbeitsauftragseinzelvorgänge** zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="eeb72-108">The updated document can then be accessed from the **All assets**, **Active assets**, **My active assets**, **All work orders**, and **Active work order jobs** menu items.</span></span> <span data-ttu-id="eeb72-109">Der Vorgang für das Zuordnen von Dokumenten zu einem Anlagendokumentdatensatz verwendet das Standardverfahren für die Dokumentverwaltung.</span><span class="sxs-lookup"><span data-stu-id="eeb72-109">The process for attaching documents to an asset document record uses the standard document handling system.</span></span>

<span data-ttu-id="eeb72-110">**Beispiel 1:** Ein Dokument, das einem Einzelvorgang zugeordnet ist, beschreibt möglicherweise eine Prozedur für diesen Einzelvorgangstyp.</span><span class="sxs-lookup"><span data-stu-id="eeb72-110">**Example 1:** A document that is related to a job type might describe a procedure for that job type.</span></span>

<span data-ttu-id="eeb72-111">**Beispiel 2:** Ein Dokument, das einer Kombination aus Anlagentyp, Hersteller und Modell zugeordnet ist, kann möglicherweise das Standardhandbuch für das ausgewählte Anlagenherstellermodell sein.</span><span class="sxs-lookup"><span data-stu-id="eeb72-111">**Example 2:** A document that is related to a combination of an asset type, manufacturer, and model might be the standard manual for the selected asset manufacturer model.</span></span>

## <a name="create-asset-document-relation"></a><span data-ttu-id="eeb72-112">Anlagendokumentzuordnung erstellen</span><span class="sxs-lookup"><span data-stu-id="eeb72-112">Create asset document relation</span></span>

1. <span data-ttu-id="eeb72-113">Wählen Sie **Anlagenverwaltung** \> **Einstellungen** \> **Anlagendokumente**.</span><span class="sxs-lookup"><span data-stu-id="eeb72-113">Select **Asset management** \> **Setup** \> **Asset documents**.</span></span>
2. <span data-ttu-id="eeb72-114">Wählen Sie **Neu**, um einen Anlagendokumentdatensatz zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="eeb72-114">Select **New** to create an asset document record.</span></span>
3. <span data-ttu-id="eeb72-115">Je nachdem, wie spezifisch die Dokumentzuordnung sein soll, nehmen Sie die entsprechende Auswahl in den folgenden Feldern vor: **Anlagentyp**, **Hersteller**, **Modell**, **Anlage**, **Einzelvorgangstypkategorie**, **Einzelvorgangstyp**, **Einzelvorgangstypvariante** und **Einzelvorgangsanforderung**.</span><span class="sxs-lookup"><span data-stu-id="eeb72-115">Depending on how specific you want the document relation to be, make relevant selections in one or more of the following fields: **Asset type**, **Manufacturer**, **Model**, **Asset**, **Job type category**, **Job type**, **Job type variant**, and **Job requirement**.</span></span> <span data-ttu-id="eeb72-116">Die Optionen, die in den Feldern **Einzelvorgangstypvariante** und **Einzelvorgangsanforderung** verfügbar sind, hängen von der Auswahl im Feld **Einzelvorgangstyp** ab.</span><span class="sxs-lookup"><span data-stu-id="eeb72-116">The options that are available in the **Job type variant** and **Job requirement** fields depend on your selection in the **Job type** field.</span></span>

    > [!NOTE]
    > <span data-ttu-id="eeb72-117">Wenn das System nach Dokumenten sucht, die einer Anlage oder einem Arbeitsauftrag zugeordnet sein sollten, durchläuft Asset Management alle Anlagendokumentdatensätze, um mögliche Übereinstimmungen zu finden.</span><span class="sxs-lookup"><span data-stu-id="eeb72-117">When the system searches for documents that should be related to an asset or a work order, Asset Management goes through all asset document records to check for a possible match.</span></span> <span data-ttu-id="eeb72-118">Die spezifischste Kombination wird immer zuerst geprüft.</span><span class="sxs-lookup"><span data-stu-id="eeb72-118">It always checks the most specific combination first.</span></span> <span data-ttu-id="eeb72-119">Das bedeutet, Asset Management sucht als Erstes nach einer Übereinstimmung für das Feld **Einzelvorgangsanforderung**.</span><span class="sxs-lookup"><span data-stu-id="eeb72-119">In other words, Asset Management first checks for a match for the **Job requirement** field.</span></span> <span data-ttu-id="eeb72-120">Wenn keine Übereinstimmung gefunden wird, sucht es nach einer Übereinstimmung für das Feld **Einzelvorgangstypvariante**.</span><span class="sxs-lookup"><span data-stu-id="eeb72-120">If no match is found, it checks for a match for the **Job type variant** field.</span></span> <span data-ttu-id="eeb72-121">Wenn keine Übereinstimmung gefunden wird, sucht es nach einer Übereinstimmung für das Feld **Einzelvorgangstyp** usw.</span><span class="sxs-lookup"><span data-stu-id="eeb72-121">If no match is found, it checks for a match for the **Job type** field, and so on.</span></span> <span data-ttu-id="eeb72-122">Wie Sie im Layout der Seite **Anlagendokumente** sehen können, bedeutet dieses Verhalten, dass Asset Management zum Auffinden der spezifischsten Kombinationen jeden Datensatz von rechts nach links auf Übereinstimmung prüft.</span><span class="sxs-lookup"><span data-stu-id="eeb72-122">As you can see in the layout of the **Asset documents** page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match.</span></span> <span data-ttu-id="eeb72-123">Es können mehrere Dokumente einer Anlage oder einem Arbeitsauftrag zugeordnet sein.</span><span class="sxs-lookup"><span data-stu-id="eeb72-123">Several documents might be related to an asset or a work order.</span></span> <span data-ttu-id="eeb72-124">Sie können den Servicelevel einer Wartungsanfrage oder eines Arbeitsauftrags bearbeiten, falls notwendig.</span><span class="sxs-lookup"><span data-stu-id="eeb72-124">You can edit the service level on a maintenance request or a work order as you require.</span></span>

4. <span data-ttu-id="eeb72-125">Wählen Sie **Anhänge** aus.</span><span class="sxs-lookup"><span data-stu-id="eeb72-125">Select **Attachments**.</span></span> <span data-ttu-id="eeb72-126">Die Standardseite **Handhabung von Dokumenten** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="eeb72-126">The standard **Document handling** page appears.</span></span>
5. <span data-ttu-id="eeb72-127">Hier können Sie die Dokumente oder Hinweise einrichten, die dem Anlagendokumentdatensatz zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="eeb72-127">Set up the documents or notes that should be attached to the asset document record.</span></span> <span data-ttu-id="eeb72-128">Nachdem Sie Dokumente zugeordnet haben, wird im Feld **Anhänge** die Anzahl der Dokumente angezeigt, die dem Datensatz zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="eeb72-128">After you attach documents, the **Attachments** field shows the number of documents that are related to the record.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]