---
title: Zugriff auf Anwendungs-Metadaten über die ER-Konfiguration
description: In diesem Thema wird erläutert, wie ein Regulatory Configuration Service-Benutzer eine neue Modellzuordnung für elektronische Berichterstellung (EB) entwerfen kann, indem er die Metadaten verwendet.
author: NickSelin
manager: AnnBe
ms.date: 06/28/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 58697148ecf83f4962bd64a221945b6d911e11a6
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093304"
---
# <a name="access-application-metadata-by-using-er-configuration"></a>Zugriff auf Anwendungs-Metadaten über die ER-Konfiguration

[!include [banner](../../includes/banner.md)]

In den folgenden Schritten wird erläutert, wie ein Regulatory Configuration Service (RCS)-Benutzer mit der Systemadministratorrolle oder der Rolle „Entwickler für elektronische Berichterstellung“ eine neue Modellzuordnung für „Elektronische Berichterstellung (ER)“ entwerfen kann, indem er die Metadaten der Anwendung verwendet. Auf Anwendungsmetadaten können zugegriffen werden, indem eine ER-Metadatenkonfiguration verwendet wird, die einen Beispielsatz der Metadaten enthält, um auf Außenhandelstransaktionen zuzugreifen. Um diese Schritte auszuführen, müssen Sie zunächst in RCS die Schritte in der Prozedur [Konfigurationsanbieter erstellen und als aktiv markieren](er-configuration-provider-mark-it-active-2016-11.md) abschließen. Schließen Sie dann die Schritte im Thema [Anwendungsmetadaten zur Verwendung in RCS vorbereiten](prepare-application-metadata-rcs.md) ab.

## <a name="prerequisites"></a>Voraussetzungen
1. Wechseln Sie zu **Alle Arbeitsbereiche** > **Elektronische Berichterstellung**. 
2. Überprüfen Sie, dass der Konfigurationsanbieter für Beispielunternehmen „Litware, Inc.” verfügbar und als **Aktiv** markiert ist. Wenn Sie diesen Konfigurationsanbieter nicht sehen, müssen Sie zunächst die Schritte in der Prozedur [Konfigurationsanbieter erstellen und diesen als aktiv markieren](er-configuration-provider-mark-it-active-2016-11.md) abschließen. 

## <a name="import-metadata-configuration"></a>Importieren der Metadatenkonfiguration 
1. Klicken Sie auf **Metadatenkonfiguration**. 
2. Importieren Sie die ER-Metadatumenkonfiguration, die Metadaten enthält und die konfiguriert wurde, um elektronische Dokumente für das Außenhandelsgeschäft zu generieren. Diese ER-Metadatumenkonfiguration wurde als XML-Datei exportiert, während die Schritte in der Prozedur [Anwendungsmetadaten vorbereiten, die in RCS verwendet werden](prepare-application-metadata-rcs.md) ausgeführt wurden. 
3. Klicken Sie auf **Austauschen**. 
4. Klicken Sie auf **Aus XML-Datei laden**. 
5. Klicken Sie **Durchsuchen** und wählen die Datei metadata.xml für Außenhandel aus. 
6. Klicken Sie auf **OK**. 
7. Schließen Sie die Seite. 

## <a name="create-data-model-configuration"></a>Datenmodellkonfiguration erstellen
1. Klicken Sie auf **Berichterstellungskonfigurationen**. 
2. Klicken Sie auf **Konfiguration erstellen** um das Dropdown-Dialogfeld zu öffnen. 
3. Geben Sie im Feld **Name** „Außenhandelsmodell“ ein. 
4. Klicken Sie auf **Konfiguration erstellen**. 
5. Klicken Sie auf **Designer**. 
6. Klicken Sie auf **Neu** zum Öffnen des Ablagedialogfeld. 
7. Geben Sie im Feld **Name** Stamm ein. 
8. Klicken Sie auf **Hinzufügen**. 
9. Klicken Sie auf **Neu** zum Öffnen des Ablagedialogfeld. 
10.    Geben Sie im Feld **Name** „Transaktion“ ein. 
11.    Wählen Sie im Feld **Artikeltyp** **Datensatzliste** aus. 
12.    Klicken Sie auf **Hinzufügen**. 
13.    Klicken Sie auf **Neu** zum Öffnen des Ablagedialogfeld. 
14.    Geben Sie im Feld **Name** „Warencode“ ein. 
15.    Wählen Sie im Feld **Artikeltyp** **Zeichenfolge** aus. 
16.    Klicken Sie auf **Hinzufügen**. 
17.    Klicken Sie auf **Neu** zum Öffnen des Ablagedialogfeld. 
18.    Geben Sie im Feld **Name** „Fakturierter Betrag“ ein. 
19.    Wählen Sie im Feld **Artikeltyp** **Gleitkommazahl** aus. 
20.    Klicken Sie auf **Hinzufügen**. 
21.    Klicken Sie auf **Neu** zum Öffnen des Ablagedialogfeld. 
22.    Geben Sie im Feld **Name** „Datum“ ein. 
23.    Wählen Sie im Feld **Artikeltyp** **Datum** aus. 
24.    Klicken Sie auf **Hinzufügen**. 
25.    Klicken Sie auf **Stammreferenz**. 
26.    Klicken Sie auf **OK**. 
27.    Klicken Sie auf **Speichern**. 
28.    Schließen Sie die Seite. 
29.    Klicken Sie auf **Status ändern**. 
30.    Klicken Sie auf **Abgeschlossen**. 
31.    Klicken Sie auf **OK**. 

