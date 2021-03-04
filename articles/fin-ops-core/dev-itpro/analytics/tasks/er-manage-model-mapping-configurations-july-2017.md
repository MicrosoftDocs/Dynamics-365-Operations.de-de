---
title: EB-Modellzuordnung in getrennten EB-Konfigurationen verwalten
description: In den folgenden Schritten wird erläutert, wie ein Benutzer, der der Systemadministratorrolle oder der Rolle "Entwickler für elektronische Berichterstellung" zugewiesen ist, einen Konfigurationsanbieter für elektronische Berichterstellung (ER) erstellen kann.
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4e59e9f2dd5a0fa6d5955e3d93d25759a478ede7
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684426"
---
# <a name="manage-er-model-mapping-in-separate-er-configurations"></a>EB-Modellzuordnung in getrennten EB-Konfigurationen verwalten

[!include [banner](../../includes/banner.md)]

In den folgenden Schritten wird erläutert, wie ein Benutzer, der der Systemadministratorrolle oder der Rolle "Entwickler für elektronische Berichterstellung" zugewiesen ist, einen Konfigurationsanbieter für elektronische Berichterstellung (ER) erstellen kann. In diesem Aufgabenleitfaden erstellen Sie erforderliche ER-Konfigurationen für das Beispielunternehmen, Litware, Inc., um diesen Aufgabenleitfaden abzuschließen, müssen Sie die Schritte im Aufgabenleitfaden erst abschließen, „ER bieten einen Konfigurationsanbieter“ erstellen und als aktiv markieren, ihn. 

Da ER-Konfigurationen unter Unternehmen freigegeben werden, können Sie diese Aufgabenleitfaden mithilfe der Unternehmensdaten aus, die von Ihrer Auswahl werden gefestgelegt werden. Die Funktionen für diesen Aufgabenleitfaden sind nur verfügbar, wenn Sie einen der folgenden Hotfixes installiert haben: https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872 für die Dynamics AX 7.0 Version oder https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 für die Dynamics 365 for Operations Version.

1. Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.
    * Überprüfen Sie, dass der Konfigurationsanbieter für Beispielunternehmen „Litware, Inc.” verfügbar und als aktiv markiert ist. Wenn Sie diesen Konfigurationsanbieter nicht sehen, müssen Sie zunächst die Schritte in der Prozedur „Konfigurationsanbieter erstellen und als aktiv markieren“ abschließen.   

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

## <a name="add-a-new-er-model-mapping-configuration"></a>Neue EB-Modellzuordnungskonfiguration hinzufügen
1. Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.
2. Geben Sie im Feld "Neu" 'Modellzuordnung basierend auf Datenmodell-Beispielsdatenmodell ein.
3. Geben Sie im Feld "Typ" Musterzuordnung ein.
    * Musterzuordnung  
4. Klicken Sie auf Konfiguration erstellen.
5. Erweitern des Abschnitts Voraussetzungen.
    * Die Implementierungs-Voraussetzungsgruppe wurde automatisch hinzugefügt. Diese Gruppe beinhaltet die erforderliche Komponente, die die Datenmodellkonfiguration bezieht und die Implementierungsmarkierung hat, die aktiviert ist. Diese Markierung gibt an, dass diese Modellzuordnungskonfiguration als „Beispielzuordnung“ zur Implementierung des „Beispieldatenmodells“ gilt. Diese Komponente zwingt die EB, die Modellzuordnungskonfiguration für die Beispielzuordnung von einem EB-Repository herunterzuladen, sobald die Modellkonfiguration für das Beispieldatenmodell heruntergeladen wird.   
6. Klicken Sie auf Designer.
    * Die erstellte Modellzuordnungskonfiguration enthält eine neue leere Zuordnung mit demselben Namen wie die erstellte Konfiguration. Wenn eine ausgewählte übergeordnete Modellkonfiguration Modellzuordnungen enthält, werden diese in eine neue Modellzuordnungskonfiguration kopiert.   
7. Klicken Sie auf Designer.
8. Wählen Sie in der Struktur 'Dynamics 365 for Operations\Tabelle' aus.
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
    * Wiederholen Sie die Ausgabe, die den Namen des Unternehmens enthält, in dem der Benutzer, der ausgeführt wird, diese Formatkonfiguration angemeldet ist. Die erstellte Modellzuordnungskonfiguration wird von dieser Formatkonfiguration verwendet, da es nur eine verfügbare Konfiguration gibt, die erforderliche Modellzuordnungen enthält.   

## <a name="add-alternative-er-model-mapping-configuration"></a>Alternative EB-Modellzuordnungskonfiguration hinzufügen
1. Wählen Sie in der Struktur 'Muster Datenmodell'.
2. Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.
3. Geben Sie im Feld "Neu" 'Modellzuordnung basierend auf Datenmodell-Beispielsdatenmodell ein.
4. Geben Sie im Feld "Typ" Musterzurodnung (alternativ) ein.
    * Beispielzuordnung (Alternative)  
5. Klicken Sie auf Konfiguration erstellen.
6. Klicken Sie auf Designer.
7. Klicken Sie auf Designer.
8. Wählen Sie in der Struktur 'Dynamics 365 for Operations\Tabelle' aus.
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

## <a name="use-an-existing-er-model-mapping-configuration"></a>Eine vorhandene EB-Modellzuordnungskonfiguration verwenden
1. Wählen Sie in der Struktur 'Muster\Datenmodell'.
2. Klicken Sie auf Ausführen.
    * Die ausgewählte Entwurfsversion der EB-Formatkonfiguration kann nicht ausgeführt werden, weil es mehr als eine Modellzuordnungskonfiguration gibt, die für das nicht definierte Datenmodell verfügbar ist, das als Datenquelle für das ausgeführte EB-Format ausgewählt wurde.   
    * Definieren Sie als Nächstes die alternative Modellzuordnungskonfiguration als diejenige Konfiguration, aus der Modellzuordnungen als Datenquellen für das ausgeführte EB-Format verwendet werden.   
3. Wählen Sie in der Struktur Musterdatenmodell\Musterzuordnung (alternativ).
4. Wählen Sie die Option „Ja” im Feld „Standard für Modellzuordnung” aus.
5. Wählen Sie in der Struktur 'Muster\Datenmodell'.
6. Klicken Sie auf Ausführen.
7. Klicken Sie auf "OK".
    * Die Standardkonfiguration der Modellzuordnung wird von dieser Formatkonfiguration zur Generierung elektronischer Dokumente verwendet (die erstellte Ausgabe enthält den Buchungskreis).  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]