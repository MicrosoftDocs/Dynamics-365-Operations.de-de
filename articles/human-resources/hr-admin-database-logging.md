---
title: Datenbankprotokollierung konfigurieren und verwalten
description: Sie können Änderungen an Tabellen und Feldern in Dynamics 365 Human Resources mit Datenbankprotokollierung verfolgen.
author: andreabichsel
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ae974436469c00a3df6fd40d9d60521a0883a917
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054811"
---
# <a name="configure-and-manage-database-logging"></a><span data-ttu-id="fb4ec-103">Datenbankprotokollierung konfigurieren und verwalten</span><span class="sxs-lookup"><span data-stu-id="fb4ec-103">Configure and manage database logging</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="fb4ec-104">Sie können Änderungen an Tabellen und Feldern in Dynamics 365 Human Resources mit Datenbankprotokollierung verfolgen.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-104">You can track changes to tables and fields in Dynamics 365 Human Resources with database logging.</span></span> <span data-ttu-id="fb4ec-105">In diesem Thema wird beschrieben, wie:</span><span class="sxs-lookup"><span data-stu-id="fb4ec-105">This topic describes how to:</span></span>

- <span data-ttu-id="fb4ec-106">Verwalten Sie Sicherheit und Leistung für die Datenbankprotokollierung</span><span class="sxs-lookup"><span data-stu-id="fb4ec-106">Manage security and performance for database logging</span></span>
- <span data-ttu-id="fb4ec-107">Datenbankprotokollierung einrichten</span><span class="sxs-lookup"><span data-stu-id="fb4ec-107">Set up database logging</span></span>
- <span data-ttu-id="fb4ec-108">Bereinigen Sie Datenbankprotokolle</span><span class="sxs-lookup"><span data-stu-id="fb4ec-108">Clean up database logs</span></span>

## <a name="overview-of-database-logging"></a><span data-ttu-id="fb4ec-109">Übersicht über die Datenbankprotokollierung</span><span class="sxs-lookup"><span data-stu-id="fb4ec-109">Overview of database logging</span></span>

<span data-ttu-id="fb4ec-110">Sie können Änderungen an Tabellen und Feldern in Microsoft Dynamics 365 Human Resources mit Datenbankprotokollierung verfolgen.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-110">Database logging tracks specific changes to Microsoft Dynamics 365 Human Resources tables and fields.</span></span> <span data-ttu-id="fb4ec-111">Diese Änderungen umfassen das Einfügen, Aktualisieren oder Löschen.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-111">These changes include inserting, updating, or deleting.</span></span> <span data-ttu-id="fb4ec-112">Die Datenbankprotokollierung speichert eine Aufzeichnung der Änderungen an Tabellen oder Feldern in der Datenbankprotokolltabelle.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-112">Database logging stores a record of changes to tables or fields in the database log table.</span></span>

<span data-ttu-id="fb4ec-113">Die geschäftlichen Verwendungen der Datenbankprotokollierung umfassen:</span><span class="sxs-lookup"><span data-stu-id="fb4ec-113">The business uses of database logging include:</span></span>

- <span data-ttu-id="fb4ec-114">Erstellen eines Überwachungsdatensatzes mit Änderungen an bestimmten Tabellen, die vertrauliche Informationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-114">Creating an audit record of changes to specific tables that contain sensitive information.</span></span>
- <span data-ttu-id="fb4ec-115">Verfolgung einzelner Transaktionen.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-115">Tracking single transactions.</span></span> <span data-ttu-id="fb4ec-116">Die Datenbankprotokollierung dient nicht zur Verfolgung automatisierter Transaktionen, die in Stapeljobs ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-116">Database logging isn't intended for tracking automated transactions that run in batch jobs.</span></span>

## <a name="security-for-database-logging"></a><span data-ttu-id="fb4ec-117">Sicherheit für die Datenbankprotokollierung</span><span class="sxs-lookup"><span data-stu-id="fb4ec-117">Security for database logging</span></span>

