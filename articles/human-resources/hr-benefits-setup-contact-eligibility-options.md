---
title: Berechtigungsoptionen für persönliche Kontakte konfigurieren
description: Konfigurieren Sie Berechtigungsoptionen für persönliche Kontakte in Microsoft Dynamics 365 Human Resources. Persönliche Kontakte können Begünstigte oder Unterhaltsberechtigte sein.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
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
ms.openlocfilehash: 0275331e600770a9f38a33bc2c3170c4cf9be951
ms.sourcegitcommit: a9461650d11d6845e1942865ebf7e35f75f61ad3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/06/2020
ms.locfileid: "3229877"
---
# <a name="configure-personal-contact-eligibility-options"></a>Berechtigungsoptionen für persönliche Kontakte konfigurieren

In diesem Artikel erfahren Sie, wie Sie Typen für persönliche Kontakte für die Verwendung von Vorteilen in Microsoft Dynamics 365 Human Resources konfigurieren. Persönliche Kontakte können Begünstigte oder Unterhaltsberechtigte sein. 

1. Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Einstellung** die Option **Berechtigungsoptionen für persönliche Kontakte**.

2. Wählen Sie **Neu** aus.

3. Geben Sie Werte für die folgenden Felder an:

   | Feld | Beschreibung |
   | --- | --- |
   | **Berechtigungsoption** | Ein eindeutiger Name oder Code der Berechtigungsoption zur Identifizierung der Berechtigungsoption. |
   | **Beschreibung** | Eine kurze Beschreibung der Berechtigungsoption. |
   | **Berechtigungscode für Kontakt** | Der Systemcode, der die persönliche Berechtigungsoption am besten beschreibt. Sie haben folgende Auswahlmöglichkeiten: <ul><li>Beziehung</li><li>Student</li><li>Überschüssige abhängige Person</li><li>Überaltertes, deaktiviertes abhängiges Objekt</li></ul> |
   | **Status** | Der Status der Berechtigungsoption. Wenn der Status für eine Berechtigungsoption auf inaktiv gesetzt ist, können Sie diese Berechtigungsoption für persönliche Kontakte nicht auswählen. |
   | **Beziehung** | Gibt die Beziehung zwischen dem persönlichen Kontakt und dem Mitarbeiter an. Dieses Feld ist nur aktiv, wenn der Kontaktberechtigungscode auf „Beziehung“ gesetzt ist. |
   | **Alter** | Das maximale Alter eines berechtigten persönlichen Kontakts für den Vorteilsplan. Dieses Feld ist nur aktiv, wenn Sie eine Beziehung auswählen. Dieses Alter wird mit dem berechneten Alter des persönlichen Kontakts verglichen. Das berechnete Alter ist: (Dispositionsdatum – Geburtsdatum des persönlichen Kontakts / 365). Diese Zahl ist immer eine ganze Zahl. |

4. Wählen Sie **Speichern**. 