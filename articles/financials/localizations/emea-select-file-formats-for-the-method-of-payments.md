---
title: Dateiformate für Zahlungsmethoden
description: In diesem Thema werden die zwei Methoden für das Zuweisen von Dateiformaten, die für Zahlungsmethoden verwendet werden können, beschrieben.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymMode, VendPaymMode
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 262514
ms.search.region: Belgium, France, Germany, Norway, Spain, Sweden, Switzerland
ms.author: v-lenest
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 350bea3e4a698e5e7c71fe4fcbb7e7386939511e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571297"
---
# <a name="file-formats-for-methods-of-payment"></a><span data-ttu-id="808f8-103">Dateiformate für Zahlungsmethoden</span><span class="sxs-lookup"><span data-stu-id="808f8-103">File formats for methods of payment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="808f8-104">In diesem Thema werden die zwei Methoden für das Zuweisen von Dateiformaten, die für Zahlungsmethoden verwendet werden können, beschrieben.</span><span class="sxs-lookup"><span data-stu-id="808f8-104">This topic describes the two methods for getting file formats that you can use for methods of payment.</span></span>

<span data-ttu-id="808f8-105">Es gibt zwei Methoden, die Sie verwenden können, um die Dateiformate für die Verwendung mit Zahlungsmethoden, elektronischen Meldedateiformaten (ER)- oder X++-Dateiformate abzurufen.</span><span class="sxs-lookup"><span data-stu-id="808f8-105">There are two methods that you can use to get file formats for use with methods of payment, electronic reporting (ER) file formats or X++ file formats.</span></span> <span data-ttu-id="808f8-106">Wenn Sie eine Zahlungsmethode für einen Debitor oder Kreditor einrichten, geben Sie an, welche Dateiformate und Standardwerten für Zahlungen verwendet werden sollen und wie Zahlungen verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="808f8-106">When you set up a method of payment for a customer or vendor, you indicate which file formats and standards should be used for payments and how payments will be processed.</span></span> <span data-ttu-id="808f8-107">Folgende Formattypenb stehen zur Auswahl:</span><span class="sxs-lookup"><span data-stu-id="808f8-107">You can select from the following types of formats:</span></span>

-   <span data-ttu-id="808f8-108">Warenexport</span><span class="sxs-lookup"><span data-stu-id="808f8-108">Export</span></span>
-   <span data-ttu-id="808f8-109">Warenimport</span><span class="sxs-lookup"><span data-stu-id="808f8-109">Import</span></span>
-   <span data-ttu-id="808f8-110">Zurück</span><span class="sxs-lookup"><span data-stu-id="808f8-110">Return</span></span>
-   <span data-ttu-id="808f8-111">Geldtransfer</span><span class="sxs-lookup"><span data-stu-id="808f8-111">Remittance</span></span>

### <a name="method-1-electronic-reporting-file-formats"></a><span data-ttu-id="808f8-112">Methode 1: Elektronische Berichterstellungsformate</span><span class="sxs-lookup"><span data-stu-id="808f8-112">Method 1: Electronic reporting file formats</span></span>

<span data-ttu-id="808f8-113">Für Dateiformate, die auf der Grundlage der ER-Konfigurationen basieren, müssen Sie die Konfigurationen aus dem Lifecycle Services (LCS) importieren.</span><span class="sxs-lookup"><span data-stu-id="808f8-113">For file formats that are based on ER configurations, you must import the configurations from Lifecycle Services (LCS).</span></span> <span data-ttu-id="808f8-114">Weitere Informationen finden Sie unter [Elektronische Berichtskonfigurationen aus Lifecycle Services herunterladen](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span><span class="sxs-lookup"><span data-stu-id="808f8-114">For more information, see [Download Electronic reporting configurations from Lifecycle Services](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span></span> <span data-ttu-id="808f8-115">Nachdem Sie diese Berichterstellungskonfigurationen für Dateiformate importieren haben, sind die importierten Formate verfügbar auf der Seite **Zahlungsmethoden**.</span><span class="sxs-lookup"><span data-stu-id="808f8-115">After you import reporting configurations for those file formats, the imported formats will be available to select on the **Methods of payment** page.</span></span> <span data-ttu-id="808f8-116">Der Prozess für den Import und die Auswahl von Dateiformaten für Europa ist gleich wie die Prozedur für Japan.</span><span class="sxs-lookup"><span data-stu-id="808f8-116">The process for importing and selecting file formats for Europe is similar to the procedure for Japan.</span></span> <span data-ttu-id="808f8-117">Weitere Informationen finden Sie unter [Aktivieren Sie das JBA-Zahlungsdateiformat](tasks/jba-payment-file-format.md)</span><span class="sxs-lookup"><span data-stu-id="808f8-117">For more details, see [Enable the JBA payment file format](tasks/jba-payment-file-format.md)</span></span>

### <a name="method-2-x-file-formats"></a><span data-ttu-id="808f8-118">Methode 2: X++-Dateiformate</span><span class="sxs-lookup"><span data-stu-id="808f8-118">Method 2: X++ file formats</span></span>

<span data-ttu-id="808f8-119">Um Dateiformate auszuwählen, die auf der Grundlage X++-Code basieren, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="808f8-119">To select file formats that are based on X++ code, complete the following steps.</span></span>

1.  <span data-ttu-id="808f8-120">Gehen Sie zur Seite **Zahlungsmethode**</span><span class="sxs-lookup"><span data-stu-id="808f8-120">Go to the **Methods of payment** page.</span></span>
2.  <span data-ttu-id="808f8-121">Wählen Sie im Inforegister **Dateiformate** **Einstellungen**.</span><span class="sxs-lookup"><span data-stu-id="808f8-121">On the **File formats** FastTab, click **Setup**.</span></span>
3.  <span data-ttu-id="808f8-122">Wählen Sie die Registerkarte aus, die dem Dateiformattyp entspricht.</span><span class="sxs-lookup"><span data-stu-id="808f8-122">Select the tab that corresponds with the file format type.</span></span>
4.  <span data-ttu-id="808f8-123">Wählen Sie ein Dateiformat aus der Liste **Verfügbar** aus und verschieben Sie diese mit dem Pfeilsteuerelement in die Liste **Ausgewählt**.</span><span class="sxs-lookup"><span data-stu-id="808f8-123">Select a file format from the **Available** list and move it to the **Selected** list with the arrow control.</span></span>
5.  <span data-ttu-id="808f8-124">Schließen Sie das Formular **Dateiformate für Zahlungsmethoden**.</span><span class="sxs-lookup"><span data-stu-id="808f8-124">Close the **File formats for methods of payment** page.</span></span>
6.  <span data-ttu-id="808f8-125">Wählen Sie im Inforegister **Dateiformate** das Dateiformat für die Zahlungsmethode aus dem entsprechenden Dateiformatfeld aus.</span><span class="sxs-lookup"><span data-stu-id="808f8-125">On the **File formats** FastTab, select the file format to use for the method of payment from the appropriate file format field.</span></span> <span data-ttu-id="808f8-126">Die allgemeinen elektronischen Berichtsoptionen sollen **Nein** für X++-Dateiformate sein.</span><span class="sxs-lookup"><span data-stu-id="808f8-126">The General electronic reporting options should be set to **No** for X++ file formats.</span></span>




