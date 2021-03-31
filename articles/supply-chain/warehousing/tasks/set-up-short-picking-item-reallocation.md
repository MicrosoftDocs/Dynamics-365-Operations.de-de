---
title: Artikelneuzuordnung für Entnahme mit unzureichender Menge einrichten
description: In diesem Thema erfahren Sie, wie Sie Lagerarbeitern ermöglichen, alternative Lagerplätze schnell zu finden, wenn kein ausreichender Bestand am Lagerort vorhanden ist.
author: ShylaThompson
manager: tfehr
ms.date: 06/29/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkException, WHSWorker, WHSLocationWithWorkException
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3ecd05add44bacae517109f8bab2cb43376fe07c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5216810"
---
# <a name="set-up-short-picking-item-reallocation"></a>Artikelneuzuordnung für Entnahme mit unzureichender Menge einrichten

[!include [banner](../../includes/banner.md)]

In diesem Verfahren erfahren Sie, wie Sie Lagerarbeitern ermöglichen, alternative Lagerplätze schnell zu finden, wenn kein ausreichender Bestand am Lagerort vorhanden ist. 

Der Neuzuordnungsprozess wird von einer **Arbeitsausnahme** gesteuert und vom **Arbeiter** des Lagerorts verwendet.

Es ist möglich, automatische, manuelle oder beide Neuzuordnungsprozesse zu verwenden:

- Automatische Neuzuordnung – Lagerplatzrichtlinien werden verwendet, um festzustellen, ob die Waren an einem anderen Lagerplatz verfügbar sind. Wenn möglich, wird die Arbeit aktualisiert und der Lagerbenutzer wird zum alternativen Lagerplatz geleitet.
- Manuelle Neuzuordnung – Ermöglicht dem Lagerbenutzer die Auswahl aus einem oder mehreren Lagerplätzen mit nicht reservierten Warenmengen. 
- Automatisch und manuell – Wenn das System keine automatische Neuzuordnung durchführen kann und Lagerplätze mit nicht reservierten Mengen verfügbar sind, wird der Benutzer aufgefordert, einen Lagerplatz auszuwählen.

## <a name="set-up-work-exceptions"></a>Arbeitsausnahmen einrichten
Es ist möglich, dass mehrere Arbeitsausnahmen mit unterschiedlichen Artikelneuzuordnungsrichtlinien zu definieren, um den Lagerarbeitern die Auswahl basierend auf den Anforderungen der Lieferung zu ermöglichen, die diese verarbeitet.

Das Demodatenunternehmen USMF wurde verwendet, um diese Prozedur zu erstellen.

1. Gehen Sie im Navigationsbereich **Navigationsbereich** zu **Lagerverwaltung > Einrichtung > Arbeit > Arbeitsausnahmen**.
2. Klicken Sie auf **Neu**. 
3. Geben Sie im Feld **Arbeitsausnahmencode** einen Wert ein. Dies ist der Titel dieser Ausnahme. Beispiel: "Manuelle Entnahme".
4. Geben Sie im Feld **Beschreibung** einen Wert ein. Dies ist eine kurze Beschreibung der Verwendung dieser Ausnahme. Zum Beispiel: Kurze Entnahme – Artikel nicht verfügbar.
5. Wählen Sie im Feldtyp **Ausnahme** die Option **Kurze Entnahme** aus.
6. Aktivieren Sie das Kontrollkästchen **Bestand anpassen**. Wenn es aktiviert ist, wird der Lagerbestand am Kurzentnahmelagerplatz automatisch auf 0 angepasst.
7. Geben Sie im Feld **Standard-Einstellungsart Code** einen Wert ein oder wählen Sie ihn aus. In USMF können Sie beispielsweise **Remove Res Adj Out** auswählen. Jeder Anpassungstypcode enthält vier Merkmale: Name, Beschreibung, Bestandserfassungsname und **Reservierungen entfernen**. Wenn die Option **Reservierungen entfernen** aktiviert ist, werden die Reservierungen der Kurzentnahmebestellposition entfernt.  
8. Wählen Sie im Feld **Artikelneuzuordnung** einen Wert aus, zum Beispiel „Manuell“. Wenn Sie "Manuell" oder "Automatisch und manuell" auswählen, muss der Lagerarbeiter für die manuelle Neuzuordnung aktiviert werden.

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a>Eine Arbeitskraft für die manuell Artikelneuzuordnung einrichten

Das Demodatenunternehmen USMF wurde verwendet, um diese Prozedur zu erstellen.

1. Schließen Sie die Seite.
2. Gehen Sie im Navigationsbereich **Navigationsbereich** zu **Lagerverwaltung > Einrichtung > Arbeiter**.
3. Klicken Sie auf **Bearbeiten**.
4. Wählen Sie in der Liste die Arbeitskraft aus. Zum Beispiel Julia Funderburk.
5. Erweitern Sie das Inforegister **Benutzer**.
6. Wählen Sie in der Liste eine **Benutzer-ID** aus. Beispiel: 24.
7. Erweitern Sie das Inforegister **Arbeit**.
8. Wählen Sie **Ja** im Feld **Manuelle Artikelneuzuordnung zulassen** aus.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]