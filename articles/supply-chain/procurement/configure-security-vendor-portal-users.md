---
title: Kreditorenportalbenutzersicherheit
description: "In diesem Artikel wird beschrieben, wie Sie die Sicherheit für externe Kreditoren einrichten, die das Kreditorenportal verwenden. Diese Informationen gelten nur für die Versionen Februar 2016 &amp; und Mai 2016 von Dynamics AX."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysUserManagement
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 30231
ms.assetid: 3574db17-81c7-4c5a-999b-0098aa0b9cda
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: ab096bcc7003f60851077d9c7e03b16c5d46ce2a
ms.contentlocale: de-de
ms.lasthandoff: 08/29/2017

---

# <a name="vendor-portal-user-security"></a><span data-ttu-id="a7960-104">Kreditorenportalbenutzersicherheit</span><span class="sxs-lookup"><span data-stu-id="a7960-104">Vendor portal user security</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="a7960-105">In diesem Artikel wird beschrieben, wie Sie die Sicherheit für externe Kreditoren einrichten, die das Kreditorenportal verwenden.</span><span class="sxs-lookup"><span data-stu-id="a7960-105">This article explains how to set up security for external vendors who use the Vendor portal.</span></span> <span data-ttu-id="a7960-106">Diese Informationen gelten nur für die Versionen Februar 2016 &amp; und Mai 2016 von Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="a7960-106">This information applies only to the February 2016 &amp; May 2016 versions of Dynamics AX.</span></span>

<span data-ttu-id="a7960-107">Die Kreditorenportalfunktion wurde durch die erweiterte Kreditorenzusammenarbeitfunktion in Dynamics 365 for Operations Version 1611 ersetzt.</span><span class="sxs-lookup"><span data-stu-id="a7960-107">The Vendor portal functionality has been replaced by extended vendor collaboration functionality in Dynamics 365 for Operations version 1611.</span></span> <span data-ttu-id="a7960-108">Weitere Informationen zur Einrichtung der Sicherheit für Kreditorenzusammenarbeit finden Sie unter [Konfiguration und Verwaltung der Sicherheit für Kreditorenzusammenarbeit](set-up-maintain-vendor-collaboration.md)</span><span class="sxs-lookup"><span data-stu-id="a7960-108">For more information about setting up security for vendor collaboration, see [Set up and maintain vendor collaboration](set-up-maintain-vendor-collaboration.md).</span></span> <span data-ttu-id="a7960-109">Das Kreditorenportal macht einen begrenzten Satz von Informationen zu Bestellungen (POs) für externe Kreditoren verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a7960-109">The Vendor portal exposes a limited set of information about purchase orders (POs) to external vendors.</span></span> <span data-ttu-id="a7960-110">Es ist wichtig, dass Sie die Benutzerrechte für das Kreditorenportal in Microsoft Dynamics AX ordnungsgemäß einrichten, damit Kreditoren nicht unerwünschten Zugriff auf zusätzliche Informationen in Ihrer Dynamics AX-Installation haben.</span><span class="sxs-lookup"><span data-stu-id="a7960-110">It's important that you correctly set up user permissions for the Vendor portal in Microsoft Dynamics AX, so that vendors don't have unintended access to additional information in your Dynamics AX installation.</span></span> <span data-ttu-id="a7960-111">**Wichtig:** Im Gegensatz zu anderen Benutzer sollten externe Kreditoren nicht die Rolle **SystemUser** haben.</span><span class="sxs-lookup"><span data-stu-id="a7960-111">**Important:** Unlike other users, external vendors should not have the **SystemUser** role.</span></span> <span data-ttu-id="a7960-112">Die Rolle **SystemUser** gewährt Zugriff auf eine Reihe von Rechten, die nicht für externe Benutzer geeignet sind.</span><span class="sxs-lookup"><span data-stu-id="a7960-112">The **SystemUser** role grants access to a set of privileges that aren't suitable for external users.</span></span>

## <a name="setting-up-a-vendor-portal-user"></a><span data-ttu-id="a7960-113">Einrichten eines Kreditorenportalbenutzers</span><span class="sxs-lookup"><span data-stu-id="a7960-113">Setting up a Vendor portal user</span></span>
<span data-ttu-id="a7960-114">Bevor Sie ein Benutzerkonto für jemanden, der das Kreditorenportal verwenden wird, erstellen, müssen Sie den Kreditor einrichten, um eine Kreditorenportalzusammenarbeit zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="a7960-114">Before you create a user account for someone who will use the Vendor portal, you must set up the vendor to allow for Vendor portal collaboration.</span></span> <span data-ttu-id="a7960-115">Verwenden Sie das Feld **Bestellungszusammenarbeit** auf der Registerkarte **Allgemeines** auf der Seite **Kreditoren**.</span><span class="sxs-lookup"><span data-stu-id="a7960-115">Use the **Purchase order collaboration** field on the **General** tab on the **Vendors** page.</span></span> <span data-ttu-id="a7960-116">Externe Kreditoren, die das Kreditorenportal verwenden, müssen die folgenden Einstellungen haben:</span><span class="sxs-lookup"><span data-stu-id="a7960-116">External vendors that use the Vendor portal must have the following setup:</span></span>

