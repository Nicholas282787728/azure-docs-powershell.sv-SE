---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 636FAD5B-8C39-4E5C-8978-6845C6B89BC0
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/set-Azkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
ms.openlocfilehash: a774c438f9be25dc55f48c5121031956374a2cb7
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94100599"
---
# <span data-ttu-id="d8999-101">Set-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d8999-101">Set-AzKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="d8999-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d8999-102">SYNOPSIS</span></span>
<span data-ttu-id="d8999-103">Tilldelar eller ändrar befintliga behörigheter för en användare, program eller säkerhets grupp för att utföra operationer med ett Key-valv.</span><span class="sxs-lookup"><span data-stu-id="d8999-103">Grants or modifies existing permissions for a user, application, or security group to perform operations with a key vault.</span></span>

## <span data-ttu-id="d8999-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d8999-104">SYNTAX</span></span>

### <span data-ttu-id="d8999-105">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="d8999-105">ByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8999-106">ByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="d8999-106">ByUserPrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -UserPrincipalName <String> [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8999-107">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="d8999-107">ByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8999-108">ByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="d8999-108">ByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d8999-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="d8999-109">ForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8999-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d8999-110">DESCRIPTION</span></span>
<span data-ttu-id="d8999-111">Cmdleten **set-AzKeyVaultAccessPolicy** beviljar eller ändrar befintliga behörigheter för en användare, program eller säkerhets grupp för att utföra de angivna åtgärderna med ett Key-valv.</span><span class="sxs-lookup"><span data-stu-id="d8999-111">The **Set-AzKeyVaultAccessPolicy** cmdlet grants or modifies existing permissions for a user, application, or security group to perform the specified operations with a key vault.</span></span> <span data-ttu-id="d8999-112">De behörigheter som andra användare, program eller säkerhets grupper har i Key-valvet ändras inte.</span><span class="sxs-lookup"><span data-stu-id="d8999-112">It does not modify the permissions that other users, applications, or security groups have on the key vault.</span></span>

<span data-ttu-id="d8999-113">Om du anger behörigheter för en säkerhets grupp påverkar den här åtgärden endast användare i den säkerhets gruppen.</span><span class="sxs-lookup"><span data-stu-id="d8999-113">If you are setting permissions for a security group, this operation affects only users in that security group.</span></span>

<span data-ttu-id="d8999-114">Följande kataloger måste vara samma Azure-katalog:</span><span class="sxs-lookup"><span data-stu-id="d8999-114">The following directories must all be the same Azure directory:</span></span>
- <span data-ttu-id="d8999-115">Standard katalogen för Azure-abonnemanget som Key-valvet finns i.</span><span class="sxs-lookup"><span data-stu-id="d8999-115">The default directory of the Azure subscription in which the key vault resides.</span></span>
- <span data-ttu-id="d8999-116">Den Azure-katalog som innehåller den användare eller program grupp som du beviljar behörigheter till.</span><span class="sxs-lookup"><span data-stu-id="d8999-116">The Azure directory that contains the user or application group that you are granting permissions to.</span></span>

<span data-ttu-id="d8999-117">Exempel på scenarier om dessa villkor inte uppfylls och denna cmdlet inte fungerar:</span><span class="sxs-lookup"><span data-stu-id="d8999-117">Examples of scenarios when these conditions are not met and this cmdlet will not work are:</span></span>

- <span data-ttu-id="d8999-118">Att auktorisera en användare från en annan organisation för att hantera ditt nyckeltal.</span><span class="sxs-lookup"><span data-stu-id="d8999-118">Authorizing a user from a different organization to manage your key vault.</span></span>
<span data-ttu-id="d8999-119">Varje organisation har sin egen katalog.</span><span class="sxs-lookup"><span data-stu-id="d8999-119">Each organization has its own directory.</span></span>
- <span data-ttu-id="d8999-120">Ditt Azure-konto har flera kataloger.</span><span class="sxs-lookup"><span data-stu-id="d8999-120">Your Azure account has multiple directories.</span></span>
<span data-ttu-id="d8999-121">Om du registrerar ett program i en annan katalog än standard katalogen kan du inte auktorisera att programmet kan använda ditt nyckeltal.</span><span class="sxs-lookup"><span data-stu-id="d8999-121">If you register an application in a directory other than the default directory, you cannot authorize that application to use your key vault.</span></span>
<span data-ttu-id="d8999-122">Programmet måste finnas i standard katalogen.</span><span class="sxs-lookup"><span data-stu-id="d8999-122">The application must be in the default directory.</span></span>

