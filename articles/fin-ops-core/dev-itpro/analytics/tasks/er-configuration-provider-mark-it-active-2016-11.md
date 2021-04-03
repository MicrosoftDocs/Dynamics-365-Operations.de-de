---
title: Erstellen von Konfigurationsanbietern und Markieren als aktiv
description: In diesem Thema wird erläutert, wie ein Benutzer, der der Systemadministratorrolle oder der Rolle „Entwickler für elektronische Berichterstellung“ zugewiesen ist, einen Konfigurationsanbieter erstellen kann.
author: NickSelin
manager: AnnBe
ms.date: 07/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERVendorTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 11ff1d531b0467cf75ec98b092fe6010f4fa95c0
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569786"
---
# <a name="create-configuration-providers-and-mark-them-as-active"></a>Erstellen von Konfigurationsanbietern und Markieren als aktiv

[!include [banner](../../includes/banner.md)]

In diesem Thema wird erläutert, wie ein Benutzer, der der Systemadministratorrolle oder der Rolle „Entwickler für elektronische Berichterstellung“ zugewiesen ist, einen Konfigurationsanbieter für elektronische Berichterstellung (ER) erstellen kann. Jede Konfiguration für elektronische Berichterstellung verweist auf den Anbieter als Autor der Konfiguration. In diesem Beispiel erstellen Sie eine Konfiguration für das Beispielunternehmen, Litware, Inc. Diese Schritte können in einem beliebigen Unternehmen ausgeführt werden, da ER-Konfigurationsanbieter unter allen Unternehmen geteilt werden.

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

![Elektronische Berichterstellung – Seite „Arbeitsbereich“](../media/GER-Task-ActiveProvider-1.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]