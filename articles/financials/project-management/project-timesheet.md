---
title: Mobile Projektarbeitszeitnachweis-Anwendung
description: Dieses Thema enthält Informationen zu Microsoft Dynamics 365 Project Timesheet mobilen Anwendung Mit der Projektarbeitszeitnachweis-App können Beutzer Arbeitszeitnachweise für Projekte auf ihrem mobilen Gerät senden und genehmigen.
author: abruer
manager: AnnBe
ms.date: 04/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: josaw1
ms.dyn365.ops.version: 10
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: a475085001b8fa10814c864ef35129eb6ebfdfef
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1529878"
---
# <a name="microsoft-dynamics-365-project-timesheet-mobile-application"></a>Microsoft Dynamics 365 Project Timesheet mobile Anwendung

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Übersicht

Mit der Microsoft Dynamics 365 Project Timesheet mobilen App können Beutzer Arbeitszeitnachweise für Projekte auf ihrem mobilen Gerät senden und genehmigen (iPhone oder Android). Die Oberflächen der Arbeitszeitnachweis-Funktion dieser App für das Mobile, die sich in der Projektverwaltung und in Buchhaltungsbereichen von Microsoft Dynamics 365 for Finance and Operations befindet, verbessert die Benutzerproduktivität sowie die Effizienz und ermöglicht den fristgerechten Eintrag und die Genehmigung von Projektarbeitszeitnachweisen.

## <a name="download-and-install-the-mobile-app"></a>Herunterladen und Installieren der mobilen App

Laden und installieren Sie die Microsoft Dynamics 365 Project Timesheet mobile App für Android oder iPhone aus dem entsprechenden Shop für Ihr Gerät herunter.

## <a name="enable-the-app"></a>App aktivieren 

In Dynamics 365 for Finance and Operations muss die mobile Projektarbeitszeit-App aktiviert werden. Um die Funktionen zu aktivieren gehen Sie zu **Projektverwaltungs- und Buchhaltungsparameter \> Arbeitszeitnachweis** und wählen Sie  **aktivieren der Microsoft Dynamics 365 Project Timesheet** Parameter.

## <a name="sign-in-to-the-app"></a>Bei der mobile App anmelden

1.  Starten Sie die App auf Ihrem mobilen Gerät.

2.  Geben Sie die Microsoft Dynamics 365 for Finance and Operations URL ein.

3.  Bei der erstmaligen Anwendung werden Sie nach Ihrem Benutzernamen und dem Kennwort gefragt. Geben Sie Ihre Anmeldeinformationen ein.

4.  Sie werden bei Ihrem Standardunternehmen angemeldet.

## <a name="submit-a-project-timesheet"></a>Einen Projekt-Arbeitszeitnachweis übermitteln

Sie können einen Projektarbeitszeitnachweis in der App erstellen und übermitteln. Sie können einen neuen Arbeitszeitnachweis auch auf Informationen aus einem vorherigen Arbeitszeitnachweis, gespeicherten Positionen oder Projektzuweisung basieren. Wenn Sie als Stellvertreter ausgewählt werden, können Sie außerdem Arbeitszeitnachweise für eine andere Arbeitskraft eingeben. Um einen Arbeitszeitnachweis als Stellvertreter zu erstellen, wählen Sie die Schaltfläche **Menü** und wählen Sie anschließend einen Ressourcennamen. aus.

Die Arbeitszeitnachweisseite wird einen neuen Arbeitszeitnachweis für die Arbeitszeitnachweisperiode erstellen, auf der das aktuelle Datum basiert. Die Arbeitswoche wird angezeigt. Wenn die Arbeitszeitnachweisperiode mehrere Wochen umfasst, können Sie in der Registerkarte Arbeitswoche eine andere Arbeitswoche auswählen.
Wenn ein Arbeitszeitnachweis für das aktuelle Datum vorhanden ist, wird er angezeigt. Wenn Sie einen neuen Arbeitszeitnachweis in einer anderen Arbeitszeitnachweisperiode erstellen müssen, wählen Sie die Schaltfläche **Menü** und wählen Sie anschließend **Neuer Arbeitszeitnachweis** aus.

Projektinformationen können eingegeben werden, indem Sie auf die Aktivität **Zeit hinzufügen** oder die Aktivität **Zeit koperen von** klicken. Die  Aktivität **Kopienzeit von** wird die Projektzeileninformationen kopieren, nicht aber die Stunden. Das Menü **Zeit kopieren von** enthält die folgenden Optionen.

