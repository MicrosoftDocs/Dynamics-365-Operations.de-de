---
title: Kandidaten für Stellen anwerben
description: Dieses Thema zeigt, wie Sie Kandidaten in Dynamics 365 Human Resources anwerben.
author: andreabichsel
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 529f419a4e3e4e8807c6938fd2425ae01ce282f9
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051808"
---
# <a name="recruit-job-candidates"></a><span data-ttu-id="ab4ac-103">Kandidaten für Stellen anwerben</span><span class="sxs-lookup"><span data-stu-id="ab4ac-103">Recruit job candidates</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="ab4ac-104">Dynamics 365 Human Resources hilft Ihnen bei der Verwaltung von Personalbeschaffungsanträgen.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-104">Dynamics 365 Human Resources helps you to manage recruiting requests.</span></span> <span data-ttu-id="ab4ac-105">Es hilft Ihnen auch beim Übergang vom Kandidaten zum Mitarbeiter.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-105">It also helps you seamlessly transition job candidates to employees.</span></span> <span data-ttu-id="ab4ac-106">Wenn Ihre Organisation eine separate Personalbeschaffungsanwendung verwendet, gehören zu Ihrem Personalbeschaffungsprozess möglicherweise die folgenden Schritte:</span><span class="sxs-lookup"><span data-stu-id="ab4ac-106">If your organization uses a separate recruiting application, your recruiting process might include the following steps:</span></span>

- <span data-ttu-id="ab4ac-107">Eingabe des Personalbeschaffungsantrags in Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-107">Enter your recruiting request in Human Resources.</span></span>
- <span data-ttu-id="ab4ac-108">Aus der Personalbeschaffungsanwendung an Human Resources weitergeleitete Kandidaten entgegennehmen.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-108">Receive candidate referrals in Human Resources from the recruiting application.</span></span>
- <span data-ttu-id="ab4ac-109">Den Genehmigungsprozess für Kandidaten in der Personalverwaltung abschließen.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-109">Complete the candidate approval process in Human Resources.</span></span>

<span data-ttu-id="ab4ac-110">Wenn Sie keine separate Personalbeschaffungsanwendung verwenden, können Sie Kandidaten in der Personalverwaltung auch manuell verwalten.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-110">If you aren't using a separate recruiting application, you can also manually manage candidates in Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="ab4ac-111">Wenn Sie Administrator oder Entwickler sind und Human Resources mit der Personalbeschaffungsanwendung eines Drittanbieters integrieren möchten, lesen Sie [Dataverse-Integration konfigurieren](hr-admin-integration-common-data-service.md) und [Virtuelle Dataverse-Tabellen konfigurieren](hr-admin-integration-common-data-service-virtual-entities.md)</span><span class="sxs-lookup"><span data-stu-id="ab4ac-111">If you're an admin or developer and want to integrate Human Resources with a third-party recruiting application, see [Configure Dataverse integration](hr-admin-integration-common-data-service.md) and [Configure Dataverse virtual tables](hr-admin-integration-common-data-service-virtual-entities.md)</span></span>
>
> <span data-ttu-id="ab4ac-112">Sie finden Personalbeschaffungsintegrations-Apps auch auf [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).</span><span class="sxs-lookup"><span data-stu-id="ab4ac-112">You can also find recruiting integration apps on [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).</span></span>
>
> <span data-ttu-id="ab4ac-113">Informationen zum Testen unserer Vorschaufunktion für die Integration in LinkedIn Talent Hub finden Sie unter [In LinkedIn Talent Hub integrieren](hr-admin-integration-linkedin.md).</span><span class="sxs-lookup"><span data-stu-id="ab4ac-113">To try out our preview feature for integrating with LinkedIn Talent Hub, see [Integrate with LinkedIn Talent Hub](hr-admin-integration-linkedin.md).</span></span>

## <a name="enable-recruiting-requests"></a><span data-ttu-id="ab4ac-114">Personalbeschaffungsanträge aktivieren</span><span class="sxs-lookup"><span data-stu-id="ab4ac-114">Enable recruiting requests</span></span>

<span data-ttu-id="ab4ac-115">Wenn Sie Personalbeschaffungsanträge in Human Resources einreichen möchten, müssen Sie die Funktionalität erst in **Gemeinsame Human Resources-Parameter** aktivieren.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-115">If you want to submit recruiting requests in Human Resources, you must first enable the functionality in **Human resources shared parameters**.</span></span>

