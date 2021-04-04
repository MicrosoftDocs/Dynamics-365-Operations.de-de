---
title: Periodische Aufgaben des Kundenkreditmanagements
description: In diesem Thema werden die regelmäßigen Aufgaben beschrieben, die für die Verwaltung der Kreditlimits für Debitoren erforderlich sind.
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: a034d563c12c4ba8b99e13b30ea2683555a01276
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254486"
---
# <a name="periodic-credit-management-tasks"></a><span data-ttu-id="27c42-103">Periodische Kreditverwaltungsaufgaben</span><span class="sxs-lookup"><span data-stu-id="27c42-103">Periodic credit management tasks</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="27c42-104">In diesem Thema werden die regelmäßigen Aufgaben beschrieben, die für die Verwaltung der Kreditlimits für Debitoren erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="27c42-104">This topic describes the periodic tasks that are a necessary part of the process of managing credit limits for customers.</span></span>

## <a name="update-risk-scores"></a><span data-ttu-id="27c42-105">Risikobewertungen aktualisieren</span><span class="sxs-lookup"><span data-stu-id="27c42-105">Update risk scores</span></span>

<span data-ttu-id="27c42-106">Wenn sich Unternehmen entwickeln und sich die Umstände ändern, können sich auch die Kreditrisiken für einen bestimmten Debitor ändern.</span><span class="sxs-lookup"><span data-stu-id="27c42-106">As businesses evolve and circumstances change, the credit risks for a given customer can also change.</span></span> <span data-ttu-id="27c42-107">Um ein angemessenes Kreditlimit für Ihre Debitoren aufrechtzuerhalten, müssen Sie die Kriterien für jede Risikobewertung regelmäßig überprüfen und die Bewertungen für jeden Debitor aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="27c42-107">To help maintain appropriate credit limits for your customers, you must periodically review the criteria for each risk score and update the scores for each customer.</span></span> <span data-ttu-id="27c42-108">Sie können die folgenden Ergebnisse über die Seite **Risikobewertungen aktualisieren** (**Kredit und Inkasso \>Periodische Aufgaben \>Kreditmanagement \> Risikobewertungen aktualisieren**) aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="27c42-108">You can update the following scores by using the **Update risk scores** page (**Credit and collections \> Periodic tasks \> Credit management \> Update risk scores**).</span></span> <span data-ttu-id="27c42-109">Alle benutzerdefinierten Berechnungen werden ebenfalls verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="27c42-109">All user-defined calculations are also processed.</span></span>

- <span data-ttu-id="27c42-110">**Durchschnittliche Zahlungstage** – Dies ist die durchschnittliche Anzahl von Tagen, die ein Debitor benötigt, um Rechnungen zu bezahlen.</span><span class="sxs-lookup"><span data-stu-id="27c42-110">**Average payment days** – This score is the average number of days that a customer takes to pay invoices.</span></span>
- <span data-ttu-id="27c42-111">**Debitor seit** – Dieser Wert gibt die Anzahl der Jahre an, in denen ein Debitor Debitor Ihrer Organisation war.</span><span class="sxs-lookup"><span data-stu-id="27c42-111">**Customer since** – This score is the number of years that a customer has been a customer of your organization.</span></span>
- <span data-ttu-id="27c42-112">**Im Geschäft seit** – Dies ist die Anzahl der Jahre, die ein Debitor im Geschäft war.</span><span class="sxs-lookup"><span data-stu-id="27c42-112">**In business since** – This score is the number of years that a customer has been in business.</span></span> <span data-ttu-id="27c42-113">Es verwendet den Wert des Felds **Geschäftsbeginn** auf der Seite **Debitoren**.</span><span class="sxs-lookup"><span data-stu-id="27c42-113">It uses the value of the **Business start** field on the **Customers** page.</span></span>
- <span data-ttu-id="27c42-114">**Dauer der ausstehenden Verkäufe in Tagen** – Diese Bewertung basiert auf dem Debitorenkontensaldo, den Umsatzerlösen und der Anzahl der Tage in den letzten 12 Monaten.</span><span class="sxs-lookup"><span data-stu-id="27c42-114">**Days sales outstanding** – This score is based on the accounts receivable balance, sales revenue, and number of days for the previous 12-month period.</span></span>
- <span data-ttu-id="27c42-115">**Durchschnittlicher Saldo** – Diese Bewertung basiert auf dem Debitorenkontensaldo der letzten 12 Monate.</span><span class="sxs-lookup"><span data-stu-id="27c42-115">**Average balance** – This score is based on the accounts receivable balance for the previous 12-month period.</span></span>
- <span data-ttu-id="27c42-116">**Kreditmanagement-Gruppe**, **Kontostatus** und **Land** – Diese Bewertungen verwenden Informationen des Debitors.</span><span class="sxs-lookup"><span data-stu-id="27c42-116">**Credit management group**, **Account status**, and **Country** – These scores use information from the customer.</span></span>

## <a name="update-customer-balance-statistics"></a><span data-ttu-id="27c42-117">Debitorenbilanzstatistik aktualisieren</span><span class="sxs-lookup"><span data-stu-id="27c42-117">Update customer balance statistics</span></span>

<span data-ttu-id="27c42-118">Sie können den Prozess **Debitorenbilanzstatistik** ausführen, um die Berechnung der Bilanzstatistik zu aktualisieren, die auf der Seite **Bilanzstatistik-Abfrage** angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="27c42-118">You can run the **Update customer balance statistics** process to update the calculation of balance statistics that is shown on the **Balance statistics inquiry** page.</span></span> <span data-ttu-id="27c42-119">Diese Informationen werden verwendet, um die Risikobewertung und die Werte zu berechnen, die in den Infoboxen auf der Seite **Kunde** angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="27c42-119">This information is used to calculate risk scores and the values that are shown in the credit statistics FactBoxes on the **Customer** page.</span></span>

<span data-ttu-id="27c42-120">Wenn Sie den Prozess ausführen, werden die Debitorenbilanzstatistiken für einen einzelnen Debitor aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="27c42-120">When you run the process, it updates customer balance statistics for a single customer.</span></span> <span data-ttu-id="27c42-121">Um einen Batchauftrag für die Ausführung des Prozesses für mehrere Debitoren einzurichten, können Sie die Seite **Bilanzstatistik berechnen** (**Kreditmanagement \> Periodische Aufgaben \>Bilanzstatistik berechnen**) verwenden.</span><span class="sxs-lookup"><span data-stu-id="27c42-121">To set up a batch job to run the process for multiple customers, you can use the **Calculate balance statistics** page (**Credit management \> Periodic tasks \> Calculate balance statistics**).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]