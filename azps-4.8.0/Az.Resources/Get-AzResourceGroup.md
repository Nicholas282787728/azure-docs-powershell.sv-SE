---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
ms.openlocfilehash: b8e74a0c349ea058d05ef044648e836fddc1f7b3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259672"
---
# Get-AzResourceGroup

## Sammanfattning
Hämtar resurs grupper.

## FRÅGESYNTAXEN

### GetByResourceGroupName (standard)
```
Get-AzResourceGroup [[-Name] <String>] [[-Location] <String>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceGroupId
```
Get-AzResourceGroup [[-Location] <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzResourceGroup** får Azure resurs grupper i det aktuella abonnemanget.
Du kan hämta alla resurs grupper eller ange en resurs grupp efter namn eller andra egenskaper.
Som standard får denna cmdlet alla resurs grupper i den aktuella prenumerationen.
Mer information om Azure-resurser och Azure resurs grupper finns i New-AzResourceGroup cmdlet.

## BESKRIVS

### Exempel 1: skaffa en resurs grupp efter namn
```
PS C:\> Get-AzResourceGroup -Name "EngineerBlog"
```

Det här kommandot får Azure-adressresursen i din prenumeration med namnet EngineerBlog.

### Exempel 2: Hämta alla flaggor för en resurs grupp
```
PS C:\> (Get-AzResourceGroup -Name "ContosoRG").Tags
```

Det här kommandot får resurs gruppen namnet ContosoRG och visar de taggar som är kopplade till gruppen.

### Exempel 3: Hämta resurs grupper baserat på tagg
```
PS C:\> Get-AzResourceGroup -Tag @{'environment'='prod'}
```

### Exempel 4: Visa resurs grupper efter plats
```
PS C:\> Get-AzResourceGroup |
  Sort Location,ResourceGroupName |
  Format-Table -GroupBy Location ResourceGroupName,ProvisioningState,Tags
```

### Exempel 5: Visa namnen på alla resurs grupper på en viss plats
```
PS C:\> Get-AzResourceGroup -Location westus2 |
   Sort ResourceGroupName | 
   Format-Wide ResourceGroupName -Column 4
```

### Exempel 6: Visa resurs grupper vars namn börjar med webb servern
```
PS C:\> Get-AzResourceGroup -Name WebServer*
```

## MALLPARAMETRAR

### -ApiVersion
Anger den API-version som stöds av resurs leverantören.
Du kan ange en annan version än standard versionen.

```yaml
Type: System.String
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

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
Type: System.String
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
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namn
Anger namnet på den resurs grupp som ska visas. Den här parametern har stöd för jokertecken i början och/eller slutet av strängen.

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupName
Aliases: ResourceGroupName

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### -För
Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tagg
Den HTML-kod som resurs grupper ska filtreras efter.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: GetByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## KOSTNADS

### System. String

### System. Collections. hash

## VÄRDEN

### Microsoft. Azure. kommandon. ResourceManager. cmdlets. SdkModels. PSResourceGroup

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[New-AzResourceGroup](./New-AzResourceGroup.md)

[Remove-AzResourceGroup](./Remove-AzResourceGroup.md)

[Set-AzResourceGroup](./Set-AzResourceGroup.md)


