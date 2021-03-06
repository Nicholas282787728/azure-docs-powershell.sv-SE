---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 115A7612-4856-47AE-AEE4-918350CD7009
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-Azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzRoleDefinition.md
ms.openlocfilehash: 79ff5a54da704e66895e280c8a2e8a93731d2083
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923754"
---
# Set-AzRoleDefinition

## Sammanfattning
Ändrar en anpassad roll i Azure RBAC.
Ange den ändrade roll definitionen antingen som en JSON-fil eller som en PSRoleDefinition.
Använd först kommandot Get-AzRoleDefinition för att hämta den anpassade rollen du vill ändra.
Ändra sedan de egenskaper du vill ändra.
Spara sedan roll definitionen med det här kommandot.

## FRÅGESYNTAXEN

### InputFileParameterSet
```
Set-AzRoleDefinition -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### RoleDefinitionParameterSet
```
Set-AzRoleDefinition -Role <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Set-AzRoleDefinition cmdlet uppdaterar en befintlig anpassad roll i Azure Role-Based Access Control.
Ange den uppdaterade roll definitionen som indata för kommandot som en JSON-fil eller ett PSRoleDefinition-objekt.
Roll definitionen för den uppdaterade anpassade rollen måste innehålla ID och alla andra obligatoriska egenskaper för rollen även om de inte har uppdaterats: DisplayName, beskrivning, åtgärder, AssignableScopes.
NotActions, DataActions, NotDataActions är valfria.
Nedan följer ett exempel på en uppdaterad roll definition JSON för Set-AzRoleDefinition {"ID": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "namn": "uppdaterad roll", "Beskrivning": "kan övervaka alla resurser och starta och starta om virtuella datorer", "åtgärder": \[ " */Read", "Microsoft. ClassicCompute/virtualmachines/restart/Action", "Microsoft. ClassicCompute/virtualmachines/start/åtgärd" \] , "NotActions": \[ "* /Write" \] , "DataActions": \[ "Microsoft. Storage/storageAccounts/blobServices/container/BLOB/Read" \] , "NotDataActions": \[ "Microsoft. Storage/storageAccounts/blobServices/container/blobbar/Write" \] , "AssignableScopes": \[ "/Subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX" \] }

## BESKRIVS

### Uppdatera med PSRoleDefinitionObject
```
PS C:\> $roleDef = Get-AzRoleDefinition "Contoso On-Call"
          PS C:\> $roleDef.Actions.Add("Microsoft.ClassicCompute/virtualmachines/start/action")
          PS C:\> $roleDef.Description = "Can monitor all resources and start and restart virtual machines"
          PS C:\> $roleDef.AssignableScopes = @("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx", "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")

          PS C:\> Set-AzRoleDefinition -Role $roleDef
```

### Skapa med en JSON-fil
```
PS C:\> Set-AzRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## MALLPARAMETRAR

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputFile
Fil namn som innehåller en enda JSON-serverroll som ska uppdateras.
Inkludera bara egenskaperna som ska uppdateras i JSON.
Egenskapen ID är obligatorisk.

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Roll
Roll definitions objekt som ska uppdateras

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition
Parameter Sets: RoleDefinitionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Microsoft. Azure. kommandon. sources. Models. Authorization. PSRoleDefinition
Parametrar: roll (ByValue)

## VÄRDEN

### Microsoft. Azure. kommandon. sources. Models. Authorization. PSRoleDefinition

## ANMÄRKNINGAR
Nyckelord: Azure, AZ, arm, resurs, hantering, chef, resurs, grupp, Mall, distribution

## RELATERADE LÄNKAR

[Get-AzProviderOperation](./Get-AzProviderOperation.md)

[Get-AzRoleDefinition](./Get-AzRoleDefinition.md)

[New-AzRoleDefinition](./New-AzRoleDefinition.md)

[Remove-AzRoleDefinition](./Remove-AzRoleDefinition.md)