<span data-ttu-id="d8999-123">Observera att även om resurs gruppen är valfri för denna cmdlet bör du göra det för bättre prestanda.</span><span class="sxs-lookup"><span data-stu-id="d8999-123">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="d8999-124">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d8999-124">EXAMPLES</span></span>

### <span data-ttu-id="d8999-125">Exempel 1: bevilja behörigheter till en användare för ett nyckeltal och ändra behörigheterna</span><span class="sxs-lookup"><span data-stu-id="d8999-125">Example 1: Grant permissions to a user for a key vault and modify the permissions</span></span>
```
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys create,import,delete,list -PermissionsToSecrets set,delete
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets set,delete,get -PassThru
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys @() -PassThru
```

<span data-ttu-id="d8999-126">Det första kommandot tilldelar behörigheter för en användare i din Azure Active Directory, PattiFuller@contoso.com för att utföra operationer på nycklar och hemligheter med en nyckel valv med namnet Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="d8999-126">The first command grants permissions for a user in your Azure Active Directory, PattiFuller@contoso.com, to perform operations on keys and secrets with a key vault named Contoso03Vault.</span></span>

<span data-ttu-id="d8999-127">Det andra kommandot ändrar de behörigheter som beviljats PattiFuller@contoso.com i det första kommandot för att nu tillåta att hemligheter läggs till för att lägga till och ta bort dem.</span><span class="sxs-lookup"><span data-stu-id="d8999-127">The second command modifies the permissions that were granted to PattiFuller@contoso.com in the first command, to now allow getting secrets in addition to setting and deleting them.</span></span> <span data-ttu-id="d8999-128">Behörigheten för viktiga operationer är oförändrad efter det här kommandot.</span><span class="sxs-lookup"><span data-stu-id="d8999-128">The permissions to key operations remain unchanged after this command.</span></span> <span data-ttu-id="d8999-129">Parametern *Passthru* ger det uppdaterade objektet som returneras av cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d8999-129">The *PassThru* parameter results in the updated object being returned by the cmdlet.</span></span>

<span data-ttu-id="d8999-130">Med kommandot slut ändrar du ytterligare behörigheter för PattiFuller@contoso.com att ta bort alla behörigheter för viktiga operationer.</span><span class="sxs-lookup"><span data-stu-id="d8999-130">The final command further modifies the existing permissions for PattiFuller@contoso.com to remove all permissions to key operations.</span></span> <span data-ttu-id="d8999-131">Behörigheterna till hemliga funktioner ändras inte efter det här kommandot.</span><span class="sxs-lookup"><span data-stu-id="d8999-131">The permissions to secret operations remain unchanged after this command.</span></span> <span data-ttu-id="d8999-132">Parametern *Passthru* ger det uppdaterade objektet som returneras av cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d8999-132">The *PassThru* parameter results in the updated object being returned by the cmdlet.</span></span>

### <span data-ttu-id="d8999-133">Exempel 2: bevilja behörigheter för en program tjänst för att läsa och skriva hemligheter</span><span class="sxs-lookup"><span data-stu-id="d8999-133">Example 2: Grant permissions for an application service principal to read and write secrets</span></span>
```
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com' -PermissionsToSecrets Get,Set
```

<span data-ttu-id="d8999-134">Det här kommandot ger behörighet till ett program för ett nyckeltal med namnet Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="d8999-134">This command grants permissions for an application for a key vault named Contoso03Vault.</span></span>

