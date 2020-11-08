---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzManagedHsmKey.md
ms.openlocfilehash: 79d01f96fe776432f650d827b16ba83f48b84ddd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272268"
---
# <span data-ttu-id="cfc23-101">Update-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="cfc23-101">Update-AzManagedHsmKey</span></span>

## <span data-ttu-id="cfc23-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cfc23-102">SYNOPSIS</span></span>
<span data-ttu-id="cfc23-103">Uppdaterar attributen för en nycklar i en hanterad HSM.</span><span class="sxs-lookup"><span data-stu-id="cfc23-103">Updates the attributes of a key in a managed HSM.</span></span>

## <span data-ttu-id="cfc23-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cfc23-104">SYNTAX</span></span>

### <span data-ttu-id="cfc23-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="cfc23-105">Default (Default)</span></span>
```
Update-AzManagedHsmKey [-HsmName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfc23-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="cfc23-106">InputObject</span></span>
```
Update-AzManagedHsmKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cfc23-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cfc23-107">DESCRIPTION</span></span>
<span data-ttu-id="cfc23-108">Cmdleten **Update-AzManagedHsmKey** uppdaterar den redigerbara attributen för en Key i en hanterad HSM.</span><span class="sxs-lookup"><span data-stu-id="cfc23-108">The **Update-AzManagedHsmKey** cmdlet updates the editable attributes of a key in a managed HSM.</span></span>

## <span data-ttu-id="cfc23-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cfc23-109">EXAMPLES</span></span>

### <span data-ttu-id="cfc23-110">Exempel 1: ändra en post för att aktivera den och ange förfallo datum och-Taggar</span><span class="sxs-lookup"><span data-stu-id="cfc23-110">Example 1: Modify a key to enable it, and set the expiration date and tags</span></span>
```powershell
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = 'true'}
PS C:\> Update-AzManagedHsmKey -HsmName testmhsm -Name testkey001 -Expires $Expires -Enable $True -Tag $Tags -PassThru

Vault/HSM Name : testmhsm
Name           : testkey001
Version        : 49b74a39dab605bd336628dc094dc31b
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey001/49b74a39dab605bd336628dc094dc31b
Enabled        : True
Expires        : 10/14/2022 9:46:55 AM
Not Before     :
Created        : 10/14/2020 3:39:16 AM
Updated        : 10/14/2020 9:47:06 AM
Recovery Level : Recoverable+Purgeable
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="cfc23-111">Det första kommandot skapar ett **datetime** -objekt med hjälp av cmdleten **Get-date** .</span><span class="sxs-lookup"><span data-stu-id="cfc23-111">The first command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="cfc23-112">Detta objekt anger en tid två år framåt i tiden.</span><span class="sxs-lookup"><span data-stu-id="cfc23-112">That object specifies a time two years in the future.</span></span> <span data-ttu-id="cfc23-113">I kommandot lagras datumet i $Expires variabel.</span><span class="sxs-lookup"><span data-stu-id="cfc23-113">The command stores that date in the $Expires variable.</span></span>
<span data-ttu-id="cfc23-114">Om du vill ha mer information skriver du `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="cfc23-114">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="cfc23-115">Det andra kommandot skapar en variabel för att lagra tagg värden med hög allvarlighets grad och redovisning.</span><span class="sxs-lookup"><span data-stu-id="cfc23-115">The second command creates a variable to store tag values of high severity and Accounting.</span></span>
<span data-ttu-id="cfc23-116">Det slutliga kommandot ändrar en tangent som heter testkey001.</span><span class="sxs-lookup"><span data-stu-id="cfc23-116">The final command modifies a key named testkey001.</span></span> <span data-ttu-id="cfc23-117">Med kommandot aktive ras den här knappen, vilket innebär att den upphör att gälla den tid som lagras i $Expires och anger de taggar som lagras i $Tags.</span><span class="sxs-lookup"><span data-stu-id="cfc23-117">The command enables the key, sets its expiration time to the time stored in $Expires, and sets the tags that are stored in $Tags.</span></span>

