---
title: Einstellungen und Arbeiten mit Callcenterbetrugswarnungen
description: In diesem Thema wird erläutert, wie Regeln eingerichtet werden, um Kundendienstmitarbeiter vor möglicherweise gefälschten Informationen zu warnen, wenn Aufträge verarbeitet werden. Sie können auch spezielle Codes definieren, die verwendet werden, um automatisch oder manuell verdächtige Aufträge zu sperren.
author: josaw1
manager: AnnBe
ms.date: 05/14/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: SalesPostingHistory, MCRHoldCodeTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 79103
ms.assetid: e342af8d-7498-4d20-8483-ab368429c578
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 38649e40021d1caaf70f217b3ebae0d488806180
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4412644"
---
# <a name="set-up-and-work-with-call-center-fraud-alerts"></a>Einstellungen und Arbeiten mit Callcenterbetrugswarnungen

[!include [banner](includes/banner.md)]

In diesem Thema wird erläutert, wie Sie Kriterien und Regeln einrichteten ,um potenziell gefälschte Aufträge für weitere Prüfung gesperrt zu halten. Betrugsprüfungsfunktionen werden verwendet, um die Gültigkeit von Informationen in einen Auftrag zu bestimmen. Wenn die Informationen im Auftrag auf Grundlage der Betrugskriterien und -Regeln einer Organisation fraglich erscheinen, kann der Auftrag für weitere Prüfung durch einen Administrator gesperrt werden. In diesem Fall kann der Auftrag nicht für den Lagerort für das spätere Verarbeiten freigegeben werden, nachdem die Sperre deaktiviert wurde.

> [!NOTE]
> Diese Funktion kann nur mit der Auftragsverarbeitung für den Commerce Callcenter-Kanal verwendet werden.

## <a name="turning-on-the-fraud-check-feature"></a>Aktiviert die Betrugsüberprüfungsfunktion

