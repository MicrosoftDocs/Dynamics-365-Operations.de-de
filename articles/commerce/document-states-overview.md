---
title: Dokumentstatus und -Lebenszyklus
description: In diesem Thema werden die verschiedenen Dokumentstatus von Seitenelementen in Microsoft Dynamics 365 Commerce behandelt.
author: phinneyridge
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 7c30932800beda13ac8fe6b0386fe29efe93f79c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982615"
---
# <a name="document-states-and-lifecycle"></a><span data-ttu-id="f702a-103">Dokumentstatus und -Lebenszyklus</span><span class="sxs-lookup"><span data-stu-id="f702a-103">Document states and lifecycle</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f702a-104">In diesem Thema werden die verschiedenen Dokumentstatus von Seitenelementen in Microsoft Dynamics 365 Commerce behandelt.</span><span class="sxs-lookup"><span data-stu-id="f702a-104">This topic covers the various document states of page elements in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="document-state-descriptions"></a><span data-ttu-id="f702a-105">Dokumentstatusbeschreibung</span><span class="sxs-lookup"><span data-stu-id="f702a-105">Document state descriptions</span></span>

<span data-ttu-id="f702a-106">Die [Seitenelemente](page-elements-overview.md) der Themen führen verschiedene Dokumente im Content Management System (CMS) auf.</span><span class="sxs-lookup"><span data-stu-id="f702a-106">The [Page elements](page-elements-overview.md) topic lists various documents types in the content management system (CMS).</span></span> <span data-ttu-id="f702a-107">Diese Dokumenttypen können mehrere Status im Erstellungstool haben.</span><span class="sxs-lookup"><span data-stu-id="f702a-107">These document types can have several states in the authoring tool.</span></span> <span data-ttu-id="f702a-108">Die Dokumenttypen helfen, Datenkonflikte zu verhindern und Versionskontrollen zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="f702a-108">The document states help prevent data conflicts and enforce version control.</span></span> <span data-ttu-id="f702a-109">Sie bestimmen, wer die Dokumente ändern kann, wenn die Dokumente geändert werden können und wenn Änderungen von anderen Personen angezeigt werden können.</span><span class="sxs-lookup"><span data-stu-id="f702a-109">They determine who can change the documents, when the documents can be changed, and when changes can be viewed by other people.</span></span>

<span data-ttu-id="f702a-110">Die folgende Tabelle enthält die möglichen Dokumentstatus von Seitenelementen in Commerce.</span><span class="sxs-lookup"><span data-stu-id="f702a-110">The following table shows the possible document states of page elements in Commerce.</span></span>

