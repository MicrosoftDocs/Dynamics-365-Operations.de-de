---
title: Unternehmenskonzept in Dataverse
description: In diesem Thema wird die Integration von Unternehmensdaten zwischen Finance and Operations und Dataverse beschrieben.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: bbe634b87b3cb30ed993f9b3afeb4321d70f07e6
ms.sourcegitcommit: 7e1be696894731e1c58074d9b5e9c5b3acf7e52a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4744878"
---
# <a name="company-concept-in-dataverse"></a>Unternehmenskonzept in Dataverse

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]


In Finance and Operations ist das Konzept *Unternehmen* sowohl ein juristisches als auch ein unternehmerisches Konstrukt. Es ist außerdem ein Sicherheits- und Sichtbarkeitsgrenze für Daten. Benutzer arbeiten immer im Kontext eines einzelnen Unternehmens, und die meisten Daten werden von dem Unternehmen gekennzeichnet.

Dataverse hat kein entsprechendes Konzept. Das nächste Konzept ist *Unternehmenseinheit*, das in erster Linie eine Sicherheits- und Sichtbarkeitsgrenze für Benutzerdaten ist. Dieses Konzept besitzt nicht die gleichen rechten oder geschäftlichen Auswirkungen wie das Unternehmenskonzept.

Da Unternehmenseinheit und Unternehmen keine entsprechenden Konzepte sind, ist es nicht möglich, eine 1:1-Zuordnung zum Zwecke der Dataverse-Integration zu erzwingen. Da Benutzer aber standardmäßig in der Lage sein müssen, dieselben Zeilen in der Anwendung und in Dataverse anzuzeigen, hat Microsoft eine neue Tabelle in Dataverse mit dem Namen „cdm\_Company“ eingeführt. Diese Tabelle entspricht der Unternehmenstabelle in der Anwendung. Um sicherzustellen, dass die Sichtbarkeit von Zeilen in der Anwendung und in Dataverse standardmäßig äquivalent ist, empfehlen wir die folgende Einstellung für Daten in Dataverse:

+ Für jede Unternehmensdatenszeile in Finance and Operations, für die duales Schreiben aktiviert ist, wird eine zugehörige cdm\_Company-Zeile erstellt.
+ Wenn eine cdm\_Company-Zeile erstellt und für duales Schreiben aktiviert wird, wird eine Standardunternehmenseinheit mit demselben Namen erstellt. Es wird zwar automatisch ein Standardteam für diese Geschäftseinheit erstellt, die Geschäftseinheit wird aber nicht verwendet.
+ Ein separates Eigentümerteam wird erstellt, das denselben Namen hat. Es wird ebenfalls der Geschäftseinheit zugeordnet.
+ Standardmäßig wird der Eigentümer einer beliebigen Zeile, die erstellt und in Dataverse dual geschrieben wird, auf das Team „DW-Eigentümer“ festgelegt, das mit der zugehörigen Unternehmenseinheit verknüpft ist.

Die folgende Abbildung zeigt ein Beispiel für diese Dateneinreichtung in Dataverse.

![Dateneinrichtung in Dataverse](media/dual-write-company-1.png)

Aufgrund dieser Konfiguration ist jede Zeile, due mit dem USMF-Unternehmen verknüpft ist, im Besitz eines Teams, das mit der USFM-Unternehmenseinheit in Dataverse verknüpft ist. Daher kann jeder Benutzer, der über eine Sicherheitsrolle Zugriff auf diese Unternehmenseinheit hat, die auf Sichtbarkeit auf Unternehmenseinheitsebene festgelegt ist, diese Zeilen nun anzeigen. Das folgende Beispiel veranschaulicht, wie Teams verwendet werden können, um den richtigen Zugang zu diesen Zeilen bereitzustellen.

+ Die Rolle „Vertriebsmanager“ ist Mitgliedern des Teams „USMF-Vertrieb“ zugewiesen.
+ Benutzer mit der Rolle „Vertriebsmanager“ können auf beliebige Kontozeilen zugreifen, die Mitglieder derselben Unternehmenseinheit wie sie sind.
+ Das Team „USMF-Vertrieb“ wird mit der zuvor erwähnten USMF-Geschäftseinheit verknüpft.
+ Daher können Mitglieder des Teams „USMF-Vertrieb“ ein beliebiges Konto sehen, das im Besitz des Benutzers „USMF DW“ ist, der aus der Tabelle des USMF-Unternehmens in Finance and Operations stammt.

![Wie Teams verwendet werden können](media/dual-write-company-2.png)

Wie in der vorherigen Abbildung dargestellt, ist diese 1:1-Zuordnung zwischen Geschäftseinheit, Unternehmen und Team nur ein Anfangspunkt. In diesem Beispiel wird eine neue Geschäftseinheit „Europa“ manuell in Dataverse als übergeordnetes Element für DEMF und ESMF erstellt. Diese neue Stammgeschäftseinheit ist nicht mit dem dualen Schreiben verknüpft. Sie kann allerdings verwendet werden, um Mitgliedern des Teams „EUR-Vertrieb“ Zugriff auf Kontodaten sowohl in DEMF als auch in ESMF zu gewähren, indem die Datensichtbarkeit in der zugehörigen Sicherheitsrolle auf **Übergeordnete/untergeordnete Geschäftseinheit** festgelegt wird.

