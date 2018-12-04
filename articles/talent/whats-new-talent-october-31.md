---
title: "Neuheiten oder Änderungen in Dynamics 365 for Talent Core HR (31. Oktober 2018)"
description: "In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 for Talent Core HR entweder neu oder geändert sind."
author: Darinkramer
manager: AnnBe
ms.date: 10/31/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: 0450326dce0ba6be99aede4ebc871dc58c8039ab
ms.openlocfilehash: c5acd09e25ecd5fefa637342f83d0ee0f1891402
ms.contentlocale: de-de
ms.lasthandoff: 11/01/2018

---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-october-31-2018"></a>Neuheiten oder Änderungen in Dynamics 365 for Talent Core HR (31. Oktober 2018)

[!include [banner](includes/banner.md)]

**Build 8.1.2031**

In diesem Thema werden die Funktionen beschrieben, die in Core HR entweder neu oder geändert sind.

## <a name="create-links-from-talent-to-finance-and-operations"></a>Links von Talent mit Finance and Operations erstellen
Diese neue Navigationsfunktionen ermöglicht es Ihnen, Talent mit Finance and Operations zu verknüpfen und so direkt zu den Seiten von Finance and Operations zu navigieren. Wenn Links konfiguriert wird, können Sie den Namen sowie die Gruppe des Links definieren, wo derder Link in Talent auftauchen soll, und die Zielseite, die in Finance and Operations geöffnet wird.

#### <a name="coming-soon"></a>Bald verfügbar
Feldkontext wird künftig hinzugefügt, um die direkte Navigation zu den entsprechenden Datensätze in Finance and Operations zuzulassen. Beispielsweise können Sie **Verknüpfung mit dem Feld** verwenden, um den Kontext bereitzustellen, um direkt zu einen bestimmten Mitarbeiter oder eine Position im Bereich Finance and Operations zu navigieren.

### <a name="configure-target-systems"></a>Zielsystem konfigurieren

In Talent können Systemadministratoren Links definieren, die durch den Systemverwaltungsarbeitsbereich überzogen werden. Teil der Konfiguration ist die Finance and Operations-Umgebung, zu der Sie als "Ziel" des Links wechseln möchten. Dazu geben Sie dem Zielsystem einen Namen und geben die URL der Finance and Operations-Umgebung an. Das folgende Beispiel einer Finance and Operations URL, die Sie bereitstellen würden:https://devax00124aos.cloud.test.dynamics.com/. Nachdem Sie Ihre Zielsysteme konfiguriert haben, können Sie die Links definieren.

### <a name="configure-links"></a>Links konfigurieren

Jeder Link, der erstellt wird, besitzt die folgenden definierten Informationen.

- Link - Name des Links, nur für die Kennung verwendet.

- Aktivieren Sie diesen Link - Legen Sie den Status auf **Ja** fest, wenn Sie den Link für Benutzer des Talents anzeigen möchten.

- Anzeigename - Hiermit legen Sie den Namen fest, der als Verknüpfung für Finance and Operations angezeigt wird. Diese Angaben werden momentan nicht übersetzt.

- Oberflächenlink im Formular - Wählen Sie aus, welcher Seite Sie anzeigen möchte auf dem Link.

- Gruppe - Gruppen sind erforderlich, aber wenn Sie die Links mit Gruppen organisieren möchten, wählen Sie eine vorhandene Gruppe aus oder erstellen Sie eine neue mithilfe des Felds **Gruppe**.

- Zielsystem - Aktivieren Sie das Zielsystem aus, das mithilfe der Option **Konfigurieren Sie Zielsystem** erstellt wurde. Dies ist die Umgebung von Finance and Operations, die verwendet wird, wenn Sie mithilfe des Links navigieren.

- Wählen Sie **Ja** wenn Sie den aktuellen Unternehmenskontext des Benutzers verwenden möchten, wenn Sie zu Finance and Operations navigieren. Wenn **Nein** aktiviert ist, können Sie das Unternehmen auswählen, das verwendet werden soll.

- Zielmenüoption - Geben Sie die Menüoption von Finance and Operations ein, für die der Link zur Navigation verwendet werden soll. Menüpunkte, zu denen Sie direkt navigieren können, sind verfügbar. Um die notwendige Menüoption zu finden, öffnen Sie Finance and Operations und öffnen Sie die Seite, die das Ziel der Navigation ist. Kopieren Sie die Menüoption aus der URL. Wenn Sie möchten, dass Sie mit dem Link zur Mitarbeiterliste in Finance and Operations gelangen, geben Sie den Wert ein, der nach " &mi " in der URL angezeigt wird. https://devax00124aos.cloud.test.dynamics.com/?p=USMF&mi=HcmWorkerListPage_Employees. Die Menüoption, um zur Mitarbeiterlistenseite in diesem Beispiel zu navigieren ist: HcmWorkerListPage_Employees.

