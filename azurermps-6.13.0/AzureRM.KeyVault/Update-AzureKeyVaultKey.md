---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/update-azurekeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultKey.md
ms.openlocfilehash: e9e2401ab96da63c3fe6b5978916b96f98db9f54
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576949"
---
# <span data-ttu-id="b8ee7-101">Update-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b8ee7-101">Update-AzureKeyVaultKey</span></span>

## <span data-ttu-id="b8ee7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b8ee7-102">SYNOPSIS</span></span>
<span data-ttu-id="b8ee7-103">Uppdaterar attributen för en nycklar i ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="b8ee7-103">Updates the attributes of a key in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8ee7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b8ee7-104">SYNTAX</span></span>

### <span data-ttu-id="b8ee7-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="b8ee7-105">Default (Default)</span></span>
```
Update-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8ee7-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="b8ee7-106">InputObject</span></span>
```
Update-AzureKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8ee7-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b8ee7-107">DESCRIPTION</span></span>
<span data-ttu-id="b8ee7-108">Cmdleten **Update-AzureKeyVaultKey** uppdaterar de redigerbara attributen för en Key i ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="b8ee7-108">The **Update-AzureKeyVaultKey** cmdlet updates the editable attributes of a key in a key vault.</span></span>

## <span data-ttu-id="b8ee7-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b8ee7-109">EXAMPLES</span></span>

### <span data-ttu-id="b8ee7-110">Exempel 1: ändra en post för att aktivera den och ange förfallo datum och-Taggar</span><span class="sxs-lookup"><span data-stu-id="b8ee7-110">Example 1: Modify a key to enable it, and set the expiration date and tags</span></span>
```powershell
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = 'true'}
PS C:\> Update-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Expires $Expires -Enable $True -Tag $Tags -PassThru

Vault Name     : Contoso
Name           : ITSoftware
Version        : 394f9379a47a4e2086585468de6c7ae5
Id             : https://Contoso.vault.azure.net:443/keys/ITSoftware/394f9379a47a4e2086585468de6c7ae5
Enabled        : True
Expires        : 5/25/2020 7:58:07 PM
Not Before     :
Created        : 4/6/2018 11:31:36 PM
Updated        : 5/25/2018 7:59:02 PM
Purge Disabled : False
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="b8ee7-111">Det första kommandot skapar ett **datetime** -objekt med hjälp av cmdleten **Get-date** .</span><span class="sxs-lookup"><span data-stu-id="b8ee7-111">The first command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="b8ee7-112">Detta objekt anger en tid två år framåt i tiden.</span><span class="sxs-lookup"><span data-stu-id="b8ee7-112">That object specifies a time two years in the future.</span></span> <span data-ttu-id="b8ee7-113">I kommandot lagras datumet i $Expires variabel.</span><span class="sxs-lookup"><span data-stu-id="b8ee7-113">The command stores that date in the $Expires variable.</span></span>
<span data-ttu-id="b8ee7-114">Om du vill ha mer information skriver du `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="b8ee7-114">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="b8ee7-115">Det andra kommandot skapar en variabel för att lagra tagg värden med hög allvarlighets grad och redovisning.</span><span class="sxs-lookup"><span data-stu-id="b8ee7-115">The second command creates a variable to store tag values of high severity and Accounting.</span></span>
<span data-ttu-id="b8ee7-116">Det slutliga kommandot ändrar en tangent som heter ITSoftware.</span><span class="sxs-lookup"><span data-stu-id="b8ee7-116">The final command modifies a key named ITSoftware.</span></span> <span data-ttu-id="b8ee7-117">Med kommandot aktive ras den här knappen, vilket innebär att den upphör att gälla den tid som lagras i $Expires och anger de taggar som lagras i $Tags.</span><span class="sxs-lookup"><span data-stu-id="b8ee7-117">The command enables the key, sets its expiration time to the time stored in $Expires, and sets the tags that are stored in $Tags.</span></span>

