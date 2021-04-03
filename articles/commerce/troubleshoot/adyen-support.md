---
title: Problembehandlung beim Zahlungskonnektor von Dynamics 365 für Adyen
description: Dieses Thema enthält Anleitungen zur Problembehandlung, die Ihnen helfen können, Unterstützung zu erhalten, wenn Sie Probleme mit dem Zahlungskonnektor von Microsoft Dynamics 365 für Adyen haben.
author: Reza-Assadi
manager: AnnBe
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
ms.openlocfilehash: f01db3fa670355696c094be544775a3abc557a70
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585332"
---
# <a name="troubleshoot-dynamics-365-payment-connector-for-adyen-issues"></a><span data-ttu-id="2e3ba-103">Problembehandlung beim Zahlungskonnektor von Dynamics 365 für Adyen</span><span class="sxs-lookup"><span data-stu-id="2e3ba-103">Troubleshoot Dynamics 365 Payment Connector for Adyen issues</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2e3ba-104">Dieses Thema enthält Anleitungen zur Problembehandlung, die Ihnen helfen können, Unterstützung zu erhalten, wenn Sie Probleme mit dem Zahlungskonnektor von Microsoft Dynamics 365 für Adyen haben.</span><span class="sxs-lookup"><span data-stu-id="2e3ba-104">This topic provides troubleshooting guidance that can help you get support when you have issues with the Microsoft Dynamics 365 Payment Connector for Adyen.</span></span>

## <a name="description"></a><span data-ttu-id="2e3ba-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2e3ba-105">Description</span></span>

<span data-ttu-id="2e3ba-106">Sie haben Probleme mit dem Zahlungskonnektor von Dynamics 365 für Adyen in den folgenden Bereichen und benötigen Unterstützung vom Adyen-Team:</span><span class="sxs-lookup"><span data-stu-id="2e3ba-106">You have issues with the Dynamics 365 Payment Connector for Adyen in the following areas, and you require support from the Adyen team:</span></span>

- <span data-ttu-id="2e3ba-107">Konfiguration von Point of Sale (POS), Modern Point of Sale (MPOS), Call Center oder Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="2e3ba-107">Configuration of Point of sale (POS), Modern point of sale (MPOS), call center, or Dynamics 365 Commerce</span></span>
- <span data-ttu-id="2e3ba-108">Die Referenznummer des Adyen-Zahlungsdienstleisters (PSP) (z. B. wenn Sie Fragen zu Ablehnungen haben, einschließlich Ablehnungen manueller Schlüsseleingaben \[MKE\])</span><span class="sxs-lookup"><span data-stu-id="2e3ba-108">The Adyen payment service provider (PSP) reference number (for example, if you have questions about refusals, including manual key entry \[MKE\] refusals)</span></span>
- <span data-ttu-id="2e3ba-109">Alles, was in Test- oder Live-Händlerumgebungen nicht funktioniert</span><span class="sxs-lookup"><span data-stu-id="2e3ba-109">Anything that isn't working in test or live merchant environments</span></span>

## <a name="resolution"></a><span data-ttu-id="2e3ba-110">Lösung</span><span class="sxs-lookup"><span data-stu-id="2e3ba-110">Resolution</span></span>

<span data-ttu-id="2e3ba-111">Verwenden Sie die folgende E-Mail-Vorlage, um den Supportprozess mit dem Adyen-Team zu starten.</span><span class="sxs-lookup"><span data-stu-id="2e3ba-111">Use the following email template to start the support process with the Adyen team.</span></span> <span data-ttu-id="2e3ba-112">Stellen Sie zur Beschleunigung der Problembehandlung sicher, dass die E-Mail alle erforderlichen Details enthält.</span><span class="sxs-lookup"><span data-stu-id="2e3ba-112">To expedite troubleshooting, make sure that the email contains all the required details.</span></span>

