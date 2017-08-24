--- 
title: "Inkassoinformationen überprüfen"
description: "Diese Prozedur zeigt Ihnen, wie Sie Inkassoinformationen sowie verschiedene Einrichtungsoptionen und Inkassobuchungen prüfen können."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: b28d41d5ecf63b22cb84aff0c12a36cb0d728945
ms.contentlocale: de-de
ms.lasthandoff: 07/27/2017

---
# <a name="review-collections-information"></a>Inkassoinformationen überprüfen

[!include[task guide banner](../../includes/task-guide-banner.md)]

Diese Prozedur zeigt Ihnen, wie Sie Inkassoinformationen sowie verschiedene Einrichtungsoptionen und Inkassobuchungen prüfen können. Für diese Prozedur wird das Demo-Unternehmen USMF verwendet.


## <a name="create-customer-pools"></a>Debitorenpools erstellen
1. Wechseln Sie zu "Kredit und Inkasso" > "Einstellungen" > "Debitorenpools".
    * Mithilfe dieser Seite können Sie Debitorenpools einrichten. Debitorenpools sind Abfragen, die eine Gruppe von Debitorenkonten definieren, die für Inkassi oder Fälligkeitsprozesse angezeigt und verwaltet werden können. Verwenden Sie Debitorenpools, um Informationen auf der Listenseite "Inkassi" und auf den zugehörigen Listenseiten zu filtern. Sie können Debitorenpools auch zum Filtern der Debitorenkonten verwenden, die einbezogen werden, wenn Fälligkeitsmomentaufnahmen erstellt werden.  
    * Sie können Debitorenpools auch zum Filtern der Debitorenkonten verwenden, die einbezogen werden, wenn Fälligkeitsmomentaufnahmen erstellt werden.  
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Poolkennung" einen Wert ein.
4. Geben Sie im Feld "Poolbeschreibung" einen Wert ein.
5. Klicken Sie auf "Poolkriterien auswählen".
6. Geben Sie im Feld "Kriterien" einen Wert ein.
7. Klicken Sie auf "OK".
8. Klicken Sie auf "Vorschau des Debitorenpools anzeigen".

## <a name="create-collections-agents"></a>Inkassobeauftragte erstellen
1. Wechseln Sie zu "Kredit und Inkasso" > "Einstellungen" > "Inkassobeauftragte".
    * Mithilfe dieser Seite können Sie Arbeitskräfte als Inkassobeauftragte einrichten und ihnen optional Debitorenpools zuweisen. Ein Inkassobeauftragter ist eine Person, die in Zusammenarbeit mit Debitoren sicherstellt, dass Zahlungen rechtzeitig eingehen.  
    * Auf dieser Seite eingerichtete Inkassobeauftragte werden automatisch einem Inkassoteam hinzugefügt. Wenn ein Team im Feld "Team" auf der Debitorenparameterseite ausgewählt wird, werden Inkassobeauftragte diesem Team hinzugefügt. Wird kein Team ausgewählt, wird automatisch ein neues Team mit dem Namen "Inkassi" erstellt, und die Inkassobeauftragten werden diesem Team hinzugefügt.  
2. Klicken Sie auf "Neu".
3. Klicken Sie auf Hinzufügen.
4. Klicken Sie auf "Schließen".
5. Klicken Sie auf Hinzufügen.
6. Markieren Sie in der Liste die ausgewählte Zeile.
7. Klicken Sie im Feld "Poolkennung" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
8. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
9. Aktivieren bzw. deaktivieren Sie das Kontrollkästchen "Standardpool".
    * Aktivieren Sie diese Option, um alle Debitorenpools in Filterlisten für den ausgewählten Inkassobeauftragten einzuschließen. Wenn diese Option nicht aktiviert wird, sind nur die Debitorenpools, die dem Inkassobeauftragten zugewiesen sind, in Filterlisten verfügbar.  

