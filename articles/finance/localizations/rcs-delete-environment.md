---
title: Regulatory Configuration Service (RCS) – Eine RCS-Umgebung löschen
description: In diesem Artikel wird erklärt, wie ein Systemadministrator des Regulatory Configuration Service (RCS) eine RCS-Umgebung und die zugehörigen Daten löschen kann.
author: kfend
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, System Admin
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-01-01
ms.dyn365.ops.version: AX 10.0.15
ms.custom: 97423
ms.assetid: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Global
ms.openlocfilehash: bdcb6820ead72fce0f89bf80cc5e474cb3942724
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277238"
---
# <a name="regulatory-configuration-service-rcs---delete-an-rcs-environment"></a>Regulatory Configuration Service (RCS) – Eine RCS-Umgebung löschen

[!include [banner](../includes/banner.md)]

In diesem Artikel wird erklärt, wie ein Systemadministrator des Regulatory Configuration Service (RCS) eine RCS-Umgebung und die zugehörigen Daten löschen kann.

Bevor Sie das Verfahren in diesem Artikel ausführen können, müssen die folgenden Voraussetzungen erfüllt sein:

- Sie müssen über die Rolle **System Admin** verfügen, die Ihnen für die RCS-Umgebung zugewiesen wurde.
- Der Rolle **System Admin** muss die Rolle **RCSDeleteEnvironmentDuty** zugewiesen sein.

## <a name="delete-an-rcs-environment"></a>Löschen einer RCS Umgebung

1. Öffnen Sie RCS und wählen Sie die Kachel **Elektronisches Berichtswesen** des Arbeitsbereichs.
2. Wählen Sie im Abschnitt **Verwandte Links** die Rolle **RCS-Umgebung löschen**.

    ![Link RCS Umgebung im Abschnitt „Zugehörige Links“ löschen.](media/01_RCS-Delete-Environ-Related-Link.PNG)

3. Überprüfen Sie im angezeigten Dialogfeld die Nachrichten über den Umfang des Löschens der Umgebung.

    ![Meldungen im Dialogfeld „RCS-Umgebung löschen“.](media/01_RCS-Delete-Environ-Msg_noGUID.PNG)

    > [!IMPORTANT]
    > Das Löschen einer RCS-Umgebung kann nicht rückgängig gemacht werden.
    >
    > Der Vorgang löscht die ausgewählte RCS-Umgebung und alle zugehörigen Daten, einschließlich Funktionen und Konfigurationen, die im globalen Repository gespeichert sind. Funktionen und Konfigurationen, die mit anderen Organisationen geteilt werden, werden nicht geteilt und gelöscht, wenn sie keine Abhängigkeiten haben. Funktionen und Konfigurationen, die Abhängigkeiten haben, werden als abgekündigt markiert.

4. Geben Sie in das vorgesehene Feld den global eindeutigen Bezeichner (GUID) der RCS-Umgebung ein, um zu bestätigen, dass Sie sie löschen möchten. Die GUID der Umgebung ist in der Nachricht über das Löschen enthalten.
5. Wählen Sie **Umgebung löschen**.
    
Ihre RCS Umgebung und alle zugehörigen Daten werden nun gelöscht.

> [!IMPORTANT]
> Nachdem Sie eine RCS Umgebung gelöscht haben, gibt es keine Möglichkeit, die Daten wiederherzustellen. Eine neue RCS-Umgebung kann in jeder verfügbaren RCS-Region erstellt werden.
