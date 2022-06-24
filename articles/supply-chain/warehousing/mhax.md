---
title: Schnittstelle für Materialhandhabung (MHAX)
description: In diesem Artikel wird beschrieben, wie Sie die Schnittstelle für Materialhandhabungsgeräte (MHAX) festlegen, damit Sie eine Verbindung zu externen physischen Systemen für die Materialhandhabung (MH) herstellen können.
author: Mirzaab
ms.date: 03/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WMHEParameters, WMHESubscription, WMHEQueueManagerWorkspace, WMHEInboundQueue, WMHEOutboundQueue
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-04
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: c4b0d991d320d5a679d0ed60880c56a6cb849e2d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907086"
---
# <a name="material-handling-equipment-interface-mhax"></a>Schnittstelle für Materialhandhabung (MHAX)

[!include [banner](../../includes/banner.md)]

Sie können die *Materialhandhabungsgeräte-Schnittstelle* (MHAX) verwenden, um externe physische Materialhandhabungs-Systeme (MH) mit einem Lagerort zu verbinden, der von der erweiterten Lagerortverwaltung (WMS) in Microsoft Dynamics 365 Supply Chain Management verwaltet wird. Die Schnittstelle zwischen den WMS- und MH-Systemen besteht aus zwei Warteschlangen: eine für ausgehende Ereignisse (WMS zu MH) und eine für eingehende Ereignisse (MH zu WMS). Das WMS-System generiert ausgehende Ereignisse auf der Basis von Arbeitszeilen, die bei verschiedenen Prozessen der Arbeitserstellung und -ausführung erstellt werden. Das MH-System fragt dann regelmäßig das WMS-System nach neuen Ereignissen ab und verarbeitet die Antworten. Nachdem das MH-System die Ereignisse gemäß den Arbeitsanweisungen abgearbeitet hat, sendet es eingehende Ereignisse, wie z. B. die Beendigung von Arbeitszeilen und die Kurzkommissionierung.

Die folgende Abbildung zeigt die verschiedenen Elemente und die Reihenfolge, in der Prozesse ablaufen, wenn Sie die MHAX-Integration verwenden.

![MHAX-Komponenten und Interaktionen.](media/mhax-components.png "MHAX-Komponenten und Interaktionen")

Hier ist eine Erklärung der Interaktionen, die in der vorherigen Abbildung gezeigt werden:

1. Während der Arbeitserstellung oder Arbeitsausführung werden ausgehende Ereignisse in der Ausgangswarteschlange erstellt.
2. Das MH-Gerät verbindet sich mit dem MH-Gerätedienst, fragt nach neuen Ereignissen ab, die für es relevant sind, und verarbeitet diese Ereignisse.
3. Wenn das MH-Gerät bereit ist, Bericht zu erstatten, verbindet es sich erneut mit dem Dienst und sendet eingehende Ereignisse. Diese Ereignisse werden sofort vom Warteschlangen-Prozessor verarbeitet.
4. Basierend auf den eingehenden Ereignissen kann der Warteschlangen-Prozessor bereits vorhandene Arbeit ausführen, sie ändern oder neue Arbeit erstellen.

## <a name="turn-on-the-mhax-feature"></a>Einschalten der MHAX-Funktion

Bevor Sie die MHAX-Funktion verwenden können, müssen Sie sowohl die Funktion als auch den Konfigurationsschlüssel einschalten.

