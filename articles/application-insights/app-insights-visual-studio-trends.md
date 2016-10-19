<properties 
    pageTitle="Analyse van Trends in Visual Studio | Microsoft Azure" 
    description="Trends analyseren, visualiseren en verkennen in uw Application Insights Telemetry in Visual Studio." 
    services="application-insights" 
    documentationCenter=".net"
    authors="numberbycolors" 
    manager="douge"/>

<tags 
    ms.service="application-insights" 
    ms.workload="tbd" 
    ms.tgt_pltfrm="ibiza" 
    ms.devlang="na" 
    ms.topic="get-started-article" 
    ms.date="08/08/2016" 
    ms.author="daviste"/>
    

# Trends analyseren in Visual Studio

Het hulpprogramma Application Insights Trends visualiseert hoe belangrijke telemetriegebeurtenissen van uw toepassing wijzigen gedurende een periode, zodat u snel problemen en afwijkingen kunt identificeren. Door een koppeling naar meer gedetailleerde diagnostische gegevens, kan Trends u helpen bij het verbeteren de prestaties van uw app, de oorzaken van uitzonderingen traceren en inzicht verwerven over uw aangepaste gebeurtenissen.

![Voorbeeld Trends-venster](./media/app-insights-visual-studio-trends/app-insights-trends-hero-750.png)

