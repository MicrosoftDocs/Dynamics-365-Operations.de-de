---
title: Vorteilsverwaltungsparameter festlegen
description: Konfigurieren Sie Parameter für die Vorteilsverwaltung in Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 85bbe5d3b422f2f29f1d1fe8ee269b407da691c2
ms.sourcegitcommit: 9dc5c7dd5877cc6e7cd0059d173bcd8052ba13bc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/16/2020
ms.locfileid: "3599355"
---
# <a name="set-benefits-management-parameters"></a>Vorteilsverwaltungsparameter festlegen

Bevor Sie Urlaubspläne in Microsoft Dynamics 365 Human Resources einrichten können, müssen Sie die Vorteilsverwaltungsparameter konfigurieren. Diese Parameter legen Standardwerte, Ursachencodes und andere Optionen fest.

## <a name="configure-general-parameters"></a>Allgemeine Parameter konfigurieren

1. Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Setup** die Option **Gemeinsam genutzte Parameter der Personalverwaltung**.

2. Definieren Sie auf der Registerkarte **Allgemeines** die Werte für die folgenden Felder:

   | Feld | Beschreibung |
   | --- | --- |
   | **Land/Region** | Das Feld **Land/Region** bestimmt die Anzeigereihenfolge der Postleitzahlen/Staaten. Das ausgewählte Land wird zuerst in der Dropdown-Liste angezeigt. |
   | **Registrierungsursachencode** | Wählen Sie einen Standardursachencode aus, der verwendet werden soll, wenn Mitarbeiterpläne während der offenen Registrierungsverarbeitung erstellt werden. |
   | **Stornierungsursachencode** | Der Ursachencode, der verwendet wird, wenn ein Mitarbeitervorteilsplan storniert wird. Er wird beim Stornierungsvorgang in einem Dialogfeld angezeigt. Benutzer können ihn im Feld **Stornierungsursachencode** bei Bedarf ändern. |
   | **Ursachencode erneut öffnen** | Der Ursachencode, der verwendet wird, wenn ein Mitarbeitervorteilsplan erneut geöffnet wird. Er wird beim Stornierungsvorgang in einem Dialogfeld angezeigt. Benutzer können ihn im Feld **Ursachencode erneut öffnen** bei Bedarf ändern. | 
   | **Ursachencode für Lebensereignis** | Der zu verwendende Ursachencode, wenn ein Lebensereignis eintritt. |
   | **Ursachencode für Satzänderung** | Der Ursachencode, der beim Stornieren und erneuten Öffnen eines Personalvorteilsplans verwendet werden soll, wenn die Satzänderung aktualisiert wird. Er zeigt an, welche Datensätze durch die Aktualisierung der Satzänderung geändert wurden. |
   | **Vergütungsjahresgehalt** | Ermöglicht das Festlegen eines Betrags **Jahresgehalt für Vorteile** für einen Mitarbeiter. Die Personalverwaltung wird den Betrag **Jahresgehalt für Vorteile** verwenden, wenn Deckungssummen bestimmt werden, anstatt eines festen jährlichen Vergütungsbetrags. |
   | **Neueinstellung möglich** | Gibt an, ob Neueinstellungen zulässig sind. |
   | **Registrierungsperiode für Neueinstellungen** | Die Periode, für die die Registrierung einer Neueinstellung zulässig ist.</br></br>**Hinweis**: Diese Einstellung überschreibt jede Registrierungsperiode für Neueinstellungen, die Sie in der Planberechtigungsregel festgelegt haben. |
   | **Standard-Zahlungshäufigkeit** | Die Standardzahlungshäufigkeit, die verwendet wird, wenn neue Mitarbeiter hinzugefügt werden. |
   | **Lebensereignisse aktiviert** | Aktiviert Lebensereignisse. |
   | **Legacy-Vergütungsformulare ausblenden** | Ermöglicht das Ausblenden von Legacy-Vergütungsformularen. |

3. Wählen Sie **Speichern**.

## <a name="configure-employee-self-service-parameters"></a>Mitarbeiter-Self-Service-Parameter konfigurieren

1. Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Setup** die Option **Personalverwaltungsparameter**.

2. Definieren Sie auf der Registerkarte **Mitarbeiter-Self-Service** die Werte für die folgenden Felder:

   | Feld | Beschreibung |
   | --- | --- |
   | **Vorteilsüberprüfung** | Der Überprüfungstext, der beim Auschecken der Self-Service-Vorteile verwendet werden soll. |
   | **Beauftragten automatisch auswählen** | Gibt an, ob Unterhaltsberechtigte und Begünstigte basierend auf ihrer Berechtigung für Planoptionen automatisch ausgewählt werden sollen. |

3. Wählen Sie **Speichern**.
