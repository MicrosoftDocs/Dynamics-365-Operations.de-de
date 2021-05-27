---
title: Gedruckte Debitorenrechnungen mit Hashnummern archivieren
description: In diesem Thema wird erläutert, wie Sie die Archivierung aktivieren, um gedruckte Debitorenrechnungen mit Hashnummern zu speichern.
author: ilyako
ms.date: 03/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 841e6059f5b0d70dbd1fe12a1f8910bbb31ddc86
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018977"
---
# <a name="archive-printed-customer-invoices-with-hash-numbers"></a><span data-ttu-id="2a391-103">Gedruckte Debitorenrechnungen mit Hashnummern archivieren</span><span class="sxs-lookup"><span data-stu-id="2a391-103">Archive printed customer invoices with hash numbers</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="2a391-104">In einigen Ländern ist es gesetzlich vorgeschrieben, berechnete Hashnummern zusammen mit Ausdrucken einiger Dokumente im System zu speichern.</span><span class="sxs-lookup"><span data-stu-id="2a391-104">In some countries, there is a legal requirement to store calculated hash numbers in the system together with printouts of some documents.</span></span> <span data-ttu-id="2a391-105">Hashnummern können für die Berichterstattung an Behörden und während Audits verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2a391-105">Hash numbers can be used for reporting to authorities and during audits.</span></span>

<span data-ttu-id="2a391-106">In diesem Thema wird erläutert, wie Sie die Archivierung konfigurieren, um gedruckte Debitorenrechnungen mit Hashnummern zu speichern.</span><span class="sxs-lookup"><span data-stu-id="2a391-106">This topic explains how to configure archiving in order to store printed customer invoices with hash numbers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2a391-107">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="2a391-107">Prerequisites</span></span>

- <span data-ttu-id="2a391-108">In dem Arbeitsbereich **Funktionsverwaltung** aktivieren Sie die Funktion **Gedruckte Debitorenrechnungen mit Hashnummern archivieren**.</span><span class="sxs-lookup"><span data-stu-id="2a391-108">In the **Feature management** workspace, turn on the feature, **Archive printed customer invoices with hash numbers**.</span></span> <span data-ttu-id="2a391-109">Weitere Informationen finden Sie unter [Funktionsverwaltung – Übersicht](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="2a391-109">For more information, see [Feature management overview](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>
- <span data-ttu-id="2a391-110">Konfigurieren Sie die druckbaren Formate der erforderlichen Dokumente in der **Druckverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="2a391-110">Configure the printable formats of required documents in **Print management**.</span></span>

<span data-ttu-id="2a391-111">Diese Funktionalität gilt für die folgenden Dokumente.</span><span class="sxs-lookup"><span data-stu-id="2a391-111">This functionality is applicable to the following documents.</span></span>

<span data-ttu-id="2a391-112">**Debitorenkonten**</span><span class="sxs-lookup"><span data-stu-id="2a391-112">**Accounts receivable**</span></span>
- <span data-ttu-id="2a391-113">Debitorenrechnung</span><span class="sxs-lookup"><span data-stu-id="2a391-113">Customer invoice</span></span>
- <span data-ttu-id="2a391-114">Debitorengutschrift</span><span class="sxs-lookup"><span data-stu-id="2a391-114">Customer credit note</span></span>
- <span data-ttu-id="2a391-115">Freitextrechnung</span><span class="sxs-lookup"><span data-stu-id="2a391-115">Free text invoice</span></span>
- <span data-ttu-id="2a391-116">Freitext-Gutschrift</span><span class="sxs-lookup"><span data-stu-id="2a391-116">Free text credit note</span></span>

<span data-ttu-id="2a391-117">**Projektverwaltung und Buchhaltung**</span><span class="sxs-lookup"><span data-stu-id="2a391-117">**Project management and accounting**</span></span>
- <span data-ttu-id="2a391-118">Projektrechnung</span><span class="sxs-lookup"><span data-stu-id="2a391-118">Project invoice</span></span>
- <span data-ttu-id="2a391-119">Projektgutschrift</span><span class="sxs-lookup"><span data-stu-id="2a391-119">Project credit note</span></span>

## <a name="configure-customer-master-data"></a><span data-ttu-id="2a391-120">Debitorenmasterdaten konfigurieren</span><span class="sxs-lookup"><span data-stu-id="2a391-120">Configure customer master data</span></span>
<span data-ttu-id="2a391-121">Führen Sie die folgenden Schritte aus, um Kundendaten zu konfigurieren und die Möglichkeit zu aktivieren, gedruckte Rechnungen automatisch als Anhänge zu speichern.</span><span class="sxs-lookup"><span data-stu-id="2a391-121">Complete the following steps to configure customer data and turn on the ability to automatically save printed invoices as attachments.</span></span>

1. <span data-ttu-id="2a391-122">Wechseln Sie zu **Debitorenkonten** > **Alle Debitoren**.</span><span class="sxs-lookup"><span data-stu-id="2a391-122">Go to **Accounts receivable** > **All customers**.</span></span> 
2. <span data-ttu-id="2a391-123">Wählen Sie einen Kunden aus und wählen Sie im Inforegister **Rechnung und Lieferung** im Abschnitt **E-RECHNUNG** im Feld **eInvoice-Anhang** die Option **Ja** aus.</span><span class="sxs-lookup"><span data-stu-id="2a391-123">Select a customer, and on the **Invoice and delivery** FastTab, in the **E-INVOCE** section, in the **eInvoice attachment** field, select **Yes**.</span></span>

## <a name="print-invoices"></a><span data-ttu-id="2a391-124">Rechnungen drucken</span><span class="sxs-lookup"><span data-stu-id="2a391-124">Print invoices</span></span>
<span data-ttu-id="2a391-125">Sie können jede Freitext-, Debitoren- und Projektrechnung oder -gutschrift für den Kunden, die im vorherigen Verfahren konfiguriert wurde, buchen und ausdrucken.</span><span class="sxs-lookup"><span data-stu-id="2a391-125">You can post and print any free text, customer, and project invoice or credit note for the customer configured in the previous procedure.</span></span>

<span data-ttu-id="2a391-126">Öffnen Sie die Seite **Anhänge** für die gedruckte Rechnung.</span><span class="sxs-lookup"><span data-stu-id="2a391-126">Open the **Attachments** page for the printed invoice.</span></span> <span data-ttu-id="2a391-127">Im Inforegister **Anhang** in der Feldgruppe **Weitere Details** im Feld **Dokument-Hashnummer** finden Sie die gespeicherte Hashnummer, die für die gedruckte Rechnung berechnet wurde.</span><span class="sxs-lookup"><span data-stu-id="2a391-127">On the **Attachment** FastTab, in the **Additional details** field group, in **Document hash number** field, find the stored hash number calculated for the printed invoice.</span></span>

![Anhangs-Hashnummer](media/attach-hash-num.jpg)

