---
title: Bearbeiten von persönlichen Informationen einschränken
description: Schränken Sie die Bearbeitung von Kontaktdetails durch Mitarbeiter in Dynamics 365 Human Resources ein.
author: twheeloc
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EssWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c82114f6600345ee5e2eb9c1c0629ae6c8f0b9a7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877684"
---
# <a name="restrict-editing-of-personal-information"></a>Bearbeiten von persönlichen Informationen einschränken


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [applies to](../includes/applies-to-hr.md)]
[!include [preview feature](./includes/preview-feature.md)]

Dieser Artikel beschreibt, wie Sie Mitarbeiter an der Bearbeitung von Kontaktdaten in Dynamics 365 Human Resources hindern können. Möglicherweise möchten Sie verhindern, dass Mitarbeiter bestimmte Kontaktdetails bearbeiten, z. B. ihren Lagerplatz oder ihre E-Mail-Adresse.

> [!NOTE]
> Um diese Funktion zu nutzen, müssen Sie zuerst **(Vorschau) Mitarbeiter vom Hinzufügen oder Bearbeiten von Adress- und Kontaktinformationen für ausgewählte Zwecke einschränken** in der Funktionsverwaltung aktivieren. Weitere Informationen zur Aktivierung der Vorschaufunktionen finden Sie unter [Funktonen verwalten](hr-admin-manage-features.md).<br><br>![Vorschaufunktion aktivieren.](./media/hr-employee-self-service-restrict-enable.png)

## <a name="choose-the-information-an-employee-can-add-or-edit"></a>Wählen Sie die Informationen, die ein Mitarbeiter hinzufügen oder bearbeiten kann

1. Wählen Sie in der Personalverwaltung **Personalverwaltung** aus, wählen Sie **Links** aus und dann **Personalverwaltungsparameter**.

   ![Gehen Sie zu Personalverwaltungsparameter.](./media/hr-employee-self-service-human-resources-parameters.png)

2. Wählen Sie auf der Seite **Parameter für Human Resources** die Registerkarte **Mitarbeiter-Self-Service**.

   ![Wählen Sie Mitarbeiter-Self-Service aus.](./media/hr-employee-self-service-tab.png)

3. Deaktivieren Sie auf der Registerkarte **Mitarbeiter-Self-Service** alle Informationen im Abschnitt **Adress- und Kontaktinformationen**, die ein Mitarbeiter nicht hinzufügen oder bearbeiten soll. In diesem Beispiel haben wir das Häkchen bei **Geschäftliche** Kontaktinformationen entfernt.

   ![Bearbeitung für geschäftliche Kontaktinformationen einschränken.](./media/hr-employee-self-service-restrict-business.png)

4. Wählen Sie **Speichern** aus.

   ![Änderungen speichern.](./media/hr-employee-self-service-restrict-save.png)

## <a name="employee-experience"></a>Erfahrung der Mitarbeiter

Nachdem Sie Mitarbeitern das Hinzufügen oder Bearbeiten von Kontaktinformationen untersagt haben, können sie die Informationen zwar sehen, aber nicht ändern.

In diesem Beispiel, in dem Mitarbeitern das Bearbeiten von **Geschäftskontakt-Details** untersagt ist, können sie die Informationen dennoch im **Mitarbeiter-Self-Service** sehen:

![Geschäftskontaktdetails anzeigen.](./media/hr-employee-self-service-restrict-view.png)

Wenn sie jedoch die geschäftlichen Kontaktdetails auswählen, wird der Bereich **Adresse bearbeiten** als schreibgeschützt angezeigt, und sie können keines der Felder ändern.

![Geschäftskontakt-Details werden als schreibgeschützt angezeigt.](./media/hr-employee-self-service-restrict-read-only.png)

Wenn sie **Hinzufügen** wählen, um eine neue Adresse hinzuzufügen, können sie außerdem nicht **Geschäftlich** aus dem Dropdown-Feld **Zweck** wählen.

![Mitarbeiter kann keine Geschäftsadresse hinzufügen.](./media/hr-employee-self-service-restrict-add.png)

Das gleiche Erlebnis haben Mitarbeiter, wenn sie **Kontaktdetails** auf der Seite **Persönliche Daten** wählen und eine neue Adresse hinzufügen. Die Dropdown-Box **Zweck** zeigt nur die Arten von Informationen an, die sie hinzufügen können. 

![Der Mitarbeiter kann im Dropdown-Feld „Zweck“ nicht „Geschäftlich“ auswählen.](./media/hr-employee-self-service-restrict-purpose.png)

**Kontaktdetails** zeigt jetzt **Zweck** im Raster an.

![Zweck wird im Raster der Kontaktdetails angezeigt.](./media/hr-employee-self-service-restrict-purpose-grid.png)

## <a name="see-also"></a>Siehe auch

[Mitarbeiter- und Manager-Self-Service-Übersicht](hr-employee-manager-self-service-overview.md)<br>
[Parameter in Human Resources konfigurieren](hr-setup-parameters.md)<br>
[Persönliche Daten bearbeiten](hr-employee-manager-self-service-edit-personal-information.md)
