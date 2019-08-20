---
title: Finanzberichte anzeigen
description: Dieses Thema beschreibt, wie Finanzberichte in Microsoft Dynamics 365 for Finance and Operations angezeigt und durchsucht werden. Er enthält Informationen zu den verschiedenen Optionen, die Sie auf Finanzberichte anwenden können, um das Erscheinungsbild und die Daten, die die Berichte enthalten, zu ändern.
author: kweekley
manager: AnnBe
ms.date: 03/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 10334
ms.assetid: d20f435f-fb65-4068-ab09-7efc7be683a6
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bce7c1b5e5780d68bde2130c25099cbaee1fa451
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834658"
---
# <a name="view-financial-reports"></a>Finanzberichte anzeigen

[!include [banner](../includes/banner.md)]

Dieses Thema beschreibt, wie Finanzberichte in Microsoft Dynamics 365 for Finance and Operations angezeigt und durchsucht werden. Er enthält Informationen zu den verschiedenen Optionen, die Sie auf Finanzberichte anwenden können, um das Erscheinungsbild und die Daten, die die Berichte enthalten, zu ändern.

<a name="financial-reporting-overview"></a>Überblick über die Finanzberichterstellung
----------------------------

## <a name="open-a-financial-report"></a>Öffnen eines Finanzberichts
Um einen Bericht zu öffnen, wählen Sie den Berichtsnamen aus. Wenn ein Bericht zum ersten Mal geöffnet wird, wird er automatisch für den vorherigen Monat generiert. Wenn Sie beispielsweise einen Bericht zum ersten Mal im August 2015 öffnen, wird der Bericht zum 31. Juli 2015 generiert. Nach dem Öffnen eines Berichts können Sie ihn durchsuchen, indem Sie Detailinformationen bestimmter Daten anzeigen und Berichtsoptionen ändern.

## <a name="drill-down-on-a-financial-report"></a>Anzeigen von Detailinformationen zu einem Finanzbericht
Finanzberichte können mehrere Detailebenen enthalten. Die Finanzebene ist die erste Ebene, die Sie sehen, wenn Sie einen Finanzbericht öffnen. Um zur Kontoebene zu wechseln, wählen Sie die Daten aus, für die Sie Details anzeigen möchten. Um beispielsweise die Kontodetails für Verkäufe anzuzeigen, wählen Sie die Verkaufsdaten aus, die Sie untersuchen möchten. Von der Kontoebene aus können Sie über die Anzeige von Details die Transaktionen anzeigen, die den Kontosaldo bilden. Es gibt zwei Möglichkeiten, um Transaktionen anzuzeigen: Berichtsbuchungen und Belegbuchungen.

-   **Berichtsbuchungen** – Transaktionen werden in einer formatierten Ansicht angezeigt, die im Finanzbericht enthalten ist. Um Transaktionen in der formatierten Ansicht anzuzeigen, wählen Sie die Daten aus, für die Details angezeigt werden sollen. Klicken Sie anschließend auf **Berichtbuchungs-Drillstufe**.
-   **Belegbuchungen** – Es wird eine Belegbuchungsanfrage geöffnet, in der Transaktionen angezeigt werden können. Um Transaktionen in der Belegbuchungsanfrage anzuzeigen, wählen Sie die Daten aus, für die Details angezeigt werden sollen. Klicken Sie anschließend auf **Kontotransaktionen öffnen**.

Wenn es sich um Budgetdaten handelt, können Sie die Budgetkontoeinträge öffnen. Um eine der Ebenen im Bericht zu schließen und zum Ausgangspunkt zurückzukehren, können Sie entweder die ESC-Taste drücken oder auf die Schaltfläche **Schließen** (**X**) oben rechts klicken.

## <a name="change-report-options"></a>Ändern von Berichtsoptionen
Sie können Attributs- und Dimensionsfilter anwenden oder das Budgetszenario in einem Bericht vom Typ **Istwert im Vergleich zu Budget** ändern. Klicken Sie im Aktivitätsbereich auf **Berichtsoptionen**, und führen Sie anschließend einen oder mehrere dieser Schritte aus:

-   Um Attributfilter auf einen Bericht anzuwenden, wählen Sie **Einen Attributfilter hinzufügen** aus. Wählen Sie das Attribut aus, geben Sie den Attributwert ein, und klicken Sie auf **OK**. Wenn Sie beispielsweise das Attribut **Kontokategorie** auswählen, geben Sie **VERKAUF** als Attributwert ein. Um einen Attributfilter zu entfernen, klicken Sie auf **Löschen**.
-   Um Dimensionsfilter auf einen Bericht anzuwenden, wählen Sie **Dimensionsfilter hinzufügen** aus. Wählen Sie die Dimension aus, und geben Sie anschließend entweder die Dimensionskennung ein oder wählen Sie die Dimension aus der Liste aus. Um einen Dimensionsfilter zu entfernen, klicken Sie auf **Löschen**.
-   Um das Szenario in einem Bericht vom Typ **Istwert im Vergleich zu Budget** zu ändern, wählen Sie ein neues Szenario aus, und klicken Sie anschließend auf **OK**. Wenn das ausgewählte Szenario für ein anderes Geschäftsjahr ist, werden keine Ergebnisse zurückgegeben. Wenn beispielsweise ein Bericht für FY2015 generiert wird und das aktuelle Szenario für FY2015 ist und das neue ausgewählte Szenario für FY2016 ist, werden keine Ergebnisse zurückgegeben. Wenn ein neues Szenario für einen anderen Geschäftsjahres benötigt wird, generieren Sie eine neue Version des Berichts für das Geschäftsjahr, das dem Szenario zugeordnet ist.

