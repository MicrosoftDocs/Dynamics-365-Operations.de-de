---
title: Problembehandlung beim Zahlungskonnektor von Dynamics 365 für Adyen
description: Dieses Thema enthält Anleitungen zur Problembehandlung, die Ihnen helfen können, Unterstützung zu erhalten, wenn Sie Probleme mit dem Zahlungskonnektor von Microsoft Dynamics 365 für Adyen haben.
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
ms.openlocfilehash: 707efeba9553b996e4e33a4754e42a9d22643e33
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019588"
---
# <a name="troubleshoot-dynamics-365-payment-connector-for-adyen-issues"></a><span data-ttu-id="82cd5-103">Problembehandlung beim Zahlungskonnektor von Dynamics 365 für Adyen</span><span class="sxs-lookup"><span data-stu-id="82cd5-103">Troubleshoot Dynamics 365 Payment Connector for Adyen issues</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="82cd5-104">Dieses Thema enthält Anleitungen zur Problembehandlung, die Ihnen helfen können, Unterstützung zu erhalten, wenn Sie Probleme mit dem Zahlungskonnektor von Microsoft Dynamics 365 für Adyen haben.</span><span class="sxs-lookup"><span data-stu-id="82cd5-104">This topic provides troubleshooting guidance that can help you get support when you have issues with the Microsoft Dynamics 365 Payment Connector for Adyen.</span></span>

## <a name="description"></a><span data-ttu-id="82cd5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="82cd5-105">Description</span></span>

<span data-ttu-id="82cd5-106">Sie haben Probleme mit dem Zahlungskonnektor von Dynamics 365 für Adyen in den folgenden Bereichen und benötigen Unterstützung vom Adyen-Team:</span><span class="sxs-lookup"><span data-stu-id="82cd5-106">You have issues with the Dynamics 365 Payment Connector for Adyen in the following areas, and you require support from the Adyen team:</span></span>

- <span data-ttu-id="82cd5-107">Konfiguration von Point of Sale (POS), Modern Point of Sale (MPOS), Call Center oder Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="82cd5-107">Configuration of Point of sale (POS), Modern point of sale (MPOS), call center, or Dynamics 365 Commerce</span></span>
- <span data-ttu-id="82cd5-108">Die Referenznummer des Adyen-Zahlungsdienstleisters (PSP) (z. B. wenn Sie Fragen zu Ablehnungen haben, einschließlich Ablehnungen manueller Schlüsseleingaben \[MKE\])</span><span class="sxs-lookup"><span data-stu-id="82cd5-108">The Adyen payment service provider (PSP) reference number (for example, if you have questions about refusals, including manual key entry \[MKE\] refusals)</span></span>
- <span data-ttu-id="82cd5-109">Alles, was in Test- oder Live-Händlerumgebungen nicht funktioniert</span><span class="sxs-lookup"><span data-stu-id="82cd5-109">Anything that isn't working in test or live merchant environments</span></span>

## <a name="resolution"></a><span data-ttu-id="82cd5-110">Lösung</span><span class="sxs-lookup"><span data-stu-id="82cd5-110">Resolution</span></span>

<span data-ttu-id="82cd5-111">Verwenden Sie die folgende E-Mail-Vorlage, um den Supportprozess mit dem Adyen-Team zu starten.</span><span class="sxs-lookup"><span data-stu-id="82cd5-111">Use the following email template to start the support process with the Adyen team.</span></span> <span data-ttu-id="82cd5-112">Stellen Sie zur Beschleunigung der Problembehandlung sicher, dass die E-Mail alle erforderlichen Details enthält.</span><span class="sxs-lookup"><span data-stu-id="82cd5-112">To expedite troubleshooting, make sure that the email contains all the required details.</span></span>

