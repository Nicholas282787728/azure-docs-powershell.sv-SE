---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultkeyattribute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultKeyAttribute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultKeyAttribute.md
ms.openlocfilehash: 4b9799a0d2433b513b801a95ffd5c408bf8bdbf2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577193"
---
# <span data-ttu-id="75218-101">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="75218-101">Set-AzureKeyVaultKeyAttribute</span></span>

## <span data-ttu-id="75218-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="75218-102">SYNOPSIS</span></span>
<span data-ttu-id="75218-103">Uppdaterar attributen för en nycklar i ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="75218-103">Updates the attributes of a key in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75218-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="75218-104">SYNTAX</span></span>

### <span data-ttu-id="75218-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="75218-105">Default (Default)</span></span>
```
Set-AzureKeyVaultKeyAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75218-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="75218-106">InputObject</span></span>
```
Set-AzureKeyVaultKeyAttribute [-InputObject] <PSKeyVaultKeyIdentityItem> [[-Version] <String>]
 [-Enable <Boolean>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75218-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="75218-107">DESCRIPTION</span></span>
<span data-ttu-id="75218-108">Cmdleten **set-AzureKeyVaultKeyAttribute** uppdaterar de redigerbara attributen för en Key i ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="75218-108">The **Set-AzureKeyVaultKeyAttribute** cmdlet updates the editable attributes of a key in a key vault.</span></span>

## <span data-ttu-id="75218-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="75218-109">EXAMPLES</span></span>

### <span data-ttu-id="75218-110">Exempel 1: ändra en post för att aktivera den och ange förfallo datum och-Taggar</span><span class="sxs-lookup"><span data-stu-id="75218-110">Example 1: Modify a key to enable it, and set the expiration date and tags</span></span>
```
PS C:\>$Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = null}
PS C:\> Set-AzureKeyVaultKeyAttribute -VaultName 'Contoso' -Name 'ITSoftware' -Expires $Expires -Enable $True -Tag $Tags -PassThru
```

<span data-ttu-id="75218-111">Det första kommandot skapar ett **datetime** -objekt med hjälp av cmdleten **Get-date** .</span><span class="sxs-lookup"><span data-stu-id="75218-111">The first command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="75218-112">Detta objekt anger en tid två år framåt i tiden.</span><span class="sxs-lookup"><span data-stu-id="75218-112">That object specifies a time two years in the future.</span></span> <span data-ttu-id="75218-113">I kommandot lagras datumet i $Expires variabel.</span><span class="sxs-lookup"><span data-stu-id="75218-113">The command stores that date in the $Expires variable.</span></span>
<span data-ttu-id="75218-114">Om du vill ha mer information skriver du `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="75218-114">For more information, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="75218-115">Det andra kommandot skapar en variabel för att lagra tagg värden med hög allvarlighets grad och redovisning.</span><span class="sxs-lookup"><span data-stu-id="75218-115">The second command creates a variable to store tag values of high severity and Accounting.</span></span>

<span data-ttu-id="75218-116">Det slutliga kommandot ändrar en tangent som heter ITSoftware.</span><span class="sxs-lookup"><span data-stu-id="75218-116">The final command modifies a key named ITSoftware.</span></span> <span data-ttu-id="75218-117">Med kommandot aktive ras den här knappen, vilket innebär att den upphör att gälla den tid som lagras i $Expires och anger de taggar som lagras i $Tags.</span><span class="sxs-lookup"><span data-stu-id="75218-117">The command enables the key, sets its expiration time to the time stored in $Expires, and sets the tags that are stored in $Tags.</span></span>

### <span data-ttu-id="75218-118">Exempel 2: ändra en tangenten för att ta bort alla Taggar</span><span class="sxs-lookup"><span data-stu-id="75218-118">Example 2: Modify a key to delete all tags</span></span>
```
PS C:\>Set-AzureKeyVaultKeyAttribute -VaultName 'Contoso' -Name 'ITSoftware' -Version '7EEA45C6EE50490B9C3176F80AC1A0DG' -Tag @{}
```

<span data-ttu-id="75218-119">De här kommandona tar bort alla Taggar för en viss version av en Key som heter ITSoftware.</span><span class="sxs-lookup"><span data-stu-id="75218-119">This commands deletes all tags for a specific version of a key named ITSoftware.</span></span>

## <span data-ttu-id="75218-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="75218-120">PARAMETERS</span></span>

### <span data-ttu-id="75218-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75218-121">-DefaultProfile</span></span>
<span data-ttu-id="75218-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="75218-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="75218-123">-Aktivera</span><span class="sxs-lookup"><span data-stu-id="75218-123">-Enable</span></span>
<span data-ttu-id="75218-124">Anger om en Key ska aktive ras eller inaktive ras.</span><span class="sxs-lookup"><span data-stu-id="75218-124">Specifies whether to enable or disable a key.</span></span> <span data-ttu-id="75218-125">Ett värde på $True aktiverar tangenten.</span><span class="sxs-lookup"><span data-stu-id="75218-125">A value of $True enables the key.</span></span> <span data-ttu-id="75218-126">Ett värde på $False inaktiverar tangenten.</span><span class="sxs-lookup"><span data-stu-id="75218-126">A value of $False disables the key.</span></span> <span data-ttu-id="75218-127">Om du inte anger den här parametern ändras inte den här cmdletens status.</span><span class="sxs-lookup"><span data-stu-id="75218-127">If you do not specify this parameter, this cmdlet does not modify the status of the key.</span></span>

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

### <span data-ttu-id="75218-128">-Upphör</span><span class="sxs-lookup"><span data-stu-id="75218-128">-Expires</span></span>
<span data-ttu-id="75218-129">Anger förfallo tid, som ett **datetime** -objekt, för den Key som denna cmdlet uppdaterar.</span><span class="sxs-lookup"><span data-stu-id="75218-129">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet updates.</span></span> <span data-ttu-id="75218-130">Den här parametern använder koordinerad Universal Time (UTC).</span><span class="sxs-lookup"><span data-stu-id="75218-130">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="75218-131">Använd cmdleten **Get-date** för att hämta ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="75218-131">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="75218-132">Om du vill ha mer information skriver du `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="75218-132">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="75218-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75218-133">-InputObject</span></span>
<span data-ttu-id="75218-134">Nyckelvärdet</span><span class="sxs-lookup"><span data-stu-id="75218-134">Key object</span></span>

```yaml
Type: PSKeyVaultKeyIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75218-135">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="75218-135">-KeyOps</span></span>
<span data-ttu-id="75218-136">Anger en matris med åtgärder som kan utföras med hjälp av den här cmdleten som läggs till.</span><span class="sxs-lookup"><span data-stu-id="75218-136">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="75218-137">Om du inte anger den här parametern kan alla operationer utföras.</span><span class="sxs-lookup"><span data-stu-id="75218-137">If you do not specify this parameter, all operations can be performed.</span></span>

<span data-ttu-id="75218-138">De acceptabla värdena för den här parametern är en kommaavgränsad lista över viktiga åtgärder som definieras i JSON Web Key-specifikationen.</span><span class="sxs-lookup"><span data-stu-id="75218-138">The acceptable values for this parameter are a comma-separated list of key operations as defined by the JSON Web Key specification.</span></span> <span data-ttu-id="75218-139">Följande värden (Skift läges känsliga):</span><span class="sxs-lookup"><span data-stu-id="75218-139">These values (case-sensitive) are:</span></span>

- <span data-ttu-id="75218-140">inträffade</span><span class="sxs-lookup"><span data-stu-id="75218-140">encrypt</span></span>
- <span data-ttu-id="75218-141">dekryptera</span><span class="sxs-lookup"><span data-stu-id="75218-141">decrypt</span></span>
- <span data-ttu-id="75218-142">ska</span><span class="sxs-lookup"><span data-stu-id="75218-142">wrap</span></span>
- <span data-ttu-id="75218-143">unwrap</span><span class="sxs-lookup"><span data-stu-id="75218-143">unwrap</span></span>
- <span data-ttu-id="75218-144">Logga in</span><span class="sxs-lookup"><span data-stu-id="75218-144">sign</span></span>
- <span data-ttu-id="75218-145">kontroll</span><span class="sxs-lookup"><span data-stu-id="75218-145">verify</span></span>
- <span data-ttu-id="75218-146">reservdomänkontrollant</span><span class="sxs-lookup"><span data-stu-id="75218-146">backup</span></span>
- <span data-ttu-id="75218-147">terställa</span><span class="sxs-lookup"><span data-stu-id="75218-147">restore</span></span>

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

### <span data-ttu-id="75218-148">-Namn</span><span class="sxs-lookup"><span data-stu-id="75218-148">-Name</span></span>
<span data-ttu-id="75218-149">Anger namnet på den du vill uppdatera.</span><span class="sxs-lookup"><span data-stu-id="75218-149">Specifies the name of the key to update.</span></span> <span data-ttu-id="75218-150">Denna cmdlet konstruerar det fullständigt kvalificerade domän namnet (FQDN) för en nycklar baserat på namnet som den här parametern anger, namnet på Key-valvet och din nuvarande miljö.</span><span class="sxs-lookup"><span data-stu-id="75218-150">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75218-151">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="75218-151">-NotBefore</span></span>
<span data-ttu-id="75218-152">Anger tiden, som ett **datetime** -objekt, innan det inte går att använda tangenten.</span><span class="sxs-lookup"><span data-stu-id="75218-152">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span>
<span data-ttu-id="75218-153">Den här parametern använder UTC.</span><span class="sxs-lookup"><span data-stu-id="75218-153">This parameter uses UTC.</span></span>
<span data-ttu-id="75218-154">Använd cmdleten **Get-date** för att hämta ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="75218-154">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>

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

### <span data-ttu-id="75218-155">-PassThru</span><span class="sxs-lookup"><span data-stu-id="75218-155">-PassThru</span></span>
<span data-ttu-id="75218-156">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="75218-156">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="75218-157">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="75218-157">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="75218-158">-Tagg</span><span class="sxs-lookup"><span data-stu-id="75218-158">-Tag</span></span>
<span data-ttu-id="75218-159">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="75218-159">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="75218-160">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="75218-160">For example:</span></span>

<span data-ttu-id="75218-161">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="75218-161">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="75218-162">-VaultName</span><span class="sxs-lookup"><span data-stu-id="75218-162">-VaultName</span></span>
<span data-ttu-id="75218-163">Anger namnet på det huvud valv där denna cmdlet ändrar tangenten.</span><span class="sxs-lookup"><span data-stu-id="75218-163">Specifies the name of the key vault in which this cmdlet modifies the key.</span></span>
<span data-ttu-id="75218-164">Denna cmdlet konstruerar FQDN för ett Key valv baserat på namnet som den här parametern anger och din nuvarande miljö.</span><span class="sxs-lookup"><span data-stu-id="75218-164">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75218-165">-Version</span><span class="sxs-lookup"><span data-stu-id="75218-165">-Version</span></span>
<span data-ttu-id="75218-166">Anger huvud versionen.</span><span class="sxs-lookup"><span data-stu-id="75218-166">Specifies the key version.</span></span>
<span data-ttu-id="75218-167">Denna cmdlet konstruerar FQDN för en nycklar baserat på Key valv-namnet, den valda miljön, namnet på knappen och huvud versionen.</span><span class="sxs-lookup"><span data-stu-id="75218-167">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: KeyVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75218-168">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="75218-168">-Confirm</span></span>
<span data-ttu-id="75218-169">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="75218-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75218-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75218-170">-WhatIf</span></span>
<span data-ttu-id="75218-171">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="75218-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75218-172">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="75218-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75218-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75218-173">CommonParameters</span></span>
<span data-ttu-id="75218-174">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75218-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75218-175">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75218-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75218-176">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="75218-176">INPUTS</span></span>

### <span data-ttu-id="75218-177">Ingen</span><span class="sxs-lookup"><span data-stu-id="75218-177">None</span></span>
<span data-ttu-id="75218-178">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="75218-178">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="75218-179">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="75218-179">OUTPUTS</span></span>

### <span data-ttu-id="75218-180">Microsoft. Azure. commands. valv. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="75218-180">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="75218-181">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="75218-181">NOTES</span></span>

## <span data-ttu-id="75218-182">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="75218-182">RELATED LINKS</span></span>

[<span data-ttu-id="75218-183">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="75218-183">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="75218-184">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="75218-184">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="75218-185">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="75218-185">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)
