---
title: Wellenausführungsbenachrichtigungen
description: In diesem Thema Wellenausführungsbenachrichtungen beschrieben und die Einrichtung erläutert.
author: mirzaab
ms.date: 04/03/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WhsWaveNotificationPolicy, WHSParameters, WHSWaveTemplateTable, BusinessEventsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2022-04-01
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: 0a61aff10234f40f14d603852be30fec3ba83647
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838081"
---
# <a name="wave-execution-notifications"></a>Wellenausführungsbenachrichtigungen

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Die Funktion *Wellenausführungsbenachrichtigungen* verwendet Geschäftsereignisse und das Aktionszentrum, um Benachrichtigungen zu übermitteln, die sich auf die Wellenausführung beziehen. Hier können Sie die Ereignistypen, die Benachrichtigungen generieren, die Lagerorte, von denen sie generiert werden, und die Benutzer, die sie erhalten, angeben.

Die Schaltfläche **Nachrichten anzeigen** (Glockensymbol) auf der rechten Seite der Navigationsleiste zeigt an, wann eine Aktionszentrumsnachricht für den aktuellen Benutzer verfügbar ist. Der Benutzer kann die Schaltfläche **Nachrichten anzeigen** auswählen, um das Aktionszentrum zu öffnen und die Nachrichten zu lesen.

Geschäftsereignisse treten auf, wenn Geschäftsprozesse ausgeführt werden. Geschäftsprozesse bestehen aus Aufgaben. Während eines Geschäftsprozesses führen die Benutzer, die daran teilnehmen, Geschäftsaktionen aus, um diese Aufgaben zu erledigen. Geschäftsereignisse bieten einen Mechanismus, mit dem externe Systeme Benachrichtigungen von Finance and Operations-Anwendungen erhalten. Auf diese Weise können die Systeme Geschäftsaktionen als Reaktion auf die Geschäftsereignisse ausführen. Weitere Informationen finden Sie unter [Übersicht über Geschäftsereignisse](../../fin-ops-core/dev-itpro/business-events/home-page.md).

## <a name="turn-on-the-wave-execution-notifications-feature"></a>Funktion für Wellenausführungsbenachrichtigungen aktivieren