<span data-ttu-id="d8999-135">Parametern *servicePrincipalName* anger programmet.</span><span class="sxs-lookup"><span data-stu-id="d8999-135">The *ServicePrincipalName* parameter specifies the application.</span></span> <span data-ttu-id="d8999-136">Programmet måste vara registrerat i din Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d8999-136">The application must be registered in your Azure Active Directory.</span></span> <span data-ttu-id="d8999-137">Värdet för parametern *servicePrincipalName* måste vara antingen tjänstens huvud namn eller GUID för programmets ID.</span><span class="sxs-lookup"><span data-stu-id="d8999-137">The value of the *ServicePrincipalName* parameter must be either the service principal name of the application or the application ID GUID.</span></span>

<span data-ttu-id="d8999-138">I det här exemplet anges tjänstens huvud namn `http://payroll.contoso.com` och kommandot ger behörighet att läsa och skriva hemligheter.</span><span class="sxs-lookup"><span data-stu-id="d8999-138">This example specifies the service principal name `http://payroll.contoso.com`, and the command grants the application permissions to read and write secrets.</span></span>

### <span data-ttu-id="d8999-139">Exempel 3: bevilja behörigheter för ett program med dess objekt-ID</span><span class="sxs-lookup"><span data-stu-id="d8999-139">Example 3: Grant permissions for an application using its object ID</span></span>
```
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectId 34595082-9346-41b6-8d6b-295a2808b8db -PermissionsToSecrets Get,Set
```

<span data-ttu-id="d8999-140">Det här kommandot ger behörighet att läsa och skriva hemligheter.</span><span class="sxs-lookup"><span data-stu-id="d8999-140">This command grants the application permissions to read and write secrets.</span></span>

<span data-ttu-id="d8999-141">I det här exemplet anges programmet med objekt-ID för tjänstens huvud program.</span><span class="sxs-lookup"><span data-stu-id="d8999-141">This example specifies the application using the object ID of the service principal of the application.</span></span>

### <span data-ttu-id="d8999-142">Exempel 4: bevilja behörigheter för ett huvud namn för användare</span><span class="sxs-lookup"><span data-stu-id="d8999-142">Example 4: Grant permissions for a user principal name</span></span>
```
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets Get,List,Set
```

<span data-ttu-id="d8999-143">Det här kommandot tilldelar behörigheterna get, list och Set för det angivna UPN-namnet för åtkomst till hemligheter.</span><span class="sxs-lookup"><span data-stu-id="d8999-143">This command grants get, list, and set permissions for the specified user principal name for access to secrets.</span></span>

