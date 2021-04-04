---
title: Abhängigkeit von ER-Konfigurationen von anderen Komponenten festlegen
description: In diesem Thema wird beschrieben, wie Sie eine EB-Konfiguration (elektronische Berichterstellung) entwerfen und ihre Abhängigkeit von anderen Softwarekomponenten angeben.
author: NickSelin
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d37a10b1430349014f55cde155c6ed6e85dfe3dc
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567317"
---
# <a name="define-the-dependency-of-er-configurations-on-other-components"></a>Abhängigkeit von ER-Konfigurationen von anderen Komponenten festlegen

[!include [banner](../../includes/banner.md)]

Um diese Schritte auszuführen, müssen Sie zunächst die Schritte im Aufgabenleitfaden ausführen (Verwalten von Modellzuordnungskonfigurationen für elektronische Berichterstellung), und Sie müssen Zugriff auf Microsoft Dynamics Lifecycle Services (LCS) haben.

Dieses Verfahren zeigt, wie eine Konfiguration für die elektronische Berichterstellung (ER) entworfen wird, und definiert die Abhängigkeit von anderen Softwarekomponenten, damit Sie sicherstellen können, dass die Konfiguration für eine bestimmten Version von Finance and Operations ordnungsgemäß heruntergeladen wurde. In diesem Beispiel erstellen Sie die erforderlichen ER-Konfigurationen für das Beispielunternehmen Litware, Inc. 

Diese Prozedur ist für Benutzer bestimmt, die die Rolle des Systemadministrators oder des elektronischen Berichtsentwicklers haben, die ihnen zugewiesen sind. Diese Schritte können an einem beliebigen Unternehmen ausgeführt werden, da die ER-Konfiguration von allen Unternehmen genutzt werden. 

1. Wechseln Sie zu Organisationsverwaltung > Elektronische Berichterstellung > Konfigurationen.
    * Stellen Sie aber sicher, dass die Konfigurationsstruktur Musterdatenmodellkonfiguration und untergeordnete Elemente enthält. Andernfalls schließen Sie die Schritte im Aufgabenleitfaden ab, ER Modellzuordnungskonfigurationen verwaltewn und starten Sie dieses anschließend erneut.   

## <a name="define-the-dependency-of-er-configurations-from-other-components"></a>Definieren Sie diese Abhängigkeit der ER-Konfigurationen von anderen Komponenten
1. Wählen Sie in der Struktur 'Muster Datenmodell' erweitern.
2. Wählen Sie in der Struktur Musterdatenmodell\Musterzuordnung.
    * Wir wählten die Entwurfsversion der Zuordnungskonfiguration Beispielzuordnungs-Modell aus. Wir definieren jetzt die Abhängigkeit von anderen Softwarekomponenten. Dieser Schritt gilt als eine Voraussetzung für das Steuern des Downloads der Version dieser Konfiguration von einem EB-Repository und von jeder dieser Version.   
3. Erweitern des Abschnitts Voraussetzungen.
    * Beachten Sie, dass die Implementierungs-Voraussetzungsgruppe nun automatisch hinzugefügt wurde. Diese Gruppe beinhaltet die erforderliche Komponente, die die Datenmodellkonfiguration bezieht und die Implementierungsmarkierung hat, die aktiviert ist. Diese Markierung gibt an, dass die Zuordnungskonfiguration als Beispielzuordnung für die Implementierung des Beispieldatmodell Datenmodells gilt. Diese Komponente zwingt EB, die Beispielzuordnungs-Zuordnungskonfiguration von einem EB-Repository herunterzuladen, sobald die Beispieldatmodell-Modellkonfiguration heruntergeladen wird.   
4. Klicken Sie auf Bearbeiten.
    * Eine einzelne Abhängigkeit von der aktuellen Version einer Konfiguration aus einer Softwarekomponente kann angegeben werden, indem die Definition der Komponente und entweder die Teilversion oder ein Bereich mit Teilversionen verwendet wird.  
    * Gewünschte Abhängigkeiten können gruppiert werden. Wenn Alle Gruppentypen aktiviert ist, gilt der Abhängigkeitszustand dieser Gruppe als erfüllt, wenn jede Abhängigkeitsbedingung aus dieser Gruppe und der untergeordneten Gruppe erfüllt ist. Wenn einer der Gruppentypen aktiviert ist, gilt der Abhängigkeitszustand dieser Gruppe als erfüllt, wenn mindestens eine Abhängigkeitsbedingung aus dieser Gruppe und der untergeordneten Gruppe erfüllt ist.   
