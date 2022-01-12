---
title: Einrichten einer Bedarfsplanung
description: In diesem Thema werden die Einrichtungsaufgaben, die Sie ausführen müssen, um die Bedarfsplanung vorzubereiten, beschrieben.
author: ChristianRytt
ms.date: 11/23/2021
ms.topic: article
ms.search.form: ReqDemPlanDefaultAlgorithmParameters, ReqDemPlanForecastParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4f53171361b655ab4ae05894d098203df0af8d60
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920772"
---
# <a name="demand-forecasting-setup"></a>Einrichtung der Bedarfsplanung

[!include [banner](../includes/banner.md)]

Dieses Thema beschreibt, wie Sie Bedarfsplanung festlegen.  

## <a name="item-allocation-keys"></a>Artikelzuteilungsschlüssel

Artikelzuordnungsschlüssel legen Artikelgruppen fest. Eine Bedarfsplanung wird für einen Artikel und die dazugehörigen Dimensionen nur berechnet, wenn der Artikel Teil eines Artikelverteilungsschlüssels ist. Diese Regel erzwingt das Gruppieren größerer Mengen, sodass die Bedarfsplanungen schneller erstellt werden können. Planungen werden auf der Grundlage von historischen Daten erstellt.

Ein Artikel und die dazugehörigen Dimensionen müssen nur zu einem Artikelverteilungsschlüssel gehören, wenn der Artikelverteilungsschlüssel für die Planungserstellung verwendet wird.

Gehen Sie folgendermaßen vor, um Artikelzuordnungsschlüssel zu erstellen und ihnen eine Lagerhaltungseinheit (SKU) hinzuzufügen.

1. Gehen Sie zu **Produktprogrammplanung \> Einrichten \> Bedarfsplanung \> Artikelzuteilungsschlüssel**.
1. Wählen Sie entweder einen Artikelzuordnungsschlüssel im Listenbereich, oder wählen Sie **Neu** im Aktivitätsbereich, um einen neuen zu erstellen. Legen Sie in der Kopfzeile für den neuen oder ausgewählten Schlüssel die folgenden Felder fest:

    - **Artikelzuordnungsschlüssel** – Geben Sie einen eindeutigen Namen für den Schlüssel ein.
    - **Name** - Geben Sie einen beschreibenden Namen für den Schlüssel ein.

1. Führen Sie einen dieser Schritte aus, um dem ausgewählten Artikelzuordnungsschlüssel Artikel hinzuzufügen oder Artikel zu entfernen:

    - Wählen Sie auf dem Inforegister **Artikelzuordnung** die Schaltflächen **Neu** und **Löschen** in der Symbolleiste, um Artikel nach Bedarf hinzuzufügen oder zu entfernen. Wählen Sie für jede Zeile die Artikelnummer aus, und weisen Sie dann den anderen Spalten nach Bedarf Dimensionswerte zu. Wählen Sie auf der Symbolleiste **Displayabmessungen** aus, um den im Raster angezeigten Satz von Dimensionsspalten zu ändern. (Der Wert in der Spalte **Prozent** wird ignoriert, wenn Bedarfsplanungen generiert werden.)
    - Wenn Sie dem Schlüssel eine große Anzahl von Artikeln hinzufügen möchten, wählen Sie im Aktivitätsbereich **Artikel zuweisen** aus, um eine Seite zu öffnen, auf der Sie mehrere Artikel suchen und der ausgewählten Taste zuweisen können.

> [!IMPORTANT]
> Achten Sie darauf, nur relevante Artikel in jeden Artikelzuordnungsschlüssel aufzunehmen. Unnötige Artikel verursachen möglicherweise höhere Kosten, wenn Sie Microsoft Azure Machine Learning verwenden.

## <a name="intercompany-planning-groups"></a>Intercompany-Planungsgruppen

Die Bedarfsplanung kann unternehmensübergreifende Planungen generieren. In Dynamics 365 Supply Chain Management werden Unternehmen, die zusammen geplant werden, in derselben Intercompany-Planungsgruppe gruppiert. Um pro Unternehmen festzulegen, welche Artikelzuordnungsschlüssel für die Bedarfsplanung berücksichtigt werden sollen, ordnen Sie dem Mitglied der Intercompony-Planungsgruppe einen Artikelzuordnungsschlüssel zu.

> [!IMPORTANT]
> Die Planungsoptimierung unterstützt derzeit keine Intercompony-Planungsgruppen. Um eine Intercompony-Planung durchzuführen, die die Planungsoptimierung verwendet, richten Sie Masterplanungs-Stapelaufträge ein, die Masterpläne für alle relevanten Unternehmen enthalten.

Gehen Sie zum Einrichten Ihrer Intercompany-Planungsgruppen folgendermaßen vor.

1. Wechseln Sie zu **Masterplan \> Einrichten \> Intercompany-Planungsgruppen**.
1. Wählen Sie entweder eine Planungsgruppe im Listenbereich, oder wählen Sie **Neu** im Aktivitätsbereich, um eine neue zu erstellen. Legen Sie in der Kopfzeile für die neue oder ausgewählte Gruppe die folgenden Felder fest:

    - **Name**: Geben Sie hier einen eindeutigen Namen für die Planungsgruppe ein.
    - **Beschreibung** – Geben Sie eine kurze Beschreibung der Planungsgruppe ein.

1. Verwenden Sie im Inforegister **Mitglieder der Intercompany-Planungsgruppe** die Schaltflächen in der Symbolleiste, um eine Zeile für jede Firma (juristische Person) hinzuzufügen, die Teil der Gruppe sein soll. Legen Sie für jede Position die folgenden Felder fest:

    - **Juristische Person** – Wählen Sie den Namen einer Firma (juristische Person) aus, die Mitglied der ausgewählten Gruppe ist.
    - **Planungsreihenfolge** – Ordnen Sie die Reihenfolge zu, in der die Firma relativ zu anderen Firmen bearbeitet werden soll. Niedrige Werte werden zuerst verarbeitet. Diese Reihenfolge kann wichtig sein, wenn die Nachfrage nach einem Unternehmen andere Unternehmen beeinflusst. In diesen Fällen sollte das Unternehmen, das den Bedarf liefert, zuletzt bearbeitet werden.
    - **Masterplan** – Wählen Sie den Masterplan aus, der für das aktuelle Unternehmen ausgelöst werden soll.
    - **Automatisch in statischen Plan kopieren** – Aktivieren Sie dieses Kontrollkästchen, um das Ergebnis des Plans in den statischen Plan zu kopieren.
    - **Automatisch in dynamischen Plan kopieren** – Aktivieren Sie dieses Kontrollkästchen, um das Ergebnis des Plans in den dynamischen Plan zu kopieren.

