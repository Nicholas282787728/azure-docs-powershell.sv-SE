---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://go.microsoft.com/fwlink/?LinkId=690302
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultKeyAttribute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultKeyAttribute.md
ms.openlocfilehash: fbc2c4cd56da23bef29716800316f479159af148
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584688"
---
# <span data-ttu-id="1e946-101">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="1e946-101">Set-AzureKeyVaultKeyAttribute</span></span>

## <span data-ttu-id="1e946-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1e946-102">SYNOPSIS</span></span>
<span data-ttu-id="1e946-103">Uppdaterar attributen för en nycklar i ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="1e946-103">Updates the attributes of a key in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e946-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1e946-104">SYNTAX</span></span>

```
Set-AzureKeyVaultKeyAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e946-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1e946-105">DESCRIPTION</span></span>
<span data-ttu-id="1e946-106">Cmdleten **set-AzureKeyVaultKeyAttribute** uppdaterar de redigerbara attributen för en Key i ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="1e946-106">The **Set-AzureKeyVaultKeyAttribute** cmdlet updates the editable attributes of a key in a key vault.</span></span>

## <span data-ttu-id="1e946-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1e946-107">EXAMPLES</span></span>

### <span data-ttu-id="1e946-108">Exempel 1: ändra en post för att aktivera den och ange förfallo datum och-Taggar</span><span class="sxs-lookup"><span data-stu-id="1e946-108">Example 1: Modify a key to enable it, and set the expiration date and tags</span></span>
```
PS C:\>$Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = null}
PS C:\> Set-AzureKeyVaultKeyAttribute -VaultName 'Contoso' -Name 'ITSoftware' -Expires $Expires -Enable $True -Tag $Tags -PassThru
```

<span data-ttu-id="1e946-109">Det första kommandot skapar ett **datetime** -objekt med hjälp av cmdleten **Get-date** .</span><span class="sxs-lookup"><span data-stu-id="1e946-109">The first command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="1e946-110">Detta objekt anger en tid två år framåt i tiden.</span><span class="sxs-lookup"><span data-stu-id="1e946-110">That object specifies a time two years in the future.</span></span> <span data-ttu-id="1e946-111">I kommandot lagras datumet i $Expires variabel.</span><span class="sxs-lookup"><span data-stu-id="1e946-111">The command stores that date in the $Expires variable.</span></span>
<span data-ttu-id="1e946-112">Om du vill ha mer information skriver du `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="1e946-112">For more information, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="1e946-113">Det andra kommandot skapar en variabel för att lagra tagg värden med hög allvarlighets grad och redovisning.</span><span class="sxs-lookup"><span data-stu-id="1e946-113">The second command creates a variable to store tag values of high severity and Accounting.</span></span>

<span data-ttu-id="1e946-114">Det slutliga kommandot ändrar en tangent som heter ITSoftware.</span><span class="sxs-lookup"><span data-stu-id="1e946-114">The final command modifies a key named ITSoftware.</span></span> <span data-ttu-id="1e946-115">Med kommandot aktive ras den här knappen, vilket innebär att den upphör att gälla den tid som lagras i $Expires och anger de taggar som lagras i $Tags.</span><span class="sxs-lookup"><span data-stu-id="1e946-115">The command enables the key, sets its expiration time to the time stored in $Expires, and sets the tags that are stored in $Tags.</span></span>

### <span data-ttu-id="1e946-116">Exempel 2: ändra en tangenten för att ta bort alla Taggar</span><span class="sxs-lookup"><span data-stu-id="1e946-116">Example 2: Modify a key to delete all tags</span></span>
```
PS C:\>Set-AzureKeyVaultKeyAttribute -VaultName 'Contoso' -Name 'ITSoftware' -Version '7EEA45C6EE50490B9C3176F80AC1A0DG' -Tag @{}
```

<span data-ttu-id="1e946-117">De här kommandona tar bort alla Taggar för en viss version av en Key som heter ITSoftware.</span><span class="sxs-lookup"><span data-stu-id="1e946-117">This commands deletes all tags for a specific version of a key named ITSoftware.</span></span>

