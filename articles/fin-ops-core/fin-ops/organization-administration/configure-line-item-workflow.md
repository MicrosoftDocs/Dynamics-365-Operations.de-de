---
title: Positionsworkflows konfigurieren
description: In diesem Artikel wird erläutert, wie das Positionsworkflowelement konfiguriert wird.
author: ChrisGarty
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195833
ms.assetid: 3237347e-71d5-4569-bc9a-0d0fc9410b78
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 511493df4c897c0a8d2c53db2c9c893aa43d3589
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8889235"
---
# <a name="configure-line-item-workflows"></a>Positionsworkflows konfigurieren

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

In diesem Artikel wird erläutert, wie das Positionsworkflowelement konfiguriert wird.

Klicken Sie zum Konfigurieren eines Positionsworkflowelements im Workflow-Editor mit der rechten Maustaste auf das Element, und klicken Sie dann auf **Eigenschaften**, um die Seite **Eigenschaften** zu öffnen. Verwenden Sie die folgenden Verfahren, um die Eigenschaften des Positionsworkflowelements zu konfigurieren.

## <a name="name-the-line-item-workflow-element"></a>Benennen des Positionsworkflowelements

Gehen Sie folgendermaßen vor, um einen Namen für das Positionsworkflowelement einzugeben.

1. Klicken Sie im linken Bereich auf **Grundeinstellungen**.
2. Geben Sie im Feld **Name** einen eindeutigen Namen für das Positionsworkflowelement ein.

## <a name="specify-whether-the-same-workflow-is-used-to-process-all-line-items"></a>Angeben, ob derselbe Workflow zum Verarbeiten aller Positionen verwendet wird

Gehen Sie folgendermaßen vor, um anzugeben, ob derselbe Workflow zum Verarbeiten aller Positionen in einem Dokument verwendet wird.

1. Klicken Sie im linken Bereich auf **Grundeinstellungen**.
2. Wird derselbe Workflow zum Verarbeiten aller Positionen in einem Dokument verwendet, klicken Sie **Einzelnen Workflow für alle Positionen aufrufen** auf. Wählen Sie anschließend den Workflow zum Verarbeiten der Positionen aus.
3. Wenn ein bestimmter Workflow Positionen verarbeiten sollte, die einen bestimmten Satz von Bedingungen erfüllen, klicken Sie auf **Einen Workflow für jede Position aufrufen**. Folgen Sie diesen Schritten, um die Bedingungen festzulegen:

    1. Klicken Sie auf **Hinzufügen**.
    2. Wählen Sie die Bedingung in der Tabelle aus.
    3. Geben Sie auf der Registerkarte **Bedingungsname** einen Namen für die festzulegenden Bedingungen ein.
    4. Klicken Sie auf **Bedingung hinzufügen**, um die Bedingung einzugeben.
    5. Geben Sie alle notwendigen zusätzlichen Bedingungen ein.
    6. Klicken Sie auf **Test**, um zu überprüfen, ob die eingegebenen Bedingungen korrekt konfiguriert sind. Auf der Seite **Workflowbedingung testen** im Bereich **Bedingung überprüfen** wählen Sie einen Datensatz aus und klicken auf **Test**. Der Datensatz wird ausgewertet, um zu bestimmen, ob er den festgelegten Bedingungen entspricht. Klicken Sie auf **OK** oder **Abbrechen**, um zur Seite **Eigenschaften** zurückzukehren.

    Wählen Sie auf der Registerkarte **Workflow** den Workflow aus, der verwendet werden soll zum Verarbeiten von Positionen, die die definierten Bedingungen erfüllen.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]