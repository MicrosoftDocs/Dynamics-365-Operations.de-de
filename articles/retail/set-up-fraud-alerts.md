---
title: Betrugswarnungen einrichten
description: "In diesem Thema wird erläutert, wie Regeln eingerichtet werden, um Kundendienstmitarbeiter vor möglicherweise gefälschten Informationen zu warnen, wenn Aufträge verarbeitet werden. Sie können auch spezielle Codes definieren, die verwendet werden, um automatisch oder manuell verdächtige Aufträge zu sperren."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: SalesPostingHistory, MCRHoldCodeTrans, SysOperationTemplateForm
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
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: f57cdb44d5ed3b078478cf47b74d1a79ba10323c
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-fraud-alerts"></a>Betrugswarnungen einrichten

[!INCLUDE [banner](includes/banner.md)]

In diesem Thema wird erläutert, wie Sie Kriterien und Regeln einrichteten ,um potenziell gefälschte Aufträge für weitere Prüfung gesperrt zu halten. Betrugsprüfungsfunktionen werden verwendet, um die Gültigkeit von Informationen in einen Auftrag zu bestimmen. Wenn die Informationen im Auftrag auf Grundlage der Betrugskriterien und -Regeln einer Organisation fraglich erscheinen, kann der Auftrag für weitere Prüfung durch einen Administrator gesperrt werden.

> [!NOTE]
> Diese Funktion kann nur mit der Retail Call Center-Kanal-Auftragsverarbeitung verwendet werden. 

Wenn der Call Center-Kanal definiert ist, muss **Auftrags-Abschluss aktivieren** auf **Ja** gesetzt werden. Wenn Auftragsabschluss aktiviert ist, können Benutzer die Auftragsrekapitulation anzeigen und auf **Übermitteln** klicken, um den Auftrag abzuschließen. Benutzer können auch Optionen erhalten, den Auftrag manuell auf Betrugsprüfungssperre zu setzen. Für Aufträge, die von einem Callcenterbenutzer verschlüsselt werden, werden durch Betrugsscheckregeln und -Kriterien während des Sendeprozesses verarbeitet.

Es gibt zwei Typen von Betrugskriterien, auf die sich das System bezieht, um zu prüfen, ob der Auftrag auf Betrug überprüft und gesperrt werden sollte:

-   **Statische Regeln** verwenden einen bestimmten Wert, wie Telefonnummer, die auf die schwarze Liste gesetzt wurde, oder eine E-Mail-Adresse, die markiert wurde als bekannt für gefälschte Transaktionen in der Vergangenheit. Auf der Seite **Statische Betrugsdaten** können Betrugsinformationen manuelle oder durch Datenimport hinzugefügt werden, mit Punktzahlen, die den betrügerischen Informationen zugeordnet sind. Wenn Betrugsüberprüfung aktiviert ist, wird der eingegebene Auftrag mit den statischen Daten verglichen. Wenn sich die Daten entweder in der Rechnungsstellung oder der Lieferadresse des Debitors befinden, oder wenn die Daten in der Lieferadresse in der Verkaufsposition gefunden werden, werden die Punktzahlen aller eindeutigen Übereinstimmungen summiert.  
-   **Dynamische Regeln** setzten sich zusammen aus Variablen und Bedingungen, die für diese Variablen definiert sind. Mit dynamischen Regeln können andere Kriterien, die nicht in den statischen Regeln definiert sind, überprüft werden. Komplexere “AND/OR”-Ausdrücke können verwendet werden, um mehrere Bedingungen zu berücksichtigen, um zu bestimmen, ob eine positive Übereinstimmung mit den Regelkriterien und dem Auftrag, der gesendet wird, vorliegen. Wenn ein Benutzer also beispielsweise für Betrugsprüfung Aufträge von Debitoren vorsehen möchte, die mit einem bestimmten Debitorengruppenwert verbunden sind und die ein bestimmtes Produkt bestellten, werden die Bedingungen definiert, um den Debitor zu überprüfen und die Produkten, auf der Seite **Regeln** mit einer "UND"-Bedingung definiert. Der Auftrag würde nur dann unter die Betrugssperre fallen, wenn beide Bedingungen erfüllt wurden und wenn der Punktzahlwert, der der Regel zugeordnet wurde, die gesamte Betrugspunktzahl des Auftrags über der Mindest-Betrugspunktzahl liegt, wie in den Callcenterparametern definiert.

Ein Callcenterbenutzer kann auch manuell ein Auftrag in die Betrugsgriffwarteschlange setzen. Wenn der Benutzer, der den Auftrag eingibt, glaubt, dass der Debitor, der den Auftrag erteilt, verdächtig sein könnte und möchte, dass eine andere Person die Gültigkeit des Auftrags prüft, bevor dieser verarbeitet wird, kann die Option **Manuelle Sperre für Betrug** im Dropdown-Menü **Sperren** auf der Seite **Auftrags-Zusammenfassung** wählen (erscheint,, nachdem die Auftragsfunktion **Vollständig** aufgerufen wurde). Der Benutzer wird aufgefordert, einen Hinweis einzugeben, um zu erläutern, warum er der Meinung ist, dass der Auftrag gefälscht sein kann, sodass der Prüfer mehr Kontext hat.

Alle Aufträge, die durch Manuelle Sperre für Betrug angehalten werden, oder durch systematische Berechnung des Betrugswertes, werden auf der Seite **Auftragssperren** angezeigt, auf der der Auftrag geprüft und dann storniert oder zur Bearbeitung freigegeben werden kann.

> [!NOTE]
> Verwendung mehrerer Regeln oder zu komplexer Regeln führt zu schlechter Systemleistung, wenn Aufträge gesendet werden. Die Betrugswarnungsfunktion ist nicht optimiert worden, um eine große Anzahl von statischen Betrugsdateneingaben und zahlreichen aktiven Regeln zu behandeln. Es ist wichtig, sich daran zu erinnern, dass jede Regel während der Senden-Funktion des Callcenter-Auftragseintrags ausgewertet wird. Die Regeln werden für den Auftragskopf sowie alle Auftragspositionen überprüft. Je mehr Regeln da sind und je komplexer Regelformulierungen sind, desto länger dauert die Verarbeitung. Wenn Sie viele Positionen in Ihrem Auftrag und viele Positionen auf dem Auftrag haben, und eine große Zahl von aktiven und statischen Dateneinträgen haben, kann dieser systematische Prozess der Überprüfung und der Überprüfung aller Daten und der Berechnung einer Betrugspunktzahl schwere Auswirkungen auf die Leistung haben.  Organisationen, die diese Funktion verwenden, müssen immer testen und bestätigen, dass die Auftragseinsendungsbearbeitungszeit akzeptabel ist, bevor Änderungen auf die Regeln oder statischen Betrugskriterien in der Produktionsumgebungen angewendet werden.

