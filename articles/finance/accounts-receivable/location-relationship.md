---
title: Standort- und Parteibeziehungstypen hinzufügen
description: In diesem Thema wird erläutert, wie Sie neue Standort- und Parteibeziehungstypen hinzufügen.
author: ShivamPandey-msft
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-05-02
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 71e4c8ad122bc52103bda04144222785e9a059f8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817244"
---
# <a name="add-location-and-party-relationship-types"></a><span data-ttu-id="141e3-103">Standort- und Parteibeziehungstypen hinzufügen</span><span class="sxs-lookup"><span data-stu-id="141e3-103">Add location and party relationship types</span></span> 

[!include [banner](../includes/banner.md)]

## <a name="add-location-roles"></a><span data-ttu-id="141e3-104">Lagerplatzrollen hinzufügen</span><span class="sxs-lookup"><span data-stu-id="141e3-104">Add location roles</span></span>

<span data-ttu-id="141e3-105">Es gibt zwei Möglichkeiten, neue Standortrollen für Adress- und Kontaktinformationen hinzuzufügen:</span><span class="sxs-lookup"><span data-stu-id="141e3-105">There are two ways to add a new location roles for address and contact information:</span></span>

-  <span data-ttu-id="141e3-106">Fügen Sie es über die Seite **Adresse und Kontaktinformationen** hinzu.</span><span class="sxs-lookup"><span data-stu-id="141e3-106">Add it through the **Address and contact information purpose** page.</span></span> <span data-ttu-id="141e3-107">Die neue Rolle wird in der Tabelle **LogisticsLocationRole** mit Typ = 0 gespeichert, was bedeutet, dass die Rolle keine Systemrolle ist, die in der **LogisticsLocationRoleType** Enumeration und ihren Erweiterungen definiert ist.</span><span class="sxs-lookup"><span data-stu-id="141e3-107">The new role will be saved to the **LogisticsLocationRole** table with type = 0, which indicates that the role is not a system role defined in the **LogisticsLocationRoleType** enum and its extensions.</span></span> <span data-ttu-id="141e3-108">Ein Benutzer kann diese Rolle bei der Erstellung von Adress- oder Kontaktinformationen verwenden.</span><span class="sxs-lookup"><span data-stu-id="141e3-108">A user will be able to use this role when creating address or contact information.</span></span>

    ![Zweck der Adress- und Inhaltsinformationen](media/Address-Contact.PNG)

-  <span data-ttu-id="141e3-110">Fügen Sie diese der Enumerationserweiterung **LogisticsLocationRoleType** hinzu und lassen Sie es über den Datenbanksynchronisierungsprozess auffüllen.</span><span class="sxs-lookup"><span data-stu-id="141e3-110">Add it to the **LogisticsLocationRoleType** enum extension, and let it populate through the database sync process.</span></span>

    1.  <span data-ttu-id="141e3-111">Erstellen Sie eine Erweiterung zur **LogisticsLocationRoleType** Enumeration und fügen Sie dann die neue Rolle der Erweiterung hinzu.</span><span class="sxs-lookup"><span data-stu-id="141e3-111">Create an extension to the **LogisticsLocationRoleType** enum and add the new role in the extension.</span></span> 
  
        ![Erweiterung zu LogisticsLocationRoleType Enum](media/Logistics.PNG)

    2. <span data-ttu-id="141e3-113">Erstellen Sie eine neue Ressourcendatei für die neue Rolle und weisen Sie anschließend einen Wert für deren Eigenschaften zu.</span><span class="sxs-lookup"><span data-stu-id="141e3-113">Create a new resource file for the new role, and then assign a value for its properties.</span></span>
     
     ![Neue Ressourcendatei](media/Resource.PNG)
        
    3.  <span data-ttu-id="141e3-115">Erstellen Sie eine Datenenauffüllungsklasse und stellen Sie eine Handlermethode zur Verfügung, um die neue Rolle zu füllen.</span><span class="sxs-lookup"><span data-stu-id="141e3-115">Create a data population class and provide a handler method to populate the new role.</span></span> 

        ![Datenauffüllung](media/Dirdata.PNG)

    4.  <span data-ttu-id="141e3-117">Um das Auffüllen der neuen Standortrolle zu testen, können Sie eine lauffähige Klasse erstellen und DirDataPopulation::insertLogisticsLocationRoles() in Main() aufrufen.</span><span class="sxs-lookup"><span data-stu-id="141e3-117">To test populating the new location role, you can create a runnable class, and call DirDataPopulation::insertLogisticsLocationRoles() in Main().</span></span> <span data-ttu-id="141e3-118">Nachdem dieser Vorgang abgeschlossen ist, sollten Sie die neue Rolle in der Tabelle **LogisticsLocationRole** mit dem Typ \> 0 sehen.</span><span class="sxs-lookup"><span data-stu-id="141e3-118">After this process is complete, you should see the new role populated in the **LogisticsLocationRole** table with type \> 0.</span></span> <span data-ttu-id="141e3-119">Die neue Rolle wird auf der Seite **Adresse und Kontaktinformationen** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="141e3-119">The new role will display on the **Address and contact information purpose** page.</span></span>

        ![Neuen Standort einfügen](media/InsertNewLocation.PNG)

