---
title: Parameter für Benefits-Management und Mitarbeiter-Self-Service für alle Firmen festlegen
description: Konfigurieren Sie die Parameter für das Benefits-Management und den Mitarbeiter-Self-Service in Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 822e5b37be7b2d5712d61bf7fb00f40d1692f406
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8066924"
---
# <a name="set-benefits-management-and-employee-self-service-parameters-for-all-companies"></a>Parameter für Benefits-Management und Mitarbeiter-Self-Service für alle Firmen festlegen


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bevor Sie Vorteilspläne in Microsoft Dynamics 365 Human Resources einrichten können, müssen Sie die Vorteilsverwaltungsparameter konfigurieren. Diese Parameter legen Standardwerte, Ursachencodes und andere Optionen fest. 

## <a name="configure-general-parameters"></a>Allgemeine Parameter konfigurieren

1. Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Setup** die Option **Gemeinsam genutzte Parameter der Personalverwaltung**.

2. Definieren Sie auf der Registerkarte **Vergütungsverwaltung** die Werte für die folgenden Felder:

   | Feld | Beschreibung |
   | --- | --- |
   | **Land/Region** | Das Feld **Land/Region** bestimmt die Anzeigereihenfolge der Postleitzahlen/Staaten. Das ausgewählte Land wird zuerst in der Dropdown-Liste angezeigt. |
   | **Registrierungsursachencode** | Wählen Sie einen Standardursachencode aus, der verwendet werden soll, wenn Mitarbeiterpläne während der offenen Registrierungsverarbeitung erstellt werden. |
   | **Stornierungsursachencode** | Der Ursachencode, der verwendet wird, wenn ein Mitarbeitervorteilsplan storniert wird. Er wird beim Stornierungsvorgang in einem Dialogfeld angezeigt. Benutzer können ihn im Feld **Stornierungsursachencode** bei Bedarf ändern. |
   | **Ursachencode erneut öffnen** | Der Ursachencode, der verwendet wird, wenn ein Mitarbeitervorteilsplan erneut geöffnet wird. Er wird beim Stornierungsvorgang in einem Dialogfeld angezeigt. Benutzer können ihn im Feld **Ursachencode erneut öffnen** bei Bedarf ändern. | 
   | **Ursachencode für Lebensereignis** | Der zu verwendende Ursachencode, wenn ein Lebensereignis eintritt. |
   | **Ursachencode für Satzänderung** | Der Ursachencode, der beim Stornieren und erneuten Öffnen eines Personalvorteilsplans verwendet werden soll, wenn die Satzänderung aktualisiert wird. Er zeigt an, welche Datensätze durch die Aktualisierung der Satzänderung geändert wurden. |
   | **Vergütungsjahresgehalt** | Ermöglicht das Festlegen eines Betrags **Jahresgehalt für Vorteile** für einen Mitarbeiter. Die Personalverwaltung wird den Betrag **Jahresgehalt für Vorteile** verwenden, wenn Deckungssummen festgelegt werden, anstatt eines festen jährlichen Vergütungsbetrags. |
   | **Neueinstellung möglich** | Gibt an, ob Neueinstellungen zulässig sind. |
   | **Registrierungsperiode für Neueinstellungen** | Die Periode, für die die Registrierung einer Neueinstellung zulässig ist.</br></br>**Hinweis**: Diese Einstellung überschreibt jede Registrierungsperiode für Neueinstellungen, die Sie in der Planberechtigungsregel festgelegt haben. |
   | **Standard-Zahlungshäufigkeit** | Die Standardzahlungshäufigkeit, die verwendet wird, wenn neue Mitarbeiter hinzugefügt werden. |
   | **Lebensereignisse aktiviert** | Aktiviert Lebensereignisse. |
   | **Legacy-Vergütungsformulare ausblenden** | Ermöglicht das Ausblenden von Legacy-Vergütungsformularen. |
   | **Vorteilsüberprüfung** | Der Überprüfungstext, der beim Auschecken der Self-Service-Vorteile verwendet werden soll. |
   | **Beauftragten automatisch auswählen** | Gibt an, ob Unterhaltsberechtigte und Begünstigte ausgehend von ihrem Anspruch für Planoptionen automatisch ausgewählt werden sollen. |

3. Wählen Sie **Speichern** aus.

## <a name="configure-employee-self-service-parameters"></a>Mitarbeiter-Self-Service-Parameter konfigurieren

1. Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Setup** die Option **Personalverwaltungsparameter**.

2. Definieren Sie auf der Registerkarte **Vergütungsverwaltung** die Werte für die folgenden Felder:

   | Feld | Beschreibung |
   | --- | --- |
   | **Vorteilsüberprüfung** | Der Überprüfungstext, der bei der Self-Service-Leistungsprüfung verwendet werden soll. |
   | **Beauftragten automatisch auswählen** | Gibt an, ob Unterhaltsberechtigte und Begünstigte basierend auf ihrer Berechtigung für Planoptionen automatisch ausgewählt werden sollen. |

3. Wählen Sie **Speichern**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
