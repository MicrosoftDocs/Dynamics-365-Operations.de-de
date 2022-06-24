---
title: Einrichten eines Experiments
description: In diesem Artikel wird beschrieben, wie Sie ein Experiment in einem Drittanbieterdienst einrichten.
author: sushma-rao
ms.date: 06/08/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.openlocfilehash: 1073cdc509622279ce7388b8b406079a4e6e9e09
ms.sourcegitcommit: 427fe14824a9d937661ae21b9e9574be2bc9360b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2022
ms.locfileid: "8946165"
---
# <a name="set-up-an-experiment"></a>Einrichten eines Experiments

Nach dem [Definieren einer Hypothese und Bestimmen, welche Erfolgsmetriken Sie verwenden möchten](experimentation-identify.md) müssen Sie Ihr Experiment im Drittanbieterdienst einrichten. Das folgende Diagramm zeigt alle Schritte, die am Einrichten und Ausführen eines Experiments auf einer E-Commerce-Website in Dynamics 365 Commerce beteiligt sind. Weitere Schritte werden in separaten Artikeln behandelt.

[ ![User Journey zum Experimentieren – Einrichtung.](./media/experimentation_setup.svg) ](./media/experimentation_setup.svg#lightbox)


## <a name="set-up-your-experiment-in-the-third-party-service"></a>Experiment im Drittanbieterdienst einrichten
Inzwischen sollten Sie Ihren Drittanbieterdienst ausgewählt haben, um Ihr Experiment auszuführen und zu überwachen, und den Experimentier-Connector eingerichtet haben. Diese Voraussetzungen sind aufgeführt unter [Experimentieren in Dynamics 365 Commerce](experimentation-overview.md).

Befolgen Sie die Schritte, die zum Erstellen Ihres Experiments im Dienst eines Drittanbieters erforderlich sind. Wenn der Connector ordnungsgemäß konfiguriert ist, wird die vollständige Liste der Experimente, die Sie im Drittanbieterdienst eingerichtet haben, innerhalb von ca. 5 Minuten im Commerce Site Builder angezeigt.

## <a name="set-up-your-success-metrics"></a>Erfolgsmetriken einrichten
Jedes Experiment benötigt Metriken, um die Auswirkungen der Variationen zu messen und die Hypothese zu validieren. Führen Sie die folgenden Schritte aus, um die Berechnung von Metriken im Drittanbieterdienst mithilfe von Live-Telemetrieereignissen von Dynamics 365 Commerce zu aktivieren.

Befolgen Sie diese Schritte, um Ihre Erfolgsmetriken für vorkonfigurierte Module einzurichten.

1. Wählen Sie im Commerce Site Builder im linken Navigationsbereich die Registerkarte **Seiten** aus, und wählen Sie dann die Seite aus, auf der Sie Metriken erfassen möchten. 
1. Gehen Sie im rechten Eigenschaftenbereich der Seite oder des Moduls, die oder das Sie verfolgen möchten, zum Abschnitt **Zu verfolgende Ereignis-IDs**.
1. Wählen Sie **Ansicht** aus. Eine Liste aller Ereignis-IDs wird angezeigt. Kopieren Sie das Ereignis, das Sie verfolgen möchten, und fügen Sie den Ereignisschlüssel an der angegebenen Stelle im Dienst eines Drittanbieters ein. Wenn Sie mehr als ein Ereignis benötigen, kopieren Sie die Schlüssel einzeln. 
1. Verwenden Sie für Seitenaufrufe den SHA-256-Hashwert des Seitennamens im angehängten Site Builder `.PageView`. Beispielsweise wäre die Ereignis-ID für `Homepage.PageView` die `e217eb66c7808ecc43b0f5c517c6a83b39d72b91412fbd54a485da9d8e186a9`.
1. Führen Sie weitere Schritte zum Verfolgen von Metriken aus, die im Drittanbieterdienst erforderlich sind.

Führen Sie für Klicks auf benutzerdefinierte Module die folgenden Schritte aus, um die Klickereignisse zu instrumentieren:

1. Bereiten Sie ein Objekt **TelemetryContent** für das Modul mit der unten stehenden Funktion vor. Diese Funktion verwendet den Seitennamen, den Modulnamen und das vom SDK bereitgestellte Standard-Telemetrieobjekt als Eingaben.

    ```TypeScript
    getTelemetryObject(pageName: string, moduleName: string, telemetry: ITelemetry): ITelemetryContent
    ```
    
    Hier sehen Sie ein Beispiel einer Anforderung: 
    
    ```TypeScript
    private readonly telemetryContent: ITelemetryContent = getTelemetryObject(this.props.context.request.telemetryPageName!, this.props.friendlyName, this.props.telemetry);
    ```
    
1. Erstellen Sie die Nutzlastdaten, die Informationen darüber enthalten, was erfasst werden muss. Für Schaltflächen und andere statische Steuerelemente können Sie **Text** wie „Jetzt einkaufen“ oder „Suchen“ einbeziehen. Und für Komponenten mit Klicks, wie z. B. das Klicken auf eine Produktkarte, können Sie die **recid** senden, die Datensatz-ID des Produkts oder die Produkt-ID.

    ```TypeScript
    getPayloadObject(eventType: string, telemetryContent: ITelemetryContent, etext: string, recid?: string): IPayLoad
    ```
    Übergeben Sie als Beispiel für statische Steuerelemente die Schaltflächen-Textzeichenfolge wie unten gezeigt:

    ```TypeScript
    const payLoad = getPayloadObject('click', this.props.telemetryContent, 'Shop Now', '');
    ```
    Übergeben Sie als Beispiel für Produktklicks die Produktdatensatz-ID wie unten gezeigt:

    ```TypeScript
    const payLoad = getPayloadObject('click', telemetryContent!, '', product.RecordId.toString());
    ```
    
1. Rufen Sie die Funktion **OnClick** zum Registrieren des Ereignisses auf.

    ```TypeScript
    onTelemetryClick = (telemetryContent: ITelemetryContent, payLoad: IPayLoad, linkText: string) => () =>
    ```

    Hier sehen Sie ein Beispiel einer Anforderung:

    ```TypeScript
    onClick: onTelemetryClick(this.props.telemetryContent, payLoad, linkText)
    ```

## <a name="previous-step"></a>Vorheriger Schritt
[Eine Hypothese identifizieren und Metriken für ein Experiment bestimmen](experimentation-identify.md) 


## <a name="next-step"></a>Nächster Schritt
[Ein Experiment verbinden und bearbeiten](experimentation-connect-edit.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
