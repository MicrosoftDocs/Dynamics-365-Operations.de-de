---
title: Datenbankprotokollierung konfigurieren und verwalten
description: Sie können Änderungen an Tabellen und Feldern in Dynamics 365 Human Resources mit Datenbankprotokollierung verfolgen.
author: Darinkramer
manager: AnnBe
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3dc4658a0a13af95978c66f5aab882902f754a2d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4418674"
---
# <a name="configure-and-manage-database-logging"></a><span data-ttu-id="9992a-103">Datenbankprotokollierung konfigurieren und verwalten</span><span class="sxs-lookup"><span data-stu-id="9992a-103">Configure and manage database logging</span></span>

<span data-ttu-id="9992a-104">Sie können Änderungen an Tabellen und Feldern in Dynamics 365 Human Resources mit Datenbankprotokollierung verfolgen.</span><span class="sxs-lookup"><span data-stu-id="9992a-104">You can track changes to tables and fields in Dynamics 365 Human Resources with database logging.</span></span> <span data-ttu-id="9992a-105">In diesem Thema wird beschrieben, wie:</span><span class="sxs-lookup"><span data-stu-id="9992a-105">This topic describes how to:</span></span>

- <span data-ttu-id="9992a-106">Verwalten Sie Sicherheit und Leistung für die Datenbankprotokollierung</span><span class="sxs-lookup"><span data-stu-id="9992a-106">Manage security and performance for database logging</span></span>
- <span data-ttu-id="9992a-107">Datenbankprotokollierung einrichten</span><span class="sxs-lookup"><span data-stu-id="9992a-107">Set up database logging</span></span>
- <span data-ttu-id="9992a-108">Bereinigen Sie Datenbankprotokolle</span><span class="sxs-lookup"><span data-stu-id="9992a-108">Clean up database logs</span></span>

## <a name="overview-of-database-logging"></a><span data-ttu-id="9992a-109">Übersicht über die Datenbankprotokollierung</span><span class="sxs-lookup"><span data-stu-id="9992a-109">Overview of database logging</span></span>

<span data-ttu-id="9992a-110">Sie können Änderungen an Tabellen und Feldern in Microsoft Dynamics 365 Human Resources mit Datenbankprotokollierung verfolgen.</span><span class="sxs-lookup"><span data-stu-id="9992a-110">Database logging tracks specific changes to Microsoft Dynamics 365 Human Resources tables and fields.</span></span> <span data-ttu-id="9992a-111">Diese Änderungen umfassen das Einfügen, Aktualisieren oder Löschen.</span><span class="sxs-lookup"><span data-stu-id="9992a-111">These changes include inserting, updating, or deleting.</span></span> <span data-ttu-id="9992a-112">Die Datenbankprotokollierung speichert eine Aufzeichnung der Änderungen an Tabellen oder Feldern in der Datenbankprotokolltabelle.</span><span class="sxs-lookup"><span data-stu-id="9992a-112">Database logging stores a record of changes to tables or fields in the database log table.</span></span>

<span data-ttu-id="9992a-113">Die geschäftlichen Verwendungen der Datenbankprotokollierung umfassen:</span><span class="sxs-lookup"><span data-stu-id="9992a-113">The business uses of database logging include:</span></span>

- <span data-ttu-id="9992a-114">Erstellen eines Überwachungsdatensatzes mit Änderungen an bestimmten Tabellen, die vertrauliche Informationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="9992a-114">Creating an audit record of changes to specific tables that contain sensitive information.</span></span>
- <span data-ttu-id="9992a-115">Verfolgung einzelner Transaktionen.</span><span class="sxs-lookup"><span data-stu-id="9992a-115">Tracking single transactions.</span></span> <span data-ttu-id="9992a-116">Die Datenbankprotokollierung dient nicht zur Verfolgung automatisierter Transaktionen, die in Stapeljobs ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="9992a-116">Database logging isn't intended for tracking automated transactions that run in batch jobs.</span></span>

## <a name="security-for-database-logging"></a><span data-ttu-id="9992a-117">Sicherheit für die Datenbankprotokollierung</span><span class="sxs-lookup"><span data-stu-id="9992a-117">Security for database logging</span></span>

