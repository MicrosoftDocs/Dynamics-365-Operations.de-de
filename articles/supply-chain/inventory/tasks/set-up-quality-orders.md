---
title: Qualitätsprüfungsaufträge einrichten
description: Diese Prozedur zeigt Ihnen an, wie ein Qualitätsmanagementprozess aktiviert wird, in dem eingehender Lagerbestand direkt nach der Eingangsregistrierung geprüft werden muss.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, InventTestReportSetup, InventTestTable, DefaultDashboard, InventTestVariable, InventTestVariableOutcome, InventItemSampling, InventTestQualityGroup, InventTestItemQualityGroupAdd, SysQueryForm, InventTestItemQualityGroup, InventTestGroup, InventTestAssociationTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5a073de7bdfd2ef597c09a8066ff2b6a7721ca62
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1561316"
---
# <a name="set-up-quality-orders"></a>Qualitätsprüfungsaufträge einrichten

[!include [task guide banner](../../includes/task-guide-banner.md)]

Diese Prozedur zeigt Ihnen an, wie ein Qualitätsmanagementprozess aktiviert wird, in dem eingehender Lagerbestand direkt nach der Eingangsregistrierung geprüft werden muss. Die Prozedur wird normalerweise von einem Qualitätsmanager ausgeführt. Der Prozess umfasst die Erstellung einer Qualitätsgruppe, um die Artikel zu definieren, bei denen Stichproben durchgeführt werden, und eine Testgruppe, um die Tests zu gruppieren, die an Artikeln in der Qualitätsgruppe ausgeführt werden sollen. Sie können diesen Leitfaden im Demodatunternehmen USMF ausführen.


## <a name="enable-quality-management"></a>Qualitätsmanagement aktivieren
1. Wechseln Sie zu "Lagerverwaltung" > "Einstellungen" > "Lager- und Lagerortverwaltungsparameter".
2. Klicken Sie auf die Registerkarte "Qualitätsmanagement".
3. Setzen Sie die Option Qualitätsmanagement verwenden auf Ja.
4. Klicken Sie auf "Berichtseinstellungen".
    * In USMF sind die Berichtseinstellungen für das Qualitätsmanagement bereits definiert. Wenn dieses nicht getan wäre, würden Sie hier neue Positionen für die verschiedenen Berichtstypen hinzufügen und den Dokumenttyp auswählen, der für jeden Bericht verwendet werden soll.  
5. Schließen Sie die Seite.
6. Schließen Sie die Seite.

## <a name="create-a-test"></a>Einen Test erstellen
1. Wechseln Sie zu "Lagerverwaltung" > "Einstellungen" > "Qualitätskontrolle" > "Tests".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Test" einen Wert ein.
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
5. Wählen Sie im Feld "Typ" die Option "Option" aus.
    * In diesem Beispiel wählen wir "Option" aus, damit können wir die Testergebnisse basierend auf vordefinierten Werten zuweisen.  
6. Klicken Sie auf "Speichern".
7. Schließen Sie die Seite.

## <a name="create-test-variables-to-define-the-way-test-results-are-recorded"></a>Erstellen von Testvariablen zum Definieren des Verfahrens zur Erfassung von Testergebnissen
1. Wechseln Sie zu "Lagerverwaltung" > "Einstellungen" > "Qualitätskontrolle" > "Testvariablen".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Variable" einen Wert ein.
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
5. Klicken Sie auf "Speichern".
6. Klicken Sie auf "Ergebnisse".
7. Klicken Sie auf "Neu".
8. Geben Sie im Feld "Ergebnis" einen Wert ein.
9. Geben Sie im Feld "Beschreibung" einen Wert ein.
10. Wählen Sie im Feld "Ergebnisstatus" die Option "Erfolgreich" aus.
11. Klicken Sie auf "Speichern".
12. Klicken Sie auf "Neu".
13. Geben Sie im Feld "Ergebnis" einen Wert ein.
14. Geben Sie im Feld "Beschreibung" einen Wert ein.
15. Klicken Sie auf "Speichern".
16. Schließen Sie die Seite.
17. Schließen Sie die Seite.

## <a name="set-up-item-sampling"></a>"Artikelmusteraufnahme" einrichten
1. Wechseln Sie zu "Lagerverwaltung" > "Einstellungen" > "Qualitätskontrolle" > "Artikelmusteraufnahme".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Artikelmusteraufnahme" einen Wert ein.
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
5. Geben Sie im Feld "Wert" eine Zahl ein.
    * Dieser Wert bezieht sich auf die "Mengenspezifikation", die im angrenzenden Feld ausgewählt ist.  
6. Erweitern oder reduzieren Sie den Abschnitt 'Prozess'.
7. Aktivieren oder deaktivieren Sie das Kontrollkästchen "Vollständige Sperrung".
    * Wenn Sie diese Option auswählen, wird alles oder die Auftragspositionsmenge gesperrt, wenn ein Test fehlschlägt. Wenn Sie sie nicht auswählen, werden nur die Artikel in der Testbestellung gesperrt.  
