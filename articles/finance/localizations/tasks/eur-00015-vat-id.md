---
title: EUR-00015 Einrichtung der MwSt Kennung
description: Diese Verfahren zeigt die MwSt.-ID-Erfassungsvoraussetzungen, z. B. das Einrichten eines Erfassungstyps und Zuweisen zu einer Erfassungskategorie.
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxRegistrationType, TaxRegistrationTypeCreate, TaxRegistrationLegislationTypes
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 127e6caf6a6273df36f580b32fa81219b88b8a29
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183543"
---
# <a name="eur-00015-set-up-vat-id"></a><span data-ttu-id="227a6-103">EUR-00015 Einrichtung der MwSt Kennung</span><span class="sxs-lookup"><span data-stu-id="227a6-103">EUR-00015 Set up VAT ID</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="227a6-104">Diese Verfahren zeigt die MwSt.-ID-Erfassungsvoraussetzungen, z. B. das Einrichten eines Erfassungstyps und Zuweisen zu einer Erfassungskategorie.</span><span class="sxs-lookup"><span data-stu-id="227a6-104">This procedure walks you through VAT ID registration prerequisites, such as setting up a registration type and assigning it to a registration category.</span></span> <span data-ttu-id="227a6-105">Zusätzliche Informationen zu Erfassungskennungen und der Verarbeitung von Erfassungskennung, einschließlich der erforderlichen Voraussetzungen, finden Sie im Hilfethema "Erfassungs-IDs".</span><span class="sxs-lookup"><span data-stu-id="227a6-105">You can find additional information about registration IDs and registration ID processing, including required prerequisites, in the Registration IDs help topic.</span></span> 

<span data-ttu-id="227a6-106">Diese Informationen gelten für alle europäischen Länder/Regionen.</span><span class="sxs-lookup"><span data-stu-id="227a6-106">The information here applies to all European countries/regions.</span></span> <span data-ttu-id="227a6-107">Diese Aufgabe wurde mithilfe des Demodatenunternehmens DEMF mit der primären Adresse einer juristischen Person in Deutschland erstellt.</span><span class="sxs-lookup"><span data-stu-id="227a6-107">The task was created using the demo data company DEMF with Germany as the legal entity primary address.</span></span> <span data-ttu-id="227a6-108">Diese Aufgabe richtet sich an Systemadministratoren.</span><span class="sxs-lookup"><span data-stu-id="227a6-108">This task is intended for system administrators.</span></span> <span data-ttu-id="227a6-109">Diese Prozedur ist eine Funktion, für die in Dynamics 365 for Operations Version 1611 hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="227a6-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="227a6-110">Navigieren zur Organisationsverwaltung > Globales Adressbuch > Erfassungstypen > Erfassungstypen.</span><span class="sxs-lookup"><span data-stu-id="227a6-110">Go to Organization administration > Global address book > Registration types > Registration types.</span></span>
2. <span data-ttu-id="227a6-111">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="227a6-111">Click New to open the drop dialog.</span></span>
3. <span data-ttu-id="227a6-112">Geben Sie im Feld Name "MwSt.-ID" ein.</span><span class="sxs-lookup"><span data-stu-id="227a6-112">In the Name field, type 'VAT ID'.</span></span>
4. <span data-ttu-id="227a6-113">Geben Sie im Feld "Beschreibung "MwSt.-Nummer" ein.</span><span class="sxs-lookup"><span data-stu-id="227a6-113">In the Description field, VAT number.</span></span>
5. <span data-ttu-id="227a6-114">Wählen Sie im Feld Name/Region "DEU" aus oder geben Sie einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="227a6-114">In the Country/region field, enter or select a value DEU</span></span>
6. <span data-ttu-id="227a6-115">Wählen Sie "Ja" im Feld "Eindeutig".</span><span class="sxs-lookup"><span data-stu-id="227a6-115">Select Yes in the Unique field.</span></span>
    * <span data-ttu-id="227a6-116">Aktivieren Sie dieses Kontrollkästchen, um sicherzustellen, das die Mehrwertsteuerkennung eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="227a6-116">Select this check box to verify if the VAT ID is unique.</span></span>  
7. <span data-ttu-id="227a6-117">Wählen Sie "Ja" im Feld "Primär für Land".</span><span class="sxs-lookup"><span data-stu-id="227a6-117">Select Yes in the Primary for country field.</span></span>
    * <span data-ttu-id="227a6-118">Aktivieren Sie dieses Kontrollkästchen, wenn die Mehrwertsteuer-ID für alle Adressen gültig ist, die zum angegebenen Land/Region gehören.</span><span class="sxs-lookup"><span data-stu-id="227a6-118">Select this check box if the VAT ID should be effective for all addresses belonging to the specified country/region.</span></span>  
