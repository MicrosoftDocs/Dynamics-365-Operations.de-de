--- 
title: "Verwalten von Modellzuordnungskonfigurationen für elektronische Berichterstellung (ER)"
description: "In den folgenden Schritten wird erläutert, wie ein Benutzer, der der Systemadministratorrolle oder der Rolle \"Entwickler für elektronische Berichterstellung\" zugewiesen ist, einen Konfigurationsanbieter für elektronische Berichterstellung (ER) erstellen kann."
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
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
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 65db27e59ce5f9234eeb486efeb9bb6e9dad40f7
ms.contentlocale: de-de
ms.lasthandoff: 07/27/2017

---
# <a name="manage-model-mapping-configurations-for-electronic-reporting-er"></a>Verwalten von Modellzuordnungskonfigurationen für elektronische Berichterstellung (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

In den folgenden Schritten wird erläutert, wie ein Benutzer, der der Systemadministratorrolle oder der Rolle "Entwickler für elektronische Berichterstellung" zugewiesen ist, einen Konfigurationsanbieter für elektronische Berichterstellung (ER) erstellen kann. In diesem Aufgabenleitfaden erstellen Sie erforderliche ER-Konfigurationen für das Beispielunternehmen, Litware, Inc., um diesen Aufgabenleitfaden abzuschließen, müssen Sie die Schritte im Aufgabenleitfaden erst abschließen, "ER bieten einen Konfigurationsanbieter" erstellen und als aktiv markieren, ihn. 

Da ER-Konfigurationen unter Unternehmen freigegeben werden, können Sie diese Aufgabenleitfaden mithilfe der Unternehmensdaten aus, die von Ihrer Auswahl werden gefestgelegt werden. Die Funktionen für diesen Aufgabenleitfaden sind nur verfügbar, wenn einer der folgenden Hotfixes installiert haben: https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872 für die Version Dynamics AX 7,0 oder https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 der Dynamics 365 for Operations Version .

1. Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.
    * Überprüfen Sie, dass der Konfigurationsanbieter für Beispielunternehmen „Litware, Inc.” verfügbar und als aktiv markiert ist. Wenn Sie diesen Konfigurationsanbieter nicht sehen, müssen Sie zunächst die Schritte in der Prozedur „Konfigurationsanbieter erstellen und als aktiv markieren” abschließen.   

## <a name="add-a-new-er-model-configuration"></a>Neue ER-Modellkonfiguration hinzufügen
1. Klicken Sie auf "Berichterstellungskonfigurationen".
    * Neue ER-Modellkonfiguration hinzufügen. Der Name des Profils muss in der Konfigurationsstruktur eindeutig sein.  
2. Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.
3. Geben Sie im Feld "Name" Datenmodellkonfiguration" ein.
    * Muster-Datenmodell  
4. Klicken Sie auf Konfiguration erstellen.
5. Klicken Sie auf Designer.
6. Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.
7. Geben Sie im Feld Name "Root" ein.
    * Stamm  
8. Klicken Sie auf Hinzufügen.
9. Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.
10. Geben Sie im Feld Name "Firma" ein.
    * Unternehmen  
11. Klicken Sie auf Hinzufügen.
12. Im Feld Beschreibung geben Sie den Text, die Beschreibung der juristischen Personen oder des Unternehmen, in denen ein Benutzer zur Laufzeit protokollierte ein. 
    * Beschreibung der juristischen Person oder des Unternehmens, bei denen Benutzer zur Laufzeit protokollierte.  
13. Stammreferenz anklicken.
14. Klicken Sie auf "OK".
15. Klicken Sie auf "Speichern".
16. Schließen Sie die Seite.
17. Klicken Sie auf "Status ändern".
18. Klicken Sie auf "Abgeschlossen".
19. Klicken Sie auf "OK".

## <a name="add-a-new-er-model-mapping-configuration"></a>Neue ER-Daten-Modellkonfigurationszuordnung hinzufügen
1. Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.
2. Geben Sie im Feld "Neu" 'Modellzuordnung basierend auf Datenmodell-Beispielsdatenmodell ein.
3. Geben Sie im Feld "Typ" Musterzuordnung ein.
    * Musterzuordnung  
