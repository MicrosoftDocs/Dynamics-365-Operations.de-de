---
title: Benutzerdefinierte Felder erstellen und damit arbeiten
description: In diesem Artikel wird gezeigt, wie Sie benutzerdefinierte Felder über die Benutzerschnittstelle erstellen, um die Anwendung für ihre geschäftlichen Bedürfnisse anzupassen.
author: jasongre
ms.date: 12/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysCustomFieldManageFields
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-1-31
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: 18e7e8525352e8fdc397621c381ed4297837e30c
ms.sourcegitcommit: 69d7dd6a2d0dc7f2661c7d1f61e8874c7bde1448
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/19/2022
ms.locfileid: "9887286"
---
# <a name="create-and-work-with-custom-fields"></a>Benutzerdefinierte Felder erstellen und damit arbeiten

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Während es einen umfangreichen Satz von vorkonfigurierten Feldern gibt, um eine große Bandbreite von Geschäftsprozessen zu verwalten, besteht manchmal für ein Unternehmen der Bedarf, zusätzliche Informationen im System nachzuverfolgen. Während Programmierer verwendet werden können, um diese Felder als Erweiterungen in den Entwicklertools hinzuzufügen, können mit der Funktion für benutzerdefinierte Felder Felder direkt über die Benutzeroberfläche hinzugefügt werden, sodass Sie die Anwendung mithilfe Ihres Webbrowsers an Ihr Unternehmen anpassen können.

*Nur Benutzer mit speziellen Berechtigungen haben Zugriff auf diese Funktion.*

