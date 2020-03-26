---
title: Import von Dateien im XML-Format mit optionalen Attributen
description: Dieses Thema enthält Informationen zum Entwurf von ER-Formaten, die XML-Attributen angeben, um eingehende elektronische Dokumente im XML-Format zu analysieren.
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 10795c90cb90961c17a4326b71ed43dc72039f2b
ms.sourcegitcommit: 66eae22cd99e53fe8e4c6c94945ad8061b69a442
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/11/2020
ms.locfileid: "3117424"
---
# <a name="import-files-in-xml-format-with-optional-attributes"></a>Import von Dateien im XML-Format mit optionalen Attributen

[!include [banner](../includes/banner.md)]

Sie können Elektronische Berichterstellung (ER)-Formate entwerfen, um eingehende Dokumente im XML-Format zu generieren. Bestimmte Attribute von XML-Elementen können in entworfenem ER-Format als optional angegeben werden. Es ermöglicht Ihnen, eingehende Dateien mit und ohne diese XML-Attribute korrekt zu bearbeiten. Sie können den Inhalt aus diesen Dateien dann verwenden, um Anwendungsdaten zu aktualisieren.

Um mehr über diese Funktion zu erfahren, führen Sie die Schritte im Thema [(RCS) Importieren von Dateien im XML-Format mit optionalen Attributen](tasks/import-files-xml-format-optional-attributes.md) aus, die Teil des Geschäftsprozesses 7.5.4.3 Acquire/Develop IT service/solution components (10677) sind. Sie können diesen Aufgabenleitfaden und die zugeordneten Beispieldateien vom [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684) herunterladen.


| Inhaltsbeschreibung       | Datei                                                         |
|---------------------------|--------------------------------------------------------------|
| Beispieldatei im XML-Format | IncomingDocumentToLearnHowToHandleOptionalAttributes.xml     |
| Aufgabenleitfaden                | (RCS) Importiert Dateien im XML-Format mit optionalen Attributen.axtr |