### <span data-ttu-id="d8999-144">Exempel 5: Aktivera att hemligheter kan hämtas från ett Key valv valv av Microsoft. Compute Resource Provider</span><span class="sxs-lookup"><span data-stu-id="d8999-144">Example 5: Enable secrets to be retrieved from a key vault vault by the Microsoft.Compute resource provider</span></span>
```
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="d8999-145">Det här kommandot ger behörighet att hämta hemligheter från Contoso03Vault Key Vault av Microsoft. Compute Resource Provider.</span><span class="sxs-lookup"><span data-stu-id="d8999-145">This command grants the permissions for secrets to be retrieved from the Contoso03Vault key vault by the Microsoft.Compute resource provider.</span></span>

### <span data-ttu-id="d8999-146">Exempel 6: bevilja behörigheter till en säkerhets grupp</span><span class="sxs-lookup"><span data-stu-id="d8999-146">Example 6: Grant permissions to a security group</span></span>
```
PS C:\>Get-AzADGroup
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'myownvault' -ObjectId (Get-AzADGroup -SearchString 'group2')[0].Id -PermissionsToKeys All -PermissionsToSecrets All
DisplayName                    Type                           ObjectId
-----------                    ----                           --------
group1                                                        96a0daa6-9841-4a9c-bdeb-e7062276c688
group2                                                        b8a401eb-63ad-4a30-b0e1-a7461969fe54
group3                                                        da07a6be-2c1e-4e42-934d-ceb57cf652b4
```

<span data-ttu-id="d8999-147">I det första kommandot används cmdleten Get-AzADGroup för att hämta alla Active Directory-grupper.</span><span class="sxs-lookup"><span data-stu-id="d8999-147">The first command uses the Get-AzADGroup cmdlet to get all Active Directory groups.</span></span> <span data-ttu-id="d8999-148">Från utdata ser du 3 grupper som returneras, med namnet **Grupp1** , **group2** och **Group3**.</span><span class="sxs-lookup"><span data-stu-id="d8999-148">From the output, you see 3 groups returned, named **group1** , **group2** , and **group3**.</span></span> <span data-ttu-id="d8999-149">Flera grupper kan ha samma namn men alltid har ett unikt ObjectId.</span><span class="sxs-lookup"><span data-stu-id="d8999-149">Multiple groups can have the same name but always have a unique ObjectId.</span></span> <span data-ttu-id="d8999-150">Om fler än en grupp med samma namn returneras använder du ObjectId i utdata för att identifiera den du vill använda.</span><span class="sxs-lookup"><span data-stu-id="d8999-150">When more than one group that has the same name is returned, use the ObjectId in the output to identify the one you want to use.</span></span>

<span data-ttu-id="d8999-151">Du kan sedan använda kommandots utdata med Set-AzKeyVaultAccessPolicy om du vill ge behörighet till group2 för ditt nyckeltal, med namnet **myownvault**.</span><span class="sxs-lookup"><span data-stu-id="d8999-151">You then use the output of this command with Set-AzKeyVaultAccessPolicy to grant permissions to group2 for your key vault, named **myownvault**.</span></span> <span data-ttu-id="d8999-152">I det här exemplet räknas grupperna ' group2 ' in i samma kommando rad.</span><span class="sxs-lookup"><span data-stu-id="d8999-152">This example enumerates the groups named 'group2' inline in the same command line.</span></span>

<span data-ttu-id="d8999-153">Det kan finnas flera grupper i den returnerade listan som heter ' group2 '.</span><span class="sxs-lookup"><span data-stu-id="d8999-153">There may be multiple groups in the returned list that are named 'group2'.</span></span>
<span data-ttu-id="d8999-154">I det här exemplet plockas den första, som anges med index \[ 0 \] i den returnerade listan.</span><span class="sxs-lookup"><span data-stu-id="d8999-154">This example picks the first one, indicated by index \[0\] in the returned list.</span></span>

### <span data-ttu-id="d8999-155">Exempel 7: bevilja åtkomst för Azure information Protection till kund hanterad klient organisation (BYOK)</span><span class="sxs-lookup"><span data-stu-id="d8999-155">Example 7: Grant Azure Information Protection access to the customer-managed tenant key (BYOK)</span></span>
```
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName 'Contoso04Vault' -ServicePrincipalName 00000012-0000-0000-c000-000000000000 -PermissionsToKeys decrypt,sign,get
```

<span data-ttu-id="d8999-156">Det här kommandot auktoriserar Azure information Protection att använda en kundhanterad knapp (skapa en egen-eller "BYOK"-scenario) som klient organisations-knappen för Azure information Protection.</span><span class="sxs-lookup"><span data-stu-id="d8999-156">This command authorizes Azure Information Protection to use a customer-managed key (the bring your own key, or "BYOK" scenario) as the Azure Information Protection tenant key.</span></span>

<span data-ttu-id="d8999-157">När du kör det här kommandot ska du ange ditt eget namn på Key Vault, men du måste ange parametern *servicePrincipalName* med GUID **00000012-0000-0000-C000-000000000000** och ange behörigheterna i exemplet.</span><span class="sxs-lookup"><span data-stu-id="d8999-157">When you run this command, specify your own key vault name but you must specify the *ServicePrincipalName* parameter with the GUID **00000012-0000-0000-c000-000000000000** and specify the permissions in the example.</span></span>

## <span data-ttu-id="d8999-158">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d8999-158">PARAMETERS</span></span>

### <span data-ttu-id="d8999-159">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="d8999-159">-ApplicationId</span></span>
<span data-ttu-id="d8999-160">För framtida användning.</span><span class="sxs-lookup"><span data-stu-id="d8999-160">For future use.</span></span>

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

### <span data-ttu-id="d8999-161">-BypassObjectIdValidation</span><span class="sxs-lookup"><span data-stu-id="d8999-161">-BypassObjectIdValidation</span></span>
<span data-ttu-id="d8999-162">Gör det möjligt att ange ett objekt-ID utan att verifiera att objektet finns i Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d8999-162">Enables you to specify an object ID without validating that the object exists in Azure Active Directory.</span></span>

<span data-ttu-id="d8999-163">Använd endast den här parametern om du vill bevilja åtkomst till ditt nyckeltal till ett objekt-ID som refererar till en delegerad säkerhets grupp från en annan Azure-klient.</span><span class="sxs-lookup"><span data-stu-id="d8999-163">Use this parameter only if you want to grant access to your key vault to an object ID that refers to a delegated security group from another Azure tenant.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByObjectId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8999-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8999-164">-DefaultProfile</span></span>
<span data-ttu-id="d8999-165">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d8999-165">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d8999-166">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="d8999-166">-EmailAddress</span></span>
<span data-ttu-id="d8999-167">Anger användarens e-postadress för den användare som ska bevilja behörigheter.</span><span class="sxs-lookup"><span data-stu-id="d8999-167">Specifies the user email address of the user to whom to grant permissions.</span></span>

<span data-ttu-id="d8999-168">Den här e-postadressen måste finnas i katalogen som är kopplad till det aktuella abonnemanget och vara unik.</span><span class="sxs-lookup"><span data-stu-id="d8999-168">This email address must exist in the directory associated with the current subscription and be unique.</span></span>

```yaml
Type: String
Parameter Sets: ByEmailAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8999-169">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="d8999-169">-EnabledForDeployment</span></span>
<span data-ttu-id="d8999-170">Gör det möjligt för Microsoft. Compute Resource-leverantören att hämta hemligheter från det här nyckelvärdet när det här nyckelvärdet refereras i resurs skapande, till exempel när du skapar en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="d8999-170">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

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

