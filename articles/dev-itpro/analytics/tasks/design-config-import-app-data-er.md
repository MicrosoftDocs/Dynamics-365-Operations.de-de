---
title: EB-Konfigurationen entwerfen, um eingehende Dokumente zu analysieren
description: Diese Prozedur zeigt, wie elektronische Berichterstellungskonfigurationen (EB) entworfen werden, um ein eingehendes elektronisches Dokument für die Anwendungsdatenaktualisierung zu analysieren.
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 23004930d2377a3d647435b53b6809cd500f44ac
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/12/2019
ms.locfileid: "1741354"
---
# <a name="design-er-configurations-to-parse-incoming-documents"></a>EB-Konfigurationen entwerfen, um eingehende Dokumente zu analysieren

[!include [task guide banner](../../includes/task-guide-banner.md)]

Diese Prozedur zeigt, wie elektronische Berichterstellungskonfigurationen (EB) entworfen werden, um ein eingehendes elektronisches Dokument für die Anwendungsdatenaktualisierung zu analysieren. In diesem Verfahren importieren Sie eine geänderte Excel-Vorlage in eine ER-Formatkonfigurationen, die für das Beispielunternehmen, Litware, Inc. erstellt wurde, und erstellen dann die elektronischen Dokumente. Um diese Schritte auszuführen, müssen Sie zunächst die Schritte unter "Konfigurationsanbieter erstellen und als aktiv markieren" abschließen.

Diese Prozedur wird für Benutzer erstellt, die die Rolle des Systemadministrators oder des Entwicklers für elektronische Berichterstellung haben, die ihnen zugewiesen sind. 

Diese Schritte können mithilfe eines beliebigen Dataset abgeschlossen werden. Bevor Sie beginnen, laden Sie die im Thema „Eingehende Dokumente analysieren, um Anwendungsdaten zu aktualisieren” aufgelisteten Dateien herunter und speichern Sie diese (https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/parse-incoming-electronic-documents). Die Dateien sind: EFSTA model.xml, EFSTA format.xml, Response1.xml, Response2.xml, Response3.xml, Response4.xml.

1. Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.
    * Überprüfen Sie, dass der Konfigurationsanbieter für Beispielunternehmen „Litware, Inc.” verfügbar und als aktiv markiert ist. Wenn Sie diesen Konfigurationsanbieter nicht sehen, müssen Sie zunächst die Schritte in der Prozedur „Konfigurationsanbieter erstellen und als aktiv markieren” abschließen.  
