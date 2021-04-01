---
title: Schicht- und Kassenladenverwaltung
description: In diesem Thema wird erläutert, wie Sie in der Commerce-Verkaufsstelle (POS) Schichten einrichten und nutzen.
author: jblucher
manager: AnnBe
ms.date: 05/10/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailHardwareProfile, RetailTerminalTable
audience: Application User
ms.reviewer: josaw
ms.custom: 105011
ms.assetid: 49a0fcc9-d4db-45ad-8c4b-213ccaced82b
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: c1038b0ec80ec3441e508bcf51bca0dac01cbd0d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234460"
---
# <a name="shift-and-cash-drawer-management"></a>Schicht- und Kassenladenverwaltung

[!include [banner](includes/banner.md)]

In diesem Thema wird erläutert, wie Sie in der Commerce-Verkaufsstelle (POS) Schichten einrichten und nutzen.

In Dynamics 365 Commerce wird der Begriff *Schicht* als die Sammlung von buchungsbezogenen POS-Daten und Aktivitäten zwischen zwei Punkten beschrieben. Für jede Schicht wurde der erwartete Geldbetrag mit dem Betrag verglichen, der gezählt und deklariert wurde.

Normalerweise sind Schichten zu Beginn des Werktages geöffnet. An diesem Punkt deklariert ein Benutzer den Anfangsbetrag, den die Kasse enthält. Verkaufsbuchungen werden anschließend den gesamten Tag lang ausgeführt. Schließlich wird am Ende des Tages die Kasse gezählt und die Abschlussbeträge werden deklariert. Die Schicht wurde geschlossen und ein Z-Bericht wird generiert. Der Z-Bericht gibt an, ob ein Überschuss oder Fehlbetrag vorliegt.

## <a name="typical-shift-scenarios"></a>Typische Schichtszenarien

Commerce bietet mehrere Konfigurationsoptionen und POS-Vorgänge an, die eine breite Palette von Tagesendgeschäftsprozessen für den POS unterstützen. In diesem Abschnitt werden einige typische Schichtszenarien beschrieben.

### <a name="fixed-till"></a>Feste Kasse

Traditionsgemäß wird dieses Szenarios am häufigsten verwendet. Es wird immer noch extensiv verwendet. In einer Schicht mit "fester Kasse" sind die Schicht und die Kasse mit einer bestimmten Erfassung verknüpft. Sie werden nicht von einem Register zu einem anderen bewegt. Eine "feste Kasse" kann von einem einzelnen Benutzer oder von mehreren Benutzern verwendet werden. Schichten mit "Fester Kasse" benötigen keine besondere Konfiguration.

### <a name="floating-till"></a>Wechselnde Kasse

Bei einer "Wechselnen Kasse" kann die Schicht und die Bargeldkasse von einer Kasse zu einer anderen verschoben werden. Obgleich ein Register nur eine aktive Schicht pro Bargeldkasse haben kann, können Schichten unterbrochen und später fortgeführt oder zu einer anderen Kasse verschoben werden.

Ein Geschäft hat beispielsweise zwei Kassen. Jede Kasse wird zu Beginn des Tages geöffnet, wenn der Kassierer eine neue Schicht öffnet und den Anfangsbetrag bereitstellt. Wenn ein Kassierer bereit ist, eine Pause einzulegen, unterbricht dieser Kassierer seine Schicht und entfernt die Kassenlade aus der Kasse. Die Kasse ist dann für andere Kassierer verfügbar. Ein anderer Kassierer kann sich anmelden und dann seine Schicht an der Kasse öffnen. Nachdem die Pause des ersten Kassiers beendet ist, kann der Kassier seine Schicht wieder aufnehmen, wenn eine Kasse verfügbar ist. Schichten mit "Fester Kasse" benötigen keine besondere Konfiguration oder Erlaubnis.

### <a name="single-user"></a>Einzelbenutzer

Viele Einzelhändler ziehen es vor, nur einem Benutzer pro Schicht zu ermöglichen, um für die Kassenlade in der Kasse höchstmögliche Sicherheit zu gewähren. Wenn nur ein Benutzer die Kassenlade nutzen darf, die der Schicht zugeordnet ist, kann der Nutzer für sämtliche Abweichungen zur Rechneschaft gezogen werden.. Wenn mehr als ein Nutzer eine Schicht verwenden ist es schwierig zu bestimmen, wer den Fehler gemacht hat oder wer versucht hat, Geld aus der Kassenlade zu entwenden.

