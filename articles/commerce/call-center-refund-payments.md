---
title: Abwicklung von Rückerstattungszahlungen in Callcentern
description: In diesem Artikel wird erläutert, wie Rückerstattungen von Zahlungen durch Callcenter zu generieren sind, wenn Retouren erstellt oder Aufträge oder Auftragspositionen storniert werden.
author: hhainesms
ms.date: 01/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 330674a31dc59e99ffedb82d0896c64214562eb3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880113"
---
# <a name="refund-payment-processing-in-call-centers"></a>Abwicklung von Rückerstattungszahlungen in Callcentern

In diesem Artikel wird erläutert, wie Rückerstattungen von Zahlungen durch Callcenter zu generieren sind, wenn Retouren erstellt oder Aufträge oder Auftragspositionen storniert werden.

Ein Benutzer, der als Callcenterbenutzer in Microsoft Dynamics 365 Commerce-Zentralverwaltung eine Rücklieferung für einen Debitoren erstellt, muss auf der Seite **Rücklieferung** die anfängliche Rücksendungsautorisierung (Return Materials Authorization, RMA) erstellen. Die RMA definiert die Produkte, die der Debitor zurückgeben oder umtauschen möchte, und erstellt einen verknüpften Rücklieferungsauftrag mit dem Auftragstyp **Zurückgegebener Auftrag**. Anhand dieses verknüpften zurückgegebenen Auftrags werden die Buchung des zurückgegebenen Bestands sowie alle gebuchten Gutschriften oder Zahlungsrückerstattungen nachverfolgt.

Ist die Option **Auftragsabschluss aktivieren** für den Callcenterkanal auf **Ja** eingestellt, muss der Callcenterbenutzer, der die RMA erstellt, den Vorgang zum Auftragsabschluss durch Auswahl von **Abschließen** auf der Seite **Rücklieferung** ausführen. Die **Abschließen**-Funktion stellt eine Rückgabenzusammenfassung bereit, in der der fällige Rückerstattungsbetrag aufgeführt ist. Darüber hinaus erstellt sie bei korrekter Konfiguration systematisch eine Rückerstattungsposition für den zurückgegebenen Auftrag.

Die Callcenter-Logik bestimmt die Zahlungsmethode für die Rückerstattungsposition basierend auf der Zahlungsmethode, die für den ursprünglichen Auftrag verwendet wurde. Ist die erstellte Rücklieferung nicht mit einem ursprünglichen Auftrag verknüpft, wird eine Standardzahlungsmethode angewendet, die einem Systemparameter entnommen wird.

## <a name="how-a-call-center-determines-which-payment-method-to-apply-to-a-return-order"></a>Wie ein Callcenter bestimmt, welche Zahlungsmethode für eine Rücklieferung verwendet werden soll

Das Callcenter verwendet die Zahlungsmethode des ursprünglichen Auftrags, um die Zahlungsmethode zu bestimmen, die für eine Rücklieferung verwendet werden soll. Bei folgenden ursprünglichen Zahlungsmethoden funktioniert dieser Prozess wie folgt:

- **Normal** (Bargeld) oder **Scheck** – Wenn eine erstellte Rücklieferung auf eine ursprüngliche Bestellung verweist, die mit der normalen (Bargeld) oder Scheckzahlungsmethode beglichen wurde, verweist die Callcenter-Anwendung auf die Konfigurationen der Seite **Callcenter-Rückerstattungsmethoden**. Auf dieser Seite können Organisationen anhand der Auftragswährung festlegen, wie Debitoren Rückerstattungen für Aufträge erhalten, die ursprünglich über die normale Zahlungsmethode oder per Scheck bezahlt wurden. Die **Callcenter-Rückerstattungsmethoden** Seite ermöglicht es Unternehmen auch auszuwählen, ob ein vom System generierter Rückerstattungsscheck an den Kunden gesendet werden soll. In diesen Szenarien bezieht sich die Callcenter-Logik auf die Währung der Rücklieferung und verwendet dann den Wert **Einzelhandels-Zahlungsmethode** für diese Währung, um eine Rückerstattungsposition für den Rücklieferungsauftrag zu erstellen. Später wird eine Debitorenzahlungserfassung für Debitoren (Accounts Receivable, AR), die die zugeordnete AR-Zahlungsmethode nutzt, mit der Währung verknüpft.

    Die folgende Abbildung zeigt die Konfiguration für ein Szenario, in dem ein Debitor Produkte aus einem Auftrag zurückgibt, der mit der USD-Währung verknüpft ist und ursprünglich mit der normalen oder Scheckzahlungsmethode bezahlt wurde. In diesem Szenario wird dem Debitor eine Rückerstattung über einen vom System generierten Rückerstattungsscheck ausgestellt. Die AR-Zahlungsmethode **REF-CHK** wurde als Zahlungsmethode für Rückerstattungsschecks konfiguriert.

    ![Konfiguration von Callcenter-Rückerstattungsmethoden für ursprünglich normale und Scheckzahlungen.](media/callcenterrefundmethods.png)

    > [!NOTE]
    > Das Kundenkonto ist keine unterstützte Rückerstattungsmethode für Bar- oder Scheckzahlungen.

