---
title: Konfigurieren einer bedingten Entscheidung in einem Workflow
description: Verwenden Sie die folgenden Verfahren, um die Eigenschaften der bedingten Entscheidung zu konfigurieren.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195703
ms.assetid: cd5554a4-210c-4c20-a7d3-4b1563c2b5df
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e9d5c8add546cad0446e863f64cac8f9cb603cbb
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

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






