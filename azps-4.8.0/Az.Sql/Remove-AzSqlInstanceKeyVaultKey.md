---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/Remove-AzSqlInstanceKeyVaultKey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceKeyVaultKey.md
ms.openlocfilehash: 6812f6da3e32fd6074dc6958568bf3bd7eddeff0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259037"
---
# <span data-ttu-id="5cb42-101">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5cb42-101">Remove-AzSqlInstanceKeyVaultKey</span></span>

## <span data-ttu-id="5cb42-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5cb42-102">SYNOPSIS</span></span>
<span data-ttu-id="5cb42-103">Tar bort en Key Vault-tangenten från en SQL-hanterad instans</span><span class="sxs-lookup"><span data-stu-id="5cb42-103">Removes a Key Vault key from a SQL managed instance</span></span>

## <span data-ttu-id="5cb42-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5cb42-104">SYNTAX</span></span>

### <span data-ttu-id="5cb42-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="5cb42-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (Default)</span></span>
```
Remove-AzSqlInstanceKeyVaultKey [-ResourceGroupName] <String> [-InstanceName] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cb42-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5cb42-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span></span>
```
Remove-AzSqlInstanceKeyVaultKey [-Instance] <AzureSqlManagedInstanceModel> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cb42-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5cb42-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span></span>
```
Remove-AzSqlInstanceKeyVaultKey [-InstanceResourceId] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5cb42-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5cb42-108">DESCRIPTION</span></span>
<span data-ttu-id="5cb42-109">Remove-AzSqlInstanceKeyVaultKey cmdlet tar bort Key Vault-tangenten från den angivna hanterade instansen.</span><span class="sxs-lookup"><span data-stu-id="5cb42-109">The Remove-AzSqlInstanceKeyVaultKey cmdlet  removes the Key Vault key from the specified Managed Instance.</span></span> <span data-ttu-id="5cb42-110">Observera att den SQL-hanterade instansens behörigheter till Key-valvet inte har ändrats.</span><span class="sxs-lookup"><span data-stu-id="5cb42-110">Note that the SQL managed instance's permissions to the key's vault are not changed.</span></span> <span data-ttu-id="5cb42-111">Använd set-AzKeyVaultAccessPolicy för att ändra behörigheter.</span><span class="sxs-lookup"><span data-stu-id="5cb42-111">To change permissions, use Set-AzKeyVaultAccessPolicy.</span></span> <span data-ttu-id="5cb42-112">Observera att denna cmdlet inte gör några ändringar i huvud valvet.</span><span class="sxs-lookup"><span data-stu-id="5cb42-112">Note that this cmdlet makes no changes to Key Vault.</span></span> <span data-ttu-id="5cb42-113">Använd Remove-AzureKeyVaultKey om du vill ta bort en Key-valv.</span><span class="sxs-lookup"><span data-stu-id="5cb42-113">To remove a key from Key Vault, use Remove-AzureKeyVaultKey.</span></span>

## <span data-ttu-id="5cb42-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5cb42-114">EXAMPLES</span></span>

### <span data-ttu-id="5cb42-115">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5cb42-115">Example 1</span></span>
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

<span data-ttu-id="5cb42-116">Det här kommandot tar bort Key valv-tangenten med ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' från den angivna hanterade instansen.</span><span class="sxs-lookup"><span data-stu-id="5cb42-116">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

### <span data-ttu-id="5cb42-117">Exempel 2: använda hanterat instans objekt</span><span class="sxs-lookup"><span data-stu-id="5cb42-117">Example 2: Using managed instance object</span></span>
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

<span data-ttu-id="5cb42-118">Det här kommandot tar bort Key valv-tangenten med ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' från den angivna hanterade instansen.</span><span class="sxs-lookup"><span data-stu-id="5cb42-118">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

### <span data-ttu-id="5cb42-119">Exempel 3: använda resurs-ID för hanterade instanser</span><span class="sxs-lookup"><span data-stu-id="5cb42-119">Example 3: Using managed instance resource id</span></span>
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

<span data-ttu-id="5cb42-120">Det här kommandot tar bort Key valv-tangenten med ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' från den angivna hanterade instansen.</span><span class="sxs-lookup"><span data-stu-id="5cb42-120">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

### <span data-ttu-id="5cb42-121">Exempel 4: använda rör dragning</span><span class="sxs-lookup"><span data-stu-id="5cb42-121">Example 4: Using piping</span></span>
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

<span data-ttu-id="5cb42-122">Det här kommandot tar bort Key valv-tangenten med ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' från den angivna hanterade instansen.</span><span class="sxs-lookup"><span data-stu-id="5cb42-122">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

## <span data-ttu-id="5cb42-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5cb42-123">PARAMETERS</span></span>

### <span data-ttu-id="5cb42-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cb42-124">-DefaultProfile</span></span>
<span data-ttu-id="5cb42-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5cb42-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5cb42-126">-Instance</span><span class="sxs-lookup"><span data-stu-id="5cb42-126">-Instance</span></span>
<span data-ttu-id="5cb42-127">Instans-indatavärdet</span><span class="sxs-lookup"><span data-stu-id="5cb42-127">The instance input object</span></span>

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

### <span data-ttu-id="5cb42-128">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="5cb42-128">-InstanceName</span></span>
<span data-ttu-id="5cb42-129">Instans namnet</span><span class="sxs-lookup"><span data-stu-id="5cb42-129">The instance name</span></span>

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

### <span data-ttu-id="5cb42-130">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="5cb42-130">-InstanceResourceId</span></span>
<span data-ttu-id="5cb42-131">Instans resurs-ID</span><span class="sxs-lookup"><span data-stu-id="5cb42-131">The instance resource id</span></span>

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

### <span data-ttu-id="5cb42-132">-KeyId</span><span class="sxs-lookup"><span data-stu-id="5cb42-132">-KeyId</span></span>
<span data-ttu-id="5cb42-133">AzureKeyVault-ID</span><span class="sxs-lookup"><span data-stu-id="5cb42-133">AzureKeyVault key id</span></span>

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

### <span data-ttu-id="5cb42-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cb42-134">-ResourceGroupName</span></span>
<span data-ttu-id="5cb42-135">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="5cb42-135">The Resource Group Name</span></span>

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

### <span data-ttu-id="5cb42-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5cb42-136">-Confirm</span></span>
<span data-ttu-id="5cb42-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5cb42-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cb42-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cb42-138">-WhatIf</span></span>
<span data-ttu-id="5cb42-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5cb42-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5cb42-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5cb42-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cb42-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cb42-141">CommonParameters</span></span>
<span data-ttu-id="5cb42-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cb42-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cb42-143">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5cb42-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cb42-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5cb42-144">INPUTS</span></span>

### <span data-ttu-id="5cb42-145">Microsoft. Azure. commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="5cb42-145">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="5cb42-146">System. String</span><span class="sxs-lookup"><span data-stu-id="5cb42-146">System.String</span></span>

## <span data-ttu-id="5cb42-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5cb42-147">OUTPUTS</span></span>

### <span data-ttu-id="5cb42-148">Microsoft. Azure. commands. SQL. TransparentDataEncryption. Model. AzureRmSqlManagedInstanceKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="5cb42-148">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span></span>

## <span data-ttu-id="5cb42-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5cb42-149">NOTES</span></span>

## <span data-ttu-id="5cb42-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5cb42-150">RELATED LINKS</span></span>