## <span data-ttu-id="cfc23-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cfc23-118">PARAMETERS</span></span>

### <span data-ttu-id="cfc23-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfc23-119">-DefaultProfile</span></span>
<span data-ttu-id="cfc23-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cfc23-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cfc23-121">-Aktivera</span><span class="sxs-lookup"><span data-stu-id="cfc23-121">-Enable</span></span>
<span data-ttu-id="cfc23-122">Värdet True gör att den här tangenten och värdet false kan komma till.</span><span class="sxs-lookup"><span data-stu-id="cfc23-122">Value of true enables the key and a value of false disabless the key.</span></span>
<span data-ttu-id="cfc23-123">Om det inte anges ändras inte det befintliga aktiverade/inaktiverade läget.</span><span class="sxs-lookup"><span data-stu-id="cfc23-123">If not specified, the existing enabled/disabled state remains unchanged.</span></span>

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

### <span data-ttu-id="cfc23-124">-Upphör</span><span class="sxs-lookup"><span data-stu-id="cfc23-124">-Expires</span></span>
<span data-ttu-id="cfc23-125">Förfallo tid i UTC-tid.</span><span class="sxs-lookup"><span data-stu-id="cfc23-125">The expiration time of a key in UTC time.</span></span>
<span data-ttu-id="cfc23-126">Om det inte anges ändras inte den befintliga förfallo tiden för den gamla.</span><span class="sxs-lookup"><span data-stu-id="cfc23-126">If not specified, the existing expiration time of the key remains unchanged.</span></span>

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

### <span data-ttu-id="cfc23-127">-HsmName</span><span class="sxs-lookup"><span data-stu-id="cfc23-127">-HsmName</span></span>
<span data-ttu-id="cfc23-128">HSM-namn.</span><span class="sxs-lookup"><span data-stu-id="cfc23-128">HSM name.</span></span> <span data-ttu-id="cfc23-129">Cmdlet konstruerar FQDN för en hanterad HSM baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="cfc23-129">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="cfc23-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cfc23-130">-InputObject</span></span>
<span data-ttu-id="cfc23-131">Nyckelvärdet</span><span class="sxs-lookup"><span data-stu-id="cfc23-131">Key object</span></span>

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

### <span data-ttu-id="cfc23-132">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="cfc23-132">-KeyOps</span></span>
<span data-ttu-id="cfc23-133">Vilka operationer som kan utföras med tangenten.</span><span class="sxs-lookup"><span data-stu-id="cfc23-133">The operations that can be performed with the key.</span></span>
<span data-ttu-id="cfc23-134">Om det inte anges förblir de befintliga nycklarnas viktiga operationer oförändrade.</span><span class="sxs-lookup"><span data-stu-id="cfc23-134">If not specified, the existing key operations of the key remain unchanged.</span></span>

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

### <span data-ttu-id="cfc23-135">-Namn</span><span class="sxs-lookup"><span data-stu-id="cfc23-135">-Name</span></span>
<span data-ttu-id="cfc23-136">Namn på knappen.</span><span class="sxs-lookup"><span data-stu-id="cfc23-136">Key name.</span></span>
<span data-ttu-id="cfc23-137">Cmdlet konstruerar FQDN för en Key från Managed HSM-namn, markerat miljö-och namn för tillfället.</span><span class="sxs-lookup"><span data-stu-id="cfc23-137">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment and key name.</span></span>

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

### <span data-ttu-id="cfc23-138">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="cfc23-138">-NotBefore</span></span>
<span data-ttu-id="cfc23-139">UTC-tiden innan den här tangenten kan användas.</span><span class="sxs-lookup"><span data-stu-id="cfc23-139">The UTC time before which key can't be used.</span></span>
<span data-ttu-id="cfc23-140">Om det inte anges ändras inte NotBefore befintliga attribut.</span><span class="sxs-lookup"><span data-stu-id="cfc23-140">If not specified, the existing NotBefore attribute of the key remains unchanged.</span></span>

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