| <span data-ttu-id="82cd5-113">Feld</span><span class="sxs-lookup"><span data-stu-id="82cd5-113">Field</span></span>        | <span data-ttu-id="82cd5-114">Wert</span><span class="sxs-lookup"><span data-stu-id="82cd5-114">Value</span></span> |
|--------------|-------|
| <span data-ttu-id="82cd5-115">Nach</span><span class="sxs-lookup"><span data-stu-id="82cd5-115">To</span></span>           | `support@adyen.com` |
| <span data-ttu-id="82cd5-116">Cc</span><span class="sxs-lookup"><span data-stu-id="82cd5-116">Cc</span></span>           | |
| <span data-ttu-id="82cd5-117">Betreffzeile</span><span class="sxs-lookup"><span data-stu-id="82cd5-117">Subject line</span></span> | <span data-ttu-id="82cd5-118">Microsoft Dynamics-Supportanfrage</span><span class="sxs-lookup"><span data-stu-id="82cd5-118">Microsoft Dynamics Support Request</span></span> |
| <span data-ttu-id="82cd5-119">Text</span><span class="sxs-lookup"><span data-stu-id="82cd5-119">Body</span></span>         | <p><span data-ttu-id="82cd5-120">Hallo Support,</span><span class="sxs-lookup"><span data-stu-id="82cd5-120">Hi Support,</span></span></p><p><span data-ttu-id="82cd5-121">bitte helfen Sie bei folgendem Problem:</span><span class="sxs-lookup"><span data-stu-id="82cd5-121">Please provide support for the following issue:</span></span></p><ul><li><span data-ttu-id="82cd5-122">Einzelhändlerkonto</span><span class="sxs-lookup"><span data-stu-id="82cd5-122">Merchant account</span></span></li><li><span data-ttu-id="82cd5-123">Umgebung (Test/Prod)</span><span class="sxs-lookup"><span data-stu-id="82cd5-123">Environment (Test/Prod)</span></span></li><li><span data-ttu-id="82cd5-124">Kanal (POS/Call Center/Commerce E-Commerce)</span><span class="sxs-lookup"><span data-stu-id="82cd5-124">Channel (POS/call center/Commerce e-commerce)</span></span></li><li><span data-ttu-id="82cd5-125">PSP-Referenznummer, wenn das Problem eine bestimmte Transaktion betraf (Sie finden die PSP-Referenznummer auf der Quittung, im Adyen-Kundenbereich oder im Transaktionsmenü im POS-Terminal.)</span><span class="sxs-lookup"><span data-stu-id="82cd5-125">PSP reference number, if the issue involved a specific transaction (You can find the PSP reference number on the receipt, in the Adyen Customer Area, or on the transactions menu on the POS terminal.)</span></span></li><li><span data-ttu-id="82cd5-126">Gegebenenfalls Screenshot oder Foto der Fehlermeldung</span><span class="sxs-lookup"><span data-stu-id="82cd5-126">Screenshot or photo of the error message, if applicable</span></span></li><li><span data-ttu-id="82cd5-127">Ereignisanzeigeprotokolle (im TXT-Format)</span><span class="sxs-lookup"><span data-stu-id="82cd5-127">Event Viewer logs (in .txt format)</span></span></li><li><span data-ttu-id="82cd5-128">Beschreibung des Problems und Schritte zur Problembehandlung, die Sie versucht haben</span><span class="sxs-lookup"><span data-stu-id="82cd5-128">Description of the issue and troubleshooting steps that you've tried</span></span></li></ul> |

## <a name="additional-resources"></a><span data-ttu-id="82cd5-129">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="82cd5-129">Additional resources</span></span>

[<span data-ttu-id="82cd5-130">Akzeptieren von Zahlungen mit dem Adyen-Connector für Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="82cd5-130">Accept payments with the Adyen connector for Dynamics 365 Commerce</span></span>](https://www.adyen.com/partners/dynamics-365-commerce)

[<span data-ttu-id="82cd5-131">Zahlungskonnektor von Dynamics 365 für Adyen</span><span class="sxs-lookup"><span data-stu-id="82cd5-131">Dynamics 365 Payment Connector for Adyen</span></span>](../dev-itpro/adyen-connector.md)

[<span data-ttu-id="82cd5-132">Adyen-Zahlungskonnektor für Dynamics 365 einrichten</span><span class="sxs-lookup"><span data-stu-id="82cd5-132">Set up the Adyen payment connector for Dynamics 365</span></span>](https://docs.adyen.com/plugins/microsoft-dynamics)