<span data-ttu-id="fb4ec-118">Datenbankprotokolle können sensible Daten enthalten.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-118">Database logs can contain sensitive data.</span></span> <span data-ttu-id="fb4ec-119">Beschränken Sie den Zugriff auf Sicherheitsrollen, die Zugriff auf die Protokolldaten benötigen.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-119">Limit access to include only security roles that need access to the log data.</span></span>

## <a name="database-logging-and-performance"></a><span data-ttu-id="fb4ec-120">Datenbankprotokollierung und Leistung</span><span class="sxs-lookup"><span data-stu-id="fb4ec-120">Database logging and performance</span></span>

<span data-ttu-id="fb4ec-121">Die Datenbankprotokollierung kann zwar aus geschäftlicher Sicht hilfreich sein, sie kann allerdings auch eine hohe Ressourcenauslastung sowie einen hohen Verwaltungsaufwand bedeuten.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-121">While valuable from a business perspective, database logging can be expensive in resource use and management.</span></span> <span data-ttu-id="fb4ec-122">Die Leistungsbeeinträchtigungen der Datenbankprotokollierung umfassen:</span><span class="sxs-lookup"><span data-stu-id="fb4ec-122">The performance implications of database logging include:</span></span>

- <span data-ttu-id="fb4ec-123">Die Datenbankprotokolltabelle kann schnell wachsen und die Größe der Datenbank erhöhen.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-123">The database log table can grow quickly and cause an increase in the size of the database.</span></span> <span data-ttu-id="fb4ec-124">Das Wachstum hängt von der Menge der protokollierten Daten ab, die Sie behalten möchten.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-124">Growth depends on the amount of logged data that you decide to keep.</span></span> <span data-ttu-id="fb4ec-125">Standardmäßig verwaltet die Datenbankprotokolltabelle nur 30 Tage Protokolldaten.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-125">By default, the database log table maintains only 30 days of log data.</span></span> 

- <span data-ttu-id="fb4ec-126">Die Datenbankprotokollierung kann sich nachteilig auf lang laufende automatisierte Prozesse auswirken, z. B. auf lang laufende Datenimporte.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-126">Database logging can adversely affect long-running automated processes, such as long-running data imports.</span></span>

### <a name="best-practices"></a><span data-ttu-id="fb4ec-127">Optimale Verfahren</span><span class="sxs-lookup"><span data-stu-id="fb4ec-127">Best practices</span></span>

<span data-ttu-id="fb4ec-128">Wählen Sie zum Eingrenzen der Anzahl von Protokolleinträgen und zur Steigerung der Leistung nur die jeweils gewünschten Felder für die Protokollierung und keine vollständigen Tabellen aus.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-128">To improve performance, limit log entries by selecting specific fields to log instead of whole tables.</span></span> <span data-ttu-id="fb4ec-129">Um die Gesamtleistung aufrechtzuerhalten, ist die Datenbankprotokollierung auf 20 Tabellen beschränkt.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-129">To help maintain overall performance, database logging is limited to 20 tables.</span></span>

> [!NOTE]
> <span data-ttu-id="fb4ec-130">Für einzelne Feldern können nur Aktualisierungen protokolliert werden.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-130">Only updates can be logged for individual fields.</span></span>

## <a name="set-up-database-logging"></a><span data-ttu-id="fb4ec-131">Datenbankprotokollierung einrichten</span><span class="sxs-lookup"><span data-stu-id="fb4ec-131">Set up database logging</span></span>

<span data-ttu-id="fb4ec-132">Sie können den Assistent **Protokollieren von Datenbankänderungen** zum Einrichten der Datenbankprotokollierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-132">You can use the **Logging database changes** wizard to set up database logging.</span></span> <span data-ttu-id="fb4ec-133">Der Assistent bietet eine flexible Möglichkeit, die Protokollierung für Tabellen oder Felder einzurichten.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-133">The wizard provides a flexible way to set up logging for tables or fields.</span></span>

