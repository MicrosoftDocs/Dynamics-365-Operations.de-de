---
title: Talent mit Power Apps und Power Automate erweitern
description: Dieser Artikel beschreibt einige Beispiele für Erweiterungsszenarien für Microsoft Dynamics 365 Talent - Attract, die Microsoft Power Apps und Microsoft Power Automate verwenden.
author: negudava
manager: Annbe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent;Core;Experience Apps
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: cfdf36e9486aa4853d3bf674afa73ec3a4d1c161
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529633"
---
# <a name="extend-talent-with-power-apps-and-power-automate"></a>Talent mit Power Apps und Power Automate erweitern

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dieser Artikel beschreibt einige Beispiele für Erweiterungsszenarien für Microsoft Dynamics 365 Talent: Attract, die Microsoft Power Apps und Microsoft Power Automate verwenden. Sie können das Lösungspaket importieren, das jedem Beispiel in der Power Apps-Umgebung zugeordnet ist. Sie können entweder die Pakete als Anleitung oder als Startpunkte zu den Werkzeugszenarien verwenden, die der Organisation zugeordnet sind.

> [!IMPORTANT]
> Wenn Sie die Vorlagen und Apps verwenden möchten, die in diesem Artikel als „wie vorliegend“ beschrieben sind, müssen Sie diese unbedingt testen, um sicherzustellen, dass sie alle Szenarien beinhalten, die für Ihre Implementierung bestimmt sind.


## <a name="prerequisites"></a>Voraussetzungen

- Um Pakete zu importieren, müssen Benutzer die Berechtigung **Umgebungs-Hersteller** haben.
- Um Apps zu exportierenden oder zu importieren, müssen Benutzer eine Lizenz für Power Apps Plan 2 oder eine Testlizenz für Power Apps-Plan 2 haben.

## <a name="power-automate--form-connect"></a>Power Automate - Formular Verbinden

Die Vorlage **Power Automate - Formular Verbinden** kann verwendet werden, um Daten aus Microsoft Forms zu lesen und in einer Common Data Service Einheit zu speichern.

Diese Vorlage kann auch erweitert werden, sodass sie für andere Szenarien verwendet werden kann. Nachfolgend finden Sie einige Beispiele:

- Kandidatenbewertungen aufzeichnen.
- Zeichnen Sie Ergebnisse aus Kursfragebögen auf.
- Kompilieren Sie eine Bibliothek von Gesprächsfragen für die Personalverwaltungs (HR)-Administratoren.
- Zeichnen Sie die Bewertung des Kandidaten aus dem Gesprächsprozess auf

In Microsoft Dynamics 365: Attract können Sie Formulare im Kandidatenportal nutzen, bei dem Kandidaten die Details selbst eingeben. Sie können Formulare auch als Aktivitäten in die Stellenvorlage einbetten.

Wenn ein Kandidat ein Formular abschickt, erfasst Microsoft Power Automate die Formularabgabe, liest die Daten und speichert sie in der Entität Common Data Service.

Um die **Power Automate - Formular verbinden** Vorlage und benutzerdefinierte Entitätsstruktur herunterzuladen, gehen Sie zu [Power Automate - Formular verbinden](https://go.microsoft.com/fwlink/?linkid=2081988) im Microsoft Download Center.

## <a name="power-automate--sharepoint-integration"></a>Power Automate - SharePoint Integration

Die Vorlage **Power Automate - SharePoint Integration** kann verwendet werden, um Daten aus einer Microsoft SharePoint-Liste zu lesen, die Liste mit Feldwerten für jede Common Data Service-Einheit zu vergleichen und die Ergebnisse des Vergleichs als Benachrichtigungs-E-Mail zu senden. 

Eine Organisation hat möglicherweise eine Reihe von Fähigkeiten, die sie dringend benötigt. Diese Qualifikationen können in SharePoint als Liste SharePoint gespeichert werden. Wenn sich ein Kandidat für eine Stelle bewirbt, die Qualifikationen verlangt, die aufgelistet sind und wenn es eine erhebliche Übereinstimmung zwischen den Fähigkeiten des Kandidaten und den Qualifikationen gibt, die in SharePoint gespeichert sind, wird eine  Benachrichtigungs-E-Mail übermittelt. Auf diese Weise werden Positionen, die dringend erforderlich sind, schneller besetzt, da die Benachrichtigungen den Personalbeschaffern helfen, Kandidaten aus der gesamten Organisation zu finden.

Diese Vorlage kann auch erweitert werden, sodass sie für ein beliebiges Szenario verwendet werden kann, das die SharePoint Integration betrifft.

Um die Vorlage **Power Automate - SharePoint Integration** herunterzuladen, gehen Sie zu [Power Automate - SharePoint Integration](https://go.microsoft.com/fwlink/?linkid=2082109) im Microsoft Download Center.

## <a name="referral-app"></a>Bezugs-App

Sie können die Empfehlungs-App verwenden, um Kandidaten einer freigegebene Talentschmiede hinzuzufügen. Der Verweiser kann **Vorname**, **Nachname**, **E-Mail** und **LinkedIn-URL** eingeben, wenn er den Kandidaten übermittelt. Die Kandidatenquellenmetadaten werden dann mit den Informationen des Empfehlers ausgefüllt.

Sie können dieser App im Mitarbeiter-Self-Service für das Übermitteln von Empfehlungen einbetten oder Sie können sie als Verknüpfung im Unternehmensportal und als eigenständige App verwenden.

Um die **Empfehlungs-App** herunterzuladen, gehen Sie zur [Dynamics 365 Talent Erweiterbarkeitslösung: Empfehlungs-App](https://www.microsoft.com/download/details.aspx?id=58497) im  Microsoft Download Center. Sie können diese App importieren und anpassen, um weitere Funktionen hinzuzufügen.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Das Microsoft Power Platform](https://docs.microsoft.com/power-platform/admin/admin-documentation)</br>
[Migrieren der App zwischen Mandanten und Umgebung](https://docs.microsoft.com/power-platform/admin/environment-and-tenant-migration)
