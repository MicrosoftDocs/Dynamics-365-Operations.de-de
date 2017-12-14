---
title: Demodaten-Bildschirmlayouts in MPOS/CPOS
description: "Dieses Thema enthält Informationen zu den Bildschirmlayouts, die in den Demodaten einbezogen sind, die für die Verkaufsstelle (POS)-Erfahrungen in Microsoft Dynamics 365 for Retail festgelegt werden."
author: zlinster
manager: AnnBe
ms.date: 10/05/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application user
ms.search.scope: Operations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Retail
ms.author: zlinster
ms.search.validFrom: 2017-10-05
ms.dyn365.ops.version: Retail April 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 563c89c75e2136294f8f841bec094c2aeb85d580
ms.openlocfilehash: b758b48230e8d9fabdccbe267a6ad6b9e74af0ff
ms.contentlocale: de-de
ms.lasthandoff: 10/17/2017

---

# <a name="demo-data-screen-layouts-in-mposcpos"></a>Demodaten-Bildschirmlayouts in MPOS/CPOS

Dieses Thema enthält Informationen zu den Bildschirmlayouts, die in den Demodaten einbezogen sind, die für die Verkaufsstelle (POS)-Erfahrungen in Microsoft Dynamics 365 for Retail festgelegt werden.

## <a name="overview"></a>Überblick

Die Beispielbildschirmlayouts, die mit Kleindemodaten einbezogen werden, enthalten Inhalt, der für verschiedene Retail-Segmente, Shoparbeitskraftrollen und Geräte optimiert ist. Ein einzelnes Layout kann mehrere Layoutgrößen und Schaltflächenrastern oder Kombinationen von enthalten, um sicherzustellen, dass Shoparbeitskräfte zwischen Stationen und Geräten wechseln. In diesem Thema werden die Unterschiede zwischen diesen Layouts, den Arbeitsgängen, die sie bieten, und den Gesamterfahrungen hervorgehoben, die sie beinhalten.

![Geräteübergreifende Demo-Datenlayouts](../retail/media/demo-screen-layouts-fig-1-1.png)

## <a name="anatomy-of-a-screen-layout-id"></a>Struktur einer Bildschirmlayout-ID

Um Bildschirmlayouts in Retail zu suchen, gehen Sie zu **Retail** > **Kanaleinstellung** > **POS-Einstellung** > **POS** > **Bildschirmlayouts**.

![Bildschirmlayoutseite in Retail](../retail/media/demo-screen-layouts-fig-2-1.png)

Bildschirmlayout-IDs können maximal 10 Zeichen haben. Die Kennung ist eine Zeichenfolge, die aus drei Informationen besteht, in dieser Reihenfolge:

1. Unternehmen
2. Layoutversion
3. Person

### <a name="company"></a>Unternehmen

| Buchstabe | Unternehmen         |
|--------|-----------------|
| H      | Adventure Works |
| F      | Fabrikam        |
| k      | Contoso         |

### <a name="layout-version"></a>Layoutversion

| Versionsnummer | Beschreibung                                                                                |
|----------------|--------------------------------------------------------------------------------------------|
| 3              | Die Basisversion, die mehrere Bildschirmgrößen für verschiedene Geräte und Seitenverhältnisse unterstützt |
| 3.1            | Die Basisversion, die zusätzlichen Support für den Bereich **Empfohlene Produkte** hat        |

### <a name="persona"></a>Person

| Abkürzung | Person       | Inhalt |
|--------------|---------------|----------|
| CSH          | Kassierer       | Kassiererlayouts enthalten alle buchungsrelevanten Arbeitsgänge, wie Debitorenaufträge, Rücklieferungen, Rabatte Lücken, Geschenkkarten. Diese Layouts enthalten außerdem tägliche Aufgaben für die Ausführung von Lagerverwaltung, Preisüberprüfungen, Bestandssuchen und Bestandszählungen. Grundlegende Schichtverwaltung wird auch für Anfangsbeträge, Aussetzen von Schichten und Vorgänge und Stempeluhr bereitgestellt. |
| MGR          | Shopleiter | Shopleiterlayouts enthalten alle buchungsrelevanten Arbeitsgänge, die in den Kassiererlayouts gefunden werden, auch Steueraußerkraftsetzungen wird bereitgestellt. Diese Layouts enthalten außerdem tägliche Aufgaben für die Ausführung von Lagerverwaltung, Preisüberprüfungen, Bestandssuchen und Bestandszählungen. Schichtverwaltung wird für das Starten, das Unterbrechen und Abschließen von Arbeitsschichten bereitgestellt. Darüber hinaus enthalten die Kassenladearbeitsgänge Layouts für Einträge, Entfernen, Kassenstürze und Safe- und Bankeinzahlungen. Schließlich enthalten diese Layouts den Zugriff auf die Performance-Berichte und aktivieren der zu druckenden X und Z-Berichte. |
| STK          | Lagerangestellter   | Lagerverwalterlayouts sind für Lagerverwaltung optimiert. Sie enthalten Zugriff auf die Tagewerke für Preisüberprüfungen, Bestandssuchen, Entnahme und Empfang Bestandszählungen, und Kit-Disassembly. Diese Layouts enthalten auch grundlegende Schichtvorgänge für Stempeluhr und Unterbrechen von Schichten. Diese Layouts sind für Backofficeaufgaben vorgesehen, Lagerangestellte besitzen die gleichen wie Arbeitsgänge für Kassierer Buchungsbildschirme. |