4. Klicken Sie auf Konfiguration erstellen.
5. Erweitern des Abschnitts Voraussetzungen.
    * Beachten Sie, dass die Implementierungs-Voraussetzungsgruppe automatisch hinzugefügt wurde. Diese Gruppe beinhaltet die erforderliche Komponente, die die Datenmodellkonfiguration bezieht und die Implementierungsmarkierung hat, die aktiviert ist. Diese Markierung gibt an, dass die Zuordnungskonfiguration als "Beispielzuordnungs" für die Implementierung des " Beispieldatmodell" Datenmodells gilt. Diese Komponente zwingt ER, die Beispielzuordnungs-Zuordnungskonfiguration von einem ER-Repository herunterzuladen, sobald die Beispieldatmodell-Modellkonfiguration heruntergeladen wird.   
6. Klicken Sie auf Designer.
    * Beachten Sie, dass die vorbildliche erstellte Zuordnungskonfiguration eine neue leere Zuordnung mit demselben Namen wie die erstellte Konfiguration enthält. Beachten Sie, dass, wenn eine ausgewählte Elternteilmodellkonfiguration vorbildliche Zuordnungen, enthält sie in eine Zuordnungskonfiguration des neuen Modells kopiert werden.   
7. Klicken Sie auf Designer.
8. Wählen Sie in der Strukturdarstellung "Dynamics 365 for Operations \Tabelle" aus.
9. Klicken Sie auf "Stamm hinzufügen".
10. Geben Sie im Feld Name "Firma" ein.
    * Unternehmen  
11. Im Tabellenfeld geben Sie "CompanyInfo" ein.
    * CompanyInfo  
12. Klicken Sie auf "OK".
13. Erweitern Sie in der Struktur Unternehmen.
14. In der Struktur erweitern Sie das Feld Unternehmen\Suchen ().
15. Wählen Sie in der Struktur 'Unternehmen\Namen\finden'.
16. Klicken Sie auf Binden.
17. Klicken Sie auf "Speichern".
18. Schließen Sie die Seite.
19. Schließen Sie die Seite.
20. Klicken Sie im Aktivitätsbereich auf Konfigurationen.
21. Klicken Sie auf Benutzerparameter.
22. Wählen Sie "Ja" im Feld "Testlaufeinstellungen".
23. Klicken Sie auf "OK".
24. Klicken Sie auf "Bearbeiten".
25. Wählen Sie "Ja" im Feld "Testentwurf".

## <a name="add-a-new-er-format-configuration"></a>Neues ER-Modellformat hinzufügen
1. Wählen Sie in der Struktur 'Muster Datenmodell'.
2. Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.
3. Geben Sie im Feld "Neu" 'Format basierend auf Modell Musterdatenmodell' ein.
4. Geben Sie im Feld "Typ" Musterformat ein.
    * Beispielformat  
5. Klicken Sie auf Konfiguration erstellen.
6. Klicken Sie auf Designer.
7. Klicken Sie auf "Stamm hinzufügen", um das Ablagedialogfeld zu öffnen.
8. Wählen Sie in der Struktur 'Text\String' aus.
9. Klicken Sie auf "OK".
10. Klicken Sie auf die Registerkarte Zuordnung.
11. Erweitern Sie in der -Struktur den Knoten 'Modell'.
12. Wählen Sie in der Struktur Modell\Unternehmen aus.
13. Klicken Sie auf Binden.
14. Klicken Sie auf "Speichern".
15. Schließen Sie die Seite.
    * Führt die Entwurfsversion des erstellten Formats für Testzwecke aus.  
16. Klicken Sie auf "Ausführen".
    * Wählen Sie in der Version Inforegister ausführen.  
