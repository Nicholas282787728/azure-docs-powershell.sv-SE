---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/Set-AzSqlInstanceTransparentDataEncryptionProtector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceTransparentDataEncryptionProtector.md
ms.openlocfilehash: 15462ea79b5499818d71b145e0faaa35c09baf0b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93927146"
---
# <span data-ttu-id="45d65-101">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="45d65-101">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="45d65-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="45d65-102">SYNOPSIS</span></span>
<span data-ttu-id="45d65-103">Ställer in skydd mot transparent data kryptering (TDE) för en SQL-hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="45d65-103">Sets the Transparent Data Encryption (TDE) protector for a SQL managed instance.</span></span>

## <span data-ttu-id="45d65-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="45d65-104">SYNTAX</span></span>

### <span data-ttu-id="45d65-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="45d65-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (Default)</span></span>
```
Set-AzSqlInstanceTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-ResourceGroupName] <String> [-InstanceName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45d65-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="45d65-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span></span>
```
Set-AzSqlInstanceTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-Instance] <AzureSqlManagedInstanceModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45d65-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="45d65-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span></span>
```
Set-AzSqlInstanceTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-InstanceResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="45d65-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="45d65-108">DESCRIPTION</span></span>
<span data-ttu-id="45d65-109">Set-AzSqlInstanceTransparentDataEncryptionProtector-cmdleten ställer in TDE-skyddskomponenten för en SQL-hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="45d65-109">The Set-AzSqlInstanceTransparentDataEncryptionProtector cmdlet sets the TDE protector for a SQL managed instance.</span></span> <span data-ttu-id="45d65-110">Om du ändrar TDE skydds typ roteras skydds komponenten.</span><span class="sxs-lookup"><span data-stu-id="45d65-110">Changing the TDE protector type will rotate the protector.</span></span>

## <span data-ttu-id="45d65-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="45d65-111">EXAMPLES</span></span>

### <span data-ttu-id="45d65-112">Exempel 1: Ange skydds typen transparent Data Encryption (TDE) till ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="45d65-112">Example 1: Set the Transparent Data Encryption (TDE) protector type to ServiceManaged</span></span>
```powershell
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -Type ServiceManaged

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : ServiceManaged
ManagedInstanceKeyVaultKeyName : ServiceManaged
KeyId                          :
```

<span data-ttu-id="45d65-113">Det här kommandot uppdaterar en hanterad instanss TDE skydds typ till tjänst hanterad.</span><span class="sxs-lookup"><span data-stu-id="45d65-113">This command updates a managed instance's TDE protector type to Service Managed.</span></span>

### <span data-ttu-id="45d65-114">Exempel 2: Ange den transparenta typen av data krypterings skydd för Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="45d65-114">Example 2: Set the Transparent Data Encryption protector type to Azure Key Vault</span></span>
```powershell
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="45d65-115">Det här kommandot uppdaterar den angivna hanterade instansen för användning av Key valv-tangenten med ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' som TDE-skydd.</span><span class="sxs-lookup"><span data-stu-id="45d65-115">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

### <span data-ttu-id="45d65-116">Exempel 3: Ange den transparenta typen av data krypterings skydd för Azure Key Vault med hanterat instans objekt</span><span class="sxs-lookup"><span data-stu-id="45d65-116">Example 3: Set the Transparent Data Encryption protector type to Azure Key Vault using managed instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -Instance $managedInstance -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="45d65-117">Det här kommandot uppdaterar den angivna hanterade instansen för användning av Key valv-tangenten med ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' som TDE-skydd.</span><span class="sxs-lookup"><span data-stu-id="45d65-117">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

### <span data-ttu-id="45d65-118">Exempel 4: Ange den transparenta typen av data krypterings skydd för Azure Key Vault med resurs-ID</span><span class="sxs-lookup"><span data-stu-id="45d65-118">Example 4: Set the Transparent Data Encryption protector type to Azure Key Vault using resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -InstanceResourceId $managedInstance.ResourceId -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="45d65-119">Det här kommandot uppdaterar den angivna hanterade instansen för användning av Key valv-tangenten med ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' som TDE-skydd.</span><span class="sxs-lookup"><span data-stu-id="45d65-119">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