1. <span data-ttu-id="ab4ac-116">Wählen Sie im Arbeitsbereich **Personalverwaltung** die Registerkarte **Links** aus.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-116">In the **Personnel management** workspace, select **Links**.</span></span>

2. <span data-ttu-id="ab4ac-117">Unter **Einrichtung** wählen Sie **Freigegebene Human Resources-Parameter** aus.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-117">Under **Setup**, select **Human resources shared parameters**.</span></span>

3. <span data-ttu-id="ab4ac-118">Setzen Sie in der Registerkarte **Personalbeschaffung** unter **PERSONALBESCHAFFUNG** **Personalbeschaffungsanträge aktivieren** auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-118">On the **Recruitment** tab, under **RECRUITING**, set **Enable recruiting requests** to **Yes**.</span></span>

## <a name="add-a-recruiting-request-location"></a><span data-ttu-id="ab4ac-119">Einen Standort für den Personalbeschaffungsantrag hinzufügen</span><span class="sxs-lookup"><span data-stu-id="ab4ac-119">Add a recruiting request location</span></span>

<span data-ttu-id="ab4ac-120">Wenn Ihre Organisation mehrere Standorte hat, können Sie diese hinzufügen, damit Anforderer den Standort auswählen können, an dem der neue Mitarbeiter arbeiten soll.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-120">If your organization has multiple locations, you can add them so requestors can select a location where the new recruit will be working.</span></span> <span data-ttu-id="ab4ac-121">Der Standort wird in die Stellenausschreibung aufgenommen.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-121">The location will be included in the job posting.</span></span>

1. <span data-ttu-id="ab4ac-122">Geben Sie in die Suchleiste **Standort für Personalbeschaffungsantrag** ein.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-122">In the search bar, enter **recruiting request location**.</span></span>

2. <span data-ttu-id="ab4ac-123">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-123">Select **New**.</span></span>

3. <span data-ttu-id="ab4ac-124">Im Feld **Standort für Personalbeschaffungsantrag** geben Sie den Standortnamen ein.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-124">In the **Recruiting request location** field, enter the location name.</span></span>

   ![Einen Standort für den Personalbeschaffungsantrag hinzufügen](./media/hr-recruit-0a-add-location.png)

4. <span data-ttu-id="ab4ac-126">Geben Sie im Feld **Beschreibung** eine Beschreibung für den Standort ein.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-126">In the **Description**, enter a description for the location.</span></span>

5. <span data-ttu-id="ab4ac-127">Wählen Sie unter **Standort** **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-127">Under **Location**, select **Add**.</span></span> <span data-ttu-id="ab4ac-128">Geben Sie die Standortadresse ein, wenn das Popout **Neue Adresse** erscheint.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-128">If the **New address** popout appears, enter the address for the location.</span></span>

   ![Adresse eingeben](./media/hr-recruit-0b-address.png)

6. <span data-ttu-id="ab4ac-130">Geben Sie unter **Kontaktinformation** die Informationen für den Kontakt des Standorts ein.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-130">Under **Contact information**, enter the information for the location's contact.</span></span>

7. <span data-ttu-id="ab4ac-131">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-131">Select **Save**.</span></span>

## <a name="add-a-recruiting-request"></a><span data-ttu-id="ab4ac-132">Einen Personalbeschaffungsantrag hinzufügen</span><span class="sxs-lookup"><span data-stu-id="ab4ac-132">Add a recruiting request</span></span>

<span data-ttu-id="ab4ac-133">Manager können Personalbeschaffungsanträge in Human Resources einreichen.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-133">Managers can submit recruiting requests in Human Resources.</span></span> <span data-ttu-id="ab4ac-134">Wenn Sie eine separate Personalbeschaffungsanwendung verwenden, können Sie mit diesen Schritten einen Personalbeschaffungsantrag senden und den Personalbeschaffungsprozess in dieser Anwendung starten.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-134">If you use a separate recruiting application, completing these steps will send a recruiting request and start the recruiting process in that application.</span></span> <span data-ttu-id="ab4ac-135">Gehen Sie andernfalls wie folgt vor, um den Workflow für Ihren eigenen internen Personalbeschaffungsprozess zu starten.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-135">Otherwise, complete this procedure to begin the workflow for your own internal recruiting process.</span></span>

