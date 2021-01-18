---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultManagedHsm.md
ms.openlocfilehash: 7d3cd39a18f7cbbd9663d656921375daa490b32e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524109"
---
# New-AzKeyVaultManagedHsm

## Sammanfattning
Skapar en hanterad HSM.

## FRÅGESYNTAXEN

```
New-AzKeyVaultManagedHsm [-Name] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Administrator] <String[]> [-Sku <String>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzKeyVaultManagedHsm** skapar en hanterad HSM i den angivna resurs gruppen. Om du vill lägga till, ta bort eller lista nycklar i den hanterade HSM ska användaren bevilja behörigheter genom att lägga till användar-ID i administratören.

## BESKRIVS

### Exempel 1: skapa en StandardB1 hanterad HSM
```powershell
PS C:\> New-AzKeyVaultManagedHsm -Name 'myhsm' -ResourceGroupName 'myrg1' -Location 'eastus2euap' -Administrator "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

Det här kommandot skapar en hanterad HSM med namnet myhsm i eastus2euap. Kommandot lägger till hanterad HSM i resurs gruppen med namnet myrg1. Eftersom kommandot inte anger ett värde för parametern *SKU* skapas en Standard_B1 hanterad HSM.

### Exempel 2: skapa en CustomB32 hanterad HSM
```powershell
PS C:\>New-AzKeyVaultManagedHsm -Name 'myhsm' -ResourceGroupName 'myrg1' -Location 'eastus2euap' -Administrator "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" -Sku 'CustomB32'
Name  Resource Group Name Location    SKU

----  ------------------- --------    ---
myhsm myrg1               eastus2euap CustomB32
```

                      

Det här kommandot skapar en hanterad HSM, precis som i föregående exempel. Men det anger ett värde för CustomB32 för parametern *SKU* för att skapa en CustomB32-hanterad HSM.

## MALLPARAMETRAR

### -Administratör
Ursprungligt administratörs objekt-ID för den här hanterade HSM-poolen.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AsJob
Kör cmdlet i bakgrunden

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

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

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
Anger det Azure-område där du vill skapa huvud valvet.
Använd kommandot Get-AzResourceProvider med parametern ProviderNamespace för att se dina val.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namn
Anger namnet på den hanterade HSM som ska skapas.
Namnet kan vara en kombination av bokstäver, siffror och bindestreck.
Namnet måste börja och sluta med en bokstav eller en siffra.
Namnet måste vara globalt unikt.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HsmName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på en befintlig resurs grupp där nyckelords valvet ska skapas.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SKU
Anger SKU för den hanterade HSM-instansen.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tagg
En hash-tabell som representerar resurs koder.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Visar vad som händer om cmdleten körs.
Cmdleten körs inte.

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
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## KOSTNADS

### System. String

### System. string []

### System. Collections. hash

## VÄRDEN

### Microsoft. Azure. commands. valv. Models. PSManagedHsm

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzKeyVaultManagedHsm](./Get-AzKeyVaultManagedHsm.md)

[Remove-AzKeyVaultManagedHsm](./Remove-AzKeyVaultManagedHsm.md)

[Update-AzKeyVaultManagedHsm](./Update-AzKeyVaultManagedHsm.md)