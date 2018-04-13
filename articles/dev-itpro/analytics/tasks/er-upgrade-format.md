--- 
title: "Aktualisieren des Formats durch Verwendung einer neuen Basisversion dieses Formats für elektronische Berichterstellung"
description: "In den folgenden Schritten wird erläutert, wie ein Benutzer, der der Systemadministratorrolle oder der Rolle \"Entwickler für elektronische Berichterstellung\" zugewiesen ist, eine Formatkonfiguration für elektronische Berichterstellung (ER) verwalten kann."
author: NickSelin
manager: AnnBe
ms.date: 02/06/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: cfc68c1d0810cbc296b35c09176dde2c948a50d0
ms.contentlocale: de-de
ms.lasthandoff: 03/26/2018

---
# <a name="upgrade-your-format-by-adopting-of-new-base-version-of-that-format-for-electronic-reporting-er"></a>Aktualisieren des Formats durch Verwendung einer neuen Basisversion dieses Formats für elektronische Berichterstellung

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

In den folgenden Schritten wird erläutert, wie ein Benutzer, der der Systemadministratorrolle oder der Rolle "Entwickler für elektronische Berichterstellung" zugewiesen ist, eine Formatkonfiguration für elektronische Berichterstellung (ER) verwalten kann. Diese Prozedur zeigt, wie eine benutzerdefinierte Version eines Formats auf Grundlage des Formats erstellt werden kann, das von einem Konfigurationsanbieter (CP) eingeht. Sie zeigt auch, wie eine neue Basisversion für dieses Format übernommen wird.



Um diese Schritte abzuschließen, müssen Sie zuerst die Schritte in den Prozeduren "Konfigurationsanbieter erstellen und ihn als aktiv markieren" und "Erstelltes Format zum Generieren elektronischer Dokumente für Zahlungen verwenden" abschließen. Diese Schritte können im GBSI-Unternehmen ausgeführt werden.


## <a name="select-format-configuration-for-customization"></a>Wählen Sie Formatkonfiguration zur Anpassung aus
1. Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.
    * In diesem Beispiel dient das Beispielunternehmen Litware, Inc. (`http://www.litware.com`) als ein Konfigurationsanbieter, der Formatkonfigurationen für elektronische Zahlungen für ein bestimmtes Land unterstützt.  Musterunternehmen Proseware, Inc. (`http://www.proseware.com`) fungiert als Kunde der Formatkonfiguration, die Litware, Inc. bereitstellt. Proseware, Inc. verwendet Formate in bestimmten Regionen dieses Landes.  
2. Klicken Sie auf "Berichterstellungskonfigurationen".
3. Klicken Sie auf "Filter anzeigen".
4. Wenden Sie die nachfolgenden Filter an: Geben Sie einen Filterwert für „BACS (Großbritannien fiktive Namen)” im Feld „Name” unter Verwendung des Filteroperators „beginnt mit” ein
    * BACS (Großbritannien fiktiven Namens)  
    * Die ausgewählte Formatkonfiguration BACS (Großbritannien, fiktiv) gehört dem Anbieter Litware, Inc.  
5. Klicken Sie auf "Filter anzeigen".
6. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Die Version des Formats mit dem Status "Fertig" wird von Proseware, Inc. für die Anpassung verwendet.  

## <a name="create-a-new-configuration-for-your-custom-format-of-electronic-document"></a>Erstellen Sie eine neue Konfiguration für Ihr benutzerdefiniertes Format des elektronischen Dokuments
Proseware, Incerhielt Version 1.1 der Konfiguration BACS (Großbritannien, fiktiv), die das anfängliche Format zum Generieren elektronischer Zahlungsdokumente von Litware, Inc. enthält. Proseware, Inc.möchte damit beginnen, dies als Standard für ihr Land zu verwenden, aber einige Anpassung ist erforderlich, um bestimmte regionale Anforderungen zu unterstützen. Proseware, Inc.möchte auch die Möglichkeit behalten, ein benutzerdefiniertes Format zu aktualisieren, sobald eine neue Version davon (mit Änderungen, um neue, länderspezifische Anforderungen zu unterstützen) von Litware, Inc. kommt  Um dies zu bewerkstelligen, muss Proseware, Inc. eine Konfiguration mit den Litware, Inc.- Konfiguration BACS (BRITISCHES als Basis erfundenes) erstellen.  
1. Schließen Sie die Seite.
2. Wählen Sie die Proseware, Inc. als Anbieter aus und machen Sie ihn aktiv.
3. Klicken Sie auf "Als aktiv festlegen"
4. Klicken Sie auf "Berichterstellungskonfigurationen".
5. Erweitern Sie "Zahlungen (vereinfachtes Modell)" in der Struktur.
6. Wählen Sie "Zahlungen (vereinfachtes Modell)\BACS (Großbritannien, fiktiv)" in der Struktur aus.
    * Wählen Sie die Konfigurations- BACS (BRITISCHE erfundenes) aus Litware, Inc. Proseware, Inc. verwendet Version 1,1 als Basis für die benutzerdefinierte Version aus.  
7. Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.
    * Dies ermöglicht Ihnen, eine neue Konfiguration für ein benutzerdefiniertes Zahlungsformat zu erstellen.  
8. Geben Sie im Feld "Neu" die Bezeichnung "Von Name ableiten: BACS (Großbritannien, fiktiv), Litware, Inc." ein.
    * Wählen Sie die Ableitungsoption aus, um die Verwendung von BACS (Großbritannien, fiktive Namen) als Grundlage für die Erstellung der benutzerdefinierten Version zu bestätigen.  
9. Geben Sie im Feld "Name" die Bezeichnung "BACS (Großbritannien, fiktiv benutzerdefiniert)" ein.
    * BACS (Großbritannien, fiktiv benutzerdefiniert)  
10. Geben Sie im Feld „Beschreibung” die Bezeichnung „BACS-Kreditorenzahlung (Großbritannien fiktive Namen)” ein.
    * BACS-Kreditorenzahlung (Großbritannien, fiktiv benutzerdefiniert)  
    * Der aktive Konfigurationsanbieter (Proseware, Inc.) wird automatisch hier eingegeben. Dieser Anbieter ist in der Lage, diese Konfiguration verwalten. Andere Anbieter können diese Konfiguration verwenden, werden jedoch nicht in der Lage sein, sie zu verwalten.  
11. Klicken Sie auf Konfiguration erstellen.

## <a name="customize-your-format-for-the-electronic-document"></a>Passen Sie Ihr Format für das elektronische Dokument an
1. Klicken Sie auf Designer.
2. Klicken Sie „Erweitern/reduzieren”.
3. Klicken Sie „Erweitern/reduzieren”.
4. Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel\Kreditor\Bank” aus.
5. Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".
6. Wählen Sie in der Struktur den Knoten 'XML\Element'.
7. Geben Sie im Feld "Name" "IBAN" ein.
    * IBAN  
8. Klicken Sie auf "OK".
9. Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel\Kreditor\Bank\IBAN” aus.
10. Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".
11. Wählen Sie in der Struktur 'Text\String' aus.
12. Klicken Sie auf "OK".
13. Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel\Kreditor\Name\Zeichenfolge” aus.
14. Geben Sie im Feld "Höchstlänge" die Zahl "60" ein.
15. Klicken Sie auf die Registerkarte Zuordnung.
16. Erweitern Sie in der -Struktur den Knoten 'Modell'.
17. Erweitern Sie 'Modell\Zahlungen' in der Struktur.
18. Erweitern Sie 'Modell\Payments\Creditor' in der Struktur.
19. In der Struktur erweitern Sie "Modell\Zahlungen\Kreditor\Konto".
20. Wählen Sie in der Struktur „Modell\Zahlungen\Kreditor\Konto\IBAN” aus.
21. Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel =  model.Payments\Vendor\Bank\IBAN\String” aus.
22. Klicken Sie auf Binden.
23. Klicken Sie auf "Speichern".

## <a name="validate-the-customized-format"></a>Überprüfen Sie das benutzerdefinierte Format
1. Klicken Sie auf "Überprüfen".
    * Überprüfen Sie die benutzerdefinierten Formatlayout- und Datenzuordnungsänderungen, um sicherzustellen, dass alle Bindungen in Ordnung sind.  
2. Schließen Sie die Seite.

