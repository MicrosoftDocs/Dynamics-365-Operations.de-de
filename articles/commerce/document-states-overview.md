---
title: Dokumentstatus und -Lebenszyklus
description: In diesem Thema werden die verschiedenen Dokumentstatus von Seitenelementen in Microsoft Dynamics 365 Commerce behandelt.
author: phinneyridge
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: edb81efc45fc5e7eed32cb7d9b8fda5ade987dd4
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914886"
---
# <a name="document-states-and-lifecycle"></a><span data-ttu-id="6016c-103">Dokumentstatus und -Lebenszyklus</span><span class="sxs-lookup"><span data-stu-id="6016c-103">Document states and lifecycle</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="6016c-104">In diesem Thema werden die verschiedenen Dokumentstatus von Seitenelementen in Microsoft Dynamics 365 Commerce behandelt.</span><span class="sxs-lookup"><span data-stu-id="6016c-104">This topic covers the various document states of page elements in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="document-state-descriptions"></a><span data-ttu-id="6016c-105">Dokumentstatusbeschreibung</span><span class="sxs-lookup"><span data-stu-id="6016c-105">Document state descriptions</span></span>

<span data-ttu-id="6016c-106">Die [Seitenelemente](page-elements-overview.md) der Themen führen verschiedene Dokumente im Content Management System (CMS) auf.</span><span class="sxs-lookup"><span data-stu-id="6016c-106">The [Page elements](page-elements-overview.md) topic lists various documents types in the content management system (CMS).</span></span> <span data-ttu-id="6016c-107">Diese Dokumenttypen können mehrere Status im Erstellungstool haben.</span><span class="sxs-lookup"><span data-stu-id="6016c-107">These document types can have several states in the authoring tool.</span></span> <span data-ttu-id="6016c-108">Die Dokumenttypen helfen, Datenkonflikte zu verhindern und Versionskontrollen zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="6016c-108">The document states help prevent data conflicts and enforce version control.</span></span> <span data-ttu-id="6016c-109">Sie bestimmen, wer die Dokumente ändern kann, wenn die Dokumente geändert werden können und wenn Änderungen von anderen Personen angezeigt werden können.</span><span class="sxs-lookup"><span data-stu-id="6016c-109">They determine who can change the documents, when the documents can be changed, and when changes can be viewed by other people.</span></span>

<span data-ttu-id="6016c-110">Die folgende Tabelle enthält die möglichen Dokumentstatus von Seitenelementen in Commerce.</span><span class="sxs-lookup"><span data-stu-id="6016c-110">The following table shows the possible document states of page elements in Commerce.</span></span>

