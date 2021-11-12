---
title: Steuerkonfigurationen für die Masterdatensuche anpassen
description: In diesem Thema wird erläutert, wie Sie Steuerkonfigurationen anpassen, um die Funktionalität der Masterdatensuche zu erweitern.
author: kai-cloud
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: pashao
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 498201d5c0377058e86b25953ebbe401ae1af9e3
ms.sourcegitcommit: ed43ceae9b2ef3f616b81127bcf4c4b0862e23f5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/28/2021
ms.locfileid: "7714879"
---
# <a name="customize-tax-configurations-for-master-data-lookup"></a>Steuerkonfigurationen für die Masterdatensuche anpassen

[!include [banner](../includes/banner.md)]

Führen Sie die Schritte in diesem Thema aus, um Steuerkonfigurationen anzupassen, um die Funktionalität der Masterdatensuche zu erweitern.

## <a name="import-a-tax-configuration-provided-by-microsoft"></a>Importieren einer von Microsoft bereitgestellten Steuerkonfiguration

1. Wählen Sie in Regulatory Configuration Service (RCS) im Arbeitsbereich **Elektronische Berichterstellung** den **Microsoft**-Konfigurationsanbieter aus.
2. Wählen Sie **Repositorys** aus.
3. Wählen Sie **Global** und dann **Öffnen** aus.
4. Wählen Sie eine Steuerkonfiguration aus, z. B. **Konfiguration der Steuerberechnung**, und wählen Sie dann auf der Registerkarte **Versionen** eine Version aus.
5. **Import** auswählen

> [!NOTE]
> Standardmäßig wird die Dataverse-Modellzuordnung importiert. Wenn Sie während des Konfigurationsimportvorgangs Warnmeldungen erhalten, aktivieren Sie die virtuellen Entitäten in Dataverse. Weitere Informationen finden Sie unter [virtuelle Dataverse-Entitäten aktivieren](../../fin-ops-core/dev-itpro/power-platform/enable-virtual-entities.md).

## <a name="create-a-customized-data-model-configuration"></a>Eine benutzerderfinierte Datenmodellkonfiguration erstellen

1. Wählen Sie im Arbeitsbereich **Elektronische Berichterstattung** **Steuerkonfigurationen** und dann die zu erweiternde Datenmodellkonfiguration aus. Wählen Sie zum Beispiel **Datenmodell zur Steuerberechnung**.
2. Wählen Sie **Konfiguration erstellen**.
3. Wählen Sie **Steuerpflichtiges Dokumentenmodell abgeleitet von Name: Tax Calculation Data Model, Microsoft**.
4. Geben Sie im Feld **Name** die Bezeichnung **Anpassungsdatenmodell** ein.
5. Wählen Sie **Konfiguration erstellen**.

## <a name="create-customized-reference-models"></a>Erstellen Sie angepasste Referenzmodelle

1. Wählen Sie auf der Seite **Steuerkonfigurationen** **Anpassungsdatenmodell** und dann **Designer**.
2. Wählen Sie die Ellipsen-Schaltfläche (**...**) und dann die Ansicht **Refernezmodul**.

    [![Referenzmodell.](./media/pic2.png)](./media/pic2.png)

3. Erstellen Sie das angepasste Referenzmodell. Das angepasste Modell ist ein Stammmodell. Die benutzerdefinierte Entität ist eine Datensatzliste. Das benutzerdefinierte Feld ist ein Zeichenfolgenfeld, das Sie in der Suche verwenden möchten. Sie können bei Bedarf weitere Felder hinzufügen.
4. Wählen Sie die Ellipsen-Schaltfläche (**...**) und dann die Ansicht **Steuerpflichtiges Dokument**.
5. Wählen Sie das Attribut aus, das an das benutzerdefinierte Referenzmodell gebunden werden soll. Wählen Sie zum Beispiel **Benutzerdefiniertes Attribut**, und führen Sie dann diese Schritte aus:

    1. Wählen Sie **Referenzmodell auswählen**.
    2. Wählen Sie **Angepasstes Modell** und dann **OK** aus. Der Name des Referenzmodells wird auf den Wert des Feld **Natürlicher Schlüssel** aktualisiert.

        [![Dialogfeld Referenzmodell auswählen.](./media/pic5.png)](./media/pic5.png)

    3. Wählen Sie **Speichern** und dann **Abschließen** aus.

