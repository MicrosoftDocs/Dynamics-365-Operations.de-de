---
title: Markieren Sie fertige Waren vor der Buchung in Erfassungen als physisch verfügbar
description: Wenn ein produzierter Artikel als fertig gemeldet wird, wird er als für die weitere physische Bearbeitung verfügbar registriert und eine oder mehrere Erfassungen werden gebucht. Dieser Artikel beschreibt, wie Sie Erfassungsbuchungen aufschieben, indem Sie deren Verarbeitung als Stapelverarbeitung in einer Nachrichtenwarteschlange ermöglichen.
author: johanhoffmann
ms.date: 08/02/2022
ms.topic: article
ms.search.form: ProdParameters, JmgProdParameters, InventLocation, JmgMES3PMessageProcessorMessage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-08-02
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: ee767a5d7c3dca2681861802ae42d7a07217c54d
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689339"
---
# <a name="make-finished-goods-physically-available-before-posting-to-journals"></a>Markieren Sie fertige Waren vor der Buchung in Erfassungen als physisch verfügbar

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Wenn eine Arbeitskraft einen produzierten Artikel als fertig gemeldet hat, registriert das System ihn als für die weitere physische Bearbeitung verfügbar (z. B. Versand oder Einlagerung). Während dieses Prozesses werden auch ein oder mehrere Erfassungen gebucht (z. B. als fertige Erfassung, Kommissionierlistenerfassung und Arbeitsplanlistenerfassung). Wenn Sie Ihre Exemplare physisch verfügbar machen möchten, bevor alle Buchungen verarbeitet wurden, können Sie das System so einrichten, dass die Erfassungsbuchungen zurückgestellt werden. Zurückgestellte Buchungen werden dann von einem Stapelverarbeitungsauftrag verwaltet, der die Buchungen so verarbeitet, wie es die Systemressourcen zulassen.

Die folgende Abbildung zeigt, wie Prozesse zum Buchen von Erfassungen sowohl mit als auch ohne zurückgestellte Buchung aufgerufen werden.

![Der Prozess zum Melden als erledigt mit und ohne zurückgestellte Erfassungsbuchung.](media/deferred-posting-flowchart.png "Der Prozess zum Melden als erledigt mit und ohne zurückgestellte Erfassungsbuchung")

## <a name="turn-on-deferred-journal-posting-for-your-system"></a>Die zurückgestellte Erfassungsbuchung für Ihr System aktivieren

