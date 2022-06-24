---
title: Einstellungen für Lieferinformationen
description: Dieser Artikel beschreibt, wie Sie Lieferinformationen für das Modul Gesamttransportkosten festlegen.
author: Weijiesa
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMPortTable, ITMLeadTimeTable, ITMLegTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 5bf9c700ecd327ab3b3948f38dc60e24efbda94c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895611"
---
# <a name="delivery-information-setup"></a>Einstellungen für Lieferinformationen

[!include [banner](../../includes/banner.md)]

Dieser Artikel beschreibt, wie Sie Lieferinformationen für das Modul **Gesamttransportkosten** festlegen.

## <a name="shipping-ports"></a>Versandports

Lieferhäfen identifizieren, von wo und wohin Waren verschifft werden. Für jede Fahrt werden ein „An Hafen“ und ein „Von Hafen“ definiert, basierend auf der Route, die für das Schiff ausgewählt wurde. Lieferhäfen werden verwendet, um die Abschnitte einer Route und auch die Aktivitäten der Fahrt zu bilden. Sie werden normalerweise durch den Namen der Stadt und des Landes oder der Region definiert, in der sich der physische Lagerplatz des Hafens befindet.

Um mit Lieferhäfen zu arbeiten, gehen Sie zu **Gesamttransportkosten \> Lieferinformationen einrichten \> Lieferhäfen**. Dort können Sie Datensätze für Ihre Lieferhäfen anzeigen, hinzufügen und entfernen. Die folgende Tabelle beschreibt die Felder, die für jeden Datensatz verfügbar sind.

| Feld | Beschreibung |
|---|---|
| Versandport | Geben Sie einen eindeutigen Identifikationsnamen/Nummer für den Lieferhafen ein. |
| Beschreibung | Geben Sie eine Beschreibung für den Lieferhafen ein. |

## <a name="tracking-control-center"></a><a name="tracking-control-center"></a>Steuerungscenter für Nachverfolgung

Sie verwenden das Tracking-Control-Center, um die Vorlaufzeiten, Statusaktualisierungen und Flows von Informationen festzulegen, die mit einer Fahrt verbunden sind, während sich die Transportcontainer von einem Abschnitt zum nächsten bewegen. Wenn Sie einen Tracking-Kontrolldatensatz erstellen, wird er mit einem bestimmten Abschnitt einer Route für eine Fahrt verknüpft. Wenn eine Fahrt einen Abschnitt aktualisiert, wird der zugehörige Datensatz aktualisiert und wie definiert ausgefüllt. Sie können Tracking-Informationen für einzelne Fahrten auf der Seite **Alle Fahrten** aktualisieren.

Um das Tracking-Control-Center zu öffnen, gehen Sie auf **Gesamttransportkosten \> Lieferinformationen einrichten \> Tracking-Control-Center**.

Das Tracking-Control-Center zeigt eine von drei Seitenansichten an, abhängig von dem Wert, der im Feld **Typ erstellen** im Listenbereich ausgewählt ist: *Leer*, *Vorlaufzeit*, oder *Statusaktualisierung*. Jeder Erstell-Typ aktualisiert eine andere festgelegte Information, die mit dem Verlauf einer Fahrt vom Ausgangspunkt bis zum endgültigen Ziel verbunden ist.

### <a name="common-rule-settings"></a>Allgemeine Regeleinstellungen

Die folgende Tabelle zeigt die Felder, die für alle drei Erstellungsarten im Tracking-Control-Center verfügbar sind.