> [AZURE.NOTE] Application Insights Trends is beschikbaar in Visual Studio 2015 Update 3 en hoger of met de [Developer Analytics Tools-extensie ](https://visualstudiogallery.msdn.microsoft.com/82367b81-3f97-4de1-bbf1-eaf52ddc635a) versie 5.209 en later.

## Open Application Insights Trends

Het venster Application Insights Trends openen:

* Kies in de Application Insights-werkbalkknop **Explore Telemetry Trends** of
* Kies in het contextmenu project **Application Insights > Explore Telemetry Trends**, of
* Kies in de menubalk Visual Studio **Beeld > Andere vensters > Application Insights Trends**.

U wordt nu mogelijk gevraagd om een resource te selecterne. Klik op **Een resource selecteren**, meld u aan met een Azure-abonnement en kies vervolgens een Application Insights-bron in de lijst waarvoor u telemetrietrends wilt analyseren.

## Kies een trendanalyse

![Menu van algemene typen trendanalyse](./media/app-insights-visual-studio-trends/app-insights-trends-1-750.png)

Ga aan de slag door één van de vijf algemene trendanalyses te selecteren, waarbij telkens gegevens van de afgelopen 24 uur worden geanalyseerd:

* **Prestatieproblemen met uw serveraanvragen analyseren** - Ranvragen worden gedaan met uw service, gegroepeerd op reactietijden
* **Problemen in uw serveraanvragen analyseren** - Ranvragen worden gedaan met uw service, gegroepeerd op HTTP-reactietijden
* **De uitzonderingen in uw toepassing onderzoeken** -Uitzonderingen van uw service, gegroepeerd op uitzonderingstype
* **De prestaties van de afhankelijkheden van uw toepassing controleren** -Services die worden aangeroepen door uw service, gegroepeerd op reactietijden
* **Uw aangepaste gebeurtenissen controleren** - Aangepaste gebeurtenissen die u hebt ingesteld voor uw service, gegroepeerd op gebeurtenistype.

Deze vooraf gemaakte analyses zijn later vanaf de knop **Algemene types telemetrieanalyses weergeven** knop in de linkerbovenhoek van het venster Trends beschikbaar.

## Trends in uw toepassing visualiseren

Application Insights Trends maakt een tijdreeksvisualisatie vanaf de telemetrie van uw app. Elke keer reeksvisualisatie geeft een soort telemetrie, gegroepeerd op een eigenschap van die telemetrie over een bepaalde tijdspanne. U wilt bijvoorbeeld serveraanvragen bekijken gegroepeerd op het land waarvan ze afkomstig zijn, gedurende de afgelopen 24 uur. In dit voorbeeld zou elke bel in de weergave een telling van het aantal serveraanvragen voor een bepaald land / regio gedurende één uur voorstellen.

Gebruik de besturingselementen aan de bovenkant van het venster om aan te passen welke typen telemetrie worden weergeven. Kies eerst de telemetrietypes waarin u bent geïnteresseerd:

* **Telemetrytype** - Serveraanvragen, uitzonderingen, afhankelijkheden of aangepaste gebeurtenissen
* **Tijdsbereik** - ongeacht uw locatie van de laatste 30 minuten in de afgelopen 3 dagen
* **Groeperen op** - uitzonderingstype, probleem-id, land/regio en meer.

Klik vervolgens op **Telemetrie analyseren** om de query uit te voeren.

U kunt als volgt tussen de bellen in de visualisatie navigeren:

* Klik om een bel te selecteren, waarmee de filters onder in het venster worden bijgewerkt en de gebeurtenissen tijdens een bepaalde periode worden samengevat
* Dubbelklik op een bel om naar de zoekfunctie te gaan en alle afzonderlijke telemetriegebeurtenissen te zien die in die periode zijn opgetreden
* Ctrl-klik om de selectie ervan in de visualisatie op te heffen.

> [AZURE.TIP] Hulpprogramma's werken samen om u te helpen de oorzaken van problemen in uw service onder duizenden telemetriegebeurtenissen vast te stellen. Als uw klanten bijvoorbeeld ‘s middags melden dat uw app minder reageert, start dan met Trends. Analyseer de aanvragen die de afgelopen uren bij uw service zijn binnengekomen, gegroepeerd op reactietijd. Kijk of er een ongebruikelijk groot cluster van trage aanvragen is. Dubbelklik vervolgens op die bel om naar de zoekfunctie te gaan, die op deze aanvraaggebeurtenissen is gefilterd. U kunt de inhoud van deze aanvragen doorzien en navigeren naar de code betrokken bij dit probleem.

## Filteren

Ontdek meer specifieke trends met de filterbesturingselementen aan de onderkant van het venster. Klik op de filternaam om het filter toe te passen. U kunt snel schakelen tussen verschillende filters voor het detecteren van trends die in een dimensie van uw telemetrie kunnen worden verborgen. Als u een filter in één dimensie toepast, zoals uitzonderingstype, blijven filters in andere dimensies aanklikbaar hoewel ze uitgegrijsd worden weergegeven. Klik opnieuw op de filters om ze te deselecteren. Ctrl-klik om meerdere filters in dezelfde dimensie selecteren.

![Trendfilters](./media/app-insights-visual-studio-trends/TrendsFiltering-750.png)

Wat gebeurt er als u meerdere filters wilt toepassen? 

1. Het eerste filter toepassen. 
2. Klik op de **Geselecteerde filters toepassen en opnieuw opvragen** met de naam van de dimensie van het eerste filter. Hiermee wordt uw telemetrie voor enkel die gebeurtenissen die overeenkomen met het eerste filter opnieuw opgevraagd. 
3. Een tweede filter toepassen. 
4. Herhaal dit proces om trends in specifieke subreeksen van uw telemetrie te zoeken. Bijvoorbeeld serveraanvragen met de naam "GET Home/Index" _en_ die afkomstig zijn van Duitsland _en_ die een 500 antwoordcode ontvangen. 

Om één van deze filters te deselecteren klikt u op de knop **Geselecteerde filters verwijderen en opnieuw een query toepassen** voor de dimensie.

![Meerdere filters](./media/app-insights-visual-studio-trends/TrendsFiltering2-750.png)

## Afwijkingen vinden

Het hulpprogramma Trends kan bellen van gebeurtenissen aangeven die afwijken van andere bellen in dezelfde tijdreeksen. Kies in de vervolgkeuzelijst Weergavetype **Aantal in tijdsinterval (afwijkingen markeren)** of **Percentages in tijdsinterval (afwijkingen markeren)**. Rode bellen zijn afwijkend. Afwijkingen worden gedefinieerd als bellen met aantallen / percentages die 2.1 maal de standaardafwijking van aantallen / percentages opgetreden in de afgelopen twee tijdsintervallen (48 uur als u de afgelopen 24 uur bekijkt).

![Gekleurde punten geven aan afwijkingen aan](./media/app-insights-visual-studio-trends/TrendsAnomalies-750.png)

> [AZURE.TIP] Markering van afwijkingen wordt met name handig voor het vinden van uitschieters in tijdreeks van kleine bellen die er anders mogelijk gelijkaardig uitzien.  

## <a name="next"></a>Volgende stappen

||
|---|---
|**[Met Application Insights werken in Visual Studio](app-insights-visual-studio.md)**<br/>Telemetrie zoeken, data in CodeLens bekijken en configureren van Application Insights. Allen vanuit Visual Studio. |![Klik met de rechtermuisknop op het project en kies Application Insights > Zoeken.](./media/app-insights-visual-studio-trends/34.png)
|**[Meer gegevens toevoegen](app-insights-asp-net-more.md)**<br/>Bewaak het gebruik, de beschikbaarheid, de afhankelijkheden en de uitzonderingen. Integreer bijgehouden informatie uit frameworks voor logboekregistratie. Schrijf aangepaste telemetrie. | ![Visual Studio](./media/app-insights-visual-studio-trends/64.png)
|**[Werken met de Application Insights-portal](app-insights-dashboards.md)**<br/>Dashboards, krachtige hulpprogramma's voor diagnose en analyse, waarschuwingen, een live afhankelijkheidskaart van uw toepassing en exportmogelijkheden voor telemetrie. |![Visual Studio](./media/app-insights-visual-studio-trends/62.png)



<!--HONumber=Sep16_HO3-->