### <a name="multiple-users"></a>Mehrere Benutzer

Einige Einzelhändler sind bereit, den Bereich der Verantwortlichkeit von Einzelschichtnutzern aufzugeben und mehr als einen Nutzer pro Schicht zuzulassen. Dieser Ansatz ist typisch, wenn mehr Benutzer als verfügbare Kassen vorhanden sind und die Anforderung für Flexibilität und Geschwindigkeit das Potential für Verlust übersteigt. Es ist ebenso typisch, wenn der Geschäftsführ keine eigene Schicht hat, aber, sofern notwendig, die Schicht eines anderen Kassiers nutzen kann. Zum Anmelden und Nutzen einer Schicht, die von einem anderen Benutzer geöffnet wurde, muss ein Benutzer die Berechtigung **Mehrere Schichtanmeldungen zulassen** haben.

### <a name="shared-shift"></a>Gemeinsame Schichten

Eine "Geteilte Schicht" erlaubt Einzelhändlern eine einzelne Schicht über verschiedene Kasse und Benutzern. Eine freigegebene Schicht hat einen einzelnen Anfangsbetrag und ein einzelnen Endbetrag, die den Abschlussbetrag für alle Kassen geben. Geteilte Schichten sind am typischsten, wenn mobile Geräte verwendet werden. In diesem Szenario ist keine separate Geldlade für jede Kasse reserviert. Stattdessen können alle Kassen eine Geldlade teilen.

Damit geteilte Schichten in einem Shop verwendet werden können, muss die Kassenlade als „Schichtkassenlade“ unter **Einzelhandel und Handel \> Kanaleinrichtung \> POS-Einrichtung \> POS-Profile \> Hardwareprofile \> Kassenladen** konfiguriert werden. Darüber hinaus müssen Benutzer eine oder beide der freigegebenen Schichtberechtigungen haben (geteilte Schicht verwalten und geteilte Schicht nutzen zulassen).

> [!NOTE]
> Hinweis: Es kann nur eine gemeinsame Schicht pro Shop geöffnet werden. Gemeinsame Schichten und eigenständige Schichten können im gleichen Shop verwendet werden.

## <a name="shift-and-drawer-operations"></a>Schicht- und Kassenverwaltung

Verschiedene Aktivitäten können ausgeführt werden, um den Status einer Schicht zu ändern oder um den Geldbetrag in der Kasse zu erhöhen oder zu verringern. Dieser Abschnitt beschreibt diese Schichtbetriebe für Modern POS und Cloud POS.

### <a name="open-shift"></a>Offene Schichten

POS erfordert, dass ein Benutzer keine aktive, offene Schicht hat, um alle möglichen Vorgänge auszuführen, die zu wertmäßiger Buchung wie Verkauf, Rücklieferung oder Kundenauftrag führen würde.

Wenn ein Benutzer sich beim POS anmeldet, überprüft das System zuerst, ob eine aktive Schicht für diesen Benutzer im aktuellen Register verfügbar ist. Falls keine aktive Scnicht verfügbar ist, kann der Benutzer eine neue Schicht öffnen, eine vorhandene Schicht wieder aufnehmen oder sich im Modus "keine Kasse" anmelden, abhängig von der Systemkonfiguration und den Berechtigungen.

### <a name="declare-start-amount"></a>Ausgangsbetrag deklarieren

Dieser Vorgang ist häufig die erste Aktivität, die bei einer neu geöffneten Schicht vorgenommen wird. Bei diesem Vorgang geben Benutzer den Anfangsbarbetrag in der Schublade für die Schicht an. Dieser Vorgang ist wichtig, da die Überschuss-/Mangelberechnung, die standardmäßig ausgeführt werden soll, wenn einer Schicht geschlossen wird, den Standardbetrag berücksichtigt.

### <a name="float-entry"></a>Mittelzugang