## <a name="create-a-customized-model-mapping-configuration"></a>Eine benutzerderfinierte Datenmodellzuordnung erstellen

1. Wählen Sie im Arbeitsbereich **Elektronische Berichterstattung** **Steuerkonfigurationen** und dann die Konfiguration **Dataverse-Modellzuordnung** aus.
2. Wählen Sie im Fekd **Standard für Modellzuordnung** **Nein** aus.
3. Wählen Sie **Konfiguration erstellen**.
4. Wählen Sie **Zuordnung des steuerpflichtigen Dokumentenmodells abgeleitet von Name: Dataverse-Modellzuordnung, Microsoft**.
5. Geben Sie im Feld **Name** die Bezeichnung **Anpassungsdatenzuordnung** ein.
6. Wählen Sie im **Zielmodell**-Feld das Datenmodell **Anpassungsdatenmodell**.
7. Wählen Sie **Konfiguration erstellen**.

    [![Konfigurations-Dropdown-Dialogfeld erstellen.](./media/pic6.png)](./media/pic6.png)

8. Wählen Sie **Zuordnung von Anpassungsmodellen** und stellen Sie das Feld **Verbundene Anwendung** auf die Verbindung, die in Schritt 8 in[Richten Sie eine Umgebung für die Stammdatensuche ein](tax-service-set-up-environment-master-data-lookup.md) erstellt wurde.
9. Hier können Sie das Feld **Standard für Modellzuordnung** auf **Ja** festlegen.

## <a name="create-customized-model-mappings"></a>Erstellen Sie benutzerdefinierte Modellzuordnungen

1. Wählen Sie auf der **Steuerkonfigurationen**-Seite **Zuordnung von Anpassungsmodellen**.
2. Wählen Sie **Designer** und dann **Anpassungsmodell** aus.

    [![Anpassungsmodell.](./media/pic8.png)](./media/pic8.png)

## <a name="map-a-model-mapping-to-a-dataverse-entity"></a>Ordnen Sie eine Modellzuordnung einer Dataverse-Entität zu

1. Wählen Sie auf der Seite **Modellzuordnungsdesigner** **Anpassungsmodell** und dann **Designer**.
2. Wählen Sie in der Struktur **Datenquellentypen** den Eintrag **Dataverse-Table** aus.
3. Wählen Sie in der Registerkarte **Stamm hinzufügen** **Datenquellen** aus.
4. Geben Sie im Feld **Name** die Bezeichnung **Angepasstes Dataverse** ein.
5. Im zweiten **Name** Feld wählen Sie eine Entität aus.
6. Wählen Sie **OK** aus.

    [![Dialogfeld für Datenquelleneigenschaften „Tabelle“.](./media/pic9.png)](./media/pic9.png)

7. Wählen Sie **Angepasstes Dataverse** und **Angepasste Entität** und dann **Binden**.

    [![Binden von anngepasstem Dataverse und angepassten Entitäten.](./media/pic10.png)](./media/pic10.png)

8. Wählen Sie unter **Angepasstes Dataverse** und **Angepasstes Feld** ein Feld und dann **Binden**.

    [![Binden von anngepasstem Dataverse und angepassten Feldern.](./media/pic11.png)](./media/pic11.png)

9. Wählen Sie **Speichern** und dann **Abschließen** aus.

## <a name="create-a-customized-tax-configuration"></a>Eine benutzerderfinierte Steuerkonfiguration erstellen

1. Wählen Sie im Arbeitsbereich **Elektronische Berichterstattung** **Steuerkonfigurationen** und dann **Steuerberechnungskonfiguration** aus.
2. Wählen Sie **Konfiguration erstellen**.
3. Wählen Sie **Steuerdienstkonfiguration abgeleitet von Name: Steuerberechnungskonfiguration, Microsoft**.
4. Geben Sie im Feld **Name** die Bezeichnung **Anpassungskonfiguration** ein.
5. Wählen Sie **Konfiguration erstellen**.
6. Wählen Sie **Anpassungskonfiguration** und dann **Designer** aus.
7. Wählen Sie im **Datenmodell**-Feld  **Anpassungsdatenmodell**.
8. Wählen Sie im Feld **Datenmodellversion** die entsprechende Datenmodellversion aus.

    [![Eigenschaftenabschnitt.](./media/pic13.png)](./media/pic13.png)

9. Wählen Sie **Abgeschlossen** aus.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
