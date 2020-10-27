---
title: Eine Variation höher stufen und ein Experiment abschließen
description: In diesem Thema wird beschrieben, wie Sie eine erfolgreiche Variation höher stufen und ein Experiment in Dynamics 365 Commerce abschließen können.
author: sushma-rao
manager: AnnBe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 2e011f10e908d6a2efe2e928fc5e0abc7659cb8b
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930200"
---
# <a name="promote-a-variation-and-complete-an-experiment"></a>Eine Variation höher stufen und ein Experiment abschließen

In diesem Thema wird beschrieben, wie Sie die Variation höher stufen, mit der die besten Ergebnisse in Ihrem Experiment erzielt wurden, und wie Sie das Experiment abschließen. Das folgende Diagramm zeigt alle Schritte, die am Einrichten und Ausführen eines Experiments auf einer E-Commerce-Website in Dynamics 365 Commerce beteiligt sind. Weitere Schritte werden in separaten Themen behandelt.

[ ![User Journey zum Experimentieren – Überprüfung und Abschluss](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)

Nachdem Sie [Ihr Experiment ausgeführt](experimentation-run-monitor.md) und genügend Daten gesammelt haben, um zu bestimmen, welche Variation Sie auf Ihrer Live-Site verwenden möchten, stufen Sie die Variation höher und beenden das Experiment.

## <a name="promote-a-variation"></a>Eine Variation höher stufen
Verwenden Sie die Daten und Analysen zum Experiment im Drittanbieterdienst, um zu entscheiden, welche Variante die besten Ergebnisse liefert. Gehen Sie wie folgt vor, um den aktuellen Inhalt der Live-Site durch die Gewinnervariante zu ersetzen, damit sie allen Benutzern Ihrer Website zur Verfügung steht. 

1. Gehen Sie zur Registerkarte **Experimente** im Site Builder, und wählen Sie das Experiment aus.
1. Wählen Sie **Experiment abschließen** in der oberen Leiste aus.
1. Wählen Sie im Dialogmenü **Experiment abschließen** die Option **Versuchsdaten überprüfen** aus. Der Dienst eines Drittanbieters wird geöffnet, in dem Sie die Metriken überprüfen und feststellen können, welche Variation am besten funktioniert.
1. Wählen Sie im Dialogmenü **Experiment abschließen** im Site Builder die Gewinnervariante aus, und wählen Sie dann **Weiter**.
1. Öffnen Sie den Dienst eines Drittanbieters und beenden Sie das Experiment.
1. Wählen Sie im Site Builder **Abschließen** aus, um die ursprüngliche Live-Seite zu überschreiben und die Gewinnervariante zu veröffentlichen, damit sie allen Benutzern Ihrer Website zur Verfügung steht. 

> [!NOTE]
> Wenn Sie die aktuelle Live-Seite beibehalten und keine Variation veröffentlichen möchten, wählen Sie **Originalseite erneut veröffentlichen** aus.

## <a name="delete-your-experiment"></a>Experiment löschen
Während es nicht erforderlich ist, ein abgeschlossenes Experiment in Commerce zu löschen, können Sie es löschen, um Speicherplatz zu sparen oder Ihren Arbeitsbereich zu bereinigen. Gehen Sie wie folgt vor, um ein Experiment zu löschen.

1. Gehen Sie zur Registerkarte **Experimente** im Site Builder, und wählen Sie das Experiment aus. 
    > [!NOTE]
    > Wenn das Experiment noch aktiv ist, beenden Sie das Experiment im Dienst eines Drittanbieters, bevor Sie fortfahren.
1. Wählen Sie **Veröffentlichung aufheben** in der Befehlsleiste aus, um den Variationsinhalt von der Live-Site zu entfernen.
1. Wählen Sie **Löschen** in der Befehlsleiste aus, um das Experiment zu löschen.

## <a name="previous-step"></a>Vorheriger Schritt
[Ein Experiment ausführen und überwachen](experimentation-run-monitor.md)
