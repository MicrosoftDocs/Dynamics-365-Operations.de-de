---
title: Schicht- und Kassenladenverwaltung
description: "Dieser Artikel erläutert die Einrichtung der zwei verschiedenen Schichttypen für POS: gemeinsam und eigenständig. Gemeinsame Schichten können von mehreren Benutzern an mehreren Orten verwendet werden. Eigenständige Schichten können nur von einer Arbeitskraft gleichzeitig verwendet werden."
author: rubencdelgado
manager: AnnBe
ms.date: 02/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailHardwareProfile, RetailTerminalTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 105011
ms.assetid: 49a0fcc9-d4db-45ad-8c4b-213ccaced82b
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 8a24f8adc4f7886a1f942d83f7a4eb12e7034fcd
ms.openlocfilehash: c1483d3240d266845cea7789b70c038cb98fdfcc
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---

# <a name="shift-and-cash-drawer-management"></a>Schicht- und Kassenladenverwaltung

[!INCLUDE [banner](includes/banner.md)]

Dieser Artikel erläutert die Einrichtung der zwei verschiedenen Schichttypen für POS: gemeinsam und eigenständig. Gemeinsame Schichten können von mehreren Benutzern an mehreren Orten verwendet werden. Eigenständige Schichten können nur von einer Arbeitskraft gleichzeitig verwendet werden.

Gibt es zwei Arten von Einzelhandels-POS-Schichten: eigenständige und gemeinsame. Eigenständige Schichten können nur von einer Arbeitskraft gleichzeitig verwendet werden. Gemeinsame Schichten können von mehreren Benutzer an mehreren Orten verwendet werden. Daher bilden sie letztendlich eine einzelne Schicht für mehrere Arbeitskräfte in einem Shop.

## <a name="standalone-shifts"></a>Eigenständige Schichten
Eigenständige Schichten werden in einem traditionellen, festen POS-Szenario verwendet, in dem Bargeld für jede POS-Kasse unabhängig abgestimmt wird. Z. B. gibt es in einem Lebensmittelgeschäft in der Regel mehrere feste POS-Kassen und Kassierer jeweils einer Kasse zugewiesen. In diesem Fall verwendet wahrscheinlich jede Kasse eine eigenständige Schicht und der Kassierer ist für die Kasse oder das Bargeld in der Kasse verantwortlich. Eine eigenständige Schicht umfasst alle Aktivitäten zu der Kasse während der Schicht des Kassierers. Zu den Aktivitäten zählen der in die Kasse hinterlegte Anfangsbetrag, das Entnehmen und Hinzufügen von Bargeld im Betrieb (z. B. bei Entnahmen zur Bankeinzahlung) und der Kassensturz am Ende der Schicht.

### <a name="set-up-a-stand-alone-shift"></a>Einrichten einer eigenständigen Schicht

Eine eigenständige Schicht gilt auf Kassenladenebene. Dieses Verfahren beschreibt die Einrichtung einer eigenständigen Schicht für eine POS-Kasse.

1.  Klicken Sie auf **Einzelhandel und Handel** &gt; **Kanaleinrichtung** &gt; **POS-Einrichtung** &gt; **POS-Profile** &gt; **Hardwareprofile**.
2.  Wählen Sie das Hardwareprofil für die eigenständige Schicht.
3.  Prüfen Sie auf dem **Kassenlade**-Inforegister, ob die Option **Kassenladen für gemeinsame Schicht** auf **Nein** festgelegt ist.
4.  Klicken Sie auf **Speichern**.
5.  Klicken Sie auf **Einzelhandel** &gt; **Kanaleinstellungen** &gt; **POS-Einstellungen** &gt; **Register**.
6.  Wählen Sie die Kasse, für die eine eigenständige Schicht erforderlich ist, und klicken Sie dann auf **Bearbeiten**.
7.  Wählen Sie im Feld **Hardwareprofil** das Hardwareprofil aus, das Sie in Schritt 2 ausgewählt haben.
8.  Klicken Sie auf **Speichern**.
9.  Klicken Sie auf **Einzelhandel** &gt; **Handel IT** &gt; **Vertriebsplan**.
10. Wählen Sie den Vertriebsplan **1090**, und klicken Sie dann auf **Jetzt ausführen**, um die Änderungen mit dem POS zu synchronisieren.