## <a name="create-aging-period-definition"></a>Zahlungsfristdefinitionen erstellen
1. Wechseln Sie zu "Kredit und Inkasso" > "Einstellungen" > "Zahlungsfristdefinitionen".
    * Mithilfe von Zahlungsfristdefinitionen können Sie – basierend auf einem gewünschten Datum – die Fälligkeit von Debitoren- und Kreditorenkonten ermitteln. Beim Ausführen der Analyse entspricht jede für die Zahlungsfristdefinition eingerichtete Zahlungsfrist einer Spalte auf der Listenseite oder einer Spalte im Formular oder Bericht.  
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Zahlungsfristdefinition" einen Wert ein.
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
    * Hier können Sie den Periodennamen, die Einheit und das Intervall für die einzelnen Zahlungsfristen angeben, die in die Zahlungsfristdefinition einbezogen werden sollen. Die Position, deren Feld "Einheit" den Wert "0" enthält, stellt das Datum dar, an dem die Analyse ausgeführt wird. Standardmäßig erhalten Positionen vor dem Wert "0" im Feld "Einheit" den Wert "-1" und Positionen nach dem Wert "0" den Wert "1", dieser Wert kann jedoch geändert werden.  Klicken Sie zum Ändern der Positionsreihenfolge auf die Schaltflächen 'Nach oben' oder 'Nach unten'. Die Position mit dem Wert "0" kann nicht verschoben werden.  
    * Platzieren Sie den Mauszeiger an der Stelle, an der eine neue Position eingefügt werden soll, und klicken Sie anschließend auf "Hinzufügen".  
    * Wählen Sie einen Indikator zur Darstellung der Zahlungsfrist im Formular "Inkassi" und auf der entsprechenden Listenseite aus. Wählen Sie also beispielsweise einen grünen Indikator für eine aktuelle Periode, einen gelben Indikator für eine Fristüberschreitung von 30 Tagen und einen roten Indikator für eine Fristüberschreitung von 90 Tagen aus.  
    * Wählen Sie die Druckrichtung für die Zahlungsfristdefinition aus. Diese Auswahl bestimmt die Reihenfolge, in der die Spalten im Debitorenfälligkeitsbericht oder im Kreditoren-Fälligkeitsbericht angezeigt werden.  Vorwärts – Druckt die Spalten (beginnend mit der ersten Zeile) in der Reihenfolge, in der die Überschriften in der Tabelle angezeigt werden.  Rückwärts – Druckt die Spalten (beginnend mit der letzten Zeile) in der umgekehrten Reihenfolge, in der die Überschriften in der Tabelle angezeigt werden.    

## <a name="setup-collections-parameters"></a>Inkassoparameter einrichten
1. Wechseln Sie zu "Kredit und Inkasso" > "Einrichten" > "Debitorenkontenparameter".
2. Klicken Sie auf die Registerkarte "Inkassi".
3. Erweitern oder reduzieren Sie den Abschnitt "Inkassostandards".
    * Wählen Sie hier eine Zahlungsfristdefinition für die standardmäßige Fälligkeitsmomentaufnahme aus, die im Formular "Inkassi" verwendet wird.  
    * Wählen Sie hier ein Team aus, dem Inkassobeauftragte im Formular "Inkassobeauftragte" zugewiesen sind. Nur Teams mit dem Teamtyp "Inkassi" werden in der Liste angezeigt.  
4. Erweitern oder reduzieren Sie den Abschnitt "Abschreiben".
    * Wählen Sie hier die Erfassung aus, die für die tägliche Sachkontoerfassungen eingerichtet ist und die Sie verwenden möchten, wenn eine Buchung abgeschrieben wird. Verwenden Sie dazu das Formular "Inkassi" oder zugehörige Listenseiten.  
    * Wählen Sie hier den Standardursachencode aus, der verwendet werden soll, wenn Abschreibungsbuchungen mithilfe des Formulars "Inkassi" oder zugehöriger Listenseiten erstellt werden.  
    * Aktivieren Sie diese Option, um eine gesonderte Erfassungsposition für Mehrwertsteuerbeträge zu erstellen, wenn Abschreibungsbuchungen mit der Seite Inkassi oder mit zugehörigen Listenseiten erstellt werden. Wenn Sie diese Option aktivieren, können Sie die Mehrwertsteuerbeträge, die in Abschreibungsbuchungen enthalten sind, einfach nachverfolgen. Sie können die Mehrwertsteuerbeträge gesondert nachverfolgen, um Mehrwertsteuerverbindlichkeiten für die betroffene Periode einfacher anzupassen.  
