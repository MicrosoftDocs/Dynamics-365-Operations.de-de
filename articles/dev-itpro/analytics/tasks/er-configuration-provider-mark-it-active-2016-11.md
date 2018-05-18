--- 
title: "Konfigurationsanbieter erstellen und als aktiv für elektronische Berichterstellung (ER) markieren"
description: "In den folgenden Schritten wird erläutert, wie ein Benutzer, der der Systemadministratorrolle oder der Rolle \"Entwickler für elektronische Berichterstellung\" zugewiesen ist, einen Konfigurationsanbieter für elektronische Berichterstellung (ER) erstellen kann."
author: NickSelin
manager: AnnBe
ms.date: 11/01/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 95d5bf26c22238753586cf4a7aaf5c26f061a705
ms.openlocfilehash: 018aee917c13f576759ebd812d31cbc9d83e2d1a
ms.contentlocale: de-de
ms.lasthandoff: 02/23/2018

---
# <a name="create-a-configuration-provider-and-mark-it-as-active-for-electronic-reporting-er"></a>Konfigurationsanbieter erstellen und als aktiv für elektronische Berichterstellung (ER) markieren

[!include [task guide banner](../../includes/task-guide-banner.md)]

In den folgenden Schritten wird erläutert, wie ein Benutzer, der der Systemadministratorrolle oder der Rolle "Entwickler für elektronische Berichterstellung" zugewiesen ist, einen Konfigurationsanbieter für elektronische Berichterstellung (ER) erstellen kann. Jede Konfiguration für elektronische Berichterstellung verweist auf den Anbieter als Autor der Konfiguration. In diesem Beispiel erstellen Sie eine Konfiguration für das Beispielunternehmen, Litware, Inc. Diese Schritte können in einem beliebigen Unternehmen ausgeführt werden, da ER-Konfigurationsanbieter unter allen Unternehmen geteilt werden.


## <a name="create-a-provider"></a>Anbieter erstellen
1. Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.
2. Klicken Sie auf "Konfigurationsanbieter".
3. Klicken Sie auf "Neu".
    * Ein Anbieterdatensatz ist nach Name und URL eindeutig. Überprüfen Sie den Inhalt dieser Seite und lassen Sie diese Prozedur aus, wenn bereits ein `http://www.litware.com` für Litware, Inc. besteht.  
4. Geben Sie im Feld "Name" "Litware, Inc." ein.
    * Litware, Inc.  
5. Geben Sie im Feld "Internetadresse" `http://www.litware.com` ein.
6. Klicken Sie auf "Speichern".
7. Schließen Sie die Seite.

## <a name="select-as-an-active-provider"></a>Als aktiven Anbieter auswählen
1. Wählen Sie den "Litware, Inc."- Anbieter.
2. Klicken Sie auf "Als aktiv festlegen"


