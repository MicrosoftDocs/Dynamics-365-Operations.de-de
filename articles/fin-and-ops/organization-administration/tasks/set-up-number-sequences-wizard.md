--- 
title: Einrichten von Nummernsequenzen mit einem Assistenten
description: "Nummernkreise dienen zum Generieren von lesbaren, eindeutigen Kennungen für Masterdaten- und Buchungsdatensätze, die diese benötigen."
author: sericks007
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e8f3227f231ffc287bd6ea6204ed50f8b684e5fb
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---
# <a name="set-up-number-sequences-by-using-a-wizard"></a><span data-ttu-id="64e8b-103">Einrichten von Nummernsequenzen mit einem Assistenten</span><span class="sxs-lookup"><span data-stu-id="64e8b-103">Set up number sequences by using a wizard</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="64e8b-104">Nummernkreise dienen zum Generieren von lesbaren, eindeutigen Kennungen für Masterdaten- und Buchungsdatensätze, die diese benötigen.</span><span class="sxs-lookup"><span data-stu-id="64e8b-104">Number sequences are used to generate readable, unique identifiers for master data records and transaction records that require them.</span></span> <span data-ttu-id="64e8b-105">Ein Masterdaten- oder Buchungsdatensatz, der eine Kennung erfordert, wird als Referenz bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="64e8b-105">A master data or transaction record that requires an identifier is referred to as a reference.</span></span> <span data-ttu-id="64e8b-106">Bevor neue Datensätze für eine Referenz erstellt werden können, muss ein Nummernkreis eingerichtet und der Referenz zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="64e8b-106">Before you can create new records for a reference, you must set up a number sequence and associate it with the reference.</span></span> <span data-ttu-id="64e8b-107">Dieses Verfahren zeigt, wie alle erforderlichen Nummernkreise gleichzeitig eingerichtet, indem Sie einen Assistenten verwendet.</span><span class="sxs-lookup"><span data-stu-id="64e8b-107">This procedure explains how to set up all required number sequences at the same time by using a wizard.</span></span> <span data-ttu-id="64e8b-108">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="64e8b-108">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="64e8b-109">Wechseln Sie zu "Organisationsverwaltung" > "Nummernkreise" > "Nummernkreise".</span><span class="sxs-lookup"><span data-stu-id="64e8b-109">Go to Organization administration > Number sequences > Number sequences.</span></span>
2. <span data-ttu-id="64e8b-110">Klicken Sie "Generieren".</span><span class="sxs-lookup"><span data-stu-id="64e8b-110">Click Generate.</span></span>
3. <span data-ttu-id="64e8b-111">Klicken Sie auf Weiter.</span><span class="sxs-lookup"><span data-stu-id="64e8b-111">Click Next.</span></span>
    * <span data-ttu-id="64e8b-112">Auf dieser Seite können der Kennungscode, der niedrigste Wert und der höchste Wert geändert werden.</span><span class="sxs-lookup"><span data-stu-id="64e8b-112">On this page, you can modify the identification code, the lowest value, and the highest value.</span></span> <span data-ttu-id="64e8b-113">Zudem kann auf dieser Seite angegeben werden, ob der aktuelle Nummernkreis fortlaufend sein muss.</span><span class="sxs-lookup"><span data-stu-id="64e8b-113">In addition, you can indicate whether the number sequence must be continuous.</span></span>   
    * <span data-ttu-id="64e8b-114">Wählen Sie die Option Fortlaufend nicht aus, wenn die Nummern für den Nummernkreis vorab zugeordnet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="64e8b-114">Do not select the Continuous option if you must preallocate numbers for the number sequence.</span></span>     <span data-ttu-id="64e8b-115">Sie können ein Bereichssegment zum Format eines Nummernkreises hinzufügen, indem Sie das Format in der Liste auswählen und dann auf "Bereich in Format einschließen" klicken.</span><span class="sxs-lookup"><span data-stu-id="64e8b-115">To add a scope segment to the format of a number sequence, select the format in the list, and then click Include scope in format.</span></span>     <span data-ttu-id="64e8b-116">Sie können ein Bereichssegment aus dem Format eines Nummernkreises entfernen, indem Sie das Format in der Liste auswählen und dann auf "Bereich aus Format entfernen" klicken.</span><span class="sxs-lookup"><span data-stu-id="64e8b-116">To remove a scope segment from the format of a number sequence, select the format in the list, and then click Remove scope from format.</span></span>     <span data-ttu-id="64e8b-117">Wenn Sie einen Nummernkreis aus der automatischen Generierung ausschließen möchten, wählen Sie den Nummernkreis in der Liste aus, und klicken Sie dann auf Löschen.</span><span class="sxs-lookup"><span data-stu-id="64e8b-117">To exclude a number sequence from automatic generation, select the number sequence in the list, and then click Delete.</span></span>  
4. <span data-ttu-id="64e8b-118">Klicken Sie auf Weiter.</span><span class="sxs-lookup"><span data-stu-id="64e8b-118">Click Next.</span></span>
5. <span data-ttu-id="64e8b-119">Klicken Sie auf Fertig stellen.</span><span class="sxs-lookup"><span data-stu-id="64e8b-119">Click Finish.</span></span>


