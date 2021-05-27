---
title: Die Rückerstattung einer Rücklieferung wird abgelehnt
description: Dieses Thema enthält Anleitungen zur Fehlerbehebung, die hilfreich sein können, wenn eine Rückerstattung für eine Rücklieferung abgelehnt wird, da sich die für die Fakturierung verwendete Kreditkarte von der Karte unterscheidet, die während der ursprünglichen Zahlungsautorisierung verwendet wurde.
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
ms.openlocfilehash: 99fd4b816b1a3a1fe3c2d1579be45b43fdc3d385
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020755"
---
# <a name="refund-on-a-return-order-is-declined"></a><span data-ttu-id="aa6f9-103">Die Rückerstattung einer Rücklieferung wird abgelehnt</span><span class="sxs-lookup"><span data-stu-id="aa6f9-103">Refund on a return order is declined</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="aa6f9-104">Dieses Thema enthält Anleitungen zur Fehlerbehebung, die hilfreich sein können, wenn eine Rückerstattung für eine Rücklieferung abgelehnt wird, da sich die für die Fakturierung verwendete Kreditkarte von der Karte unterscheidet, die während der ursprünglichen Zahlungsautorisierung verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="aa6f9-104">This topic provides troubleshooting guidance that can help when a refund on a return order is declined because the credit card that is used for invoicing differs from the card that was used during the original payment authorization.</span></span>

## <a name="description"></a><span data-ttu-id="aa6f9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aa6f9-105">Description</span></span>

<span data-ttu-id="aa6f9-106">Eine Rückerstattung wird abgelehnt, wenn die Kreditkarte, mit der eine Rücklieferung fakturiert wird, von der Karte abweicht, die während der ursprünglichen Zahlungsautorisierung verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="aa6f9-106">A refund is declined when the credit card that is used to invoice a return order differs from the card that was used during the original payment authorization.</span></span> <span data-ttu-id="aa6f9-107">Sie erhalten die folgende Fehlermeldung: „Einige Zahlungen haben nicht den richtigen Status für die Buchung.</span><span class="sxs-lookup"><span data-stu-id="aa6f9-107">You receive the following error message: "Some payments are not in the correct status for posting.</span></span> <span data-ttu-id="aa6f9-108">Bitte überprüfen Sie den Status aller Zahlungen vor der Fakturierung erneut.“</span><span class="sxs-lookup"><span data-stu-id="aa6f9-108">Please re-validate the status of all payments prior to invoicing."</span></span>

<span data-ttu-id="aa6f9-109">Die Details der Zahlungsautorisierung enthalten folgende Fehlermeldung: „Adyen-Gateway SendRequest() ist mit dem Status 'InternalServerError'.22144 fehlgeschlagen; leere Antwort von Adyen zurückgegeben.(22001);“</span><span class="sxs-lookup"><span data-stu-id="aa6f9-109">The payment authorization details will include the following error message: "Adyen gateway SendRequest() failed with status 'InternalServerError'.22144; Empty response returned from Adyen.(22001);"</span></span>

![Abgelehnte Rückerstattung einer Rücklieferung – Fehler](media/refund-order-decline.jpg)

## <a name="resolution"></a><span data-ttu-id="aa6f9-111">Lösung</span><span class="sxs-lookup"><span data-stu-id="aa6f9-111">Resolution</span></span>

### <a name="enable-blind-returns-in-adyen"></a><span data-ttu-id="aa6f9-112">Blindretouren in Adyen aktivieren</span><span class="sxs-lookup"><span data-stu-id="aa6f9-112">Enable blind returns in Adyen</span></span>

<span data-ttu-id="aa6f9-113">Befolgen Sie die Schritte in [Problembehandlung beim Zahlungskonnektor von Dynamics 365 für Adyen](adyen-support.md). Wenden Sie sich an das Adyen-Supportteam, und fordern Sie an, dass Blindretouren in Ihrem Adyen-Händlerkonto aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="aa6f9-113">To enable blind returns, follow the steps in [Troubleshoot Dynamics 365 Payment Connector for Adyen issues](adyen-support.md) to contact the Adyen support team and request that blind returns be enabled on your Adyen merchant account.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="aa6f9-114">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="aa6f9-114">Additional resources</span></span>

[<span data-ttu-id="aa6f9-115">Zahlungskonnektor von Dynamics 365 für Adyen</span><span class="sxs-lookup"><span data-stu-id="aa6f9-115">Dynamics 365 Payment Connector for Adyen</span></span>](../dev-itpro/adyen-connector.md)

[<span data-ttu-id="aa6f9-116">Adyen-Zahlungskonnektor für Dynamics 365 einrichten</span><span class="sxs-lookup"><span data-stu-id="aa6f9-116">Set up the Adyen payment connector for Dynamics 365</span></span>](https://docs.adyen.com/plugins/microsoft-dynamics)
