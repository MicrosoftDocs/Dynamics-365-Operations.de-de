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
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fa86d408727ecf2127308070fda592ff6a1fccf4
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982453"
---
# <a name="import-users-in-bulk"></a>Massenimport von Benutzern

[!include [banner](../../includes/banner.md)]

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

