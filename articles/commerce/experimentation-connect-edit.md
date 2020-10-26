---
title: Ein Experiment verbinden und Variationen bearbeiten
description: In diesem Thema wird beschrieben, wie Sie ein Experiment in einem Dienst eines Drittanbieters mit Dynamics 365 Commerce verbinden und wie man Variationen für das Experiment bearbeitet.
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
ms.openlocfilehash: ea1da0a7dc90b7197f3ee532bccc55d2ddbe4ddd
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930206"
---
# <a name="connect-an-experiment-and-edit-variations"></a>Ein Experiment verbinden und Variationen bearbeiten

In diesem Thema wird beschrieben, wie Sie Ihr Experiment in Commerce verbinden und Änderungen an Ihren Variationen vornehmen, damit diese mit Ihrer Hypothese übereinstimmen. Das folgende Diagramm zeigt alle Schritte, die am Einrichten und Ausführen eines Experiments auf einer E-Commerce-Website in Dynamics 365 Commerce beteiligt sind. Weitere Schritte werden in separaten Themen behandelt.

[ ![User Journey zum Experimentieren – Verbindung und Bearbeitung](./media/experimentation_connect_edit.svg) ](./media/experimentation_connect_edit.svg#lightbox)

Nach dem [Einrichten Ihres Experiments](experimentation-setup.md) in einem Drittanbieterdienst verbinden Sie das Experiment mit Dynamics 365 Commerce und bearbeiten Sie die Experimentvarianten.

## <a name="planning-considerations"></a>Planen von Aspekten

Bevor Sie Ihr Experiment in Commerce verbinden, müssen Sie einige Entscheidungen treffen, die sich auf die Art und Weise auswirken, wie Commerce Ihre Inhalte verwaltet.

### <a name="determine-the-scope-of-your-experiment"></a>Den Umfang Ihres Experiments bestimmen
Wenn Sie ein Experiment verbinden, werden Sie aufgefordert, den Umfang des Experiments zu definieren. Experimente sind definiert als **teilweiser** Umfang oder **ganzer** Umfang.
- Wählen Sie **teilweise**, wenn Sie ein Experiment für einen bestimmten Teil einer Seite durchführen möchten. Wenn Sie diese Option auswählen, müssen Sie angeben, welche Module im Experiment enthalten sind. Änderungen, die an Teilen der Standardseite oder des Standardfragments vorgenommen werden, die nicht mit dem Experiment zusammenhängen, werden automatisch über Variationen hinweg synchronisiert.
- Wählen Sie **ganz**, wenn Sie ein Experiment für eine ganze Seite oder ein Fragment durchführen möchten. Es werden separate Kopien der Standardseite oder des Standardfragments erstellt. Sie müssen nicht auswählen, welche Module im Experiment enthalten sind, da die gesamte Bearbeitungsfläche geändert werden kann. Sie können Module nach Bedarf hinzufügen, löschen und neu anordnen. Wenn jedoch Änderungen an der Standardseite oder dem Standardfragment vorgenommen werden, mit denen das Experiment verknüpft ist, müssen diese Änderungen über alle Variationen hinweg manuell synchronisiert werden.

<!-- not to editors, we're adding an image here to illustrate the difference. it will help.) -->

> [!NOTE]
> Wenn Sie Ihr Experiment einer Seite zuordnen, die ein Layout verwendet, können Sie das Experiment nur als **ganz** festlegen.

### <a name="decide-if-you-want-to-schedule-when-your-experiment-is-published"></a>Entscheiden Sie, ob Sie planen möchten, wann Ihr Experiment veröffentlicht wird
Wenn Sie planen möchten, wann Ihr Experiment auf Ihrer Live-Site veröffentlicht wird, stellen Sie sicher, dass der Inhalt, den Sie dem Experiment zuordnen möchten, in einer Veröffentlichungsgruppe verfügbar ist, *bevor* Sie das Experiment verbinden. 

Weitere Informationen zu Veröffentlichungsgruppen finden Sie unter [Arbeiten mit Veröffentlichungsgruppen](publish-groups.md).


## <a name="connect-your-experiment"></a>Ihr Experiment verbinden
Um Ihr Experiment zu verbinden, starten Sie den Assistenten **Experiment verbinden**. Der Assistent führt Sie durch die Schritte, die zum Verbinden Ihres Experiments erforderlich sind. Wenn Sie den Assistenten abgeschlossen haben, ist Ihr Experiment verbunden und Variationen werden erstellt und können bearbeitet werden.

1. Um den Assistenten zu starten, wählen Sie die **Experimente**-Registerkarte im Site Builder und dann **Verbinden** aus. Alternativ kann auf den Assistenten über einen Seiten- oder Fragmenteditor zugegriffen werden. Wählen Sie im Bearbeitungsmodus **Experiment verbinden** in der Befehlsleiste.

> [!NOTE]
> Eine Seite kann jeweils nur mit einem Experiment verbunden werden. Um eine Seite mit einem anderen Experiment zu verbinden, löschen Sie zuerst das Experiment, mit dem die Seite derzeit verbunden ist.

1. Wählen Sie die Seite oder das Fragment aus, an der bzw. dem Sie Ihr Experiment ausführen möchten.
1. Stellen Sie den Experimentierbereich auf **teilweise** oder **ganz** ein, basierend auf der Auswahl, die Sie im Abschnitt oben [Bestimmen Sie den Umfang Ihres Experiments](#determine-the-scope-of-your-experiment) getroffen haben.
    > [!NOTE]
    > Das Funktionsflag zum **Experimentieren an Seiten oder Fragmenten** muss aktiviert sein, wenn Sie mit einer ganzen Seite oder einem Fragment experimentieren möchten. Weitere Informationen finden Sie im Thema [Experimentieren in Dynamics 365 Commerce](experimentation-overview.md).
    
1. Wählen Sie im letzten Schritt des Assistenten die Option **Variationen generieren und Assistenten beenden**. Für das Experiment werden Variationen erstellt. 

## <a name="edit-your-variations"></a>Ihre Variationen bearbeiten
Wenn Sie den Assistenten beenden, werden Variationen für Sie erstellt. 

Als Nächstes bearbeiten Sie die Variationen so, dass sie die Auswahlmöglichkeiten widerspiegeln, die Sie in der Experimenthypothese überprüfen müssen. Wählen Sie eines der folgenden Verfahren, das dem Umfang entspricht, den Sie für Ihr Experiment im Abschnitt oben [Bestimmen Sie den Umfang Ihres Experiments](#determine-the-scope-of-your-experiment) ausgewählt haben.

### <a name="edit-variations-for-experiments-with-partial-scope"></a>Variationen für Experimente mit Teilumfang bearbeiten
Befolgen Sie diese Schritte, wenn Sie den Umfang Ihres Experiments als **teilweise** definiert haben im Assistenten **Experiment verbinden**.

1. Verwenden Sie in der Editoransicht das Dropdown-Menü für Variationen unter der Befehlsleiste, um jede Variation basierend auf Ihrer ursprünglichen Hypothese zu bearbeiten. Möglicherweise möchten Sie auch eine Steuerungs- oder Basisvariation einrichten, indem Sie eine der Variationen unverändert lassen.
1. Wählen Sie das Modul aus, an dem experimentiert werden soll, wählen Sie die Auslassungspunkte (...) aus und wählen Sie dann **Zum Experiment hinzufügen**.

### <a name="edit-variations-for-experiments-with-entire-scope"></a>Variationen für Experimente mit vollem Umfang bearbeiten
Wenn Sie den Umfang Ihres Experiments als **ganz** im Assistenten **Experiment verbinden** definiert haben, verwenden Sie in der Editoransicht das Dropdown-Menü für Variationen unter der Befehlsleiste, um jede Variation basierend auf Ihrer ursprünglichen Hypothese zu bearbeiten. 

> [!NOTE]
> In jedem Fall möchten Sie möglicherweise auch eine Steuerungs- oder Basisvariation einrichten, indem Sie eine der Variationen unverändert lassen.

## <a name="previous-step"></a>Vorheriger Schritt
[Einrichten eines Experiments](experimentation-setup.md) 


## <a name="next-step"></a>Nächster Schritt
[Vorschau und Veröffentlichung eines Experiments](experimentation-preview-publish.md)