- **Kreditkarte** – Wenn eine erstellte Rücklieferung auf einen ursprünglichen Auftrag verweist, der per Kreditkarte bezahlt wurde, verwendet die Callcenter-Logik für Rückerstattungszahlungen dieselbe ursprüngliche Kreditkarte für den Rückgabeauftrag.
- **Treuekarte** – Wenn eine erstellte Rücklieferung auf einen ursprünglichen Auftrag verweist, der per Treuekarte bezahlt wurde, bucht die Callcenter-Logik für Rückerstattungszahlungen die Rückerstattung auf dieselbe Treuekarte.
- **Geschenkkarte** (intern) – Wenn eine erstellte Rücklieferung auf einen ursprüngliche Auftrag verweist, der mit einer Geschenkkarte bezahlt wurde, die über Dynamics 365 Commerce (interne Geschenkkartenfunktionalität) ausgestellt wurde, bucht die Callcenter-Logik für Rückerstattungszahlungen die Rückerstattung auf dieselbe ursprüngliche Geschenkkartennummer.
- **Geschenkkarte** (Extern) – Wenn eine erstellte Rücklieferung auf einen ursprünglichen Auftrag verweist, der mit einer externen Geschenkkarte eines Drittanbieters bezahlt wurde, wendet die Callcenter-Logik für Rückerstattungszahlungen die Standard-Rückzahlungsmethode an, die auf der Registerkarte **RMA/Rückgabe** der Seite **Callcenter-Parameter** definiert ist.

Wenn die Zahlungsmethode des ursprünglichen Auftrags aus irgendeinem Grund unbekannt ist oder wenn mehrere Zahlungsmethoden verwendet wurden, um den ursprünglichen Auftrag zu bezahlen, wendet die Callcenter-Logik die Standard-Rückzahlungsmethode an, die auf der Registerkarte **RMA/Rückgabe** der Seite **Callcenter-Parameter** definiert ist.

Die folgende Abbildung zeigt das Feld **Zahlungsmethode** auf der Registerkarte **RMA/Rückgabe** der Seite **Callcenter-Parameter**.

![Feld „Zahlungsmethode“ auf der Registerkarte „RMA/Rückgabe“ der Seite „Callcenter-Parameter“.](media/callcenterrefundparameters.png)

> [!NOTE]
> Die zuvor beschriebenen Regeln für die Abwicklung von Rückerstattungen gelten auch für Aufträge oder Auftragspositionen, die ein Callcenterbenutzer in der Commerce-Zentralverwaltung storniert. Wenn die Stornierung eines Auftrags oder bestimmter Auftragspositionen zu Überzahlungen führt, werden dieselben Regeln verwendet, um Rückerstattungspositionen zu generieren.

In der Regel durchläuft eine Rücklieferung einen Standardprozess, bei dem Bestand empfangen (oder verschrottet) wird, ein Lieferschein gegen die Rücklieferung gebucht und anschließend ein Rechnungsbuchungsprozess für den Rücklieferungsauftrag ausgeführt wird. Der Rücklieferungsauftrag wird im Rahmen der Rücklieferungserstellung verknüpft und systematisch generiert. In typischen Szenarien werden Zahlungserstattungen erst dann für Debitoren ausgestellt, wenn die Rechnung für den Rücklieferungsauftrag gebucht wurde.

