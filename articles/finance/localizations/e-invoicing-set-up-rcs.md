---
title: Regulatory Configuration Service (RCS) festlegen
description: In diesem Artikel wird erklärt, wie Sie den Regulatory Configuration Service (RCS) festlegen.
author: gionoder
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.custom: 97423,  ""intro-internal
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 63a4f77d6e80133947dff678cef3885167ec55be
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285786"
---
# <a name="set-up-regulatory-configuration-service-rcs"></a>Regulatory Configuration Service (RCS) festlegen

[!include [banner](../includes/banner.md)]

In diesem Artikel wird erklärt, wie Sie den Regulatory Configuration Service (RCS) festlegen.

## <a name="turn-on-globalization-features"></a>Schalten Sie die Funktionen zur Globalisierung ein

1. Melden Sie sich bei Ihrem RCS-Konto an.
2. Wählen Sie die Kachel **Funktionsverwaltung**.
3. In dem **Funktionsverwaltung** Arbeitsbereich wählen Sie **Globalisierungsfunktionen** in der Liste und wählen Sie dann **Jetzt aktivieren**.

Eine Kachel für den Arbeitsbereich **Globalisierungsfunktionen** sollte jetzt auf dem Haupt-Dashboard von RCS erscheinen.

## <a name="set-up-the-parameters-for-rcs-integration-with-electronic-invoicing"></a>Parameter für die RCS-Integration in die elektronische Rechnungsstellung einrichten

1. Wählen Sie im Arbeitsbereich **Globalisierungsfunktionen** im Abschnitt **Zugehörige Einstellungen** die Option **Elektronische Berichterstellungsparameter** aus.
2. Geben Sie auf der Registerkarte **Elektronische Rechnungsstellung** in das Feld **Service-Endpunkt URI** den entsprechenden Service-Endpunkt für Ihre Microsoft Azure-Geographie ein, wie in der folgenden Tabelle dargestellt.

    | Azure-Rechenzentrumgeografie | Dienst-Endpunkt-URI |
    |----------------------------|----------------------|
    | USA              | <p>`https://gw.us-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Europa                     | <p>`https://gw.eu-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il110.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Vereinigtes Königreich             | <p>`https://gw.uk-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.uk-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Asien                       | <p>`https://gw.as-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.as-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Japan                      | <p>`https://gw.jp-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Schweiz                | <p>`https://gw.ch-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Brasilien                     | <p>`https://gw.br-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> <p>`https://gw.br-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Vereinigte Arabische Emirate       | <p>`https://gw.ae-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Australien                  | <p>`https://gw.au-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> <p>`https://gw.au-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Kanada                     | <p>`https://gw.ca-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> <p>`https://gw.ca-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Frankreich                     | <p>`https://gw.fr-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Indien                      | <p>`https://gw.in-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |

3. Vergewissern Sie sich, dass das Feld **Anwendungs-ID** auf **0cdb527f-a8d1-4bf8-9436-b352c68682b2** festgelegt ist. Dieser Wert ist ein fester Wert. Stellen Sie sicher, dass nur ein global eindeutiger Bezeichner (GUID) eingegeben wird und dass der Wert keine anderen Symbole wie Leerzeichen, Kommas, Punkte oder Anführungszeichen enthält.
4. Geben Sie in das Feld **LCS-Umgebungs-ID** die ID Ihrer Microsoft Dynamics Lifecycle Services (LCS) Umgebung ein. Dieser Wert ist der Verweis auf die Finance- oder Supply Chain Management-Umgebung, die Sie mit dem Dienst für die elektronische Rechnungsstellung verwenden werden. Um Ihre ID zu erhalten, melden Sie sich bei [LCS](https://lcs.dynamics.com/) an, öffnen Ihr Projekt und suchen dann auf der Registerkarte **Umgebung verwalten** im Abschnitt **Umgebungsdetails** das Feld **Umgebungskennung**.

    > [!IMPORTANT]
    > Wenn das Add-In für die Elektronische Rechnungsstellung in mehreren Finance- oder Supply Chain Management-Umgebungen in LCS installiert ist, verwenden Sie immer die Umgebungs-ID der zuletzt installierten Umgebung. Wenn Sie sich entschließen, das Add-In in einer neuen Umgebung zu installieren, nachdem Sie die Funktion Elektronische Rechnungsstellung festgelegt haben und damit arbeiten, aktualisieren Sie das Feld **LCS Umgebungs-ID** in RCS auf den neuesten Wert.

5. Klicken Sie auf **Speichern** und schließen Sie die Seite.

## <a name="configuration-providers"></a>Konfigurationsanbieter

Sie können Konfigurationsanbieter verwenden, um die Besitzer der Konfigurationen für die Elektronische Rechnungsstellung (ER), die in elektronischen Rechnungsstellungsprozessen verwendet werden, und die Besitzer der Globalisierungsfunktionen zu unterscheiden. Für alle Funktionen der Globalisierung, die von Microsoft bereitgestellt und im Global Repository veröffentlicht werden, wird der Konfigurationsanbieter auf **Microsoft** (`http://microsoft.com`) festgelegt.

Sie können nur ER-Konfigurationen und Globalisierungsfunktionen anpassen, die zu dem aktiven Konfigurationsanbieter gehören. Sie können diese Konfigurationen und Funktionen als Vorlagen verwenden, um Konfigurationen und Funktionen zu erstellen, die zum aktiven Konfigurationsanbieter gehören, damit Sie sie anpassen können.

Erstellen Sie zunächst die Konfigurationsanbieter. Legen Sie dann eine von ihnen als aktiv fest. Sie können den **Microsoft** Konfigurationsanbieter nicht als aktiv festlegen.

### <a name="create-a-configuration-provider"></a>Erzeugen Sie einen Konfigurationsanbieter

1. Wählen Sie im Arbeitsbereich **Elektronische Berichterstellung** im Abschnitt **Zugehörige Links** die Option **Konfigurationsanbieter** aus.
2. Wählen Sie **Neu** aus.
3. Geben Sie in das Feld **Name** einen eindeutigen Namen für den Konfigurationsanbieter ein.
4. Geben Sie in das Feld **Internetadresse** die eindeutige URL des Konfigurationsanbieters ein.
5. Klicken Sie auf **Speichern** und schließen Sie die Seite.

### <a name="select-a-configuration-provider-as-active"></a>Wählen Sie einen Konfigurationsanbieter als aktiv

1. Wählen Sie in der Liste der Konfigurationsanbieter den Konfigurationsanbieter, den Sie als aktiv festlegen möchten.
2. Wählen Sie **Als aktiv festlegen**.

## <a name="import-er-configurations-from-the-global-repository"></a>ER-Konfigurationen aus dem Global Repository importieren

1. Wählen Sie im Arbeitsbereich **Elektronische Berichterstellung** im Abschnitt **Zugehörige Links** die Option **Konfigurationsanbieter** aus.
2. Wählen Sie in der Liste der Konfigurationsanbieter **Microsoft** und dann **Repositories**.
3. Wählen Sie **Global**, und wählen Sie dann im Aktionsbereich **Öffnen**.
4. Importieren Sie die folgenden ER-Modelle:

    - **Kontextmodell Debitorenrechnung**
    - **Rechnungsmodell**
    - **Fiskaldokumente** (für brasilianische Szenarien, falls erforderlich)
    - **Antwortnachrichtenmodell**

5. Wenn die **Rechnungsmodell-Zuordnung** nicht automatisch importiert wurde, importieren Sie sie.
6. Schließen Sie die Seite.
