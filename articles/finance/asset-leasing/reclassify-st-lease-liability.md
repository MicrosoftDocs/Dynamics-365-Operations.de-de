---
title: Den kurzfristigen Anteil einer Leasingverbindlichkeit umgliedern
description: In diesem Thema wird erläutert, wie Sie einen monatlichen Journaleintrag erstellen, um einen Teil der Leasingverbindlichkeit als kurzfristig zu umzugliedern.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 21cf81ce84d91d88a800cd250fca8fd5a9c876e66f506cd366b8d61ed480ea7e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6720621"
---
# <a name="reclassify-the-short-term-portion-of-lease-liability"></a>Den kurzfristige Anteil der Leasingverbindlichkeit umgliedern

[!include [banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie einen monatlichen Journaleintrag erstellen, um einen Teil der Leasingverbindlichkeit als kurzfristig zu umzugliedern. Wenn der im Stapelverarbeitungsvorgang ausgewählte Zeitplan **Umgliederung der kurzfristigen Leasingverbindlichkeit** ist, wird ein Journaleintrag erstellt. Dieser Eintrag wird verwendet, um den aktuellen Teil der Leasingverbindlichkeit am letzten Tag des Monats zu buchen. Gleichzeitig wird ab dem ersten Tag des nächsten Monats eine Stornobuchung gebucht.

Der kurzfristige Teil der Leasingverbindlichkeit wird im Tilgungsplan für Verbindlichkeiten ausgewiesen. Wenn der Journaleintrag gebucht wird, wird die **Umgliederungserfassung für Verbindlichkeiten erstellt**-Spalte verfügbar, und die Erfassungs-ID wird ebenfalls in den Zeitplan eingetragen.

Führen Sie die folgenden Schritte aus, um den Journaleintrag für die kurzfristige Umgliederung von Verbindlichkeiten zu erstellen und zu buchen.

1. Gehen Sie zu **Anlagenleasing \> Periodisch \> Batch-Erfassungserstellung**.
2. Wählen Sie in dem **Batch-Erfassungserstellung**-Dialogfeld im **Zeitplan auswählen**-Feld **Umgliederung der kurzfristigen Leasingverbindlichkeit** aus.
3. Wählen Sie im Feld **Leasinggruppe** eine Leasinggruppe aus. Wählen Sie alternativ im **Buch-ID**-Feld die Buch-ID aus.
4. Aktivieren Sie den **Buchen**-Parameter. Wenn der Eintrag erstellt, aber nicht gebucht werden soll, lassen Sie diesen Parameter alternativ deaktiviert.
5. Wählen Sie **OK**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
