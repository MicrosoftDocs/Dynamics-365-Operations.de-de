---
title: Talent mit PowerApps und Microsoft Flow erweitern – Beispielsszenarien
description: In diesem Thema werden einige Beispiele von Erweiterbarkeitsszenarien für Microsoft Dynamics 365 for Talent beschrieben, die Microsoft PowerApps und Microsoft Flow verwenden.
author: negudava
manager: Annbe
ms.date: 05/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: Dynamics 365 for Talent;PowerApps;Flow;Common Data Service
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent;Core;Experience Apps
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2019-03-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: c113b0f4ab2c8e44d00fcfca3f0a6ca828a854ae
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518066"
---
# <a name="extend-talent-by-using-powerapps-and-microsoft-flow---example-scenarios"></a><span data-ttu-id="021b2-103">Talent mit PowerApps und Microsoft Flow erweitern – Beispielsszenarien</span><span class="sxs-lookup"><span data-stu-id="021b2-103">Extend Talent by using PowerApps and Microsoft Flow - Example scenarios</span></span>

<span data-ttu-id="021b2-104">In diesem Thema werden einige Beispiele von Erweiterbarkeitsszenarien für Microsoft Dynamics 365 for Talent beschrieben, die Microsoft PowerApps und Microsoft Flow verwenden.</span><span class="sxs-lookup"><span data-stu-id="021b2-104">This topic describes some examples of extensibility scenarios for Microsoft Dynamics 365 for Talent that use Microsoft PowerApps and Microsoft Flow.</span></span> <span data-ttu-id="021b2-105">Sie können das Lösungspaket importieren, das jedem Beispiel in der PowerApps-Umgebung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="021b2-105">You can import the solution package that is associated with each example into your PowerApps environment.</span></span> <span data-ttu-id="021b2-106">Sie können entweder die Pakete als Anleitung oder als Startpunkte zu den Werkzeugszenarien verwenden, die der Organisation zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="021b2-106">You can then use the packages either as guidance or as starting points to implement scenarios that are applicable to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="021b2-107">Wenn Sie die Vorlagen und Apps verwenden möchten, die in diesem Thema als "wie vorliegend" beschrieben sind, müssen Sie diese unbedingt testen, um sicherzustellen, dass sie alle Szenarien beinhalten, die für Ihre Implementierung bestimmt sind.</span><span class="sxs-lookup"><span data-stu-id="021b2-107">If you want to use the templates and app that are described in this topic "as is," be sure to test them to make sure that they cover all the scenarios that are specific to your implementation.</span></span>


## <a name="prerequisites"></a><span data-ttu-id="021b2-108">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="021b2-108">Prerequisites</span></span>

- <span data-ttu-id="021b2-109">Um Pakete zu importieren, müssen Benutzer die Berechtigung **Umgebungs-Hersteller** haben.</span><span class="sxs-lookup"><span data-stu-id="021b2-109">To import packages, users must have the **Environment Maker** permission.</span></span>
- <span data-ttu-id="021b2-110">Um Apps zu exportierenden oder zu importierenen, müssen Benutzer eine Lizenz PowerApp Plans 2 oder eine Testlizenz PowerApps-Plan 2 haben.</span><span class="sxs-lookup"><span data-stu-id="021b2-110">To export or import apps, users must have a PowerApps Plan 2 license or a PowerApps Plan 2 trial license.</span></span>

## <a name="flow--form-connect"></a><span data-ttu-id="021b2-111">Ablauf - Formular schließen</span><span class="sxs-lookup"><span data-stu-id="021b2-111">Flow – Form Connect</span></span>

<span data-ttu-id="021b2-112">Die Vorlage **Ablauf - Formular verbinden** kann verwendet werden, wenn Daten aus Microsoft Formularen gelesen und in einer Common Data Service Entität gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="021b2-112">The **Flow – Form Connect** template can be used to read data from Microsoft Forms and store it in a Common Data Service entity.</span></span>

