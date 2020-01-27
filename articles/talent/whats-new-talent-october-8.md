---
title: Neuerungen oder Änderungen in Dynamics 365 Talent – Core HR (8. Oktober 2018)
description: In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 Talent – Core HR entweder neu oder geändert sind.
author: Darinkramer
manager: AnnBe
ms.date: 10/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 30c148a1bf27a221c1d4feacbe89cabfc412872c
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897344"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-october-8-2018"></a>Neuerungen oder Änderungen in Dynamics 365 Talent – Core HR (8. Oktober 2018)

**Build 8.1.1050.0**

In diesem Thema werden die Funktionen beschrieben, die in Core HR entweder neu oder geändert sind.

## <a name="allow-other-dates-to-be-used-on-leave-tier-basis-leave-management"></a>Gestatten Sie andere Daten, die für Urlaubsebenengrundlagen (Urlaubs-Verwaltung )verwendet werden.

Wenn den Mitarbeitern Sonderurlaub bewilligt wird, bestimmt die Prämienebenengrundlage, wie viel Freizeit für einen Mitarbeiter anfällt. Aktuell basieren diese Ebenen auf Grundlage von Mitarbeiterstartdatum und Dienstalter. In einigen Szenarien brauchen Organisationen diese Ebenen, die auf anderen Daten basieren, wie Jahrestagsdatum oder ursprüngliches Einstellungsdatum. Diese Datumsangaben werden bereits im Urlaubplan, die bestimmen, wann Abgrenzungen finden statt, die Möglichkeit verwendet, sodass diese gleichen Daten verwendet werden können, wenn ein Mitarbeiter in einem Plan wurden hinzugefügt, um dem Abgrenzungsbetrag zu bestimmen registriert. 

## <a name="other-changes"></a>Andere Änderungen
Verschiedene Korrekturen sind in dieser Version berücksichtigt worden.

## <a name="known-issue"></a>Bekannte Probleme

**Problem:** Wenn einer Arbeitskraft ein neuer Anhang hinzugefügt wird, werden die Schaltflächen **Neu** und **Bearbeiten** abgeblendet. **Problemumgehung:**, Bevor die Anhangsseite geöffnet wird, überprüfen Sie, dass die Infoboxen **Arbeitskraft** geschlossen werden. Wenn die Infoboxen geschlossen werden, wenn die **Arbeitskraft**-Seite geladen wird, werden die Anhangschaltflächen aktiviert. (Dieses Problem wird in der folgenden Plattformaktualisierung korrigiert.)