### <span data-ttu-id="b8ee7-118">Exempel 2: ändra en tangenten för att ta bort alla Taggar</span><span class="sxs-lookup"><span data-stu-id="b8ee7-118">Example 2: Modify a key to delete all tags</span></span>
```powershell
PS C:\> Update-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Version '394f9379a47a4e2086585468de6c7ae5' -Tag @{}

Vault Name     : Contoso
Name           : ITSoftware
Version        : 394f9379a47a4e2086585468de6c7ae5
Id             : https://Contoso.vault.azure.net:443/keys/ITSoftware/394f9379a47a4e2086585468de6c7ae5
Enabled        : True
Expires        : 5/25/2020 7:58:07 PM
Not Before     :
Created        : 4/6/2018 11:31:36 PM
Updated        : 5/25/2018 8:00:08 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="b8ee7-119">De här kommandona tar bort alla Taggar för en viss version av en Key som heter ITSoftware.</span><span class="sxs-lookup"><span data-stu-id="b8ee7-119">This commands deletes all tags for a specific version of a key named ITSoftware.</span></span>

## <span data-ttu-id="b8ee7-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b8ee7-120">PARAMETERS</span></span>

### <span data-ttu-id="b8ee7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8ee7-121">-DefaultProfile</span></span>
<span data-ttu-id="b8ee7-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b8ee7-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8ee7-123">-Aktivera</span><span class="sxs-lookup"><span data-stu-id="b8ee7-123">-Enable</span></span>
<span data-ttu-id="b8ee7-124">Värdet True gör att den här tangenten och värdet false kan komma till.</span><span class="sxs-lookup"><span data-stu-id="b8ee7-124">Value of true enables the key and a value of false disabless the key.</span></span>
<span data-ttu-id="b8ee7-125">Om det inte anges ändras inte det befintliga aktiverade/inaktiverade läget.</span><span class="sxs-lookup"><span data-stu-id="b8ee7-125">If not specified, the existing enabled/disabled state remains unchanged.</span></span>

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

### <span data-ttu-id="b8ee7-126">-Upphör</span><span class="sxs-lookup"><span data-stu-id="b8ee7-126">-Expires</span></span>
<span data-ttu-id="b8ee7-127">Förfallo tid i UTC-tid.</span><span class="sxs-lookup"><span data-stu-id="b8ee7-127">The expiration time of a key in UTC time.</span></span>
<span data-ttu-id="b8ee7-128">Om det inte anges ändras inte den befintliga förfallo tiden för den gamla.</span><span class="sxs-lookup"><span data-stu-id="b8ee7-128">If not specified, the existing expiration time of the key remains unchanged.</span></span>

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

### <span data-ttu-id="b8ee7-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b8ee7-129">-InputObject</span></span>
<span data-ttu-id="b8ee7-130">Nyckelvärdet</span><span class="sxs-lookup"><span data-stu-id="b8ee7-130">Key object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8ee7-131">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="b8ee7-131">-KeyOps</span></span>
<span data-ttu-id="b8ee7-132">Vilka operationer som kan utföras med tangenten.</span><span class="sxs-lookup"><span data-stu-id="b8ee7-132">The operations that can be performed with the key.</span></span>
<span data-ttu-id="b8ee7-133">Om det inte anges förblir de befintliga nycklarnas viktiga operationer oförändrade.</span><span class="sxs-lookup"><span data-stu-id="b8ee7-133">If not specified, the existing key operations of the key remain unchanged.</span></span>

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

### <span data-ttu-id="b8ee7-134">-Namn</span><span class="sxs-lookup"><span data-stu-id="b8ee7-134">-Name</span></span>
<span data-ttu-id="b8ee7-135">Namn på knappen.</span><span class="sxs-lookup"><span data-stu-id="b8ee7-135">Key name.</span></span>
<span data-ttu-id="b8ee7-136">Cmdlet konstruerar FQDN för en Key från valv namnet, den valda miljön och det här namnet.</span><span class="sxs-lookup"><span data-stu-id="b8ee7-136">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8ee7-137">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="b8ee7-137">-NotBefore</span></span>
<span data-ttu-id="b8ee7-138">UTC-tiden innan den här tangenten kan användas.</span><span class="sxs-lookup"><span data-stu-id="b8ee7-138">The UTC time before which key can't be used.</span></span>
<span data-ttu-id="b8ee7-139">Om det inte anges ändras inte NotBefore befintliga attribut.</span><span class="sxs-lookup"><span data-stu-id="b8ee7-139">If not specified, the existing NotBefore attribute of the key remains unchanged.</span></span>

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

### <span data-ttu-id="b8ee7-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b8ee7-140">-PassThru</span></span>
<span data-ttu-id="b8ee7-141">Cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="b8ee7-141">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="b8ee7-142">Om den här växeln anges returneras det uppdaterade nyckelvärdet.</span><span class="sxs-lookup"><span data-stu-id="b8ee7-142">If this switch is specified, returns the updated key bundle object.</span></span>

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

### <span data-ttu-id="b8ee7-143">-Tagg</span><span class="sxs-lookup"><span data-stu-id="b8ee7-143">-Tag</span></span>
<span data-ttu-id="b8ee7-144">En hash-produkt representerar viktiga taggar.</span><span class="sxs-lookup"><span data-stu-id="b8ee7-144">A hashtable represents key tags.</span></span>
<span data-ttu-id="b8ee7-145">Om det inte anges ändras inte de befintliga taggarna för tangenten.</span><span class="sxs-lookup"><span data-stu-id="b8ee7-145">If not specified, the existings tags of the key remain unchanged.</span></span>

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

### <span data-ttu-id="b8ee7-146">-VaultName</span><span class="sxs-lookup"><span data-stu-id="b8ee7-146">-VaultName</span></span>
<span data-ttu-id="b8ee7-147">Valv namn.</span><span class="sxs-lookup"><span data-stu-id="b8ee7-147">Vault name.</span></span>
<span data-ttu-id="b8ee7-148">Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="b8ee7-148">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="b8ee7-149">-Version</span><span class="sxs-lookup"><span data-stu-id="b8ee7-149">-Version</span></span>
<span data-ttu-id="b8ee7-150">Huvud version.</span><span class="sxs-lookup"><span data-stu-id="b8ee7-150">Key version.</span></span>
<span data-ttu-id="b8ee7-151">Cmdlet konstruerar FQDN för en Key från valv namnet, den valda miljön, namn och huvud version.</span><span class="sxs-lookup"><span data-stu-id="b8ee7-151">Cmdlet constructs the FQDN of a key from vault name, currently selected environment, key name and key version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8ee7-152">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b8ee7-152">-Confirm</span></span>
<span data-ttu-id="b8ee7-153">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b8ee7-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8ee7-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8ee7-154">-WhatIf</span></span>
<span data-ttu-id="b8ee7-155">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b8ee7-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8ee7-156">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b8ee7-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8ee7-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8ee7-157">CommonParameters</span></span>
<span data-ttu-id="b8ee7-158">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8ee7-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8ee7-159">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8ee7-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8ee7-160">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b8ee7-160">INPUTS</span></span>

### <span data-ttu-id="b8ee7-161">Microsoft. Azure. commands. valv. Models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="b8ee7-161">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>
<span data-ttu-id="b8ee7-162">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b8ee7-162">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="b8ee7-163">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b8ee7-163">OUTPUTS</span></span>

### <span data-ttu-id="b8ee7-164">Microsoft. Azure. commands. valv. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b8ee7-164">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="b8ee7-165">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b8ee7-165">NOTES</span></span>

## <span data-ttu-id="b8ee7-166">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b8ee7-166">RELATED LINKS</span></span>
