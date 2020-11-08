---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/Get-AzSqlInstanceKeyVaultKey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceKeyVaultKey.md
ms.openlocfilehash: 8c17ca9f899adc731c549b45617c287010baaac5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920627"
---
# <span data-ttu-id="59808-101">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="59808-101">Get-AzSqlInstanceKeyVaultKey</span></span>

## <span data-ttu-id="59808-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="59808-102">SYNOPSIS</span></span>
<span data-ttu-id="59808-103">Hämtar en SQL-hanterad instanss nyckel valv.</span><span class="sxs-lookup"><span data-stu-id="59808-103">Gets a SQL managed instance's Key Vault keys.</span></span>

## <span data-ttu-id="59808-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="59808-104">SYNTAX</span></span>

### <span data-ttu-id="59808-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="59808-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstanceKeyVaultKey [[-KeyId] <String>] [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59808-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="59808-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceKeyVaultKey [[-KeyId] <String>] [-Instance] <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59808-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="59808-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceKeyVaultKey [[-KeyId] <String>] [-InstanceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59808-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="59808-108">DESCRIPTION</span></span>
<span data-ttu-id="59808-109">I Get-AzSqlInstanceKeyVaultKey cmdlet får du information om nyckel valv nycklar på en SQL-hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="59808-109">The Get-AzSqlInstanceKeyVaultKey cmdlet gets information about the Key Vault keys on a SQL managed instance.</span></span> <span data-ttu-id="59808-110">Du kan visa alla nycklar på en hanterad instans eller Visa en specifik nyckel genom att ange KeyId.</span><span class="sxs-lookup"><span data-stu-id="59808-110">You can view all keys on a managed instance or view a specific key by providing the KeyId.</span></span>

## <span data-ttu-id="59808-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="59808-111">EXAMPLES</span></span>

### <span data-ttu-id="59808-112">Exempel 1: Hämta alla nyckel valv nycklar</span><span class="sxs-lookup"><span data-stu-id="59808-112">Example 1: Get all Key Vault keys</span></span>
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

<span data-ttu-id="59808-113">Det här kommandot får alla nyckel valv nycklar på en SQL-hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="59808-113">This command gets all the Key Vault keys on a SQL managed instance.</span></span>

### <span data-ttu-id="59808-114">Exempel 2: skaffa ett speciellt nyckeltal</span><span class="sxs-lookup"><span data-stu-id="59808-114">Example 2: Get a specific Key Vault key</span></span>
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

<span data-ttu-id="59808-115">Det här kommandot får Key valv-tangenten med ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 '.</span><span class="sxs-lookup"><span data-stu-id="59808-115">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'.</span></span>

### <span data-ttu-id="59808-116">Exempel 3: använda instans objekt</span><span class="sxs-lookup"><span data-stu-id="59808-116">Example 3: Using instance object</span></span>
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

<span data-ttu-id="59808-117">Det här kommandot får Key valv-tangenten med ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 '.</span><span class="sxs-lookup"><span data-stu-id="59808-117">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'.</span></span>

### <span data-ttu-id="59808-118">Exempel 4: använda resurs-ID för instans</span><span class="sxs-lookup"><span data-stu-id="59808-118">Example 4: Using instance resource id</span></span>
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

<span data-ttu-id="59808-119">Det här kommandot får Key valv-tangenten med ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 '.</span><span class="sxs-lookup"><span data-stu-id="59808-119">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'.</span></span>

### <span data-ttu-id="59808-120">Exempel 5: använda rör</span><span class="sxs-lookup"><span data-stu-id="59808-120">Example 5: Using piping</span></span>
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

<span data-ttu-id="59808-121">Det här kommandot får Key valv-tangenten med ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 '.</span><span class="sxs-lookup"><span data-stu-id="59808-121">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'.</span></span>

## <span data-ttu-id="59808-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="59808-122">PARAMETERS</span></span>

### <span data-ttu-id="59808-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59808-123">-DefaultProfile</span></span>
<span data-ttu-id="59808-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="59808-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59808-125">-Instance</span><span class="sxs-lookup"><span data-stu-id="59808-125">-Instance</span></span>
<span data-ttu-id="59808-126">Instans-indatavärdet</span><span class="sxs-lookup"><span data-stu-id="59808-126">The instance input object</span></span>

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

### <span data-ttu-id="59808-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="59808-127">-InstanceName</span></span>
<span data-ttu-id="59808-128">Instans namnet</span><span class="sxs-lookup"><span data-stu-id="59808-128">The instance name</span></span>

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

### <span data-ttu-id="59808-129">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="59808-129">-InstanceResourceId</span></span>
<span data-ttu-id="59808-130">Instans resurs-ID</span><span class="sxs-lookup"><span data-stu-id="59808-130">The instance resource id</span></span>

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

### <span data-ttu-id="59808-131">-KeyId</span><span class="sxs-lookup"><span data-stu-id="59808-131">-KeyId</span></span>
<span data-ttu-id="59808-132">AzureKeyVault-ID</span><span class="sxs-lookup"><span data-stu-id="59808-132">AzureKeyVault key id</span></span>

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

### <span data-ttu-id="59808-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59808-133">-ResourceGroupName</span></span>
<span data-ttu-id="59808-134">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="59808-134">The Resource Group Name</span></span>

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

### <span data-ttu-id="59808-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="59808-135">-Confirm</span></span>
<span data-ttu-id="59808-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="59808-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59808-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59808-137">-WhatIf</span></span>
<span data-ttu-id="59808-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="59808-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59808-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="59808-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59808-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59808-140">CommonParameters</span></span>
<span data-ttu-id="59808-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59808-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59808-142">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="59808-142">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59808-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="59808-143">INPUTS</span></span>

### <span data-ttu-id="59808-144">Microsoft. Azure. commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="59808-144">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="59808-145">System. String</span><span class="sxs-lookup"><span data-stu-id="59808-145">System.String</span></span>

## <span data-ttu-id="59808-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="59808-146">OUTPUTS</span></span>

### <span data-ttu-id="59808-147">Microsoft. Azure. commands. SQL. TransparentDataEncryption. Model. AzureRmSqlManagedInstanceKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="59808-147">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span></span>

## <span data-ttu-id="59808-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="59808-148">NOTES</span></span>

## <span data-ttu-id="59808-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="59808-149">RELATED LINKS</span></span>