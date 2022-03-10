---
title: Datenmodelldefinitionen beim Erstellen von Formaten auswählen
description: Um diese Schritte auszuführen, müssen Sie zunächst die Schritte unter "Konfigurationsanbieter erstellen und als aktiv markieren" abschließen.
author: NickSelin
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 34e6c8df735976ca0f7805fe3e06f141d38abf12faf02ff66195339147aa5405
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6720831"
---
# <a name="select-data-model-definitions-when-you-create-formats"></a>Datenmodelldefinitionen beim Erstellen von Formaten auswählen

[!include [banner](../../includes/banner.md)]

Um diese Schritte auszuführen, müssen Sie zunächst die Schritte unter "Konfigurationsanbieter erstellen und als aktiv markieren" abschließen. 

Dieses Verfahren zeigt, wie Stammartikel eines Modells als Datenmodelldefinition zum Einfügen einer elektronischen meldenden (ER)- Formatkonfiguration ausgewählt werden kann, die dazu da ist, um elektronische Dokumente zu generieren. In dieser Prozedur fügen Sie eine neue ER-Formatkonfigurartion für das Beispielunternehmen „Litware, Inc.” hinzu. 

Diese Prozedur ist für Benutzer bestimmt, die die Rolle des Systemadministrators oder des elektronischen Berichtsentwicklers haben, die ihnen zugewiesen sind. Die Schritte können abgeschlossen werden, indem Sie einen Datensatz verwenden.

1. Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.
    * Überprüfen Sie, dass der Konfigurationsanbieter für Beispielunternehmen „Litware, Inc.” verfügbar und als aktiv markiert ist. Wenn Sie diesen Konfigurationsanbieter nicht sehen, müssen Sie zuerst die Schritte in der Prozedur „Konfigurationsanbieter erstellen und als aktiv markieren“ abschließen.  
2. Klicken Sie auf "Berichterstellungskonfigurationen".

## <a name="add-a-new-er-data-model-configuration"></a>Neue ER-Daten-Modellkonfiguration hinzufügen
1. Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.
    * Wir fügen eine neue ER-Modellkonfiguration hinzu, die das Datenmodell enthält, das entwickelt wurde, die als Datenquelle für das Generieren des Intrastat-Berichts verwendet werden.  
2. Geben Sie im Feld "Name" "Zahlungsmodell (fiktiv) ein.
    * Zahlungsmodell (fiktiv)  
3. Klicken Sie auf Konfiguration erstellen.
4. Klicken Sie auf Designer.
    * Öffnen Sie den ER-Designer, um die Struktur des Datenmodells dieser Variante angeben.  
    * Angenommen, dass wir das Datenmodell für Zahlungen entwerfen, um damit die 2-Zahlungsgeschäftsdomänen-Methoden - Kreditübertragungen und Direktbelastungen.  
5. Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.
6. Geben Sie im Feld "Name" Typ Zahlung - Kreditübertragung ein.
    * Zahlungen - Überweisungszahlung  
7. Klicken Sie auf Hinzufügen.
8. Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.
9. Geben Sie im Feld „Neuer Knoten als ein Feld” die Bezeichnung „Modellwurzel” ein.
10. Geben Sie im Feld "Name" Typ Zahlung - Direktbelastung ein.
    * Zahlungen - Direkteinzugszahlungen  
11. Klicken Sie auf Hinzufügen.
12. Klicken Sie auf "Speichern".
13. Schließen Sie die Seite.
14. Klicken Sie auf "Status ändern".
    * Schließt die Entwurfsversion des Modells ab, um die neuen Zuordnungsmodelle und Formate verfügbar zu machen.  
15. Klicken Sie auf "Abgeschlossen".
16. Klicken Sie auf "OK".

## <a name="start-to-enter-a-new-er-format-configuration"></a>Start, um eine neue ER-Formatkonfiguration einzugeben
1. Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.
2. Geben Sie im Feld "Neu" 'Format basierend auf Modell Zahlungsmodell (fiktiv) ein.
3. Geben Sie im Feld "Datenmodelldefinition" einen Wert ein, oder wählen Sie einen Wert aus.
    * Beachten Sie, dass alle Stammartikel des Datenmodells für die ausgewählten Auswahl als Datenmodelldefinition im Zeitpunkt vorhanden sind. Sie können fortfahren, um das Format zu entwerfen, indem Sie eines der erforderlichen Stammartikel des - Datenmodells verwenden. Eine fehlende Modellzuordnung für den ausgewählten Stammartikel hindert Sie nicht am Fortsetzen.  
4. Schließen Sie die Seite.

## <a name="add-a-new-er-model-mapping-configuration"></a>Neue ER-Daten-Modellkonfigurationszuordnung hinzufügen
1. Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.
2. Geben Sie im Feld "Neu" 'Modellzuordnung basierend auf Datenmodell-Zahlungsmodell (fiktiv) ein.
3. Geben Sie im Feld "Name" "Zahlungsmodellzuordnung (fiktiv) ein.
    * Zahlungsmodell-Zuordnungen (fiktiv)  
4. Geben Sie im Feld "Datenmodelldefinition" einen Wert ein, oder wählen Sie einen Wert aus.
5. Klicken Sie auf Konfiguration erstellen.

## <a name="design-er-model-mappings"></a>Modellzuordnungsdesigner
1. Klicken Sie auf Designer.
    * Verwenden Sie den ER-Designer, um das Lagermodell der Zuordnungen für die erforderlichen Stammartikel anzugeben.  
2. Klicken Sie auf Designer.
    * Einrichtung ausgewälter Modellzuordnungen für den ausgewählten Stammartikel des Modells simulieren.  
3. Wählen Sie in der Struktur 'Dynamics 365 for Operations\Tabellendatensätze' aus.
4. Klicken Sie auf "Stamm hinzufügen".
5. Geben Sie im Feld Name den Typ Sachkonto ein.
6. Im Tabellenfeld geben Sie "LedgerJournalTrans" ein.
    * LedgerJournalTrans  
7. Klicken Sie auf "OK".
8. Klicken Sie auf "Speichern".
9. Schließen Sie die Seite.
10. Schließen Sie die Seite.

## <a name="start-to-enter-another-new-er-format-configuration"></a>Start, um eine andere ER-Formatkonfiguration einzugeben
1. Wählen Sie in der Struktur die Option "Zahlungsmodell" (fiktiv) aus.
2. Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.
3. Geben Sie im Feld "Neu" 'Format basierend auf Modell Zahlungsmodell (fiktiv) ein.
4. Geben Sie im Feld "Datenmodelldefinition" einen Wert ein, oder wählen Sie einen Wert aus.
    * Beachten Sie, dass ein Stammartikel nun verfügbar ist, um diesen den Bewerbungsdatenquellen zuzuordnen. Wenn mindestens eine vorbildliche Zuordnung eingegeben wird, werden nur die Stammartikel des Modells, die den Bewerbungsdatenquellen zugeordnet werden, als vorbildliche Definition ausgewählt werden können, für die das ER-Format hinzugefügt wird.   
5. Schließen Sie die Seite.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]