*Angebotsentfernungen* sind Nichtverkaufstransaktionen, die in einer aktiven Schicht ausgeführt werden, um die Menge des Bargelds in der Schublade zu reduzieren. Ein allgemeines Beispiel für einen Float-Eintrag wäre es, zusätzliche Änderung dem Wechselaussteller hinzufügen, wenn die Ausführung gering ist.

### <a name="tender-removal"></a>Zahlungsmittel entfernen

*Angebotsentfernungen* sind Nichtverkaufstransaktionen, die in einer aktiven Schicht ausgeführt werden, um die Menge des Bargelds in der Schublade zu reduzieren. Dieser Vorgang wird am häufigsten in Verbindung mit einem Mittelzugang bei einer anderen Schicht verwendet. Beispielsweise hat Kasse 1 wenig Bargeld und der Benutzer von Kasse 2 macht einen Bezug, um den Betrag in der eigenen Kasse zu reduzieren. Der Benutzer von Kasse 1 führt dann einen Mittelzugang aus, um den Betrag in seiner Kassenlade zu erhöhen.

### <a name="suspend-shift"></a>Schicht aussetzen

Benutzer können ihre aktive Schicht unterbrechen, um die aktuelle Erfassung für einen anderen Benutzer freizugeben oder um ihre Schicht in eine andere Erfassung zu verschieben (dies wird oft als „gleitende Kassenlade” bezeichnet).

Das Unterbrechen der Schicht verhindert, dass irgendwelche neuen Transaktionen oder Änderungen an der Schicht vorgenommen werden, bis sie wieder fortgesetzt wird.

### <a name="resume-shift"></a>Schicht fortsetzen

Dieser Vorgang ermöglicht es einem Benutzer, eine zuvor unterbrochene Schicht an einer beliebigen Kasse wieder aufzunehmen, die noch keine aktive Schicht hat.

### <a name="tender-declaration"></a>Kassensturz

Dieser Vorgang erfolgt, um den Gesamtbetrag des Geldes anzugeben, der gerade in der Kassenlade ist. Benutzer führen am häufigsten diesen Arbeitsgang aus, bevor sie eine Schicht schließen. Dies ist der Wert, der gegenüber der erwarteten Schicht verglichen wird, um den Über-/Fehlbetrag zu berechnen.

### <a name="safe-drop"></a>Ablage in Tresor

Ablagen im Tresor können jederzeit in einer aktiven Schicht ausgeführt werden. Durch diesen Vorgang wird Geld aus der Schublade entfernt, sodass es an einen sichereren Ort übertragen werden kann, wie beispielsweise einen Tresor im Hinterzimmer. Der Gesamtbetrag, der für Ablagen im Tresor erfasst ist, ist immer noch in den Schichtsummen enthalten. Er muss jedoch nicht als Teil des Kassensturzes gezählt werden.

### <a name="bank-drop"></a>Bankeinzahlung

Wie Ablagen in Tresor werden auch Bankeinzahlungen auf aktiven Schichten ausgeführt. Durch diesen Vorgang wird Geld aus der Schicht entfernt, um es für die Bankeinzahlung vorzubereiten.

### <a name="blind-close-shift"></a>Schicht blind schließen

*Blind-geschlossene Schichten* sind nicht mehr aktiv, aber noch nicht vollständig abgeschlossen. Anders als unterbrochene Schichten können blind-geschlossene Schichten nicht fortgesetzt werden.. Vorgänge wie Startbetrag deklarieren und Kassensturz knnen dann später auf dieser oder einer anderen Kasse ausgeführt werden.

Geschlossene Schichten werden häufig verwendet, um eine Kasse für einen neuen Benutzer oder eine Schicht freizugeben, ohne diese Schicht zuerest vollständig zählen, abzustimmen und vollständig beenden zu müssen.

### <a name="close-shift"></a>Schicht schließen

Dieser Vorgang berechnet Schichtsummen und Über-/Fehlbeträge und schließt dann eine aktive oder blinde geschlossene Schicht ab. Abhängig von den Berechtigungen des Benutzers wird ein Z-Bericht auch für die Schicht gedruckt. Abgeschlossene Schichten können nicht fortgesetzt oder geändert werden.

### <a name="print-x"></a>X drucken

Dieser Arbeitsgang generiert und druckt einen X-Berichts für die aktuelle aktive Schicht.