1. <span data-ttu-id="fb4ec-134">Gehen Sie zu **Systemadministration> Links> Datenbank> Datenbankprotokoll einrichten**.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-134">Go to **System administration > Links > Database > Database log setup**.</span></span> <span data-ttu-id="fb4ec-135">Wählen Sie **Neu** aus, um den Assistent **Protokollieren von Datenbankänderungen** zu starten.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-135">Select **New** to start the **Logging database changes** wizard.</span></span>
2. <span data-ttu-id="fb4ec-136">Wählen Sie **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-136">Select **Next**.</span></span> 
3. <span data-ttu-id="fb4ec-137">Wählen Sie auf der Seite **Tabellen und Felder** des Assistenten die Tabellen und Felder aus, für die Sie die Datenbankprotokollierung aktivieren möchten, und wählen Sie **Weiter** aus.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-137">On the **Tables and fields** page of the wizard, select the the tables and fields on which you want to enable database logging, and select **Next**.</span></span>

   > [!Note]
   > <span data-ttu-id="fb4ec-138">Die Datenbankprotokollierung ist nicht für alle Tabellen in der Personaldatenbank verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-138">Database logging is not available on all tables in the Human Resources database.</span></span> <span data-ttu-id="fb4ec-139">Wenn Sie **Alle Tabellen anzeigen** unterhalb der Liste auswählen, wird die Liste der Tabellen und Felder erweitert, um alle Datenbanktabellen anzuzeigen, für die die Datenbankprotokollierung verfügbar ist. Dies ist jedoch eine Teilmenge der vollständigen Liste der Datenbanktabellen.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-139">Selecting **Show all tables** below the list expands the list of tables and fields to show all database tables for which database logging is available, but this will be a subset of the full list of database tables.</span></span>

4. <span data-ttu-id="fb4ec-140">Wählen Sie auf der Seite **Änderungstypen** des Assistenten die Datenvorgänge aus, für die Sie Änderungen für jede der Tabellen und Felder verfolgen möchten, und wählen Sie **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-140">On the **Types of change** page of the wizard, select the data operations for which you want to track changes for each of the tables and fields, and select **Next**.</span></span> <span data-ttu-id="fb4ec-141">In der folgenden Tabelle finden Sie eine Beschreibung der Datenvorgänge, die für die Protokollierung verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-141">See the table below for a description of the data operations that are available for logging.</span></span>
5. <span data-ttu-id="fb4ec-142">Überprüfen Sie auf der Seite **Fertig stellen** die vorgenommenen Änderungen und wählen Sie **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-142">On the **Finish** page, review the changes that will be made, and select **Finish**.</span></span>

| <span data-ttu-id="fb4ec-143">Vorgang</span><span class="sxs-lookup"><span data-stu-id="fb4ec-143">Operation</span></span> | <span data-ttu-id="fb4ec-144">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fb4ec-144">Description</span></span> |
| -- | -- |
| <span data-ttu-id="fb4ec-145">Neue Buchungen nachverfolgen</span><span class="sxs-lookup"><span data-stu-id="fb4ec-145">Track new transactions</span></span> | <span data-ttu-id="fb4ec-146">Erstellen Sie ein Protokoll für neue Datensätze, die in der Tabelle erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-146">Create a log for new records that are created in the table.</span></span> |
| <span data-ttu-id="fb4ec-147">Buchen</span><span class="sxs-lookup"><span data-stu-id="fb4ec-147">Update</span></span> | <span data-ttu-id="fb4ec-148">Erstellen Sie ein Protokoll für Aktualisierungen von Tabellendatensätzen oder Aktualisierungen für einzeln ausgewählte Felder in der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-148">Create a log for updates to table records, or updates to individually selected fields in the table.</span></span> <span data-ttu-id="fb4ec-149">Wenn Sie auswählen, Aktualisierungen für die Tabelle zu protokollieren, wird jedes Mal ein Protokolldatensatz erstellt, wenn eine Aktualisierung an einem Feld eines Datensatzes in der Tabelle vorgenommen wird.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-149">If you select to log updates for the table, then a log record is created each time an update is made to any field of any record on the table.</span></span> <span data-ttu-id="fb4ec-150">Wenn Sie auswählen, Aktualisierungen für bestimmte Felder zu protokollieren, wird ein Protokolldatensatz nur erstellt, wenn Aktualisierungen an diesen Feldern von Tabellendatensätzen vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-150">If you select to log updates for specific fields, then a log record is created only when updates are made to those fields of table records.</span></span> |
| <span data-ttu-id="fb4ec-151">Löschen</span><span class="sxs-lookup"><span data-stu-id="fb4ec-151">Delete</span></span> | <span data-ttu-id="fb4ec-152">Erstellen Sie ein Protokoll für Datensätze, die aus der Tabelle gelöscht wurden.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-152">Create a log for records deleted from the table.</span></span> |
| <span data-ttu-id="fb4ec-153">Schlüssel umbenennen</span><span class="sxs-lookup"><span data-stu-id="fb4ec-153">Rename key</span></span> | <span data-ttu-id="fb4ec-154">Erstellen Sie einen Protokolldatensatz, wenn ein Tabellenschlüssel umbenannt wird.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-154">Create a log record when a table key is renamed.</span></span> |


