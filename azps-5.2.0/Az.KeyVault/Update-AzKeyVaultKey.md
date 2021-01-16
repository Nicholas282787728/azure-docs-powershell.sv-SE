---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultKey.md
ms.openlocfilehash: de8e542079cdeebdb6513c8e0febf8cfe0952889
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394419"
---
# <span data-ttu-id="45877-101">Update-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="45877-101">Update-AzKeyVaultKey</span></span>

## <span data-ttu-id="45877-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="45877-102">SYNOPSIS</span></span>
<span data-ttu-id="45877-103">Uppdaterar attributen för en nycklar i ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="45877-103">Updates the attributes of a key in a key vault.</span></span>

## <span data-ttu-id="45877-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="45877-104">SYNTAX</span></span>

### <span data-ttu-id="45877-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="45877-105">Default (Default)</span></span>
```
Update-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45877-106">HsmInteractive</span><span class="sxs-lookup"><span data-stu-id="45877-106">HsmInteractive</span></span>
```
Update-AzKeyVaultKey -HsmName <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45877-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="45877-107">InputObject</span></span>
```
Update-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45877-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="45877-108">DESCRIPTION</span></span>
<span data-ttu-id="45877-109">Cmdleten **Update-AzKeyVaultKey** uppdaterar de redigerbara attributen för en Key i ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="45877-109">The **Update-AzKeyVaultKey** cmdlet updates the editable attributes of a key in a key vault.</span></span>

## <span data-ttu-id="45877-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="45877-110">EXAMPLES</span></span>

### <span data-ttu-id="45877-111">Exempel 1: ändra en post för att aktivera den och ange förfallo datum och-Taggar</span><span class="sxs-lookup"><span data-stu-id="45877-111">Example 1: Modify a key to enable it, and set the expiration date and tags</span></span>
```powershell
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = 'true'}
PS C:\> Update-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Expires $Expires -Enable $True -Tag $Tags -PassThru

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

<span data-ttu-id="45877-112">Det första kommandot skapar ett **datetime** -objekt med hjälp av cmdleten **Get-date** .</span><span class="sxs-lookup"><span data-stu-id="45877-112">The first command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="45877-113">Detta objekt anger en tid två år framåt i tiden.</span><span class="sxs-lookup"><span data-stu-id="45877-113">That object specifies a time two years in the future.</span></span> <span data-ttu-id="45877-114">I kommandot lagras datumet i $Expires variabel.</span><span class="sxs-lookup"><span data-stu-id="45877-114">The command stores that date in the $Expires variable.</span></span>
<span data-ttu-id="45877-115">Om du vill ha mer information skriver du `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="45877-115">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="45877-116">Det andra kommandot skapar en variabel för att lagra tagg värden med hög allvarlighets grad och redovisning.</span><span class="sxs-lookup"><span data-stu-id="45877-116">The second command creates a variable to store tag values of high severity and Accounting.</span></span>
<span data-ttu-id="45877-117">Det slutliga kommandot ändrar en tangent som heter ITSoftware.</span><span class="sxs-lookup"><span data-stu-id="45877-117">The final command modifies a key named ITSoftware.</span></span> <span data-ttu-id="45877-118">Med kommandot aktive ras den här knappen, vilket innebär att den upphör att gälla den tid som lagras i $Expires och anger de taggar som lagras i $Tags.</span><span class="sxs-lookup"><span data-stu-id="45877-118">The command enables the key, sets its expiration time to the time stored in $Expires, and sets the tags that are stored in $Tags.</span></span>

### <span data-ttu-id="45877-119">Exempel 2: ändra en tangenten för att ta bort alla Taggar</span><span class="sxs-lookup"><span data-stu-id="45877-119">Example 2: Modify a key to delete all tags</span></span>
```powershell
PS C:\> Update-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Version '394f9379a47a4e2086585468de6c7ae5' -Tag @{}

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

<span data-ttu-id="45877-120">De här kommandona tar bort alla Taggar för en viss version av en Key som heter ITSoftware.</span><span class="sxs-lookup"><span data-stu-id="45877-120">This commands deletes all tags for a specific version of a key named ITSoftware.</span></span>

## <span data-ttu-id="45877-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="45877-121">PARAMETERS</span></span>

### <span data-ttu-id="45877-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45877-122">-DefaultProfile</span></span>
<span data-ttu-id="45877-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="45877-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45877-124">-Aktivera</span><span class="sxs-lookup"><span data-stu-id="45877-124">-Enable</span></span>
<span data-ttu-id="45877-125">Värdet True gör att den här tangenten och värdet false kan komma till.</span><span class="sxs-lookup"><span data-stu-id="45877-125">Value of true enables the key and a value of false disabless the key.</span></span>
<span data-ttu-id="45877-126">Om det inte anges ändras inte det befintliga aktiverade/inaktiverade läget.</span><span class="sxs-lookup"><span data-stu-id="45877-126">If not specified, the existing enabled/disabled state remains unchanged.</span></span>

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

### <span data-ttu-id="45877-127">-Upphör</span><span class="sxs-lookup"><span data-stu-id="45877-127">-Expires</span></span>
<span data-ttu-id="45877-128">Förfallo tid i UTC-tid.</span><span class="sxs-lookup"><span data-stu-id="45877-128">The expiration time of a key in UTC time.</span></span>
<span data-ttu-id="45877-129">Om det inte anges ändras inte den befintliga förfallo tiden för den gamla.</span><span class="sxs-lookup"><span data-stu-id="45877-129">If not specified, the existing expiration time of the key remains unchanged.</span></span>

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