5. Erweitern oder reduzieren Sie den Abschnitt "E-Mail-Vorlage".
    * Wählen Sie hier die E-Mail-Vorlage aus, die Sie zum Senden einer E-Mail verwenden möchten. Verwenden Sie dazu die Aktion "E-Mail" > "Buchungen - Kontakt" im Formular "Inkassi".  
    * Wählen Sie die E-Mail-Vorlage aus, die Sie zum Senden von Debitorenaufstellungen als Anlage zu einer E-Mail verwenden möchten. Verwenden Sie dazu die Aktion "E-Mail" > "Aufstellung - Kontakt" im Formular "Inkassi".  
    * Wählen Sie hier die E-Mail-Vorlage aus, die Sie zum Senden einer E-Mail verwenden möchten. Verwenden Sie dazu die Aktion "E-Mail" > "Buchungen - Verkäufer" im Formular "Inkassi" .  

## <a name="age-customer-balance"></a>Fälliges Debitorensaldo
1. Wechseln Sie zu "Kredit und Inkasso" > "Periodische Aufgaben" > "Fälligkeit von Debitorensalden bestimmen".
    * Wählen Sie eine Zahlungsfristdefinition aus. Im Rahmen des Prozesses für Fälligkeitsmomentaufnahmen altern Buchungen gemäß den Zahlungsfristen, die in der ausgewählten Zahlungsfristdefinition definiert wurden.  
    * Wählen Sie entweder einen Debitorenpool aus, oder lassen Sie das Feld leer, um eine Fälligkeitsmomentaufnahme für alle Debitoren zu erstellen. Wenn Sie einen Debitorenpool auswählen, wird der Prozess für die Fälligkeitsmomentaufnahme nur auf die Debitorenkonten angewendet, die Teil des Debitorenpools sind. Der ausgewählte Debitorenpool muss den Typ "Fälligkeitsmomentaufnahme" besitzen.  
    * Wählen Sie den Datumstyp aus, auf dem die Fälligkeitsmomentaufnahme basieren soll.    Buchungsdatum – Alter jeder Transaktion basiert auf deren Buchungsdatum.    Fälligkeitsdatum – Alter jeder Transaktion basiert auf deren Fälligkeitsdatum.    Dokumentdatum - Alter jeder Transaktion basiert auf deren Dokumentdatum.  
    * Wählen Sie das Datum aus, das als aktuelles Datum für die Fälligkeitsmomentaufnahme verwendet werden soll. Zahlungsfristen werden auf der Grundlage dieses Datums berechnet.    Heutiges Datum - Wählen Sie das Systemdatum aus. Verwenden Sie diese Option, wenn für die Verarbeitung ein sich wiederholender Stapel eingerichtet wurde. Wenn Sie dieses Datum verwenden, kann der sich wiederholende Stapel regelmäßig ausgeführt werden, und das Systemdatum zu diesem Zeitpunkt wird verwendet.    Gewähltes Datum - Wählen Sie ein Datum aus, das Sie festlegen. Bei Verwendung dieser Option muss ein Fälligkeitsdatum eingegeben werden.  
2. Klicken Sie auf "OK".

## <a name="view-aged-customer-balances"></a>Fällige Debitorensalden anzeigen
1. Wechseln Sie zu "Kredit und Inkasso" > "Inkassi" > "Saldenrückblick".
    * Mithilfe dieser Listenseite können Sie Debitorensalden und Saldenrückblicke nach Zahlungsfrist anzeigen. Diese Informationen werden in einer Fälligkeitsmomentaufnahme gespeichert. Die Zahlungsfristen werden anhand der verwendeten Zahlungsfristdefinition ermittelt. Die Zahlungsfristdefinition stammt aus dem Debitorenpool, sofern dieser für die Poolabfrage angegeben wurde. Falls der Debitorenpool nicht über eine Zahlungsfristdefinition verfügt, wird die im Formular "Debitorenparameter" angegebene Zahlungsfristdefinition verwendet.  
2. Erweitern Sie die Infobox "Kontakte".
    * Inkassokontakt für den Debitor.  
    * Standardverkäufer für den Debitor.  
3. Erweitern Sie die Infobox "Kreditlimit".
    * In der Infobox "Kreditinformationen" werden das Kreditlimit und aktuelle Saldoinformationen für den Debitor angezeigt.  