- **Aus bestehendem Arbeitszeitnachweis kopieren** – Kopiert Arbeitsnachweispositionen aus einem vorhandenen Arbeitszeitnachweis.

- **Aus Favoriten kopieren** – Erstellen Sie neue Arbeitszeitnachweise-Zeilen, indem Sie die Arbeitszeitnachweise verwenden, die Sie als Favoriten ausgewählt haben.

- **Aus der Zuordnung kopieren** - Erstellen Sie neue Arbeitszeitnachweis-Zeilen von zugewiesenen Projekten.

Die Projektinformation, die angezeigt wird, ist vom mobilen Parameter abhängig, den Sie auf der Seite **Projektverwaltungs- und Buchhaltungsparameter** definiert haben.

Wählen Sie im Feld **Juristische Entität** die juristische Person aus, für die Sie die Projektarbeit ausgeführt haben. Das Feld **Juristische Entität** ist nur verfügbar, wenn die Unterstützung von Intercompany-Arbeitszeitnachweisen für die juristische Person aktiviert wurde.

Wählen Sie die Arbeitskraft aus, die dem Projekt für den Arbeitszeitnachweis zugeordnet ist. Für die erste Version von Android wird die Erfassung vom Debitor nicht unterstützt, da Sie das Projekt zuerst auswählen müssen. Wenn Sie das Projekt zuerst ausgewählt haben, wird das Feld **Debitor** automatisch ausgefüllt.

Wählen Sie im Feld **Projekt** das Projekt aus, für das Sie die Zeit eingeben möchten. Das Feld **Debitor** wird automatisch ausgefüllt.

Die Debitoren- und Projektsuchen aktivieren die Suche in Debitoren und Projekten.

Hier können Sie spezifische Kontoinformationen in den Feldern **Kategorie**, **Aktivität**, **Abrechnungscode**, **Mehrwertsteuergruppe** und **Artikel-Mehrwertsteuergruppe** auswählen. Diese Felder können überschrieben werden.

Das Feld **Abrechnungscode** wird in einen Standardwert basierend auf den Projektverwaltungs- und Buchhaltungsparametern festgelegt. Wenn  Projekt/Kategorie- und Kategorie/Ressourcenparameter aktiviert sind, wird der **Abrechnungscode** für den Standardwert festgelegt, den Sie für diese Überprüfung definiert haben. Wenn Projekt/Kategorie- und Kategorie/Ressourcenparameter nicht aktiviert sind, wird der **Abrechnungscode** zum Standard entsprechend dem Feld **Stadardabrechnungscode aktivieren** auf der Seite **Projektverwaltungs- und Buchhaltungsparameter**. Der **Eigenschaftswert**kann nicht überschrieben werden.

Wählen Sie einen Tag aus, um Zeit hinzuzufügen. Geben Sie die Anzahl der Stunden ein, die Sie jeden Tag gearbeitet haben.

Zum Hinzufügen von Kommentaren zu den Stunden, die Sie eingeben, klicken Sie auf **Kommentare hinzufügen** und geben Sie Kommentare für interne oder externe Benutzer bzw. für beide ein.
Interne Kommentare können von Projektmanagern angezeigt werden. Externe Kommentare sind in Rechnungen enthalten.

Wenn Sie die Zeile als Favorit speichern möchten, aktivieren Sie das Kontrollkästchen, und klicken Sie anschließend auf **Als Favorit speichern**.

Finanzdimensions- und Anhangsupport werden in der mobilen Anwendung nicht bereitgestellt.

Setzen Sie Projektpositionen nach Bedarf hinzu, um den Arbeitszeitnachweis abzuschließen.

Klicken Sie auf **Übermitteln**, um den Arbeitszeitnachweis für den Genehmigungsworkflow zu senden.

## <a name="review-timesheets"></a>Arbeitszeitnachweise überprüfen

Eine Liste der Arbeitszeitnachweise, die geprüft werden müssen, ist im Menü verfügbar. Diese Option ist nur verfügbar, wenn Sie als Workflowgenehmiger ausgewählt wurden. Sowohl Kopf- wie auch Positions-Genehmigungen werde unterstützt. Positionsebenegenehmigung bietet die Möglichkeit, eine oder mehrere Positionen zur Genehmigung zu markieren. Nach der Überprüfung der Arbeitszeitnachweisinformationen klicken Sie auf **Genehmigen**, **Delegieren** oder **Zurück**, um den Workflow fortzusetzen.
