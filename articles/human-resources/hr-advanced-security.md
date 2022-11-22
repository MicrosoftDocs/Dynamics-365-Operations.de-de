---
title: Zugriff auf Arbeitskräfte nach juristischer Person einschränken
description: In diesem Artikel wird erläutert, wie Sie den Arbeitskraftzugriff nach juristischer Person einrichten.
author: twheeloc
ms.date: 11/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSharedParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fadd2c34d31bbd259255596c06a8e7517f7a774b
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780391"
---
# <a name="restrict-access-to-workers-by-legal-entity"></a>Zugriff auf Arbeitskräfte nach juristischer Person einschränken

In diesem Artikel wird erläutert, wie Sie den Arbeitskraftzugriff nach juristischer Person einrichten.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Arbeitnehmer sind in juristischen Personen beschäftigt. Im Folgenden finden Sie einige Beispiele hierfür:

- Aaron Con ist bei der juristischen Person USSI beschäftigt.
- Ahmed Barnett ist bei der juristischen Person USMF beschäftigt.
- Alicia Thornber ist bei den juristischen Personen GLSI und USMF beschäftigt.

Abhängig von der Rolle eines Benutzers im Unternehmen benötigen sie möglicherweise Zugriff, um alle Mitarbeiter aller juristischen Personen anzuzeigen. Alternativ muss ein Benutzer möglicherweise eingeschränkt werden, sodass er nur Mitarbeiter in der juristischen Person sehen kann, auf die er Zugriff hat. Um zu steuern, welche Mitarbeiter ein Benutzer anzeigen kann, wählen Sie die **Beschränken Sie den Zugriff auf Mitarbeiterinformationen** Parameter auf der **Gemeinsame Parameter der Personalabteilung** Seite aus.

Beispielsweise hat ein Benutzer Zugriff auf die **Arbeiter** Seite und hat nur Zugriff auf die juristische Person USMF. In diesem Fall kann der Benutzer die folgenden Informationen für die Mitarbeiter in der vorherigen Liste anzeigen:

- Wenn die Funktion zum Einschränken des Zugriffs auf Mitarbeiterinformationen nicht aktiviert ist, kann der Benutzer Informationen für Aaron, Ahmed und Alicia anzeigen.
- Wenn die Funktion aktiviert ist, kann der Benutzer nur Informationen für Alicia und Ahmed anzeigen, da sie auch bei der juristischen Person USMF beschäftigt sind.

Die angezeigten Informationen variieren je nach verwendeter Anwendung.

## <a name="dynamics-365-human-resources-stand-alone"></a>Dynamics 365 Human Resources Eigenständig

Wenn die Funktion zum Einschränken des Zugriffs auf Mitarbeiterinformationen aktiviert ist, sieht der eingeschränkte Benutzer in einigen Listen, die den Namen des Mitarbeiters enthalten, einen leeren Wert.

Beispielsweise wird ein Benutzer, der nur Zugriff auf die juristische Person USMF hat, das folgende Verhalten erleben.

- In der **Aktive Positionen** Liste, ist die **Arbeitskraft** Spalte für Aarons Position leer, da der Benutzer keinen Zugriff auf Mitarbeiter in der juristischen Person USSI hat.
- Wenn der Benutzer den Namen des Mitarbeiters aufschlüsselt, wird eine leere **Arbeitskraft** Seite angezeigt.

## <a name="dynamics-365-human-resources-on-finance-infrastructure"></a>Dynamics 365 Human Resources in Finance-Infrastruktur

Wenn die Funktion zum Einschränken des Zugriffs auf Mitarbeiterinformationen aktiviert ist, sieht der eingeschränkte Benutzer in einigen Listen, die den Namen des Mitarbeiters.

Beispielsweise wird ein Benutzer, der nur Zugriff auf die juristische Person USMF hat, das folgende Verhalten erleben.

- In der **Aktive Positionen** Liste, zeigt die **Arbeitskraft** Spalte Aarons Namen an. Wenn der Benutzer den Mauszeiger über den Namen des Mitarbeiters bewegt, werden nur der Name und der Titel angezeigt.
- Wenn der Benutzer den Namen des Mitarbeiters aufschlüsselt, wird eine leere **Arbeitskraft** Seite angezeigt.

> [!TIP]
> Wenn Sie die Dynamics 365 Human Resources on Finance-Infrastruktur verwenden und möchten, dass eingeschränkte Benutzer leere Werte für Arbeiternamen sehen, können Sie das **Beschränken Sie den Zugriff auf Mitarbeiter** Sicherheitsprivileg für die Benutzerrollen auf der **Sicherheitskonfiguration** Seite anzeigen.

Nachdem diese Funktion aktiviert haben, müssen Sie einige zusätzliche Schritte ausführen, um Berechtigungen für jeden Benutzer festzulegen, der die Informationen nur eingeschränkt anzeigen können soll.

1. Wählen Sie auf der Seite **Benutzer** einen Benutzer aus.
2. Wählen Sie eine Rolle für den Benutzer aus. Die Option **Organisationen zuweisen** wird verfügbar.
3. Wählen Sie **Organisationen zuweisen** aus.
4. Wählen Sie auf der neuen Seite **Zugriff individuell auf spezifische Organisationen erteilen** und dann die Organisationen aus, auf die der Benutzer Zugriff haben soll.
5. Wiederholen Sie die Schritte 2 bis 4 für jede weitere Rolle des Benutzers, einschließlich der Systembenutzerrolle.

> [!NOTE]
> Die juristischen Entitäten, auf die ein Benutzer Zugriff hat, müssen in allen Rollen des Benutzers übereinstimmen.
