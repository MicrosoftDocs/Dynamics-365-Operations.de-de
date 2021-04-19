---
title: Parameter in Human Resources konfigurieren
description: Dieses Thema erklärt, wie Sie firmenspezifische Parameter in Dynamics 365 Human Resources festlegen.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HRMParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 74bdf891ffa7a9d875e23cf46aeee1dbaf86db48
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802406"
---
# <a name="configure-human-resources-parameters"></a>Parameter in Human Resources konfigurieren

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Die Einstellungen einiger Human Resources-Parameter sind firmenübergreifend, während die Einstellungen anderer Parameter firmenspezifisch sind. In diesem Thema wird erklärt, wie Sie firmenspezifische Human Resources-Parameter festlegen.

Zum Festlegen der Human Resources-Parameter werden zwei Seiten verwendet. Für Parameter, die innerhalb des Unternehmens freigegeben werden, verwenden Sie die Seite **Freigegeben Parameter für Personalverwaltung**. Für Parameter, die unternehmensspezifisch sind (das heißt, die Einstellungen beziehen sich auf ein einzelnes Unternehmen), verwenden Sie die Seite **Personalverwaltungsparameter**.

![Gehen Sie zu Human Resources-Parameter](./media/hr-employee-self-service-human-resources-parameters.png)

Auf der Seite **Personalverwaltungsparameter** sind die Einstellungen in sechs Registerkarten unterteilt:

- **Allgemeines**
- **Rekrutierung** (diese Registerkarte ist nicht in Dynamics 365 Human Resources enthalten)
- **Kompensation**
- **Nummernkreise**
- **FMLA**
- **Mitarbeiter-Self-Service**
- **Manager-Self-Service**
- **Vergütungsverwaltung**
- **Beurlaubung und Abwesenheit**
- **Zahlungsmethoden**

Jede Registerkarte enthält Informationen, die sich auf ein einzelnes Unternehmen beziehen.

## <a name="general"></a>Allgemeines

Die Einstellungen auf der Registerkarte **Allgemein** definieren die Darstellung von Informationen zu Abwesenheitszeiten, Verletzung und Krankheit und Neueinstellungen. Die Einstellungen in dieser Registerkarte können auch mehrere Standardeingaben definieren, die angezeigt werden, während Sie arbeiten. Auf dieser Registerkarte können Sie insbesondere:

- Eine Farbe auswählen, die auf offene Transaktionen zur Abwesenheit angewendet werden soll
- die Formatvorlage für die Berichte festlegen
- die Integration zwischen Schulungskursen und Abwesenheitsregistrierung aktivieren
- Den Abwesenheitscode auswählen, der zur Steuerung dieser Integration verwendet wird.
- Geben Sie an, wie lange Fälle von Verletzungen und Krankheiten aufbewahrt werden sollen.
- Legen Sie die Standard-Identifikationsnummer fest, die angezeigt wird, wenn eine neue Arbeitskraft eingestellt wird.

![Registerkarte „Allgemeines“](./media/hr-setup-parameters-general.png)

## <a name="recruitment"></a>Personalbeschaffung

Die Einstellungen auf der Registerkarte **Rekrutierung** legen die Dokumenttypen fest, die für die Korrespondenz verwendet werden, die automatisch an Bewerber gesendet wird. Sie können auch das Rekrutierungsprojekt angeben, das für Spontanbewerbungen verwendet wird.

Der für die Alterung der Rekrutierungsprojekte definierte Zeitraum bestimmt die Rekrutierungsprojekte, die auf der Kachel **Alterungsprojekte** im Arbeitsbereich **Rekrutierungsmanagement** enthalten sind. Der für die Bewerbungsfrist-Warnung definierte Zeitraum wird verwendet, um Rekrutierungsprojekte, die sich ihrer Bewerbungsfrist nähern, auf der Kachel **Bewerbungsfrist nähert sich** im Arbeitsbereich **Rekrutierung** anzuzeigen.

Weitere Informationen zur Rekrutierung finden Sie unter [Bewerbung von Kandidaten](hr-personnel-recruit.md).

## <a name="compensation"></a>Kompensation

In Dynamics 365 Finance legen die Einstellungen auf der Registerkarte **Vergütung** fest, ob Benutzer bestätigen müssen, dass sie Informationen für einen festen oder variablen Vergütungsplan speichern wollen. Wenn Sie **Speichervalidierung aktivieren** wählen, erhalten Benutzer beim Schließen einer vergütungsbezogenen Seite eine Meldung, die sie fragt, ob sie den Datensatz speichern wollen. Einige Seiten im Vergütungsmanagement erlauben es Benutzern nicht, Informationen zu löschen. Indem Sie Benutzer auffordern, zu bestätigen, dass sie Informationen speichern möchten, können Sie möglicherweise die Menge der Informationen begrenzen, die gespeichert werden, aber später nicht gelöscht werden können. Wenn Sie **Speichervalidierung aktivieren** deaktivieren, werden Datensätze sofort gespeichert, möglicherweise bevor der Benutzer dazu bereit ist. Wenn Sie das Leistungsmanagement verwenden, können Sie auf der Registerkarte **Vergütung** auch ein Bewertungsmodell auswählen, das anstelle des Modells, das den Vergütungsplänen zugeordnet ist, bei der Bewertung der Leistung verwendet wird.