17. Klicken Sie auf "OK".
    * Wiederholen Sie die Ausgabe, die den Namen des Unternehmens enthält, in dem der Benutzer, der ausgeführt wird, diese Formatkonfiguration angemeldet ist. Beachten Sie, dass die vorbildliche erstellte Zuordnungskonfiguration von dieser Formatkonfiguration verwendet wird, da es nur eine verfügbare Variante gibt, die erforderliche vorbildliche Zuordnungen enthält.   

## <a name="add-alternative-er-model-mapping-configuration"></a>Fügen Sie alternaitve ER-Modellzuordnungskonfiguration hinzu
1. Wählen Sie in der Struktur 'Muster Datenmodell'.
2. Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.
3. Geben Sie im Feld "Neu" 'Modellzuordnung basierend auf Datenmodell-Beispielsdatenmodell ein.
4. Geben Sie im Feld "Typ" Musterzurodnung (alternativ) ein.
    * Beispielzuordnung (Alternative)  
5. Klicken Sie auf Konfiguration erstellen.
6. Klicken Sie auf Designer.
7. Klicken Sie auf Designer.
8. Wählen Sie in der Strukturdarstellung "Dynamics 365 for Operations \Tabelle" aus.
9. Klicken Sie auf "Stamm hinzufügen".
10. Geben Sie im Feld Name "Firma" ein.
    * Unternehmen  
11. Im Tabellenfeld geben Sie "CompanyInfo" ein.
    * CompanyInfo  
12. Klicken Sie auf "OK".
13. Klicken Sie auf "Bearbeiten".
14. Wählen Sie in der Struktur 'String\CONCATENATE' aus.
15. Klicken Sie auf Funktion hinzufügen.
16. Erweitern Sie in der Struktur Unternehmen.
17. In der Struktur erweitern Sie das Feld Unternehmen\Suchen ().
18. Wählen Sie in der Struktur 'Unternehmen\Namen\finden'.
19. Klicken Sie auf Datenquelle hinzufügen.
20. Geben Sie im Feld "Formel" einen Wert ein.
    * e Company.'find()'.'name()'  
21. Wählen Sie in der Struktur 'Unternehmen\finden()\Unternehmen(DataArea).
22. Klicken Sie auf Datenquelle hinzufügen.
23. Geben Sie im Feld "Formel" einen Wert ein.
    * CONCATENATE(Company.'find()Adressbüchern. Name, "; ", Company.'find()' .DataArea)  
24. Klicken Sie auf "Speichern".
25. Schließen Sie die Seite.
26. Klicken Sie auf "Speichern".
27. Schließen Sie die Seite.
28. Schließen Sie die Seite.
29. Wählen Sie "Ja" im Feld "Testentwurf".

## <a name="use-an-existing-er-model-mapping-configuration"></a>Verwenden Sie eine vorhandene ER-Modellzuordnungskonfiguration
1. Wählen Sie in der Struktur 'Muster\Datenmodell'.
2. Klicken Sie auf "Ausführen".
    * Beachten Sie, dass die ausgewählte ER-Formatkonfiguration der Entwurfsversion nicht ausgeführt werden, weil es mehr als eine vorbildliche Zuordnungskonfiguration gibt, die für das definierten Datenmodell nicht verfügbar ist, das als Datenquelle des Ausführungsbeginns ER-Formats ausgewählt wurde.   
    * Definieren Sie als Nächstes die Zuordnungskonfiguration des alternativen Modells da, die von der als vorbildliche Zuordnungen Datenquellen für die Ausführung von ER-Format verwendet werden.   
3. Wählen Sie in der Struktur Musterdatenmodell\Musterzuordnung (alternativ).
4. Wählen Sie die Option „Ja” im Feld „Standard für Modellzuordnung” aus.
5. Wählen Sie in der Struktur 'Muster\Datenmodell'.
6. Klicken Sie auf "Ausführen".
7. Klicken Sie auf "OK".
    * Beachten Sie, dass die Standardmodellzuordnungskonfiguration von dieser Formatkonfiguration für die Generierung elektronischer Dokumente verwendet wird (die erstellten Ausgaben enthält den Unternehmenscode).  