### <a name="use-a-stand-alone-shift"></a>Nutzen einer eigenständigen Schicht

1.  Melden Sie sich am POS an.
2.  Wenn keine Schicht geöffnet ist, wählen Sie **Eine neue Schicht öffnen**.
3.  Wechseln Sie zum **Ausgangsbetrag deklarieren**-Vorgang, und geben Sie die Bargeldmenge an, die zu Beginn des Arbeitstags hinzugefügt wird.
4.  Führen Sie einige Transaktionen durch.
5.  Am Ende des Tages wählen Sie **Kassensturz**, um die Bargeldmenge aus der Kassenlade zu anzugeben.
6.  Geben Sie die Bargeldmenge ein, und klicken Sie dann auf **Speichern**, um die Angabe zu speichern.
7.  Wählen Sie **Schicht schließen**, um die Schicht zu schließen.

**Hinweis:** Andere während einer Schicht verfügbare Vorgänge sind von den vorhandenen Geschäftsprozessen abhängig. Die Vorgänge **Ablage in Tresor**, **Bankeinzahlung** und **Zahlungsmittel entfernen** können zur Entnahme von Bargeld während des Tages oder Vor dem Ende der Schicht genutzt werden. Wenn in einer Kassenlade kein Bargeld mehr vorhanden ist, kann über den Vorgang **Bareinlage** Bargeld hinzugefügt werden.

## <a name="shared-shifts"></a>Gemeinsame Schichten
Eine gemeinsame Schicht wird in einer Umgebung genutzt, in der mehrere Kassierer eine Kassenlade oder eine Reihe von Kassenladen während des Arbeitstags gemeinsam nutzen. Eine gemeinsame Schicht wird meist in mobilen POS-Umgebung verwendet. In einer mobilen Umgebung kann ein Kassierer nicht zu einer einzelnen Kassenlade zugeordnet werden und für diese verantwortlich sein. Stattdessen müssen alle Kassierer über die nächstliegende Kassenlade abrechnen können. In diesem Szenario gehören die gemeinsam genutzten Kassenladen zu einer gemeinsamen Schicht. Alle Kassenladen in einer gemeinsamen Schicht gehören in Bezug auf die Aktivitäten im Rahmen des Bargeldmanagements zur selben Schicht. Daher beträgt der Ausgangsbetrag für die Schicht die Summe alle Kassenladen aus der gemeinsamen Schicht. Auch der Kassensturz beträgt die Summe alle Kassenladen aus der gemeinsamen Schicht. **Hinweis:** Es kann nur eine gemeinsame Schicht pro Shop geöffnet werden. Gemeinsame Schichten und eigenständige Schichten können im gleichen Shop verwendet werden.

### <a name="set-up-a-shared-shift"></a>Einrichten einer gemeinsamer Schicht

1.  Klicken Sie auf **Einzelhandel und Handel** &gt; **Kanaleinrichtung** &gt; **POS-Einrichtung** &gt; **POS-Profile** &gt; **Hardwareprofile**.
2.  Wählen Sie das Hardwareprofil für die gemeinsame Schicht.
3.  Legen Sie auf dem **Kassenlade**-Inforegister die Option **Kassenladen für gemeinsame Schicht** auf **Ja** fest.
4.  Klicken Sie auf **Speichern**.
5.  Klicken Sie auf **Einzelhandel** &gt; **Kanaleinstellungen** &gt; **POS-Einstellungen** &gt; **Register**.
6.  Wählen Sie die Kasse, für die eine gemeinsame Schicht erforderlich ist, und klicken Sie dann auf **Bearbeiten**.
7.  Wählen Sie im Feld **Hardwareprofil** das Hardwareprofil aus, das Sie in Schritt 2 ausgewählt haben.
8.  Klicken Sie auf **Speichern**.
9.  Klicken Sie auf **Einzelhandel** &gt; **Handel IT** &gt; **Vertriebsplan**.
10. Wählen Sie den Vertriebsplan **1090**, und klicken Sie dann auf **Jetzt ausführen**, um die Änderungen mit dem POS zu synchronisieren.