In Human Resources können Sie auf der Registerkarte **Vergütung** wählen, ob Sie den Zugriff auf Vergütungspläne beschränken und eine Standardwährung festlegen wollen.

Weitere Informationen über Vergütungen finden Sie unter [Übersicht über Vergütungspläne](hr-compensation-overview.md).

![Registerkarte „Vergütung“](./media/hr-setup-parameters-compensation.png)

## <a name="number-sequences"></a>Nummernkreise

Die Einstellungen auf der Registerkarte **Nummernkreis** legen die Sequenzen fest, mit denen Artikeln in Human Resources automatisch IDs zugewiesen werden, z.B:

- Bewerbungen
- Abwesenheitserfassungen
- Ergebnisse des Vergütungsprozesses
- Fallnummern
- Kurse
- Kurs-Agenden

Um Nummernkreis-Referenzen und -Codes zu pflegen, verwenden Sie die Listenseite **Nummernkreise** (wählen Sie **Organisationsverwaltung > Nummernkreise > Nummernkreise**).

Weitere Informationen finden Sie unter [Übersicht über Nummernkreise](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview?toc=/dynamics365/human-resources/toc.json).

> [!NOTE]
> Die Anzahl der gearbeiteten Stunden kann 1,250 Stunden und eine Beschäftigungsdauer von 12 Monate nicht überschreiten. Diese maximalen Werte sind in Übereinstimmung mit dem Bundesgesetz in den USA festgelegt.

![Registerkarte Nummernkreise](./media/hr-setup-parameters-number-sequences.png)

## <a name="fmla"></a>FMLA

Auf der Registerkarte FMLA legen Sie die FMLA-Berechtigungsvoraussetzungen und die FMLA-Anspruchsstunden fest. Weitere Informationen finden Sie unter [Urlaub- und Abwesenheitsparameter konfigurieren](hr-leave-and-absence-parameters.md).

![Registerkarte FMLA](./media/hr-setup-parameters-fmla.png)

## <a name="employee-self-service"></a>Mitarbeiter-Self-Service

Die Einstellungen auf der Registerkarte **Mitarbeiter-Self-Service** beeinflussen, wie der Mitarbeiter-Self-Service den Mitarbeitern erscheint. Auf dieser Registerkarte können Sie:

- Einen Namen für den Arbeitsbereich des Mitarbeiter-Self-Service eingeben
- auswählen, welche Informationen ein Manager für Mitarbeiter eingeben kann
- Nützliche Links für Mitarbeiter hinzufügen
- Mitarbeitern das Hinzufügen oder Bearbeiten von geschäftlichen Kontaktdetails verbieten. Weitere Informationen finden Sie unter [Bearbeiten von persönlichen Informationen einschränken](hr-employee-self-service-restrict-editing.md).

Weitere Informationen zum Festlegen des Mitarbeiter-Self-Service finden Sie unter [Übersicht über den Mitarbeiter- und Manager-Self-Service](hr-employee-manager-self-service-overview.md).

![Registerkarte Mitarbeiter-Self-Service](./media/hr-setup-parameters-employee-self-service.png)

## <a name="manager-self-service"></a>Manager-Self-Service

Die Einstellungen auf der Registerkarte **Manager-Self-Service** beeinflussen, was Manager im Manager-Self-Service sehen. Auf dieser Registerkarte können Sie die folgenden Optionen konfigurieren:

- Der Bereich für auslaufende Datensätze
- Informationen, die Manager in auslaufenden Datensätzen sehen können
- Ob Manager offene Positionen für erweiterte Berichte anzeigen können
- Ansichten von auslaufenden Arbeitskräften
- Nützliche Links für Manager

Weitere Informationen zum Einrichten des Manager-Self-Service finden Sie unter [Übersicht über den Mitarbeiter- und Manager-Self-Service](hr-employee-manager-self-service-overview.md).

![Registerkarte Manager-Self-Service](./media/hr-setup-parameters-manager-self-service.png)

## <a name="benefits-management"></a>Vergütungsverwaltung

Auf der Registerkarte Manager-Selfservice können Sie E-Mail-Optionen für den Manager-Selfservice konfigurieren. Informationen zum Festlegen und Verwenden der Vorteilsverwaltung finden Sie unter [Übersicht zur Vorteilsverwaltung](hr-benefits-management-overview.md).

![Registerkarte Vergütungsverwaltung](./media/hr-setup-parameters-benefits-management.png)

## <a name="leave-and-absence"></a>Beurlaubung und Abwesenheit

Informationen zum Festlegen und Verwenden von Urlaub und Abwesenheit finden Sie unter [Übersicht über Urlaub und Abwesenheit](hr-leave-and-absence-overview.md).

## <a name="payment-methods"></a>Zahlungsmethoden

Auf der Registerkarte **Zahlungsmethoden** können Sie die von Ihrer Organisation unterstützten Zahlungsmethoden auswählen. Weitere Informationen zum Konfigurieren von Vergütungen finden Sie unter [Übersicht über Vergütungspläne](hr-compensation-overview.md).

![Registerkarte Zahlungsarten](./media/hr-setup-parameters-payment-methods.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]