---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8300B143-E322-419E-BC98-DBA56DD90A59
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleDefinition.md
ms.openlocfilehash: 8916b35da467fb16fd3802b726a7e105093b1c7a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100217726"
---
# New-AzRoleDefinition

## SYNOPSIS
Skapar en anpassad roll i Azure RBAC.
Ange antingen en JSON-rolldefinitionsfil eller ett PSRoleDefinition-objekt som indata.
Använd först kommandot Get-AzRoleDefinition för att generera ett originalrolldefinitionsobjekt.
Ändra sedan dess egenskaper efter behov.
Använd slutligen det här kommandot för att skapa en anpassad roll med rolldefinition.

## SYNTAX

### InputFileParameterSet
```
New-AzRoleDefinition [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### RoleDefinitionParameterSet
```
New-AzRoleDefinition [-Role] <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
Med New-AzRoleDefinition-cmdleten skapas en anpassad roll i Azure Role-Based Access Control.
Ange en rolldefinition som indata till kommandot som en JSON-fil eller ett PSRoleDefinition-objekt.
Indatarolldefinitionen MÅSTE innehålla följande egenskaper:
1) DisplayName: namnet på den anpassade rollen
2) Beskrivning: en kort beskrivning av rollen som sammanfattar den åtkomst som rollen beviljar.
3) Åtgärder: den uppsättning åtgärder som den anpassade rollen beviljar åtkomst till.
Använd Get-AzProviderOperation för att få åtgärden för Azure-resursleverantörer som kan skyddas med Azure RBAC.
Här följer några giltiga åtgärdssträngar:
 - "*/read" beviljar åtkomst till läsåtgärder för alla Azure-resursleverantörer.
 - "Microsoft.Network/*/read" beviljar åtkomst till läsåtgärder för alla resurstyper i Microsoft.Network-resursleverantören för Azure.
 - "Microsoft.Compute/virtualMachines/*" beviljar åtkomst till alla åtgärder som utförs av virtuella datorer och dess underordnade resurstyper.
4) AssignableScopes: uppsättningen omfattningar (Azure-prenumerationer eller resursgrupper) där den anpassade rollen är tillgänglig för tilldelning.
Med AssignableScopes kan du göra den anpassade rollen tillgänglig för tilldelning endast i de prenumerationer eller resursgrupper som behöver den, och inte göra användarupplevelsen rörig för resten av prenumerationer eller resursgrupper.
Här följer några giltiga tilldelningsbara omfattningar:
 - "/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e", "/subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": gör rollen tillgänglig för tilldelning i två prenumerationer.
 - "/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e": gör rollen tillgänglig för tilldelning i en enda prenumeration.
 - "/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": gör rollen tillgänglig för tilldelning endast i gruppen med nätverksresurser.
Indatarolldefinitionen KAN innehålla följande egenskaper:
1) NotActions: den uppsättning åtgärder som måste undantas från åtgärderna för att fastställa de effektiva åtgärderna för den anpassade rollen.
Om det finns en specifik åtgärd som du inte vill ge åtkomst till i en anpassad roll är det lämpligt att använda NotActions för att utesluta den, i stället för att ange alla åtgärder som inte är den specifika åtgärden i Åtgärder.
2) DataActions: den uppsättning dataåtgärder som den anpassade rollen beviljar åtkomst till.
3) NotDataActions: den uppsättning åtgärder som måste undantas från dataåtgärder för att fastställa de effektiva dataåtgärderna för den anpassade rollen.
Om det finns en specifik dataåtgärd som du inte vill ge åtkomst till i en anpassad roll är det lämpligt att använda NotDataActions för att utesluta den, i stället för att ange alla andra åtgärder än den specifika åtgärden i Åtgärder.
Obs! Om en användare tilldelas en roll som anger en åtgärd i NotActions och även tilldelats en annan roll, beviljar åtkomst till samma åtgärd, kan användaren utföra åtgärden.
NotActions är inte en regel för nekande – det är bara ett bekvämt sätt att skapa en uppsättning tillåtna åtgärder när särskilda åtgärder behöver uteslutas.
Följande är en exempelrolldefinition för json som kan tillhandahållas som indata { "Namn": "Uppdaterad roll", "Beskrivning": "Kan övervaka alla resurser och starta och starta om virtuella datorer", "Åtgärder": \[ "*/read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \] , "NotActions": \[ "*/write" \] , "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/containers/action" blobs/read" \] , "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \] , "AssignableScopes": \[ "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" \] }

## EXEMPEL

### Exempel 1: Skapa med PSRoleDefinitionObject
```powershell
PS C:\> $role = Get-AzRoleDefinition -Name "Virtual Machine Contributor"

PS C:\> $role.Id = $null
PS C:\> $role.Name = "Virtual Machine Operator"
PS C:\> $role.Description = "Can monitor, start, and restart virtual machines."
PS C:\> $role.Actions.RemoveRange(0,$role.Actions.Count)
PS C:\> $role.Actions.Add("Microsoft.Compute/*/read")
PS C:\> $role.Actions.Add("Microsoft.Compute/virtualMachines/start/action")
PS C:\> $role.Actions.Add("Microsoft.Compute/virtualMachines/restart/action")
PS C:\> $role.Actions.Add("Microsoft.Compute/virtualMachines/downloadRemoteDesktopConnectionFile/action")
PS C:\> $role.Actions.Add("Microsoft.Network/*/read")
PS C:\> $role.Actions.Add("Microsoft.Storage/*/read")
PS C:\> $role.Actions.Add("Microsoft.Authorization/*/read")
PS C:\> $role.Actions.Add("Microsoft.Resources/subscriptions/resourceGroups/read")
PS C:\> $role.Actions.Add("Microsoft.Resources/subscriptions/resourceGroups/resources/read")
PS C:\> $role.Actions.Add("Microsoft.Insights/alertRules/*")
PS C:\> $role.Actions.Add("Microsoft.Support/*")
PS C:\> $role.AssignableScopes.Clear()
PS C:\> $role.AssignableScopes.Add("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")

PS C:\> New-AzRoleDefinition -Role $role
```

### Exempel 2: Skapa med JSON-fil
```powershell
PS C:\> New-AzRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## PARAMETERS

### -DefaultProfile
Autentiseringsuppgifter, konto, klientorganisation och prenumeration som används för kommunikation med Azure

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

### -InputFile
Filnamn som innehåller en enda jsonrolldefinition.

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Role
Rolldefinitionsobjekt.

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition
Parameter Sets: RoleDefinitionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### Ingen

## UTDATA

### Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition

## ANTECKNINGAR
Nyckelord: azure, azurerm, arm, resurs, hantering, chef, resurs, grupp, mall, distribution

## RELATERADE LÄNKAR

[Get-AzProviderOperation](./Get-AzProviderOperation.md)

[Get-AzRoleDefinition](./Get-AzRoleDefinition.md)

[Set-AzRoleDefinition](./Set-AzRoleDefinition.md)

[Remove-AzRoleDefinition](./Remove-AzRoleDefinition.md)

