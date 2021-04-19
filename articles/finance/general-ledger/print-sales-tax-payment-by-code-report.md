---
title: Bericht zu Mehrwertsteuerzahlung nach Code drucken
description: Dieses Thema enthält Informationen zu den Einstellungen und Aktionen, die zum Drucken des Umsatzsteuerzahlungsberichts in der Buchhaltungs- oder Steuercodewährung erforderlich sind.
author: anasyash
ms.date: 05/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: 2020-04-08
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: eb3ee4a12d2d29c2769f1ae22e11dc05608b47c1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815451"
---
# <a name="print-the-sales-tax-payment-by-code-report"></a><span data-ttu-id="86ffa-103">Bericht zu Mehrwertsteuerzahlung nach Code drucken</span><span class="sxs-lookup"><span data-stu-id="86ffa-103">Print the Sales tax payment by code report</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="86ffa-104">Um den Bericht **Umsatzsteuerzahlung per Code** zu drucken gehen Sie zu **MwSt** \> **Anfragen und Berichte** \> **Umsatzsteuerberichte** \> **Umsatzsteuerzahlung per Code**.</span><span class="sxs-lookup"><span data-stu-id="86ffa-104">To print the **Sales tax payment by code** report, go to **Tax** \> **Inquiries and reports** \> **Sales tax reports** \> **Sales tax payment by code**.</span></span> <span data-ttu-id="86ffa-105">Standardmäßig werden Berichtsbeträge in der Rechnungswährung der juristischen Person für alle Berichtscodes generiert, die auf der Seite **Umsatzsteuer-Berichtscodes** eingerichtet sind.</span><span class="sxs-lookup"><span data-stu-id="86ffa-105">By default, report amounts are generated in the accounting currency of the legal entity for all reporting codes that are set up on the **Sales tax reporting codes** page.</span></span>

<span data-ttu-id="86ffa-106">Sie können diesen Bericht auch so erstellen, dass er die Umsatzsteuerzahlungsbeträge in den Währungen der Umsatzsteuercodes für alle Berichtscodes anzeigt, die den Umsatzsteuercodes auf der Seite **Umsatzsteuerkennzeichen** zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="86ffa-106">You can also generate this report so that it shows the sales tax payment amounts in the currencies of sales tax codes for all reporting codes that are assigned to sales tax codes on the **Sales tax codes** page.</span></span>

## <a name="turn-on-the-feature"></a><span data-ttu-id="86ffa-107">Aktivieren Sie die Funktion</span><span class="sxs-lookup"><span data-stu-id="86ffa-107">Turn on the feature</span></span>

<span data-ttu-id="86ffa-108">Im Arbeitsbereich **Funktionsverwaltung** aktivieren Sie die folgende Funktion: **Generieren Sie die Umsatzsteuerzahlung per Code-Bericht in der Währung des Umsatzsteuer-Codes**.</span><span class="sxs-lookup"><span data-stu-id="86ffa-108">In the **Feature management** workspace, turn on the following feature: **Generate the Sales tax payment by code report in the sales tax code currency**.</span></span>

## <a name="run-the-report"></a><span data-ttu-id="86ffa-109">Führen Sie den Bericht aus</span><span class="sxs-lookup"><span data-stu-id="86ffa-109">Run the report</span></span>

1. <span data-ttu-id="86ffa-110">Wechseln Sie zu **Steuer** \> **Abfragen und Berichte** \> **Mehrwertsteuerberichte** \> **Mehrwertsteuerzahlung nach Code**.</span><span class="sxs-lookup"><span data-stu-id="86ffa-110">Go to **Tax** \> **Inquiries and reports** \> **Sales tax reports** \> **Sales tax payment by code**.</span></span>
2. <span data-ttu-id="86ffa-111">In dem Feld **Währung melden** wählen Sie im Feld einen der folgenden Werte aus:</span><span class="sxs-lookup"><span data-stu-id="86ffa-111">In the **Report currency** field, select one of the following values:</span></span>

    - <span data-ttu-id="86ffa-112">**Buchhaltungswährung** – Drucken Sie die Berichtsbeträge in der Buchhaltungswährung aus.</span><span class="sxs-lookup"><span data-stu-id="86ffa-112">**Accounting currency** – Print the report amounts in the accounting currency.</span></span>
    - <span data-ttu-id="86ffa-113">**Umsatzsteuercode Währung** – Drucken Sie die Berichtsbeträge in den Währungen der Umsatzsteuerkennzeichen aus.</span><span class="sxs-lookup"><span data-stu-id="86ffa-113">**Sales tax code currency** – Print the report amounts in the currencies of sales tax codes.</span></span>

    ![Bericht Umsatzsteuerzahlung nach Dialogfeld Code](media/Sales-tax-payment-by-code.png)

<span data-ttu-id="86ffa-115">Die folgende Abbildung zeigt ein Beispiel eines anderen Berichts, der erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="86ffa-115">The following illustration shows an example of the report that is generated.</span></span> <span data-ttu-id="86ffa-116">Der Bericht zeigt, dass dieser Berichtscode **101** die **EUR** Währung hat, wenn das Feld **Umsatzsteuerwährung** auf **EUR** gesetzt ist für das Umsatzsteuerkennzeichen, das dem Berichtscode zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="86ffa-116">The report shows that reporting code **101** has the **EUR** currency if the **Sales tax currency** field is set to **EUR** for the sales tax code that the reporting code is assigned to.</span></span>

![Beispiel der Mehrwertsteuerzahlung nach Code](media/Sales-tax-payment-by-code-2.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]