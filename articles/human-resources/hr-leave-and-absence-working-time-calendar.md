---
title: Erstellen eines Arbeitszeitkalenders
description: Definieren Sie einen Arbeitszeitkalender, Feiertage und arbeitsfreie Zeiten in Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 04/01/2020
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
ms.openlocfilehash: dc209b62836011b18362f78b63cdd3fcda884dc3
ms.sourcegitcommit: 79f8aa2c0b166a423db9b8503da53e96e3fc43dc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3198026"
---
# <a name="create-a-working-time-calendar"></a>Erstellen eines Arbeitszeitkalenders

Ein Arbeitszeitkalender in Dynamics 365 Human Resources zeigt die Tage und Stunden an, an denen Mitarbeiter in Ihrer Organisation arbeiten. Wenn ein Mitarbeiter eine Freistellung beantragt, muss er sich keine Gedanken über Feiertage und Schließungen machen.

Konfigurieren Sie die folgenden Elemente für Ihre Organisation, um Anfragen nach Freizeit zu optimieren:

- Arbeitszeitkalender
- Feiertage und Schließungen
- Arbeitsfreie Zeit

Sie können die letzten beiden Elemente hinzufügen, während Sie einen Arbeitszeitkalender einrichten. Sie können sie auch separat konfigurieren oder aktualisieren.

## <a name="set-up-a-working-time-calendar"></a>Einen Arbeitszeitkalender einrichten

Richten Sie mindestens einen Arbeitszeitkalender ein, der Ihre Tage und Betriebsstunden anzeigt. Wenn Sie Standorte in mehreren Ländern und Regionen haben, möchten Sie möglicherweise einen Arbeitszeitkalender für jeden Bereich einrichten.

1. Klicken Sie auf der Seite **Organisationsadministration** auf **Kalender**.

2. Geben Sie unter **Neu** einen Namen und eine Beschreibung für Ihren Kalender ein.

3. Unter **Generierungsoptionen** wählen Sie die Arbeitstage für Ihre Organisation aus und geben Sie die Arbeitszeiten ein. 
   - Um einen Feiertag oder eine Schließung hinzuzufügen, wählen Sie die Schaltfläche **Hinzufügen** neben **Feiertage und Schließungen**.
   - Wählen Sie, um arbeitsfreie Zeiten wie Mittagessen oder Pausen hinzuzufügen, wählen Sie **Hinzufügen** unter **Arbeitsfreie Zeit** und geben Sie den Namen und den Zeitraum ein.

4. Unter **Tage** wählen Sie **Generieren**, um die Tage in dem Kalender zu generieren. Geben Sie den Datumsbereich für Ihren Kalender ein und wählen Sie dann **Tage generieren**.

5. Um Arbeitszeitpläne hinzuzufügen, gehen Sie zu **Arbeitsplan** und wählen **Hinzufügen** und geben Sie dann die Zeiten für jeden Arbeitszeitplan ein.

## <a name="configure-holidays-and-closures"></a>Feiertage und Schließungen konfigurieren

Sie können Feiertage und Schließungen separat von einem Arbeitszeitkalender hinzufügen oder ändern.

1. Klicken Sie auf der Seite **Organisationsadministration** auf **Feiertage und Schließungen**.

2. Geben Sie unter **Neu** einen neuen Namen und ein Datum für die Daten und Schließungen ein.

## <a name="configure-non-work-time"></a>Arbeitsfreie Zeit konfigurieren

Sie können Feiertage und Schließungen separat von einem Arbeitszeitkalender hinzufügen oder ändern.

1. Klicken Sie auf der Seite **Organisationsadministration** auf **Arbeitsfreie Zeit**.

2. Wählen Sie **Neu** und geben Sie einen Namen und den Zeitraum für die arbeitsfreie Zeit ein.

Wenn Sie die Vorschau für Urlaubs- und Abwesenheitskorrekturen für Feiertage aktiviert haben, verwendet die Personalabteilung Feiertage und Schließungsdaten, um die Anzahl der Tage zu bestimmen, die für die im Kalender registrierten Mitarbeiter angepasst werden müssen.

## <a name="see-also"></a>Siehe auch

- [Urlaubs- und Abwesenheitsübersicht](hr-leave-and-absence-overview.md)
- [Urlaubs- und Abwesenheitstypen konfigurieren](hr-leave-and-absence-types.md)