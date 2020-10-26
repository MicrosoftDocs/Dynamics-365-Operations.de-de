---
title: Ein Experiment ausführen und überwachen
description: In diesem Thema wird beschrieben, wie Sie ein Experiment in einem Drittanbieterdienst ausführen und überwachen. Außerdem wird beschrieben, wie Sie nach Beginn des Experiments Änderungen an Variationen vornehmen.
author: sushma-rao
manager: AnnBe
ms.date: 10/01/2020
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
ms.openlocfilehash: 4cb7d863d9d69612aa0c340099c1f7861c9d12ba
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930203"
---
# <a name="run-and-monitor-an-experiment"></a>Ein Experiment ausführen und überwachen

In diesem Thema wird beschrieben, wie Sie Ihr Experiment in einer Drittanbieter-App ausführen und überwachen und bei Bedarf Variationen ändern. Bevor Sie die Schritte in diesem Thema ausführen, müssen Sie Ihr Experiment in Commerce [veröffentlichen](experimentation-preview-publish.md). Das folgende Diagramm zeigt alle Schritte, die am Einrichten und Ausführen eines Experiments auf einer E-Commerce-Website in Dynamics 365 Commerce beteiligt sind. Weitere Schritte werden in separaten Themen behandelt.

[ ![User Journey zum Experimentieren – Ausführung und Überwachung](./media/experimentation_run_monitor.svg) ](./media/experimentation_run_monitor.svg#lightbox)

Nachdem Sie Ihre Variationen veröffentlicht haben, werden alle Schritte ausgeführt, die Sie in Commerce ausführen müssen, um Ihr Experiment auszuführen. Der nächste Schritt besteht darin, zu bestimmen, welche Variation jedem Benutzer angezeigt werden soll, wenn er eine Seite anfordert. Der Drittanbieterdienst trifft diese Entscheidung, aber zuerst müssen Sie das Experiment innerhalb des Dienstes aktivieren. Da die Schritte zum Aktivieren eines Experiments von Dienst zu Dienst unterschiedlich sind, müssen Sie die Anweisungen Ihres Dienstes oder Anbieters befolgen. Wenn das Experiment nicht aktiviert ist, wird den Benutzern nur die Standardversion der Seite angezeigt. Es werden keine Variationen angezeigt.

Sie müssen das Experiment lange genug laufen lassen, um Daten für statistisch gültige Ergebnisse zu sammeln. Verwenden Sie den Dienst eines Drittanbieters, um die experimentellen Daten und Analysen zu überwachen, während das Experiment ausgeführt wird.

## <a name="adjust-your-variations"></a>Ihre Variationen anpassen
Wenn Sie aus irgendeinem Grund Ihre Variationen ändern müssen, führen Sie die folgenden Schritte aus.

> [!IMPORTANT]
> Wenn Sie Änderungen an einem Live-Experiment in Commerce oder dem Drittanbieterdienst vornehmen, können Ihre Ergebnisse erheblich beeinträchtigt werden. Lassen Sie das Experiment seinen Lauf nehmen und lassen Sie dann ein neues Experiment für größere Änderungen erstellen.

1. Gehen Sie zur Registerkarte **Experimente** im Site Builder, und wählen Sie das Experiment aus. 
1. Wählen Sie aus dem Dropdown-Menü die Variante aus, die Sie aktualisieren möchten.
1. Nehmen Sie die erforderlichen Änderungen vor und zeigen Sie die Variationen in der Vorschau an und veröffentlichen Sie sie. Weitere Informationen finden Sie unter [Vorschau und Veröffentlichung eines Experiments](experimentation-preview-publish.md).
1. Wechseln Sie zum Drittanbieterdienst, um Änderungen im Zusammenhang mit dem Experimentaufbau vorzunehmen.
    
## <a name="previous-step"></a>Vorheriger Schritt
[Vorschau und Veröffentlichung eines Experiments](experimentation-preview-publish.md)

## <a name="next-step"></a>Nächster Schritt
[Eine Variation höher stufen und ein Experiment abschließen](experimentation-review-complete.md)
