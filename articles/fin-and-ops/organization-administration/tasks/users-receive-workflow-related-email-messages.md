---
title: Ermöglichen Sie es Benutzern, workflowbezogene E-Mail-Nachrichten zu erhalten.
description: Sie können das System konfigurieren, um E-Mail-Nachrichten an Benutzer zu senden, wenn workflowbezogene Ereignisse auftreten.
author: jasongre
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysUserSetup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6800d02878123388611d35760123d0215e9d539f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "344592"
---
# <a name="enable-users-to-receive-workflow-related-email-messages"></a>Ermöglichen Sie es Benutzern, workflowbezogene E-Mail-Nachrichten zu erhalten.

[!include [task guide banner](../../includes/task-guide-banner.md)]

Sie können das System konfigurieren, um E-Mail-Nachrichten an Benutzer zu senden, wenn workflowbezogene Ereignisse auftreten. So können E-Mail-Nachrichten an Benutzer gesendet werden, wenn ihnen Dokumente zur Genehmigung zugewiesen sind. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.

1. Wechseln Sie zu "Systemverwaltung" > "Benutzer" > "Benutzer".
2. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
3. Klicken Sie auf "Benutzeroptionen".
4. Klicken Sie auf die Registerkarte „Workflow”.
    * Überprüfen Sie, ob der Bereich „Benachrichtigungen” erweitert ist.     Im Abschnitt „Benachrichtigungen” geben Sie an, wie der Benutzer über workflowbezogene Ereignisse informiert werden soll.  
5. Wählen Sie im Feld Positionsartikelworkflow-Benachrichtigungstyp eine Option aus.
    * Gruppiert – Benachrichtigungen für Positionsartikel werden in eine einzige E-Mail-Nachricht gruppiert.    Einzeln - eine E-Mail wird für jeden Positionsartikel übermittelt.  
    * Wenn der Benutzer Benachrichtigungen im Microsoft -Client erhalten soll, aktivieren Sie das Kontrollkästchen „Benachrichtigungen per E-Mail senden”.  
6. Klicken Sie auf "Speichern".
7. Schließen Sie die Seite.