### <span data-ttu-id="d8999-171">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="d8999-171">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="d8999-172">Aktiverar tjänsten Azure Disk Encryption för att få hemligheter och unwrap-nycklar från det här nyckel valvet.</span><span class="sxs-lookup"><span data-stu-id="d8999-172">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

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

### <span data-ttu-id="d8999-173">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="d8999-173">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="d8999-174">Gör det möjligt för Azure Resource Manager att få hemligheter från detta viktiga valv när det här nyckelvärdet refereras till i en mall.</span><span class="sxs-lookup"><span data-stu-id="d8999-174">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

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

### <span data-ttu-id="d8999-175">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="d8999-175">-ObjectId</span></span>
<span data-ttu-id="d8999-176">Anger objekt-ID: t för användaren eller tjänstens huvud namn i Azure Active Directory för vilket behörigheter ska beviljas.</span><span class="sxs-lookup"><span data-stu-id="d8999-176">Specifies the object ID of the user or service principal in Azure Active Directory for which to grant permissions.</span></span>

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

### <span data-ttu-id="d8999-177">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d8999-177">-PassThru</span></span>
<span data-ttu-id="d8999-178">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="d8999-178">Returns an object representing the item with which you are working.</span></span>

<span data-ttu-id="d8999-179">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="d8999-179">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d8999-180">-PermissionsToCertificates</span><span class="sxs-lookup"><span data-stu-id="d8999-180">-PermissionsToCertificates</span></span>
<span data-ttu-id="d8999-181">Anger en matris med certifikat behörigheter som ska beviljas till en användare eller tjänstens huvud konto.</span><span class="sxs-lookup"><span data-stu-id="d8999-181">Specifies an array of certificate permissions to grant to a user or service principal.</span></span>

