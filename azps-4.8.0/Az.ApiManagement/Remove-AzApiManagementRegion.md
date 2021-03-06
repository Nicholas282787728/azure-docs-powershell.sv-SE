---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
ms.openlocfilehash: 70816b054acc7667d2246ea72901c65890f9389e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258390"
---
# Remove-AzApiManagementRegion

## Sammanfattning
Tar bort ett befintligt distributions område från PsApiManagement-instansen.

## FRÅGESYNTAXEN

```
Remove-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Remove-AzApiManagementRegion** tar bort instansen av typen **Microsoft. Azure. kommandon. ApiManagement. Models. PsApiManagementRegion** från en mängd **AdditionalRegions** som tillhandahålls instansen av typen **Microsoft. Azure. commands. ApiManagement. Models. PsApiManagement**.
Denna cmdlet ändrar inte distribution fristående men uppdaterar instansen av **PsApiManagement** i minnet.
Om du vill uppdatera en distribution av en API-hantering skickar du den ändrade **PsApiManagementInstance** till **set-AzApiManagement**.

## BESKRIVS

### Exempel 1: ta bort en region från en PsApiManagement-instans
```
PS C:\>Remove-AzApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

Det här kommandot tar bort regionen öst från **PsApiManagement** -instansen.

### Exempel 2: ta bort en region från en PsApiManagement-instans med en serie kommandon
```
PS C:\>Get-AzApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzApiManagementRegion -Location "East US" | Set-AzApiManagement
```

Det här första kommandot får en instans av **PsApiManagement** från resurs gruppen med namnet contoso med namnet ContosoApi.
Kommandot sista tar sedan bort den region som heter östra USA från den instansen och uppdaterar sedan distributionen.

## MALLPARAMETRAR

### -ApiManagement
Anger den **PsApiManagement** -instans som denna cmdlet tar bort det extra distributions området från.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Plats
Anger platsen för den region som cmdleten tar bort.
Anger platsen för det nya distributions området bland de regioner som stöds för API-hanterings tjänsten.
För att få giltiga platser, Använd cmdleten Get-AzResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | där {$ _. ResourceTypes [0]. ResourceTypeName-EQ "tjänst"} | Select-Object platser

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## KOSTNADS

### Microsoft. Azure. commands. ApiManagement. Models. PsApiManagement

### System. String

## VÄRDEN

### Microsoft. Azure. commands. ApiManagement. Models. PsApiManagement

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Add-AzApiManagementRegion](./Add-AzApiManagementRegion.md)

[Update-AzApiManagementRegion](./Update-AzApiManagementRegion.md)


