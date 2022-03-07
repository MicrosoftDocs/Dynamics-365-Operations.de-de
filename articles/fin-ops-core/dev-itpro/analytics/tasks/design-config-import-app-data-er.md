---
title: EB-Konfigurationen entwerfen, um eingehende Dokumente zu analysieren
description: Diese Prozedur zeigt, wie elektronische Berichterstellungskonfigurationen (EB) entworfen werden, um ein eingehendes elektronisches Dokument für die Anwendungsdatenaktualisierung zu analysieren.
author: NickSelin
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8068850ee143540ff9f3b6222485d3ecd2a2a82020063f34cfd7b5a69826eda3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756380"
---
# <a name="design-er-configurations-to-parse-incoming-documents"></a>EB-Konfigurationen entwerfen, um eingehende Dokumente zu analysieren

[!include [banner](../../includes/banner.md)]

Diese Prozedur zeigt, wie elektronische Berichterstellungskonfigurationen (EB) entworfen werden, um ein eingehendes elektronisches Dokument für die Anwendungsdatenaktualisierung zu analysieren. In diesem Verfahren importieren Sie eine geänderte Excel-Vorlage in eine ER-Formatkonfigurationen, die für das Beispielunternehmen, Litware, Inc. erstellt wurde, und erstellen dann die elektronischen Dokumente. Um diese Schritte auszuführen, müssen Sie zunächst die Schritte unter Konfigurationsanbieter erstellen und als aktiv markieren abschließen.

Diese Prozedur wird für Benutzer erstellt, die die Rolle des Systemadministrators oder des Entwicklers für elektronische Berichterstellung haben, die ihnen zugewiesen sind.

Diese Schritte können mithilfe eines beliebigen Dataset abgeschlossen werden. Bevor Sie beginnen, laden Sie die im Thema „Eingehende Dokumente analysieren, um Anwendungsdaten zu aktualisieren“ ([Eingehende Dokumente analysieren](../parse-incoming-electronic-documents.md)) aufgelisteten Dateien herunter und speichern Sie sie. Die Dateien sind: EFSTA model.xml, EFSTA format.xml, Response1.xml, Response2.xml, Response3.xml, Response4.xml.

1. Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.
    * Überprüfen Sie, dass der Konfigurationsanbieter für Beispielunternehmen „Litware, Inc.” verfügbar und als aktiv markiert ist. Wenn Sie diesen Konfigurationsanbieter nicht sehen, müssen Sie zuerst die Schritte in der Prozedur „Konfigurationsanbieter erstellen und als aktiv markieren“ abschließen.