### <a name="example-layout"></a>Beispielslayout

Das folgende Beispiel einer Bildschirmlayout-Kennung und Verlustrechnung für die Layoutversion, 3 und die Shopleiterperson:

F3MGR

In der folgenden Abbildung wird ein Beispiel des Begrüßungsbildschirms für einen Fabrikam-Shopleiter angezeigt.

![Begrüßungsbildschirm für den Fabrikam-Shopleiter](../retail/media/demo-screen-layouts-fig-2-2.png)

## <a name="layout-sizes"></a>Layoutgrößen

### <a name="full-vs-compact-layouts"></a>Volle vs. kompakte Layouts

Ein Bildschirmlayout kann die Konfigurationen von Komplett- und Kompaktgeräten angeben. Diese Konfiguration ermöglicht ein einzelnes Bildschirmlayout zu einem Benutzer zuzuordnen, der mit verschiedene Größen und Formularfaktoren im Shop arbeitet.

- **Modern POS - Vollständig** - Vollständige Layouts werden verwendet für große PC-Bildschirme oder Tablets. Benutzer können die Benutzeroberflächenelemente auswählen, die das Layout umfasst, angeben der Größe und der Position dieser Elemente und konfigurieren ihrer detaillierte Eigenschaften. Vollständige Layouts unterstützen Hochformat- und Querformatkonfigurationen.
- **Modern POS - Kompakt** - Kompakte Layouts werden verwendet für kleine Telefone oder Tablets. Designmöglichkeiten werden für kompakte Geräte beschränkt. Benutzer können die Spalten und Felder für den Zugriff und summenbereiche konfigurieren.

### <a name="screen-resolutions-that-are-provided"></a>Bildschirmauflösungen, die bereitgestellt werden

In der folgenden Tabelle werden die Layoutgrößen angezeigt, die aus für typische bereitgestellt werden.

| Layouttyp | Auflösung | Ansichtverhältnis | Zielanzeige          |
|-------------|------------|--------------|-------------------------|
| Kompaktieren\*   | 480 × 853  | 16:9         | Telefone                  |
| Voll        | 1024 × 768 | 4:3          | Tablets                 |
| Voll\*      | 1280 × 720 | 16:9         | Tablets                 |
| Voll        | 1366 × 768 | 16:9         | Tablets, größere Bildschirme |
| Voll        | 1440 × 960 | 3:2          | Tablets, größere Bildschirme |

\* Diese zusätzliche Layoutgrößen sind nur in Adventure Works- und Fabrikam-Layouts verfügbar.


>[!TIP]
> POS wählt automatisch Layoutgrößen, basierend auf der nächsten Größe, für die die Bildschirmauflösung des aktuellen App-Fensters verfügbar ist. Um die Bildschirmlayout-ID- und -Layoutlösung, die derzeit verwendet werden, in Retail Modern POS (MPOS) oder Retail Cloud POS (CPOS) zu finden, öffnen Sie die Seite **Einstellungen** im Abschnitt **Sitzungsinformationen**. Sie können die aktuelle Fensterauflösung für die aktuelle Anwendung oder Browserrahmen finden. Nachdem Sie diese Informationen enthalten haben, können Sie die Quelle des Layoutinhalts in Retail finden, indem Sie zu **Kanaleinstellung** > **POS-Einstellung** > **POS** > **Bildschirmlayouts** gehen.


![Bildschirmlayouts und Layoutlösungen/Größen in Retail und POS](../retail/media/demo-screen-layouts-fig-3-1.png)

## <a name="companies-and-brands"></a>Unternehmen und Marken

