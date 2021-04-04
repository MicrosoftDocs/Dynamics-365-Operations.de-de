---
title: Juristische Personen erstellen
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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 016b67631a53139d12d65dfaf594f49b030326b1
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478211"
---
# <a name="create-legal-entities"></a><span data-ttu-id="1b9d9-103">Juristische Personen erstellen</span><span class="sxs-lookup"><span data-stu-id="1b9d9-103">Create legal entities</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1b9d9-104">In diesem Thema wird beschrieben, wie Sie juristische Personen in Microsoft Dynamics 365 Commerce erstellen, die erstellt und konfiguriert werden müssen, bevor Kanäle erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="1b9d9-104">This topic describes how to create legal entities in Microsoft Dynamics 365 Commerce, which must be created and configured before creating channels.</span></span>

<span data-ttu-id="1b9d9-105">Eine juristische Person ist eine Organisation mit einer registrierten oder eingetragenen Rechtsform.</span><span class="sxs-lookup"><span data-stu-id="1b9d9-105">A legal entity is an organization that has a registered or legislated legal structure.</span></span> <span data-ttu-id="1b9d9-106">Juristische Personen können Verträge abschließen und sind verpflichtet, Finanzaufstellungen zum Erstellen eines Berichts über ihre Vermögens-, Finanz- und Ertragslage vorzubereiten.</span><span class="sxs-lookup"><span data-stu-id="1b9d9-106">Legal entities can enter into legal contracts and are required to prepare statements that report on their performance.</span></span>

<span data-ttu-id="1b9d9-107">Ein Unternehmen ist eine Art von juristischer Person.</span><span class="sxs-lookup"><span data-stu-id="1b9d9-107">A company is a type of legal entity.</span></span> <span data-ttu-id="1b9d9-108">Derzeit sind Unternehmen die einzige Art von juristischer Person, die Sie erstellen können, und jeder juristischen Person ist eine Unternehmenskennung zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="1b9d9-108">Currently, companies are the only kind of legal entity that you can create, and every legal entity is associated with a company ID.</span></span> <span data-ttu-id="1b9d9-109">Diese Zuordnung ist notwendig, da einige Funktionsbereiche im Programm eine Unternehmenskennung (oder *DataAreaId*) in den Datenmodellen verwenden.</span><span class="sxs-lookup"><span data-stu-id="1b9d9-109">This association exists because some functional areas in the program use a company ID, or *DataAreaId*, in their data models.</span></span> <span data-ttu-id="1b9d9-110">In diesen Funktionsbereichen werden Unternehmen als Grenze für die Datensicherheit verwendet.</span><span class="sxs-lookup"><span data-stu-id="1b9d9-110">In these functional areas, companies are used as a boundary for data security.</span></span> <span data-ttu-id="1b9d9-111">Benutzer können nur auf Daten für das Unternehmen zugreifen, bei dem sie derzeit angemeldet sind.</span><span class="sxs-lookup"><span data-stu-id="1b9d9-111">Users can access data only for the company that they are currently logged on to.</span></span> 

<span data-ttu-id="1b9d9-112">Beim Erstellen eines Kanals müssen Sie angeben, zu welcher juristischen Person dieser Kanal gehört.</span><span class="sxs-lookup"><span data-stu-id="1b9d9-112">When creating a channel, you must specify which legal entity that channel belongs to.</span></span>

## <a name="create-a-new-legal-entity"></a><span data-ttu-id="1b9d9-113">Eine neue juristische Person erstellen</span><span class="sxs-lookup"><span data-stu-id="1b9d9-113">Create a new legal entity</span></span>

<span data-ttu-id="1b9d9-114">Gehen Sie folgendermaßen vor, um eine neue juristische Person in Dynamics 365 Commerce zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1b9d9-114">To create a new legal entity in Dynamics 365 Commerce, follow these steps.</span></span>

