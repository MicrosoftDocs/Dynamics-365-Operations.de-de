---
title: Lagerplätze für Lagerbestand
description: Lagerplätze für Lagerbestand werden mit grundlegendem Warehousing (WMS I) verwendet , um zu bestimmen, wo Artikel in einem WMS I-Lagerort gelagert und entnommen werden.
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSLocation
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2134
ms.assetid: 69bf6922-4151-447f-b678-4ba95637f54c
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ce1e33fab6704dd3387f0c2034a8a950a858b2e0
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2019
ms.locfileid: "2814305"
---
# <a name="inventory-locations"></a>Lagerplätze für Lagerbestand

[!include [banner](../includes/banner.md)]

Lagerplätze für Lagerbestand werden mit grundlegendem Warehousing (WMS I) verwendet , um zu bestimmen, wo Artikel in einem WMS I-Lagerort gelagert und entnommen werden.

Dieses Thema gilt für Funktionen im Modul "Bestandsverwaltung". Es gilt nicht für Funktionen im Modul "Lagerverwaltung".

Der Begriff Lagerplatz bezieht sich auf den Ort, an dem Artikel gespeichert und entnommen werden.

Für jeden Lagerplatz kann auch der Ort angegeben werden, an dem der Artikel eingelagert wird. Standardmäßig handelt es sich hierbei um den gleichen Ort. Artikel werden an einem Lagerplatz in der Regel von der gleichen Seite aus eingelagert und entnommen. Es gibt jedoch auch Ausnahmen. So werden beispielsweise Artikel, die in Durchreichregalen gelagert werden, von einem Lagergang aus eingelagert und von einem anderen Gang aus entnommen. Die wichtigste Angabe ist der Lagerplatzname, der üblicherweise anhand der Koordinaten "Lagerort", "Gang", "Regal", "Regalboden" und "Lagerfach" bestimmt wird. Dieser Name bzw. diese Kennung kann manuell eingegeben oder auf der Seite "Lagerplätze für Lagerbestand" auf Basis der Lagerplatzkoordinaten generiert werden. Beispiel: "01-02-03-4" für Gang 1, Regal 2, Regalboden 3, Lagerfach 4.
Lagerplatzeigenschaften

Ein Lagerplatz hat folgende Merkmale:
-   Größe (Höhe, Breite, Tiefe und damit Volumen)
-   Lagerort, Gang, Regal, Regalboden und Lagerfach.
-   Lagerplatztyp (Sammellagerplatz, Entnahmeort, Eingangsrampe, Ausgangsrampe, Produktionseingangslagerplatz, Inspektionslagerplatz oder Kanban-Supermarkt)

In Onlinesystemen kann ein Prüftext verwendet werden, um sicherzustellen, dass der Mitarbeiter den richtigen Lagerplatz für einen bestimmten Artikel gewählt hat. Dieser Prüftext kann manuell erstellt oder standardmäßig bereitgestellt werden.

## <a name="sort-codes"></a>Sortiercodes
Sortiercodes dienen zur Optimierung der Handhabung von Entnahmepositionen. Sie enthalten detaillierte Informationen für die Entnahme von Artikeln aus dem Lager, einschließlich der Entnahmereihenfolge. Sortiercodes können nach Gang oder anderen Koordinaten angegeben oder manuell für den Lagerplatz zugewiesen werden.

## <a name="blocked-locations"></a>Blockierte Lagerplätze
Gelegentlich kann es erforderlich sein, einen Lagerplatz für einen gewissen Zeitraum zu blockieren, z. B. für Reparaturarbeiten. Es kann möglicherweise auch ausreichend sein, nur die Eingabe oder nur die Ausgabe zu blockieren.

## <a name="tree-structure"></a>Strukturdarstellung

Auf der Seite "Lagerplätze für Lagerbestand" können Sie das Lagerortlayout in einer Strukturdarstellung auf Basis der Koordinaten der Lagerplätze des Lagerbestands in einem definierten Anzeigeformat anzeigen.

## <a name="maintain-inventory-locations-via-the-warehouse-form"></a>Verwalten von Lagerplätzen über das Formular "Lagerort"

Es ist möglich, Lagerplätze von einem Lagerort an einen anderen zu kopieren und Lagerplätze mit einem Assistenten zu erstellen. Bevor Sie den Assistenten ausführen, sollten Sie sicherstellen, dass Sie die Standard-Lagerortnamen auf der Seite "Lagerort" definiert haben.



<a name="additional-resources"></a>Zusätzliche Ressourcen
--------

[Ein neues Lagerortlayout erstellen](tasks/create-new-warehouse-layout.md)
