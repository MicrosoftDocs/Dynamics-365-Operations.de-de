---
title: Ermöglichen Sie es Benutzern, workflowbezogene E-Mail-Nachrichten zu erhalten.
description: Sie können das System konfigurieren, um E-Mail-Nachrichten an Benutzer zu senden, wenn workflowbezogene Ereignisse auftreten.
author: jasongre
manager: AnnBe
ms.date: 07/01/2019
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
ms.openlocfilehash: 5e08f95ef6d263ee0f8c0a94b258c8a2795786bc
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916391"
---
# <a name="enable-users-to-receive-workflow-related-email-messages"></a>Ermöglichen Sie es Benutzern, workflowbezogene E-Mail-Nachrichten zu erhalten.

[!include [task guide banner](../../includes/task-guide-banner.md)]

Sie können das System konfigurieren, um E-Mail-Nachrichten an Benutzer zu senden, wenn workflowbezogene Ereignisse auftreten. So können E-Mail-Nachrichten an Benutzer gesendet werden, wenn ihnen Dokumente zur Genehmigung zugewiesen sind. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.

1. Wechseln Sie zu **Navigationsbereich > Module > Systemverwaltung > Benutzer > Benutzer**.
2. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
3. Klicken Sie im **Aktionsbereich** auf **Benutzeroptionen**.
4. Klicken Sie auf die Registerkarte **Workflow**. Stellen Sie sicher, dass der Abschnitt **Benachrichtigungen** erweitert ist. Im Abschnitt **Benachrichtigungen** können Sie festlegen, wie der Benutzer über workflowbezogene Ereignisse informiert werden soll.  
5. Wählen Sie im Feld **Positionsartikelworkflow-Benachrichtigungstyp** eine Option aus.
    - Gruppiert – Benachrichtigungen für Positionsartikel werden in eine einzige E-Mail-Nachricht gruppiert.
    - Einzeln - eine E-Mail wird für jeden Positionsartikel übermittelt.  
    - Wenn der Benutzer im Client Benachrichtigungen erhalten soll, aktivieren Sie das Kontrollkästchen **Benachrichtigungen in E-Mail senden**.  
6. Klicken Sie auf **Speichern**.
7. Schließen Sie die Seite.

