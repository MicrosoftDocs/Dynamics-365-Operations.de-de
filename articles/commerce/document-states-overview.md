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
# <a name="document-states-and-lifecycle"></a>Dokumentstatus und -Lebenszyklus

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

In diesem Thema werden die verschiedenen Dokumentstatus von Seitenelementen in Microsoft Dynamics 365 Commerce behandelt.

## <a name="document-state-descriptions"></a>Dokumentstatusbeschreibung

Die [Seitenelemente](page-elements-overview.md) der Themen führen verschiedene Dokumente im Content Management System (CMS) auf. Diese Dokumenttypen können mehrere Status im Erstellungstool haben. Die Dokumenttypen helfen, Datenkonflikte zu verhindern und Versionskontrollen zu erzwingen. Sie bestimmen, wer die Dokumente ändern kann, wenn die Dokumente geändert werden können und wenn Änderungen von anderen Personen angezeigt werden können.

Die folgende Tabelle enthält die möglichen Dokumentstatus von Seitenelementen in Commerce.

| Dokumentstatus | Beschreibung |
|---|---|
| Ausgecheckt | Wenn ein CMS-Artikel ausgecheckt wird von Ihnen, kann dies nicht von jedem beliebigen anderen authentifizierten Systembenutzern bearbeitet werden. Alle Änderungen, die Sie am Artikel vornehmen, sind nur für Sie angezeigt. |
| Eingecheckt | Wenn ein CMS-Artikel eingecheckt wird, sind alle Änderungen für andere authentifizierte Systembenutzer angezeigt, und die Benutzer können den Artikel dann auschecken und bearbeitet werden. Jedes Einchecken erstellt einen Dokumentversionsdatensatz im Workflowverlauf des Artikels. |
| Publiziert | Wenn ein CMS-Artikel veröffentlicht wird, wird er an Ihre Livesite weitergeleitet und wird im Internet für nicht-authentifizierte externe Benutzer sichtbar. Artikel können veröffentlicht werden, nachdem sie eingecheckt wurden. |
| Gespeichert | Änderungen, die an einem ausgecheckten CMS-Element erfolgt sind, können im CMS gespeichert werden, bevor der Artikel eingecheckt oder veröffentlicht wird. Diese gespeicherten Änderungen sind nicht für andere authentifizierten Systembenutzer sichtbar, bis der Artikel eingecheckt ist. Sie sind nicht für externe Benutzer sichtbar, bis der Artikel veröffentlicht wird. |
| Auschecken verworfen | Wenn ein ausgecheckter CMS-Artikel verworfen wird, werden sämtliche gespeicherten Änderungen gelöscht, und der Artikel wieder in der Version verwendet, die zuletzt eingecheckt wurde. |

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Möglichkeiten zum Hinzufügen von Inhalten](add-manage-content.md)

[Seitenmodellglossar](page-elements-overview.md)

[Arbeiten mit Veröffentlichungsgruppen](publish-groups.md)

[Arbeiten mit Modulen](work-with-modules.md)

[Arbeiten mit Fragmenten](work-with-fragments.md)

[Übersicht über Vorlagen und Layouts](templates-layouts-overview.md)

[Anpassen der Sitenavigation](customize-site-navigation.md)
