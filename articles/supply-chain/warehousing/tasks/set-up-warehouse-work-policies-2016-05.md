---
title: Richten Sie Lagerortarbeitsrichtlinien ein (Anwendung, im Mai 2016)
description: Lagerortprozesse enthalten nicht immer Lagerortarbeit.
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkPolicy, WMSLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 62fbf2f44216c300af5e092f5dbd05ef2239321b
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216780"
---
# <a name="set-up-warehouse-work-policies-application-may-2016"></a>Richten Sie Lagerortarbeitsrichtlinien ein (Anwendung, im Mai 2016)

[!include [banner](../../includes/banner.md)]

Lagerortprozesse enthalten nicht immer Lagerortarbeit. Wenn Sie eine Arbeitsrichtlinie definieren, können Sie die Erstellung von Arbeit für Rohmaterialentnahme sowie die Einlagerung fertiger Waren für einen Satz von Produkten an bestimmten Lagerplätzen verhindern. Das Demodatenunternehmen USMF wurde dazu verwendet, diese Aufzeichnung zu erstellen. Dieser Aufgabenleitfaden erfordert eine Dynamics AX-Anwendung der Version 7.0.1 oder später.

1. Wechseln Sie zu "Lagerortverwaltung" > "Einstellungen" > "Arbeit" > "Arbeitsrichtlinien".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Arbeitsrichtlinienname" die Bezeichnung "Keine Einlagerungsarbeit" ein.
4. Klicken Sie auf "Speichern".
5. Klicken Sie auf Hinzufügen.
6. Markieren Sie in der Liste die ausgewählte Zeile.
7. Wählen Sie im Feld "Arbeitsauftragstyp" die Option "Einlagerung fertiger Waren" aus.
8. Klicken Sie auf Hinzufügen.
9. Markieren Sie in der Liste die ausgewählte Zeile.
10. Wählen Sie im Feld "Arbeitsauftragstyp" die Option "Einlagerung von Co-Produkt und Nebenprodukt" aus.
11. Erweitern Sie den Abschnitt "Lagerplätze für Lagerbestand".
12. Klicken Sie auf Hinzufügen.
13. Markieren Sie in der Liste die ausgewählte Zeile.
14. In der Lagerortliste geben Sie "51" ein.
15. Geben Sie im Feld "Lagerplatz" den Wert "001" ein oder wählen Sie ihn aus.
16. Erweitern Sie den Abschnitt Produkte.
17. Wählen Sie im Feld "Produktauswahl" die Option "Ausgewählt" aus.
18. Klicken Sie auf Hinzufügen.
19. Markieren Sie in der Liste die ausgewählte Zeile.
20. Geben Sie im Feld "Artikelnummer" den Wert "L0101" ein oder wählen Sie ihn aus.
21. Klicken Sie auf "Speichern".

