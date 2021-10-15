---
title: Belastungen für Intercompany-Aufträge einrichten
description: In diesem Thema wird erläutert, wie Sie Belastungen für Intercompany-Aufträge einrichten.
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: CustTable, VendTable, EcoResProductListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 3786df5ce185fa8433d7c69bed5bef09b4983b8b
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548291"
---
# <a name="set-up-charges-on-intercompany-orders"></a>Belastungen für Intercompany-Aufträge einrichten

[!include [banner](../../includes/banner.md)]

Sie können Belastungen einrichten, die Intercompany-Aufträgen hinzugefügt werden. Wenn einem Intercompany-Auftrag eine Belastung hinzugefügt wird, wird diese automatisch mit der Intercompany-Bestellung synchronisiert. Dies funktioniert in beide Richtungen, also vom Intercompany-Auftrag zur Intercompany-Bestellung und umgekehrt.

Mit Belastungen können Sie einem Intercompany-Auftrag auch einen Gewinn hinzuaddieren, indem Sie die Belastungen als „Intercompany-Prozentsatz“ definieren.

Beim Einrichten von Belastungen, die auf Intercompany-Aufträge angewendet werden sollen, aktivieren Sie die Berechnung des internen Gewinns eines Intercompany-Auftrags aus dem Nettobetrag des Originalauftrags. Diese Vorgehensweise ist denkbar, wenn der Verkaufspreis des Intercompany-Kreditors gleich dem Einstandspreis ist. In der folgenden Prozedur wird erläutert, wie Belastungen für Intercompany-Debitoren eingerichtet werden. Sie können dasselbe Verfahren für Kreditoren verwenden.

1. Wechseln Sie zu **Debitoren \> Einrichtung \> Belastungen \> Kunden-Belastungsgruppen**.
1. Erstellen Sie eine Belastungsgruppe.
1. Gehen Sie zu **Debitorenkonten \> Debitoren \> Alle Debitoren**. Wählen Sie einen Debitorenkonto-Link aus. Wählen Sie im Aktionsbereich die Registerkarte **Debitor** und dann das Inforegister **Auftrag** aus.
1. Wählen Sie im Aktionsbereich **Bearbeiten** aus, um das Feld zu bearbeiten. Wählen Sie im Feld **Belastungsgruppe** die Intercompany-Belastungsgruppe aus, die Sie in Schritt 2 eingerichtet haben.
1. Wechseln Sie zu **Debitoren \> Einrichtung \> Belastungen \> Auto-Belastungen** aus.
1. Richten Sie die Belastungen ein, indem Sie die relevanten Felder ausfüllen.
1. Wählen Sie im Feld **Debitorenrelation** die Intercompany-Belastungsgruppe aus, die Sie in Schritt 2 eingerichtet haben.
1. Wählen Sie auf dem Inforegister **Positionen** im Feld **Kategorie** **Intercompany-Prozentsatz** aus.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
