---
title: TDS-Sachkonten einrichten
description: In diesem Thema wird erklärt, wie Sie Sachkonten für die Quellenbesteuerungsfunktion (TDS) einrichten.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 93d4cb54488ec0eeee40ca56f3e46f30012f54f5
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023267"
---
# <a name="set-up-tds-ledger-accounts"></a><span data-ttu-id="96ce9-103">TDS-Sachkonten einrichten</span><span class="sxs-lookup"><span data-stu-id="96ce9-103">Set up TDS ledger accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="96ce9-104">In diesem Thema wird erklärt, wie Sie Sachkonten für die Quellenbesteuerungsfunktion (TDS) einrichten.</span><span class="sxs-lookup"><span data-stu-id="96ce9-104">This topic explains how to set up ledger accounts for the Tax Deducted at Source (TDS) feature.</span></span> <span data-ttu-id="96ce9-105">Sie verwenden die Seite **Kontenplan** zum Einrichten von Sachkonten für TDS.</span><span class="sxs-lookup"><span data-stu-id="96ce9-105">You use the **Chart of accounts** page to set up ledger accounts for TDS.</span></span>

1. <span data-ttu-id="96ce9-106">Wechseln Sie zu **Hauptbuch \> Kontenplan \> Konten \> Hauptkonten**.</span><span class="sxs-lookup"><span data-stu-id="96ce9-106">Go to **General ledger \> Chart of accounts \> Accounts \> Main accounts**.</span></span>
2. <span data-ttu-id="96ce9-107">Erstellen Sie auf der Registerkarte **Übersicht** **ALT + N** aus, um ein TDS-Sachkonto zu erstellen und die erforderlichen Details einzugeben.</span><span class="sxs-lookup"><span data-stu-id="96ce9-107">On the **Overview** tab, select **Alt+N** to create a TDS ledger account, and enter the required details.</span></span>
3. <span data-ttu-id="96ce9-108">Wählen Sie auf der Registerkarte **Setup** im Feld **Buchungstyp** **Quellensteuer** aus.</span><span class="sxs-lookup"><span data-stu-id="96ce9-108">On the **Setup** tab, in the **Posting type** field, select **Withholding tax**.</span></span>     

    > [!NOTE]
    > <span data-ttu-id="96ce9-109">Sachkonten mit dem Buchungstyp **Quellensteuer** kann nur als Debitorenkonto festgelegt werden, mit denen der TDS-Forderungsbetrag für einen TDS-Steuercode gebucht wird.</span><span class="sxs-lookup"><span data-stu-id="96ce9-109">Ledger accounts that have a posting type of **Withholding tax** can be defined only as receivable accounts that are used to post the TDS receivable amount for a TDS tax code.</span></span>

4. <span data-ttu-id="96ce9-110">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="96ce9-110">Close the page.</span></span>
