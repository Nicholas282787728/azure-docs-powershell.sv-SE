---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 846F781C-73A3-4BBE-ABD9-897371109FBE
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
ms.openlocfilehash: 61125ae7d9fa78ec9f121cc9b60610258ad2c67c
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100405405"
---
# Add-AzKeyVaultKey

## SYNOPSIS
Skapar en nyckel i ett nyckelvalv eller importerar en nyckel till ett nyckelvalv.

## SYNTAX

### InteractiveCreate (standard)
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InteractiveImport
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-KeyType <String>] [-CurveName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### HsmInteractiveCreate
```
Add-AzKeyVaultKey -HsmName <String> [-Name] <String> [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>] -KeyType <String> [-CurveName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### HsmInteractiveImport
```
Add-AzKeyVaultKey -HsmName <String> [-Name] <String> -KeyFilePath <String> [-KeyFilePassword <SecureString>]
 [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObjectCreate
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObjectImport
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-KeyType <String>] [-CurveName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### HsmInputObjectCreate
```
Add-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [-Name] <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>] -KeyType <String>
 [-CurveName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### HsmInputObjectImport
```
Add-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ResourceIdCreate
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceIdImport
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-KeyType <String>] [-CurveName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### HsmResourceIdCreate
```
Add-AzKeyVaultKey -HsmResourceId <String> [-Name] <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>] -KeyType <String>
 [-CurveName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### HsmResourceIdImport
```
Add-AzKeyVaultKey -HsmResourceId <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Add-AzKeyVaultKey** skapar en nyckel i ett nyckelvalv i Azure-nyckelvalv eller importerar en nyckel till ett nyckelvalv.
Använd den här cmdleten för att lägga till nycklar med någon av följande metoder:
- Skapa en nyckel i en maskinvarusäkerhetsmodul (HSM) i nyckelvalvtjänsten.
- Skapa en nyckel i programvaran i nyckelvalvtjänsten.
- Importera en nyckel från din egen maskinvarusäkerhetsmodul (HSM) till HSMs i nyckelvalvtjänsten.
- Importera en nyckel från en PFX-fil på datorn.
- Importera en nyckel från en PFX-fil på datorn till maskinvarusäkerhetsmoduler (HSMs) i nyckelvalvtjänsten.
Du kan ange nyckelattribut eller acceptera standardinställningar för de här åtgärderna.
Om du skapar eller importerar en nyckel som har samma namn som en befintlig nyckel i nyckelvalvet uppdateras den ursprungliga nyckeln med de värden som du anger för den nya nyckeln. Du kan komma åt de tidigare värdena genom att använda den versionsspecifika URI:en för den versionen av nyckeln. Mer information om viktiga versioner och URI-strukturen finns i [dokumentationen om Om nycklar](http://go.microsoft.com/fwlink/?linkid=518560) och hemligheter i REST API-dokumentationen för nyckelvalv.
Obs! Om du vill importera en nyckel från din egen maskinvarusäkerhetsmodul måste du först generera ett BYOK-paket (en fil med filnamnstillägget .byok) med hjälp av BYOK-verktyguppsättningen för Azure-nyckelvalv. Mer information finns i Skapa [och överföra HSM-Protected nyckelnycklar för Azure Key Vault.](http://go.microsoft.com/fwlink/?LinkId=522252)
Det är en bra metod att backa upp nyckeln efter att den har skapats eller uppdaterats, med hjälp av cmdleten Backup-AzKeyVaultKey. Det finns inga ouppklarade funktioner. Om du tar bort eller tar bort nyckeln av misstag och sedan ändrar dig är nyckeln inte återställningsbar om du inte har en säkerhetskopia av den som du kan återställa.

## EXEMPEL

### Exempel 1: Skapa en nyckel
```powershell
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITSoftware' -Destination 'Software'

Vault Name     : contoso
Name           : ITSoftware
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITSoftware/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

Det här kommandot skapar en programvaruskyddad nyckel med namnet ITSoftware i nyckelvalvet Contoso.

### Exempel 2: Skapa en HSM-skyddad nyckel
```powershell
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITHsm' -Destination 'HSM'

Vault Name     : contoso
Name           : ITHsm
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITSoftware/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

Det här kommandot skapar en HSM-skyddad nyckel i nyckelvalvet Contoso.

### Exempel 3: Skapa en nyckel med värden som inte är standardvärden
```powershell
PS C:\> $KeyOperations = 'decrypt', 'verify'
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NotBefore = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = "true"}
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITHsmNonDefault' -Destination 'HSM' -Expires $Expires -NotBefore $NotBefore -KeyOps $KeyOperations -Disable -Tag $Tags

Vault Name     : contoso
Name           : ITHsmNonDefault
Version        : 929bfc14db84439b823ffd1bedadaf5f
Id             : https://contoso.vault.azure.net:443/keys/ITHsmNonDefault/929bfc14db84439b823ffd1bedadaf5f
Enabled        : False
Expires        : 5/21/2020 11:12:43 PM
Not Before     : 5/21/2018 11:12:50 PM
Created        : 5/21/2018 11:13:17 PM
Updated        : 5/21/2018 11:13:17 PM
Purge Disabled : False
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

Det första kommandot lagrar värdena dekryptera och verifierar i $KeyOperations variabeln.
Det andra kommandot skapar ett **DateTime-objekt** som definierats i UTC med cmdleten **Get-Date.**
Objektet anger en tid två år i framtiden. Kommandot lagrar det datumet i den $Expires variabeln. Om du vill ha mer information skriver du `Get-Help Get-Date` .
Det tredje kommandot skapar ett **DateTime-objekt** med **cmdleten Get-Date.** Objektet anger aktuell UTC-tid. Kommandot lagrar det datumet i den $NotBefore variabeln.
Det slutliga kommandot skapar en nyckel med namnet ITHsmNonDefault som är en HSM-skyddad nyckel. Kommandot anger värden för tillåtna nyckelåtgärder som lagras $KeyOperations. Kommandot anger tider för  parametrarna Förfallotid och *NotBefore* som skapats i tidigare kommandon samt taggar för hög allvarlighetsgrad och IT. Den nya nyckeln är inaktiverad. Du kan aktivera det med hjälp av **cmdleten Set-AzKeyVaultKey.**

### Exempel 4: Importera en HSM-skyddad nyckel
```powershell
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITByok' -KeyFilePath 'C:\Contoso\ITByok.byok' -Destination 'HSM'

Vault Name     : contoso
Name           : ITByok
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITByok/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

Det här kommandot importerar nyckeln med namnet ITByok från den plats som *KeyFilePath-parametern* anger. Den importerade nyckeln är en HSM-skyddad nyckel.
Om du vill importera en nyckel från din egen maskinvarusäkerhetsmodul måste du först generera ett BYOK-paket (en fil med filnamnstillägget .byok) med hjälp av AZURE-nyckelvalv BYOK-verktyguppsättningen.
Mer information finns i Skapa [och överföra HSM-Protected nyckelnycklar för Azure Key Vault.](http://go.microsoft.com/fwlink/?LinkId=522252)

### Exempel 5: Importera en programvaruskyddad nyckel
```powershell
PS C:\> $Password = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITPfx' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password

Vault Name     : contoso
Name           : ITPfx
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITPfx/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

Det första kommandot konverterar en sträng till en säker sträng med hjälp av cmdleten **ConvertTo-SecureString** och lagrar sedan strängen i $Password variabeln. Om du vill ha mer information skriver du `Get-Help
ConvertTo-SecureString` .
Det andra kommandot skapar ett programvarulösenord i Contosos nyckelvalv. Kommandot anger platsen för nyckeln och lösenordet som lagras i $Password.

### Exempel 6: Importera en nyckel och tilldela attribut
```powershell
PS C:\> $Password = ConvertTo-SecureString -String 'password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'high'; 'Accounting' = "true" }
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITPfxToHSM' -Destination 'HSM' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password -Expires $Expires -Tag $Tags

Vault Name     : contoso
Name           : ITPfxToHSM
Version        : 929bfc14db84439b823ffd1bedadaf5f
Id             : https://contoso.vault.azure.net:443/keys/ITPfxToHSM/929bfc14db84439b823ffd1bedadaf5f
Enabled        : True
Expires        : 5/21/2020 11:12:43 PM
Not Before     :
Created        : 5/21/2018 11:13:17 PM
Updated        : 5/21/2018 11:13:17 PM
Purge Disabled : False
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

Det första kommandot konverterar en sträng till en säker sträng med hjälp av cmdleten **ConvertTo-SecureString** och lagrar sedan strängen i $Password variabeln.
Det andra kommandot skapar ett **DateTime-objekt** med cmdleten **Get-Date** och lagrar sedan objektet i $Expires variabeln.
Det tredje kommandot skapar den $tags för att ange taggar för hög allvarlighetsgrad och IT.
Det sista kommandot importerar en nyckel som en HSM-nyckel från den angivna platsen. Kommandot anger förfallotiden som lagras i $Expires och lösenord som lagras i $Password, och de taggar som lagras i $tags.

### Exempel 7: Generera en BYOK-funktion (Key Exchange Key) för att "ta med din egen nyckel" (BYOK)

```powershell
PS C:\> $key = Add-AzKeyVaultKey -VaultName $vaultName -Name $keyName -Destination HSM -Size 2048 -KeyOps "import"
```

Genererar en nyckel (kallas även för en nyckelnyckel för Exchange (KEK)). KEK måste vara en RSA-HSM-nyckel som bara har importnyckelåtgärden. Endast Key Vault Premium SKU har stöd för RSA-HSM-nycklar.
Mer information finns i https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys

## PARAMETERS

### -CurveName
Anger kurvans namn på ellipskurva med kryptografi, det här värdet är giltigt när KeyType är EC.

```yaml
Type: System.String
Parameter Sets: InteractiveImport, HsmInteractiveCreate, InputObjectImport, HsmInputObjectCreate, ResourceIdImport, HsmResourceIdCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -Destination
Anger om nyckeln ska läggas till som en programvaruskyddad nyckel eller en HSM-skyddad nyckel i nyckelvalvtjänsten.
Giltiga värden är: HSM och programvara.
Obs! Om du vill använda HSM som destination måste du ha ett nyckelvalv som har stöd för HSMs. Mer information om tjänstnivåer och funktioner för Azure-nyckelvalv finns på webbplatsen för priser för [Azure-nyckelvalv.](http://go.microsoft.com/fwlink/?linkid=512521)
Den här parametern krävs när du skapar en ny nyckel. Om du importerar en nyckel med hjälp av *KeyFilePath-parametern* är den här parametern valfri:
- Om du inte anger den här parametern och den här cmdleten importerar en nyckel som har filnamnstillägget .byok importeras den nyckeln som en HSM-skyddad nyckel. Cmdleten kan inte importera den nyckeln som en programvaruskyddad nyckel.
- Om du inte anger den här parametern och denna cmdlet importerar en nyckel som har filnamnstillägget .pfx importeras nyckeln som en programvaruskyddad nyckel.

```yaml
Type: System.String
Parameter Sets: InteractiveCreate, InputObjectCreate, ResourceIdCreate
Aliases:
Accepted values: HSM, Software

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:
Accepted values: HSM, Software

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Disable
Anger att nyckeln du lägger till är inställd på ett inaktiverat initialt tillstånd. Alla försök att använda nyckeln misslyckas. Använd den här parametern om du förinstallerar nycklar som du tänker aktivera senare.

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

### -Förfaller
Anger förfallotiden som ett **DateTime-objekt** för nyckeln som denna cmdlet lägger till. Den här parametern använder UTC (Coordinated Universal Time). Om du vill **hämta ett DateTime-objekt** använder du cmdleten **Get-Date.** Om du vill ha mer information skriver du `Get-Help Get-Date` . Om du inte anger den här parametern förfaller inte nyckeln.

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

### -HsmName
HSM-namn. Cmdlet skapar FQDN för en hanterad HSM baserat på namnet och den valda miljön.

```yaml
Type: System.String
Parameter Sets: HsmInteractiveCreate, HsmInteractiveImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HsmObject
HSM-objekt.

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: HsmInputObjectCreate, HsmInputObjectImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -HsmResourceId
Resurs-ID för HSM.

```yaml
Type: System.String
Parameter Sets: HsmResourceIdCreate, HsmResourceIdImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InputObject
Valv-objekt.

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: InputObjectCreate, InputObjectImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -KeyFilePassword
Anger ett lösenord för den importerade filen som ett **SecureString-objekt.** Om du vill **hämta ett SecureString-objekt** använder du **cmdleten ConvertTo-SecureString.** Om du vill ha mer information skriver du `Get-Help ConvertTo-SecureString` . Du måste ange det här lösenordet om du vill importera en fil med filnamnstillägget .pfx.

```yaml
Type: System.Security.SecureString
Parameter Sets: InteractiveImport, HsmInteractiveImport, InputObjectImport, HsmInputObjectImport, ResourceIdImport, HsmResourceIdImport
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyFilePath
Anger sökvägen till en lokal fil som innehåller nyckelmaterial som cmdleten importerar.
Giltiga filnamnstillägg är .byok och .pfx.
- Om filen är en .byok-fil skyddas nyckeln automatiskt av HSMs efter importen och du kan inte åsidosätta den här standardinställningen.
- Om filen är en PFX-fil skyddas nyckeln automatiskt av programvaran efter importen. Om du vill åsidosätta standardinställningen anger du *målparametern* till HSM så att nyckeln är HSM-skyddad.
När du anger den här parametern är *målparametern* valfri.

```yaml
Type: System.String
Parameter Sets: InteractiveImport, HsmInteractiveImport, InputObjectImport, HsmInputObjectImport, ResourceIdImport, HsmResourceIdImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyOps
Anger en matris med åtgärder som kan utföras med hjälp av nyckeln som denna cmdlet adderar.
Om du inte anger den här parametern kan alla åtgärder utföras.
Godtagbara värden för den här parametern är en kommaavgränsad lista med nyckelåtgärder som definieras i [specifikationen JSON Web Key (JWK):](http://go.microsoft.com/fwlink/?LinkID=613300)
- kryptera
- dekryptera
- wrapKey
- unwrapKey
- signera
- verifiera
- import (endast för KEK, se exempel 7)

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyType
Anger nyckeltypen för den här nyckeln. Vid import av BYOK-nycklar används RSA som standard.

```yaml
Type: System.String
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: HsmInteractiveCreate, HsmInputObjectCreate, HsmResourceIdCreate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Anger namnet på nyckeln som ska läggas till i nyckelvalvet. Den här cmdleten skapar det fullständigt kvalificerade domännamnet (FQDN) för en nyckel baserat på namnet som den här parametern anger, namnet på nyckelvalvet och den aktuella miljön. Namnet måste vara en sträng med en teckenlängd på 1 till 63 tecken som bara innehåller 0-9, a-z, A-Ö och - (strecksymbolen).

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NotBefore
Anger tiden, som ett **DateTime-objekt,** före vilken nyckeln inte kan användas. Den här parametern använder UTC. Om du vill **hämta ett DateTime-objekt** använder du cmdleten **Get-Date.** Om du inte anger den här parametern kan nyckeln användas direkt.

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

### -ResourceId
Resurs-ID för valv.

```yaml
Type: System.String
Parameter Sets: ResourceIdCreate, ResourceIdImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Size
RSA-tangentstorlek, i bitar. Om detta inte anges anges en säker standard för tjänsten.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: InteractiveCreate, HsmInteractiveCreate, InputObjectCreate, HsmInputObjectCreate, ResourceIdCreate, HsmResourceIdCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
Nyckelvärdepar i form av en hash-tabell. Exempel: @{key0="value0";key1=$null;key2="value2"}

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
Anger namnet på nyckelvalvet som denna cmdlet lägger till nyckeln för. Den här cmdleten skapar FQDN för ett nyckelvalv baserat på namnet som den här parametern anger och din aktuella miljö.

```yaml
Type: System.String
Parameter Sets: InteractiveCreate, InteractiveImport
Aliases:

Required: True
Position: 0
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

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault

### System.String

## UTDATA

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Backup-AzKeyVaultKey](./Backup-AzKeyVaultKey.md)

[Get-AzKeyVaultKey](./Get-AzKeyVaultKey.md)

[Remove-AzKeyVaultKey](./Remove-AzKeyVaultKey.md)