1. <span data-ttu-id="ab4ac-136">Wählen Sie **Mitarbeiter-Self-Service** aus.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-136">Select **Employee self service**.</span></span>

2. <span data-ttu-id="ab4ac-137">Wählen Sie die Registerkarte **Mein Team** aus.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-137">Select the **My team** tab.</span></span>

3. <span data-ttu-id="ab4ac-138">Wählen Sie **Antrag auf Personalbeschaffung**.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-138">Select  **Request to recruit**.</span></span>

   ![Einen Personalbeschaffungsantrag starten](./media/hr-recruit-1-request-to-recruit.png)

4. <span data-ttu-id="ab4ac-140">Füllen Sie die Felder **Beschreibung**, **Stelle** und **Voraussichtliches Startdatum** aus.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-140">Complete the **Description**, **Job**, and **Estimated start date** fields.</span></span>

   ![Die Personalbeschaffungsanträge vervollständigen](./media/hr-recruit-2-request-to-recruit.png)

5. <span data-ttu-id="ab4ac-142">Wählen Sie **Fortsetzen** aus.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-142">Select **Continue**.</span></span> <span data-ttu-id="ab4ac-143">Der Personalbeschaffungsantrag für Ihre Stelle wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-143">The recruiting request for your position appears.</span></span>

6. <span data-ttu-id="ab4ac-144">Wählen Sie unter **Allgemein** einen Personalbeschaffungsmitarbeiter aus der Dropdownliste **Personalbeschaffungsmitarbeiter** und dann einen Standort aus der Dropdownliste **Standort für Personalbeschaffungsantrag** aus.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-144">Under **General**, select a recruiter from the **Recruiter** dropdown, and then select a location from the **Recruiting request location** dropdown.</span></span>

7. <span data-ttu-id="ab4ac-145">Ändern Sie unter **Stelle** alle Informationen nach Bedarf und wählen Sie dann **Details aus Stelle erstellen**.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-145">Under **Job**, change any information as needed, and then select **Create details from job**.</span></span>

   ![Details aus Stelle erstellen](./media/hr-recruit-3-create-details-from-job.png)

   <span data-ttu-id="ab4ac-147">Der Rest des Personalbeschaffungsantrags wird mit den Standardinformationen für die von Ihnen eingegebene Stelle automatisch ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-147">The rest of the recruiting request will populate with the default information for the job you entered.</span></span>

8. <span data-ttu-id="ab4ac-148">Geben Sie unter **Externe Beschreibung** eine nach außen gerichtete Stellenbeschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-148">Under **External description**, enter an external-facing job description.</span></span>

9. <span data-ttu-id="ab4ac-149">Wählen Sie unter **Positionen** **Hinzufügen** aus und wählen Sie dann eine Position für diesen Personalbeschaffungsantrag aus.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-149">Under **Positions**, select **Add**, and then select a position for this recruiting request.</span></span>

   ![Eine Position hinzufügen](./media/hr-recruit-4-select-position.png)

10. <span data-ttu-id="ab4ac-151">Wählen Sie unter **Qualifikationen** **Hinzufügen** und dann eine Qualifikation aus.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-151">Under **Skills**, select **Add**, and then select a skill.</span></span>

11. <span data-ttu-id="ab4ac-152">Unter **Ausbildungsanforderungen** wählen Sie **Hinzufügen** und dann die Werte aus den Dropdownlisten **Ausbildung** und **Bildungsgrad** aus.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-152">Under **Educational requirements**, select **Add**, and then select values from the **Education** and **Level of education** dropdowns.</span></span>

   ![Ausbildungsanforderungen hinzufügen](./media/hr-recruit-5-select-educational-requirements.png)

12. <span data-ttu-id="ab4ac-154">Fügen Sie unter **Kommentar** notwendige Kommentare ein.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-154">Under **Comment**, add comments as necessary.</span></span>

13. <span data-ttu-id="ab4ac-155">Wählen Sie unter **Vergütung** eine Ebene aus der Dropdownliste **Ebene** aus und passen Sie dann den **Niedrigen Schwellenwert**, den **Kontrollpunkt** und den **Hohen Schwellenwert** wie erforderlich an.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-155">Under **Compensation**, select a level from the **Level** dropdown, and then adjust **Low threshold**, **Control point**, and **High threshold** as necessary.</span></span>

