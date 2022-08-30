---
title: Vorteilsverwaltungsparameter pro Unternehmen konfigurieren
description: In diesem Artikel wird beschrieben, wie Sie die Parameter für die Verwaltung der Vorteile pro Firma in Microsoft Dynamics 365 Human Resources konfigurieren.
author: twheeloc
ms.date: 8/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2f3f8625a8ebbe6812d2f051649ff2a608ed4b54
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2022
ms.locfileid: "9323897"
---
# <a name="configure-benefits-management-parameters-per-company"></a>Parameter für die Vorteilsverwaltung je Unternehmen konfigurieren


Für jede Organisation, die Vorteile bereitstellt, müssen Sie Einstellungen für E-Mails zur Vorteilsbestätigung konfigurieren.

## <a name="configure-confirmation-email-settings"></a>Einstellungen für Bestätigungs-E-Mail konfigurieren

1. Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Setup** die Option **Personalverwaltungsparameter**.

2. Definieren Sie auf der Registerkarte **Vergütungsverwaltung** die Werte für die folgenden Felder: 

   | Feld | Beschreibung |
   | --- | --- |
   | **Bestätigungs-E-Mail senden** | Wenn diese Funktion aktiviert ist, wird eine Bestätigungs-E-Mail an die Mitarbeiter gesendet, wenn sie sich von der Anmeldung für die Vorteile in **Mitarbeiter-Self-Service** abmelden. |
   | **E-Mail-Vorlage für Bestätigung** | Wählen Sie die E-Mail-Vorlage der Organisation aus, die beim Senden der Anmeldebestätigung verwendet werden soll. Wenn Sie keine Vorlage auswählen, wird die folgende allgemeine E-Mail gesendet:<br><br>%EmployeeFirstName%,<br><br>Herzlichen Glückwunsch! Sie haben sich erfolgreich für Vorteile angemeldet.<br><br>Vielen Dank,<br>Vorteil <Name des Unternehmens/der Organisation>. |
   | **Standard-E-Mail-Adresse des Absenders** | Die E-Mail-Adresse, die beim Senden der Bestätigungs-E-Mail verwendet werden soll. |

3. Wählen Sie **Speichern** aus.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
