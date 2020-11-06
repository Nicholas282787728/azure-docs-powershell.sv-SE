---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: AE7B103B-23ED-4A66-A0DC-14FB0DF38FA8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurermkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVaultAccessPolicy.md
ms.openlocfilehash: ca175d0873b74d8b13d1755f3d0986580c5853ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579519"
---
# <span data-ttu-id="2117e-101">Remove-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2117e-101">Remove-AzureRmKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="2117e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2117e-102">SYNOPSIS</span></span>
<span data-ttu-id="2117e-103">Tar bort alla behörigheter för en användare eller ett program från ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="2117e-103">Removes all permissions for a user or application from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2117e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2117e-104">SYNTAX</span></span>

### <span data-ttu-id="2117e-105">ByUserPrincipalName (standard)</span><span class="sxs-lookup"><span data-stu-id="2117e-105">ByUserPrincipalName (Default)</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -UserPrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2117e-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="2117e-106">ByObjectId</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2117e-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="2117e-107">ByServicePrincipalName</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2117e-108">ByEmail</span><span class="sxs-lookup"><span data-stu-id="2117e-108">ByEmail</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2117e-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="2117e-109">ForVault</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-EnabledForDeployment] [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2117e-110">InputObjectByObjectId</span><span class="sxs-lookup"><span data-stu-id="2117e-110">InputObjectByObjectId</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ObjectId <String> [-ApplicationId <Guid>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2117e-111">InputObjectByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="2117e-111">InputObjectByServicePrincipalName</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ServicePrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2117e-112">InputObjectByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="2117e-112">InputObjectByUserPrincipalName</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -UserPrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2117e-113">InputObjectByEmail</span><span class="sxs-lookup"><span data-stu-id="2117e-113">InputObjectByEmail</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -EmailAddress <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2117e-114">InputObjectForVault</span><span class="sxs-lookup"><span data-stu-id="2117e-114">InputObjectForVault</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2117e-115">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2117e-115">DESCRIPTION</span></span>
<span data-ttu-id="2117e-116">Cmdleten **Remove-AzureRmKeyVaultAccessPolicy** tar bort alla behörigheter för en användare eller ett program eller för alla användare och program från ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="2117e-116">The **Remove-AzureRmKeyVaultAccessPolicy** cmdlet removes all permissions for a user or application or for all users and applications from a key vault.</span></span>
<span data-ttu-id="2117e-117">Även om du tar bort alla behörigheter kan ägaren av Azure-prenumerationen som innehåller nyckelordet lägga till behörigheter i Key Vault.</span><span class="sxs-lookup"><span data-stu-id="2117e-117">Even if you remove all permissions, the owner of the Azure subscription that contains the key vault can add permissions to the key vault.</span></span>

<span data-ttu-id="2117e-118">Observera att även om resurs gruppen är valfri för denna cmdlet bör du göra det för bättre prestanda.</span><span class="sxs-lookup"><span data-stu-id="2117e-118">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="2117e-119">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2117e-119">EXAMPLES</span></span>

### <span data-ttu-id="2117e-120">Exempel 1: ta bort behörigheter för en användare</span><span class="sxs-lookup"><span data-stu-id="2117e-120">Example 1: Remove permissions for a user</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com'
```

<span data-ttu-id="2117e-121">Det här kommandot tar bort alla behörigheter som en användare PattiFuller@contoso.com har i det nyckelord som heter Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="2117e-121">This command removes all the permissions that a user PattiFuller@contoso.com has on the key vault named Contoso03Vault.</span></span>

### <span data-ttu-id="2117e-122">Exempel 2: ta bort behörigheter för ett program</span><span class="sxs-lookup"><span data-stu-id="2117e-122">Example 2: Remove permissions for an application</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com'
```

