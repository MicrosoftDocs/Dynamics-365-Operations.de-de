---
title: Erstellen eines Stapelverarbeitungsauftrags
description: Bei einem Batchauftrag handelt es sich um eine Gruppe von Aufgaben, die zur automatischen Verarbeitung an eine Anwendungsobjektserver-Instanz (AOS) übermittelt werden.
author: matapg007
ms.date: 11/22/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: matgupta
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: BatchJob, SysRecurrence, BatchAlerts
ms.openlocfilehash: 06fb9a18e70c316be97645ba76f9462cd3ccc729
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292449"
---
# <a name="create-a-batch-job"></a>Erstellen eines Stapelverarbeitungsauftrags

[!include [banner](../../includes/banner.md)]

Bei einem Batchauftrag handelt es sich um eine Gruppe von Aufgaben, die zur automatischen Verarbeitung an eine Anwendungsobjektserver-Instanz (AOS) übermittelt werden. Stapelverarbeitungsaufträge werden unter Verwendung der Sicherheitsanmeldeinformationen des Benutzers ausgeführt, von dem der Auftrag erstellt wurde. Verwenden Sie die folgende Prozedur, um einen Batchauftrag zu erstellen. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.


## <a name="create-the-batch-job"></a>Den Batchauftrag erstellen
1. Wechseln Sie zu **Navigationsbereich > Module > Systemverwaltung > Anfragen > Batchauftrag**.
2. Wählen Sie **Neu** aus.
3. Geben Sie im Feld **Stellenbeschreibung** eine Beschreibung für den Batchauftrag ein.
4. Geben Sie im Feld **Geplantes Startdatum/-uhrzeit** das Datum und die Uhrzeit ein, zu der der Batchauftrag ausgeführt werden soll.
5. Wählen Sie **Speichern** aus.

## <a name="create-a-recurrence"></a>Eine Wiederholung erstellen
1. Klicken Sie im Aktivitätsbereich auf **Batchauftrag**.
2. Wählen Sie **Wiederholung**. Verwenden Sie diese Optionen, um einen Bereich und ein Muster für die Wiederholung einzugeben.  
3. Wählen Sie **OK** aus.

## <a name="add-alerts"></a>Warnungen hinzufügen
1. Klicken Sie im Aktivitätsbereich auf **Batchauftrag**.
2. Wählen Sie **Benachrichtigungen** aus. Geben Sie an, ob Sie möchten, dass Warnmeldungen gesendet werden, wenn der Batchauftrag endet, einen Fehler aufweist oder abgebrochen wird. Geben Sie dann an, ob Sie möchten, dass die Warnungen als Popupmeldungen angezeigt werden.   
3. Wählen Sie **OK** aus.

## <a name="add-a-task-to-a-batch-job"></a>Hinzufügen einer Aufgabe zu einem Stapelverarbeitungsauftrag
1.  Wählen Sie auf der Seite **Batchaufträge** die Option **Aufgaben anzeigen** aus.
2.  Wählen Sie **Strg+N**, um eine Aufgabe zu erstellen.
3.  Geben Sie eine Beschreibung des Batchauftrags ein.
4.  Wählen Sie im Feld **Firmenkonten** die Unternehmensdatenbank aus, in der die Aufgabe ausgeführt werden soll.
5.  Wählen Sie im Feld **Klassenname** den Prozess aus, den die Aufgabe ausführen soll. 
6.  Wählen Sie bei Bedarf eine Stapelverarbeitungsgruppe für die Aufgabe aus.

    Client-Aufgaben müssen einer Batchgruppe zugewiesen werden. Sie werden automatisch der Standardbatchgruppe (auch bekannt als leere Batchgruppe) zugewiesen.

7.  Wählen Sie **STRG+S**, um die Aufgabe zu speichern.
8.  Um die ausgewählte Aufgabe von einer anderen Aufgabe im Stapel abhängig zu machen, wählen Sie das **Hat Bedingungen**-Raster, und führen Sie dann diese Schritte für jede Bedingung aus, die Sie definieren möchten:

    1. Wählen Sie **Strg+N**, um eine Bedingung zu erstellen.
    2. Wählen Sie die Aufgabenkennung der übergeordneten Aufgabe aus.
    3. Wählen Sie den Status aus, den die übergeordnete Aufgabe erreichen muss, damit die abhängige Aufgabe ausgeführt werden kann.
    4. Wählen Sie **STRG+S**, um die Bedingung zu speichern.

    Wurden mehrere Bedingungen definiert und *alle* Bedingungen müssen erfüllt sein, die zum Ausführen der abhängigen Aufgabe nötig sind, wählen Sie den Bedingungstyp **Alle** aus. Soll die abhängige Aufgabe ausgeführt werden, sobald eine *beliebige* Bedingung erfüllt ist, wählen Sie den Bedingungstyp **Beliebig** aus.

9.  Wählen Sie aus, wie Aufgabenfehler behandelt werden sollen. Sollen Fehler bei einer bestimmten Aufgabe ignoriert werden, aktivieren Sie für diese Aufgabe auf der Registerkarte **Allgemein** die Option **Aufgabenfehler ignorieren**. Ist diese Option ausgewählt, führt das Auftreten eines Fehlers bei dieser Aufgabe nicht dazu, dass für den gesamten Auftrag ein Fehler auftritt. Im Feld **Maximale Wiederholungsversuche** können Sie zudem angeben, wie oft ein Auftrag wiederholt werden soll, bevor er als fehlerhaft eingestuft wird. Als bewährte Methode empfehlen wir Ihnen, das **Maximale Wiederholungsversuche**-Feld auf einen Wert größer als **5** festzulegen.

    Weitere Informationen zu Batch-Wiederholungen finden Sie unter [Batch-Wiederholungen aktivieren](../retryable-batch.md).

## <a name="adjust-batch-job-status"></a>Status des Stapelverarbeitungsauftrags anpassen
1. Wechseln Sie zu **Systemverwaltung > Anfragen > Batchaufträge**.
2. Wählen Sie den entsprechenden Batchauftrag aus.
3. Klicken Sie im Aktivitätsbereich auf **Batchauftrag > Funktionen > Status ändern**.
4. Wählen Sie den entsprechenden Status aus.
    - **Zurückhalten**: Legen Sie für den Batchauftrag **Zurückhalten** fest, damit er vom Planungsprogramm für Batchaufträge zurückgehalten wird. Entspricht *Stopp*.
    - **Im Wartezustand**: Legen Sie für den Batchauftrag **Im Wartezustand** fest, damit er darauf wartet, vom Planungsprogramm fpr Batchaufträge aufgenommen zu werden. Entspricht *Los*.
5. Wählen Sie **OK** aus.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
