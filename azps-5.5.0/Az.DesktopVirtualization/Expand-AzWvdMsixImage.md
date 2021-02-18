---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/expand-azwvdmsiximage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Expand-AzWvdMsixImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Expand-AzWvdMsixImage.md
ms.openlocfilehash: 56122e8d1ae94b6a898c073f2b2f2fb891504789
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100220142"
---
# Expand-AzWvdMsixImage

## SYNOPSIS
Expanderar och visar MSIX-paket i en bild, givet bildsökvägen.

## SYNTAX

### ExpandExpanded (standard)
```
Expand-AzWvdMsixImage -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Uri <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### Utöka
```
Expand-AzWvdMsixImage -HostPoolName <String> -ResourceGroupName <String> -MsixImageUri <IMsixImageUri>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### ExpandViaIdentity
```
Expand-AzWvdMsixImage -InputObject <IDesktopVirtualizationIdentity> -MsixImageUri <IMsixImageUri>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### ExpandViaIdentityExpanded
```
Expand-AzWvdMsixImage -InputObject <IDesktopVirtualizationIdentity> [-Uri <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## BESKRIVNING
Expanderar och visar MSIX-paket i en bild, givet bildsökvägen.

## EXEMPEL

### Exempel 1: Expanderar angiven bildsökväg och hämtar paketmetadata från AppxManifest.xml
```powershell
PS C:\> Expand-AzWvdMsixImage -HostPoolName HostPoolName `
          -ResourceGroupName resourceGroupName `
          -SubscriptionId SubscriptionId `
          -Uri ImagePathURI

Name                          Type
----                          ----
HostPoolName/extractmsiximage Microsoft.DesktopVirtualization/hostpools/extractmsiximage
```

Det här kommandot returnerar metadata för MSIX-paket som finns i den angivna bildsökvägen.

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

### -HostPoolName
Namnet på värdpoolen i den angivna resursgruppen

```yaml
Type: System.String
Parameter Sets: Expand, ExpandExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Identitetsparameter att skapa finns i avsnittet ANTECKNINGAR för INPUTOBJECT-egenskaper och skapa en hash-tabell.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: ExpandViaIdentity, ExpandViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -MsixImageUri
Representerar URI som refererar till MSIX-bild till-bygge, se avsnittet ANTECKNINGAR för MSIXIMAGEURI-egenskaper och skapa en hash-tabell.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixImageUri
Parameter Sets: Expand, ExpandViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
Namnet på resursgruppen.
Namnet är okänsligt.

```yaml
Type: System.String
Parameter Sets: Expand, ExpandExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
ID för målprenumerationen.

```yaml
Type: System.String
Parameter Sets: Expand, ExpandExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Uri
URI till bild

```yaml
Type: System.String
Parameter Sets: ExpandExpanded, ExpandViaIdentityExpanded
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

### Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixImageUri

### Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity

## UTDATA

### Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IExpandMsixImage

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

MSIXIMAGEURI <IMsixImageUri> : Representerar URI som refererar till MSIX-bild
  - `[Uri <String>]`: URI till bild

## RELATERADE LÄNKAR

