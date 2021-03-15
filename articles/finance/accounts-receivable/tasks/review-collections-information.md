---
title: Inkassoinformationen überprüfen
description: In diesem Thema wird erläutert, wie Sie Inkassoinformationen sowie verschiedene Einrichtungsoptionen und Inkassobuchungen prüfen können.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustCollectionsPool, SysQueryForm, CustCollectionsAgent, OMTeamSelectMemberDialog, CustVendReportInterval, CustParameters, CustAgingSnapshot, CustVendAgingBucketLookUp, CustCollectionsPoolsListPage, CustCollectionsContactPart, CustCollections
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9bbfb6537118a9936c127018427b0516e7ea002a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971527"
---
# <a name="review-collections-information"></a>Inkassoinformationen überprüfen

[!include [banner](../../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie Inkassoinformationen sowie verschiedene Einrichtungsoptionen und Inkassobuchungen prüfen können. Für diese Prozedur wird das Demo-Unternehmen USMF verwendet.

## <a name="create-customer-pools"></a>Debitorenpools erstellen
1. Wechseln Sie im Navigationsbereich zu **Module > Kredit und Inkasso > Einstellungen > Debitorenpools**.
- Mithilfe dieser Seite können Sie Debitorenpools einrichten. Debitorenpools sind Abfragen, die eine Gruppe von Debitorenkonten definieren, die für Inkassi oder Fälligkeitsprozesse angezeigt und verwaltet werden können. Verwenden Sie Debitorenpools, um Informationen auf der Listenseite **Inkassi** und auf den zugehörigen Listenseiten zu filtern. Sie können Debitorenpools auch zum Filtern der Debitorenkonten verwenden, die einbezogen werden, wenn Fälligkeitsmomentaufnahmen erstellt werden.  
- Sie können Debitorenpools auch zum Filtern der Debitorenkonten verwenden, die einbezogen werden, wenn Fälligkeitsmomentaufnahmen erstellt werden.  
2. Wählen Sie **Neu** aus.
3. Geben Sie im Feld **Poolkennung** einen Wert ein.
4. Geben Sie im Feld **Poolbeschreibung** einen Wert ein.
5. Klicken Sie auf **Poolkriterien auswählen**.
6. Geben Sie im Feld **Kriterien** einen Wert ein.
7. Wählen Sie **OK**.
8. Wählen Sie **Vorschau des Debitorenpools anzeigen**.

## <a name="create-collections-agents"></a>Inkassobeauftragte erstellen
1. Wechseln Sie im Navigationsbereich zu **Module > Kredit und Inkasso > Einstellungen > Inkassobeauftragte**.  
- Mithilfe dieser Seite können Sie Arbeitskräfte als Inkassobeauftragte einrichten und ihnen optional Debitorenpools zuweisen. Ein *Inkassobeauftragter* ist eine Person, die in Zusammenarbeit mit Debitoren sicherstellt, dass Zahlungen rechtzeitig eingehen.  
- Auf dieser Seite eingerichtete Inkassobeauftragte werden automatisch einem Inkassoteam hinzugefügt. Wenn ein Team im Feld **Team** auf der Seite **Debitorenparameter** ausgewählt wird, werden Inkassobeauftragte diesem Team hinzugefügt. Wird kein Team ausgewählt, wird automatisch ein neues Team mit dem Namen "Inkassi" erstellt, und die Inkassobeauftragten werden diesem Team hinzugefügt.  
2. Wählen Sie den gewünschten Beauftragten aus, und wählen Sie dann **Hinzufügen** auf der Seite aus.
3. Wählen Sie im Feld **Poolkennung** den gewünschten Datensatz im Dropdownmenü aus.
4. Aktivieren bzw. deaktivieren Sie das Kontrollkästchen **Standardpool**.
- Aktivieren Sie diese Option, um alle Debitorenpools in Filterlisten für den ausgewählten Inkassobeauftragten einzuschließen. Wenn diese Option nicht aktiviert wird, sind nur die Debitorenpools, die dem Inkassobeauftragten zugewiesen sind, in Filterlisten verfügbar.  

## <a name="create-aging-period-definition"></a>Zahlungsfristdefinitionen erstellen
1. Wechseln Sie im Navigationsbereich zu **Module > Kredit und Inkasso > Einstellungen > Zahlungsfristdefinitionen**.
- Mithilfe von Zahlungsfristdefinitionen können Sie – basierend auf einem gewünschten Datum – die Fälligkeit von Debitoren- und Kreditorenkonten ermitteln. Beim Ausführen der Analyse entspricht jede für die Zahlungsfristdefinition eingerichtete Zahlungsfrist einer Spalte auf der Listenseite oder einer Spalte im Formular oder Bericht.  
2. Wählen Sie **Neu** aus.
3. Geben Sie im Feld **Zahlungsfristdefinition** einen Wert ein.
4. Geben Sie im Feld **Beschreibung** einen Wert ein.
- Hier können Sie den Periodennamen, die Einheit und das Intervall für die einzelnen Zahlungsfristen angeben, die in die Zahlungsfristdefinition einbezogen werden sollen. Die Position, deren Feld "Einheit" den Wert "0" enthält, stellt das Datum dar, an dem die Analyse ausgeführt wird. Standardmäßig erhalten Positionen vor dem Wert "0" im Feld "Einheit" den Wert "-1" und Positionen nach dem Wert "0" den Wert "1", dieser Wert kann jedoch geändert werden. Wählen Sie **Nach oben** und **Nach unten** aus, um die Positionen neu anzuordnen. Die Position mit dem Wert "0" kann nicht verschoben werden.  
- Platzieren Sie den Mauszeiger an der Stelle, an der eine neue Position eingefügt werden soll, und wählen Sie anschließend **Hinzufügen** aus.  
- Wählen Sie einen Indikator zur Darstellung der Zahlungsfrist im Formular **Inkassi** und auf der entsprechenden Listenseite aus. Wählen Sie also beispielsweise einen grünen Indikator für eine aktuelle Periode, einen gelben Indikator für eine Fristüberschreitung von 30 Tagen und einen roten Indikator für eine Fristüberschreitung von 90 Tagen aus.  
- Wählen Sie die Druckrichtung für die Zahlungsfristdefinition aus. Diese Auswahl bestimmt die Reihenfolge, in der die Spalten im Debitorenfälligkeitsbericht oder im Kreditoren-Fälligkeitsbericht angezeigt werden.  
  - Vorwärts – Druckt die Spalten (beginnend mit der ersten Zeile) in der Reihenfolge, in der die Überschriften in der Tabelle angezeigt werden.  
  - Rückwärts – Druckt die Spalten (beginnend mit der letzten Zeile) in der umgekehrten Reihenfolge, in der die Überschriften in der Tabelle angezeigt werden.    

## <a name="setup-collections-parameters"></a>Inkassoparameter einrichten
1. Wechseln Sie im Navigationsbereich zu **Module > Kredit und Inkasso > Einstellungen > Debitorenparameter**.
2. Wählen Sie die Registerkarte **Inkassi** aus.
3. Erweitern oder reduzieren Sie den Abschnitt **Inkassostandards**.
- Wählen Sie eine Zahlungsfristdefinition für die standardmäßige Fälligkeitsmomentaufnahme aus, die im Formular **Inkassi** verwendet werden soll.  
- Wählen Sie ein Team aus, dem Inkassobeauftragte im Formular **Inkassobeauftragte** zugewiesen werden. Nur Teams mit dem Teamtyp "Inkassi" werden in der Liste angezeigt.  
4. Erweitern oder reduzieren Sie den Abschnitt **Abschreiben**.
- Wählen Sie den Namen der Erfassung aus, die für tägliche Sachkontoerfassungen eingerichtet ist und die Sie verwenden möchten, wenn eine Buchung mit dem Formular **Inkassi** oder zugehörigen Listenseiten abgeschrieben wird.  
- Wählen Sie den Standardursachencode aus, der verwendet werden soll, wenn Abschreibungsbuchungen mithilfe des Formulars **Inkassi** oder zugehöriger Listenseiten erstellt werden.  
- Aktivieren Sie diese Option, um eine gesonderte Erfassungsposition für Mehrwertsteuerbeträge zu erstellen, wenn Abschreibungsbuchungen mit der Seite **Inkassi** oder mit zugehörigen Listenseiten erstellt werden. Wenn Sie diese Option aktivieren, können Sie die Mehrwertsteuerbeträge, die in Abschreibungsbuchungen enthalten sind, einfach nachverfolgen. Sie können die Mehrwertsteuerbeträge gesondert nachverfolgen, um Mehrwertsteuerverbindlichkeiten für die betroffene Periode einfacher anzupassen.  
5. Erweitern oder reduzieren Sie den Abschnitt **E-Mail-Vorlage**.
- Wählen Sie die E-Mail-Vorlage aus, die Sie beim Senden einer E-Mail mit der Aktion **E-Mail > Buchungen - Kontakt** im Formular **Inkassi** verwenden möchten.  
- Wählen Sie die E-Mail-Vorlage aus, die Sie beim Senden von Debitorenaufstellungen als Anlage zu einer E-Mail mit der Aktion **E-Mail > Aufstellung - Kontakt** im Formular **Inkassi** verwenden möchten.  
- Wählen Sie die E-Mail-Vorlage aus, die Sie beim Senden einer E-Mail mit der Aktion **E-Mail > Buchungen - Verkäufer** im Formular **Inkassi** verwenden möchten.  

## <a name="age-customer-balance"></a>Fälliges Debitorensaldo
1. Wechseln Sie im Navigationsbereich zu **Module > Kredit und Inkasso > Periodische Aufgaben > Fällige Debitorensalden**.
- Wählen Sie eine Zahlungsfristdefinition aus. Im Rahmen des Prozesses für Fälligkeitsmomentaufnahmen altern Buchungen gemäß den Zahlungsfristen, die in der ausgewählten Zahlungsfristdefinition definiert wurden.  
- Wählen Sie entweder einen Debitorenpool aus, oder lassen Sie das Feld leer, um eine Fälligkeitsmomentaufnahme für alle Debitoren zu erstellen. Wenn Sie einen Debitorenpool auswählen, wird der Prozess für die Fälligkeitsmomentaufnahme nur auf die Debitorenkonten angewendet, die Teil des Debitorenpools sind. Der ausgewählte Debitorenpool muss den Typ "Fälligkeitsmomentaufnahme" besitzen.  
- Wählen Sie den Datumstyp aus, auf dem die Fälligkeitsmomentaufnahme basieren soll.  
  - Buchungsdatum – Alter jeder Transaktion basiert auf deren Buchungsdatum.    
  - Fälligkeitsdatum – Alter jeder Transaktion basiert auf deren Fälligkeitsdatum.    
  - Dokumentdatum - Alter jeder Transaktion basiert auf deren Dokumentdatum.  
- Wählen Sie das Datum aus, das als aktuelles Datum für die Fälligkeitsmomentaufnahme verwendet werden soll. Zahlungsfristen werden auf der Grundlage dieses Datums berechnet.    
  - Heutiges Datum - Wählen Sie das Systemdatum aus. Verwenden Sie diese Option, wenn für die Verarbeitung ein sich wiederholender Stapel eingerichtet wurde. Wenn Sie dieses Datum verwenden, kann der sich wiederholende Stapel regelmäßig ausgeführt werden, und das Systemdatum zu diesem Zeitpunkt wird verwendet.    
  - Gewähltes Datum - Wählen Sie ein Datum aus, das Sie festlegen. Bei Verwendung dieser Option muss ein Fälligkeitsdatum eingegeben werden.  
2. Wählen Sie **OK**.

## <a name="view-aged-customer-balances"></a>Fällige Debitorensalden anzeigen
1. Wechseln Sie im Navigationsbereich zu **Module > Kredit und Inkasso > Inkasso > Saldenrückblick**.
- Mithilfe dieser Listenseite können Sie Debitorensalden und Saldenrückblicke nach Zahlungsfrist anzeigen. Diese Informationen werden in einer Fälligkeitsmomentaufnahme gespeichert. Die Zahlungsfristen werden anhand der verwendeten Zahlungsfristdefinition ermittelt. Die Zahlungsfristdefinition stammt aus dem Debitorenpool, sofern dieser für die Poolabfrage angegeben wurde. Falls der Debitorenpool nicht über eine Zahlungsfristdefinition verfügt, wird die im Formular "Debitorenparameter" angegebene Zahlungsfristdefinition verwendet.  
2. Erweitern Sie die Infobox **Kontakt**. Hier können Sie Kontaktinformationen einsehen:
- Inkassokontakt für den Debitor.  
- Standardverkäufer für den Debitor.  
3. Erweitern Sie die Infobox **Kreditlimit**.
- In der Infobox **Kreditinformationen** werden das Kreditlimit und aktuelle Saldoinformationen für den Debitor angezeigt.  

## <a name="view-customer-collections-details"></a>Debitoreninkassodetails anzeigen
1. Stellen Sie sicher, dass die gewünschten Datensatz ausgewählt wurde.
2. Erweitern Sie die Infoboxen **Adresse**, **Kontakt**, **Fälligkeit** und **Kreditlimit** , um die entsprechenden Informationen anzuzeigen.
3. Klicken Sie im Aktivitätsbereich auf **Mahnen**.
- Aktualisiert die Fälligkeitsmomentaufnahme für den Debitor. Dabei wird das aktuelle Datum als das Fälligkeitsdatum verwendet, mit dem Buchungsdaten verglichen werden. Wenn die Fälligkeitsmomentaufnahme Informationen für mehrere juristische Personen beinhaltet, enthält die aktualisierte Fälligkeitsmomentaufnahme Informationen für die gleichen juristischen Personen. Beträge werden beim Aktualisieren der Fälligkeitsmomentaufnahme in der Buchhaltungswährung der juristischen Person gespeichert, bei der Sie angemeldet sind.  
- Wählen Sie eine Zahlungsfristdefinition aus. Standardmäßig wird die Zahlungsfristdefinition angezeigt, die der Fälligkeitsmomentaufnahme für den Debitor zugeordnet ist. Die Zahlungsfristdefinition bestimmt, welche Zahlungsfristen und Beträge in den Infoboxen **Saldenrückblick** und **Kreditinformationen** angezeigt werden.  
- Öffnet ein Menü mit den folgenden Optionen:    
  - Unternehmen – Zeigt Beträge in den Infoboxen „Saldenrückblick“ und „Kreditinformationen“ in der Buchhaltungswährung der juristischen Person an.  
  - Debitor - Beträge in den Infoboxen „Saldenrückblick“ und „Kreditinformationen“ in der Währung des Debitors anzeigen.  
- Wählen Sie mindestens eine juristische Person in der Fälligkeitsmomentaufnahme des Debitors aus, für die Sie Informationen anzeigen möchten. In der Liste werden die juristischen Personen angezeigt, die beim Erstellen der Fälligkeitsmomentaufnahme ausgewählt wurden.  
- Zeigen Sie die Debitorenaufstellungen im Microsoft Excel-Format an. Sie können ein Startdatum für den Buchungsbereich auswählen, der in der Aufstellung enthalten sein soll, und festlegen, ob nur offene oder sowohl offene als auch ausgeglichene Buchungen eingeschlossen werden. Wenn die Fälligkeitsmomentaufnahme Informationen für mehrere juristische Personen enthält, werden Buchungen für alle enthaltenen juristischen Personen angezeigt.  
- Öffnen Sie das Formular **Dokumente**, in dem Sie Dokumente oder Hinweise erstellen oder anzeigen können.  
4. Klicken Sie im Aktivitätsbereich auf **Kommunikation**.  
- Öffnen Sie Outlook, sodass Sie eine E-Mail an den im Feld "Kontakt" angegebenen Kontakt senden können. Wenn kein Inkassokontakt angegeben ist, wird die primäre Adresse für den Debitor verwendet. Falls kein Primärkontakt angegeben ist, werden E-Mails an die erste Adresse im Formular **Kontakte** gesendet. Die ausgewählten Buchungen werden als Anlage hinzugefügt. Bei der Anlage handelt es sich um eine Excel-Datei mit drei Arbeitsblättern. Im Formular **Debitorenkontenparameter** kann eine E-Mail-Vorlage für Nachrichten an Debitorenkontakte festgelegt werden.  
- Diese Schaltfläche ist nicht verfügbar, wenn für den im Formular ausgewählten Kontakt keine E-Mail-Adresse eingerichtet ist.  
- Erstellen Sie eine Aufstellung und öffnen Sie Outlook, sodass Sie eine E-Mail mit der Aufstellung als Anlage an die im Feld **Kontakt** angegebene Adresse senden können. Wenn kein Inkassokontakt angegeben ist, wird die primäre Adresse für den Debitor verwendet. Falls kein Primärkontakt angegeben ist, werden E-Mails an die erste Adresse im Formular **Kontakte** gesendet.  
- Diese Schaltfläche ist nicht verfügbar, wenn für den im Formular ausgewählten Kontakt keine E-Mail-Adresse eingerichtet ist.  
- Öffnet Outlook, sodass Sie eine E-Mail an den Mitarbeiter senden können, der der Verkäufer für die dem Debitor zugewiesene Verkaufsgruppe ist. Wenn Buchungen ausgewählt sind, werden sie als Anlage hinzugefügt. Bei der Anlage handelt es sich um eine Excel-Datei mit zwei Arbeitsblättern. Im Formular **Debitorenkontenparameter** kann eine E-Mail-Vorlage für Nachrichten an Verkäufer festgelegt werden.  
- Diese Schaltfläche ist nicht verfügbar, wenn für den im Formular angezeigten Verkäufer keine E-Mail-Adresse eingerichtet ist.  
- Hier können Sie Buchungsaktivitäten für den Debitor anzeigen und ausführen. Wenn Sie zentralisierte Zahlungen verwenden, werden Informationen für alle juristischen Personen angezeigt, die in der Fälligkeitsmomentaufnahme des Debitors enthalten sind. Die Informationen zur juristischen Person können durch Auswahl von **Unternehmen** in der Gruppe **Auswählen** im Aktivitätsbereich eingeschränkt werden.  
- Dient zum Ändern des Inkassostatus für die ausgewählten Buchungen.    
  - Keine Streitigkeit – Für die Transaktion hat keine Inkassoaktivität stattgefunden.    
  - Strittig – Der Debitor hat Sie darüber informiert, dass ein Problem mit der Transaktion vorliegt.    
  - Zahlungszusage – Der Debitor hat sich einverstanden erklärt, den Buchungsbetrag zu bezahlen.    
  - Gelöst – Alle Probleme mit der Buchung wurden gelöst, und es ist keine weitere Inkassoaktivität erforderlich.  
- Öffnet ein Menü, in dem Sie eine der folgenden Optionen auswählen können, um die in diesem Formular anzuzeigenden Buchungen anzugeben:    
  - Offen – Zeigt nur Buchungen an, die nicht ausgeglichen wurden.    
  - Offen und abgeschlossen – Zeigt alle Buchungen an, sowohl ausgeglichene als auch nicht ausgeglichene.  
- Verarbeiten Sie die ausgewählte Zahlung als Zahlung ohne ausreichende Deckung (NSF-Zahlung).    
  - Diese Schaltfläche ist nur verfügbar, wenn es sich bei der ausgewählten Buchung um eine in eine Zahlungserfassung eingegebene Zahlung (ein Guthaben ohne Rechnung) handelt, der Buchung ein Bankkonto zugewiesen ist und die Zahlung zuvor nicht storniert wurde.  
- Schreibt die ausgewählten Buchungen ab.  
- Markiert die ausgewählten Buchungen für den Ausgleich.  
- Öffnen Sie das Formular **Originaldokument**, in dem das Dokument für die ausgewählte Buchung angezeigt und gedruckt werden kann.  
- Öffnet ein **Menü** mit den folgenden Optionen:    
  - Inkassi – Zeigt nur Aktivitäten an, die im Formular „Inkassi“ erstellt wurden.    
  - Alle – Zeigt alle Aktivitäten für den Debitor an, unabhängig davon, wo sie erstellt wurden.  
- Öffnet ein **Menü** mit den folgenden Optionen:    
  - Offen – Zeigt nur Aktivitäten an, die noch nicht abgeschlossen sind.    
  - Offen und abgeschlossen – Zeigt alle Aktivitäten unabhängig vom Status an.  
- Wählen Sie eine Inkassoanfrage aus, die dem Debitor zugewiesen ist, oder lassen Sie dieses Feld leer. Wenn eine Anfrage ausgewählt wird, werden in diesem Formular nur Buchungen und Aktivitäten angezeigt, die der Anfrage zugeordnet sind.  
5. Wählen Sie **Liste anzeigen** aus.
- Wählen Sie ein Debitorenkonto aus, oder übernehmen Sie den Standardeintrag. Hier wird standardmäßig das Debitorenkonto angezeigt, das auf der Listenseite oder in dem Formular ausgewählt ist, über die bzw. das dieses Formular geöffnet wurde. Wenn Sie das Formular über eine Listenseite geöffnet haben, enthält die Liste die Debitoren, die in dem auf der Listenseite verwendeten Debitorenpool enthalten sind.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]