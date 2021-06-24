---
title: Seriennummergesteuerte Produkte in POS zurückgeben
description: In diesem Thema werden die Funktionen zum Validieren von Artikeln mit Seriennummer als Teil des Rückgabeprozesses in der Microsoft Dynamics 365 Commerce Point-of-Sale-Anwendung (POS) beschrieben.
author: hhainesms
ms.date: 06/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 7a067994828f3df577c0dc4146d26ac81990d4ac
ms.sourcegitcommit: 927574c77f4883d906e5c7bddf0af9b717e492bf
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129809"
---
# <a name="return-serial-numbercontrolled-products-in-pos"></a><span data-ttu-id="b715d-103">Seriennummergesteuerte Produkte in POS zurückgeben</span><span class="sxs-lookup"><span data-stu-id="b715d-103">Return serial number–controlled products in POS</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="b715d-104">In diesem Thema werden die Funktionen zum Validieren von Artikeln mit Seriennummer als Teil des Rückgabeprozesses in der Microsoft Dynamics 365 Commerce Point-of-Sale-Anwendung (POS) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b715d-104">This topic describes the capabilities for validating serialized items as part of the return process in the Microsoft Dynamics 365 Commerce point of sale (POS) application.</span></span>

> [!NOTE]
> <span data-ttu-id="b715d-105">In der Commerce-Version 10.0.20 und höher wird eine neue Funktion mit dem Namen **Einheitliche Retourenbearbeitungserfahrung in POS** verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b715d-105">In the Commerce version 10.0.20 release and later, a new feature that is named **Unified return processing experience in POS** is available.</span></span> <span data-ttu-id="b715d-106">Um die Seriennummernvalidierung während der Retourenbearbeitung in POS zu verwenden, müssen Sie diese Funktion aktivieren.</span><span class="sxs-lookup"><span data-stu-id="b715d-106">To use serial number validation during return order processing in POS, you must turn on this feature.</span></span> <span data-ttu-id="b715d-107">Informationen zu anderen Funktionen, die diese Funktion bietet, wenn sie aktiviert ist, finden Sie unter [Retouren im POS erstellen)](POS-returns.md).</span><span class="sxs-lookup"><span data-stu-id="b715d-107">For information about others capabilities that this feature provides when it's turned on, see [Create returns in POS)](POS-returns.md).</span></span>
>
> <span data-ttu-id="b715d-108">Nachdem die Funktion aktiviert wurde, kann sie nicht mehr deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="b715d-108">After the feature is turned on, it can't be turned off.</span></span>

## <a name="options-for-validating-serialized-returns"></a><span data-ttu-id="b715d-109">Optionen zur Validierung serialisierter Retouren</span><span class="sxs-lookup"><span data-stu-id="b715d-109">Options for validating serialized returns</span></span>

<span data-ttu-id="b715d-110">Wenn die Funktion **Einheitliche Retourenbearbeitungserfahrung in POS** aktiviert ist, können Unternehmen eine Validierung von Rücksendungen von Artikeln mit Seriennummernkontrolle über POS durchführen.</span><span class="sxs-lookup"><span data-stu-id="b715d-110">When the **Unified return processing experience in POS** feature is turned on, organizations can perform a validation on returns of serial number–controlled items through POS.</span></span> <span data-ttu-id="b715d-111">Diese Funktion kann Benutzer warnen, wenn die zurückgegebene Seriennummer von der ursprünglich verkauften Seriennummer abweicht.</span><span class="sxs-lookup"><span data-stu-id="b715d-111">This capability can warn users if the serial number that is being returned differs from the original serial number that was sold.</span></span> <span data-ttu-id="b715d-112">In der Commerce-Version 10.0.20 und höher ist die Nachricht, die Benutzer erhalten, nur eine Warnmeldung.</span><span class="sxs-lookup"><span data-stu-id="b715d-112">In the Commerce version 10.0.20 release and later, the message that users receive is only a warning message.</span></span> <span data-ttu-id="b715d-113">Benutzer können eine Rücksendung weiterhin gegen eine Seriennummer bearbeiten, die sich von der ursprünglich verkauften Seriennummer unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="b715d-113">Users can continue to process a return against a serial number that differs from the serial number that was originally sold.</span></span>

