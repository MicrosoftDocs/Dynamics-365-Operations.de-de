---
title: Ein Experiment verbinden und Variationen bearbeiten
description: In diesem Artikel wird beschrieben, wie Sie ein Experiment in einem Dienst eines Drittanbieters mit Dynamics 365 Commerce verbinden und wie man Variationen für das Experiment bearbeitet.
author: sushma-rao
ms.date: 06/07/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.openlocfilehash: dcdbd61976402ddd719ece184a86692fbc7c628d
ms.sourcegitcommit: ddcb62bb5fbf26a1178c2bb1aec45a3d2362339e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/07/2022
ms.locfileid: "8942821"
---
# <a name="connect-an-experiment-and-edit-variations"></a>Ein Experiment verbinden und Variationen bearbeiten

In diesem Artikel wird beschrieben, wie Sie Ihr Experiment in Commerce verbinden und Änderungen an Ihren Variationen vornehmen, damit sie mit Ihrer Hypothese übereinstimmen. 

Das folgende Diagramm zeigt alle Schritte, die am Einrichten und Ausführen eines Experiments auf einer E-Commerce-Website in Dynamics 365 Commerce beteiligt sind. Weitere Schritte werden in separaten Artikeln behandelt.

[ ![User Journey zum Experimentieren – Verbindung und Bearbeitung.](./media/experimentation_connect_edit.svg) ](./media/experimentation_connect_edit.svg#lightbox)

Nach dem [Einrichten Ihres Experiments](experimentation-setup.md) in einem Drittanbieterdienst verbinden Sie das Experiment mit Dynamics 365 Commerce und bearbeiten Sie die Experimentvarianten.

## <a name="connect-your-experiment"></a>Ihr Experiment verbinden
Um Ihr Experiment zu verbinden, starten Sie den Assistenten **Experiment verbinden**. Der Assistent führt Sie durch die Schritte, die zum Verbinden Ihres Experiments erforderlich sind. Wenn Sie den Assistenten abgeschlossen haben, ist Ihr Experiment verbunden und Variationen werden erstellt und können bearbeitet werden.

Führen Sie die folgenden Schritte aus, um Ihr Experiment in Commerce Site Builder zu verbinden.

1. Um den **Experiment verbinden** Assistent zu starten, wählen Sie **Experimente** im linken Navigationsbereich und wählen Sie dann **Verbinden**. Alternativ können Sie über einen Seiten- oder Fragmenteditor auf den Assistenten zugreifen, indem Sie ihn bearbeiten und **Experiment verbinden** in der Befehlsleiste auswählen.

    > [!NOTE]
    > - Eine Seite kann jeweils nur mit einem Experiment verbunden werden. Um eine Seite mit einem anderen Experiment zu verbinden, löschen Sie zuerst das Experiment, mit dem die Seite derzeit verbunden ist.
    > - Sie können nur auf Seiten mit einem benutzerdefinierten Layout experimentieren. Wenn Ihre Seite ein voreingestelltes Layout hat, konvertieren Sie es zuerst in ein benutzerdefiniertes Layout. Sie können dies tun, indem Sie auf die Seite gehen und **In benutzerdefiniertes Layout konvertieren** in der Befehlsleiste auswählen. Weitere Informationen zu Layouts finden Sie unter [Voreingestellte und benutzerdefinierte Layouts](templates-layouts-overview.md#preset-and-custom-layouts). 

1. Wenn Sie eine Verbindung zu einem Experiment aus dem **Experimente** herstellen, wählen Sie auf der Registerkarte im linken Navigationsbereich den Namen des Experiments aus der angezeigten Liste aus.
1. Wählen Sie die Seite oder das Fragment aus, an der bzw. dem Sie Ihr Experiment ausführen möchten.
1. Wählen Sie im letzten Schritt des Assistenten die Option **Variationen generieren und Assistenten beenden**. Für das Experiment werden Variationen erstellt. 

> [!NOTE]
> Wenn Sie planen möchten, wann Ihr Experiment auf Ihrer Live-Site veröffentlicht wird, stellen Sie sicher, dass der Inhalt, den Sie dem Experiment zuordnen möchten, in einer Veröffentlichungsgruppe verfügbar ist, *bevor* Sie das Experiment verbinden. Weitere Informationen zu Veröffentlichungsgruppen finden Sie unter [Arbeiten mit Veröffentlichungsgruppen](publish-groups.md).

## <a name="edit-your-variations"></a>Ihre Variationen bearbeiten

Beim Verlassen des Assistenten **Experiment verbinden** werden Variationen für Sie erstellt. Folgen Sie den Schritten unten, und bearbeiten Sie die Variationen so, dass sie die Auswahlmöglichkeiten widerspiegeln, die Sie in der Experimenthypothese überprüfen müssen.

1. Verwenden Sie in der Editoransicht das Dropdown-Menü für Variationen unter der Befehlsleiste, um jede Variation basierend auf Ihrer ursprünglichen Hypothese zu bearbeiten. Möglicherweise möchten Sie auch eine Steuerungs- oder Basisvariation einrichten, indem Sie eine der Variationen unverändert lassen.
1. Wählen Sie das Modul aus, an dem experimentiert werden soll, wählen Sie die Auslassungspunkte (...) aus und wählen Sie dann **Zum Experiment hinzufügen**.

> [!NOTE]
> Erwägen Sie das Etablieren einer Steuerungs- oder Basisvariation, indem Sie eine der Variationen unverändert lassen.

## <a name="previous-step"></a>Vorheriger Schritt
[Einrichten eines Experiments](experimentation-setup.md) 


## <a name="next-step"></a>Nächster Schritt
[Vorschau und Veröffentlichung eines Experiments](experimentation-preview-publish.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
