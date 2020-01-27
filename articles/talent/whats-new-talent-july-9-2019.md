---
title: Neuerungen und Änderungen in Dynamics 365 Talent (9. Juli 2019)
description: In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 Talent entweder neu oder geändert sind.
author: Darinkramer
manager: AnnBe
ms.date: 07/09/2019
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
ms.search.validFrom: 2019-07-09
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 99a7e6130d45229011a185087d4872fe34b8224a
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897625"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-july-9-2019"></a>Neuerungen und Änderungen in Dynamics 365 Talent (9. Juli 2019)

In diesem Thema werden die Funktionen beschrieben, die in Dynamics 365 Talent neu oder geändert wurden.

## <a name="changes-in-attract"></a>Änderungen in Attract

Diese Version enthält kleinere Fehlerkorrekturen für Dynamics 365 Talent: Attract.

### <a name="coming-soon-in-attract"></a>Bald verfügbar in Attract

#### <a name="job-approvals-appear-on-the-home-page"></a>Stellengenehmigungen werden auf der Startseite angezeigt

Genehmigungen werden im Abschnitt **Genehmigungen** im Dashboard angezeigt. Genehmiger können ihre Genehmigungen unter **Ihnen zugewiesen** überprüfen. Sie zeigen die Stellen-ID, den Stellen-Titel, andere Genehmiger und das Datum an, an der die Stelle zugewiesen wurde. Benutzer, die eine Stelle zur Genehmigung übermitteln, können ihre Stellen unter **Von Ihnen angefordert** überprüfen. Dort werden die Genehmiger angezeigt, die immer noch die übermittelte Stelle genehmigen müssen.

## <a name="changes-in-onboard"></a>Änderungen in Onboard

Diese Version enthält kleinere Fehlerkorrekturen für Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Core HR-Änderungen

Die in diesem Abschnitt beschriebenen Änderungen gelten für Buildnummer 8.1.2374.

### <a name="platform-update-28-for-finance-and-operations"></a>Platform update 28 für Finance and Operations

