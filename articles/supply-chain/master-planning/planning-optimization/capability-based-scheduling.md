---
title: Planung mit Ressourcenauswahl basierend auf Fähigkeiten
description: In diesem Artikel wird die Ressourcenauswahl während der Planung mit unbegrenzter Kapazität beschrieben, wenn Sie Fähigkeiten als Ressourcenanforderungen für einen Vorgang angeben.
author: t-benebo
ms.date: 08/09/2022
ms.topic: article
ms.search.form: RouteInventProd, WrkCtrTable, WrkCtrCapability
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-09-03
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 176f40ad8cd1aa1831bbe50c0ebd91ec0cc3bc89
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2022
ms.locfileid: "9739897"
---
# <a name="scheduling-with-resource-selection-based-on-capability"></a>Planung mit Ressourcenauswahl basierend auf Fähigkeiten

[!include [banner](../../includes/banner.md)]

Indem Sie die Ressourcenanforderungen für einen Vorgang eines Produktionsarbeitsplans angeben, definieren Sie, was für die Ausführung dieses Vorgangs erforderlich ist. Ein Vorgang kann beispielsweise eine bestimmte Ressource oder eine Ressourcengruppe oder eine Kombination von Fähigkeiten erfordern. In diesem Artikel wird die Ressourcenauswahl während der Planung mit unbegrenzter Kapazität beschrieben, wenn Sie Fähigkeiten als Ressourcenanforderungen für einen Vorgang angeben.

## <a name="turn-the-capability-based-scheduling-feature-on-or-off"></a>Die fähigkeitsbasierte Planungsfunktion aktivieren und deaktivieren

Um diese Funktion nutzen zu können, muss sie für Ihr System aktiviert werden. Ab Supply Chain Management Version 10.0.29 ist die Funktion standardmäßig aktiviert. Administratoren können diese Funktionalität an- oder ausschalten, indem Sie nach der Funktion zur *Endloskapazitätsplanung zur Planungsoptimierung* im Arbeitsbereich [Funktionsverwaltung](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) suchen.

Weitere Informationen zu dieser Funktion finden Sie unter [Zeitplanung mit unbegrenzter Kapazität](infinite-capacity-planning.md).

## <a name="capability-based-scheduling"></a>Fähigkeitsbasierte Planung

Eine Fähigkeit gibt einer betrieblichen Ressource die Möglichkeit, eine bestimmte Aktivität auszuführen. Mehr als eine Fähigkeit kann einer einzelnen betrieblichen Ressource zugewiesen werden, und eine einzelne Fähigkeit kann mehr als einer Ressource zugewiesen erden. Funktionen können allen Typen von Ressourcen, wie Werkzeug, Anbieter, Maschine, Lagerplatz, Einrichtungen und Personalverwaltung, zugewiesen werden.

Wenn Sie Fähigkeiten als Ressourcenanforderungen angeben, können Sie die Ressourcenzuordnung aufschieben, bis Aufträge geplant sind. Anstatt einem Routenvorgang bestimmte Ressourcen oder Ressourcengruppen zuzuweisen, können Sie die Funktionen definieren, die für jeden Routenvorgang erforderlich sind. Dann gleicht das System während der Planung die erforderlichen Fähigkeiten mit den Fähigkeiten ab, die für die Ressourcen definiert sind. Das System wählt nur Ressourcen aus, die die Anforderungen erfüllen.

Um einer Betriebsressource Fähigkeiten zuzuweisen, verwenden Sie das Inforegister **Fähigkeiten** auf der Seite **Ressourcen**. Um einer Ressource Fähigkeiten zuzuweisen, verwenden Sie das Inforegister **Ressourcen** auf der Seite **Ressourcenfähigkeiten**. Beide Seiten können unter **Produktionskontrolle \> Einstellungen \> Ressourcen** im Navigationsbereich aufgerufen werden. Beide Inforegister enthalten ein Raster, das die Ressourcen auflistet, die einer ausgewählten Ressource oder Funktion zugeordnet sind. Beide Inforegister enthalten auch eine Symbolleiste, mit der Sie Zeilen im Raster hinzufügen, entfernen und bearbeiten können. Das Raster enthält die folgenden Spalten:

