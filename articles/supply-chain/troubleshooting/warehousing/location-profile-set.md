---
title: Das Lagerplatzprofil verbietet negative Bestände, negative verfügbare Bestände sind jedoch zulässig
description: Die Option „Negativen Bestand zulassen“ ist für das Lagerplatzprofil auf „Nein“ festgelegt, das System lässt jedoch weiterhin negative Bestände zu.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WHSLocationProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: shawan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 2a7345281301ee70a512dfadcd553cb4eb33003904d0dddf6967659b693f60d7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742607"
---
# <a name="location-profile-disallows-negative-inventory-but-negative-on-hand-inventory-is-permitted"></a>Das Lagerplatzprofil verbietet negative Bestände, negative verfügbare Bestände sind jedoch zulässig

KB-Nummer: 4613622

## <a name="symptoms"></a>Symptome

Die Option **Negativen Bestand zulassen** ist für das Lagerplatzprofil auf *Nein* festgelegt, das System lässt jedoch weiterhin negative Bestände zu.

## <a name="example-scenario"></a>Beispielszenario

Bei staatlich regulierten Transaktionen muss das System in der Lage sein, negative Bestände zu erfassen, um Verluste zu buchen. Sie möchten, dass ein Artikel einen negativen Bestand aufweist, jedoch nur an bestimmten Lagerplätzen, z. B. in Tanks. Wenn die Artikelmodellgruppe jedoch einen negativen Bestand zulässt, spielt es keine Rolle, ob der Lagerlatz so eingestellt ist, dass ein negativer Bestand zulässig ist. Wenn der Artikel so eingerichtet ist, dass kein negativer Bestand zulässig ist, spielt es keine Rolle, wie das Lagerplatzprofil eingerichtet ist.

## <a name="resolution"></a>Lösung

Die Einstellung **Negativen Bestand zulassen** aus dem Lagerplatzprofil gilt nur für Lagerortprozesse, z. B. Kommissionierung. Artikelmodellgruppen, die so eingestellt sind, dass sie einen negativen Bestand zulassen, wirken sich jedoch auf alle Prozesse aus den Modulen „Bestandsverwaltung“ und „Lagerortverwaltung“ aus, und das Lagerplatzprofil überschreibt die Einstellung nicht.

Sie können steuern, ob ein Lagerort einen negativen Bestand führen darf. Stellen Sie Ihre Artikelmodellgruppen so ein, dass negative Bestände nicht zulässig sind, und legen Sie nur den entsprechenden Lagerort fest, um negative Bestände zuzulassen.