Jedes fiktive Unternehmen zielt auf eine andere Retail-Zielgruppe und enthält Produktkataloge, die für den Betrieb des Unternehmens optimiert werden. Jedes Unternehmen verfügt über eine eindeutige Sichtmarke, die den Produkte beigelegt werden soll. Brandingelemente enthalten die Akzentfarbe, das dunkle oder helle Thema und begleitende Fotografien, die realistische Erfahrungen enthalten.

### <a name="company-segment-and-visual-characteristics"></a>Unternehmenssegment und Sichtmerkmale

| Unternehmen         | Ziel | Segment        | Akzent | Thema |
|-----------------|----------|----------------|--------|-------|
| Adventure Works | Seattle  | Sport-Waren | Blau   | Dunkel  |
| Fabrikam        | Houston  | Mode        | Green  | Hell |
| Contoso         | Boston   | Elektrogeräte    | Red    | Dunkel  |


>[!NOTE]
> Adventure Works und Fabrikam sind die beiden Flaggschiffmarken. Contoso ist verfügbar, aber nicht alle Layouts sind bereitgestellt worden.


Die folgenden Abbildungen zeigen Beispiele der Willkommensseite und Buchungsseite für die drei erfundenen Unternehmen.

### <a name="adventure-works"></a>Adventure Works

![Demodatwillkommensseite für Adventure Works](../retail/media/demo-screen-layouts-fig-4-1a.png)

![Demodatenbuchungsseite für Adventure Works](../retail/media/demo-screen-layouts-fig-4-1b.png)

### <a name="fabrikam"></a>Fabrikam

![Demodaten-Willkommensseite für Fabrikam](../retail/media/demo-screen-layouts-fig-4-2a.png)

![Demodatenbuchung-Willkommensseite für Fabrikam](../retail/media/demo-screen-layouts-fig-4-2b.png)

### <a name="contoso"></a>Contoso

![Demodatlayouts für Contoso](../retail/media/demo-screen-layouts-fig-4-3.png)

## <a name="user-sign-in-matrix"></a>Benutzeranmeldung in Matrix

Benutzer wurden für die verschiedenen Bildschirmlayouts bereitgestellt. Mit der folgenden Tabelle sollte es möglich sein, auf jeden Bildschirm zuzugreifen. Melden Sie einfach an, indem Sie eine entsprechende Operator-ID verwenden.

| Unternehmen         | Bildschirmlayoutkennung | Person          | Bedienerkennungen           |
|-----------------|------------------|---------------   |------------------------|
| Adventure Works | A3MGR            | Shopleiter    | 000154, 000137, 000073 |
| Adventure Works | A3CSH            | Kassierer          | 000150, 000175, 000165 |
| Adventure Works | A3STK            | Lagerangestellter      | 000155, 000181, 000152 |
| Fabrikam        | F3MGR            | Shopleiter    | 000160, 000168, 000163 |
| Fabrikam        | F3CSH            | Kassierer          | 000161, 000113, 000114 |
| Fabrikam        | F3STK            | Lagerangestellter      | 000164, 000112, 000123 |
| Contoso         | C3MGR            | Shopleiter    | 000100, 000111         |
| Contoso         | C3CSH            | Kassierer          | 000110, 000120         |
| Contoso         | Nicht zutreffend   | Lagerangestellter      | Nicht zutreffend         |


>[!TIP]
> Für beste Ergebnisse aktivieren Sie ein Register im entsprechenden Filialstandort, und legen Sie das Unternehmen auf das Unternehmen der Persona fest, die Sie planen, zu verwenden ist, wenn Sie sich anmelden. Auf diese Weise können Sie sicherzustellen, dass Bilder des visuellen Profils und des Brandings über die Erfahrung hinweg angepasst werden. Wenn Sie z. B. interessiert sind,ein Fabrikam-Layout für einen Kassierer zu finden, sollten Sie ein Register im Houston-Shop aktivieren.


<!-- Hiding until the content page is available on CustomerSource -->

<!-- ## Reference icons and images -->

<!-- The screen layouts, button grids, and visual profiles were created using images and icons that can be found in **Retail > Channel setup > POS setup > POS > Images**. -->

<!-- ![Images in Dynamics 365 for Retail](../retail/media/demo-screen-layouts-fig-5-1.png) -->

<!-- Use the [POS Icon and Image Mapping](../retail/media/POS_Icon_and_Image_Mapping.xlsx) reference spreadsheet to locate operation icons, reference photos, swap logos, or provide new images of your own that can be referenced in custom designs. -->

<!-- END HIDDEN CONTENT -->