### <span data-ttu-id="45877-130">-HsmName</span><span class="sxs-lookup"><span data-stu-id="45877-130">-HsmName</span></span>
<span data-ttu-id="45877-131">HSM-namn.</span><span class="sxs-lookup"><span data-stu-id="45877-131">HSM name.</span></span> <span data-ttu-id="45877-132">Cmdlet konstruerar FQDN för en hanterad HSM baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="45877-132">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmInteractive
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45877-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="45877-133">-InputObject</span></span>
<span data-ttu-id="45877-134">Nyckelvärdet</span><span class="sxs-lookup"><span data-stu-id="45877-134">Key object</span></span>

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

### <span data-ttu-id="45877-135">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="45877-135">-KeyOps</span></span>
<span data-ttu-id="45877-136">Vilka operationer som kan utföras med tangenten.</span><span class="sxs-lookup"><span data-stu-id="45877-136">The operations that can be performed with the key.</span></span>
<span data-ttu-id="45877-137">Om det inte anges förblir de befintliga nycklarnas viktiga operationer oförändrade.</span><span class="sxs-lookup"><span data-stu-id="45877-137">If not specified, the existing key operations of the key remain unchanged.</span></span>

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

### <span data-ttu-id="45877-138">-Namn</span><span class="sxs-lookup"><span data-stu-id="45877-138">-Name</span></span>
<span data-ttu-id="45877-139">Namn på knappen.</span><span class="sxs-lookup"><span data-stu-id="45877-139">Key name.</span></span>
<span data-ttu-id="45877-140">Cmdlet konstruerar FQDN för en Key från valv namnet, den valda miljön och det här namnet.</span><span class="sxs-lookup"><span data-stu-id="45877-140">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, HsmInteractive
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45877-141">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="45877-141">-NotBefore</span></span>
<span data-ttu-id="45877-142">UTC-tiden innan den här tangenten kan användas.</span><span class="sxs-lookup"><span data-stu-id="45877-142">The UTC time before which key can't be used.</span></span>
<span data-ttu-id="45877-143">Om det inte anges ändras inte NotBefore befintliga attribut.</span><span class="sxs-lookup"><span data-stu-id="45877-143">If not specified, the existing NotBefore attribute of the key remains unchanged.</span></span>

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

### <span data-ttu-id="45877-144">-PassThru</span><span class="sxs-lookup"><span data-stu-id="45877-144">-PassThru</span></span>
<span data-ttu-id="45877-145">Cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="45877-145">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="45877-146">Om den här växeln anges returneras det uppdaterade nyckelvärdet.</span><span class="sxs-lookup"><span data-stu-id="45877-146">If this switch is specified, returns the updated key bundle object.</span></span>

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

### <span data-ttu-id="45877-147">-Tagg</span><span class="sxs-lookup"><span data-stu-id="45877-147">-Tag</span></span>
<span data-ttu-id="45877-148">En hash-produkt representerar viktiga taggar.</span><span class="sxs-lookup"><span data-stu-id="45877-148">A hashtable represents key tags.</span></span>
<span data-ttu-id="45877-149">Om det inte anges ändras inte de befintliga taggarna för tangenten.</span><span class="sxs-lookup"><span data-stu-id="45877-149">If not specified, the existings tags of the key remain unchanged.</span></span>

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

### <span data-ttu-id="45877-150">-VaultName</span><span class="sxs-lookup"><span data-stu-id="45877-150">-VaultName</span></span>
<span data-ttu-id="45877-151">Valv namn.</span><span class="sxs-lookup"><span data-stu-id="45877-151">Vault name.</span></span>
<span data-ttu-id="45877-152">Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="45877-152">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="45877-153">-Version</span><span class="sxs-lookup"><span data-stu-id="45877-153">-Version</span></span>
<span data-ttu-id="45877-154">Huvud version.</span><span class="sxs-lookup"><span data-stu-id="45877-154">Key version.</span></span>
<span data-ttu-id="45877-155">Cmdlet konstruerar FQDN för en Key från valv namnet, den valda miljön, namn och huvud version.</span><span class="sxs-lookup"><span data-stu-id="45877-155">Cmdlet constructs the FQDN of a key from vault name, currently selected environment, key name and key version.</span></span>

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

### <span data-ttu-id="45877-156">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="45877-156">-Confirm</span></span>
<span data-ttu-id="45877-157">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="45877-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45877-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45877-158">-WhatIf</span></span>
<span data-ttu-id="45877-159">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="45877-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45877-160">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="45877-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45877-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45877-161">CommonParameters</span></span>
<span data-ttu-id="45877-162">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45877-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45877-163">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="45877-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45877-164">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="45877-164">INPUTS</span></span>

### <span data-ttu-id="45877-165">Microsoft. Azure. commands. valv. Models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="45877-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="45877-166">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="45877-166">OUTPUTS</span></span>

### <span data-ttu-id="45877-167">Microsoft. Azure. commands. valv. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="45877-167">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="45877-168">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="45877-168">NOTES</span></span>

## <span data-ttu-id="45877-169">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="45877-169">RELATED LINKS</span></span>
