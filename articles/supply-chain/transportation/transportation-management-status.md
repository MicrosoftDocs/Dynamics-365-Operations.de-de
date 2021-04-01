---
title: Status der Transportverwaltung
description: In diesem Thema wird erklärt, wie Sie einen Transportstatus erstellen und diesen Status einem Spediteur-Status zuordnen.
author: Henrikan
manager: tfehr
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: fb0d98729046330037f96ab7e13a1bf897e35a1e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233342"
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