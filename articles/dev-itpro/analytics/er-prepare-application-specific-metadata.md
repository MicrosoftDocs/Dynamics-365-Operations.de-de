---
title: Bereiten Sie anwendungsspezifische Metadaten für RCS und ER vor
description: In diesem Thema wird erläutert, wie anwendungsspezifische Metadaten für Regulatory Configuration Service (RCS) und elektronische Berichterstellung (ER) vorbereitet werden.
author: NickSelin
manager: AnnBe
ms.date: 04/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 289f901501a68319c9d85e993d8dfbfc3838a8eb
ms.sourcegitcommit: d940c7892b6caa6141b3bda8abf1c56e9df4687a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/03/2019
ms.locfileid: "1726431"
---
# <a name="prepare-application-specific-metadata-for-rcs"></a>Vorbereiten anwendungsspezifischer Metadaten für RCS

[!include[banner](../includes/banner.md)]

Dieses Thema führt Sie durch Beispiele der folgenden Aufgaben:

- [Vorbereiten von Anwendungs-Metadaten zur Verwendung in RCS](#prepare-application-metadata-that-can-be-used-in-rcs)
- [Zugriff auf Anwendungs-Metadaten über die ER-Konfiguration](#access-application-metadata-by-using-an-er-configuration)
- [Zugriff auf Anwendungs-Metadaten über verbundene Anwendungen](#access-application-metadata-by-using-connected-applications)

## <a name="prepare-application-metadata-that-can-be-used-in-rcs"></a>Vorbereiten von Anwendungs-Metadaten zur Verwendung in RCS

Die folgenden Prozedur zeigt, wie ein Finance and Operations-Benutzer mit der **Systemadministrator**- oder der **Elektronische Berichtsentwickler**-Rolle eine elektronische Berichterstellungskonfiguration (ER) erstellen kann, die die Metadaten für die Microsoft Dynamics 365 for Finance and Operations-Anwendung enthält und für das Entwerfen der ER-Modellzuordnungskonfigurationen im Regulatory Configuration Service (RCS) verwendet wird. Die Beispiel-ER-Modellzuordnungskonfiguration, die in diesem Beispiel erstellt wird, wird verwendet, um auf Außenhandelsbuchungen zuzugreifen.

In diesem Beispiel verwenden Sie RCS um eine ER-Lösung für eine Finance and Operations zu entwerfen, die verwendet wird, um elektronische Dokumente zu erstellen, die Informationen aus der Außenhandelsgeschäftsdomäne enthält. Um die Zuordnung zwischen dem ER-Datenmodell und den Quellen der erforderlichen Daten anzugeben, müssen Sie Zugriff auf die Anwendungs-Metadaten für Finance and Operations in RCS haben. Daher konfigurieren müssen Sie als Teil des Entwurfsprozesses der ER-Lösung eine neue ER-Metadatenkonfiguration konfigurieren, die alle Metadaten enthält, die zur Generierung der ER-Berichte für ausgewählte Geschäftsdomänen derzeit erforderlich sind.

> [!NOTE]
> In diesem Beispiel erstellen Sie eine Konfiguration für das Beispielunternehmen, Litware, Inc. Diese Schritte können in jedem Unternehmen ausgeführt werden.

1. Wechseln Sie zu **Organisationsverwaltung  \>Arbeitsbereiche \>  Elektronische Berichterstellung**.
2. Überprüfen Sie, dass der Konfigurationsanbieter für Beispielunternehmen „Litware, Inc.” verfügbar und als **Aktiv** markiert ist. Wenn Sie diesen Konfigurationsanbieter nicht sehen, schließen Sie die Prozedur [Konfigurationsanbieter erstellen und als aktiv markieren](tasks/er-configuration-provider-mark-it-active-2016-11.md) ab. 
3. Wählen Sie **Metadatenkonfiguration** aus.
4. Wählen Sie **Konfiguration erstellen**.
5. Geben Sie im Drop-Down-Dialogfeld im Feld **Name** einen Namen ein. In vorliegenden Beispiel geben Sie **Außenhandelmetadaten** ein.
6. Wählen Sie **Konfiguration erstellen**.
7. Wählen Sie **Designer** aus.
8. Wählen Sie **Hinzufügen** aus.

    > [!NOTE]
    > Sie können alle Metadaten entweder für die gesamte Anwendung, oder für ausgewählte Modelle oder Module auswählen. Beachten Sie In beiden Fällen, dass die folgenden Metadaten automatisch hinzugefügt werden: Tabellen von Datensätzen, Aufzählungen und erweiterte Datentypen (EDTs). Wenn zusätzliche Arten von Metadaten erforderlich sind, müssen sie ggf. manuell hinzugefügt werden.

Sie müssen einige zum Außenhandel zugehörige Metadaten hinzufügen und manuell Metadatenelemente auswählen.

9. Wählen Sie **Datenquelle hinzufügen \> Tabellendatensätze** aus.
10. Filtern Sie auf Wert von **Intrastat** im Feld **Name**.
11. Wählen Sie den **Intrastat**-Tabellendatensatz aus.
12. Wählen Sie **OK**.

Sie müssen Metadateninformationen zur Intrastat-Datensatztabelle hinzufügen.

13. Wählen Sie in der Strukturdarstellung **Intrastat-Tabellendatensätze \> \>Beziehungen \> IntrastatCommodity (Tabellendatensätze EcoResCategory)** aus.
14. Wählen Sie **Metadaten hinzufügen** aus.

    > [!NOTE]
    > Metadaten über erforderliche Beziehungen für die ausgewählte Tabelle von Datensätzen müssen manuell hinzugefügt werden.

15. Wählen Sie **Datenquelle hinzufügen** aus:
16. Wählen Sie **Aufzählung** aus.
17. Filtern Sie auf Wert von **IntrastatDirection** im Feld **Name**.
18. Wählen Sie den Aufzählungsdatensatz **IntrastatDirections** aus.
19. Wählen Sie **OK**.
20. Wählen Sie **Speichern**.
21. Schließen Sie die Seite.
22. Schließt die Entwurfsversion der Metadatenkonfiguration ab:

    1. Wählen Sie **Status ändern \>Abschließen** aus.
    2. Wählen Sie **OK**.
    3. Wählen Sie die abgeschlossene Version 1.

23. Exportiert die abgeschlossene Version der Metadatenkonfiguration der Anwendung als eine XML-Datei:

    1. Wählen Sie **Austauschen \> Als XML-Datei exportieren** aus.
    2. Wählen Sie **OK**.

Die ER-Metadatenkonfiguration, die Sie erstellt haben, wird als **Metadata.xml für Außenhandel** gespeichert. Sie können es jetzt in RCS importieren, damit es als Metadatenquelle für die Außenhandelsgeschäftdomäne in Finance and Operations verwendet werden kann. Auf Basis dieser Informationen können Sie die Zuordnung zwischen Bewerbungsmetadaten und dem ER-Datenmodell angeben.

## <a name="access-application-metadata-by-using-an-er-configuration"></a>Zugriff auf Anwendungs-Metadaten über die ER-Konfiguration

Die folgende Prozedur veranschaulicht, wie ein RCS-Benutzer, mit der Rolle **Systemadministrator** oder **Elektronischer Berichterstellungs-Entwickler** ein neues ER-Modell entwerfen kann, indem er Metadaten aus der Finance and Operations-Anwendung verwendet. Auf Anwendungsmetadaten können zugegriffen werden, indem eine ER-Metadatenkonfiguration verwendet wird, die einen Beispielsatz der Metadaten enthält, um auf Außenhandelstransaktionen zuzugreifen.

Bevor Sie diese Prozedur abschließen können, müssen Sie zunächst die folgende Prozedur abschließen.

- [Konfigurationsanbieter erstellen und als aktiv markieren](tasks/er-configuration-provider-mark-it-active-2016-11.md)
- [Vorbereiten von Anwendungs-Metadaten zur Verwendung in RCS](#prepare-application-metadata-that-can-be-used-in-rcs)

1. Wechseln Sie zu **Alle Arbeitsbereiche \> Elektronische Berichterstellung**.
2. Überprüfen Sie, dass der Konfigurationsanbieter für Beispielunternehmen „Litware, Inc.” verfügbar und als **Aktiv** markiert ist. Wenn Sie diesen Konfigurationsanbieter nicht sehen, schließen Sie die Prozedur [Konfigurationsanbieter erstellen und als aktiv markieren](tasks/er-configuration-provider-mark-it-active-2016-11.md) ab. 
3. Importieren Sie die ER-Metadatumenkonfiguration, die Metadaten für die Finance and Operations-Anwendung enthält und die konfiguriert ist, um elektronische Dokumente für die Außenhandelsgeschäftsdomäne zu generieren. Sie haben in der Prozedur [Vorbereiten von Anwendungs-Metadaten zur Verwendung in RCS](#prepare-application-metadata-that-can-be-used-in-rcs) zuvor in diesem Thema diese ER-Metadatumenkonfiguration erstellt und als eine XML-Datei exportiert.

    1. Wählen Sie **Metadatenkonfiguration** aus.
    2. Wählen Sie **Wechselkurs** aus.
    3. Wählen Sie **Aus XML-Datei laden** aus.
    4. Durchsuchen, um die Datei **metadata.xml für Außenhandel** auszuwählen.
    5. Wählen Sie **OK**.
    6. Schließen Sie die Seite.

4. Eine Datenmodellkonfiguration erstellen:

    1. Wählen Sie **Berichterstellungskonfigurationen** aus.
    2. Wählen Sie **Konfiguration erstellen**.
    3. Geben Sie im Drop-Down-Dialogfeld im Feld **Name** **Außenhandelsmodell** ein.
    4. Wählen Sie **Konfiguration erstellen**.
    5. Wählen Sie **Designer** aus.
    6. Wählen Sie **Neu** aus, um das Ablagedialogfeld zu öffnen.

        1. Geben Sie im Feld **Name** **Stamm** ein.
        2. Wählen Sie **Hinzufügen** aus.
    
    7. Wählen Sie **Neu** aus, um das Ablagedialogfeld zu öffnen.

        1. Geben Sie im Feld **Name** **Transaktion** ein.
        2. Wählen Sie im Feld **Artikeltyp** **Datensatzliste** aus.
        3. Wählen Sie **Hinzufügen** aus.
 
    8. Wählen Sie **Neu** aus, um das Ablagedialogfeld zu öffnen.

        1. Geben Sie im Feld **Name** **Warencode**ein.
        2. Wählen Sie im Feld **Artikeltyp** **Zeichenfolge** aus.
        3. Wählen Sie **Hinzufügen** aus.

    9. Wählen Sie **Neu** aus, um das Ablagedialogfeld zu öffnen.

        1. Geben Sie im Feld „Name“ **Fakturierter Betrag** ein.
        2. Wählen Sie im Feld **Artikeltyp** **Gleitkommazahl** aus.
        3. Wählen Sie **Hinzufügen** aus.

    10. Wählen Sie **Neu** aus, um das Ablagedialogfeld zu öffnen.

        1. Geben Sie im Feld **Name** **Datum** ein.
        2. Wählen Sie im Feld **Artikeltyp** **Datum** aus.
        3. Wählen Sie **Hinzufügen** aus.
 
    11. Wählen Sie **Hinzufügen \> Stammreferenz** aus.
    12. Wählen Sie **OK**.
    13. Wählen Sie **Speichern**.
    14. Schließen Sie die Seite.
    15. Wählen Sie **Status ändern \>Abschließen** aus.
    16. Wählen Sie **OK**.

5. Erstellen einer Modellzuordnungskonfiguration:

    1. Wählen Sie **Konfiguration erstellen**.
    2. Geben Sie im Dropdown-Dialogfeld **Neu** **Modellzuordnung basierend auf Datenmodell-Außenhandelsmodell** ein.
    3. Geben Sie im Feld **Name** **Außenhandelsmodellzuordnung** ein.
    4. Wählen Sie **Konfiguration erstellen**.
    5. Wählen Sie auf dem Inforegister **Voraussetzungen** **Bearbeiten** aus.
    6. Wählen Sie **Neu** aus.
    7. Wählen Sie im Feld **Vorausgesetzter Komponententyp** **Konfiguration** aus.
    8. Wählen Sie die Konfiguration **Außenhandelsmetadaten** aus.
    9. Wählen Sie **Speichern**. Beachten Sie, dass der Verweis zur Version 1 der **Außenhandelsmetadaten**-Konfiguration hinzugefügt wird. Anwendungsmetadaten aus dieser Konfiguration werden angeboten, während die Modellzuordnung entworfen wird.
    10. Schließen Sie die Seite.
    11. Wählen Sie **Designer** aus.
    12. Wählen Sie **Designer** aus.
    13. Wählen Sie in der Struktur **Dynamics 365 for Operations \> Tabellendatensätze** aus.
    14. Wählen Sie **Stamm hinzufügen** aus.
    15. Geben Sie im Feld **Name** die Bezeichnung **Intrastat** ein.
    16. Wählen Sie die **Intrastat** Tabellendatensätze aus.
    17. Wählen Sie **OK**.

        > [!NOTE]
        > Es werden nur zwei Tabellen angeboten, da nur zwei Tabellen dem Satz der Metadaten hinzugefügt wurden, der gerade verwendet wird.

    18. Wählen Sie **Bindung** aus.
    19. In der Struktur wählen Sie **Intrastat \> AmountMST** aus.
    20. Wählen Sie in der Struktur **Transaktion = Intrastat \> Fakturierter Betrag** aus.
    21. Wählen Sie **Bindung** aus.
    22. In der Struktur wählen Sie **Intrastat \> TransDate** aus.
    23. In der Struktur wählen Sie **Transaktion = Intrastat \> Datum** aus.
    24. Wählen Sie **Bindung** aus.
    25. Wählen Sie in der Struktur **Intrastat \> \> Beziehungen \> IntrastatCommodity \> Code** aus.
    26. Wählen Sie in der Struktur **Transaktion = Intrastat \> Warencode** aus.
    27. Wählen Sie **Bindung** aus.
    28. Wählen Sie **Überprüfen** aus.

        > [!NOTE]
        > Nach Abschluss der Validierung haben Sie die Elemente des Datenmodells erfolgreich an die Datenquellenelemente gebunden, die mit Details aus den Anwendungsmetadaten aus der referenzierten ER-Metadatenkonfiguration beschrieben werden.

    29. Wählen Sie **Speichern**.

Nach Bedarf können Sie den vorhandenen Satz von Metadaten in Finance and Operations erweitern. Sie können anschließend die neue abgeschlossene Version der ER-Metadatenkonfiguration aus Finance and Operations exportieren, sie in RCS importieren und die Voraussetzungen der konfigurierten Zuordnungsmodellkonfiguration aktualisieren und auf eine neue Version der importierten Metadatenkonfiguration verweisen.

> [!NOTE]
> Diese Methode des Informationsabrufs von Informationen zu Anwendungsmetadaten ist die einzige Methode für Anwendungen, die lokal bereitgestellt werden (d. h., wenn lokale Geschäftsdaten \[LBD\] oder ein lokales Bereitstellungsmodell für Finance and Operations verwendet werden).

## <a name="access-application-metadata-by-using-connected-applications"></a>Zugriff auf Anwendungs-Metadaten über verbundene Anwendungen

Die folgende Prozedur veranschaulicht, wie ein RCS-Benutzer, mit der Rolle **Systemadministrator** oder **Elektronischer Berichterstellungs-Entwickler** ein neues ER-Modell entwerfen kann, indem er Metadaten von der Finance and Operations-Anwendung verwendet. Zugriff auf Anwendungs-Metadaten erfolgt online über RCS verbundene Anwendungen. Eine Beispiel-ER-Modellzuordnung wird konfiguriert, um auf Außenhandelstransaktionen zuzugreifen.

Um diese Prozedur auszuführen, müssen Sie zunächst die Prozedur [Konfigurationsanbieter erstellen und als aktiv markieren](tasks/er-configuration-provider-mark-it-active-2016-11.md) in RCS abschließen. Wenn Sie die Prozedur [Zugriff auf Anwendungs-Metadaten über die ER-Konfiguration](#access-application-metadata-by-using-an-er-configuration) zuvor in diesem Thema noch nicht abgeschlossen haben, navigieren Sie zur Seite [Aufgabenleitfaden für elektronische Berichterstellung für Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739), um die folgenden ER-Konfigurationsdateien im Voraus herunterzuladen und lokal zu speichern: **Metadata.xml für Außenhandel**, **Model.xml für Außenhandel** und **Mapping.xml für Außenhandel**.


### <a name="get-required-er-configurations"></a>Erforderliche ER-Konfigurationen abrufen

Wenn Sie die Schritte in der Prozedur [Zugriff auf Anwendungs-Metadaten über eine ER-Konfiguration](#access-application-metadata-by-using-an-er-configuration) zuvor in diesem Thema bereits abgeschlossen haben, haben Sie bereits alle erforderlichen ER-Konfigurationen (Außenhandelsmetadaten, Modell- und Zuordnungskonfigurationen) in der aktuellen RCS-Instanz. In diesem Fall können Sie diese Prozedur überspringen.

1. Wechseln Sie zu **Alle Arbeitsbereiche \> Elektronische Berichterstellung**.
2. Wählen Sie **Berichterstellungskonfigurationen** aus.
3. Laden Sie die Konfigurationsdateien **metadata.xml für Außenhandel**, **model.xml für Außenhandel** und **mapping.xml für Außenhandel** und wiederholen Sie die folgende Schrittfolge für jede einzelne davon:

    1. Wählen Sie **Wechselkurs** aus.
    2. Wählen Sie **Aus XML-Datei laden** aus.
    3. Wählen Sie **Duchsuchen** und eine Datei aus.
    4. Wählen Sie **OK**.

### <a name="register-the-connection-with-finance-and-operations"></a>Registrieren der Verbindung mit Finance and Operations

1. Wechseln Sie zu **Alle Arbeitsbereiche \> Elektronische Berichterstellung**.
2. Wählen Sie **Verbundene Anwendung** aus.
3. Überprüfen Sie, ob die konfigurierte Anwendung auf Microsoft Azure basiert und dass RCS-Benutzer im Allgemeinen darauf zugreifen können. Der aktuelle RCS-Benutzer muss Zugriff auf die konfigurierte Anwendung haben und als Benutzer dieser Anwendung in einer Rolle registriert sein, die ihm oder ihr die Rechte für den Zugriff auf die die Metadaten der Anwendung gibt.
4. Wählen Sie **Neu** aus.
5. Wählen Sie im Feld **Name** **MyConnectedApp** als den Namen der verbundenen Anwendung ein.
6. Geben Sie im Feld **Anwendung** die URL der Anwendung an.
7. Geben Sie im Feld **Mandant** den Anbieter der Anwendung an.
8. Wählen Sie **Speichern**. 
9. Wenn Sie die Verbindung zur der konfigurierten Anwendung überprüfen, wählen Sie auf der Seite **Mit Remote-Anwendung verbinden** den Link **Hier klicken, um Verbindung mit der ausgewählten Remote-Anwendung herzustellen** aus. 
10. Wählen Sie **Verbindung überprüfen** aus, um den Zugriff auf den konfigurierte Anwendung zu überprüfen.
11. Wählen Sie **Schließen** aus.

Nach Abschluss dieser Prozedur und nach Validierung des Verbindungserfolgs, werden die Versions- und Mandantendetails für die konfigurierte Anwendung im aktuellen Raster aktualisiert.

### <a name="review-the-existing-model-mapping-configuration"></a>Überprüfen der vorhandenen Modellzuordnungskonfiguration

1. Wechseln Sie zu **Alle Arbeitsbereiche \> Elektronische Berichterstellung**.
2. Wählen Sie **Berichterstellungskonfigurationen** aus.
3. Wählen Sie in der Struktur **Außenhandelsmodell \> Außenhandelszuordnung** aus.
4. Wählen Sie auf dem Inforegister **Voraussetzungen** aus.

    > [!NOTE]
    > Diese Zuordnung bezieht sich derzeit auf die Metadatenkonfiguration. Anwendungsmetadaten aus dieser Konfiguration werden angeboten, während diese Modellzuordnung entworfen wird.

4. Wählen Sie **Designer** aus.
5. Wählen Sie **Designer** aus.
6. Wählen Sie in der Struktur **Dynamics 365 for Operations \> Tabellendatensätze** aus.
7. Wählen Sie **Stamm hinzufügen** aus.
8. Geben Sie im Feld **Tabelle** einen Wert ein, oder wählen Sie einen Wert aus.

    > [!NOTE]
    > Diese Zuordnung bezieht sich derzeit auf die Metadatenkonfiguration. Anwendungsmetadaten aus dieser Konfiguration werden angeboten, während diese Modellzuordnung entworfen wird.

9. Wählen Sie **Abbrechen** aus.

### <a name="assign-the-connected-application-to-a-model-mapping"></a>Weisen Sie die verbundene Anwendung einer Modellzuordnung zu

1. Wählen Sie **Bearbeiten** aus.
2. Wählen Sie im Feld **Verbundene Anwendung** die Anwendung **MyConnectedApp** aus.

    > [!NOTE]
    > Diese Zuordnung bezieht sich auf die Metadaten der ausgewählten verbundenen Anwendung. Wenn sich eine Zuordnung gleichzeitig auf die Metadatenkonfiguration sowie die verbundene Anwendung bezieht, werden die Metadaten der verbundenen Anwendung verwendet.

3. Wählen Sie **Designer** aus.
4. Wählen Sie **Designer** aus.
5. Wählen Sie in der Struktur **Dynamics 365 for Operations \> Tabellendatensätze** aus.
6. Wählen Sie **Stamm hinzufügen** aus.
7. Geben Sie im Feld **Tabelle** einen Wert ein, oder wählen Sie einen Wert aus.

    > [!NOTE]
    > An diesem Punkt werden mehr als zwei Anwendungstabellen angeboten, da diese Zuordnung alle Metadaten der verbundenen Anwendung verwenden, die ihr zugeordnet sind.

8. Wählen Sie **Abbrechen** aus.
9. Wählen Sie **Überprüfen** aus.

Sie haben nun erfolgreich Elemente des Datenmodells an die Elemente der Datenquellen gebunden, die Details der Metadaten der verbundenen Anwendung verwendet, die dieser Zuordnung zugewiesen wurde.

Wenn Sie diese Modellzuordnung überprüfen müssen, indem Sie die Metadaten einer anderen Version der Anwendung verwenden, registrieren Sie eine andere verbundene Anwendung, weisen Sie sie dieser Modellzuordnung zu und prüfen Sie sie anhand der neuen Metadaten.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

Alternativ können Sie den Aufgabenleitfaden **Anwendungsmetadaten vorbereiten, die in RCS verwendet werden können** in Finance and Operations sowie die Aufgabenleitfäden **Zugriff auf Anwendungsmetadaten über eine ER-Konfiguration** und **Zugriff auf Anwendungsmetadaten mithilfe verbundener Bewerbungen** in RCS wiedergeben. Diese Aufgabenleitfäden können von der Seite [Aufgabenleitfäden für elektronische Berichterstellung für Dynamics 365 for Finance and Operations 8,1](https://go.microsoft.com/fwlink/?linkid=2082739) heruntergeladen werden.
