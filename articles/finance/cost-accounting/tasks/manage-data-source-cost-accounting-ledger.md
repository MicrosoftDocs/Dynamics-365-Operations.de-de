---
title: Eine Datenquelle für das Sachkonto der Kostenrechnung verwalten
description: Verwenden Sie diese Prozedur, um die Hauptbuchdatenquelle für ein Kostenrechnungssachkonto zu verwalten.
author: ShylaThompson
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMAXGeneralLedgerEntryProviderConfiguration
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: da4d351f4bce6494a107a55895866e4d3d43953f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841068"
---
# <a name="manage-a-data-source-for-the-cost-accounting-ledger"></a><span data-ttu-id="cbc82-103">Eine Datenquelle für das Sachkonto der Kostenrechnung verwalten</span><span class="sxs-lookup"><span data-stu-id="cbc82-103">Manage a data source for the cost accounting ledger</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cbc82-104">Verwenden Sie diese Prozedur, um die Hauptbuchdatenquelle für ein Kostenrechnungssachkonto zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="cbc82-104">Use this procedure to manage the general ledger data source for a cost accounting ledger.</span></span> <span data-ttu-id="cbc82-105">Bevor Sie diese Aufgabe abschließen, prüfen Sie, ob Sie ein Kostenrechnungssachkonto den "Erstellen "und" Kostenkontrollesteuereinheits" besetzen Aufgabenleitfäden definieren.</span><span class="sxs-lookup"><span data-stu-id="cbc82-105">Before you complete this task, make sure that you play the "Create a cost accounting ledger" and "Define cost control units" task guides.</span></span> <span data-ttu-id="cbc82-106">Für diese Aufzeichnung wird das Demo-Datenunternehmen USP2 verwendet.</span><span class="sxs-lookup"><span data-stu-id="cbc82-106">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="cbc82-107">Wechseln Sie zu Kostenbuchhaltung > Sachkontoeinstellung > Kostenbuchhaltungs-Sachkonto .</span><span class="sxs-lookup"><span data-stu-id="cbc82-107">Go to Cost accounting > Ledger setup > Cost accounting ledgers.</span></span>
2. <span data-ttu-id="cbc82-108">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="cbc82-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="cbc82-109">Tatsächliche Versionen anklicken.</span><span class="sxs-lookup"><span data-stu-id="cbc82-109">Click Actual versions.</span></span>
4. <span data-ttu-id="cbc82-110">Klicken Sie im Aktivitätsbereich auf Verwalten.</span><span class="sxs-lookup"><span data-stu-id="cbc82-110">On the Action Pane, click Manage.</span></span>
5. <span data-ttu-id="cbc82-111">Hauptbuch anklicken.</span><span class="sxs-lookup"><span data-stu-id="cbc82-111">Click General ledger.</span></span>
6. <span data-ttu-id="cbc82-112">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="cbc82-112">Click New.</span></span>
7. <span data-ttu-id="cbc82-113">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="cbc82-113">In the Name field, type a value.</span></span>
8. <span data-ttu-id="cbc82-114">Geben Sie im Feld Datenanbieter einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="cbc82-114">In the Data provider field, enter or select a value.</span></span>
    * <span data-ttu-id="cbc82-115">Wählen Sie für dieses Beispiel die Option Dynamics 365 Finance - Hauptbucheinträge aus.</span><span class="sxs-lookup"><span data-stu-id="cbc82-115">For this example, select Dynamics 365 Finance - General ledger entries.</span></span>  
9. <span data-ttu-id="cbc82-116">Geben Sie im Feld "Kostenelementdimensionshierarchie" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="cbc82-116">In the Cost element dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="cbc82-117">Wählen Sie für dieses Beispiel die Option "Kostenelemente" aus.</span><span class="sxs-lookup"><span data-stu-id="cbc82-117">For this example, select Cost elements.</span></span>  
10. <span data-ttu-id="cbc82-118">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="cbc82-118">Click Save.</span></span>
11. <span data-ttu-id="cbc82-119">Datenanbieter konfigurieren anklicken.</span><span class="sxs-lookup"><span data-stu-id="cbc82-119">Click Configure data provider.</span></span>
12. <span data-ttu-id="cbc82-120">Geben Sie im Feld „Juristische Person” einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="cbc82-120">In the Legal entity field, enter or select a value.</span></span>
    * <span data-ttu-id="cbc82-121">Wählen Sie für dieses Beispiel "USP2" aus.</span><span class="sxs-lookup"><span data-stu-id="cbc82-121">For this example, select USP2.</span></span>  
13. <span data-ttu-id="cbc82-122">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="cbc82-122">Click New.</span></span>
14. <span data-ttu-id="cbc82-123">Wählen Sie im Feld Buchungsebene Aktuell aus.</span><span class="sxs-lookup"><span data-stu-id="cbc82-123">In the Posting layer field, select Current.</span></span>
15. <span data-ttu-id="cbc82-124">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="cbc82-124">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]