| Feld | Beschreibung |
|---|---|
| Quelltabelle, Quellfeld | Diese Felder identifizieren eine Quelltabelle und ein Quellfeld in der Datenbank. Die Regel lädt den Wert in das Feld und verwendet ihn dann auf die Weise, die durch andere Einstellungen der Regel festgelegt ist. |
| Zieltabelle, Zielfeld | Diese Felder identifizieren eine Zieltabelle und ein Zielfeld in der Datenbank. Die Regel lädt den Wert in das Feld und verwendet (oder überschreibt) ihn dann auf die Weise, die durch andere Einstellungen der Regel festgelegt ist. |
| Aktivität | Dieses Feld identifiziert die Art der Aktivität, die auf einen Transportcontainer angewendet werden soll, auf den eine Regel zutrifft. |
| Passende Kriterien | Dieses Feld bestimmt, wie das System eine Übereinstimmung für eine Regel identifiziert. In jedem Fall überprüft das System die Daten in den Quell- und Zieltabellen, um zu bestimmen, ob und wann ein Feld in der Zieltabelle aktualisiert werden soll.<p>Zum Beispiel ist die Quelltabelle *Fahrtn* und die Zieltabelle ist *Kauf Kopfzeile* oder *Kauf Zeilen*. Die Tabelle *Fahrten* hat einen **Von Hafen**-Wert von *Hongkong*, und die Tabelle *Kauf Kopfzeile* hat einen **Von Hafen**-Wert von *Shanghai*. Dann wird eine Regel erstellt, die *Hongkong* als Von Hafen hat. In diesem Fall funktionieren die Werte des Feldes **Übereinstimmende Kriterien** folgendermaßen:</p><ul><li>**Beide** - Das Zielfeld wird nicht aktualisiert, weil einer der beiden Häfen nicht übereinstimmt.</li><li>**Quelle** - Das Zielfeld wird aktualisiert, weil der „Von“-Hafen der Quelltabelle *Hongkong* ist.</li><li>**Ziel** - Das Zielfeld wird nicht aktualisiert, weil der „Von“-Hafen der Zieltabelle *Shanghai* ist (nicht *Hongkong*).</li></ul> |
| Aktivität kopieren | Die verfügbaren Werte sind *Kopieren* und *Standard*. Wählen Sie *Kopieren*, um den Wert im Quellfeld in das Zielfeld zu kopieren. Wählen Sie *Vorgabe*, um einen statischen Wert für das Zielfeld festzulegen. |
| Standard | Wenn das Feld **Kopieraktion** auf *Standard* festgelegt ist, definiert das Feld **Standard** den Standardwert für das Zielfeld. Wenn sich die Aktion beispielsweise auf eine Hafenaktualisierung bezieht und das Feld **Aktion kopieren** auf *Vorgabe* festgelegt ist, identifiziert das Feld **Vorgabe** einen Hafen. |
| Teilstrecke | Dieses Feld identifiziert den Abschnitt der Route, für den die angegebene Aktion stattfindet, z. B. Ladung oder Zoll. |
| Dienstanbieter | Wenn für den aktuellen Status-Update/Abschnitt der Route ein bestimmter Dienstleister verwendet wird, identifiziert dieses Feld den Dienstleister. Dienstleister werden im Lieferantenkonto definiert. |

### <a name="lead-time-rules"></a>Regeln für die Vorlaufzeit

Die Vorlaufzeit ist die geschätzte Zeit, die eine Fahrt benötigt, um einen definierten Abschnitt einer Route zu beenden. Die Vorlaufzeit eines jeden Abschnitts einer Route wird verwendet, um das geschätzte Lieferdatum der Fahrt zu berechnen. Dieses Datum wird dann in das Feld **Bestätigtes Lieferdatum** auf jeder Kauf-Zeile der Fahrt eingetragen.

Sie verwenden Vorlaufzeit-Regeln, um Aktualisierungen von Terminen zu verwalten. Die Aktivitäten werden automatisch generiert, wenn eine Fahrtenvorlage für eine Fahrt verwendet wird.

Um eine Vorlaufzeit-Regel zum Tracking-Control-Center hinzuzufügen, gehen Sie wie folgt vor.

