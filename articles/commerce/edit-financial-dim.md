---
title: Finanzdimensionen für Einzelhandelstransaktionen bearbeiten
description: In diesem Thema wird beschrieben, wie Finanzdimensionen für Einzelhandelstransaktionen in Microsoft Dynamics 365 Commerce bearbeitet werden.
author: josaw1
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 381d8bb0939f6c4c163477990e49382201487375
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019906"
---
# <a name="edit-financial-dimensions-for-retail-transactions"></a><span data-ttu-id="1dcf2-103">Finanzdimensionen für Einzelhandelstransaktionen bearbeiten</span><span class="sxs-lookup"><span data-stu-id="1dcf2-103">Edit financial dimensions for retail transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1dcf2-104">In diesem Thema wird beschrieben, wie Finanzdimensionen für Einzelhandelstransaktionen in Microsoft Dynamics 365 Commerce bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="1dcf2-104">This topic describes how to edit financial dimensions for retail transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="edit-financial-dimensions"></a><span data-ttu-id="1dcf2-105">Finanzdimensionen bearbeiten</span><span class="sxs-lookup"><span data-stu-id="1dcf2-105">Edit financial dimensions</span></span>

<span data-ttu-id="1dcf2-106">Führen Sie die folgenden Schritte aus, um Finanzdimensionen für Einzelhandelstransaktionen in Commerce Headquarters zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="1dcf2-106">To edit financial dimensions for retail transactions in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="1dcf2-107">Öffnen Sie die Seite **Finanzdimensionskonfiguration für Integrationsanwendungen**.</span><span class="sxs-lookup"><span data-stu-id="1dcf2-107">Open the **Financial dimensions configuration for integrating applications** page.</span></span>
1. <span data-ttu-id="1dcf2-108">Wählen Sie den aktiven Datensatz **Standarddimensionsintegration**.</span><span class="sxs-lookup"><span data-stu-id="1dcf2-108">Select the active **Default dimensions integration** record.</span></span>
1. <span data-ttu-id="1dcf2-109">Vergewissern Sie sich, dass im Inforegister **Finanzdimensionen** alle Dimensionen, die Sie im Excel-Arbeitsblatt bearbeiten möchten, in der **Ausgewählt**-Liste vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="1dcf2-109">On the **Financial dimensions** FastTab, make sure that all the dimensions that you want to edit in the Excel worksheet are present in the **Selected** list.</span></span> <span data-ttu-id="1dcf2-110">Weitere Informationen finden Sie unter [Datenentitäten](../fin-ops-core/dev-itpro/financial/financial-dimension-configuration-integration.md#data-entities).</span><span class="sxs-lookup"><span data-stu-id="1dcf2-110">For more information, see [Data entities](../fin-ops-core/dev-itpro/financial/financial-dimension-configuration-integration.md#data-entities).</span></span>
1. <span data-ttu-id="1dcf2-111">Laden Sie die Excel-Datei von der Seite **Aufstellungen**, der Seite **Einzelhandelstransaktionen** oder der Kachel **Transaktionsüberprüfungsfehler** im Arbeitsbereich **Finanzdaten für Shop** herunter, und öffnen Sie sie.</span><span class="sxs-lookup"><span data-stu-id="1dcf2-111">Download and open the Excel file from the **Statements** page, the **Retail transactions** page, or the **Transaction validation failures** tile in the **Store financials** workspace.</span></span>
1. <span data-ttu-id="1dcf2-112">Wählen Sie **Entwerfen** aus, um die Finanzdimension der Transaktion zu ändern, und wählen Sie anschließend das Stiftsymbol neben der Zeile **Transaktion (prüfbar)** aus.</span><span class="sxs-lookup"><span data-stu-id="1dcf2-112">To change the transaction financial dimension, select **Design**, and then select the pencil symbol next to the **Transaction (auditable)** row.</span></span>
1. <span data-ttu-id="1dcf2-113">Suchen und wählen Sie das Feld **FinancialDimensionDisplayValue**. Wählen Sie Kopfzeilenbereich des Excel-Arbeitsblatts eine Zelle und anschließend **Beschriftung hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="1dcf2-113">Find and select the **FinancialDimensionDisplayValue** field, select a cell in the header part of the Excel worksheet, and then select **Add label**.</span></span>
1. <span data-ttu-id="1dcf2-114">Wählen Sie unter der im vorherigen Schritt ausgewählten Zelle eine Zelle aus. Wählen Sie **Wert hinzufügen** und anschließend **Aktualisieren** aus.</span><span class="sxs-lookup"><span data-stu-id="1dcf2-114">Select a cell below the cell that you selected in the previous step, select **Add Value**, and then select **Refresh**.</span></span> <span data-ttu-id="1dcf2-115">Die Finanzdimensionen werden dem Excel-Arbeitsblatt hinzugefügt und können dann bearbeitet und veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="1dcf2-115">The financial dimensions are added to the Excel worksheet, and they can then be edited and published.</span></span>
1. <span data-ttu-id="1dcf2-116">Um die Dimensionen in den Transaktionspositionen zu ändern, wählen Sie die Zeile **Verkaufstransaktionen (prüfbar)** und das Stiftsymbol aus. Wiederholen Sie die Schritte 6 und 7.</span><span class="sxs-lookup"><span data-stu-id="1dcf2-116">To change the dimensions on the transaction lines, select the **Sales transactions (auditable)** row, select the pencil symbol, and then repeat steps 6 and 7.</span></span>
1. <span data-ttu-id="1dcf2-117">Um die Dimensionen in den Zahlungspositionen zu ändern, wählen Sie die Zeile **Zahlungstransaktionen (prüfbar)** und das Stiftsymbol aus. Wiederholen Sie die Schritte 6 und 7.</span><span class="sxs-lookup"><span data-stu-id="1dcf2-117">To change the dimensions on the payment lines, select the **Payment transactions (auditable)** row, select the pencil symbol, and then repeat steps 6 and 7.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1dcf2-118">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1dcf2-118">Additional resources</span></span>

[<span data-ttu-id="1dcf2-119">Abholungs- und Bargeldverwaltungstransaktionen bearbeiten und prüfen</span><span class="sxs-lookup"><span data-stu-id="1dcf2-119">Edit and audit cash and carry and cash management transactions</span></span>](edit-cash-trans.md)

[<span data-ttu-id="1dcf2-120">Onlineauftrag und asynchrone Debitorenauftragstransaktionen bearbeiten und prüfen</span><span class="sxs-lookup"><span data-stu-id="1dcf2-120">Edit and audit online order and asynchronous customer order transactions</span></span>](edit-order-trans.md)

[<span data-ttu-id="1dcf2-121">Excel-Arbeitsmappe zum Bearbeiten von Einzelhandelstransaktionen erstellen</span><span class="sxs-lookup"><span data-stu-id="1dcf2-121">Create an Excel workbook to edit retail transactions</span></span>](create-excel-edit.md)

[<span data-ttu-id="1dcf2-122">Einer Excel-Arbeitsmappe zum Bearbeiten von Einzelhandelstransaktionen Felder hinzufügen</span><span class="sxs-lookup"><span data-stu-id="1dcf2-122">Add fields to an Excel workbook to edit retail transactions</span></span>](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]