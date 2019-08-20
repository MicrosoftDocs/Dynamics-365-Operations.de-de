---
title: Persönliche Spesen in einer Spesenabrechnung
description: In diesem Thema werden die zwei Methoden zur Handhabung der persönlichen Spesen einer Arbeitskraft in Microsoft Dynamics 365 for Finance and Operations erläutert.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b072fa9e78563d3e89b4d60e9ce61473902fee76
ms.sourcegitcommit: ef08bf1258aefb525d56bf85ef19311be26ab94c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/30/2019
ms.locfileid: "1794987"
---
# <a name="personal-expenses-on-an-expense-report"></a><span data-ttu-id="2c3e0-103">Persönliche Spesen in einer Spesenabrechnung</span><span class="sxs-lookup"><span data-stu-id="2c3e0-103">Personal expenses on an expense report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2c3e0-104">Im Zuge von Geschäftsreisen kann es vorkommen, dass Arbeitskräfte die Kreditkarte des Unternehmen mit persönlichen Spesen belasten.</span><span class="sxs-lookup"><span data-stu-id="2c3e0-104">During business travel, workers might sometimes charge personal expenses to their corporate credit cards.</span></span> <span data-ttu-id="2c3e0-105">Wurde kein Verfahren für persönliche Spesen definiert, tritt möglicherweise bei der Genehmigung der Spesenabrechnung ein Problem auf, nachdem Arbeitskräfte die aufgeschlüsselten Spesenabrechnungen eingereicht haben.</span><span class="sxs-lookup"><span data-stu-id="2c3e0-105">If you don't define a process for handling personal expenses, the approval process for expense reports might be disrupted when workers submit their itemized expense reports.</span></span> 

<span data-ttu-id="2c3e0-106">In Microsoft Dynamics 365 for Finance and Operations stehen für den Umgang mit den persönlichen Spesen einer Arbeitskraft zwei Methoden zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="2c3e0-106">In Microsoft Dynamics 365 for Finance and Operations, there are two methods for handling a worker's personal expenses:</span></span>

- <span data-ttu-id="2c3e0-107">**Bezahlung durch den Mitarbeiter** – Die Organisation kommt nicht für die persönlichen Spesen in der Abrechnung der Unternehmenskreditkarte auf.</span><span class="sxs-lookup"><span data-stu-id="2c3e0-107">**Paid by employee** – Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="2c3e0-108">Stattdessen erstellt die Organisation einen Bericht, der die persönlichen Spesen zusammen mit den Spesen für das Unternehmen enthält, mit denen die Kreditkarte des Unternehmens belastet wurde.</span><span class="sxs-lookup"><span data-stu-id="2c3e0-108">Instead, it creates a report that shows personal expenses together with the corporate expenses that were charged to the corporate credit card.</span></span>
- <span data-ttu-id="2c3e0-109">**Bezahlung durch das Unternehmen** – Die Organisation kommt für die gesamte Abrechnung der Unternehmenskreditkarte auf und belastet anschließend das Konto der jeweiligen Arbeitskraft mit den persönlichen Spesen.</span><span class="sxs-lookup"><span data-stu-id="2c3e0-109">**Paid by company** – Your organization pays the whole bill for the corporate credit card and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="2c3e0-110">Sie können die Methode auswählen, die Ihre Organisation auf der Seite **Ausgabenverwaltungsparameter** verwendet.</span><span class="sxs-lookup"><span data-stu-id="2c3e0-110">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>