<span data-ttu-id="021b2-113">Diese Vorlage kann auch erweitert werden, sodass sie für andere Szenarien verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="021b2-113">This template can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="021b2-114">Nachfolgend finden Sie einige Beispiele:</span><span class="sxs-lookup"><span data-stu-id="021b2-114">Here are some examples:</span></span>

- <span data-ttu-id="021b2-115">Kandidatenbewertungen aufzeichnen.</span><span class="sxs-lookup"><span data-stu-id="021b2-115">Capture candidate assessments.</span></span>
- <span data-ttu-id="021b2-116">Zeichnen Sie Ergebnisse aus Kursfragebögen auf.</span><span class="sxs-lookup"><span data-stu-id="021b2-116">Capture results from course questionnaires.</span></span>
- <span data-ttu-id="021b2-117">Kompilieren Sie eine Bibliothek von Gesprächsfragen für die Personalverwaltungs (HR)-Administratoren.</span><span class="sxs-lookup"><span data-stu-id="021b2-117">Compile a library of interview questions for Human resources (HR) administrators.</span></span>
- <span data-ttu-id="021b2-118">Zeichnen Sie die Bewertung des Kandidaten aus dem Gesprächsprozess auf</span><span class="sxs-lookup"><span data-stu-id="021b2-118">Capture a candidate's evaluation of the interview process</span></span>

<span data-ttu-id="021b2-119">In Microsoft Dynamics 365:  Attract Formulare können in Kandidatenprofilen angezeigt werden und der Kandidat kann die Details ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="021b2-119">In Microsoft Dynamics 365: Attract, forms can appear in Candidate portal, and candidates can fill in details.</span></span> <span data-ttu-id="021b2-120">Formulare können als Aktivitäten auch in einer Stellenvorlage eingebettet werden.</span><span class="sxs-lookup"><span data-stu-id="021b2-120">Forms can also be embedded as activities in a job template.</span></span>

<span data-ttu-id="021b2-121">Wenn ein Kandidat ein Formular sendet, zeichnet Microsoft Flow die Formularübermittlung auf, liest die Daten und speichert sie in der Common Data Service Entität.</span><span class="sxs-lookup"><span data-stu-id="021b2-121">When a candidate submits a form, Microsoft Flow captures the form submission, reads the data, and stores it in the Common Data Service entity.</span></span>

