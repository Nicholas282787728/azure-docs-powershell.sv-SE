---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8300B143-E322-419E-BC98-DBA56DD90A59
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleDefinition.md
ms.openlocfilehash: 8916b35da467fb16fd3802b726a7e105093b1c7a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271434"
---
# New-AzRoleDefinition

## Sammanfattning
Skapar en anpassad roll i Azure RBAC.
Ange antingen en definitions fil för JSON-roll eller ett PSRoleDefinition-objekt som indata.
Använd först kommandot Get-AzRoleDefinition för att skapa ett definitions objekt för bas linje.
Ändra sedan dess egenskaper efter behov.
Använd sedan det här kommandot för att skapa en anpassad roll med roll definition.

## FRÅGESYNTAXEN

### InputFileParameterSet
```
New-AzRoleDefinition [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### RoleDefinitionParameterSet
```
New-AzRoleDefinition [-Role] <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
New-AzRoleDefinition cmdlet skapar en anpassad roll i Azure Role-Based Access Control.
Ange en roll definition som indata för kommandot som en JSON-fil eller ett PSRoleDefinition-objekt.
Definitionen av en indatafil måste innehålla följande egenskaper:
1) DisplayName: namnet på den anpassade rollen
2) Beskrivning: en kort beskrivning av den roll som sammanfattar den åtkomst som rollen ger.
3) Åtgärder: den uppsättning operationer som den anpassade rollen ger åtkomst till.
Använd Get-AzProviderOperation för att få den funktion för Azure Resource provider som kan säkras med Azure RBAC.
Här är några giltiga åtgärds strängar:
 - "*/Read" beviljar åtkomst till Läs åtgärder för alla Azure Resource providers.
 - "Microsoft. Network/*/Read" beviljar åtkomst till Läs åtgärder för alla resurs typer i Microsoft. Network Resource Provider för Azure.
 - "Microsoft. Compute/virtualMachines/*" beviljar åtkomst till alla åtgärder för virtuella datorer och dess underordnade resurs typer.
4) AssignableScopes: uppsättningen med omfattningar (Azure-prenumerationer eller resurs grupper) där den anpassade rollen ska vara tillgänglig för tilldelning.
Med AssignableScopes kan du göra den anpassade rollen tillgänglig för tilldelning i endast de abonnemang eller resurs grupper som behöver den, och inte rörigt användar upplevelsen för resten av abonnemangen eller resurs grupperna.
Här är några giltiga tilldelnings bara scope:
 - "/Subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e", "/Subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": gör rollen tillgänglig för tilldelning i två prenumerationer.
 - "/Subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e": gör rollen tillgänglig för tilldelning i ett enda abonnemang.
 - "/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": gör rollen tillgänglig endast för tilldelning i nätverks resurs gruppen.
Definitionen av en indatafil kan innehålla följande egenskaper:
1) NotActions: den uppsättning operationer som måste undantas från åtgärderna för att fastställa de effektiva åtgärderna för den anpassade rollen.
Om det finns en specifik åtgärd som du inte vill ge åtkomst till i en anpassad roll är det praktiskt att använda NotActions för att utesluta den, i stället för att ange alla andra åtgärder än den specifika åtgärden i åtgärder.
2) DataActions: den uppsättning data åtgärder som den anpassade rollen ger åtkomst till.
3) NotDataActions: den uppsättning operationer som måste undantas från DataActions för att fastställa de effektiva data åtgärderna för den anpassade rollen.
Om det finns en specifik data åtgärd som du inte vill ge åtkomst till i en anpassad roll är det lämpligt att använda NotDataActions för att utesluta den, i stället för att ange alla andra åtgärder än den specifika åtgärden i åtgärder.
OBS! om en användare har tilldelats en roll som anger en åtgärd i NotActions och även har tilldelats en annan roll som beviljar åtkomst till samma åtgärd – användaren kan utföra åtgärden.
NotActions är inte en regel för neka-det är ett bekvämt sätt att skapa en uppsättning tillåtna operationer när specifika operationer måste uteslutas.
Nedan följer ett exempel på en JSON-rolltjänsten som kan tillhandahållas som indata {"namn": "uppdaterad roll", "Beskrivning": "kan övervaka alla resurser och starta och starta om virtuella datorer", "åtgärder": \[ " */Read", "Microsoft. ClassicCompute/virtualmachines/restart/Action", "Microsoft. ClassicCompute/virtualmachines/start/åtgärd" \] , "NotActions": \[ "* /Write" \] , "DataActions": \[ "Microsoft. Storage/storageAccounts/blobServices/container/BLOB/Read" \] , "NotDataActions": \[ "Microsoft. Storage/storageAccounts/blobServices/container/blobbar/Write" \] , "AssignableScopes": \[ "/Subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX" \] }

## BESKRIVS

### Exempel 1: skapa med PSRoleDefinitionObject
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

### Exempel 2: skapa med en JSON-fil
```powershell
PS C:\> New-AzRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## MALLPARAMETRAR

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

### -InputFile
Fil namn som innehåller en enda JSON-serverroll.

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

### -Roll
Roll definitions objekt.

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
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## KOSTNADS

### Ingen

## VÄRDEN

### Microsoft. Azure. kommandon. sources. Models. Authorization. PSRoleDefinition

## ANMÄRKNINGAR
Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, resurs, grupp, Mall, distribution

## RELATERADE LÄNKAR

[Get-AzProviderOperation](./Get-AzProviderOperation.md)

[Get-AzRoleDefinition](./Get-AzRoleDefinition.md)

[Set-AzRoleDefinition](./Set-AzRoleDefinition.md)

[Remove-AzRoleDefinition](./Remove-AzRoleDefinition.md)

