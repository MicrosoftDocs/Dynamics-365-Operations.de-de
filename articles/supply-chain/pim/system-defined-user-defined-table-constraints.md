---
title: Systemdefinierte und benutzerdefinierte Tabelleneinschränkungen
description: 'Dieser Artikel beschreibt die zwei Arten von Tabelleneinschränkungen für Komponenten in einem Produktkonfigurationsmodell: benutzerdefiniert und systemdefiniert. Tabelleneinschränkungen stellen Matrizes der zulässigen Attributkombinationen dar, in denen jede Zeile einen Satz möglicher Attributwerte definiert.'
author: cvocph
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PCTableConstraintAttachAttributeTree, PCTableConstraintColumnSystem, PCTableConstraintContentUserDef, PCTableConstraintDefinition, PCTableConstraintWizard
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19781
ms.assetid: 0a4ea930-b344-43a8-871e-d5cd077892c4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 120ffe8e64629d0f99ac036d6ae6a933575903e3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4987153"
---
# <a name="system-defined-and-user-defined-table-constraints"></a>Systemdefinierte und benutzerdefinierte Tabelleneinschränkungen

[!include [banner](../includes/banner.md)]

Dieser Artikel beschreibt die zwei Arten von Tabelleneinschränkungen für Komponenten in einem Produktkonfigurationsmodell: benutzerdefiniert und systemdefiniert. Tabelleneinschränkungen stellen Matrizes der zulässigen Attributkombinationen dar, in denen jede Zeile einen Satz möglicher Attributwerte definiert.

Tabelleneinschränkungen stellen Matrizen aus Kombinationen von Attribute dar, die für Komponenten in einem Produktkonfigurationsmodell zulässig sind. Jede Zeile in der Tabelle definiert einen Satz möglicher Attributwerte. Sie können zwei Typen von Einschränkungen in einem Produktmodell deklarieren:

-   **Ausdruckseinschränkung** – Verwenden Sie Ausdruckseinschränkungen, um Beziehungen zwischen Attributen auszudrücken und sicherzustellen, dass bei der Produktkonfiguration nur kompatible Werte ausgewählt werden können.
-   **Tabelleneinschränkung** – Erstellen Sie eine Tabelle, die alle Kombinationen definiert, die für einen angegebenen Satz Attribute zulässig sind. Zwei Arten von Tabelleneinschränkungen sind verfügbar: benutzerdefinierte Tabelleneinschränkungen und systemdefinierte Tabelleneinschränkungen.

In diesem Artikel werden Tabelleneinschränkungen beschrieben, die benutzerdefiniert und für Komponenten in einem Produktkonfigurationsmodell systemdefiniert sind.

## <a name="user-defined-table-constraints"></a>Benutzerdefinierte Tabelleneinschränkungen
Eine benutzerdefinierte Tabelleneinschränkung ist eine Art Matrix, der verwendet wird, um den Satz der Kombinationen für die Attributwerte zu beschreiben, die von Attributtypen definiert werden. Wenn Sie zum Beispiel Lautsprecher herstellen, können Sie Spalten für die Oberfläche und den Grill in die benutzerdefinierte Tabelleneinschränkung einschließen. Der Attributtyp für die Oberfläche besitzt vier Werte, und der Attributtyp für den Grill hat drei Werte. Wenn keine Einschränkungen verwendet werden, gibt es 4 × 3 = 12 Kombinationen. In diesem Beispiel werden jedoch nur sechs Kombinationen zugelassen (wie in der folgenden Tabelle dargestellt) Diese Informationen werden auf der Registerkarte **Zulässige Kombinationen** auf der Seite **Tabelleneinschränkung bearbeiten** angezeigt.

| Gehäuseoberfläche | Vordergerippe |
|----------------|-------------|
| Schwarz          | Schwarz       |
| Schwarz          | Metall       |
| Eiche            | Schwarz       |
| Rosenholz       | Weiß       |
| Weiß          | Schwarz       |
| Weiß          | Weiß       |

Benutzerdefinierte Tabelleneinschränkungen werden durch die statische eingegebene Tabelle definiert, die genauso wie eine Ausdruckseinschränkung funktioniert. Wenn Sie eine benutzerdefinierte Tabelleneinschränkung verwenden, ist der Vorteil, dass Tabellen oftmals einfacher zu erstellen zu verstehen und verwalten sind als lange Ausdruckseinschränkungen.

## <a name="system-defined-table-constraints"></a>Vom System definierte Tabelleneinschränkungen
Eine systemdefinierte Tabelleneinschränkung schafft eine dynamische Verknüpfung zwischen einem Attributtyp und einem Feld in einer Tabelle. Wenn eine systemdefinierte Tabelleneinschränkung in einem Produktkonfigurationsmodell enthalten ist, stellt Zuordnung sicher, dass die Daten in der Tabelle anstelle der Werte des Attributtyps angezeigt werden. Das Ergebnis ist eine dynamische Einschränkung, da die Tabelleninhalte bearbeitet werden können (z. B. über andere Module).  

Wenn Sie eine systemdefinierte Tabelleneinschränkung erstellen, wählen Sie eine Tabelle aus, definieren die optional zu verwendende Abfrage, und ordnen Attributtypen den Feldern in der ausgewählten Tabelle zu. Die Typen der Felder müssen mit den Typen der Attributtypen übereinstimmen.  

Bevor sich eine Tabelleneinschränkung auf ein Produktkonfigurationsmodell auswirken kann, muss die Tabelleneinschränkung in einer Einschränkung für eine der Komponenten des Modells einbezogen werden. Dazu muss eine neue Einschränkung erstellt und dann erst der Tabelleneinschränkungstyp und anschließend die Tabelleneinschränkungsdefinition gewählt werden, die verwendet werden soll. Schließlich müssen alle Felder in der Tabelleneinschränkung zu den Attributen im Produktkonfigurationsmodell zugeordnet werden.

<a name="additional-resources"></a>Zusätzliche Ressourcen
--------

[Produktkonfigurationsmodelle – Überblick](product-configuration-models.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]