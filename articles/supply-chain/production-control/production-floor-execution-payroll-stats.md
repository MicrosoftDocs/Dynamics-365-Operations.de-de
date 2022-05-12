---
title: Urlaubssalden in der Produktionsausführungsoberfläche anzeigen
description: Dieses Thema enthält ein Beispielszenario, das zeigt, wie Sie Microsoft Dynamics 365 Supply Chain Management einrichten, sodass es Arbeitskräften anhand der Lohnstatistik einen Überblick über ihren Urlaubssaldo für das laufende Jahr gibt.
author: johanhoffmann
ms.date: 04/22/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-04-22
ms.dyn365.ops.version: 10.0.XX
ms.openlocfilehash: a97858c72b0be50609cee552bd0635e2d68ea478
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2022
ms.locfileid: "8645346"
---
# <a name="show-vacation-balances-in-the-production-floor-execution-interface"></a>Urlaubssalden in der Produktionsausführungsoberfläche anzeigen

[!include [banner](../includes/banner.md)]

Dieses Thema enthält ein Beispielszenario, das zeigt, wie Sie Microsoft Dynamics 365 Supply Chain Management einrichten, sodass jeder einzelnen Arbeitskraft anhand der Lohnstatistik einen Überblick über ihren Urlaubssaldo für das laufende Jahr gibt. Arbeitskräfte können ihren Urlaubssaldo im Dialogfeld **Mein Tag** in der Produktionsausführungsoberfläche sehen.

Dieses Szenario verwendet das dänische Urlaubsgesetz, bei dem das Urlaubsjahr vom 1. September bis zum 31. August dauert. In diesem Szenario hat Ihr Unternehmen eine neue Arbeitskraft eingestellt und gewährt dieser Arbeitskraft einen Urlaub von 10 Tagen für den Rest des aktuellen Urlaubsjahres.

## <a name="turn-on-the-required-features"></a>Aktivieren Sie die erforderlichen Funktionen

Um dieses Szenario auszuführen, müssen Sie die *Ansicht „Mein Tag“ für die Produktionsausführungsoberfläche*-Funktion in [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) aktivieren. Informationen zum Aktivieren dieser und anderer Funktionen für die Produktionsausführungsoberfläche finden Sie unter [Produktionsausführungsoberfläche konfigurieren](production-floor-execution-configure.md).

## <a name="make-sample-data-available"></a>Beispieldaten zur Verfügung stellen

Um dieses Szenario mithilfe der Beispieldatensätze und -werte, die hier angegeben sind, zu verarbeiten, müssen Sie ein System verwenden, auf dem die standardmäßigen [Demodaten](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) installiert sind. Außerdem müssen Sie die **USMF** juristische Person auswählen, bevor Sie beginnen.

## <a name="create-a-new-pay-type"></a>Neue Lohnart erstellen

Beginnen Sie mit der Erstellung einer neuen *Lohnart*, um die verdienten Urlaubstage der Arbeitskräfte (auch ihr *Urlaubssaldo* genannt) nachzuverfolgen. In der Regel werden Lohnarten verwendet, um den Lohn der Arbeitskräfte zu berechnen. Die Lohnart, die Sie hier anlegen, wird jedoch zur Berechnung eines Saldos verwendet.

1. Wechseln Sie zu **Zeit und Anwesenheit \> Einstellungen \> Lohn \> Lohnarten**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Zeile zum Raster hinzuzufügen.
1. Legen Sie in der neuen Zeile die folgenden Werte fest:

    - **Lohnart:** *5151-1*
    - **Beschreibung:** *Zähler für Arbeitskrafturlaubstage*
    - **In Export einbeziehen:** *Nein*

## <a name="update-the-pay-agreement"></a>Lohnvereinbarung aktualisieren

In diesem Abschnitt bearbeiten Sie eine vorhandene *Lohnvereinbarung*, indem Sie die neue Lohnart hinzufügen und die Regeln festlegen, die definieren, wie der Urlaubssaldo jeder Arbeitskraft angepasst wird, wenn Urlaubstage registriert werden.