### <a name="what-happens-when-an-invoice-is-posted-on-a-return-sales-order"></a>Was passiert, wenn eine Rechnung auf einen Rücklieferungsauftrag gebucht wird?

Die folgenden Szenarien erläutern, was passiert, wenn eine Rechnung auf einen Rücklieferungsauftrag gebucht wird:

- Wenn es sich bei der Rückerstattungszahlung auf der Rücklieferung um eine Kreditkarte handelt, wird beim Buchen der Rechnung eine zusätzliche Logik aufgerufen. Diese Logik ruft den Zahlungsdienstleister auf, um die Zahlung auf die Kreditkarte des Debitoren zurückzuerstatten. Ein Rückerstattungs-Debitorzahlungsbeleg wird ebenfalls erstellt und systematisch auf das Konto des Debitoren gebucht. Diese Zahlungserfassung wird mit dem Gutschriftbeleg für die Rücklieferung verrechnet.
- Wenn es sich bei der auszustellenden Rückerstattungszahlung um die Scheckzahlungsmethode handelt, wird ein Debitorzahlungsbeleg erstellt, der die AR-Zahlungsmethode verwendet. Dieser muss manuell gebucht oder gedruckt werden, bevor der Zahlungsbeleg auf das Debitorenkonto gebucht werden kann. Benutzer können zur Verarbeitung des Rückerstattungsschecks entweder die Seite **Debitorzahlungserfassung** in „Debitorenkonten“ oder spezielle Seite **Rückerstattungsscheckverarbeitung** in „Einzelhandel und Handel“.
- Handelt es sich bei der auszustellenden Rückerstattungszahlung um die Zahlungsmethode Geschenkkarte oder Treuekarte, wird bei der Fakturierung der Rücklieferung der Rückerstattungszahlungsbeleg erstellt und auf das Debitorenkonto gebucht. Bei diesem Rechnungsschritt wird der Rückerstattungsbetrag auch dem intern nachverfolgten Geschenkkarten- oder Treuepunktesaldo des Debitoren hinzugefügt.
- Wenn eine Zahlungsmethode, die die Funktion **Debitor** verwendet (z. B. ein Debitorenkonto), mit dem Rücklieferungsauftrag verknüpft ist, werden Kreditlimitüberprüfungen bei der Verarbeitung der Zahlung ignoriert. In diesem Zusammenhang wird kein Zahlungsbeleg erstellt oder gebucht. Wenn eine Debitorzahlungsmethode für eine Rücklieferung verwendet wird, dient der Gutschriftbeleg, den der Rechnungsbuchungsprozess erstellt, als Debitorhabenbeleg und zeigt eine Rückerstattung auf den AR-Saldo des Debitors an.

## <a name="advance-credit"></a>Gutschrift vorverlegen

Wenn ein Benutzer Rücklieferungen als Callcenter-Benutzer in einem Callcenter verarbeitet, in dem die Option **Auftragsabschluss aktivieren** auf **Ja** gesetzt ist, kann eine Ausnahme zu dem zuvor beschriebenen Vorgang für die Buchung von Rückerstattungszahlungen auftreten, wenn der Callcenter-Benutzer, der die Rücklieferung erstellt, die Option **Gutschrift vorverlegen** auf der Registerkarte **RMA/Rückgabe** der Seite **Callcenter-Parameter** auf **Ja** setzt. In diesem Fall erfolgt die Zahlungserstattung unmittelbar nach erfolgreicher Rücklieferungsübermittlung unter Verwendung der **Senden**-Funktion auf der Seite **Rückgabenzusammenfassung**. Das System erstellt sofort einen Vorauszahlungs-Debitorzahlungsbeleg über den Rückgabewert, obwohl der Rücklieferungsauftrag selbst noch nicht fakturiert wurde. Dieser Ansatz kann in Situationen verwendet werden, in denen eine Organisation aufgrund von Kundendienstproblemen im Voraus Rückerstattungen an Debitoren ausstellen muss und nicht möchte, dass der zurückgegebene Bestand vor der Ausstellung der Rückerstattungen eingeht.

