---
title: Fehler bei der Auftragssynchronisierung im Zusammenhang mit dem Standardzahlungsservice
description: Dieses Thema enthält Anleitungen zur Fehlerbehebung, mit deren Hilfe ein Fehler behoben werden kann, der bei der Synchronisierung eines Onlineauftrags auftreten kann.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: fa174bbb257379f6ce906dd21180bbcb19f8bc3f
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021126"
---
# <a name="order-synchronization-error-related-to-the-default-payment-service"></a><span data-ttu-id="eb0ad-103">Fehler bei der Auftragssynchronisierung im Zusammenhang mit dem Standardzahlungsservice</span><span class="sxs-lookup"><span data-stu-id="eb0ad-103">Order synchronization error related to the default payment service</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="eb0ad-104">Dieses Thema enthält Anleitungen zur Fehlerbehebung, mit deren Hilfe ein Fehler behoben werden kann, der bei der Synchronisierung eines Onlineauftrags auftreten kann.</span><span class="sxs-lookup"><span data-stu-id="eb0ad-104">This topic provides troubleshooting guidance that can help fix an error that might occur when an online order is synced.</span></span>

## <a name="description"></a><span data-ttu-id="eb0ad-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eb0ad-105">Description</span></span>

<span data-ttu-id="eb0ad-106">Wenn Sie einen Onlineauftrag synchronisieren, wird die folgende Fehlermeldung angezeigt: „Für die Verarbeitung von Kreditkartentransaktionen muss ein Standardzahlungsservice vorhanden sein.“</span><span class="sxs-lookup"><span data-stu-id="eb0ad-106">When you sync an online order, you receive the following error message: "There must be a default payment service to process credit card transactions."</span></span>

![„Fehlender Standardzahlungsservice“-Fehler](media/default-payment-method-error.jpg)

## <a name="resolution"></a><span data-ttu-id="eb0ad-108">Lösung</span><span class="sxs-lookup"><span data-stu-id="eb0ad-108">Resolution</span></span>

### <a name="confirm-or-set-the-default-payment-service-in-commerce-headquarters"></a><span data-ttu-id="eb0ad-109">Standardzahlungsservice in der Commerce-Zentralverwaltung bestätigen oder festlegen</span><span class="sxs-lookup"><span data-stu-id="eb0ad-109">Confirm or set the default payment service in Commerce headquarters</span></span>

<span data-ttu-id="eb0ad-110">Befolgen Sie diese Schritte, um den Standardzahlungsservice in der Commerce-Zentralverwaltung zu bestätigen oder festzulegen.</span><span class="sxs-lookup"><span data-stu-id="eb0ad-110">To confirm or set the default payment service in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="eb0ad-111">Rufen Sie **Debitorenkonten \> Zahlungseinstellungen \> Zahlungsdienste** auf.</span><span class="sxs-lookup"><span data-stu-id="eb0ad-111">Go to **Accounts receivable \> Payment setup \> Payment services**.</span></span>
1. <span data-ttu-id="eb0ad-112">Vergewissern Sie sich, dass für einen Zahlungsdienst die Option **Standardmäßige Verarbeitungsstelle für neue Kreditkarten** auf **Ja** gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="eb0ad-112">Make sure that the **Default processor for new credit cards** option is set to **Yes** for one payment service.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="eb0ad-113">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="eb0ad-113">Additional resources</span></span>

[<span data-ttu-id="eb0ad-114">Einrichten, Genehmigen und Erfassen von Kreditkarten</span><span class="sxs-lookup"><span data-stu-id="eb0ad-114">Credit card setup, authorization, and capture</span></span>](../../finance/accounts-receivable/credit-card-authorizations.md)