Um die Betrugsscheckfunktion zu verwenden, müssen Sie die Option **Aktivieren Sie Auftragsabschluss** im Kanal auf **Ja** festlegen, wenn der Callcenterkanal [ist](https://docs.microsoft.com/dynamics365/unified-operations/retail/set-up-order-processing-options). Wenn Auftragsabschluss aktiviert ist, müssen Callcenterbenutzer auf der Seite Auftrag **Vollständig** auswählen für alle Aufträge, die erstellt werden. Die vollständige Aktivität hat zur Folge, dass die Seite **Auftragszusammenfassung** geöffnet wird. Nachdem Benutzer die obligatorischen Zahlungsdaten auf der Seite **Auftragszusammenfassung** eingeben haben, wählen Sie **Übermitteln**, um den Auftrag einrichten. Wenn der Auftrag übermittelt wird, wird die Betrugsscheckfunktion ausgelöst, und alle Regeln, die im System aktiv sind, werden automatisch geprüft.

Callcenterbenutzer können Aufträge für Betrugsprüfung auch manuell sperren, bevor sie **Übermitteln** wählen. Um einen Auftrag, auf der Seite **Auftragszusammenfassung** manuell zu sperren, wählen Sie **Anhalten** \> **Manueller Betrugsstopp** aus. Sie werden aufgefordert, dann einen Kommentar einzugeben, um den Grund für das Sperren des Auftrags darzulegen. Dieser Kommentar erscheint unter [Auftragsstopp](https://docs.microsoft.com/dynamics365/unified-operations/retail/work-with-order-holds), um dem Benutzer den Kontext anzugeben, der den Auftrag berprüft, der gestoppt wurde, um zu bestimmen, ob der Auftrag freigegeben werden soll.

Zusätzlich zur Konfiguration der Option **Auftragabschluss aktivieren** im Kanal müssen Sie die Betrugsprüffunktion in den Callcenter-Parametern konfigurieren.  Gehen Sie zu **Retail und Commerce** \> **Kanaleinstellung** \> **Callcenter-Einrichtung** \> **Callcenter-Parameter**. Auf der Seite **Callcenterparameter** auf der Registerkarte **Sperren**, setzen Sie die  **Betrugsscheck** Option auf **Ja**.

Auf der Registerkarte **Sperren** können Sie auch [Codes halten](https://docs.microsoft.com/dynamics365/unified-operations/retail/work-with-order-holds) definieren, die für einen Aftrag angewendet werden, der entweder manuell oder automatisch für Betrugsprüfung gesperrt wird. Legen Sie die Haltecodes in den Feldern **Betrughaltecode manuell** und **Betrugshaltecode** fest. Sie finden es möglicherweise hilfreich, zwei eindeutige Haltecodes zu erstellen, damit Benutzer, die Workbench Sperre arbeiten, einfach automatische Sperren von manuellen Sperrren unterscheiden können.

Damit die Betrugssperrfunktion effektiv ist, müssen Sie das Feld **Minimale Punktzahl** festlegen. Jedes Betrugskriterium und - regel, die im System definiert wird, besitzt eine Bewertung. Wenn ein Auftrag für Betrugsabgleichungen geprüft wird, wenn mindestens Übereinstimmungen gefunden werden, werden die Punktzahlen zusammen hinzugefügt, um dem Auftrag eine gesamte Betrugspunktzahl zu geben. Wenn die gesamte Betrugspunktzahl für einen Auftrag den Wert **Minimale Punktzahl** überschreitet, wird der Auftrag automatisch gesperrt. Sie können optional die anderen punktebezogenen Felder auf der Registerkarte **Sperren** nutzen, um die E-Mail-Punktzahl, die Telefonnummer-Punktzahl, die Postleitzahl-Punktzahl und die erweiterte Postleitzahlpunktzahl zu definieren. Wird keine Punktzahl für ein statisches Betrugskriterien angeben, wenn Sie diese auf der Seite **Statische Betrugsdaten** festlegen, wird sie das System bewerten, indem es die Standardpunktzahlen verwendet, die Sie auf der Registerkarte **Sperren** auf der Seite **Callcenterparameter** definieren.

Schließlich verwenden Sie das Feld **Betrugskommentartyp**, um den Dokumenttyp anzugeben, der verwendet werden soll, wenn Benutzer Kommentare eingeben, wenn sie manuell einen Auftrag für Betrugsprüfung anordnen. Meistens wird dieses Feld auf **Hinweis** festgelegt.

## <a name="defining-fraud-criteria-and-rules"></a>Definieren von Betrugskriterien und -Regeln

Es gibt zwei Typen von Betrugskriterien, auf die sich das System bezieht, um zu prüfen, ob der Auftrag auf Betrug überprüft und gesperrt werden sollte:

- **Statische Betrugsdaten** verwendet einen bestimmten Wert, wie Telefonnummer, die auf eine Liste von gesperrten Nummern von oder E-Mail-Adresse gesetzt wurde, die markiert wurde, da dieses bekannt ist, für gefälschte vorherige Buchungen verwendet zu werden. Um statische Betrugsdaten einzurichten, wechseln Sie zu **Retail und Commerce** \> **Kanaleinrichtung** \> **Callcenter-Einrichtung** \> **Betrug** \> **Statische Betrugsdaten**. Auf der Seite **Statische Betrugsdaten** können Sie Betrugskriterien manuell oder durch Datenimport hinzufügen. Bewertungen werden zu den gefälschten Informationen zugeordnet. Wenn Betrugsüberprüfung aktiviert ist, wird der eingegebene Auftrag mit den statischen Daten verglichen. Wenn die Daten entweder in der Rechnungsadresse oder der Lieferadresse des Debitors gefunden wird, oder wenn die Daten in der Lieferadressen gefunden werden, die mit einer Position in diesem Auftrag verknüpft sind, werden die Punktzahlen aller eindeutigen Übereinstimmungen zusammengefügt und mit dem Wert **Minimale Punktzahl** verglichen, um zu bestimmen, ob der Auftrag gesperrt werden soll.

- **Betrugsregeln** bestehen aus benutzerdefinierten Variablen und den Bestimmungen, die für diese Variablen definiert werden. Um Regeln zu erstellen, gehen Sie zu **Retail und Commerce** \> **Kanaleinrichtung** \> **Callcenter-Einrichtung** \> **Betrug** \> **Regeln**. Mit Betrugsregeln können Unternehmen komplexere Regeln erstellen mit **UND** oder **ODER** Bedingungen, um mehrere Bedingungen zu evaluieren. Beispielsweise fordert ein Benutzer alle Aufträge für Debitoren, die einer bestimmten Debitorengruppe angehören und die ein bestimmtes Produkt bestellten, um für die Betrugsprüfung gesperrt zu werden. In diesem Fall werden die Bedingungen für den Debitor und die Produkte auf der Seite **Regeln** definiert und die UND Bedingung wird verwendet. Ein Auftrag wird dann gesperrt, wenn beide Bedingungen erfüllt sind und der Punktzahlwert, der dieser Regel zugeordnet wird, zuzüglich dem Punktzahlwert aller anderen Regeln, auf die die Auftragsabgleichung passt, verursacht, dass die gesamte Betrugspunktzahl des Auftrags den Wert der **Minimalen Punktzahl** überschreitet, der auf der Seite **Callcenterparameter** definiert ist.

> [!NOTE]
> Verwendung mehrerer Regeln oder zu komplexe Regeln führen zu schlechter Systemleistung, wenn Aufträge gesendet werden. Die Betrugswarnungsfunktion ist nicht optimiert worden, um eine große Anzahl von statischen Betrugsdateneingaben und zahlreichen aktiven Regeln zu behandeln. Bedenken Sie, dass jede Regel ausgewertet wird, wenn Callcenterbenutzer **Übermitteln** während des Auftragseintrags auswählen. Die Regeln werden für den Auftragskopf sowie alle Auftragspositionen überprüft. Je mehr Regeln da sind und je komplexer Regelformulierungen sind, desto länger dauert die Verarbeitung. Wenn Sie viele Positionen in Ihrem Auftrag und viele Positionen auf dem Auftrag haben, und eine große Zahl von aktiven und statischen Dateneinträgen haben, kann dieser systematische Prozess der Überprüfung und der Überprüfung aller Daten und der Berechnung einer Betrugspunktzahl schwere Auswirkungen auf die Leistung haben. Organisationen, die diese Funktion verwenden, müssen immer testen und bestätigen, dass die Auftragseinsendungsbearbeitungszeit akzeptabel ist, bevor Änderungen auf die Regeln oder statischen Betrugskriterien in der Produktionsumgebungen angewendet werden.

## <a name="identifying-orders-that-are-on-hold-for-fraud-review"></a>Identifizieren Aufträge, die für Betrugsprüfung gesperrt sind

Wenn Callcenterbenutzer einen Auftrag senden, wenn der Auftrag mit den Betrugskriterien oder der Regeln übereinstimmt und die Bewertung das Minimum überschreitet, dann erhalten die Benutzer eine Warnmeldung angezeigt, der kennzeichnet, dass der Auftrag gesperrt wurde. Benutzer können diese Meldung schließen, da sie ausschließlich zu Informationszwecken ist. Benutzer können optional diese Informationen dem Debitor kommunizieren. Das Unternehmen sollte das Protokoll bestimmen, dem Benutzer in dieser Situation folgen.

Die Reihenfolge wird gespeichert, jedoch wird die Markierung auf **nicht verarbeiten** festgelegt. Mit dieser Markierung wird sichergestellt, dass die Bestellung nicht am Lagerort freigegeben werden kann. Benutzer können jederzeit die Einstellung **Verarbeiten Sie nicht** für jeden Auftrag auf der Seite **Detaillierter Status** sehen. Diese Seite kann von den Seiten **Jeder Auftrag** und **Kundendienst** geöffnet werden. Das System nimmt auch den Wert des Felds **Detaillierter Status** für den Auftrag auf **Betrugsgriff**.

Um die Aufträge anzuzeigen und zu verwalten, die für Betrugsprüfung gesperrt sind, wechseln Sie zu **Retail und Commerce** \> **Kunden** \> **Auftragssperren**. Auf der Seite **Aufträge sperren** wählen Sie einen Eintrag in der Liste aus, und klicken Sie dann auf **Auftrag gesperrt**, um eine detailliertere Ansicht anzuzeigen, die Informationen über den Grund für die Sperre enthält. Auf dem Inforegister **Betrugsdetails** können Sie die systematische die Betrugskriterien anzeigen, die gefunden wurden, um für eine Übereinstimmung die Reihenfolge und die Bewertungen abzustimmen. Wenn der Auftrag manuell gesperrt wurde, können Sie beliebige Kommentare anzeigen, die vom Benutzer eingegeben wurden, der den Auftrag gesperrt hat unter **Betrugs-Hinweise** im Inforegister  **Hinweise**.

Weitere Informationen zum Arbeiten mit dem Formular, finden Sie unter [Auftrag sperren ](https://docs.microsoft.com/dynamics365/unified-operations/retail/work-with-order-holds).
