---
title: Reparaturverwaltung
description: Für die Reparaturverwaltung können Probleme systematisch gruppiert werden. Dadurch können Lösungsvorschläge gemacht werden, die bereits in der Vergangenheit funktioniert haben.
author: ShylaThompson
manager: tfehr
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAConditionTable, SMASymptomArea, SMADiagnosisArea, SMAResolutionTable, SMARepairStage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4d45732ff35069a64b37b6c53d9e22adf9a9a46d
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3975607"
---
# <a name="repair-management"></a>Reparaturverwaltung       

[!include [banner](../includes/banner.md)]


Für die Reparaturverwaltung können Probleme systematisch gruppiert werden. Dadurch können Lösungsvorschläge gemacht werden, die bereits in der Vergangenheit funktioniert haben.

Zu diesem Zweck werden Einstellungen für Symptome, Diagnose und Lösung eingerichtet, die dann später bei der Reparatur ähnlicher Artikel angewendet werden können. Zum Nachverfolgen des Status einer Reparatur können auch Reparaturphasen eingerichtet werden.

## <a name="setting-up-repair-management"></a>Einrichten der Reparaturverwaltung

Verwenden Sie die folgenden Einrichtungsformulare, um Informationen über Symptome, Diagnose und Lösung in Bezug auf die Reparatur einzugeben.

1.  Klicken Sie auf **Serviceverwaltung** \> **Einrichten** \> **Reparatur** \> **Bedingungen**.

2.  Klicken Sie auf **Serviceverwaltung** \> **Einrichten** \> **Reparatur** \> **Symptombereiche**.

3.  Klicken Sie auf **Serviceverwaltung** \> **Einrichten** \> **Reparatur** \> **Diagnosebereiche**.

4.  Klicken Sie auf **Serviceverwaltung** \> **Einrichten** \> **Reparatur** \> **Lösungen**.

5.  Klicken Sie auf **Serviceverwaltung** \> **Einrichten** \> **Reparatur** \> **Reparaturphasen**.

## <a name="symptoms-and-conditions"></a>Symptome und Bedingungen

Bei den Symptomen handelt es sich um die Problembeschreibung des Kunden. Hierzu zählen auch die Informationen des Kunden zum Grund für die Reparatur.

Für Symptome können Symptombereiche und -codes sowie Bedingungen eingerichtet werden. Der Symptombereich enthält den Bereich der Fehlerfunktion, und der Symptomcode steht für das Symptom der Fehlerfunktion. Die Bedingung beschreibt die Situation oder Umgebung, in der das Problem auftritt.

**Beispiel**

Ein Kunde bringt einen Computer zur Reparatur, da die Festplatte nach längerer Computernutzung ausfällt. Der Festplattenausfall verursacht einen Bluescreen-Fehler. Der Techniker, der den Computer empfängt, gibt folgende Symptome und Bedingungen ein:

1.  Der Symptombereich ist die Festplatte.

2.  Der Symptomcode ist der Bluescreen-Fehler.

3.  Die Bedingung ist, dass die Festplatte nach längerer Computernutzung ausfällt.

## <a name="diagnosis-and-resolutions"></a>Diagnose und Lösungen

Die Felder für die Diagnose und die Lösung enthalten Informationen zur Reparatur. Hierbei handelt es sich um die Schritte, die von einem Techniker zum Ergründen des Problems ausgeführt wurden.

Im Diagnosebereich wird der Arbeitsgang angegeben, der zum Beheben des Problems ausgeführt werden muss. Der Diagnosecode gibt Aufschluss darüber, wie das Problem behandelt wurde. Für die Lösung kann beispielsweise angegeben werden, dass der Artikel repariert oder ausgetauscht wurde oder dass der Kunde den Auftrag storniert hat. Für den reparierten Computer können beispielsweise folgende Informationen angegeben werden: Diagnosebereich: "Teil defekt", Diagnosecode: "Einbau einer neuen Grafikkarte", Lösung: "Ausgetauscht".

## <a name="repair-stages"></a>Reparaturphasen

Anhand von Reparaturphasen lässt sich der Status der Reparatur ablesen. Die Reparaturphase verfügt über den Abzeichnungsparameter **Abgeschlossen**, mit dem angegeben wird, dass die Reparaturposition abgeschlossen ist und Enddatum sowie -zeit erfasst wurden.

## <a name="applying-repair-management"></a>Verwenden der Reparaturverwaltung

Zum Verwenden der Reparaturverwaltung muss der entsprechende Artikel in einem Serviceauftrag mit einer Serviceobjektbeziehung versehen sein. Im Serviceauftrag kann dann eine Reparaturposition mit Informationen zum vorliegenden Problem erstellt werden. In der Reparaturposition werden das zu reparierende Serviceobjekt sowie Informationen zu Symptomen, Diagnose und Ausführung angegeben. Darüber hinaus kann die Reparaturposition mit einem Hinweis versehen werden.

Reparaturpositionen können für jeden Schritt des Reparaturvorgangs erstellt werden.

## <a name="create-a-repair-line-on-a-service-order"></a>Erstellen einer Reparaturposition in einem Serviceauftrag

1.  Klicken auf **Serviceverwaltung** \> **Gemeinsam** \> **Serviceaufträge** \> **Serviceaufträge**.

2.  Wählen Sie den Serviceauftrag mit dem zu reparierenden Serviceobjekt aus.

3.  Klicken Sie **Reparatur** \> **Reparaturpositionen**, um das Formular **Reparaturpositionen** zu öffnen.

4.  Erstellen Sie durch Drücken von Strg+N eine neue Position.

5.  Wählen Sie ein Serviceobjekt aus. Sie können jedes beliebige Serviceobjekt auswählen, für das im Serviceauftrag eine Objektbeziehung eingerichtet wurde.

6.  Wählen Sie in der Reparaturposition die zutreffenden Werte für Symptome, Diagnose und Ausführung aus, und klicken Sie ggf. zum Erstellen eines Hinweises für die Reparaturposition auf die Registerkarte **Hinweis**.

7.  Drücken Sie zum Speichern der neuen Reparaturposition die Tastenkombination STRG+S. Das Feld **Erstellungsdatum und -uhrzeit** auf der Registerkarte **Allgemein** des Formulars **Reparaturpositionen** wird mit dem Zeitpunkt des Speichervorgangs aktualisiert.

## <a name="tracking-progress-and-resolving-a-repair-issue"></a>Nachverfolgen des Status und Beheben eines Reparaturproblems

Mithilfe der Reparaturphasen einer Reparaturposition lässt sich der Status der Reparatur nachverfolgen.

Nach erfolgter Reparatur kann die Reparaturposition abgeschlossen werden. Hierzu muss als Reparaturphase eine Phase gewählt werden, bei der die Eigenschaft **Abschlossen** aktiviert ist. Daraufhin werden in der Position das aktuelle Datum sowie die aktuelle Uhrzeit als Abschlusszeit erfasst.

## <a name="close-a-repair-line-for-a-resolved-issue"></a>Abschließen der Reparaturposition eines behobenen Problems

1.  Formular für **Reparaturpositionen**öffnen. Führen Sie die Schritte zum Erstellen einer Reparaturposition durch, die weiter oben in diesem Thema aufgeführt sind.

2.  Wählen Sie die Reparaturposition mit der abzuschließenden Reparatur aus.

3.  Wählen Sie im Feld **Reparaturphase** eine Phase aus, bei der die Eigenschaft **Abgeschlossen** aktiviert ist.

  


