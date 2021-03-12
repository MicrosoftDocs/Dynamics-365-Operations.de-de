---
title: Verkaufsstellen-(POS)-Anwendung und Benutzerspracheinstellungen
description: In diesem Thema wird beschrieben, wie Spracheinstellungen in Modern POS (MPOS) und Cloud POS geändert werden.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: HcmWorker, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.custom: 78891
ms.assetid: 0030940c-e0a5-4345-9511-8c3bd1f487ad
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 0f196b3077b0a8d80cac93a8b6b3f8c5c08c3c96
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000558"
---
# <a name="point-of-sale-pos-application-and-user-language-settings"></a><span data-ttu-id="31deb-103">Verkaufsstellen-(POS)-Anwendung und Benutzerspracheinstellungen</span><span class="sxs-lookup"><span data-stu-id="31deb-103">Point of sale (POS) application and user language settings</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="31deb-104">In diesem Thema wird beschrieben, wie Spracheinstellungen in Modern POS (MPOS) und Cloud POS geändert werden.</span><span class="sxs-lookup"><span data-stu-id="31deb-104">This topic describes how to change language settings in Modern POS (MPOS) and Cloud POS.</span></span>

## <a name="overview"></a><span data-ttu-id="31deb-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="31deb-105">Overview</span></span>
<span data-ttu-id="31deb-106">Modern POS (MPOS) und Cloud POS unterstützen Umgebung, in denen Spracheinstellungen und -übersetzungen zwischen die Filiale und die Benutzereinstellungen variieren können.</span><span class="sxs-lookup"><span data-stu-id="31deb-106">Modern POS (MPOS) and Cloud POS support environments where language settings and translations can vary between the store and user settings.</span></span> <span data-ttu-id="31deb-107">Beispielsweise kann sich der Shop in einer Region befinden, der in Englisch die gängigsten für seine Kunden ist, manche Arbeitskräfte ziehen sie vor, die Anwendung mit französischen Übersetzungen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="31deb-107">For example, the store could be located in a region where English is most common for their customers, but some workers prefer to use the application with French translations.</span></span>

## <a name="data-language"></a><span data-ttu-id="31deb-108">Sprache der Daten</span><span class="sxs-lookup"><span data-stu-id="31deb-108">Data language</span></span>

<span data-ttu-id="31deb-109">Unabhängig von der Einstellungen des Benutzers verwendet MPOS und Cloud POS immer die Spracheinstellungen des Shops, um die Übersetzungen bestimmt, die für Daten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="31deb-109">Regardless of the user's settings, MPOS and Cloud POS will always use the store's language settings to determine the translations used for data.</span></span> <span data-ttu-id="31deb-110">Dadurch wird sichergestellt, dass alle Benutzer und Debitoren eine konsistente Erfahrung haben.</span><span class="sxs-lookup"><span data-stu-id="31deb-110">This will ensure that all users and customers will have a consistent experience.</span></span> <span data-ttu-id="31deb-111">Beispiele zu Daten sind:</span><span class="sxs-lookup"><span data-stu-id="31deb-111">Examples of data include:</span></span>

- <span data-ttu-id="31deb-112">Produkte</span><span class="sxs-lookup"><span data-stu-id="31deb-112">Products</span></span>
- <span data-ttu-id="31deb-113">Attribute und Werte</span><span class="sxs-lookup"><span data-stu-id="31deb-113">Attributes and values</span></span>
- <span data-ttu-id="31deb-114">Kategorienamen</span><span class="sxs-lookup"><span data-stu-id="31deb-114">Category names</span></span>
- <span data-ttu-id="31deb-115">Gedruckte oder per E-Mail übermittelte Transaktionsbelege</span><span class="sxs-lookup"><span data-stu-id="31deb-115">Printed or emailed transaction receipts</span></span>
- <span data-ttu-id="31deb-116">Namen der Zahlungsmethoden</span><span class="sxs-lookup"><span data-stu-id="31deb-116">Payment method names</span></span>
- <span data-ttu-id="31deb-117">Zeilenanzeigemeldungen</span><span class="sxs-lookup"><span data-stu-id="31deb-117">Line display messages</span></span>

<span data-ttu-id="31deb-118">Die Sprache der Filiale wird auch für den POS-Haupt-Anmelden Bildschirm verwendet, da der Benutzer nicht bekannt, vor dem Anmelden.</span><span class="sxs-lookup"><span data-stu-id="31deb-118">The store's language will also be used for the main POS login screen, since the user is not known before logging in.</span></span> <span data-ttu-id="31deb-119">Wenn eine Übersetzung nicht für die Sprache der Filiale verfügbar ist, stellt der Betrag vom POS der Sprache des Unternehmens wieder her.</span><span class="sxs-lookup"><span data-stu-id="31deb-119">If a translation is not available for the store's language, the POS will revert to the company's language.</span></span>

### <a name="configuring-the-stores-language-setting"></a><span data-ttu-id="31deb-120">Konfigurieren der Spracheinstellung des Shops</span><span class="sxs-lookup"><span data-stu-id="31deb-120">Configuring the store's language setting</span></span>

