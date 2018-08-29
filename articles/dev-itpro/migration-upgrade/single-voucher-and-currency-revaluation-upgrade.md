---
title: "Einzelbelegerfassungen und Währungsneubewertungen aktualisieren"
description: "Einige Organisationen erfassen Journale, die einen einzelnen Beleg enthalten, dem mehr als ein Debitor oder Kreditor zugeordnet ist und führen den Prozess der Neubewertung der Fremdwährung für Kreditoren und Debitoren aus. In diesem Abschnitt werden die Schritte beschrieben, denen diese Organisationen folgen sollten, wenn diese ein Upgrade auf Microsoft Dynamics 365 for Operations Version 1611 durchführen."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 343fa226e1cf9072696082e9ebf0a1629e553ae9
ms.contentlocale: de-de
ms.lasthandoff: 08/08/2018

---

# <a name="upgrade-single-voucher-journals-and-currency-revaluations"></a><span data-ttu-id="eb2a1-104">Einzelbelegerfassungen und Währungsneubewertungen aktualisieren</span><span class="sxs-lookup"><span data-stu-id="eb2a1-104">Upgrade single-voucher journals and currency revaluations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eb2a1-105">Einige Organisationen erfassen Journale, die einen einzelnen Beleg enthalten, dem mehr als ein Debitor oder Kreditor zugeordnet ist und führen den Prozess der Neubewertung der Fremdwährung für Kreditoren und Debitoren aus.</span><span class="sxs-lookup"><span data-stu-id="eb2a1-105">Some organizations enter journals that contain a single voucher that has more than one customer or vendor, and they also run the Accounts receivable or Accounts payable foreign currency revaluation process.</span></span> <span data-ttu-id="eb2a1-106">In diesem Abschnitt werden die Schritte beschrieben, denen diese Organisationen folgen sollten, wenn diese ein Upgrade auf Microsoft Dynamics 365 for Operations Version 1611 durchführen.</span><span class="sxs-lookup"><span data-stu-id="eb2a1-106">This topic describes the steps that these organizations should follow when they upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

<span data-ttu-id="eb2a1-107">Gehen Sie folgendermaßen vor, wenn Sie ein Upgrade auf Microsoft Dynamics 365 for Operations Version 1611 durchführen.</span><span class="sxs-lookup"><span data-stu-id="eb2a1-107">Follow these steps when you upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

1.  <span data-ttu-id="eb2a1-108">Bevor Sie ein Upgrade auf Dynamics 365 for Operations durchführen, müssen Sie die Prozesse der Neubewertung der Fremdwährung für Kreditoren- und Debitorenkonten durchführen.</span><span class="sxs-lookup"><span data-stu-id="eb2a1-108">Before you upgrade to Dynamics 365 for Operations, run the foreign currency revaluation processes for Accounts receivable and Accounts payable.</span></span> <span data-ttu-id="eb2a1-109">Legen Sie das Feld **Methode** auf das **Rechnungsdatum** fest.</span><span class="sxs-lookup"><span data-stu-id="eb2a1-109">Set the **Method** field to **Invoice date**.</span></span> <span data-ttu-id="eb2a1-110">Eine Neubewertungsbuchung wird erstellt, die die letzte Neubewertung der Fremdwährung rückgängig macht.</span><span class="sxs-lookup"><span data-stu-id="eb2a1-110">A revaluation transaction is created that reverses the last foreign currency revaluation.</span></span> <span data-ttu-id="eb2a1-111">Daher werden die offenen Buchungen nach ihrer ursprünglichen Buchhaltungswährung bewertet.</span><span class="sxs-lookup"><span data-stu-id="eb2a1-111">Therefore, the open transactions are valued at their original accounting currency.</span></span>
2.  <span data-ttu-id="eb2a1-112">Führen Sie ein Upgrade auf Dynamics 365 for Operations Version 1611 durch.</span><span class="sxs-lookup"><span data-stu-id="eb2a1-112">Upgrade to Dynamics 365 for Operations version 1611.</span></span>
3.  <span data-ttu-id="eb2a1-113">Führen Sie den Prozess der Neubewertung der Fremdwährung für die Debitoren- und Kreditorenkonten erneut durch.</span><span class="sxs-lookup"><span data-stu-id="eb2a1-113">Run the Accounts receivable and Accounts payable foreign currency revaluation processes again.</span></span> <span data-ttu-id="eb2a1-114">Setzen Sie diesmal das Feld **Methode** auf **Standard**.</span><span class="sxs-lookup"><span data-stu-id="eb2a1-114">This time, set the **Method** field to **Standard**.</span></span> <span data-ttu-id="eb2a1-115">Es wird eine neue Neubewertungsbuchung erstellt, die auf dem aktuellen Wechselkurs basiert.</span><span class="sxs-lookup"><span data-stu-id="eb2a1-115">A new revaluation transaction is created that is based on the current exchange rates.</span></span> <span data-ttu-id="eb2a1-116">Dies Buchung erfasst die unrealisierten Gewinne/Verluste und das korrekte Zusammenfassungssachkonto.</span><span class="sxs-lookup"><span data-stu-id="eb2a1-116">This transaction records the unrealized gain/loss and the correct summary ledger account.</span></span>