### <a name="use-a-shared-shift"></a>Verwenden der gemeinsamen Schicht

1.  Melden Sie sich am POS an.
2.  Wenn der POS nicht mit einer Hardwarestation verbunden ist, wählen Sie **Kassenladenfremder Vorgang**, und wählen Sie dann den Vorgang **Hardwarestation auswählen**, um eine Hardwarestation für die gemeinsame Schicht zu aktivieren. Dieser Schritt muss nur beim ersten Hinzufügen einer Kasse zu einer Umgebung mit einer gemeinsamen Schicht ausgeführt werden.
3.  Melden Sie sich am POS ab und wieder an.
4.  Wählen Sie **Neue Schicht erstellen**.
5.  Wählen Sie **Ausgangsbetrag deklarieren**.
6.  Geben Sie den Ausgangsbetrag aller Kassenladen im Shop ein, die Teil der gemeinsamen Schicht sind. kklicken Sie dann auf **Speichern**.
    -   Um einen Teil des Ausgangsbetrags zu den einzelnen Kassenladen hinzuzufügen nutzen Sie den Vorgang **Hardwarestation wählen**. Stellen Sie sicher, dass die Hardwarestation aktiv ist.
    -   Um eine Geldlade zu einer bestimmten Kassenlade hinzufügen, verwenden Sie den Vorgang **Kassenlade öffnen**.
    -   Fahren Sie fort, bis alle Kassenladen in der gemeinsamen Schicht über den jeweiligen Ausgangsbetrag verfügen.

7.  Am Ende des Tages öffnen Sie jede Kassenlade und entfernen das Geld.
8.  Nachdem Sie das Geld aus der letzten Kassenlade entfernt haben, zählen Sie das Geld aus allen Kassenladen.
9.  Verwenden den Vorgang **Kassensturz**, um den Gesamtbetrag aus allen Kassenladen der gemeinsamen Schicht anzugeben.
10. Verwenden den Vorgang **Schicht schließen**, um die gemeinsame Schicht zu schließen.

## <a name="shift-operations"></a>Schichtvorgänge
Verschiedene Aktivitäten können ausgeführt werden, um den Status einer Schicht zu ändern oder um den Geldbetrag in der Schublade zu erhöhen oder zu verringern. Im Abschnitt unten werden dieses Schichtvorgänge für Dynamics 365 for Retail Modern POS und Cloud POS beschrieben.

**Offene Schichten**

POS erfordert, dass ein Benutzer keine aktive, offene Schicht hat, um alle möglichen Vorgänge auszuführen, die zu wertmäßiger Buchung wie Verkauf, Rücklieferung oder Kundenauftrag führen würde.  

Beim Anmelden bei POS prüft das System zuerst, um zu sehen, ob beim Benutzer eine aktive Schicht in der aktuellen Erfassung vefügbar ist. Falls nicht, kann der Benutzer dann wählen, um eine neue Schicht zu öffnen, setzt eine vorhandene oder Nachtschicht fort oder meldet sich beim "Nicht-Konfromen" Modus an, abhängig von der Systemkonfiguration und ihren Berechtigungen.

**Ausgangsbetrag deklarieren**

Dieser Vorgang ist häufig die erste Aktivität, die bei einer neu geöffneten Schicht vorgenommen wird. Benutzer geben den Anfangsbarbetrag in der Schublade für die Schicht an. Dies ist wichtig, da die Über-/Fehlberechnung, die beim Abschluss einer Schicht erfolgt, diesen Betrag berücksichtigt.

**Mittelzugang**

Angebotsentfernungen sind Nichtverkaufstransaktionen, die in einer aktiven Schicht ausgeführt werden, um die Menge des Bargelds in der Schublade zu reduzieren. Ein allgemeines Beispiel für einen Float-Eintrag wäre es, zusätzliche Änderung dem Wechselaussteller hinzufügen, wenn die Ausführung gering ist.

**Zahlungsmittel entfernen**

