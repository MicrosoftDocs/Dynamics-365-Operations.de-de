---
title: Dateiformate für Zahlungsmethoden
description: In diesem Thema werden die zwei Methoden für das Zuweisen von Dateiformaten, die für Zahlungsmethoden verwendet werden können, beschrieben.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPaymMode, VendPaymMode
audience: Application User
ms.reviewer: kfend
ms.custom: 262514
ms.search.region: Belgium, France, Germany, Norway, Spain, Sweden, Switzerland
ms.author: v-lenest
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 895fbe2a46d99aed175676c22ba13c30d6d8b98e
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5894676"
---
# <a name="file-formats-for-methods-of-payment"></a><span data-ttu-id="8f990-103">Dateiformate für Zahlungsmethoden</span><span class="sxs-lookup"><span data-stu-id="8f990-103">File formats for methods of payment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8f990-104">In diesem Thema werden die zwei Methoden für das Zuweisen von Dateiformaten, die für Zahlungsmethoden verwendet werden können, beschrieben.</span><span class="sxs-lookup"><span data-stu-id="8f990-104">This topic describes the two methods for getting file formats that you can use for methods of payment.</span></span>

<span data-ttu-id="8f990-105">Es gibt zwei Methoden, die Sie verwenden können, um die Dateiformate für die Verwendung mit Zahlungsmethoden, elektronischen Meldedateiformaten (ER)- oder X++-Dateiformate abzurufen.</span><span class="sxs-lookup"><span data-stu-id="8f990-105">There are two methods that you can use to get file formats for use with methods of payment, electronic reporting (ER) file formats or X++ file formats.</span></span> <span data-ttu-id="8f990-106">Wenn Sie eine Zahlungsmethode für einen Debitor oder Kreditor einrichten, geben Sie an, welche Dateiformate und Standardwerten für Zahlungen verwendet werden sollen und wie Zahlungen verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="8f990-106">When you set up a method of payment for a customer or vendor, you indicate which file formats and standards should be used for payments and how payments will be processed.</span></span> <span data-ttu-id="8f990-107">Folgende Formattypenb stehen zur Auswahl:</span><span class="sxs-lookup"><span data-stu-id="8f990-107">You can select from the following types of formats:</span></span>

-   <span data-ttu-id="8f990-108">Warenexport</span><span class="sxs-lookup"><span data-stu-id="8f990-108">Export</span></span>
-   <span data-ttu-id="8f990-109">Warenimport</span><span class="sxs-lookup"><span data-stu-id="8f990-109">Import</span></span>
-   <span data-ttu-id="8f990-110">Zurück</span><span class="sxs-lookup"><span data-stu-id="8f990-110">Return</span></span>
-   <span data-ttu-id="8f990-111">Geldtransfer</span><span class="sxs-lookup"><span data-stu-id="8f990-111">Remittance</span></span>

### <a name="method-1-electronic-reporting-file-formats"></a><span data-ttu-id="8f990-112">Methode 1: Elektronische Berichterstellungsformate</span><span class="sxs-lookup"><span data-stu-id="8f990-112">Method 1: Electronic reporting file formats</span></span>

<span data-ttu-id="8f990-113">Für Dateiformate, die auf der Grundlage der ER-Konfigurationen basieren, müssen Sie die Konfigurationen aus dem Lifecycle Services (LCS) importieren.</span><span class="sxs-lookup"><span data-stu-id="8f990-113">For file formats that are based on ER configurations, you must import the configurations from Lifecycle Services (LCS).</span></span> <span data-ttu-id="8f990-114">Weitere Informationen finden Sie unter [Elektronische Berichtskonfigurationen aus Lifecycle Services herunterladen](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span><span class="sxs-lookup"><span data-stu-id="8f990-114">For more information, see [Download Electronic reporting configurations from Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span></span> <span data-ttu-id="8f990-115">Nachdem Sie diese Berichterstellungskonfigurationen für Dateiformate importieren haben, sind die importierten Formate verfügbar auf der Seite **Zahlungsmethoden**.</span><span class="sxs-lookup"><span data-stu-id="8f990-115">After you import reporting configurations for those file formats, the imported formats will be available to select on the **Methods of payment** page.</span></span> <span data-ttu-id="8f990-116">Der Prozess für den Import und die Auswahl von Dateiformaten für Europa ist gleich wie die Prozedur für Japan.</span><span class="sxs-lookup"><span data-stu-id="8f990-116">The process for importing and selecting file formats for Europe is similar to the procedure for Japan.</span></span> <span data-ttu-id="8f990-117">Weitere Informationen finden Sie unter [Aktivieren Sie das JBA-Zahlungsdateiformat](tasks/jba-payment-file-format.md)</span><span class="sxs-lookup"><span data-stu-id="8f990-117">For more details, see [Enable the JBA payment file format](tasks/jba-payment-file-format.md)</span></span>

### <a name="method-2-x-file-formats"></a><span data-ttu-id="8f990-118">Methode 2: X++-Dateiformate</span><span class="sxs-lookup"><span data-stu-id="8f990-118">Method 2: X++ file formats</span></span>

<span data-ttu-id="8f990-119">Um Dateiformate auszuwählen, die auf der Grundlage X++-Code basieren, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="8f990-119">To select file formats that are based on X++ code, complete the following steps.</span></span>

1.  <span data-ttu-id="8f990-120">Gehen Sie zur Seite **Zahlungsmethode**</span><span class="sxs-lookup"><span data-stu-id="8f990-120">Go to the **Methods of payment** page.</span></span>
2.  <span data-ttu-id="8f990-121">Wählen Sie im Inforegister **Dateiformate** **Einstellungen**.</span><span class="sxs-lookup"><span data-stu-id="8f990-121">On the **File formats** FastTab, click **Setup**.</span></span>
3.  <span data-ttu-id="8f990-122">Wählen Sie die Registerkarte aus, die dem Dateiformattyp entspricht.</span><span class="sxs-lookup"><span data-stu-id="8f990-122">Select the tab that corresponds with the file format type.</span></span>
4.  <span data-ttu-id="8f990-123">Wählen Sie ein Dateiformat aus der Liste **Verfügbar** aus und verschieben Sie diese mit dem Pfeilsteuerelement in die Liste **Ausgewählt**.</span><span class="sxs-lookup"><span data-stu-id="8f990-123">Select a file format from the **Available** list and move it to the **Selected** list with the arrow control.</span></span>
5.  <span data-ttu-id="8f990-124">Schließen Sie das Formular **Dateiformate für Zahlungsmethoden**.</span><span class="sxs-lookup"><span data-stu-id="8f990-124">Close the **File formats for methods of payment** page.</span></span>
6.  <span data-ttu-id="8f990-125">Wählen Sie im Inforegister **Dateiformate** das Dateiformat für die Zahlungsmethode aus dem entsprechenden Dateiformatfeld aus.</span><span class="sxs-lookup"><span data-stu-id="8f990-125">On the **File formats** FastTab, select the file format to use for the method of payment from the appropriate file format field.</span></span> <span data-ttu-id="8f990-126">Die allgemeinen elektronischen Berichtsoptionen sollen **Nein** für X++-Dateiformate sein.</span><span class="sxs-lookup"><span data-stu-id="8f990-126">The General electronic reporting options should be set to **No** for X++ file formats.</span></span>






[!INCLUDE[footer-include](../../includes/footer-banner.md)]