<span data-ttu-id="9992a-118">Datenbankprotokolle können sensible Daten enthalten.</span><span class="sxs-lookup"><span data-stu-id="9992a-118">Database logs can contain sensitive data.</span></span> <span data-ttu-id="9992a-119">Beschränken Sie den Zugriff auf Sicherheitsrollen, die Zugriff auf die Protokolldaten benötigen.</span><span class="sxs-lookup"><span data-stu-id="9992a-119">Limit access to include only security roles that need access to the log data.</span></span>

## <a name="database-logging-and-performance"></a><span data-ttu-id="9992a-120">Datenbankprotokollierung und Leistung</span><span class="sxs-lookup"><span data-stu-id="9992a-120">Database logging and performance</span></span>

<span data-ttu-id="9992a-121">Die Datenbankprotokollierung kann zwar aus geschäftlicher Sicht hilfreich sein, sie kann allerdings auch eine hohe Ressourcenauslastung sowie einen hohen Verwaltungsaufwand bedeuten.</span><span class="sxs-lookup"><span data-stu-id="9992a-121">While valuable from a business perspective, database logging can be expensive in resource use and management.</span></span> <span data-ttu-id="9992a-122">Die Leistungsbeeinträchtigungen der Datenbankprotokollierung umfassen:</span><span class="sxs-lookup"><span data-stu-id="9992a-122">The performance implications of database logging include:</span></span>

- <span data-ttu-id="9992a-123">Die Datenbankprotokolltabelle kann schnell wachsen und die Größe der Datenbank erhöhen.</span><span class="sxs-lookup"><span data-stu-id="9992a-123">The database log table can grow quickly and cause an increase in the size of the database.</span></span> <span data-ttu-id="9992a-124">Das Wachstum hängt von der Menge der protokollierten Daten ab, die Sie behalten möchten.</span><span class="sxs-lookup"><span data-stu-id="9992a-124">Growth depends on the amount of logged data that you decide to keep.</span></span> <span data-ttu-id="9992a-125">Standardmäßig verwaltet die Datenbankprotokolltabelle nur 30 Tage Protokolldaten.</span><span class="sxs-lookup"><span data-stu-id="9992a-125">By default, the database log table maintains only 30 days of log data.</span></span> 

- <span data-ttu-id="9992a-126">Die Datenbankprotokollierung kann sich nachteilig auf lang laufende automatisierte Prozesse auswirken, z. B. auf lang laufende Datenimporte.</span><span class="sxs-lookup"><span data-stu-id="9992a-126">Database logging can adversely affect long-running automated processes, such as long-running data imports.</span></span>

### <a name="best-practices"></a><span data-ttu-id="9992a-127">Optimale Verfahren</span><span class="sxs-lookup"><span data-stu-id="9992a-127">Best practices</span></span>

<span data-ttu-id="9992a-128">Wählen Sie zum Eingrenzen der Anzahl von Protokolleinträgen und zur Steigerung der Leistung nur die jeweils gewünschten Felder für die Protokollierung und keine vollständigen Tabellen aus.</span><span class="sxs-lookup"><span data-stu-id="9992a-128">To improve performance, limit log entries by selecting specific fields to log instead of whole tables.</span></span> <span data-ttu-id="9992a-129">Um die Gesamtleistung aufrechtzuerhalten, ist die Datenbankprotokollierung auf 20 Tabellen beschränkt.</span><span class="sxs-lookup"><span data-stu-id="9992a-129">To help maintain overall performance, database logging is limited to 20 tables.</span></span>

> [!NOTE]
> <span data-ttu-id="9992a-130">Für einzelne Feldern können nur Aktualisierungen protokolliert werden.</span><span class="sxs-lookup"><span data-stu-id="9992a-130">Only updates can be logged for individual fields.</span></span>

## <a name="set-up-database-logging"></a><span data-ttu-id="9992a-131">Datenbankprotokollierung einrichten</span><span class="sxs-lookup"><span data-stu-id="9992a-131">Set up database logging</span></span>

