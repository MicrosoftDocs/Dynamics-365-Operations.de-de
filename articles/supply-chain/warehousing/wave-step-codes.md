---
title: Wellenschrittcodes
description: Dieses Thema bietet einen Überblick über Wellenschrittcodes und wie diese verwendet werden.
author: josaw1
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1a1a32495b63a5a67a49bf3b02710aba63c1e2f0
ms.sourcegitcommit: bfd6142569196a060e3f37893c78f00c40a2a18c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/09/2020
ms.locfileid: "2946189"
---
# <a name="wave-step-codes"></a>Wellenschrittcodes

[!include [banner](../includes/preview-banner.md)]
[!include [banner](../includes/banner.md)]

Wellenschrittcodes sind Codes, die Benutzer einrichten und verwenden können, um bestimmte Instanzen von Wellenmethoden mit einer entsprechenden Vorlage zu verknüpfen. Die Vorlagen enthalten Vorlagen für die Auffüllung, Containerisierung, Etikettendruck, Auslastungsgebäude und Sortieren.

Wenn keine Wellenschrittcodes verwendet werden, müssen Benutzer Freitext eingeben, um auf eine bestimmte Vorlage aus der Wellenmethodeninstanz zu verweisen. Freier Text ist fehleranfällig, da Benutzer sicherstellen müssen, dass der Wellenschritttext, den sie für eine bestimmte Wellenschrittmethode in einer Wellenvorlage hinzufügen, genau mit dem Wellenschritttext in der Zielvorlage übereinstimmt.

Wellenschrittcodes für einen bestimmten Wellenschritttyp werden auf einer separaten Seite eingerichtet. Für jede Wellenschritt-Methodeninstanz in einer Wellenvorlage, die einen Wellenschrittcode erfordert, muss der Wellenschrittcode in einer Dropdownliste ausgewählt werden. Die Auswahl in einer Dropdownliste ersetzt den freien Texteintrag und hilft, das Risiko und die Auswirkungen des menschlichen Versagens zu verringern. Einstellungscodes werden verwendet, um eine Wellenschrittmethode in einer Wellenvorlage zu einer Zielvorlage für die Methode zu verknüpfen.

> [!NOTE]
> Die Verwendung der Wellenschrittcode-Funktion ist optional. Sie ist organisationsweit für alle juristischen Personen aktiviert.

## <a name="setup-demo"></a>Demo einrichten 

Für diese Vorführung müssen Demodaten eingerichtet werden, und Sie müssen das **USMF**-Demodatunternehmen verwenden.

### <a name="enable-wave-step-codes"></a>Wellenschrittcodes aktivieren

Gehen Sie folgendermaßen vor, um die Wellenschritt-Codefunktion zu aktivieren.

1. Navigieren Sie zu **Funktionsverwaltung**.
2. Wählen Sie diese Option aus, um die Funktion mit der Bezeichnung **Organisationsweiter Wellenschrittcode** zu aktivieren.

Alle Freitexte des vorhandenen Wellenschritts in allen juristischen Personen werden in der neuen Struktur aktualisiert. Nachdem dieses Upgrade für alle juristischen Personen abgeschlossen ist, wird die Funktion aktiviert. Wenn die Funktion für eine oder mehrere juristische Personen nicht aktiviert werden kann, ist die Funktion für keine juristische Person aktiviert.

Während der Aktivierung werden Überprüfungen während der Datenaktualisierung durchgeführt. Wenn das Upgrade fehlschlägt, erhalten Sie eine Fehlermeldung. Eine Aktualisierung kann aufgrund der folgenden Konflikte fehlschlagen:

- Es sind doppelte Freitexte des Wellenschritts vorhanden.
- Es sind Anpassungen vorhanden.
- Ein Wellenschrittfreitext, der einer Wellenschritt-Methodeninstanz zugeordnet ist, entspricht nicht dem erwarteten Vorlagentyp.

