---
title: Fehler bei der Auftragssynchronisierung im Zusammenhang mit dem Standardzahlungsservice
description: Dieses Thema enthält Anleitungen zur Fehlerbehebung, mit deren Hilfe ein Fehler behoben werden kann, der bei der Synchronisierung eines Onlineauftrags auftreten kann.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: 45eeae751051b58e1c9e725eb4ed4b5240026e7f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801434"
---
# <a name="order-synchronization-error-related-to-the-default-payment-service"></a><span data-ttu-id="4bb25-103">Fehler bei der Auftragssynchronisierung im Zusammenhang mit dem Standardzahlungsservice</span><span class="sxs-lookup"><span data-stu-id="4bb25-103">Order synchronization error related to the default payment service</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4bb25-104">Dieses Thema enthält Anleitungen zur Fehlerbehebung, mit deren Hilfe ein Fehler behoben werden kann, der bei der Synchronisierung eines Onlineauftrags auftreten kann.</span><span class="sxs-lookup"><span data-stu-id="4bb25-104">This topic provides troubleshooting guidance that can help fix an error that might occur when an online order is synced.</span></span>

## <a name="description"></a><span data-ttu-id="4bb25-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4bb25-105">Description</span></span>

<span data-ttu-id="4bb25-106">Wenn Sie einen Onlineauftrag synchronisieren, wird die folgende Fehlermeldung angezeigt: „Für die Verarbeitung von Kreditkartentransaktionen muss ein Standardzahlungsservice vorhanden sein.“</span><span class="sxs-lookup"><span data-stu-id="4bb25-106">When you sync an online order, you receive the following error message: "There must be a default payment service to process credit card transactions."</span></span>

![„Fehlender Standardzahlungsservice“-Fehler](media/default-payment-method-error.jpg)

## <a name="resolution"></a><span data-ttu-id="4bb25-108">Lösung</span><span class="sxs-lookup"><span data-stu-id="4bb25-108">Resolution</span></span>

### <a name="confirm-or-set-the-default-payment-service-in-commerce-headquarters"></a><span data-ttu-id="4bb25-109">Standardzahlungsservice in der Commerce-Zentralverwaltung bestätigen oder festlegen</span><span class="sxs-lookup"><span data-stu-id="4bb25-109">Confirm or set the default payment service in Commerce headquarters</span></span>

<span data-ttu-id="4bb25-110">Befolgen Sie diese Schritte, um den Standardzahlungsservice in der Commerce-Zentralverwaltung zu bestätigen oder festzulegen.</span><span class="sxs-lookup"><span data-stu-id="4bb25-110">To confirm or set the default payment service in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="4bb25-111">Rufen Sie **Debitorenkonten \> Zahlungseinstellungen \> Zahlungsdienste** auf.</span><span class="sxs-lookup"><span data-stu-id="4bb25-111">Go to **Accounts receivable \> Payment setup \> Payment services**.</span></span>
1. <span data-ttu-id="4bb25-112">Vergewissern Sie sich, dass für einen Zahlungsdienst die Option **Standardmäßige Verarbeitungsstelle für neue Kreditkarten** auf **Ja** gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="4bb25-112">Make sure that the **Default processor for new credit cards** option is set to **Yes** for one payment service.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4bb25-113">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4bb25-113">Additional resources</span></span>

[<span data-ttu-id="4bb25-114">Einrichten, Genehmigen und Erfassen von Kreditkarten</span><span class="sxs-lookup"><span data-stu-id="4bb25-114">Credit card setup, authorization, and capture</span></span>](https://docs.microsoft.com/dynamics365/finance/accounts-receivable/credit-card-authorizations)
