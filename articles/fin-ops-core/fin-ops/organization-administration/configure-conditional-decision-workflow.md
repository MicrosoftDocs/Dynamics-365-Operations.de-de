---
title: Konfigurieren von bedingten Entscheidungen in einem Workflow
description: Verwenden Sie die folgenden Verfahren, um die Eigenschaften der bedingten Entscheidung zu konfigurieren.
author: ChrisGarty
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195703
ms.assetid: cd5554a4-210c-4c20-a7d3-4b1563c2b5df
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a593d4e188f47b73967f0c5468f7d7c3e9f64dc8
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567459"
---
# <a name="configure-conditional-decisions-in-a-workflow"></a>Konfigurieren von bedingten Entscheidungen in einem Workflow

[!include [banner](../includes/banner.md)]

Verwenden Sie die folgenden Verfahren, um die Eigenschaften der bedingten Entscheidung zu konfigurieren.

Eine bedingte Entscheidung ist ein Punkt, an dem ein Workflow sich in zwei Verzweigungen gabelt. Klicken Sie zum Konfigurieren einer bedingten Entscheidung im Workflow-Editor mit der rechten Maustaste auf die bedingte Entscheidung, und klicken Sie dann auf **Eigenschaften**, um das Formular **Eigenschaften** zu öffnen.

## <a name="name-a-decision"></a>Name einer Entscheidung

Gehen Sie folgendermaßen vor, um einen Namen für die bedingte Entscheidung einzugeben.

1. Klicken Sie im linken Bereich auf **Grundeinstellungen**.
2. Geben Sie im Feld **Name** einen eindeutigen Namen für die bedingte Entscheidung ein.

## <a name="set-conditions"></a>Festlegen von Bedingungen

Das System bestimmt durch Überprüfen, ob das übermittelte Dokument bestimmten Bedingungen entspricht, welche Verzweigung verwendet wird.

1. Klicken Sie im linken Bereich auf **Grundeinstellungen**.
2. Klicken Sie auf **Bedingung hinzufügen**.
3. Geben Sie eine Bedingung ein.
4. Geben Sie ggf. zusätzliche Bedingungen ein.
5. Führen Sie folgende Schritte aus, um die korrekte Konfiguration der eingegebenen Bedingungen zu überprüfen:

    1. Klicken Sie auf **Test**, um das Formular **Workflow-Bedingungen testen** zu öffnen.
    2. Wählen Sie im Bereich **Bedingung überprüfen** des Formulars einen Datensatz aus.
    3. Klicken Sie auf **Test**. Der Datensatz wird ausgewertet, um zu bestimmen, ob er den festgelegten Bedingungen entspricht.
    4. Klicken Sie auf **OK** oder **Abbrechen**, um zum Formular **Eigenschaften** zurückzukehren.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]