## <a name="change-the-status-of-the-current-version-of-the-custom-format-configuration"></a>Ändern Sie den Status der aktuellen Version der benutzerdefinierten Formatkonfiguration
    * Ändern Sie den Status der entworfenen Formatkonfiguration von „Entwurf” zu „Abgeschlossen”, um sie für die Generierung von Zahlungsdokumenten verfügbar zu machen.  
1. Klicken Sie auf "Status ändern".
    * Beachten Sie, dass die aktuelle Version der ausgewählten Konfiguration im Status "Entwurf" ist.  
2. Klicken Sie auf "Abgeschlossen".
3. Geben Sie im Feld "Beschreibung" einen Wert ein.
4. Klicken Sie auf "OK".
5. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Beachten Sie, dass die erstellte Konfiguration als abgeschlossene Version 1.1.1 gespeichert wird. Das bedeutet, es ist Version 1 des benutzerdefinierten BACS-Formats (Großbritannien, fiktiv benutzerdefiniert), das auf Version 1 des BACS-Formats (Großbritannien, benutzerdefiniert) basiert, das auf Version 1 des Datenmodells "Zahlungen" (vereinfachtes Modell) beruht.  

## <a name="test-the-customized-format-to-generate-payment-files"></a>Testen Sie das benutzerdefinierte Format, um Zahlungsdateien zu generieren
Schließen Sie die Schritte in der Prozedur „Erstelltes Format zum Generieren von elektronischen Dokumenten für Zahlungen verwenden” in einer parallelen Dynamics 365 for Finance and Operations ab. Wählen Sie das Format BACS (Großbritannien, fiktiv benutzerdefiniert) in den Methodenparametern für die elektronische Zahlung aus. Stellen Sie sicher, dass die erstellte Zahlungsdatei den vor kurzem eingeführten XML-Knoten enthält, der den IBAN-Code in Übereinstimmung mit regionalen Anforderungen darstellt.  

## <a name="update-the-existing-country-specific-configuration"></a>Aktualisieren Sie die vorhandene landesspezifische Konfiguration
Litware, Inc muss die Konfiguration "BACS (Großbritannien, fiktiv)" aktualisieren und neue Länderanforderungen für die Verwaltung des Formats des elektronischen Dokuments verwenden. Später wird dies in einer neuen Version dieser Konfiguration eingeschlossen sein, die Dienstleistungsabonnenten angeboten wird, einschließlich Proseware, Inc..  

In den realen Prozessen, die mit der Dienstleistungsbereitstellung verknüpft sind, kann jede neue Version von BACS (Großbritannien, fiktiv) von Litware, Inc. importiert werden. In dieser Prozedur simulieren wir dies, indem wir BACS (Großbritannien, fiktiv) im Auftrag eines Dienstanbieters aktualisieren.

1. Schließen Sie die Seite.
2. Anbieter Litware, Inc. wählen
3. Klicken Sie auf "Als aktiv festlegen"
4. Klicken Sie auf "Berichterstellungskonfigurationen".
5. Erweitern Sie "Zahlungen (vereinfachtes Modell)" in der Struktur.
6. Wählen Sie "Zahlungen (vereinfachtes Modell)\BACS (Großbritannien, fiktiv)" in der Struktur aus.
    * Die Entwurfversion von Litware, Inc. Anbieter BACS (Großbritannien, fiktiv)" wird ausgewählt, um Änderungen einzuführen, um neue länderspezifische Anforderungen zu unterstützen.  

## <a name="localize-the-base-format-of-the-electronic-document"></a>Lokalisieren Sie das Basisformat des elektronischen Dokuments
Angenommen, es gibt neue landesspezifische Anforderungen, um Litware unterstützt werden:  
- Ein Wert des SWIFT-Codes der Bank des Kreditors für jede Zahlungsbuchung.  
- Eine Begrenzung auf 100 Zeichen für die Textlänge des Namens des Händlers in einer generierenden Datei.  
 
Wählen Sie die Entwurfsversion der gewünschten Konfiguration aus, um erforderliche Änderungen einzuführen.  

1. Klicken Sie auf Designer.
2. Klicken Sie „Erweitern/reduzieren”.
3. Klicken Sie „Erweitern/reduzieren”.
4. Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel\Kreditor\Bank” aus.
5. Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".
6. Wählen Sie in der Struktur den Knoten 'XML\Element'.
7. Geben Sie im Feld "Name" "SWIFT" ein.
    * SWIFT BIC  
