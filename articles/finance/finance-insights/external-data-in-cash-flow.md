---
title: Externe Daten in Cashflow-Planungen verwenden (Vorschau)
description: In diesem Thema werden die Einrichtungsschritte beschrieben, die Sie ausführen müssen, damit externe Daten eingegeben oder in Cashflow-Planungen importiert werden können.
author: rcarlson
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-06-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 66bdb8bd638859bb4fc5565e3f12a8f671addcff
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186689"
---
# <a name="use-external-data-in-cash-flow-forecasts-preview"></a><span data-ttu-id="f863a-103">Externe Daten in Cashflow-Planungen verwenden (Vorschau)</span><span class="sxs-lookup"><span data-stu-id="f863a-103">Use external data in cash flow forecasts (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="f863a-104">Externe Daten können eingegeben oder in Cashflow-Planungen importiert werden.</span><span class="sxs-lookup"><span data-stu-id="f863a-104">External data can be entered or imported into cash flow forecasts.</span></span> <span data-ttu-id="f863a-105">In diesem Thema werden die Einrichtungsschritte beschrieben, die für die Verwendung externer Daten spezifisch sind und die es ermöglichen, die externen Daten in eine Cashflow-Planung aufzunehmen.</span><span class="sxs-lookup"><span data-stu-id="f863a-105">This topic describes the setup steps that are specific to the use of external data and that enable the external data to be included in a cash flow forecast.</span></span>

## <a name="external-data-setup"></a><span data-ttu-id="f863a-106">Externe Daten einrichten</span><span class="sxs-lookup"><span data-stu-id="f863a-106">External data setup</span></span>

<span data-ttu-id="f863a-107">Verwenden Sie die **Externe Quelle**-Registerkarte auf der **Einrichtung der Cashflow-Planung**-Seite (**Bargeld- und Bankverwaltung \> Cashflow-Planung**), um Einstellungen einzugeben, die die Verwendung externer Daten in Cashflow-Planungen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="f863a-107">Use the **External source** tab on the **Cash flow forecast setup** page (**Cash and bank management \> Cash flow forecasting**) to enter settings that support the use of external data in cash flow forecasts.</span></span>

<span data-ttu-id="f863a-108">Weitere Informationen zum Einrichten finden Sie unter [Cashflow-Planung](../cash-bank-management/cash-flow-forecasting.md).</span><span class="sxs-lookup"><span data-stu-id="f863a-108">For more information about the setup, see [Cash flow forecasting](../cash-bank-management/cash-flow-forecasting.md).</span></span>

<span data-ttu-id="f863a-109">Um externe Daten für Cashflow-Planungen einzugeben, können Sie die Erfahrung zum Öffnen in Excel zum Eingeben und Ändern externer Daten verwenden.</span><span class="sxs-lookup"><span data-stu-id="f863a-109">To enter external data for cash flow forecasts, you can use the Open in Excel experience for entering and modifying external data.</span></span> <span data-ttu-id="f863a-110">Wählen Sie die Schaltfläche **Externe Daten** und dann entweder **Externe Daten hinzufügen** oder **Vorhandene externe Daten bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="f863a-110">Select the **External data** button, and then select either **Add External Data** or **Edit existing external data**.</span></span> <span data-ttu-id="f863a-111">Wenn die Microsoft Excel-Datei geöffnet ist, können Sie Informationen in die folgenden Felder eingeben:</span><span class="sxs-lookup"><span data-stu-id="f863a-111">When the Microsoft Excel file is opened, you can enter information in the following fields:</span></span>

- <span data-ttu-id="f863a-112">**Eintragskennung**</span><span class="sxs-lookup"><span data-stu-id="f863a-112">**Entry ID**</span></span>
- <span data-ttu-id="f863a-113">**Beschreibung** (optional)</span><span class="sxs-lookup"><span data-stu-id="f863a-113">**Description** (optional)</span></span>
- <span data-ttu-id="f863a-114">**Name der externen Quelle** – Wählen Sie einen der Werte in der Liste aus, die Sie beim Einrichten von Finance Insights definiert haben.</span><span class="sxs-lookup"><span data-stu-id="f863a-114">**External Source name** – Select one of the values in the list that you defined when you set up Finance Insights.</span></span>
- <span data-ttu-id="f863a-115">**Juristische Person**</span><span class="sxs-lookup"><span data-stu-id="f863a-115">**Legal Entity**</span></span>
- <span data-ttu-id="f863a-116">**Datum**</span><span class="sxs-lookup"><span data-stu-id="f863a-116">**Date**</span></span>
- <span data-ttu-id="f863a-117">**Betrag in Buchungswährung**</span><span class="sxs-lookup"><span data-stu-id="f863a-117">**Amount in transaction currency**</span></span>
- <span data-ttu-id="f863a-118">**Währungscode**</span><span class="sxs-lookup"><span data-stu-id="f863a-118">**Currency Code**</span></span>
- <span data-ttu-id="f863a-119">**Standarddimension** (Optional)</span><span class="sxs-lookup"><span data-stu-id="f863a-119">**Default Dimension** (optional)</span></span>
- <span data-ttu-id="f863a-120">**Dokumentnummer** (Optional)</span><span class="sxs-lookup"><span data-stu-id="f863a-120">**Document number** (optional)</span></span>
- <span data-ttu-id="f863a-121">**Kontonummer** (Optional)</span><span class="sxs-lookup"><span data-stu-id="f863a-121">**Account number** (optional)</span></span>
- <span data-ttu-id="f863a-122">**Kontoname** (Optional)</span><span class="sxs-lookup"><span data-stu-id="f863a-122">**Account name** (optional)</span></span>

## <a name="importing-external-data-by-using-the-data-management-framework"></a><span data-ttu-id="f863a-123">Importieren externer Daten mithilfe des Datenverwaltungsframeworks</span><span class="sxs-lookup"><span data-stu-id="f863a-123">Importing external data by using the Data Management framework</span></span>

<span data-ttu-id="f863a-124">Sie können externe Daten für Cashflow-Planungen mithilfe des **Datenverwaltung**-Arbeitsbereichs und der Entität namens **Cashflow-Planung – externer Quelleneintrag** importieren.</span><span class="sxs-lookup"><span data-stu-id="f863a-124">You can import external data for cash flow forecasts by using the **Data Management** workspace and the entity that is named **Cash flow forecast external source entry**.</span></span>

<span data-ttu-id="f863a-125">Wenn Sie Einrichtungsdaten von einer Umgebung in eine andere verschieben müssen, steht außerdem der folgende Entitätsbereich für die erforderlichen Einrichtungstabellen zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="f863a-125">Additionally, if you must move setup data from one environment to another, the following entities area available for the setup tables that are required:</span></span>

- <span data-ttu-id="f863a-126">Einrichtung der externen Quelle für Cashflow-Planung</span><span class="sxs-lookup"><span data-stu-id="f863a-126">Cash flow forecast external source setup</span></span>
- <span data-ttu-id="f863a-127">Einrichtung der juristischen Person für externe Quelle für Cashflow-Planung</span><span class="sxs-lookup"><span data-stu-id="f863a-127">Cash flow forecast external source legal entity setup</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