1. Führen Sie einen dieser Schritte aus:

    - Gehen Sie zu **Gesamttransportkosten \> Route mit mehreren Abschnitten einrichten \> Abschnitte**. Wählen Sie den Abschnitt aus, für den Sie Vorlaufzeiten festlegen möchten, und wählen Sie dann im Aktivitätsbereich **Tracking-Control-Center**. Das Tracking-Control-Center wird mit Informationen über den ausgewählten Abschnitt vorgeladen.
    - Gehen Sie zu **Gesamttransportkosten \> Lieferinformationen einrichten \> Tracking-Control-Center**. Sie müssen dann in Schritt 4 dieses Vorgangs einen Abschnitt manuell auswählen.

1. Legen Sie im Listenbereich das Feld **Erstellungsart** auf *Vorlaufzeit* fest.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Wenn Sie in Schritt 1 vom Tracking-Control-Center ausgegangen sind, legen Sie das Feld **Bein** auf den Abschnitt fest, für den Sie eine Vorlaufzeit-Regel erstellen möchten. Wenn Sie von der Seite **Beine** aus gestartet sind, ist das Feld **Bein** auf den Abschnitt voreingestellt, den Sie ausgewählt haben, bevor Sie das Tracking-Control-Center geöffnet haben.

    Basierend auf dem Wert des Feldes **Bein** werden mehrere Felder automatisch festgelegt, wie hier gezeigt:

    - **Quellentabelle:** *Behälteraktivitäten*
    - **Quellfeld:** *Startdatum*
    - **Ziel-Tabelle:** *Container-Aktivitäten*
    - **Zielfeld:** *Geschätztes Enddatum*

1. Wählen Sie im Feld **Aktivität** die Aktivität aus, für die die aktuelle Regel gelten soll.
1. Geben Sie in das Feld **Vorlaufzeit** die Vorlaufzeit (in Tagen) ein, die gelten soll, wenn die aktuelle Regel ausgelöst wird.

### <a name="status-update-rules"></a>Regeln zur Statusaktualisierung

Datensätze, bei denen das Feld **Erstellungstyp** auf *Statusaktualisierung* festgelegt ist, aktualisieren den Status von Zeilen der Einkaufsbestellung oder den Status auf der Ebene von Fahrt, Transportcontainer oder Palette. Die Stati können unabhängig voneinander festgelegt werden. Verwenden Sie sie, um den Benutzer oder die Abteilung über den Stand einer Fahrt zu informieren (z.B. empfangene Dokumente oder Waren in Zustellung).

Wenn das Feld **Erstellungstyp** auf *Statusaktualisierung* festgelegt ist, enthält das Tracking-Control-Center ein **Zeilen** Inforegister, in dem Sie einen Kalkulationsbereich und den aktualisierten Status der Fahrt definieren können. Sie haben z.B. eine Zeile, in der das Feld **Kostenbereich** auf *Container* festgelegt ist und das Feld **Fahrtstatus** auf *Waren in Zustellung* festgelegt ist. In diesem Fall wird, wenn ein Auftrag den angegebenen Abschnitt beendet, das Feld **Fahrtstatus** des Transportcontainers auf *Waren in Zustellung* aktualisiert.

Die Statusaktualisierungen liefern den Status einer Fahrt über die Zeilen der Fahrt und der Einkaufsbestellung, die mit dieser Fahrt verbunden sind. Während eine Fahrt ihre Route vom Hafen, An Hafen und Zoll bis zum Lagerort am Zielort durchläuft, bietet das Feld **Fahrtstatus** des Fahrtdatensatzes einen schnellen Überblick über das Stadium, in dem sich die Artikel befinden.

Um dem Tracking-Control-Center eine Statusaktualisierungsregel hinzuzufügen, gehen Sie wie folgt vor.

