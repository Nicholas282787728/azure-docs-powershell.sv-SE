---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: AE7B103B-23ED-4A66-A0DC-14FB0DF38FA8
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-Azkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultAccessPolicy.md
ms.openlocfilehash: f5cd00e0ef8e8936a4c87ee313054ae4c084a879
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/08/2020
ms.locfileid: "93931621"
---
# <span data-ttu-id="b7d65-101">Remove-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b7d65-101">Remove-AzKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="b7d65-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b7d65-102">SYNOPSIS</span></span>
<span data-ttu-id="b7d65-103">Tar bort alla behörigheter för en användare eller ett program från ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="b7d65-103">Removes all permissions for a user or application from a key vault.</span></span>

## <span data-ttu-id="b7d65-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b7d65-104">SYNTAX</span></span>

### <span data-ttu-id="b7d65-105">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="b7d65-105">ByServicePrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b7d65-106">ByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="b7d65-106">ByUserPrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -UserPrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b7d65-107">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="b7d65-107">ByObjectId</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b7d65-108">ByEmail</span><span class="sxs-lookup"><span data-stu-id="b7d65-108">ByEmail</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7d65-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="b7d65-109">ForVault</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-EnabledForDeployment] [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7d65-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b7d65-110">DESCRIPTION</span></span>
<span data-ttu-id="b7d65-111">Cmdleten **Remove-AzKeyVaultAccessPolicy** tar bort alla behörigheter för en användare eller ett program eller för alla användare och program från ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="b7d65-111">The **Remove-AzKeyVaultAccessPolicy** cmdlet removes all permissions for a user or application or for all users and applications from a key vault.</span></span>
<span data-ttu-id="b7d65-112">Även om du tar bort alla behörigheter kan ägaren av Azure-prenumerationen som innehåller nyckelordet lägga till behörigheter i Key Vault.</span><span class="sxs-lookup"><span data-stu-id="b7d65-112">Even if you remove all permissions, the owner of the Azure subscription that contains the key vault can add permissions to the key vault.</span></span>

<span data-ttu-id="b7d65-113">Observera att även om resurs gruppen är valfri för denna cmdlet bör du göra det för bättre prestanda.</span><span class="sxs-lookup"><span data-stu-id="b7d65-113">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="b7d65-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b7d65-114">EXAMPLES</span></span>

### <span data-ttu-id="b7d65-115">Exempel 1: ta bort behörigheter för en användare</span><span class="sxs-lookup"><span data-stu-id="b7d65-115">Example 1: Remove permissions for a user</span></span>
```
PS C:\>Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com'
```

<span data-ttu-id="b7d65-116">Det här kommandot tar bort alla behörigheter som en användare PattiFuller@contoso.com har i det nyckelord som heter Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="b7d65-116">This command removes all the permissions that a user PattiFuller@contoso.com has on the key vault named Contoso03Vault.</span></span>

### <span data-ttu-id="b7d65-117">Exempel 2: ta bort behörigheter för ett program</span><span class="sxs-lookup"><span data-stu-id="b7d65-117">Example 2: Remove permissions for an application</span></span>
```
PS C:\>Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com'
```

<span data-ttu-id="b7d65-118">Det här kommandot tar bort alla behörigheter som ett program har i det nyckelord som heter Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="b7d65-118">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="b7d65-119">I det här exemplet identifieras programmet med hjälp av tjänstens huvud namn som är registrerat i Azure Active Directory `http://payroll.contoso.com` .</span><span class="sxs-lookup"><span data-stu-id="b7d65-119">This example identifies the application by using the service principal name registered in Azure Active Directory, `http://payroll.contoso.com`.</span></span>

### <span data-ttu-id="b7d65-120">Exempel 3: ta bort behörigheter för ett program med dess objekt-ID</span><span class="sxs-lookup"><span data-stu-id="b7d65-120">Example 3: Remove permissions for an application by using its object ID</span></span>
```
PS C:\>Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectID 34595082-9346-41b6-8d6b-295a2808b8db
```

<span data-ttu-id="b7d65-121">Det här kommandot tar bort alla behörigheter som ett program har i det nyckelord som heter Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="b7d65-121">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="b7d65-122">I det här exemplet identifieras programmet av tjänstens objekt-ID.</span><span class="sxs-lookup"><span data-stu-id="b7d65-122">This example identifies the application by the object ID of the service principal.</span></span>

