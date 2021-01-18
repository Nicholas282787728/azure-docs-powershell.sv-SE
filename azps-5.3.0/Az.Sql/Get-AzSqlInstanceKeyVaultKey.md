---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/Get-AzSqlInstanceKeyVaultKey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceKeyVaultKey.md
ms.openlocfilehash: 61672d71c2b65ff3588f4a4d8827220695c2d8de
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522986"
---
# <span data-ttu-id="3ab85-101">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="3ab85-101">Get-AzSqlInstanceKeyVaultKey</span></span>

## <span data-ttu-id="3ab85-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3ab85-102">SYNOPSIS</span></span>
<span data-ttu-id="3ab85-103">Hämtar en SQL-hanterad instanss nyckel valv.</span><span class="sxs-lookup"><span data-stu-id="3ab85-103">Gets a SQL managed instance's Key Vault keys.</span></span>

## <span data-ttu-id="3ab85-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3ab85-104">SYNTAX</span></span>

### <span data-ttu-id="3ab85-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="3ab85-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstanceKeyVaultKey [[-KeyId] <String>] [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ab85-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ab85-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceKeyVaultKey [[-KeyId] <String>] [-Instance] <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ab85-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ab85-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceKeyVaultKey [[-KeyId] <String>] [-InstanceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ab85-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3ab85-108">DESCRIPTION</span></span>
<span data-ttu-id="3ab85-109">I Get-AzSqlInstanceKeyVaultKey cmdlet får du information om nyckel valv nycklar på en SQL-hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="3ab85-109">The Get-AzSqlInstanceKeyVaultKey cmdlet gets information about the Key Vault keys on a SQL managed instance.</span></span> <span data-ttu-id="3ab85-110">Du kan visa alla nycklar på en hanterad instans eller Visa en specifik nyckel genom att ange KeyId.</span><span class="sxs-lookup"><span data-stu-id="3ab85-110">You can view all keys on a managed instance or view a specific key by providing the KeyId.</span></span>

## <span data-ttu-id="3ab85-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3ab85-111">EXAMPLES</span></span>

### <span data-ttu-id="3ab85-112">Exempel 1: Hämta alla nyckel valv nycklar</span><span class="sxs-lookup"><span data-stu-id="3ab85-112">Example 1: Get all Key Vault keys</span></span>
```powershell
PS C:\> Get-AzSqlInstanceKeyVaultKey -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="3ab85-113">Det här kommandot får alla nyckel valv nycklar på en SQL-hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="3ab85-113">This command gets all the Key Vault keys on a SQL managed instance.</span></span>

### <span data-ttu-id="3ab85-114">Exempel 2: skaffa ett speciellt nyckeltal</span><span class="sxs-lookup"><span data-stu-id="3ab85-114">Example 2: Get a specific Key Vault key</span></span>
```powershell
PS C:\> Get-AzSqlInstanceKeyVaultKey -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="3ab85-115">Det här kommandot får Key valv-tangenten med ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 '.</span><span class="sxs-lookup"><span data-stu-id="3ab85-115">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'.</span></span>

### <span data-ttu-id="3ab85-116">Exempel 3: använda instans objekt</span><span class="sxs-lookup"><span data-stu-id="3ab85-116">Example 3: Using instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Get-AzSqlInstanceKeyVaultKey -ManagedInstance $managedInstance -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="3ab85-117">Det här kommandot får Key valv-tangenten med ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 '.</span><span class="sxs-lookup"><span data-stu-id="3ab85-117">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'.</span></span>

### <span data-ttu-id="3ab85-118">Exempel 4: använda resurs-ID för instans</span><span class="sxs-lookup"><span data-stu-id="3ab85-118">Example 4: Using instance resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Get-AzSqlInstanceKeyVaultKey -InstanceResourceId $managedInstance.ResourceId -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="3ab85-119">Det här kommandot får Key valv-tangenten med ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 '.</span><span class="sxs-lookup"><span data-stu-id="3ab85-119">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'.</span></span>

### <span data-ttu-id="3ab85-120">Exempel 5: använda rör</span><span class="sxs-lookup"><span data-stu-id="3ab85-120">Example 5: Using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Get-AzSqlInstanceKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="3ab85-121">Det här kommandot får Key valv-tangenten med ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 '.</span><span class="sxs-lookup"><span data-stu-id="3ab85-121">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'.</span></span>

## <span data-ttu-id="3ab85-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3ab85-122">PARAMETERS</span></span>

### <span data-ttu-id="3ab85-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ab85-123">-DefaultProfile</span></span>
<span data-ttu-id="3ab85-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3ab85-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ab85-125">-Instance</span><span class="sxs-lookup"><span data-stu-id="3ab85-125">-Instance</span></span>
<span data-ttu-id="3ab85-126">Instans-indatavärdet</span><span class="sxs-lookup"><span data-stu-id="3ab85-126">The instance input object</span></span>

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

### <span data-ttu-id="3ab85-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="3ab85-127">-InstanceName</span></span>
<span data-ttu-id="3ab85-128">Instans namnet</span><span class="sxs-lookup"><span data-stu-id="3ab85-128">The instance name</span></span>

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

### <span data-ttu-id="3ab85-129">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="3ab85-129">-InstanceResourceId</span></span>
<span data-ttu-id="3ab85-130">Instans resurs-ID</span><span class="sxs-lookup"><span data-stu-id="3ab85-130">The instance resource id</span></span>

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

### <span data-ttu-id="3ab85-131">-KeyId</span><span class="sxs-lookup"><span data-stu-id="3ab85-131">-KeyId</span></span>
<span data-ttu-id="3ab85-132">AzureKeyVault-ID</span><span class="sxs-lookup"><span data-stu-id="3ab85-132">AzureKeyVault key id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ab85-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ab85-133">-ResourceGroupName</span></span>
<span data-ttu-id="3ab85-134">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="3ab85-134">The Resource Group Name</span></span>

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

### <span data-ttu-id="3ab85-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3ab85-135">-Confirm</span></span>
<span data-ttu-id="3ab85-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3ab85-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ab85-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ab85-137">-WhatIf</span></span>
<span data-ttu-id="3ab85-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3ab85-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ab85-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3ab85-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ab85-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ab85-140">CommonParameters</span></span>
<span data-ttu-id="3ab85-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ab85-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ab85-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3ab85-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ab85-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3ab85-143">INPUTS</span></span>

### <span data-ttu-id="3ab85-144">Microsoft. Azure. commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="3ab85-144">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="3ab85-145">System. String</span><span class="sxs-lookup"><span data-stu-id="3ab85-145">System.String</span></span>

## <span data-ttu-id="3ab85-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3ab85-146">OUTPUTS</span></span>

### <span data-ttu-id="3ab85-147">Microsoft. Azure. commands. SQL. TransparentDataEncryption. Model. AzureRmSqlManagedInstanceKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="3ab85-147">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span></span>

## <span data-ttu-id="3ab85-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3ab85-148">NOTES</span></span>

## <span data-ttu-id="3ab85-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3ab85-149">RELATED LINKS</span></span>
