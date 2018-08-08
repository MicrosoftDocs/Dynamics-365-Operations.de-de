---
title: "Persönliche Spesen in einer Spesenabrechnung"
description: "In diesem Thema werden die zwei Methoden zur Handhabung der persönlichen Spesen einer Arbeitskraft in Microsoft Dynamics 365 for Finance and Operations erklärt."
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: a6b6c505e7dc5e6544658b00d9f59e6062353608
ms.contentlocale: de-de
ms.lasthandoff: 08/07/2018

---

# <a name="personal-expenses-on-an-expense-report"></a><span data-ttu-id="b6236-103">Persönliche Spesen in einer Spesenabrechnung</span><span class="sxs-lookup"><span data-stu-id="b6236-103">Personal expenses on an expense report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b6236-104">Im Zuge von Geschäftsreisen kann es vorkommen, dass Arbeitskräfte die Kreditkarte des Unternehmen mit persönlichen Spesen belasten.</span><span class="sxs-lookup"><span data-stu-id="b6236-104">During business travel, workers might sometimes charge personal expenses to their corporate credit cards.</span></span> <span data-ttu-id="b6236-105">Wurde kein Verfahren für persönliche Spesen definiert, tritt möglicherweise bei der Genehmigung der Spesenabrechnung ein Problem auf, nachdem Arbeitskräfte die aufgeschlüsselten Spesenabrechnungen eingereicht haben.</span><span class="sxs-lookup"><span data-stu-id="b6236-105">If you don't define a process for handling personal expenses, the approval process for expense reports might be disrupted when workers submit their itemized expense reports.</span></span> 

<span data-ttu-id="b6236-106">In Microsoft Dynamics 365 for Finance and Operations werden die zwei Methoden zur Handhabung der persönlichen Spesen einer Arbeitskraft erklärt:</span><span class="sxs-lookup"><span data-stu-id="b6236-106">In Microsoft Dynamics 365 for Finance and Operations, there are two methods for handling a worker's personal expenses:</span></span>

- <span data-ttu-id="b6236-107">**Bezahlung durch den Mitarbeiter** – Die Organisation kommt nicht für die persönlichen Spesen in der Abrechnung der Unternehmenskreditkarte auf.</span><span class="sxs-lookup"><span data-stu-id="b6236-107">**Paid by employee** – Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="b6236-108">Stattdessen erstellt die Organisation einen Bericht, der die persönlichen Spesen zusammen mit den Spesen für das Unternehmen enthält, mit denen die Kreditkarte des Unternehmens belastet wurde.</span><span class="sxs-lookup"><span data-stu-id="b6236-108">Instead, it creates a report that shows personal expenses together with the corporate expenses that were charged to the corporate credit card.</span></span>
- <span data-ttu-id="b6236-109">**Bezahlung durch das Unternehmen** – Die Organisation kommt für die gesamte Abrechnung der Unternehmenskreditkarte auf und belastet anschließend das Konto der jeweiligen Arbeitskraft mit den persönlichen Spesen.</span><span class="sxs-lookup"><span data-stu-id="b6236-109">**Paid by company** – Your organization pays the whole bill for the corporate credit card and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="b6236-110">Sie können die Methode auswählen, die Ihre Organisation auf der Seite **Ausgabenverwaltungsparameter** verwendet.</span><span class="sxs-lookup"><span data-stu-id="b6236-110">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>

