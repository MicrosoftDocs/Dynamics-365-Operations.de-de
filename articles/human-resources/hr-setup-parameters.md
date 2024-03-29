---
title: Parameter in Human Resources konfigurieren
description: In diesem Artikel wird beschrieben, wie unternehmensspezifische Parameter in Dynamics 365 Human Resources eingerichtet werden.
author: twheeloc
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HRMParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 13a25d3f1f72d8053ed3951b036522cfa3a15959
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9065643"
---
# <a name="configure-human-resources-parameters"></a>Parameter in Human Resources konfigurieren

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Die Einstellungen einiger Human Resources-Parameter sind firmenübergreifend, während die Einstellungen anderer Parameter firmenspezifisch sind. In diesem Artikel wird erklärt, wie Sie firmenspezifische Human Resources-Parameter festlegen.

Zum Festlegen der Human Resources-Parameter werden zwei Seiten verwendet. Für Parameter, die innerhalb des Unternehmens freigegeben werden, verwenden Sie die Seite **Freigegeben Parameter für Personalverwaltung**. Für Parameter, die firmenspezifisch sind, verwenden Sie die Seite **Parameter für personelle Ressourcen**.

![Gehen Sie zu Personalverwaltungsparameter.](./media/hr-employee-self-service-human-resources-parameters.png)

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

- Eine Farbe auswählen, die auf offene Transaktionen zur Abwesenheit angewendet werden soll.
- die Formatvorlage für die Berichte festlegen.
- die Integration zwischen Schulungskursen und Abwesenheitsregistrierung aktivieren.
- Den Abwesenheitscode auswählen, der zur Steuerung dieser Integration verwendet wird.
- Geben Sie an, wie lange Fälle von Verletzungen und Krankheiten aufbewahrt werden sollen.
- Legen Sie die Standard-Identifikationsnummer fest, die angezeigt wird, wenn eine neue Arbeitskraft eingestellt wird.
- Geben Sie das Datum an, das zur Berechnung der Dienstjahre verwendet wird. 

![Registerkarte „Allgemeines“.](./media/hr-setup-parameters-general.png)

## <a name="recruitment"></a>Personalbeschaffung

Die Einstellungen auf der Registerkarte **Rekrutierung** legen die Dokumenttypen fest, die für die Korrespondenz verwendet werden, die automatisch an Bewerber gesendet wird. Sie können auch das Rekrutierungsprojekt angeben, das für Spontanbewerbungen verwendet wird.

Die Periode, die für die **Personalbeschaffungsprojektfälligkeit** definiert wird, bestimmt die Personalbeschaffungsprojekte, die auf der Kachel **Fälligkeitsdatum-Projekte** im Arbeitsbereich **Einstellungsverwaltung** eingeschlossen wird. Die Periode, die für die Bewerbungsfristwarnung definiert ist, wird verwendet, um Personalbeschaffungsprojekte, deren Bewerbungsfrist demnächst abläuft im Arbeitsbereich **Personalbeschaffung** auf der Kachel **Bewerbungsfrist läuft demnächst ab** anzuzeigen.

Weitere Informationen zur Rekrutierung finden Sie unter [Bewerbung von Kandidaten](hr-personnel-recruit.md).

## <a name="compensation"></a>Vergütung

In Dynamics 365 Finance legen die Einstellungen auf der Registerkarte **Vergütung** fest, ob Benutzer bestätigen müssen, dass sie Informationen für einen festen oder variablen Vergütungsplan speichern wollen. Wenn Sie **Speichervalidierung aktivieren** wählen, erhalten Benutzer beim Schließen einer vergütungsbezogenen Seite eine Meldung, die sie fragt, ob sie den Datensatz speichern wollen. Einige Seiten im Vergütungsmanagement erlauben es Benutzern nicht, Informationen zu löschen. Indem Sie Benutzer auffordern, zu bestätigen, dass sie Informationen speichern möchten, können Sie möglicherweise die Menge der Informationen begrenzen, die gespeichert werden, aber später nicht gelöscht werden können. Wenn Sie **Speichervalidierung aktivieren** deaktivieren, werden Datensätze sofort gespeichert, möglicherweise bevor der Benutzer dazu bereit ist. Wenn Sie das Leistungsmanagement verwenden, können Sie auf der Registerkarte **Vergütung** auch ein Bewertungsmodell auswählen, das anstelle des Modells, das den Vergütungsplänen zugeordnet ist, bei der Bewertung der Leistung verwendet wird.

In Human Resources können Sie auf der Registerkarte **Vergütung** wählen, ob Sie den Zugriff auf Vergütungspläne beschränken und eine Standardwährung festlegen wollen.

