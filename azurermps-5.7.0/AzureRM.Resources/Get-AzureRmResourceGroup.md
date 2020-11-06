---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroup.md
ms.openlocfilehash: f3924115d68d7e844503e076a214c95bf3d2239d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583067"
---
# Get-AzureRmResourceGroup

## Sammanfattning
Hämtar resurs grupper.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### GetByResourceGroupName (standard)
```
Get-AzureRmResourceGroup [-Name <String>] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceGroupId
```
Get-AzureRmResourceGroup [-Location <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureRmResourceGroup** får Azure resurs grupper i det aktuella abonnemanget.
Du kan hämta alla resurs grupper eller ange en resurs grupp efter namn eller andra egenskaper.
Som standard får denna cmdlet alla resurs grupper i den aktuella prenumerationen.

Mer information om Azure-resurser och Azure resurs grupper finns i New-AzureRmResourceGroup cmdlet.

## BESKRIVS

### Exempel 1: skaffa en resurs grupp efter namn
```
PS C:\>Get-AzureRmResourceGroup -Name "EngineerBlog"
```

Det här kommandot får Azure-adressresursen i din prenumeration med namnet EngineerBlog.

### Exempel 2: Hämta alla flaggor för en resurs grupp
```
PS C:\>(Get-AzureRmResourceGroup -Name "ContosoRG").Tags
```

Det här kommandot får resurs gruppen namnet ContosoRG och visar de taggar som är kopplade till gruppen.

### Exempel 3: Visa resurs grupper efter plats
```
PS C:\> Get-AzureRmResourceGroup |
  Sort Location,ResourceGroupName |
  Format-Table -GroupBy Location ResourceGroupName,ProvisioningState,Tags
```

### Exempel 4: Visa namnen på alla resurs grupper på en viss plats
```
PS C:\> Get-AzureRmResourceGroup -Location westus2 |
   Sort ResourceGroupName | 
   Format-Wide ResourceGroupName -Column 4
```

### Exempel 5: Visa resurs grupper vars namn börjar med webserver
```
PS C:\> Get-AzureRmResourceGroup | Where ResourceGroupName -like WebServer*
```

## MALLPARAMETRAR

### -ApiVersion
Anger den API-version som stöds av resurs leverantören.
Du kan ange en annan version än standard versionen.

```yaml
Type: String
Parameter Sets: (All)
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

### -ID
Anger ID för den resurs grupp som ska visas.
Jokertecken är inte tillåtna.

```yaml
Type: String
Parameter Sets: GetByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Plats
Anger platsen för den resurs grupp som ska visas.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namn
Anger namnet på den resurs grupp som ska visas.
Jokertecken är inte tillåtna.

```yaml
Type: String
Parameter Sets: GetByResourceGroupName
Aliases: ResourceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -För
Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.

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

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Strängvärdet
Du kan ange indata för cmdleten med egenskaps namnet men inte efter värde.

## VÄRDEN

### Microsoft. Azure. commands. ResourceManagement. PSResourceGroup
Denna cmdlet returnerar resurs grupper.

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[New-AzureRmResourceGroup](./New-AzureRmResourceGroup.md)

[Remove-AzureRmResourceGroup](./Remove-AzureRmResourceGroup.md)

[Set-AzureRmResourceGroup](./Set-AzureRmResourceGroup.md)


