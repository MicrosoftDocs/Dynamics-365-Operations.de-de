--- 
title: Erstellen eines Stapelverarbeitungsauftrags
description: "Bei einem Batchauftrag handelt es sich um eine Gruppe von Aufgaben, die zur automatischen Verarbeitung an eine Anwendungsobjektserver-Instanz (AOS) übermittelt werden."
author: maertenm
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: ca2b755406fb7fce4b11457be86f6a8685004438
ms.contentlocale: de-de
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-batch-job"></a>Erstellen eines Stapelverarbeitungsauftrags

[!include[task guide banner](../../includes/task-guide-banner.md)]

Bei einem Batchauftrag handelt es sich um eine Gruppe von Aufgaben, die zur automatischen Verarbeitung an eine Anwendungsobjektserver-Instanz (AOS) übermittelt werden. Stapelverarbeitungsaufträge werden unter Verwendung der Sicherheitsanmeldeinformationen des Benutzers ausgeführt, von dem der Auftrag erstellt wurde. Verwenden Sie die folgende Prozedur, um einen Batchauftrag zu erstellen. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.


## <a name="create-the-batch-job"></a>Den Batchauftrag erstellen
1. Wechseln Sie zu "Systemverwaltung" > "Anfragen" > "Batchaufträge".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Stellenbeschreibung" einen Wert ein.
4. Geben Sie im Feld "Geplantes Startdatum/-uhrzeit" ein Datum und eine Uhrzeit ein.
5. Klicken Sie auf "Speichern".

## <a name="create-a-recurrence"></a>Eine Wiederholung erstellen
1. Klicken Sie im Aktivitätsbereich auf "Batchauftrag".
2. Klicken Sie auf "Wiederholung".
    * Verwenden Sie diese Optionen, um einen Bereich und ein Muster für die Wiederholung einzugeben.  
3. Klicken Sie auf "OK".

## <a name="add-alerts"></a>Warnungen hinzufügen
1. Klicken Sie im Aktivitätsbereich auf "Batchauftrag".
2. Klicken Sie auf "Warnungen".
    * Geben Sie an, ob Sie möchten, dass Warnmeldungen gesendet werden, wenn der Batchauftrag endet, einen Fehler aufweist oder abgebrochen wird. Geben Sie dann an, ob Sie möchten, dass die Warnungen als Popupmeldungen angezeigt werden.   
3. Klicken Sie auf "OK".