8. Klicken Sie auf "OK".
9. Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel\Kreditor\Bank\SWIFT” aus.
10. Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".
11. Wählen Sie in der Struktur 'Text\String' aus.
12. Klicken Sie auf "OK".
13. Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel\Kreditor\Name\Zeichenfolge” aus.
14. Geben Sie im Feld "Höchstlänge" die Zahl "100" ein.
15. Klicken Sie auf die Registerkarte Zuordnung.
16. Erweitern Sie in der -Struktur den Knoten 'Modell'.
17. Erweitern Sie 'Modell\Zahlungen' in der Struktur.
18. Erweitern Sie 'Modell\Payments\Creditor' in der Struktur.
19. In der Struktur erweitern Sie "Modell\Zahlungen\Kreditor\Agent".
20. Wählen Sie in der Struktur Folgendes aus: „Modell\Zahlungen\Kreditor\Agent\SWIFT”.
21. Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel =  model.Payments\Vendor\Bank\SWIFT\String” aus.
22. Klicken Sie auf Binden.
23. Klicken Sie auf "Speichern".

## <a name="validate-the-localized-format"></a>Überprüfen Sie das lokalisierte Format
1. Klicken Sie auf "Überprüfen".
2. Schließen Sie die Seite.

## <a name="change-the-status-of-the-current-version-of-the-base-format-configuration"></a>Ändern Sie den Status der aktuellen Version der Basisformatkonfiguration
Ändern Sie den Status der aktualisierten Basisformatkonfiguration von "Entwurf" zu "Abgeschlossen", um sie für die Generierung von Zahlungsdokumenten und Updates der daraus abgeleiteten Formatkonfigurationen verfügbar zu machen.  
1. Klicken Sie auf "Status ändern".
    * Beachten Sie, dass die aktuelle Version der ausgewählten Konfiguration im Status "Entwurf" ist.  
2. Klicken Sie auf "Abgeschlossen".
3. Geben Sie im Feld "Beschreibung" einen Wert ein.
4. Klicken Sie auf "OK".
5. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.

## <a name="change-the-base-version-for-the-custom-format-configuration"></a>Ändern Sie die Basisversion für die benutzerdefinierte Formatkonfiguration
Proseware, Inc. ist darüber informiert, dass eine neue Version 1.2 der Konfiguration "BACS (Großbritannien, fiktiv)" verfügbar ist, um Dokumente für die elektronische Zahlung in Übereinstimmung mit vor kurzem angekündigten landesspezifischen Anforderungen zu generieren. Proseware, Inc. möchte damit beginnen, diese als Standard für das Land zu verwenden.  Dazu muss Proseware, Inc. die Basiskonfigurationsversion für die benutzerdefinierte Konfiguration "BACS (Großbritannien, fiktiv)" ändern. Anstelle Version 1.1 von "BACS (Großbritannien, fiktiv)" verwenden Sie die neue Version 1.2.  

1. Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.
2. Wählen Sie die Proseware, Inc. aus. Anbieter, um sie als aktiv zu markieren.
3. Klicken Sie auf "Als aktiv festlegen"
4. Klicken Sie auf "Berichterstellungskonfigurationen".
5. Erweitern Sie "Zahlungen (vereinfachtes Modell)" in der Struktur.
6. Erweitern Sie "Zahlungen (vereinfachtes Modell)\BACS (Großbritannien, fiktiv)" in der Struktur.
7. Wählen Sie "Zahlungen (vereinfachtes Modell)\BACS (Großbritannien, fiktiv)\BACS (Großbritannien, fiktiv benutzerdefiniert)" in der Struktur aus.
    * Wählen Sie die Konfiguration BACS (Großbritannien, fiktiv benutzerdefiniert) aus, die Proseware, Inc. gehört.  
    * Verwenden Sie die Entwurfsversion der ausgewählten Konfiguration, um erforderliche Änderungen einzuführen.  
8. Klicken Sie auf "Zurücksetzen".
    * Wählen Sie die neue Version 1.2 der Basiskonfiguration aus, die als neue Basis zur Aktualisierung der Konfiguration angewendet werden soll.  