<span data-ttu-id="b715d-114">Sie konfigurieren die Seriennummernvalidierung für eine Organisation, nachdem die Funktion **Einheitliche Retourenbearbeitungserfahrung in POS** aktiviert wurde, indem Sie zu **Retail and Commerce \> Zentralverwaltungseinrichtung \> Parameter \> Handelsparameter** in der Commerce-Zentralverwaltung gehen.</span><span class="sxs-lookup"><span data-stu-id="b715d-114">To configure serial number validation for an organization after the **Unified return processing experience in POS** feature is turned on, go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters** in Commerce headquarters.</span></span> <span data-ttu-id="b715d-115">Auf der Registerkarte **Bestand** auf dem Inforegister **Lagerbestandsvorgänge** stellen Sie die Option **Validierung von Seriennummern bei POS-Rücksendungen aktivieren** auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="b715d-115">On the **Inventory** tab, on the **Store inventory operations** FastTab, set the **Enable validation of serial numbers on POS returns** option to **Yes**.</span></span>

## <a name="process-returns-for-serialized-items-in-pos"></a><span data-ttu-id="b715d-116">Retouren für Artikel mit Seriennummer in POS verarbeiten</span><span class="sxs-lookup"><span data-stu-id="b715d-116">Process returns for serialized items in POS</span></span>

<span data-ttu-id="b715d-117">Wenn die Option **Validierung von Seriennummern bei POS-Rücksendungen aktivieren** auf **Ja** gesetzt wird, kann der Benutzer, wenn ein Artikel mit Seriennummer über POS zurückgegeben wird, die Seriennummer für die Rücksendeposition im Detailbereich auf der Seite **Retournierbare Produkte** eingeben.</span><span class="sxs-lookup"><span data-stu-id="b715d-117">If the **Enable validation of serial numbers on POS returns** option has been set to **Yes**, when a serial number–controlled item is returned through POS, the user can enter the serial number for the return line in the details pane on the **Returnable products** page.</span></span> <span data-ttu-id="b715d-118">Wenn die eingegebene Seriennummer nicht mit der Originalseriennummer übereinstimmt, die für den Verkaufsvorgang verkauft wurde, erhält der Benutzer eine Warnmeldung.</span><span class="sxs-lookup"><span data-stu-id="b715d-118">If the serial number that is entered doesn't match the original serial number that was sold for the sales transaction, the user receives a warning message.</span></span> <span data-ttu-id="b715d-119">Die Anwendung hindert den Benutzer jedoch nicht daran, die Retoure weiterhin zu buchen.</span><span class="sxs-lookup"><span data-stu-id="b715d-119">However, the application doesn't prevent the user from continuing to post the return.</span></span>

> [!NOTE]
> <span data-ttu-id="b715d-120">Derzeit unterstützt POS die Validierung von Seriennummern nur bei Rücksendungen, bei denen die ursprünglich bestellte Menge nicht mehr als eins beträgt.</span><span class="sxs-lookup"><span data-stu-id="b715d-120">Currently, POS supports validation of serial numbers only on return lines where the original ordered quantity is no more than one.</span></span> <span data-ttu-id="b715d-121">Wenn die ursprüngliche Verkaufsauftragsposition in einem Nicht-POS-Kanal erstellt wurde und die Menge, die für den Artikel mit Seriennummer in einer bestimmten Verkaufsposition bestellt wurde, mehr als eins beträgt, kann der Artikel nicht korrekt über POS zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b715d-121">If the original sales order line was created in a non-POS channel, and if the quantity that was ordered for the serialized item on a given sales line is more than one, the item can't be correctly returned through POS.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b715d-122">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b715d-122">Additional resources</span></span>

[<span data-ttu-id="b715d-123">Retouren in POS erstellen</span><span class="sxs-lookup"><span data-stu-id="b715d-123">Create returns in POS</span></span>](POS-returns.md)
