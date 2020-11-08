---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/Remove-AzSqlInstanceKeyVaultKey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceKeyVaultKey.md
ms.openlocfilehash: 6812f6da3e32fd6074dc6958568bf3bd7eddeff0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269050"
---
# <span data-ttu-id="4301c-101">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4301c-101">Remove-AzSqlInstanceKeyVaultKey</span></span>

## <span data-ttu-id="4301c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4301c-102">SYNOPSIS</span></span>
<span data-ttu-id="4301c-103">Tar bort en Key Vault-tangenten från en SQL-hanterad instans</span><span class="sxs-lookup"><span data-stu-id="4301c-103">Removes a Key Vault key from a SQL managed instance</span></span>

## <span data-ttu-id="4301c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4301c-104">SYNTAX</span></span>

### <span data-ttu-id="4301c-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="4301c-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (Default)</span></span>
```
Remove-AzSqlInstanceKeyVaultKey [-ResourceGroupName] <String> [-InstanceName] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4301c-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4301c-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span></span>
```
Remove-AzSqlInstanceKeyVaultKey [-Instance] <AzureSqlManagedInstanceModel> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4301c-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4301c-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span></span>
```
Remove-AzSqlInstanceKeyVaultKey [-InstanceResourceId] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4301c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4301c-108">DESCRIPTION</span></span>
<span data-ttu-id="4301c-109">Remove-AzSqlInstanceKeyVaultKey cmdlet tar bort Key Vault-tangenten från den angivna hanterade instansen.</span><span class="sxs-lookup"><span data-stu-id="4301c-109">The Remove-AzSqlInstanceKeyVaultKey cmdlet  removes the Key Vault key from the specified Managed Instance.</span></span> <span data-ttu-id="4301c-110">Observera att den SQL-hanterade instansens behörigheter till Key-valvet inte har ändrats.</span><span class="sxs-lookup"><span data-stu-id="4301c-110">Note that the SQL managed instance's permissions to the key's vault are not changed.</span></span> <span data-ttu-id="4301c-111">Använd set-AzKeyVaultAccessPolicy för att ändra behörigheter.</span><span class="sxs-lookup"><span data-stu-id="4301c-111">To change permissions, use Set-AzKeyVaultAccessPolicy.</span></span> <span data-ttu-id="4301c-112">Observera att denna cmdlet inte gör några ändringar i huvud valvet.</span><span class="sxs-lookup"><span data-stu-id="4301c-112">Note that this cmdlet makes no changes to Key Vault.</span></span> <span data-ttu-id="4301c-113">Använd Remove-AzureKeyVaultKey om du vill ta bort en Key-valv.</span><span class="sxs-lookup"><span data-stu-id="4301c-113">To remove a key from Key Vault, use Remove-AzureKeyVaultKey.</span></span>

## <span data-ttu-id="4301c-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4301c-114">EXAMPLES</span></span>

### <span data-ttu-id="4301c-115">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4301c-115">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlInstanceKeyVaultKey -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="4301c-116">Det här kommandot tar bort Key valv-tangenten med ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' från den angivna hanterade instansen.</span><span class="sxs-lookup"><span data-stu-id="4301c-116">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

### <span data-ttu-id="4301c-117">Exempel 2: använda hanterat instans objekt</span><span class="sxs-lookup"><span data-stu-id="4301c-117">Example 2: Using managed instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Remove-AzSqlInstanceKeyVaultKey -Instance $managedInstance -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="4301c-118">Det här kommandot tar bort Key valv-tangenten med ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' från den angivna hanterade instansen.</span><span class="sxs-lookup"><span data-stu-id="4301c-118">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

### <span data-ttu-id="4301c-119">Exempel 3: använda resurs-ID för hanterade instanser</span><span class="sxs-lookup"><span data-stu-id="4301c-119">Example 3: Using managed instance resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Remove-AzSqlInstanceKeyVaultKey -InstanceResourceId $managedInstance.ResourceId -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="4301c-120">Det här kommandot tar bort Key valv-tangenten med ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' från den angivna hanterade instansen.</span><span class="sxs-lookup"><span data-stu-id="4301c-120">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

### <span data-ttu-id="4301c-121">Exempel 4: använda rör dragning</span><span class="sxs-lookup"><span data-stu-id="4301c-121">Example 4: Using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Remove-AzSqlInstanceKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="4301c-122">Det här kommandot tar bort Key valv-tangenten med ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' från den angivna hanterade instansen.</span><span class="sxs-lookup"><span data-stu-id="4301c-122">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

## <span data-ttu-id="4301c-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4301c-123">PARAMETERS</span></span>

### <span data-ttu-id="4301c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4301c-124">-DefaultProfile</span></span>
<span data-ttu-id="4301c-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4301c-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4301c-126">-Instance</span><span class="sxs-lookup"><span data-stu-id="4301c-126">-Instance</span></span>
<span data-ttu-id="4301c-127">Instans-indatavärdet</span><span class="sxs-lookup"><span data-stu-id="4301c-127">The instance input object</span></span>

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

### <span data-ttu-id="4301c-128">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="4301c-128">-InstanceName</span></span>
<span data-ttu-id="4301c-129">Instans namnet</span><span class="sxs-lookup"><span data-stu-id="4301c-129">The instance name</span></span>

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

### <span data-ttu-id="4301c-130">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="4301c-130">-InstanceResourceId</span></span>
<span data-ttu-id="4301c-131">Instans resurs-ID</span><span class="sxs-lookup"><span data-stu-id="4301c-131">The instance resource id</span></span>

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

### <span data-ttu-id="4301c-132">-KeyId</span><span class="sxs-lookup"><span data-stu-id="4301c-132">-KeyId</span></span>
<span data-ttu-id="4301c-133">AzureKeyVault-ID</span><span class="sxs-lookup"><span data-stu-id="4301c-133">AzureKeyVault key id</span></span>

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

### <span data-ttu-id="4301c-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4301c-134">-ResourceGroupName</span></span>
<span data-ttu-id="4301c-135">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="4301c-135">The Resource Group Name</span></span>

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

### <span data-ttu-id="4301c-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4301c-136">-Confirm</span></span>
<span data-ttu-id="4301c-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4301c-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4301c-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4301c-138">-WhatIf</span></span>
<span data-ttu-id="4301c-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4301c-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4301c-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4301c-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4301c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4301c-141">CommonParameters</span></span>
<span data-ttu-id="4301c-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4301c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4301c-143">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4301c-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4301c-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4301c-144">INPUTS</span></span>

### <span data-ttu-id="4301c-145">Microsoft. Azure. commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="4301c-145">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="4301c-146">System. String</span><span class="sxs-lookup"><span data-stu-id="4301c-146">System.String</span></span>

## <span data-ttu-id="4301c-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4301c-147">OUTPUTS</span></span>

### <span data-ttu-id="4301c-148">Microsoft. Azure. commands. SQL. TransparentDataEncryption. Model. AzureRmSqlManagedInstanceKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="4301c-148">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span></span>

## <span data-ttu-id="4301c-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4301c-149">NOTES</span></span>

## <span data-ttu-id="4301c-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4301c-150">RELATED LINKS</span></span>