## <a name="replacement-orders"></a>Ersatzaufträge

Wird eine Rücklieferung ausgestellt, kann über die Funktion **Ersatzauftrag** ein neuer Auftrag für den Debitor generiert werden. Dieser Ansatz kann in Austauschszenarien verwendet werden. Die Funktion **Ersatzauftrag** erstellt einen weiteren Auftrag für die neuen, zu versendenden Artikel. Allerdings verknüpft ein Querverweislink auf der Registerkarte **RMA/Rückgabe** der Seite **Callcenter-Parameter** den Ersatzauftrag, die RMA und den zurückgegebenen Auftrag.

Bei der Verarbeitung von Zahlungen für einen Ersatzauftrag haben Organisationen zwei Möglichkeiten:

- Dem Kunden die Rücklieferung basierend auf der ursprünglichen Zahlungsmethode zu erstatten und anschließend eine separate Zahlung für den Ersatzauftrag einzuziehen. Für die Verwendung dieser Option ist keine zusätzliche Konfiguration erforderlich.
- Auf der Registerkarte **RMA/Rückgabe** der Seite **Callcenter-Parameter** die Option **Gutschrift anwenden** auf **Ja** setzen. In diesem Fall wird eine Debitorenzahlungsmethode systematisch sowohl für die Rücklieferung als auch für den Ersatzauftrag verwendet. Diese Option kann dazu beitragen, die Ausstellung externer Rückerstattungszahlungen zu verhindern. Dadurch können auch Zahlungsabwicklungen bei der Transaktion verhindert werden. Dies kann in Situationen nützlich sein, in denen ein gleichmäßiger Umtausch verarbeitet wird, und die Organisation den Habenbeleg, der bei der Fakturierung der Rücklieferung generiert wird, für die Zahlung der Rechnung, die durch den Ersatzauftrag generiert wird, bevorzugt. Wenn die Option **Gutschrift anwenden** auf **Ja** gesetzt ist, muss die Organisation die Gutschrift manuell mit der Rechnung des Ersatzauftrags verrechnen, sobald beide Finanzdokumente generiert wurden.

Die Einstellung auf **Ja** für die Option **Gutschrift anwenden** ist nur anwendbar, wenn die Rücklieferung mit einem Ersatzauftrag verknüpft wird. In diesem Fall wird die Debitor-Zahlungsmethode, mit der die Rücklieferung und der Umtauschauftrag systematisch bezahlt werden, anhand des Felds **Gutschriftzahlungsmethode anwenden** auf der Registerkarte **RMA/Rückgabe** der Seite **Callcenter-Parameter** definiert. In diesem Feld kann nur eine Zahlung über die Zahlungsmethode **Debitor** ausgewählt werden.

> [!NOTE]
> Bei einer Rücklieferung ohne verknüpften Ersatzauftrag hat eine Einstellung auf **Ja** bei der Option **Gutschrift anwenden** keine Auswirkung auf die Zahlungslogik der Rücklieferung, da diese Einstellung nur für Ersatzaufträge gilt.

![Feld „Gutschriftzahlungsmethode anwenden“ auf der Registerkarte „RMA/Rückgabe“ der Seite „Callcenter-Parameter“.](media/callcenterrefundparameters1.png)

> [!IMPORTANT]
> Wenn Benutzer, die Ersatzaufträge erstellen, die Verwendung der Option **Gutschrift anwenden** planen, sollten sie die Funktion **Abschließen** für die Rücklieferung erst ausführen, wenn sie die Option **Gutschrift anwenden** auf **Ja** gesetzt haben. Sobald die Funktion **Abschließen** ausgeführt wurde, wird die Rückerstattungszahlung berechnet und für den Rücklieferungsauftrag verwendet. Jeder Versuch, die Option **Gutschrift anwenden** auf **Ja** zu setzen, wenn eine Rückerstattungszahlung bereits berechnet und angewendet wurde, löst keine Neuberechnung der Rückerstattungszahlung aus, und die im Feld **Gutschriftzahlungsmethode anwenden** ausgewählte Zahlungsmethode wird nicht angewendet. Falls die Option **Gutschrift anwenden** in diesem Zusammenhang verwendet werden muss, muss der Benutzer den Ersatzauftrag und die RMA löschen und von Neuem beginnen und eine neue RMA erstellen. Diesmal muss der Benutzer sicherstellen, dass die Option **Gutschrift anwenden** auf **Ja** gesetzt ist, bevor die Funktion **Abschließen** ausgeführt wird.