- **Ressource** oder **Fähigkeit** – Wählen Sie die Ressource oder Fähigkeit aus, die von der Zeile zugewiesen wird.
- **Beschreibung** – Geben Sie eine kurze Beschreibung der Ressource oder der Fähigkeit ein.
- **Wirksam** – Geben Sie das erste Datum an, an dem die Ressourcen- oder Fähigkeitszuordnung wirksam wird. Während der Planung verwendet das System keine Ressource oder Fähigkeit mit einer abgelaufenen Fähigkeitszuweisung, selbst wenn diese Ressource ansonsten die Anforderungen erfüllt.
- **Ablauf** – Geben Sie das letzte Datum an, an dem die Ressourcen- oder Fähigkeitszuordnung gültig ist. Während der Planung verwendet das System keine Ressource oder Fähigkeit mit einer abgelaufenen Fähigkeitszuweisung, selbst wenn diese Ressource ansonsten die Anforderungen erfüllt.
- **Niveau** – Geben Sie den Kenntnisstand an, den die Ressource für die Fähigkeit haben muss. Wenn Sie dann den Wert **Mindestanforderung** für die Ressourcen- oder Fähigkeitenanforderung angeben, berücksichtigt das Planungsmodel den Kenntnisstand bei der Ressourcenauswahl. Das System wählt nur Ressourcen aus, die die erforderliche Fähigkeit auf einer Ebene haben, die der Ebene entsprechen oder die minimale Ebene überschreitet, die für die Ressourcenanforderung angegeben ist.
- **Priorität** – Dieses Feld wird von der Planungsoptimierung noch nicht unterstützt. Wenn Sie jedoch das veraltete Masterplanungsmodul verwenden, können Sie das Feld **Priorität** in der Ressourcen- oder Fähigkeitszuweisung nutzen, um die Ressourcenpriorität zu definieren. Wenn *Priorität* dann im Feld **Primäre Ressourcen-Auswahl** auf der Seite **Planungsparameter** aktiviert ist, wählt das System zunächst die Ressource aus, die die höchste Priorität (d. h. der niedrigste numerischen Wert im Feld **Priorität**) bei der Planung hat.

## <a name="example"></a>Beispiel

Dieses Beispiel zeigt, wie das Planungsmodul Ressourcen basierend auf der Fähigkeit auswählt.

Eine Produktionsroute hat fünf Vorgänge: *10*, *20*, *30*, *40* und *50*. Jeder Routenvorgang erfordert eine Ressource mit unterschiedlichen Fähigkeiten. Beispielsweise erfordert der Routenbetrieb *10* eine Ressource, die einen Lautsprecher zusammenbauen kann (*0050 Lautsprecher-Baugruppe*) und Holz bearbeiten kann (*1010 Fähigkeiten zur Holzbearbeitung*). Routenvorgang *50* erfordert eine Ressource, die ein Produkt packen kann (*0070 Packfähigkeit*).

![Die zur Planung verwendete Fähigkeit](media/capability-based-scheduling.png "Die zur Planung verwendete Fähigkeit")

Während der Planung sucht das Modul nach Ressourcen, die die betrieblichen Anforderungen erfüllen. Das Planungsmodul wählt beispielsweise die Ressource *00101* aus, um den Vorgang *10* durchzuführen, da diese Ressource die erste gefundene Ressource ist, die über beide erforderlichen Fähigkeiten verfügt. Das Planungsmodul wählt die Ressource *00301* aus, um den Vorgang *50* durchzuführen, da diese Ressource die einzige Ressource ist, die über Packfähigkeiten verfügt.

Betrachten Sie als Nächstes, wie sich dieses Beispiel auswirkt, wenn Kenntnisstufen verwendet werden:

- Vorgang *10* erfordert einen Mindestkenntnisstand von *7* für die Fähigkeit *0059 Montage*.
- Ressource *00101* besitzt ein Leistungsniveau von *5* für die Fähigkeit *0059 Montage*.
- Ressource *00102* besitzt ein Leistungsniveau von *10* für die Fähigkeit *0059 Montage*.

In diesem Fall wählt das Planungsmodul während der Planung mit unbegrenzter Kapazität die Ressource *00102* aus, um den Vorgang *10* durchzuführen, da diese Ressource im Gegensatz zur Ressource *00101* das erforderliche Kompetenzniveau für die Fähigkeit besitzt.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
