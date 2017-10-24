---
title: Betrugswarnungen einrichten
description: "In diesem Thema wird erläutert, wie Regeln eingerichtet werden, um Kundendienstmitarbeiter vor möglicherweise gefälschten Informationen zu warnen, wenn Aufträge verarbeitet werden. Sie können auch spezielle Codes definieren, die verwendet werden, um automatisch oder manuell verdächtige Aufträge zu sperren."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 79103
ms.assetid: e342af8d-7498-4d20-8483-ab368429c578
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 09d80015298c3d0219b6ffb290dc456990536a62
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-fraud-alerts"></a><span data-ttu-id="3734f-104">Betrugswarnungen einrichten</span><span class="sxs-lookup"><span data-stu-id="3734f-104">Set up fraud alerts</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="3734f-105">In diesem Thema wird erläutert, wie Regeln eingerichtet werden, um Kundendienstmitarbeiter vor möglicherweise gefälschten Informationen zu warnen, wenn Aufträge verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="3734f-105">This topic explains how to set up rules to alert customer service representatives of potentially fraudulent information when orders are processed.</span></span> <span data-ttu-id="3734f-106">Sie können auch spezielle Codes definieren, die verwendet werden, um automatisch oder manuell verdächtige Aufträge zu sperren.</span><span class="sxs-lookup"><span data-stu-id="3734f-106">You can define specific codes to use to automatically or manually put suspicious orders on hold.</span></span> 

<span data-ttu-id="3734f-107">Bevor Sie Betrugsüberprüfungsregeln einrichten und verwenden, müssen Sie die Betrugsprüfung aktivieren und die grundlegenden Betrugsprüfungswerte in den Callcenterparametern definieren.</span><span class="sxs-lookup"><span data-stu-id="3734f-107">Before you set up and use fraud checking rules, you must enable fraud checking and define the basic fraud checking values in the call center parameters.</span></span> <span data-ttu-id="3734f-108">Es gibt zwei Arten von Betrugsregeln:</span><span class="sxs-lookup"><span data-stu-id="3734f-108">There are two types of fraud rules:</span></span>

-   <span data-ttu-id="3734f-109">**Statische Regeln** verwenden Sie einen bestimmten Wert, wie Telefonnummer, die auf die schwarze Liste gesetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="3734f-109">**Static rules** use a specific value, such as a phone number that has been blacklisted.</span></span>
-   <span data-ttu-id="3734f-110">**Dynamische Regeln** können aus Variablen und der Bedingungen bestehen.</span><span class="sxs-lookup"><span data-stu-id="3734f-110">**Dynamic rules** can be composed from variables and conditions.</span></span>

<span data-ttu-id="3734f-111">Bevor Sie eine dynamische Regel erstellen, müssen Sie die Variablen und Bedingungen erstellen, die definieren, für wen die Regel gilt und wann die Regel angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3734f-111">Before you create a dynamic rule, you must create the variables and conditions that define who the rule applies to and when the rule should be applied.</span></span> <span data-ttu-id="3734f-112">Sie möchten beispielsweise eine Regel erstellen, um festzulegen, dass ein Auftrag gesperrt werden muss, wenn Debitor 1202 eine Bestellung im Wert von 1.000,00 oder mehr platziert, bis die Debitorenzahlung geprüft werden kann.</span><span class="sxs-lookup"><span data-stu-id="3734f-112">For example, you want to create a rule to require that any sales order that customer 1202 places that is worth 1,000.00 or more be put on hold until the customer payment can be verified.</span></span> <span data-ttu-id="3734f-113">In diesem Beispiel sind die Variablen Debitor 1202 und die Gesamtsumme der Bestellung von 1.000,00.</span><span class="sxs-lookup"><span data-stu-id="3734f-113">In this case, the variables are customer 1202 and an order total of 1,000.00.</span></span> <span data-ttu-id="3734f-114">Die Bedingung gibt an, dass, wenn Debitor 1202 einen Auftrag platziert und der Gesamtbetrag des Auftrags gleich oder höher als 1,000.00 ist, der Auftrag gesperrt werden muss, bis die Debitorenzahlung überprüft werden kann.</span><span class="sxs-lookup"><span data-stu-id="3734f-114">The condition specifies that if customer 1202 places an order, and the total amount of the order is equal to or more than 1,000.00, the sales order must be put on hold until the customer payment can be verified.</span></span>