<span data-ttu-id="31deb-121">Die Spracheinstellung eines Shops wird über **Alle Einzelhandelsgeschäfte** auf der Seite **Shop** unter **Allgemein &gt; Regionaleinstellungen &gt; Sprache** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="31deb-121">The store's language setting is set from **All stores** on the **Store** page under **General &gt; Regional Settings &gt; Language**.</span></span> <span data-ttu-id="31deb-122">Verwenden Sie die Dropdownliste, um eine Sprache für jeden Shop auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="31deb-122">Use the drop-down list to choose the language for each store.</span></span>

## <a name="user-interface-language"></a><span data-ttu-id="31deb-123">Benutzeroberflächensprache</span><span class="sxs-lookup"><span data-stu-id="31deb-123">User interface language</span></span>

<span data-ttu-id="31deb-124">Die Einstellung des POS- Benutzers werden die Übersetzungen, die in der Bewerbungsbenutzeroberfläche verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="31deb-124">The POS user's language setting determines the translations used in the application user interface.</span></span> <span data-ttu-id="31deb-125">Dies umfasst alle Beschriftungen, Menüs und Listen ein, die nicht als Daten anwenden.</span><span class="sxs-lookup"><span data-stu-id="31deb-125">This includes all labels, menus, and lists that are not considered data.</span></span> <span data-ttu-id="31deb-126">Eine Ausnahme ist der Text, der in POS-Schaltflächenrastern angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="31deb-126">One exception is the text that is displayed on POS button grids.</span></span> <span data-ttu-id="31deb-127">Die Schaltflächenraster nicht unterstützt Übersetzungen, sodass die Konten immer Text anzeigen, wie auf der Schaltfläche definiert.</span><span class="sxs-lookup"><span data-stu-id="31deb-127">The button grids don't support translations, so they will always show the text as defined on the button.</span></span> <span data-ttu-id="31deb-128">Um zu unterstützen übersetzte Schaltflächen, müssen Sie separate Schaltflächenraster kopieren und verwalten und diese den entsprechenden Benutzer zuweisen.</span><span class="sxs-lookup"><span data-stu-id="31deb-128">In order to support translated buttons, you'll have to copy and maintain separate button grids and assign them to the users as appropriate.</span></span>

### <a name="configuring-the-users-language-setting"></a><span data-ttu-id="31deb-129">Konfigurieren der Spracheinstellung der Benutzers</span><span class="sxs-lookup"><span data-stu-id="31deb-129">Configuring the user's language setting</span></span>

<span data-ttu-id="31deb-130">Die Spracheinstellung des POS-Benutzers wird unter **Alle Arbeitskräfte** auf der Seite **Arbeitskraft** unter **Einzelhandel und Commerce &gt;  Sprache** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="31deb-130">The POS user's language setting is set from **All workers** on the **Worker** page under **Retail and Commerce &gt; Language**.</span></span> <span data-ttu-id="31deb-131">Sie wird nicht auf der Hauptregisterkarte „Profil“ festgelegt. Diese Einstellung wird nicht durch POS verwendet.</span><span class="sxs-lookup"><span data-stu-id="31deb-131">It is not set on the main Profile tab. This setting is not used by POS.</span></span> <span data-ttu-id="31deb-132">Wenn die Sprache des Benutzers nicht festgelegt wird oder sie auf eine Sprache festgelegt wird, in der Übersetzungen nicht verfügbar sind, stellt das POS die Sprache des Shops wieder her.</span><span class="sxs-lookup"><span data-stu-id="31deb-132">If the user's language is not set or it is set to a language where translations are not available, the POS will revert to the store's language.</span></span>

|             | <span data-ttu-id="31deb-133">Sprache der Benutzeroberfläche  </span><span class="sxs-lookup"><span data-stu-id="31deb-133">UI language</span></span>                | <span data-ttu-id="31deb-134">Datensprache (Produkte, Bonlayouts, Zeilenanzeige usw.)</span><span class="sxs-lookup"><span data-stu-id="31deb-134">Data language (products, receipt formats, line display, etc.)</span></span> |
|-------------|----------------------------|---------------------------------------------------------------|
| <span data-ttu-id="31deb-135">**Unternehmen**</span><span class="sxs-lookup"><span data-stu-id="31deb-135">**Company**</span></span> | <span data-ttu-id="31deb-136">Standard</span><span class="sxs-lookup"><span data-stu-id="31deb-136">Default</span></span>                    | <span data-ttu-id="31deb-137">Standard</span><span class="sxs-lookup"><span data-stu-id="31deb-137">Default</span></span>                                                       |
| <span data-ttu-id="31deb-138">**Shop**</span><span class="sxs-lookup"><span data-stu-id="31deb-138">**Store**</span></span>   | <span data-ttu-id="31deb-139">Überschreibt Unternehmen</span><span class="sxs-lookup"><span data-stu-id="31deb-139">Overrides company</span></span>          | <span data-ttu-id="31deb-140">Überschreibt Unternehmen</span><span class="sxs-lookup"><span data-stu-id="31deb-140">Overrides company</span></span>                                             |
| <span data-ttu-id="31deb-141">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="31deb-141">**User**</span></span>    | <span data-ttu-id="31deb-142">Überschreibt Shop oder Unternehmen</span><span class="sxs-lookup"><span data-stu-id="31deb-142">Overrides store or company</span></span> | <span data-ttu-id="31deb-143">Nie</span><span class="sxs-lookup"><span data-stu-id="31deb-143">Never</span></span>                                                         |