<span data-ttu-id="9992a-132">Sie können den Assistent **Protokollieren von Datenbankänderungen** zum Einrichten der Datenbankprotokollierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="9992a-132">You can use the **Logging database changes** wizard to set up database logging.</span></span> <span data-ttu-id="9992a-133">Der Assistent bietet eine flexible Möglichkeit, die Protokollierung für Tabellen oder Felder einzurichten.</span><span class="sxs-lookup"><span data-stu-id="9992a-133">The wizard provides a flexible way to set up logging for tables or fields.</span></span>

1. <span data-ttu-id="9992a-134">Gehen Sie zu **Systemadministration> Links> Datenbank> Datenbankprotokoll einrichten**.</span><span class="sxs-lookup"><span data-stu-id="9992a-134">Go to **System administration > Links > Database > Database log setup**.</span></span> <span data-ttu-id="9992a-135">Wählen Sie **Neu** aus, um den Assistent **Protokollieren von Datenbankänderungen** zu starten.</span><span class="sxs-lookup"><span data-stu-id="9992a-135">Select **New** to start the **Logging database changes** wizard.</span></span>
2. <span data-ttu-id="9992a-136">Schließen Sie den Assistenten ab.</span><span class="sxs-lookup"><span data-stu-id="9992a-136">Complete the wizard.</span></span>

## <a name="clean-up-database-logs"></a><span data-ttu-id="9992a-137">Bereinigen Sie Datenbankprotokolle</span><span class="sxs-lookup"><span data-stu-id="9992a-137">Clean up database logs</span></span>

<span data-ttu-id="9992a-138">Sie können alle oder einen Teil der Datenbankprotokolle mit den folgenden Optionen löschen:</span><span class="sxs-lookup"><span data-stu-id="9992a-138">You can delete all or part of the database logs, using the following options:</span></span>

- <span data-ttu-id="9992a-139">Wählen Sie alle Protokolle für eine bestimmte Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="9992a-139">Select all logs for a particular table.</span></span>
- <span data-ttu-id="9992a-140">Wählen Sie bestimmte Arten von Datenbankprotokollen aus.</span><span class="sxs-lookup"><span data-stu-id="9992a-140">Select specific types of database log.</span></span>
- <span data-ttu-id="9992a-141">Wählen Sie ein Datum und eine Uhrzeit aus, zu der ein Protokoll erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="9992a-141">Select a date and time that a log was created.</span></span>

<span data-ttu-id="9992a-142">Gehen Sie zum Einrichten der Datenbankprotokoll-Bereinigung folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="9992a-142">To set up database log cleanup, follow these steps:</span></span> 

1. <span data-ttu-id="9992a-143">Gehen Sie zu **Systemadministration> Links > Datenbank > Datenbankprotokoll einrichten**.</span><span class="sxs-lookup"><span data-stu-id="9992a-143">Go to **System administration > Links > Database > Database log**.</span></span> <span data-ttu-id="9992a-144">Wählen Sie **Protokoll bereinigen**.</span><span class="sxs-lookup"><span data-stu-id="9992a-144">Select **Clean up log**.</span></span>

2. <span data-ttu-id="9992a-145">Wählen Sie eine Methode zum Auswählen der zu löschenden Protokolle aus, indem Sie eine der folgenden Optionen eingeben:</span><span class="sxs-lookup"><span data-stu-id="9992a-145">Choose a method of selecting logs to delete by entering one of the following options:</span></span>

   - <span data-ttu-id="9992a-146">Tabellenkennung (ID)</span><span class="sxs-lookup"><span data-stu-id="9992a-146">Table ID</span></span>
   - <span data-ttu-id="9992a-147">Art des Protokolls</span><span class="sxs-lookup"><span data-stu-id="9992a-147">Type of log</span></span>
   - <span data-ttu-id="9992a-148">Erstellungsdatum und -uhrzeit</span><span class="sxs-lookup"><span data-stu-id="9992a-148">Created date and time</span></span>

3. <span data-ttu-id="9992a-149">Verwenden Sie die **Bereinigung des Datenbankprotokolls** Registerkarte, um festzulegen, wann die Protokollbereinigungsaufgabe ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9992a-149">Use the **Database log cleanup** tab to determine when to run the log cleanup task.</span></span> <span data-ttu-id="9992a-150">Standardmäßig sind Datenbankprotokolle 30 Tage lang verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9992a-150">By default, database logs are available for 30 days.</span></span>
