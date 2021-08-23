---
title: Mehrere abgeleitete Zuordnungen für einen einzelnen Modellstamm verwalten
description: In diesem Thema wird erläutert, wie Sie mehrere abgeleitete Zuordnungen verwalten, die für einen einzelnen Modellstamm konfiguriert wurden.
author: NickSelin
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERModelMappingTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 10363371713bd5a882b41900249e7061afc577ba6473fdb3356a822c8e48f8f3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6743286"
---
# <a name="manage-several-derived-mappings-for-a-single-model-root"></a>Mehrere abgeleitete Zuordnungen für einen einzelnen Modellstamm verwalten

[!include [banner](../includes/banner.md)]

Eine [EB-](general-electronic-reporting.md)Daten[modell](general-electronic-reporting.md#data-model-and-model-mapping-components)komponente wird in jeder konfigurierten EB-[Format](general-electronic-reporting.md#FormatComponentOutbound)komponente als Datenquelle zum Generieren ausgehender Dokumente verwendet. Konfigurieren Sie zur Beschreibung einer einzelnen Geschäftsdomäne eine Datenmodellkomponente mit vielen Stammdefinitionen. 

Mit jeder Stammdefinition können Sie Daten dieser Domäne so darstellen, wie es für bestimmte Berichtszwecke am besten geeignet ist. Für jede Stammdefinition können Sie eine EB-[Modellzuordnungs](general-electronic-reporting.md#data-model-and-model-mapping-components)komponente als die Microsoft Dynamics 365 Finance–spezifische Implementierung Ihres Datenmodells konfigurieren. Auf diese Weise beschreiben Sie, wie Ihr Datenmodell zur Runtime ausgefüllt wird.

Zuordnungskomponenten für EB-Modelle können sich in [Konfigurationen](general-electronic-reporting.md#Configuration) von EB-Datenmodelllen und EB-Modellzuordnungskonfigurationen befinden. Eine einzelne EB-Konfiguration kann viele Zuordnungskomponenten enthalten, von denen jede für eine einzelne Stammdefinition konfiguriert ist. Eine einzelne EB-Konfiguration kann alternativ nur eine Zuordnungskomponente enthalten, die für eine einzelne Stammdefinition konfiguriert ist.

Viele Konfigurationsanbieter bieten möglicherweise EB-Modellzuordnungskonfigurationen für dasselbe EB-Datenmodell an. Diese Modellzuordnungskonfigurationen können Zuordnungskomponenten für verschiedene Stammdefinitionen enthalten. Sie können eine Modellzuordnung für eine Stammdefinition verwenden, die von einem [Anbieter](general-electronic-reporting.md#Provider) angeboten wird, und eine Modellzuordnung für eine andere Stammdefinition verwenden, die von einem anderen Anbieter angeboten wird.

In den Prozeduren in diesem Thema wird erläutert, wie mehrere EB-Modellzuordnungskonfigurationen eines EB-Datenmodells verwaltet werden, wenn sie verschiedene Modellzuordnungskomponenten enthalten, die für dieselbe Stammdefinition konfiguriert sind. 

Um die Prozeduren in diesem Thema abzuschließen, muss Ihnen die Rolle des Systemadministrators oder des elektronischen Berichtsentwicklers zugewiesen sein.

Alle der folgenden Prozeduren können im USMF-Unternehmen ausgeführt werden. Eine Codierung ist nicht erforderlich.

## <a name="configure-the-er-framework"></a>Konfigurieren des EB-Frameworks

Als Benutzer mit der Rolle „Entwickler für elektronische Berichterstellung“ müssen Sie den [minimalen Satz von EB-Parametern konfigurieren](er-quick-start2-customize-report.md#ConfigureFramework), bevor Sie mit dem EB-Framework Geschäftsdokumente generieren.

## <a name="import-the-standard-er-format-configurations"></a>Importieren der standardmäßigen EB-Formatkonfigurationen

Um Ihrer aktuellen Instanz von Finance die standardmäßigen EB-Konfigurationen hinzuzufügen, müssen Sie sie aus dem EB-Repository importieren, das für diese Instanz konfiguriert wurde. Befolgen Sie die Schritte unter [Laden Sie EB-Konfigurationen aus dem globalen Repository des Konfigurationsdienstes herunter](er-download-configurations-global-repo.md), um die folgenden EB-Formatkonfigurationen zu importieren:

- **Freitextrechnung (Excel)**, Version 220.106
- **Projektrechnung (Excel)**, Version 226.27

## <a name="review-the-imported-er-configurations"></a>Überprüfen der importierten EB-Konfigurationen

1. Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.
2. Auf der Seite **Lokalisierungskonfigurationen** im Abschnitt **Konfigurationen** wählen Sie die Kachel **Berichterstellungskonfigurationen** aus.
3. Erweitern Sie auf der Seite **Konfigurationen** in der Konfigurationsstruktur im linken Bereich den Punkt **Rechnungsmodell**.

    ![Überprüfen der importierten Konfigurationen auf der Seite „Konfigurationen“.](./media/er-multiple-model-mappings-image1.png)

4. Überprüfen Sie das Format **Freitextrechnung (Excel)**:

    1. Wählen Sie in der Konfigurationsstruktur im linken Bereich **Freitextrechnung (Excel)** aus.
    2. Wählen Sie im Aktivitätsbereich **Designer** aus.
    3. Wählen Sie auf der Seite **Format-Designer** auf der Registerkarte **Zuordnung** in der Datenquellenliste **Modell** aus.
    4. Wählen Sie **Ansicht** aus.
    
       Das aktuelle EB-Format ist für die Verwendung der Stammdefinition **InvoiceCustomer** von **Rechnungsmodell** konfiguriert. Wenn dieses Format ausgeführt wird und die Datenquelle **Modell** aufgerufen wrid, wird die Modellzuordnung verwendet, die für die Stammdefinition **InvoiceCustomer** konfiguriert ist, um auf Anwendungsdaten zuzugreifen und das Datenmodell auszufüllen.

        ![Überprüfen der Modelldatenquelle auf der Seite „Formatdesigner“.](./media/er-multiple-model-mappings-image2.png)

    6. Seite **Format-Designer** schließen.

5. Überprüfen Sie den Inhalt der Konfiguration **Rechnungsmodellzuordnung**:

    1. Wählen Sie in der Konfigurationsstruktur im linken Bereich **Rechnungsmodellzuordnung** aus.
    2. Wählen Sie im Aktivitätsbereich **Designer** aus.
    3. Beachten Sie auf der Seite **Zuordnung Modell zu Datenquelle**, dass die aktuelle ER-Modellzuordnungskonfiguration mehrere Modellzuordnungskomponenten enthält:

        + Die Modellzuordnung **Debitorenrechnung** ist für die Stammdefinition **InvoiceCustomer** von **Rechnungsmodell** konfiguriert. Wenn das EB-Format **Freitextrechnung (Excel)** ausgeführt wird, kann daher die Modellzuordnung **Debitorenrechnung** dieser EB-Konfiguration ausgewählt werden, um auf Anwendungsdaten zuzugreifen und das Datenmodell auszufüllen.
        + Die Modellzuordnung **Projektrechnung** ist für die Stammdefinition **InvoiceProject** von **Rechnungsmodell** konfiguriert. Wenn das EB-Format **Projektrechnung (Excel)** ausgeführt wird, kann daher die Modellzuordnung **Projektrechnung** dieser EB-Konfiguration ausgewählt werden, um auf Anwendungsdaten zuzugreifen und das Datenmodell auszufüllen.

        ![Rechnungsmodellzuordnung auf der Seite „Zuordnung Modell zu Datenquelle“.](./media/er-multiple-model-mappings-image3.png)

    4. Schließen Sie die Seite **Zuordnung Modell zu Datenquelle**.
    5. Auf dem Inforegister **Versionen** wählen Sie **Löschen** aus, um alle Versionen dieser EB-Konfiguration zu löschen, die neuer als die Version 240.175 sind.

6. Überprüfen Sie den Inhalt der Konfiguration **Projektrechnungsmodell-Zuordnung (RDP)**:

    1. Wählen Sie in der Konfigurationsstruktur im linken Bereich **Projektrechnungsmodell-Zuordnung (RDP)** aus.
    2. Wählen Sie im Aktivitätsbereich **Designer** aus.
    3. Beachten Sie auf der Seite **Zuordnung Modell zu Datenquelle**, dass die aktuelle EB-Modellzuordnungskonfiguration die Modellzuordnung **InvoiceProject** enthält und dass diese Modellzuordnung für die Stammdefinition **InvoiceProject** des **Rechnungsmodells** konfiguriert ist. Wenn das EB-Format **Projektrechnung (Excel)** ausgeführt wird, wählen Sie die Modellzuordnung **InvoiceProject** dieser EB-Konfiguration aus, um auf Anwendungsdaten zuzugreifen und das Datenmodell auszufüllen.

        ![Projektrechnungsmodell-Zuordnung auf der Seite „Zuordnung Modell zu Datenquelle“.](./media/er-multiple-model-mappings-image4.png)

    4. Schließen Sie die Seite **Zuordnung Modell zu Datenquelle**.
    5. Auf dem Inforegister **Versionen** wählen Sie **Löschen** aus, um alle Versionen dieser EB-Konfiguration zu löschen, die neuer als die Version 226.35 sind.

## <a name="customize-the-imported-er-configurations"></a>Importierte EB-Konfigurationen anpassen

In diesem Abschnitt wird erklärt, wie die von Microsoft bereitgestellten Modellzuordnungen [angepasst werden](er-quick-start3-customize-report.md#customize-the-model-mapping-configuration). Beispielsweise kann eine Anpassung erforderlich sein, um Ihre benutzerdefinierte Logik zu implementieren oder fehlende Bindungen hinzuzufügen.

### <a name="customize-the-invoice-model-mapping-configuration"></a>Rechnungsmodellkonfigurations-Zuordnung anpassen

1. Wählen Sie auf der Seite **Konfigurationen** in der Konfigurationsstruktur im linken Bereich **Rechnungsmodellzuordnung** aus.
2. Wählen Sie im Aktivitätsbereich **Konfiguration erstellen** aus.
3. Wählen Sie im Dropdownfeld **Konfiguration erstellen** im Feld **Neu** den Eintrag **Ableiten vom Namen: Kundenrechnungsmodellzuordnung, Microsoft** aus.
4. Geben Sie im Feld **Name** die Bezeichnung **Rechnungsmodellzuordnung Litware** ein.
5. Wählen Sie **Konfiguration erstellen**.
6. [Kennzeichnen Sie](er-quick-start2-customize-report.md#MarkFormatRunnable) die [Entwurfsversion](general-electronic-reporting.md#component-versioning) der abgeleiteten Zuordnung als zur Laufzeit verfügbar:

    1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Konfigurationen** in der Gruppe **Erweiterte Einstellungen** die Option **Benutzerparameter** aus.
    2. Legen Sie im Dialogfeld **Benutzerparameter** die Option **Testlaufeinstellungen** auf **Ja** fest und wählen Sie dann **OK** aus.
    3. Wählen Sie **Bearbeiten** aus, um die Seite bei Bedarf bearbeiten zu können.
    4. Für die Konfiguration **Rechnungsmodellzuordnung Litware**, die derzeit in der Konfigurationsstruktur ausgewählt ist, setzen Sie die Option **Entwurf ausführen** auf **Ja**.

7. Wählen Sie im Aktivitätsbereich die Option **Designer** aus, um die Modellzuordnungen dieser Konfiguration zu überprüfen.

    ![Überprüfen der Rechnungsmodellzuordnungen auf der Seite „Zuordnung Modell zu Datenquelle“.](./media/er-multiple-model-mappings-image5.png)

    > [!TIP]
    > Sie können jetzt alle EB-Modellzuordnungskomponenten dieser EB-Konfiguration im Designer öffnen, um Ihre benutzerdefinierte Logik zu konfigurieren. Weitere Informationen finden Sie unter [Datenmodellkonfigurations-Zuordnung anpassen](er-quick-start3-customize-report.md#customize-the-model-mapping-configuration).

8. Schließen Sie die Seite **Zuordnung Modell zu Datenquelle**.

Sie haben jetzt die Konfigurationen **Rechnungsmodellzuordnung** und **Rechnungsmodellzuordnung Litware**, von denen jede eine Modellzuordnung hat, die für die Stammdefinition **InvoiceCustomer** konfiguriert ist. Weisen Sie explizit eine der Modellzuordnungen als Standardmodellzuordnung zu, die von einem der EB-Formate verwendet wird, z. B. dem Format **Freitextrechnung (Excel)**, das eine Modelldatenquelle enthält, die die Stammdefinition **InvoiceCustomer** aufweist. Andernfalls wird beim Ausführen, Bearbeiten oder Überprüfen eines der EB-Formate die folgende Ausnahme ausgelöst, um Sie darüber zu informieren, dass keine Standardmodellzuordnung explizit zugewiesen wurde:
 
> Es gibt mehr als eine Modellzuordnung für das Datenmodell '\<model name\> (\<root descriptor\>)' in den Konfigurationen \<configuration names separated by commas\>. Legen Sie eine der Konfigurationen als Standard fest.

![Öffnen des Formats zum Bearbeiten auf der Seite „Konfigurationen“.](./media/er-multiple-model-mappings-image6.gif)

### <a name="customize-the-project-invoice-model-mapping-rdp-configuration"></a>Konfiguration der Projektrechnungsmodell-Zuordnung (RDP) anpassen

1. Wählen Sie auf der Seite **Konfigurationen** in der Konfigurationsstruktur im linken Bereich **Projektrechnungsmodell-Zuordnung (RDP)** aus.
2. Wählen Sie im Aktivitätsbereich **Konfiguration erstellen** aus.
3. Wählen Sie im Dialogfeld **Konfiguration erstellen** im Feld **Neu** den Eintrag **Ableiten vom Namen: Projektrechnungsmodell-Zuordnung (RDP)** aus.
4. Geben Sie im Feld **Name** die Bezeichnung **Projektrechnungsmodell-Zuordnung (Litware)** ein.
5. Wählen Sie **Konfiguration erstellen**.
6. Für die Konfiguration **Projektrechnungsmodell-Zuordnung Litware**, die derzeit in der Konfigurationsstruktur ausgewählt ist, setzen Sie die Option **Entwurf ausführen** auf **Ja**.
7. Wählen Sie im Aktivitätsbereich die Option **Designer** aus, um die Modellzuordnungen dieser Konfiguration zu überprüfen.

    ![Die angepassten Projektrechnungsmodell-Zuordnungen auf der Seite „Zuordnung Modell zu Datenquelle“ überprüfen.](./media/er-multiple-model-mappings-image7.png)

8. Schließen Sie die Seite **Zuordnung Modell zu Datenquelle**.

Sie haben jetzt die Konfigurationen **Rechnungsmodellzuordnung**, **Projektrechnungsmodellzuordnung (RDP)** und **Projektrechnungsmodell-Zuordnung Litware**. Für jede dieser Konfigurationen ist eine Modellzuordnung für die Stammdefinition **InvoiceProject** konfiguriert. Weisen Sie explizit eine der Modellzuordnungen als Standardmodellzuordnung zu, die von einem der EB-Formate verwendet wird. Verwenden Sie zum Beispiel das Format **Projektrechnung (Excel)**, das eine Modelldatenquelle enthält, die die Stammdefinition **InvoiceProject** aufweist. Andernfalls wird beim Ausführen oder Bearbeiten eines der EB-Formate eine Ausnahme ausgelöst, um Sie darüber zu informieren, dass keine Standardmodellzuordnung explizit zugewiesen wurde.

## <a name="select-the-derived-invoice-model-mapping-litware-configuration-as-the-configuration-that-contains-default-model-mappings"></a>Wählen Sie die abgeleitete Konfiguration „Rechnungsmodellzuordnung Litware“ als die Konfiguration aus, die Standardmodellzuordnungen enthält.

1. Wählen Sie auf der Seite **Konfigurationen** in der Konfigurationsstruktur im linken Bereich **Rechnungsmodellzuordnung Litware** aus.
2. Hier können Sie die Option **Standard für Modellzuordnung** auf **Ja** festlegen.

    ![Festlegen der Modellzuordnung als Standardmodellzuordnung auf der Seite „Konfigurationen“.](./media/er-multiple-model-mappings-image8.png)

    Aufgrund dieser Einstellung wird die Modellzuordnung **Kopie der Kundenrechnung** verwendet, wenn Sie das Format **Freitextrechnung (Excel)** ausführen oder wenn Sie es bearbeiten oder validieren. Die Modellzuordnung **Kundenrechnung** aus der Konfiguration **Rechnungsmodellzuordnung** wird ignoriert.

    Sie können jetzt das Format **Freitextrechnung (Excel)** zur Überprüfung im Format-Designer öffnen.

## <a name="select-the-derived-project-invoice-model-mapping-litware-configuration-as-the-configuration-that-contains-default-model-mappings"></a>Wählen Sie die abgeleitete Konfiguration „Projektrechnungsmodell-Zuordnung Litware“ als die Konfiguration aus, die Standardmodellzuordnungen enthält.

1. Wählen Sie auf der Seite **Konfigurationen** in der Konfigurationsstruktur im linken Bereich **Projektrechnungsmodell-Zuordnung Litware** aus.
2. Hier können Sie die Option **Standard für Modellzuordnung** auf **Ja** festlegen.

    Im Gegensatz zu dem Fall, der für die Konfiguration **Rechnungsmodellzuordnung Litware** im vorherigen Abschnitt beschrieben wird, können Sie in diesem Fall nicht mit der Verwendung der Modellzuordnung **InvoiceProject Kopie** aus der Konfiguration **Projektrechnungsmodell-Zuordnung Litware** beginnen. Zwei Konfigurationen, die eine Modellzuordnung für die Stammdefinition **InvoiceProject** enthalten, sind derzeit als Standardkonfiguration markiert. Daher haben sie die gleiche Priorität für die Verwendung. Führen Sie die verbleibenden Schritte diese Prozedur aus, um dieses Problem zu beheben.

3. Wählen Sie in der Konfigurationsstruktur im linken Bereich **Rechnungsmodellzuordnung Litware** aus.
4. Wählen Sie im Aktivitätsbereich **Designer** aus.
5. Auf der Seite **Zuordnung Modell zu Datenquelle** wählen Sie **Bearbeiten** aus, um die Seite nach Bedarf bearbeitbar zu machen.
6. Wählen Sie die Modellzuordnung **Projektrechnungskopie** aus, und aktivieren Sie dann das Kontrollkästchen **Ist gelöscht** für sie.

    ![Festlegen der Modellzuordnung als virtuell gelöscht auf der Seite „Zuordnung Modell zu Datenquelle“.](./media/er-multiple-model-mappings-image9.png)

    Aufgrund dieser Einstellung wird die **Rechnungsmodellzuordnung Litware** so behandelt, als hätte sie keine Modellzuordnung für die Stammdefinition **InvoiceProject**. Die Modellzuordnung **InvoiceProject Kopie** wird standardmäßig ausgegeben. Die Konfiguration **Projektrechnungsmodell-Zuordnung Litware**, die diese Modellzuordnung enthält, wird als Standardkonfiguration markiert. Da sie als Standard markiert ist, hat sie eine höhere Priorität als die Modellzuordnung **InvoiceProject** aus der Konfiguration **Projektrechnungsmodell-Zuordnung (RDP)**.

## <a name="other-considerations"></a>Weitere Überlegungen

Die Modellzuordnung **InvoiceProject Kopie** der Konfiguration **Projektrechnungsmodell-Zuordnung Litware** ist für die Verwendung der Datenquelle **ReportDataProvider** ausgelegt. Die Datenquelle ist Teil des Typs *Objekt*, der auf die Anwendungsklasse **PsaProjInvoiceDP** verweist. Diese Klasse wird als Datenanbieter für den SSRS-Bericht (SQL Server Reporting Services) der Projektrechnung des Druckverwaltungsframeworks implementiert. Wählen Sie diese Datenquelle als EB-[Integrationspunkt](er-apis-app10-0-11.md#api-to-run-a-format-mapping-for-the-generation-of-outbound-documents) aus. Die aktuelle EB-Implementierung für Druckverwaltungsberichte berücksichtigt diese Einstellung. Weitere Informationen finden Sie im Quellcode der Anwendungsklasse **ERPrintMgmtDataProviderReport**. Zur Laufzeit erzwingt die Zuordnung der Datenquelle **ReportDataProvider** als Integrationspunkt der Modellzuordnung Finance, diese Zuordnungskomponente mit einer höheren Priorität zu behandeln als die Zuordnungskomponente **InvoiceProject** aus der Konfiguration **Projektrechnungsmodell-Zuordnung (RDP)**.

## <a name="see-also"></a>Siehe auch

- [ER-Modellzuordnungen in separaten EB-Konfigurationen verwalten](./tasks/er-manage-model-mapping-configurations-july-2017.md)
- [Auf Länderkontext beruhende ER-Modellzuordnungen konfigurieren](er-country-dependent-model-mapping.md)
- [Änderungen der EB-Framework-API](er-apis-app10-0-11.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]