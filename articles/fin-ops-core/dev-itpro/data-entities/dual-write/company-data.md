---
title: Unternehmenskonzept in Common Data Service
description: In diesem Thema wird die Integration von Unternehmensdaten zwischen Finance and Operations und Common Data Service beschrieben.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 08/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 444bfc1698a206ca34e67f742df63431a3b02649
ms.sourcegitcommit: 7da8811f1a7db858efb76edb0bdf857a47d07600
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2020
ms.locfileid: "3728412"
---
# <a name="company-concept-in-common-data-service"></a>Unternehmenskonzept in Common Data Service

[!include [banner](../../includes/banner.md)]


In Finance and Operations ist das Konzept *Unternehmen* sowohl ein juristisches als auch ein unternehmerisches Konstrukt. Es ist außerdem ein Sicherheits- und Sichtbarkeitsgrenze für Daten. Benutzer arbeiten immer im Kontext eines einzelnen Unternehmens, und die meisten Daten werden von dem Unternehmen gekennzeichnet.

Common Data Service hat kein entsprechendes Konzept. Das nächste Konzept ist *Unternehmenseinheit*, das in erster Linie eine Sicherheits- und Sichtbarkeitsgrenze für Benutzerdaten ist. Dieses Konzept besitzt nicht die gleichen rechten oder geschäftlichen Auswirkungen wie das Unternehmenskonzept.

Da Unternehmenseinheit und Unternehmen keine entsprechenden Konzepte sind, ist es nicht möglich, eine 1:1-Zuordnung zum Zwecke der Common Data Service-Integration zu erzwingen. Da Benutzer aber standardmäßig in der Lage sein müssen, dieselben Datensätze in der Anwendung und in Common Data Service anzuzeigen, hat Microsoft hat eine neue Entität in Common Data Service mit dem Namen „cdm\_Company“ eingeführt. Diese Entität entspricht der Unternehmensentität in der Anwendung. Um sicherzustellen, dass die Sichtbarkeit von Datensätzen in der Anwendung und Common Data Service standardmäßig äquivalent ist, empfehlen wir die folgende Einstellung für Daten in Common Data Service:

+ Für jeden Unternehmensdatensatz in Finance and Operations, für den duales Schreiben aktiviert ist, wird ein zugehöriger cdm\_Company-Datensatz erstellt.
+ Wenn ein cdm\_Company-Datensatz erstellt und für duales Schreiben aktiviert wird, wird eine Standardgeschäftseinheit mit demselben Namen erstellt. Es wird zwar automatisch ein Standardteam für diese Geschäftseinheit erstellt, die Geschäftseinheit wird aber nicht verwendet.
+ Ein separates Eigentümerteam wird erstellt, das denselben Namen hat. Es wird ebenfalls der Geschäftseinheit zugeordnet.
+ Standardmäßig wird der Eigentümer eines beliebigen Datensatzes, der erstellt und in Common Data Service dualgeschrieben wird, auf das Team „DW-Eigentümer“ festgelegt, das mit der zugehörigen Geschäftseinheit verknüpft ist.

Die folgende Abbildung zeigt ein Beispiel für diese Dateneinreichtung in Common Data Service.

![Dateneinrichtung in Common Data Service](media/dual-write-company-1.png)

Aufgrund dieser Konfiguration ist jeder Datensatz, der mit dem USMF-Unternehmen verknüpft ist, im Besitz eines Teams, das mit der USFM-Geschäftseinheit in Common Data Service verknüpft ist. Daher kann jeder Benutzer, der Zugriff auf diese Geschäftseinheit über eine Sicherheitsrolle hat, die auf Sichtbarkeit auf Geschäftseinheitsebene festgelegt ist, diese Datensätze nun anzeigen. Das folgende Beispiel veranschaulicht, wie Teams verwendet werden können, um den richtigen Zugang zu diesen Datensätzen bereitzustellen.

+ Die Rolle „Vertriebsmanager“ ist Mitgliedern des Teams „USMF-Vertrieb“ zugewiesen.
+ Benutzer mit der Rolle „Vertriebsmanager“ können auf beliebige Kontodatensätze zugreifen, die Mitglieder derselben Geschäftseinheit wie sie sind.
+ Das Team „USMF-Vertrieb“ wird mit der zuvor erwähnten USMF-Geschäftseinheit verknüpft.
+ Daher können Mitglieder des Teams „USMF-Vertrieb“ ein beliebiges Konto sehen, das im Besitz des Benutzers „USMF DW“ ist, der von der USMF-Unternehmenseinheit in Finance and Operations stammt.

![Wie Teams verwendet werden können](media/dual-write-company-2.png)

Wie in der vorherigen Abbildung dargestellt, ist diese 1:1-Zuordnung zwischen Geschäftseinheit, Unternehmen und Team nur ein Anfangspunkt. In diesem Beispiel wird eine neue Geschäftseinheit „Europa“ manuell in Common Data Service als übergeordnetes Element für DEMF und ESMF erstellt. Diese neue Stammgeschäftseinheit ist nicht mit dem dualen Schreiben verknüpft. Sie kann allerdings verwendet werden, um Mitgliedern des Teams „EUR-Vertrieb“ Zugriff auf Kontodaten sowohl in DEMF als auch in ESMF zu gewähren, indem die Datensichtbarkeit in der zugehörigen Sicherheitsrolle auf **Übergeordnete/untergeordnete Geschäftseinheit** festgelegt wird.