| <span data-ttu-id="f702a-111">Dokumentstatus</span><span class="sxs-lookup"><span data-stu-id="f702a-111">Document state</span></span>      | <span data-ttu-id="f702a-112">Site Builder Aktivität</span><span class="sxs-lookup"><span data-stu-id="f702a-112">Site builder action</span></span>        | <span data-ttu-id="f702a-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f702a-113">Description</span></span>                                                  |
| ------------------- | -------------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="f702a-114">Ausgecheckt</span><span class="sxs-lookup"><span data-stu-id="f702a-114">Checked out</span></span>         | <span data-ttu-id="f702a-115">Wählen Sie **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="f702a-115">Select **Edit**.</span></span>           | <span data-ttu-id="f702a-116">Das entsprechende Dokument wird Ihnen ausgecheckt.</span><span class="sxs-lookup"><span data-stu-id="f702a-116">The applicable document is checked out to you.</span></span> <span data-ttu-id="f702a-117">Während sich ein Dokument in diesem Status befindet, kann es von anderen authentifizierten Systembenutzern nicht geändert werden, und alle Änderungen, die Sie am Dokument vornehmen, sind nur für Sie sichtbar.</span><span class="sxs-lookup"><span data-stu-id="f702a-117">While a document is in this state, it can't be changed by other authenticated system users, and any changes that you make to the document are visible only to you.</span></span> |
| <span data-ttu-id="f702a-118">Gespeichert</span><span class="sxs-lookup"><span data-stu-id="f702a-118">Saved</span></span>               | <span data-ttu-id="f702a-119">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="f702a-119">Select **Save**.</span></span>           | <span data-ttu-id="f702a-120">Änderungen, die an einem ausgecheckten Dokument vorgenommen wurden, werden in der Datenbank gespeichert, das Dokument ist jedoch noch nicht eingecheckt oder veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="f702a-120">Changes that have been made to a checked-out document are saved to the database, but the document isn't yet checked in or published.</span></span> <span data-ttu-id="f702a-121">Die gespeicherten Änderungen sind nicht für andere authentifizierten Systembenutzer sichtbar, bis der Artikel **Bearbeitung beendet** gewählt wird.</span><span class="sxs-lookup"><span data-stu-id="f702a-121">The saved changes aren't visible to other authenticated system users until the author selects **Finish editing**.</span></span> <span data-ttu-id="f702a-122">Sie sind nicht für externe Benutzer sichtbar, bis der Artikel veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="f702a-122">They aren't visible to external users until the item is published.</span></span> |
| <span data-ttu-id="f702a-123">Auschecken verworfen</span><span class="sxs-lookup"><span data-stu-id="f702a-123">Discarded check out</span></span> | <span data-ttu-id="f702a-124">Wählen Sie **Änderungen verwerfen**.</span><span class="sxs-lookup"><span data-stu-id="f702a-124">Select **Discard edits**.</span></span>  | <span data-ttu-id="f702a-125">Alle Änderungen am ausgecheckten Dokument werden verworfen, und das Element wird auf die zuletzt eingecheckte Version zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="f702a-125">All changes to the checked-out document are discarded, and the item reverts to the last version that was checked in.</span></span> |
| <span data-ttu-id="f702a-126">Eingecheckt</span><span class="sxs-lookup"><span data-stu-id="f702a-126">Checked in</span></span>          | <span data-ttu-id="f702a-127">Wählen Sie **Beenden Sie die Bearbeitung**.</span><span class="sxs-lookup"><span data-stu-id="f702a-127">Select **Finish editing**.</span></span> | <span data-ttu-id="f702a-128">Das bearbeitete Dokument ist eingecheckt.</span><span class="sxs-lookup"><span data-stu-id="f702a-128">The edited document is checked in.</span></span> <span data-ttu-id="f702a-129">Alle Änderungen sind für andere authentifizierte Systembenutzer sichtbar, und diese Benutzer können das Dokument dann bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="f702a-129">All changes are visible to other authenticated system users, and those users can then edit the document.</span></span> <span data-ttu-id="f702a-130">Jedes Einchecken erstellt einen Dokumentversionsdatensatz im Workflowverlauf des Artikels.</span><span class="sxs-lookup"><span data-stu-id="f702a-130">Each check-in creates a document version record in the item's history.</span></span> |
| <span data-ttu-id="f702a-131">Publiziert</span><span class="sxs-lookup"><span data-stu-id="f702a-131">Published</span></span>           | <span data-ttu-id="f702a-132">Wählen Sie **Veröffentlichen** aus.</span><span class="sxs-lookup"><span data-stu-id="f702a-132">Select **Publish**.</span></span>        | <span data-ttu-id="f702a-133">Das Dokument wird veröffentlicht, und die Änderungen werden auf Ihre Live-Site übertragen und können von externen Benutzern erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="f702a-133">The document is published, and the changes are pushed to your live site and become discoverable by external users.</span></span> <span data-ttu-id="f702a-134">Artikel können nur veröffentlicht werden, wenn sie zuerst eingecheckt wurden durch Auswahl von **Bearbeitung beenden**.</span><span class="sxs-lookup"><span data-stu-id="f702a-134">Items can be published only if they have first been checked in by selecting **Finish editing**.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="f702a-135">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f702a-135">Additional resources</span></span>

[<span data-ttu-id="f702a-136">Möglichkeiten zum Hinzufügen von Inhalten</span><span class="sxs-lookup"><span data-stu-id="f702a-136">Ways to add content</span></span>](add-manage-content.md)

[<span data-ttu-id="f702a-137">Seitenmodellglossar</span><span class="sxs-lookup"><span data-stu-id="f702a-137">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="f702a-138">Arbeiten mit Veröffentlichungsgruppen</span><span class="sxs-lookup"><span data-stu-id="f702a-138">Work with publish groups</span></span>](publish-groups.md)

[<span data-ttu-id="f702a-139">Aktivieren und verwenden Sie die kanalübergreifende Freigabe</span><span class="sxs-lookup"><span data-stu-id="f702a-139">Enable and use cross-channel sharing</span></span>](cross-channel-sharing.md)

[<span data-ttu-id="f702a-140">Arbeiten mit Modulen</span><span class="sxs-lookup"><span data-stu-id="f702a-140">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="f702a-141">Arbeiten mit Fragmenten</span><span class="sxs-lookup"><span data-stu-id="f702a-141">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="f702a-142">Übersicht über Vorlagen und Layouts</span><span class="sxs-lookup"><span data-stu-id="f702a-142">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="f702a-143">Anpassen der Sitenavigation</span><span class="sxs-lookup"><span data-stu-id="f702a-143">Customize site navigation</span></span>](customize-site-navigation.md)