1. <span data-ttu-id="1b9d9-115">Gehen Sie im Navigationsbereich zu **Module \> Hauptsitz einrichten \> Juristische Personen**.</span><span class="sxs-lookup"><span data-stu-id="1b9d9-115">In the navigation pane, go to  **Modules \> Headquarters setup \> Legal entities**.</span></span>
1. <span data-ttu-id="1b9d9-116">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="1b9d9-116">On the action pane, select **New**.</span></span> <span data-ttu-id="1b9d9-117">Das Fenster **Neue juristische Person** wird rechts angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1b9d9-117">The **New legal entity** pane appears on the right.</span></span>
1. <span data-ttu-id="1b9d9-118">Geben Sie im Feld **Name** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="1b9d9-118">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="1b9d9-119">Geben Sie im Feld **Unternehmen** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="1b9d9-119">In the **Company** field, enter a value.</span></span>
1. <span data-ttu-id="1b9d9-120">Wählen Sie im Feld **Land/Region** einen Wert aus, oder geben Sie einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="1b9d9-120">In the **Country/region** field, enter or select a value.</span></span>
1. <span data-ttu-id="1b9d9-121">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="1b9d9-121">Select **OK**.</span></span> 

   ![Erstellung einer juristischen Person](media/legal-entities.png)

1. <span data-ttu-id="1b9d9-123">Stellen Sie im Abschnitt **Allgemein** die folgenden allgemeinen Informationen zur juristischen Person bereit:</span><span class="sxs-lookup"><span data-stu-id="1b9d9-123">In the **General** section, provide the following general information about the legal entity:</span></span> 
   1. <span data-ttu-id="1b9d9-124">Geben Sie einen Suchbegriff ein, falls erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1b9d9-124">Enter a search name, if a search name is required.</span></span> <span data-ttu-id="1b9d9-125">Ein Suchbegriff ist ein alternativer Name, der verwendet werden kann, um nach dieser juristischen Person zu suchen.</span><span class="sxs-lookup"><span data-stu-id="1b9d9-125">A search name is an alternate name that can be used to search for this legal entity.</span></span> 
   1. <span data-ttu-id="1b9d9-126">Wählen Sie aus, ob diese juristische Person als Konsolidierungsunternehmen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1b9d9-126">Select whether this legal entity is being used as a consolidation company.</span></span>
   1. <span data-ttu-id="1b9d9-127">Wählen Sie aus, ob diese juristische Person als Unternehmen mit Löschungseinträgen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1b9d9-127">Select whether this legal entity is being used as an elimination company.</span></span> 
   1. <span data-ttu-id="1b9d9-128">Wählen Sie die **Standardsprache** für die Entität aus.</span><span class="sxs-lookup"><span data-stu-id="1b9d9-128">Select the **default language** for the entity.</span></span> 
   1. <span data-ttu-id="1b9d9-129">Wählen Sie die **Zeitzone** für die Entität aus.</span><span class="sxs-lookup"><span data-stu-id="1b9d9-129">Select the **time zone** for the entity.</span></span>