2. Wählen Sie Berichterstellungskonfigurationen aus.
    * Anhand des folgenden Szenarios werden die Funktionen beim Analysieren eingehender elektronischer Dokumente im XML-Format gezeigt: Die ERP-Anwendung fordert Daten vom Webdienst (z. B. vom steuerlichen Dienst der [EFSTA](http://efsta.org/) an und analysiert die eingehenden Antworten), um die Anwendungsdaten entsprechend zu aktualisieren. Um auf effizienteste Weise zu analysieren, wird ein einziges EB-Format verwendet, trotz der anderen Struktur der erwarteten eingehenden Dokumente im XML-Format.

## <a name="import-and-review-er-configurations"></a>EB-Konfigurationen importieren und überprüfen

Importieren Sie die EB-Modellkonfiguration, die das Beispieldatenmodell enthält, das entwickelt wurde, um die Details der eingehenden Datei zu speichern.

1. Wählen Sie Wechselkurs aus.
2. Wählen Sie Aus XML-Datei laden aus.
    * Wählen Sie „Durchsuchen“ aus und wählen Sie dann die Datei model.xml für EFSTA aus.
3. Wählen Sie OK.
4. Wählen Sie in der Struktur die Option „EFSTA-Modell” aus.
5. Wählen Sie Designer aus.
    * Überprüfe Sie die Struktur des importierten Datenmodells. Die enumType-Aufzählung wird definiert, um so die folgenden Typen von Serviceantworten zu erkennen: die Bestätigung zur Übermittlung einer Transaktion abrufen, die Informationen zur letzten übermittelten Transaktion abrufen und nicht unterstützte Antworttypen erkennen.
6. Erweitern Sie in der Struktur „Antwort”.
    * Der Stammartikel „Antwort“ ist definiert, um anzugeben, welche Arten von Daten aus einer Serviceantwort entnommen werden müssen, um so die Anwendungsdaten entsprechend zu aktualisieren.
7. Schließen Sie die Seite.
    * Sie importieren die EB-Formatkonfiguration, die angibt, wie die eingehenden Dokumente analysiert werden, um Daten im EB-Datenmodell zu speichern.
8. Wählen Sie Wechselkurs aus.
9. Wählen Sie Aus XML-Datei laden aus.
    * Wählen Sie „Durchsuchen“ aus und wählen Sie dann die Datei format.xml für EFSTA aus.
10. Wählen Sie OK.
11. Erweitern Sie in der Struktur „EFSTA-Modell”.
12. Wählen Sie in der Struktur „EFSTA-Modell\EFSTA-Format” aus.
13. Wählen Sie Designer aus.
14. Wählen Sie „Erweitern/Reduzieren“ aus.
    * Das ANFRAGE-Formatelement wird als Stamm verwendet und enthält die drei geschachtelten DATEI-Elemente, was bedeutet, dass dieses Format dazu konzipiert wurde, eingehende Dateien mehrerer Format zu analysieren.
15. Wählen Sie in der Struktur „Antworten\Buchungsabschluss\TraC” aus.
    * Die Antwort der übermittelten Buchung beginnt ab dem Stammelement „TraC“.
16. Wählen Sie in der Struktur „Antworten\Letzte Buchungsanforderung\Tra” aus.
    * Die Antwort der zuletzt übermittelten Buchung beginnt ab dem Stammelement „Era“.
17. Wählen Sie in der Struktur „Antworten\Unerwartete Antwort\Text” aus.
    * Der dritte DATEI-Element mit geschachteltem TEXT-Element wurde hinzugefügt, um alle anderen Arten von Antworten zu ermitteln, die sich von den oben genannten unterscheiden.
18. Wählen Sie „Format zu Modell zuordnen“ aus.
    * Diese Modellzuordnung enthält die Definition des Datenflusses, um Details zum analysierten eingehenden Dokument mit Verwendung der Artikel des - Datenmodells zu speichern.
19. Wählen Sie Designer aus.
20. Erweitern Sie in der Struktur Format.
21. In der Struktur erweitern Sie „Format\Antworten: Anfrage(Antworten)”.
    * Überprüfen Sie die Struktur der Datenquelle Format. Alle drei Antworttypen werden getrennt angeboten.
22. In der Struktur wählen Sie „Format\Antworten: Anfrage(Antworten)\aType” aus.
    * Der Datenquellenartikel „aType“ wurde hinzugefügt, um den Antworttyp anzugeben. Er ist an den Datenmodellartikel „Type“ gebunden.
23. Wählen Sie die Registerkarte „Prüfungen“ aus.
24. In der Struktur wählen Sie „Type = format.Responses.aType” aus.
    * Die EB-Prüfung wurde konfiguriert, um den Benutzer über die Situation zu informieren, wenn die Antwortstruktur nicht mit der Bestätigung zur Übermittlung der Buchung oder den Informationen zur letzten übermittelten Buchung übereinstimmt (eine nicht unterstützte Antwortanfrage).
25. Schließen Sie die Seite.

## <a name="run-model-mapping-of-er-format-configured-for-parsing-incoming-files"></a>Modellzuordnung von EB-Format ausführen, das für die Analyse eingehender Dateien konfiguriert ist

Sie führen die erstellte Modellzuordnung für Testzwecke durch um zu sehen, wie das konfigurierte EB-Format eingehende Serviceantworten analyisiert. Bei diesem Schritt werden verschiedene XML-Dateien verwendet, um unterschiedliche Arten von Webdienstantworten zu simulieren.

1. Öffnen Sie die Datei Response1.xml in einem XML-Reader, wie einem Webbrowser. Diese Datei enthält Bestätigungsdetails zur abgeschlossenen Buchung („TraC“ ist dabei das Stammelement).
2. Wählen Sie Ausführen aus.
    * Wählen Sie „Durchsuchen“ aus und wählen Sie dann die Datei Response1.xml aus.
3. Wählen Sie OK.
    * Prüfen Sie das generierte Ergebnis. Der Antworttyp wurde korrekt erkannt und analysiert (`ERModelEnumDataSourceHandler#EFSTA model#enumType#C` bedeutet Buchungsabschlussanfrage).
    * Öffnen Sie die Datei Response2.xml in einem XML-Reader. Diese Datei enthält Informationen über die zuletzt übermittelte Buchung (`Tra` ist dabei das Stammelement).
4. Wählen Sie Ausführen aus.
    * Wählen Sie „Durchsuchen“ aus und wählen Sie dann die Datei Response2.xml aus.
5. Wählen Sie OK.
    * Prüfen Sie das generierte Ergebnis. Der Antworttyp wurde korrekt erkannt und analysiert (`ERModelEnumDataSourceHandler#EFSTA model#enumType#R` bedeutet Systemneustartanfrage).
    * Öffnen Sie die Datei Response3.xml in einem XML-Reader. Diese Datei beginnt beim TraZ-Stammartikel diese Struktur ist nicht mithilfe des EB-Formats konfiguriert.
6. Wählen Sie Ausführen aus.
    * Wählen Sie „Durchsuchen“ aus und wählen Sie dann die Datei Response3.xml aus.
7. Wählen Sie OK.
    * Prüfen Sie das generierte Ergebnis. Der Antworttyp wurde korrekt als nicht unterstützt erkannt (`ERModelEnumDataSourceHandler#EFSTA model#enumType#U`). Die entsprechenden Meldung wurde in den Infolog platziert (gemäß der EB-Prüfungseinstellung), und der größte Teil des Datenmodells ist nicht ausgefüllt worden.
    * Öffnen Sie die Datei Response4.xml in einem XML-Reader. Die Struktur dieser Datei ist fast identisch mit der erfolgreich analysierten Datei Response1.xml, mit der Ausnahme der Reihenfolge der geschachtelten Elemente des Stammelements „TraC“.
8. Wählen Sie Ausführen aus.
    * Wählen Sie „Durchsuchen“ aus und wählen Sie dann die Datei Response4.xml aus.
9. Wählen Sie OK.
    * Prüfen Sie das generierte Ergebnis. Der Antworttyp wurde korrekt als nicht unterstützt erkannt (`ERModelEnumDataSourceHandler#EFSTA model#enumType#U`). Die entsprechenden Meldung wurde in den Infolog platziert, und der größte Teil des Datenmodells ist nicht ausgefüllt worden. Dieses Verhalten liegt daran, dass bei der aktuellen Einstellung dieses EB-Formats von eine bestimmten Reihenfolge geschachtelter Elemente des Stammartikels der eingehenden Datei ausgegangen wird.
10. Schließen Sie die Seite.
11. Wählen Sie in der Struktur „Antworten\Buchungsabschluss\TraC” aus.
12. Im Feld „Reihenfolge geschachtelter Elemente analysieren” wählen Sie „Beliebige” aus.
    * Wählen Sie „Beliebig“ im Feld „Reihenfolge geschachtelter Elemente analysieren“ aus, um dann eine beliebige Reihenfolge geschachtelter Elemente für dieses Stamm-XML-Element zuzulassen.
13. Wählen Sie Speichern aus.
14. Wählen Sie „Format zu Modell zuordnen“ aus.
15. Wählen Sie Ausführen aus.
    * Wählen Sie „Durchsuchen“ aus und wählen Sie dann die Datei Response4.xml aus.
16. Wählen Sie OK.
    * Prüfen Sie das generierte Ergebnis. Der Antworttyp wurde nun ordnungsgemäß als gleich für die Datei Response1.xml-Datei erkannt.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]