<span data-ttu-id="021b2-122">Um die Vorlage **Ablauf - Formular verbinden** und die benutzerdefinierte Entitäts-Struktur herunterzuladen, gehen Sie zu [Ablauf - Formular verbinden](https://go.microsoft.com/fwlink/?linkid=2081988) im Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="021b2-122">To download the **Flow – Form Connect** template and Custom Entity Structure, go to [Flow – Form Connect](https://go.microsoft.com/fwlink/?linkid=2081988) on the Microsoft Download Center.</span></span>

## <a name="initiate-and-extract-parameters-passed-to-powerapps"></a><span data-ttu-id="021b2-123">Parameter, die an Powerapps übergeben werden, auslösen und extrahieren</span><span class="sxs-lookup"><span data-stu-id="021b2-123">Initiate and Extract Parameters Passed to Powerapps</span></span>

<span data-ttu-id="021b2-124">Die Vorlag **An Powerapps übergebene Parameter einleiten und extrahieren** kann als Ausgangspunkt für alle PowerApps-Szenarien verwendet werden, die Attract spezfisch sind.</span><span class="sxs-lookup"><span data-stu-id="021b2-124">The **Initiate and Extract Parameters Passed to Powerapps** template can be used as a starting point for any PowerApps scenario that is specific to Attract.</span></span> <span data-ttu-id="021b2-125">Dies umfasst alle Standardparameter, die von Attract weitergegeben werden, wie beispielsweise **Stellenbewerbung**, **Kandidaten-ID** und **JobID**.</span><span class="sxs-lookup"><span data-stu-id="021b2-125">It includes all the default parameters that are passed by Attract, such as **Job Application**, **Candidate ID**, and **JobID**.</span></span>

<span data-ttu-id="021b2-126">Diese Vorlage kann verwendet werden, um einen Kandidatenbewertungsbogen abzurufen, damit ein zukünftiger Vorgesetzter die Bewertung sehen kann, die ein Kandidat ausfüllte.</span><span class="sxs-lookup"><span data-stu-id="021b2-126">This template can be used to retrieve a candidate assessment form, so that a hiring manager can view the assessment that a candidate filled in.</span></span>

<span data-ttu-id="021b2-127">Apps, die mithilfe von PowerApps erstellt wurden, können in die Stellenvorlage in Attract eingebettet werden.</span><span class="sxs-lookup"><span data-stu-id="021b2-127">Apps that are created by using PowerApps can be embedded into the job template in Attract.</span></span>

<span data-ttu-id="021b2-128">Wenn Sie die Vorlage **Parameter, die die Powerapps durchlaufen einleiten und extrahieren** und die benutzerdefinierte Entitätsstruktur herunterladen, gehen Sie im Microsoft Download Center auf [Parameter,di die Powerapps durchlaufen einleiten und extrahieren](https://go.microsoft.com/fwlink/?linkid=2081991).</span><span class="sxs-lookup"><span data-stu-id="021b2-128">To download the **Initiate and Extract Parameters Passed to Powerapps** template and Custom Entity Structure, go to [Initiate and Extract Parameters Passed to Powerapps](https://go.microsoft.com/fwlink/?linkid=2081991) on the Microsoft Download Center.</span></span>

## <a name="integration-with-office-365"></a><span data-ttu-id="021b2-129">Integration mit Office 365</span><span class="sxs-lookup"><span data-stu-id="021b2-129">Integration with Office 365</span></span>

<span data-ttu-id="021b2-130">Die **Integration mit Office 365** App kann verwendet werden, um Teaminformationen für angemeldete Benutzer von Microsoft Office 365 zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="021b2-130">The **Integration with Office 365** app can be used to extract team information for signed-in users from Microsoft Office 365.</span></span> <span data-ttu-id="021b2-131">Sie verweist Arbeitskräfte in Talent dahingehend, Ausstempeldetails und Ausnahmeaufzeichnungen zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="021b2-131">It references workers in Talent to extract clock-in and clock-out details and exception recordings.</span></span> <span data-ttu-id="021b2-132">Ein- und Ausstempelndetails werden in den benutzerdefinierten Common Data Service Entitäten gespeichert.</span><span class="sxs-lookup"><span data-stu-id="021b2-132">Clock-in and Clock-out details are stored in custom Common Data Service entities.</span></span> <span data-ttu-id="021b2-133">Die Voraussetzung ist, dass diese Details von einem System von einem Fremdanbietern über die Integration ausgefüllt werden.</span><span class="sxs-lookup"><span data-stu-id="021b2-133">The assumption is that these details are filled in from third-party systems via integration.</span></span>

<span data-ttu-id="021b2-134">Diese App kann auch erweitert werden, sodass sie für andere Szenarien verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="021b2-134">This app can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="021b2-135">Sie kann zum Beispiel dazu verwendet werden, Teamferieninformationen, Kalenderereignisse und weitere Team spezifische Ereignisse anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="021b2-135">For example, it can be used to show team vacation information, calendar events, and any team-specific events.</span></span>

<span data-ttu-id="021b2-136">Wenn Sie die App**Integration mit Office 365** und die benutzerdefinierte Entitäts-Struktur herunterladen, gehen Sie zu [Integration mit Office 365](https://go.microsoft.com/fwlink/?linkid=2081787) im Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="021b2-136">To download the **Integration with Office 365** app and Custome Entity Structure, go to [Integration with Office 365](https://go.microsoft.com/fwlink/?linkid=2081787) on the Microsoft Download Center.</span></span>

## <a name="flow--email-notification"></a><span data-ttu-id="021b2-137">Fluss – E-Mail-Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="021b2-137">Flow – Email Notification</span></span>

<span data-ttu-id="021b2-138">Die Vorlage **Fluss - E-Mail-Benachrichtigung** kann für E-Mail-Benachrichtigungsszenarien verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="021b2-138">The **Flow – Email Notification** template can be used for email notification scenarios.</span></span> <span data-ttu-id="021b2-139">Sie kann verwendet werden, um Benachrichtigungs-E-Mails zu den Kandidaten zu starten, die das Einstellungsteam während jeder Phase des Rekrutierungsprozesses abgelehnt hat.</span><span class="sxs-lookup"><span data-stu-id="021b2-139">It can be used to trigger notification emails to candidates that the hiring team rejects during any stage of the recruiting process.</span></span>

<span data-ttu-id="021b2-140">Diese Vorlage kann erweitert werden, um Änderungen an der Kandidatenphase während des Rekrutierungsprozesses nachzuverfolgen und, Benachrichtigungen an das Einstellungsteam und die Kandidaten zu senden.</span><span class="sxs-lookup"><span data-stu-id="021b2-140">This template can be extended to track changes to the candidate stage throughout the recruiting process, and to send notifications to the hiring team and candidate.</span></span>

<span data-ttu-id="021b2-141">Im Allgemeinen gilt für Entitäten, die in Common Data Service gespeichert werden,, dass Fluss eingerichtet werden kann, um Benachrichtigungen für Ereignisse zu versenden, die in Core HR Attract oder in Dynamics 365 Talent: Onboard auftreten.</span><span class="sxs-lookup"><span data-stu-id="021b2-141">In general, for entities that are stored in Common Data Service, flows can be set up to send notifications for events that occur in Core HR, Attract, or Dynamics 365 Talent: Onboard.</span></span>

<span data-ttu-id="021b2-142">Um die Vorlage **Flussf - E-Mail-Benachrichtigung** herunterzuladen gehen Sie zu [Fluss - E-Mail-Benachrichtigung](https://go.microsoft.com/fwlink/?linkid=2082103) im Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="021b2-142">To download the **Flow – Email Notification** template, go to [Flow – Email Notification](https://go.microsoft.com/fwlink/?linkid=2082103) on the Microsoft Download Center.</span></span>

## <a name="flow--sql-connect-and-execute"></a><span data-ttu-id="021b2-143">Fluss - SQL Connect und ausführen</span><span class="sxs-lookup"><span data-stu-id="021b2-143">Flow – SQL Connect and execute</span></span>

<span data-ttu-id="021b2-144">Die Vorlage **Fluss - SQL Connect und ausführen** verbindet mit  Microsoft SQL Server und aktiviert die SQL Abfrage, die dann ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="021b2-144">The **Flow – SQL Connect and execute** template connects to Microsoft SQL Server and enables SQL queries to be run.</span></span>

<span data-ttu-id="021b2-145">Obwohl diese Vorlage dazu entwickelt wurde, SQL-Tabellen zu lesen und zu aktualisieren, kann sie auch erweitert werden, sodass sie für andere Szenarien verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="021b2-145">Although this template is designed to read and update SQL tables, it can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="021b2-146">Sie kann beispielsweise dazu verwendet werden, um eine Stagingtabelle in Common Data Service mit Datensätzen vom SQL Server zu füllen und um die Stagingtabelle regelmäßig zu synchronisieren, indem ein inkrementeller Push von SQL Server verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="021b2-146">For example, it can be used to fill a staging table in Common Data Service with records from SQL Server, and to periodically synchronize the staging table by using an incremental push from SQL Server.</span></span>

<span data-ttu-id="021b2-147">Um die Vorlage **Ablauf - SQL verbinden und ausführen** herunterzuladen, gehen Sie zu [Ablauf - Formular verbinden](https://go.microsoft.com/fwlink/?linkid=2081789) im Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="021b2-147">To download the **Flow – SQL Connect and execute** template, go to [Flow – SQL Connect and execute](https://go.microsoft.com/fwlink/?linkid=2081789) on the Microsoft Download Center.</span></span>

## <a name="flow--sharepoint-integration"></a><span data-ttu-id="021b2-148">Fluss SharePoint-Integration</span><span class="sxs-lookup"><span data-stu-id="021b2-148">Flow – SharePoint Integration</span></span>

<span data-ttu-id="021b2-149">Die Vorlage **Fluss – SharePoint Integration** kann verwendet werden, um Daten aus einer Microsoft SharePoint  Liste zu lesen, die Liste mit Feldwerten für jede beliebige Common Data Service Entität zu vergleichen und die Ergebnisse des Vergleichs als Benachrichtigungs-E-Mail zu versenden.</span><span class="sxs-lookup"><span data-stu-id="021b2-149">The **Flow – SharePoint Integration** template can be used to read data from a Microsoft SharePoint list, compare the list with field values for any Common Data Service entity, and send the results of the comparison as a notification email.</span></span> 

<span data-ttu-id="021b2-150">Eine Organisation hat möglicherweise eine Reihe von Fähigkeiten, die sie dringend benötigt.</span><span class="sxs-lookup"><span data-stu-id="021b2-150">An organization might have a set of skills that it urgently requires.</span></span> <span data-ttu-id="021b2-151">Diese Qualifikationen können in SharePoint als Liste SharePoint gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="021b2-151">These skills can be stored in SharePoint as a SharePoint list.</span></span> <span data-ttu-id="021b2-152">Wenn sich ein Kandidat für eine Stelle bewirbt, die Qualifikationen verlangt, die aufgelistet sind und wenn es eine erhebliche Übereinstimmung zwischen den Fähigkeiten des Kandidaten und den Qualifikationen gibt, die in SharePoint gespeichert sind, wird eine  Benachrichtigungs-E-Mail übermittelt.</span><span class="sxs-lookup"><span data-stu-id="021b2-152">When a candidate applies for any job that a set of required skills is listed for, if there is a significant match between the candidate's skill and the skills that are stored in SharePoint, a notification email is sent.</span></span> <span data-ttu-id="021b2-153">Auf diese Weise werden Positionen, die dringend erforderlich sind, schneller gefüllt, da die Benachrichtigungen den Personalbeschaffern hilft, Kandidaten aus der gesamten Organisation zu finden.</span><span class="sxs-lookup"><span data-stu-id="021b2-153">In this way, positions that are urgently required are filled faster, because the notifications help recruiters reach out and cross-hire candidates throughout the organization.</span></span>

<span data-ttu-id="021b2-154">Diese Vorlage kann auch erweitert werden, sodass sie für ein beliebiges Szenario verwendet werden kann, das die SharePoint Integration betrifft.</span><span class="sxs-lookup"><span data-stu-id="021b2-154">This template can be extended so that it can be used for any scenario that involves SharePoint integration.</span></span>

<span data-ttu-id="021b2-155">Um die Vorlage **Fluss – SharePoint Integration**herunterzuladen, gehen Sie zu [Fluss SharePoint Integration ](https://go.microsoft.com/fwlink/?linkid=2082109) im Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="021b2-155">To download the **Flow – SharePoint Integration** template, go to [Flow – SharePoint Integration](https://go.microsoft.com/fwlink/?linkid=2082109) on the Microsoft Download Center.</span></span>

## <a name="admin-console-to-manage-talent-pools"></a><span data-ttu-id="021b2-156">Administratorkonsole, um Talentpools zu verwalten</span><span class="sxs-lookup"><span data-stu-id="021b2-156">Admin console to manage talent pools</span></span>

<span data-ttu-id="021b2-157">Bei der Aktivierung von Integration in LinkedIn, erstellt Attract automatisch einen LinkedIn-Talentpool.</span><span class="sxs-lookup"><span data-stu-id="021b2-157">When you enable integration with LinkedIn, Attract automatically createas a LinkedIn talent pool.</span></span> <span data-ttu-id="021b2-158">Wenn ein Personalvermittler InMail über LinkedIn mit einem Rekruten austauscht, erstellt Attract ein Profil für den Rekruten und dieser wird ein Mitglied im LinkedIn-Talentpool.</span><span class="sxs-lookup"><span data-stu-id="021b2-158">When a recruiter exchanges InMail with a recruit through LinkedIn, Attract creates a profile for the recruit, and the recruit becomes a member of the LinkedIn talent pool.</span></span> <span data-ttu-id="021b2-159">Diese PowerApps-App ist für die Neuanordnung von Kandidaten in Talentpools auf Grundlage ihrer Fähigkeiten nützlich.</span><span class="sxs-lookup"><span data-stu-id="021b2-159">This PowerApps app is useful for reorganizing candidates in talent pools based on skill.</span></span>

<span data-ttu-id="021b2-160">Führen Sie diese PowerApps-App als eine Administratorkonsole aus, um die folgenden Aufgaben auszuführen:</span><span class="sxs-lookup"><span data-stu-id="021b2-160">Run this PowerApps app as an admin console to perform the following tasks:</span></span>

- <span data-ttu-id="021b2-161">Kandidaten in einem Talentpool aufführen</span><span class="sxs-lookup"><span data-stu-id="021b2-161">List candidates in a talent pool</span></span>
- <span data-ttu-id="021b2-162">Kandidaten einem Talentpool hinzufügen und daraus entfernen</span><span class="sxs-lookup"><span data-stu-id="021b2-162">Add and remove candidates from a talent pool</span></span>
- <span data-ttu-id="021b2-163">Kandidaten von einem Talentpool zu einem anderen verschieben</span><span class="sxs-lookup"><span data-stu-id="021b2-163">Move candidates from one talent pool to another</span></span>
- <span data-ttu-id="021b2-164">Bestimmen, ob Kandidaten bereits Teil eines Talentpools sind, bevor Sie verschoben werden</span><span class="sxs-lookup"><span data-stu-id="021b2-164">Determine whether candidates are already part of a talent pool before moving them</span></span>
- <span data-ttu-id="021b2-165">Überprüfen der Fähigkeiten von Kandidaten, bevor sie in andere Talentpools verschoben werden</span><span class="sxs-lookup"><span data-stu-id="021b2-165">Check the skills of candidates before moving them to other talent pools</span></span>

<span data-ttu-id="021b2-166">Diese PowerApps-App verwendet n:n-Beziehungen, sodass Sie diese App als Vorlage für andere Szenarien verwenden können, in denen Sie Datensätze mit n:n-Beziehungen extrahieren müssen.</span><span class="sxs-lookup"><span data-stu-id="021b2-166">This PowerApps app uses many-to-many relationships, so you can use it as a template for other scenarios where you need to extract records that have many-to-many relationships.</span></span>

<span data-ttu-id="021b2-167">Zum herunterladen der Vorlage **Administratorkonsole zum Verwalten von Talentpools** wechseln Sie zu [Administratorkonsole zum Verwalten von Talentpools](http://www.microsoft.com/downloads/details.aspx?FamilyID=780a5eee-0e2a-4159-9a83-009f9ccdc469) im Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="021b2-167">To download the **Admin console to manage talent pools** template,  go to [Admin console to manage talent pools](http://www.microsoft.com/downloads/details.aspx?FamilyID=780a5eee-0e2a-4159-9a83-009f9ccdc469) on the Microsoft Download Center.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="021b2-168">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="021b2-168">Additional resources</span></span>

[<span data-ttu-id="021b2-169">Das Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="021b2-169">The Microsoft Power Platform</span></span>](https://docs.microsoft.com/power-platform/admin/admin-documentation)

[<span data-ttu-id="021b2-170">Migrieren der App zwischen Mandanten und Umgebung</span><span class="sxs-lookup"><span data-stu-id="021b2-170">Migrate app between tenants and environments</span></span>](https://docs.microsoft.com/en-us/power-platform/admin/environment-and-tenant-migration)