## <span data-ttu-id="1e946-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1e946-118">PARAMETERS</span></span>

### <span data-ttu-id="1e946-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1e946-119">-Confirm</span></span>
<span data-ttu-id="1e946-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1e946-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e946-121">-Aktivera</span><span class="sxs-lookup"><span data-stu-id="1e946-121">-Enable</span></span>
<span data-ttu-id="1e946-122">Anger om en Key ska aktive ras eller inaktive ras.</span><span class="sxs-lookup"><span data-stu-id="1e946-122">Specifies whether to enable or disable a key.</span></span> <span data-ttu-id="1e946-123">Ett värde på $True aktiverar tangenten.</span><span class="sxs-lookup"><span data-stu-id="1e946-123">A value of $True enables the key.</span></span> <span data-ttu-id="1e946-124">Ett värde på $False inaktiverar tangenten.</span><span class="sxs-lookup"><span data-stu-id="1e946-124">A value of $False disables the key.</span></span> <span data-ttu-id="1e946-125">Om du inte anger den här parametern ändras inte den här cmdletens status.</span><span class="sxs-lookup"><span data-stu-id="1e946-125">If you do not specify this parameter, this cmdlet does not modify the status of the key.</span></span>

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

### <span data-ttu-id="1e946-126">-Upphör</span><span class="sxs-lookup"><span data-stu-id="1e946-126">-Expires</span></span>
<span data-ttu-id="1e946-127">Anger förfallo tid, som ett **datetime** -objekt, för den Key som denna cmdlet uppdaterar.</span><span class="sxs-lookup"><span data-stu-id="1e946-127">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet updates.</span></span> <span data-ttu-id="1e946-128">Den här parametern använder koordinerad Universal Time (UTC).</span><span class="sxs-lookup"><span data-stu-id="1e946-128">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="1e946-129">Använd cmdleten **Get-date** för att hämta ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="1e946-129">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="1e946-130">Om du vill ha mer information skriver du `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="1e946-130">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e946-131">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="1e946-131">-KeyOps</span></span>
<span data-ttu-id="1e946-132">Anger en matris med åtgärder som kan utföras med hjälp av den här cmdleten som läggs till.</span><span class="sxs-lookup"><span data-stu-id="1e946-132">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="1e946-133">Om du inte anger den här parametern kan alla operationer utföras.</span><span class="sxs-lookup"><span data-stu-id="1e946-133">If you do not specify this parameter, all operations can be performed.</span></span>

<span data-ttu-id="1e946-134">De acceptabla värdena för den här parametern är en kommaavgränsad lista över viktiga åtgärder som definieras i JSON Web Key-specifikationen.</span><span class="sxs-lookup"><span data-stu-id="1e946-134">The acceptable values for this parameter are a comma-separated list of key operations as defined by the JSON Web Key specification.</span></span> <span data-ttu-id="1e946-135">Följande värden (Skift läges känsliga):</span><span class="sxs-lookup"><span data-stu-id="1e946-135">These values (case-sensitive) are:</span></span>

- <span data-ttu-id="1e946-136">inträffade</span><span class="sxs-lookup"><span data-stu-id="1e946-136">encrypt</span></span>
- <span data-ttu-id="1e946-137">dekryptera</span><span class="sxs-lookup"><span data-stu-id="1e946-137">decrypt</span></span>
- <span data-ttu-id="1e946-138">ska</span><span class="sxs-lookup"><span data-stu-id="1e946-138">wrap</span></span>
- <span data-ttu-id="1e946-139">unwrap</span><span class="sxs-lookup"><span data-stu-id="1e946-139">unwrap</span></span>
- <span data-ttu-id="1e946-140">Logga in</span><span class="sxs-lookup"><span data-stu-id="1e946-140">sign</span></span>
- <span data-ttu-id="1e946-141">kontroll</span><span class="sxs-lookup"><span data-stu-id="1e946-141">verify</span></span>
- <span data-ttu-id="1e946-142">reservdomänkontrollant</span><span class="sxs-lookup"><span data-stu-id="1e946-142">backup</span></span>
- <span data-ttu-id="1e946-143">terställa</span><span class="sxs-lookup"><span data-stu-id="1e946-143">restore</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e946-144">-Namn</span><span class="sxs-lookup"><span data-stu-id="1e946-144">-Name</span></span>
<span data-ttu-id="1e946-145">Anger namnet på den du vill uppdatera.</span><span class="sxs-lookup"><span data-stu-id="1e946-145">Specifies the name of the key to update.</span></span> <span data-ttu-id="1e946-146">Denna cmdlet konstruerar det fullständigt kvalificerade domän namnet (FQDN) för en nycklar baserat på namnet som den här parametern anger, namnet på Key-valvet och din nuvarande miljö.</span><span class="sxs-lookup"><span data-stu-id="1e946-146">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e946-147">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="1e946-147">-NotBefore</span></span>
<span data-ttu-id="1e946-148">Anger tiden, som ett **datetime** -objekt, innan det inte går att använda tangenten.</span><span class="sxs-lookup"><span data-stu-id="1e946-148">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span>
<span data-ttu-id="1e946-149">Den här parametern använder UTC.</span><span class="sxs-lookup"><span data-stu-id="1e946-149">This parameter uses UTC.</span></span>
<span data-ttu-id="1e946-150">Använd cmdleten **Get-date** för att hämta ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="1e946-150">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e946-151">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1e946-151">-PassThru</span></span>
<span data-ttu-id="1e946-152">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="1e946-152">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1e946-153">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="1e946-153">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1e946-154">-Tagg</span><span class="sxs-lookup"><span data-stu-id="1e946-154">-Tag</span></span>
<span data-ttu-id="1e946-155">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="1e946-155">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1e946-156">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="1e946-156">For example:</span></span>

<span data-ttu-id="1e946-157">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="1e946-157">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e946-158">-VaultName</span><span class="sxs-lookup"><span data-stu-id="1e946-158">-VaultName</span></span>
<span data-ttu-id="1e946-159">Anger namnet på det huvud valv där denna cmdlet ändrar tangenten.</span><span class="sxs-lookup"><span data-stu-id="1e946-159">Specifies the name of the key vault in which this cmdlet modifies the key.</span></span>
<span data-ttu-id="1e946-160">Denna cmdlet konstruerar FQDN för ett Key valv baserat på namnet som den här parametern anger och din nuvarande miljö.</span><span class="sxs-lookup"><span data-stu-id="1e946-160">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e946-161">-Version</span><span class="sxs-lookup"><span data-stu-id="1e946-161">-Version</span></span>
<span data-ttu-id="1e946-162">Anger huvud versionen.</span><span class="sxs-lookup"><span data-stu-id="1e946-162">Specifies the key version.</span></span>
<span data-ttu-id="1e946-163">Denna cmdlet konstruerar FQDN för en nycklar baserat på Key valv-namnet, den valda miljön, namnet på knappen och huvud versionen.</span><span class="sxs-lookup"><span data-stu-id="1e946-163">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyVersion

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e946-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e946-164">-WhatIf</span></span>
<span data-ttu-id="1e946-165">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1e946-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e946-166">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1e946-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e946-167">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e946-167">-DefaultProfile</span></span>
<span data-ttu-id="1e946-168">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1e946-168">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e946-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e946-169">CommonParameters</span></span>
<span data-ttu-id="1e946-170">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e946-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e946-171">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e946-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e946-172">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1e946-172">INPUTS</span></span>

## <span data-ttu-id="1e946-173">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1e946-173">OUTPUTS</span></span>

### <span data-ttu-id="1e946-174">Microsoft. Azure. commands...</span><span class="sxs-lookup"><span data-stu-id="1e946-174">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="1e946-175">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1e946-175">NOTES</span></span>

## <span data-ttu-id="1e946-176">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1e946-176">RELATED LINKS</span></span>

[<span data-ttu-id="1e946-177">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1e946-177">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="1e946-178">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1e946-178">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="1e946-179">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1e946-179">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)