1. Wechseln Sie zu **Systemverwaltung \> Arbeitsbereiche \> Funktionsverwaltung**.
2. Schalten Sie im Arbeitsbereich **[Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** die Funktion mit dem Namen *Schnittstelle für Materialhandhabung* ein.
3. Legen Sie Ihr System in den Wartungsmodus ein, wie in [Wartungsmodus](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) beschrieben.
4. Gehen Sie zu **Systemadministration \> Einrichten \> Lizenzkonfiguration**.
5. Erweitern Sie **Gewerbe \> Lagerort- und Transportverwaltung**, und aktivieren Sie dann das Kontrollkästchen **Schnittstelle für Materialhandhabung**.
6. Schalten Sie den Wartungsmodus aus, wie in [Wartungsmodus](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) beschrieben.

## <a name="set-mhax-parameters"></a>MHAX-Parameter festlegen

Um die Funktion zu konfigurieren, müssen Sie einige allgemeine Parameter auf der Seite **Materialhandhabungsgeräte-Schnittstelle Parameter** festlegen.

1. Gehen Sie auf die Seite **Schnittstelle für Materialhandhabung \> Einrichten \> Schnittstellenparameter für Materialhandhabung**.
2. Legen Sie auf der Registerkarte **Allgemein** die folgenden Felder fest:

    - **Benutzer-ID** - Wählen Sie eine Arbeitskraft aus. Diese Arbeitskraft wird verwendet, um alle Arbeitsvorgänge (Entnehmen und Einlagern) auszuführen, die über die eingehende Warteschlange verarbeitet werden.
    - **Eingehende Nachrichten-ID aktivieren** - Wenn diese Option auf *Ja* festgelegt ist, wird bei einer doppelten eingehenden Nachrichten-ID die Nachricht abgelehnt und eine Fehlermeldung gibt an, dass die Nachricht bereits existiert. Wenn diese Option auf *Nein* festgelegt ist, werden doppelte eingehende Nachrichten-IDs zugelassen.

3. Wählen Sie auf der Registerkarte **Nummernkreis** die systemweiten Nummernkreise aus, die verwendet werden sollen, um eindeutige IDs für die eingehenden Artikel der Warteschlange, die ausgehenden Artikel der Warteschlange und die Arbeitslinienpaare zu erzeugen.

## <a name="outbound-events"></a>Ausgehende Ereignisse

An bestimmten Punkten während der Work-Erstellung oder Work-Ausführung bestimmt das System, ob es ausgehende Ereignisse erzeugen muss, um sie an das MH-System zu senden. Wenn ein Abonnement für einen bestimmten Punkt während der Lagerort-Verarbeitung konfiguriert ist, generiert das System das Ereignis entsprechend der Einrichtung des Abonnements.

### <a name="structure-of-outbound-events"></a>Struktur der ausgehenden Ereignisse

Jedes ausgehende Ereignis wird durch eine Ausgangswarteschlangen-ID eindeutig identifiziert. Die Art der ausgehenden Transaktion bestimmt die Art des Ereignisses. Der Lagerort und die ID des Abonnements, das das Ereignis erzeugt hat, werden ebenfalls auf dem Ereignis vermerkt.

Um Daten an das MH-System zu übertragen, enthält das ausgehende Ereignis 10 Datenfelder (**data01** bis **data10**). Diese Datenfelder haben eine eins-zu-eins (1:1) Zuordnung zu bestehenden Datenbankfeldern. Genauer gesagt werden sie aus Feldern in den Tabellen „Arbeitszeile“ und „Arbeitskopf“ extrahiert. Die Felder sind frei wählbar. Sie legen sie fest, wenn Sie das Abonnement erstellen.

Neben den 10 Datenfeldern, die eine 1:1 Zuordnung zu bestehenden Datenbankfeldern haben, kann das Ereignis ein zusätzliches Datenfeld enthalten, das als *Payload* bezeichnet wird. Der Inhalt dieses Feldes wird durch benutzerdefinierten X++ Code generiert, der als *Payload-Generator* bezeichnet wird. Ein beliebiger Payload-Generator, der verwendet werden soll, wird im Abonnement festgelegt.

Um sicherzustellen, dass das MH-System jede Ausgangswarteschlange-ID nur einmal erhält, wird ein Statusfeld verwendet, um anzugeben, ob ein Ereignis bereit ist, an das externe System gesendet zu werden, oder ob es bereits gesendet wurde.

### <a name="outbound-queue-subscriptions"></a>Ausgehende Warteschlangen-Abonnements

Bevor Ereignisse generiert werden, muss ein Abonnement festgelegt werden, das der Funktion MHAX mitteilt, ob und wie Ereignisse generiert werden sollen. Erstellte Ereignisse werden mit der Abonnement-Kennung versehen. Daher können sich mehrere MH-Systeme mit demselben WMS-System verbinden, aber ihre Ereignisse getrennt halten. Wenn der MHAX-Dienst nach neuen Ereignissen abgefragt wird, ist ein Abonnement eine der verfügbaren Optionen zum Abrufen der Ereignisse.

Um ein Abonnement zu erstellen, gehen Sie zu **Schnittstelle für Materialhandhabung \> Einrichten \> Abonnements**. Für jedes Abonnement sind die folgenden Parameter verfügbar:

- **Abonnement-ID** - Ein eindeutiger Name, der das Abonnement identifiziert.
- **Beschreibung** - Eine Freitextbeschreibung des Abonnements.
- **Lagerort** - Die spezifischen Lagerorte, nach denen Ereignisse gefiltert werden sollen.
- **Typ der ausgehenden Transaktion** - Die Art der Ereignisse, die das Abonnement enthalten soll.
- **Payload-Generator** - Eine optionale Code-Erweiterung, die zusätzliche Informationen in das Feld **Payload** des ausgehenden Ereignisses eingeben kann.

Mit jedem Abonnement kann eine Abfrage verknüpft werden. Diese Abfrage filtert Arbeitszeilen und Kopfzeilen, um die Arbeit, die das Abonnement zur Erzeugung von Ereignissen verwendet, weiter einzuschränken. Um eine Abfrage zu einem Abonnement hinzuzufügen, aktivieren Sie das Kontrollkästchen **Abfrage ausführen** für das betreffende Abonnement auf der Seite **Abonnements** und wählen dann **Abfrage bearbeiten** im Aktivitätsbereich. Der Standard-Abfrage-Editor von Supply Chain Management wird angezeigt.

Zusätzlich enthält das Abonnement eine *Abonnement-Zuordnung*, die Felder aus dem Arbeitskopf oder der Arbeitszeile je nach Bedarf einigen oder allen der 10 freien Datenfelder des ausgehenden Ereignisses zuordnet. Um Informationen an den MHAX-Dienst zurückzugeben, werden Sie typischerweise die Datensatz-ID der Arbeitszeile oder die *Arbeitszeilen-Paar-ID* angeben. (Die Arbeitszeilenpaar-ID ist eine neue Eigenschaft, die es dem System ermöglicht, einen einzigen Rückgabebefehl zu verwenden, um Zeilen zu entnehmen und einzulagern.) Die übrigen Felder hängen vom Anwendungsfall ab. Einige Beispiele finden Sie weiter unten in diesem Artikel.

Um eine Zuordnung festzulegen, wählen Sie auf der Seite **Abonnements** das betreffende Abonnement aus und wählen dann im Aktivitätsbereich **Abonnementzuordnung**. Im erscheinenden Dialogfenster **Abonnement-Map** können Sie für jedes verfügbare Datenfeld eine Tabelle und ein Feld nach Bedarf zuordnen.

### <a name="outbound-event-types"></a>Ausgehende Ereignistypen

Dieser Abschnitt beschreibt die verschiedenen Ereignistypen, die zur Verfügung stehen. (Ereignistypen werden auch als *Transaktionstypen* bezeichnet.) Er erklärt auch, wann jeder Ereignistyp im WMS-System erstellt wird.

#### <a name="work-creation-events"></a>Ereignisse zur Arbeitserstellung

Ereignisse zur Arbeitserstellung werden erstellt, nachdem die Arbeit von der Anwendung erzeugt wurde. Dieses Verhalten gilt für die meisten Arten von Arbeitserstellungsprozessen, vor allem für die Erstellung von Kommissionierungs- und Wiederbeschaffungsarbeiten. Allgemein gilt: Wenn eine Arbeit in einem *Offen* Status erstellt wird, der anzeigt, dass die Arbeit bereit ist, von einer Arbeitskraft ausgeführt zu werden, wird ein Arbeitserstellungs-Ereignis erzeugt. Außerdem werden Ereignisse zur Arbeitserzeugung für grundlegende Bewegungsarbeit (nicht für Bewegung durch Vorlagenarbeit) erzeugt, auch wenn diese Arbeit nicht als offene Arbeit erstellt wird.

Eine bemerkenswerte Ausnahme von diesem Verhalten ist Zykluszählarbeit, die derzeit nicht unterstützt wird. Bestandszählungen im MH-System liegen außerhalb des Anwendungsbereichs von MHAX, und die Ergebnisse von Zählungen müssen in ein Bestandszählungserfassung importiert werden.

Nachdem Arbeit erstellt wurde, verarbeitet der MHAX-Dienst die erzeugten Arbeitszeilen und ordnet allen erzeugten Arbeitszeilen für jeden Arbeitskopf eine Arbeitszeilenpaar-ID zu. Ziel ist es, alle Zeilen der Entnahmearbeiten mit den aufeinanderfolgenden Einlagerungen unter einer Arbeitszeilenpaar-ID zu gruppieren. (Die Gruppen entsprechen den Entnahme-/Einlagerungspaaren in Arbeitsvorlagen.) Auf diese Weise kann eine einzige ID verwendet werden, um den Arbeitsabschluss für alle zusammenhängenden Entnahme- und Einlagerungszeilen zu melden. Der Gruppierungsprozess beginnt mit der ersten Zeile und wird dann mit der gleichen ID fortgesetzt, bis er auf ein aufeinanderfolgendes Paar von Einlagerungs-/Entnahme-Arbeitszeilen trifft. Die laufende ID wird der eingelagerten Zeile dieses Paares zugewiesen. Eine neue ID wird dann für die entnehmende Zeile dieses Paares verwendet. Dieser Prozess wird fortgesetzt, bis alle Zeilen, die zum Arbeitskopf gehören, verarbeitet wurden.

Als besondere Funktion von Ereignissen der Arbeitserzeugung, wenn die Option **Blockierte Welle** auf dem Arbeitskopf auf *Ja* festgelegt ist, haben die erzeugten Ereignisse einen Status von *Blockiert* anstelle des üblichen Status von *Bereit*, mit dem sie an das MH-System gesendet werden. Das Flag **Blockierte Welle** auf dem Arbeitskopf zeigt an, dass der Arbeitskopf noch nicht für die Arbeitskräfte bereit ist, vielleicht wegen nicht abgeschlossener Wiederbeschaffung. Wenn das Flag **Blockierte Welle** gelöscht wird, werden Ereignisse, die bereits generiert wurden, entsperrt und stehen dem MH-System zum Abrufen aus der Warteschlange zur Verfügung.

#### <a name="work-initiation-events"></a>Ereignisse zur Arbeitseinleitung

Arbeitseinleitungsereignisse werden ausgelöst, wenn der Arbeitsstatus während der Arbeitsaktualisierung von *Offen* auf *In Bearbeitung* wechselt.

#### <a name="work-completion-events"></a>Arbeitsabschluss-Ereignisse

Arbeitsabschluss-Ereignisse werden ausgelöst, wenn der Arbeitsstatus während der Arbeitsaktualisierung von *In Bearbeitung* zu *Geschlossen* wechselt.

#### <a name="work-cancellation-events"></a>Ereignisse bei Arbeitsabbruch

Arbeitsabbruch-Ereignisse werden ausgelöst, wenn sich der Arbeitsstatus während der Arbeitsaktualisierung von einem beliebigen Status außer *Abgebrochen* auf *Abgebrochen* ändert. Außerdem werden alle anderen Ereignisse, die sich auf den Arbeitskopf beziehen, für alle Abonnements aus der Warteschlange gelöscht. Auf diese Weise wird verhindert, dass externe Systeme Ereignisse verarbeiten, die nicht benötigt werden.

#### <a name="pickput-completion-events"></a>Ereignisse für den Abschluss des Entnehmens/Einlegens

Ereignisse zum Entnehmen/Einlagern werden ausgelöst, wenn der Status der Zeile zum Entnehmen/Einlagern während der Aktualisierung der Arbeitszeile von *In Bearbeitung* auf *Geschlossen* wechselt.

### <a name="monitor-the-outbound-queue"></a>Überwachen der ausgehenden Warteschlange

Um die ausgehende Warteschlange zu überwachen, gehen Sie auf **Schnittstelle für Materialhandhabung \> Allgemein \> Ausgehende Warteschlange**. Die Seite **Ausgangs-Warteschlange** listet jeden Artikel der ausgehenden Warteschlange und seinen Status auf. Wählen Sie einen Artikel in der Warteschlange aus, um seine Details zu sehen. Diese Details umfassen den Transaktionstyp des Artikels, das verwendete Abonnement und Werte für jedes Datenfeld (**data01** bis **data10**) sowie die Payload.

### <a name="clean-up-the-outbound-queue"></a>Bereinigen der ausgehenden Warteschlange

Mit der Zeit wird sich Ihre ausgehende Warteschlange mit Artikeln füllen, die bereits versendet worden sind. Um diese Artikel zu entfernen, gehen Sie zu **Schnittstelle der Materialhandhabung \> Periodische Aufgaben \> Bereinigung \> Bereinigung der ausgehenden Warteschlange**.

## <a name="inbound-events"></a>Eingehende Ereignisse

Dieser Abschnitt beschreibt die verschiedenen Arten von eingehenden Ereignissen, die das MH-System an das WMS-System zurückmelden kann. Es wird auch erklärt, welche Daten vom MH-System geliefert werden müssen und was jedes eingehende Ereignis im WMS-System bewirkt.

### <a name="structure-of-inbound-events"></a>Struktur von eingehenden Ereignissen

Wenn ein eingehendes Ereignis gesendet wird, muss das externe System den Typ der eingehenden Transaktion zusammen mit bis zu 10 Parametern liefern (**data01** bis **data10**). Durch eine optionale Validierung kann sichergestellt werden, dass der MHAX-Dienst dasselbe eingehende Ereignis nicht mehr als einmal erhalten hat. Um diese Validierung zu aktivieren, muss jedes eingehende Ereignis eine eindeutige Nachrichten-ID haben. Wenn eine doppelte Nachrichten-ID empfangen wird und die Option **Eingehende Nachrichten-ID aktivieren** auf der Seite **Schnittstellenparameter für Materialhandhabung** auf *Ja* festgelegt ist, wird die Nachricht zurückgewiesen. In einer Fehlermeldung wird angegeben, dass die Nachricht bereits existiert.

Zusätzlich zu den eingehenden Datenfeldern ordnet das System dem Ereignis eine eindeutige ID der eingehenden Warteschlange zu.

### <a name="inbound-event-types"></a>Eingehende Ereignistypen

Dieser Abschnitt beschreibt die eingehenden Ereignistypen (Transaktionstypen), die unterstützt werden, und die Daten, die für die Verarbeitung der Ereignisse bereitgestellt werden müssen.

#### <a name="work-confirm-events"></a>Ereignisse zur Arbeitsbestätigung

Ereignisse zur Arbeitsbestätigung erfordern, dass die eingehenden Datenfelder die folgenden Informationen enthalten:

- **data01** - Die ID des Arbeitslinienpaares.
- **data02** - Die Arbeitszeilen-Datensatz-ID (Wert `RecId`).

    > [!NOTE]
    > *Es muss entweder* das Feld **data01** *oder* das Feld **data02** vorhanden sein.

- **data03** - Die ID des Ladungsträgers, der entnommen werden soll.
- **data04** - Die ID des Ziel-Ladungsträgers des Arbeitskopfes.

Wenn die ID des Arbeitszeilenpaares angegeben wird, werden alle Entnahme-, Einlagerungs- oder benutzerdefinierten Arbeitszeilen, die durch die ID des Arbeitszeilenpaares markiert sind und den Status *Offen* oder *In Bearbeitung* haben, nacheinander ausgeführt. Wenn eine Arbeitslinien-Datensatz-ID (Wert `RecId`) angegeben ist, muss die Arbeitslinie eine Entnahme-, Einlagerungs- oder benutzerdefinierte Arbeitslinie sein, die den Status *Offen* oder *In Bearbeitung* hat.

Bei Entnahmezeilen von Ladungsträgern von Lagerplätzen muss **data03** das Nummernschild angeben, von dem entnommen werden soll, unabhängig davon, ob die Zeilen durch die Arbeitszeilen-Datensatz-ID oder die Arbeitszeilen-Paar-ID gekennzeichnet sind. Das Feld **data04** muss das Zielkennzeichen des Arbeitskopfes für die Entnahme angeben.

Eingelagerte Zeilen nehmen keine weiteren Informationen an. Sie werden nur auf der Basis des Lagerplatzes der aktuellen Zeile und des Ziel-Ladungsträgers des Werks ausgeführt. Wenn das Einlagern an einem anderen Lagerplatz erfolgen muss, ändern Sie den Lagerplatz der Arbeitslinie wie im Abschnitt [Ereignisse außer Kraft setzen](#override-events) weiter unten in diesem Artikel beschrieben.

Benutzerdefinierte Arbeitslinien erfordern oder unterstützen keine zusätzlichen Informationen im eingehenden Ereignis.

#### <a name="short-pick-events"></a>Kurzes Entnehmen von Ereignissen

Kurze Ereignisse zum Entnehmen von Daten erfordern, dass die eingehenden Datenfelder die folgenden Informationen enthalten:

- **data02** - Die ID des Arbeitsdatensatzes (Wert `RecId`).
- **data03** - Die ID des Ladungsträgers, der entnommen werden soll.
- **data04** - Die zu entnehmende Menge.
- **data05** - Der kurze Ausnahmecode für die Kommissionierung.
- **data06** - Die Ziel-Ladungsträger-ID des Arbeitskopfes.

> [!NOTE]
> Das Feld **data01** wird bei Ereignissen mit kurzer Entnahme nicht verwendet.

Dieses Ereignis ähnelt dem Arbeitsbestätigungs-Ereignis, aber es gilt nur für Pick-Zeilen.

#### <a name="override-events"></a><a id="override-events"></a>Override-Ereignisse

Override-Ereignisse erfordern, dass die eingehenden Datenfelder die folgenden Informationen enthalten:

- **data01** - Die ID des Arbeitsdatensatzes (Wert `RecId`).
- **data02** - Die ID des neuen Lagerplatzes.

Die Arbeitszeile muss entweder den Status *Offen* oder *In Bearbeitung* haben und der neue Lagerplatz muss existieren.

#### <a name="license-plate-receipt-events"></a>Ereignisse für den Empfang von Ladungsträgern

Ereignisse zum Empfang von Ladungsträgern erfordern, dass die eingehenden Datenfelder die folgenden Informationen enthalten:

- **data01** - Die ID des eingehenden Ladungsträgers, der empfangen werden soll.

Das System führt einen Kennzeichen-Empfangsvorgang durch, basierend auf dem Ladungsträger, der als Wert des Feldes **data01** übergeben wird.

### <a name="monitor-the-inbound-queue"></a>Überwachen der eingehenden Warteschlange

Um die eingehende Warteschlange zu überwachen, gehen Sie auf **Schnittstelle für Materialhandhabung \> Allgemein \> Eingehende Warteschlange**. Die Seite **Eingangswarteschlange** listet jeden eingehenden Artikel und seinen Status auf. Wählen Sie einen Artikel in der Warteschlange aus, um seine Details zu sehen. Diese Details umfassen den Transaktionstyp des Artikels, die Nachrichten-ID und Werte für jedes Datenfeld (**data01** bis **data10**).

Wenn bei der Verarbeitung eingehender Ereignisse ein Fehler oder ein anderer Typ von Artikel aufgetreten ist, können Sie das Protokoll einsehen, indem Sie **Fehlerprotokoll** im Aktivitätsbereich wählen.

### <a name="inbound-event-processing"></a>Verarbeitung eingehender Ereignisse

Eingehende Ereignisse werden zunächst in die Datenbank geschrieben und dann sofort (synchron) ausgeführt. Wenn während der Verarbeitung ein Fehler auftritt, wird das Ereignis trotzdem in die Warteschlange geschrieben, aber der Status wird auf *Errored* festgelegt. Der MHAX-Dienst gibt eine Fehlermeldung an das MH-System zurück und speichert das Fehlerprotokoll im eingehenden Ereignissatz zur späteren Untersuchung.

Ereignisse, die den Status *Errored* haben, können später erneut verarbeitet werden, wenn der Fehlerzustand behoben ist. Um sie erneut zu verarbeiten, führen Sie einen der folgenden Schritte aus:

- Gehen Sie zu **Schnittstelle für Materialhandhabung \> Allgemeine \> Eingehende Warteschlange**. Wählen Sie die entsprechende eingehende Warteschlange aus und wählen Sie dann **Wiederverarbeiten** im Aktivitätsbereich.
- Gehen Sie auf **Materialhandhabung Schnittstelle \> Allgemein \> Fehlerhafte eingehende Warteschlange neu verarbeiten**. Es erscheint ein Standard-Dialogfeld für Batch-Jobs. Dort können Sie einen Datensatzfilter festlegen und einen Batch-Job planen oder ausführen, um die Warteschlange erneut zu verarbeiten.

Alle Arbeitsvorgänge (Entnehmen und Einlagern) werden unter Verwendung der Arbeitskraft ausgeführt, die im Feld **Benutzer-ID** auf der Seite **Schnittstellenparameter der Materialhandhabung** ausgewählt ist.

### <a name="clean-up-the-inbound-queue"></a>Aufräumen der eingehenden Warteschlange

Mit der Zeit wird sich Ihre eingehende Warteschlange mit Artikeln füllen, die bereits verarbeitet wurden. Um diese Artikel zu entfernen, gehen Sie zu **Schnittstelle für Materialhandhabung \> Periodische Aufgaben \> Bereinigung \> Bereinigung der eingehenden Warteschlange**.

## <a name="get-a-quick-overview-by-using-the-queue-manager"></a>Verschaffen Sie sich einen schnellen Überblick mit Hilfe des Warteschlangenmanagers

Um einen schnellen Überblick über alle Aktivitäten zu erhalten, die sich auf Ihre eingehenden und ausgehenden Warteschlangen beziehen, gehen Sie zu **Schnittstelle für Materialhandhabung \> Arbeitsbereiche \> Warteschlangen-Manager**. Die Seite **Warteschlangen-Manager** bietet eine Reihe von Registern und Kacheln, mit denen Sie Ihre Warteschlangen überwachen und erkunden können. Sie bietet auch nützliche Links zu den meisten anderen Seiten, die in diesem Artikel erwähnt werden.

## <a name="connect-to-the-mhax-service"></a>Verbinden mit dem MHAX-Dienst

MHAX ist als benutzerdefinierter Dienst implementiert. Daher ist er über SOAP- und REST-Aufrufe zugänglich. Hier sind die Adressen der SOAP- und REST-Endpunkte:

- **SOAP:** `https://base_environment_URL/soap/services/WMHEServices`
- **REST:** `https://base_environment_URL/api/services/WMHEServices/WMHEService`

## <a name="retrieve-messages-from-the-outbound-queue"></a>Abrufen von Nachrichten aus der ausgehenden Warteschlange

Um Nachrichten aus der ausgehenden Warteschlange abzurufen, verwenden Sie eine der folgenden Methoden:

- Verwenden Sie `readOutboundSubscriptionQueue`, um die Ereignisse basierend auf der Abonnement-ID abzurufen.
- Verwenden Sie `readOutboundWarehouseQueue`, um die Ereignisse basierend auf dem Ereignistyp und der Lagerort-ID über mehrere Abonnements abzurufen.