-   <span data-ttu-id="a7960-117">Ein Microsoft Azures Active Directory(AAD)-Benutzerkonto muss für den Kreditor auf der Seite **Benutzer** in Dynamics AX registriert werden.</span><span class="sxs-lookup"><span data-stu-id="a7960-117">A Microsoft Azure Active Directory (AAD) user account must be registered for the vendor on the **Users** page in Dynamics AX.</span></span>
-   <span data-ttu-id="a7960-118">Der Kreditor muss die Sicherheitsrolle **Kreditor (extern)** und nicht die Rolle **SystemUser** haben.</span><span class="sxs-lookup"><span data-stu-id="a7960-118">The vendor must have the **Vendor (external)** security role, not the **SystemUser** role.</span></span> <span data-ttu-id="a7960-119">**Hinweis:** Die Rolle **SystemUser** wird automatisch gewährt, wenn Sie ein neues Benutzerkonto in Dynamics AX erstellen.</span><span class="sxs-lookup"><span data-stu-id="a7960-119">**Note:** The **SystemUser** role is automatically granted when you create a new user account in Dynamics AX.</span></span> <span data-ttu-id="a7960-120">Daher müssen Sie diese Rolle entfernen und die Warnmeldung bestätigen, die Sie erhalten.</span><span class="sxs-lookup"><span data-stu-id="a7960-120">Therefore, you must remove that role and acknowledge the warning message that you receive.</span></span>
-   <span data-ttu-id="a7960-121">Dem Kreditorenbenutzer sollte keine Berechtigung erteilt werden, zusätzliche Felder aus den Bestellungstabellen zu seiner Ansicht der Bestellung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="a7960-121">The vendor user should not be granted permission to add additional fields from the PO tables to their view of the PO.</span></span> <span data-ttu-id="a7960-122">Legen Sie auf der Registerkarte **Benutzereinstellungen** auf der Registerkarte **Benutzer** die Option **Zulässige explizite Personalisierung** für den Benutzer auf **Nein** fest.</span><span class="sxs-lookup"><span data-stu-id="a7960-122">On the **Personalization** tab, on the **Users** tab, set the **Explicit personalization allowed** option for the user to **No**.</span></span>
-   <span data-ttu-id="a7960-123">Das Benutzerkonto muss einer registrierten Kontaktperson zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="a7960-123">The user account must be associated with a registered contact person.</span></span> <span data-ttu-id="a7960-124">Wählen Sie auf der Seite **Benutzer** eine Kontaktperson im Feld **Name** aus.</span><span class="sxs-lookup"><span data-stu-id="a7960-124">On the **Users** page, select a contact person in the **Name** field.</span></span> <span data-ttu-id="a7960-125">Die Person, die Sie auswählen, sollte die Rolle **Kontakt** für den relevanten Kreditor haben.</span><span class="sxs-lookup"><span data-stu-id="a7960-125">The person that you select should have the **Contact** role for the relevant vendor.</span></span>

<span data-ttu-id="a7960-126">Wenn die gleiche Person Zugriff auf das Kreditorenportal für mehrere Kreditorenkontos (eventuell für unterschiedliche juristische Personen) benötigt, muss jedes der Benutzerkonten dieser Person derselben registrierten Kontaktperson zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="a7960-126">If the same person requires access to the Vendor portal for multiple vendor accounts (for different legal entities, perhaps), each of that person's user accounts must be associated with the same registered contact person.</span></span> <span data-ttu-id="a7960-127">Die Rolle **Kreditor (extern)** umfasst alle grundlegenden Funktionen, die erforderlich sind, um die Funktionen zu verwenden, die im Kreditorenportal verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="a7960-127">The **Vendor (external)** role includes all the basic capabilities that are required in order to use the functionality that is available in the Vendor portal.</span></span> <span data-ttu-id="a7960-128">Durch diese Einstellung wird sichergestellt, dass die Benutzeroberfläche, die der externe Benutzer sieht, ausschließlich auf das gewünschte Szenario fokussiert ist.</span><span class="sxs-lookup"><span data-stu-id="a7960-128">This setup helps guarantee that the user interface that the external user sees is focused on the intended scenario only.</span></span>

<a name="see-also"></a><span data-ttu-id="a7960-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a7960-129">See also</span></span>
--------

[<span data-ttu-id="a7960-130">Kreditor-Zusammenarbeit</span><span class="sxs-lookup"><span data-stu-id="a7960-130">Vendor collaboration</span></span>](collaborate-vendors-vendor-portal.md)




