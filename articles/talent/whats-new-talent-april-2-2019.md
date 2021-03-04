---
title: Neuigkeiten oder Änderungen in Dynamics 365 Talent (2. April, 2019)
description: In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 Talent entweder neu oder geändert sind.
author: Darinkramer
manager: AnnBe
ms.date: 04/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-04-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 04b5a006d4580fe419d81986a90851bc8d611722
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528218"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-april-2-2019"></a>Neuigkeiten oder Änderungen in Dynamics 365 Talent (2. April, 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

In diesem Thema werden die Funktionen beschrieben, die in Dynamics 365 Talent neu oder geändert wurden.

## <a name="changes-in-attract"></a>Änderungen in Attract

### <a name="approval-emails-in-attract"></a>Genehmigungs-E-Mails in Attract
Neue Genehmigungs-E-Mails verbessern die Sichtbarkeit im Genehmigungsprozess. E-Mails werden an genehmigende Personen gesendet, wenn eines der folgenden Szenarien werden ausgeführt wird:

- Ein Anforderer übermittelt eine Stelle zur Genehmigung.
- Eine Stelle wird entweder genehmigt oder abgelehnt.
- Ein Genehmiger hat nicht innerhalb von 24 Stunden auf die Genehmigungsanforderung reagiert.

Sie können den Inhalt von Genehmigungs-E-Mails mit neuen Vorlagen anpassen.

### <a name="application-and-profile-attachments"></a>Bewerbung und Profilanhänge
Verbesserungen an der Registerkarte **Dokumente** auf dem Bewerbungs- und Talentpoolprofil zeigt nun den Dokumentnamen und den Typ an.

## <a name="changes-in-onboard"></a>Änderungen in Onboard
Diese Version enthält kleinere Fehlerkorrekturen für Dynamics 365 Talent: Onboard.

## <a name="coming-soon-attract-and-onboard"></a>Bald verfügbar (Attract und Onboard)

### <a name="lifecycle-services-lcs-integration-with-report-a-problem"></a>LIfecycle Services (LCS) Integration mit "ein Problem melden"
In Attract und Onboard erstellen Probleme, die von den Endbenutzer mithilfe der Funktion "ein Problem melden" erfasst werden, nun automatisch Support-Probleme im LCS Projekt des Debitors. Administratoren können anschließend die Probleme selektieren und bei Bedarf an Microsoft senden. Dies ist konsistent damit, wie Core HR Probleme von Endnutzern behandelt.

## <a name="changes-in-core-hr"></a>Core HR-Änderungen
Die in diesem Abschnitt beschriebenen Änderungen gelten für Buildnummer 8.1.2216.

### <a name="platform-update-25-for-finance-and-operations"></a>Plattformupdate 25 für Finance and Operations
Weitere Informationen zum Plattformupdate 25 für Finance and Operations finden Sie unter [Vorschaufunktionen im Dynamics 365 for Finance and Operations-Plattformupdate 25 (April 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-25).

###  <a name="advanced-compensation-security-fixed-and-variable"></a>Erweiterte Vergütungssicherheit (feste oder variable)
In vielen Organisationen hat der Kompensations- und Vergütungsmanager nur Zugriff auf bestimmte Kompensationsdatensätze. Diese Datensätze enthalten möglicherweise Datensätze für Führungskräfte oder regionale Mitarbeiter. Diese Änderung gibt HR die Möglichkeit, Vergütungspläne für verschiedene Mitarbeitergruppen in der Organisation zu verwalten. Sie können den festen und variablen Vergütungsplänen Sicherheitsrollen zuweisen. Diese Sicherheitsrollen bestimmen den Zugriff auf Plänen und die zugehörigen Mitarbeiterdaten wie Gehalts- oder Bonusdatensätze, damit nur jene Rollen die Kompensation für Mitarbeitergruppen bearbeiten können.

### <a name="upgrade-to-common-data-service"></a>Upgrade auf Common Data Service
Die Fristen für das Upgrade auf Common Data Service kommen sehr schnell näher. Melden Sie sich im Microsoft Power Apps-Administratorcenter an, um zu bestimmen, ob die Datenbank aktualisiert werden muss. Weitere Informationen über die Termine und erforderlichen Schritte finden Sie unter [Upgrade auf Common Data Service](https://docs.microsoft.com/common-data-service/upgradecds/introduction-upgrade-cds).

## <a name="in-preview"></a>Vorschau

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>Ermöglichen Sie, dass Ursachencodes für Sonderurlaubstypen angegeben werden können
Organisationen brauchen möglicherweise zusätzliche Informationen zu Freizeitanforderungen. Sie können nun Ursachencodes für Sonderurlaubstypen definieren und Mitarbeiter aktivieren, damit sie einen Ursachencode für ihre Freizeitanforderungen auszuwählen können.

### <a name="require-reason-codes-for-certain-leave-types-on-time-off-requests"></a>Erfordert Ursachencodes für bestimmte Urlaubstypen bei Freizeitanforderungen
Organisationen brauchen ggf. bestimmte Ursachencodes für Sonderurlaubstypen, wenn Mitarbeiter Freizeit einreichen. Dies kann möglicherweise aufgrund der Unternehmensrichtlinie oder von gesetzlichen Vorgaben der Fall sein. Sie können nun angeben, welche Urlaubstypen einen Ursachencodes erfordern und Sie können von Mitarbeitern verlangen, dass sie einen Ursachencode für den Sonderurlaubstyp für ihre Freizeitanforderungen angeben.

## <a name="coming-soon"></a>Bald verfügbar

### <a name="improvements-to-the-user-interface-for-duplicate-employee-check"></a>Verbesserungen zur Benutzeroberfläche, um doppelten Mitarbeiter zu überprüfen
Mit dieser Änderung werden Duplikate erkannt, während Sie Namenfelder eingeben, und ein Status zeigt, wie viele Duplikate gefunden wurden. Sie können die zur Verfügung gestellte Verknüpfung aktivieren, um eine neue Seite zu öffnen, um zu prüfen, ob die gefundene Übereinstimmung verwendet werden soll. Das Duplikatsformular wird nicht automatisch geöffnet, damit die Dateneingabe nicht unterbrochen wird.

###  <a name="email-support-for-alerts"></a>E-Mail-Support für Warnungen
Mit der Plattformaktualisierung 25 für Finance and Operations können Benutzer Warnregeln erstellen, dass automatisch E-Mail-Benachrichtigungen an Kontakte gesendet werden, wenn dies von einem Ereignis ausgelöst wird. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]