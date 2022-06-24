---
title: Neuerungen oder Änderungen in Dynamics 365 Human Resources (19. November 2021)
description: Dieser Artikel beschreibt Funktionen, die entweder neu sind oder in der eigenständigen Microsoft Dynamics 365 Human Resources für den 19. November 2021 geändert wurden.
author: marcelbf
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-12-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d3e08432a4ce4d73cd67ad839191abe9f6e691a6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886072"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-november-19-2021"></a>Neuerungen oder Änderungen in Dynamics 365 Human Resources (19. November 2021)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dieser Artikel beschreibt Funktionen, die in Microsoft Dynamics 365 Human Resources neu oder geändert sind oder bald eingeführt werden.

Weitere Informationen zu unserem Aktualisierungsprozess und Zeitplan finden Sie unter [Aktualisierungsprozess](hr-admin-setup-update-process.md).

Weitere Informationen zu neuen Funktionen und den voraussichtlichen allgemeinen Verfügbarkeitsterminen finden Sie unter [Dynamics 365 Human Resources 2021 Veröffentlichungszyklus 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>In dieser Version

Die folgenden Fehlerkorrekturen sind in diesem Release enthalten. Änderungen gelten für Build-Nummer 8.1.4591.

### <a name="bug-fixes"></a>Fehlerkorrekturen

Die folgenden Fehlerkorrekturen sind in diesem Release enthalten.

> [!NOTE]
> Unser Ziel ist es, Ihnen diese Informationen so schnell wie möglich zukommen zu lassen. Wir können diesen Artikel aktualisieren, um Fehlerbehebungen aufzunehmen, die es nach der Erstveröffentlichung dieses Artikels in den Build geschafft haben.

| Problemnummer | Problem | Description |
|---|---|---|
| 626178 | In den Arbeiterkacheln fehlt die Navigation in **Manager-Self-Service** | Dieses Problem ist jetzt behoben. Die Navigation ist verfügbar, um die Berichtsdetails in **Manager-Self-Service** anzuzeigen. |
| 632573 | Es gibt keinen Validierungsfehler beim Speichern eines **Kurses** | Dieses Problem ist jetzt behoben. Beim Erstellen eines Kurses mit **Mindestteilnehmerzahl** von größer als 0 durfte noch gespeichert werden, auch wenn die **Maximale Teilnehmerzahl** 0 ist. |
| 615955 | Fehler „Feld **Zweck** muss ausgefüllt sein“ beim Anlegen eines neuen Standorts für den Personalbeschaffungsantrag. | Beim Erstellen einer Adresse für einen neuen Standort für den Personalbeschaffungsantrag erhalten Sie den Fehler: Feld „Zweck“ muss ausgefüllt sein. Das Feld **Zweck** steht auf der Seite jedoch nicht zur Verfügung. |
| 620797 | Fehler bei leerem Feld **Geschlecht** ist irreführend | Wenn für einen persönlichen Kontakt kein Geschlecht eingegeben wird, zeigt der Bericht „Hier klicken oder tippen, um Text einzugeben“ an – das ist irreführend, da in das Feld nichts eingegeben werden kann. |
| 620800 | Link zum Leistungsnachweis ist ausgeblendet | Der Leistungsnachweis ist in **Mitarbeiter-Self-Service** standardmäßig nicht sichtbar.  Ein Link wurde auf der rechten Seite von **Mitarbeiter-Self-Service** unter dem Abschnitt **Links** hinzugefügt |
| 629778 | Leistungsproblem bei der CDS-Integration. | Autorisierungsbezogene Anfrage verursachte Leistungsprobleme. |

## <a name="in-preview"></a>Vorschau

Die folgenden neuen Funktionen stehen in der Vorschau zur Verfügung. Weitere Informationen über das Ein- und Ausschalten von Funktionen finden Sie unter [Funktionen verwalten](hr-admin-manage-features.md).

| Funktion | Freigabeplan | Dokumentation |
|---|---|---|
| Arbeitsbereich für Vorteilsverwaltung | [Arbeitsbereich für die Verwaltung von Zusatzleistungen (Vorschau)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Arbeitsbereich „Vorteilsverwaltung“](hr-benefits-management-workspace.md) |


## <a name="coming-soon"></a>Demnächst
Eine vollständige Liste der geplanten Funktionen und ihrer geplanten Versionen finden Sie unter [Dynamics 365 und industrielle Clouds: 2021 Veröffentlichungszyklus 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