## <a name="create-model-mapping-configuration"></a>Erstellen der Modellzuordnungskonfiguration 
1. Klicken Sie auf **Konfiguration erstellen** um das Dropdown-Dialogfeld zu öffnen. 
2. Geben Sie im Feld **Neu** 'Modellzuordnung basierend auf Datenmodell-Außenhandelsmodell' ein. 
3. Geben Sie im Feld **Name** „Außenhandelsmodellzuordnung“ ein. 
4. Klicken Sie auf **Konfiguration erstellen**. 
5. Erweitern Sie den Abschnitt **Voraussetzungen**. 
6. Klicken Sie auf **Bearbeiten**. 
7. Klicken Sie auf **Neu**. 
8. Markieren Sie in der Liste die ausgewählte Zeile. 
9. Wählen Sie im Feld **Vorausgesetzter Komponententyp** **Konfiguration** aus. 
10.    Wählen Sie die Konfiguration **Außenhandelsmetadaten** aus. 
11.    Klicken Sie auf **Speichern**. 
12.    Wir haben die Referenz der Version 1 der Außenhandelsmetadaten-Konfiguration hinzugefügt. Anwendungsmetadaten aus dieser Konfiguration werden angeboten, während diese Modellzuordnung entworfen wird. 
13.    Schließen Sie die Seite. 
14.    Klicken Sie auf **Designer**. 
15.    Klicken Sie auf **Designer**. 
16.    Wählen Sie in der Struktur **Dynamics 365 for Operations\Tabellendatensätze** aus. 
17.    Klicken Sie auf **Stamm hinzufügen**. 
18.    Geben Sie im Feld **Name** „Intrastat“ ein. 
19.    Wählen Sie die **Intrastat** Tabellendatensätze aus. 
20.    Klicken Sie auf **OK**. 

> [!NOTE]
> Die einzigen 2 Tabellen wurden angeboten, als die einzigen 2 Tabellen dem Satz der Metadaten hinzugefügt wurden, die gerade verwendet werden. 

21.    Klicken Sie auf **Binden**. 
22.    Erweitern Sie in der Struktur **Intrastat**. 
23.    In der Struktur wählen Sie **Intrastat\AmountMST** aus. 
24.    Erweitern Sie in der Struktur **Transaction = Intrastat**. 
25.    Wählen Sie in der Struktur **Transaction = Intrastat\Fakturierter Betrag** aus. 
26.    Klicken Sie auf **Binden**. 
27.    In der Struktur wählen Sie **Intrastat\TransDate** aus. 
28.    In der Struktur wählen Sie **Transaction = Intrastat\Datum** aus. 
29.    Klicken Sie auf **Binden**. 
30.    Erweitern Sie in der Struktur **Intrastat\>Beziehungen**. 
31.    Erweitern Sie in der Struktur **Intrastat\>Beziehungen\IntrastatCommodity**. 
32.    Wählen Sie in der Struktur **Intrastat\>Beziehungen\IntrastatCommodity\Code**. 
33.    Wählen Sie in der Struktur **Transaction = Intrastat\Warencode** aus. 
34.    Klicken Sie auf **Binden**. 
35.    Klicken Sie auf **Überprüfen**. 

> [!NOTE]
> Es wurden erfolgreich Elemente des Datenmodells mit Datenquellenelementen gebunden, die mit Details aus Bewerbungsmetadaten aus der referenzierten ER-Metadatenkonfiguration beschrieben werden. 
36.    Klicken Sie auf **Speichern**. 
37.    Schließen Sie die Seite. 
38.    Schließen Sie die Seite. 
39.    Bei Bedarf können Sie die vorhandene Gruppe von Metadaten erweitern und dann die abgeschlossene neue Version der ER-Metadatumenkonfiguration exportieren. Sie können sie dann in RCS importieren und die Voraussetzungen der Zuordnungskonfiguration des Modells aktualisieren, die sich auf eine neue Version der importierten Metadatumenkonfiguration beziehen. 

> [!NOTE]
> Diese Art des Informationsabrufs von Informationen zu Anwendungsmetadaten ist als einzige für lokal bereitgestellte Anwendungen verfügbar (wenn lokale Geschäftsdaten (LBD) oder ein lokales Bereitstellungsmodell verwendet werden).
        


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]