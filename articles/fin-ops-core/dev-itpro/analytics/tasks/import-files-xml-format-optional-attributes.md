---
title: (RCS) Importiert Dateien im XML-Format mit optionalen Attributen
description: Dieser Artikel enthält Informationen darüber, wie ein Benutzer ER-Formatkonfiguration entwerfen kann, um Dateien im XML-Format mit optionalen Attributen zu importieren.
author: kfend
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ''
ms.openlocfilehash: 5254a3d631129d0e41fcd37a341b54f97cfe6a9e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290003"
---
# <a name="rcs-import-files-in-xml-format-with-optional-attributes"></a>(RCS) Importiert Dateien im XML-Format mit optionalen Attributen

[!include [banner](../../includes/banner.md)]

In den folgenden Schritten wird erläutert, wie ein Benutzer, der der Systemadministratorrolle oder der Rolle Entwickler für elektronische Berichterstellung zugewiesen ist, eine ER-Formatkonfiguration entwerfen kann, um die Dateien im XML-Format, die optionale Attribute enthalten, zu importieren. Um diese Schritte auszuführen, müssen Sie zunächst die Schritte unter „Konfigurationsanbieter erstellen und als aktiv markieren“ abschließen. Bevor Sie beginnen, laden Sie die IncomingDocumentToLearnHowToHandleOptionalAttributes.xml-Datei aus [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684) und herunter speichern Sie sie lokal.

1.    Wechseln Sie zu **Alle Arbeitsbereiche** > **Elektronische Berichterstellung**.
2.    Überprüfen Sie, dass der Konfigurationsanbieter für Beispielunternehmen „Litware, Inc.” verfügbar und als **Aktiv** markiert ist. Wenn Sie diesen Konfigurationsanbieter nicht sehen, müssen Sie zunächst die Schritte in der Prozedur [Konfigurationsanbieter erstellen und diesen als aktiv markieren](er-configuration-provider-mark-it-active-2016-11.md) abschließen.
3.    Klicken Sie auf **Berichterstellungskonfigurationen**.

## <a name="create-a-new-data-model-configuration"></a>Neue Datenmodellkonfiguration erstellen
1.    Klicken Sie auf **Konfiguration erstellen** um das Dropdown-Dialogfeld zu öffnen.
2.    Geben Sie im Feld **Name** Modell ein, um die XML-Datei zu importieren.
3.    Klicken Sie auf **Konfiguration erstellen**.
4.    Klicken Sie auf **Designer**.
5.    Klicken Sie auf **Neu** zum Öffnen des Ablagedialogfeld.
6.    Geben Sie im Feld **Name** Stamm ein.
7.    Klicken Sie auf **Hinzufügen**.
8.    Klicken Sie auf **Neu** zum Öffnen des Ablagedialogfeld.
9.    Geben Sie im Feld **Name** Liste ein.
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
1.    Klicken Sie auf **Konfiguration erstellen** um das Dropdown-Dialogfeld zu öffnen.
2.    Geben Sie im Feld **Neu** Format basierend auf Datenmodell, um die xml Datei zum importieren ein.
3.    Geben Sie im Feld **Name** „Formatieren, um XML-Datei zu importieren“ ein.
4.    Wählen Sie die Option **Ja** im Feld **Unterstützt Datenimport** aus.
5.    Klicken Sie auf **Konfiguration erstellen**.

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a>Entwerfen Sie ein Format, um eingehende Datei im XML-Format zu analysieren
1.    Klicken Sie auf **Designer**.
2.    Klicken Sie auf **Stamm hinzufügen**, um das Ablagedialogfeld zu öffnen.
3.    Wählen Sie in der Struktur den Knoten **XML\Element**.
4.    Geben Sie im Feld **Name** Stamm ein.
5.    Klicken Sie auf **OK**.
6.    Klicken Sie zum Öffnen des Ablage-Dialogfelds auf **Hinzufügen**.
7.    Wählen Sie in der Struktur den Knoten **XML\Element**.
8.    Geben Sie im Feld **Name** 'Dokument' ein.
9.    Wählen Sie im **Vielfältigkeitsgebiet** **viele** aus.
10.    Klicken Sie auf **OK**.
11.    Wählen Sie in der Struktur **Root\Dokument**.
12.    Klicken Sie zum Öffnen des Ablage-Dialogfelds auf **Hinzufügen**.
13.    Wählen Sie in der Struktur **XML\Attribute** aus.
14.    Geben Sie im Feld **Name** „ID“ ein.
15.    Klicken Sie auf **OK**.
16.    Klicken Sie auf **Speichern**.

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a>Entwerfen Sie eine Formatzuordnung, um analysierte Informationen zum Datenmodell zu speichern
1. Klicken Sie auf **Format zu Modell zuordnen**.
2. Klicken Sie auf **Neu**.
3. Geben Sie im Feld **Definition** einen Wert ein, oder wählen Sie einen Wert aus.
4. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
5. Geben Sie im Feld **Name** 'Zuordnung' ein.
6. Klicken Sie auf **Speichern**.
7. Klicken Sie auf **Designer**.
8. Erweitern Sie in der Struktur **Format**.
9. Erweitern Sie in der Struktur **format\root: XML Element(root)**.
10.    Wählen Sie in der Struktur **format\root: XML Element(root)\document: XML Element 1..* (dokument)**.
11.    Klicken Sie auf **Binden**.
12.    Erweitern Sie in der Struktur **format\root: XML Element(root)\document: XML Element 1..* (dokument)**.
13.    Wählen Sie in der Struktur **format\root: XML Element(root)\document: XML Element 1..* (dokument)\id**.
14.    Erweitern Sie in der Struktur **Liste = format.root.dokument**.
15.    Wählen Sie in der Struktur **Liste = format.root.dokument\code**.
16.    Klicken Sie auf **Binden**.
17.    Klicken Sie auf **Speichern**.
18.    Schließen Sie die Seite.
 
## <a name="run-format-mapping"></a>Formularzuordnung ausführen
1. Klicken Sie auf **Ausführen**.
2. Klicken Sie auf **Durchsuchen** und wählen Sie **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml** aus.
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
3. Klicken Sie auf **Durchsuchen** und wählen Sie die **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**-Datei aus.
4. Klicken Sie auf **OK**.
5. Erstellte XML Datei überprüfen. 

> [!NOTE]
> Dieselbe Datei wurde importiert, da das Formatdesign nun das „ID“-Attribut für das Element „Dokument“ als optional betrachtet.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