1. Wechseln Sie zu **Zeit und Anwesenheit \> Einstellungen \> Lohn \> Lohnvereinbarungen**.
1. Wählen Sie die Lohnvereinbarung aus, in der Sie die Urlaubsrichtlinie einrichten möchten. (Wenn Sie mit standardmäßigen USMF-Beispieldaten arbeiten, gibt es nur eine Lohnvereinbarung, *Man*.)
1. Stellen Sie sicher, dass die gewählte Lohnvereinbarung für das aktuelle Datum gültig ist. Wenn Sie mit standardmäßigen USMF-Beispieldaten arbeiten, ist das Feld **Bis-Datum** der Lohnvereinbarung *Man* ggf. auf ein in der Vergangenheit liegendes Datum gesetzt. Ändern Sie den Wert nach Bedarf so, dass er ein oder zwei Jahre in der Zukunft liegt.
1. Wählen Sie im Aktivitätsbereich **Vereinbarungspositionen** aus.
1. Legen Sie auf der Seite **Vereinbarungspositionen** im Inforegister **Überblick** die folgenden Werte in der Symbolleiste fest:

    - Wählen Sie in der ersten Dropdownliste **Montag** aus.
    - Wählen Sie in der zweiten Dropdownliste **Abwesenheit** aus.

1. Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Zeile zum Raster hinzuzufügen.
1. Legen Sie in der neuen Zeile das Feld **Lohnart** auf die Lohnart fest, die Sie für dieses Szenario angelegt haben (*5151-1*). Belassen Sie alle anderen Einstellungen auf ihren Standardwerten.
1. Während die neue Zeile noch ausgewählt ist, legen Sie im Inforegister **Allgemein** die folgenden Werte fest:

    - **Abwesenheitscode:** *Urlaub*
    - **Feste Menge verwenden:** *Ja*
    - **Dauerhaft:** *-1*

1. Wählen Sie im Aktivitätsbereich **Tag kopieren**.
1. Legen Sie im Dialogfeld **Tag kopieren** die folgenden Werte fest:

    - **Dienstag**, **Mittwoch**, **Donnerstag** und **Freitag**: *Ja*
    - **Überschreiben:** *Ja*
    - **Abwesenheit:** *Ja*

1. Wählen Sie **OK** aus.

## <a name="create-a-payroll-statistic-group"></a>Lohnstatistikgruppe erstellen

*Lohnstatistikgruppen* werden verwendet, um Statistiken für Arbeitskraftregistrierungen während eines Zeitraums einzurichten. In diesem Szenario verwenden Sie eine Lohnstatistikgruppe, um die Anzahl der Urlaubstage zu berechnen, die Arbeitskräfte während eines Urlaubszeitraums verdienen. In Dänemark läuft die Urlaubszeit vom 1. September bis 31. August.

1. Wechseln Sie zu **Zeit und Anwesenheit \> Einstellungen \> Lohn \> Lohnstatistikgruppen**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Zeile zum Raster hinzuzufügen.
1. Legen Sie in der neuen Zeile die folgenden Werte fest:

    - **Lohnstatistikgruppe:** *VAC*
    - **Beschreibung:** *Urlaubssaldo*
    - **Übertrag:** *Nein*

1. Während die neue Zeile noch markiert ist, wählen Sie **Einrichtung** im Aktivitätsbereich.
1. Wählen Sie auf der Seite **Einrichtung** im Aktivitätsbereich **Neu**, um dem Raster eine Zeile hinzuzufügen.
1. Stellen Sie in der neuen Zeile das Feld **Lohnart** auf *5151-1*.
1. Halten Sie das Feld **Periodencode** gedrückt (oder klicken Sie mit der rechten Maustaste darauf) und wählen Sie dann **Details anzeigen**. Sie können jetzt den Periodencode einrichten, den Sie diesem Feld später zuweisen werden.
1. Wählen Sie auf der Seite **Periodentypen** im Aktivitätsbereich **Neu**, um dem Raster eine Zeile hinzuzufügen.
1. Legen Sie in der neuen Zeile die folgenden Werte fest:

    - **Periodentypen:** *VacYear*
    - **Beschreibung:** *Urlaubsjahr*
    - **Frequenz:** *Jahre*

1. Während die neue Zeile noch markiert ist, wählen Sie **Perioden erzeugen** im Aktivitätsbereich.
1. Legen Sie im Dialogfeld **Perioden erzeugen** die folgenden Werte fest:

    - **Startdatum der Periode angeben:** *1. September 2021*
    - **Länge der Periode:** *5*

