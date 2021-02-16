---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultSecret.md
ms.openlocfilehash: 5efc920d4dd6e8e83c0a2ee5f61768ac7373f864
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100219431"
---
# Update-AzKeyVaultSecret

## SYNOPSIS
Uppdaterar attribut för en hemlig i ett nyckelvalv.

## SYNTAX

### Standard (standard)
```
Update-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObject
```
Update-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Update-AzKeyVaultSecret** uppdaterar redigerbara attribut för en hemlig i ett nyckelvalv.

## EXEMPEL

### Exempel 1: Ändra attributen för en hemlig
```powershell
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Nbf = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'HR' = 'true'}
PS C:\> $ContentType= 'xml'
PS C:\> Update-AzKeyVaultSecret -VaultName 'ContosoVault' -Name 'HR' -Expires $Expires -NotBefore $Nbf -ContentType $ContentType -Enable $True -Tag $Tags -PassThru

Vault Name   : ContosoVault
Name         : HR
Version      : d476edfcd3544017a03bc49c1f3abec0
Id           : https://ContosoVault.vault.azure.net:443/secrets/HR/d476edfcd3544017a03bc49c1f3abec0
Enabled      : True
Expires      : 5/25/2020 8:01:58 PM
Not Before   : 5/25/2018 8:02:02 PM
Created      : 4/11/2018 11:45:06 PM
Updated      : 5/25/2018 8:02:45 PM
Content Type : xml
Tags         : Name      Value
               Severity  medium
               HR        true
```

De första fyra kommandona definierar attribut för utgångsdatumet, NotBefore-datum, taggar och kontexttyp och lagrar attributen i variabler.
Det slutliga kommandot ändrar attributen för hemligheten med namnet HR i nyckelvalvet ContosoVault, med hjälp av de lagrade variablerna.

### Exempel 2: Ta bort taggarna och innehållstypen för en hemlig
```
PS C:\> Update-AzKeyVaultSecret -VaultName 'ContosoVault' -Name 'HR' -Version '9EEA45C6EE50490B9C3176A80AC1A0DF' -ContentType '' -Tag -@{}
```

Det här kommandot tar bort taggarna och innehållstypen för den angivna versionen av hemligheten med namnet HR i nyckelvalvet Contoso.

### Exempel 3: Inaktivera den aktuella versionen av hemligheter vars namn börjar med IT
```
PS C:\> $Vault = 'ContosoVault'
PS C:\> $Prefix = 'IT'
PS C:\> Get-AzKeyVaultSecret $Vault | Where-Object {$_.Name -like $Prefix + '*'} | Update-AzKeyVaultSecret -Enable $False
```

Med det första kommandot lagras strängvärdet Contoso i $Vault variabeln.
Det andra kommandot lagrar strängvärdet IT i den $Prefix variabeln.
Det tredje kommandot använder cmdleten Get-AzKeyVaultSecret för att hämta hemligheterna i det angivna nyckelvalvet och skickar sedan dessa hemligheter till cmdleten **Where-Object.** **Cmdleten Where-Object** filtrerar hemligheterna efter namn som börjar med tecknen IT. Kommandorören de hemligheter som matchar filtret till Update-AzKeyVaultSecret cmdlet, vilket inaktiverar dem.

### Exempel 4: Ange ContentType för alla versioner av en hemlig
```
PS C:\> $VaultName = 'ContosoVault'
PS C:\> $Name = 'HR'
PS C:\> $ContentType = 'xml'
PS C:\> Get-AzKeyVaultKey -VaultName $VaultName -Name $Name -IncludeVersions | Update-AzKeyVaultSecret -ContentType $ContentType
```

De tre första kommandona definierar strängvariabler som används för *parametrarna VaultName,* *Name* *och ContentType.* Det fjärde kommandot använder cmdleten Get-AzKeyVaultKey för att få angivna nycklar och rör nycklarna till cmdleten Update-AzKeyVaultSecret för att ange innehållstypen till XML.

## PARAMETERS

### -ContentType
Hemligt innehållstyp.
Om det inte anges ändras inte det befintliga värdet av hemlighetens innehållstyp.
Ta bort det befintliga innehållstypvärdet genom att ange en tom sträng.

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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Enable
Aktivera i så fall en hemlig om-värde är sant.
Inaktivera en hemlig om värdet är falskt.
Om det inte anges ändras inte det befintliga värdet av hemlighetens aktiverade/inaktiverade tillstånd.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Förfaller
Utgångstiden för en hemlig i UTC-tid.
Om inget anges ändras inte det befintliga värdet av hemlighetens förfallotid.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Hemligt objekt

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Hemligt namn.
Cmdlet skapar FQDN för en hemlig från valv-namn, för närvarande markerad miljö och hemligt namn.

```yaml
Type: System.String
Parameter Sets: Default
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NotBefore
Tiden före vilken hemliga utc-timmar inte kan användas.
Om det inte anges ändras inte det befintliga värdet för hemlighetens NotBefore-attribut.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Cmdlet returnerar inte objekt som standard.
Returnera hemligt objekt om växeln har angetts.

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

### -Tag
En hashtabell som representerar hemliga taggar.
Om de inte anges ändras inte de befintliga taggarna för hemligheten.
Ta bort en tagg genom att ange en tom Hash-tabell.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VaultName
Valvnamn.
Cmdlet skapar FQDN för ett valv baserat på namnet och den valda miljön.

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Version
Hemlig version.
Cmdleten skapar FQDN för en hemlig från valvnamn, för närvarande markerad miljö, hemligt namn och hemlig version.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SecretVersion

Required: False
Position: 2
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

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem

## UTDATA

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret

## ANTECKNINGAR

## RELATERADE LÄNKAR
