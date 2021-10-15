---
title: Intercompany-Parameter
description: In diesem Thema werden Intercompany-Parameter erläutert
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
ms.openlocfilehash: 705efee84b255105ba39c603d23d2509e77b331a
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548287"
---
# <a name="intercompany-parameters"></a>Intercompany-Parameter

[!include [banner](../../includes/banner.md)]

In einer Intercompany-Organisation können Sie Parameter einrichten, mit denen festgelegt wird, wie der Handel zwischen den verschiedenen juristischen Personen ablaufen soll. Diese Parameter werden anhand der ausgewählten Felder bestimmt. Sie können je nach Handelsszenario verschiedene Kombinationen auswählen.

Die folgenden beiden Beispiele beschreiben Szenarien für Intercompany-Organisationen, eine mit zwei Ebenen und eine mit drei Ebenen.

## <a name="example-1-two-level-intercompany-chain"></a>Beispiel 1: Intercompany-Kette mit zwei Ebenen

Die Intercompany-Organisation schließt die folgenden juristischen Personen ein:

- Juristische Person A – Verkauft Waren an externe Debitoren, verfügt jedoch über keinen Lagerbestand. Dies juristische Person kauft Waren bei der juristischen Person B.
- Juristische Person B – Verkauft nur Waren an die juristische Person A.

Beide juristische Personen können sich gegenseitig Waren verkaufen.

Im vorliegenden Beispiel basieren die Preise auf dem Originalauftrag, der an den externen Debitor geht, immer auf dem Verkaufspreis. Die Preise im Intercompany-Auftrag und in der Intercompany-Bestellung werden über den internen Verkaufs- bzw. Verrechnungspreis auf dem Intercompany-Auftrag in der juristischen Person B gesteuert.

Die Informationen im Auftragskopf werden vom Originalauftrag an den externen Debitor gesteuert. Änderungen am Intercompany-Auftrag werden nicht mit dem Originalauftrag synchronisiert.

Wählen Sie auf der Seite **Intercompany** unter „Juristische Person A“ für Kreditoren die Option **Bestellrichtlinien** aus. Wählen Sie die folgenden Felder in der Feldgruppe **Originalauftrag (Direktlieferung)** aus:

- **Lieferschein automatisch drucken**
- **Rechnung automatisch buchen**
- **Rechnung automatisch drucken**

Wählen Sie in der Feldgruppe **Intercompany-Bestellung (Direktlieferung)** das folgende Feld aus:

- **Rechnung automatisch buchen**

Wählen Sie in der Gruppe **Originalauftrag <-> Intercompany-Bestellung** die folgenden Felder aus:

- **Debitoreninformationen**
- **RMA-Nummer**

Wählen Sie in der Feldgruppe **Intercompany-Bestellung <-> Intercompany-Auftrag** die folgenden Felder aus:

- **Debitoreninformationen**
- **RMA-Nummer**
- **Chargennummer**
- **Seriennummer**

Wählen Sie auf der Seite **Intercompany** unter „Juristische Person B“ die Option **Auftragsrichtlinien** aus. Wählen Sie die folgenden Felder in der Feldgruppe **Erstellung von Intercompany-Aufträgen** aus:

- **Nummerierung für Verkaufsaufträge**: **Unternehmen + Originalnummer**
- **Zusammenfassungsaktualisierung von Dokumenten für ursprünglichen Debitor zulassen**

Wählen Sie in der Feldgruppe **Intercompany-Auftragspreise** die folgenden Felder aus:

- **Preis- und Rabattsuche**
- **Preisbearbeitung zulassen**
- **Rabattbearbeitung zulassen**

Wählen Sie in der Feldgruppe **Intercompany-Bestellung \> Intercompany-Auftrag** die folgenden Felder aus:

- **Chargennummer**
- **Seriennummer**

## <a name="example-2-three-level-intercompany-chain"></a>Beispiel 2: Intercompany-Kette mit drei Ebenen

Die Intercompany-Organisation schließt die folgenden juristischen Personen ein:

- Juristische Person A – Eine juristische Person aus dem Bereich Verkauf, die Waren an externe Debitoren verkauft und bei der juristischen Person B Waren erwirbt.
- Juristische Person B – Eine juristische Person aus dem Bereich Produktion oder Vertrieb, die keine Produkte liefern kann und Waren bei der juristischen Person C erwirbt.
- Juristische Person C – Eine juristische Person aus dem Bereich Produktion oder Vertrieb, die Produkte an die juristische Person B liefert.

Der interne Verrechnungspreis zwischen den juristischen Personen B und C entspricht dem Einstandspreis des verkaufenden Unternehmens am Anfang der Kette. Er entspricht dem Einstandspreis der juristischen Person A, die an externe Debitoren verkauft. Die Preise auf dem Originalauftrag für den externen Debitor basieren jedoch immer auf dem Verkaufspreis.

