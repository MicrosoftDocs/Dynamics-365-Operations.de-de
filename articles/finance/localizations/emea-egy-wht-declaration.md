---
title: Quellensteuererklärung für Ägypten
description: In diesem Artikel wird erläutert, wie Sie die Quellensteuererklärungen für Ägypten konfigurieren und generieren.
author: AdamTrukawka
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: 2017-06-20
ms.dyn365.ops.version: 10.0.18
ms.search.scope: ''
ms.openlocfilehash: 83def72f1ff0423d1c2d217847082fa9bf1c3bca
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269373"
---
#  <a name="withholding-tax-declaration-for-egypt-eg-00005"></a>Quellensteuererklärung für Ägypten (EG-00005)

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

## <a name="overview"></a>Übersicht
In diesem Artikel wird erläutert, wie Sie die Quellensteuererklärung und die Quellensteuererklärungsformulare 41 und 11 für juristische Personen in Ägypten einrichten und erstellen. 

Alle ägyptischen Unternehmen müssen das Formular 41 erstellen, in dem alle Steuern zusammengefasst sind, die von lokalen Lieferanten und Dienstleistern einbehalten werden. Zusätzlich zu Formular 41 muss Formular 11 erstellt werden, in dem alle von ausländischen Anbietern einbehaltene Steuern aufgeführt sind. 

Der Bericht **Quellensteuererklärung** in Dynamics 365 Finance enthält die folgenden Berichte:

- Erklärungsformular Nr. 41
- Erklärungsformular Nr. 11
    
    
## <a name="prerequisites"></a>Voraussetzungen
Die primäre Adresse der juristischen Person muss in Ägypten liegen.
Im Arbeitsbereich **Funktionsverwaltung** muss die folgende Funktion aktiviert sein:

   - **Globale Quellensteuer**

