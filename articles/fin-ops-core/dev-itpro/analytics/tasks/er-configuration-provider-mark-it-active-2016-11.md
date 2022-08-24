---
title: Erstellen von Konfigurationsanbietern und Markieren als aktiv
description: In diesem Artikel wird erläutert, wie Benutzer, die der Systemadministratorrolle oder der Rolle „Entwickler für elektronische Berichterstellung“ zugewiesen sind, einen Konfigurationsanbieter erstellen können.
author: kfend
ms.date: 07/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ERWorkspace, ERVendorPart, ERVendorTable
ms.openlocfilehash: db5226720a4e0c0f167921a972429c0a5ecdd2e9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267812"
---
# <a name="create-configuration-providers-and-mark-them-as-active"></a>Erstellen von Konfigurationsanbietern und Markieren als aktiv

[!include [banner](../../includes/banner.md)]

In diesem Artikel wird erläutert, wie Benutzer, die der Systemadministratorrolle oder der Rolle „Entwickler für elektronische Berichterstellung“ zugewiesen sind, einen Konfigurationsanbieter für elektronische Berichterstellung (EB) erstellen können. Jede Konfiguration für elektronische Berichterstellung verweist auf den Anbieter als Autor der Konfiguration. In diesem Beispiel erstellen Sie eine Konfiguration für das Beispielunternehmen, Litware, Inc. Diese Schritte können in einem beliebigen Unternehmen ausgeführt werden, da ER-Konfigurationsanbieter unter allen Unternehmen geteilt werden.

## <a name="create-a-provider"></a>Anbieter erstellen
1. Wechseln Sie zum **Navigationsbereich** in der oberen linken Ecke und wählen Sie **Organisationsverwaltung** aus.
2. Wechseln Sie zu **Arbeitsbereiche > Elektronische Berichterstellung**.
3. Wechseln Sie zu **Zugehörige Verknüpfungen > Konfigurationsanbieter**.
4. Wählen Sie **Neu** aus.
    - Ein Anbieterdatensatz ist nach Name und URL eindeutig. Überprüfen Sie den Inhalt dieser Seite und lassen Sie diese Prozedur aus, wenn bereits ein Datensatz für Litware, Inc. (https://www.litware.com) besteht.  
5. Geben Sie im Feld „Name“ „`Litware, Inc.`“ ein.
6. Geben Sie im Feld „Internetadresse” „`https://www.litware.com`” ein.
7. Wählen Sie **Speichern**.
8. Schließen Sie die Seite.

## <a name="select-as-an-active-provider"></a>Als aktiven Anbieter auswählen
1. Wählen Sie den "Litware, Inc."- Anbieter.
2. Wählen Sie **Als aktiv festlegen**.

![Elektronische Berichterstellung – Seite „Arbeitsbereich“.](../media/GER-Task-ActiveProvider-1.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