> [!NOTE]
> In der zusammengeführten Infrastruktur wurde der Standardparameter **Währung** auf der Registerkarte **Vergütung** der Seite **Parameter für Human Resources** entfernt. In Zukunft wird die Währung über den Parameter **Sachkonto-Währung** gehandhabt, um sicherzustellen, dass es keine Konflikte mit bestehenden Funktionen für Finanzen und Betrieb gibt und um Doppelarbeit zu vermeiden. Weitere Informationen über die Verwendung der Sachkonto-Währungsfunktionalität finden Sie unter [Sachkonten konfigurieren](/general-ledger/configure-ledger#configuring-currencies-for-the-ledger.md). 

Weitere Informationen über Vergütungen finden Sie unter [Übersicht über Vergütungspläne](hr-compensation-overview.md).

## <a name="number-sequences"></a>Nummernkreise

Die Einstellungen auf der Registerkarte **Nummernkreis** legen die Sequenzen fest, mit denen Artikeln in Human Resources automatisch IDs zugewiesen werden, z.B:

- Bewerbungen
- Abwesenheitserfassungen
- Ergebnisse des Vergütungsprozesses
- Fallnummern
- Kurse
- Kurs-Agenden

Um Nummernkreis-Referenzen und -Codes zu pflegen, verwenden Sie die Listenseite **Nummernkreise** (wählen Sie **Organisationsverwaltung > Nummernkreise > Nummernkreise**).

Weitere Informationen finden Sie unter [Übersicht über Nummernkreise](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).

> [!NOTE]
> Die Anzahl der gearbeiteten Stunden kann 1,250 Stunden und eine Beschäftigungsdauer von 12 Monate nicht überschreiten. Diese maximalen Werte sind in Übereinstimmung mit dem Bundesgesetz in den USA festgelegt.

![Registerkarte „Nummernkreise“.](./media/hr-setup-parameters-number-sequences.png)

## <a name="fmla"></a>FMLA

Auf der Registerkarte FMLA legen Sie die FMLA-Berechtigungsvoraussetzungen und die FMLA-Anspruchsstunden fest. Weitere Informationen finden Sie unter [Urlaub- und Abwesenheitsparameter konfigurieren](hr-leave-and-absence-parameters.md).

![Registerkarte FMLA.](./media/hr-setup-parameters-fmla.png)

## <a name="employee-self-service"></a>Mitarbeiter-Self-Service

Die Einstellungen auf der Registerkarte **Mitarbeiter-Self-Service** beeinflussen, wie der **Mitarbeiter-Self-Service** den Mitarbeitern erscheint. Auf dieser Registerkarte können die folgenden Aufgaben ausgeführt werden:

- Einen Namen für den Arbeitsbereich des **Mitarbeiter-Self-Service** eingeben
- auswählen, welche Informationen ein Manager für Mitarbeiter eingeben kann
- Nützliche Links für Mitarbeiter hinzufügen
- Mitarbeitern das Hinzufügen oder Bearbeiten von geschäftlichen Kontaktdetails verbieten. Weitere Informationen finden Sie unter [Bearbeiten von persönlichen Informationen einschränken](hr-employee-self-service-restrict-editing.md).

Weitere Informationen zum Festlegen des **Mitarbeiter-Self-Service** finden Sie unter [Übersicht über den Mitarbeiter- und Manager-Self-Service](hr-employee-manager-self-service-overview.md).

![Registerkarte Mitarbeiter-Self-Service.](./media/hr-setup-parameters-employee-self-service.png)

## <a name="manager-self-service"></a>Manager-Self-Service

Die Einstellungen auf der Registerkarte **Manager-Self-Service** beeinflussen, was Manager im **Manager-Self-Service** sehen. Auf dieser Registerkarte können Sie die folgenden Optionen konfigurieren:

- Der Bereich für auslaufende Datensätze
- Informationen, die Manager in auslaufenden Datensätzen sehen können
- Ob Manager offene Positionen für erweiterte Berichte anzeigen können
- Ansichten von auslaufenden Arbeitskräften
- Nützliche Links für Manager

Weitere Informationen zum Einrichten des **Manager-Self-Service** finden Sie unter [Übersicht über den Mitarbeiter- und Manager-Self-Service](hr-employee-manager-self-service-overview.md).

![Registerkarte Manager-Self-Service.](./media/hr-setup-parameters-manager-self-service.png)

## <a name="benefits-management"></a>Vorteilsverwaltung

Auf der Registerkarte **Vorteilsverwaltung** können Sie E-Mail-Optionen für den die Vorteilsverwaltung konfigurieren. Informationen zum Einrichten und Verwenden der Vorteilsverwaltung finden Sie unter [Übersicht zur Vorteilsverwaltung](hr-benefits-management-overview.md).

![Registerkarte „Vorteilsverwaltung“.](./media/hr-setup-parameters-benefits-management.png)

## <a name="leave-and-absence"></a>Beurlaubung und Abwesenheit

Informationen zum Festlegen und Verwenden von Urlaub und Abwesenheit finden Sie unter [Übersicht über Urlaub und Abwesenheit](hr-leave-and-absence-overview.md).

## <a name="payment-methods"></a>Zahlungsmethoden

Auf der Registerkarte **Zahlungsmethoden** können Sie die von Ihrer Organisation unterstützten Zahlungsmethoden auswählen. Weitere Informationen zum Konfigurieren von Vergütungen finden Sie unter [Übersicht über Vergütungspläne](hr-compensation-overview.md).

![Registerkarte „Zahlungsmethoden“.](./media/hr-setup-parameters-payment-methods.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
