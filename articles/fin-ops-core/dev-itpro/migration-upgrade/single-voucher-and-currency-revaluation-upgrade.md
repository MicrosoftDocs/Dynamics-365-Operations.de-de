---
title: Aktualisieren von Einzelbelegerfassungen und Währungsneubewertungen
description: In diesem Thema wird beschrieben, wie Einzelbelegerfassungen und Währungsneubewertungen aktualisiert werden.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 3504c01a4ed1571866fd2a0cd83eef86a57d684a
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2021
ms.locfileid: "5127302"
---
# <a name="upgrade-single-voucher-journals-and-currency-revaluations"></a><span data-ttu-id="d8935-103">Aktualisieren von Einzelbelegerfassungen und Währungsneubewertungen</span><span class="sxs-lookup"><span data-stu-id="d8935-103">Upgrade single-voucher journals and currency revaluations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d8935-104">Einige Organisationen erfassen Journale, die einen einzelnen Beleg enthalten, dem mehr als ein Debitor oder Kreditor zugeordnet ist und führen den Prozess der Neubewertung der Fremdwährung für Kreditoren und Debitoren aus.</span><span class="sxs-lookup"><span data-stu-id="d8935-104">Some organizations enter journals that contain a single voucher that has more than one customer or vendor, and they also run the Accounts receivable or Accounts payable foreign currency revaluation process.</span></span> <span data-ttu-id="d8935-105">In diesem Abschnitt werden die Schritte beschrieben, denen diese Organisationen folgen sollten, wenn diese ein Upgrade auf Microsoft Dynamics 365 for Operations Version 1611 durchführen.</span><span class="sxs-lookup"><span data-stu-id="d8935-105">This topic describes the steps that these organizations should follow when they upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

<span data-ttu-id="d8935-106">Gehen Sie folgendermaßen vor, wenn Sie Microsoft Dynamics 365 for Operations-Version 1611 aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="d8935-106">Follow these steps when you upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

1.  <span data-ttu-id="d8935-107">Bevor Sie ein Upgrade auf Finance and Operations durchführen, müssen Sie die Prozesse der Neubewertung der Fremdwährung für Kreditoren- und Debitorenkonten durchführen.</span><span class="sxs-lookup"><span data-stu-id="d8935-107">Before you upgrade to Finance and Operations, run the foreign currency revaluation processes for Accounts receivable and Accounts payable.</span></span> <span data-ttu-id="d8935-108">Legen Sie das Feld **Methode** auf das **Rechnungsdatum** fest.</span><span class="sxs-lookup"><span data-stu-id="d8935-108">Set the **Method** field to **Invoice date**.</span></span> <span data-ttu-id="d8935-109">Eine Neubewertungsbuchung wird erstellt, die die letzte Neubewertung der Fremdwährung rückgängig macht.</span><span class="sxs-lookup"><span data-stu-id="d8935-109">A revaluation transaction is created that reverses the last foreign currency revaluation.</span></span> <span data-ttu-id="d8935-110">Daher werden die offenen Buchungen nach ihrer ursprünglichen Buchhaltungswährung bewertet.</span><span class="sxs-lookup"><span data-stu-id="d8935-110">Therefore, the open transactions are valued at their original accounting currency.</span></span>
2.  <span data-ttu-id="d8935-111">Upgrade auf Version 1611</span><span class="sxs-lookup"><span data-stu-id="d8935-111">Upgrade to version 1611.</span></span>
3.  <span data-ttu-id="d8935-112">Führen Sie den Prozess der Neubewertung der Fremdwährung für die Debitoren- und Kreditorenkonten erneut durch.</span><span class="sxs-lookup"><span data-stu-id="d8935-112">Run the Accounts receivable and Accounts payable foreign currency revaluation processes again.</span></span> <span data-ttu-id="d8935-113">Setzen Sie diesmal das Feld **Methode** auf **Standard**.</span><span class="sxs-lookup"><span data-stu-id="d8935-113">This time, set the **Method** field to **Standard**.</span></span> <span data-ttu-id="d8935-114">Es wird eine neue Neubewertungsbuchung erstellt, die auf dem aktuellen Wechselkurs basiert.</span><span class="sxs-lookup"><span data-stu-id="d8935-114">A new revaluation transaction is created that is based on the current exchange rates.</span></span> <span data-ttu-id="d8935-115">Dies Buchung erfasst die unrealisierten Gewinne/Verluste und das korrekte Zusammenfassungssachkonto.</span><span class="sxs-lookup"><span data-stu-id="d8935-115">This transaction records the unrealized gain/loss and the correct summary ledger account.</span></span>