<span data-ttu-id="2117e-123">Det här kommandot tar bort alla behörigheter som ett program har i det nyckelord som heter Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="2117e-123">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="2117e-124">I det här exemplet identifieras programmet med hjälp av tjänstens huvud namn som är registrerat i Azure Active Directory http://payroll.contoso.com .</span><span class="sxs-lookup"><span data-stu-id="2117e-124">This example identifies the application by using the service principal name registered in Azure Active Directory, http://payroll.contoso.com.</span></span>

### <span data-ttu-id="2117e-125">Exempel 3: ta bort behörigheter för ett program med dess objekt-ID</span><span class="sxs-lookup"><span data-stu-id="2117e-125">Example 3: Remove permissions for an application by using its object ID</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectID 34595082-9346-41b6-8d6b-295a2808b8db
```

<span data-ttu-id="2117e-126">Det här kommandot tar bort alla behörigheter som ett program har i det nyckelord som heter Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="2117e-126">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="2117e-127">I det här exemplet identifieras programmet av tjänstens objekt-ID.</span><span class="sxs-lookup"><span data-stu-id="2117e-127">This example identifies the application by the object ID of the service principal.</span></span>

### <span data-ttu-id="2117e-128">Exempel 4: ta bort behörigheter för Microsoft. Compute Resource Provider</span><span class="sxs-lookup"><span data-stu-id="2117e-128">Example 4: Remove permissions for the Microsoft.Compute resource provider</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="2117e-129">Det här kommandot tar bort behörigheter för Microsoft. Compute Resource Provider för att få hemligheter från Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="2117e-129">This command removes permission for the Microsoft.Compute resource provider to get secrets from the Contoso03Vault.</span></span>

## <span data-ttu-id="2117e-130">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2117e-130">PARAMETERS</span></span>

### <span data-ttu-id="2117e-131">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="2117e-131">-ApplicationId</span></span>
<span data-ttu-id="2117e-132">Anger ID för programmet vars behörigheter ska tas bort</span><span class="sxs-lookup"><span data-stu-id="2117e-132">Specifies the ID of application whose permissions should be removed</span></span>

```yaml
Type: Guid
Parameter Sets: ByObjectId, InputObjectByObjectId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2117e-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2117e-133">-DefaultProfile</span></span>
<span data-ttu-id="2117e-134">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="2117e-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2117e-135">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="2117e-135">-EmailAddress</span></span>
<span data-ttu-id="2117e-136">Anger användarens e-postadress för den användare vars åtkomst du vill ta bort.</span><span class="sxs-lookup"><span data-stu-id="2117e-136">Specifies the user email address of the user whose access you want to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByEmail, InputObjectByEmail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2117e-137">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="2117e-137">-EnabledForDeployment</span></span>
<span data-ttu-id="2117e-138">Om du anger det här alternativet inaktive ras hämtning av hemligheter från det här nyckelordet av Microsoft. Compute Resource Provider när den refereras i skapa resurs.</span><span class="sxs-lookup"><span data-stu-id="2117e-138">If specified, disables the retrieval of secrets from this key vault by the Microsoft.Compute resource provider when referenced in resource creation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault, InputObjectForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2117e-139">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="2117e-139">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="2117e-140">Om det här alternativet anges inaktiverar hämtning av hemligheter från den här nyckeln för Azure Disk Encryption.</span><span class="sxs-lookup"><span data-stu-id="2117e-140">If specified, disables the retrieval of secrets from this key vault by Azure Disk Encryption.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault, InputObjectForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2117e-141">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="2117e-141">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="2117e-142">Om det här alternativet anges inaktiverar hämtning av hemligheter från det här nyckelordet av Azure Resource Manager när den refereras till i mallar.</span><span class="sxs-lookup"><span data-stu-id="2117e-142">If specified, disables the retrieval of secrets from this key vault by Azure Resource Manager when referenced in templates.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault, InputObjectForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2117e-143">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2117e-143">-InputObject</span></span>
<span data-ttu-id="2117e-144">Key valv-objekt.</span><span class="sxs-lookup"><span data-stu-id="2117e-144">Key Vault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmail, InputObjectForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2117e-145">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="2117e-145">-ObjectId</span></span>
<span data-ttu-id="2117e-146">Anger objekt-ID: t för användaren eller tjänstens huvud namn i Azure Active Directory som du vill ta bort behörigheter för.</span><span class="sxs-lookup"><span data-stu-id="2117e-146">Specifies the object ID of the user or service principal in Azure Active Directory for which to remove permissions.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectId, InputObjectByObjectId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2117e-147">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2117e-147">-PassThru</span></span>
<span data-ttu-id="2117e-148">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="2117e-148">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2117e-149">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="2117e-149">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2117e-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2117e-150">-ResourceGroupName</span></span>
<span data-ttu-id="2117e-151">Anger namnet på den resurs grupp som är kopplad till det huvud valv vars åtkomst princip ändras.</span><span class="sxs-lookup"><span data-stu-id="2117e-151">Specifies the name of the resource group associated with the key vault whose access policy is being modified.</span></span>
<span data-ttu-id="2117e-152">Om det inte anges söker denna cmdlet efter det viktigaste valvet i den aktuella prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="2117e-152">If not specified, this cmdlet searches for the key vault in the current subscription.</span></span>

