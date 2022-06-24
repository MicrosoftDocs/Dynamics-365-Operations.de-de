---
title: Mit Konfigurationen arbeiten
description: Dieser Artikel bietet einen Überblick über das Hauptszenario für die Arbeit mit Konfigurationen für das elektronische Berichtswesen (ER) aus dem Arbeitsbereich der Funktionen für die Globalisierung.
author: dkalyuzh
ms.date: 01/26/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 359f00336811efd5f21463a325627df0e01a5f3a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875941"
---
# <a name="work-with-configurations"></a>Mit Konfigurationen arbeiten

[!include [banner](../includes/banner.md)]

Die Konfigurationen für die elektronische Rechnungsstellung (ER) sind eine der Hauptkomponenten der Funktionen der elektronischen Rechnungsstellung. Eine ER-Konfiguration enthält die Einrichtung der Dateistruktur und eine Reihe von Transformationsregeln für die Umwandlung von Daten auf zwei Arten:

- **Konfiguration ER-Format exportieren** - Diese Konfiguration wandelt Daten aus der einheitlichen internen Struktur (ER-Modell) in das elektronische Dateiformat um.
- **Konfiguration ER-Format importieren** - Diese Konfiguration wandelt Daten aus dem elektronischen Dateiformat in die einheitliche interne Struktur (ER-Modell) um.

Neben der Erzeugung ausgehender elektronischer Dateien im vordefinierten Format werden ER-Konfigurationen häufig dazu verwendet, eingehende Nachrichten von externen Webdiensten als Antworten zu parsen. Diese Funktionalität hilft beim Aufbau einer konfigurierbaren Logik, um die Ergebnisse der Kommunikation mit externen Kanälen zu erhalten, diese Ergebnisse (Codes, Nachrichten und Protokolle) in eine für den Benutzer lesbare Struktur umzuwandeln und diese Informationen dann an die Client-Anwendung weiterzugeben.

Um ER-Konfigurationen in Ihrer Funktion für die Elektronische Rechnungsstellung verwenden zu können, müssen Sie sie mit der Funktion verknüpfen und auf der Registerkarte **Konfigurationen** für die aktuelle Version der Funktion verfügbar machen. Sie können mit einer verknüpften ER-Konfiguration arbeiten, indem Sie **Hinzufügen**, **Löschen**, **Bearbeiten** oder **Ansehen** wählen.

Bevor Sie einen Link zu einer ER-Konfiguration hinzufügen können, muss die Konfiguration in Ihrem Regulatory Configuration Service (RCS) Repository vorhanden sein. Um die ER-Konfigurationen zu überprüfen, die in Ihrem RCS-Repository verfügbar sind, folgen Sie diesen Schritten.

1. Melden Sie sich bei Ihrem RCS-Konto an.
2. Im Arbeitsbereich **Elektronische Berichterstellung** im Abschnitt **Konfigurationen** wählen Sie die Kachel **Berichterstellungskonfigurationen** aus.

Wie Sie eine neue ER-Konfiguration erstellen oder eine bestehende ER-Konfiguration aus dem Global Repository importieren, erfahren Sie unter [Elektronische Berichterstattung](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).

Um eine verknüpfte ER-Konfiguration anzupassen, wählen Sie **Bearbeiten** auf der Registerkarte **Konfigurationen** für die aktuelle Funktion der Elektronischen Rechnungsstellung. Das System erstellt automatisch eine Version der ER-Konfiguration. Wenn die aktuelle Version nicht von dem aktiven Konfigurationsanbieter erstellt wurde, erstellt das System eine abgeleitete Version, die Ihren Konfigurationsanbieter verwendet. Wenn die aktuelle Version von dem aktiven Konfigurationsanbieter erstellt wurde, erstellt das System eine neue Version. In beiden Fällen können Sie die erstellte Version ändern und dann automatisch alle erforderlichen Aktualisierungen vornehmen.
