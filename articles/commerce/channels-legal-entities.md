---
title: Erstellen juristischer Personen
description: In diesem Thema wird beschrieben, wie Sie juristische Personen in Microsoft Dynamics 365 Commerce erstellen, die erstellt und konfiguriert werden müssen, bevor Kanäle erstellt werden.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 28cbcc42505f1dc90c420adc812735841541c8e0
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002403"
---
# <a name="create-legal-entities"></a><span data-ttu-id="db43f-103">Erstellen juristischer Personen</span><span class="sxs-lookup"><span data-stu-id="db43f-103">Create legal entities</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="db43f-104">In diesem Thema wird beschrieben, wie Sie juristische Personen in Microsoft Dynamics 365 Commerce erstellen, die erstellt und konfiguriert werden müssen, bevor Kanäle erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="db43f-104">This topic describes how to create legal entities in Microsoft Dynamics 365 Commerce, which must be created and configured before creating channels.</span></span>

## <a name="overview"></a><span data-ttu-id="db43f-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="db43f-105">Overview</span></span>

<span data-ttu-id="db43f-106">Eine juristische Person ist eine Organisation mit einer registrierten oder eingetragenen Rechtsform.</span><span class="sxs-lookup"><span data-stu-id="db43f-106">A legal entity is an organization that has a registered or legislated legal structure.</span></span> <span data-ttu-id="db43f-107">Juristische Personen können Verträge abschließen und sind verpflichtet, Finanzaufstellungen zum Erstellen eines Berichts über ihre Vermögens-, Finanz- und Ertragslage vorzubereiten.</span><span class="sxs-lookup"><span data-stu-id="db43f-107">Legal entities can enter into legal contracts and are required to prepare statements that report on their performance.</span></span>

<span data-ttu-id="db43f-108">Ein Unternehmen ist eine Art von juristischer Person.</span><span class="sxs-lookup"><span data-stu-id="db43f-108">A company is a type of legal entity.</span></span> <span data-ttu-id="db43f-109">Derzeit sind Unternehmen die einzige Art von juristischer Person, die Sie erstellen können, und jeder juristischen Person ist eine Unternehmenskennung zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="db43f-109">Currently, companies are the only kind of legal entity that you can create, and every legal entity is associated with a company ID.</span></span> <span data-ttu-id="db43f-110">Diese Zuordnung ist notwendig, da einige Funktionsbereiche im Programm eine Unternehmenskennung (oder *DataAreaId*) in den Datenmodellen verwenden.</span><span class="sxs-lookup"><span data-stu-id="db43f-110">This association exists because some functional areas in the program use a company ID, or *DataAreaId*, in their data models.</span></span> <span data-ttu-id="db43f-111">In diesen Funktionsbereichen werden Unternehmen als Grenze für die Datensicherheit verwendet.</span><span class="sxs-lookup"><span data-stu-id="db43f-111">In these functional areas, companies are used as a boundary for data security.</span></span> <span data-ttu-id="db43f-112">Benutzer können nur auf Daten für das Unternehmen zugreifen, bei dem sie derzeit angemeldet sind.</span><span class="sxs-lookup"><span data-stu-id="db43f-112">Users can access data only for the company that they are currently logged on to.</span></span> 

<span data-ttu-id="db43f-113">Beim Erstellen eines Kanals müssen Sie angeben, zu welcher juristischen Person dieser Kanal gehört.</span><span class="sxs-lookup"><span data-stu-id="db43f-113">When creating a channel, you must specify which legal entity that channel belongs to.</span></span>

## <a name="create-a-new-legal-entity"></a><span data-ttu-id="db43f-114">Eine neue juristische Person erstellen</span><span class="sxs-lookup"><span data-stu-id="db43f-114">Create a new legal entity</span></span>

<span data-ttu-id="db43f-115">Gehen Sie folgendermaßen vor, um eine neue juristische Person in Dynamics 365 Commerce zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="db43f-115">To create a new legal entity in Dynamics 365 Commerce, follow these steps.</span></span>

