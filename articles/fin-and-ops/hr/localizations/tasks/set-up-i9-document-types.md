--- 
title: I-9-Dokumenttypen einrichten
description: "Im folgenden Verfahren wird dargestellt, wie Dokumenttypen angezeigt und eingerichtet werden, die für die I-9-Überprüfung verwendet werden."
author: ShielaSogge
manager: AnnBe
ms.date: 11/01/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a05fec7b79003d5b98470d85644d70bd1dbac285
ms.openlocfilehash: d3d2f38327ea82ecddf998161edf86bf32e04db0
ms.contentlocale: de-de
ms.lasthandoff: 02/06/2018

---
# <a name="set-up-i-9-document-types"></a><span data-ttu-id="d4955-103">I-9-Dokumenttypen einrichten</span><span class="sxs-lookup"><span data-stu-id="d4955-103">Set up I-9 document types</span></span>

[!include[task guide banner](../../../includes/task-guide-banner.md)]

<span data-ttu-id="d4955-104">Im folgenden Verfahren wird dargestellt, wie Dokumenttypen angezeigt und eingerichtet werden, die für die I-9-Überprüfung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d4955-104">This procedure shows how to view and set up document types that are used for I-9 verification.</span></span> <span data-ttu-id="d4955-105">Bevor Sie I-9-Dokumenttypen einrichten, müssen Sie die ausstellenden Behörden und die Ausweistypen einrichten.</span><span class="sxs-lookup"><span data-stu-id="d4955-105">Before you set up I-9 document types, you must also set up the issuing agencies and identification types.</span></span> <span data-ttu-id="d4955-106">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF. Es enthält Beispiele für ausstellende Stellen und Ausweistypen, die erforderlich sind, um die Verfahren auszuführen.</span><span class="sxs-lookup"><span data-stu-id="d4955-106">The demo data company used to create this procedure is USMF, which includes examples of the issue agencies and identification types that are needed to complete the procedure.</span></span>

1. <span data-ttu-id="d4955-107">Wechseln Sie zu Personalverwaltung > Arbeitskräfte > I-9 > I-9-Dokumenttypen.</span><span class="sxs-lookup"><span data-stu-id="d4955-107">Go to Human resources > Workers > I-9 > I-9 document types.</span></span>
2. <span data-ttu-id="d4955-108">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="d4955-108">Click New.</span></span>
3. <span data-ttu-id="d4955-109">Geben Sie im Feld "I-9-Dokumenttypen" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="d4955-109">In the I-9 document type field, type a value.</span></span>
    * <span data-ttu-id="d4955-110">Beispiel: Schule-ID.</span><span class="sxs-lookup"><span data-stu-id="d4955-110">Example: School ID.</span></span>  
4. <span data-ttu-id="d4955-111">Wählen Sie den Kennungstyp aus.</span><span class="sxs-lookup"><span data-stu-id="d4955-111">Select the identification type.</span></span>  <span data-ttu-id="d4955-112">Beispiel: Schule-ID</span><span class="sxs-lookup"><span data-stu-id="d4955-112">Example:  School ID</span></span>
    * <span data-ttu-id="d4955-113">Beispiele für Identifikationstypen umfassen eine Sozialversicherungsnummer (SSN), Visumsnummer, Personalausweisnummer oder Führerschein.</span><span class="sxs-lookup"><span data-stu-id="d4955-113">Examples of identification types include a Social Security number (SSN), visa number, passport ID, or driver's license.</span></span>  
5. <span data-ttu-id="d4955-114">Wählen Sie die I-9-Dokumentliste aus, die für den Dokumenttyp verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d4955-114">Select the I-9 document list that is used for the document type.</span></span>
    * <span data-ttu-id="d4955-115">Im Rahmen des Prozesses I-9 müssen Mitarbeiter Dokumentation vorweisen, die dem Arbeitgeber ihre Identität und Arbeitsgenehmigung zeigen.</span><span class="sxs-lookup"><span data-stu-id="d4955-115">As part of the I-9 process, employees must present documentation that shows the employer their identity and employment authorization.</span></span> <span data-ttu-id="d4955-116">Auf der Website der U.S. Citizenship and Immigration Services finden Sie Informationen zu den akzeptablen Dokumenten und welcher Liste diese angehören.</span><span class="sxs-lookup"><span data-stu-id="d4955-116">The US Citizenship and Immigration Services website contains information about which documents are acceptable, and which list they belong to.</span></span>  <span data-ttu-id="d4955-117">http://www.uscis.gov</span><span class="sxs-lookup"><span data-stu-id="d4955-117">http://www.uscis.gov</span></span>  
6. <span data-ttu-id="d4955-118">Geben Sie im Feld "Formular" die offizielle Formularnummer für den Dokumenttyp ein.</span><span class="sxs-lookup"><span data-stu-id="d4955-118">In the Form field, Enter the official form number for the document type.</span></span> <span data-ttu-id="d4955-119">Beispiel: Schule-ID.</span><span class="sxs-lookup"><span data-stu-id="d4955-119">Example: School ID.</span></span>
    * <span data-ttu-id="d4955-120">Die offiziellen Formularnummern sind auf der Website der U.S. Citizenship and Immigration Services zu finden.</span><span class="sxs-lookup"><span data-stu-id="d4955-120">The official form numbers can be found on the US Citizenship and Immigration Services website.</span></span>  <span data-ttu-id="d4955-121">http://www.uscis.gov</span><span class="sxs-lookup"><span data-stu-id="d4955-121">http://www.uscis.gov</span></span>  
7. <span data-ttu-id="d4955-122">Aktivieren oder deaktivieren Sie das Kontrollkästchen "Aktiv".</span><span class="sxs-lookup"><span data-stu-id="d4955-122">Check or uncheck the Active checkbox.</span></span>
8. <span data-ttu-id="d4955-123">Legen Sie das Datum "2019-10-27" im Feld "Ablauf" fest.</span><span class="sxs-lookup"><span data-stu-id="d4955-123">In the Expire field, set the date to '2019-10-27'.</span></span>
    * <span data-ttu-id="d4955-124">Das Ablaufdatum ist optional.</span><span class="sxs-lookup"><span data-stu-id="d4955-124">The expiration date is optional.</span></span>  
9. <span data-ttu-id="d4955-125">Wählen Sie die Behörde aus, die den Dokumenttyp ausgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="d4955-125">Select the agency that issued the document type.</span></span> <span data-ttu-id="d4955-126">Beispiel: Feld/Kanton</span><span class="sxs-lookup"><span data-stu-id="d4955-126">Example: Province/territory</span></span>
10. <span data-ttu-id="d4955-127">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="d4955-127">Click Save.</span></span>


