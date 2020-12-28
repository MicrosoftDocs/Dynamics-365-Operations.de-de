---
title: Anlagenfehleranalyse
description: In diesem Thema wird die Anlagenfehleranalyse in Asset Management erläutert.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectFaultCalculate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e911f7ca3b67acd9d5a1b170d8c99135da730847
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428818"
---
# <a name="asset-fault-analysis"></a>Anlagenfehleranalyse

[!include [banner](../../includes/banner.md)]

 

In Asset Management können Sie Anlagenfehlererfassungen analysieren, um eine Übersicht über die Gesamtzahl der Fehler zu erhalten, die für einen bestimmten Zeitraum erfasst werden. Fehlererfassungen können aus verschiedenen Perspektiven analysiert werden, beispielsweise mit dem Fokus auf Anlagen, Anlagentypen, funktionalen Standorten, Fehlersymptomen oder Fehlerarten.

1. Klicken Sie auf **Anlagenverwaltung** > **Abfragen** > **Anlagenfehler** > **Anlagenfehleranalyse**.

2. Im Dialogfeld **Anlagenfehleranalyseberechnung** können Sie das Feld **Ebene** verwenden, um anzugeben, wie detailliert die Anlagenfehlerpositionen in Bezug auf funktionale Standorte sein soll. 

    Wenn Sie beispielsweise die Zahl „1“ im Feld einfügen und eine funktionale Standortstruktur auf mehreren Ebenen haben, werden alle Anlagenfehlerpositionen für einen funktionalen Standort auf der höchsten Ebene angezeigt, und daher werden die Stunden in einer Position von den funktionalen Standorten auf einer niedrigeren Ebene hinzugefügt. 
        
    Wenn Sie die Zahl „0“ im Feld **Ebene** eingeben, wird ein detailliertes Ergebnis mit allen Anlagenfehlerpositionen für alle funktionalen Standortebenen angezeigt, denen sie zugeordnet sind.

3. Wenn Sie die Suche begrenzen möchten, können Sie bestimmte Anlagen, Fehlerdaten, Fehlerursachen und Fehlerlösungen auf dem Inforegister **Einzuschließende Datensätze** auswählen.

4. Klicken Sie auf **OK**, um die Berechnung zu starten.

5. Klicken Sie auf der Registerkarte **Anlagenfehleranalyse** auf eine oder mehrere **Gruppieren nach…**-Schaltflächen, um die Detailebene anzuzeigen, die Sie anzeigen möchten. Aktivierte Schaltflächen werden hervorgehoben. Aktivieren oder deaktivieren Sie Schaltflächen, indem Sie sie auf klicken.

6. Klicken Sie auf **Berechnungen aktualisieren**, um die Auswahl auf dem Bildschirm anzuzeigen. 

>[!NOTE]
>Denken Sie daran, bei jeder Aktivierung oder Deaktivierung einer **Gruppieren nach**-Schaltfläche auf die Schaltfläche **Berechnungen aktualisieren** zu klicken. Dies ist erforderlich, da eine große Datenmenge verarbeitet wird, während Sie die Fehlerwahrscheinlichkeit neu berechnen.

## <a name="examples"></a>Beispiele

Es gibt mehrere Möglichkeiten, Fehlererfassungen zu analysieren. Dieser Abschnitt zeigt anhand von fünf Beispielen, wie verschiedene Datenauswahlen mehr Einblick und Details bieten können, wenn Anlagenfehlererfassungen analysiert werden.

### <a name="group-by-symptoms"></a>Nach Symptomen gruppieren

Im Screenshot unten ist nur die Schaltfläche **Symptom** aktiviert.

- Fehlererfassungen sind für drei Fehlersymptome erfolgt: „Luftdurchlässigkeit“, „durchgebrannte Sicherung“ und „Gerät gestört“.  
- In der Spalte **Wahrscheinlichkeit %** summieren sich alle Prozentsätze auf 100 %. Die Wahrscheinlichkeit basiert auf allen **Symptom**-Erfassungen in dieser Fehleranalyse.

![Abbildung 1](media/06-controlling-and-reporting.png)

### <a name="group-by-symptoms-and-time-period"></a>Nach Symptomen und Zeitperiode gruppieren

Im Screenshot unten wurden **Jahr** und **Monat** hinzugefügt, um anzuzeigen, wie Sie Fehlererfassungen für eine ausgewählte Periode anzeigen können.

- Die Fehlersymptome werden nun als Erfassungen pro Monat/Jahr angezeigt.  
- In der Spalte **Wahrscheinlichkeit %** ergeben alle Sie Prozentsätze für jeden Monat 100 %, wenn Sie addiert werden. Die Wahrscheinlichkeit basiert auf den **Symptom**-Erfassungen in dieser Fehleranalyse. Wenn Sie viele Positionen in einer Anlage haben, aber eine Position einen sehr hohen Prozentsatz aufweist, ist dies ein Hinweis darauf, dass ein Fehlersymptom sorgfältiger untersucht werden sollte, um die Anzahl von Erfassungen für dieses Fehlersymptom einzuschränken.

