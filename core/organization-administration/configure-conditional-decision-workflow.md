---
title: Konfigurieren einer bedingten Entscheidung in einem Workflow
description: Verwenden Sie die folgenden Verfahren, um die Eigenschaften der bedingten Entscheidung zu konfigurieren.
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 195703
ms.assetid: cd5554a4-210c-4c20-a7d3-4b1563c2b5df
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: c21c8e33ab3a88e1b93ca81d6f0770f1c77fe139
ms.contentlocale: de-de
ms.lasthandoff: 05/25/2017


---

# <a name="configure-a-conditional-decision-in-a-workflow"></a>Konfigurieren einer bedingten Entscheidung in einem Workflow

[!include[banner](../includes/banner.md)]


Verwenden Sie die folgenden Verfahren, um die Eigenschaften der bedingten Entscheidung zu konfigurieren.

Eine bedingte Entscheidung ist ein Punkt, an dem ein Workflow sich in zwei Verzweigungen gabelt. Klicken Sie zum Konfigurieren einer bedingten Entscheidung im Workflow-Editor mit der rechten Maustaste auf die bedingte Entscheidung, und klicken Sie dann auf **Eigenschaften**, um das Formular **Eigenschaften** zu öffnen.

## <a name="name-a-decision"></a>Name einer Entscheidung
Gehen Sie folgendermaßen vor, um einen Namen für die bedingte Entscheidung einzugeben.
1.  Klicken Sie im linken Bereich auf **Grundeinstellungen**.
2.  Geben Sie im Feld **Name** einen eindeutigen Namen für die bedingte Entscheidung ein.

## <a name="set-conditions"></a> Festlegen von Bedingungen
Das System bestimmt durch Überprüfen, ob das übermittelte Dokument bestimmten Bedingungen entspricht, welche Verzweigung verwendet wird.
1.  Klicken Sie im linken Bereich auf **Grundeinstellungen**.
2.  Klicken Sie auf **Bedingung hinzufügen**.
3.  Geben Sie eine Bedingung ein.
4.  Geben Sie ggf. zusätzliche Bedingungen ein.
5.  Führen Sie folgende Schritte aus, um die korrekte Konfiguration der eingegebenen Bedingungen zu überprüfen:
    1.  Klicken Sie auf **Test**, um das Formular **Workflow-Bedingungen testen** zu öffnen.
    2.  Wählen Sie im Bereich **Bedingung überprüfen** des Formulars einen Datensatz aus.
    3.  Klicken Sie auf **Test**. Der Datensatz wird ausgewertet, um zu bestimmen, ob er den festgelegten Bedingungen entspricht.
    4.  Klicken Sie auf **OK** oder **Abbrechen**, um zum Formular **Eigenschaften** zurückzukehren.






