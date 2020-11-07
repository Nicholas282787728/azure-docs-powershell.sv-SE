---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 846F781C-73A3-4BBE-ABD9-897371109FBE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/add-azurekeyvaultkey
schema: 2.0.0
ms.openlocfilehash: 7af5afeac742bf9d256ac16470af0169170eb1e9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93928838"
---
# Add-AzureKeyVaultKey

## Sammanfattning
Skapar en Key i ett nyckelord eller importerar en Key till ett Key Vault.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### Skapa (standard)
```
Add-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Importeras
```
Add-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Add-AzureKeyVaultKey** skapar en Key i ett nyckelord i ett nyckeltal i Azure Key Vault, eller importerar en till en Key Vault.
Använd denna cmdlet för att lägga till nycklar på något av följande sätt:

- Skapa en knapp i en maskinvarubaserad säkerhetsmodul (HSM) i Key valv-tjänsten.
- Skapa en under program vara i Key valv-tjänsten.
- Importera en knapp från din egen Hardware säkerhetsmodul (HSM) till HSMs i Key valv-tjänsten.
- Importera en från en. pfx-fil på datorn.
- Importera en knapp från en. pfx-fil på datorn till HSMs (Hardware Security modules) i Key valv-tjänsten.

Du kan ange nyckelattribut eller acceptera standardinställningar för de här åtgärderna.

