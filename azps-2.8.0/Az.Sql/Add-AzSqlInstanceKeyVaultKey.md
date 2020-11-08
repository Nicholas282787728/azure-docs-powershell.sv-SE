---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Add-AzSqlInstanceKeyVaultKey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlInstanceKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlInstanceKeyVaultKey.md
ms.openlocfilehash: 4c0f576d118a502b04d4effd9a1de8f98e2a3813
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919903"
---
# <span data-ttu-id="c701c-101">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="c701c-101">Add-AzSqlInstanceKeyVaultKey</span></span>

## <span data-ttu-id="c701c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c701c-102">SYNOPSIS</span></span>
<span data-ttu-id="c701c-103">Lägger till en Key valv-nycklar till den tillhandahållna hanterade instansen.</span><span class="sxs-lookup"><span data-stu-id="c701c-103">Adds a key vault key to the provided Managed Instance.</span></span> 

## <span data-ttu-id="c701c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c701c-104">SYNTAX</span></span>

### <span data-ttu-id="c701c-105">AddAzureRmSqlInstanceKeyVaultKeyDefaultParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="c701c-105">AddAzureRmSqlInstanceKeyVaultKeyDefaultParameterSet (Default)</span></span>
```
Add-AzSqlInstanceKeyVaultKey [-ResourceGroupName] <String> [-InstanceName] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c701c-106">AddAzureRmSqlInstanceKeyVaultKeyInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c701c-106">AddAzureRmSqlInstanceKeyVaultKeyInputObjectParameterSet</span></span>
```
Add-AzSqlInstanceKeyVaultKey [-Instance] <AzureSqlManagedInstanceModel> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c701c-107">AddAzureRmSqlInstanceKeyVaultKeyResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c701c-107">AddAzureRmSqlInstanceKeyVaultKeyResourceIdParameterSet</span></span>
```
Add-AzSqlInstanceKeyVaultKey [-InstanceResourceId] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c701c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c701c-108">DESCRIPTION</span></span>
<span data-ttu-id="c701c-109">Add-AzSqlInstanceKeyVaultKey cmdlet lägger till en Key valv-nycklar till den tillhandahållna hanterade instansen.</span><span class="sxs-lookup"><span data-stu-id="c701c-109">The Add-AzSqlInstanceKeyVaultKey cmdlet adds a key vault key to the provided Managed Instance.</span></span> <span data-ttu-id="c701c-110">Den hanterade instansen måste ha behörigheterna get, wrapKey, unwrapKey och The valv för att ge behörighet till den hanterade instansen.</span><span class="sxs-lookup"><span data-stu-id="c701c-110">The managed instance must have 'get, wrapKey, unwrapKey' permissions to the vault, use the following script to grant permission to the managed instance.</span></span>
<span data-ttu-id="c701c-111">$managedInstance = Get-AzSqlInstance-namn ' ContosoManagedInstanceName '-ResourceGroupName ' ContosoResourceGroup ' Set-AzKeyVaultAccessPolicy-VaultName ContosoVault-ObjectId $managedInstance. Identity. PrincipalId-PermissionsToKeys get, wrapKey, unwrapKey</span><span class="sxs-lookup"><span data-stu-id="c701c-111">$managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup' Set-AzKeyVaultAccessPolicy -VaultName ContosoVault -ObjectId $managedInstance.Identity.PrincipalId -PermissionsToKeys get, wrapKey, unwrapKey</span></span>

## <span data-ttu-id="c701c-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c701c-112">EXAMPLES</span></span>

### <span data-ttu-id="c701c-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c701c-113">Example 1</span></span>
```powershell
PS C:\> Add-AzSqlInstanceKeyVaultKey -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="c701c-114">Det här kommandot lägger till Key valv-tangenten med ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' till den SQL-hanterade instans med namnet "ContosoManagedInstanceName" i resurs gruppen "ContosoResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="c701c-114">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