Die Preise in allen Intercompany-Aufträgen und Intercompany-Bestellungen werden mit dem Intercompany-Auftrag gesteuert. Die Preise werden am Anfang der Kette gesteuert. Daher steuert die juristische Person C, die Waren an die juristische Person B verkauft, die Preisgestaltung. Die Preise im Intercompany-Auftrag basieren auf dem internen Verkaufs- bzw. Verrechnungspreis, der in der juristischen Person C eingerichtet ist.

Die Informationen im Auftragskopf werden vom Originalauftrag an den externen Debitor gesteuert. Änderungen an den Intercompany-Aufträgen werden nicht auf den Originalauftrag synchronisiert.

Die folgenden Parameter sollten ausgewählt werden:

Wählen Sie auf der Seite **Intercompany** unter „Juristische Person A“ für Kreditoren die Option **Bestellrichtlinien** aus. Wählen Sie die folgenden Felder in der Feldgruppe **Originalauftrag (Direktlieferung)** aus:

- **Lieferschein automatisch drucken**
- **Rechnung automatisch buchen**
- **Rechnung automatisch drucken**

Wählen Sie in der Feldgruppe **Intercompany-Bestellung (Direktlieferung)** das folgende Feld aus:

- **Rechnung automatisch buchen**

Wählen Sie in der Feldgruppe **Originalauftrag <-> Intercompany-Bestellung** die folgenden Felder aus:

- **Debitoreninformationen**
- **RMA-Nummer**

Wählen Sie in der Feldgruppe **Intercompany-Bestellung <-> Intercompany-Auftrag** die folgenden Felder aus:

- **Debitoreninformationen**
- **RMA-Nummer**
- **Chargennummer**
- **Seriennummer**

Wählen Sie auf der Seite **Intercompany** unter „Juristische Person B“ die Option **Auftragsrichtlinien** aus. Wählen Sie die folgenden Felder in der Feldgruppe **Erstellung von Intercompany-Aufträgen** aus:

- **Nummerierung für Verkaufsaufträge**: **Unternehmen + Originalnummer**
- **Zusammenfassungsaktualisierung von Dokumenten für ursprünglichen Debitor zulassen**

Wählen Sie in der Feldgruppe **Intercompany-Bestellung \> Intercompany-Auftrag** die folgenden Felder aus:

- **Chargennummer**
- **Seriennummer**

Wählen Sie in der Feldgruppe **Rechnungsbuchung für Intercompany-Debitorenrechnung** die folgenden Felder aus:

- **Preis pro Einheit gleich Einstandspreis**
- **Rechungsbuchung der ursprünglichen Debitorenrechnung starten**

Wählen Sie auf der Seite **Intercompany** unter „Juristische Person B“ für Kreditoren die Option **Bestellrichtlinien** aus. Wählen Sie die folgenden Felder in der Feldgruppe **Originalauftrag (Direktlieferung)** aus:

- **Lieferschein automatisch drucken**
- **Rechnung automatisch buchen**
- **Rechnung automatisch drucken**

Wählen Sie in der Feldgruppe **Intercompany-Bestellung (Direktlieferung)** das folgende Feld aus:

- **Rechnung automatisch buchen**

Wählen Sie in der Feldgruppe **Originalauftrag <-> Intercompany-Bestellung** die folgenden Felder aus:

- **Debitoreninformationen**
- **RMA-Nummer**
- **Preis und Rabatt**

Wählen Sie in der Feldgruppe **Intercompany-Bestellung <-> Intercompany-Auftrag** die folgenden Felder aus:

- **Debitoreninformationen**
- **RMA-Nummer**
- **Chargennummer**
- **Seriennummer**

Wählen Sie auf der Seite **Intercompany** unter „Juristische Person C“ die Option **Auftragsrichtlinien** aus. Wählen Sie die folgenden Felder in der Feldgruppe **Erstellung von Intercompany-Aufträgen** aus:

- **Nummerierung für Verkaufsaufträge**: **Nummernkreiscode**
- **Zusammenfassungsaktualisierung von Dokumenten für ursprünglichen Debitor zulassen**

Wählen Sie in der Feldgruppe **Intercompany-Auftragspreise** das folgende Feld aus:

- **Preis- und Rabattsuche**

Wählen Sie in der Feldgruppe **Rechnungsbuchung für Intercompany-Debitorenrechnung** die folgenden Felder aus:

- **Preis pro Einheit gleich Einstandspreis**
- **Rechungsbuchung der ursprünglichen Debitorenrechnung starten**

Wählen Sie in der Feldgruppe **Intercompany-Auftragspreise <-> Intercompany-Bestellung** die folgenden Felder aus:

- **Chargennummer**
- **Seriennummer**

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