## <a name="payment-overrides-for-call-center-returns"></a>Zahlungsüberschreibungen bei Callcenter-Rückerstattungen

Obwohl die Callcenter-Logik die Zahlungsmethode für Rückerstattungen systematisch auf die zuvor in diesem Artikel beschriebene Weise ermittelt, möchten Benutzer diese Zahlungen manchmal überschreiben. So möchte ein Benutzer beispielsweise vorhandene Rückerstattungspositionen bearbeiten oder entfernen und neue Zahlungspositionen anlegen. Vom System berechnete Rückerstattungszahlungen können nur von Benutzern geändert werden, die über die richtigen Überschreibungsberechtigungen verfügen. Diese Berechtigungen können auf der Seite **Berechtigung überschreiben** in Einzelhandel und Handel konfiguriert werden. Der Benutzer muss für die Überschreibung einer Erstattungszahlung mit einer Sicherheitsrolle verknüpft sein, in der die Option **Alternative Zahlung zulassen** auf der Seite **Berechtigung überschreiben** auf **Ja** gesetzt ist.

![„Alternative Zahlung zulassen“-Option auf der Seite „Berechtigungen überschreiben“.](media/overridepermissions.png)

Alternativ kann eine Organisation die Option **Alternative Zahlung zulassen** auf der Registerkarte **RMA/Rückgabe** der Seite **Callcenter-Parameter** auf **Ja** setzen. In diesem Fall muss im Feld **Sicherheitsüberschreibungscode** ein Sicherheitsüberschreibungscode ausgewählt werden. Der Sicherheitsüberschreibungscode ist ein alphanumerischer Code, der extern verwaltet werden muss, da Benutzer ihn sich nach dem Festlegen nicht in der Commerce-Zentralverwaltung anzeigen lassen können. Der Sicherheitsüberschreibungscode sollte nur wenigen, wichtigen und vertrauenswürdigen Personen in einer Organisation bekannt sein. Wenn Benutzer, die nicht über die richtigen Rollenberechtigungen verfügen, versuchen, die Zahlungsmethode für eine Rücklieferung zu ändern, und die Option **Zahlungsüberschreibung zulassen** auf **Ja** gesetzt ist, haben sie die Möglichkeit, den Sicherheitsüberschreibungscode einzugeben. Wenn sie diesen nicht wissen, oder ein Manager oder Vorgesetzter ihn nicht auf der Seite für sie eingeben kann, können sie die Rückzahlungsmethode nicht überschreiben.

> [!NOTE]
> Wenn der Sicherheitsüberschreibungscode verloren geht oder vergessen wird, muss die Organisation ihn zurücksetzen, indem sie im Feld **Sicherheitsüberschreibungscode** auf der Registerkarte **RMA/Rückgabe** der Seite **Callcenter-Parameter** einen neuen Sicherheitsüberschreibungscode definiert.

![Parameter zur Zahlungsüberschreibung auf der Registerkarte „RMA/Rückgabe“ der Seite „Callcenter-Parameter“.](media/overridepaymentparameter.png)

> [!IMPORTANT]
> Bevor Unternehmen versuchen, Rückerstattungszahlungen, die die Kreditkarten-Zahlungsmethode nutzen, zu überschreiben, sollten sie überprüfen, ob der Kreditkartendienstleister nicht verknüpfte Rückgaben zulässt. Viele Dienstleister verlangen, dass Rückerstattungen auf die Originalkarte zurückgebucht werden. Jeder Versuch, eine Rückerstattung auf eine Karte vorzunehmen, die keine vorherigen Eintragungen hat, kann zu Buchungsfehlern beim Dienstleister führen.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Zahlungsmethoden in Callcentern](work-with-payments.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]