### <span data-ttu-id="cfc23-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cfc23-141">-PassThru</span></span>
<span data-ttu-id="cfc23-142">Cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="cfc23-142">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="cfc23-143">Om den här växeln anges returneras det uppdaterade nyckelvärdet.</span><span class="sxs-lookup"><span data-stu-id="cfc23-143">If this switch is specified, returns the updated key bundle object.</span></span>

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

### <span data-ttu-id="cfc23-144">-Tagg</span><span class="sxs-lookup"><span data-stu-id="cfc23-144">-Tag</span></span>
<span data-ttu-id="cfc23-145">En hash-produkt representerar viktiga taggar.</span><span class="sxs-lookup"><span data-stu-id="cfc23-145">A hashtable represents key tags.</span></span>
<span data-ttu-id="cfc23-146">Om det inte anges ändras inte de befintliga taggarna för tangenten.</span><span class="sxs-lookup"><span data-stu-id="cfc23-146">If not specified, the existings tags of the key remain unchanged.</span></span>

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

### <span data-ttu-id="cfc23-147">-Version</span><span class="sxs-lookup"><span data-stu-id="cfc23-147">-Version</span></span>
<span data-ttu-id="cfc23-148">Huvud version.</span><span class="sxs-lookup"><span data-stu-id="cfc23-148">Key version.</span></span>
<span data-ttu-id="cfc23-149">Cmdlet konstruerar FQDN för en Key från Managed HSM-namn, markerad miljö, namn och viktig version.</span><span class="sxs-lookup"><span data-stu-id="cfc23-149">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment, key name and key version.</span></span>

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

### <span data-ttu-id="cfc23-150">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cfc23-150">-Confirm</span></span>
<span data-ttu-id="cfc23-151">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cfc23-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfc23-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfc23-152">-WhatIf</span></span>
<span data-ttu-id="cfc23-153">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cfc23-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cfc23-154">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cfc23-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfc23-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfc23-155">CommonParameters</span></span>
<span data-ttu-id="cfc23-156">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfc23-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfc23-157">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cfc23-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfc23-158">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cfc23-158">INPUTS</span></span>

### <span data-ttu-id="cfc23-159">Microsoft. Azure. commands. valv. Models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="cfc23-159">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="cfc23-160">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cfc23-160">OUTPUTS</span></span>

### <span data-ttu-id="cfc23-161">Microsoft. Azure. commands. valv. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="cfc23-161">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="cfc23-162">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cfc23-162">NOTES</span></span>

## <span data-ttu-id="cfc23-163">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cfc23-163">RELATED LINKS</span></span>

[<span data-ttu-id="cfc23-164">Add-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="cfc23-164">Add-AzManagedHsmKey</span></span>](./Add-AzManagedHsmKey.md)

[<span data-ttu-id="cfc23-165">Säkerhets kopiering-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="cfc23-165">Backup-AzManagedHsmKey</span></span>](./Backup-AzManagedHsmKey.md)

[<span data-ttu-id="cfc23-166">Remove-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="cfc23-166">Remove-AzManagedHsmKey</span></span>](./Remove-AzManagedHsmKey.md)

[<span data-ttu-id="cfc23-167">Ångra-AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="cfc23-167">Undo-AzManagedHsmKeyRemoval</span></span>](./Undo-AzManagedHsmKeyRemoval.md)

[<span data-ttu-id="cfc23-168">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="cfc23-168">Get-AzManagedHsmKey</span></span>](./Get-AzManagedHsmKey.md)

[<span data-ttu-id="cfc23-169">Återställ-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="cfc23-169">Restore-AzManagedHsmKey</span></span>](./Restore-AzManagedHsmKey.md)