---
title: Unternehmens-Bankkonten für ISO20022-Überweisungen einrichten
description: Dieses Verfahren zeigt, wie Sie die unternehmensspezifischen Bankkontoinformationen einrichten, die für die Zahlungsdateigenerierung erforderlich sind.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankAccountTable, OMLegalEntity, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5e121ce7d87ee50a4e6b367a170eea4375d64fb3
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144872"
---
# <a name="set-up-company-bank-accounts-for-iso20022-credit-transfers"></a><span data-ttu-id="b0544-103">Unternehmens-Bankkonten für ISO20022-Überweisungen einrichten</span><span class="sxs-lookup"><span data-stu-id="b0544-103">Set up company bank accounts for ISO20022 credit transfers</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b0544-104">Dieses Verfahren zeigt, wie Sie die unternehmensspezifischen Bankkontoinformationen einrichten, die für die Zahlungsdateigenerierung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="b0544-104">This procedure shows how to set up company-specific bank account information that is required for payment file generation.</span></span> <span data-ttu-id="b0544-105">Sie richten die Informationen ein, die erforderlich sind, um das ISO 20022-Banküberweisungsformat zu generieren. Abhängig vom Format werden möglicherweise auch andere Informationen benötigt (z. B. die Unternehmenskennung oder die Bankleitzahl).</span><span class="sxs-lookup"><span data-stu-id="b0544-105">You set up information required to generate ISO 20022 credit transfer format but depending on the format there might be other information required, such as the Company ID or the Sort code.</span></span> 

<span data-ttu-id="b0544-106">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist DEMF.</span><span class="sxs-lookup"><span data-stu-id="b0544-106">The demo data company used to create this procedure is DEMF.</span></span>

<span data-ttu-id="b0544-107">Dies ist der zweite von fünf Aufgaben, die das Verfahren für Kreditorenzahlung über elektronischen Berichterstellungskonfigurationen zeigen.</span><span class="sxs-lookup"><span data-stu-id="b0544-107">This is the second procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="b0544-108">Diese Prozedur ist eine Funktion, für die in Dynamics 365 for Operations Version 1611 hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="b0544-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="set-up-iban-and-swift-code"></a><span data-ttu-id="b0544-109">Einrichten von IBAN- und SWIFT-Code</span><span class="sxs-lookup"><span data-stu-id="b0544-109">Set up IBAN and SWIFT code</span></span>
1. <span data-ttu-id="b0544-110">Wechseln Sie zu "Bargeld- und Bankverwaltung" > "Bankkonten".</span><span class="sxs-lookup"><span data-stu-id="b0544-110">Go to Cash and bank management > Bank accounts.</span></span>
2. <span data-ttu-id="b0544-111">Verwenden Sie den Schnellfilter, um im Feld "Bankkonto" nach dem Wert "DEMF OPER" zu filtern.</span><span class="sxs-lookup"><span data-stu-id="b0544-111">Use the Quick Filter to filter on the Bank account field with a value of 'DEMF OPER'.</span></span>
3. <span data-ttu-id="b0544-112">Klicken Sie auf DEMF OPER, um die Bankkontodetails zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b0544-112">Click DEMF OPER to open bank account details.</span></span>
4. <span data-ttu-id="b0544-113">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="b0544-113">Click Edit.</span></span>
5. <span data-ttu-id="b0544-114">Erweitern Sie den Abschnitt "Zusätzliche Kennung".</span><span class="sxs-lookup"><span data-stu-id="b0544-114">Expand the Additional identification section.</span></span>
6. <span data-ttu-id="b0544-115">Geben Sie im Feld "IBAN" den Wert "DE89370400440532013000" ein.</span><span class="sxs-lookup"><span data-stu-id="b0544-115">In the IBAN field, type 'DE89370400440532013000'.</span></span>
7. <span data-ttu-id="b0544-116">Geben Sie im Feld "SWIFT-Code" "DEUTDEFF" ein.</span><span class="sxs-lookup"><span data-stu-id="b0544-116">In the SWIFT code field, type 'DEUTDEFF'.</span></span>
    * <span data-ttu-id="b0544-117">Beachten Sie, dass die SWIFT\BIC nicht für mehrere Zahlungsformate erforderlich ist, jedoch empfohlen wird, um sie für ein Bankkonto zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="b0544-117">Note that SWIFT\BIC is not required for many payment formats, however it is recommended to have it registered for a bank account.</span></span>  
8. <span data-ttu-id="b0544-118">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="b0544-118">Click Save.</span></span>

## <a name="set-up-bank-account-for-the-legal-entity"></a><span data-ttu-id="b0544-119">Bankkonto für die juristische Person einrichten</span><span class="sxs-lookup"><span data-stu-id="b0544-119">Set up bank account for the legal entity</span></span>
1. <span data-ttu-id="b0544-120">Wechseln Sie zu Organisationsverwaltung > Organisationen > Juristische Personen.</span><span class="sxs-lookup"><span data-stu-id="b0544-120">Go to Organization administration > Organizations > Legal entities.</span></span>
2. <span data-ttu-id="b0544-121">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="b0544-121">Click Edit.</span></span>
3. <span data-ttu-id="b0544-122">Erweitern Sie den Abschnitt "Bankkontoinformationen".</span><span class="sxs-lookup"><span data-stu-id="b0544-122">Expand the Bank account information section.</span></span>
4. <span data-ttu-id="b0544-123">Geben Sie im Feld 'Bankkonto' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="b0544-123">In the Bank account field, enter or select a value.</span></span>
5. <span data-ttu-id="b0544-124">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="b0544-124">Click Save.</span></span>