Nachdem Sie alle Konflikte behoben haben, die während der Überprüfung aufgetreten sind, können Sie erneut versuchen, die Funktion zu aktivieren.

Wenn die Funktion aktiviert wurde, wird die Seite **Wellenschrittcodes** (**Lagerortverwaltung \> Einstellungen \> Wellen \> Wellenschrittcodes**) verfügbar. Auf dieser Seite werden die Wellenschrittcodes aufgelistet, die aktualisiert wurden, als die Funktion „Organisationsweiter Wellenschrittcode“ aktiviert wurde.

### <a name="create-new-wave-step-codes"></a>Erstellen neuer Wellenschrittcodes

Sie können die Seite **Wellenschrittcodes** verwenden, um Wellenschrittcodes zu erstellen und zu löschen.

Jeder neue Wellenschrittcode und die zugeordnete Kennung müssen für alle Wellenschritttypen eindeutig sein, und sie müssen für einen bestimmten Wellenschritttyp definiert werden.

### <a name="apply-wave-step-codes"></a>Wellenschrittcodes anwenden

Nachdem Sie die gewünschten Wellenschrittcodes definiert haben, können sie auf die Wellenprozessmethoden angewendet werden.

Um Wellenschrittcodes anzuwenden, wechseln zur entsprechenden Zielvorlage. Hierbei gelten die Zielvorlagen, auf die die Wellenschrittcodes verweisen:

- **Wiederbeschaffungsvorlagen:** Lagerortverwaltung \> Einstellungen \> Wiederbeschaffung \> Wiederbeschaffungsvorlagen
- **Ladungserstellungsvorlagen:** Lagerortverwaltung \> Einstellungen \> Laden \> Ladungserstellungsvorlagen
- **Vorlagen sortieren:** Lagerortverwaltung \> Einstellungen \> Verpackung \> Ausgehende Sortierenvorlagen
- **Containerisierungsvorlagen:** Lagerortverwaltung \> Einstellungen \> Container \> Containererstellungsvorlagen
- **Etikettendruckvorlagen:** Lagerortverwaltung \> Einstellungen \> Dokumentweiterleitung \> Wellenbeschriftungsvorlagen

Die Vorlagen in dieser Liste werden angewendet, wenn auf sie aus einer Wellenprozessmethode verwiesen wird, die in einer Wellenvorlage aktiviert ist. Wenn der Wellenschrittcode auf einer Wellenprozessmethode in einer Wellenvorlage den Wellenschrittcode in einem der Vorlagentypen entspricht, wird die Vorlage angewendet.

### <a name="sample-scenario"></a>Beispielszenario

Die folgenden Prozedurhilfen stellen sicher, dass die Wiederbeschaffungsvorlage, die Sie erstellt haben, auf die Wellenvorlage angewendet wird.

1. Navigieren Sie zu **Lagerortverwaltung \> Einstellungen \> Wellen \> Wellenschrittcodes**, und erstellen Sie einen Wellenschrittcode für den Typ **Wiederbeschaffung**.
2. Navigieren Sie zu **Lagerortverwaltung \> Einstellungen \> Wiederbeschaffung \> Wiederbeschaffungsvorlagen**, und erstellen Sie eine Wiederbeschaffungsvorlage.
3. In der Wiederbeschaffungsvorlage wählen Sie den Wellenschrittcode aus, den Sie für die Art haben **Wiederbeschaffung**
4. Navigieren Sie zu **Lagerortverwaltung \> Einstellungen \> Wellen \> Wellenvorlagen**, und wählen Sie die Wellenvorlage aus, die Sie verwenden möchten.
5. In der Vorlage auf dem Inforegister **Methoden** wählen Sie die Methode **Wiederbeschaffung**.
6. Im Feld **Wellenschrittcode** wählen Sie den Wellenschrittcode aus, den Sie für die Wiederbeschaffungsvorlage ausgewählt haben.

Sie führen diese Schritte für jede juristische Person aus.