| <span data-ttu-id="6016c-111">Dokumentstatus</span><span class="sxs-lookup"><span data-stu-id="6016c-111">Document state</span></span> | <span data-ttu-id="6016c-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6016c-112">Description</span></span> |
|---|---|
| <span data-ttu-id="6016c-113">Ausgecheckt</span><span class="sxs-lookup"><span data-stu-id="6016c-113">Checked out</span></span> | <span data-ttu-id="6016c-114">Wenn ein CMS-Artikel ausgecheckt wird von Ihnen, kann dies nicht von jedem beliebigen anderen authentifizierten Systembenutzern bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="6016c-114">When a CMS item is checked out to you, it can't be edited by any other authenticated system users.</span></span> <span data-ttu-id="6016c-115">Alle Änderungen, die Sie am Artikel vornehmen, sind nur für Sie angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6016c-115">Any changes that you make to the item are visible only to you.</span></span> |
| <span data-ttu-id="6016c-116">Eingecheckt</span><span class="sxs-lookup"><span data-stu-id="6016c-116">Checked in</span></span> | <span data-ttu-id="6016c-117">Wenn ein CMS-Artikel eingecheckt wird, sind alle Änderungen für andere authentifizierte Systembenutzer angezeigt, und die Benutzer können den Artikel dann auschecken und bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="6016c-117">When a CMS item is checked in, all changes are visible to other authenticated system users, and those users can then check out the item and edit it.</span></span> <span data-ttu-id="6016c-118">Jedes Einchecken erstellt einen Dokumentversionsdatensatz im Workflowverlauf des Artikels.</span><span class="sxs-lookup"><span data-stu-id="6016c-118">Each check-in creates a document version record in the item's history.</span></span> |
| <span data-ttu-id="6016c-119">Publiziert</span><span class="sxs-lookup"><span data-stu-id="6016c-119">Published</span></span> | <span data-ttu-id="6016c-120">Wenn ein CMS-Artikel veröffentlicht wird, wird er an Ihre Livesite weitergeleitet und wird im Internet für nicht-authentifizierte externe Benutzer sichtbar.</span><span class="sxs-lookup"><span data-stu-id="6016c-120">When a CMS item is published, it's pushed to your live site and becomes discoverable on the internet by non-authenticated external users.</span></span> <span data-ttu-id="6016c-121">Artikel können veröffentlicht werden, nachdem sie eingecheckt wurden.</span><span class="sxs-lookup"><span data-stu-id="6016c-121">Items can be published only if they have been checked in.</span></span> |
| <span data-ttu-id="6016c-122">Gespeichert</span><span class="sxs-lookup"><span data-stu-id="6016c-122">Saved</span></span> | <span data-ttu-id="6016c-123">Änderungen, die an einem ausgecheckten CMS-Element erfolgt sind, können im CMS gespeichert werden, bevor der Artikel eingecheckt oder veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="6016c-123">Changes that have been made to a checked-out CMS item can be saved to the CMS before the item is checked in or published.</span></span> <span data-ttu-id="6016c-124">Diese gespeicherten Änderungen sind nicht für andere authentifizierten Systembenutzer sichtbar, bis der Artikel eingecheckt ist.</span><span class="sxs-lookup"><span data-stu-id="6016c-124">These saved changes aren't visible to other authenticated system users until the item is checked in.</span></span> <span data-ttu-id="6016c-125">Sie sind nicht für externe Benutzer sichtbar, bis der Artikel veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="6016c-125">They aren't visible to external users until the item is published.</span></span> |
| <span data-ttu-id="6016c-126">Auschecken verworfen</span><span class="sxs-lookup"><span data-stu-id="6016c-126">Discarded check out</span></span> | <span data-ttu-id="6016c-127">Wenn ein ausgecheckter CMS-Artikel verworfen wird, werden sämtliche gespeicherten Änderungen gelöscht, und der Artikel wieder in der Version verwendet, die zuletzt eingecheckt wurde.</span><span class="sxs-lookup"><span data-stu-id="6016c-127">When a checked-out CMS item is discarded, all saved changes are deleted, and the item reverts to the version that was most recently checked in.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="6016c-128">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6016c-128">Additional resources</span></span>

[<span data-ttu-id="6016c-129">Möglichkeiten zum Hinzufügen von Inhalten</span><span class="sxs-lookup"><span data-stu-id="6016c-129">Ways to add content</span></span>](add-manage-content.md)

[<span data-ttu-id="6016c-130">Seitenmodellglossar</span><span class="sxs-lookup"><span data-stu-id="6016c-130">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="6016c-131">Arbeiten mit Veröffentlichungsgruppen</span><span class="sxs-lookup"><span data-stu-id="6016c-131">Work with publish groups</span></span>](publish-groups.md)

[<span data-ttu-id="6016c-132">Arbeiten mit Modulen</span><span class="sxs-lookup"><span data-stu-id="6016c-132">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="6016c-133">Arbeiten mit Fragmenten</span><span class="sxs-lookup"><span data-stu-id="6016c-133">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="6016c-134">Übersicht über Vorlagen und Layouts</span><span class="sxs-lookup"><span data-stu-id="6016c-134">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="6016c-135">Anpassen der Sitenavigation</span><span class="sxs-lookup"><span data-stu-id="6016c-135">Customize site navigation</span></span>](customize-site-navigation.md)