<span data-ttu-id="d8999-182">De acceptabla värdena för den här parametern:</span><span class="sxs-lookup"><span data-stu-id="d8999-182">The acceptable values for this parameter:</span></span>

- <span data-ttu-id="d8999-183">Lära</span><span class="sxs-lookup"><span data-stu-id="d8999-183">Get</span></span>
- <span data-ttu-id="d8999-184">Förteckning</span><span class="sxs-lookup"><span data-stu-id="d8999-184">List</span></span>
- <span data-ttu-id="d8999-185">Ta bort</span><span class="sxs-lookup"><span data-stu-id="d8999-185">Delete</span></span>
- <span data-ttu-id="d8999-186">Göra</span><span class="sxs-lookup"><span data-stu-id="d8999-186">Create</span></span>
- <span data-ttu-id="d8999-187">Importeras</span><span class="sxs-lookup"><span data-stu-id="d8999-187">Import</span></span>
- <span data-ttu-id="d8999-188">Uppdatera</span><span class="sxs-lookup"><span data-stu-id="d8999-188">Update</span></span>
- <span data-ttu-id="d8999-189">Managecontacts</span><span class="sxs-lookup"><span data-stu-id="d8999-189">Managecontacts</span></span>
- <span data-ttu-id="d8999-190">Getissuers</span><span class="sxs-lookup"><span data-stu-id="d8999-190">Getissuers</span></span>
- <span data-ttu-id="d8999-191">Listissuers</span><span class="sxs-lookup"><span data-stu-id="d8999-191">Listissuers</span></span>
- <span data-ttu-id="d8999-192">Setissuers</span><span class="sxs-lookup"><span data-stu-id="d8999-192">Setissuers</span></span>
- <span data-ttu-id="d8999-193">Deleteissuers</span><span class="sxs-lookup"><span data-stu-id="d8999-193">Deleteissuers</span></span>
- <span data-ttu-id="d8999-194">Manageissuers</span><span class="sxs-lookup"><span data-stu-id="d8999-194">Manageissuers</span></span>

