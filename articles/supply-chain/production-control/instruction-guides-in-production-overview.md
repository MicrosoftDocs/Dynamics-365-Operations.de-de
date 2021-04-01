---
title: Bereitstellung von Anleitungen mit gemischter Realität für Arbeiter in der Produktion
description: In diesem Thema wird erläutert, wie Sie das Produktionsverwaltungsmodul in Microsoft Dynamics 365 Supply Chain Management mit Dynamics 365 Guides integrieren.
author: cabeln
manager: tfehr
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkGuidesManufacturing
audience: Application User
ms.reviewer: kamaybac
ms.custom: 61943
ms.assetid: a3847f07-fca4-4140-a26f-d83c6ac68dde
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: cabeln
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.15
ms.openlocfilehash: 48e0dfeba1a9744c90608d4d9009484df91c4b85
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5246140"
---
# <a name="provide-mixed-reality-guides-for-workers-in-production"></a>Bereitstellung von Anleitungen mit gemischter Realität für Arbeiter in der Produktion

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Mitarbeiter in Produktionsprozessen profitieren von relevanten Anweisungen, die zum richtigen Zeitpunkt im Rahmen ihrer Arbeit bereitgestellt werden. *Anleitungen* gelten in verschiedenen Arbeitsbereichen, einschließlich: Montage, Service, Betrieb, Zertifizierung und Sicherheit. In all diesen Kerngeschäftsfunktionen können fortlaufende Schulungsanweisungen dazu beitragen, dass die Mitarbeiter mehr erreichen und besser arbeiten können.

## <a name="introduction"></a>Einführung

