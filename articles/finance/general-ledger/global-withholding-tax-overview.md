---
title: Globale Quellensteuer
description: Dieses Thema enthält Informationen zur globalen Quellensteuerfunktionalität und zu deren Einrichtung. Die globale Quellensteuerfunktionalität wurde für Kreditoren- und Debitorenbuchungen erweitert, sodass die Quellensteuer auf Artikelebene berechnet wird.
author: roschlom
ms.date: 01/12/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "15721"
- intro-internal
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: 7a3bb3c8766c7dd591f66a663d8be17769bb7d53
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2022
ms.locfileid: "7986175"
---
# <a name="global-withholding-tax"></a>Globale Quellensteuer

[!include [banner](../includes/banner.md)]

Dieses Thema enthält Informationen zur globalen Quellensteuerfunktionalität und erläutert deren Einrichtung. Die neue Funktionalität ist ab der Version 10.0.17 und höher verfügbar.

Die globale Quellensteuerfunktionalität wurde für Kreditoren- und Debitorenbuchungen erweitert, sodass die Quellensteuer auf Artikelebene berechnet wird. Der Saldo des Quellensteuerkontos aus Kaufbuchungen kann durch Ausführen des Einzelvorgang zur Quellensteuerzahlung gegen das Quellensteuerverrechnungskonto ausgeglichen werden.

> [!NOTE]
> Die globale Quellensteuer unterstützt nicht die Funktion **Belastungen verwalten** auf den Seiten „Bestellung“, „Kreditorenrechnung“ und „Auftrag“.

## <a name="turn-on-global-withholding-tax"></a>Globale Quellensteuer aktivieren

1. Wählen Sie im Arbeitsbereich **Funktionsverwaltung** die Option **Globale Quellensteuer** und anschließend **Jetzt aktivieren** aus.
2. Rufen Sie **Steuer \> Einrichtung \> Parameter \> Hauptbuchparameter** auf. Setzen Sie anschließend auf der Registerkarte **Quellensteuer** die Option **Globale Quellensteuer aktivieren** auf **Ja**.
3. Wählen Sie **Speichern** aus.
4. Aktualisieren Sie die Seite in Ihrem Webbrowser.

> [!NOTE]
> Die globale Quellensteuerfunktionalität kann nicht für Länder/Regionen aktiviert werden, in denen bereits lokalisierte Quellensteuerlösungen existieren. Diese Gebiete umfassen Indien, Brasilien, Thailand, Saudi-Arabien, Irland, Großbritannien und die Vereinigten Staaten, sind aber nicht auf diese beschränkt.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
