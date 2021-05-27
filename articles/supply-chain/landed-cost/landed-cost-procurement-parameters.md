---
title: Beschaffungs- und Bezugsquellenparameter für Gesamttransportkosten
description: Dieses Thema beschreibt, wie Sie die relevanten Beschaffungs- und Bezugsquellenparameter festlegen, wenn Sie das Modul Gesamttransportkosten verwenden.
author: sherry-zheng
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SrmParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: ccda3bd769a646e2390711883b8e40bec50e4d6a
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020982"
---
# <a name="procurement-and-sourcing-parameters-for-landed-cost"></a>Beschaffungs- und Bezugsquellenparameter für Gesamttransportkosten

[!include [banner](../../includes/banner.md)]

Die Seite **Beschaffungs- und Bezugsquellenparameter** enthält einige Einstellungen, die besonders relevant sind, wenn Sie das Modul **Gesamttransportkosten** verwenden. Verwenden Sie das Dialogfeld **Bestellzeilen aktualisieren**, das von der Seite **Beschaffungs- und Bezugsquellenparameter** geöffnet wird, um festzulegen, ob die Zeilen der Einkaufsbestellung automatisch aktualisiert werden sollen, wenn Änderungen am Kopf der Bestellung vorgenommen werden.

Gehen Sie wie folgt vor, um diese Einrichtung abzuschließen.

1. Gehen Sie zu **Beschaffung und Ursproung\> Einstellungen \> Beschaffungs- und Ursprungsparameter**.
1. Wählen Sie auf der Registerkarte **Allgemein** den Link **Bestellzeilen aktualisieren**.
1. Das Dialogfeld **Bestellzeilen aktualisieren** listet die Felder im Bestellkopf auf, die auch automatische Aktualisierungen auf Bezugsfelder in den Bestellzeilen anwenden können. Legen Sie jedes Feld in der Liste auf einen der folgenden Werte fest:

    - **Immer** - Die Auftragszeilen sollen automatisch aktualisiert werden, wenn der Auftragskopf aktualisiert wird.
    - **Nie** - Die Auftragszeilen sollen nie aktualisiert werden, wenn der Auftragskopf aktualisiert wird.
    - **Aufforderung** - Der Benutzer wird aufgefordert, auszuwählen, ob die Auftragszeilen aktualisiert werden sollen.
