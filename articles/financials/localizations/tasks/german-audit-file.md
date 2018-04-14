--- 
title: Protokolldatei generieren (Deutschland)
description: Im folgenden Verfahren sehen Sie, wie die deutsche Protokolldatei generiert wird.
author: mrolecki
manager: AnnBe
ms.date: 02/18/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Germany
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: bcdf4645d6b6f341ed765126eea0d93c9ebe6c86
ms.contentlocale: de-de
ms.lasthandoff: 04/13/2018

---
# <a name="generate-audit-file-germany"></a><span data-ttu-id="5365e-103">Protokolldatei generieren (Deutschland)</span><span class="sxs-lookup"><span data-stu-id="5365e-103">Generate audit file (Germany)</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5365e-104">Im folgenden Verfahren sehen Sie, wie die deutsche Protokolldatei generiert wird.</span><span class="sxs-lookup"><span data-stu-id="5365e-104">This procedure shows how to generate the German audit file.</span></span> <span data-ttu-id="5365e-105">Diese Aufgabe wurde mithilfe des Demodatenunternehmens DEMF erstellt, mit "Deutschland" als Land/Region für die primäre Adresse für die juristischen Person.</span><span class="sxs-lookup"><span data-stu-id="5365e-105">This procedure was created using the demo data company DEMF with Germany as the country/region of legal entity primary address.</span></span>

1. <span data-ttu-id="5365e-106">Wechseln Sie zu "Hauptbuch" > "Periodische Aufgaben" > "Datenexport".</span><span class="sxs-lookup"><span data-stu-id="5365e-106">Go to General ledger > Periodic tasks > Data export.</span></span>
2. <span data-ttu-id="5365e-107">Geben Sie im Feld "Artikelnummer" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="5365e-107">In the Format mapping field, enter or select a value.</span></span>
    * <span data-ttu-id="5365e-108">Wenn die Liste leer ist, bedeutet dies, dass es kein deutsches Protokolldateiexportformat und keine aktive Debitorenzahlungs-Exportformatkonfiguration gibt.</span><span class="sxs-lookup"><span data-stu-id="5365e-108">If the list is empty, it means that there is no German audit file export format configuration imported and active.</span></span> <span data-ttu-id="5365e-109">Sie müssen eine deutsche Protokolldateiexportformatkonfiguration importieren, bevor Sie den Vorgang fortsetzen können.</span><span class="sxs-lookup"><span data-stu-id="5365e-109">You must import a German audit file export format configuration before you can continue.</span></span>  
3. <span data-ttu-id="5365e-110">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="5365e-110">Click OK.</span></span>
4. <span data-ttu-id="5365e-111">Geben Sie im Feld "Kommentar" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="5365e-111">In the Comment field, type a value.</span></span>
5. <span data-ttu-id="5365e-112">Geben Sie im Feld "Medien" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="5365e-112">In the Media field, type a value.</span></span>
6. <span data-ttu-id="5365e-113">Geben Sie im Feld "Version" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="5365e-113">In the Version field, type a value.</span></span>
7. <span data-ttu-id="5365e-114">Geben Sie im Feld "Tabellengruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="5365e-114">In the Table Group field, enter or select a value.</span></span>
    * <span data-ttu-id="5365e-115">Wählen Sie beispielsweise "Kunden", um den Masterdaten und Transaktionen von Debitoren zu buchen.</span><span class="sxs-lookup"><span data-stu-id="5365e-115">For example, select 'Kunden' to export customer master data and transactions.</span></span>  
8. <span data-ttu-id="5365e-116">Geben Sie ein Datum in das Feld "Periode - Von Datum" ein.</span><span class="sxs-lookup"><span data-stu-id="5365e-116">In the Period - date from field, enter a date.</span></span>
9. <span data-ttu-id="5365e-117">Geben Sie in das Feld "Periode - Bis Datum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="5365e-117">In the Period - date to field, enter a date.</span></span>
10. <span data-ttu-id="5365e-118">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="5365e-118">Click OK.</span></span>


