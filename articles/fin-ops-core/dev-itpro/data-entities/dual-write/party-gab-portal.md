---
title: Verwenden von Power Portal mit dem Partei-Datenmodell
description: In diesem Thema werden die Änderungen an den Power Portal-Webrollen aufgrund des Partei-Datenmodells in Duales Schreiben beschrieben.
author: RamaKrishnamoorthy
ms.date: 03/22/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-22
ms.openlocfilehash: a2ea914344341ee26138e853727c551bdd5d733e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833089"
---
# <a name="using-power-portal-with-the-party-data-model"></a><span data-ttu-id="d2271-103">Verwenden von Power Portal mit dem Partei-Datenmodell</span><span class="sxs-lookup"><span data-stu-id="d2271-103">Using Power Portal with the Party data model</span></span>

[!INCLUDE[banner](../../includes/banner.md)]

[!INCLUDE[rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="d2271-104">Die Duales Schreiben-Anwendungsorchestrierungslösung, Version 2.0.999.0 und höher enthält Änderungen des Datenmodells an Partei und globalem Adressbuch für die Konto- und Kontakttabellen.</span><span class="sxs-lookup"><span data-stu-id="d2271-104">The Dual-write application orchestration solution version 2.0.999.0 and later includes data model changes to party and global address book for the Account and Contact tables.</span></span> <span data-ttu-id="d2271-105">Die Änderungen ermöglichen Viele-zu-Viele-Beziehungen, die erweiterte Geschäftsszenarien unterstützen.</span><span class="sxs-lookup"><span data-stu-id="d2271-105">The changes allow many-to-many relationships that support advanced business scenarios.</span></span> <span data-ttu-id="d2271-106">Diese Änderungen werden von Portal-Webrollen, einschließlich des Kundenportals, nicht unterstützt, die standardmäßig ausgeliefert wurden oder in Ihrer Umgebung vorhanden waren, bevor Sie Duales Schreiben installiert haben.</span><span class="sxs-lookup"><span data-stu-id="d2271-106">These changes are not supported by portal web roles, including the customer portal, that are shipped out-of-the-box or that existed in your environment before you installed dual-write.</span></span> <span data-ttu-id="d2271-107">Damit die Webrollen wie erwartet funktionieren, müssen Sie mithilfe des neuen Datenmodells neue Webrollen erstellen.</span><span class="sxs-lookup"><span data-stu-id="d2271-107">For the web roles to work as expected, you need to create new web roles using the new data model.</span></span> 

<span data-ttu-id="d2271-108">Zusammenfassend hat sich die Art und Weise, wie die Tabellen interagieren, geändert, aber die Tabellenberechtigungen im Kundenportal haben sich nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="d2271-108">In summary, the way the tables interact has changed, but the table permissions in the customer portal haven't changed.</span></span> <span data-ttu-id="d2271-109">In diesem Thema wird erläutert, wie Sie neue Webrollen erstellen, die mit dem neuen erweiterten Datenmodell funktionieren.</span><span class="sxs-lookup"><span data-stu-id="d2271-109">This topic explains how to create new web roles that work with the new advanced data model.</span></span>

<span data-ttu-id="d2271-110">Dieses Diagramm zeigt die Tabellenbeziehung **ohne** das Datenmodell der Partei und des globalen Adressbuchs:</span><span class="sxs-lookup"><span data-stu-id="d2271-110">This diagram shows the table relationship **without** the party and global address book data model:</span></span>

   ![ohne Parteimodell](media/without-party-model.PNG)

<span data-ttu-id="d2271-112">Dieses Diagramm zeigt die Tabellenbeziehung **mit** dem Datenmodell der Partei und des globalen Adressbuchs:</span><span class="sxs-lookup"><span data-stu-id="d2271-112">This diagram shows the table relationship **with** the party and global address book data model:</span></span>

   ![mit Parteimodell](media/with-party-model.png)

## <a name="create-a-new-table-permission"></a><span data-ttu-id="d2271-114">Erstellen einer neuen Tabellenberechtigung</span><span class="sxs-lookup"><span data-stu-id="d2271-114">Create a new table permission</span></span>

<span data-ttu-id="d2271-115">Gehen Sie folgendermaßen vor, um diese neuen Tabellenberechtigungen zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="d2271-115">To create these new table permissions, follow these steps:</span></span>

1. <span data-ttu-id="d2271-116">Melden Sie sich bei [Power Apps](https://make.powerapps.com) an und gehen Sie zu Ihren Apps.</span><span class="sxs-lookup"><span data-stu-id="d2271-116">Sign in to [Power Apps](https://make.powerapps.com), and go to your apps.</span></span>
2. <span data-ttu-id="d2271-117">Wählen Sie Ihre Portal Management-App aus.</span><span class="sxs-lookup"><span data-stu-id="d2271-117">Select your Portal Management app.</span></span>
3. <span data-ttu-id="d2271-118">Wählen Sie in der Seitenleiste **Sicherheit > Tabellenberechtigungen** aus.</span><span class="sxs-lookup"><span data-stu-id="d2271-118">In the side bar, select **Security > Table permissions**.</span></span>

    <span data-ttu-id="d2271-119">Sie müssen drei neue Berechtigungen erstellen:</span><span class="sxs-lookup"><span data-stu-id="d2271-119">You must create three new permissions:</span></span>

    + <span data-ttu-id="d2271-120">Kontakt-zu-Partei-Verbindung</span><span class="sxs-lookup"><span data-stu-id="d2271-120">Contact to Party connection</span></span>
    + <span data-ttu-id="d2271-121">Partei-zu-Konto-Verbindung</span><span class="sxs-lookup"><span data-stu-id="d2271-121">Party to Account connection</span></span>
    + <span data-ttu-id="d2271-122">Konto-zu-Auftrag-Verbindung</span><span class="sxs-lookup"><span data-stu-id="d2271-122">Account to Order connection</span></span>

4. <span data-ttu-id="d2271-123">Erstellen und speichern Sie eine neue Berechtigung für die Kontakt-zu-Partei-Verbindung, indem Sie die folgenden Parameter festlegen:</span><span class="sxs-lookup"><span data-stu-id="d2271-123">Create and save a new permission for the Contact to Party connection, setting these parameters:</span></span>

    + <span data-ttu-id="d2271-124">**Name**: Partei-zu-Konto-Verbindung (oder Ihre Wahl)</span><span class="sxs-lookup"><span data-stu-id="d2271-124">**Name**: Party to Account Connection (or your choice)</span></span>
    + <span data-ttu-id="d2271-125">**Tabellenname**: msdyn_contactforparty</span><span class="sxs-lookup"><span data-stu-id="d2271-125">**Table Name**: msdyn_contactforparty</span></span>
    + <span data-ttu-id="d2271-126">**Website**: Kundenportal</span><span class="sxs-lookup"><span data-stu-id="d2271-126">**Website**: Customer Portal</span></span>
    + <span data-ttu-id="d2271-127">**Umfang**: Kontakt</span><span class="sxs-lookup"><span data-stu-id="d2271-127">**Scope**: Contact</span></span>
    + <span data-ttu-id="d2271-128">**Rechte**: Alles auswählen</span><span class="sxs-lookup"><span data-stu-id="d2271-128">**Privileges**: Select all</span></span>
    + <span data-ttu-id="d2271-129">**Webrollen**: Authentifizierte Benutzer, Kundenvertreter (oder Ihre Wahl)</span><span class="sxs-lookup"><span data-stu-id="d2271-129">**Web roles**: Authenticated Users, Customer Representative (or your choice)</span></span>

5. <span data-ttu-id="d2271-130">Erstellen und speichern Sie eine neue Berechtigung für die Partei-zu-Konto-Verbindung, indem Sie die folgenden Parameter festlegen:</span><span class="sxs-lookup"><span data-stu-id="d2271-130">Create and save a new permission for the Party to Account connection, setting these parameters:</span></span>

    + <span data-ttu-id="d2271-131">**Name**: Partei-zu-Konto-Verbindung (oder Ihre Wahl)</span><span class="sxs-lookup"><span data-stu-id="d2271-131">**Name**: Party to Account Connection (or your choice)</span></span>
    + <span data-ttu-id="d2271-132">**Tabellenname**: Konto</span><span class="sxs-lookup"><span data-stu-id="d2271-132">**Table Name**: account</span></span>
    + <span data-ttu-id="d2271-133">**Website**: Kundenportal</span><span class="sxs-lookup"><span data-stu-id="d2271-133">**Website**: Customer Portal</span></span>
    + <span data-ttu-id="d2271-134">**Umfang**: Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="d2271-134">**Scope**: Parent</span></span>
    + <span data-ttu-id="d2271-135">**Rechte**: Alles auswählen</span><span class="sxs-lookup"><span data-stu-id="d2271-135">**Privileges**: Select all</span></span>
    + <span data-ttu-id="d2271-136">**Berechtigung für übergeordnete Tabelle**: Kontakt-zu-Partei-Verbindung</span><span class="sxs-lookup"><span data-stu-id="d2271-136">**Parent Table Permission**: Contact to Party Connection</span></span>

6. <span data-ttu-id="d2271-137">Erstellen und speichern Sie eine neue Berechtigung für die Konto-zu-Auftrag-Verbindung, indem Sie die folgenden Parameter festlegen:</span><span class="sxs-lookup"><span data-stu-id="d2271-137">Create and save a new permission for the Account to Order connection, setting these parameters:</span></span>

    + <span data-ttu-id="d2271-138">**Name**: Konto-zu-Auftrag-Verbindung (oder Ihre Wahl)</span><span class="sxs-lookup"><span data-stu-id="d2271-138">**Name**: Account to Order Connection (or your choice)</span></span>
    + <span data-ttu-id="d2271-139">**Tabellenname**: salesorder</span><span class="sxs-lookup"><span data-stu-id="d2271-139">**Table Name**: salesorder</span></span>
    + <span data-ttu-id="d2271-140">**Website**: Kundenportal</span><span class="sxs-lookup"><span data-stu-id="d2271-140">**Website**: Customer Portal</span></span>
    + <span data-ttu-id="d2271-141">**Umfang**: Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="d2271-141">**Scope**: Parent</span></span>
    + <span data-ttu-id="d2271-142">**Rechte**: Alles auswählen</span><span class="sxs-lookup"><span data-stu-id="d2271-142">**Privileges**: Select all</span></span>
    + <span data-ttu-id="d2271-143">**Berechtigung für übergeordnete Tabelle**: Partei-zu-Konto-Verbindung</span><span class="sxs-lookup"><span data-stu-id="d2271-143">**Parent Table Permission**: Party to Account Connection</span></span>

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
