---
title: Globale Parameter für mobile Geräte
description: Dieses Thema erklärt, wie Sie die Einstellungen für mobile Geräte auf der Seite „Lagerverwaltungsparameter“ einrichten.
author: HuberIvan
ms.date: 08/13/2021
ms.topic: article
ms.search.form: WHS
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-huberivan
ms.search.validFrom: 2021-08-13
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 03c10232d55c99c73e625170797f89f6c77e812b
ms.sourcegitcommit: 99bde425ade701ef244c6bca6d411aef94a59b3c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/20/2021
ms.locfileid: "7505570"
---
# <a name="global-mobile-device-parameters"></a>Globale Parameter für mobile Geräte

[!include [banner](../includes/banner.md)]

Dieses Thema erklärt, wie Sie globale Lagerverwaltungsparameter einrichten, die sich darauf auswirken, wie das System mit mobilen Geräten interagiert.

Weitere Informationen zum Einrichten von Lagerortarbeitskräften erhalten Sie in [Lagerortarbeitskräfte verwalten](manage-warehouse-workers.md). Weitere Informationen zur Kennzeichenbehandlung auf mobilen Geräten finden Sie unter [Kennzeichenempfang über die Warehouse Management Mobile App](warehousing-mobile-device-app-license-plate-receiving.md). Weitere Informationen zu den Zykluszählungsprozessen finden Sie unter [Zykluszählung](cycle-counting.md) und [Beispielszenarien für Zykluszählungen](cycle-counting-scenarios.md).

## <a name="open-the-warehouse-management-parameters-page"></a>Die Seite „Lagerortverwaltungsparameter“ öffnen

Um die Seite **Lagerortverwaltungsparameter** zu öffnen, navigieren Sie zu **Lagerortverwaltung \> Setup \> Lagerortverwaltungsparameter**. Anschließend können Sie die Felder festlegen, die sich auf die Arbeit mit mobilen Geräten beziehen, wie im nächsten Abschnitt dieses Themas beschrieben.

## <a name="mobile-device-fasttab-on-the-general-tab"></a>Inforegister „Mobile Geräte“ auf der Registerkarte „Allgemein“

Die globalen Einstellungen für mobile Geräte finden Sie auf dem Inforegister **Mobiles Gerät** auf der Registerkarte **Allgemein** der Seite **Lagerortverwaltungsparameter**. Die folgenden Felder sind verfügbar.

| Feld | Beschreibung |
|---|---|
| Hinweistyp des mobilen Geräts | Wählen Sie den Informationstyp aus, der einer Arbeitskraft während der Auftragskommissionierung angezeigt wird. |
| Grenzwert für die gescannte Menge | Geben Sie die maximale Artikelmenge ein, die eine Arbeitskraft während jeder Sitzung scannen kann, indem Sie ein Menüelement eines mobilen Geräts verwenden, das über den Wert **Arbeitserstellungsprozess** von *Anpassung in* verfügt. Dieses Feld wirkt sich nicht auf Scans aus, die mit einem anderen Menüelementtyp durchgeführt werden. |
| Sitzungsprotokollierung des mobilen Geräts verwenden | Legen Sie diese Option auf *Ja* fest, um ein Protokoll des Anmeldeverlaufs einer Arbeitskraft aufzubewahren. Um das Protokoll anzuzeigen, navigieren Sie zu **Arbeitsbenutzersitzungen \> Anfragen und Berichte \> Protokolle von mobilen Geräten \> Arbeitsbenutzersitzungen**. |
| Anzahl der gespeicherten Fehler | Geben Sie die maximale Anzahl von Fehlersätzen ein, die das System speichern soll. Um das Fehlerprotokoll anzuzeigen, navigieren Sie zu **Arbeitsbenutzersitzungen \> Anfragen und Berichte \> Protokolle von mobilen Geräten \> Arbeitsbenutzersitzungen**. |
| Umlagerungserfassung Standardlagerort | Wählen Sie die Erfassung aus, die verwendet wird, wenn Mitarbeiter ein mobiles Gerät verwenden, um Produkte von einem Lager in ein anderes zu transportieren. |
| Bestellpositionsregistrierung bei externer Prüfung zulassen | Legen Sie diese Option auf *Ja* fest, wenn Mitarbeiter mobile Geräte verwenden können, um Bestellpositionen für Bestellungen zu registrieren, die über den Wert **Genehmigungsstatus** von *In externer Überprüfung* verfügen. Legen Sie diese Option auf *Nein* fest, um zu verhindern, dass Mitarbeiter Zeilen für Bestellungen registrieren können, die sich in externer Überprüfung befinden. |
| RSAT-Unterstützung aktivieren | Das Feld aktiviert die Aufgabenvalidierung der mobilen Warehouse Management-App, die jeden von der App ausgeführten Schritt protokolliert und validiert. Da dieser Vorgang die Systemleistung erheblich verlangsamen kann, sollten Sie die Validierung nur während des Tests aktivieren. Sie sollten sie niemals in einer Produktionsumgebung aktivieren. |