1. <span data-ttu-id="1b9d9-130">Wählen Sie im Abschnitt **Adressen** die Option **Bearbeiten**, um die Adressinformationen wie die Straße und Hausnummer, die Postleitzahl und den Ort einzugeben.</span><span class="sxs-lookup"><span data-stu-id="1b9d9-130">In the **Addresses** section, select **Edit** to enter address information, such as the street name and number, postal code, and city.</span></span>
1. <span data-ttu-id="1b9d9-131">Geben Sie im Abschnitt **Kontaktinformationen** Informationen zu den Kommunikationsmethoden ein, wie beispielsweise E-Mail-Adressen, URLs und Telefonnummern.</span><span class="sxs-lookup"><span data-stu-id="1b9d9-131">In the **Contact information** section, enter information about methods of communication, such as email addresses, URLs, and telephone numbers.</span></span>
1. <span data-ttu-id="1b9d9-132">Geben Sie im Abschnitt **Offenlegungspflicht** die Registrierungsnummern ein, die für die Offenlegungspflicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1b9d9-132">In the **Statutory reporting** section, enter the registration numbers that are used for statutory reporting.</span></span>
1. <span data-ttu-id="1b9d9-133">Geben Sie im Abschnitt **Registrierungsnummern** alle Informationen ein, die für die juristische Person erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="1b9d9-133">In the **Registration numbers** section, enter any information required by the legal entity.</span></span>
1. <span data-ttu-id="1b9d9-134">Geben Sie im Abschnitt **Bankkontinformationen** die Bankkonten und Bankleitzahlen für die juristische Person ein.</span><span class="sxs-lookup"><span data-stu-id="1b9d9-134">In the **Bank account information** section, enter bank accounts and routing numbers for the legal entity.</span></span>
1. <span data-ttu-id="1b9d9-135">Geben Sie im Abschnitt **Außenhandel und Logistik** die Versandinformationen für die juristische Person ein.</span><span class="sxs-lookup"><span data-stu-id="1b9d9-135">In the **Foreign trade and logistics** section, enter shipping information for the legal entity.</span></span>
1. <span data-ttu-id="1b9d9-136">Im Abschnitt **Nummernkreise** können Sie die Nummernkreise anzeigen, die der juristischen Person zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="1b9d9-136">In the **Number sequences** section, you can view the number sequences that are associated with the legal entity.</span></span> <span data-ttu-id="1b9d9-137">Dies ist zunächst leer.</span><span class="sxs-lookup"><span data-stu-id="1b9d9-137">This will be empty to start with.</span></span>
1. <span data-ttu-id="1b9d9-138">Im Abschnitt **Dashboardbild** zeigen Sie das Logo und/oder Dashboardbild an, das der juristischen Person zugeordnet ist, oder ändern Sie es.</span><span class="sxs-lookup"><span data-stu-id="1b9d9-138">In the **Dashboard image** section, view or change the logo and dashboard image associated with the legal entity.</span></span>
1. <span data-ttu-id="1b9d9-139">Geben Sie im Abschnitt **Steuerregistrierung** die Registrierungsnummern ein, die für die Meldung bei Steuerbehörden verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1b9d9-139">In the **Tax registration** section, enter the registration numbers that are used to report to tax authorities.</span></span>
1. <span data-ttu-id="1b9d9-140">Geben Sie im Abschnitt **Steuererklärung (US 1099)** die Informationen zur Steuererklärung (US 1099) für die juristische Person ein.</span><span class="sxs-lookup"><span data-stu-id="1b9d9-140">In the **Tax 1099** section, enter 1099 information for the legal entity.</span></span>
1. <span data-ttu-id="1b9d9-141">Geben Sie im Abschnitt **Steuerinformation** die Steuerinformation für die juristische Person ein.</span><span class="sxs-lookup"><span data-stu-id="1b9d9-141">In the **Tax invormation** section, enter tax information for the legal entity.</span></span>
1. <span data-ttu-id="1b9d9-142">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="1b9d9-142">Select **Save**.</span></span>

<span data-ttu-id="1b9d9-143">Das folgende Bild zeigt die Details eines Beispiels für eine juristische Person.</span><span class="sxs-lookup"><span data-stu-id="1b9d9-143">The following image shows details of an example legal entity.</span></span>

![Allgemeiner Teil der juristischen Person](media/legal-entities-general.png)
   
## <a name="additional-resources"></a><span data-ttu-id="1b9d9-145">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1b9d9-145">Additional resources</span></span>

[<span data-ttu-id="1b9d9-146">Organisationen und Organisationshierarchien – Übersicht</span><span class="sxs-lookup"><span data-stu-id="1b9d9-146">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="1b9d9-147">Planen Ihrer Organisationshierarchie</span><span class="sxs-lookup"><span data-stu-id="1b9d9-147">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="1b9d9-148">Organisationshierarchien</span><span class="sxs-lookup"><span data-stu-id="1b9d9-148">Organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="1b9d9-149">Kanalübersicht</span><span class="sxs-lookup"><span data-stu-id="1b9d9-149">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="1b9d9-150">Voraussetzungen der Kanaleinrichtung</span><span class="sxs-lookup"><span data-stu-id="1b9d9-150">Channel setup prerequisites</span></span>](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
