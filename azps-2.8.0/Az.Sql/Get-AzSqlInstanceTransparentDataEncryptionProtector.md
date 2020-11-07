---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/Get-AzSqlInstanceTransparentDataEncryptionProtector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceTransparentDataEncryptionProtector.md
ms.openlocfilehash: 827c3c3d3cb87fbc3e51b8f083c74af559152115
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920344"
---
# <span data-ttu-id="fc2eb-101">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="fc2eb-101">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="fc2eb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fc2eb-102">SYNOPSIS</span></span>
<span data-ttu-id="fc2eb-103">Hämtar skyddet för transparent Data Encryption (TDE) för en SQL-hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="fc2eb-103">Gets the Transparent Data Encryption (TDE) protector for a SQL managed instance.</span></span>

## <span data-ttu-id="fc2eb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fc2eb-104">SYNTAX</span></span>

### <span data-ttu-id="fc2eb-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="fc2eb-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstanceTransparentDataEncryptionProtector [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc2eb-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc2eb-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceTransparentDataEncryptionProtector [-Instance] <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc2eb-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc2eb-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceTransparentDataEncryptionProtector [-InstanceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc2eb-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fc2eb-108">DESCRIPTION</span></span>
<span data-ttu-id="fc2eb-109">Get-AzSqlInstanceTransparentDataEncryptionProtector-cmdleten hämtar TDE-skyddskomponenten för den angivna SQL-hanterade instansen.</span><span class="sxs-lookup"><span data-stu-id="fc2eb-109">The Get-AzSqlInstanceTransparentDataEncryptionProtector cmdlet gets the TDE protector for the specified SQL managed instance.</span></span>

## <span data-ttu-id="fc2eb-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fc2eb-110">EXAMPLES</span></span>

### <span data-ttu-id="fc2eb-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fc2eb-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceTransparentDataEncryptionProtector -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="fc2eb-112">Det här kommandot får TDE skydds komponenten för den hanterade instans som heter ContosoManagedInstanceName i resurs gruppen med namnet ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="fc2eb-112">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="fc2eb-113">Exempel 2: använda hanterat instans objekt</span><span class="sxs-lookup"><span data-stu-id="fc2eb-113">Example 2: Using managed instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Get-AzSqlInstanceTransparentDataEncryptionProtector -Instance $managedInstance 'ContosoManagedInstanceName'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="fc2eb-114">Det här kommandot får TDE skydds komponenten för den hanterade instans som heter ContosoManagedInstanceName i resurs gruppen med namnet ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="fc2eb-114">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="fc2eb-115">Exempel 3: använda resurs-ID för hanterade instanser</span><span class="sxs-lookup"><span data-stu-id="fc2eb-115">Example 3: Using managed instance resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Get-AzSqlInstanceTransparentDataEncryptionProtector -InstanceResourceId $managedInstance.ResourceId

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="fc2eb-116">Det här kommandot får TDE skydds komponenten för den hanterade instans som heter ContosoManagedInstanceName i resurs gruppen med namnet ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="fc2eb-116">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="fc2eb-117">Exempel 4: använda rör dragning</span><span class="sxs-lookup"><span data-stu-id="fc2eb-117">Example 4: Using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Get-AzSqlInstanceTransparentDataEncryptionProtector

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="fc2eb-118">Det här kommandot får TDE skydds komponenten för den hanterade instans som heter ContosoManagedInstanceName i resurs gruppen med namnet ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="fc2eb-118">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="fc2eb-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fc2eb-119">PARAMETERS</span></span>

### <span data-ttu-id="fc2eb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc2eb-120">-DefaultProfile</span></span>
<span data-ttu-id="fc2eb-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fc2eb-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc2eb-122">-Instance</span><span class="sxs-lookup"><span data-stu-id="fc2eb-122">-Instance</span></span>
<span data-ttu-id="fc2eb-123">Instans-indatavärdet</span><span class="sxs-lookup"><span data-stu-id="fc2eb-123">The instance input object</span></span>

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

### <span data-ttu-id="fc2eb-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="fc2eb-124">-InstanceName</span></span>
<span data-ttu-id="fc2eb-125">Instans namnet</span><span class="sxs-lookup"><span data-stu-id="fc2eb-125">The instance name</span></span>

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

### <span data-ttu-id="fc2eb-126">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="fc2eb-126">-InstanceResourceId</span></span>
<span data-ttu-id="fc2eb-127">Instans resurs-ID</span><span class="sxs-lookup"><span data-stu-id="fc2eb-127">The instance resource id</span></span>

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

### <span data-ttu-id="fc2eb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc2eb-128">-ResourceGroupName</span></span>
<span data-ttu-id="fc2eb-129">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="fc2eb-129">The Resource Group Name</span></span>

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

### <span data-ttu-id="fc2eb-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fc2eb-130">-Confirm</span></span>
<span data-ttu-id="fc2eb-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fc2eb-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc2eb-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc2eb-132">-WhatIf</span></span>
<span data-ttu-id="fc2eb-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fc2eb-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc2eb-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fc2eb-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc2eb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc2eb-135">CommonParameters</span></span>
<span data-ttu-id="fc2eb-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc2eb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc2eb-137">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fc2eb-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc2eb-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fc2eb-138">INPUTS</span></span>

### <span data-ttu-id="fc2eb-139">Microsoft. Azure. commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="fc2eb-139">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="fc2eb-140">System. String</span><span class="sxs-lookup"><span data-stu-id="fc2eb-140">System.String</span></span>

## <span data-ttu-id="fc2eb-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fc2eb-141">OUTPUTS</span></span>

### <span data-ttu-id="fc2eb-142">Microsoft. Azure. commands. SQL. TransparentDataEncryption. Model. AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="fc2eb-142">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="fc2eb-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fc2eb-143">NOTES</span></span>

## <span data-ttu-id="fc2eb-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fc2eb-144">RELATED LINKS</span></span>
