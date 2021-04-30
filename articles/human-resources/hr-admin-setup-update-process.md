---
title: Aktualisierungsprozess
description: Microsoft Dynamics 365 Human Resources ist ein echter Software-as-a-Service (SaaS), der kontinuierliche, eingriffsfreie Service-Updates für Anwendungs- und Plattformwechsel bietet.
author: andreabichsel
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-27
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ca8868069fca4453efbb76694702a554da6d7aa6
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892274"
---
# <a name="update-process"></a><span data-ttu-id="bc9e5-103">Aktualisierungsprozess</span><span class="sxs-lookup"><span data-stu-id="bc9e5-103">Update process</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="bc9e5-104">Microsoft Dynamics 365 Human Resources ist eine echte Software-as-a-Service (SaaS), die kontinuierliche, berührungslose Dienstupdates bietet.</span><span class="sxs-lookup"><span data-stu-id="bc9e5-104">Microsoft Dynamics 365 Human Resources is a true software as a service (SaaS) that provides continuous, touchless service updates.</span></span> <span data-ttu-id="bc9e5-105">Diese Updates enthalten sowohl Anwendungs‑ als auch Plattformänderungen, die häufig wichtige Verbesserungen des Dienstes bewirken, einschließlich rechtlicher Aktualisierungen.</span><span class="sxs-lookup"><span data-stu-id="bc9e5-105">These updates contain both application and platform changes that often provide critical improvements to the service, including regulatory updates.</span></span>

## <a name="update-policy"></a><span data-ttu-id="bc9e5-106">Updaterichtlinie</span><span class="sxs-lookup"><span data-stu-id="bc9e5-106">Update policy</span></span>

<span data-ttu-id="bc9e5-107">Aktualisierungen werden in regelmäßigen Abständen in allen Umgebungen veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="bc9e5-107">Updates are released on a regular cadence to all environments.</span></span> <span data-ttu-id="bc9e5-108">Human Resources wird entsprechend der [Microsoft Lifecycle-Richtlinie](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy) unterstützt, die einen konsistenten und voraussehbaren Leitfaden für die Supportverfügbarkeit bietet.</span><span class="sxs-lookup"><span data-stu-id="bc9e5-108">Human Resources is supported according to the [Microsoft Lifecycle policy](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy), which provides consistent and predictable guidelines for the availability of support.</span></span>

## <a name="release-cadence"></a><span data-ttu-id="bc9e5-109">Veröffentlichungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="bc9e5-109">Release cadence</span></span> 

<span data-ttu-id="bc9e5-110">Human Resources-Aktualisierungen werden automatisch auf alle Umgebungen angewendet.</span><span class="sxs-lookup"><span data-stu-id="bc9e5-110">Human Resources updates are applied to all environments automatically.</span></span> <span data-ttu-id="bc9e5-111">Human Resources bietet zwei Versionstypen:</span><span class="sxs-lookup"><span data-stu-id="bc9e5-111">Human Resources provides two types of releases:</span></span>

