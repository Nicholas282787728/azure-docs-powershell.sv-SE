---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: E2A45461-6B41-42FF-A874-A4CEFC867A33
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/set-AzKeyvaultsecretattribute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultSecretAttribute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultSecretAttribute.md
ms.openlocfilehash: 719f0676b87cf785785b0adfbfde71ad2a6b965b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922670"
---
# Set-AzKeyVaultSecretAttribute

## Sammanfattning
Uppdaterar attribut för en hemlighet i ett nyckel valv.

## FRÅGESYNTAXEN

```
Set-AzKeyVaultSecretAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-Enable <Boolean>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **set-AzKeyVaultSecretAttribute** uppdaterar redigerbara attribut för en hemlighet i ett nyckel valv.

## BESKRIVS

### Exempel 1: ändra attributen för en hemlighet
```
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Nbf = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'HR' = null}
PS C:\> $ContentType= 'xml'
PS C:\> Set-AzKeyVaultSecretAttribute -VaultName 'ContosoVault' -Name 'HR' -Expires $Expires -NotBefore $Nbf -ContentType $ContentType -Enable $True -Tag $Tags -PassThru
```

De första fyra kommandona definierar attributen för utgångs datumet, NotBefore datum, taggar och kontext typ och lagrar attributen i variabler.

Det sista kommandot ändrar attributen för hemligheten HR i nyckel valvet med namnet ContosoVault, med hjälp av lagrade variabler.

### Exempel 2: ta bort taggarna och innehålls typen för en hemlighet
```
PS C:\>Set-AzKeyVaultSecretAttribute -VaultName 'ContosoVault' -Name 'HR' -Version '9EEA45C6EE50490B9C3176A80AC1A0DF' -ContentType '' -Tag -@{}
```

Detta kommando tar bort taggarna och innehålls typen för den angivna versionen av hemligheten med namnet HR i nyckel valvet contoso.

### Exempel 3: inaktivera den aktuella versionen av hemligheter vars namn börjar med den
```
PS C:\> $Vault = 'ContosoVault'
PS C:\> $Prefix = 'IT'
PS C:\> Get-AzKeyVaultSecret $Vault | Where-Object {$_.Name -like $Prefix + '*'} | Set-AzKeyVaultSecretAttribute -Enable $False
```

Det första kommandot lagrar strängvärdet Contoso i $Vault variabel.

Det andra kommandot lagrar det sträng värde som det $Prefix variabeln.

I det tredje kommandot används cmdleten Get-AzKeyVaultSecret för att hämta hemligheten i det angivna Key-valvet och sedan överförs dessa till cmdleten **WHERE-objekt** . Med cmdleten **Where-Object** filtrerar du hemligheterna för namnen som börjar med de tecken som. Kommandot rör den hemlighet som matchar filtret för Set-AzKeyVaultSecretAttribute cmdlet som inaktiverar dem.

### Exempel 4: Ange ContentType för alla versioner av en hemlighet
```
PS C:\>$VaultName = 'ContosoVault'
PS C:\> $Name = 'HR'
PS C:\> $ContentType = 'xml'
PS C:\> Get-AzKeyVaultKey -VaultName $VaultName -Name $Name -IncludeVersions | Set-AzKeyVaultSecretAttribute -ContentType $ContentType
```

De första tre kommandona definierar de String-variabler som ska användas för parametrarna *VaultName* , *Name* och *ContentType* . Med det fjärde kommandot används cmdleten Get-AzKeyVaultKey för att hämta de angivna nycklarna, och när du anger innehålls typen till XML för en Set-AzKeyVaultSecretAttribute-cmdlet.

## MALLPARAMETRAR

### -ContentType
Anger innehålls typen för en hemlighet. Om du inte anger den här parametern ändras inte den aktuella hemlighetens innehålls typ. Om du vill ta bort den befintliga innehålls typen anger du en tom sträng.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Aktivera
Anger om en hemlighet ska aktive ras. Ange $False om du vill inaktivera en hemlig hemlighet eller $True för att aktivera en hemlighet. Om du inte anger den här parametern ändras inte den aktuella hemlighetens aktiverade eller inaktiverade status.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Upphör
Anger det datum och den tid då en hemlig hemlighet upphör.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namn
Anger namnet på en hemlighet. Denna cmdlet konstruerar det fullständigt kvalificerade domän namnet (FQDN) på en hemlighet baserad på namnet som den här parametern anger, namnet på nyckel valvet och din nuvarande miljö.

```yaml
Type: String
Parameter Sets: (All)
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NotBefore
Anger den koordinerade universella tiden (UTC) innan hemligheten inte kan användas.
Om du inte anger den här parametern ändras inte den aktuella hemlighetens NotBefore-attribut.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Returnerar ett objekt som representerar det objekt som du arbetar med.
Denna cmdlet genererar som standard inga utdata.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tagg
Par med nyckelord i form av en hash-tabell. Till exempel:

@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VaultName
Anger namnet på det Key-valv som ska ändras.
Denna cmdlet konstruerar FQDN för ett Key valv baserat på namnet som den här parametern anger och din valda miljö.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Version
Anger vilken version av en hemlighet du har.
Denna cmdlet konstruerar FQDN för en hemlighet som baseras på nyckel valv namnet, din valda miljö, det hemliga namnet samt den hemliga versionen.

```yaml
Type: String
Parameter Sets: (All)
Aliases: SecretVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bekräfta
Du uppmanas att bekräfta innan du kör cmdleten.

```yaml
Type: SwitchParameter
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Ingen
Denna cmdlet accepterar inte indata.

## VÄRDEN

### Microsoft. Azure. commands. nyckel valv. Models. Secret
Returnerar Microsoft. Azure. commands. nyckel valv. Models. Secret-objekt om PassThru har angetts. Annars returnerar nej.

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzKeyVaultKey](./Get-AzKeyVaultKey.md)

[Get-AzKeyVaultSecret](./Get-AzKeyVaultSecret.md)

[Remove-AzKeyVaultSecret](./Remove-AzKeyVaultSecret.md)