```yaml
Type: String[]
Parameter Sets: ByServicePrincipalName, ByUserPrincipalName, ByObjectId, ByEmailAddress
Aliases:
Accepted values: get, list, delete, create, import, update, managecontacts, getissuers, listissuers, setissuers, deleteissuers, manageissuers, recover, purge, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8999-195">-PermissionsToKeys</span><span class="sxs-lookup"><span data-stu-id="d8999-195">-PermissionsToKeys</span></span>
<span data-ttu-id="d8999-196">Anger en matris med viktiga behörigheter för att bevilja en användare eller tjänstens huvud konto.</span><span class="sxs-lookup"><span data-stu-id="d8999-196">Specifies an array of key operation permissions to grant to a user or service principal.</span></span>

<span data-ttu-id="d8999-197">De acceptabla värdena för den här parametern:</span><span class="sxs-lookup"><span data-stu-id="d8999-197">The acceptable values for this parameter:</span></span>

- <span data-ttu-id="d8999-198">Dekryptera</span><span class="sxs-lookup"><span data-stu-id="d8999-198">Decrypt</span></span>
- <span data-ttu-id="d8999-199">Inträffade</span><span class="sxs-lookup"><span data-stu-id="d8999-199">Encrypt</span></span>
- <span data-ttu-id="d8999-200">UnwrapKey</span><span class="sxs-lookup"><span data-stu-id="d8999-200">UnwrapKey</span></span>
- <span data-ttu-id="d8999-201">WrapKey</span><span class="sxs-lookup"><span data-stu-id="d8999-201">WrapKey</span></span>
- <span data-ttu-id="d8999-202">Kontroll</span><span class="sxs-lookup"><span data-stu-id="d8999-202">Verify</span></span>
- <span data-ttu-id="d8999-203">Logga in</span><span class="sxs-lookup"><span data-stu-id="d8999-203">Sign</span></span>
- <span data-ttu-id="d8999-204">Lära</span><span class="sxs-lookup"><span data-stu-id="d8999-204">Get</span></span>
- <span data-ttu-id="d8999-205">Förteckning</span><span class="sxs-lookup"><span data-stu-id="d8999-205">List</span></span>
- <span data-ttu-id="d8999-206">Uppdatera</span><span class="sxs-lookup"><span data-stu-id="d8999-206">Update</span></span>
- <span data-ttu-id="d8999-207">Göra</span><span class="sxs-lookup"><span data-stu-id="d8999-207">Create</span></span>
- <span data-ttu-id="d8999-208">Importeras</span><span class="sxs-lookup"><span data-stu-id="d8999-208">Import</span></span>
- <span data-ttu-id="d8999-209">Ta bort</span><span class="sxs-lookup"><span data-stu-id="d8999-209">Delete</span></span>
- <span data-ttu-id="d8999-210">Reservdomänkontrollant</span><span class="sxs-lookup"><span data-stu-id="d8999-210">Backup</span></span>
- <span data-ttu-id="d8999-211">Terställa</span><span class="sxs-lookup"><span data-stu-id="d8999-211">Restore</span></span>
- <span data-ttu-id="d8999-212">Ã</span><span class="sxs-lookup"><span data-stu-id="d8999-212">Recover</span></span>
- <span data-ttu-id="d8999-213">Tömning</span><span class="sxs-lookup"><span data-stu-id="d8999-213">Purge</span></span>

```yaml
Type: String[]
Parameter Sets: ByServicePrincipalName, ByUserPrincipalName, ByObjectId, ByEmailAddress
Aliases:
Accepted values: decrypt, encrypt, unwrapKey, wrapKey, verify, sign, get, list, update, create, import, delete, backup, restore, recover, purge, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8999-214">-PermissionsToSecrets</span><span class="sxs-lookup"><span data-stu-id="d8999-214">-PermissionsToSecrets</span></span>
<span data-ttu-id="d8999-215">Anger en matris med hemliga åtgärds behörigheter som ska beviljas till en användare eller tjänstens huvud konto.</span><span class="sxs-lookup"><span data-stu-id="d8999-215">Specifies an array of secret operation permissions to grant to a user or service principal.</span></span>

<span data-ttu-id="d8999-216">De acceptabla värdena för den här parametern:</span><span class="sxs-lookup"><span data-stu-id="d8999-216">The acceptable values for this parameter:</span></span>

- <span data-ttu-id="d8999-217">Lära</span><span class="sxs-lookup"><span data-stu-id="d8999-217">Get</span></span>
- <span data-ttu-id="d8999-218">Förteckning</span><span class="sxs-lookup"><span data-stu-id="d8999-218">List</span></span>
- <span data-ttu-id="d8999-219">Ge</span><span class="sxs-lookup"><span data-stu-id="d8999-219">Set</span></span>
- <span data-ttu-id="d8999-220">Ta bort</span><span class="sxs-lookup"><span data-stu-id="d8999-220">Delete</span></span>
- <span data-ttu-id="d8999-221">Reservdomänkontrollant</span><span class="sxs-lookup"><span data-stu-id="d8999-221">Backup</span></span>
- <span data-ttu-id="d8999-222">Terställa</span><span class="sxs-lookup"><span data-stu-id="d8999-222">Restore</span></span>
- <span data-ttu-id="d8999-223">Ã</span><span class="sxs-lookup"><span data-stu-id="d8999-223">Recover</span></span>
- <span data-ttu-id="d8999-224">Tömning</span><span class="sxs-lookup"><span data-stu-id="d8999-224">Purge</span></span>

