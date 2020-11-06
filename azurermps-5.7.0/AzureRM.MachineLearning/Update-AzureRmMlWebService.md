---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/update-azurermmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Update-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Update-AzureRmMlWebService.md
ms.openlocfilehash: 5fb8c8f71366dd9fd0a2c6b12fc023c1ce3ccf9b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583139"
---
# Update-AzureRmMlWebService

## Sammanfattning
Uppdaterar egenskaper för en befintlig webb tjänst resurs.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### UpdateFromParameters
```
Update-AzureRmMlWebService -ResourceGroupName <String> -Name <String> [-Title <String>] [-Description <String>]
 [-IsReadOnly] [-Keys <WebServiceKeys>] [-StorageAccountKey <String>] [-Diagnostics <DiagnosticsConfiguration>]
 [-RealtimeConfiguration <RealtimeConfiguration>] [-Assets <Hashtable>]
 [-Input <ServiceInputOutputSpecification>] [-Output <ServiceInputOutputSpecification>]
 [-Parameters <Hashtable>] [-Package <GraphPackage>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### UpdateFromObject
```
Update-AzureRmMlWebService -ResourceGroupName <String> -Name <String> -ServiceUpdates <WebService> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Med Update-AzureRmMlWebService cmdlet kan du uppdatera icke-statiska egenskaper för en webb tjänst.
Cmdleten fungerar som en korrigerings åtgärd.
Skicka bara de egenskaper som du vill ändra.

## BESKRIVS

### --------------------------Exempel 1: argument för selektiv uppdatering--------------------------
```
Update-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Description "new update to description" -Keys @{Primary='changed primary key'} -Diagnostics @{Level='All'}
```

Här ändrar vi beskrivningen, den primära åtkomst tangenten och aktiverar diagnostikprogrammet för alla spårningar under körningen för webb tjänsten.

### --------------------------Exempel 2: uppdatering baserad på en webb tjänst instans--------------------------
```
$updates = @{ Properties = @{ Title="New Title"; RealtimeConfiguration = @{ MaxConcurrentCalls=25 }}}

Update-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -ServiceUpdates $updates
```

I exemplet skapas först en webb tjänst definition som bara innehåller de fält som ska uppdateras och sedan anropar Update-AzureRmMlWebService för att tillämpa dem med hjälp av parametern ServiceUpdates.

## MALLPARAMETRAR

### -Till gångar
Den uppsättning till till gångar (till exempel moduler, data mängder) som utgör webb tjänsten.

```yaml
Type: Hashtable
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Beskrivning
Det nya värdet för webb tjänstens beskrivning.
Detta visas i tjänstens Swagger API-schema.

```yaml
Type: String
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Diagnostik
Inställningar som styr insamling av diagnos spår för webb tjänsten.

```yaml
Type: DiagnosticsConfiguration
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Fråga inte efter bekräftelse.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Inmatning
Definitionen för webb tjänstens indata, som Swagger schema konstruktion.

```yaml
Type: ServiceInputOutputSpecification
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsReadOnly
Anger att den här webb tjänsten är skrivskyddad.
När du har angett kan webb tjänsten längre uppdateras, inklusive ändring av värdet för den här egenskapen och kan bara tas bort.

```yaml
Type: SwitchParameter
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tangenter
Uppdaterar en eller båda åtkomst nycklar som används för att autentisera samtal i tjänstens runtime API: er.

```yaml
Type: WebServiceKeys
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namn
Namnet på webb tjänst resursen som ska uppdateras.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Utdata
Definitionen för webb tjänstens resultat, som Swagger schema konstruktion.

```yaml
Type: ServiceInputOutputSpecification
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Paketera
Definitionen av grafsystemet som definierar den här webb tjänsten.

```yaml
Type: GraphPackage
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Parametrar
Uppsättningen globala parameter värden som har definierats för webb tjänsten, med namn som standard för globala parametrar \> .
Om inget standardvärde anges anses parametern vara obligatorisk.

```yaml
Type: Hashtable
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RealtimeConfiguration
Uppdateringar för konfiguration av tjänstens slut punkt för tjänste tid.

```yaml
Type: RealtimeConfiguration
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Resurs gruppen som innehåller webb tjänsten som ska uppdateras.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceUpdates
En uppsättning uppdateringar som ska tillämpas på webb tjänsten som tillhandahålls som webb tjänst definitions instans.
Endast icke-statiska fält ändras.

```yaml
Type: WebService
Parameter Sets: UpdateFromObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -StorageAccountKey
Roterar snabb tangenten för det lagrings konto som är associerat med webb tjänsten.

```yaml
Type: String
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Rubrik
Det nya värdet för webb tjänstens titel.
Detta visas i tjänstens Swagger API-schema.

```yaml
Type: String
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bekräfta
Du uppmanas att bekräfta innan du kör cmdleten.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Visar vad som händer om cmdleten körs.
Cmdleten körs inte.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Webb tjänst
Parametern ' ServiceUpdates ' godkänner värdet för typen "WebService" från pipeline

## VÄRDEN

### Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService
En sammanfattning av Azure Machine Learning web service.
Liknar beskrivningen som returneras när du anropar Get-AzureRmMlWebService cmdlet på en befintlig webb tjänst.
Den här beskrivningen innehåller inte känsliga egenskaper som lagrings kontots autentiseringsuppgifter och tjänstens åtkomst nycklar.

## ANMÄRKNINGAR
Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, maskin, maskin inlärning, azureml

## RELATERADE LÄNKAR