8. Klicken Sie auf "Speichern".
9. Schließen Sie die Seite.

## <a name="create-a-quality-group"></a>Eine Qualitätsgruppe erstellen
1. Wechseln Sie zu "Lagerverwaltung" > "Einstellungen" > "Qualitätskontrolle" > "Qualitätsgruppen".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Qualitätsgruppe" einen Wert ein.
    * Verwenden Sie einen beschreibenden Namen, damit Sie identifizieren können, welche Art von Artikeln die Gruppe enthalten wird (Ihre Sampling-Kriterien).  
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
5. Klicken Sie auf "Speichern".
6. Klicken Sie auf Artikel hinzufügen.
7. Die Zeile "Artikelnummer" auswählen
    * In diesem Beispiel wird der Filter auf Grundlage der Artikelnummer ausgeführt.  
8. Geben Sie im Feld "Kriterien" einen Wert ein.
    * Beispielsweise Typ T*, um nach den Artikelnummern zu filtern, die mit T starten.  
9. Klicken Sie auf "OK".
10. Klicken Sie auf "OK".
11. Klicken Sie auf "Artikelqualitätsgruppen".
12. Schließen Sie die Seite.
13. Schließen Sie die Seite.

## <a name="create-a-test-group"></a>Erstellen einer Testgruppe
1. Wechseln Sie zu "Lagerverwaltung" > "Einstellungen" > "Qualitätskontrolle" > "Testgruppen".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Testgruppe" einen Wert ein.
    * Geben Sie der Testgruppe einen Namen, womit Sie sich merken können, welche Arten von Tests ausgeführt werden und welcher Qualitätsgruppe sie zugeordnet werden soll. Beispielsweise, wenn sie mit einer Qualitätsgruppe verwendet wird, die Artikel auswählt, die mit "T" anfangen, könnten Sie sie "T-Artikel-Tests" nennen.  
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
5. Wählen Sie im Feld "Artikelmusteraufnahme" die Artikelmusteraufnahmeposition aus, die Sie zuvor erstellten.
6. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
7. Klicken Sie auf Hinzufügen.
8. Geben Sie im Feld "Laufende Nummer" eine Zahl ein.
9. Wählen Sie im Feld "Test" den Test aus, den Sie zuvor erstellt haben.
10. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
11. Klicken Sie auf die Registerkarte Test.
12. Wählen Sie im Feld "Variable" die Variable aus, die Sie zuvor erstellt haben.
13. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
14. Klicken Sie im Feld "Standardergebnis" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
15. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
16. Klicken Sie auf "Speichern".
17. Schließen Sie die Seite.

## <a name="define-when-quality-orders-will-be-created"></a>Definieren, wann Testbestellungen erstellt werden
1. Wechseln Sie zu "Lagerverwaltung" > "Einstellungen" > "Qualitätskontrolle" > "Qualitätszuordnungen".
2. Klicken Sie auf "Neu".
3. Wählen Sie im Feld "Referenztyp" eine Option aus.
4. Wählen Sie im Feld "Artikelcode" die Option "Gruppe" aus.
    * In diesem Beispiel wählen wir" Gruppe" aus und verwenden die Qualitätsgruppe, die wir zuvor erstellt hatten. Sie können dies auch als "Tabelle" festlegen, um die Artikel manuell anzugeben, oder Sie können "Alle" auswählen, um alle Artikel der Testbestellung hinzuzufügen.  
5. Wählen Sie im Feld "Artikel" die Qualitätsgruppe aus, die Sie zuvor erstellt haben.
    * Die Optionen, die im Feld "Artikel" verfügbar sind, hängen davon ab, was Sie im Feld "Artikelcode" festlegen.  
6. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
7. Erweitern oder reduzieren Sie den Abschnitt 'Prozess'.
8. Wählen Sie im Feld "Ereignistyp" eine Option aus.
    * Dies ist das Ereignis, das den Test auslöst. Die hier verfügbaren Optionen hängen davon ab, welchen Prozess Sie im Feld "Referenztyp" ausgewählt haben.  
9. Wählen Sie im Feld "Ausführung" eine Option aus.
10. Erweitern oder reduzieren Sie den Abschnitt 'Qualitätsauftragsprozess'.
11. Klicken Sie im Feld "Ereignissperrung" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
    * Dieses Feld zeigt die Liste der Prozesse an, die gesperrt werden können, wenn die Testbestellung noch offen ist. Die Optionen hängen davon ab, was Sie im Feld "Ereignistyp" ausgewählt haben.  
12. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
    * Dies hängt von den vorher ausgewählten Werten ab. Wählen Sie aus, ob die folgenden Prozesse gesperrt werden müssen, während Sie offene Testbestellungen mit einer Quelldokumentposition verknüpfen lassen.  
13. Erweitern oder reduzieren Sie den Abschnitt 'Spezifikationen'.
14. Wählen Sie im Feld "Testgruppe" die Testgruppe aus, die Sie zuvor erstellt haben.
15. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
16. Klicken Sie auf "Speichern".
17. Schließen Sie die Seite.

