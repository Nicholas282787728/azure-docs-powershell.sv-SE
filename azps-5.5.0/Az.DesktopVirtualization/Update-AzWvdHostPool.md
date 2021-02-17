---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdHostPool.md
ms.openlocfilehash: e6b77d9d779931d9b50de2b504b357ecd22a2b92
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100234558"
---
# Update-AzWvdHostPool

## SYNOPSIS
Uppdatera en värdpool.

## SYNTAX

### UpdateExpanded (standard)
```
Update-AzWvdHostPool -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-CustomRdpProperty <String>] [-Description <String>] [-FriendlyName <String>]
 [-LoadBalancerType <LoadBalancerType>] [-MaxSessionLimit <Int32>]
 [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>]
 [-PreferredAppGroupType <PreferredAppGroupType>] [-RegistrationInfoExpirationTime <DateTime>]
 [-RegistrationInfoRegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>]
 [-SsoadfsAuthority <String>] [-SsoClientId <String>] [-SsoClientSecretKeyVaultPath <String>]
 [-SsoContext <String>] [-SsoSecretType <SsoSecretType>] [-StartVMOnConnect] [-Tag <Hashtable>]
 [-ValidationEnvironment] [-VMTemplate <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### UpdateViaIdentityExpanded
```
Update-AzWvdHostPool -InputObject <IDesktopVirtualizationIdentity> [-CustomRdpProperty <String>]
 [-Description <String>] [-FriendlyName <String>] [-LoadBalancerType <LoadBalancerType>]
 [-MaxSessionLimit <Int32>] [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>]
 [-PreferredAppGroupType <PreferredAppGroupType>] [-RegistrationInfoExpirationTime <DateTime>]
 [-RegistrationInfoRegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>]
 [-SsoadfsAuthority <String>] [-SsoClientId <String>] [-SsoClientSecretKeyVaultPath <String>]
 [-SsoContext <String>] [-SsoSecretType <SsoSecretType>] [-StartVMOnConnect] [-Tag <Hashtable>]
 [-ValidationEnvironment] [-VMTemplate <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## BESKRIVNING
Uppdatera en värdpool.

## EXEMPEL

### Exempel 1: Uppdatera en Windows Virtual Desktop HostPool med namn
```powershell
PS C:\> Update-AzWvdHostPool -ResourceGroupName ResourceGroupName `
                            -Name HostPoolName `
                            -LoadBalancerType 'BreadthFirst' `
                            -Description 'Description' `
                            -FriendlyName 'Friendly Name' `
                            -MaxSessionLimit 6 `
                            -SsoContext $null `
                            -CustomRdpProperty $null `
                            -Ring $null `
                            -ValidationEnvironment:$false

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

Det här kommandot uppdaterar en Windows Virtual Desktop HostPool i en resursgrupp.

## PARAMETERS

### -CustomRdpProperty
Egenskapen Custom rdp för HostPool.

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

### -Beskrivning
Beskrivning av HostPool.

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

### -FriendlyName
Eget namn på HostPool.

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

### -InputObject
Identitetsparameter att skapa finns i avsnittet ANTECKNINGAR för INPUTOBJECT-egenskaper och skapa en hash-tabell.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -LoadBalancerType
Typen av belastningsutjämning.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.LoadBalancerType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxSessionLimit
Maximal sessionsgräns för HostPool.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Namnet på värdpoolen i den angivna resursgruppen

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: HostPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PersonalDesktopAssignmentType
PersonalDesktopAssignment-typ för HostPool.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.PersonalDesktopAssignmentType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PreferredAppGroupType
Typ av önskad programgruppstyp, som standard skrivbordsappprogramgrupp

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.PreferredAppGroupType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RegistrationInfoExpirationTime
Registreringstokens förfallodatum.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RegistrationInfoRegistrationTokenOperation
Typ av återställning av token.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.RegistrationTokenOperation
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Namnet på resursgruppen.
Namnet är okänsligt.

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ring
Ringnumret för HostPool.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SsoadfsAuthority
URL till kundens ADFS-server för signering av WVD SSO-certifikat.

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

### -SsoClientId
ClientId för den registrerade förlitar parten som används för att utfärda WVD SSO-certifikat.

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

### -SsoClientSecretKeyVaultPath
Sökväg till Azure KeyVault som lagrar hemligheten som används för kommunikation med ADFS.

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

### -SsoContext
Sökväg till tangentvault som innehåller ssoContext-hemligt.

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

### -SsoSecretType
Typen av enskilt tecken i hemlig typ.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.SsoSecretType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartVMOnConnect
Flaggan för att aktivera/inaktivera StartVMOnConnect-funktionen.

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

### -SubscriptionId
ID för målprenumerationen.

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
taggar som ska uppdateras

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ValidationEnvironment
Är verifieringsmiljö.

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

### -VMTemplate
VM-mall för konfiguration av sessionsvärdar i värdpool.

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

### Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity

## UTDATA

### Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IHostPool

## ANTECKNINGAR

ALIAS

KOMPLEXA PARAMETEREGENSKAPER

Skapa de parametrar som beskrivs nedan genom att skapa en hash-tabell som innehåller rätt egenskaper. Om du vill ha information om hash-tabeller kör du Get-Help about_Hash_Tables.


INPUTOBJECT <IDesktopVirtualizationIdentity> : Identity Parameter
  - `[ApplicationGroupName <String>]`: Namnet på programgruppen
  - `[ApplicationName <String>]`: Namnet på programmet i den angivna programgruppen
  - `[DesktopName <String>]`: Namnet på skrivbordet i den angivna skrivbordsgruppen
  - `[HostPoolName <String>]`: Namnet på värdpoolen i den angivna resursgruppen
  - `[Id <String>]`: Resursidentitetssökväg
  - `[MsixPackageFullName <String>]`: Det versionsspecifika paketets fullständiga namn för MSIX-paketet inom angiven värdpool
  - `[ResourceGroupName <String>]`: Namnet på resursgruppen. Namnet är okänsligt.
  - `[SessionHostName <String>]`: Namnet på sessionsvärden i den angivna värdpoolen
  - `[SubscriptionId <String>]`: ID för målprenumerationen.
  - `[UserSessionId <String>]`: Namnet på användarsessionen inom den angivna sessionsvärden
  - `[WorkspaceName <String>]`: Namnet på arbetsytan

## RELATERADE LÄNKAR

