---
title: Ressourcenfähigkeiten definieren
description: Ressourcenfunktionen beschreiben, was betriebliche Ressourcen ausführen können.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WrkCtrCapability
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 42451da0bd465ce3a18ecf18570f3331847474c1
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579111"
---
# <a name="define-resource-capabilities"></a>Ressourcenfähigkeiten definieren

[!include [banner](../../includes/banner.md)]

Ressourcenfunktionen beschreiben, was betriebliche Ressourcen ausführen können. Während der Planung werden die Anforderungen jedes Einzelvorgangs und Arbeitsgangs mit den Funktionen der verfügbaren Ressourcen abgeglichen. Dieses Aufgabenhandbuch unterstützt Sie dabei, eine Ressourcenfunktion zu erstellen und sie einer Ressource zuzuweisen. Das Demodatenunternehmen, das verwendet wird, um diese Aufgabe zu erstellen, ist USMF.


## <a name="create-a-resource-capability"></a>Erstellen einer neuen Ressourcenfunktion
1. Wechseln Sie zu Ressourcenfunktionen.
2. Klicken Sie auf Neu.
3. Geben Sie im Feld "Funktion" die Kennung der Ressourcenfunktion ein.
    * Für einen angegebenen Arbeitsgang verwenden Sie die Funktionskennung, um anzugeben, dass Ressourcen diese Funktion aufweisen müssen, um den Arbeitsgang auszuführen.  
4. Geben Sie im Feld "Beschreibung" eine Beschreibung der Funktion ein.

## <a name="assign-capability-to-a-resource"></a>Einer Ressource eine Funktion zuweisen
1. Klicken Sie auf Hinzufügen.
2. Geben Sie im Feld "Ressource" die Kennung der Ressource ein.
    * Eine Ressourcenfunktion kann einer oder mehreren Ressourcen zugewiesen werden.  
3. Geben Sie im Feld "Ablauf" ein Datum ein.
    * Sie können dieses Feld verwenden, um anzugeben, dass eine Ressource nur während einer begrenzten Zeit die Funktion hat.  
4. Geben Sie im Feld "Priorität" eine Zahl ein.
    * Wenn Sie Einzelvorgänge und Arbeitsgänge planen, können Sie angeben, ob Ressourcen nach Priorität ausgewählt werden. Wenn Sie diese Wahl treffen und mehr als eine Ressource den Einzelvorgang oder den Arbeitsgang bis zum angeforderten Datum ausführen kann, wird die Ressource ausgewählt, die die niedrigste Priorität hinsichtlich der erforderlichen Funktion hat.  
5. Geben Sie im Feld "Ebene" eine Zahl ein.
    * Wenn Sie angeben, dass ein Einzelvorgang oder ein Arbeitsgang eine bestimmte Funktion erfordert, können Sie auch die Mindestanforderung angeben, die erforderlich ist. Verwenden Sie die Funktionsebene, um Ressourcen zu unterscheiden, die den gleichen Einzelvorgang ausführen können, aber mit verschiedenen Geschwindigkeiten, Stärken, Größen, usw.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]