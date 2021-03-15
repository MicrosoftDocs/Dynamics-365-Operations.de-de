---
title: Kreditverwaltungseinstellungen
description: In diesem Thema wird die Einstellung beschrieben, das für das Kreditmanagement erforderlich ist.
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: a2aa1980ebc1fa8412fc388e7837bc40b6902bc0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991244"
---
# <a name="credit-management-setup"></a>Kreditverwaltungseinstellungen 

[!include [banner](../includes/banner.md)]

## <a name="credit-management-workflows"></a>Kreditverwaltungsworkflows

Gehe zu **Kredit und Inkasso \> Einstellung \> Kreditmanagement-Workflows**, um die Workflows zu definieren, die zum Verwalten von Kreditlimitanpassungen verwendet werden.

- Sie können einen Workflow erstellen, mit dem Sie eine Reihe von Kreditlimitanpassungen über eine einzige Genehmigung genehmigen können.
- Sie können einen Workflow auf Zeilenebene hinzufügen, sodass Kreditlimitanpassungen einzeln genehmigt werden können.
- Sie können einen Freigabe-Workflow erstellen, der automatisch Sperren an einen Workflow-Prozess weiterleitet.

## <a name="blocking-rules"></a>Sperrungsregeln

### <a name="ranking-payment-terms"></a>Bewertung Zahlungskonditionen

Sie können einen Auftrag sperren, wenn die Zahlungsbedingungen in der Bestellung nicht mit den Standardzahlungsbedingungen für den Debitor übereinstimmen. Manchmal weichen die Zahlungsbedingungen jedoch voneinander ab, sind jedoch so ähnlich, dass Sie die Bestellung nicht sperren möchten. Sie können die Zahlungsbedingungen so einstufen, dass einige den gleichen Rang haben, während andere einen höheren oder niedrigeren Rang haben.

Wenn die Rangfolge für Zahlungsbedingungen aktiv ist und wenn die Zahlungsbedingungen für die Bestellung einen höheren Rang als die Standardzahlungsbedingungen für den Debitor haben, wird der Auftrag gesperrt.

Sie können die Rangfolge der Zahlungsbedingungen auf der Seite **Kredit und Inkasso \> Einrichten \> Kreditmanagement einrichten \>Rangfolge der Zahlungsbedingungen** festlegen  

### <a name="ranking-settlement-discounts"></a>Bewertung Ausgleichsrabatte

Sie können einen Auftrag sperren, wenn der Skonto in der Bestellung nicht mit dem Standardskonto für den Debitor übereinstimmt. Manchmal weichen die Skonten jedoch voneinander ab, sind jedoch so ähnlich, dass Sie die Bestellung nicht sperren möchten. Sie können die Skonten so einstufen, dass einige den gleichen Rang haben, während andere einen höheren oder niedrigeren Rang haben.

Wenn die Rangfolge für Ausgleichsrabatte aktiv ist und wenn Skonto auf den Aufträgen einen höheren Rang als die Skonto für den Debitor haben, wird der Auftrag gesperrt.

Sie können die Rangfolge der Zahlungsbedingungen auf der Seite **Kredit und Inkasso \> Einrichten \> Kreditmanagement einrichten \>Rangfolge der Zahlungermässigungen** festlegen  

## <a name="reasons"></a>Ursachen

Im Kreditmanagement werden verschiedene Arten von Gründen verwendet:

- Haltegründe geben an, warum ein Auftrag gesperrt wurde.
- Freigabegründe werden einem Auftrag zugeordnet, wenn er aus dem Wartezustand freigegeben wird.
- Statusgründe geben an, warum einem Debitor ein Kontostatus zugewiesen wurde.

Sie können Gründe auf der Seite **Gründe für das Kreditmanagement** (**Kredit und Inkasso \> Einrichten\> Kreditmanagement \> Gründe für das Kreditmanagement**) einstellen.

1. Wählen Sie im Feld **Grundtyp** den Grund aus: **Sperren**, **Freigeben** oder **Status**.
2. Geben Sie im Feld **Grund** einen Namen für die Grund ein.
3. Geben Sie im Feld **Beschreibung** eine Beschreibung für den Ursachencode ein.

## <a name="credit-management-groups"></a>Kreditverwaltungsgruppen

Kreditverwaltungsgruppen werden verwendet, um Debitoren oder Debitorengruppen mit denselben Kreditverwaltungseigenschaften zu identifizieren. Beispielsweise können Kreditverwaltungsgruppen verwendet werden, um die Sperr- und Ausschluss-Kreditverwaltungsregeln für Debitoren zu bestimmen.

Sie können Kreditmanagementgruppen auf der Seite **Kreditmanagementgruppen** (**Kreditmanagement \> Einstellung> Kreditmanagementgruppen einstellen \> Kreditmanagementgruppen**) erstellen.