```yaml
Type: String[]
Parameter Sets: ByServicePrincipalName, ByUserPrincipalName, ByObjectId, ByEmailAddress
Aliases:
Accepted values: get, list, set, delete, backup, restore, recover, purge, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8999-225">-PermissionsToStorage</span><span class="sxs-lookup"><span data-stu-id="d8999-225">-PermissionsToStorage</span></span>
<span data-ttu-id="d8999-226">Anger hanterat lagrings konto och behörigheter för säkerhets associationer för att bevilja användare eller tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="d8999-226">Specifies managed storage account and SaS-definition operation permissions to grant to a user or service principal.</span></span>

```yaml
Type: String[]
Parameter Sets: ByServicePrincipalName, ByUserPrincipalName, ByObjectId, ByEmailAddress
Aliases:
Accepted values: get, list, delete, set, update, regeneratekey, getsas, listsas, deletesas, setsas, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8999-227">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8999-227">-ResourceGroupName</span></span>
<span data-ttu-id="d8999-228">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="d8999-228">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d8999-229">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="d8999-229">-ServicePrincipalName</span></span>
<span data-ttu-id="d8999-230">Anger tjänstens huvud namn för det program som ska bevilja behörigheter.</span><span class="sxs-lookup"><span data-stu-id="d8999-230">Specifies the service principal name of the application to which to grant permissions.</span></span>

<span data-ttu-id="d8999-231">Ange program-ID, som också kallas klient-ID, som är registrerat i AzureActive-katalogen.</span><span class="sxs-lookup"><span data-stu-id="d8999-231">Specify the application ID, also known as client ID, registered for the application in AzureActive Directory.</span></span> <span data-ttu-id="d8999-232">Programmet med SPN-namnet som den här parametern anger måste vara registrerat i Azure-katalogen som innehåller ditt nuvarande abonnemang.</span><span class="sxs-lookup"><span data-stu-id="d8999-232">The application with the service principal name that this parameter specifies must be registered in the Azure directory that contains your current subscription.</span></span>

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

### <span data-ttu-id="d8999-233">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="d8999-233">-UserPrincipalName</span></span>
<span data-ttu-id="d8999-234">Anger användarens huvud namn för den användare som ska bevilja behörigheter.</span><span class="sxs-lookup"><span data-stu-id="d8999-234">Specifies the user principal name of the user to whom to grant permissions.</span></span>

<span data-ttu-id="d8999-235">Det här UPN-namnet måste finnas i katalogen som är kopplad till det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="d8999-235">This user principal name must exist in the directory associated with the current subscription.</span></span>

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

### <span data-ttu-id="d8999-236">-VaultName</span><span class="sxs-lookup"><span data-stu-id="d8999-236">-VaultName</span></span>
<span data-ttu-id="d8999-237">Anger namnet på ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="d8999-237">Specifies the name of a key vault.</span></span>

<span data-ttu-id="d8999-238">Denna cmdlet ändrar åtkomst principen för det Key-valv som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="d8999-238">This cmdlet modifies the access policy for the key vault that this parameter specifies.</span></span>

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

### <span data-ttu-id="d8999-239">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d8999-239">-Confirm</span></span>
<span data-ttu-id="d8999-240">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d8999-240">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8999-241">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8999-241">-WhatIf</span></span>
<span data-ttu-id="d8999-242">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d8999-242">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d8999-243">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d8999-243">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8999-244">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8999-244">CommonParameters</span></span>
<span data-ttu-id="d8999-245">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8999-245">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8999-246">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8999-246">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8999-247">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d8999-247">INPUTS</span></span>

### <span data-ttu-id="d8999-248">Sträng, GUID, sträng [], växel</span><span class="sxs-lookup"><span data-stu-id="d8999-248">String, Guid, String[], Switch</span></span>

## <span data-ttu-id="d8999-249">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d8999-249">OUTPUTS</span></span>

### <span data-ttu-id="d8999-250">Microsoft. Azure. commands. valv. Models. PSVault</span><span class="sxs-lookup"><span data-stu-id="d8999-250">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

## <span data-ttu-id="d8999-251">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d8999-251">NOTES</span></span>

## <span data-ttu-id="d8999-252">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d8999-252">RELATED LINKS</span></span>

[<span data-ttu-id="d8999-253">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="d8999-253">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="d8999-254">Remove-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d8999-254">Remove-AzKeyVaultAccessPolicy</span></span>](./Remove-AzKeyVaultAccessPolicy.md)