Weitere Informationen zur Aktivierung von Funktionen finden Sie unter [Funktionsverwaltungsüberblick](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

1. Rufen Sie **Steuer** > **Einrichtung** > **Parameter** > **Hauptbuchparameter** auf. Setzen Sie anschließend auf der **Quellensteuer**-Registerkarte **Globale Quellensteuer aktivieren** auf **Ja**.
2. Importieren Sie im Arbeitsbereich **Elektronische Berichterstattung** die folgenden elektronischen Berichtsformate aus dem Repository:

    - Quellensteuererklärung Excel (EG)

    > [!NOTE]
    > Das obige Format basiert auf dem **Steuererklärungsmodell** und verwendet die **Zuordnung des Steuererklärungsmodells**. Diese zusätzliche Konfiguration wird automatisch importiert.

Weitere Informationen zum Importieren von Konfigurationen für elektronische Berichte finden Sie unter [Elektronische Berichterstellungskonfigurationen von Lifecycle Services herunterladen](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

## <a name="download-electronic-reporting-configurations"></a>Elektronische Berichtskonfigurationen herunterladen

Die Implementierung der Quellensteuererklärungsformulare für Ägypten basiert auf Konfigurationen für die elektronische Berichterstattung (ER). Weitere Informationen zu den Funktionen und Konzepten der konfigurierbaren Berichterstellung finden Sie unter [Elektronische Berichterstattung](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).

Befolgen Sie für Produktions- und UAT-Umgebungen (User Acceptance Testing) die Anweisungen im Artikel: [Elektronische Berichterstellungskonfigurationen von Lifecycle Services herunterladen](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

Um die Quellensteuererklärungen in einer ägyptischen juristischen Person zu generieren, müssen Sie die folgenden Konfigurationen hochladen:

- Steuererklärung model.version.82.xml oder eine neuere Version
- Steuererklärungsmodell mapping.version.82.133.xml oder eine neuere Version
- Quellensteuererklärung Excel (EG).version.82.21 oder eine neuere Version

Führen Sie die folgenden Schritte aus, nachdem Sie die ER-Konfigurationen von Lifecycle Services (LCS) oder dem globalen Repository heruntergeladen haben.

1. Wechseln Sie in den Arbeitsbereich **Elektronische Berichterstellung** und wählen Sie die Kachel **Berichterstellungskonfigurationen** aus.
1. Wählen Sie auf der Seite **Konfigurationen** im Aktionsbereich **Austausch > Aus XML-Datei laden** aus.
1. Laden Sie alle Dateien in der Reihenfolge hoch, in der sie in den vorherigen Aufzählungszeichen aufgeführt sind. Nachdem alle Konfigurationen hochgeladen wurden, sollte der Konfigurationsbaum in Finance vorhanden sein.

## <a name="set-up-application-specific-parameters"></a>Anwendungsspezifische Parameter einrichten

Mit der Option für anwendungsspezifische Parameter können Benutzer die Kriterien festlegen, nach denen die Steuertransaktionen in jeder Zeile eines generierten Berichts abhängig von der Konfiguration von **Artikel-Quellensteuergruppe** oder andere Kriterien, die in der Definition der Suche festgelegt sind, klassifiziert und berechnet werden.

Das Quellensteuererklärungsformular 41 enthält eine bestimmte Spalte, in der die Quellensteuertransaktion gemäß der Klassifizierung der Steuerbehörde namens **Rabattcode-Typ** klassifiziert werden muss. Anstatt diese neuen Klassifizierungen als neue Eintragsdaten einzuschließen, wenn die Transaktionen gebucht werden, werden die Klassifizierungen basierend auf den verschiedenen in **Konfigurationen** > **Anwendungsspezifische Parameter einrichten** > **Einrichten** eingeführten Suchvorgängen bestimmt, um die Anforderungen der Quellensteuerberichte für Ägypten zu erfüllen. 

Die folgende Konfiguration wird verwendet, um die Transaktionen im Bericht des Quellensteuererklärungsformulars 41 zu klassifizieren:

- **DiscountTaxTypeLookup**-> Spalte Nr. 18 

Führen Sie die folgenden Schritte aus, um die verschiedenen Suchvorgänge einzurichten, die zum Generieren der Quellensteuererklärung und der zugehörigen Buchberichte verwendet werden. 

1. In dem Arbeitsbereich **Elektronische Berichterstattung** wählen Sie **Konfigurationen** > **Einrichten** aus, um die Regeln zur Identifizierung der Klassifizierung von Transaktionen im Quellensteuererklärungsbericht einzurichten. 
2. Wählen Sie die aktuelle Version aus und wählen Sie im Inforegister **Suchvorgänge** den Suchnamen. Zum Beispiel **DiscountTaxTypeLookup**. Diese Suche identifiziert die Liste der von der Steuerbehörde benötigten Rabattarten.
3. Im Inforegister **Bedingungen** wählen Sie **Hinzufügen** aus und in der neuen Zeile in der Spalte **Suchergebnis** wählen Sie die zugehörige Zeile aus, die die Klassifizierung in der **Spalte 18** darstellt.
4. In der Spalte **Artikel-Quellensteuergruppe** wählen Sie den zugehörigen Code aus, mit dem die Klassifizierung identifiziert wird. Zum Beispiel **Zulässiger Rabatt**.  
5. Wiederholen Sie die Schritte 3 und 4 für alle verfügbaren Suchvorgänge.
6. Wählen Sie erneut **Hinzufügen** aus, um die letzte Belegzeile aufzunehmen, und in der **Suchergebnis**-Spalte wählen Sie **Unzutreffend** aus. 
7. Wählen Sie in den verbleibenden Spalten **Nicht leer** aus. 

> [!NOTE]

## <a name="set-up-general-ledger-parameters"></a>Einrichten der Hauptbuchparameter

Um die Quellensteuer-Erklärungsformularberichte in Microsoft Excel zu generieren, definieren Sie ein ER-Format auf der **Hauptbuchparameter**-Seite.

1. Gehen Sie zu **Steuer** > **Einrichten** > **Hauptbuchparameter**.
2. Auf der **Quellensteuer**-Registerkarte im Feld **Quellensteuer-Erklärungsformularzuordnung** wählen Sie **Quellensteuererklärung Excel (EG)** aus. Wenn Sie das Feld leer lassen, wird der Standardmehrwertsteuerbericht im SSRS-Format erstellt.


![Erklärungsformular.](media/egypt-wht-declaration-setup1.png)

## <a name="generate-the-withholding-declaration-forms"></a>Quellensteuererklärungsformulare generieren
Der Prozess der Erstellung und Übermittlung eines Quellensteuererklärungsformulars für einen bestimmten Zeitraum basiert auf den Quellensteuertransaktionen, die während des Abrechnungs- und Nachzahlungssteuerauftrags gebucht wurden. Weitere Informationen zur globalen Quellensteuer finden Sie unter [Globale Quellensteuer](../general-ledger/global-withholding-tax-overview.md).

Führen Sie die folgenden Schritte zum Generieren des Steuererklärungsberichts aus:

1. Gehen Sie zu **Steuer** > **Erklärungen** > **Quellensteuer** > **Quellensteuerzahlung*.
2. Wählen Sie den Abrechnungszeitraum und dann das Anfangsdatum für den Bericht aus. 
3. Geben Sie Transaktionsdatum ein, und wählen Sie **OK** aus.
4. Wählen Sie in dem sich öffnenden Dialogfeld eines oder mehrere der Formulare **Formular Nr. 41**, **Formular Nr. 11** oder **Keine**. Wenn Sie **Keiner** auswählen, wird der Standardbericht generiert. 
5. Wählen Sie die Sprache aus. Alle Berichte werden in **en-us** und **ar-eg** übersetzt.
6. Geben Sie die Filiale und den Namen der Bank ein, bei der die Steuerzahlung erfolgen soll.
7. Wählen Sie den Geschäftstyp aus und geben Sie die Scheck- und Belegnummern ein. 
8. Geben Sie den Entitätstyp ein. 
9. Geben Sie den Namen der registrierten Person ein, um das Formular zuzuweisen, und wählen Sie **OK**, um die Berichterstellung zu bestätigen. 

 
[!INCLUDE[footer-include](../../includes/footer-banner.md)]