1. <span data-ttu-id="db43f-116">Gehen Sie im Navigationsbereich zu **Module \> Hauptsitz einrichten \> Juristische Personen**.</span><span class="sxs-lookup"><span data-stu-id="db43f-116">In the navigation pane, go to  **Modules \> Headquarters setup \> Legal entities**.</span></span>
1. <span data-ttu-id="db43f-117">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="db43f-117">On the action pane, select **New**.</span></span> <span data-ttu-id="db43f-118">Das Fenster **Neue juristische Person** wird rechts angezeigt.</span><span class="sxs-lookup"><span data-stu-id="db43f-118">The **New legal entity** pane appears on the right.</span></span>
1. <span data-ttu-id="db43f-119">Geben Sie im Feld **Name** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="db43f-119">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="db43f-120">Geben Sie im Feld **Unternehmen** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="db43f-120">In the **Company** field, enter a value.</span></span>
1. <span data-ttu-id="db43f-121">Wählen Sie im Feld **Land/Region** einen Wert aus, oder geben Sie einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="db43f-121">In the **Country/region** field, enter or select a value.</span></span>
1. <span data-ttu-id="db43f-122">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="db43f-122">Select **OK**.</span></span> 

   ![Erstellung einer juristischen Person](media/legal-entities.png)

1. <span data-ttu-id="db43f-124">Stellen Sie im Abschnitt **Allgemein** die folgenden allgemeinen Informationen zur juristischen Person bereit:</span><span class="sxs-lookup"><span data-stu-id="db43f-124">In the **General** section, provide the following general information about the legal entity:</span></span> 
   1. <span data-ttu-id="db43f-125">Geben Sie einen Suchbegriff ein, falls erforderlich.</span><span class="sxs-lookup"><span data-stu-id="db43f-125">Enter a search name, if a search name is required.</span></span> <span data-ttu-id="db43f-126">Ein Suchbegriff ist ein alternativer Name, der verwendet werden kann, um nach dieser juristischen Person zu suchen.</span><span class="sxs-lookup"><span data-stu-id="db43f-126">A search name is an alternate name that can be used to search for this legal entity.</span></span> 
   1. <span data-ttu-id="db43f-127">Wählen Sie aus, ob diese juristische Person als Konsolidierungsunternehmen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="db43f-127">Select whether this legal entity is being used as a consolidation company.</span></span>
   1. <span data-ttu-id="db43f-128">Wählen Sie aus, ob diese juristische Person als Unternehmen mit Löschungseinträgen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="db43f-128">Select whether this legal entity is being used as an elimination company.</span></span> 
   1. <span data-ttu-id="db43f-129">Wählen Sie die **Standardsprache** für die Entität aus.</span><span class="sxs-lookup"><span data-stu-id="db43f-129">Select the **default language** for the entity.</span></span> 
   1. <span data-ttu-id="db43f-130">Wählen Sie die **Zeitzone** für die Entität aus.</span><span class="sxs-lookup"><span data-stu-id="db43f-130">Select the **time zone** for the entity.</span></span>