14. <span data-ttu-id="ab4ac-156">Wenn Ihr Personalbeschaffungsantrag fertig ist und Sie bereit sind, den Personalbeschaffungsprozess zu starten, wählen Sie in der Menüleiste **Aktivieren** aus.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-156">When your recruiting request is complete and you're ready to start the recruiting process, select **Activate** in the menu bar.</span></span>

   ![Personalbeschaffungsantrag aktivieren](./media/hr-recruit-6-activate-recruit-request.png)

15. <span data-ttu-id="ab4ac-158">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-158">Select **Save**.</span></span>

## <a name="view-and-edit-your-recruiting-requests"></a><span data-ttu-id="ab4ac-159">Personalbeschaffungsantrag auswählen und bearbeiten</span><span class="sxs-lookup"><span data-stu-id="ab4ac-159">View and edit your recruiting requests</span></span>

<span data-ttu-id="ab4ac-160">Wenn Sie ein Manager sind und sich Ihre eigenen Anträge anzeigen lassen möchten:</span><span class="sxs-lookup"><span data-stu-id="ab4ac-160">If you're a manager and want to view your own requests:</span></span>

1. <span data-ttu-id="ab4ac-161">Wählen Sie **Mitarbeiter-Self-Service** aus.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-161">Select **Employee self service**.</span></span>

2. <span data-ttu-id="ab4ac-162">Wählen Sie die Registerkarte **Mein Team** aus.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-162">Select the **My team** tab.</span></span>

3. <span data-ttu-id="ab4ac-163">Wählen Sie unter **Meine Teaminformationen** die Registerkarte **Personalbeschaffungsanträge** aus.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-163">Under **My team information**, select the **Recruiting requests** tab.</span></span>

   ![Registerkarte Personalbeschaffungsantrag auswählen](./media/hr-recruit-7-recruiting-requests.png)

4. <span data-ttu-id="ab4ac-165">Um einen Personalbeschaffungsantrag anzuzeigen oder zu bearbeiten, wählen Sie ihn im Raster aus.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-165">To view or edit a recruiting request, select it in the grid.</span></span>

<span data-ttu-id="ab4ac-166">Wenn Sie ein Mitarbeiter der Personalverwaltung sind und alle Personalbeschaffungsanträge anzeigen möchten:</span><span class="sxs-lookup"><span data-stu-id="ab4ac-166">If you're an HR pro and want to view all recruiting requests:</span></span>

1. <span data-ttu-id="ab4ac-167">Wählen Sie **Personalverwaltung** aus.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-167">Select **Personnel management**.</span></span>

2. <span data-ttu-id="ab4ac-168">Wählen Sie **Personalbeschaffungsantrag** aus.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-168">Select **Recruiting requests**.</span></span>

   ![Personalbeschaffungsanträge in der Personalverwaltung anzeigen](./media/hr-recruit-8-recruiting-requests-personnel-management.png)

3. <span data-ttu-id="ab4ac-170">Um einen Personalbeschaffungsantrag anzuzeigen oder zu bearbeiten, wählen Sie ihn im Raster aus.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-170">To view or edit a recruiting request, select it in the grid.</span></span>

## <a name="add-or-edit-a-candidate-profile"></a><span data-ttu-id="ab4ac-171">Ein Kandidatenprofil hinzufügen oder bearbeiten</span><span class="sxs-lookup"><span data-stu-id="ab4ac-171">Add or edit a candidate profile</span></span>

<span data-ttu-id="ab4ac-172">Wenn Ihre Organisation für die Verwaltung von Personalbeschaffungsanträge eine Integration mit einer anderen Anwendung vorgenommen hat, werden Personalbeschaffungsanträge an diese Anwendung weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-172">If your organization has integrated with another application to manage recruiting requests, recruiting requests are forwarded to that application.</span></span> <span data-ttu-id="ab4ac-173">Die Personalbeschaffungsanwendung sendet dann Kandidateninformationen zurück an die Personalverwaltung.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-173">The recruiting application then sends candidate information back to Human Resources.</span></span> <span data-ttu-id="ab4ac-174">Andernfalls können Sie Ihre eigenen internen Personalbeschaffungsprozesse nutzen und Kandidateninformationen manuell eingeben.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-174">Otherwise, you can follow your own internal recruiting processes and enter candidate information manually.</span></span>

1. <span data-ttu-id="ab4ac-175">Wählen Sie **Personalverwaltung** aus.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-175">Select **Personnel management**.</span></span>

2. <span data-ttu-id="ab4ac-176">Wählen Sie **Links** aus.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-176">Select **Links**.</span></span>

