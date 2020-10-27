---
title: Eine Arbeitskraft konfigurieren, die das mobile Einzelvorgangsgerät verwendet
description: In diesem Thema wird erklärt, wie Sie dem Benutzerkonto einer Arbeitskraft die richtigen Rollen zuweisen und dann die Arbeitskraft für Fertigungsbereichregistrierungen aktivieren.
author: ShylaThompson
manager: tfehr
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, HcmWorker, JmgRegistrationSetupTouch, JmgRegistrationSetupAssignUsers
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ada42a98a8a87e377f939d063b17f9904f6b3408
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3978233"
---
# <a name="configure-a-worker-using-the-mobile-job-device"></a>Eine Arbeitskraft konfigurieren, die das mobile Einzelvorgangsgerät verwendet

[!include [banner](../../includes/banner.md)]

In diesem Thema wird erklärt, wie Sie dem Benutzerkonto einer Arbeitskraft die richtigen Rollen zuweisen und dann die Arbeitskraft für Fertigungsbereichregistrierungen aktivieren.

## <a name="verify-that-a-worker-is-assigned-a-certain-role"></a>Überprüfen, ob einer Arbeitskraft eine bestimmte Rolle zugewiesen ist

Bei diesem Beispiel sollen Sie überprüfen, ob dem Benutzer „SHANNON“ die Maschinistenrolle zugewiesen ist, bevor Sie das Arbeitskraftkonto konfigurieren.

1. Wechseln Sie zu **Navigationsbereich > Module > Systemverwaltung > Benutzer > Benutzer**.
2. Suche im Schnellfilter nach einem Benutzer. Geben Sie für dieses Beispiel `shannon` ein.
3. Wählen Sie den Link in der Spalte **Benutzerkennung** des Benutzerkontos aus, das angezeigt wird.
4. Wählen Sie in der Struktur **Benutzerrollen** den Eintrag **Rollen> Maschinist** aus.
5. Schließen Sie die Seiten **Benutzerdetails** und **Benutzer**, um zur Startseite zurückzukehren.

## <a name="configure-worker-account"></a>Arbeitskräftekonten konfigurieren
1. Wechseln Sie zu **Navigationsbereich > Module > Personalverwaltung > Arbeitskräfte > Arbeitskräfte**.
2. Suche im Schnellfilter nach einem Benutzer. Geben Sie für dieses Beispiel `shannon` ein.
3. Wählen Sie den Link in der Spalte **Name** des Benutzerkontos aus, das angezeigt wird.
4. Wählen Sie die Registerkarte **Zeiterfassung** aus.
5. Wählen Sie **In Erfassungsterminals aktivieren** aus.
6. Geben Sie in den folgenden Feldern Werte ein, oder wählen Sie Werte aus:  

    - **Berechnungsgruppe**  
    - **Standardberechnungsgruppe**  
    - **Genehmigungsgruppe**  
    - **Standardprofil**  
    - **Profilgruppe**  

7. Wählen Sie **OK**.
8. Wählen Sie **Bearbeiten** aus, um eine Kennkartennummer für die neue Zeiterfassungsarbeitskraft einzugeben. Geben Sie im Feld **Kennkartenkennung** einen Wert ein.
9. Wählen Sie **Speichern**.
10. Schließen Sie die Seiten **Details zur Arbeitskraft** und **Arbeitskräfte**.

## <a name="assign-worker-to-device-group"></a>Arbeitskräfte zu Gerätegruppen zuweisen
1. Wechseln Sie zu **Produktionssteuerung > Einstellungen > Fertigungssteuerung > Einzelvorgangsliste für Geräte konfigurieren**.
2. Wählen Sie **Hinzufügen** aus.
3. Wählen Sie in der Liste die gewünschte Arbeitskraft aus. Wählen Sie für dieses Beispiel **SHANNON** aus.
4. Wählen Sie **OK**.
5. Wählen Sie **Bearbeiten** aus.
6. Im Feld **Produktionseinheit** können Sie den Standardfilter für die Arbeitskraft festlegen. Dadurch wird sichergestellt, dass nur Produktions-Einzelvorgänge für die ausgewählte Produktionseinheit angezeigt werden, wenn die Arbeitskraft sich beim Gerät anmeldet. Geben Sie den gewünschten Wert ein.
7. Schließen Sie die Seite.

