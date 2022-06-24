---
title: Verwalten von Funktionen in der Personalverwaltung
description: In diesem Artikel werden die Funktionsverwaltungsfunktion und deren Verwendung beschrieben.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a5023e8b60ede1f75961abff158bec9424d1aca4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907608"
---
# <a name="manage-features-in-human-resources"></a>Verwalten von Funktionen in der Personalverwaltung


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Im Rahmen unseres kontinuierlichen Rollouts von neuen Funktionen für Microsoft Dynamics 365 Human Resources wollen wir unseren Kunden so schnell wie möglich neue Funktionen zur Verfügung stellen. Wir bieten Vorschaufunktionen, die fast bereit für die allgemeine Verfügbarkeit sind und ausgiebig getestet wurden. Wir sind nur auf der Suche nach einer letzten Runde von Kunden-Feedback und Validierung, bevor wir sie zur allgemeinen Verfügbarkeit veröffentlichen.

Weitere Informationen über neue Funktionen im Human Resources finden Sie unter [Neuerungen in Human Resources](hr-admin-whats-new.md) und [Dynamics 365 und Power Platform-Versionsveröffentlichungsplan](/dynamics365/release-plans/?panel=products1#pivot=products).

Der Arbeitsbereich **Funktionsverwaltung** bietet eine Liste der in jedem Release ausgelieferten Features. Standardmäßig sind neue Funktionen ausgeschaltet. Sie können den Arbeitsbereich verwenden, um sie zu aktivieren und die Dokumentation für sie anzuzeigen. Weitere Informationen zur Feature-Verwaltung finden Sie unter [Feature-Verwaltung Übersicht](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Alle neuen Funktionen bleiben mindestens 30 Tage und in der Regel 30-60 Tage in der Vorschau. Die wichtigsten Funktionen sind in der Regel im Oktober und April eines jeden Jahres nach dem Vorschauzeitraum verfügbar. Sobald Sie neue Funktionen im Arbeitsbereich **Feature-Management** sehen, können Sie diese einschalten. Einige Funktionen sind möglicherweise standardmäßig aktiviert.

Sobald eine Funktion allgemein verfügbar ist, kann sie in Produktionsumgebungen ein- und ausgeschaltet werden. Der Arbeitsbereich **Feature-Management** zeigt an, wann eine Vorschaufunktion obligatorisch wird. Dieses Datum ist in der Regel der 1. Oktober oder 1. April, um mit den halbjährlichen Release-Plänen übereinzustimmen. Sie können obligatorische Funktionen nicht deaktivieren. Bis es obligatorisch wird, können Sie eine Funktion in allen Umgebungen ein- und ausschalten.

## <a name="enable-or-disable-preview-features"></a>Vorschaufunktionen aktivieren oder deaktivieren

Um auf Vorschaufunktionen zugreifen zu können, müssen Sie sie in Ihrer Umgebung zunächst aktivieren. Aktivieren oder Deaktivieren von Vorschaufunktionen ist umgebungsspezifisch.

> [!IMPORTANT]
> Vorschaufunktionen werden nur in **Sandbox**-Umgebungen aktiviert. Durch das Aktivieren der Vorschaufunktion aktivieren Sie Vorschaufunktionen für alle Benutzer in Ihrer Organisation, die sich in dieser Umgebung befinden. Wenn Sie die Vorschaufunktion deaktivieren, machen Sie sie für Ihre Benutzer unzugänglich. Die Vorschaufunktionen werden in Human Resources nur eingeschränkt unterstützt. Sie verwenden möglicherweise weniger Datenschutz‑ und Sicherheitsmaßnahmen und sind nicht in der Human Resources-Service-Level-Vereinbarung (SLA) enthalten. Sie sollten keine Vorschaufunktionen verwenden, um personenbezogene Daten (d. h. Informationen, die Sie identifizieren könnten) oder andere Daten zu verarbeiten, die gesetzlichen oder behördlichen Anforderungen unterliegen.

1. Wählen Sie in Human Resources **Systemverwaltung** aus.

2. Wählen Sie die Kachel **Funktionsverwaltung**.

3. Um eine Vorschaufunktion zu aktivieren, wählen Sie sie aus der Liste aus und wählen Sie dann **Aktivieren**. Um eine Vorschaufunktion zu deaktivieren, wählen Sie sie aus der Liste aus und wählen Sie dann **Deaktivieren**.

## <a name="enable-or-disable-benefits-management"></a>Vorteilsverwaltung aktivieren oder deaktivieren

Verwenden Sie das gleiche Verfahren, um die Leistungsverwaltung zu aktivieren [Aktivieren oder Deaktivieren der Vorschaufunktionen](hr-admin-manage-features.md?enable-or-disable-preview-features).

> [!IMPORTANT]
> Sie können die Leistungsverwaltung in einer **Produktions** Umgebung nicht deaktivieren, nachdem Sie diese aktiviert haben. Sie können die Leistungsverwaltung in der **Sandkasten** Umgebungen jedoch deaktivieren.

Weitere Informationen zur Konfiguration und Verwendung der Vorteilsverwaltung finden Sie unter [Übersicht über die Vorteilsverwaltung](hr-benefits-management-overview.md).

Vorteilsverwaltung ersetzt die Funktionalität im Arbeitsbereich **Vorteile**. Wenn Sie die Vorschaufunktion für die Vorteilsverwaltung aktivieren, können Sie im Arbeitsbereich **Vorteile** nicht mehr auf die folgenden Formulare zugreifen:

- **Vergütungen**
- **Vergütungselemente**
- **Beitragsberechnungssätze**
- **Leistungsregistrierungsergebnisse**
- **Ergebnisse für Vergütungsablauf und -verlängerung**
- **Regeltypen für Vergütungsberechtigungsrichtlinien**
- **Vorteilsberechtigungsrichtlinien**
- **Berechtigungsereignisse**

Sie können die Informationen auf diesen Seiten im schreibgeschützten Modus anzeigen. Wenn Sie die Informationen bearbeiten möchten, müssen Sie zuerst die Vorschaufunktion für die Vorteilsverwaltung deaktivieren (gilt nur für **Sandkasten** Umgebungen).

## <a name="enable-or-disable-leave-and-absence"></a>Urlaub und Abwesenheit aktivieren oder deaktivieren

Verwenden Sie das gleiche Verfahren, um die Urlaub und Abwesenheiten zu aktivieren [Aktivieren oder Deaktivieren der Vorschaufunktionen](hr-admin-manage-features.md?enable-or-disable-preview-features).

> [!IMPORTANT]
> Sie können die Funktion **Mehrere Urlaubsarten** in Urlaub und Abwesenheit nicht deaktivieren, nachdem Sie sie aktiviert haben. Dies gilt für beide **Sandkasten** und **Produktios** Umgebungen.

Weitere Informationen zur Vorschau-Funktion von Urlaubs- und Abwesenheitsverwaltung finden Sie unter [Urlaub- und Abwesenheitsvorschaufunktion](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

## <a name="send-us-feedback"></a>Senden Sie uns Feedback

Wir möchten von Ihnen über Ihre Erfahrung mit Vorschaufunktionen hören. Wir empfehlen Ihnen, Ihr Feedback regelmäßig auf den folgenden Seiten zu veröffentlichen, wenn Sie diese oder andere Funktionen nutzen:

- [Community](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) - Diese Seite ist eine großartige Ressource, auf der Benutzer Anwendungsfälle diskutieren, Fragen stellen und Hilfe von der Community erhalten können.
- Teilen Sie uns mit, welche Funktionen Sie im Produkt sehen möchten und welche Änderungen Ihrer Meinung nach an bestehenden Funktionen vorgenommen werden sollten. Schlagen Sie Produktideen über [Ideen für Human Resources](https://powerusers.microsoft.com/t5/Ideas-for-Human-Resources/idb-p/HumanResources) vor.
    
Bitte geben Sie keine persönlichen Daten (Informationen, die Sie identifizieren könnten) in Ihre Feedback- oder Produktbewertungseinreichungen ein. Die gesammelten Informationen können weiter analysiert werden und werden nicht zur Beantwortung von Anfragen im Rahmen der geltenden Datenschutzgesetze verwendet. Personenbezogene Daten, die im Rahmen dieser Programme separat erfasst werden, unterliegen der [Microsoft-Datenschutzerklärung](https://privacy.microsoft.com/privacystatement).

## <a name="see-also"></a>Siehe auch

- [Neuerungen in Human Resources](hr-admin-whats-new.md)
- [Dynamics 365 und Power Platform-Versionsveröffentlichungsplan](/dynamics365/release-plans/?panel=products1#pivot=products)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
