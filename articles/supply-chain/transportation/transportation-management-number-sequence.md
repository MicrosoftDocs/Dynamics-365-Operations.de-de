---
title: Transportverwaltung Sequenznummer
description: Dieses Thema beschreibt, wie Sie Nummernfolgen für die Transportverwaltung festlegen.
author: Henrikan
manager: tfehr
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 2c3f087ac76412cd2dce93dcb31b796ce2cb3bc4
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/29/2020
ms.locfileid: "4429167"
---
# <a name="transportation-management-number-sequence"></a>Transportverwaltung Sequenznummer

[!include [banner](../includes/banner.md)]

Verwenden Sie die Seite **Nummernfolgen** im Modul Transportverwaltung, um verschiedene Pro-Nummern festzulegen. Pro-Nummern werden von Spediteuren verwendet, um den Fortschritt der einzelnen Sendungen zu organisieren und zu verfolgen.

## <a name="create-a-number-sequence-for-a-pro-number"></a>Erstellen einer Nummernfolge für eine Pro-Nummer

Um eine Sequenz für eine Pro-Nummer zu erstellen, gehen Sie wie folgt vor:

1. Gehen Sie zu **Transportverwaltung \> Einrichten \> Spediteure \> Nummernfolgen**.
1. Wählen Sie **Neu**, um eine neue Sequenz für eine Nummer zu erstellen.
1. Geben Sie eine eindeutige ID und einen beschreibenden Namen für die Nummernfolge ein.
1. Im Feld **Nummernfolge-Typ** ist *Pro-Nummer* die einzige Option.
1. Im Feld **Prüfziffer** ist *Prüfziffer* die einzige Option und ist als generische Engine festgelegt.
1. Geben Sie auf dem Inforegister **Sequenz** Informationen über die Sequenz an.
1. Schließen Sie die Seite.

## <a name="link-a-number-sequence-to-a-shipping-carrier"></a>Verknüpfen einer Sequenz mit einem Spediteur

Um eine Sequenz mit einem Spediteur zu verknüpfen, gehen Sie wie folgt vor:

1. Wechseln Sie zu **Transportverwaltung \> Einstellungen \> Spediteure \> Spediteure**.
1. Wählen Sie einen Spediteur aus.
1. Wählen Sie **Bearbeiten** aus.
1. Wählen Sie auf der Inforegister-Registerkarte **Übersicht** eine Option im Feld **Pro Nummernfolge**.
1. Schließen Sie die Seite.