1. Wenn den Intercompany-Planungsgruppenmitgliedern keine Artikelverteilungsschlüssel zugewiesen sind, wird standardmäßig eine Bedarfsplanung für alle Artikel berechnet, die allen Artikelverteilungsschlüsseln aus allen Unternehmen zugewiesen sind. Zusätzliche Filtermöglichkeiten für Firmen und Artikelzuordnungsschlüssel sind im Dialogfeld **Statistische Grundplanung erstellen** (**Masterplanung \> Planung \> Bedarfsplanung \> Statistische Grundplanung erstellen**). Um einem Unternehmen in der ausgewählten Intercompany-Planungsgruppe Artikelzuordnungsschlüssel zuzuweisen, wählen Sie das Unternehmen und dann im Inforegister **Mitglieder der Intercompany-Planungsgruppe** auf der Symbolleiste **Artikelzuordnungsschlüssel** aus.

> [!IMPORTANT]
> Achten Sie darauf, nur relevante Artikelzuordnungsschlüssel in jede Intercompany-Planungsgruppe aufzunehmen. Unnötige Artikel verursachen möglicherweise höhere Kosten, wenn Sie Azure Machine Learning verwenden.

## <a name="set-up-demand-forecasting-parameters"></a><a name="parameters"></a>Parameter für die Bedarfsplanung festlegen

Verwenden Sie die **Parameter der Bedarfsplanung**-Seite, um mehrere Optionen einzurichten, die steuern, wie die Bedarfsplanung in Ihrem System funktioniert.

### <a name="open-the-demand-forecasting-parameters-page"></a>Die Seite „Parameter der Bedarfsplanung“ öffnen

Um die Parameter der Bedarfsplanung einzurichten, gehen Sie zu **Masterplanung \> Einstellungen \>  Bedarfsplanung \> Bedarfsplanungsparameter**. Da die Bedarfsplanung unternehmensübergreifend ausgeführt wird, sind die Einstellungen global. Das bedeutet, sie beziehen sich auf alle juristischen Personen (Unternehmen).

### <a name="general-settings"></a>Allgemeine Einstellungen

Verwenden Sie die Registerkarte **Allgemein** der Seite **Bedarfsplanungsparameter**, um allgemeine Einstellungen für die Bedarfsplanung zu definieren.

#### <a name="demand-forecast-unit"></a>Bedarfsplanungseinheit

Die Bedarfsplanung generiert die Planung in Mengen. Daher muss die Maßeinheit, in der die Menge ausgedrückt werden soll, im Feld **Bedarfsplanungseinheit** angegeben werden. Dieses Feld definiert die Einheit, die für alle Bedarfsplanungen verwendet wird, unabhängig von den üblichen Lagereinheiten für jedes Produkt. Durch die Verwendung einer konsistenten Einheit helfen Sie sicherzustellen, dass die Aggregation und Prozentverteilung sinnvoll sind. Weitere Informationen zur Aggregation und Prozentverteilung finden Sie unter [Manuelle Anpassungen der Grundplanung](manual-adjustments-baseline-forecast.md).

Für jede Maßeinheit, die für Lagermengeneinheiten verwendet wird, die in der Bedarfsplanung enthalten sind, überprüfen Sie, ob eine Umrechnungsregel für die Maßeinheit und die allgemeine Maßeinheit der Planung vorliegt, die Sie hier auswählen. Wenn Sie eine Planung generieren, wird die Liste der Artikel, die keine Maßeinheitsumrechnung haben, protokolliert. Daher können Sie die Einrichtung leicht korrigieren. Weitere Informationen über Maßeinheiten und wie sie untereinander konvertiert werden, finden Sie unter [Maßeinheit verwalten](../pim/tasks/manage-unit-measure.md).

#### <a name="transaction-types"></a>Transaktionstypen

Verwenden Sie die Felder im Inforegister **Transaktionsarten**, um die Transaktionsarten auszuwählen, die verwendet werden, wenn die statistische Grundplanung generiert wird.

Die Bedarfsplanung kann verwendet werden, um abhängigen Bedarf und unabhängigen Bedarf zu planen. Wenn beispielsweise nur die Option **Auftrag** auf *Ja* festgelegt wird und wenn alle Artikel, die für die Bedarfsplanung berücksichtigt werden, verkauft wurden, berechnet das System unabhängigen Bedarf. Allerdings können wichtige Unterkomponenten zu den Artikelverteilungsschlüsseln hinzugefügt werden und in die Bedarfsplanung einbezogen werden. Wenn in diesem Fall die Option **Produktionsauftragsposition** auf *Ja* festgelegt ist, wird eine abhängige Planung berechnet.

Sie können Transaktionsarten für einen oder mehrere bestimmte Artikelzuordnungsschlüssel überschreiben, indem Sie die Registerkarte **Artikelzuordnungsschlüssel** verwenden. Diese Registerkarte bietet ähnliche Felder.

#### <a name="choose-how-to-create-the-baseline-forecast"></a>Auswählen, wie Sie die Grundplanung erstellen

Im Feld **Strategie zur Planungsgenerierung** können Sie die Methode auswählen, die zum Erstellen einer Grundplanung verwendet wird. Es stehen drei Methoden zur Verfügung:

- *Den historischen Bedarf kopieren* – Erstellen Sie Planungen, indem Sie einfach historische Daten kopieren.
- *Azure Machine Learning-Dienst* – Verwenden Sie ein Planungsmodell, das den Azure Machine Learning Service verwendet. Der Azure Machine Learning Service ist die aktuelle Machine Learning-Lösung für Azure. Daher empfehlen wir Ihnen, ihn zu verwenden, wenn Sie ein Planungsmodell verwenden möchten.
- *Azure Machine Learning* – Verwenden Sie ein Planungsmodell, das Azure Machine Learning Studio (klassisch) verwendet. Azure Machine Learning Studio (klassisch) ist veraltet und wird in Kürze aus Azure entfernt. Daher empfehlen wir Ihnen die Auswahl von *Azure Machine Learning Sercice*, wenn Sie die Bedarfsplanung zum ersten Mal einrichten. Wenn Sie derzeit Azure Machine Learning Studio (klassisch) verwenden, sollten Sie so schnell wie möglich zum Azure Machine Learning Service wechseln.

Sie können die Planungsgenerierungsmethode für einen oder mehrere bestimmte Artikelzuordnungsschlüssel überschreiben, indem Sie die Registerkarte **Artikelzuordnungsschlüssel** verwenden. Diese Registerkarte bietet ähnliche Felder.

