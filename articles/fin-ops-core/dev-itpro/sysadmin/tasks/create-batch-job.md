---
title: Erstellen eines Stapelverarbeitungsauftrags
description: Bei einem Batchauftrag handelt es sich um eine Gruppe von Aufgaben, die zur automatischen Verarbeitung an eine Anwendungsobjektserver-Instanz (AOS) übermittelt werden.
author: maertenm
manager: AnnBe
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BatchJob, SysRecurrence, BatchAlerts
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 27541c84a40fe9b7e7705162e06167ad4f7e4ed9
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191384"
---
# <a name="create-a-batch-job"></a>Erstellen eines Stapelverarbeitungsauftrags

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bei einem Batchauftrag handelt es sich um eine Gruppe von Aufgaben, die zur automatischen Verarbeitung an eine Anwendungsobjektserver-Instanz (AOS) übermittelt werden. Stapelverarbeitungsaufträge werden unter Verwendung der Sicherheitsanmeldeinformationen des Benutzers ausgeführt, von dem der Auftrag erstellt wurde. Verwenden Sie die folgende Prozedur, um einen Batchauftrag zu erstellen. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.


## <a name="create-the-batch-job"></a>Den Batchauftrag erstellen
1. Wechseln Sie zu **Navigationsbereich > Module > Systemverwaltung > Anfragen > Batchauftrag**.
2. Klicken Sie auf **Neu**.
3. Geben Sie im Feld **Stellenbeschreibung** einen Wert ein.
4. Geben Sie im Feld **Geplantes Startdatum/-uhrzeit** ein Datum und eine Uhrzeit ein.
5. Klicken Sie auf **Speichern**.

## <a name="create-a-recurrence"></a>Eine Wiederholung erstellen
1. Klicken Sie im Aktivitätsbereich auf **Batchauftrag**.
2. Klicken Sie auf **Wiederholung**. Verwenden Sie diese Optionen, um einen Bereich und ein Muster für die Wiederholung einzugeben.  
3. Klicken Sie auf **OK**.

## <a name="add-alerts"></a>Warnungen hinzufügen
1. Klicken Sie im Aktivitätsbereich auf **Batchauftrag**.
2. Klicken Sie auf **Warnungen**. Geben Sie an, ob Sie möchten, dass Warnmeldungen gesendet werden, wenn der Batchauftrag endet, einen Fehler aufweist oder abgebrochen wird. Geben Sie dann an, ob Sie möchten, dass die Warnungen als Popupmeldungen angezeigt werden.   
3. Klicken Sie auf **OK**.

## <a name="adjust-batch-job-status"></a>Status des Stapelverarbeitungsauftrags anpassen
1. Wechseln Sie zu **Systemverwaltung > Anfragen > Batchaufträge**.
2. Wählen Sie den entsprechenden Batchauftrag aus.
3. Klicken Sie im Aktivitätsbereich auf **Batchauftrag > Funktionen > Status ändern**.
4. Wählen Sie den entsprechenden Status aus.
    - **Zurückhalten**: Legen Sie für den Batchauftrag **Zurückhalten** fest, damit er vom Planungsprogramm für Batchaufträge zurückgehalten wird. Entspricht *Stopp*.
    - **Im Wartezustand**: Legen Sie für den Batchauftrag **Im Wartezustand** fest, damit er darauf wartet, vom Planungsprogramm fpr Batchaufträge aufgenommen zu werden. Entspricht *Los*.
5. Klicken Sie auf **OK**.