### <a name="reprint-z"></a>Z erneut drucken

Dieser Arbeitsgang druckt den letzten Z-Bericht, den das System erzeugt hatte, als die Schicht abgeschlossen wurde.

### <a name="manage-shifts"></a>Schichten verwalten

Dieser Vorgang ermöglicht es Benutzern, alle aktiven, unterbrochenen und blinden geschlossenen Schichten für die Filiale anzuzeigen. Abhängig von den Berechtigungen können Benutzer die endgültig Abschlussprozedur wie Deklaration und Schichten beenden selber vornehmen. Dieser Arbeitsgang ermöglicht es auch Benutzern, ungültige Schichten anzuzeigen und zu löschen, und zwar im seltenen Fall, in dem eine Schicht in einem schlechten Zustand zurückbleibt, nachdem zwischen Offline- und Onlinemodi umgeschaltet wurde. Diese ungültigen Schichten enthalten keine finanziellen Informationen oder Buchungsdaten, die für die Abstimmung erforderlich sind.

## <a name="shift-and-drawer-permissions"></a>Schicht- und Kassenverwaltung

Die folgende POS-Berechtigung beeinflusst, was ein Benutzer in unterschiedlichen Szenarios ausführen kann und nicht kann:

- **Blindschließen zulassen**
- **Drucken von X-Bericht zulassen**
- **Drucken von Z-Bericht zulassen**
- **Kassensturz zulassen**
- **Offene Deklaration zulassen**
- **Kassenlade öffnen (ohne Verkauf)**
- **Mehrere Schichtanmeldungen zulassen** - - Diese Berechtigung erlaubt es dem Benutzer, sich bei einer Schicht anzumelden und die Schicht zu nutzen, die ein anderer Benutzer geöffnet hat. Benutzer, die nicht diese Berechtigung verfügen, können sich nur bei Schichten anmelden und Schichten nutzen, die sie selber geöffnet haben.
- **Freigegebene Schicht verwalten zulassen** – Benutzer müssen diese Berechtigung haben, um eine freigegebene Schicht zu öffnen oder zu schließen.
- **Freigegebene Schicht nutzen zulassen** – Benutzer müssen diese Berechtigung haben, um sich bei einer freigegebenen Schicht anzumelden und diese zu nutzen.

## <a name="back-office-end-of-day-considerations"></a>Backoffice-Tagesendeüberlegungen

Die Methode, die Schichten und Geldladenabstimmung im POS verwendet, unterscheidet sich von der Art, wie die Buchungsdaten für die Auszugsberechnung zusammengefasst werden. Es ist wichtig, dass Sie den Unterschied verstehen. Abhängig von der Konfiguration und den Geschäftsprozessen können die Schichtdaten am Point-of-Sale (Z-Bericht) und ein berechneter Auszug im Back Office Ihnen unterschiedliche Ergebnisse geben. Diese Differenz bedeutet nicht unbedingt, dass entweder die Schichtdaten des berechneten Auszug falsch sind oder dass ein Problem mit den Daten besteht. Dies bedeutet, dass die Parameter, die zur Verfügung stehen, eine zusätzliche Buchung oder weniger umfassen oder dass die Buchungen anders zusammengefasst wurden.

Obwohl jeder Einzelhändler verschiedene geschäftliche Anforderungen hat, empfiehlt es sich, das System folgendermaßen einzurichten, um Situationen zu vermeiden, in denen Unterschiede dieses Typs passieren:

Gehen Sie zu **Einzelhandel und Handel \> Kanäle \> Shops \> Alle Shops \> Auszug/Abschluss** und legen Sie für jeden Shop das Feld **Auszugsmethode** und das Feld **Abschlussmethode** auf **Schicht** fest.

Diese Einstellung stellt sicher, dass Backofficeauszüge die gleichen Buchungen wie Schichten im POS enthalten und die Daten durch diese Schicht zusammengefasst werden.

Weitere Informationen zu Auszugs- und Abschlussmethoden, finden Sie unter [Shopkonfigurationen für Einzelhandelsauszug](https://docs.microsoft.com/dynamics365/unified-operations/retail/tasks/store-configurations-retail-statements).


[!INCLUDE[footer-include](../includes/footer-banner.md)]