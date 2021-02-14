---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/get-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitor.md
ms.openlocfilehash: 1ec82e745c7f6521a62db80ca109078bb1681172
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100237721"
---
# Get-AzSapMonitor

## SYNOPSIS
Hämtar egenskaper för en SAP-bildskärm för angiven prenumeration, resursgrupp och resursnamn.

## SYNTAX

### Lista (standard)
```
Get-AzSapMonitor [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### Skaffa
```
Get-AzSapMonitor -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzSapMonitor -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## BESKRIVNING
Hämtar egenskaper för en SAP-bildskärm för angiven prenumeration, resursgrupp och resursnamn.

## EXEMPEL

### Exempel 1: Få alla SAP-bildskärmar under en prenumeration
```powershell
PS C:\> Get-AzSapMonitor

Location Name              Type
-------- ----              ----
westus2  ps-sapmonitor-t01 Microsoft.HanaOnAzure/sapMonitors
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

Det här kommandot får SAP-bildskärmar under en prenumeration.

### Exempel 2: Hämta en SAP-bildskärm efter namn
```powershell
PS C:\> Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

Det här kommandot får namnet på en SAP-bildskärm.

### Exempel 3: Hämta en SAP-bildskärm efter objekt
```powershell
PS C:\> $sap = Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01
PS C:\> Get-AzSapMonitor -InputObject $sap

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

Det här kommandot hämtar en SAP-bildskärm per objekt.

### Exempel 4: Hämta en SAP-bildskärm efter rörledning
```powershell
PS C:\> @{Id='/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/nancyc-hn1/providers/Microsoft.HanaOnAzure/sapMonitors/ps-spamonitor-t01'} | Get-AzSapMonitor

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

Med det här kommandot får du en SAP-bildskärm per pipeline.

## PARAMETERS

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
Type: Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Namnet på SAP-bildskärmen.

```yaml
Type: System.String
Parameter Sets: Get
Aliases: SapMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Namn på resursgruppen.

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Prenumerations-ID som unikt identifierar Microsoft Azure-prenumerationen.
Prenumerations-ID:t utgör en del av URI:n för varje servicesamtal.

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity

## UTDATA

### Microsoft.Azure.PowerShell.cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor

## ANTECKNINGAR

ALIAS

KOMPLEXA PARAMETEREGENSKAPER

Skapa de parametrar som beskrivs nedan genom att skapa en hash-tabell som innehåller rätt egenskaper. Om du vill ha information om hash-tabeller kör du Get-Help about_Hash_Tables.


INPUTOBJECT <IHanaOnAzureIdentity> : Identity Parameter
  - `[Id <String>]`: Resursidentitetssökväg
  - `[Location <String>]`: Platsen för det borttagna valvet.
  - `[OperationKind <AccessPolicyUpdateKind?>]`: Namnet på åtgärden
  - `[ProviderInstanceName <String>]`: Namn på leverantörsinstansen.
  - `[ResourceGroupName <String>]`: Namn på resursgruppen.
  - `[ResourceName <String>]`: Namnet på identitetsresursen.
  - `[SapMonitorName <String>]`: Namn på SAP-bildskärmen.
  - `[Scope <String>]`: Resursens resursleverantörs omfattning. Överordnad resurs som utökas med hanterade identiteter.
  - `[SubscriptionId <String>]`: Prenumerations-ID som unikt identifierar Microsoft Azure-prenumerationen. Prenumerations-ID:t utgör en del av URI:n för varje servicesamtal.
  - `[VaultName <String>]`: Namn på valvet

## RELATERADE LÄNKAR