Wenn Sie auf **OK** klicken, werden alle Optionen, die Sie ausgewählt haben, auf den Bericht angewendet. Wenn Sie die ausgewählten Optionen doch nicht anwenden möchten, klicken Sie auf **Abbrechen**.

## <a name="update-a-financial-report"></a>Aktualisieren eines Finanzberichts
Sie können einen Finanzbericht aktualisieren, sodass die aktuellen Daten für die Periode und das Jahr angezeigt werden, für die der Bericht generiert wurde. Wenn Sie beispielsweise einen Finanzbericht aktualisieren, der für Oktober 2015 generiert wurde, spiegelt der Bericht alle neuen Transaktionen wider, die für Oktober 2015 gebucht wurden. Um einen Finanzbericht zu aktualisieren, klicken Sie im Aktivitätsbereich auf **Aktualisieren**. Ein aktualisierter Bericht steht nur für die Person zur Verfügung, die ihn aktualisiert hat. Damit andere Personen dieselben Daten anzeigen können, muss der Bericht veröffentlicht werden.

## <a name="publish-a-financial-report"></a>Veröffentlichen eines Finanzberichts
Nachdem Sie einen Finanzbericht aktualisiert haben, können Sie ihn veröffentlichen. Andere Personen in der Organisation können ihn dann anzeigen. Um einen Bericht zu veröffentlichen, klicken Sie im Aktivitätsbereich auf **Veröffentlichen**.

## <a name="display-a-financial-report-in-a-different-currency"></a>Anzeigen eines Finanzberichts in einer anderen Währung
Ein Finanzbericht kann jederzeit in jeder Währung angezeigt werden. Um einen Bericht in einer anderen Währung anzuzeigen, klicken Sie im Aktivitätsbereich auf **Währung** und wählen Sie dann eine Währung aus. Der Bericht wird in diese Währung konvertiert, und die Ergebnisse werden angezeigt. Alle Währungscodes oder Symbole, die im Rahmen des Berichtsentwurf enthalten sind, werden aktualisiert, um die neue Währung widerzuspiegeln. Die Währungen, die in der Liste angezeigt werden, sind die in Finance and Operations konfigurierten Berichtswährungen.

## <a name="display-a-summarized-view-of-the-financial-report"></a>Anzeigen einer zusammengefassten Ansicht des Finanzberichts
Ein Finanzbericht kann Detailpositionen und zusammengefasste Positionen enthalten. Detailpositionen sind Positionen, die Hauptkonten oder Dimensionen enthalten. Zusammengefasste Positionen sind Beschreibungs-, Gesamt- und Berechnungspositionen. Um nur die zusammengefassten Positionen eines Berichts anzuzeigen, klicken Sie auf **Anzeigen** und dann auf **Nur zusammengefasste Positionen**. Der Bericht wird reduziert, und es werden nur die zusammengefassten Positionen angezeigt. Um die Detailpositionen zusammen mit den zusammengefassten Positionen anzuzeigen, klicken Sie auf **Anzeigen** und dann erneut auf **Nur zusammengefasste Positionen**.

## <a name="print-a-financial-report"></a>Drucken eines Finanzberichts
Das Drucken eines Finanzberichts erstellt eine PDF-Datei, die dann manuell gedruckt werden kann. Um einen druckbaren Finanzbericht zu erstellen, klicken Sie im Aktivitätsbereich auf **Drucken**. Führen Sie dann einen oder mehrere der folgenden Schritte aus, um die Druckoptionen festzulegen:

-   Um die verschiedenen Detailebenen im gedruckten Bericht einzubeziehen, legen Sie den Schieberegler auf **Ja** oder **Nein** fest. Wenn ein Bericht eine Berichterstellungsstruktur verwendet, können Sie festlegen, ob alle Berichterstellungseinheiten oder nur die aktuelle Berichterstellungseinheit einbezogen werden sollen.
-   Um die Seitengröße festzulegen, wählen Sie eine Seitengröße in der Liste aus.
-   Um das Seitenlayout festzulegen, wählen Sie ein Layout in der Liste aus. Wenn der Berichtsinhalt an die ausgewählte Breite angepasst werden soll, legen Sie den Schieberegler auf **Ja** fest.
-   Um die Seitenränder festzulegen, geben Sie die Größe der Ränder für oben, unten, links und rechts in Zoll an.

Nachdem Sie die Druckoptionen festgelegt haben, klicken Sie auf **Drucken**, um fortzufahren. Sie werden aufgefordert, anzugeben, ob Sie die Datei herunterladen oder in OneDrive oder auf SharePoint speichern möchten. Wenn Sie doch noch nicht fortfahren möchten, klicken Sie stattdessen auf **Abbrechen**. Sobald Sie fortfahren, wird der Bericht auf dem Server gerendert und Sie werden aufgefordert, den Bericht im PDF-Format herunterzuladen. Sie können den Bericht nun in Ihrem PDF-Viewer anzeigen, den Drucker auswählen, an den der Bericht gesendet werden soll, und alle anderen Druckoptionen anpassen.

## <a name="export-a-financial-report"></a>Exportieren eines Finanzberichts
Um einen Finanzbericht zu exportieren, klicken Sie im Aktivitätsbereich auf **Exportieren**. Der Bericht wird in Microsoft Excel exportiert, und Ihr Browser fordert Sie auf, die exportierte Datei zu öffnen oder zu speichern. Die im Berichtsentwurf definierten Exporteinstellungen werden auf den exportierten Bericht angewendet.    

<a name="additional-resources"></a>Zusätzliche Ressourcen
--------

[Finanzberichterstellung](../../dev-itpro/analytics/financial-reporting-intro.md)




