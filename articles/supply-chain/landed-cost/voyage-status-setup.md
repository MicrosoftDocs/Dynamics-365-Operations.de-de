---
title: Fahrt-Status einrichten
description: Dieser Artikel beschreibt, wie Sie die Statuswerte einrichten, die Benutzer Fahrten zuweisen können.
author: Weijiesa
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMStatusTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 1cec728f2fa49175c063818ee7f188b441945647
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907318"
---
# <a name="voyage-status-setup"></a>Einrichten des Status einer Fahrt

[!include [banner](../../includes/banner.md)]

Auf der Seite **Fahrtstatus** legen Sie die Statuswerte fest, die Benutzer den Fahrten zuweisen können. Benutzer können allen Ebenen einer Fahrt Statuswerte zuweisen: Fahrt, Transportcontainer, Palette, Einkaufsbestellung und Artikel (Einkaufs- und Umlagerungsauftragszeilen). Sie werden für zwei Zwecke verwendet:

- Den Benutzer über den Status der Fahrt, des Transportcontainers, der Palette, der Einkaufsbestellung oder des Artikels zu informieren (Einkaufs- und Umlagerungsauftragszeilen).
- Begrenzen Sie die Verwendung des Kalkulationsbereichs, indem Sie Änderungen oder Löschungen verhindern.

Um die Status Ihrer Fahrten festzulegen, gehen Sie zu **Gesamttransportkosten \> Einrichten \> Fahrten-Status**. Dort können Sie mit Hilfe der Schaltflächen im Aktivitätsbereich Status hinzufügen, entfernen und bearbeiten.

Jeder Kalkulationsbereich hat seinen eigenen Satz und seine eigene Hierarchie von Fahrt-Status. Daher müssen Sie auf der Seite **Fahrtstatus** im Feld **Kalkulationsbereich** zunächst den Kostenbereich auswählen, für den Sie Fahrtstatus anzeigen oder erstellen möchten. Legen Sie dann für jeden Fahrtstatus die Felder fest, die in der folgenden Tabelle beschrieben sind, je nach Bedarf. Beachten Sie, dass der Status einer Fahrt auch automatisch durch Systemereignisse geändert werden kann, z.B. durch Regeln, die mit Hilfe des Tracking-Control-Centers festgelegt wurden.

| Feld | Beschreibung |
|---|---|
| Seereisestatus | Geben Sie den Namen des Status der Fahrt ein. |
| Beschreibung | Geben Sie eine Beschreibung für den Status der Fahrt ein. |
| Änderung | Aktivieren Sie dieses Kontrollkästchen, wenn Benutzer Fahrten, die diesen Status haben, ändern dürfen. |
| Löschen | Aktivieren Sie dieses Kontrollkästchen, wenn Benutzer Fahrten, die diesen Status haben, löschen dürfen. |
| Obligatorisch | Aktivieren Sie dieses Kontrollkästchen, um den Status der Fahrt obligatorisch zu machen, so dass er nicht übersprungen werden kann. |
| Übergeordnet | Verwenden Sie dieses Feld, um eine Hierarchie zwischen den Statuswerten zu erstellen. Fahrt-Statuswerte können (entweder manuell oder automatisch) nur abwärts in der Hierarchie geändert werden, von einem übergeordneten Status zu einem seiner untergeordneten Statuswerte.

> [!NOTE]
> Sie müssen nur die spezifischen Fahrt-Status festlegen, die Ihre Organisation verwendet. Typische Fahrtstatus sind *Bestätigt*, *Waren in Zustellung*, *Eingegangen*, *Bereit zur Kalkulation* und *Kalkuliert*. Es können aber auch andere Zustände vorhanden sein.
