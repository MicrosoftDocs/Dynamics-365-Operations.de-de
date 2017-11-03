---
title: "Anwendungs- und Benutzerspracheneinstellungen für POS"
description: "In diesem Thema wird beschrieben, wie Spracheinstellungen in Retail Modern POS (MPOS) und Cloud POS geändert werden."
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: HcmWorker, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 78891
ms.assetid: 0030940c-e0a5-4345-9511-8c3bd1f487ad
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: dacc072ab5c070010d86302fa08a3066125b23a6
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="pos-application-and-user-language-settings"></a><span data-ttu-id="29250-103">Anwendungs- und Benutzerspracheneinstellungen für POS</span><span class="sxs-lookup"><span data-stu-id="29250-103">POS application and user language settings</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="29250-104">In diesem Thema wird beschrieben, wie Spracheinstellungen in Retail Modern POS (MPOS) und Cloud POS geändert werden.</span><span class="sxs-lookup"><span data-stu-id="29250-104">This topic describes how to change language settings in Retail Modern POS (MPOS) and Cloud POS.</span></span>

<a name="overview"></a><span data-ttu-id="29250-105">Überblick</span><span class="sxs-lookup"><span data-stu-id="29250-105">Overview</span></span>
========

<span data-ttu-id="29250-106">Retail Modern POS (MPOS) und Cloud POS unterstützen Umgebung, in denen Spracheinstellungen und -übersetzungen zwischen die Filiale und die Benutzereinstellungen variieren können.</span><span class="sxs-lookup"><span data-stu-id="29250-106">Retail Modern POS (MPOS) and Cloud POS support environments where language settings and translations can vary between the store and user settings.</span></span> <span data-ttu-id="29250-107">Beispielsweise kann sich der Shop in einer Region befinden, der in Englisch die gängigsten für seine Kunden ist, manche Arbeitskräfte ziehen sie vor, die Anwendung mit französischen Übersetzungen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="29250-107">For example, the store could be located in a region where English is most common for their customers, but some workers prefer to use the application with French translations.</span></span>

## <a name="data-language"></a><span data-ttu-id="29250-108">Sprache der Daten</span><span class="sxs-lookup"><span data-stu-id="29250-108">Data language</span></span>
<span data-ttu-id="29250-109">Unabhängig von der Einstellungen des Benutzers verwendet MPOS und Cloud POS immer die Spracheinstellungen des Shops, um die Übersetzungen bestimmt, die für Daten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="29250-109">Regardless of the user’s settings, MPOS and Cloud POS will always use the store's language settings to determine the translations used for data.</span></span> <span data-ttu-id="29250-110">Dadurch wird sichergestellt, dass alle Benutzer und Debitoren eine konsistente Erfahrung haben.</span><span class="sxs-lookup"><span data-stu-id="29250-110">This will ensure that all users and customers will have a consistent experience.</span></span>  <span data-ttu-id="29250-111">Beispiele zu Daten sind:</span><span class="sxs-lookup"><span data-stu-id="29250-111">Examples of data include:</span></span>

-   <span data-ttu-id="29250-112">Produkte</span><span class="sxs-lookup"><span data-stu-id="29250-112">Products</span></span>
-   <span data-ttu-id="29250-113">Attribute und Werte</span><span class="sxs-lookup"><span data-stu-id="29250-113">Attributes and values</span></span>
-   <span data-ttu-id="29250-114">Kategorienamen</span><span class="sxs-lookup"><span data-stu-id="29250-114">Category names</span></span>
-   <span data-ttu-id="29250-115">Gedruckte oder per E-Mail übermittelte Transaktionsbelege</span><span class="sxs-lookup"><span data-stu-id="29250-115">Printed or emailed transaction receipts</span></span>
-   <span data-ttu-id="29250-116">Namen der Zahlungsmethoden</span><span class="sxs-lookup"><span data-stu-id="29250-116">Payment method names</span></span>
-   <span data-ttu-id="29250-117">Zeilenanzeigemeldungen</span><span class="sxs-lookup"><span data-stu-id="29250-117">Line display messages</span></span>

<span data-ttu-id="29250-118">Die Sprache der Filiale wird auch für den POS-Haupt-Anmelden Bildschirm verwendet, da der Benutzer nicht bekannt, vor dem Anmelden.</span><span class="sxs-lookup"><span data-stu-id="29250-118">The store’s language will also be used for the main POS login screen, since the user is not known before logging in.</span></span> <span data-ttu-id="29250-119">Wenn eine Übersetzung nicht für die Sprache der Filiale verfügbar ist, stellt der Betrag vom POS der Sprache des Unternehmens wieder her.</span><span class="sxs-lookup"><span data-stu-id="29250-119">If a translation is not available for the store’s language, the POS will revert to the company’s language.</span></span>

### <a name="configuring-the-stores-language-setting"></a><span data-ttu-id="29250-120">Konfigurieren der Spracheinstellung des Shops</span><span class="sxs-lookup"><span data-stu-id="29250-120">Configuring the store’s language setting</span></span>

