---
title: Übergeben von zurückgelieferten Artikeln zur Prüfung
description: Beim Erfassen eines zurückgelieferten Artikels können Sie festlegen, dass ein Artikel zur Prüfung gesendet wird, bevor er an das Lager zurückgegeben oder anderweitig veräußert wird.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WMSJournalTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bdee1ed2c7e98843e5dcfe9669e6a7c1eb11173c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810677"
---
# <a name="pass-returned-items-on-to-inspection"></a><span data-ttu-id="1fd78-103">Übergeben von zurückgelieferten Artikeln zur Prüfung</span><span class="sxs-lookup"><span data-stu-id="1fd78-103">Pass returned items on to inspection</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="1fd78-104">Beim Erfassen eines zurückgelieferten Artikels können Sie festlegen, dass ein Artikel zur Prüfung gesendet wird, bevor er an das Lager zurückgegeben oder anderweitig veräußert wird.</span><span class="sxs-lookup"><span data-stu-id="1fd78-104">When registering a returned item, you may determine that an item should be sent for inspection before it is returned to inventory or disposed of in some other way.</span></span>

1.  <span data-ttu-id="1fd78-105">Klicken Sie auf **Lagerverwaltung** \> **Journaleinträge** \> **Wareneingang** \> **Wareneingang**.</span><span class="sxs-lookup"><span data-stu-id="1fd78-105">Click **Inventory management** \> **Journals** \> **Item arrival** \> **Item arrival**.</span></span>
    
    <span data-ttu-id="1fd78-106">\-oder-</span><span class="sxs-lookup"><span data-stu-id="1fd78-106">\-or-</span></span>
    
    <span data-ttu-id="1fd78-107">Klicken Sie auf **Lagerverwaltung** \> **Journaleinträge** \> **Wareneingang** \> **Produktions-Wareneingang**.</span><span class="sxs-lookup"><span data-stu-id="1fd78-107">Click **Inventory management** \> **Journals** \> **Item arrival** \> **Production input**.</span></span>

2.  <span data-ttu-id="1fd78-108">Erfassen Sie den Zugang eines Artikels wie gewohnt im Formular **Lagerplatzerfassung**.</span><span class="sxs-lookup"><span data-stu-id="1fd78-108">On the **Location journal** form, register the receipt of an item as usual.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="1fd78-109">Informationen zum Erfassen des Zugangs zurückgelieferter Artikel finden Sie, <A href="register-the-receipt-of-returned-items.md">Erfassen des Empfangs zurückgelieferter Artikel</A></span><span class="sxs-lookup"><span data-stu-id="1fd78-109">For information about registering the receipt of returned items, see <A href="register-the-receipt-of-returned-items.md">Register the receipt of returned items</A></span></span></P>



3.  <span data-ttu-id="1fd78-110">Auf der Registerkarte **Standardwerte** im Bereich **Handhabungsmodus**, wählen Sie das Feld **Quarantäneverwaltung** aus.</span><span class="sxs-lookup"><span data-stu-id="1fd78-110">On the **Default values** tab, in the **Mode of handling** area, select the **Quarantine management** box.</span></span>

<span data-ttu-id="1fd78-111">Damit wird das System aufgefordert, einen Quarantäneauftrag zu erstellen, und die Person bzw. die Abteilung, die Prüfungen durchführt, antwortet auf diesen Auftrag mithilfe des Formulars **Quarantäneauftrag**.</span><span class="sxs-lookup"><span data-stu-id="1fd78-111">This will prompt the system to create a quarantine order, and the person or department that performs inspections will respond to this order using the **Quarantine order** form.</span></span>

## <a name="see-also"></a><span data-ttu-id="1fd78-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1fd78-112">See also</span></span>

[<span data-ttu-id="1fd78-113">Prüfen von zurückgelieferten Artikeln</span><span class="sxs-lookup"><span data-stu-id="1fd78-113">Take returned items through inspection</span></span>](take-returned-items-through-inspection.md)

[<span data-ttu-id="1fd78-114">Angeben zur Entsorgung zurückgelieferter Artikel</span><span class="sxs-lookup"><span data-stu-id="1fd78-114">Specify how to dispose of returned items</span></span>](specify-how-to-dispose-of-returned-items.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]