Zusätzliche Details zu Platform update 28 für Finance and Operations finden Sie unter [Vorschaufunktionen in Dynamics 365 Finance and Operations Plattformaktualisierung 28 (Juli 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-28).

### <a name="entity-support-for-custom-fields-in-common-data-service"></a>Entitätssupport für benutzerdefinierte Felder in Common Data Service 

Die folgenden Entitäten unterstützen benutzerdefinierte Felder: 

- **Plan für feste Vergütung**
- **Vergütungsreferenzpunkten einrichten**
- **Vergütungsreferenzpunktzeile einrichten**
- **Einkommenscode**
- **Lohnperiode**
- **Ereignis für feste Vergütung**
- **Vergütungsraster**

Klicken Sie zum Anzeigen aller aktualisierten Entitäten im Talent:

1. Wählen Sie **Systemverwaltung** aus, wählen Sie **Links** und **Comon Data Service Konfiguration** aus.
2. Wählen Sie das Dropdownmenü **CDS-Entitätsname** aus. Alle aufgelisteten Entitäten sind auf der aktuellen Version. 

###  <a name="full-name-added-to-worker-entity-in-common-data-service"></a>Vollständiger Name der Arbeitskraftentität in Common Data Service hinzugefügt

Das Feld **Bestandseinheit** wurde der **Arbeitskraft** hinzugefügt.

### <a name="full-time-equivalent-higher-than-10"></a>Ganztägiges Äquivalent höher als 1.0

Eine Warnung zeigt an, wenn nun Wert eingegeben wird, der größer als 1.0 ist für einen Vollzeitmitarbeiter auf einer Position. 

### <a name="a-warning-no-longer-displays-on-the-worker-page-when-there-is-no-future-dated-employment"></a>Eine Warnung wird nicht mehr auf der Arbeitskraftseite angezeigt, wenn keine zukünftige datierte Beschäftigung vorhanden ist.

Sie erhalten keine Meldung mehr, die anzeigt, dass eine zukünftige Beschäftigung beim Wechseln der Seite **Arbeitskraft** in der Liste **Kündigen von Mitarbeitern** im **Personalführung** Arbeitsbereich vorhanden ist. 

### <a name="unable-to-delete-a-business-process-in-talent"></a>Unfähig, einen Geschäftsprozess im Talent zu löschen

Sie können jetzt Geschäftsprozesse im Arbeitsbereich **Geschäftsprozesse** löschen..

### <a name="leave-balance-no-longer-displays-zero-for-plans-with-no-accruals-when-using-balance-as-of-accrual-period"></a>Urlaubsaldo werden nicht mehr für Pläne Null ohne Abgrenzungen angezeigt, falls dieser Saldo ab Abgrenzungsperiode verwendet wird.

Pläne, die ohne Abgrenzungen eingerichtet werden, können einen Saldo nun anzeigen.

## <a name="in-preview"></a>Vorschau

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>Vorschaufunktionen werden nur in den Sandkasteninstanzen aktiviert

Wenn Sie eine neue Instanz von Talent bereitstellen, können Sie angeben, ob der Instanztyp **Produktion** oder **Sandkasten** ist. Die Instanzen vom **Sandkasten** Typ ermöglichen ein frühzeitiges Testen neuer Funktionen. Alle vorhandenen Talent-Instanzen werden zum Instanztyp **Produktion** aktualisiert. Wenn eine der vorhandenen Instanzen auf den aktualisierten Instanztyp **Sandkasten** aktualisiert werden soll, wenden Sie sich an den [Support](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support), um die Änderungsanforderung zu initiieren.

Weitere Informationen dazu, wie Änderungen veröffentlicht werden, finden unter [Talent bereitstellen](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

### <a name="restrict-leave-types-in-time-off-requests"></a>Begrenzen der Sonderurlaubstypen in den Abwesenheitsanforderungen

Organisationen können Mitarbeitern viele unterschiedliche Arten von Sonderurlaub anbieten. Allerdings ist er möglicherweise nicht angebracht, dass Mitarbeiter einen Freizeitantrag für bestimmte Sonderurlaubstypen senden. Diese Sonderurlaubstypen können stattdessen von der Personalverwaltung (HR) verwaltet werden. Mit dieser Version können Sie konfigurieren, für welche Sonderurlaubstypen die Mitarbeiter Abwesenheitsanforderungen übermitteln können. 

## <a name="coming-soon-in-core-hr"></a>Bald in Core HR verfügbar

### <a name="view-extended-information-for-performance-in-manager-self-service"></a>Anzeigen von erweiterten Informationen, um die Leistung im Manager Self-Service zu melden

Mit einer neuen Option können Manager die Leistung von ihren direkten Mitarbeitern und den erweiterten Mitarbeitern anzeigen. Aktuell können Linienmanager Leistungsziele zuweisen und aktualisieren und neue Überprüfungen ausstellen, die ihre Mitarbeiter mitverwalten. Darüber hinaus können Vorgesetzte und ihre Mitarbeiter Leistungserfassungen verwalten und aktualisieren, um sicherzustellen, dass der Leistungsprüfungsprozess problemlos verläuft. Wenn diese Änderung implementiert ist, sind Manager in der Lage, leistungsbezogene Informationen neben jenen für die direkt unterstellten Mitarbeitern auch jene für ihre erweiterten Mitarbeiter anzuzeigen und zu verwalten. 

### <a name="entities-supporting-custom-fields"></a>Entitäten, die benutzerdefinierte Felder unterstützen

Die folgenden Entitäten werden für benutzerdefinierte Felder in Common Data Serviceaktiviert: 

- **Sonderurlaubstyp**
- **Arbeitskraftbankkonto**
- **Arbeitskalender**