Dieses Video zeigt, wie einfach es ist, ein benutzerdefiniertes Feld einer Seite hinzuzufügen: [Hinzufügen von benutzerdefinierten Feldern](https://www.youtube.com/watch?v=gWSGZI9Vtnc)

## <a name="creating-custom-fields"></a>Erstellen benutzerdefinierter Felder

Nachdem Sie zusätzliche Informationen identifiziert haben, die Sie in der Anwendung nachverfolgen möchten, können Sie ein benutzerdefiniertes Feld in der entsprechenden Tabelle erstellen und dieses Feld auf einer Seite verfügbar machen.

In den folgenden Schritten wird der Prozess zum Erstellen eines benutzerdefinierten Felds und der Platzierung dieses Felds in einer Seite beschrieben.

1. Navigieren Sie zur Seite, in dem das neue Feld benötigt wird.
2. Da es das Endziel ist, das benutzerdefinierte Feld in einem Formular verfügbar zu machen, befindet sich der Einstiegspunkt zur Erstellung benutzerdefinierter Felder innerhalb der Personalisierungsoberfläche. Öffnen Sie die Personalisierungssymbolleiste, indem Sie **Optionen** auswählen und dann **Dieses Formular personalisieren**
3. Klicken Sie auf **Einfügen** und dann auf **Feld**.
4. Wählen Sie im Formular die Region aus, in der Sie das neue Feld verfügbar machen möchten. Nach der Auswahl wird das Dialogfeld **Felder einfügen** eine Liste vorhandener Feldern anzeigen, die in die ausgewählte Region auf der Seite eingefügt werden können.
5. Bestätigen Sie, dass das Feld, das Sie interessiert sind, nicht bereits in der Liste vorhanden ist. Wenn dies der Fall ist, können Sie einfach dieses Feld in der Liste auswählen und auf **Einfügen** klicken.
6. Klicken Sie auf die Schaltfläche **Neues Feld erstellen** über der Liste, um den Prozess der Erstellung eines benutzerdefinierten Felds zu initiieren. Dadurch wird das Dialogfeld **Neues Feld erstellen** geöffnet.

    Wenn Sie die Schaltfläche **Neues Feld erstellen** nicht sehen, haben Sie nicht die notwendigen Berechtigungen, um diese Funktion zu verwenden.

7. Geben Sie im Dialogfeld **Neues Feld erstellen** die folgenden Informationen ein.
   
    1. Wählen Sie die Datenbanktabelle aus, in der dieses Feld hinzugefügt werden soll. Beachten Sie, dass in der Dropdownliste nur Tabellen angezeigt werden, die benutzerdefinierte Felder unterstützen. Sehen Sie den Abschnitt unten für technische Details zu unterstützen Tabellen.

    2. Wählen Sie den Datentyp für das neue Feld aus. Die verfügbaren Datentypen sind Kontrollkästchen, Datum, Datum/Uhrzeit, Dezimal, Zahl, Auswahlliste und Text.

        - Wenn Sie den Textdatentyp auswählen, können Sie auch die maximale Länge des Texts angeben, der in diesem Feld eingegeben werden kann.
        - Wenn Sie den Auswahllisten-Datentyp auswählen, können Sie auch die Gruppe mit gültigen Werte für das Feld auswählen.

    3. Geben Sie einen Namen, eine Beschriftung und einen Hilfetext für das Feld an. Der Name entspricht dem physischen Feldnamen in der Datenbank, wohingegen die Beschriftung und der Hilfetext der Text sind, der zur Darstellung dieses Felds in der Benutzeroberfläche verwendet wird.

8. Wenn dies das einzige Feld ist, das Sie für diese Seite erstellen müssen, klicken Sie auf **Speichern**. Wenn Sie zusätzliche Felder erstellen müssen, klicken Sie auf **Speichern und neu**, und kehren Sie zu Schritt 7 zurück. 

>[!Note] 
> Aktuell gibt es eine Begrenzung von **20 benutzerdefinierten Feldern pro Tabelle**.

9. Wenn Sie das Dialogfeld **Neues Feld erstellen** verlassen, kehren Sie zum Dialogfeld **Felder einfügen** zurück. Alle benutzerdefinierten Felder, die gerade erst hinzugefügt wurden, werden automatisch in der Feldliste markiert, um in die Seite eingefügt zu werden.
10. Klicken Sie auf **Einfügen**, um die markierten Felder in den ausgewählten Bereich der Seite einzufügen.
11. **Optional:** Aktivieren Sie den Modus **Verschieben** aus der Personalisierungssymbolleiste, um die neuen Felder an die gewünschte Position im ausgewählten Bereich zu verschieben. Weitere Informationen darüber, wie die verschiedenen Personalisierungsfunktionen verwendet werden, um ein Formular für Ihre persönliche Verwendung zu optimieren, finden Sie unter [Die Benutzeroberfläche personalisieren](personalize-user-experience.md).

> [!WARNING]
> Die Möglichkeit, Werte in ein benutzerdefiniertes Feld einzugeben, das einer Seite hinzugefügt wurde, hängt davon ab, ob die dem benutzerdefinierten Feld zugeordnete Tabelle bearbeitet oder schreibgeschützt ist. Wenn die zugeordnete Tabelle schreibgeschützt ist, sind alle mit dieser Tabelle verknüpften Felder, einschließlich aller benutzerdefinierten Felder, ebenfalls schreibgeschützt.


## <a name="sharing-custom-fields-with-other-users"></a>Benutzerdefinierte Felder für andere Benutzer freigeben

Nachdem Sie ein benutzerdefiniertes Feld erstellt haben und es auf einer Seite verfügbar gemacht haben, möchten Sie vielleicht diese aktualisierte Seitenansicht bereitstellen, die das neue Feld für andere Benutzer im System enthält. Dies kann auf zwei unterschiedliche Arten mithilfe der Personalisierungsfunktionen des Produkts ausgeführt werden:

- Die empfohlene Route ist zu **Veröffentlichen einer [gespeicherte Ansicht](saved-views.md)** mit dem benutzerdefinierten Feld, das der Seite zu den entsprechenden Benutzern hinzugefügt wurde. Wenn die Funktion zum Speichern gespeicherter Ansichten nicht aktiviert ist, kann der Systemadministrator die Personalisierung über die Seite **Personalisierung** auf die gewünschten Benutzer anwenden. Weitere Informationen unter [Personalisieren der Benutzeroberfläche](personalize-user-experience.md).
- Alternativ können Sie Ihre Änderungen exportieren (genannt *Personalisierungen*), sie an einen oder mehrere Benutzer übermitteln und jeden dieser Benutzer dazu veranlassen, Ihre Änderungen zu importieren. Die Option **Verwalten** in der Personalisierungssymbolleiste ermöglich es Ihnen, Personalisierungen zu exportieren und importieren.

## <a name="managing-custom-fields"></a>Benutzerdefinierte Felder verwalten

Verwaltung aller benutzerdefinierten Felder kann über die Seite **Benutzerdefinierte Felder** im Systemverwaltungsmodul erfolgen. Diese Seite ermöglicht Benutzern den Zugriff auf viele Funktionen, einschließlich:

- Anzeigen einer Liste aller benutzerdefinierten Felder im System.
- Begrenzte Bearbeitung vorhandener benutzerdefinierter Felder.
- Löschen benutzerdefinierter Felder.
- Benutzerdefinierte Feldern in Datenentitäten verfügbar machen.
- Bereitstellen von Übersetzungen benutzerdefinierter Feldbeschriftungen und von Hilfetext.

### <a name="viewing-all-custom-fields"></a>Anzeigen aller benutzerdefinierten Felder

Die Seite **Benutzerdefinierte Felder** bietet Sichtbarkeit für alle benutzerdefinierten Felder, die im System definiert wurden. Wählen Sie die Tabelle aus, an der Sie interessiert sind, und die Seite wird aktualisiert, damit sie eine Liste der benutzerdefinierten Felder anzeigt, die dieser Tabelle zugeordnet sind. Das Auswählen eines benutzerdefinierten Felds aus der Liste ermöglicht es Ihnen, alle Details über das Feld anzuzeigen.

### <a name="editing-custom-fields"></a>Benutzerdefinierter Felder bearbeiten

Nachdem ein benutzerdefiniertes Feld erstellt wurde, können nur bestimmte Informationen über das benutzerdefinierte Feld auf der Seite **Benutzerdefinierte Felder** geändert werden.

Sie *können* diese Attribute ändern:

- Etikett
- Hilfetext
- Länge, für Textfelder

Sie *können nicht* die folgenden Attribute ändern:

- Feldname
- Datentyp

Darüber hinaus kann bei Auswahllistenfelder der Satz gültiger Werte für das benutzerdefinierte Feld neu angeordnet werden und neue Werte können hinzugefügt werden. Vorhandene Werte für das Auswahllistenfeld können jedoch nicht entfernt werden. Klicken Sie auf **Änderungen anwenden**, wenn Sie mit der Bearbeitung von Feldern für eine bestimmte Tabelle fertig sind, damit die Änderungen gespeichert werden.

### <a name="exposing-custom-fields-on-data-entities"></a>Benutzerdefinierte Felder in Datenentitäten verfügbar machen

Gegebenenfalls ist es auch wichtig, zuzulassen, dass benutzerdefinierte Felder in Datenentitäten sichtbar sind. Dateneinheiten werden in der Funktion [Office Integrationsübersicht](../../dev-itpro/office-integration/office-integration.md) sowie für Datenimport/-export-Szenarien verwendet.

Folgen Sie diesen Schritten, um ein benutzerdefiniertes Feld in einer Datenentität verfügbar zu machen:

1. Wählen Sie das benutzerdefinierte Feld auf der Seite **Benutzerdefinierte Felder** aus.
2. Erweitern Sie den Bereich **Entitäten**, um den Satz relevanter Entitäten anzuzeigen.
3. Klicken Sie auf die Schaltfläche **Bearbeiten**.
4. Ändern Sie das Feld **Aktiviert**, das für jede Entität ausgewählt werden muss, die dieses Feld verfügbar machen soll.
5. Klicken Sie auf **Änderungen anwenden**, um Ihre Auswahlen zu speichern

### <a name="allowing-custom-fields-to-be-displayed-in-other-languages"></a>Die Anzeige von benutzerdefinierten Feldern in anderen Sprachen zulassen

Da auf benutzerdefinierte Felder möglicherweise von Benutzern in einer Vielzahl von Sprachen zugegriffen werden muss, bietet die Seite **Benutzerdefinierte Felder** einen Mechanismus, der es ermöglicht, dass die Beschriftung und der Hilfetext eines benutzerdefinierten Felds in andere Sprachen übersetzt wird.

In den folgenden Schritten wird der Prozess zum Übersetzen von benutzerdefinierten Felder in andere Sprachen beschrieben:

1. Wählen Sie das benutzerdefinierte Feld auf der Seite **Benutzerdefinierte Felder** aus.
2. Aktivieren Sie die Schaltfläche **Übersetzungen** im Aktivitätsbereich. Dadurch wird ein Dropdownmenü mit vorhandenen Übersetzungen für dieses Feld geöffnet.
3. Im Dropdownmenü **Sprache** wird die Gruppe von Sprachen angezeigt, für die bereits Übersetzungen bereitgestellt wurden.

    Wenn Sie eine vorhandene Übersetzung bearbeiten möchten, wählen Sie die Sprache im Menü aus und ändern Sie die Werte für die Beschriftung und den Hilfetext.

    Andernfalls klicken Sie auf die Schaltfläche **Sprache hinzufügen**, wählen Sie die gewünschte Sprache im Menü aus, und geben Sie dann übersetzte Werte für die Beschriftung und den Hilfetext an.

4. Klicken Sie auf **OK**, wenn Sie fertig sind.

### <a name="deleting-custom-fields"></a>Benutzerdefinierte Felder löschen

Wenn Sie beschließen, dass ein benutzerdefiniertes Feld nicht mehr gebraucht wird, kann ein Systemadministrator beschließen, das Feld aus der Seite **Benutzerdefinierte Felder** zu löschen. Um ein benutzerdefiniertes Feld zu löschen, wählen Sie das zu löschende Feld aus, klicken Sie auf **Löschen**, klicken Sie auf **Ja**, um den Löschvorgang zu bestätigen, und klicken Sie schließlich auf **Änderungen anwenden**.

> [!NOTE]
> Diese Aktivität kann nicht rückgängig gemacht werden und führt dazu, dass die Daten, die diesem Feld zugeordnet sind, dauerhaft aus der Datenbank gelöscht werden.

## <a name="appendix"></a>Anhang

### <a name="why-cant-i-enter-a-value-in-my-custom-field"></a>Warum kann ich keinen Wert in mein benutzerdefiniertes Feld eingeben? 

Wenn Sie im **Bearbeitung** Modus der Seite keinen Wert in das benutzerdefinierte Feld eingeben können, liegt dies möglicherweise daran, dass die Tabelle, zu der das Feld hinzugefügt wurde, derzeit schreibgeschützt ist. Alle Felder in einer Tabelle sind schreibgeschützt, wenn die Sicherungstabelle derzeit auf der Seite als schreibgeschützt konfiguriert ist.   

### <a name="who-can-create-custom-fields"></a>Wer kann benutzerdefinierte Felder erstellen?

Standardmäßig können nur Systemadministratoren benutzerdefinierte Felder erstellen. Allerdings kann denjenigen Powerusern, die die Organisation für notwendig erachtet, Rechte erteilt werden, um benutzerdefinierte Felder durch einen Systemadministrator zu erstellen, indem die Sicherheitsrolle **Laufzeitanpassungs-Poweruser** verwendet wird. Benutzer ohne diese Sicherheitsrolle sind nicht in der Lage, benutzerdefinierte Felder zu erstellen, sie können jedoch trotzdem benutzerdefinierte Felder, die von anderen Benutzern im System hinzugefügt wurden, anzeigen und mit ihnen interagieren.

### <a name="what-tables-support-custom-fields"></a>Welche Tabellen unterstützen benutzerdefinierte Felder?

Aus Gründen der Leistung und technischen Gründen ist es nur bei Tabellen, die die folgenden Bedingungen erfüllen, aktuell zulässig, benutzerdefinierte Felder hinzuzufügen.

- Die Tabelle muss als eine dieser Gruppen markiert sein:

    - Gruppieren
    - WorksheetHeader
    - Haupttabelle
    - Sonstiges
    - Parameter
    - Referenz
    - TransactionHeader

- Die Tabelle kann keine andere Tabelle erweitern.
- Die Tabelle kann nicht als Systemtabelle markiert werden.
- Die Tabelle kann keine temporäre Tabelle sein.

### <a name="can-i-reference-custom-fields-from-the-developer-tools"></a>Kann ich in den Entwicklertools auf benutzerdefinierte Felder verweisen?  

Benutzerdefinierte Felder können nur über die Benutzeroberfläche verwaltet und nicht durch Code referenziert werden. 

### <a name="how-can-i-move-custom-fields-between-environments"></a>Wie kann ich benutzerdefinierte Felder zwischen Umgebungen verschieben? 

Die aktuelle Empfehlung zum Verschieben von benutzerdefinierten Feldern zwischen Umgebungen besteht darin, die benutzerdefinierten Felder in der Zielumgebung manuell neu zu erstellen. So zeigen Sie die vollständige Liste der benutzerdefinierten Felder in einer bestimmten Tabelle an:
1. Rufen Sie die Seite **Benutzerdefinierte Felder** auf und wählen Sie diese Tabelle aus der Dropdown-Liste aus. 
2. Folgen Sie in der Zielumgebung dem weiter oben in diesem Artikel beschriebenen Prozess, um jedes Feld neu zu erstellen. 
3. Nachdem alle Felder erstellt wurden, klicken Sie auf **Änderungen übernehmen**.  
4. Verschieben Sie alle Personalisierungen, die benutzerdefinierte Felder enthalten, indem Sie diese Personalisierungen aus der ursprünglichen Umgebung exportieren und in die Zielumgebung importieren.  


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
