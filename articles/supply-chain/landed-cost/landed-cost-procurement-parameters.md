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
ms.openlocfilehash: d8aa7e6ebd254289df410814a08a5d0fe31239dd103cb428f0d4bc401fbfb28a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6747936"
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
