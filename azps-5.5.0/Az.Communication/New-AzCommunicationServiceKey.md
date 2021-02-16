---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/new-azcommunicationservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/New-AzCommunicationServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/New-AzCommunicationServiceKey.md
ms.openlocfilehash: b97b0d640b00e2aa3b75d829464f8ebe7dd4f6d0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100211863"
---
# New-AzCommunicationServiceKey

## SYNOPSIS
Generera en åtkomstnyckel för CommunicationService.
PrimaryKey och SecondaryKey kan inte återskapas samtidigt.

## SYNTAX

### RegenerateExpanded (standard)
```
New-AzCommunicationServiceKey -CommunicationServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-KeyType <KeyType>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### Återskapa
```
New-AzCommunicationServiceKey -CommunicationServiceName <String> -ResourceGroupName <String>
 -Parameter <IRegenerateKeyParameters> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### RegenerateViaIdentity
```
New-AzCommunicationServiceKey -InputObject <ICommunicationIdentity> -Parameter <IRegenerateKeyParameters>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### RegenerateViaIdentityExpanded
```
New-AzCommunicationServiceKey -InputObject <ICommunicationIdentity> [-KeyType <KeyType>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## BESKRIVNING
Generera en åtkomstnyckel för CommunicationService.
PrimaryKey och SecondaryKey kan inte återskapas samtidigt.

## EXEMPEL

### Exempel 1: Återskapar primärnyckeln med en IRegenerateKeyParameters-hashtabell
```powershell
PS > New-AzCommunicationServiceKey -CommunicationServiceName ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1 -Parameter @{KeyType="Primary"}

PrimaryConnectionString              PrimaryKey
-----------------------              ----------
endpoint=<example-primary-endpoint>  <example-primarykey>
```

Upphäver den föregående primärnyckeln, återskapar en ny och returnerar den.

### Exempel 2: Återskapar sekundärnyckeln med en KeyType
```powershell
PS C:\> New-AzCommunicationServiceKey -CommunicationServiceName ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1 -KeyType Secondary

SecondaryConnectionString               SecondaryKey
-----------------------                 ----------
endpoint=<example-secondary-endpoint>   <example-secondarykey>
```

Upphäver den föregående sekundära nyckeln, återskapar en ny och returnerar den.

## PARAMETERS

### -CommunicationServiceName
Namnet på CommunicationService-resursen.

```yaml
Type: System.String
Parameter Sets: Regenerate, RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klientorganisation och prenumeration som används för kommunikation med Azure.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Identitetsparameter att skapa finns i avsnittet ANTECKNINGAR för INPUTOBJECT-egenskaper och skapa en hash-tabell.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity
Parameter Sets: RegenerateViaIdentity, RegenerateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -KeyType
KeyType som ska återskapas.
Måste vara antingen 'primär' eller 'sekundär'(case-insensitive).

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Support.KeyType
Parameter Sets: RegenerateExpanded, RegenerateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Parameter
Parametrar beskriver begäran om att generera snabbtangenter för att skapa, se avsnittet ANTECKNINGAR för PARAMETERegenskaper och skapa en hash-tabell.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.IRegenerateKeyParameters
Parameter Sets: Regenerate, RegenerateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
Namnet på resursgruppen som innehåller resursen.
Du kan hämta det här värdet från Azure Resource Manager API eller portalen.

```yaml
Type: System.String
Parameter Sets: Regenerate, RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Får prenumerations-ID som unikt identifierar Microsoft Azure-prenumerationen.
Prenumerations-ID:t utgör en del av URI:n för varje servicesamtal.

```yaml
Type: System.String
Parameter Sets: Regenerate, RegenerateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bekräfta
Frågar dig om bekräftelse innan du kör cmdleten.

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
Visar vad som skulle hända om cmdleten körs.
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
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### Microsoft.Azure.PowerShell.cmdlets.Communication.Models.Api20200820Preview.IRegenerateKeyParameters

### Microsoft.Azure.PowerShell.cmdlets.Communication.Models.ICommunicationIdentity

## UTDATA

### Microsoft.Azure.PowerShell.cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceKeys

## ANTECKNINGAR

ALIAS

KOMPLEXA PARAMETEREGENSKAPER

Skapa de parametrar som beskrivs nedan genom att skapa en hash-tabell som innehåller rätt egenskaper. Om du vill ha information om hash-tabeller kör du Get-Help about_Hash_Tables.


INPUTOBJECT <ICommunicationIdentity> : Identity Parameter
  - `[CommunicationServiceName <String>]`: Namnet på resursen CommunicationService.
  - `[Id <String>]`: Resursidentitetssökväg
  - `[Location <String>]`: Azure-regionen
  - `[OperationId <String>]`: ID för en pågående async-åtgärd
  - `[ResourceGroupName <String>]`: Namnet på resursgruppen som innehåller resursen. Du kan hämta det här värdet från Azure Resource Manager API eller portalen.
  - `[SubscriptionId <String>]`: Får prenumerations-ID som unikt identifierar Microsoft Azure-prenumerationen. Prenumerations-ID:t utgör en del av URI:n för varje servicesamtal.

PARAMETER: <IRegenerateKeyParameters> Parametrar beskriver begäran om att återskapa snabbtangenter
  - `[KeyType <KeyType?>]`: KeyType som ska återskapas. Måste vara antingen 'primär' eller 'sekundär'(case-insensitive).

## RELATERADE LÄNKAR