9. Klicken Sie auf "OK".
    * Beachten Sie, dass einige Konflikte zwischen der Zusammenführung der benutzerdefinierten Version und der neuen Version ermittelt worden sind. Diese stellen einige Formatänderungen dar, die nicht automatisch zusammengeführt werden können.  

## <a name="resolve-rebase-conflicts"></a>Lösen Sie Konflikte beim Zurücksetzen auf
1. Klicken Sie auf Designer.
    * Beachten Sie, dass Änderungen der Längenbegrenzung des Händlernamentexts nicht automatisch aufgelöst werden können. Daher wird dies in einer Konfliktliste dargestellt. Für jeden Konflikt vom Typ "Update" stehen folgende Optionen zur Verfügung: - Wenden Sie einen früheren Basiswert (Schaltfläche über dem Raster) an, um den vorherigen Basisversionswert (0 in unserem Fall) aufzufüllen.  - Wenden Sie einen Basiswert (Schaltfläche über dem Raster) an, um den neuen Basisversionswert (100 in unserem Fall) aufzufüllen.  - Behalten Sie Ihren eigenen (benutzerdefinierten) Wert (60 in unserem Fall).  Klicken Sie auf "Basiswert anwenden", um eine länderspezifische Begrenzung auf 100 Zeichen für die Textlänge von Händlernamen anzuwenden.  
    * Beachten Sie, dass Proseware, Inc. und Litware, Inc. benutzerdefinierten und lokale Versionen dieses Formats haben. Diese verwenden IBAN- und SWIFT-Codes mit zugehörigen Komponenten, die automatisch im verwaltenden Format zusammengeführt werden.  
2. Klicken Sie auf "Basiswert anwenden".
    * Klicken Sie auf "Basiswert anwenden", um die länderspezifische Begrenzung auf 100 Zeichen für Händlernamen anzuwenden.  
3. Klicken Sie auf "Speichern".
    * Durch Speichern des Formats werden nicht aufgelöste Konflikte aus der Konfliktliste entfernt.  
4. Schließen Sie die Seite.

## <a name="change-the-status-of-the-new-version-of-the-custom-format-configuration"></a>Ändern Sie den Status der neuen Version der benutzerdefinierten Formatkonfiguration
1. Klicken Sie auf "Status ändern".
    * Ändern Sie den Status der aktualisierten, benutzerdefinierten Formatkonfiguration von "Entwurf" zu "Abgeschlossen". Dadurch wird die Formatkonfiguration für das Generieren von Zahlungsdokumenten verfügbar. Beachten Sie, dass die aktuelle Version der ausgewählten Konfiguration im Status "Entwurf" ist.  
2. Klicken Sie auf "Abgeschlossen".
3. Geben Sie im Feld "Beschreibung" einen Wert ein.
4. Klicken Sie auf "OK".
    * Beachten Sie, dass die erstellte Konfiguration als abgeschlossene Version 1.2.2 gespeichert wird: Version 2 des Basisformats "BACS (Großbritannien, fiktiv benutzerdefiniert)", das auf Version 2 des Basisformats "BACS (Großbritannien, fiktiv)" beruht, das auf Version 1 des Datenmodells "Zahlungen" (vereinfachtes Modell) beruht.  

## <a name="test-the-customized-format-for-payment-files-generation"></a>Testen Sie das benutzerdefinierte Format zum Generieren von Zahlungsdateien
Schließen Sie die Schritte in der Prozedur „Erstelltes Format zum Generieren von elektronischen Dokumenten für Zahlungen verwenden” in einer parallelen Dynamics 365 for Finance and Operations Sitzung ab. Wählen Sie das erstellte Format "BACS (Großbritannien, fiktiv benutzerdefiniert)" in den Methodenparametern für die elektronische Zahlung aus. Stellen Sie sicher, dass die erstellte Zahlungsdatei den vor kurzem von Proseware, Inc.eingeführten XML-Knoten enthält, der den IBAN-Code in Übereinstimmung mit regionalen Anforderungen darstellt. Die Datei sollte auch den vor kurzem von LItware, Inc. eingegeben XML Knoten enthalten, der in SWIFT-Bankleitzahl die Übereinstimmung der Landanforderungen darstellt.  


