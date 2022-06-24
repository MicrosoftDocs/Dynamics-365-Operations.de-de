---
title: Verknüpfungen von Human Resources zu einer anderen Umgebung erstellen
description: In diesem Artikel wird erläutert, wie Sie einen Link von Microsoft Dynamics 365 Human Resources zu einer anderen Dynamics 365-Umgebung erstellen.
author: twheeloc
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-29-11
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0c9efae1061e96c0c42d5ca6a100bb36889ce56b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859665"
---
# <a name="create-links-from-human-resources-to-another-finance-environment"></a>Verknüpfungen von Human Resources zu einer anderen Finance-Umgebung erstellen

Ein Kunde hat möglicherweise zwei Dynamics 365-Umgebungen, in denen er arbeitet. Als Beispiel könnte der Kunde eine Dynamics 365 Human Resources-Umgebung in der Finance-Infrastruktur haben und eine Verbindung zu einer anderen Dynamics 365 Finance-Umgebung herstellen müssen. 

Diese Funktion ermöglicht Links von einer Human Resources-Seite zu einer bestimmten Seite in einer anderen Finance-Umgebung. Wenn die Links konfiguriert werden, können Sie angeben, wo der Link in Human Resources verfügbar sein wird und welche Zielseite in der anderen Umgebung geöffnet wird.

> [!Note] 
> Sie müssen **Verbesserungen der Benutzererfahrung für das Personalwesen** in **Funktionsverwaltung** aktivieren, um diese Funktion zu erhalten.

## <a name="configure-target-systems"></a>Zielsystem konfigurieren

In Human Resources können Systemadministratoren Links definieren, die auf **Human Resources**-Seiten angezeigt werden. Teile der Konfiguration sind Finance-Umgebungen, zu denen Sie als Ziel des Links wechseln möchten. 

So konfigurieren Sie das Zielsystem:
1. Wählen Sie auf der **Links konfigurieren**-Seite **Zielsystem konfigurieren** aus.  
2. Geben Sie den Zielsystemnamen ein und die URL der Finance-Umgebung an. Nachdem Sie Ihre Zielsysteme konfiguriert haben, können Sie die Links definieren.

## <a name="configure-links"></a>Links konfigurieren

Jeder Link, der erstellt wird, besitzt die folgenden definierten Informationen:
 - **Link**: Name des Links. Nur zur Kennung verwendet.
 - **Diese Verknüpfung aktivieren**: Legen Sie die Option auf **Ja** fest, wenn Sie den Link für Benutzer von Human Resources anzeigen möchten.
 - **Anzeigename**: Geben Sie den Namen ein, der als Verknüpfung zur sekundären Umgebung angezeigt wird. 
 - **Oberflächenverknüpfung auf Formular**: Wählen Sie aus, auf welcher Seite Sie den Link anzeigen möchten. Links können nur im Arbeitsbereich **Mitarbeiter-Self-Service** und auf den Seiten **Stelle**, **Position**, **Arbeitskraft** und **Optimierte Arbeitskraft** angezeigt werden.
 - **Gruppe**: Sie können Ihre Links mithilfe von Gruppen organisieren. Wählen Sie eine vorhandene Gruppe aus oder erstellen Sie eine neue mithilfe der Spalte **Gruppe**.
 - **Zielsystem**: Wählen Sie das Zielsystem aus, das mithilfe der Option **Zielsystem konfigurieren** erstellt wurde. Dies ist die sekundäre Umgebung, die verwendet wird, wenn Sie mithilfe des Links navigieren.
 - **Aktuelles Unternehmen des Benutzers verwenden**: Wählen Sie **Ja** aus, um das aktuelle Unternehmen des Benutzers zu verwenden, wenn Sie zu Finance navigieren. Wählen Sie **Nein** aus, um das Unternehmen auszuwählen, das verwendet werden soll.
 - **Ziel**-Menüelement: Geben Sie das Menüelement der Finance-Umgebung ein, das der Link zur Navigation verwenden soll. Menüpunkte, zu denen Sie direkt navigieren können, sind verfügbar. 

   So finden Sie das gewünschte Menüelement:
   1. Gehen Sie zur Finance-Umgebung und öffnen Sie die Seite, die das Ziel der Navigation ist. 
   2. Kopieren Sie die Menüoption aus der URL. Wenn Sie möchten, dass Sie mit dem Link zur Mitarbeiterliste in Finance and Operations gelangen, geben Sie den Wert ein, der nach " &mi " in der URL angezeigt wird. 
   3. Die Menüoption, um zur Mitarbeiterlistenseite in diesem Beispiel zu navigieren ist: HcmWorkerListPage_Employees.

 - **Verknüpfung zur Datenquelle**: Wählen Sie die Quelle der Daten aus, auf die die Verknüpfung verweist. Die häufigsten Gründe sind wie **Arbeitskraft** und **Position** sind verfügbar

### <a name="access-to-links"></a>Zugriff zu Links

Systemadministratoren finden die neu erstellten Links auf den festgelegten Seiten, selbst wenn die Option **Diesen Link aktivieren** auf **Nein** festgelegt ist. Dies kann zum Testen von Links verwendet werden, bevor diese für andere Mitarbeiter verwendet werden. Alle anderen Rollen sehen nur die konfigurierten Links, nachdem die Option **Diese Verknüpfung aktivieren** auf **Ja** festgelegt ist. Mitarbeiter, die Zugriff auf die Seiten haben, bei denen die Links überzogen werden, besitzen Zugriff auf Links.

Benutzer müssen außerdem über Sicherheitsrechte innerhalb der definierten sekundären Umgebung verfügen, um auf die Seiten in dieser Umgebung zugreifen zu können. Wenn dies nicht der Fall, wird ein Sicherheitsdialogfeld angezeigt, sofern der Link verwendet wird.