1. Wählen Sie **OK** aus.
1. Schließen Sie die Seite **Periodentypen**, um zur Seite **Lohnstatistikgruppen** zurückzukehren.
1. Stellen Sie das Feld **Periodencode** auf die Periodenart, die Sie gerade erstellt haben (*VacYear*).

## <a name="create-a-statistical-balance-setup"></a>Einstellungen für die Statistikbilanz erstellen

In diesem Abschnitt erstellen Sie die *Einstellungen für die Statistikbilanz*, die mit der Lohnstatistikgruppe verknüpft sind, die Sie im vorherigen Abschnitt erstellt haben. Später werden Sie diese Einstellungen für die Statistikbilanz mit der Ansicht **Mein Tag** in der Produktionsausführungsoberfläche verknüpfen. Die Ansicht **Mein Tag** kann dann die Urlaubssalden für die Lohnart anzeigen, die der zugehörigen Lohnstatistikgruppe zugeordnet ist.

1. Wechseln Sie zu **Zeit und Anwesenheit \> Einstellungen \> Lohn \> Einstellungen für die Statistikbilanz**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Zeile zum Raster hinzuzufügen.
1. Legen Sie in der neuen Zeile die folgenden Werte fest:

    - **Lohnstatistikgruppe:** *VAC*
    - **Externer Name:** *Urlaubssaldo*
    - **Gleitzeit:** *Nein*

## <a name="create-a-manual-premium"></a>Manuelle Zulage erstellen

*Manuelle Zulagen* werden in der Regel verwendet, um Arbeitskräften für zusätzliche Arbeit einen Zuschlag zu gewähren. In diesem Szenario erstellen Sie eine manuelle Zulage, die Sie verwenden können, um den anfänglichen Urlaubssaldo für jede Arbeitskraft festzulegen.

1. Wechseln Sie zu **Zeit und Anwesenheit \> Einstellungen \> Lohn \> Manuelle Zulagen**.
1. Wählen Sie im Aktionsbereich **Neu** aus, um einen Datensatz hinzuzufügen.
1. Legen Sie im neuen Datensatz die folgenden Werte fest:

    - **Zulagen:** *VAC*
    - **Beschreibung:** *Anpassungen des Urlaubssaldos der Arbeitskräfte*
    - **Lohnart:** *5151-1*

## <a name="set-a-workers-initial-vacation-balance-and-adjust-it-by-one-day"></a>Anfänglichen Urlaubssaldo einer Arbeitskraft festlegen und um einen Tag anpassen

Lohnadministratoren verwenden die Seite **Genehmigen**, um die täglichen Registrierungen der Arbeitskräfte zu überprüfen und zu genehmigen. In diesem Szenario übernehmen Sie die Rolle eines Administrators, damit Sie den anfänglichen Urlaubssaldo für eine Arbeitskraft festlegen und Urlaubstage registrieren können, die die Arbeitskraft nimmt.

1. Wechseln Sie zu **Zeit und Anwesenheit \> Prüfen und genehmigen \> Genehmigen**.
1. Im angezeigten Dialogfeld **Genehmigen** legen Sie die folgenden Felder fest:

    - **Genehmigungsgruppe** – Wählen Sie die Genehmigungsgruppe aus, der Sie angehören. (Wenn Sie mit standardmäßigen USMF-Beispieldaten arbeiten, gibt es nur eine Genehmigungsgruppe, *AdmMan*.)
    - **Gesamte Gruppe anzeigen (1 Tag)** – Wählen Sie die Option aus und stellen Sie dann das Feld auf das aktuelle Datum ein.

1. Wählen Sie **OK** aus.
1. Die Seite **Genehmigen** zeigt eine Liste der Datensätze, die Ihren Kriterien entsprechen. Wählen Sie die Arbeitskraft, der Sie eine Genehmigung geben wollen. Wenn Sie mit standardmäßigen USMF-Beispieldaten arbeiten, wählen Sie Arbeitskraft *000496* (*Christina Portra*) aus.
1. Gewähren Sie der ausgewählten Arbeitskraft 10 Tage Urlaub:

    1. Während die Arbeitskraft noch markiert ist, wählen Sie **Zulagenpositionen** im Aktivitätsbereich.
    1. Wählen Sie auf der Seite **Zulagenpositionen** im Aktivitätsbereich **Neu**, um dem Raster eine Zeile hinzuzufügen.
    1. Legen Sie in der neuen Zeile die folgenden Werte fest:

        - **Zulagen:** *VAC*
        - **Menge** *10*

    1. Schließen Sie die Seite **Zulagenpositionen**.

