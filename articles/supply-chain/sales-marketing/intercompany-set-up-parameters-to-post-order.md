---
title: Parameter zum Buchen eines Intercompany-Auftrags einrichten
description: In diesem Thema wird erläutert, wie Sie Parameter zum Buchen eines Intercompany-Aufträge einrichten.
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: c728f2f491948ae1c8550396ba4d72f76f46fe85
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548284"
---
# <a name="set-up-parameters-to-post-an-intercompany-order"></a>Parameter zum Buchen eines Intercompany-Auftrags einrichten

[!include [banner](../../includes/banner.md)]

Wenn eine Intercompany-Debitorenrechnung gebucht wird, können Sie diese so einrichten, dass sowohl die Intercompany-Bestellung als auch die Debitorenrechnung für den Originalauftrag automatisch gebucht werden.

> [!NOTE]
> Richten Sie vor dem Ausführen dieser Prozedur in der Druckverwaltung der Organisation den richtigen Rechnungsdrucker ein. Dadurch wird sichergestellt, dass die Rechnung für den ursprünglichen Auftrag auf dem richtigen Drucker ausgedruckt wird.

Hierfür müssen Sie die folgenden Parameter einrichten:

1. Wechseln Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**. Wählen Sie den Auftrag aus, mit dem Sie arbeiten möchten.
1. Wählen Sie im Auftrag im Aktivitätsbereich die Option **Kopfzeilenansicht** und dann das Inforegister **Intercompany-Einstellungen** aus, um es zu öffnen.
1. Wechseln Sie zum Aktivitätsbereich auf der Registerkarte **Auftrag**, und wählen Sie anschließend **Bearbeiten** aus.
1. Wechseln Sie zum Inforegister **Intercompany-Einstellungen**, und wählen Sie **Direktlieferung** aus, um die Direktlieferung innerhalb der Intercompany-Kette (alle Aufträge) zu aktivieren.
1. Wählen Sie **Speichern** aus, um den Auftrag mit der neuen Einstellung zu speichern. Wählen Sie anschließend **Schließen** aus, um den Auftrag zu schließen.
1. Gehen Sie zu **Beschaffung \> Kreditoren \> Alle Kreditoren**. Wählen Sie auf der Registerkarte **Allgemein** die Option **Intercompany** aus.
1. Wählen Sie auf der Seite **Intercompany** den Link **Auftragsrichtlinien** aus. Wählen Sie in der Feldgruppe **Intercompany-Bestellung (Direktlieferung)** die Option **Rechnung automatisch buchen** aus, und entfernen Sie das Häkchen im Feld **Rechnung automatisch drucken**.
1. Wählen Sie in der Feldgruppe **Originalauftrag (Direktlieferung)** die Felder **Rechnung automatisch buchen** und **Rechnung automatisch drucken** aus.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