Ein abschließendes Thema ist, wie durch das duale Schreiben bestimmt wird, welchem Eigentümerteam Datensätze zugewiesen werden sollen. Dieses Verhalten wird vom Feld **Standardeigentümerteam** im Datensatz cdm\_Company gesteuert. Wenn ein cdm\_Company-Datensatz für duales Schreiben aktiviert ist, erstellt ein Plug-In automatisch die zugewiesene Geschäftseinheit und das Eigentümerteam (wenn nicht bereits vorhanden) und legt das Feld **Standardeigentümerteam** fest. Der Administrator kann das Feld in einen anderen Wert ändern. Allerdings kann der Administrator das Feld nicht deaktivieren, sofern die Entität für duales Schreiben aktiviert ist.

> [!div class="mx-imgBorder"]
![Feld „Standardeigentümerteam“](media/dual-write-default-owning-team.jpg)

## <a name="company-striping-and-bootstrapping"></a>Unternehmensstriping und Bootstrapping

Die Common Data Service-Integration bringt Unternehmensparität durch Verwendung eines Unternehmensbezeichners zum Kennzeichen von Daten. Wie in der folgenden Abbildung dargestellt, werden alle unternehmensspezifischen Entitäten so erweitert, dass sie eine Viele-zu-Eins-Beziehung (N:1) mit der cdm\_Company-Entität haben.

> [!div class="mx-imgBorder"]
![N:1-Beziehung zwischen einer unternehmensspezifischen Entität und der cdm_Company-Entität](media/dual-write-bootstrapping.png)

+ Für Datensätze wird der Wert schreibgeschützt, nachdem ein Unternehmen hinzugefügt und gespeichert wird. Daher sollten Benutzer sicherstellen, dass Sie das korrekte Unternehmen auswählen.
+ Nur Datensätze mit Unternehmensdaten kommen für duales Schreiben zwischen der Anwendung und Common Data Service infrage.
+ Für vorhandene Common Data Service-Daten wird in Kürze eine vom Administrator geführte Bootstrapping-Erfahrung verfügbar sein.


## <a name="autopopulate-company-name-in-customer-engagement-apps"></a>Unternehmensname in Kundenbindungs-Apps automatisch ausfüllen

Es gibt verschiedene Möglichkeiten, den Unternehmensnamen in Kundenbindungs-Apps automatisch auszufüllen.

+ Wenn Sie ein Systemadministrator sind, können Sie das Standardunternehmen festlegen, indem Sie zu **Erweiterte Einstellungen > System > Sicherheit > Benutzer** navigieren. Öffnen Sie das Formular **Benutzer**, und im Abschnitt **Organisationsinformationen** legen Sie den Wert **Unternehmen gemäß Standard auf Formularen** fest.

    :::image type="content" source="media/autopopulate-company-name-1.png" alt-text="Legen Sie im Abschnitt Organisationsinformationen das Standardunternehmen fest.":::

+ Wenn Sie **Schreib**-Zugriff auf die Entität **SystemUser** für die Ebene **Unternehmenseinheit** haben, können Sie das Standardunternehmen auf jedem beliebigen Formular ändern, indem Sie ein Unternehmen aus dem Dropdownmenü **Unternehmen** auswählen.

    :::image type="content" source="media/autopopulate-company-name-2.png" alt-text="Ändern des Unternehmensnamens bei einem neuen Konto.":::

+ Wenn Sie **Schreib**-Zugriff auf Daten in mehr als einem Unternehmen haben, können Sie das Standardunternehmen ändern, indem Sie einen Datensatz auswählen, der zu einem anderen Unternehmen gehört.

    :::image type="content" source="media/autopopulate-company-name-3.png" alt-text="Durch Auswahl eines Datensatzes wird die Standardunternehmen geändert.":::

+ Wenn Sie ein Systemkonfigurator oder -Administrator sind und Unternehmensdaten automatisch in ein benutzerdefiniertes Formular einfügen möchten, können Sie [Formularereignisse](https://docs.microsoft.com/powerapps/developer/model-driven-apps/clientapi/events-forms-grids) verwenden. Fügen Sie einen JavaScript-Verweis auf **msdyn_/DefaultCompany.js** hinzu, und verwenden Sie die folgenden Ereignisse. Sie können jedes sofort einsatzbereite Formular verwenden, z. B. das **Konto**-Formular.

    + **OnLoad**-Ereignis für das Formular: Legen Sie das Feld **defaultCompany** fest.
    + **OnChange**-Ereignis für das Feld **Unternehmen**: Legen Sie das Feld **updateDefaultCompany** fest.

## <a name="apply-filtering-based-on-the-company-context"></a>Wenden Sie die Filterung basierend auf dem Unternehmenskontext an

Um die Filterung in Ihren benutzerdefinierten Formularen oder in benutzerdefinierten Suchfeldern, die den Standardformularen hinzugefügt wurden, basierend auf dem Unternehmenskontext anzuwenden, öffnen Sie das Formular, und verwenden Sie den Abschnitt **Filterung zugehöriger Datensätze**, um den Unternehmensfilter anzuwenden. Sie müssen dies für jedes Suchfeld festlegen, das die Filterung basierend auf dem zugrunde liegenden Unternehmen für einen bestimmten Datensatz erfordert. Die Einstellung wird für **Konto** in der folgenden Abbildung angezeigt.

:::image type="content" source="media/apply-company-context.png" alt-text="Unternehmenskontext anwenden":::

