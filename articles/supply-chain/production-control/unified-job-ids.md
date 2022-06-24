---
title: Vereinheitlichte Nummernkreise für Einzelvorgangskennungen
description: Diese Funktion bietet einen einzelnen, einheitliche Nummernkreis, die Auftrags-IDs für die Module Produktionssteuerung, Fertigungssteuerung sowie Zeit und Anwesenheit generieren.
author: johanhoffmann
ms.date: 03/25/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 301a4bb58f896a2dc0f0cddcd2e29344865ca898
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897544"
---
# <a name="unified-number-sequence-for-job-ids"></a>Vereinheitlichte Nummernkreise für Einzelvorgangskennungen

[!include [banner](../includes/banner.md)]

Diese Funktion bietet einen einzelnen, einheitliche Nummernkreis, die Auftrags-IDs für die Module Produktionssteuerung, Fertigungssteuerung sowie Zeit und Anwesenheit generieren. Bisher konnten Sie für jedes dieser Module einen anderen Nummernkreis auswählen, was zu widersprüchlichen Auftrags-IDs führen kann, wenn zwei oder mehr dieser Kreise ein identisches Format verwenden. Ein solcher Konflikt kann zu Datenkorruption führen.

## <a name="turn-on-this-feature-for-your-system"></a>Schalten Sie diese Funktion für Ihr System ein

Wenn Ihr System nicht bereits die in diesem Artikel beschriebene Funktion enthält, gehen Sie zu [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) und schalten Sie die Funktion *Einheitliche Nummernkreise für Auftrags-IDs* ein.

## <a name="set-up-the-unified-number-sequence-for-job-ids"></a>Einheitliche Nummernkreise für Auftrags-IDs einrichten

Nach dem Aktivieren dieser Funktion sind die vorhandenen Einstellungen für die **Auftragskennung** und Nummernkreise auf den Parameterseiten für die Module Produktionssteuerung, Fertigungssteuer sowie Zeit und Anwesenheit veraltet und ein neues Feld **Einheitliche Auftrags-ID** wird hinzugefügt. Der Wert **Einheitliche Auftrags-ID** wird von allen drei Modulen geteilt, wodurch sichergestellt wird, dass alle Module auf denselben Nummernkreis verweisen. Auftrags-IDs sind daher in allen drei Modulen eindeutig und es kommt nie zu Konflikten.

Um einheitliche Nummernkreise für Auftrags-IDs einzurichten, gehen Sie wie folgt vor:

1. Aktivieren Sie die Funktion wie im vorherigen Abschnitt beschrieben.
1. Identifizieren Sie entweder den Nummernkreis, den Sie für Ihre einheitlichen Auftrags-IDs verwenden möchten, oder erstellen Sie einen neuen. Weitere Informationen finden Sie unter [Übersicht über Nummernkreise](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md).
1. Gehen Sie zur Seite **Produktionssteuerungsparameter**, **Fertigungssteuerungsparameter** oder **Zeit- und Anwesenheitsparameter**. Es spielt keine Rolle, wofür Sie sich entscheiden, denn wenn Sie diese Einstellung auf einer dieser Seiten vornehmen, werden alle anderen Seiten automatisch aktualisiert.
1. Öffnen Sie die Registerkarte **Nummernkreise** auf der Seite mit den ausgewählten Parametern.
1. Weisen Sie den **Nummernkreiscode**, den Sie zuvor für die Zeile **Einheitliche Auftrags-IDs** des Rasters festgelegt haben.