2. Klicken Sie auf "Berichterstellungskonfigurationen".
    * Anhand des folgenden Szenarios werden die Funktionen beim Analysieren eingehender elektronischer Dokumente im XML-Format gezeigt: ERP-Anwendung (Dynamics 365 for Finance and Operations) fordert Daten aus dem Webdienst an (beispielsweise http://efsta.org//EFSTA-Steuerdienst) und analysiert die eingehenden Antworten, um die Anwendungsdaten entsprechend zu aktualisieren. Um auf effizienteste Weise zu analysieren, wird ein einziges EB-Format verwendet, trotz der anderen Struktur der erwarteten eingehenden Dokumente im XML-Format.   

## <a name="import-and-review-er-configurations"></a>EB-Konfigurationen importieren und überprüfen
Importieren Sie die EB-Modellkonfiguration, die das Beispieldatenmodell enthält, das entwickelt wurde, um die Details der eingehenden Datei zu speichern.  
1. Klicken Sie auf „Austauschen”.
2. Klicken Sie auf „Aus XML-Datei laden”.
    * Klicken Sie auf Durchsuchen, und wählen Sie die Datei model.xml für EFSTA aus.  
3. Klicken Sie auf "OK".
4. Wählen Sie in der Struktur die Option „EFSTA-Modell” aus.
5. Klicken Sie auf Designer.
    * Überprüfe Sie die Struktur des importierten Datenmodells. Beachten Sie, dass die enumType-Aufzählung definiert wird, um die folgenden Typen von Serviceantworten zu erkennen: die Bestätigung zur Übermittlung einer Transaktion abrufen, die Informationen über die letzte übermittelte Transaktion abrufen und nicht unterstützte Antworttypen erkennen.   
6. Erweitern Sie in der Struktur „Antwort”.
    * Beachten Sie, dass der Stammartikel „Antwort” definiert ist, um anzugeben, welche Arten von Daten aus einer Serviceantwort entnommen werden müssen, um die Anwendungsdaten entsprechend zu aktualisieren.   
7. Schließen Sie die Seite.
    * Sie importieren die EB-Formatkonfiguration, die angibt, wie die eingehenden Dokumente analysiert werden, um Daten im EB-Datenmodell zu speichern.   
8. Klicken Sie auf „Austauschen”.
9. Klicken Sie auf „Aus XML-Datei laden”.
    * Klicken Sie auf „Durchsuchen”, und wählen Sie die Datei format.xml für EFSTA aus.  
10. Klicken Sie auf "OK".
11. Erweitern Sie in der Struktur „EFSTA-Modell”.
12. Wählen Sie in der Struktur „EFSTA-Modell\EFSTA-Format” aus.
13. Klicken Sie auf Designer.
14. Klicken Sie „Erweitern/reduzieren”.
    * Beachten Sie, dass das ANFRAGE-Formatelement als Stamm verwendet wird und die drei geschachtelten DATEI-Elemente enthält, was bedeutet, dass dieses Format dazu konzipiert wurde, eingehende Dateien mehrerer Format zu analysieren.  
15. Wählen Sie in der Struktur „Antworten\Buchungsabschluss\TraC” aus.
    * Beachten Sie, dass die Antwort über die übermittelte Buchung ab dem Stammelement „TraC” beginnt.   
16. Wählen Sie in der Struktur „Antworten\Letzte Buchungsanforderung\Tra” aus.
    * Beachten Sie, dass die Antwort über die zuletzt übermittelte Buchung ab dem Stammelement „Tra” beginnt.   
17. Wählen Sie in der Struktur „Antworten\Unerwartete Antwort\Text” aus.
    * Der dritte DATEI-Element mit geschachteltem TEXT-Element wurde hinzugefügt, um alle anderen Arten von Antworten zu ermitteln, die sich von den oben genannten unterscheiden.   
18. Klicken Sie auf „Format zu Modell zuordnen”.
    * Diese Modellzuordnung enthält die Definition des Datenflusses, um Details zum analysierten eingehenden Dokuments mit Verwendung der Artikel des - Datenmodells zu speichern.  
19. Klicken Sie auf Designer.
20. Erweitern Sie in der Struktur Format.
21. In der Struktur erweitern Sie „Format\Antworten: Anfrage(Antworten)”.
    * Überprüfen Sie die Struktur der Datenquelle „Format”. Beachten Sie, dass alle drei Antworttypen getrennt angeboten werden.   
22. In der Struktur wählen Sie „Format\Antworten: Anfrage(Antworten)\aType” aus.
    * Der Datenquellenartikel „aType” wurde hinzugefügt, um den Antworttyp anzugeben, und er ist an den Datenmodellartikel „Type” gebunden.  
23. Klicken Sie auf die Registerkarte „Überprüfungen”.
24. In der Struktur wählen Sie „Type = format.Responses.aType” aus.
    * Beachten Sie, dass die EB-Prüfung konfiguriert wurde, um den Benutzer über die Situation zu informieren, wenn die Antwortstruktur nicht mit der Bestätigung zur Übermittlung der Buchung oder den Informationen zur letzten übermittelten Buchung übereinstimmt (nicht unterstützte Antwortanfrage).   
25. Schließen Sie die Seite.

## <a name="run-model-mapping-of-er-format-configured-for-parsing-incoming-files"></a>Modellzuordnung von EB-Format ausführen, das für die Analyse eingehender Dateien konfiguriert ist
Sie führen die erstellte Modellzuordnung für Testzwecke durch um zu sehen, wie das konfigurierte EB-Format eingehende Serviceantworten analyisiert. Bei diesem Schritt werden verschiedene XML-Dateien verwendet, um unterschiedliche Arten von Webdienstantworten zu simulieren.   
1. Öffnen Sie die Datei Response1.xml in einem XML-Reader, wie einem Webbrowser. Beachten Sie, dass diese Datei Bestätigungsdetails zur abgeschlossenen Buchung enthält („TraC” ist das Stammelement).   
2. Klicken Sie auf "Ausführen".
    * Klicken Sie auf „Durchsuchen”, und wählen Sie die Datei Response1.xml aus.  
3. Klicken Sie auf "OK".
    * Prüfen Sie das generierte Ergebnis. Beachten Sie, dass der Antworttyp ordnungsgemäß erkannt und analysiert wurde (ERModelEnumDataSourceHandler#EFSTA-model#enumType#C bedeutet Buchungsabschlussanfrage).   
    * Öffnen Sie die Datei Response2.xml in einem XML-Reader. Beachten Sie, dass diese Datei Informationen über die zuletzt übermittelte Buchung enthält („Tra” ist das Stammelement).   
4. Klicken Sie auf "Ausführen".
    * Klicken Sie auf „Durchsuchen”, und wählen Sie die Datei Response2.xml aus.  
5. Klicken Sie auf "OK".
    * Prüfen Sie das generierte Ergebnis. Beachten Sie, dass der Antworttyp ordnungsgemäß erkannt und analysiert wurde (ERModelEnumDataSourceHandler#EFSTA model#enumType#R bedeutet Systemneustartanfrage).   
    * Öffnen Sie die Datei Response3.xml in einem XML-Reader. Beachten Sie, dass diese Datei vom TraZ-Stammartikel beginnt und dass diese Struktur nicht mithilfe des EB-Formats konfiguriert ist.   
6. Klicken Sie auf "Ausführen".
    * Klicken Sie auf „Durchsuchen”, und wählen Sie die Datei Response3.xml aus.  
7. Klicken Sie auf "OK".
    * Prüfen Sie das generierte Ergebnis. Beachten Sie, dass der Antworttyp ordnungsgemäß als nicht unterstützt erkannt wurde (ERModelEnumDataSourceHandler#EFSTA model#enumType#U). Die entsprechenden Meldung wurde in den Infolog platziert (gemäß der EB-Prüfungseinstellung), und der größte Teil des Datenmodells ist nicht ausgefüllt worden.   
    * Öffnen Sie die Datei Response4.xml in einem XML-Reader. Beachten Sie, dass die Struktur dieser Datei fast identisch mit der erfolgreich analysierten Datei Response1.xml ist, mit Ausnahme der Reihenfolge der geschachtelten Elemente des Stammelements „TraC”.   
8. Klicken Sie auf "Ausführen".
    * Klicken Sie auf „Durchsuchen”, und wählen Sie die Datei Response4.xml aus.  
9. Klicken Sie auf "OK".
    * Prüfen Sie das generierte Ergebnis. Beachten Sie, dass der Antworttyp ordnungsgemäß als nicht unterstützt erkannt wurde (ERModelEnumDataSourceHandler#EFSTA model#enumType#U)). Die entsprechenden Meldung wurde in den Infolog platziert, und der größte Teil des Datenmodells ist nicht ausgefüllt worden. Dies liegt daran, dass bei der aktuellen Einstellung dieses EB-Formats von eine bestimmten Reihenfolge geschachtelter Elemente des Stammartikels der eingehenden Datei ausgegangen wird.   
10. Schließen Sie die Seite.
11. Wählen Sie in der Struktur „Antworten\Buchungsabschluss\TraC” aus.
12. Im Feld „Reihenfolge geschachtelter Elemente analysieren” wählen Sie „Beliebige” aus.
    * Wählen Sie „Beliebig” im Feld „Reihenfolge geschachtelter Elemente analysieren” aus, um eine beliebige Reihenfolge geschachtelter Elemente für dieses Stamm-XML-Element zuzulassen.  
13. Klicken Sie auf "Speichern".
14. Klicken Sie auf „Format zu Modell zuordnen”.
15. Klicken Sie auf "Ausführen".
    * Klicken Sie auf „Durchsuchen”, und wählen Sie die Datei Response4.xml aus.  
16. Klicken Sie auf "OK".
    * Prüfen Sie das generierte Ergebnis. Beachten Sie, dass der Antworttyp nun ordnungsgemäß als gleich für die Datei Response1.xml-Datei erkannt wurde.  

