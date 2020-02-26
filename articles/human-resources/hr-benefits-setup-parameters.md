---
title: Vorteilsverwaltungsparameter festlegen
description: Konfigurieren Sie Parameter für die Vorteilsverwaltung in Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ab9b1fc78ce42479d9265b80337adf899cec3866
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009155"
---
# <a name="set-benefits-management-parameters"></a>Vorteilsverwaltungsparameter festlegen

[!include [banner](includes/preview-feature.md)]

Bevor Sie Urlaubspläne in Microsoft Dynamics 365 Human Resources einrichten können, müssen Sie die Vorteilsverwaltungsparameter konfigurieren. Diese Parameter legen Standardwerte, Ursachencodes und andere Optionen fest.

## <a name="configure-general-parameters"></a>Allgemeine Parameter konfigurieren

1. Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Einstellungen** die Option **Parameter**.

2. Definieren Sie auf der Registerkarte **Allgemeines** die Werte für die folgenden Felder:

   | Feld | Beschreibung |
   | --- | --- |
   | **Land/Region** | Das Feld **Land/Region** bestimmt die Anzeigereihenfolge der Postleitzahlen/Staaten. Das ausgewählte Land wird zuerst in der Dropdown-Liste angezeigt. |
   | **Registrierungsursachencode** | Wählen Sie einen Standardursachencode aus, der verwendet werden soll, wenn Mitarbeiterpläne während der offenen Registrierungsverarbeitung erstellt werden. |
   | **Stornierungsursachencode** | Der Ursachencode, der verwendet wird, wenn ein Mitarbeitervorteilsplan storniert wird. Er wird beim Stornierungsvorgang in einem Dialogfeld angezeigt. Benutzer können ihn im Feld **Stornierungsursachencode** bei Bedarf ändern. |
   | **Ursachencode erneut öffnen** | Der Ursachencode, der verwendet wird, wenn ein Mitarbeitervorteilsplan erneut geöffnet wird. Er wird beim Stornierungsvorgang in einem Dialogfeld angezeigt. Benutzer können ihn im Feld **Ursachencode erneut öffnen** bei Bedarf ändern. | 
   | **Ursachencode für Lebensereignis** | Der zu verwendende Ursachencode, wenn ein Lebensereignis eintritt. |
   | **Ursachencode für Satzänderung** | Der Ursachencode, der beim Stornieren und erneuten Öffnen eines Personalvorteilsplans verwendet werden soll, wenn die Satzänderung aktualisiert wird. Er zeigt an, welche Datensätze durch die Aktualisierung der Satzänderung geändert wurden. |
   | **Neueinstellung möglich** | Gibt an, ob Neueinstellungen zulässig sind. |
   | **Registrierungsperiode für Neueinstellungen** | Die Periode, für die die Registrierung einer Neueinstellung zulässig ist.</br></br>**Hinweis**: Diese Einstellung überschreibt jede Registrierungsperiode für Neueinstellungen, die Sie in der Planberechtigungsregel festgelegt haben. | 
   | **Jährliche Gehaltserhöhung** | Gibt an, ob das **Jährliches Vorteilsgehalt** in **Mitarbeitervorteilsdetails** automatisch berechnet werden soll. Basiert auf dem **Festen Lohnsatz**, **Durchschnittlichen Stunden** und **Zahlungshäufigkeit** des Mitarbeiters.</br></br>**Durchschnittliche Stunden** x **Fester Lohnsatz** x **Zahlungshäufigkeit** (Anzahl der Lohnperioden) = **Jährliches Vorteilsgehalt** </br></br>Wenn einer der Werte in den Feldern **Durchschnittliche Stunden**, **Fester Lohnsatz** oder **Zahlungshäufigkeit** geändert wird, berechnet das System den Betrag **Jährliches Vorteilsgehalt** des Mitarbeiters basierend auf den geänderten Werten automatisch neu. Das System erstellt einen Datensatz **Gültigkeitsdatum**, um das genaue Datum und die Uhrzeit der Änderung festzuhalten. Sie können den Betrag **Jährliches Vorteilsgehalt** bei Bedarf manuell bearbeiten. |
   | **Lebensereignisse aktiviert** | Aktiviert Lebensereignisse. |
   | **Legacy-Vergütungsformulare ausblenden** | Ermöglicht das Ausblenden von Legacy-Vergütungsformularen. |

3. Wählen Sie **Speichern**.

## <a name="configure-employee-self-service-parameters"></a>Mitarbeiter-Self-Service-Parameter konfigurieren

1. Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Einstellungen** die Option **Parameter**.

2. Definieren Sie auf der Registerkarte **Mitarbeiter-Self-Service** die Werte für die folgenden Felder:

   | Feld | Beschreibung |
   | --- | --- |
   | **Vorteilsüberprüfung** | Der Überprüfungstext, der beim Auschecken der Self-Service-Vorteile verwendet werden soll. |
   | **Beauftragten automatisch auswählen** | Gibt an, ob Unterhaltsberechtigte und Begünstigte basierend auf ihrer Berechtigung für Planoptionen automatisch ausgewählt werden sollen. |

3. Wählen Sie **Speichern**.
