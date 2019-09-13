---
title: Planungen, Arbeitsaufträge und Projekte
description: In diesem Thema wird die Integration von Planungen und Arbeitsaufträgen in das Projektverwaltungs- und Buchhaltungsmodul in der Anlagenverwaltung erklärt.
author: josaw1
manager: AnnBe
ms.date: 08/16/2019
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
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5e986d139ac9d0a7729bb9787f05332bcc09f59b
ms.sourcegitcommit: 109a6ef2d20758dc4a25c51b11e22dd2214a1cc4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/16/2019
ms.locfileid: "1886815"
---
# <a name="forecasts-work-orders-and-projects"></a>Planungen, Arbeitsaufträge und Projekte

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

In der Anlagenverwaltung wird die Integration in das Modul **Projektverwaltung und Buchhaltung** ausgeführt, um die Kostenkontrolle zu optimieren, sodass Benutzer die Kosten für die Wartungsauftragstyp-Planungen und Arbeitsauftragseinzelvorgänge nachverfolgen können.

Um Wartungsauftragstyp-Planungen nachzuverfolgen, sind zwei Einstellungen erforderlich:

1. Wählen Sie ein Projekt im Link **Anlagenverwaltung** > **Einstellungen** > **Anlagenverwaltungsparameter** > **Anlagen** > Inforegister **Projekt** > Feld **Wartungsprognoseprojekt** aus.

2. In **Wartungsauftragstyp-Standardwerte**, wenn Sie eine Wartungsauftragstyp-Standardposition erstellen, wird automatisch eine Aktivitätsnummer für die Position (**Anlagenverwaltung** > **Einstellungen** > **Einzelvorgänge** > **Wartungsauftragstyp-Standardwerte**) erstellt.

Wartungsauftragstyp-Planungen erfüllen zwei Funktionen: Sie können Kosten für Wartungsauftragstyp-Planungen im Modul **Projektverwaltung und Buchhaltung** nachverfolgen. Weiterhin werden Planungen automatisch einem Arbeitsauftragseinzelvorgangsprojekt übertragen, wenn Sie einen Wartungsauftragstyp für einen Arbeitsauftragseinzelvorgang auswählen.

Um Arbeitsauftragseinzelvorgänge nachzuverfolgen, müssen Sie zunächst Arbeitsauftragsprojekte einrichten. Im Abschnitt [Arbeitsauftrags-Projekteinstellungen](../setup-for-work-orders/work-order-project-setup.md) finden Sie eine Beschreibung der Prozedur.

## <a name="work-order-job-projects"></a>Einzelvorgangsprojekte für Arbeitsaufträge

Wenn Sie einen Arbeitsauftragseinzelvorgang für einen Arbeitsauftrag erstellen, wird das Arbeitsauftragsprojekt von der Einstellung des übergeordneten Projekts für Arbeitsaufträge in **Anlagenverwaltung** > **Einstellungen** > **Arbeitsaufträge** > **Projekteinstellungen** bestimmt.

Arbeitsauftragseinzelvorgangsprojekte werden erstellt, indem eine Kombination aus den folgenden Arbeitsauftragsinformationen verwendet wird:

- Der Arbeitsauftragstyp, der für den Arbeitsauftrag ausgewählt wurde 
- Der funktionale Standort im Zusammenhang mit der Anlage für den Arbeitsauftragseinzelvorgang
- Der Anlagentyp im Zusammenhang mit der Anlage für den Arbeitsauftragseinzelvorgang  
- Die voraussichtliche Start- und Endzeit, die für den Arbeitsauftrag festgelegt wurde  

Es ist möglich, dass nicht alle Informationen, die oben genannten werden, zu einem Arbeitsauftrag gefunden werden. Daher erfolgt die Suche nach einem übergeordneten Arbeitsauftragsprojekt über die verfügbare Kombination von Daten und die Auswahl der Projektkennung, die den Arbeitsauftragsdaten entspricht.

Beispiel: In der nachfolgenden Abbildung bedeuten die Einstellungen des Anlagentyps „Lkw-Motor“, dass jeder Arbeitsauftragseinzelvorgang, der mit diesem Anlagentyp erstellt wird, ein Unterprojekt der Projektkennung „000186“ ist.

![Abbildung 1](media/01-integration-to-pma.png)

Der Zweck der Projektkennung für den Arbeitsauftragseinzelvorgang und die zugeordnete Aktivitätsnummer (**Anlagenverwaltung** > **Allgemein** > **Arbeitsaufträge** > **Alle Arbeitsaufträge** > wählen Sie Arbeitsauftrag in der Liste > Inforegister **Positionsdetails** > Feld **Projektkennung** und Feld **Aktivitätsnummer** aus), ist die Nachverfolgung der Kosten im Zusammenhang mit dem Arbeitsauftragseinzelvorgang und der Anlage, die für den Arbeitsauftragseinzelvorgang im Modul **Projektverwaltung und Buchhaltung** ausgewählt wird. 

In der nachfolgenden Abbildung finden Sie eine grafische Übersicht der Arbeitsauftragsprojekte und zugehörigen Projektaktivitäten.

![Abbildung 2](media/02-integration-to-pma.png)

