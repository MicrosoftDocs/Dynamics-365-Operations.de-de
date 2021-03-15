---
title: Wartungsstatus
description: In diesem Thema wird erläutert, wie Sie den Instandhaltungsstatus in der Anlagenverwaltung berechnen.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetStatusCalculate, EntAssetStatus
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b5bac42d5cdc62361ee9a562e59bafa09ca7a215
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/16/2021
ms.locfileid: "5018495"
---
# <a name="maintenance-status"></a>Wartungsstatus

[!include [banner](../../includes/banner.md)]

 

Im Anlagenmanagement können Sie eine Übersichtskalkulation für eine bestimmte Periode für neue, aktive und abgeschlossene Wartungsanfragen, Arbeitsaufträge und Wartungsausfallzeiten durchführen. Sie können auch die Anzahl der abgeschlossenen Zustandsbewertungen für den gleichen Zeitraum sehen. Verwenden Sie diese Kalkulation, um sich einen Überblick über den Arbeitsaufwand bei eingehenden und abgeschlossenen Wartungsanfragen und Arbeitsaufträgen zu verschaffen.

## <a name="make-a-maintenance-status-calculation"></a>Eine Berechnung des Wartungsstatus durchführen

1. Klicken Sie auf **Anlagemanagement** > **Anfragen** > **Wartungsstatus**.

2. Wählen Sie im Dialog **Status berechnen** in den Feldern **Ab Datum** und **Bis Datum** den Zeitbereich aus, für den Sie die Berechnung durchführen möchten.

3. Über das Feld **Stufe** können Sie angeben, wie detailliert die Wartungszeilen zu Technischen Standorten sein sollen. 

  Wenn Sie z.B. die Zahl in das Feld einfügen und eine mehrstufige Struktur des Technischen Standorts haben, werden alle Wartungszeilen zu einem Technischen Standort auf der obersten Ebene angezeigt, so dass der Status auf einer Zeile von untergeordneten Technischen Standorten aufsummiert werden kann. 
  
  Wenn Sie in das Feld **Ebene** die Zahl „0“ eingeben, erhalten Sie ein detailliertes Ergebnis, das alle Wartungszeilen auf allen Ebenen des Technischen Standorts anzeigt, auf denen sie sich befinden.

4. Klicken Sie auf **OK**, um die Berechnung zu starten.

5. Klicken Sie auf die **Gruppieren nach…**-Schaltflächen, um die erforderliche Detailebene der Berechnung anzuzeigen. Die ausgewählten **Gruppieren nach…**-Schaltflächen werden hervorgehoben. Klicken Sie auf eine Schaltfläche, um sie zu aktivieren oder zu deaktivieren.

6. Denken Sie daran, auf die Schaltfläche **Aktualisieren** zu klicken, um die Berechnung jedes Mal zu aktualisieren, wenn Sie Änderungen vornehmen, indem Sie die **Gruppieren nach...**-Schaltflächen aktivieren oder deaktivieren oder eine Berechnung für einen neuen Zeitraum durchführen.

7. Klicken Sie auf **Status**, wenn Sie eine neue Berechnung des Wartungsstatus erstellen möchten.

>[!NOTE]
>Die unter **Wartungsstatus** angezeigten Ergebnisse umfassen nur Wartungsanforderungen und Arbeitsaufträge, die ein tatsächliches Startdatum und eine tatsächliche Startzeit haben. Enddatum und -zeit können leer sein.

## <a name="example-1"></a>Beispiel 1

Im Screenshot unten wurden die Schaltflächen **Jahr** und **Monat** aktiviert. Werden diese **Gruppieren nach...**-Optionen ausgewählt, erhalten Sie einen allgemeinen Überblick über den monatlichen Arbeitsaufwand und -durchsatz im Zusammenhang mit Wartungsanfragen und Arbeitsaufträgen. 

![Beispiel des monatlichen Arbeitsaufwands](media/13-controlling-and-reporting.png)

## <a name="example-2"></a>Beispiel 2

Im Screenshot unten wurden Informationen über funktionale Standorte hinzugefügt. Jetzt ist es möglich, Arbeitslast und Durchsatz über funktionale Standorte hinweg zu vergleichen, die geografische Standorte, Fabriken oder Arbeitsbereiche repräsentieren können. 

![Beispiel des monatlichen Arbeitsaufwands mit funktionalen Standorten](media/14-controlling-and-reporting.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]