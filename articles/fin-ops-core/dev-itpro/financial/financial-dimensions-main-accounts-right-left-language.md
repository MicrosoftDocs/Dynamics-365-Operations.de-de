---
title: Finanzdimensionen und Hauptkonten in Rechts-nach-links-Sprachen
description: In diesem Thema werden Entscheidungen beschrieben, die Sie treffen müssen, wenn Sie eine Rechts-nach-links-Sprache verwenden, und Sie müssen Finanzdimensionen und Hauptkonten einrichten.
author: RyanCCarlson2
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: tfehr
ms.custom: 222564
ms.assetid: 875dcebb-1bbb-4841-a8c6-9e134da07e96
ms.search.region: global
ms.author: rcarlson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 0c88b95ba7c596f4e8c1677c475ca92deba1cb71
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/10/2021
ms.locfileid: "7781744"
---
# <a name="financial-dimensions-and-main-accounts-in-right-to-left-languages"></a>Finanzdimensionen und Hauptkonten in Rechts-nach-links-Sprachen

[!include [banner](../includes/banner.md)]

In diesem Thema werden einige der Implementierungsentscheidungen beschrieben, die Sie berücksichtigen sollten, wenn Sie eine Rechts-nach-links-Sprache verwenden, und Sie müssen Finanzdimensionen und Hauptkonten einrichten.

Finanzdimensionen und Hauptkonten sind Schlüsselkomponenten der Planungsphase für eine Implementierung. Nachdem Finanzdimensionen und Hauptkonten im System erstellt wurden, werden sie auf den Seiten **Kontostrukturen konfigurieren**, **Erweiterte Regelstrukturen** und **Finanzdimensionskonfiguration zum Integrieren von Anwendungen** verwendet. Die Reihenfolge, die auf diesen Seiten definiert wird, wird im System für die Dateneingabe und -nutzung verwendet. An verschiedenen Stellen im System werden die Finanzdimensionen und Hauptkonten in separaten Feldern angezeigt. An anderen Stellen, wie Erfassungen, werden die Finanzdimensionen und Hauptkonten als einzelne Zeichenfolge angezeigt.

## <a name="best-practices-for-setting-up-financial-dimensions-and-main-accounts-in-a-right-to-left-system"></a>Optimale Verfahren zum Einrichten von Finanzdimensionen und Hauptkonten in einem Rechts-nach-links-System

- Wenn Sie das Trennzeichen für Kontenpläne auswählen, wählen Sie eine der Optionen für doppelte Trennzeichen aus: doppelter Bindestrich (`--`), doppelter Balken (`||`), doppelter Punkt (`..`) oder doppelter Unterstrich (`\\`).
- Wenn Sie Finanzdimensions- und Hauptkontowerte erstellen, verwenden Sie nur Nummern sowie Zeichen von Rechts-nach-Links-Sprachen.
- Vermeiden Sie es, die ausgewählte Trennzeichen für Kontenpläne in den Finanzdimensions- und Hauptkontowerten zu verwenden.

Indem Sie diese bewährten Methoden verwenden, tragen Sie zu einer konsistenten Darstellung der benutzerdefinierten Reihenfolge im gesamten System bei.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]