## <a name="view-customer-collections-details"></a>Debitoreninkassodetails anzeigen
1. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
2. Erweitern Sie die Adresse-Infobox.
3. Erweitern Sie die Infobox Kontakte.
4. Erweitern Sie die Infobox "Fälligkeit".
5. Erweitern Sie die Infobox "Kreditlimit".
6. Klicken Sie im Aktivitätsbereich auf "Sammeln".
    * Aktualisiert die Fälligkeitsmomentaufnahme für den Debitor. Dabei wird das aktuelle Datum als das Fälligkeitsdatum verwendet, mit dem Buchungsdaten verglichen werden. Wenn die Fälligkeitsmomentaufnahme Informationen für mehrere juristische Personen beinhaltet, enthält die aktualisierte Fälligkeitsmomentaufnahme Informationen für die gleichen juristischen Personen. Beträge werden beim Aktualisieren der Fälligkeitsmomentaufnahme in der Buchhaltungswährung der juristischen Person gespeichert, bei der Sie angemeldet sind.  
    * Wählen Sie eine Zahlungsfristdefinition aus. Standardmäßig wird die Zahlungsfristdefinition angezeigt, die der Fälligkeitsmomentaufnahme für den Debitor zugeordnet ist. Die Zahlungsfristdefinition bestimmt, welche Zahlungsfristen und Beträge in den Infoboxen "Saldenrückblick" und "Kreditinformationen" angezeigt werden.  
    * Öffnen Sie ein Menü mit den folgenden Optionen: Unternehmen - Beträge in den Infoboxen "Saldenrückblick" und "Kreditinformationen" in der Buchhaltungswährung der juristischen Person anzeigen.    Debitor - Beträge in den Infoboxen "Saldenrückblick" und "Kreditinformationen" in der Währung des Debitors anzeigen.  
    * Wählen Sie mindestens eine juristische Person in der Fälligkeitsmomentaufnahme des Debitors aus, für die Sie Informationen anzeigen möchten. In der Liste werden die juristischen Personen angezeigt, die beim Erstellen der Fälligkeitsmomentaufnahme ausgewählt wurden.  
    * Zeigt die Aufstellung des Debitors im Microsoft Excel-Format an. Sie können ein Startdatum für den Buchungsbereich auswählen, der in der Aufstellung enthalten sein soll, und festlegen, ob nur offene oder sowohl offene als auch ausgeglichene Buchungen eingeschlossen werden. Wenn die Fälligkeitsmomentaufnahme Informationen für mehrere juristische Personen enthält, werden Buchungen für alle enthaltenen juristischen Personen angezeigt.  
    * Öffnen Sie das Formular "Dokumente", in dem Sie Dokumente oder Hinweise erstellen oder anzeigen können.  