Sie können Anweisungen auf verschiedene Arten bereitstellen. Ein effizientes System, das Standardverwendungen liefert [Dynamics 365 Guides](https://dynamics.microsoft.com/mixed-reality/guides/).

Dynamics 365 Guides kann helfen, Ihre Mitarbeiter durch praktisches Lernen zu befähigen. Sie können standardisierte Prozesse mit schrittweisen Anweisungen definieren, die Ihre Mitarbeiter zu den benötigten Werkzeugen und Teilen führen und den Mitarbeitern zeigen, wie sie diese Werkzeuge in realen Arbeitssituationen einsetzen können.

Sie können Anleitungen zu verschiedenen Aspekten der Produktionssteuerung anhängen, darunter:

- [Ressourcen](#resources)
- [Ressourcengruppen ](#resource-groups)
- [Freigegebene Produkte](#released-products)
- [Formeln](#formulas)
- [Formelversionen](#formula-versions)
- [Stücklisten](#bom)
- [Stücklistenversionen](#bom-versions)
- [Arbeitspläne](#routes)
- [Arbeitsplanversionen](#route-versions)
- [Arbeitsplanbetriebsbeziehungen](#route-operation-relations)

> [!NOTE]
> Sie können Guides auch an Anlagenverwaltung anhängen. Weitere Informationen zu dieser Option finden Sie unter [Dynamics 365 Supply Chain Management-(Anlagenverwaltung) mit Dynamics 365 Guides](../asset-management/asset-management-guides-integration.md) integrieren.

Wenn ein Mitarbeiter erster Linie über Supply Chain Management einen Job in der Werkstatt auswählt, kann der Mitarbeiter [die entsprechenden Anleitungen](#logic) auf der Einzelvorgangskarte sehen. Wenn der Mitarbeiter eine bestimmte Anleitung auswählt, wird auf dem Bildschirm ein QR-Code für diese Anleitung angezeigt. Der Arbeiter benutzt dann ihre HoloLens, um den QR-Code zu scannen, der Guides startet und die erforderlichen Anweisungen anzeigt.

In den folgenden Unterabschnitten werden einige ausgewählte Szenarien beschrieben, in denen Unternehmen in verschiedenen Branchen den größten Wert sehen können, wenn sie mithilfe von Guides Anweisungen für die Herstellung präsentieren.

### <a name="assembly"></a>Assembly

![Verwenden Sie Guides für Montageaufgaben](media/instruction-guides-hero-assembly.png "Verwenden Sie Guides für Dienstleistungsaufgaben")

Anweisungen für Montagevorgänge zeigen den Mitarbeitern die Werkzeuge und Teile, die sie benötigen, und wie sie in realen Arbeitssituationen eingesetzt werden können.

Produktionsleiter können Guides erstellen und zuweisen, zum Beispiel für [Produktionswege](routes-operations.md), [Vorgangsbeziehungen](routes-operations.md#operation-relations) oder [Stückliste](bill-of-material-bom.md). Die entsprechenden Anweisungen zur jeweiligen Vorgangserfahrung finden die Mitarbeiter in der Werkstatt.

### <a name="service"></a>Dienstleistung

![Verwenden Sie Guides für Dienstleistungsaufgaben](media/instruction-guides-hero-service.png "Verwenden Sie Guides für Dienstleistungsaufgaben")

Rüsten Sie die Techniker auf der Baustelle mit geführten Anweisungen aus, sodass keine zusätzlichen Besuche geplant werden müssen.

Serviceleiter können Guides beispielsweise bestimmten [Produkten](../../commerce/product.md) zuweisen, die durch Routinen der Qualitätsbewertung gehen.

### <a name="quality"></a>Qualität

![Verwenden Sie Guides für Qualitätssicherungsaufgaben](media/instruction-guides-hero-quality.png "Verwenden Sie Guides für Qualitätssicherungsaufgaben")

Führen Sie neue Prozesse ein und sorgen Sie für mehr Konsistenz, indem Sie das Wissen der Mitarbeiter in ein wiederholbares Werkzeug verwandeln.

Qualitätssicherungsleiter können Guides beispielsweise bestimmten [Produkten](../../commerce/product.md) zuweisen, die durch Routinen der Qualitätsbewertung gehen.

### <a name="certifications"></a>Bescheinigungen

![Verwenden Sie Anleitungen für zertifizierungsbezogene Aufgaben](media/instruction-guides-hero-certification.png "Verwenden Sie Guides für zertifizierungsbezogene Aufgaben")

Stellen Sie sicher, dass jeder Mitarbeiter hohe Standards erfüllt, indem Sie schnell erkennen, wer wo Hilfe benötigt.

### <a name="safety"></a>Sicherheit

![Verwenden Sie Guides in Arbeitsschutzanweisungen](media/instruction-guides-hero-safety.png "Verwenden Sie Guides in Arbeitsschutzanweisungen")

Geben Sie Anweisungen, die gefährliche Vorgänge virtuell durchlaufen, bevor Sie es in der physischen Umgebung versuchen. Mit einem Mixed-Reality-Ansatz können Mitarbeiter gefährliche Verfahren virtuell erleben.

Produktionsleiter können spezielle Handhabungsanweisungen für den Umgang mit Gefahrstoffen oder heikle Handhabungsverfahren bereitstellen, indem sie Anweisungen zu [Produktartikeln](../../commerce/product.md), [Arbeitspläne](routes-operations.md) und [Vorgängen](routes-operations.md#operation-relations) zuweisen.

## <a name="get-started-with-instructions-and-guides"></a>Los geht's mit Anweisungen und Guides

Um Anweisungen in Produktionsprozessen zu ermöglichen, bietet Supply Chain Management eine vorgefertigte Integration mit Dynamics 365 Guides an. Eine lizenzierte und installierte Anwendungsinstanz von Guides ist erforderlich, um Anweisungen für die Mixed Reality zu erstellen, zu warten und Produktionsressourcen und -arbeiten zuzuweisen.

### <a name="prerequisites"></a>Voraussetzungen

Um diese Funktion nutzen zu können, muss Ihr System Folgendes enthalten:

- Dynamics 365 Supply Chain Management Version 10.0.15 oder höher
- [Duales Schreiben](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write) für Supply Chain Management-Apps.
- [Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution)-Version 400.0.1.48 oder höher

### <a name="turn-on-the-feature"></a>Aktivieren Sie die Funktion

Um die Funktion auf Ihrem System verfügbar zu machen, müssen Sie dessen Konfigurationsschlüssel aktivieren. Sie müssen dies nur einmal tun. Dazu muss ein Administrator Folgendes tun:

1. Versetzen Sie Ihr System wie in [Wartungsmodus](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) beschrieben in den Wartungsmodus.
1. Gehen Sie zu **Systemadministration \> Einrichten \> Lizenzkonfiguration**.
1. Erweitern Sie den Abschnitt **Mixed Reality** und wählen Sie dann das Kontrollkästchen **Mixed-Reality-Anleitungen**.
1. Erweitern Sie den Abschnitt **Produktionsmanagement** und wählen Sie dann das Kontrollkästchen **Produktionsanweisungen**.
1. Deaktivieren Sie den Wartungsmodus wie in [Wartungsmodus](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) beschrieben.
  
## <a name="configure-how-guides-appear-on-the-shop-floor"></a>Konfigurieren Sie, wie Guides in der Werkstatt angezeigt werden

Um zu konfigurieren, wie Guides in der Werkstatt angezeigt werden, gehen Sie zu **Mixed Reality \> Dynamics 365 Guides \>, Guides-Integration konfigurieren**.

![Konfigurieren Sie die Guide-Integration für die Fertigung](media/instruction-guides-configure-integration.png "Konfigurieren Sie die Guide-Integration für die Fertigung")

Stellen Sie die folgenden Felder ein:

- **Microsoft Dataverse URL** - Geben Sie die URL für die Microsoft Dataverse Umgebung an, in der Sie Ihre Guides erstellen. Das Format ist „contoso.crm4.dynamics.com“, wobei der erste Teil der URL typischerweise nach Ihrer Organisation benannt ist (z. B. „contoso.“), der zweite Teil ist spezifisch für die Datenregion Ihrer Umgebung (z. B. „crm4.“) und der letzte Teil ist die Domäne (z. B. „dynamics.com“). Eine Möglichkeit, die richtige URL zu finden, ist, zu [home.dynamics.com](https://home.dynamics.com/) zu gehen und dann Ihre App Guides zu öffnen. Wenn Guides geöffnet wird, sehen Sie die URL in der Adressleiste Ihres Browsers (nehmen Sie nur die Basis-URL, die dem vorherigen Beispiel ähneln sollte). Dieser Wert wird verwendet, um Adressen für Ihre Anleitungen zusammenzustellen und wird in die QR-Codes kodiert.“
- **QR-Code-Größe** – Stellen Sie die Größe des gerenderten QR-Codes ein. Wir empfehlen, eine Größe zu wählen, die den größten Teil Ihres Bildschirms ausfüllt, jedoch nicht mehr. In der Regel ist *15* ist ein guter Wert.
- **QR-Code-Fehlerkorrekturstufe** – Stellen Sie die Granularität des QR-Codes ein. Eine höhere Granularität kann dazu beitragen, die Zuverlässigkeit des Codes zu erhöhen; Ihre **QR-Code-Größe** muss jedoch groß genug sein, um den Detaillierungsgrad zu unterstützen, der für die von Ihnen ausgewählte Korrekturstufe erforderlich ist.

> [!TIP]
> - Das Rendern von QR-Codes, die für Ihr Display zu groß sind, dauert etwas länger und wird dann verkleinert, um sie an Ihr Display anzupassen. Diese bieten keinen Vorteil.
> - Zu kleine QR-Codegrößen können die Fähigkeit von HoloLens zum richtigen Lesen des Codes in einigen Umgebungen verringern.
> - Wir empfehlen, dass Sie die Einstellungen für jedes Gerät testen, für das QR-Codes für HoloLens-Benutzer angezeigt werden. Wählen Sie Einstellungen, die eine ausreichende Lesbarkeit in Ihrer Werkstattumgebung gewährleisten.  

## <a name="get-an-overview-of-all-guide-assignments"></a>Verschaffen Sie sich einen Überblick über alle Aufgaben des Guides

Verwenden Sie die Seite **Alle Guides**, um eine Liste aller verfügbaren Guides in Ihrer Organisation sowie alle Zuordnungen zu Ihren Produktionsprozessen und Ressourcen zu sehen.. Zum Öffnen der Liste gehen Sie zu **Mixed Reality \> Guides \> Alle Guides**. Die Liste oben zeigt alle verfügbaren Guides. Sie können das Feld hier verwenden, um die Liste zu filtern. Die Liste unten zeigt alle Guide-Zuweisungen und bietet eine Symbolleiste für deren Verwaltung.

![Guides verwalten](media/instruction-guides-allguides.png "Guides verwalten")

In den folgenden Abschnitten werden die Objekttypen beschrieben, denen Sie Guides zuweisen können. Jede zugewiesene Anleitung enthält Anweisungen, die automatisch den jeweiligen Produktionsaufträgen beigefügt werden und in der Werkstatt verfügbar sind.

## <a name="associate-a-guide-to-a-resource"></a><a name="resources"></a>Verknüpfen Sie einen Guide mit einer Ressource

Fügen Sie einen Guide einer [Ressource](operations-resources.md) hinzu, um den Guide im Zusammenhang mit relevanten Produktionsaufträgen anzubieten.

### <a name="typical-scenario-using-resources"></a>Typisches Szenario mit Ressourcen

Sie können beispielsweise einen Guide mit allgemeinen Anweisungen zur Maschinensicherheit oder zur Handhabung an eine Ressource vom Typ Maschine anhängen. Der Guide ist dann für jeden Auftrag verfügbar, der auf der Maschine ausgeführt wird.

### <a name="add-a-guide-to-a-resource"></a>Fügen Sie einen Guide zu einer Ressource hinzu

So fügen Sie einen Guide einer Ressource hinzu:

1. Gehen Sie zu **Produktionssteuerung \> Setup \> Ressourcen \> Ressourcen**.
1. Wählen Sie im Listenbereich die Ressource aus, der Sie einen Guide zuweisen möchten.
1. Erweitern Sie das Inforegister **Zugehörige Guides**.
1. Wählen Sie **Hinzufügen** von der Symbolleiste **Zugehörige Guides**. Dem Raster wird eine neue Zeile hinzugefügt.
1. Verwenden Sie für die neue Zeile die Dropdown-Liste in der Spalte **Name**, um den Guide auszuwählen, den Sie zuweisen möchten. Wenn Sie eine große Anzahl von Guides haben, können Sie die Liste filtern, um den gesuchten zu finden.
    ![Guides verwalten](media/instruction-guides-allguides.png "Guides verwalten")

## <a name="associate-a-guide-to-a-resource-group"></a><a name="resource-groups"></a>Verknüpfen Sie einen Guide mit einer Ressourcengruppe

Sie können einen Guide [Ressourcengruppen](tasks/define-discrete-manufacturing-resource-group.md) hinzufügen, wenn Sie sie zum Verwalten von Gruppen von Maschinen, Produktionslinien oder Arbeitszellen verwenden.

### <a name="typical-scenarios-using-resource-groups"></a>Typisches Szenario mit Ressourcengruppen

**Beispiel 1:** Sie haben eine Ressourcengruppe für mehrere Maschinen desselben Modells definiert. Anstatt jeder relevanten Ressource die entsprechende Bedienungsanleitung für das Maschinenmodell zuzuweisen, können Sie den Guide auch der Ressourcengruppe zuweisen, die dieses Maschinenmodell widerspiegelt.

**Beispiel 2:** Sie haben eine Ressourcengruppe für eine Arbeitszelle definiert, die verschiedene Maschinen enthält, und Sie haben einen Guide, der allgemeine Anweisungen zum Verwalten der Arbeitszelle enthält. Der Guide gilt für alle Produktionsaktivitäten in dieser Arbeitszelle.

### <a name="add-a-guide-to-a-resource-group"></a>Einen Guide einer Ressourcengruppe hinzuzufügen

So fügen Sie einen Guide einer Ressourcengruppe hinzu:

1. Gehen Sie zu **Produktionssteuerung \> Setup \> Ressourcen \> Ressourcengruppen**.
1. Wählen Sie im Listenbereich die Ressourcengruppe aus, der Sie einen Guide zuweisen möchten.
1. Erweitern Sie das Inforegister **Zugehörige Guides**.
1. Wählen Sie **Hinzufügen** von der Symbolleiste **Zugehörige Guides**. Dem Raster wird eine neue Zeile hinzugefügt.
1. Verwenden Sie für die neue Zeile die Dropdown-Liste in der Spalte **Name**, um den Guide auszuwählen, den Sie zuweisen möchten. Wenn Sie eine große Anzahl von Guides haben, können Sie die Liste filtern, um den gesuchten zu finden.
    ![Hinzufügen eines Guide zu einer Ressourcengruppe](media/instruction-guides-resourcegroup.png "Hinzufügen eines Guide zu einer Ressourcengruppe")

## <a name="associate-a-guide-to-a-released-product"></a><a name="released-products"></a>Verknüpfen eines Guide mit einem freigegebenen Produkt

Sie können einen Guide jedem [freigegebenes Produkt](../pim/tasks/create-released-product-single-company.md) hinzufügen.

### <a name="typical-scenario-using-released-products"></a>Typisches Szenario mit freigegebenen Produkten

Guides auf Produktebene helfen den Mitarbeitern in der Werkstatt mit Anweisungen, die für den Betrieb oder die Handhabung eines bestimmten freigegebenen Produkts oder Artikels relevant sind.

### <a name="add-a-guide-to-a-released-product"></a>Hinzufügen eines Guide zu einem freigegebenen Produkt

So fügen Sie einen Guide einem freigegebenen Produkt hinzu:

1. Gehen Sie zu **Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**.
1. Öffnen Sie das Produkt, dem Sie einen Guide zuweisen möchten.
1. Öffnen Sie im Aktionsbereich die Registerkarte **Entwickler** und wählen Sie aus der Gruppe **Anzeige** **Zugehörige Guides** aus.
1. Die Seite **Zugehörige Guides** wird für Ihr ausgewähltes Produkt geöffnet.
1. Wählen Sie im Aktivitätsbereich **Hinzufügen** aus, um eine neue Position zum Raster hinzuzufügen. 
1. Verwenden Sie für die neue Zeile die Dropdown-Liste in der Spalte **Name**, um den Guide auszuwählen, den Sie zuweisen möchten.
    ![Hinzufügen eines Guides zu einem freigegebenen Produkt](media/instruction-guides-ReleasedProduct-AddGuides.png "Hinzufügen eines Guides zu einem freigegebenen Produkt")

## <a name="associate-a-guide-to-a-formula"></a><a name="formulas"></a>Verknüpfen eines Guides mit einer Formel

Sie können einen Guide jeder beliebigen [Formel](bill-of-material-bom.md#formulas-co-products-and-by-products) hinzufügen.

### <a name="typical-scenario-using-formulas"></a>Typisches Szenario mit Formeln
  
Guides auf Formelebene bieten Werkstattmitarbeitern Anweisungen zur Handhabung im Zusammenhang mit einer Formel oder einem Rezept. Guides können auch Versionen einer Formel zugewiesen werden.

> [!NOTE]
> Sie können einem Arbeitsplan, einer Arbeitsplanversion oder einer Arbeitsplanvorgangsbeziehung einen fertigungsrelevanten Leitfaden auf der Basis einer Formel zuordnen.  

> Guides können derzeit nicht an einzelne Formelpositionen angehängt werden.

### <a name="add-a-guide-to-a-formula"></a>Hinzufügen eines Guides zu einer Formel

So fügen Sie einen Guide einer Formel hinzu:

1. Gehen Sie zu **Produktinformationsverwaltung \> Stücklisten und Formeln \> Formeln**.
1. Öffnen Sie die Formel, der Sie einen Guide zuweisen möchten.
1. Öffnen Sie die Registerkarte **Überschrift** über dem oberen Inforegister.
1. Erweitern Sie das Inforegister **Zugehörige Guides**.
1. Wählen Sie **Hinzufügen** von der Symbolleiste **Zugehörige Guides**. Dem Raster wird eine neue Zeile hinzugefügt.
1. Verwenden Sie für die neue Zeile die Dropdown-Liste in der Spalte **Name**, um den Guide auszuwählen, den Sie zuweisen möchten.
    ![Hinzufügen eines Guides zu einer Formel](media/instruction-guides-Formula.png "Hinzufügen eines Guides zu einer Formel")

## <a name="associate-a-guide-to-a-formula-version"></a><a name="formula-versions"></a>Verknüpfen eines Guides mit einer Formelversion

Sie können einen Guide jeder beliebigen [Formelversion](bill-of-material-bom.md#bom-and-formula-versions) hinzufügen.

### <a name="typical-scenario-using-formula-versions"></a>Typisches Szenario mit Formelversionen

An einer einzelnen Version einer Formel angehängte Guides geben den Mitarbeitern in der Werkstatt Anweisungen, die sie durch die Erstellung dieser Version des Formelrezepts führen.

> [!TIP]
> Sie können einem Arbeitsplan, einer Arbeitsplanversion oder einer Arbeitsplanvorgangsbeziehung einen fertigungsrelevanten Leitfaden auf der Basis dieser Formelversion zuordnen.  

> [!NOTE]
> Guides können derzeit nicht an einzelne Formelpositionen angehängt werden.

### <a name="add-a-guide-to-a-formula-version"></a>Hinzufügen eines Guides zu einer Formelversion

So fügen Sie einen Guide einer Formelversion hinzu:

1. Gehen Sie zu **Produktinformationsverwaltung \> Stücklisten und Formeln \> Formeln**.
1. Öffnen Sie die Formel, die eine Version enthält, der Sie einen Guide zuweisen möchten.
1. Öffnen Sie die Registerkarte **Überschrift** über dem oberen Inforegister.
1. Auf dem Inforegister **Formelversionen** wählen Sie die Version aus, der Sie einen Guide zuweisen möchten.
1. Auf der Symbolleiste **Formelversionen** wählen Sie **Zugehörige Guides** aus.
    ![Öffnen Sie die Guides, die einer ausgewählten Formelversion zugeordnet sind](media/instruction-guides-FormulaVersion.png "Öffnen Sie die Guides, die einer ausgewählten Formelversion zugeordnet sind")
1. Die Seite **Zugehörige Guides** wird für Ihre Formelversion geöffnet.
1. Wählen Sie im Aktivitätsbereich **Hinzufügen** aus, um eine neue Position zum Raster hinzuzufügen. 
1. Verwenden Sie für die neue Zeile die Dropdown-Liste in der Spalte **Name**, um den Guide auszuwählen, den Sie zuweisen möchten.
    ![Hinzufügen eines Guides zu einer Formelversion](media/instruction-guides-FormulaVersionAddGuide.png "Hinzufügen eines Guides zu einer Formelversion")

## <a name="associate-a-guide-to-a-bill-of-materials"></a><a name="bom"></a>Verknüpfen eines Guides mit einer Stückliste

Sie können eine Anleitung jeder beliebigen [Stückliste](bill-of-material-bom.md) (BOM) hinzufügen.

### <a name="typical-scenario-using-bills-of-materials"></a>Typisches Szenario mit Stücklisten

An eine Stückliste angehängte Guides geben den Mitarbeitern in der Werkstatt Anweisungen, wie das Material aus einer Stückliste vorbereitet und gehandhabt wird. Guides können auch Versionen einer Stückliste zugewiesen werden.

> [!NOTE]
> Guides können derzeit nicht an einzelne Stücklistenpositionen angehängt werden.

### <a name="add-a-guide-to-a-bill-of-materials"></a>Hinzufügen eines Guides zu einer Stückliste

So fügen Sie einen Guide einer Stückliste hinzu:

1. Gehen Sie zu **Produktinformationsverwaltung \> Stücklisten und Formeln \> Stücklisten**.
1. Öffnen Sie die Stückliste, der Sie einen Guide zuweisen möchten.
1. Öffnen Sie die Registerkarte **Überschrift** über dem oberen Inforegister.
1. Erweitern Sie das Inforegister **Zugehörige Guides**.
1. Wählen Sie **Hinzufügen** von der Symbolleiste **Zugehörige Guides**. Dem Raster wird eine neue Zeile hinzugefügt.
1. Verwenden Sie für die neue Zeile die Dropdown-Liste in der Spalte **Name**, um den Guide auszuwählen, den Sie zuweisen möchten.
    ![Hinzufügen eines Guides zu einer Stückliste](media/instruction-guides-BOM.png "Hinzufügen eines Guides zu einer Stückliste")

## <a name="associate-a-guide-to-a-bill-of-materials-version"></a><a name="bom-versions"></a>Verknüpfen eines Guides mit einer Stücklistenversion

Sie können eine Anleitung jeder beliebigen [Stücklistenversion](bill-of-material-bom.md#bom-and-formula-versions) hinzufügen.

### <a name="typical-scenario-using-bill-of-materials-versions"></a>Typisches Szenario mit Stücklistenversionen

An einer einzelnen Stücklistenversion angehängte Guides enthalten Fertigungsanweisungen, in denen erläutert wird, wie Material für eine Version einer Stückliste vorbereitet und gehandhabt wird, die sich von der generischen Stückliste oder anderen Versionen davon unterscheidet.

> [!NOTE]
> Guides können derzeit nicht an einzelne Stücklistenpositionen angehängt werden.

### <a name="add-a-guide-to-a-bill-of-materials-version"></a>Hinzufügen eines Guides zu einer Stücklistenversion

So fügen Sie einen Guide einer Stücklistenversion hinzu:

1. Gehen Sie zu **Produktinformationsverwaltung \> Stücklisten und Formeln \> Stücklisten**.
1. Öffnen Sie die Stückliste, die eine Version enthält, der Sie einen Guide zuweisen möchten.
1. Öffnen Sie die Registerkarte **Überschrift** über dem oberen Inforegister.
1. Auf dem Inforegister **Stücklistenversionen** wählen Sie die Version aus, der Sie einen Guide zuweisen möchten.
1. Auf der Symbolleiste **Stücklistenversionen** wählen Sie **Zugehörige Guides** aus.
    ![Öffnen Sie die Guides, die einer ausgewählten Stücklistenversion zugeordnet sind](media/instruction-guides-BOMVersion.png "Öffnen Sie die Guides, die einer ausgewählten Stücklistenversion zugeordnet sind")
1. Die Seite **Zugehörige Guides** wird für Ihre Stücklistenversion geöffnet.
1. Wählen Sie im Aktivitätsbereich **Hinzufügen** aus, um eine neue Position zum Raster hinzuzufügen.
1. Verwenden Sie für die neue Zeile die Dropdown-Liste in der Spalte **Name**, um den Guide auszuwählen, den Sie zuweisen möchten.
    ![Hinzufügen eines Guides zu einer Stücklistenversion](media/instruction-guides-BOMVersionAddGuide.png "Hinzufügen eines Guides zu einer Stücklistenversion")

## <a name="associate-a-guide-to-a-route"></a><a name="routes"></a>Verknüpfen eines Guides mit einem Arbeitsplan

Sie können einen Guide jedem beliebigen [Arbeitsplan](routes-operations.md) hinzufügen.

### <a name="typical-scenario-using-routes"></a>Typisches Szenario mit Arbeitsplänen

Arbeitspläne werden normalerweise verwendet, um anzugeben, wie ein bestimmtes freigegebenes Produkt basierend auf einer Stückliste oder Stücklistenversion und mit einer Reihe von Ressourcen oder Ressourcengruppen hergestellt werden soll.

Weisen Sie einem Arbeitsplan einen Leitfaden zu, um schrittweise Anweisungen für den jeweiligen Produktionsprozess bereitzustellen.

### <a name="add-a-guide-to-a-route"></a>Hinzufügen eines Guides zu einem Arbeitsplan

So fügen Sie einen Guide einem Arbeitsplan hinzu:

1. Gehen Sie zu **Produktionskontrolle \> Alle Arbeitspläne**.
1. Öffnen Sie den Arbeitsplan, dem Sie einen Guide zuweisen möchten.
1. Erweitern Sie das Inforegister **Zugehörige Guides**.
1. Wählen Sie **Hinzufügen** von der Symbolleiste **Zugehörige Guides**. Dem Raster wird eine neue Zeile hinzugefügt.
1. Verwenden Sie für die neue Zeile die Dropdown-Liste in der Spalte **Name**, um den Guide auszuwählen, den Sie zuweisen möchten.
    ![Hinzufügen eines Guides zu einem Arbeitsplan](media/instruction-guides-Route.png "Hinzufügen eines Guides zu einem Arbeitsplan")

## <a name="associate-a-guide-to-a-route-version"></a><a name="route-versions"></a>Verknüpfen eines Guides mit einer Arbeitsplanversion

Sie können einen Guide jeder beliebigen [Arbeitsplanversion](routes-operations.md#route-versions) hinzufügen.

### <a name="typical-scenario-using-route-versions"></a>Typisches Szenario mit Arbeitsplanversionen

Arbeitsplanversionen werden normalerweise verwendet, um Varianten von Produktionsprozessen basierend auf einem vorhandenen Arbeitsplan anzugeben. Sie können jeder Arbeitsplanversion unterschiedliche Guides zuweisen.

### <a name="add-a-guide-to-a-route-version"></a>Hinzufügen eines Guides zu einer Arbeitsplanversion

So fügen Sie einen Guide einer Arbeitsplanversion hinzu:

1. Gehen Sie zu **Produktionskontrolle \> Alle Arbeitspläne**.
1. Öffnen Sie den Arbeitsplan, dem Sie einen Guide zuweisen möchten.
1. Auf dem Inforegister **Versionen** wählen Sie die Version aus, der Sie einen Guide zuweisen möchten.
1. Auf der Symbolleiste **Versionen** wählen Sie **Zugehörige Guides** aus.
    ![Öffnen Sie die Guides, die einer ausgewählten Arbeitsplanversion zugeordnet sind](media/instruction-guides-RouteVersion.png "Öffnen Sie die Guides, die einer ausgewählten Arbeitsplanversion zugeordnet sind")
1. Die Seite **Zugehörige Guides** wird für Ihre Stücklistenversion geöffnet.
1. Wählen Sie im Aktivitätsbereich **Hinzufügen** aus, um eine neue Position zum Raster hinzuzufügen.
1. Verwenden Sie für die neue Zeile die Dropdown-Liste in der Spalte **Name**, um den Guide auszuwählen, den Sie zuweisen möchten.
    ![Hinzufügen eines Guides zu einer Arbeitsplanversion](media/instruction-guides-RouteVersionAddGuide.png "Hinzufügen eines Guides zu einer Arbeitsplanversion")

## <a name="associate-a-guide-to-a-route-operation-relation"></a><a name="route-operation-relations"></a>Verknüpfen eines Guides mit einer Arbeitsplanvorgangsbeziehung

Sie können einen Guide jeder beliebigen [Arbeitsplanvorgangsbeziehung](routes-operations.md#operation-relations) hinzufügen.

### <a name="typical-scenario-using-route-operation-relations"></a>Typisches Szenario mit Arbeitsplanvorgangsbeziehung

Vorgangsbeziehungen sind die spezifischste Methode, um einem Produktprozess und den damit verbundenen Vorgängen eine Anleitung hinzuzufügen. Sie können Anleitungen für jeden Vorgang in einem Arbeitsplan und unterschiedliche Anleitungen für jede Art von Beziehungskontext angeben, die für einen Arbeitsplan angegeben sind, z. B. für bestimmte Elemente, Konfigurationen und mehr. Sie können auch angeben, für welche Phasen des Vorgangs die Anleitung gilt (z. B. Einrichtung, Warteschlange, Prozess oder Transport).

> [!NOTE]
> Wenn Sie spezifische Guides für mehrere Vorgangsbeziehungen eines Arbeitsplans angeben, wird unter diesen Guides nur die Anleitung aus der spezifischsten Beziehung in der Werkstatt für den generierten Einzelvorgang angezeigt.

### <a name="add-a-guide-to-a-route-operation-relation"></a>Hinzufügen eines Guides zu einer Arbeitsplanvorgangsbeziehung

So fügen Sie einen Guide zu einer Arbeitsplanvorgangsbeziehung hinzu:

1. Gehen Sie zu **Produktionskontrolle \> Alle Arbeitspläne**.
1. Öffnen Sie den Arbeitsplan, dem Sie einen Guide zuweisen möchten.
1. Öffnen Sie im Aktionsbereich die Registerkarte **Arbeitsplan** und wählen Sie aus der Gruppe **Verwalten** **Arbeitsplandetails** aus.
1. Die Seite **Arbeitsplandetails** wird für Ihren ausgewählten Arbeitsplan geöffnet.
1. Wählen Sie im oberen Raster den Vorgang aus, für den Sie eine Anleitung bereitstellen möchten.
1. Wählen Sie im unteren Raster eine bestimmte Beziehung (oder die generische Beziehung **Alle**) aus.
    ![Wählen Sie einen Vorgang und dann eine Beziehung aus](media/instruction-guides-RouteOperationRelation.png "Wählen Sie einen Vorgang und dann eine Beziehung aus")
1. Öffnen Sie über dem unteren Raster die Registerkarte **Zugehörige Guides** aus.  ![Die Registerkarte Zugehörige Guides](media/instruction-guides-RouteOperationRelation-AddGuide.png "Die Registerkarte Zugehörige Guides")
1. Wählen Sie **Hinzufügen** in der Symbolleiste oben im unteren Raster aus, um dem Raster eine neue Position hinzuzufügen.
1. Verwenden Sie für die neue Zeile die Dropdown-Liste in der Spalte **Name**, um den Guide auszuwählen, den Sie zuweisen möchten. Aktivieren Sie im Rest der Zeile das Kontrollkästchen für jeden Kontext, in dem der ausgewählte Guide verfügbar sein soll.

> [!NOTE]
> Sie können für jede Phase jedes Vorgangs eine oder mehrere Guides hinzufügen.

## <a name="select-guides-from-the-shop-floor-execution-interface"></a>Wählen Sie Guides aus der Fertigungsausführungsoberfläche aus

Wenn ein Mitarbeiter eine Einzelvorgangsliste auf der Fertigungsausführungsoberfläche öffnet, findet Supply Chain Management die relevanten Guides für die angezeigten Einzelvorgänge. Verwenden Sie die **Anleitungen**-Schaltfläche, um die entsprechenden Anleitungen anzuzeigen.

![Schaltfläche Guides auf der Fertigungsausführungsoberfläche](media/instruction-guides-Shopfloor1.png "Schaltfläche Guides auf der Fertigungsausführungsoberfläche")

Ziehen Sie dann eine HoloLens an und greifen Sie auf die jeweilige Anleitung zu, indem Sie einen Blick auf den QR-Code werfen und den entsprechenden Guide aktivieren.

![QR-Code für den Zugriff auf Anleitungen mit einer HoloLens](media/instruction-guides-Shopfloor2.png "QR-Code für den Zugriff auf Guides mit einer HoloLens")

## <a name="resolving-the-logic-for-selecting-guides"></a><a name="logic"></a>Auflösen der Logik zur Auswahl von Guides

Sie können den folgenden Produktionsdaten Guides hinzufügen:

- [Ressourcen](#resources)
- [Ressourcengruppen ](#resource-groups)
- [Freigegebene Produkte](#released-products)
- [Formeln](#formulas)
- [Formelversionen](#formula-versions)
- [Stücklisten](#bom)
- [Stücklistenversionen](#bom-versions)
- [Arbeitspläne](#routes)
- [Arbeitsplanversionen](#route-versions)
- [Arbeitsplanbetriebsbeziehungen](#route-operation-relations)

Wenn das Supply Chain Management die Einzelvorgänge für die Produktion generiert, werden die entsprechenden Guides aus diesen Quellen gesammelt. Beachten Sie die folgenden wichtigen Regeln.

- Wenn Sie eine Stücklisten- oder Formelversion an einen Arbeitsplan oder einen Fertigungsauftrag anhängen, werden alle an diese Version angehängten Guides und auch die an die übergeordnete Stückliste oder Formel dieser Version angehängten Guides im Einzelvorgang angezeigt.
- Wenn Sie eine Arbeitsplanversion an einen Produktionsauftrag anhängen, werden alle an diese Version angehängten Guides und auch die Guides, die an den übergeordneten Arbeitsplan dieser Version angehängt sind, im Einzelvorgang angezeigt.
- Wenn Sie mehrere Arbeitsplanvorgangsbeziehungen definieren, die die Beziehung *Alle* enthalten, und ihnen Guides zuordnen, werden nur die Guides aus der spezifischsten Beziehung für den Einzelvorgang angezeigt.  

![Diagramm zum Auflösen der relevanten Guides](media/instruction-guides-Resolve.png "Diagramm zum Auflösen der relevanten Guides")


[!INCLUDE[footer-include](../../includes/footer-banner.md)]