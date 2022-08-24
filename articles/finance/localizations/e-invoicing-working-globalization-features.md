---
title: Komponenten der Funktionen für die Globalisierung
description: Dieser Artikel gibt Ihnen einen Überblick über die Funktionen der Globalisierung.
author: gionoder
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 94e2d118c332a15f41f33184f5e44b0fdaccd000
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275225"
---
# <a name="globalization-feature-components"></a>Komponenten der Funktionen für die Globalisierung

[!include [banner](../includes/banner.md)]

Eine Funktion zur Globalisierung ist eine Reihe von Komponenten, die die Regeln für die Datentransformation in Konfigurationen für die elektronische Berichterstattung (ER) festlegen. Diese Komponenten enthalten Anweisungen zum Verarbeiten elektronischer Belege und zum anschließenden Versenden oder Empfangen dieser Belege über externe Kanäle. Sie enthalten auch Bedingungen, die festlegen, wann eine Funktion für die eingehenden Geschäftsdaten ausgeführt werden soll.

Alle Komponenten hängen voneinander ab. Globalisierungsfunktionen erleichtern das Erstellen und Pflegen dieser Abhängigkeiten und unterstützen die Lebenszyklusverwaltung und Versionsverwaltung des Komponentensatzes.

## <a name="access-electronic-invoicing-feature-components"></a>Zugriff auf die Funktionen der Elektronischen Rechnungsstellung 

1. Melden Sie sich bei Ihrem RCS-Konto (Regulatory Configuration Service) an.
2. Wählen Sie im Abschnitt **Funktionen** des Arbeitsbereichs **Globalisierungsfunktion** die Kachel **Elektronische Rechnungsstellung** aus.

    Globalisierungsfunktionen haben mehrere Komponenten. Die Seite **Funktionen für die elektronische Rechnungsstellung** enthält für jede Komponente eine eigene Registerkarte.

    - **Version** - Diese Komponente unterstützt die Lebenszyklusverwaltung der Funktion. Sie können damit den Status für verschiedene Versionen der Funktion verwalten.
    - **Konfigurationen** - Mit dieser Komponente können Sie zugehörige ER-Format- und Formatzuordnungskonfigurationen, die in der Pipeline für die Verarbeitung verwendet werden, verwalten, anzeigen und bearbeiten.
    - **Einrichtungen** – Mit dieser Komponente können Benutzer von Globalisierungsdiensten, z. B. einem E-Invoicing-Dienst, die Einrichtung der zugehörigen Funktionsversion verwalten. Daher unterstützt es die flexible Erstellung von Kommunikations- und Antwortregeln.
    - **Umgebungen** - Mit dieser Komponente können Benutzer von Globalisierungsdiensten, wie z.B. einem E-Invoicing-Dienst, die Umgebung verwalten, in der die Einrichtung der Funktion Version verwendet wird. Außerdem können sie den Benutzern, die Zugriff auf die Einrichtung der Funktion Version haben werden, eine Berechtigung erteilen.
    - **Organisationen** - Mit dieser Komponente können Benutzer die Funktion mit externen Organisationen teilen.
    - **Tags** - Mit dieser Komponente können Sie Funktionen markieren, die im Globalization Blueprint als Referenz verwendet werden können.