Ein abschließendes Thema ist, wie durch das duale Schreiben bestimmt wird, welchem Eigentümerteam Zeilen zugewiesen werden sollen. Dieses Verhalten wird von der Spalte **Standardeigentümerteam** in der Zeile cdm\_Company gesteuert. Wenn eine cdm\_Company-Zeile für duales Schreiben aktiviert ist, erstellt ein Plug-In automatisch die zugewiesene Unternehmenseinheit sowie das Eigentümerteam (wenn nicht bereits vorhanden) und legt die Spalte **Standardeigentümerteam** fest. Der Administrator kann die Spalte in einen anderen Wert ändern. Allerdings kann der Administrator die Spalte nicht deaktivieren, sofern die Tabelle für duales Schreiben aktiviert ist.

> [!div class="mx-imgBorder"]
![Spalte „Standardeigentümerteam“](media/dual-write-default-owning-team.jpg)

## <a name="company-striping-and-bootstrapping"></a>Unternehmensstriping und Bootstrapping

Die Dataverse-Integration bringt Unternehmensparität durch Verwendung eines Unternehmensbezeichners zum Kennzeichen von Daten. Wie in der folgenden Abbildung dargestellt, werden alle unternehmensspezifischen Tabellen so erweitert, dass sie eine Viele-zu-Eins-Beziehung (N:1) mit der cdm\_Company-Tabelle haben.

> [!div class="mx-imgBorder"]
![N:1-Beziehung zwischen einer unternehmensspezifischen Tabelle und der cdm_Company-Tabelle](media/dual-write-bootstrapping.png)

+ Für Zeilen wird der Wert schreibgeschützt, nachdem ein Unternehmen hinzugefügt und gespeichert wird. Daher sollten Benutzer sicherstellen, dass Sie das korrekte Unternehmen auswählen.
+ Nur Zeilen mit Unternehmensdaten kommen für duales Schreiben zwischen der Anwendung und Dataverse infrage.
+ Für vorhandene Dataverse-Daten wird in Kürze eine vom Administrator geführte Bootstrapping-Erfahrung verfügbar sein.


## <a name="autopopulate-company-name-in-customer-engagement-apps"></a>Unternehmensname in Kundenbindungs-Apps automatisch ausfüllen

Es gibt verschiedene Möglichkeiten, den Unternehmensnamen in Kundenbindungs-Apps automatisch auszufüllen.

+ Wenn Sie ein Systemadministrator sind, können Sie das Standardunternehmen festlegen, indem Sie zu **Erweiterte Einstellungen > System > Sicherheit > Benutzer** navigieren. Öffnen Sie das Formular **Benutzer**, und im Abschnitt **Organisationsinformationen** legen Sie den Wert **Unternehmen gemäß Standard auf Formularen** fest.

    :::image type="content" source="media/autopopulate-company-name-1.png" alt-text="Legen Sie im Abschnitt Organisationsinformationen das Standardunternehmen fest.":::

+ Wenn Sie **Schreib**-Zugriff auf die Tabelle **SystemUser** für die Ebene **Unternehmenseinheit** haben, können Sie das Standardunternehmen auf jedem beliebigen Formular ändern, indem Sie ein Unternehmen aus dem Dropdownmenü **Unternehmen** auswählen.

    :::image type="content" source="media/autopopulate-company-name-2.png" alt-text="Ändern des Unternehmensnamens bei einem neuen Konto.":::

+ Wenn Sie **Schreibzugriff** auf Daten in mehr als einem Unternehmen haben, können Sie das Standardunternehmen ändern, indem Sie eine Zeile auswählen, die zu einem anderen Unternehmen gehört.

    :::image type="content" source="media/autopopulate-company-name-3.png" alt-text="Durch Auswahl einer Zeile wird das Standardunternehmen geändert.":::

+ Wenn Sie ein Systemkonfigurator oder -Administrator sind und Unternehmensdaten automatisch in ein benutzerdefiniertes Formular einfügen möchten, können Sie [Formularereignisse](https://docs.microsoft.com/powerapps/developer/model-driven-apps/clientapi/events-forms-grids) verwenden. Fügen Sie einen JavaScript-Verweis auf **msdyn_/DefaultCompany.js** hinzu, und verwenden Sie die folgenden Ereignisse. Sie können jedes sofort einsatzbereite Formular verwenden, z. B. das **Konto**-Formular.

    + **OnLoad**-Ereignis für das Formular: Legen Sie die Spalte **defaultCompany** fest.
    + **OnChange**-Ereignis für die Spalte **Unternehmen**: Legen Sie die Spalte **updateDefaultCompany** fest.

## <a name="apply-filtering-based-on-the-company-context"></a>Wenden Sie die Filterung basierend auf dem Unternehmenskontext an

Um die Filterung in Ihren benutzerdefinierten Formularen oder in benutzerdefinierten Suchspalten, die den Standardformularen hinzugefügt wurden, basierend auf dem Unternehmenskontext anzuwenden, öffnen Sie das Formular, und verwenden Sie den Abschnitt **Filterung zugehöriger Datensätze**, um den Unternehmensfilter anzuwenden. Sie müssen dies für jede Suchspalte festlegen, die die Filterung basierend auf dem zugrunde liegenden Unternehmen für eine bestimmte Zeile erfordert. Die Einstellung wird für **Konto** in der folgenden Abbildung angezeigt.

:::image type="content" source="media/apply-company-context.png" alt-text="Unternehmenskontext anwenden":::



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]