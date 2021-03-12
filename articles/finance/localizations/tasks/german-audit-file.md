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
ms.search.region: Germany
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8eaf87d63c2991a9c1ed4aace58b588adaa5bca4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988293"
---
# <a name="generate-german-audit-file"></a><span data-ttu-id="1c6f3-103">Generieren Sie deutsche Protokolldatei</span><span class="sxs-lookup"><span data-stu-id="1c6f3-103">Generate German audit file</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1c6f3-104">Im folgenden Verfahren sehen Sie, wie die deutsche Protokolldatei generiert wird.</span><span class="sxs-lookup"><span data-stu-id="1c6f3-104">This procedure shows how to generate the German audit file.</span></span> <span data-ttu-id="1c6f3-105">Diese Aufgabe wurde mithilfe des Demodatenunternehmens DEMF erstellt, mit "Deutschland" als Land/Region für die primäre Adresse für die juristischen Person.</span><span class="sxs-lookup"><span data-stu-id="1c6f3-105">This procedure was created using the demo data company DEMF with Germany as the country/region of legal entity primary address.</span></span>

1. <span data-ttu-id="1c6f3-106">Wechseln Sie zu "Hauptbuch" > "Periodische Aufgaben" > "Datenexport".</span><span class="sxs-lookup"><span data-stu-id="1c6f3-106">Go to General ledger > Periodic tasks > Data export.</span></span>
2. <span data-ttu-id="1c6f3-107">Geben Sie im Feld "Artikelnummer" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="1c6f3-107">In the Format mapping field, enter or select a value.</span></span>
    - <span data-ttu-id="1c6f3-108">Wenn die Liste leer ist, bedeutet dies, dass es kein deutsches Protokolldateiexportformat und keine aktive Debitorenzahlungs-Exportformatkonfiguration gibt.</span><span class="sxs-lookup"><span data-stu-id="1c6f3-108">If the list is empty, it means that there is no German audit file export format configuration imported and active.</span></span> <span data-ttu-id="1c6f3-109">Sie müssen eine deutsche Protokolldateiexportformatkonfiguration importieren, bevor Sie den Vorgang fortsetzen können.</span><span class="sxs-lookup"><span data-stu-id="1c6f3-109">You must import a German audit file export format configuration before you can continue.</span></span>  
3. <span data-ttu-id="1c6f3-110">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="1c6f3-110">Click OK.</span></span>
4. <span data-ttu-id="1c6f3-111">Geben Sie im Feld "Kommentar" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="1c6f3-111">In the Comment field, type a value.</span></span>
5. <span data-ttu-id="1c6f3-112">Geben Sie im Feld "Medien" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="1c6f3-112">In the Media field, type a value.</span></span>
6. <span data-ttu-id="1c6f3-113">Geben Sie im Feld "Version" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="1c6f3-113">In the Version field, type a value.</span></span>
7. <span data-ttu-id="1c6f3-114">Geben Sie im Feld "Tabellengruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="1c6f3-114">In the Table Group field, enter or select a value.</span></span>
    - <span data-ttu-id="1c6f3-115">Wählen Sie beispielsweise "Kunden", um den Masterdaten und Transaktionen von Debitoren zu buchen.</span><span class="sxs-lookup"><span data-stu-id="1c6f3-115">For example, select 'Kunden' to export customer master data and transactions.</span></span>  
8. <span data-ttu-id="1c6f3-116">Geben Sie ein Datum in das Feld "Periode - Von Datum" ein.</span><span class="sxs-lookup"><span data-stu-id="1c6f3-116">In the Period - date from field, enter a date.</span></span>
9. <span data-ttu-id="1c6f3-117">Geben Sie in das Feld "Periode - Bis Datum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="1c6f3-117">In the Period - date to field, enter a date.</span></span>
10. <span data-ttu-id="1c6f3-118">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="1c6f3-118">Click OK.</span></span>