5. Klicken Sie auf "Neu".
6. Wählen Sie Produktvoraussetzungskomponente aus.
7. Microsoft Dynamics 365 for Operations (1611) auswählen.
8. Geben Sie im Feld Version Typ '(7.1.1541.3036,8)' ein.
    * (7.1.1541.3036,8)  
    * Abhängigkeiten, die Sie eingeben, werden ausgewertet, wenn die Konfiguration von einem beliebigen ER-Repository heruntergeladen wird. Diese wird aus der RCS-Repository Variantenversion heruntergeladen, wenn Version 1 der Beispieldatmodell- Konfiguration entweder bereits an der richtigen Stelle ist oder im Voraus heruntergeladen wurde. Wenn sie vorab heruntergeladen wird, muss sie in Finance and Operations Version 7.1.1541.3036 oder höher abgeschlossen werden, darf aber Hauptversion 8 nicht überschreiten.   
9. Klicken Sie auf "Speichern".
10. Schließen Sie die Seite.
11. Klicken Sie auf "Status ändern".
12. Klicken Sie auf "Abgeschlossen".
13. Klicken Sie auf "OK".
14. Wählen Sie in der Struktur Musterdatenmodell\Musterzuordnung (alternativ).
15. Klicken Sie auf "Bearbeiten".
16. Klicken Sie auf "Neu".
17. Wählen Sie Produktvoraussetzungskomponente aus.
18. Wählen Sie Microsoft Dynamics AX 7.0 RTW aus.
19. Geben Sie im Feld Version Typ '(7.0.1265.3015,7.1)' ein.
    * (7.0.1265.3015,7.1)  
    * Abhängigkeiten, die Sie eingeben, werden ausgewertet, wenn die Konfiguration von einem beliebigen ER-Repository heruntergeladen wird. Diese wird aus der RCS-Repository Variantenversion heruntergeladen, wenn Version 1 der Beispieldatmodell- Konfiguration entweder bereits an der richtigen Stelle ist oder im Voraus heruntergeladen wurde. Wenn sie im Voraus heruntergeladen wird, muss sie in Microsoft Dynamics 365 for Finance and Operations Enterprise Edition abgeschlossen werden, wobei die Version 7.0.1265.3015 oder höher sein muss, aber die Nebenversion 1 nicht überschreiten darf.   
20. Klicken Sie auf "Speichern".
21. Schließen Sie die Seite.
22. Klicken Sie auf "Status ändern".
23. Klicken Sie auf "Abgeschlossen".
24. Klicken Sie auf "OK".

## <a name="configure-the-er-repository"></a>Konfigurieren Sie das ER-Repository
1. Schließen Sie die Seite.
2. Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.
    * Öffnen Sie die Liste von Repositorys für den aktuellen ER-Anbieter "Litware, Inc.".  
3. Markieren Sie in der Liste die ausgewählte Zeile.
4. Klicken Sie auf Repositorys.
5. Klicken Sie auf "Filter anzeigen".
6. Verwenden Sie den Filteroperator LCS im Filterwert Typ mithilfe des Filterzeichesn "Enthält".
    * Wenn das LCS-Repository bereits für den aktuellen ER-Anbieter erfasst wird, können Sie die übrigen Schritte in dieser Unteraufgabe überspringen. Wenn das LCS-Repository nicht bereits erfasst wird, führen Sie die verbleibenden Schritte aus.   
7. Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".
8. Wählen Sie im Feld "Konfigurationsrepository-Typ" die Option "LCS" aus.
9. Klicken Sie auf "Repository erstellen".
10. Geben Sie im Feld "Projekt" einen Wert ein, oder wählen Sie einen Wert aus.
    * Wählen Sie das gewünschte LCS-Projekt von der Suche im Feld Projekt aus.  
11. Klicken Sie auf "OK".
12. Schließen Sie die Seite.

## <a name="upload-configurations-to-lcs"></a>Laden Sie Konfiguration in LCS hoch
1. Klicken Sie auf "Berichterstellungskonfigurationen".
2. Wählen Sie in der Struktur 'Muster Datenmodell'.
3. Wählen Sie die abgeschlossene Version der aktuellen Konfiguration aus.
4. Klicken Sie auf "Status ändern".
5. Klicken Sie auf "Freigeben".
6. Klicken Sie auf "OK".
    * Version 1 dieser Konfiguration eines Projekt-Planzahlenmodells wird mit LCS hochgeladen, indem Sie das LCS-Projekt für das verwendete ER-Repository verwenden, das zuvor konfiguriert wurde.   
