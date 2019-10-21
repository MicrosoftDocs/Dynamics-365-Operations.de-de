---
title: Importbenutzer in großer Stückzahl
description: Diese Prozedur kann von Systemadministratoren verwendet werden, um viele Benutzer aus Azure Active Directory zu importieren.
author: maertenm
manager: AnnBe
ms.date: 07/07/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cb2c316465f8c6964a562e92ce0a2233b37d38fe
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180897"
---
# <a name="import-users-in-bulk"></a>Massenimport von Benutzern

[!include [task guide banner](../../includes/task-guide-banner.md)]

Diese Prozedur kann von Systemadministratoren verwendet werden, um viele Benutzer aus Azure Active Directory zu importieren.


## <a name="run-as-a-batch-job"></a>Als Batchauftrag ausführen
1. Wechseln Sie zu "Systemverwaltung" > "Benutzer" > "Benutzer".
2. Stapelimportpfade anklicken.
3. Erweitern Sie den Abschnitt "Ausführen im Hintergrund".
4. Wählen Sie "Ja" im Feld "Stapelverarbeitung" aus.
5. «»Geben Sie im Feld Elementbeschreibung einen Wert ein.
6. Geben Sie im Feld "Chargengruppenfeld" einen Wert ein oder wählen Sie einen Wert aus.
    * Dieser Schritt ist optional.  
7. Wählen Sie "Ja" im Feld "Privat" aus.
    * Dieser Schritt ist optional.  
8. Wählen Sie "Ja" im Feld "Kritische Aufgabe".
    * Dieser Schritt ist optional.  
9. Wählen Sie im Feld "Kategorie überwachen" eine Option aus.
10. Klicken Sie auf "OK".

## <a name="run-in-a-sandbox-environment"></a>Eine Sandkastenumgebung ausführen
1. Stapelimportpfade anklicken.
2. Klicken Sie auf "OK".

