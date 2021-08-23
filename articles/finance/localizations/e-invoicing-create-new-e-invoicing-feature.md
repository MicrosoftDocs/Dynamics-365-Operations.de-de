---
title: Neue Funktion zur elektronischen Rechnungsstellung erstellen
description: Dieses Thema erklärt, wie Sie eine neue Funktion für die elektronische Rechnungsstellung erstellen, wenn keine konfigurierbare Funktion für Ihr Land oder Ihre Region standardmäßig verfügbar ist.
author: gionoder
ms.date: 07/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2021-07-21
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: ffef49c78fd0564db7a2329580ad33a9ccc633c8ac74557e625d1cfb29931576
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6744934"
---
# <a name="create-a-new-electronic-invoicing-feature"></a>Neue Funktion zur elektronischen Rechnungsstellung erstellen

[!include [banner](../includes/banner.md)]

Dieses Thema erklärt, wie Sie eine neue Funktion für die elektronische Rechnungsstellung erstellen, wenn keine konfigurierbare Funktion für Ihr Land oder Ihre Region standardmäßig verfügbar ist.

Erledigen Sie diese Aufgaben, um eine neue Funktion für die elektronische Rechnungsstellung zu erstellen.

1. Erstellen Sie eine neue Dateiformatkonfiguration, indem Sie die bereitgestellte Rechnungsmodellkonfiguration verwenden und die vorhandene Rechnungszuordnung für die zu erstellende Funktion nutzen.
2. Fügen Sie die Dateiformatkonfigurationen den Konfigurationen der elektronischen Rechnungsstellungsfunktion hinzu.
3. Erstellen Sie die Einstellungen der Funktion zur elektronischen Rechnungsstellung.
4. Vervollständigen Sie die neue Funktion zur elektronischen Rechnungsstellung und veröffentlichen Sie sie im globalen Repository für Ihre Organisation.
5. Stellen Sie die neue Funktion zur elektronischen Rechnungsstellung in der Service-Umgebung bereit.

## <a name="create-new-file-format-configurations-that-are-derived-from-the-existing-invoice-model"></a>Erstellen Sie neue Dateiformatkonfigurationen, die aus dem bestehenden Rechnungsmodell abgeleitet werden

In diesem Verfahren erstellen Sie die Dateiformatkonfigurationen, die für die neue Funktion zur elektronischen Rechnungsstellung erforderlich sind, die Sie erstellen möchten. Sie können die Dateiformatkonfiguration für elektronische Rechnungen und alle anderen Dateiformatkonfigurationen erstellen, die Ihre neue Funktion zur elektronischen Rechnungsstellung möglicherweise erfordert.

Bevor Sie mit diesem Verfahren beginnen, melden Sie sich bei Ihrem Regulatory Configuration Service-Konto (RCS-Konto) an.

1. Wählen Sie in Microsoft Dynamics 365 Finance im Arbeitsbereich **Elektronische Berichterstellung** **Repositorys** für den Konfigurationsanbieter **Microsoft** an.
2. Wählen Sie **Global**, **Öffnen** und dann im linken Bereich die Konfiguration des **Rechnungsmodells** aus.

    > [!IMPORTANT]
    > Wählen Sie für Brasilien stattdessen die Modellkonfiguration **Steuerdokumente** aus.

3. Wählen Sie auf der Registerkarte **Konfigurationen** **Importieren** aus.
4. Schließen Sie die Seite.
5. Schließen Sie die Seite.
6. Wählen Sie die Kachel **Berichterstellungskonfigurationen** und dann das importierte Rechnungsmodell aus.
7. Wählen Sie **Konfiguration erstellen** und dann **Format basiert auf dem Rechnungskontextmodell**.
8. Geben Sie einen Namen sowie die Beschreibung für die Formatkonfiguration ein.
9. Wählen Sie im Feld **Formattyp** den Dateierweiterungstyp aus.
10. Wählen Sie **Konfiguration erstellen** und dann die erstellte Formatkonfiguration aus.
11. Wählen Sie **Designer** aus und verwenden Sie das Formatdesigner-Tool, um das Dateilayout so zu konfigurieren, dass es den Dateiformatspezifikationen entspricht.
12. Schließen Sie die Seite.
13. Wählen Sie in der Registerkarte **Versionen** die **Status ändern** \> **Abschließen** aus.
14. Wählen Sie **Status ändern** \> **Teilen** aus, um die Formatkonfiguration im globalen Repository zu veröffentlichen.