```yaml
Type: String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmail, ForVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2117e-153">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="2117e-153">-ServicePrincipalName</span></span>
<span data-ttu-id="2117e-154">Anger huvud namnet på den tillämpning vars behörigheter du vill ta bort.</span><span class="sxs-lookup"><span data-stu-id="2117e-154">Specifies the service principal name of the application whose permissions you want to remove.</span></span>
<span data-ttu-id="2117e-155">Ange program-ID, som också kallas klient-ID, för programmet i Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2117e-155">Specify the application ID, also known as client ID, registered for the application in Azure Active Directory.</span></span>

```yaml
Type: String
Parameter Sets: ByServicePrincipalName, InputObjectByServicePrincipalName
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2117e-156">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="2117e-156">-UserPrincipalName</span></span>
<span data-ttu-id="2117e-157">Anger användarens huvud namn för den användare vars åtkomst du vill ta bort.</span><span class="sxs-lookup"><span data-stu-id="2117e-157">Specifies the user principal name of the user whose access you want to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByUserPrincipalName, InputObjectByUserPrincipalName
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2117e-158">-VaultName</span><span class="sxs-lookup"><span data-stu-id="2117e-158">-VaultName</span></span>
<span data-ttu-id="2117e-159">Anger namnet på Key-valvet.</span><span class="sxs-lookup"><span data-stu-id="2117e-159">Specifies the name of the key vault.</span></span>
<span data-ttu-id="2117e-160">Denna cmdlet tar bort behörigheter för det Key-valv som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="2117e-160">This cmdlet removes permissions for the key vault that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmail, ForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2117e-161">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2117e-161">-Confirm</span></span>
<span data-ttu-id="2117e-162">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2117e-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2117e-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2117e-163">-WhatIf</span></span>
<span data-ttu-id="2117e-164">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2117e-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2117e-165">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2117e-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2117e-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2117e-166">CommonParameters</span></span>
<span data-ttu-id="2117e-167">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2117e-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2117e-168">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2117e-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2117e-169">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2117e-169">INPUTS</span></span>

### <span data-ttu-id="2117e-170">Ingen</span><span class="sxs-lookup"><span data-stu-id="2117e-170">None</span></span>
<span data-ttu-id="2117e-171">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="2117e-171">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2117e-172">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2117e-172">OUTPUTS</span></span>

### <span data-ttu-id="2117e-173">Microsoft. Azure. commands. valv. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="2117e-173">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="2117e-174">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2117e-174">NOTES</span></span>

## <span data-ttu-id="2117e-175">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2117e-175">RELATED LINKS</span></span>

[<span data-ttu-id="2117e-176">Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2117e-176">Set-AzureRmKeyVaultAccessPolicy</span></span>](./Set-AzureRmKeyVaultAccessPolicy.md)

