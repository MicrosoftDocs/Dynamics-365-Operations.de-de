---
title: Steuerberechnungen importieren und exportieren
description: Dieses Thema enthält Informationen zu den Import‑ und Exportfunktionen des Steuerberechnungsdienstes.
author: Kai-Cloud
ms.date: 11/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-11-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 02ad47b5f350969b4935a8f383ddf26a7ce7a46a
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8690889"
---
# <a name="import-and-export-tax-calculations"></a>Steuerberechnungen importieren und exportieren

Dieses Thema enthält Informationen zu den Import‑ und Exportfunktionen des Steuerberechnungsdienstes. Diese Funktionalität trägt zu einem flexiblen und effizienten Konfigurationserlebnis bei.

## <a name="import-and-export-tax-codes"></a>Steuercodes importieren und exportieren

### <a name="export-templates"></a>Vorlagen exportieren

1. Melden Sie sich beim [Regulatory Configuration Service (RCS)](https://marketing.configure.global.dynamics.com/) an.
2. Wählen Sie im Arbeitsbereich **Globalisierungsfunktionen** die Funktion **Funktionen** und wählen Sie die Kachel **Steuerberechnung** aus.
3. Wählen Sie eine bestehende Funktion aus oder [erstellen Sie eine neue Funktion](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs).
4. Wählen Sie im Raster **Versionen** die Option **Bearbeiten**.
5. Auf der Funktionsseite **Steuerberechnung** stellen Sie die [Konfigurationsversion](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs) ein.
6. Wählen Sie auf der Registerkarte **Steuercodes** **Importieren** aus.
7. Wählen Sie **Steuercodevorlage exportieren** aus, um die Datei **TaxCodesTemplate.zip** herunterzuladen.
8. Entpacken Sie **TaxCodesTemplate.zip**. Die Steuercodevorlagen werden separat gemäß **Berechnungsherkunft**-Wert komprimiert.
9. Entpacken Sie **By Net Amount.zip**, um die folgenden CSV-Dateien abzurufen:

    - **TaxCode.csv** – Geben Sie die Steuercodes ein.
    - **TaxLimit.csv** – Geben Sie die Steuergrenzen für jeden Steuercode ein.
    - **TaxRate.csv** – Geben Sie die Steuersätze für jeden Steuercode ein.

> [!NOTE]
> Standardmäßig sind Einträge für den **Beispiel**-Steuercode in den Vorlagen verfügbar. Wenn der **Beispiel**-Steuercode nicht aus den CSV-Dateien entfernt wird, wird er in die Funktion importiert.

### <a name="import-tax-codes"></a>Steuercodes importieren

Befolgen Sie diese Schritte, um den **Beispiel**-Steuercode in der Vorlage in Ihre Steuerberechnungsfunktion zu importieren.

1. Wählen Sie in RCS auf der Funktionsseite **Steuerberechnung** auf der Registerkarte **Steuercodes** die Option **Importieren** aus.
2. Wählen Sie **Durchsuchen**, suchen und wählen Sie die Datei **TaxCode.csv** und wählen Sie dann im Feld **Zieltabelle** die Option **Steuercode** aus.
3. Wählen Sie **OK** aus, um den Steuercode zu importieren.
4. Suchen und wählen Sie die Datei **TaxRate.csv** und wählen Sie dann im Feld **Zieltabelle** die Option **Steuersatz** aus.
5. Wählen Sie **OK** aus, um den Steuersatz zu importieren.
6. Suchen und wählen Sie die Datei **TaxLimit.csv** und wählen Sie dann im Feld **Zieltabelle** die Option **Steuergrenze** aus.
7. Wählen Sie **OK** aus, um die Steuergrenze zu importieren.

Sie können die ZIP-Datei, die alle drei CSV-Dateien enthält, auch direkt importieren. Auf diese Weise können Sie den Import schnell und einfach abschließen.

1. Wählen Sie in RCS auf der Funktionsseite **Steuerberechnung** auf der Registerkarte **Steuercodes** die Option **Importieren** aus.
2. Wählen Sie **Durchsuchen**, suchen und wählen Sie die Datei **By Net Amount.zip** und wählen Sie dann **OK**.

### <a name="export-tax-codes"></a>Steuercodes exportieren

1. Wählen Sie in RCS auf der Funktionsseite **Steuerberechnung** auf der Registerkarte **Steuercodes** die Option **Exportieren** aus.

    Die Schaltfläche **Export** ist verfügbar, wenn mindestens ein Steuercode im Raster **Steuercodes** ist.

2. Wählen Sie **OK**, um alle Steuercodes der Funktion in eine ZIP-Datei zu exportieren.

> [!NOTE]
> Verwenden Sie die exportierte Datei als Vorlage, um Steuercodes in die entsprechende Funktion zu importieren.

## <a name="import-and-export-applicability-rules"></a>Anwendbarkeitsregeln importieren und exportieren

### <a name="export-applicability-rules"></a>Anwendbarkeitsregeln exportieren

1. Melden Sie sich bei [RCS](https://marketing.configure.global.dynamics.com/) an.
2. Wählen Sie im Arbeitsbereich **Globalisierungsfunktionen** die Funktion **Funktionen** und wählen Sie die Kachel **Steuerberechnung** aus.
3. Wählen Sie eine bestehende Funktion aus oder [erstellen Sie eine neue Funktion](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs).
4. Wählen Sie im Raster **Versionen** die Option **Bearbeiten**.
5. Auf der Funktionsseite **Steuerberechnung** stellen Sie die [Konfigurationsversion](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs) ein.
6. Wählen Sie auf der Registerkarte **Anwendbarkeit der Steuergruppe** die Zeilen im Raster **Anwendbarkeit der Steuergruppe einrichten** aus.
7. Wählen Sie die Schaltfläche **Öffnen in Microsoft Office** und wählen Sie dann **Dynamische Anwendbarkeitsmatrix für Steuerdienst**.

    [![Exportieren Sie die Anwendbarkeitsregeln zu Microsoft Excel auf der Steuerberechnung-Funktionsseite.](./media/tax-cal-import-export-1.png)](./media/tax-cal-import-export-1.png)

8. Wählen Sie **Herunterladen**, um die ausgewählten Zeilen in ein Microsoft Excel-Arbeitsblatt zu exportieren.

### <a name="import-applicability-rules"></a>Anwendbarkeitsregeln importieren

Das heruntergeladene Excel-Arbeitsblatt enthält die Struktur des Rasters **Anwendbarkeit der Steuergruppe einrichten**. Sie können neue Regeln direkt im Arbeitsblatt hinzufügen. Wenn Sie fertig sind, führen Sie diese Schritte aus, um die neuen Regeln wieder in das Raster **Anwendbarkeit der Steuergruppe einrichten** zu importieren.

1. Wählen Sie im Excel-Arbeitsblatt die zu importierenden Zeilen aus und kopieren Sie sie.
2. Wählen Sie in RCS auf der Funktionsseite **Steuerberechnung** auf der Registerkarte **Anwendbarkeit der Steuergruppe** die Option **Hinzufügen** aus, um einen leeren Datensatz am unteren Rand des Rasters **Anwendbarkeit der Steuergruppe einrichten** einzufügen.
3. Wählen Sie **Strg+V** aus, um die kopierten Zeilen in das Raster einzufügen.
4. Wählen Sie **Speichern** aus.
