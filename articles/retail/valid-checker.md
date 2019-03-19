---
title: Konsistenzprüfung für Einzelhandelstransaktionen
description: In diesem Thema werden die Funktionen der Konsistenzprüfung für Einzelhandelstransaktionen in Microsoft Dynamics 365 for Retail beschrieben.
author: josaw1
manager: AnnBe
ms.date: 01/08/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: 8b373ce3cfd1183a082e2b1ebaf8c907b16e581e
ms.sourcegitcommit: ca4562fafa33b3512f0a5e246b15545fcf53e834
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2019
ms.locfileid: "379992"
---
# <a name="retail-transaction-consistency-checker"></a>Konsistenzprüfung für Einzelhandelstransaktionen


[!include [banner](includes/banner.md)]
[!include [preview banner](includes/preview-banner.md)]

In diesem Thema werden die in Version 8.1.3 von Microsoft Dynamics 365 for Finance and Operations eingeführten Funktionen der Konsistenzprüfung für Einzelhandelstransaktionen beschrieben. Die Konsistenzprüfung ermittelt und isoliert inkonsistente Transaktionen, bevor sie im Aufstellungsbuchungsprozess verarbeitet werden.

Wenn eine Aufstellung in Retail gebucht wird, kann die Buchung aufgrund der inkonsistenten Daten in den Einzelhandelstransaktionstabellen fehlschlagen. Die Datenfehler können durch unvorhergesehene Probleme in der Verkaufsstellenanwendung oder durch Fehler beim Importieren von Buchungen aus POS-Systemen von Drittanbietern auftreten. Im Folgenden sind Beispiele für diese Inkonsistenzen aufgeführt: 

  - Der Transaktionsgesamtbetrag in der Kopftabelle entspricht nicht dem Transaktionsgesamtbetrag der Positionen.
  - Die Positionsanzahl in der Kopftabelle entspricht nicht der Anzahl von Positionen in der Transaktionstabelle.
  - Die Steuern in der Kopftabelle stimmen nicht mit dem Steuerbetrag in den Positionen überein. 
  
Wenn inkonsistente Transaktionen durch den Aufstellungsbuchungsprozess verarbeitet werden, werden inkonsistente Verkaufsrechnungen und Zahlungserfassungen erstellt, und der gesamte Aufstellungsbuchungsprozess schlägt anschließend fehl. Das Wiederherstellen der Aufstellungen aus einem solchen Zustand umfasst komplexe Datenkorrekturen in mehreren Transaktionstabellen. Die Konsistenzprüfung für Einzelhandelstransaktionen verhindert solche Probleme.

Das folgende Diagramm veranschaulicht den Buchungsprozess mit Transaktionskonsistenzprüfung.

![Aufstellungsbuchungsprozess mit der Konsistenzprüfung für Einzelhandelstransaktionen](./media/validchecker.png "Aufstellungsbuchungsprozess mit der Konsistenzprüfung für Einzelhandelstransaktionen")

Der **Geschäftsbuchungen überprüfen** Stapelverarbeitungsvorgang prüft die Konsistenz der Einzelhandelstransaktionstabellen für die folgenden Szenarien.

- Debitorenkonto - überprüft, dass das Debitorenkonto in den Einzelhandelstransaktionstabellen in den HQ-Debitorenmasterdaten vorhanden ist.
- Positionsanzahl – überprüft, dass die Positionsanzahl mit der Anzahl der Positionen in den Verkaufstransaktionstabellen übereinstimmt, wie diese in der Transaktionskopftabelle aufgezeichnet wurden.

## <a name="set-up-the-consistency-checker"></a>Konsistenzprüfung einrichten
Konfigurieren Sie den Stapelverarbeitungsvorgang „Geschäftsbuchungen überprüfen“ unter **Einzelhandel \> IT für den Einzelhandel \> POS-Buchung**, sodass er regelmäßig ausgeführt wird. Der Stapelverarbeitungsauftrag kann basierend auf der Shoporganisationshierarchie in ähnlicher Weise wie die Funktionen zum Berechnen und Buchen im Stapel geplant werden. Es wird empfohlen, diesen Stapelverarbeitungsauftrag so zu konfigurieren, dass mehrmals am Tag ausgeführt wird, und ihn so zu planen, dass er am Ende jeder P-Auftragsausführung ausgeführt wird.

## <a name="results-of-validation-process"></a>Ergebnisse des Überprüfungsprozesses
Die Ergebnisse der Überprüfung durch den Stapelverarbeitungsauftrag werden in der entsprechenden Einzelhandelstransaktion markiert. Das Feld **Überprüfungsstatus** im Einzelhandelstransaktionsdatensatz wird entweder auf **Erfolgreich** oder **Fehler** festgelegt und das Datum der letzten Prüfungsausführung wird im Feld **Uhrzeit der letzten Überprüfung** angezeigt.

Um eine ausführlichere Fehlerbeschreibung in Bezug auf einen Validierungsfehler zu erhalten, wählen Sie den entsprechenden Shoptransaktionsdatensatz aus und klicken auf die Schaltfläche **Überprüfungsfehler**.

Transaktionen mit Überprüfungsfehlern und noch nicht validierte Transaktionen werden nicht in Aufstellungen einbezogen. Während des Prozesses „Auszug berechnen“ werden Benutzer darüber informiert, wenn Transaktionen vorliegen, die in die Aufstellung aufgenommen hätten werden können, wo dies jedoch nicht der Fall war.

Wenn ein Überprüfungsfehler gefunden wird, können Sie ihn nur beheben, indem Sie sich an den Microsoft Support wenden. In einer zukünftigen Version werden Funktionen hinzugefügt, mit denen Benutzer die Fehler, die in der Benutzeroberfläche erfolgten, in den Datensätzen selbst beheben können. Es werden außerdem Protokollierungs- und Überwachungsfunktionen zur Nachverfolgung des Änderungsverlaufs bereitgestellt.

> [!NOTE]
> In zukünftigen Versionen werden zudem zusätzliche Validierungsregeln zur Unterstützung weiterer Szenarien hinzugefügt.
