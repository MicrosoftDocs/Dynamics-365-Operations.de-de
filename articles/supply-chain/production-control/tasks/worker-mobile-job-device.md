--- 
title: "Eine Arbeitskraft konfigurieren, die das mobile Einzelvorgangsgerät verwendet"
description: "Dieses Verfahren zeigt Ihnen an, wie Sie richtigen Rollen zu einem Benutzerkonto einer Arbeitskraft zuzuordnen und dann die Arbeitskraft für Fertigungsbereichregistrierungen aktivieren."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysUserManagement, HcmWorker, JmgRegistrationSetupTouch, JmgRegistrationSetupAssignUsers
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: dadf0e87eac8522f61bb094c146e37f46a21fc09
ms.openlocfilehash: f9de2f79c68fead5ede714ff05bba97118874aad
ms.contentlocale: de-de
ms.lasthandoff: 02/06/2018

---
# <a name="configure-a-worker-using-the-mobile-job-device"></a>Eine Arbeitskraft konfigurieren, die das mobile Einzelvorgangsgerät verwendet

[!include [task guide banner](../../includes/task-guide-banner.md)]

Dieses Verfahren zeigt Ihnen an, wie Sie richtigen Rollen zu einem Benutzerkonto einer Arbeitskraft zuzuordnen und dann die Arbeitskraft für Fertigungsbereichregistrierungen aktivieren.


## <a name="assign-roles-to-user-account"></a>Zuweisen von Rollen zum Benutzerkonto
1. Wechseln Sie zu "Systemverwaltung" > "Benutzer" > "Benutzer".
2. Verwenden Sie den Schnellfilter, um nach dem Namen einer Arbeitskraft zu filtern, deren Benutzerkonto der Rolle Maschinist zugeordnet ist. In den Beispieldaten wäre der Name "Shannon".
3. Markieren Sie den Benutzerkontodatensatz.
4. Klicken Sie in der Liste auf den Link "Name" in der ausgewählten Zeile, um die Details des Benutzerkontos anzuzeigen.
5. Wählen Sie in der Struktur "Rollen\Maschinist" aus.
6. Schließen Sie die Seite "Benutzerkontodetails".
7. Schließen Sie die Seite.

## <a name="configure-worker-account"></a>Konfigurieren von Arbeitskräftekonten
1. Wechseln Sie zu "Personalverwaltung" > "Arbeitskräfte" > "Arbeitskräfte".
2. Verwenden Sie den Schnellfilter, um nach dem Namen einer Arbeitskraft zu filtern, deren Benutzerkonto der Rolle Maschinist zugeordnet ist. In den Beispieldaten wäre der Name "Shannon".
3. Markieren Sie den Benutzerkontodatensatz.
4. Klicken Sie in der Liste auf den Link "Name" in der ausgewählten Zeile, um die Details des Benutzerkontos anzuzeigen.
5. Klicken Sie auf die Registerkarte "Anstellung".
6. Erweitern Sie das Zeiterfassungs-Inforegister und klicken auf "In Erfassungsterminals aktivieren".
7. Klicken Sie auf "In Erfassungsterminals aktivieren".
8. Geben Sie im Feld "Berechnungsgruppe" einen Wert ein oder wählen Sie einen Wert aus.
9. Geben Sie im Feld "Standardberechnungsgruppe" einen Wert ein oder wählen Sie einen Wert aus.
10. Geben Sie im Feld "Genehmigungsgruppe" einen Wert ein oder wählen Sie einen Wert aus.
11. Geben Sie im Feld "Standardprofil" einen Wert ein, oder wählen Sie einen Wert aus.
12. Geben Sie im Feld "Profilgruppe" einen Wert ein oder wählen Sie einen Wert aus.
13. Klicken Sie auf "OK".
14. Klicken Sie auf "Bearbeiten", um eine Nummer auf der Kennkarte für die neue Zeiterfassungsarbeitskraft einzugeben.
15. Geben Sie im Feld "Kennkartenkennung" einen Wert ein.
16. Klicken Sie auf Speichern.
17. Verwenden Sie das Tastenkürzel SaveRecord.
18. Schließen Sie die Seite "Arbeitskräftedetails".
19. Schließen Sie die Seite.

## <a name="assign-worker-to-device-group"></a>Zuweisen von Arbeitskräften zu Gerätegruppen
1. Wechseln Sie zu "Produktionssteuerung" > "Einrichtung" > "Fertigungssteuerung" > "Einzelvorgangsliste für Geräte konfigurieren".
2. Klicken Sie auf Hinzufügen.
3. Markieren Sie in der Liste die ausgewählte Zeile.
4. Klicken Sie auf "OK".
5. Klicken Sie auf "Bearbeiten".
6. Im Feld "Produktionseinheits" können Sie den standardmäßigen Filter für die Arbeitskraft festlegen. Dadurch wird sichergestellt, dass nur Produktions-Einzelvorgänge für die ausgewählte Produktionseinheit angezeigt werden, wenn die Arbeitskraft sich beim Gerät anmeldet.
7. Schließen Sie die Seite.


