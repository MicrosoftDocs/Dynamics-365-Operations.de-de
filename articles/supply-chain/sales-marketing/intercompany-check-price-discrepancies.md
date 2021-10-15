---
title: Abweichungen der Intercompany-Auftragspreise überprüfen
description: In diesem Thema wird erläutert, wie Sie konzerninterne Preisabweichungen überprüfen können.
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: PurchTable, PurchTablePart, PurchLineOpenOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: f9a0ba4980f8acf56d84dc865094b405b7402ad5
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548277"
---
# <a name="check-intercompany-order-price-discrepancies"></a>Abweichungen der Intercompany-Auftragspreise überprüfen

[!include [banner](../../includes/banner.md)]

Sie können auf diese Weise nach Preisabweichungen bei Intercompany-Aufträgen suchen.

1. Wechseln Sie zu **Beschaffung \> Periodisch \> Bereinigen \> Abweichungen der Intercompany-Auftragspreise überprüfen**.
1. Richten Sie ggf. einen Stapelverarbeitungsauftrag ein, und wählen Sie anschließend **OK** aus, um die Preise und Rabatte für Intercompany-Aufträge und Bestellungen zu überprüfen. Wählen Sie anderenfalls **Abbrechen** aus, um die Seite ohne Überprüfung zu schließen.

    > [!TIP]
    > Sofern Probleme bei der Synchronisierung oder wegen der Preise aufgetreten sind, werden diese in einer Informationsnachricht aufgelistet, die angezeigt wird. Sie können die Informationsnachricht zu Referenzzwecken drucken.

1. Wählen Sie in der Informationsnachricht die betreffende Position aus, um den Auftrag in der aktuellen juristischen Person zu öffnen. Öffnen Sie den Auftrag in der zugehörigen juristischen Person, indem Sie **Intercompany** und dann **Intercompany-Bestellung** oder **Intercompany-Verkaufsauftrag** auswählen.

    > [!NOTE]
    > So lassen Sie die Aktualisierung des Intercompany-Auftrags zu:
    >
    > 1. Gehen Sie zu **Debitorenkonten \> Debitoren \> Alle Debitoren**.
    > 1. Wählen Sie im Aktionsbereich die Registerkarte **Allgemein** und dann **Intercompany** aus.
    > 1. Wählen Sie auf der Seite **Intercompany** die Option **Bestellrichtlinien** oder **Auftragsrichtlinien** aus.
    > 1. Wählen Sie in beiden Bereichen **Preisbearbeitung zulassen** und **Rabattbearbeitung zulassen** aus.

1. Öffnen Sie den entsprechenden Intercompany-Auftrag, in dem Sie den Preis beibehalten möchten.
1. Ändern Sie für jede Auftragsposition das Feld **Preis je Einheit** für die Position, und ändern Sie es anschließend wieder in den ursprünglichen Wert. Wechseln Sie den Wert des Felds **Rabatt** für die Position hin und her, und wechseln Sie den entsprechenden Wert der Felder **Belastungen für Einkäufe** oder **Verkaufsbelastungen** hin und her. Durch diese Änderungen wird eine Synchronisierung der Preise, Rabatte und Belastungen der aktuellen Intercompany-Auftragsposition mit der referenzierten Intercompany-Auftragsposition ausgelöst, sodass diese automatisch abgeglichen werden.

    > [!NOTE]
    > Diese Synchronisierung ist nur gültig, wenn der Intercompany-Auftrag noch nicht fakturiert wurde. Wenn die Rechnung für den Intercompany-Auftrag gebucht und eine Debitorenrechnungserfassung erstellt wurde, müssen die Änderungen direkt in den Intercompany-Bestellpositionen durchgeführt werden, indem die Preise, Rabatte und Belastungen mit denen in der Intercompany-Debitorenrechnungserfassung in Übereinstimmung gebracht werden. Andernfalls kann die Rechnung für die Intercompany-Bestellung nicht gebucht werden, da die Auftragssummen nicht übereinstimmen.

1. Wiederholen Sie das Verfahren, bis alle Intercompany-Bestellungen und -Aufträge synchronisiert wurden.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
