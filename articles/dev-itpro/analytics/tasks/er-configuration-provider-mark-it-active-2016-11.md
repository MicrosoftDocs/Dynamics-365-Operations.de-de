---
title: Konfigurationsanbieter erstellen und sie als aktiv markieren
description: In den folgenden Schritten wird erläutert, wie ein Benutzer, der der Systemadministratorrolle oder der Rolle "Entwickler für elektronische Berichterstellung" zugewiesen ist, einen Konfigurationsanbieter für elektronische Berichterstellung (ER) erstellen kann.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERVendorTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a4b1cd7a02cdf4c650af50199f4425eb53cef0a8
ms.sourcegitcommit: 574d4dda83dcab94728a3d35fc53ee7e2b90feb0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/22/2019
ms.locfileid: "1595394"
---
# <a name="create-configuration-providers-and-mark-them-as-active"></a>Konfigurationsanbieter erstellen und sie als aktiv markieren

[!include [task guide banner](../../includes/task-guide-banner.md)]

In den folgenden Schritten wird erläutert, wie ein Benutzer, der der Systemadministratorrolle oder der Rolle "Entwickler für elektronische Berichterstellung" zugewiesen ist, einen Konfigurationsanbieter für elektronische Berichterstellung (ER) erstellen kann. Jede Konfiguration für elektronische Berichterstellung verweist auf den Anbieter als Autor der Konfiguration. In diesem Beispiel erstellen Sie eine Konfiguration für das Beispielunternehmen, Litware, Inc. Diese Schritte können in einem beliebigen Unternehmen ausgeführt werden, da ER-Konfigurationsanbieter unter allen Unternehmen geteilt werden.


## <a name="create-a-provider"></a>Anbieter erstellen
1. Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.
2. Klicken Sie auf "Konfigurationsanbieter".
3. Klicken Sie auf "Neu".
    * Ein Anbieterdatensatz ist nach Name und URL eindeutig. Überprüfen Sie den Inhalt dieser Seite und lassen Sie diese Prozedur aus, wenn bereits ein Datensatz für Litware, Inc. (https://www.litware.com) besteht.  
4. Geben Sie im Feld "Name" "Litware, Inc." ein.
    * Litware, Inc.  
5. Geben Sie im Feld „Internetadresse” „https://www.litware.com” ein.
    * https://www.litware.com  
6. Klicken Sie auf "Speichern".
7. Schließen Sie die Seite.

## <a name="select-as-an-active-provider"></a>Als aktiven Anbieter auswählen
1. Wählen Sie den "Litware, Inc."- Anbieter.
2. Klicken Sie auf "Als aktiv festlegen"

