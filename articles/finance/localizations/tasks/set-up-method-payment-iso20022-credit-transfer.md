---
title: Zahlungsmethode für ISO20022-Kreditübertragung einrichten
description: Dieses Verfahren zeigt, wie ISO20022 für die Kreditorenzahlungsmethode Banküberweisung oder einen anderen Zahlungstyp über eine elektronischen Berichterstellung zur Generierung einer Datei verwendet wird.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPaymMode
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8bb54864c8d0a57510b4d47b00aed60c5be95512
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174879"
---
# <a name="set-up-method-of-payment-for-iso20022-credit-transfer"></a><span data-ttu-id="1bb71-103">Zahlungsmethode für ISO20022-Kreditübertragung einrichten</span><span class="sxs-lookup"><span data-stu-id="1bb71-103">Set up method of payment for ISO20022 credit transfer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1bb71-104">Dieses Verfahren zeigt, wie ISO20022 für die Kreditorenzahlungsmethode Banküberweisung oder einen anderen Zahlungstyp über eine elektronischen Berichterstellung zur Generierung einer Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1bb71-104">This procedure shows how to set up the vendor method of payment for ISO20022 credit transfer or any other payment type using electronic reporting to generate a file.</span></span> 

<span data-ttu-id="1bb71-105">Bevor Sie diese Aufgabe abschließen, müssen Sie Exportformatkonfigurations- und Zahlungskonteneinstellung eingerichtet haben.</span><span class="sxs-lookup"><span data-stu-id="1bb71-105">Before you complete this task, you must export format configurations and set up payment accounts.</span></span>

<span data-ttu-id="1bb71-106">Diese Aufgabe wurde mit dem Demodatenunternehmen DEMF erstellt.</span><span class="sxs-lookup"><span data-stu-id="1bb71-106">This task was created using the DEMF demo data company.</span></span>

<span data-ttu-id="1bb71-107">Dies ist der dritte von fünf Aufgaben, die das Verfahren für Kreditorenzahlung über elektronischen Berichterstellungskonfigurationen zeigen.</span><span class="sxs-lookup"><span data-stu-id="1bb71-107">This is the third procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="1bb71-108">Diese Prozedur ist eine Funktion, für die in Dynamics 365 for Operations Version 1611 hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="1bb71-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="1bb71-109">Wechseln Sie zu "Kreditoren" > "Zahlungseinstellungen" > "Zahlungsmethoden".</span><span class="sxs-lookup"><span data-stu-id="1bb71-109">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
2. <span data-ttu-id="1bb71-110">Verwenden Sie den Schnellfilter, um Datensätze zu suchen.</span><span class="sxs-lookup"><span data-stu-id="1bb71-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="1bb71-111">Filtern Sie beispielsweise im Feld "Zahlungsmethoden" mit dem Wert "SEPA CT".</span><span class="sxs-lookup"><span data-stu-id="1bb71-111">For example, filter on the Method of payment field with a value of 'SEPA CT'.</span></span>
3. <span data-ttu-id="1bb71-112">Klicken Sie auf Bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="1bb71-112">Click Edit.</span></span>
4. <span data-ttu-id="1bb71-113">Wählen Sie im Feld "Zeitraum" die Option "Summe".</span><span class="sxs-lookup"><span data-stu-id="1bb71-113">In the Period field, select 'Total'.</span></span>
5. <span data-ttu-id="1bb71-114">Wählen Sie im Feld "Zahlungstyp" "Elektronischer Zahlungsverkehr" aus.</span><span class="sxs-lookup"><span data-stu-id="1bb71-114">In the Payment type field, select 'Electronic payment'.</span></span>
6. <span data-ttu-id="1bb71-115">Erweitern Sie den Abschnitt 'Dateiformate'.</span><span class="sxs-lookup"><span data-stu-id="1bb71-115">Expand the File formats section.</span></span>
7. <span data-ttu-id="1bb71-116">Wählen Sie „Ja“ im Feld "Generische elektronische Berichterstellung" aus.</span><span class="sxs-lookup"><span data-stu-id="1bb71-116">Select Yes in the Generic electronic reporting field.</span></span>
8. <span data-ttu-id="1bb71-117">Wählen Sie im Feld "Formatkonfiguration exportieren" einen Wert aus oder geben Sie ihn ein.</span><span class="sxs-lookup"><span data-stu-id="1bb71-117">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="1bb71-118">Wählen Sie in der Liste den Wert ISO20022 Banküberweisung (DE) aus.</span><span class="sxs-lookup"><span data-stu-id="1bb71-118">In the list, select the value ISO20022 Credit transfer (DE).</span></span> <span data-ttu-id="1bb71-119">Wenn die Liste leer ist, bedeutet dies, dass es keine importierte und aktive Kreditorenzahlungs-Exportformatkonfiguration gibt.</span><span class="sxs-lookup"><span data-stu-id="1bb71-119">If the list is empty, the vendor payment export format configuration is not imported and active.</span></span>  
9. <span data-ttu-id="1bb71-120">Wählen Sie im Feld "Kontotyp" "Bank" aus.</span><span class="sxs-lookup"><span data-stu-id="1bb71-120">In the Account type field, select 'Bank'.</span></span>
10. <span data-ttu-id="1bb71-121">Geben Sie im Feld "Zahlungskonto" die Werte "DEMF OPER" an.</span><span class="sxs-lookup"><span data-stu-id="1bb71-121">In the Payment account field, specify the values 'DEMF OPER'.</span></span>
11. <span data-ttu-id="1bb71-122">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="1bb71-122">Click Save.</span></span>

