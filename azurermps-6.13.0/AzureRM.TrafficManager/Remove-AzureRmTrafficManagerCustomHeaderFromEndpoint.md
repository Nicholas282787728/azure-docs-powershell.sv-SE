---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D342
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/remove-azurermtrafficmanagercustomheaderfromendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint.md
ms.openlocfilehash: 452e252b7bf9368ea89e81f2d37fd5a80ab079b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573841"
---
# Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint

## Sammanfattning
Tar bort anpassad huvud information från ett lokalt Traffic Manager-slutobjekt.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint -Name <String>
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint** tar bort anpassad huvud information från ett lokalt objekt i Azure Traffic Manager.
Du kan få en slut punkt genom att använda New-AzureRmTrafficManagerEndpoint eller Get-AzureRmTrafficManagerEndpoint cmdletar.

Denna cmdlet fungerar med det lokala slutpunktsmapparen.
Bekräfta dina ändringar av slut punkten för Traffic Manager genom att använda Set-AzureRmTrafficManagerEndpoint cmdlet.

## BESKRIVS

### Exempel 1: ta bort anpassad under näts information från en slut punkt
```
PS C:\> $TrafficManagerEndpoint = Get-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
PS C:\> Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host"
PS C:\> Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

Det första kommandot får Azure-slutpunkten contoso från den profil som heter ContosoProfile i resurs gruppen med namnet ResourceGroup11 och lagrar sedan objektet i $TrafficManagerEndpoint variabel.
Det andra kommandot tar bort den anpassade huvud rubrik informationen från slut punkten som lagras i $TrafficManagerEndpoint.
Kommandot uppdaterar slut punkten i Traffic Manager för att matcha det lokala värdet i $TrafficManagerEndpoint.

## MALLPARAMETRAR

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namn
Anger namnet på den anpassade huvud informationen som ska tas bort.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficManagerEndpoint
Anger ett lokalt **TrafficManagerEndpoint** -objekt.
Denna cmdlet ändrar detta lokala objekt.
Du kan hämta ett **TrafficManagerEndpoint** -objekt med hjälp av Get-AzureRmTrafficManagerEndpoint eller New-AzureRmTrafficManagerEndpoint cmdlet.

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Bekräfta
Du uppmanas att bekräfta innan du kör cmdleten.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Visar vad som händer om cmdleten körs. Cmdleten körs inte.

```yaml
Type: System.Management.Automation.SwitchParameter
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

### Microsoft. Azure. commands. Network. TrafficManagerEndpoint
Denna cmdlet accepterar ett **TrafficManagerEndpoint** -objekt till denna cmdlet.

## VÄRDEN

### Microsoft. Azure. commands. Network. TrafficManagerEndpoint
Denna cmdlet returnerar ett ändrat TrafficManagerEndpoint-objekt.

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Add-AzureRmTrafficManagerCustomHeaderToEndpoint](./Add-AzureRmTrafficManagerCustomHeaderToEndpoint.md)

[Get-AzureRmTrafficManagerProfile](./Get-AzureRmTrafficManagerEndpoint.md)

[New-AzureRmTrafficManagerEndpoint](./New-AzureRmTrafficManagerEndpoint.md)

[Set-AzureRmTrafficManagerEndpoint](./Set-AzureRmTrafficManagerEndpoint.md)