1. Wählen Sie **Neu**, um eine Position zu erstellen.
2. Geben Sie eine ID für die Gruppe ein. Die ID kann bis zu 10 Zeichen lang sein.
3. Geben Sie im Feld **Beschreibung** einen Namen für die Gruppe ein. Der Name kann bis zu 60 Zeichen lang sein.

Die Kreditmanagementgruppe ist auf der Seite Inforegister **Kredit und Inkasso** auf der Seite **Alle Debitoren** (**Debitorenbuchhaltung \> Debitoren \> Alle Debitoren**) einem Kreditor zugewiesen.

## <a name="account-statuses"></a>Kontostatus

Sie können Kontostati erstellen, um die Bonität eines Debitorenkontos zu ermitteln. Sie können einen Status und dessen Auswirkung auf die Fakturierungs- und Lieferungsprozesse in der Warteschleife definieren. Kontostatus können auch verwendet werden, um Sperrregeln für einen Debitor zu bestimmen.

Sie können Kontostatus auf der Seite **Kontostatus** (**Kredit und Inkasso \> Einstellung > Kreditmanagementgruppen einrichten \> Kontostatus**) erstellen.

1. Fügen Sie einen Kontostatus hinzu und geben Sie eine Beschreibung für die Bonität eines Debitors ein. Verwenden Sie zum Beispiel **Normal** um anzuzeigen, dass ein Debitor in gutem Zustand ist und offene Aufträge einer standardmäßigen Kreditmanagementverarbeitung unterliegen.
2. Wählen Sie in den Feldern **Fakturierung** und **Lieferung gesperrt** die Art der Sperrung aus, die für Debitoren mit diesem Kontostatus erfolgen soll. Sie können die gesamte Verarbeitung, nur die Rechnungsverarbeitung oder keine Verarbeitung zurückhalten, wenn die Kreditlimitregeln angewendet werden.

## <a name="scoring-groups"></a>Bewertungsgruppen

Sie können Bewertungsgruppen einrichten, um Risikofaktoren und die Kriterien zu definieren, anhand derer diese gemessen werden. Wenn Informationen zu einem Debitor auf eine Bewertungsgruppe angewendet werden, wird für jeden Risikofaktor eine Bewertung berechnet und verwendet, um den Debitor in eine Risikogruppe einzuteilen. Die Risikogruppe kann verwendet werden, um die Kreditwürdigkeit zu identifizieren und automatische Kreditlimits zu berechnen.

Sie können Bewertungsgruppen auf der Seite **Bewertungsgruppen** (**Kreditmanagement und Inkasso \> Installieren \> Kreditmanagement einrichten \>  Risiko \> Bewertungsgruppen**) erstellen.

1. Erstellen sie eine Bewertungsgruppe und geben Sie ihr einen beschreibenden Namen.
2. Geben Sie eine Beschreibung ein, um die Bewertungsgruppe näher zu beschreiben.
3. Wählen Sie einen Gruppentyp aus. Es gibt acht vordefinierte Typen. Sie können auch **Benutzerdefiniert** auswählen, um einen Gruppentyp zu definieren, der besser zu Ihrer Organisation passt.
4. Wählen Sie einen Bewertungstyp aus, um zu definieren, wie die Bewertungsgruppe die Risikobewertung berechnet. Die folgenden Optionen stehen zur Verfügung:

    - **Angebot** – Verwenden Sie diese Option, um einen Wertebereich festzulegen, der zur Berechnung einer Punktzahl verwendet werden soll.
    - **Benutzerdefiniert** – Verwenden Sie diese Option, um manuell eine Liste von Werten zu definieren, die für die Bewertung verwendet werden sollen.

5. Wenn Sie **Bereich** als Bewertungstyp ausgewählt haben, fügen Sie Linien hinzu, um den Wertebereich und die entsprechenden Bewertungen zu definieren.

    1. Geben Sie im **Vom Wert** den niedrigsten Wert im Bereich an.
    2. Geben Sie im **Bis Wert** den höchsten Wert im Bereich an.
    3. Geben Sie im **Ergebnis** die Punktzahl ein, die zugewiesen werden soll, wenn der angegebene Wert im Bereich „von”/„bis“ liegt.

    Wenn Sie **Benutzerdefiniert** als Bewertungstyp ausgewählt haben, fügen Sie Linien hinzu, um die benutzerdefinierten Werte und die entsprechenden Bewertungen zu definieren.

    1. Geben Sie im Feld **Wert** den benutzerdefinierten Wert ein, der aus den Debitorinformationen bereitgestellt werden soll.
    2. Geben Sie im **Ergebnis** die Punktzahl ein, die zugewiesen werden soll, wenn der angegebene Wert im Bereich „von”/„bis“ liegt.

## <a name="risk-classification"></a>Risikoklassifizierung