1. Führen Sie einen dieser Schritte aus:

    - Gehen Sie zu **Gesamttransportkosten \> Route mit mehreren Abschnitten einrichten \> Abschnitte**. Wählen Sie den Abschnitt, für den Sie eine Statusaktualisierung festlegen möchten, und wählen Sie dann im Aktivitätsbereich **Tracking-Control-Center**. Das Tracking-Control-Center wird mit Informationen über den ausgewählten Abschnitt vorgeladen.
    - Gehen Sie zu **Gesamttransportkosten \> Lieferinformationen einrichten \> Tracking-Control-Center**. Sie müssen dann in Schritt 4 dieses Vorgangs einen Abschnitt manuell auswählen.

1. Legen Sie im Listenbereich das Feld **Erstellungstyp** auf *Statusaktualisierung* fest.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Wenn Sie in Schritt 1 vom Tracking-Control-Center ausgegangen sind, legen Sie das Feld **Abschnitt** auf den Abschnitt fest, für den Sie eine Statusaktualisierungsregel erstellen möchten. Wenn Sie von der Seite **Beine** aus gestartet sind, ist das Feld **Bein** auf den Abschnitt voreingestellt, den Sie ausgewählt haben, bevor Sie das Tracking-Control-Center geöffnet haben.

    Basierend auf dem Wert des Feldes **Bein** werden mehrere Felder automatisch festgelegt, wie hier gezeigt:

    - **Quellentabelle:** *Behälteraktivitäten*
    - **Quellfeld:** *Aktuelles Enddatum*
    - **Zieltabelle:** Dieses Feld wird leer gelassen.
    - **Zielfeld:** Dieses Feld wird leer gelassen.

1. Wählen Sie im Feld **Aktivität** die Aktivität aus, für die Ihre Regel gelten soll.
1. Geben Sie im Inforegister **Zeilen** die Statusaktualisierungen für jeden Kalkulationsbereich ein.

### <a name="blank-type-rules"></a>Regeln vom Typ Leerzeichen

Sie verwenden Datensätze, die einen **Erstellungstyp** Wert von *Leerzeichen* haben, um einen Feldwert zu überschreiben oder einzugeben, basierend auf den Daten eines anderen Feldes. Ein Feld aus Gesamttransportkosten überschreibt Daten in anderen Bereichen von Microsoft Dynamics 365 Supply Chain Management, basierend auf Regeln, die im Tracking-Control-Center festgelegt sind.

1. Gehen Sie zu **Gesamttransportkosten \> Lieferinformationen einrichten \> Tracking-Control-Center**.
1. Legen Sie im Listenbereich das Feld **Erstellungstyp** auf *Leerzeichen* fest.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Definieren Sie die Quell- und Zielwerte, die Abgleichskriterien, die Kopieraktion und andere relevante Parameter, wie für Ihre Regel erforderlich.

### <a name="required-tracking-control-setup"></a>Erforderliches Einrichten der Tracking-Steuerung

Für jede Route-Vorlage müssen im Tracking-Control-Center zwei Datensätze festgelegt werden. Diese beiden Datensätze haben einen **Erstellungstyp** Wert von *Leerzeichen* und werden in allen Implementierungen der Gesamttransportkosten verwendet. Sie tragen dazu bei, dass das bestätigte Datum des Kaufs und die erwarteten Daten der Waren in Zustellung für Fahrten und die zugehörigen Zeilen der Einkaufsbestellung auf die erwartete Weise aktualisiert werden.

Der erste Datensatz ist erforderlich, um Kauf-Zeilen zu aktualisieren. Er muss die folgenden Einstellungen haben:

- **Quellentabelle:** *Behälteraktivitäten*
- **Quellfeld:** *Erwartetes Enddatum*
- **Zieltabelle:** *Einkaufszeilen*
- **Zielfeld:** *Bestätigtes oder Lieferdatum*

Der zweite Datensatz wird benötigt, um Transaktionen von Waren in Zustellung zu aktualisieren. Er muss die folgenden Einstellungen haben:

- **Quellentabelle:** *Behälteraktivitäten*
- **Quellfeld:** *Erwartetes Enddatum*
- **Zieltabelle:** *Auftrag für Waren in Zustellung*
- **Zielfeld:** *Erwartetes Datum*