Om du skapar eller importerar en nycklar som har samma namn som en befintlig nycklar i ditt nyckelord uppdateras den ursprungliga tangenten med de värden som du anger för den nya. Du kan komma åt föregående värden med den version-specifika URI för den versionen av den här tangenten. Mer information om nyckel versioner och URI-strukturen finns i [om nycklar andSecrets](https://go.microsoft.com/fwlink/?linkid=518560) i nyckel VALVETS REST API-dokumentation.

Obs! Du måste först skapa ett BYOK-paket (en fil med fil namns tillägget. BYOK) med hjälp av BYOK-verktyg för Azure Key valv för att importera en nyckeln från din egen säkerhets modul för maskin vara. Mer information finns i [hur du skapar och överför HSM-Protected nycklar för Azure Key Vault](https://go.microsoft.com/fwlink/?LinkId=522252).

Vi rekommenderar att du säkerhetskopierar din-tangenten efter att den har skapats eller uppdaterats genom att använda Backup-AzureKeyVaultKey cmdlet. Det finns inga funktioner för att ångra borttagning, så om du råkar ta bort en eller flera rader och sedan ändrar dig kan du inte återställa den, såvida du inte har en säkerhets kopia av den.

## BESKRIVS

### Exempel 1: skapa en-tangenten
```
PS C:\>Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Destination 'Software'
```

Det här kommandot skapar en programskyddad nycklar med namnet ITSoftware i det nyckelord som heter Contoso.

### Exempel 2: skapa en HSM-skyddad nycklar
```
PS C:\>Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITHsm' -Destination 'HSM'
```

Det här kommandot skapar en HSM-skyddad nycklar i det nyckelord som heter Contoso.

### Exempel 3: skapa en transparens med icke-standardvärden
```
PS C:\>$KeyOperations = 'decrypt', 'verify'
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NotBefore = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = null}
PS C:\> Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITHsmNonDefault' -Destination 'HSM' -Expires $Expires -NotBefore $NotBefore -KeyOps $KeyOperations -Disable -Tag $Tags
```

Med det första kommandot lagras värdena dekryptera och verifiera i $KeyOperations variabeln.

Det andra kommandot skapar ett **datetime** -objekt, DEFINIERAT i UTC, med hjälp av cmdleten **Get-date** .
Detta objekt anger en tid två år framåt i tiden. I kommandot lagras datumet i $Expires variabel. Om du vill ha mer information skriver du `Get-Help Get-Date` .

Det tredje kommandot skapar ett **datetime** -objekt med hjälp av cmdleten **Get-date** . Det objektet anger den aktuella UTC-tiden. I kommandot lagras datumet i $NotBefore variabel.

Med kommandot slut skapas en Key med namnet ITHsmNonDefault som är en HSM-skyddad. Kommandot anger värden för tillåtna operationer som lagras $KeyOperations. Kommandot anger tider för parametrarna *Expires* och *NotBefore* som skapats i föregående kommandon och taggar för hög allvarlighets grad och det. Den nya knappen är inaktive rad. Du kan aktivera den med cmdleten **set-AzureKeyVaultKey** .

### Exempel 4: importera en HSM-skyddad nycklar
```
PS C:\>Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITByok' -KeyFilePath 'C:\Contoso\ITByok.byok' -Destination 'HSM'
```

Det här kommandot importerar den nycklar som heter ITByok från platsen som parametern för *fil Sök vägen* anger. Den importerade knappen är en HSM-skyddad.

Du måste först skapa ett BYOK-paket (en fil med fil namns tillägget. BYOK) med hjälp av BYOK-verktyg för Azure Key valv för att importera en nyckeln från din egen säkerhets modul för maskin vara.
Mer information finns i [hur du skapar och överför HSM-Protected nycklar för Azure Key Vault](https://go.microsoft.com/fwlink/?LinkId=522252).

### Exempel 5: importera en skyddad program vara
```
PS C:\>$Password = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITPfx' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password
```

Det första kommandot konverterar en sträng till en skyddad sträng med hjälp av cmdleten **ConvertTo-SecureString** och lagrar sedan strängen i $Password variabel. Om du vill ha mer information skriver du `Get-Help
ConvertTo-SecureString` .

Det andra kommandot skapar ett program varu lösen ord i ett contoso-valv. Kommandot anger platsen för den och det lösen ord som lagras i $Password.

### Exempel 6: importera en nycklar och tilldela attribut
```
PS C:\>$Password = ConvertTo-SecureString -String 'password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'high'; 'Accounting' = null }
PS C:\> Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITPfxToHSM' -Destination 'HSM' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password -Expires $Expires -Tag $Tags
```

Det första kommandot konverterar en sträng till en skyddad sträng med hjälp av cmdleten **ConvertTo-SecureString** och lagrar sedan strängen i $Password variabel.

Det andra kommandot skapar ett **datetime** -objekt med hjälp av cmdleten **Get-date** och lagrar sedan objektet i $expires variabeln.

Det tredje kommandot skapar $tags variabel för att ställa in taggar för hög allvarlighets grad och det.

Med kommandot slut importeras en nycklar som en HSM-tangenten från den angivna platsen. Kommandot anger den förfallo tid som är lagrad i $Expires och lösen ord som lagras i $Password och tillämpar taggarna som lagras i $tags.

## MALLPARAMETRAR

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Mål
Anger om du vill lägga till en nycklar som en programvarubaserad eller en HSM-skyddad nycklar i Key valv-tjänsten.
Giltiga värden är: HSM och program vara.

Obs! Om du vill använda HSM som mål måste du ha ett huvud valv som stöder HSMs. Mer information om tjänst nivåer och funktioner för Azure Key Vault finns på [webbplatsen för Azure Key Vault prissättning](https://go.microsoft.com/fwlink/?linkid=512521).

Den här parametern är obligatorisk när du skapar en ny. Om du importerar en fil med parametern *sökväg* är denna parameter valfri:

- Om du inte anger den här parametern och den här cmdleten importerar en fil som har namns tillägget. BYOK importeras den till en HSM-skyddad nycklar. Cmdleten kan inte importera den här tangenten som program skyddad.

- Om du inte anger den här parametern och den här cmdleten importerar en fil med namn tillägget. pfx importeras den som en programskyddad Server.

```yaml
Type: String
Parameter Sets: Create
Aliases: 
Accepted values: HSM, Software

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Import
Aliases: 
Accepted values: HSM, Software

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Inaktivera
Visar att den aktuella knappen är inaktive rad. Alla försök att använda den här knappen fungerar inte. Använd den här parametern om du har förinstallerat de nycklar du tänker aktivera senare.

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

### -Upphör
Anger förfallo tid, som ett **datetime** -objekt, för den Key som denna cmdlet lägger till. Den här parametern använder koordinerad Universal Time (UTC). Använd cmdleten **Get-date** för att hämta ett **datetime** -objekt. Om du vill ha mer information skriver du `Get-Help Get-Date` . Om du inte anger den här parametern upphör inte den att gälla.

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

### -KeyFilePassword
Anger ett lösen ord för den importerade filen som ett **SecureString** -objekt. För att få ett **SecureString** -objekt, Använd cmdleten **ConvertTo-SecureString** . Om du vill ha mer information skriver du `Get-Help ConvertTo-SecureString` . Du måste ange lösen ordet för att importera en fil med fil namns tillägget. pfx.

```yaml
Type: SecureString
Parameter Sets: Import
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Fil Sök väg
Anger sökvägen till en lokal fil som innehåller nyckel material som denna cmdlet importerar.
De giltiga fil namns tilläggen är. BYOK och. pfx.

- Om filen är en. BYOK-fil skyddas tangenten automatiskt av HSMs efter importen och du kan inte åsidosätta denna standard.

- Om filen är en. pfx-fil skyddas den automatiskt av program vara efter importen. Om du vill åsidosätta denna standard ställer du in *mål* parametern på HSM så att tangenten är HSM-skyddad.

Om du anger den här parametern är *mål* parametern valfri.

```yaml
Type: String
Parameter Sets: Import
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyOps
Anger en matris med åtgärder som kan utföras med hjälp av den här cmdleten som läggs till.
Om du inte anger den här parametern kan alla operationer utföras.

De acceptabla värdena för den här parametern är en kommaavgränsad lista med viktiga åtgärder som definieras av [JSON Web Key (JWK)-specifikationen](https://go.microsoft.com/fwlink/?LinkID=613300):

- Inträffade
- Dekryptera
- Ska
- Unwrap
- Logga in
- Kontroll

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namn
Anger namnet på den som ska läggas till i nyckelordet. Denna cmdlet konstruerar det fullständigt kvalificerade domän namnet (FQDN) för en nycklar baserat på namnet som den här parametern anger, namnet på Key-valvet och din nuvarande miljö. Namnet måste vara en sträng på mellan 1 och 63 tecken som bara innehåller 0-9, a-z, A-Z och-(streck symbolen).

```yaml
Type: String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NotBefore
Anger tiden, som ett **datetime** -objekt, innan det inte går att använda tangenten. Den här parametern använder UTC. Använd cmdleten **Get-date** för att hämta ett **datetime** -objekt. Om du inte anger den här parametern kan du använda den direkt.

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
Anger namnet på det nyckelord som den här cmdleten lägger till. Denna cmdlet konstruerar FQDN för ett Key valv baserat på namnet som den här parametern anger och din nuvarande miljö.

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
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

### Microsoft. Azure. commands...

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Säkerhets kopiering-AzureKeyVaultKey](./Backup-AzureKeyVaultKey.md)

[Get-AzureKeyVaultKey](./Get-AzureKeyVaultKey.md)

[Remove-AzureKeyVaultKey](./Remove-AzureKeyVaultKey.md)

[Set-AzureKeyVaultKeyAttribute](./Set-AzureKeyVaultKeyAttribute.md)