<span data-ttu-id="29250-121">Die Spracheinstellung eines Shops wird über **“Alle Einzelhandelsgeschäfte”**auf der Seite “**Ladengeschäft”** unter **Allgemein &gt; Regionaleinstellungen &gt; Sprache festgelegt.</span><span class="sxs-lookup"><span data-stu-id="29250-121">The store’s language setting is set from **All retail stores** on the **Retail Store** page under **General &gt; Regional Settings &gt; Language.</span></span> <span data-ttu-id="29250-122">**Verwenden Sie das Dropdownfeld, um eine Sprache für jeden Shop auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="29250-122">**Use the drop down to choose the language for each store.</span></span>

## <a name="user-interface-language"></a><span data-ttu-id="29250-123">Benutzeroberflächensprache</span><span class="sxs-lookup"><span data-stu-id="29250-123">User interface language</span></span>
<span data-ttu-id="29250-124">Die Einstellung des POS- Benutzers werden die Übersetzungen, die in der Bewerbungsbenutzeroberfläche verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="29250-124">The POS user’s language setting determines the translations used in the application user interface.</span></span> <span data-ttu-id="29250-125">Dies umfasst alle Beschriftungen, Menüs und Listen ein, die nicht als Daten anwenden.</span><span class="sxs-lookup"><span data-stu-id="29250-125">This includes all labels, menus, and lists that are not considered data.</span></span> <span data-ttu-id="29250-126">Eine Ausnahme ist der Text, der in POS-Schaltflächenrastern angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="29250-126">One exception is the text that is displayed on POS button grids.</span></span> <span data-ttu-id="29250-127">Die Schaltflächenraster nicht unterstützt Übersetzungen, sodass die Konten immer Text anzeigen, wie auf der Schaltfläche definiert.</span><span class="sxs-lookup"><span data-stu-id="29250-127">The button grids don't support translations, so they will always show the text as defined on the button.</span></span> <span data-ttu-id="29250-128">Um zu unterstützen übersetzte Schaltflächen, müssen Sie separate Schaltflächenraster kopieren und verwalten und diese den entsprechenden Benutzer zuweisen.</span><span class="sxs-lookup"><span data-stu-id="29250-128">In order to support translated buttons, you'll have to copy and maintain separate button grids and assign them to the users as appropriate.</span></span>

### <a name="configuring-the-users-language-setting"></a><span data-ttu-id="29250-129">Konfigurieren der Spracheinstellung der Benutzers</span><span class="sxs-lookup"><span data-stu-id="29250-129">Configuring the user’s language setting</span></span>

<span data-ttu-id="29250-130">Die Spracheinstellung des POS-Benutzers wird unter "**Alle Arbeitskräfte**" auf der Seite "**Arbeitskraft**" unter **Einzelhandel &gt; Sprache** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="29250-130">The POS user’s language setting is set from **All workers** on the **Worker** page under **Retail &gt; Language**.</span></span>  <span data-ttu-id="29250-131">Sie wird nicht auf der Hauptregisterkarte „Profil“ festgelegt. Diese Einstellung wird nicht durch POS verwendet.</span><span class="sxs-lookup"><span data-stu-id="29250-131">It is not set on the main Profile tab.  This setting is not used by POS.</span></span> <span data-ttu-id="29250-132">Wenn die Sprache des Benutzers nicht festgelegt wird oder sie auf eine Sprache festgelegt wird, in der Übersetzungen nicht verfügbar sind, stellt das POS die Sprache des Shops wieder her.</span><span class="sxs-lookup"><span data-stu-id="29250-132">If the user’s language is not set or it is set to a language where translations are not available, the POS will revert to the store’s language.</span></span>  

|             |                            |                                                                   |
|-------------|----------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="29250-133">** **</span><span class="sxs-lookup"><span data-stu-id="29250-133">** **</span></span>       | <span data-ttu-id="29250-134">**Sprache der Benutzeroberfläche** ** **</span><span class="sxs-lookup"><span data-stu-id="29250-134">**UI language** ** **</span></span>      | <span data-ttu-id="29250-135">**Datensprache (Produkte, Bonlayouts, Zeilenanzeige usw.)**</span><span class="sxs-lookup"><span data-stu-id="29250-135">**Data language (products, receipt formats, line display, etc.)**</span></span> |
| <span data-ttu-id="29250-136">**Unternehmen**</span><span class="sxs-lookup"><span data-stu-id="29250-136">**Company**</span></span> | <span data-ttu-id="29250-137">Standard</span><span class="sxs-lookup"><span data-stu-id="29250-137">Default</span></span>                    | <span data-ttu-id="29250-138">Standard</span><span class="sxs-lookup"><span data-stu-id="29250-138">Default</span></span>                                                           |
| <span data-ttu-id="29250-139">**Shop**</span><span class="sxs-lookup"><span data-stu-id="29250-139">**Store**</span></span>   | <span data-ttu-id="29250-140">Überschreibt Unternehmen</span><span class="sxs-lookup"><span data-stu-id="29250-140">Overrides company</span></span>          | <span data-ttu-id="29250-141">Überschreibt Unternehmen</span><span class="sxs-lookup"><span data-stu-id="29250-141">Overrides company</span></span>                                                 |
| <span data-ttu-id="29250-142">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="29250-142">**User**</span></span>    | <span data-ttu-id="29250-143">Überschreibt Shop oder Unternehmen</span><span class="sxs-lookup"><span data-stu-id="29250-143">Overrides store or company</span></span> | <span data-ttu-id="29250-144">Nie</span><span class="sxs-lookup"><span data-stu-id="29250-144">Never</span></span>                                                             |