- <span data-ttu-id="bc9e5-112">**Dienstupdates**: Updates finden alle zwei Wochen staat und enthalten Fehlerkorrekturen und neuen Funktionen.</span><span class="sxs-lookup"><span data-stu-id="bc9e5-112">**Service updates**: Updates occur every two weeks that include bug fixes and new features.</span></span> <span data-ttu-id="bc9e5-113">Zu den Dienstupdates gehören auch relevante veröffentlichte Plattformupdates.</span><span class="sxs-lookup"><span data-stu-id="bc9e5-113">Service updates also include applicable Platform updates when they release.</span></span> <span data-ttu-id="bc9e5-114">Informationen zum Zeitpunkt der Veröffentlichung von Plattformupdates finden Sie unter [Tabelle 3: Plattformfreigaben](../fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy.md#table-3-platform-releases).</span><span class="sxs-lookup"><span data-stu-id="bc9e5-114">To get an idea of when Platform updates are released, see [Table 3: Platform releases](../fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy.md#table-3-platform-releases).</span></span> <span data-ttu-id="bc9e5-115">Zweiwöchentliche Updates werden in allen Regionen global eingeführt.</span><span class="sxs-lookup"><span data-stu-id="bc9e5-115">Biweekly updates have a staged global rollout across regions.</span></span> <span data-ttu-id="bc9e5-116">Weitere Informationen zu zweiwöchentlichen Updates finden Sie unter [Neuerungen oder Änderungen in Dynamics 365 Human Resources](hr-admin-whats-new.md).</span><span class="sxs-lookup"><span data-stu-id="bc9e5-116">For more information about biweekly updates, see [What's new or changed in Dynamics 365 Human Resources](hr-admin-whats-new.md).</span></span>

    <span data-ttu-id="bc9e5-117">Alle unterstützten Rechenzentren werden alle zwei Wochen aktualisiert, sofern nicht anders angegeben.</span><span class="sxs-lookup"><span data-stu-id="bc9e5-117">All supported data centers update every two weeks, unless otherwise noted.</span></span> <span data-ttu-id="bc9e5-118">In den USA, Australien, Europa, Vereinigtes Königreich, Asien und Kanada finden zweiwöchentliche Updates statt.</span><span class="sxs-lookup"><span data-stu-id="bc9e5-118">US, Australia, Europe, UK, Asia, and Canada regions are included in biweekly updates.</span></span> 

- <span data-ttu-id="bc9e5-119">**Dataverse-Lösungsupdates**: Diese Updates werden nach Bedarf etwa alle sechs Wochen durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="bc9e5-119">**Dataverse solution updates**: These updates occur approximately every six weeks, as needed.</span></span> <span data-ttu-id="bc9e5-120">Dazu gehören neue Entitäten und Änderungen an vorhandenen Entitäten in Dataverse.</span><span class="sxs-lookup"><span data-stu-id="bc9e5-120">They include new entities and changes to existing entities in Dataverse.</span></span> <span data-ttu-id="bc9e5-121">Diese Updates werden in denselben Regionen wie die zweiwöchentlichen Updates veröffentlicht. Die Replikation in allen Rechenzentren dauert ungefähr sechs Wochen.</span><span class="sxs-lookup"><span data-stu-id="bc9e5-121">These updates release to the same regions as the biweekly updates, and they take about six weeks to replicate through all data centers.</span></span> <span data-ttu-id="bc9e5-122">Lösungsupdates stimmen möglicherweise mit zweiwöchentlichen Dienstupdates überein.</span><span class="sxs-lookup"><span data-stu-id="bc9e5-122">Solution updates may or may not align with biweekly service updates.</span></span>

> [!NOTE]
> <span data-ttu-id="bc9e5-123">Lösungsupdates sind in allen Rechenzentren verfügbar, sobald sie veröffentlicht wurden.</span><span class="sxs-lookup"><span data-stu-id="bc9e5-123">Solution updates are available on all data centers once they're released.</span></span> <span data-ttu-id="bc9e5-124">Wenn Sie nicht darauf warten möchten, dass die Updates automatisch repliziert werden, können Sie diese Updates in jeder Umgebung in jedem Rechenzentrum manuell anwenden.</span><span class="sxs-lookup"><span data-stu-id="bc9e5-124">If you don't want to wait for the updates to replicate automatically, you can manually apply these updates on any environment in any data center.</span></span>

<span data-ttu-id="bc9e5-125">Bei Bedarf bietet Human Resources auch die folgenden Fehlerkorrekturtypen:</span><span class="sxs-lookup"><span data-stu-id="bc9e5-125">When needed, Human Resources also provides the following types of fixes:</span></span>

- <span data-ttu-id="bc9e5-126">**Überarbeitung (Hotfix)**: Fehlerkorrekturen, die mit oder außerhalb eines zweiwöchentliches Dienstupdates auftreten können</span><span class="sxs-lookup"><span data-stu-id="bc9e5-126">**Revision (hotfix)**: Bug fixes that can occur either with or apart from a biweekly service update release</span></span>

- <span data-ttu-id="bc9e5-127">**Notfall-Fix**: Proaktive und reaktive eigenständige Hotfixes, können Nur-Konfigurations‑ oder Codeänderungen zur Behebung von Problemen mit der Live-Site enthalten und unabhängig von einem zweiwöchentlichen Dienstupdate auftreten</span><span class="sxs-lookup"><span data-stu-id="bc9e5-127">**Emergency fix**: Proactive and reactive hotfixes that are standalone in nature, can include configuration-only or code changes to resolve live site issues, and can occur apart from a biweekly service update release</span></span>

<span data-ttu-id="bc9e5-128">Versionen werden in einer internen Umgebung überprüft, getestet und validiert.</span><span class="sxs-lookup"><span data-stu-id="bc9e5-128">Releases are reviewed, tested, and validated on an internal environment.</span></span> <span data-ttu-id="bc9e5-129">Nachdem die Builds genehmigt wurden, werden sie für die Produktion bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="bc9e5-129">After builds are signed off, they're then deployed to production.</span></span>

## <a name="release-cadence-exceptions-in-2021"></a><span data-ttu-id="bc9e5-130">Freigabe von Trittfrequenzausnahmen im Jahr 2021</span><span class="sxs-lookup"><span data-stu-id="bc9e5-130">Release cadence exceptions in 2021</span></span>

<span data-ttu-id="bc9e5-131">Um die Feiertage zu berücksichtigen, sieht der Veröffentlichungsplan für November und Dezember 2021 wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="bc9e5-131">To account for holidays, the release schedule for November and December 2021 is as follows:</span></span>

- <span data-ttu-id="bc9e5-132">November-Veröffentlichung: 1. November – 14. November</span><span class="sxs-lookup"><span data-stu-id="bc9e5-132">November release: November 1 - November 14</span></span>
- <span data-ttu-id="bc9e5-133">Dezember-Veröffentlichung: 29. November – 12. Dezember</span><span class="sxs-lookup"><span data-stu-id="bc9e5-133">December release: November 29 - December 12</span></span>
 
<span data-ttu-id="bc9e5-134">Die zweiwöchige Veröffentlichungshäufigkeit wird wie gewohnt am 10. Januar 2022 wieder aufgenommen.</span><span class="sxs-lookup"><span data-stu-id="bc9e5-134">The two-week release cadence will resume as usual on January 10, 2022.</span></span>

## <a name="communications"></a><span data-ttu-id="bc9e5-135">Kommunikation</span><span class="sxs-lookup"><span data-stu-id="bc9e5-135">Communications</span></span>

<span data-ttu-id="bc9e5-136">Hier können Sie herausfinden, was für Human Resources in Arbeit ist und was wir veröffentlicht haben:</span><span class="sxs-lookup"><span data-stu-id="bc9e5-136">You can find out what's in the works for Human Resources and what we've released in the following locations:</span></span>

- [<span data-ttu-id="bc9e5-137">Dynamics 365 Human Resources-Produktplan</span><span class="sxs-lookup"><span data-stu-id="bc9e5-137">Dynamics 365 Human Resources roadmap</span></span>](https://dynamics.microsoft.com/roadmap/human-resources/)

- [<span data-ttu-id="bc9e5-138">Dynamics 365-Veröffentlichungspläne</span><span class="sxs-lookup"><span data-stu-id="bc9e5-138">Dynamics 365 Release Plans</span></span>](/dynamics365/release-plans/)

- [<span data-ttu-id="bc9e5-139">Was ist neu oder geändert in Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="bc9e5-139">What's new or changed in Dynamics 365 Human Resources</span></span>](hr-admin-whats-new.md)

- <span data-ttu-id="bc9e5-140">[Problemsuche in Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs.md) (nur für plattformbezogene Fehler)</span><span class="sxs-lookup"><span data-stu-id="bc9e5-140">[Issue search in Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs.md) (for Platform-related bugs only)</span></span>

- [<span data-ttu-id="bc9e5-141">Human Resources-Blog</span><span class="sxs-lookup"><span data-stu-id="bc9e5-141">Human Resources blog</span></span>](https://community.dynamics.com/365/talent/b/dynamics365fortalent)

- [<span data-ttu-id="bc9e5-142">Human Resources Yammer-Community</span><span class="sxs-lookup"><span data-stu-id="bc9e5-142">Human Resources Yammer community</span></span>](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=10542230)

## <a name="preview-features-in-a-sandbox-environment"></a><span data-ttu-id="bc9e5-143">Vorschaufunktionen in einer Sandkastenumgebung</span><span class="sxs-lookup"><span data-stu-id="bc9e5-143">Preview features in a sandbox environment</span></span>

<span data-ttu-id="bc9e5-144">Sie können Vorschaufunktionen in einer Sandkastenumgebung überprüfen, bevor Sie sie in Ihrer Produktionsumgebung aktivieren.</span><span class="sxs-lookup"><span data-stu-id="bc9e5-144">You can validate preview features in a sandbox environment before enabling them in your production environment.</span></span> <span data-ttu-id="bc9e5-145">Weitere Informationen zur Aktivierung von Funktionen finden Sie unter [Funktionsverwaltungsüberblick](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="bc9e5-145">For more information about enabling features, see [Feature management overview](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

<span data-ttu-id="bc9e5-146">Alle neuen Funktionen bleiben mindestens 30 Tage und in der Regel 30-60 Tage in der Vorschau.</span><span class="sxs-lookup"><span data-stu-id="bc9e5-146">All new features remain in preview for at least 30 days, and typically 30-60 days.</span></span> <span data-ttu-id="bc9e5-147">Die wichtigsten Funktionen sind in der Regel im Oktober und April eines jeden Jahres nach dem Vorschauzeitraum verfügbar.</span><span class="sxs-lookup"><span data-stu-id="bc9e5-147">Major features are generally available in October and April of each year following the preview period.</span></span> <span data-ttu-id="bc9e5-148">Sobald Sie neue Funktionen im Arbeitsbereich Feature-Management sehen, können Sie diese einschalten.</span><span class="sxs-lookup"><span data-stu-id="bc9e5-148">As soon as you see new capabilities in the Feature management workspace, you can turn them on.</span></span> <span data-ttu-id="bc9e5-149">Einige Funktionen sind möglicherweise standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="bc9e5-149">Some features may be on by default.</span></span>

<span data-ttu-id="bc9e5-150">Manchmal ist ein integrales Feature standardmäßig eingeschaltet und kann nicht deaktiviert werden (z.B. das Feature-Management Arbeitsbereich).</span><span class="sxs-lookup"><span data-stu-id="bc9e5-150">At times, an integral feature will be on by default and can't be turned off (for example, the Feature management workspace).</span></span>

<span data-ttu-id="bc9e5-151">Sobald eine Funktion allgemein verfügbar ist, kann sie in Produktionsumgebungen ein- und ausgeschaltet werden.</span><span class="sxs-lookup"><span data-stu-id="bc9e5-151">Once a feature is generally available, it may be turned on or off in production environments.</span></span> <span data-ttu-id="bc9e5-152">Der Arbeitsbereich Feature-Management zeigt an, wann eine Vorschaufunktion obligatorisch wird.</span><span class="sxs-lookup"><span data-stu-id="bc9e5-152">The Feature management workspace indicates when a preview feature will become mandatory.</span></span> <span data-ttu-id="bc9e5-153">Dieses Datum ist in der Regel der 1. Oktober oder 1. April, um mit den halbjährlichen Release-Plänen übereinzustimmen.</span><span class="sxs-lookup"><span data-stu-id="bc9e5-153">This date is usually on October 1 or April 1 to align with the semiannual release plans.</span></span> <span data-ttu-id="bc9e5-154">Sie können obligatorische Funktionen nicht deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="bc9e5-154">You can't turn off mandatory features.</span></span> <span data-ttu-id="bc9e5-155">Bis es obligatorisch wird, können Sie eine Funktion in allen Umgebungen ein- und ausschalten.</span><span class="sxs-lookup"><span data-stu-id="bc9e5-155">Until it becomes mandatory, you can turn a feature on and off in all environments.</span></span>

<span data-ttu-id="bc9e5-156">Es wird dringend empfohlen, eine Vorschau der Funktionen in einer Sandkasten‑ oder Testumgebung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="bc9e5-156">We highly recommend previewing features in a sandbox or trial environment.</span></span> <span data-ttu-id="bc9e5-157">Erstellen Sie am besten eine Kopie Ihrer aktuellen Produktionsumgebung oder Datenbank in einer Sandkastenumgebung, damit Sie die neuen Funktionen mit Ihren Daten optimal nutzen können.</span><span class="sxs-lookup"><span data-stu-id="bc9e5-157">It's best to create a copy of your current production environment or database into a sandbox environment so you can get the complete experience of the new features with your data.</span></span>

<span data-ttu-id="bc9e5-158">Weitere Informationen zum Bereitstellen einer Sandkastenumgebung finden Sie unter [Human Resources-Projekt bereitstellen](hr-admin-setup-provision.md).</span><span class="sxs-lookup"><span data-stu-id="bc9e5-158">For more information about provisioning a sandbox environment, see [Provision a Human Resources project](hr-admin-setup-provision.md).</span></span> <span data-ttu-id="bc9e5-159">Informationen zum Entfernen einer Testumgebung finden Sie unter [Instanz entfernen](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment).</span><span class="sxs-lookup"><span data-stu-id="bc9e5-159">To remove a test environment, see [Remove an instance](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment).</span></span> 

## <a name="report-bugs"></a><span data-ttu-id="bc9e5-160">Fehler melden</span><span class="sxs-lookup"><span data-stu-id="bc9e5-160">Report bugs</span></span>

<span data-ttu-id="bc9e5-161">Beim Testen der Vorschaufunktionen oder neuer Funktionen werden möglicherweise Elemente gefunden, die nicht wie erwartet funktionieren.</span><span class="sxs-lookup"><span data-stu-id="bc9e5-161">While testing preview features or trying new capabilities, you might find items that don't work as expected.</span></span> <span data-ttu-id="bc9e5-162">Bitte melden Sie alle Fehler dem [Microsoft Dynamics 365 Support](https://dynamics.microsoft.com/support/).</span><span class="sxs-lookup"><span data-stu-id="bc9e5-162">Please report any bugs through [Microsoft Dynamics 365 support](https://dynamics.microsoft.com/support/).</span></span>

## <a name="see-also"></a><span data-ttu-id="bc9e5-163">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc9e5-163">See also</span></span>

[<span data-ttu-id="bc9e5-164">Dynamics 365 und Power Platform-Versionsveröffentlichungspläne</span><span class="sxs-lookup"><span data-stu-id="bc9e5-164">Dynamics 365 and Power Platform Release Plans</span></span>](/dynamics365/release-plans)</br>
[<span data-ttu-id="bc9e5-165">Neuerungen oder Änderungen in Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="bc9e5-165">What's new or changed in Dynamics 365 Human Resource</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="bc9e5-166">Software-Lebenszyklusrichtlinie</span><span class="sxs-lookup"><span data-stu-id="bc9e5-166">Software lifecycle policy</span></span>](../fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]