1. <span data-ttu-id="db43f-131">Wählen Sie im Abschnitt **Adressen** die Option **Bearbeiten**, um die Adressinformationen wie die Straße und Hausnummer, die Postleitzahl und den Ort einzugeben.</span><span class="sxs-lookup"><span data-stu-id="db43f-131">In the **Addresses** section, select **Edit** to enter address information, such as the street name and number, postal code, and city.</span></span>
1. <span data-ttu-id="db43f-132">Geben Sie im Abschnitt **Kontaktinformationen** Informationen zu den Kommunikationsmethoden ein, wie beispielsweise E-Mail-Adressen, URLs und Telefonnummern.</span><span class="sxs-lookup"><span data-stu-id="db43f-132">In the **Contact information** section, enter information about methods of communication, such as email addresses, URLs, and telephone numbers.</span></span>
1. <span data-ttu-id="db43f-133">Geben Sie im Abschnitt **Offenlegungspflicht** die Registrierungsnummern ein, die für die Offenlegungspflicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="db43f-133">In the **Statutory reporting** section, enter the registration numbers that are used for statutory reporting.</span></span>
1. <span data-ttu-id="db43f-134">Geben Sie im Abschnitt **Registrierungsnummern** alle Informationen ein, die für die juristische Person erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="db43f-134">In the **Registration numbers** section, enter any information required by the legal entity.</span></span>
1. <span data-ttu-id="db43f-135">Geben Sie im Abschnitt **Bankkontinformationen** die Bankkonten und Bankleitzahlen für die juristische Person ein.</span><span class="sxs-lookup"><span data-stu-id="db43f-135">In the **Bank account information** section, enter bank accounts and routing numbers for the legal entity.</span></span>
1. <span data-ttu-id="db43f-136">Geben Sie im Abschnitt **Außenhandel und Logistik** die Versandinformationen für die juristische Person ein.</span><span class="sxs-lookup"><span data-stu-id="db43f-136">In the **Foreign trade and logistics** section, enter shipping information for the legal entity.</span></span>
1. <span data-ttu-id="db43f-137">Im Abschnitt **Nummernkreise** können Sie die Nummernkreise anzeigen, die der juristischen Person zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="db43f-137">In the **Number sequences** section, you can view the number sequences that are associated with the legal entity.</span></span> <span data-ttu-id="db43f-138">Dies ist zunächst leer.</span><span class="sxs-lookup"><span data-stu-id="db43f-138">This will be empty to start with.</span></span>
1. <span data-ttu-id="db43f-139">Im Abschnitt **Dashboardbild** zeigen Sie das Logo und/oder Dashboardbild an, das der juristischen Person zugeordnet ist, oder ändern Sie es.</span><span class="sxs-lookup"><span data-stu-id="db43f-139">In the **Dashboard image** section, view or change the logo and dashboard image associated with the legal entity.</span></span>
1. <span data-ttu-id="db43f-140">Geben Sie im Abschnitt **Steuerregistrierung** die Registrierungsnummern ein, die für die Meldung bei Steuerbehörden verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="db43f-140">In the **Tax registration** section, enter the registration numbers that are used to report to tax authorities.</span></span>
1. <span data-ttu-id="db43f-141">Geben Sie im Abschnitt **Steuererklärung (US 1099)** die Informationen zur Steuererklärung (US 1099) für die juristische Person ein.</span><span class="sxs-lookup"><span data-stu-id="db43f-141">In the **Tax 1099** section, enter 1099 information for the legal entity.</span></span>
1. <span data-ttu-id="db43f-142">Geben Sie im Abschnitt **Steuerinformation** die Steuerinformation für die juristische Person ein.</span><span class="sxs-lookup"><span data-stu-id="db43f-142">In the **Tax invormation** section, enter tax information for the legal entity.</span></span>
1. <span data-ttu-id="db43f-143">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="db43f-143">Select **Save**.</span></span>

<span data-ttu-id="db43f-144">Das folgende Bild zeigt die Details eines Beispiels für eine juristische Person.</span><span class="sxs-lookup"><span data-stu-id="db43f-144">The following image shows details of an example legal entity.</span></span>

![Allgemeiner Teil der juristischen Person](media/legal-entities-general.png)
   
## <a name="additional-resources"></a><span data-ttu-id="db43f-146">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="db43f-146">Additional resources</span></span>

[<span data-ttu-id="db43f-147">Organisationen und Organisationshierarchien – Übersicht</span><span class="sxs-lookup"><span data-stu-id="db43f-147">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="db43f-148">Planen Ihrer Organisationshierarchie</span><span class="sxs-lookup"><span data-stu-id="db43f-148">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="db43f-149">Organisationshierarchien</span><span class="sxs-lookup"><span data-stu-id="db43f-149">Organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="db43f-150">Kanalübersicht</span><span class="sxs-lookup"><span data-stu-id="db43f-150">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="db43f-151">Voraussetzungen der Kanaleinrichtung</span><span class="sxs-lookup"><span data-stu-id="db43f-151">Channel setup prerequisites</span></span>](channels-prerequisites.md)