3. <span data-ttu-id="ab4ac-177">Wählen Sie unter **Personalbeschaffung** **Kandidaten** aus.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-177">Under **Recruiting**, select **Candidates**.</span></span>

   ![Kandidaten anzeigen](./media/hr-recruit-9-candidates.png)

4. <span data-ttu-id="ab4ac-179">Um einen Kandidaten hinzuzufügen, wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-179">To add a candidate, select **New**.</span></span> <span data-ttu-id="ab4ac-180">Um einen vorhandenen Bewerber zu bearbeiten, wählen Sie den Bewerber aus der Liste aus und klicken Sie dann auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-180">To edit an existing candidate, select the candidate from the list and then select **Edit**.</span></span> <span data-ttu-id="ab4ac-181">Das Kandidatenprofil wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-181">The candidate profile appears.</span></span>

5. <span data-ttu-id="ab4ac-182">Geben Sie unter **Kandidatenzusammenfassung** die Kandidateninformationen ein oder bearbeiten Sie sie nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-182">Under **Candidate summary**, enter or edit the candidate information as necessary.</span></span>

6. <span data-ttu-id="ab4ac-183">Wählen Sie unter **Personalbeschaffungsantrag** einen Personalbeschaffungsantrag aus, mit dem der Kandidat verknüpft werden soll.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-183">Under **Recruiting request**, select a recruiting request to link the candidate to.</span></span> <span data-ttu-id="ab4ac-184">Füllen Sie dann die Felder **Voraussichtliches Startdatum**, **Zukünftiger Vorgesetzter**, **Position** und **Beschreibung** entsprechend aus.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-184">Then complete the **Estimated start date**, **Hiring manager**, **Position**, and **Description fields** as appropriate.</span></span>

   ![Personalbeschaffungsantrag verlinken](./media/hr-recruit-10-link-to-recruiting-request.png)

7. <span data-ttu-id="ab4ac-186">Füllen Sie alle Informationen in den folgenden Bereichen aus, die Sie in den Datensatz des Bewerbers aufnehmen möchten:</span><span class="sxs-lookup"><span data-stu-id="ab4ac-186">Complete all the information in the following areas that you want to include in the candidate's record:</span></span>
   - <span data-ttu-id="ab4ac-187">**Kommentare**</span><span class="sxs-lookup"><span data-stu-id="ab4ac-187">**Comments**</span></span>
   - <span data-ttu-id="ab4ac-188">**Berufserfahrung**</span><span class="sxs-lookup"><span data-stu-id="ab4ac-188">**Professional experience**</span></span>
   - <span data-ttu-id="ab4ac-189">**Kontaktinformationen**</span><span class="sxs-lookup"><span data-stu-id="ab4ac-189">**Contact information**</span></span>
   - <span data-ttu-id="ab4ac-190">**Ausbildung**</span><span class="sxs-lookup"><span data-stu-id="ab4ac-190">**Education**</span></span>
   - <span data-ttu-id="ab4ac-191">**Qualifikationen**</span><span class="sxs-lookup"><span data-stu-id="ab4ac-191">**Skills**</span></span>
   - <span data-ttu-id="ab4ac-192">**Bescheinigungen**</span><span class="sxs-lookup"><span data-stu-id="ab4ac-192">**Certificates**</span></span>
   - <span data-ttu-id="ab4ac-193">**Prüfungen**</span><span class="sxs-lookup"><span data-stu-id="ab4ac-193">**Screenings**</span></span>

8. <span data-ttu-id="ab4ac-194">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-194">Select **Save**.</span></span>

## <a name="hire-a-candidate"></a><span data-ttu-id="ab4ac-195">Einen Kandidaten einstellen</span><span class="sxs-lookup"><span data-stu-id="ab4ac-195">Hire a candidate</span></span>

<span data-ttu-id="ab4ac-196">Wenn Sie bereit sind, einen Kandidaten einzustellen, machen Sie den Kandidaten wie folgt zum Mitarbeiter.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-196">When you're ready to hire a candidate, follow this procedure to transition the candidate to an employee.</span></span>

1. <span data-ttu-id="ab4ac-197">Wählen Sie im Kandidatenformular **Einstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-197">On the candidate form, select **Hire**.</span></span>

   ![Einen Kandidaten einstellen](./media/hr-recruit-11-hire.png)