- Link der Datenquelle - Wählen Sie die Quelle aus, auf die die Verknüpfung verweist. Die häufigsten Gründe sind wie **Arbeitskraft** und **Position** sind verfügbar

- Link zum Feld - (bald verfügbar). Diese Feldauswahl ermöglicht eine direkte Navigation von einem einzelnen Datensatz bis zu einem einzelen Datensatz in Finance and Operations.

### <a name="access-to-links"></a>Zugriff zu Links

Systemadministratoren finden die neu erstellten Links auf den festgelegten Seiten, selbst wenn die Option **Diesen Link aktivieren** auf **Nein** festgelegt ist. Dies kann zum Testen von Links verwendet werden, bevor diese für andere Mitarbeiter verwendet werden. Alle anderen Rollen sehen nur die konfigurierten Links, nachdem die Option **Aktivieren Sie diesen Link** auf **Ja** festgelegt ist. Mitarbeiter, die Zugriff auf die Seiten haben, bei denen die Links überzogen werden, besitzen Zugriff auf Links.

Benutzer können Sicherheitsrechte innerhalb von Finance and Oerations  haben, um auf die Seiten in Finance and Operations zuzugreifen. Wenn dies nicht der Fall, wird ein Sicherheitsdialogfeld angezeigt, sofern der Link verwendet wird.


## <a name="other-changesfixes"></a>Andere Änderungen/Korrekturen

### <a name="positions-with-a-future-start-date-cannot-be-assigned-to-a-new-employee"></a>Positionen mit einem zukünftigen Startdatum können nicht zugeordnet werden für einen neuen Mitarbeiter

Änderungen wurden gemacht, um Mitarbeiter-Zuweisungen für künftige terminierte Positionen zu ermöglichen. Positionen, deren Startdatum in der Zukunft liegt, können ausgewählt werden und die Mitarbeiter-Zuweisungen werden nach der Speicherung oder Beendigung des Workflows  gemacht (wenn der Workflow aktiviert ist).

### <a name="new-employee-cannot-be-assigned-existing-position"></a>Neuer Mitarbeiter kann vorhandener Position nicht zugewiesen werden

Änderungen können vorgenommen werden, damit eine neue Mitarbeiter-Zuweisung den bestehenden Positionen zugewiesen werden kann.

### <a name="seniority-dateoffice-location-disappears-when-the-employment-start-date-is-in-the-past-and-the-record-is-saved"></a>Dienstalter-Datum/Bürostandort verschwindet, wenn das Anfangsdatum der Beschäftigung in der Vergangenheit liegt und der Datensatz gespeichert wird

Änderungen können vorgenommen werden, um die Sichtbarkeit des **Senioritätsdatums** und des **Bürostandorts** zu korrigieren, wenn Änderungen für die letzten Mitarbeiter erfolgen.

### <a name="cant-enter-data-for-future-dated-employments-on-the-worker-page"></a>Daten für zukünftige Beschäftigungen können auf der Arbeitskraftseite nicht eingeben werden

Beschäftigungsdaten für zukünftige Beschäftigungen sind auf der Hauptarbeitskraftseite deaktiviert. Beschäftigungsdaten können durch die Seite **Datums-Manager** eingegeben werden. Zusätzliche Änderungen werden in künftigen Versionen vorgenommen, um die Eingabe von direkten Beschäftigungsdaten während des Workflowprozesses zu aktivieren.

### <a name="add-validfrom-and-validto-to-hcmpersonalcontactpersonentity"></a>Fügen Sie ValidFrom und ValidTo HcmPersonalContactPersonEntity hinzu

Die Datenverwaltungs-Framework (DMF)-Entität HcmPersonalContactPerson-Entität wurde aktualisiert, um "gültig ab" und "gültig bis"-Daten abzudecken, um bestimmte Vorteilsintegrationsszenarien zu aktivieren. 

## <a name="known-issue"></a>Bekannte Probleme
- **Abgang**: Wenn sie einer Arbeitskraft einen neuen Anhang hinzufügen, sind die Schaltflächen **Neu** und **Bearbeiten** ausgegraut. 
- **Problemumgehung:**, Bevor die Anhangseite geöffnet wird, stellen Sie sicher, dass die Infoboxen auf der Seite **Arbeitskraft** geschlossen sind. Wenn die Infoboxen geschlossen werden, wenn die **Arbeitskraft**-Seite geladen wird, werden die Anhangschaltflächen aktiviert. (Dieses Problem wird in der folgenden Plattformaktualisierung korrigiert.)