Bevor Sie die Funktion *Wellenausführungsbenachrichtigungen* verwenden können, muss sie in Ihrem System aktiviert sein. Administratoren können mit der Einstellung [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und ggf. aktivieren. Dort wird die Funktion folgendermaßen aufgelistet:

- **Module:** *Lagerortverwaltung*
- **Funktionsname:** *Wellenausführungsbenachrichtigungen*

## <a name="scenario-send-wave-batch-execution-notifications-to-the-action-center"></a>Szenario: Senden Sie Benachrichtigungen zur Ausführung von Wellenstapelverarbeitungen an das Aktionszentrum

Dieses Szenario zeigt den End-to-End-Flow zum Senden von Benachrichtigungen über Ausführungsfehler bei Wellenstapelverarbeitungen an eine bestimmte Rolle über das Aktionszentrum.

### <a name="make-demo-data-available"></a>Demodaten zur Verfügung stellen

Um diesem Szenario zu folgen, müssen Demodaten installiert sein, und Sie müssen die juristische Person **USMF** auswählen.

### <a name="make-sure-that-waves-are-run-in-batch-mode"></a>Sicherstellen, dass Wellen im Stapelverarbeitungsmodus ausgeführt werden

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerortverwaltungsparameter**.
1. Im Inforegister **Wellenverarbeitung** setzen Sie die Option **Wellen in einem Stapel verarbeiten** auf *Ja*.

> [!NOTE]
> Wenn Sie Wellenausführungsbenachrichtigungen deaktivieren möchten, legen Sie die Option **Wellenausführungsbenachrichtigungen deaktivieren** auf *Ja* fest.

### <a name="configure-a-wave-notification-policy"></a>Eine Wellenbenachrichtigungsrichtlinie konfigurieren

Wellenenachrichtigungsrichtlinien definieren die Arten der gesendeten Benachrichtigungen und die Benutzer, die benachrichtigt werden.

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Wellen \> Wellenbenachrichtigungsrichtlinien**.
1. Erstellen Sie einen Datensatz mit den folgenden Einstellungen:

    - **Wellenbenachrichtigungsrichtlinie:** *24BatchError*
    - **Beschreibung:** *Wellenstapelverarbeitungsfehler bei Lagerort 24*
    - **Benachrichtigung senden an:** *Nur Fehler*
    - **An Rolle:** *Systemadministratorrolle*

        > [!NOTE]
        > Da in diesem Szenario Demodaten verwendet werden, wird die Rolle *Systemadministrator* der Einfachheit halber ausgewählt. Da Sie als Systemadministrator angemeldet sind, erhalten Sie daher die Benachrichtigungen. In der Praxis sollten Sie jedoch normalerweise eine spezifischere Rolle auswählen, um über Fehler bei der Ausführung von Wellenstapelverarbeitungen zu informieren, z. B. den *Lagerortleiter*.

1. Wählen Sie im Aktionsbereich **Speichern** aus.

### <a name="configure-a-wave-template"></a>Eine Wellenvorlage konfigurieren

Mit Wellenvorlagen können Sie bestimmte Instanzen von Wellenmethoden mit entsprechenden Wellenetikettenvorlagen verknüpfen.

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Wellen \> Wellenvorlagen**.
1. Stellen Sie im Listenbereich das Feld **Wellenvorlagentyp** auf *Versand* und wählen Sie dann die Wellenvorlage *Standard-24-Lieferung* für Lagerort 24 aus.
1. Im Inforegister **Allgemein** legen Sie das Feld **Wellenbenachrichtigungsrichtlinie** auf *24BatchError* fest.

### <a name="configure-a-work-template"></a>Eine Arbeitsvorlage konfigurieren

Arbeitsvorlagen werden während der Wellenausführung verwendet, um Arbeit zu generieren. In diesem Szenario sollte die Wellenausführung einen Fehler auslösen. Indem Sie die Arbeitsvorlagenabfrage so einstellen, dass ein nicht vorhandene Lagerort verwendet wird, stellen Sie sicher, dass die Wellenausführung fehlschlägt und daher eine Benachrichtigung sendet.

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Arbeit \> Arbeitsvorlagen**.
1. Stellen Sie im Listenbereich das Feld **Arbeitsvorlagentyp** auf *Aufträge* und wählen Sie dann die Arbeitsvorlage *24 SO-Phase* für Lagerort 24 aus.
1. Wählen Sie im Aktionsbereich **Abfrage bearbeiten** aus.
1. Bearbeiten Sie in der Registerkarte **Bereich** des Dialogfelds des Abfrageeditors die folgende Zeile (oder fügen Sie sie hinzu, wenn sie nicht vorhanden ist):

    - **Tabelle:** *Temporäre Arbeitstransaktionen*
    - **Abgeleitete Tabelle:** *Temporäre Arbeitstransaktionen*
    - **Feld:** *Lagerort*
    - **Kriterien:** Ändern Sie den Wert von *24* auf *Fehler*.

1. Bestätigen Sie die Änderung mit **OK**.

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a>Einen Auftrag erstellen und ihn für den Lagerort freigeben

1. Gehen Sie zu **Vertrieb und Marketing \> Auftrag \> Alle Aufträge**.
1. Erstellen Sie einen Auftrag mit den folgenden Einstellungen:

    - **Debitorenkonto:** *US-001*
    - **Lagerort:** *24*

1. Fügen Sie im Inforegister **Auftragspositionen** eine Auftragsposition mit den folgenden Einstellungen hinzu:

    - **Artikelnummer** *A001*
    - **Menge** *10*

    > [!NOTE]
    > Diese Artikel und Mengen sind nur Beispiele. Der betroffene Lagerort muss ausreichen Bestände haben.

1. Während die neue Auftragsposition weiterhin im Inforegister **Auftragspositionen** ausgewählt ist, wählen Sie im Menü **Bestand \> Reservierung** aus.
1. Wählen Sie auf der Seite **Reservierung** im Aktivitätsbereich **Los reservieren** aus. Schließen Sie nun die Seite.
1. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Lagerort** auf **Lagerortfreigabe**.

### <a name="notifications-from-wave-batch-job-execution"></a>Benachrichtigungen von der Ausführung von Wellenstapelverarbeitungsaufträgen

Abhängig von der Einrichtung Ihrer Geschäftsereignisse erhalten Sie möglicherweise eine Benachrichtigung über einen Fehler bei der Wellenausführung. Die Aktionszentrumsnachricht ähnelt dem folgenden Beispiel und enthält einen Link zu der Welle, die fehlgeschlagen ist.

> **Fehler bei der Zyklusausführung**  
> Beim Ausführen der Welle USMF-000000001 ist ein Fehler aufgetreten.  
> Letzte Nachrichten: Für Welle USMF-000000001 wurde keine Arbeit erstellt.
>
> **STATUS**  
> Aktiv
>
> Offene Zyklusdetails

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