## <a name="add-party-relationship-types"></a><span data-ttu-id="141e3-121">Neue Parteibeziehungstypen hinzufügen</span><span class="sxs-lookup"><span data-stu-id="141e3-121">Add party relationship types</span></span> 

<span data-ttu-id="141e3-122">Es gibt zwei Möglichkeiten, einen neuen Beziehungstyp hinzuzufügen:</span><span class="sxs-lookup"><span data-stu-id="141e3-122">There are two ways to add a new relationship type:</span></span>

-   <span data-ttu-id="141e3-123">Fügen Sie sie über die Seite **Beziehungstypen** hinzu.</span><span class="sxs-lookup"><span data-stu-id="141e3-123">Add it through the **Relationship types** page.</span></span> <span data-ttu-id="141e3-124">Die neue Beziehung wird unter **DirRelationshipTypeTable** mit systemtype = 0 gespeichert.</span><span class="sxs-lookup"><span data-stu-id="141e3-124">The new relationship will be saved to **DirRelationshipTypeTable** with systemtype = 0.</span></span>

    ![Beziehungstypen](media/Relationship.PNG)

-  <span data-ttu-id="141e3-126">Fügen Sie diese der Erweiterung der **DirSystemRelationshipType** Enumeration hinzu und lassen Sie es über den Datenbanksynchronisierungsprozess auffüllen.</span><span class="sxs-lookup"><span data-stu-id="141e3-126">Add it to the extension of the **DirSystemRelationshipType** enum, and let it populate through database sync process.</span></span>

    1.  <span data-ttu-id="141e3-127">Erstellen Sie eine Erweiterung zur **DirSystemRelationshipType** Enumeration und fügen Sie den neuen Beziehungstyp hinzu.</span><span class="sxs-lookup"><span data-stu-id="141e3-127">Create an extension to the **DirSystemRelationshipType** enum and add the new relationship type.</span></span>

    2. <span data-ttu-id="141e3-128">Legen Sie einen Initialisierer für diesen neuen Typ an.</span><span class="sxs-lookup"><span data-stu-id="141e3-128">Create an initializer for this new type.</span></span> <span data-ttu-id="141e3-129">Sie finden mehrere Beispiele im Kerncode, eines davon ist  **DirRelationshipTypeChildInitialize**.</span><span class="sxs-lookup"><span data-stu-id="141e3-129">You can find several examples in the core code, one of them is  **DirRelationshipTypeChildInitialize**.</span></span> <span data-ttu-id="141e3-130">Dies ist eine Initialisierungsklasse für den Parteienbeziehungstyp "Child".</span><span class="sxs-lookup"><span data-stu-id="141e3-130">This is an initializer class for party relationship type “Child”.</span></span> <span data-ttu-id="141e3-131">Sie können mit Ihrem Initializer beginnen, indem Sie diesen Code kopieren und einfügen und dann die markierten Bereiche aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="141e3-131">You can start with your initializer by copying and pasting this code and then update the highlighted areas.</span></span>
    
    ![DirRelationshipChild Initialisierer](media/DirRelationship.PNG)

    3.  <span data-ttu-id="141e3-133">Um das Auffüllen des neuen Beziehungstyps zu testen, können Sie eine lauffähige Klasse erstellen und DirDataPopulation::insertDirRelationshipTypes() in Main() aufrufen.</span><span class="sxs-lookup"><span data-stu-id="141e3-133">To test populating the new relationship type, you can create a runnable class, and call DirDataPopulation::insertDirRelationshipTypes() in Main().</span></span> <span data-ttu-id="141e3-134">Sie sollten den neuen Beziehungstyp in der **DirRelationshipTypeTable** sehen, und der neue Beziehungstyp wird auf der Seite **Beziehungstypen** verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="141e3-134">You should see the new relationship type in the **DirRelationshipTypeTable**, and the new relationship type will be available on the **Relationship types** page.</span></span>

        ![Ausführbare Klasse](media/Runnable.PNG)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]