Sie können Risikobewertungen definieren, die Debitoren anhand ihrer Risikobewertung zugewiesen werden können. Eine Risikobewertung wird berechnet, indem Debitorinformationen mit jeder Bewertungsgruppe verglichen werden. Die Bewertungen werden summiert und die Gesamtbewertung wird mit den Werten in der Risikogruppeneinrichtung verglichen, um die Risikogruppe zu identifizieren, zu der der Debitor gehört. Die Risikogruppenbewertungen wird dann verwendet, um Sperr- und Ausschlussregeln für das Kreditmanagement für den Debitor zu definieren.

Sie können Risikogruppen auf der Seite **Risikobewertungen** **(Kredit und Inkasso \> Einrichten \> Kreditmanagement einrichten \> Risiko \> Risikoklassifizierung**) einrichten.

1. Geben Sie eine Risikogruppen-ID ein.
2. Geben Sie eine Beschreibung ein, um die Risikogruppe näher zu erläutern.
3. Geben Sie eine Reihe von Bewertungen ein, anhand derer bestimmt wird, welche Debitoren zur Risikogruppe gehören.
4. Wählen Sie einen Risikogruppenindikator aus, um das Symbol anzugeben, das die Risikogruppe darstellt.

## <a name="guaranteeinsurance-types"></a>Garantie/Versicherungstypen

Sie können Garantie-/Versicherungsarten auf der Seite **Garantie-/Versicherungstypen** (**Kreditmanagement \> Installieren \> Kreditmanagement einrichten \> Versicherungen und Garantien \> Garantie- und Versicherungstypen**) einrichten.

1. Geben Sie einen Garantie- oder Versicherungstyp ein, der den Namen des Garantiegebers oder Versicherungsmaklers angibt.
2. Geben Sie eine Beschreibung ein, um den Garantiegeber/Versicherungsmakler zu beschreiben.

## <a name="coverage-types"></a>Dispositionstypen

Deckungsarten können zur weiteren Klassifizierung von Versicherungspolicen verwendet werden. Sie können nicht mit Garantien verwendet werden.

Sie können Deckungsarten auf der Seite **Deckungstypen** (**Kredit und Inkasso \> Einrichten \> Kreditmanagement einrichten \> Versicherung und Deckung \> Deckungstypen**) hinzufügen.

1. Geben Sie eine Deckungsart ein, um die Art der Deckung anzugeben, die als Versicherung oder Garantie hinzugefügt werden soll.
2. Eine Beschreibung für den Deckungstype ein.

## <a name="automatic-credit-limits"></a>Automatische Kreditlimits

Sie können Kriterien für automatische Kreditlimiten auf der Seite **Automatische Kreditlimiten** (**Kreditmanagement \> Einrichten \> Kreditmanagement einrichten \> Risiko \> Automatische Kreditlimiten**) erstellen.

1. Wählen Sie eine Risikogruppe aus, der das automatische Kreditlimit zugewiesen werden soll.
2. Wählen Sie die Währung für das automatische Kreditlimit. Sie können mehrere automatische Kreditlimits in verschiedenen Währungen für dieselbe Risikogruppe erstellen.
3. Geben Sie den Erlösbetrag ein, der den maximalen Unternehmenserlös darstellt, der für dieses automatische Kreditlimit verwendet werden kann. Wenn Kreditlimits erstellt werden, wird der Einnahmenbetrag mit einem Einnahmenwert verglichen, der auf der Seite **Finanzen** (**Debitoren \>Alle Debitoren \>Einen Debitoren auswählen \>Allgemeines \>Statistiken \>Finanzen**) gefunden wird. Das System verwendet den neuesten Wert im Abschnitt **Überblick**.

Führen Sie die folgenden Schritte aus, um Zeilen hinzuzufügen, die das Kreditlimit darstellen, das anhand der ausgewählten Kriterien generiert wird.

1. Wählen Sie die Bewertungsgruppe aus, die die Debitorinformationen definiert, die zur Berechnung des Kreditlimits verwendet werden sollen.
2. Wählen Sie den Vergleichsoperator aus, der definiert, wie die Bewertungsgruppeninformationen ausgewertet werden sollen.
3. Geben Sie den Wert ein, der mit dem für die Bewertungsgruppe angegebenen Wert verglichen werden soll.
4. Geben Sie das Kreditlimit ein, das zugewiesen werden soll, wenn die Debitorinformationen mit dem für die Bewertungsgruppe angegebenen Wert übereinstimmen. Beispielsweise erstellen Sie ein automatisches Kreditlimit für die Bewertungsgruppe **Niedrig**. Wenn die Geschäftsjahre zu den Bewertungsgruppen gehören, können Sie eine Zeile definieren, die ein Kreditlimit von 100.000 zuweist, wenn der Debitor fünf Jahre im Geschäft war, und eine andere Zeile, die ein Kreditlimit von 200.000 zuweist, wenn der Debitor zehn Jahre im Geschäft war Jahre.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]