![Abbildung 2](media/07-controlling-and-reporting.png)

### <a name="group-by-multiple-symptoms-and-assets"></a>Nach mehreren Symptomen und Anlagen gruppieren

Die Kombination von Anlagen und Anlagentyp wird als Grundlage für die Berechnung verwendet, die in den drei Screenshots unten angezeigt werden, was die Detailebene erhöht.  

Im Allgemeinen enthalten die Schaltflächen in den Aktivitätsbereichsgruppen **Nach Datum gruppieren**, **Nach Anlage gruppieren**, **Nach funktionalem Standort gruppieren** sowie die Schaltfläche **Fehler** (Fehlerkennung) Perioden oder Anlagenbeziehungen. Die Schaltflächen **Symptom**, **Bereich**, **Typ**, **Ursache** und **Behebung** sind die , die in der Fehlerverwaltung verwendet werden, um Anlagenfehlererfassungen zu analysieren und Problembereiche zu bestimmen.  

**Nach Symptom, Anlage und Anlagentyp gruppieren**

Im Screenshot unten wurden **Anlage** und **Anlagentyp** hinzugefügt, um weitere Informationen zu Fehlererfassungen bereitzustellen.

- Die Fehlersymptome werden jetzt in Kombinationen **Anlage** / **Anlagentyp** / **Symptom** eingeteilt.  
- Wenn Sie in der Spalte **Wahrscheinlichkeit %** alle Prozentsätze für die Kombination **Anlage** / **Anlagetyp** / **Symptom** jeweils addieren, ergeben sie jeweils 100 %. Die Wahrscheinlichkeit basiert auf den **Symptom**-Erfassungen in dieser Fehleranalyse. Wenn Sie viele Positionen in einer Anlage haben, aber eine Position einen sehr hohen Prozentsatz aufweist, ist dies ein Hinweis darauf, dass ein Fehlersymptom sorgfältiger untersucht werden sollte, um die Anzahl von Erfassungen für dieses Fehlersymptom einzuschränken.

![Abbildung 3](media/08-controlling-and-reporting.png)

**Nach zwei Symptomen, Anlage und Anlagentyp gruppieren**

Im Screenshot unten wurden **Bereich** zu **Symptom**, **Anlage** und **Anlagentyp** hinzugefügt, um weitere Informationen zu Fehlererfassungen bereitzustellen.

- Wenn Sie in der Spalte **Wahrscheinlichkeit %** alle Prozentsätze für die Kombination **Anlage** / **Anlagetyp** / **Symptom** für eine Anlage addieren, ergeben sie jeweils 100 %. Die Wahrscheinlichkeit basiert auf der Kombination aus **Symptom** und **Bereich** in dieser Fehleranalyse. Wenn Sie viele Positionen in einer Anlage haben, aber eine Position einen sehr hohen Prozentsatz aufweist, ist dies ein Hinweis darauf, dass ein Fehlerbereich sorgfältiger untersucht werden sollte, um die Anzahl von Erfassungen für diesen Fehlerbereich einzuschränken.  

![Abbildung 4](media/09-controlling-and-reporting.png)

**Nach drei Symptomen, Anlage und Anlagentyp gruppieren**

Im Screenshot unten wurde **Typ** hinzugefügt, und in diesem Beispiel wird die detaillierteste Berechnung angezeigt.
 
- Wenn Sie in der Spalte **Wahrscheinlichkeit %** alle Prozentsätze für die Kombination **Anlage** / **Anlagetyp** / **Symptom** für eine Anlage addieren, ergeben sie jeweils 100 %. Die Wahrscheinlichkeit basiert auf der Kombination aus **Symptom**, **Bereich** und **Typ** in dieser Fehleranalyse. Wenn Sie viele Positionen in einer Anlage haben, aber eine Position einen sehr hohen Prozentsatz aufweist, ist dies ein Hinweis darauf, dass ein Fehlertyp sorgfältiger untersucht werden sollte, um die Anzahl von Erfassungen für diesen Fehlertyp einzuschränken.

![Abbildung 5](media/10-controlling-and-reporting.png)


>[!NOTE]
>Einen Überblick über alle erstellten Fehlererfassungen für Arbeitsaufträgen und Wartungsanfragen erhalten Sie, indem Sie auf **Anlagenverwaltung** > **Abfragen** > **Anlagenfehler** > **Anlagenfehler** klicken. Wählen Sie auf der Seite **Anlagenfehler** eine Anlagenfehlererfassung aus, und erweitern Sie den Bereich **Zugehörige Informationen**, um Informationen zum zugehörigen Arbeitsauftrag oder zur zugehörigen Wartungsanforderung anzuzeigen.