7. Klicken Sie im Aktivitätsbereich auf "Kommunikation".
    * Öffnen Sie Outlook, sodass Sie eine E-Mail an den im Feld "Kontakt" angegebenen Kontakt senden können. Wenn kein Inkassokontakt angegeben ist, wird die primäre Adresse für den Debitor verwendet. Falls kein Primärkontakt angegeben ist, werden E-Mails an die erste Adresse im Formular "Kontakte" gesendet. Die ausgewählten Buchungen werden als Anlage hinzugefügt. Bei der Anlage handelt es sich um eine Excel-Datei mit drei Arbeitsblättern. Im Formular "Debitorenkontenparameter" kann eine E-Mail-Vorlage für Nachrichten an Debitorenkontakte festgelegt werden.  
    * Diese Schaltfläche ist nicht verfügbar, wenn für den im Formular ausgewählten Kontakt keine E-Mail-Adresse eingerichtet ist.  
    * Erstellen Sie eine Aufstellung und öffnen Sie Outlook, sodass Sie eine E-Mail mit der Aufstellung als Anlage an die im Feld "Kontakte" angegebene Adresse senden können. Wenn kein Inkassokontakt angegeben ist, wird die primäre Adresse für den Debitor verwendet. Falls kein Primärkontakt angegeben ist, werden E-Mails an die erste Adresse im Formular "Kontakte" gesendet.  
    * Diese Schaltfläche ist nicht verfügbar, wenn für den im Formular ausgewählten Kontakt keine E-Mail-Adresse eingerichtet ist.  
    * Öffnet Outlook, sodass Sie eine E-Mail an den Mitarbeiter senden können, der der Verkäufer für die dem Debitor zugewiesene Verkaufsgruppe ist. Wenn Buchungen ausgewählt sind, werden sie als Anlage hinzugefügt. Bei der Anlage handelt es sich um eine Excel-Datei mit zwei Arbeitsblättern. Im Formular "Debitorenkontenparameter" kann eine E-Mail-Vorlage für Nachrichten an Verkäufer festgelegt werden.  
    * Diese Schaltfläche ist nicht verfügbar, wenn für den im Formular angezeigten Verkäufer keine E-Mail-Adresse eingerichtet ist.  
    * Hier können Sie Buchungsaktivitäten für den Debitor anzeigen und ausführen. Wenn Sie zentralisierte Zahlungen verwenden, werden Informationen für alle juristischen Personen angezeigt, die in der Fälligkeitsmomentaufnahme des Debitors enthalten sind. Die Informationen zur juristischen Person können über die Schaltfläche "Unternehmen" in der Gruppe "Auswählen" im Aktivitätsbereich eingeschränkt werden.  
    * Dient zum Ändern des Inkassostatus für die ausgewählten Buchungen.    Keine Streitigkeit – Für die Transaktion hat keine Inkassoaktivität stattgefunden.    Strittig – Der Debitor hat Sie darüber informiert, dass ein Problem mit der Transaktion vorliegt.    Zahlungszusage – Der Debitor hat sich einverstanden erklärt, den Buchungsbetrag zu bezahlen.    Gelöst – Alle Probleme mit der Buchung wurden gelöst, und es ist keine weitere Inkassoaktivität erforderlich.  
    * Öffnen Sie ein Menü und wählen Sie eine der folgenden Optionen aus, um die Transaktionen, die in diesem Formular angezeigt werden sollen, festzulegen: Öffnen - Zeigt nur Buchungen an, die nicht ausgeglichen wurden.    Offen und abgeschlossen – Zeigt alle Buchungen an, sowohl ausgeglichene als auch nicht ausgeglichene.  
    * Verarbeiten Sie die ausgewählte Zahlung als Zahlung ohne ausreichende Deckung (NSF-Zahlung).    Diese Schaltfläche ist nur verfügbar, wenn es sich bei der ausgewählten Buchung um eine in eine Zahlungserfassung eingegebene Zahlung (ein Guthaben ohne Rechnung) handelt, der Buchung ein Bankkonto zugewiesen ist und die Zahlung zuvor nicht storniert wurde.  
    * Schreibt die ausgewählten Buchungen ab.  
    * Markiert die ausgewählten Buchungen für den Ausgleich.  
    * Öffnen Sie das Formular "Originaldokument", in dem das Dokument für die ausgewählte Transaktion angezeigt und gedruckt wird.  
    * Öffnen Sie ein Menü mit den folgenden Optionen: Inkassi - Zeigt nur Aktivitäten an, die im Formular "Inkassi" erstellt wurden.    Alle – Zeigt alle Aktivitäten für den Debitor an, unabhängig davon, wo sie erstellt wurden.  
    * Öffnen Sie ein Menü mit den folgenden Optionen: Offen - Zeigt lediglich die Aktivitäten an, die nicht geschlossen werden.    Offen und abgeschlossen – Zeigt alle Aktivitäten unabhängig vom Status an.  
    * Wählen Sie eine Inkassoanfrage aus, die dem Debitor zugewiesen ist, oder lassen Sie dieses Feld leer. Wenn eine Anfrage ausgewählt wird, werden in diesem Formular nur Buchungen und Aktivitäten angezeigt, die der Anfrage zugeordnet sind.  
8. Klicken Sie auf "Liste anzeigen".
    * Wählen Sie ein Debitorenkonto aus, oder übernehmen Sie den Standardeintrag. Hier wird standardmäßig das Debitorenkonto angezeigt, das auf der Listenseite oder in dem Formular ausgewählt ist, über die bzw. das dieses Formular geöffnet wurde. Wenn Sie das Formular über eine Listenseite geöffnet haben, enthält die Liste die Debitoren, die in dem auf der Listenseite verwendeten Debitorenpool enthalten sind.  