Wenn ein neuer Arbeitsauftragseinzelvorgang für einen Arbeitsauftrag erstellt wird, wird automatisch ein Arbeitsauftragsprojekt für den Einzelvorgang erstellt. Die Finanzdimensionen für die Anlage im Zusammenhang mit dem Arbeitsauftragseinzelvorgang werden automatisch an das Arbeitsauftragsprojekt übertragen. Der Projektaktivität, die für einen Arbeitsauftragseinzelvorgang erstellt wird, sind die zugehörigen Informationen in Bezug auf Wartungsauftragstyp, Wartungsauftragstypvariante und Handel angefügt. Diese Daten sind z. B. hilfreich, wenn Sie eine Bestellung aus einem Arbeitsauftrag erstellen (siehe [Beschaffung](../work-orders/procurement.md)) oder das Modul **Projektverwaltung und Buchhaltung** für die Zeiterfassung verwenden.  

Wenn die Anlage für einen funktionalen Standort eingerichtet wurde und diese Anlage später für einen anderen funktionalen Standort eingerichtet wird, werden die Finanzdimensionen, die dem neuen funktionalen Standort zugeordnet sind, automatisch für die Anlage aktualisiert. Danach, wenn Sie einen Arbeitsauftragseinzelvorgang für die Anlage erstellen, erhält das Arbeitsauftragsprojekt für den Arbeitsauftragseinzelvorgang automatisch die Finanzdimensionen, die jetzt der Anlage zugeordnet sind. Das bedeutet, dass, wenn Sie funktionale Standorte verwenden, die Kosten für die funktionalen Standorte, für die eine Anlage zu einem beliebigen Zeitpunkt eingerichtet wurde, immer nachverfolgt werden können. Die automatische Aktualisierung der Finanzdimensionen stellt die vollständige Nachverfolgbarkeit der Kosten für das Projekt-Controlling und -Reporting sicher.  


## <a name="work-order-projects-work-order-lifecycle-states-project-stages-and-project-types"></a>Arbeitsauftragsprojekte, Arbeitsauftrags-Lebenszyklusstatus, Projektphasen und Projekttypen

Zur richtigen Verwendung von Arbeitsauftrags-Lebenszyklusstatus und zugehörigen Projektphasen für Arbeitsaufträge beachten Sie die Abhängigkeiten in Beziehung zum Modul **Projektverwaltung und Buchhaltung**:

- Im Modul **Projektverwaltung und Buchhaltung** werden die Projektphasen für Projekttypen unter **Projektverwaltungs- und Buchhaltungsparameter** eingerichtet.  
- In **Projektverwaltungs- und Buchhaltungsparameter** denken Sie daran, entsprechende Projektphasenkontrollkästchen für alle Projekttypen auszuwählen, die Sie verwenden möchten. In der nachfolgenden Abbildung wurden die fünf Phasen **Erstellt** - **Vorkalkuliert** - **Eingeplant** - **In Bearbeitung** - **Abgeschlossen** für die Projekttypen für „Nach Aufwand“ und „Intern“ ausgewählt. Diese fünf Phasen sind für interne Wartungs- und Dienstwartungsaufträge relevant.  
- In **Anlagenverwaltung** werden Projekttypen von den Projektgruppen definiert, die Sie im Formular **Arbeitsauftrags-Projekteinstellungen** > Link **Projektgruppe** eingerichtet haben.  
- Die Projektgruppeneinstellungen in **Arbeitsauftrags-Projekteinstellungen** werden verwendet, wenn Sie Arbeitsaufträge erstellen. Wenn ein Arbeitsauftrag erstellt wird, wird automatisch ein Arbeitsauftragsprojekt für den Arbeitsauftrag erstellt.  
- Arbeitsauftrags-Lebenszyklusstatus müssen jeweils eine zugehörige Projektphase haben.  
- Die Projektphase, die einem Arbeitsauftrags-Lebenszyklusstatus zugeordnet ist, muss als aktive Phase für die Projektgruppe definiert werden, die im Arbeitsauftragsprojekt definiert wird. Das Arbeitsauftragsprojekt wird automatisch für einen Arbeitsauftrag erstellt.  
- Wenn Sie einen neuen Arbeitsauftrag erstellen, basiert die automatische Zuteilung eines Arbeitsauftragsprojekts auf den Einstellungen in **Arbeitsauftrags-Projekteinstellungen** (**Anlagenverwaltung** > **Einstellungen** > **Arbeitsaufträge** > **Projekteinstellungen**).  

Zuordnungen zwischen Arbeitsauftragsprojektgruppen, zugehörigen Projekttypen, Projektphasen und Arbeitsauftrags-Lebenszyklusstatus werden unten angezeigt.  

![Abbildung 3](media/03-integration-to-pma.png)

![Abbildung 4](media/04-integration-to-pma.png)

![Abbildung 5](media/05-integration-to-pma.png)

In [Arbeitsauftrags-Projekteinstellungen](../setup-for-work-orders/work-order-project-setup.md) erfahren Sie, wie Arbeitsauftragsprojekte eingerichtet werden, und in [Arbeitsauftrag-Lebenszyklusstatus](../setup-for-work-orders/work-order-lifecycle-states.md), wie Arbeitsauftrag-Lebenszyklusstatus erstellt werden.

Die folgende Abbildung zeigt einen grafischen Überblick der verschiedenen Projekte, die im Modul **Anlagenverwaltung** erstellt wurden, um die Integration in das Modul **Projektverwaltung und Buchhaltung** zu ermöglichen, sowie die Arbeitsprozesse, denen die Projekte zugeordnet sind.

![Abbildung 6](media/06-integration-to-pma.png)