Bevor Sie die verzögerte Erfassungsbuchung verwenden können, muss sie in Ihrem System aktiviert werden. Administratoren können mit dem Arbeitsbereich [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und sie aktivieren. Im Arbeitsbereich **Funktionsverwaltung** ist die Funktion wie folgt aufgeführt:

- **Modul:** *Produktionssteuerung*
- **Funktionsname:** *(Vorschauversion) Markieren Sie fertige Waren vor der Buchung in Erfassungen als physisch verfügbar*

## <a name="set-up-journal-posting-options-for-reporting-as-finished"></a>Erfassungsbuchungsoptionen für die Meldung als fertig einrichten

Arbeitskräfte können Artikel als fertig melden, indem sie einen der folgenden Clients verwenden:

- Webclient
- Mobile Warehouse-Management-App
- Produktionsausführungsschnittstelle

Der Webclient verwendet die gleiche Konfiguration der Buchungsmethode wie die mobile Warehouse-Management-App. Die Buchungsmethode, die die Ausführungsschnittstelle der Produktion verwendet, muss jedoch separat konfiguriert werden.

### <a name="set-journal-posting-options-for-the-web-client-and-the-warehouse-management-mobile-app"></a>Legen Sie Erfassungsbuchungsoptionen für den Webclient und die mobile Warehouse-Management-App fest

In der mobilen App melden Arbeitskräfte Artikel als fertig, indem sie einen Menüpunkt auf dem mobilen Gerät öffnen, wo der Wert **Arbeitserstellungsprozess** *Als fertig melden* oder *Als fertig und eingelagert melden* ist. Im Webclient melden Arbeitskräfte Artikel von der Listenseite **Alle Produktionsaufträge** oder der Seite **Produktionsauftrag (Details)** als fertig. Sie können eine unternehmensweite Standardmethode konfigurieren und bei Bedarf auch lagerspezifische Überschreibungen einrichten.

Verwenden Sie das folgende Verfahren, um die unternehmensweite Standardbuchungsmethode zum Melden von Artikeln als fertig über den Webclient oder die mobile Warehouse-Management-App zu konfigurieren.

1. Wechseln Sie zu **Produktionssteuerung \> Einstellungen \> Produktionssteuerungsparameter**.
1. Auf der Registerkarte **Erfassungen** im Abschnitt **Fertigmeldungserfassung** legen Sie das Feld **Buchungsmethode** auf einen der folgenden Werte fest:

    - *Sofort*: Wenn ein Artikel als fertig gemeldet wird, verarbeitet das System alle zugehörigen Erfassungsbuchungen vollständig, bevor es den fertigen Artikel als physisch verfügbar kennzeichnet.
    - *Zurückgestellt*: Wenn ein Artikel als fertig gemeldet wird, kennzeichnet das System den fertigen Artikel als physisch verfügbar und fügt die Erfassungsbuchung einer Nachrichtenwarteschlange hinzu. Das System wartet nicht, bis die Buchungen vollständig verarbeitet sind, bevor es den fertigen Artikel als physisch verfügbar kennzeichnet.

Verwenden Sie das folgende Verfahren, um lagerortspezifische Überschreibungen für die Standardbuchungsmethode zu konfigurieren, die auf der Seite **Produktionssteuerungsparameter** konfiguriert ist.

1. Gehen Sie zu **Lagerverwaltung \> Einrichten \> Lageraufschlüsselung \> Lagerorte**.
1. Wählen Sie den Lagerort aus, den Sie einrichten wollen.
1. Wählen Sie im Aktionsbereich **Bearbeiten** aus.
1. Legen Sie auf dem Inforegister **Lagerort** im Abschnitt **Produktionsaufträge** das Feld **Buchungsmethode** auf einen der folgenden Werte fest:

    - *Erben*: Der ausgewählte Lagerort erbt die Einstellung von der Seite **Produktionssteuerungsparameter**.
    - *Sofort*: Wenn ein Artikel als fertig gemeldet wird, verarbeitet das System alle zugehörigen Erfassungsbuchungen vollständig, bevor es den fertigen Artikel als physisch verfügbar kennzeichnet.
    - *Zurückgestellt*: Wenn ein Artikel als fertig gemeldet wird, kennzeichnet das System den fertigen Artikel als physisch verfügbar und fügt die Erfassungsbuchung einer Nachrichtenwarteschlange hinzu. Das System wartet nicht, bis die Buchungen vollständig verarbeitet sind, bevor es den fertigen Artikel als physisch verfügbar kennzeichnet.

### <a name="set-journal-posting-options-for-the-production-floor-execution-interface"></a>Erfassungsbuchungsoptionen für die Produktionsausführungsschnittstelle einrichten

Gehen Sie wie folgt vor, um die Buchungsmethode zu konfigurieren, die verwendet wird, wenn Artikel von der Produktionsausführungsschnittstelle als fertig gemeldet werden.

1. Gehen Sie zu **Produktionssteuerung \> Einstellungen \> Fertigungssteuerung \> Produktionsparameterstandard**.
1. Legen Sie auf der Registerkarte **Als fertig melden** im Abschnitt **Fertigmeldungserfassung** das Feld **Buchungsmethode** auf einen der folgenden Werte fest:

    - *Sofort*: Wenn ein Artikel als fertig gemeldet wird, verarbeitet das System alle zugehörigen Erfassungsbuchungen vollständig, bevor es den fertigen Artikel als physisch verfügbar kennzeichnet.
    - *Zurückgestellt*: Wenn ein Artikel als fertig gemeldet wird, kennzeichnet das System den fertigen Artikel als physisch verfügbar und fügt die Erfassungsbuchung einer Nachrichtenwarteschlange hinzu. Das System wartet nicht, bis die Buchungen vollständig verarbeitet sind, bevor es den fertigen Artikel als physisch verfügbar kennzeichnet.

## <a name="schedule-the-message-processor-batch-job-to-process-deferred-postings"></a>Den Nachrichtenprozessor-Stapelverarbeitungsauftrag planen, um verzögerte Buchungen zu verarbeiten

Der Nachrichtenprozessor-Stapelverarbeitungsauftrag ist für die Verarbeitung der Erfassungsbuchungen verantwortlich, nachdem sie in die Warteschlange gestellt wurden. Um sicherzustellen, dass Ihre Erfassungsbuchungen verarbeitet werden, müssen Sie diesen Auftrag so konfigurieren, dass er in regelmäßigen Abständen ausgeführt wird. Gehen Sie wie folgt vor, um den erforderlichen Stapelverarbeitungsauftrag einzurichten.

1. Gehen Sie zu **Systemverwaltung \> Nachrichtenprozessor \> Nachrichtenprozessor**.
1. Legen Sie im Inforegister **Parameter** das Feld **Nachrichtenwarteschlange** auf *Produktion* fest.
1. Legen Sie im Inforegister **Im Hintergrund ausführen** die Option **Stapelverarbeitung** auf *Ja* fest. Legen Sie dann einen wiederkehrenden Zeitplan fest und konfigurieren Sie andere Einstellungen nach Bedarf. Die Einstellungen funktionieren genauso wie bei anderen Arten von [Hintergrundaufträgen](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) in Microsoft Dynamics 365 Supply Chain Management.

## <a name="track-the-progress-of-your-deferred-postings"></a>Den Fortschritt Ihrer aufgeschobenen Buchungen verfolgen

Zurückgestellte Erfassungsbuchungen werden als *Nachrichtenprozessormeldungen* in die Warteschlange gestellt und warten dort, bis sie vom *Nachrichtenprozessor* verarbeitet werden. Der Nachrichtenprozessor sollte so eingerichtet werden, dass er als geplanter Stapelverarbeitungsauftrag ausgeführt wird. Um die zurückgestellten Buchungsnachrichten anzuzeigen, die vom Nachrichtenprozessor verarbeitet wurden oder werden, gehen Sie zu **Produktionssteuerung \> Produktionsaufträge \> Zurückgestellte Produktionsauftragsbuchung**.

### <a name="message-grid-columns-and-filters"></a>Spalten des Nachrichten-Rasters und Filter

Sie können die Felder oben auf der Seite **Zurückgestellte Produktauftragsbuchung** verwenden, um bestimmte Nachrichten zu finden, die Sie suchen.

Folgende Filter sind verfügbar:

- **Nachrichtentyp**: Geben Sie die Art der Nachrichten an, die im Raster angezeigt werden.
- **Nachrichtenstatus**: Geben Sie des Status der Nachrichten an, die im Raster angezeigt werden. Es gibt die folgenden Status:

    - *Warteschlange* – Die Nachricht ist bereit, vom Nachrichtenprozessor verarbeitet zu werden.
    - *Verarbeitet* – Die Nachricht wurde erfolgreich vom Nachrichtenprozessor verarbeitet.
    - *Storniert*: Die Nachricht konnte beim letzten Versuch nicht verarbeitet werden und wurde dann vom Benutzer storniert.
    - *Fehlgeschlagen*: Die Nachricht konnte beim letzten Versuch nicht verarbeitet werden. Das System versucht fehlgeschlagene Nachrichten dreimal erneut auszuführen. Dann gibt es auf und lässt die Nachricht im Status *Fehlgeschlagen*. Beachten Sie, dass Sie eine Nachricht erst nach dem letzten dieser drei Versuche manuell stornieren oder bearbeiten können.

- **Nachrichteninhalt** – Dieser Filter führt eine Volltextsuche im Inhalt der Nachricht durch. (Der Inhalt von Nachrichten wird im Raster nicht angezeigt.) Der Filter behandelt die meisten Sonderzeichen (z. B. Bindestriche) als Leerzeichen und behandelt alle Leerzeichen als boolesche ODER-Operatoren. Wenn Sie beispielsweise nach einem bestimmten `journalid`-Wert suchen, der *USMF-123456* entspricht, findet das System alle Nachrichten, die entweder „USMF“ oder „123456“ enthalten. In diesem Fall dürften Sie eine lange Ergebnisliste erhalten. Daher wäre es besser, nur *123456* einzugeben, weil Sie so spezifischere Ergebnisse erhalten.

Sie können die Liste auch sortieren und filtern, indem Sie eine der Spaltenüberschriften auswählen und Kriterien in das Dropdown-Dialogfeld eingeben.

### <a name="view-the-message-log-message-content-and-details"></a>Anzeigen des Nachrichtenprotokolls, des Inhalts von Nachrichten und der Details

Sie finden detaillierte Informationen zu einer Nachricht, indem Sie sie im Raster und dann die Registerkarte **Protokoll** oder **Unformatierter Inhalt** unter dem Nachrichtenraster auswählen, wo jedes verarbeitete Ereignis angezeigt wird.

Die Symbolleiste auf der Registerkarte **Protokoll** enthält die folgenden Schaltflächen:

- **Protokoll**: Wählen Sie diese Schaltfläche, um die Verarbeitungsergebnisse anzuzeigen. Diese Schaltfläche ist besonders nützlich, wenn Nachrichten den **Verarbeitungsergebnis**-Wert *Fehlgeschlagen* haben und Sie die Gründe für den Verarbeitungsfehler erfahren möchten.
- **Bündel** – Mehrere Vorgänge zur Verarbeitung von Nachrichten können als Teil desselben Batch-Prozesses ausgeführt werden. Wählen Sie diese Schaltfläche, um diese detaillierten Daten anzuzeigen. Sie können z. B. sehen, ob Abhängigkeiten bestehen, aufgrund derer für einige Nachrichten eine bestimmte Verarbeitungsreihenfolge notwendig ist.

### <a name="manually-process-or-cancel-a-message"></a>Manuelles Verarbeiten oder Stornieren einer Nachricht

Sie können eine Nachricht bei Bedarf und abhängig von ihrem aktuellen Status manuell verarbeiten. Wählen Sie die Nachricht im Raster und dann **Verarbeiten** oder **Stornieren** im Aktivitätsbereich aus.

### <a name="set-up-business-events-to-deliver-alerts-for-failed-processing-results"></a>Festlegen von Ereignissen, um Warnungen für fehlgeschlagene Verarbeitungen zu liefern

Sie können [Geschäftsereignisse](../../fin-ops-core/dev-itpro/business-events/home-page.md) einrichten, die Sie bei fehlgeschlagenen Verarbeitungsergebnissen benachrichtigen. Gehen Sie zu **Systemverwaltung \> Einrichten \> Geschäftsereignisse \> Geschäftsereigniskatalog** und aktivieren Sie das Geschäftsereignis mit dem Namen *Nachrichtenprozessornachricht verarbeitet*.

Sie werden im Rahmen des Aktivierungsprozesses aufgefordert, anzugeben, ob das Ereignis für eine bestimmte juristische Person spezifisch oder für alle juristischen Personen gilt. Sie werden auch aufgefordert, einen Wert für den **Endpunktnamen** einzugeben. Dieser Wert muss zuerst festgelegt werden.

> [!NOTE]
> Wenn das Feld **Wenn ein Ereignis eintritt** auf *Microsoft Power Automate* festgelegt ist (anstatt z. B. auf *HTTPS*), wird der Wert für den **Endpunktnamen** automatisch im Supply Chain Management erstellt, basierend auf den *Microsoft Power Automate*-Einstellungen.