#### <a name="override-default-forecast-algorithm-parameters-globally"></a>Standardparameter des Planungsalgorithmus global überschreiben

Standardparameter und -werte für den Planungsalgorithmus werden der Seite **Parameter der Bedarfsplanung** (**Masterplanung \> Einrichtung \> Bedarfsplanung \> Parameter der Bedarfsplanung**) zugewiesen. Sie können sie jedoch global überschreiben, indem Sie das Inforegister **Parameter des Planungsalgorithmus** auf der Registerkarte **Allgemein** der Seite **Parameter der Bedarfsplanung** verwenden. (Sie können sie auch für bestimmte Zuordnungsschlüssel überschreiben, indem Sie die **Artikelzuordnungsschlüssel**-Registerkarte auf der **Parameter der Bedarfsplanung**-Seite verwenden.)

Verwenden Sie die Schaltflächen **Hinzufügen** und **Entfernen** in der Symbolleiste, um die erforderliche Sammlung der Parameterüberschreibungen zu erstellen. Wählen Sie für jeden Parameter in der Liste einen Wert im Feld **Name** aus und geben Sie dann einen entsprechenden Wert in das Feld **Wert** ein. Alle hier nicht aufgeführten Parameter übernehmen ihre Werte aus den Einstellungen auf der Seite **Parameter der Bedarfsplanung**. Weitere Informationen zur Verwendung des Standardparametersatzes und zur Auswahl von Werten finden Sie im Abschnitt [Standardparameter und -werte für Bedarfsplanungsmodelle](#model-parameters) Sektion.

### <a name="set-forecast-dimensions"></a>Planungsdimensionen festlegen

Eine Planungsdimension gibt die Detailebene an, für die die Planung definiert ist. Unternehmen, Site und Artikelzuordnungsschlüssel sind erforderliche Planungsdimensionen. Sie können Planungen auch für Lagerort, Bestandsstatus, Debitorengruppe, Debitorenkonto, Land/Region, Bundesland und/oder Artikelebene sowie auf allen Artikeldimensionsebenen generieren. Verwenden Sie die Registerkarte **Planungsdimensionen** auf der Seite **Bedarfsplanungsparameter**, um die Gruppe von Planungsdimensionen auswählen, die verwendet wird, wenn die Bedarfsplanung generiert wird.

Sie können jederzeit Planungsdimensionen zur Liste mit den Dimensionen hinzufügen, die für Bedarfsplanung verwendet werden. Sie können Planungsdimensionen auch aus der Liste entfernen. Allerdings gehen manuelle Anpassungen verloren, wenn Sie eine Planungsdimension hinzufügen oder entfernen.

### <a name="set-up-overrides-for-specific-item-allocation-keys"></a>Überschreibungen für bestimmte Artikelzuordnungsschlüssel einrichten

Nicht alle Artikel funktionieren aus Sicht der Bedarfsplanung auf dieselbe Weise. Daher können Sie für die meisten Einstellungen, die auf der Registerkarte **Allgemein** definiert sind, Überschreibungen einrichten, die für Zuweisungsschlüssel spezifisch sind. Ausnahme ist die Einheit der Bedarfsplanung. Gehen Sie folgendermaßen vor, um Überschreibungen für einen bestimmten Artikelzuordnungsschlüssel einzurichten.

1. Verwenden Sie auf der Seite **Parameter der Bedarfsplanung**, auf der Registerkarte **Artikelzuordnungsschlüssel** die Schaltflächen in der Symbolleiste, um dem Raster auf der linken Seite Artikelzuordnungsschlüssel hinzuzufügen oder sie nach Bedarf zu entfernen. Wählen Sie dann den Zuordnungsschlüssel aus, für den Sie Überschreibungen einrichten möchten.
1. Aktivieren Sie im Inforegister **Transaktionsarten** die Arten von Transaktionen, die Sie verwenden möchten, um die statistische Grundplanung für Produkte zu generieren, die zum ausgewählten Zuordnungsschlüssel gehören. Die Einstellungen funktionieren genauso wie auf der Registerkarte **Allgemein**, sie gelten jedoch nur für den ausgewählten Artikelzuordnungsschlüssel. Alle Einstellungen hier (die *Ja*- Werte und die *Nein*-Werte) überschreiben alle **Transaktionsarten**-Einstellungen auf der Registerkarte **Allgemein**.
1. Wählen Sie im Inforegister **Parameter des Planungsalgorithmus** die Planungsgenerierungsstrategie und die Parameterüberschreibungen des Planungsalgorithmus für Produkte aus, die zum ausgewählten Zuordnungsschlüssel gehören. Diese Einstellungen funktionieren genauso wie auf der Registerkarte **Allgemein**, sie gelten jedoch nur für den ausgewählten Artikelzuordnungsschlüssel. Verwenden Sie die Schaltflächen **Hinzufügen** und **Entfernen** in der Symbolleiste, um die erforderliche Sammlung der Parameterüberschreibungen zu definieren. Wählen Sie für jeden Parameter in der Liste einen Wert im Feld **Name** aus und geben Sie dann einen entsprechenden Wert in das Feld **Wert** ein. Weitere Informationen zur Verwendung des Standardparametersatzes und zur Auswahl von Werten finden Sie im Abschnitt [Standardparameter und -werte für Bedarfsplanungsmodelle](#model-parameters) Sektion.

### <a name="set-up-the-connection-to-the-azure-machine-learning-service"></a>Einrichten der Verbindung mit dem Azure Machine Learning Service

Verwenden Sie die Registerkarte **Azure Machine Learning Service**, um die Verbindung mit dem Azure Machine Learning Service einzurichten. Diese Lösung ist eine der Optionen zum Erstellen der Grundplanung. Diese Einstellungen auf dieser Registerkarte wirken sich nur aus, wenn das Feld **Strategie zur Planungsgenerierung** auf *Azure Machine Learning Service* festgeleget ist.

Weitere Informationen zum Einrichten des Azure Machine Learning Service und zum Herstellen einer Verbindung mit den Einstellungen hier finden Sie im Abschnitt [Einrichten des Azure Machine Learning Service](#setup-amls).

### <a name="set-up-the-connection-to-azure-machine-learning-studio-classic"></a>Einrichten der Verbindung mit Azure Machine Learning Studio (klassisch)

> [!IMPORTANT]
> Azure Machine Learning Studio (klassisch) ist veraltet. Daher können Sie in Azure keine neuen Arbeitsbereiche mehr dafür erstellen. Es wurde durch den Azure Machine Learning Service ersetzt, der ähnliche Funktionen und mehr bietet. Wenn Sie Azure Machine Learning noch nicht verwenden, sollten Sie damit beginnen, den Azure Machine Learning Service zu verwenden. Wenn Sie bereits über einen Arbeitsbereich verfügen, der für Azure Machine Learning Studio (klassisch) erstellt wurde, können Sie ihn weiterhin verwenden, bis die Funktion vollständig aus Azure entfernt wird. Wir empfehlen jedoch, dass Sie so bald wie möglich auf den Azure Machine Learning Service aktualisieren. Obwohl die Anwendung Sie weiterhin warnt, dass Azure Machine Learning Studio (klassisch) veraltet ist, hat dies keine Auswirkungen auf das Planungsergebnis. Weitere Informationen zum neuen Azure Machine Learning Service und zum Einrichten finden Sie im Abschnitt [Einrichten des Azure Machine Learning Service](#setup-amls).
>
> Sie können frei zwischen der Verwendung der neuen und alten Machine Learning-Lösungen mit Supply Chain Management wechseln, solange Ihr alter Azure Machine Learning Studio (klassisch)-Arbeitsbereich verfügbar bleibt.

Wenn Sie bereits über einen verfügbaren Azure Machine Learning Studio (klassisch)-Arbeitsbereich verfügen, können Sie ihn zum Generieren von Planungen verwenden, indem Sie ihn mit Supply Chain Management verbinden. Sie können diese Verbindung herstellen, indem Sie die Registerkarte **Azure Machine Learning** auf der Seite **Parameter der Bedarfsplanung** verwenden. (Die Einstellungen auf dieser Registerkarte wirken sich nur aus, wenn das Feld **Strategie zur Planungsgenerierung** auf *Azure Machine Learning* festgelegt ist.) Geben Sie die folgenden Details für Ihren Azure Machine Learning Studio (klassisch)-Arbeitsbereich ein:

- API-Schlüssel des Webdiensts
- URL des Webdienst-Endpunkts
- Azure-Speicherkontoname
- Azure-Speicherkontoschlüssel

> [!NOTE]
> Azure-Speicherkontenname und -schlüssel sind nur erforderlich, wenn Sie ein benutzerdefiniertes Speicherkonto verwenden. Wenn Sie die lokale Version bereitstellen, müssen Sie ein benutzerdefiniertes Speicherkonto in Azure haben, sodass das Machine Learning auf die historischen Daten zugreifen kann.

## <a name="default-parameters-and-values-for-demand-forecasting-models"></a><a name="model-parameters"></a>Standardparameter und -werte für Bedarfsplanungsmodelle

Wenn Sie Machine Learning verwenden, um Ihre Prognoseplanungsmodelle zu generieren, steuern Sie die Optionen des Machine Learnning, indem Sie Werte für *Parameter des Planungsalgorithmus* festlegen. Diese Werte werden von Supply Chain Management an Azure Machine Learning gesendet. Verwenden Sie der Seite **Parameter des Planungsalgorithmus**, um zu steuern, welche Arten von Werten bereitgestellt werden sollen und welche Werte jeder haben soll.

Um die Standardparameter und -werte einzurichten, die für Bedarfsplanungsmodelle verwendet werden, gehen Sie zu **Masterplanung \> Einstellungen \> Bedarfsplanung \> Planungsalgorithmusparameter**. Ein Standardsatz von Parametern wird bereitgestellt. Jeder Parameter hat die folgenden Felder:

- **Name** – Der Name des Parameters, wie er von Azure verwendet wird. Normalerweise sollten Sie diesen Namen nicht ändern, es sei denn, Sie haben das Experiment in Azure Machine Learning angepasst.
- **Beschreibung** – Ein allgemeiner Name für den Parameter. Dieser Name wird verwendet, um den Parameter an anderen Stellen im System zu identifizieren (z. B. auf der Seite  **Parameter der Bedarfsplanung**).
- **Wert** – Der Standardwert für den Parameter. Der Wert, den Sie eingeben sollten, hängt von dem Parameter ab, den Sie bearbeiten. 
- **Erläuterung** – Eine kurze Beschreibung des Parameters und seiner Verwendung. Diese Beschreibung enthält in der Regel Hinweise zu gültigen Werten für das Feld **Wert**.

Die folgenden Parameter werden standardmäßig bereitgestellt. (Wenn Sie jemals auf diese Standardliste zurücksetzen müssen, wählen Sie im Aktivitätsbereich **Wiederherstellen** aus.)

- **Zuverlässigkeitsstufe (Prozentsatz)**  – Ein Zuverlässigkeitsintervall besteht aus einem Wertebereich, der eine gute Einschätzung der Bedarfsplanung ermöglicht. Eine Zuverlässigkeitsstufe von 95 % bedeutet beispielsweise, dass der zukünftige Bedarf mit einer Chance von 5 % aus dem Intervallbereich der Zuverlässigkeit fällt.
- **Saisonalität erzwingen** – Gibt an, ob das Modell gezwungen wird, eine bestimmte Art der Saisonalität zu verwenden. Dieser Parameter gilt nur für ARIMA und ETS. Optionen: *AUTO (Standard)*, *KEINE*, *ADDITIV*, *MULTIPLIKATIV*.
- **Planungsmodell** – Gibt an, welches Planungsmodell verwendet werden soll. Optionen: *ARIMA*, *ETS*, *STL*, *ETS+ARIMA*, *ETS+STL*, *ALLE*. Um das passendste Modell auszuwählen, verwenden Sie *ALLE*.
- **Maximaler vorhergesagter Wert** – Gibt den Maximalwert an, der für Vorhersagen verwendet werden kann. Format: +1E[n] oder numerische Konstante.
- **Minimaler vorhergesagter Wert** – Gibt den Minimalwert an, der für Vorhersagen verwendet werden kann. Format: -1E[n] oder numerische Konstante.
- **Fehlende Wertersetzung** – Gibt an, wie Lücken in historischen Daten ausgefüllt werden. Optionen: *(numerischer Wert)*, *MITTEL*, *VORHERIG*, *LINEARINTERPOLATION*, *POLYNOMINTERPOLATION*.
- **Umfang der fehlenden Wertersetzung** – Gibt an, ob die Wertersetzung nur auf den Datumsbereich jedes einzelnen Granularitätsattributs angewendet wird, oder auf den gesamten Dataset. Folgende Optionen stehen zur Verfügung, um den Datumsbereich festzulegen, den das System beim Auffüllen von Lücken in historischen Daten verwendet:

    - *GLOBAL* – Das System verwendet den gesamten Datumsbereich aller Granularitätsattribute.
    - *HISTORY_DATE_RANGE* – Das System verwendet einen bestimmten Datumsbereich, der durch die Felder **Startdatum** und **Enddatum** im Abschnitt **Historischer Horizont** im Dialogfeld **Statistische Grundplanung generieren** definiert ist.
    - *GRANULARITY_ATTRIBUTE* – Das System verwendet den Datumsbereich des aktuell verarbeiteten Granularitätsattributs.

    > [!NOTE]
    > Ein Granularitätsattribut ist eine Kombination von Planungsdimensionen, für die die Planung erstellt wird. Sie können Planungsdimensionen auf der Seite **Bedarfsplanungsparameter** definieren.

- **Hinweis zur Saisonalität** – Geben Sie für Saisondaten einen Hinweis an das Planungsmodell, um die Planungsgenauigkeit zu verbessern. Format: Ganzzahl, die die Anzahl der Buckets angibt, die sich ein Bedarfsmuster wiederholt. Geben Sie zum Beispiel *6* für Daten ein, die alle sechs Monate wiederholt werden.
- **Testsatzgröße in Prozent** – Prozentsatz der historischen Daten, die als Testsatz für die Berechnung der Planungsgenauigkeit verwendet werden.

Sie können die Werte für diese Parameter überschreiben, indem Sie zu **Masterplanung \> Einstellungen \> Bedarfsplanung \> Bedarfsplanungsparameter** gehen. Auf der Seite **Bedarfsplanungsparameter** können Sie die Parameter auf folgende Weise überschreiben:

- Verwenden Sie die Registerkarte **llgemein**, um die Parameter global zu überschreiben.
- Verwenden Sie die Registerkarte **Artikelzuteilungsschlüssel**, um die Parameter für bestimmte Artikelzuteilungsschlüssel zu überschreiben. Parameter, die für einen bestimmten Artikelverteilungsschlüssel überschreiben werden, wirken sich nur auf die Planung von Artikeln aus, die diesem Artikelverteilungsschlüssel zugeordnet sind.

> [!NOTE]
> Auf der Seite **Parameter des Planungsagortighmus** können Sie mit den Schaltflächen im Aktivitätsbereich Parameter zur Liste hinzufügen oder Parameter aus der Liste entfernen. Allerdings sollten Sie diesen Ansatz normalerweise nicht verwenden, es sei denn, Sie haben das Experiment in Azure Machine Learning angepasst.

## <a name="set-up-the-azure-machine-learning-service"></a><a name="setup-amls"></a>Einrichten des Azure Machine Learning Service

Supply Chain Management berechnet Bedarfsplanungen mithilfe des Azure Machine Learning Service, den Sie in Ihrem eigenen Azure-Abonnement einrichten und ausführen müssen. In diesem Abschnitt wird beschrieben, wie Sie den Azure Machine Learning Service in Azure einrichten und ihn dann mit Ihrer Supply Chain Management-Umgebung verbinden.

### <a name="enable-the-azure-machine-learning-service-in-feature-management"></a>Aktivieren Sie den Azure Machine Learning Service in der Funktionsverwaltung

Bevor Sie den Azure Machine Learning Service für die Bedarfsprognose verwenden können, müssen Sie eine Funktion in Supply Chain Management aktivieren, um die Integration zu aktivieren. Administratoren können mit den Einstellungen [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und sie aktivieren. Im Arbeitsbereich **Funktionsverwaltung** ist die Funktion wie folgt aufgeführt:

- **Modul:** *Produktprogrammplanung*
- **Funktionsname:** *Azure Machine Learning Service für Bedarfsplanung*

### <a name="set-up-machine-learning-in-azure"></a><a name="ml-workspace"></a>Einrichten von Machine Learning in Azure

Damit Azure Machine Learning zum Verarbeiten Ihrer Planungen verwenden kann, müssen Sie zu diesem Zweck einen Azure Machine Learning-Arbeitsbereich einrichten. Sie haben zwei Möglichkeiten:

- Um den Arbeitsbereich einzurichten, indem Sie ein von Microsoft bereitgestelltes Skript ausführen, befolgen Sie die Anweisungen im Abschnitt [Option 1: Ein Skript ausführen, um automatisch Ihren Arbeitsbereich für Machine Learning einzurichten](#ml-workspace-script), und springen Sie dann zum Abschnitt [Einrichten von Verbindungsparametern für Azure Machine Learning Service in Supply Chain Management](#demand-forecast-parameters).
- Um Ihren Arbeitsbereich manuell einzurichten, indem Sie ein von Microsoft bereitgestelltes Skript ausführen, befolgen Sie die Anweisungen im Abschnitt [Option 2: Manuell ein Skript ausführen, um automatisch Ihren Arbeitsbereich für Machine Learning einzurichten](#ml-workspace-manual), und springen Sie dann zum Abschnitt [Einrichten von Verbindungsparametern für Azure Machine Learning Service in Supply Chain Management](#demand-forecast-parameters). Diese Option nimmt mehr Zeit in Anspruch, gibt Ihnen aber mehr Kontrolle.

#### <a name="option-1-run-a-script-to-automatically-set-up-your-machine-learning-workspace"></a><a name="ml-workspace-script"></a>Option 1: Führen Sie ein Skript aus, um Ihren Machine Learning-Arbeitsbereich automatisch einzurichten

In diesem Abschnitt wird beschrieben, wie Sie Ihren Machine Learning-Arbeitsbereich mithilfe eines von Microsoft bereitgestellten automatisierten Skripts einrichten. Wenn Sie möchten, können Sie alle Ressourcen manuell einrichten, indem Sie die Anweisungen im Abschnitt [Option 2:Ihren Machine Learning-Arbeitsbereich manuell einrichten](#ml-workspace-manual) befolgen. Sie müssen nicht beide Optionen ausführen.

1. Öffnen Sie auf GitHub das [Vorlagen für Dynamics 365 Supply Chain Management-Bedarfsplanungen mit Azure Machine Learning](https://github.com/microsoft/Dynamics-365-Supply-Chain-Management-Demand-Forecasting-With-Azure-Machine-Learning-Service)-Repository (Repo), und laden Sie die folgenden Dateien herunter:

    - quick_setup.ps1
    - sampleInput.csv
    - src/parameters.py
    - src/api_trigger.py
    - src/run.py
    - src/REntryScript/forecast.r

1. Öffnen Sie ein PowerShell-Fenster, und führen Sie das **quick_setup.ps1**-Skript aus, das Sie im vorherigen Schritt heruntergeladen haben. Befolgen Sie die Anweisungen auf dem Bildschirm. Das Skript richtet den erforderlichen Arbeitsbereich, den Speicher, den Standarddatenspeicher und die Rechenressourcen ein. Sie müssen jedoch trotzdem die erforderlichen Pipelines erstellen, indem Sie die verbleibenden Schritte dieses Verfahrens ausführen. (Pipelines bieten eine Möglichkeit, Planungsskripts aus dem Supply Chain Management zu starten.)
1. Laden Sie in Azure Machine Learning Studio die **sampleInput.csv**-Datei, die Sie in Schritt 1 heruntergeladen haben, in den Container namens *demplan-azureml*. (Dieser Container wurde vom Skript quick_setup.ps1 erstellt.) Diese Datei ist erforderlich, um die Pipeline zu veröffentlichen und eine Testplanung zu generieren. Anweisungen finden Sie unter [Einen Blockblob hochladen](/azure/storage/blobs/storage-quickstart-blobs-portal#upload-a-block-blob).
1. Wählen Sie in Azure Machine Learning Studio im Navigator **Notizbücher** aus.
1. Finden Sie den folgenden Speicherort in der Struktur **Dateien**: **Benutzer/\[aktueller Benutzer\]/src**.
1. Laden Sie die verbleibenden vier Dateien, die Sie in Schritt 1 heruntergeladen haben, auf den Speicherort hoch, den Sie im vorherigen Schritt gefunden haben.
1. Wählen Sie die **api_trigger.py**-Datei aus, die Sie gerade hochgeladen haben, und führen Sie sie aus. Es wird eine Pipeline erstellt, die über die API ausgelöst werden kann.
1. Ihr Arbeitsbereich ist jetzt eingerichtet. Machen Sie bei Abschnitt [Einrichten der Verbindungsparameter von Azure Machine Learning Service in Supply Chain Management](#demand-forecast-parameters) weiter.

#### <a name="option-2-manually-set-up-your-machine-learning-workspace"></a><a name="ml-workspace-manual"></a>Option 2: Ihren Machine Learning-Arbeitsbereich manuell einrichten

In diesem Abschnitt wird beschrieben, wie Sie Ihren Machine Learning-Arbeitsbereich manuell einrichten. Sie müssen die Verfahren in diesem Abschnitt nur ausführen, wenn Sie sich entschieden haben, das im Abschnitt [ Option 1: Ein Skript ausführen, um Ihren Machine Learning-Arbeitsbereich einzurichten](#ml-workspace-script) beschriebene Skript für die automatisierte Einrichtung nicht auszuführen.

##### <a name="step-1-create-a-new-workspace"></a><a name="create-workspace"></a>Schritt 1: Erstellen eines neuen Arbeitsbereichs

Gehen Sie zum Erstellen eines neuen Machine Learning-Arbeitsbereichs folgendermaßen vor.

1. Melden Sie sich bei Ihrem Azure-Portal an.
1. Öffnen Sie den **Machine Learning**-Service.
1. Wählen Sie in der Symbolleiste **Erstellen** aus, um den **Erstellungsassistenten** zu öffnen.
1. Schließen Sie den Assistenten ab, indem Sie die Bildschirmanweisungen befolgen. Beachten Sie bei Ihrer Arbeit folgende Punkte:

    - Verwenden Sie die Standardeinstellungen, es sei denn, andere Punkte in dieser Liste empfehlen andere Einstellungen.
    - Achten Sie darauf, die geografische Region auszuwählen, die der Region entspricht, in der Ihre Instanz von Supply Chain Management bereitgestellt wird. Andernfalls könnten einige Ihrer Daten die Regionsgrenzen überschreiten. Weitere Informationen finden Sie im Abschnitt [Datenschutzhinweis](#privacy) weiter unten in diesem Thema.
    - Verwenden Sie dedizierte Ressourcen wie Ressourcengruppen, Speicherkonten, Containerregistrierungen, Azure-Schlüsseltresore und Netzwerkressourcen.
    - Auf der Seite **Einrichten der Verbindungsparametern von Azure Machine Learning Service** des Assistenten müssen Sie einen Speicherkontonamen angeben. Verwenden Sie ein Konto, das für die Bedarfsplanung bestimmt ist. In diesem Speicherkonto werden die Eingabe- und Ausgabedaten der Bedarfsplanung gespeichert.

Weitere Informationen finden Sie unter [Erstellen eines Arbeitsbereichs](/azure/machine-learning/quickstart-create-resources#create-the-workspace).

##### <a name="step-2-configure-storage"></a><a name="config-storage"></a>Schritt 2: Speicher konfigurieren

Verwenden Sie die folgende Prozedur, um Ihren Speicher einzurichten.

1. Öffnen Sie auf GitHub das [Vorlagen für Dynamics 365 Supply Chain Management-Bedarfsplanungen mit Azure Machine Learning](https://github.com/microsoft/Dynamics-365-Supply-Chain-Management-Demand-Forecasting-With-Azure-Machine-Learning-Service)-Repo, und laden Sie die Datei **sampleInput.csv** herunter.
1. Öffnen Sie das Speicherkonto, das Sie im Abschnitt [Schritt 1: Erstellen eines neuen Arbeitsbereichs](#create-workspace) erstellt haben.
1. Folgen Sie den Anweisungen in [Erstellen eines Containers](/azure/storage/blobs/storage-quickstart-blobs-portal#create-a-container), um einen Container mit dem Namen *demplan-azureml* zu erstellen.
1. Laden Sie die Datei **sampleInput.csv**, die Sie in Schritt 1 heruntergeladen haben, in den Container hoch, den Sie gerade erstellt haben. Diese Datei ist erforderlich, um die Pipeline zu veröffentlichen und eine Testplanung zu generieren. Anweisungen finden Sie unter [Einen Blockblob hochladen](/azure/storage/blobs/storage-quickstart-blobs-portal#upload-a-block-blob).

##### <a name="step-3-configure-a-default-datastore"></a>Schritt 3: Konfigurieren eines Standarddatenspeichers

Verwenden Sie die folgende Prozedur, um Ihren Standarddatenspeicher einzurichten.

1. Wählen Sie in Azure Machine Learning Studio im Navigator **Datenspeicher** aus.
1. Erstellen Sie einen neuen Datenspeicher des Typs *Azure Blob Storage*, der auf den Blob Storage-Container *demplan-azureml* weist, den Sie im Abschnitt [Schritt 2: Speicher konfigurieren](#config-storage) erstellt haben. (Wenn der Authentifizierungstyp des neuen Datenspeichers ein *Kontoschlüssel* ist, geben Sie einen Kontoschlüssel für das erstellte Speicherkonto an. Anweisungen finden Sie unter [Zugriffsschlüssel für Speicherkonten verwalten](/azure/storage/common/storage-account-keys-manage?tabs=azure-portal) .)
1. Machen Sie Ihren neuen Datenspeicher zum Standarddatenspeicher, indem Sie die Details öffnen und **Als Standard-Datenspeicher festlegen** auswählen.

##### <a name="step-4-configure-compute-resources"></a><a name="config-compute-resources"></a>Schritt 4: Rechenressourcen konfigurieren

Verwenden Sie das folgende Verfahren, um eine Rechenressource in Azure Machine Learning Studio einzurichten, um Ihre Skripts zur Erstellung von Planungen auszuführen.

1. Öffnen Sie die Detailseite für den Machine Learning-Arbeitsbereich, den Sie im Abschnitt [Schritt 1: Erstellen eines neuen Arbeitsbereichs](#create-workspace) erstellt haben. Finden Sie den Wert **Studio-Web-URL**, und wählen Sie den Link aus, um ihn zu öffnen.
1. Wählen Sie im Navigationsbereich **Berechnen** aus.
1. wählen Sie auf der Registerkarte **Compute-Instanzen** die Opion  **Neu** aus, um einen Assistenten zu öffnen, der Sie beim Erstellen einer neuen Compute-Instanz unterstützt. Befolgen Sie die Anweisungen auf dem Bildschirm. Die Compute-Instanz wird verwendet, um die Pipeline für die Bedarfsplanung zu erstellen. (Sie kann nach der Veröffentlichung der Pipeline gelöscht werden.) Verwenden Sie die Standardeinstellungen.
1. wählen Sie auf der Registerkarte **Compute-Cluster** die Opion  **Neu** aus, um einen Assistenten zu öffnen, der Sie beim Erstellen eines neuen Compute-Clusters unterstützt. Befolgen Sie die Anweisungen auf dem Bildschirm. Der Compute-Cluster wird verwendet, um Bedarfsplanungen zu generieren. Seine Einstellungen wirken sich auf die Leistung und den maximalen Grad der Parallelisierung bei der Ausführung aus. Legen Sie die folgenden Felder fest, verwenden Sie jedoch die Standardeinstellungen für alle anderen Felder:

    - **Name** – geben Sie *e2ecpucluster* ein.
    - **Größe des virtuellen Computers** – passen Sie diese Einstellung an das Datenvolumen an, das Sie voraussichtlich als Eingabe für die Bedarfsplanung verwenden werden. Die Anzahl der Knoten sollte 11 nicht überschreiten, da ein Knoten erforderlich ist, um die Erzeugung der Bedarfsplanung auszulösen, und die maximale Anzahl von Knoten, die dann zum Erstellen einer Planung verwendet werden können, 10 beträgt. (Sie werden auch die Knotenanzahl in der Datei parameters.py im Abschnitt [Schritt 5: Pipelines erstellen](#create-pipelines) festlegen.) Auf jedem Knoten gibt es mehrere Worker-Prozesse, die Planungsskripts parallel ausführen. Die Gesamtzahl der Worker-Prozesse in Ihrem Einzelvorgang beträgt *Anzahl der Kerne, die ein Knoten hat* × *Knotenanzahl*. Wenn Ihr Compute-Cluster beispielsweise vom Typ *Standard\_ D4* (acht Kerne) ist und maximal 11 Knoten hat, und wenn der `nodes_count`-Wert in der Datei Parameters.py auf *10* festgelegt ist, beträgt der effektive Parallelitätsgrad 80.

##### <a name="step-5-create-pipelines"></a><a name="create-pipelines"></a>Schritt 5: Erstellen von Pipelines

Pipelines bieten eine Möglichkeit, Planungsskripts aus dem Supply Chain Management zu starten. Gehen Sie wie folgt vor, um die erforderlichen Pipelines zu erstellen.

1. Öffnen Sie auf GitHub das [Vorlagen für Dynamics 365 Supply Chain Management-Bedarfsplanungen mit Azure Machine Learning](https://github.com/microsoft/Dynamics-365-Supply-Chain-Management-Demand-Forecasting-With-Azure-Machine-Learning-Service)-Repo, und laden Sie die folgenden Dateien herunter:

    - src/parameters.py
    - src/api_trigger.py
    - src/run.py
    - src/REntryScript/forecast.r

1. Wählen Sie in Azure Machine Learning Studio im Navigator **Notizbücher** aus.
1. Finden Sie den folgenden Speicherort in der Struktur **Dateien**: **Benutzer/\[aktueller Benutzer\]/src**.
1. Laden Sie die vier Dateien, die Sie in Schritt 1 heruntergeladen haben, auf den Speicherort hoch, den Sie im vorherigen Schritt gefunden haben.
1. Öffnen und überprüfen Sie in Azure die Datei **parameters.py**, die Sie gerade hochgeladen haben. Stellen Sie sicher, dass der Wert `nodes_count` eins weniger ist, als der Wert, den Sie im Abschnitt [ Schritt 4: Rechenressourcen konfigurieren](#config-compute-resources) für den Compute-Cluster konfiguriert haben. Wenn der Wert `nodes_count` größer oder gleich der Anzahl der Knoten im Compute-Cluster ist, kann die Pipelineausführung möglicherweise gestartet werden. Sie wird dann jedoch nicht mehr reagieren, während sie auf die erforderlichen Ressourcen wartet. Weitere Informationen zur Knotenanzahl finden Sie im Abschnitt [Schritt 4: Rechenressourcen konfigurieren](#config-compute-resources).
1. Wählen Sie die **api_trigger.py**-Datei aus, die Sie gerade hochgeladen haben, und führen Sie sie aus. Es wird eine Pipeline erstellt, die über die API ausgelöst werden kann.

### <a name="set-up-a-new-active-directory-application"></a><a name="aad-app"></a>Einrichten einer neuen Active Directory-Anwendung

Eine Active Directory-Anwendung ist erforderlich, um sich mithilfe des Dienstprinzipals bei den Ressourcen zu authentifizieren, die für die Bedarfsplanung reserviert sind. Daher sollte die Anwendung die niedrigste Berechtigungsebene haben, die zum Generieren der Planung erforderlich ist.

1. Melden Sie sich bei Ihrem Azure-Portal an.
1. Registrieren Sie eine neue Anwendung im Azure Active Directory (Azure AD) des Mandanten. Anweisungen finden Sie uner [Das Portal verwenden, um eine Azure AD-Anwendung- und einen -Dienstprinzipal zu erstellen, die auf Ressourcen zugreifen können](/azure/active-directory/develop/howto-create-service-principal-portal).
1. Befolgen Sie die Bildschirmanweisungen, wenn Sie den Assistenten abschließen. Verwenden Sie die Standardeinstellungen.
1. Gewähren Sie Ihrer neuen Active Directory-Anwendung Zugriff auf die folgenden Ressourcen, die Sie im Abschnitt [Einrichten von Machine Learning in Azure](#ml-workspace) erstellt haben. Anweisungen finden Sie unter [Zuweisen von Azure-Rollen über das Azure-Portal](/azure/role-based-access-control/role-assignments-portal?tabs=current). Dieser Schritt ermöglicht es dem System, Planungsdaten zu importieren und zu exportieren und Pipeline-Ausführungen für Machine Learning aus dem Supply Chain Management auszulösen.

    - Mitwirkender-Rolle im Machine Learning-Arbeitsbereich
    - Mitwirkender-Rolle für das dedizierte Speicherkonto
    - Storage Blob Data-Mitwirkender-Rolle für das dedizierte Speicherkonto

1. Im **Zertifikate & Geheimnisse**-Abschnitt der Anwendung, die Sie erstellt haben, erstellen Sie ein Geheimnis für die Anwendung. Anweisungen finden Sie unter [Hinzufügen eines Client-Geheimnisses](/azure/active-directory/develop/quickstart-register-app#add-a-client-secret).
1. Notieren Sie sich die Anwendungs-ID und ihr Geheimnis. Die Angaben zu dieser Anwendung benötigen Sie später bei der Einrichtung der Seite **Bedarfsplanungsparameters** im Supply Chain Management.

### <a name="set-up-azure-machine-learning-service-connection-parameters-in-supply-chain-management"></a><a name="demand-forecast-parameters"></a>Machen Sie bei Abschnitt Einrichten der Verbindungsparameter von Azure Machine Learning Service in Supply Chain Management weiter

Verwenden Sie die folgende Prozedur, um Ihre Supply Chain Management-Umgebung mit dem Machine Learning-Service zu verbinden, den Sie soeben in Azure erstellt haben.

1. Melden Sie sich im Supply Chain Management an.
1. Wechseln Sie zu **Masterplan \> Einrichten \> Bedarfsplanung \> Bedarfsplanungsparameter**.
1. Stellen Sie auf der Registerkarte **Allgemein** sicher, dass das Feld **Strategie zur Prognosegenerierung** auf *Azure Machine Learning Service* festgelegt ist.
1. Stellen Sie auf der Registerkarte **Artikelzuordnungsschlüssel** sicher, dass das Feld **Strategie zur Prognosegenerierung** für jeden Zuordnungsschlüssel, der den Azure Machine Learning Service für die Bedarfsprognose verwenden soll auf *Azure Machine Learning Service* festgelegt ist.
1. Legen Sie auf der Registerkarte **Azure Machine Learning Service** die folgenden Felder fest:

    - **Mandanten-ID** - geben Sie die ID für Ihren Azure-Mandanten ein. Supply Chain Management verwendet diese ID, um sich beim Azure Machine Learning Service zu authentifizieren. Ihre Mandanten-ID finden Sie auf der Seite **Überblick** für Azure AD im Azure-Portal.
    - **Dienstprinzipalanwendungs-ID** – geben Sie die Anwendungs-ID für die Anwendung ein, die Sie im Abschnitt [Active Directory-Anwendung](#aad-app) erstellt haben. Dieser Wert wird verwendet, um API-Anforderungen an Azure Machine Learning Service zu autorisieren.
    - **Dienstprinzipal-Anwendungsgeheimnis** – geben Sie das Dienstprinzipal-Anwendungsgeheimnis für die Anwendung ein, die Sie im Abschnitt [Active Directory-Anwendung](#aad-app) erstellt haben. Dieser Wert wird verwendet, um das Zugriffstoken für den Sicherheitsprinzipal abzurufen, den Sie erstellt haben, um autorisierte Vorgänge für Azure Storage und den Azure Machine Language-Arbeitsbereich auszuführen.
    - **Name des Speicherkontos** – geben Sie den Namen des Azure-Speicherkontos ein, den Sie beim Ausführen des Einrichtungsassistenten in Ihrem Azure-Arbeitsbereich angegeben haben. (Weitere Informationen finden Sie im Abschnitt [Einrichten von Machine Learning in Azure](#ml-workspace).)
    - **Pipeline-Endpunktadresse** – geben Sie die URL des Pipeline-REST-Endpunkts für Ihren Azure Machine Learning Service ein. Sie haben diese Pipeline als letzten Schritt erstellt, als Sie das [Einrichten von Machine Learning in Azure](#ml-workspace) durchgeführt haben. Um die Pipeline-URL abzurufen, melden Sie sich bei Ihrem Azure-Portal an und wählen Sie auf der Navigation **Pipelines** aus. Wählen Sie auf der Registerkarte **Pipeline** den Pipeline-Endpunkt namens **TriggerDemandForecastGeneration** aus. Kopieren Sie dann den angezeigten REST-Endpunkt.

    ![Parameter auf der Registerkarte Azure Machine Learning Service der Seite Bedarfsplanungsparameter.](media/azure-ml-service-parameters.png "parameter auf der Registerkarte Azure Machine Learning Service der Seite Bedarfsplanungsparameter")

## <a name="privacy-notice"></a><a name="privacy"></a>Datenschutzhinweis

Wenn Sie *Azure Machine Learning Service* als Ihre Strategie zur Planungserstellung auswählen, sendet Supply Chain Management automatisch Ihre Kundendaten für den historischen Bedarf, wie aggregierte Mengen, Produktnamen und deren Produktabmessungen, Versand- und Empfangsorte, Kundenbezeichner und auch Planungsparameter zum Zweck der Planung des zukünftigen Bedarfs an die geografische Region, in der sich Ihr Machine Learning-Arbeitsbereich und sein verknüpftes Speicherkonto befinden. Der Azure Machine Learning Service befindet sich möglicherweise in einer anderen geografischen Region als der geografischen Region, in der Supply Chain Management bereitgestellt wird. Einige Benutzer können steuern, ob diese Funktion aktiviert ist, indem sie die Strategie der Planungserstellung auf der Seite **Parameter der Bedarfsplanung** auswählen.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Bedarfsplanung – Übersicht](introduction-demand-forecasting.md)
- [Eine statistische Grundplanung generieren](generate-statistical-baseline-forecast.md)
- [Manuelle Anpassungen an der Grundplanung](manual-adjustments-baseline-forecast.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