| <span data-ttu-id="2e3ba-113">Feld</span><span class="sxs-lookup"><span data-stu-id="2e3ba-113">Field</span></span>        | <span data-ttu-id="2e3ba-114">Wert</span><span class="sxs-lookup"><span data-stu-id="2e3ba-114">Value</span></span> |
|--------------|-------|
| <span data-ttu-id="2e3ba-115">Nach</span><span class="sxs-lookup"><span data-stu-id="2e3ba-115">To</span></span>           | `support@adyen.com` |
| <span data-ttu-id="2e3ba-116">Cc</span><span class="sxs-lookup"><span data-stu-id="2e3ba-116">Cc</span></span>           | |
| <span data-ttu-id="2e3ba-117">Betreffzeile</span><span class="sxs-lookup"><span data-stu-id="2e3ba-117">Subject line</span></span> | <span data-ttu-id="2e3ba-118">Microsoft Dynamics-Supportanfrage</span><span class="sxs-lookup"><span data-stu-id="2e3ba-118">Microsoft Dynamics Support Request</span></span> |
| <span data-ttu-id="2e3ba-119">Text</span><span class="sxs-lookup"><span data-stu-id="2e3ba-119">Body</span></span>         | <p><span data-ttu-id="2e3ba-120">Hallo Support,</span><span class="sxs-lookup"><span data-stu-id="2e3ba-120">Hi Support,</span></span></p><p><span data-ttu-id="2e3ba-121">bitte helfen Sie bei folgendem Problem:</span><span class="sxs-lookup"><span data-stu-id="2e3ba-121">Please provide support for the following issue:</span></span></p><ul><li><span data-ttu-id="2e3ba-122">Einzelhändlerkonto</span><span class="sxs-lookup"><span data-stu-id="2e3ba-122">Merchant account</span></span></li><li><span data-ttu-id="2e3ba-123">Umgebung (Test/Prod)</span><span class="sxs-lookup"><span data-stu-id="2e3ba-123">Environment (Test/Prod)</span></span></li><li><span data-ttu-id="2e3ba-124">Kanal (POS/Call Center/Commerce E-Commerce)</span><span class="sxs-lookup"><span data-stu-id="2e3ba-124">Channel (POS/call center/Commerce e-commerce)</span></span></li><li><span data-ttu-id="2e3ba-125">PSP-Referenznummer, wenn das Problem eine bestimmte Transaktion betraf (Sie finden die PSP-Referenznummer auf der Quittung, im Adyen-Kundenbereich oder im Transaktionsmenü im POS-Terminal.)</span><span class="sxs-lookup"><span data-stu-id="2e3ba-125">PSP reference number, if the issue involved a specific transaction (You can find the PSP reference number on the receipt, in the Adyen Customer Area, or on the transactions menu on the POS terminal.)</span></span></li><li><span data-ttu-id="2e3ba-126">Gegebenenfalls Screenshot oder Foto der Fehlermeldung</span><span class="sxs-lookup"><span data-stu-id="2e3ba-126">Screenshot or photo of the error message, if applicable</span></span></li><li><span data-ttu-id="2e3ba-127">Ereignisanzeigeprotokolle (im TXT-Format)</span><span class="sxs-lookup"><span data-stu-id="2e3ba-127">Event Viewer logs (in .txt format)</span></span></li><li><span data-ttu-id="2e3ba-128">Beschreibung des Problems und Schritte zur Problembehandlung, die Sie versucht haben</span><span class="sxs-lookup"><span data-stu-id="2e3ba-128">Description of the issue and troubleshooting steps that you've tried</span></span></li></ul> |

## <a name="additional-resources"></a><span data-ttu-id="2e3ba-129">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="2e3ba-129">Additional resources</span></span>

[<span data-ttu-id="2e3ba-130">Akzeptieren von Zahlungen mit dem Adyen-Connector für Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="2e3ba-130">Accept payments with the Adyen connector for Dynamics 365 Commerce</span></span>](https://www.adyen.com/partners/dynamics-365-commerce)

[<span data-ttu-id="2e3ba-131">Zahlungskonnektor von Dynamics 365 für Adyen</span><span class="sxs-lookup"><span data-stu-id="2e3ba-131">Dynamics 365 Payment Connector for Adyen</span></span>](../dev-itpro/adyen-connector.md)

[<span data-ttu-id="2e3ba-132">Adyen-Zahlungskonnektor für Dynamics 365 einrichten</span><span class="sxs-lookup"><span data-stu-id="2e3ba-132">Set up the Adyen payment connector for Dynamics 365</span></span>](https://docs.adyen.com/plugins/microsoft-dynamics)