7. Wählen Sie in der Struktur 'Muster Datenmodell' erweitern.
8. Wählen Sie in der Struktur Musterdatenmodell\Musterzuordnung.
9. Wählen Sie die abgeschlossene Version der aktuellen Konfiguration aus.
10. Klicken Sie auf "Status ändern".
11. Klicken Sie auf "Freigeben".
12. Klicken Sie auf "OK".
    * Version 1.1 dieser Modellzuordnungskonfiguration wurde in LCS hochgeladen, indem Sie das LCS-Projekt für das verwendete ER-Repository verwenden, das zuvor konfiguriert wurde.   
13. Wählen Sie in der Struktur Musterdatenmodell\Musterzuordnung (alternativ).
14. Wählen Sie die abgeschlossene Version der aktuellen Konfiguration aus.
15. Klicken Sie auf "Status ändern".
16. Klicken Sie auf "Freigeben".
17. Klicken Sie auf "OK".
    * Version 1.1 dieser Modellzuordnungskonfiguration wurde in LCS hochgeladen, indem Sie das LCS-Projekt für das verwendete ER-Repository verwenden, das zuvor konfiguriert wurde.   

## <a name="evaluate-er-configuration-dependencies"></a>Überprüfen der ER-Konfigurationsabhängigkeiten
Wir werden erstellte Konfigurationen löschen und laden sie erneut vom LCS-Repository herunter.  
1. Wählen Sie in der Struktur Musterdatenmodell\Musterzuordnung.
2. Klicken Sie auf Löschen.
3. Klicken Sie auf "Ja".
4. Wählen Sie in der Struktur Musterdatenmodell\Musterzuordnung (alternativ).
5. Klicken Sie auf Löschen.
6. Klicken Sie auf "Ja".
7. Wählen Sie in der Struktur 'Muster\Datenmodell'.
8. Klicken Sie auf Löschen.
9. Klicken Sie auf "Ja".
10. Wählen Sie in der Struktur 'Muster Datenmodell'.
11. Klicken Sie auf Löschen.
12. Klicken Sie auf "Ja".
13. Schließen Sie die Seite.
    * Öffnen Sie die Liste von Repositorys für den aktuellen ER-Anbieter "Litware, Inc.".  
14. Klicken Sie auf Repositorys.
15. Klicken Sie auf "Filter anzeigen".
16. Verwenden Sie den Filteroperator LCS im Filterwert Typ mithilfe des Filterzeichesn "Enthält".
17. Klicken Sie auf "Öffnen".
18. Wählen Sie in der Struktur 'Muster Datenmodell'.
    * Beachten Sie, dass Sie eine Bewertung anzeigen könne, ob die Voraussetzungsbedingungen für jede version der ER-Konfiguration für das aktuelle Repository erfüllt wurde. Um diese Bewertung anzuzeigen, klicken Sie auf Scheck-Voraussetzungen.   
19. Voraussetzungen überprüfen anklicken.
20. Klicken Sie auf Import.
21. Klicken Sie auf "Ja".
22. Schließen Sie die Seite.
23. Schließen Sie die Seite.
24. Schließen Sie die Seite.
25. Wechseln Sie zu Organisationsverwaltung > Elektronische Berichterstellung > Konfigurationen.
26. Wählen Sie in der Struktur 'Muster Datenmodell' erweitern.
    * Beachten Sie, dass die vorbildliche Beispielzuordnung Zuordnungskonfiguration zusammen mit der gewählten Datenmodellkonfiguration heruntergeladen wurde. Die zwei Dateien werden zusammen heruntergeladen, da die „Beispielzuordnung“ als Implementierung des ausgewählten Datenmodells definiert wurde und weil sie für die Anwendung anwendbar ist. Die Variante Beispielzuordnung (Alternative) ist nicht heruntergeladen worden, da die Bedingung für die erforderliche Anwendungsversion nicht erfüllt ist.   
    * Wenn Sie sich bei Finance and Operations anmelden, registrieren Sie den gleichen Anbieter, greifen auf das gleiche LCS-Projekt zu und laden die gleiche Datenmodellkonfiguration, die Beispielzuordnung (Alternative) herunter, während die Beispielzuordnung-Konfiguration übersprungen wird.  


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]