## <a name="clean-up-database-logs"></a><span data-ttu-id="fb4ec-155">Bereinigen Sie Datenbankprotokolle</span><span class="sxs-lookup"><span data-stu-id="fb4ec-155">Clean up database logs</span></span>

<span data-ttu-id="fb4ec-156">Sie können alle oder einen Teil der Datenbankprotokolle mit den folgenden Optionen löschen:</span><span class="sxs-lookup"><span data-stu-id="fb4ec-156">You can delete all or part of the database logs, using the following options:</span></span>

- <span data-ttu-id="fb4ec-157">Wählen Sie alle Protokolle für eine bestimmte Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-157">Select all logs for a particular table.</span></span>
- <span data-ttu-id="fb4ec-158">Wählen Sie bestimmte Arten von Datenbankprotokollen aus.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-158">Select specific types of database log.</span></span>
- <span data-ttu-id="fb4ec-159">Wählen Sie ein Datum und eine Uhrzeit aus, zu der ein Protokoll erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-159">Select a date and time that a log was created.</span></span>

<span data-ttu-id="fb4ec-160">Gehen Sie zum Einrichten der Datenbankprotokoll-Bereinigung folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="fb4ec-160">To set up database log cleanup, follow these steps:</span></span> 

1. <span data-ttu-id="fb4ec-161">Gehen Sie zu **Systemadministration> Links > Datenbank > Datenbankprotokoll einrichten**.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-161">Go to **System administration > Links > Database > Database log**.</span></span> <span data-ttu-id="fb4ec-162">Wählen Sie **Protokoll bereinigen**.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-162">Select **Clean up log**.</span></span>

2. <span data-ttu-id="fb4ec-163">Wählen Sie eine Methode zum Auswählen der zu löschenden Protokolle aus, indem Sie eine der folgenden Optionen eingeben:</span><span class="sxs-lookup"><span data-stu-id="fb4ec-163">Choose a method of selecting logs to delete by entering one of the following options:</span></span>

   - <span data-ttu-id="fb4ec-164">Tabellenkennung (ID)</span><span class="sxs-lookup"><span data-stu-id="fb4ec-164">Table ID</span></span>
   - <span data-ttu-id="fb4ec-165">Art des Protokolls</span><span class="sxs-lookup"><span data-stu-id="fb4ec-165">Type of log</span></span>
   - <span data-ttu-id="fb4ec-166">Erstellungsdatum und -uhrzeit</span><span class="sxs-lookup"><span data-stu-id="fb4ec-166">Created date and time</span></span>

3. <span data-ttu-id="fb4ec-167">Verwenden Sie die **Bereinigung des Datenbankprotokolls** Registerkarte, um festzulegen, wann die Protokollbereinigungsaufgabe ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-167">Use the **Database log cleanup** tab to determine when to run the log cleanup task.</span></span> <span data-ttu-id="fb4ec-168">Standardmäßig sind Datenbankprotokolle 30 Tage lang verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-168">By default, database logs are available for 30 days.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
