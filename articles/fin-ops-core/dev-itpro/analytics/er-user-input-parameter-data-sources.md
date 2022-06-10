---
title: Verwenden von USER INPUT PARAMETER-Datenquellen, um Parameter für einen Bericht anzugeben
description: In diesem Thema wird erläutert, wie Sie USER INPUT PARAMETER-Datenquellen verwenden, um Parameter für von Ihnen generierte Berichte anzugeben.
author: NickSelin
ms.date: 04/20/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: Version 10.0.27
ms.openlocfilehash: 4e431c9dd59080af17fa073547073037ba233288
ms.sourcegitcommit: 6c1bf233748c4bc70fc5a1a9711758cdfd9e07dc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/19/2022
ms.locfileid: "8782314"
---
# <a name="use-user-input-parameter-data-sources-to-specify-parameters-for-a-report"></a>Verwenden von USER INPUT PARAMETER-Datenquellen, um Parameter für einen Bericht anzugeben

[!include[banner](../includes/banner.md)]

Wenn Sie [Elektronische Berichterstattung](general-electronic-reporting.md) (ER)-[Modellzuordnung](er-overview-components.md#model-mapping-component) und ER-[Format](er-overview-components.md#format-component)-Komponenten entwerfen, können Sie Datenquellen von einem *USER INPUT PARAMETER*-Typ verwenden, um die erforderlichen Werte abzurufen, die zur Laufzeit in Dateneingabefeldern im Dialogfeld angegeben werden können, bevor die Ausführung eines ER-Formats beginnt. Dieses Thema beschreibt die *USER INPUT PARAMETER*-Datenquellen, die derzeit unterstützt werden.

## <a name="mandatory-properties"></a><a name="mandatory-properties"></a>Obligatorische Eigenschaften

Sie müssen die folgenden Eigenschaften für Datenquellen jedes *USER INPUT PARAMETER*-Typs angeben:

- Geben Sie im Feld **Name** den internen Namen der Datenquelle an. Sie können diesen Namen in anderen [Ausdrücken](er-formula-language.md) und Bindungen der konfigurierten Modellzuordnungs- oder Formatkomponente verwenden.

## <a name="optional-properties"></a><a name="optional-properties"></a>Optionale Eigenschaften

Sie können optional die folgenden Eigenschaften für Datenquellen eines *USER INPUT PARAMETER*-Typs angeben:

- Im Feld **Beschriftung** geben Sie die Beschriftung an, die für das zugehörige Dateneingabefeld im Dialogfeld zur Laufzeit verwendet wird. Sie können unterschiedliche Beschriftungstexte für unterschiedliche Sprachcodes hinzufügen, indem Sie das **Beschriftung**-Feld aktivieren und dann **Übersetzen** auswählen.
- Geben Sie im Feld **Hilfe** den Hilfetext an, der zur Entwurfszeit unten auf der **Format Designer**-Seite oder der **Modelzuordnungs-Designer**-Seite angezeigt wird, wenn eine bearbeitbare Datenquelle von einem *USER INPUT PARAMETER*-Typ ausgewählt ist. Dieser Text enthält möglicherweise zusätzliche Details zur Datenquelle, um Benutzern bei der Konfiguration des bearbeitbaren Formats oder der Modellzuordnungskomponente zu helfen. Sie können unterschiedliche Hilfetexte für unterschiedliche Sprachcodes hinzufügen, indem Sie **Übersetzen** auswählen.

    > [!NOTE]
    > Die **Übersetzen**-Schaltfläche, die Sie zum Hinzufügen verwenden können, um [sprachspezifische Beschriftungen und Texte](er-design-multilingual-reports.md#format-component) hinzuzufügen, wird erst verfügbar, nachdem Sie die Datenquelle hinzugefügt, Ihre Änderungen gespeichert und die Datenquelle dann erneut zur Bearbeitung geöffnet haben.

- In dem **Schreibgeschützt**-Feld konfigurieren Sie einen Ausdruck, der einen *[Booleschen](er-formula-supported-data-types-primitive.md#boolean)*-Wert zurückgibt.

    - Wenn der konfigurierte Ausdruck zur Laufzeit einen Wert von **Wahr** zurückgibt, wird das entsprechende Dateneingabefeld im Dialogfeld ausgeblendet angezeigt, und Sie können seinen Wert nicht ändern.
    - Wenn der konfigurierte Ausdruck zur Laufzeit einen Wert von **Falsch** zurückgibt oder kein Ausdruck konfiguriert ist, ist das entsprechende Dateneingabefeld im Dialogfeld verfügbar, und Sie können seinen Wert ändern.

- In dem **Standardwert**-Feld konfigurieren Sie einen Ausdruck, der den Wert des referenzierten Parametertyps zurückgibt. Dieser Wert kann verwendet werden, um zur Laufzeit einen Standardwert für das zugehörige Dateneingabefeld im Dialogfeld einzugeben.

    Wenn Sie ein ER-Format ausführen, wird der Wert, den Sie zur Laufzeit in das zugehörige Dateneingabefeld im Dialogfeld eingeben, als zuvor verwendeter Wert im Arbeitsspeicher gespeichert. Zuvor verwendete Werte werden individuell für jedes Feld, laufendes ER-Format, aktuellen Benutzer und aktuelle Organisation (Firma) gespeichert.

    - Stellen Sie die **Immer auf Standardwert zurücksetzen**-Option auf **Ja** ein, wenn der Wert, der vom **Standardwert**-Ausdruck zurückgegeben wird, immer als Standardwert verwendet werden soll, unabhängig vom zuvor verwendeten Wert.
    - Stellen Sie die **Immer auf Standardwert zurücksetzen**-Option auf **Nein** ein, wenn der Wert, der vom **Standardwert**-Ausdruckswert zurückgegeben wird, nur als Standardwert verwendet werden soll, wenn der zuvor verwendete Wert fehlt.

    > [!NOTE]
    > Wenn Sie die **Immer auf Standardwert zurücksetzen**-Option auf **Ja** festlegen, muss ein Ausdruck i Feld **Standardwert** konfiguriert werden.

- Wenn Sie die **Mehrfachauswahl zulassen**-Option auf **Ja** einstellen, können Sie zur Laufzeit mehrere Werte für den konfigurierten Parameter auswählen. Wenn Sie sie auf **Nein** einstellen, können Sie nur einen einzelnen Wert auswählen.

    > [!NOTE]
    > Diese Option gilt nicht für alle *USER INPUT PARAMETER*-Typen. Zur Entwurfszeit wird eine Ausnahme ausgelöst, um den Benutzer darüber zu informieren, dass der konfigurierte Benutzereingabeparameter keine Mehrfachauswahl unterstützt und dass nur ein einzelner Wert ausgewählt oder eingegeben werden kann.
    >
    > Wenn Sie die **Mehrfachauswahl zulassen**-Option auf **Ja** einstellen, und einen Ausdruck im **Standardwert**-Feld angegeben haben, kann dieser Ausdruck verwendet werden, um nur einen einzigen Standardwert festzulegen.

- Wählen Sie die **Sichtbarkeit bearbeiten**-Option aus, um festzulegen, ob der konfigurierte Parameter zur Laufzeit im Dialogfeld angezeigt werden soll.

    > [!NOTE]
    > Die standardmäßige Sichtbarkeit von Datenquellen von einem *USER INPUT PARAMETER*-Typ hängt von der ER-Komponente ab, die sie enthält.
    >
    > - Wenn eine Datenquelle in der Formatkomponente konfiguriert ist, ist sie standardmäßig sichtbar.
    > - Wenn eine Datenquelle in der Modellzuordnungskomponente konfiguriert ist, ist sie nur sichtbar, wenn der Wert der Datenquelle das Ergebnis beeinflusst, wenn eine ER-Komponente ausgeführt wird. Sie haben beispielsweise eine Datenquelle hinzugefügt, sie aber nicht in Ausdrücken und Bindungen der aktuellen Modellzuordnungskomponente verwendet. In diesem Fall wird das entsprechende Dateneingabefeld zur Laufzeit standardmäßig nicht im Dialogfeld angezeigt. 

    Konfigurieren Sie auf der **Formel-Designer**-Seite im **Formel**-Feld einen Ausdruck, der einen *Booleschen* Wert zurückgibt.

    - Wenn der konfigurierte Ausdruck zur Laufzeit einen Wert von **Wahr** zurückgibt oder kein Ausdruck konfiguriert ist, ist das entsprechende Dateneingabefeld im Dialogfeld zur Laufzeit sichtbar.
    - Wenn der konfigurierte Ausdruck einen Wert von **Falsch** zurückgibt, wird das zugehörige Dateneingabefeld zur Laufzeit im Dialogfeld ausgeblendet. Wenn er zur Laufzeit von anderen Ausdrücken aufgerufen wird, gibt er abhängig von anderen Einstellungen den Standardwert, den zuvor verwendeten Wert oder den Standardwert für den aktuellen Datentypwert zurück.

## <a name="type-specific-properties"></a>Typspezifische Eigenschaften

### <a name="application-dependent-user-input-parameter"></a>Anwendungsabhängiger Benutzereingabeparameter

Verwenden Sie eine Datenquelle vom Typ **Allgemein** \> **Benutzereingabeparameter**, um den erforderlichen Wert oder die erforderlichen Werte eines Datentyps abzurufen, der für die aktuelle Instanz der Microsoft Dynamics 365 Finance-Anwendung angegeben ist. Wenn Sie einer ER-Komponente eine Datenquelle dieses Typs hinzufügen, geben Sie die folgenden Eigenschaften an:

- Wählen Sie im Feld **Betriebsdatentypname (EDT, enum)** eine Anwendung [erweiterter Datentyp (EDT)](../extensibility/extensible-edts.md) oder eine Anwendungsaufzählung aus.

> [!NOTE]
> Wir empfehlen, dass Sie die Ausdrücke überprüfen, die in den Feldern **Schreibgeschützt** und **Standardwert** konfiguriert sind, wenn Sie die **Betriebsdatentypname (EDT, enum)**-Referenz in einer editierbaren Datenquelle dieses *USER INPUT PARAMETER* Typs ändern.

Die folgende Abbildung zeigt Eigenschaften der `$TaxRegNum`-Datenquelle, die in der **Instat-XML (DE)**-ER-Formatkonfiguration konfiguriert wurde. Diese Datenquelle ist für die Verwendung von *Beschreibung*-EDT konfiguriert, um zur Laufzeit das **Steuerregistrierungsnummer**-Dateneingabefeld im Dialogfeld zu bieten.

![Eigenschaften einer Datenquelle des Typs USER INPUT PARAMETER im Dialogfeld der Format-Designer-Seite.](./media/er-user-input-parameter-data-sources-01.png)

Die folgende Abbildung zeigt das Dialogfeld, das zur Laufzeit angezeigt wird, wenn das **Instat-XML (DE)**-ER-Formatkonfiguration ausgeführt wird, um die Intrastat-Meldung zu [generieren](../../../finance/localizations/tasks/eur-00002-eu-intrastat-declaration.md). Beachten Sie, dass das konfigurierte **Steuerregistrierungsnummer**-Feld für die Dateneingabe zur Verfügung steht.

![Dialogfeld „Intrastat-Bericht“ des laufenden ER-Formats auf der Seite „Intrastat“.](./media/er-user-input-parameter-data-sources-02.png)

### <a name="data-model-enumeration-user-input-parameter"></a>Benutzereingabeparameter  der Datenmodellenumeration

Verwenden Sie eine Datenquelle des **Datenmodell** \> **Enumerations-Benutzereingabeparameter**-Typs, um den erforderlichen Wert oder die erforderlichen Werte einer einzelnen Datenmodell-[Aufzählung](er-formula-supported-data-types-primitive.md#enumeration) zu erhalten. Wenn Sie einer ER-Komponente eine Datenquelle dieses Typs hinzufügen, geben Sie die folgenden Eigenschaften an:

- Geben Sie im Feld **Modell** eine Referenz auf das Basisdatenmodell an.
- Geben Sie im Feld **Modellenumeration** eine Referenz auf eine Enumeration des referenzierten Datenmodells an.
- Wählen Sie im Feld **Version** die Revisionsnummer der ER-Datenmodellkomponente aus, die die referenzierte Modellenumeration enthält.

    > [!TIP]
    > Zur Entwurfszeit können Sie das **Version**-Feld leer lassen, um auf die Liste der Enumerationen für die referenzierte Datenmodellkomponente zuzugreifen, die sich in der Entwurfsversion der entsprechenden ER-Datenmodellkonfiguration befindet. Auf diese Weise können Sie gleichzeitig die Entwurfsversion Ihrer Modellzuordnungs- oder Formatkomponente und die Entwurfsversion der Basisdatenmodellkomponente bearbeiten.
    >
    > Beachten Sie jedoch, dass das **Version**-Feld nur in der Entwurfsversion einer Modellzuordnungs- oder Formatkomponente leer gelassen werden kann. Wenn Sie den Status einer ER-Modellzuordnungs- oder Formatkonfiguration von **Entwurf** auf **Abgeschlossen** ändern, wird dieses Feld automatisch mit der höchsten Modellrevisionsnummer ausgefüllt, die in der aktuellen Finance-Instanz verfügbar ist. Wenn Sie eine neue Enumeration oder einen neuen Enumerationswert in die Entwurfsversion Ihres Basisdatenmodells einführen und in der bearbeitbaren Modellzuordnungs- oder Formatkomponente darauf verweisen, vervollständigen Sie diese Entwurfsversion der Konfiguration des Basisdatenmodells, bevor der Entwurfsversion Ihrer ER-Modellzuordnung oder Formatkonfiguration abgeschlossen ist. Andernfalls wird eine „Pfad nicht gefunden“-Ausnahme ausgelöst, wenn Sie den Status der Modellzuordnungs- oder Formatkonfiguration von **Entwurf** auf **Abgeschlossen** ändern. Die Meldung informiert Sie darüber, dass die referenzierte Aufzählung oder der Aufzählungswert im Basisdatenmodell fehlt.

Die folgende Abbildung zeigt Eigenschaften der `$ReportDirection`-Datenquelle, die in der **Instat-XML (DE) Contoso**-ER-Formatkonfiguration konfiguriert wurde. Die **Instat-XML (DE) Contoso**-Konfiguration wurde aus der **Instat-XML (DE)**-Konfiguration [abgeleitet](general-electronic-reporting.md#Configuration). Diese Datenquelle ist für die Verwendung der Modellenumeration *ReportDirection* konfiguriert, um zur Laufzeit das geeignete Suchfeld im Dialogfeld zu bieten.

![Eigenschaften der Datenquelle des Typs USER INPUT PARAMETER im Dialogfeld der Format-Designer-Seite.](./media/er-user-input-parameter-data-sources-03.png)

### <a name="format-enumeration-user-input-parameter"></a>Benutzereingabeparameter  für Formatenumeration

Verwenden Sie eine Datenquelle des Typs **Format-Enumeration** \> **Enumerations-Benutzereingabeparameter**, um den erforderlichen Wert oder die erforderlichen Werte einer einzelnen Format-Enumeration zu erhalten. Wenn Sie einer ER-Komponente eine Datenquelle dieses Typs hinzufügen, geben Sie die folgenden Eigenschaften an:

- Geben Sie im Feld **Format-Enumeration** eine Aufzählung des bearbeitbaren Formats an.

> [!NOTE]
> Datenquellen dieses Typs können nur im Bereich der bearbeitbaren Formatkomponente konfiguriert werden.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Formeldesigner in der elektronischen Berichterstellung](general-electronic-reporting-formula-designer.md)

[Datenquellenwerte vom Typ USER INPUT PARAMETER aus dem Quellcode initiieren](er-initiate-uip-data-source-value-from-source-code.md)