In den folgenden Schritten wird erläutert, wie ein Benutzer, der der Systemadministratorrolle oder der Rolle Entwickler für elektronische Berichterstellung zugewiesen ist, eine ER-Formatkonfiguration entwerfen kann, um die Dateien im XML-Format, die optionale Attribute enthalten, zu importieren. Um diese Schritte abzuschließen, müssen Sie zunächst die Schritte der Vorgehensweise [Konfigurationsanbieter anlegen und als aktiv markieren](tasks/er-configuration-provider-mark-it-active-2016-11.md). Bevor Sie beginnen, laden Sie die IncomingDocumentToLearnHowToHandleOptionalAttributes.xml-Datei aus dem Microsoft Download Center(https://go.microsoft.com/fwlink/?linkid=874684) und herunter speichern Sie sie lokal.

1. Wechseln Sie zu **Organisationsverwaltung**  >  **Arbeitsbereiche**  >  **Elektronische Berichterstellung**.
2. Überprüfen Sie, dass der Konfigurationsanbieter für Beispielunternehmen „Litware, Inc.” verfügbar und als **Aktiv** markiert ist. Wenn Sie diesen Konfigurationsanbieter nicht sehen, führen Sie die Schritte im Thema [Konfigurationsanbieter anlegen aus und markieren Sie ihn als aktiv](tasks/er-configuration-provider-mark-it-active-2016-11.md).
3. Klicken Sie auf **Berichterstellungskonfigurationen**.

## <a name="create-a-new-data-model-configuration"></a>Neue Datenmodellkonfiguration erstellen
1. Klicken Sie auf **Konfiguration erstellen** um das Dropdown-Dialogfeld zu öffnen.
2. Geben Sie im Feld **Name** Modell ein, um die XML-Datei zu importieren.
3. Klicken Sie auf **Konfiguration erstellen**.
4. Klicken Sie auf **Designer**.
5. Klicken Sie auf **Neu** zum Öffnen des Ablagedialogfeld.
6. Geben Sie im Feld **Name** Stamm ein.
7. Klicken Sie auf **Hinzufügen**.
8. Klicken Sie auf **Neu** zum Öffnen des Ablagedialogfeld.
9. Geben Sie im Feld **Name** Liste ein.
10.    Wählen Sie im Feld **Artikeltyp** **Datensatzliste** aus.
11.    Klicken Sie auf **Hinzufügen**.
12.    Klicken Sie auf **Neu** zum Öffnen des Ablagedialogfeld.
13.    Geben Sie im Feld **Name** 'Code' ein.
14.    Wählen Sie im Feld **Artikeltyp** **Zeichenfolge** aus.
15.    Klicken Sie auf **Hinzufügen**.
16.    Klicken Sie auf **Speichern**.
17.    Schließen Sie die Seite.
18.    Klicken Sie auf **Status ändern**.
19.    Klicken Sie auf **Abgeschlossen**.
20.    Klicken Sie auf **OK**.

## <a name="create-a-format-for-data-import"></a>Erstellen Sie ein Format für den Datenimport
1. Klicken Sie auf **Konfiguration erstellen** um das Dropdown-Dialogfeld zu öffnen.
2. Geben Sie im Feld **Neu** Format basierend auf Datenmodell, um die xml Datei zum importieren ein.
3. Geben Sie im Feld **Name** 'Formatieren, um XML-Datei zu importieren' ein. 
4. Wählen Sie die Option **Ja** im Feld **Unterstützt Datenimport** aus.
5. Klicken Sie auf **Konfiguration erstellen**.

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a>Entwerfen Sie ein Format, um eingehende Datei im XML-Format zu analysieren
1. Klicken Sie auf **Designer**.
2. Klicken Sie auf **Stamm hinzufügen**, um das Ablagedialogfeld zu öffnen.
3. Wählen Sie in der Struktur den Knoten **XML\Element**.
4. Geben Sie im Feld **Name** Stamm ein.
5. Klicken Sie auf **OK**.
6. Klicken Sie zum Öffnen des Ablage-Dialogfelds auf **Hinzufügen**.
7. Wählen Sie in der Struktur den Knoten **XML\Element**.
8. Geben Sie im Feld **Name** 'Dokument' ein.
9. Wählen Sie im **Vielfältigkeitsgebiet** **viele** aus.
10.    Klicken Sie auf **OK**.
11.    Wählen Sie in der Struktur **Root\Dokument**.
12.    Klicken Sie zum Öffnen des Ablage-Dialogfelds auf **Hinzufügen**.
13.    Wählen Sie in der Struktur **XML\Attribute** aus.
14.    Geben Sie im Feld **Name** 'ID' ein.
15.    Klicken Sie auf **OK**.
16.    Klicken Sie auf **Speichern**.

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a>Entwerfen Sie eine Formatzuordnung, um analysierte Informationen zum Datenmodell zu speichern
1.    Klicken Sie auf **Format zu Modell zuordnen**.
2.    Klicken Sie auf **Neu**.
3.    Geben Sie im Feld **Definition** einen Wert ein, oder wählen Sie einen Wert aus.
4.    Geben Sie im Feld **Name** 'Zuordnung' ein.
5.    Klicken Sie auf **Speichern**.
6.    Klicken Sie auf **Designer**.
7.    Erweitern Sie in der Struktur **Format**.
8.    Erweitern Sie in der Struktur **format\root: XML Element(root)**.
9.    Wählen Sie in der Struktur **format\root: XML Element(root)\document: XML Element 1..* (dokument)**.
10.    Klicken Sie auf **Binden**.
11.    Erweitern Sie in der Struktur **format\root: XML Element(root)\document: XML Element 1..* (dokument)**.
12.    Wählen Sie in der Struktur **format\root: XML Element(root)\document: XML Element 1..* (dokument)\id**.
13.    Erweitern Sie in der Struktur **Liste = format.root.dokument**.
14.    Wählen Sie in der Struktur **Liste = format.root.dokument\code**.
15.    Klicken Sie auf **Binden**.
16.    Klicken Sie auf **Speichern**.
17.    Schließen Sie die Seite.

## <a name="run-format-mapping"></a>Formularzuordnung ausführen
1. Klicken Sie auf **Ausführen**.
2. Klicken Sie auf **Durchsuchen** und wählen Sie die Datei **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml** aus.
3. Klicken Sie auf **OK**.

> [!NOTE]
> Die ausgewählte Datei wurde nicht importiert, da das Formatdesign die Präsenz der Kennung des Attributs für das Element Dokument annimmt, aber die importierte Datei enthält kein solches Attribut.

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a>Ändern Sie die Formatstruktur, um XML-Attribute optional zu ermöglichen
1. Schließen Sie die Seite.
2. Erweitern Sie in der Struktur **root\dokument**.
3. Wählen Sie in der Struktur **Root\dokument\id**.
4. Wählen Sie **Ja** im Feld **Leere Zeichenfolge für fehlendes Attribut** aus.
5. Klicken Sie auf **Speichern**.

## <a name="run-format-mapping-to-test-changes"></a>Führen Sie die Formatzuordnung zu den Teständerungen aus
1. Klicken Sie auf **Format zu Modell zuordnen**.
2. Klicken Sie auf **Ausführen**.
3. Klicken Sie auf **Durchsuchen** und wählen Sie die Datei **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml** aus.
4. Klicken Sie auf **OK**.
5. Erstellte XML Datei überprüfen. Beachten Sie, dass dieselbe Datei importiert wurde, da das Formatdesign nun das  ID-Attribut für das Element Dokument als optional betrachtet.