Angebotsentfernungen sind Nichtverkaufstransaktionen, die in einer aktiven Schicht ausgeführt werden, um die Menge des Bargelds in der Schublade zu reduzieren. Dies wird am häufigsten in Verbindung mit einem Mittelzugang bei einer anderen Schicht verwendet. Beispielsweise wird Register 1 gering auf Änderung ausgeführt, so führt der Benutzer 2 im Register ein sanftes Entfernen aus, um den Betrag zu reduzieren. Der Benutzer in der Erfassung 1 würde dann einen Mittelzugang ausführen, um den Betrag zu erhöhen.

**Schicht aussetzen**

Benutzer können ihre aktive Schicht unterbrechen, um die aktuelle Erfassung für einen anderen Benutzer freizugeben oder um ihre Schicht in eine andere Erfassung zu verschieben (dies wird oft als „gleitende Kassenlade” bezeichnet). 

Das Unterbrechen der Schicht verhindert, dass irgendwelche neuen Transaktionen oder Änderungen an der Schicht vorgenommen werden, bis sie wieder fortgesetzt wird.

**Schicht fortsetzen**

Dieser Vorgang ermöglicht es einem Benutzer, eine zuvor unterbrochene Schicht in einer Erfassung wieder aufzunehmen, die noch keine aktive Schicht hat.

**Kassensturz**

Der Kassensturz ist die Aktivität, die der Benutzer vornimmt, um den Betrag des gesamten Geldes anzugeben, das sich aktuell in der Schublade befindet, meistens vor Abschluss der Schicht. Dies ist der Wert, der gegenüber der erwarteten Schicht verglichen wird, um den Über-/Fehlbetrag zu berechnen.

**Ablage in Tresor**

Ablagen im Tresor können jederzeit in einer aktiven Schicht ausgeführt werden. Durch diesen Vorgang wird Geld aus der Schublade entfernt, sodass es an einen sichereren Ort übertragen werden kann, wie beispielsweise einen Tresor im Hinterzimmer. Der Gesamtbetrag, der für Ablagen im Tresor erfasst ist, ist immer noch in den Schichtsummen enthalten. Er muss jedoch nicht als Teil des Kassensturzes gezählt werden.

**Bankeinzahlung**

Wie Ablagen in Tresor, werden auch Bankeinzahlungen auf aktiven Schichten ausgeführt. Durch diesen Vorgang wird Geld aus der Schicht entfernt, um es für die Bankeinzahlung vorzubereiten.

**Schicht blind schließen**

Eine blinde geschlossene Schicht ist eine Schicht, die nicht mehr aktiv ist, jedoch noch nicht vollständig geschlossen wurde. Geschlossene Schichten können nicht als eine Schicht unterbrochen werden, aber Verfahren wie Anfangsbeträge und Angebote können zu einem späteren Zeitpunkt oder von einem anderen Register erfasst werden.

Geschlossene Schichten werden häufig verwendet, um ein Register für einen neuen Benutzer oder eine Schicht freizugeben, ohne diese Schicht zu zählen, abzustimmen und vollständig beenden zu müssen. 

**Schicht schließen**

Dieser Vorgang berechnet Schichtsummen, Über-/Fehlbeträge und schließt dann eine aktive oder blinde geschlossene Schicht ab. Abgeschlossene Schichten können nicht fortgesetzt oder geändert werden.  

**Schichten verwalten**

Dieser Vorgang ermöglicht es Benutzern, alle aktiven, unterbrochenen und blinden geschlossenen Schichten für die Filiale anzuzeigen. Abhängig von den Berechtigungen können Benutzern die endgültig Abschlussprozedur wie Deklaration und Schichten beenden selber vornehmen. Dieser Arbeitsgang ermöglicht es auch Benutzern, ungültige Schichten anzuzeigen und zu löschen, und zwar im seltenen Fall, in dem eine Schicht in einem schlechten Zustand zurückbleibt, nachdem zwischen Offline- und Onlinemodi umgeschaltet wurde. Diese ungültigen Schichten enthalten keine finanziellen Informationen oder Buchungsdaten, die für die Abstimmung erforderlich sind. 