### <span data-ttu-id="45d65-120">Exempel 5: Ange den transparenta typen av data krypterings skydd till Azure Key Vault med ledning</span><span class="sxs-lookup"><span data-stu-id="45d65-120">Example 5: Set the Transparent Data Encryption protector type to Azure Key Vault using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Set-AzSqlInstanceTransparentDataEncryptionProtector -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="45d65-121">Det här kommandot uppdaterar den angivna hanterade instansen för användning av Key valv-tangenten med ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' som TDE-skydd.</span><span class="sxs-lookup"><span data-stu-id="45d65-121">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

## <span data-ttu-id="45d65-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="45d65-122">PARAMETERS</span></span>

### <span data-ttu-id="45d65-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45d65-123">-DefaultProfile</span></span>
<span data-ttu-id="45d65-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="45d65-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45d65-125">-Force</span><span class="sxs-lookup"><span data-stu-id="45d65-125">-Force</span></span>
<span data-ttu-id="45d65-126">Hoppa över bekräftelse meddelande för att utföra åtgärden</span><span class="sxs-lookup"><span data-stu-id="45d65-126">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="45d65-127">-Instance</span><span class="sxs-lookup"><span data-stu-id="45d65-127">-Instance</span></span>
<span data-ttu-id="45d65-128">Instans-indatavärdet</span><span class="sxs-lookup"><span data-stu-id="45d65-128">The instance input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet
Aliases: InputObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="45d65-129">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="45d65-129">-InstanceName</span></span>
<span data-ttu-id="45d65-130">Instans namnet</span><span class="sxs-lookup"><span data-stu-id="45d65-130">The instance name</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45d65-131">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="45d65-131">-InstanceResourceId</span></span>
<span data-ttu-id="45d65-132">Instans resurs-ID</span><span class="sxs-lookup"><span data-stu-id="45d65-132">The instance resource id</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45d65-133">-KeyId</span><span class="sxs-lookup"><span data-stu-id="45d65-133">-KeyId</span></span>
<span data-ttu-id="45d65-134">KeyId för Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="45d65-134">The Azure Key Vault KeyId.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45d65-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45d65-135">-ResourceGroupName</span></span>
<span data-ttu-id="45d65-136">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="45d65-136">The Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45d65-137">– Skriv</span><span class="sxs-lookup"><span data-stu-id="45d65-137">-Type</span></span>
<span data-ttu-id="45d65-138">Den transparenta data krypterings skydds typen för Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="45d65-138">The Azure Sql Database Transparent Data Encryption Protector type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType
Parameter Sets: (All)
Aliases:
Accepted values: AzureKeyVault, ServiceManaged

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45d65-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="45d65-139">-Confirm</span></span>
<span data-ttu-id="45d65-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="45d65-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45d65-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45d65-141">-WhatIf</span></span>
<span data-ttu-id="45d65-142">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="45d65-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45d65-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="45d65-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45d65-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45d65-144">CommonParameters</span></span>
<span data-ttu-id="45d65-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45d65-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45d65-146">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="45d65-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45d65-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="45d65-147">INPUTS</span></span>

### <span data-ttu-id="45d65-148">Microsoft. Azure. commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="45d65-148">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="45d65-149">System. String</span><span class="sxs-lookup"><span data-stu-id="45d65-149">System.String</span></span>

## <span data-ttu-id="45d65-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="45d65-150">OUTPUTS</span></span>

### <span data-ttu-id="45d65-151">Microsoft. Azure. commands. SQL. TransparentDataEncryption. Model. AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="45d65-151">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="45d65-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="45d65-152">NOTES</span></span>

## <span data-ttu-id="45d65-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="45d65-153">RELATED LINKS</span></span>