8. <span data-ttu-id="227a6-119">Klicken Sie auf "Erstellen".</span><span class="sxs-lookup"><span data-stu-id="227a6-119">Click Create.</span></span>
9. <span data-ttu-id="227a6-120">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="227a6-120">Click Add.</span></span>
10. <span data-ttu-id="227a6-121">Wählen Sie im Feld Name/Region "ITA" aus oder geben Sie einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="227a6-121">In the Country/region field, enter or select a value ITA</span></span>
11. <span data-ttu-id="227a6-122">Geben Sie im Feld 'Format' den Wert '###########' ein.</span><span class="sxs-lookup"><span data-stu-id="227a6-122">In the Format field, type '###########'.</span></span>
    * <span data-ttu-id="227a6-123">Wenn Sie einer Erfassungskennung dieses Typs für das ausgewählte Land/Region eingeben, wird die Erfassungskennung gegen dieses Format geprüft.</span><span class="sxs-lookup"><span data-stu-id="227a6-123">When you enter a registration ID of this type for the selected country/region, the registration ID will be verified against this format.</span></span>  
12. <span data-ttu-id="227a6-124">Aktivieren Sie das Kontrollkästchen "Eindeutig".</span><span class="sxs-lookup"><span data-stu-id="227a6-124">Select the Unique check box.</span></span>
    * <span data-ttu-id="227a6-125">Aktivieren Sie dieses Kontrollkästchen, um sicherzustellen, das die Mehrwertsteuerkennung eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="227a6-125">Select this check box to verify if the VAT ID is unique.</span></span>  
13. <span data-ttu-id="227a6-126">Aktivieren Sie das Kontrollkästchen "Primär für Land".</span><span class="sxs-lookup"><span data-stu-id="227a6-126">Select the Primary for country check box.</span></span>
    * <span data-ttu-id="227a6-127">Aktivieren Sie dieses Kontrollkästchen, wenn die Mehrwertsteuer-ID für alle Adressen gültig ist, die zum angegebenen Land/Region gehören.</span><span class="sxs-lookup"><span data-stu-id="227a6-127">Select this check box if the VAT ID should be effective for all addresses belonging to the specified country/region.</span></span>  
14. <span data-ttu-id="227a6-128">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="227a6-128">Click Save.</span></span>
15. <span data-ttu-id="227a6-129">Navigieren zur Organisationsverwaltung > Globales Adressbuch > Erfassungstypen > Erfassungskategorien.</span><span class="sxs-lookup"><span data-stu-id="227a6-129">Go to Organization administration > Global address book > Registration types > Registration categories.</span></span>
16. <span data-ttu-id="227a6-130">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="227a6-130">Click New.</span></span>
17. <span data-ttu-id="227a6-131">Wählen Sie im Feld Name/Region "MwSt.-ID, DEU" aus oder geben Sie einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="227a6-131">In the Country/region field, enter or select a value VAT ID, DEU</span></span>
18. <span data-ttu-id="227a6-132">Wählen Sie im Feld "Registrierungskategorie" die Option "MwSt.-ID" aus.</span><span class="sxs-lookup"><span data-stu-id="227a6-132">In the Registration category field, select 'VAT ID'.</span></span>
    * <span data-ttu-id="227a6-133">Weisen Sie den Journaltyp zu, den Sie eben für eine vordefinierte Erfassungskategorie erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="227a6-133">Assign the registration type that you created earlier to a predefined Registration category.</span></span>  
19. <span data-ttu-id="227a6-134">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="227a6-134">Click New.</span></span>
20. <span data-ttu-id="227a6-135">Wählen Sie im Feld Name/Region "MwSt.-ID, ITA" aus oder geben Sie einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="227a6-135">In the Country/region field, enter or select a value VAT ID, ITA</span></span>
21. <span data-ttu-id="227a6-136">Wählen Sie im Feld "Registrierungskategorie" die Option "MwSt.-ID" aus.</span><span class="sxs-lookup"><span data-stu-id="227a6-136">In the Registration category field, select 'VAT ID'.</span></span>
    * <span data-ttu-id="227a6-137">Weisen Sie den Journaltyp zu, den Sie für eine vordefinierte Erfassungskategorie erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="227a6-137">Assign the registration type that you created to a predefined registration category.</span></span>  
22. <span data-ttu-id="227a6-138">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="227a6-138">Click Save.</span></span>

