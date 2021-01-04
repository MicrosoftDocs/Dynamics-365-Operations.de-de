---
title: Einrichten von Nummernkreisen mit einem Assistenten
description: In diesem Abschnitt wird erläutert, wie Sie mit Hilfe eines Assistenten alle erforderlichen Zahlenreihen gleichzeitig einrichten können.
author: sericks007
manager: AnnBe
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: NumberSequenceTableListPage, NumberSequenceWizard
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ca8174444d5a84f7efb402d6efc787e693801e82
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "4694738"
---
# <a name="set-up-number-sequences-using-a-wizard"></a><span data-ttu-id="7bd0a-103">Einrichten von Nummernkreisen mit einem Assistenten</span><span class="sxs-lookup"><span data-stu-id="7bd0a-103">Set up number sequences using a wizard</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7bd0a-104">Nummernkreise dienen zum Generieren von lesbaren, eindeutigen Kennungen für Masterdaten- und Buchungsdatensätze, die diese benötigen.</span><span class="sxs-lookup"><span data-stu-id="7bd0a-104">Number sequences are used to generate readable, unique identifiers for master data records and transaction records that require them.</span></span> <span data-ttu-id="7bd0a-105">Ein Masterdaten- oder Buchungsdatensatz, der eine Kennung erfordert, wird als Referenz bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="7bd0a-105">A master data or transaction record that requires an identifier is referred to as a reference.</span></span> <span data-ttu-id="7bd0a-106">Bevor neue Datensätze für eine Referenz erstellt werden können, muss ein Nummernkreis eingerichtet und der Referenz zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="7bd0a-106">Before you can create new records for a reference, you must set up a number sequence and associate it with the reference.</span></span> <span data-ttu-id="7bd0a-107">In diesem Abschnitt wird erläutert, wie Sie mit Hilfe eines Assistenten alle erforderlichen Zahlenreihen gleichzeitig einrichten können.</span><span class="sxs-lookup"><span data-stu-id="7bd0a-107">This topic explains how to set up all required number sequences at the same time by using a wizard.</span></span> <span data-ttu-id="7bd0a-108">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="7bd0a-108">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="7bd0a-109">Gehen Sie zu **Navigation > Module > Organisationsverwaltung > Zahlenreihen > Zahlenreihen**.</span><span class="sxs-lookup"><span data-stu-id="7bd0a-109">Go to **Navigation > Modules > Organization administration > Number sequences > Number sequences**.</span></span>
2. <span data-ttu-id="7bd0a-110">Wählen Sie **Generieren**.</span><span class="sxs-lookup"><span data-stu-id="7bd0a-110">Select **Generate**.</span></span>
3. <span data-ttu-id="7bd0a-111">Wählen Sie **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="7bd0a-111">Select **Next**.</span></span>

   - <span data-ttu-id="7bd0a-112">Auf dieser Seite können der Kennungscode, der niedrigste Wert und der höchste Wert geändert werden.</span><span class="sxs-lookup"><span data-stu-id="7bd0a-112">On this page, you can modify the identification code, the lowest value, and the highest value.</span></span> <span data-ttu-id="7bd0a-113">Zudem kann auf dieser Seite angegeben werden, ob der aktuelle Nummernkreis fortlaufend sein muss.</span><span class="sxs-lookup"><span data-stu-id="7bd0a-113">In addition, you can indicate whether the number sequence must be continuous.</span></span>   
   - <span data-ttu-id="7bd0a-114">Wählen Sie die Option **Kontinuierlich** nicht, wenn Sie Zahlen für die Zahlenfolge vorbelegen müssen.</span><span class="sxs-lookup"><span data-stu-id="7bd0a-114">Do not select the **Continuous** option if you must preallocate numbers for the number sequence.</span></span> <span data-ttu-id="7bd0a-115">Um ein Umfangssegment zum Format einer Zahlenfolge hinzuzufügen, wählen Sie das Format in der Liste aus und wählen Sie dann **Umfang in Format** aufnehmen.</span><span class="sxs-lookup"><span data-stu-id="7bd0a-115">To add a scope segment to the format of a number sequence, select the format in the list, and then select **Include scope in format**.</span></span> <span data-ttu-id="7bd0a-116">Um ein Umfangssegment aus dem Format einer Zahlenfolge zu entfernen, wählen Sie das Format in der Liste aus und wählen Sie dann **Scope aus dem Format** entfernen.</span><span class="sxs-lookup"><span data-stu-id="7bd0a-116">To remove a scope segment from the format of a number sequence, select the format in the list, and then select **Remove scope from format**.</span></span> <span data-ttu-id="7bd0a-117">Um eine Zahlenfolge von der automatischen Generierung auszuschließen, markieren Sie die Zahlenfolge in der Liste und wählen Sie dann **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="7bd0a-117">To exclude a number sequence from automatic generation, select the number sequence in the list, and then select **Delete**.</span></span>  

4. <span data-ttu-id="7bd0a-118">Wählen Sie **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="7bd0a-118">Select **Next**.</span></span>
5. <span data-ttu-id="7bd0a-119">Wählen Sie **Fertig stellen** aus.</span><span class="sxs-lookup"><span data-stu-id="7bd0a-119">Select **Finish**.</span></span>

