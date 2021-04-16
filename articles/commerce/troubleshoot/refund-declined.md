---
title: Die Rückerstattung einer Rücklieferung wird abgelehnt
description: Dieses Thema enthält Anleitungen zur Fehlerbehebung, die hilfreich sein können, wenn eine Rückerstattung für eine Rücklieferung abgelehnt wird, da sich die für die Fakturierung verwendete Kreditkarte von der Karte unterscheidet, die während der ursprünglichen Zahlungsautorisierung verwendet wurde.
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
ms.openlocfilehash: 5961e77de1de5dc23454fc1a6e16f8c0b4e7cc6a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801554"
---
# <a name="refund-on-a-return-order-is-declined"></a><span data-ttu-id="e7ed7-103">Die Rückerstattung einer Rücklieferung wird abgelehnt</span><span class="sxs-lookup"><span data-stu-id="e7ed7-103">Refund on a return order is declined</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e7ed7-104">Dieses Thema enthält Anleitungen zur Fehlerbehebung, die hilfreich sein können, wenn eine Rückerstattung für eine Rücklieferung abgelehnt wird, da sich die für die Fakturierung verwendete Kreditkarte von der Karte unterscheidet, die während der ursprünglichen Zahlungsautorisierung verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="e7ed7-104">This topic provides troubleshooting guidance that can help when a refund on a return order is declined because the credit card that is used for invoicing differs from the card that was used during the original payment authorization.</span></span>

## <a name="description"></a><span data-ttu-id="e7ed7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e7ed7-105">Description</span></span>

<span data-ttu-id="e7ed7-106">Eine Rückerstattung wird abgelehnt, wenn die Kreditkarte, mit der eine Rücklieferung fakturiert wird, von der Karte abweicht, die während der ursprünglichen Zahlungsautorisierung verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="e7ed7-106">A refund is declined when the credit card that is used to invoice a return order differs from the card that was used during the original payment authorization.</span></span> <span data-ttu-id="e7ed7-107">Sie erhalten die folgende Fehlermeldung: „Einige Zahlungen haben nicht den richtigen Status für die Buchung.</span><span class="sxs-lookup"><span data-stu-id="e7ed7-107">You receive the following error message: "Some payments are not in the correct status for posting.</span></span> <span data-ttu-id="e7ed7-108">Bitte überprüfen Sie den Status aller Zahlungen vor der Fakturierung erneut.“</span><span class="sxs-lookup"><span data-stu-id="e7ed7-108">Please re-validate the status of all payments prior to invoicing."</span></span>

<span data-ttu-id="e7ed7-109">Die Details der Zahlungsautorisierung enthalten folgende Fehlermeldung: „Adyen-Gateway SendRequest() ist mit dem Status 'InternalServerError'.22144 fehlgeschlagen; leere Antwort von Adyen zurückgegeben.(22001);“</span><span class="sxs-lookup"><span data-stu-id="e7ed7-109">The payment authorization details will include the following error message: "Adyen gateway SendRequest() failed with status 'InternalServerError'.22144; Empty response returned from Adyen.(22001);"</span></span>

![Abgelehnte Rückerstattung einer Rücklieferung – Fehler](media/refund-order-decline.jpg)

## <a name="resolution"></a><span data-ttu-id="e7ed7-111">Lösung</span><span class="sxs-lookup"><span data-stu-id="e7ed7-111">Resolution</span></span>

### <a name="enable-blind-returns-in-adyen"></a><span data-ttu-id="e7ed7-112">Blindretouren in Adyen aktivieren</span><span class="sxs-lookup"><span data-stu-id="e7ed7-112">Enable blind returns in Adyen</span></span>

<span data-ttu-id="e7ed7-113">Befolgen Sie die Schritte in [Problembehandlung beim Zahlungskonnektor von Dynamics 365 für Adyen](adyen-support.md). Wenden Sie sich an das Adyen-Supportteam, und fordern Sie an, dass Blindretouren in Ihrem Adyen-Händlerkonto aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="e7ed7-113">To enable blind returns, follow the steps in [Troubleshoot Dynamics 365 Payment Connector for Adyen issues](adyen-support.md) to contact the Adyen support team and request that blind returns be enabled on your Adyen merchant account.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e7ed7-114">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e7ed7-114">Additional resources</span></span>

[<span data-ttu-id="e7ed7-115">Zahlungskonnektor von Dynamics 365 für Adyen</span><span class="sxs-lookup"><span data-stu-id="e7ed7-115">Dynamics 365 Payment Connector for Adyen</span></span>](../dev-itpro/adyen-connector.md)

[<span data-ttu-id="e7ed7-116">Adyen-Zahlungskonnektor für Dynamics 365 einrichten</span><span class="sxs-lookup"><span data-stu-id="e7ed7-116">Set up the Adyen payment connector for Dynamics 365</span></span>](https://docs.adyen.com/plugins/microsoft-dynamics)
