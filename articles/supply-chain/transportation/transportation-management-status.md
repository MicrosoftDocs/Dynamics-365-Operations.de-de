---
title: Status der Transportverwaltung
description: In diesem Artikel wird erklärt, wie Sie einen Transportstatus erstellen und diesen Status einem Spediteur-Status zuordnen.
author: Weijiesa
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 9b20570a87a9f8969ca6dcf898176fd40f88eeca
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897370"
---
# <a name="transportation-management-statuses"></a>Status der Transportverwaltung

[!include [banner](../includes/banner.md)]

Legen Sie Mastercodes für Transportstatus fest, um Codes zu interpretieren, die von Ihren Spediteuren bereitgestellt werden. So können Sie mit Spediteuren zusammenarbeiten, um einen Status bereitzustellen. Der Transportstatus, den Sie für einen Transport-Stammstatuscode bereitstellen, kann Ihnen helfen, den Status einer Ladung, einer Sendung oder eines Containers zu verfolgen. Der spezifische Transportstatus für eine Ladung, eine Sendung oder einen Container kann nur durch Datenintegration und nicht manuell über die Benutzeroberfläche aktualisiert werden.

## <a name="create-a-transportation-status"></a>Erzeugen eines Transportstatus

Um einen Transportstatus zu erstellen, gehen Sie wie folgt vor:

1. Gehen Sie zu **Transportverwaltung \> Einrichten \> Transportstatus-Stämme**.
1. Wählen Sie **Neu**, um einen Transportstatus-Stamm zu erstellen.
1. Geben Sie in das Feld **Transportstatus-Stamm** einen eindeutigen Code für den Transportstatus ein.
1. Wählen Sie im Feld **Transportart** entweder *Spediteur* oder *Hub* als Transportart.
1. Geben Sie einen Namen und einen Transportstatus ein.
1. Schließen Sie die Seite.

## <a name="map-a-transportation-status-to-a-carrier-status"></a>Zuordnen eines Transportstatus zu einem Spediteur-Status

Um einen Transportstatus einem Spediteur-Status zuzuordnen, gehen Sie wie folgt vor:

1. Gehen Sie zu **Transportverwaltung \> Einrichten \> Spediteure \> Spediteur-Transportstatus**.
1. Wählen Sie **Neu**, um einen Code eines Spediteurs einem Transportstatus-Stammcode zuzuordnen.
1. Wählen Sie die eindeutige ID für den Spediteur und den Speditionsdienst.
1. Wählen Sie den Transportstatus-Code, den Sie dem Code des gewählten Spediteurs zuordnen wollen.
1. Geben Sie den externen Code ein, der von dem Spediteur verwendet wird.
1. Schließen Sie die Seite.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]