### <span data-ttu-id="b7d65-123">Exempel 4: ta bort behörigheter för Microsoft. Compute Resource Provider</span><span class="sxs-lookup"><span data-stu-id="b7d65-123">Example 4: Remove permissions for the Microsoft.Compute resource provider</span></span>
```
PS C:\>Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="b7d65-124">Det här kommandot tar bort behörigheter för Microsoft. Compute Resource Provider för att få hemligheter från Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="b7d65-124">This command removes permission for the Microsoft.Compute resource provider to get secrets from the Contoso03Vault.</span></span>

## <span data-ttu-id="b7d65-125">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b7d65-125">PARAMETERS</span></span>

### <span data-ttu-id="b7d65-126">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="b7d65-126">-ApplicationId</span></span>
<span data-ttu-id="b7d65-127">För framtida användning.</span><span class="sxs-lookup"><span data-stu-id="b7d65-127">For future use.</span></span>

```yaml
Type: Guid
Parameter Sets: ByObjectId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7d65-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7d65-128">-DefaultProfile</span></span>
<span data-ttu-id="b7d65-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="b7d65-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b7d65-130">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="b7d65-130">-EmailAddress</span></span>
<span data-ttu-id="b7d65-131">Anger användarens e-postadress för den användare vars åtkomst du vill ta bort.</span><span class="sxs-lookup"><span data-stu-id="b7d65-131">Specifies the user email address of the user whose access you want to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByEmail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7d65-132">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="b7d65-132">-EnabledForDeployment</span></span>
<span data-ttu-id="b7d65-133">Gör det möjligt för Microsoft. Compute Resource-leverantören att hämta hemligheter från det här nyckelvärdet när det här nyckelvärdet refereras i resurs skapande, till exempel när du skapar en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="b7d65-133">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7d65-134">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="b7d65-134">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="b7d65-135">Aktiverar tjänsten Azure Disk Encryption för att få hemligheter och unwrap-nycklar från det här nyckel valvet.</span><span class="sxs-lookup"><span data-stu-id="b7d65-135">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7d65-136">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="b7d65-136">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="b7d65-137">Gör det möjligt för Azure Resource Manager att få hemligheter från detta viktiga valv när det här nyckelvärdet refereras till i en mall.</span><span class="sxs-lookup"><span data-stu-id="b7d65-137">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7d65-138">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="b7d65-138">-ObjectId</span></span>
<span data-ttu-id="b7d65-139">Anger objekt-ID: t för användaren eller tjänstens huvud namn i Azure Active Directory som du vill ta bort behörigheter för.</span><span class="sxs-lookup"><span data-stu-id="b7d65-139">Specifies the object ID of the user or service principal in Azure Active Directory for which to remove permissions.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7d65-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b7d65-140">-PassThru</span></span>
<span data-ttu-id="b7d65-141">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="b7d65-141">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b7d65-142">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="b7d65-142">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b7d65-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7d65-143">-ResourceGroupName</span></span>
<span data-ttu-id="b7d65-144">Anger namnet på den resurs grupp som är kopplad till det huvud valv vars åtkomst princip ändras.</span><span class="sxs-lookup"><span data-stu-id="b7d65-144">Specifies the name of the resource group associated with the key vault whose access policy is being modified.</span></span>
<span data-ttu-id="b7d65-145">Om det inte anges söker denna cmdlet efter det viktigaste valvet i den aktuella prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="b7d65-145">If not specified, this cmdlet searches for the key vault in the current subscription.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7d65-146">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="b7d65-146">-ServicePrincipalName</span></span>
<span data-ttu-id="b7d65-147">Anger huvud namnet på den tillämpning vars behörigheter du vill ta bort.</span><span class="sxs-lookup"><span data-stu-id="b7d65-147">Specifies the service principal name of the application whose permissions you want to remove.</span></span>
<span data-ttu-id="b7d65-148">Ange program-ID, som också kallas klient-ID, för programmet i Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b7d65-148">Specify the application ID, also known as client ID, registered for the application in Azure Active Directory.</span></span>

```yaml
Type: String
Parameter Sets: ByServicePrincipalName
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7d65-149">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="b7d65-149">-UserPrincipalName</span></span>
<span data-ttu-id="b7d65-150">Anger användarens huvud namn för den användare vars åtkomst du vill ta bort.</span><span class="sxs-lookup"><span data-stu-id="b7d65-150">Specifies the user principal name of the user whose access you want to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByUserPrincipalName
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7d65-151">-VaultName</span><span class="sxs-lookup"><span data-stu-id="b7d65-151">-VaultName</span></span>
<span data-ttu-id="b7d65-152">Anger namnet på Key-valvet.</span><span class="sxs-lookup"><span data-stu-id="b7d65-152">Specifies the name of the key vault.</span></span>
<span data-ttu-id="b7d65-153">Denna cmdlet tar bort behörigheter för det Key-valv som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="b7d65-153">This cmdlet removes permissions for the key vault that this parameter specifies.</span></span>

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

### <span data-ttu-id="b7d65-154">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b7d65-154">-Confirm</span></span>
<span data-ttu-id="b7d65-155">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b7d65-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7d65-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7d65-156">-WhatIf</span></span>
<span data-ttu-id="b7d65-157">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b7d65-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7d65-158">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b7d65-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7d65-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7d65-159">CommonParameters</span></span>
<span data-ttu-id="b7d65-160">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7d65-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7d65-161">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7d65-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7d65-162">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b7d65-162">INPUTS</span></span>

### <span data-ttu-id="b7d65-163">Ingen</span><span class="sxs-lookup"><span data-stu-id="b7d65-163">None</span></span>
<span data-ttu-id="b7d65-164">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="b7d65-164">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b7d65-165">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b7d65-165">OUTPUTS</span></span>

### <span data-ttu-id="b7d65-166">Microsoft. Azure. commands. valv. Models. PSVault</span><span class="sxs-lookup"><span data-stu-id="b7d65-166">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

## <span data-ttu-id="b7d65-167">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b7d65-167">NOTES</span></span>

## <span data-ttu-id="b7d65-168">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b7d65-168">RELATED LINKS</span></span>

[<span data-ttu-id="b7d65-169">Set-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b7d65-169">Set-AzKeyVaultAccessPolicy</span></span>](./Set-AzKeyVaultAccessPolicy.md)

