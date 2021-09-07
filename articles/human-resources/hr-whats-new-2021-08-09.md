---
title: Was ist neu oder geändert in Dynamics 365 Human Resources 9. August 2021
description: Dieses Thema beschreibt Funktionen, die in Microsoft Dynamics 365 Human Resources für den 9. August 2021 neu sind oder geändert wurden.
author: marcelbf
ms.date: 08/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-08-09
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0f515b614aedce3d58994bf21104ada25702a71e
ms.sourcegitcommit: fc19ee0aba2a6174fef305d151f1eb23ca6c0346
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2021
ms.locfileid: "7385699"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-9-2021"></a>Was ist neu oder geändert in Dynamics 365 Human Resources 9. August 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dieses Thema beschreibt Funktionen, die in Microsoft Dynamics 365 Human Resources neu sind, geändert wurden oder demnächst erscheinen.

Weitere Informationen zu unserem Aktualisierungsprozess und Zeitplan finden Sie unter [Aktualisierungsprozess](hr-admin-setup-update-process.md).

Weitere Informationen zu neuen Funktionen und den voraussichtlichen allgemeinen Verfügbarkeitsterminen finden Sie unter [Überblick Dynamics 365 Human Resources 2021 Veröffentlichungszyklus 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>In dieser Version

Diese Version enthält die folgenden neuen Funktionen und Fehlerbehebungen. Änderungen gelten für Build-Nummer 8.1.4393.

### <a name="bug-fixes"></a>Fehlerkorrekturen

Die folgenden Fehlerkorrekturen sind in diesem Release enthalten.

> [!NOTE]
> Unser Ziel ist es, Ihnen diese Informationen so schnell wie möglich zukommen zu lassen. Möglicherweise aktualisieren wir dieses Thema, um Fehlerkorrekturen einzubeziehen, die es in den Build geschafft haben, nachdem dieses Thema ursprünglich veröffentlicht wurde.

| Problemnummer | Problem | Beschreibung |
| --- | --- | --- |
| 558385 | Der Standard-Beauftragte wird nicht ausgewählt, wenn die Option **Befehlsempfänger automatisch auswählen** für Standard-Beauftragte aktiviert ist. | Dieses Problem ist jetzt behoben. Mehrere Standard-Beauftragte werden in berechtigten Plänen automatisch ausgewählt, wenn die Option **Automatische Auswahl von Beauftragten** auf der Seite **Human Resources gemeinsame Parameter** eingeschaltet ist. |
| 589617 | Auf der Seite **Auszeit** sind die Salden **Verfügbar zum Kaufen** und **Verfügbar zum Verkaufen** leer, wenn der Zugriff auf eine bestimmte Firma beschränkt ist. | Dieses Problem ist jetzt behoben. Die Seite **Zeit aus** zeigt die korrekten **Verfügbar zum Kaufen** und **Verfügbar zum Verkaufen**-Salden, wenn der Benutzer auf eine bestimmte Firma beschränkt ist. |

## <a name="in-preview"></a>Vorschau

Die folgenden neuen Funktionen stehen in der Vorschau zur Verfügung. Weitere Informationen über das Ein- und Ausschalten von Funktionen finden Sie unter [Funktionen verwalten](hr-admin-manage-features.md).

| Funktion | Freigabeplan | Dokumentation |
| --- | --- | --- |
| Arbeitsbereich für Vorteilsverwaltung | [Arbeitsbereich für die Verwaltung von Zusatzleistungen (Vorschau)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Arbeitsbereich „Vorteilsverwaltung“](hr-benefits-management-workspace.md) |
| Ermöglicht eine vereinfachte Integration der Gehaltsabrechnung (APIs zur Integration der Gehaltsabrechnung) | [Ermöglichen Sie eine vereinfachte Integration mit Gehaltsabrechnungsanbietern](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Lohnintegrations-API](hr-admin-integration-payroll-api-introduction.md)|
| Aktivieren Sie einen Abwesenheitsmanager, um den Urlaub zu verwalten | [Aktivieren Sie einen Abwesenheitsmanager, um den Urlaub zu verwalten](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) | In diesem Release aktualisieren wir die Ansicht des Arbeitsbereichs des Abwesenheitsmanagers. Weitere Informationen finden Sie unter [Rolle des Abwesenheitsmanagers konfigurieren](https://go.microsoft.com/fwlink/?linkid=2168107). |
| Anhangsanforderung pro Urlaubsart konfigurieren | [Anhangsanforderung pro Urlaubsart konfigurieren](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/mandate-attachments-specific-leave-types) |[Urlaubs- und Abwesenheitstypen konfigurieren](https://go.microsoft.com/fwlink/?linkid=2168108)|
| Urlaubseinheiten pro Urlaubstyp konfigurieren | [Urlaubseinheiten pro Urlaubstyp konfigurieren](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/configure-leave-units-per-leave-type) |[Urlaubs- und Abwesenheitstypen konfigurieren](https://go.microsoft.com/fwlink/?linkid=2168215)|
| Aktivieren, dass Mitarbeiter als zahlungsbereit markiert werden | [Mitarbeiter als zahlungsbereit markieren](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [Für Zahlung bereit](/dynamics365/human-resources/hr-compensation-payroll) |

## <a name="coming-soon"></a>Demnächst

Eine vollständige Liste der geplanten Funktionen und ihrer geplanten Versionen finden Sie unter [Überblick über Dynamics 365 Human Resources 2021 Veröffentlichungszyklus 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

| Funktion | Informationen |
| --- | --- |
| Plattformupdate 10.0.21 (45) | Der Roll-out des Plattform-Updates 10.0.21 wird voraussichtlich mit dem Service-Release am 4. Oktober 2021 beginnen. Weitere Informationen finden Sie unter [Plattform-Updates für Version 10.0.21 von Finance and Operations-Apps (Oktober 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21). |

## <a name="see-also"></a>Siehe auch

[Welche Neuerungen oder Änderungen bietet Human Resources?](hr-admin-whats-new.md)</br>
[Übersicht zu Dynamics 365 Human Resources 2021 Versionswelle 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[Aktualisierungsprozess](hr-admin-setup-update-process.md)</br>
[Funktionen verwalten](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
