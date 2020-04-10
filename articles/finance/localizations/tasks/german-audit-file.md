---
title: Generieren Sie deutsche Protokolldatei
description: Diese Prozedur führt Sie durch das Generieren einer deutschen Protokolldatei.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Germany
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a93b89627b95a4a6343a88efb1487351fe69927b
ms.sourcegitcommit: b92c3e1b3403d0455fc4e0bf9132d6bc0d7aba5e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3139006"
---
# <a name="generate-german-audit-file"></a><span data-ttu-id="f28fe-103">Generieren Sie deutsche Protokolldatei</span><span class="sxs-lookup"><span data-stu-id="f28fe-103">Generate German audit file</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f28fe-104">Im folgenden Verfahren sehen Sie, wie die deutsche Protokolldatei generiert wird.</span><span class="sxs-lookup"><span data-stu-id="f28fe-104">This procedure shows how to generate the German audit file.</span></span> <span data-ttu-id="f28fe-105">Diese Aufgabe wurde mithilfe des Demodatenunternehmens DEMF erstellt, mit "Deutschland" als Land/Region für die primäre Adresse für die juristischen Person.</span><span class="sxs-lookup"><span data-stu-id="f28fe-105">This procedure was created using the demo data company DEMF with Germany as the country/region of legal entity primary address.</span></span>

1. <span data-ttu-id="f28fe-106">Wechseln Sie zu "Hauptbuch" > "Periodische Aufgaben" > "Datenexport".</span><span class="sxs-lookup"><span data-stu-id="f28fe-106">Go to General ledger > Periodic tasks > Data export.</span></span>
2. <span data-ttu-id="f28fe-107">Geben Sie im Feld "Artikelnummer" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="f28fe-107">In the Format mapping field, enter or select a value.</span></span>
    - <span data-ttu-id="f28fe-108">Wenn die Liste leer ist, bedeutet dies, dass es kein deutsches Protokolldateiexportformat und keine aktive Debitorenzahlungs-Exportformatkonfiguration gibt.</span><span class="sxs-lookup"><span data-stu-id="f28fe-108">If the list is empty, it means that there is no German audit file export format configuration imported and active.</span></span> <span data-ttu-id="f28fe-109">Sie müssen eine deutsche Protokolldateiexportformatkonfiguration importieren, bevor Sie den Vorgang fortsetzen können.</span><span class="sxs-lookup"><span data-stu-id="f28fe-109">You must import a German audit file export format configuration before you can continue.</span></span>  
3. <span data-ttu-id="f28fe-110">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="f28fe-110">Click OK.</span></span>
4. <span data-ttu-id="f28fe-111">Geben Sie im Feld "Kommentar" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="f28fe-111">In the Comment field, type a value.</span></span>
5. <span data-ttu-id="f28fe-112">Geben Sie im Feld "Medien" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="f28fe-112">In the Media field, type a value.</span></span>
6. <span data-ttu-id="f28fe-113">Geben Sie im Feld "Version" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="f28fe-113">In the Version field, type a value.</span></span>
7. <span data-ttu-id="f28fe-114">Geben Sie im Feld "Tabellengruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="f28fe-114">In the Table Group field, enter or select a value.</span></span>
    - <span data-ttu-id="f28fe-115">Wählen Sie beispielsweise "Kunden", um den Masterdaten und Transaktionen von Debitoren zu buchen.</span><span class="sxs-lookup"><span data-stu-id="f28fe-115">For example, select 'Kunden' to export customer master data and transactions.</span></span>  
8. <span data-ttu-id="f28fe-116">Geben Sie ein Datum in das Feld "Periode - Von Datum" ein.</span><span class="sxs-lookup"><span data-stu-id="f28fe-116">In the Period - date from field, enter a date.</span></span>
9. <span data-ttu-id="f28fe-117">Geben Sie in das Feld "Periode - Bis Datum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="f28fe-117">In the Period - date to field, enter a date.</span></span>
10. <span data-ttu-id="f28fe-118">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="f28fe-118">Click OK.</span></span>