### <span data-ttu-id="c701c-115">Exempel 2: använda hanterat instans objekt</span><span class="sxs-lookup"><span data-stu-id="c701c-115">Example 2: Using managed instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Add-AzSqlInstanceKeyVaultKey -Instance $managedInstance -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="c701c-116">Det här kommandot lägger till Key valv-tangenten med ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' till den SQL-hanterade instans med namnet "ContosoManagedInstanceName" i resurs gruppen "ContosoResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="c701c-116">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

### <span data-ttu-id="c701c-117">Exempel 3: använda resurs-ID för hanterade instanser</span><span class="sxs-lookup"><span data-stu-id="c701c-117">Example 3: Using managed instance resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Add-AzSqlInstanceKeyVaultKey -InstanceResourceId $managedInstance.ResourceId -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="c701c-118">Det här kommandot lägger till Key valv-tangenten med ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' till den SQL-hanterade instans med namnet "ContosoManagedInstanceName" i resurs gruppen "ContosoResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="c701c-118">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

### <span data-ttu-id="c701c-119">Exempel 4: använda rör dragning</span><span class="sxs-lookup"><span data-stu-id="c701c-119">Example 4: Using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Add-AzSqlInstanceKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="c701c-120">Det här kommandot lägger till Key valv-tangenten med ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' till den SQL-hanterade instans med namnet "ContosoManagedInstanceName" i resurs gruppen "ContosoResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="c701c-120">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

## <span data-ttu-id="c701c-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c701c-121">PARAMETERS</span></span>

### <span data-ttu-id="c701c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c701c-122">-DefaultProfile</span></span>
<span data-ttu-id="c701c-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c701c-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c701c-124">-Instance</span><span class="sxs-lookup"><span data-stu-id="c701c-124">-Instance</span></span>
<span data-ttu-id="c701c-125">Instans-indatavärdet</span><span class="sxs-lookup"><span data-stu-id="c701c-125">The instance input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet
Aliases: InputObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c701c-126">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="c701c-126">-InstanceName</span></span>
<span data-ttu-id="c701c-127">Instans namnet</span><span class="sxs-lookup"><span data-stu-id="c701c-127">The instance name</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c701c-128">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="c701c-128">-InstanceResourceId</span></span>
<span data-ttu-id="c701c-129">Instans resurs-ID</span><span class="sxs-lookup"><span data-stu-id="c701c-129">The instance resource id</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c701c-130">-KeyId</span><span class="sxs-lookup"><span data-stu-id="c701c-130">-KeyId</span></span>
<span data-ttu-id="c701c-131">AzureKeyVault-ID</span><span class="sxs-lookup"><span data-stu-id="c701c-131">AzureKeyVault key id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c701c-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c701c-132">-ResourceGroupName</span></span>
<span data-ttu-id="c701c-133">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="c701c-133">The Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c701c-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c701c-134">-Confirm</span></span>
<span data-ttu-id="c701c-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c701c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c701c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c701c-136">-WhatIf</span></span>
<span data-ttu-id="c701c-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c701c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c701c-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c701c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c701c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c701c-139">CommonParameters</span></span>
<span data-ttu-id="c701c-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c701c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c701c-141">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c701c-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c701c-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c701c-142">INPUTS</span></span>

### <span data-ttu-id="c701c-143">Microsoft. Azure. commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="c701c-143">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="c701c-144">System. String</span><span class="sxs-lookup"><span data-stu-id="c701c-144">System.String</span></span>

## <span data-ttu-id="c701c-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c701c-145">OUTPUTS</span></span>

### <span data-ttu-id="c701c-146">Microsoft. Azure. commands. SQL. TransparentDataEncryption. Model. AzureRmSqlManagedInstanceKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="c701c-146">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span></span>

## <span data-ttu-id="c701c-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c701c-147">NOTES</span></span>

## <span data-ttu-id="c701c-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c701c-148">RELATED LINKS</span></span>