2. <span data-ttu-id="ab4ac-199">Füllen Sie im Formular **Neue Arbeitskraft einstellen** alle Felder unter **Details** aus.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-199">On the **Hire new worker** form, under **Details**, complete all the fields.</span></span>

   ![Details zum neuen Mitarbeiter eingeben](./media/hr-recruit-12-hire-new-worker.png)

3. <span data-ttu-id="ab4ac-201">Überprüfen Sie unter **Positionsdetails** die Angaben und ändern Sie sie bei Bedarf.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-201">Under **Position details**, verify and change information as necessary.</span></span>

4. <span data-ttu-id="ab4ac-202">Wählen Sie unter **Onboarding-Checklisten** die entsprechenden Onboarding-Checklisten für diesen Mitarbeiter aus.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-202">Under **Onboarding checklists**, select the relevant onboarding checklists for this employee.</span></span>

5. <span data-ttu-id="ab4ac-203">Wählen Sie **Fortsetzen** aus, um den Mitarbeiterdatensatz zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-203">Select **Continue** to create the employee record.</span></span>

   >[!NOTE]
   ><span data-ttu-id="ab4ac-204">Je nach den Workflows Ihrer Organisation durchläuft der Kandidatendatensatz zusätzliche Genehmigungsschritte, bevor er zum Mitarbeiterdatensatz wird.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-204">Depending on your organization's workflows, the candidate record may go through additional approval steps before becoming an employee record.</span></span>

## <a name="decide-not-to-hire-a-candidate"></a><span data-ttu-id="ab4ac-205">Einen Kandidaten nicht einstellen</span><span class="sxs-lookup"><span data-stu-id="ab4ac-205">Decide not to hire a candidate</span></span>

<span data-ttu-id="ab4ac-206">Wenn Sie sich entscheiden, einen Kandidaten nicht einzustellen, entfernen Sie ihn wie folgt aus dem Überprüfungsprozess.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-206">If you decide not to hire a candidate, follow this procedure to remove them from the vetting process.</span></span> 

1. <span data-ttu-id="ab4ac-207">Wählen Sie im Kandidatenformular **Nicht einstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-207">On the candidate form, select **Do not hire**.</span></span>

   ![Kandidaten nicht einstellen](./media/hr-recruit-13-do-not-hire.png)

2. <span data-ttu-id="ab4ac-209">Wählen Sie einen **Ursachencode** aus und fügen Sie mögliche Kommentare hinzu.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-209">Select a **Reason code** and include any comments.</span></span>

3. <span data-ttu-id="ab4ac-210">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-210">Select **OK**.</span></span>

## <a name="dismiss-a-candidate"></a><span data-ttu-id="ab4ac-211">Kandidaten entlassen</span><span class="sxs-lookup"><span data-stu-id="ab4ac-211">Dismiss a candidate</span></span>

<span data-ttu-id="ab4ac-212">Bei Bedarf können Sie einen Kandidaten nach der Einstellung wieder entlassen.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-212">If needed, you can dismiss a candidate after hiring them.</span></span> <span data-ttu-id="ab4ac-213">Es kann zum Beispiel sein, dass ein Kandidat Ihr Angebot ablehnt oder am ersten Tag nicht erscheint.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-213">For example, a candidate might reject your offer or not show up on their first day.</span></span>

- <span data-ttu-id="ab4ac-214">Wählen Sie im Kandidatenformular **Kandidat entlassen** aus.</span><span class="sxs-lookup"><span data-stu-id="ab4ac-214">On the candidate form, select **Dismiss candidate**.</span></span>

  ![Kandidat ablehnen](./media/hr-recruit-14-dismiss-candidate.png)

## <a name="see-also"></a><span data-ttu-id="ab4ac-216">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ab4ac-216">See also</span></span>

[<span data-ttu-id="ab4ac-217">Virtuelle Dataverse-Tabellen konfigurieren</span><span class="sxs-lookup"><span data-stu-id="ab4ac-217">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="ab4ac-218">Belegschaft organisieren</span><span class="sxs-lookup"><span data-stu-id="ab4ac-218">Organize your workforce</span></span>](hr-personnel-departments-jobs-positions.md)<br>
[<span data-ttu-id="ab4ac-219">Komponenten eines Einzelvorgangs einrichten</span><span class="sxs-lookup"><span data-stu-id="ab4ac-219">Set up the components of a job</span></span>](hr-personnel-jobs.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