1. Registrieren Sie auf der Seite **Genehmigen** die Tatsache, dass die Arbeitskraft einen ihrer Urlaubstage am aktuellen Datum verbraucht hat:

    1. Während die Arbeitskraft noch markiert ist, wählen Sie im unteren Teil der Seite auf der Registerkarte **Übersicht** in der Symbolleiste **Neu**, um dem Raster eine Zeile hinzuzufügen.
    1. Legen Sie in der neuen Zeile die folgenden Werte fest:

        - **Journalerfassungstyp:** *Abwesenheit*
        - **Referenz:** *Urlaub*

    1. Wählen Sie im oberen Teil der Seite **Übertrag** in der Symbolleiste aus, um den Urlaubssaldo anzuwenden und den Abzug zu berechnen.

## <a name="configure-the-production-floor-execution-interface-so-that-it-includes-the-my-day-dialog-box"></a>Produktionsausführungsoberfläche so konfigurieren, dass sie das Dialogfeld „Mein Tag“ enthält

In diesem Abschnitt fügen Sie eine Schaltfläche **Mein Tag** zur Produktionsausführungsoberfläche hinzu. Arbeitskräfte können dann diese Schaltfläche verwenden, um die Dialogbox **Mein Tag** zu öffnen.

1. Gehen Sie zu **Produktionskontrolle \> Einrichtung \> Fertigungsausführung \> Ausführung in der Produktion**.
1. Wählen Sie eine Konfiguration wie *Standard* aus.
1. Wählen Sie im Aktivitätsbereich **Entwurfsregisterkarten** aus.
1. Wählen Sie auf der Seite **Entwurfsregisterkarten** im Listenbereich *Alle Einzelvorgänge* aus, um die Einstellungen für diese Registerkarte anzuzeigen. Das Feld **Hauptansicht** sollte jetzt einen Wert *Alle Einzelvorgänge* anzeigen.
1. Wählen Sie im Aktionsbereich **Bearbeiten** aus.
1. Wählen Sie im Inforegister **Sekundäre Symbolleiste** in der Spalte **Verfügbare Aktionen** die Option **Mein Tag**. Wählen Sie dann die Schaltfläche mit dem Pfeil nach rechts, um das Element in die Spalte **Ausgewählte Aktionen** zu verschieben.

## <a name="check-your-balance-in-the-production-floor-execution-interface"></a>Saldo in der Produktionsausführungsoberfläche überprüfen

In diesem Abschnitt melden Sie sich als die Arbeitskraft, deren Urlaubszeit Sie zuvor eingerichtet haben, bei der Produktionsausführungsoberfläche an. Sie öffnen dann das Dialogfeld **Mein Tag**, um Ihren Urlaubssaldo anzuzeigen.

1. Wechseln Sie zu **Produktionskontrolle \> Einrichtung \> Fertigungsausführung \> Produktionsumgebungsausführung**.
1. Wenn Sie aufgefordert werden, eine Konfiguration auszuwählen, wählen Sie die Konfiguration aus, die Sie zuvor in diesem Szenario eingerichtet haben (*Standard*).
1. Melden Sie sich als der Benutzer an, den Sie zuvor in diesem Szenario eingerichtet haben. Wenn Sie mit standardmäßigen USMF-Beispieldaten arbeiten, sollten Sie sich durch Eingabe von *123* im Feld **Kennkartenkennung** anmelden können. Diese Kennkartenkennung entspricht Christina Portra.
1. Wählen Sie in der linken Symbolleiste die Option **Mein Tag** aus.
1. Untersuchen Sie den Abschnitt **Salden** des Dialogfelds. Dieser Abschnitt sollte nun zeigen, dass Sie einen Saldo von neun Urlaubstagen haben.