Die neue Dateiformatkonfiguration muss für die Microsoft Domäne freigegeben werden, bevor die Konfiguration vom Dienst für die elektronische Rechnungsstellung verwendet werden kann.

1. Wählen Sie die Formatkonfiguration aus, an der Sie arbeiten. Der Status der Konfiguration muss **Freigegeben** lauten.
2. Wählen Sie auf der Registerkarte **Versionen** **Erweitertes Teilen** \> **Globales Repository**.
3. Wählen Sie auf der Registerkarte **Geteilt mit** **Organisation** aus.
4. Geben Sie im Feld **Parameter** **Microsoft.com** ein, um die Formatkonfiguration mit der Microsoft Domäne zu teilen.
5. Wählen Sie **OK** aus.

## <a name="create-the-new-electronic-invoicing-feature"></a>Die neue Funktion zur elektronischen Rechnungsstellung erstellen

1. Wählen Sie im RCS im Arbeitsbereich **Globalisierungsfunktionen** im Abschnitt **Funktionen** die Kachel **Elektronische Rechnungsstellung** aus.
2. Wählen Sie **Hinzufügen** und anschließend **Neue Funktion** aus.
3. Geben Sie einen Namen und eine Beschreibung für die Funktion zur elektronischen Rechnungsstellung ein.
4. Wählen Sie **Funktion erstellen**.

## <a name="add-electronic-invoicing-feature-configurations"></a>Konfigurationen für die Funktion für die elektronische Rechnungsstellung hinzufügen

1. Wählen Sie die elektronische Rechnungsstellungsfunktion aus, an denen Sie arbeiten.
2. Wählen Sie auf der Registerkarte **Konfigurationen** **Hinzufügen** aus.
3. Suchen Sie im Raster **Konfigurationen** nach den Dateiformatkonfiguration, die Ihre Funktion zur elektronischen Rechnungsstellung benötigt, um die elektronische Rechnungsdatei zu erstellen, und wählen Sie sie aus.
4. Wählen Sie **OK** aus.

## <a name="add-electronic-invoicing-feature-setups"></a>Einstellungen der Funktion für die elektronische Rechnungsstellung hinzufügen

1. Wählen Sie auf der Registerkarte **Einstellungen** **Hinzufügen** und dann **Benutzerdefinierte Einstellungen**.
2. Geben Sie einen Namen und eine Beschreibung für die Funktionseinstellungen ein.
3. Wählen Sie im Feld **Einstellungstyp** **Verarbeitungspipeline**.
4. Wählen Sie **Erstellen** aus.
5. Wählen Sie Einstellung aus, an der Sie gerade arbeiten, und wählen Sie dann **Bearbeiten**.
6. Wählen Sie auf der Registerkarte **Verarbeitungspipeline** **Neu** aus, um eine Pipelineaktivität hinzuzufügen. Weitere Informationen zu Pipelines finden Sie unter [Aktivitäten](e-invoicing-configuration-rcs.md#actions).
7. Wählen Sie auf der die Registerkarte **Anwendbarkeitsregeln** **Neu** aus, um die Anwendbarkeitsregelklauseln hinzuzufügen. Weitere Informationen über Anwendbarkeitsregeln finden Sie unter [Anwendbarkeitsregeln](e-invoicing-configuration-rcs.md#applicability-rules).
8. Wählen Sie auf der Registerkarte **Variablen** **Neu** aus, um Variablen nach Bedarf hinzuzufügen.
9. Wählen Sie **Speichern** und dann **Überprüfen** aus, um die Konsistenz der Konfiguration zu überprüfen.
10. Schließen Sie die Seite.

## <a name="deploy-the-electronic-invoicing-feature-to-the-service-environment"></a>Die Funktion zur elektronischen Rechnungsstellung in der Service-Umgebung bereitstellen

Informationen zum Ausführen dieser Aufgabe finden Sie unter [Bereitstellen der Funktion für die elektronische Rechnungsstellung in der Service-Umgebung](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-service-environment).

## <a name="deploy-the-electronic-invoicing-feature-to-a-connected-application"></a>Die Funktion zur elektronischen Rechnungsstellung einer verbundenen Anwendung bereitstellen

Informationen zum Ausführen dieser Aufgabe finden Sie unter [Anwendungseinrichtung konfigurieren](e-invoicing-get-started.md#configure-the-application-setup) und [Bereitstellen der Funktion für die elektronische Rechnungsstellung in der verbundenen Anwendung](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-connected-application).
