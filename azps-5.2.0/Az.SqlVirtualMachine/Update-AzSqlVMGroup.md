---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/update-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVMGroup.md
ms.openlocfilehash: 885be17315e0dc0be8223f0d28bc11a6d6e41146
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394040"
---
# <span data-ttu-id="55fd4-101">Update-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="55fd4-101">Update-AzSqlVMGroup</span></span>

## <span data-ttu-id="55fd4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="55fd4-102">SYNOPSIS</span></span>
<span data-ttu-id="55fd4-103">Uppdaterar en virtuell SQL-dator grupp.</span><span class="sxs-lookup"><span data-stu-id="55fd4-103">Updates a sql virtual machine group.</span></span>

## <span data-ttu-id="55fd4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="55fd4-104">SYNTAX</span></span>

### <span data-ttu-id="55fd4-105">Namn (standard)</span><span class="sxs-lookup"><span data-stu-id="55fd4-105">Name (Default)</span></span>
```
Update-AzSqlVMGroup [-AsJob] [-ClusterOperatorAccount <String>] [-SqlServiceAccount <String>]
 [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>] [-DomainFqdn <String>]
 [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>] [-Tag <Hashtable>]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="55fd4-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="55fd4-106">InputObject</span></span>
```
Update-AzSqlVMGroup [-InputObject] <AzureSqlVMGroupModel> [-AsJob] [-ClusterOperatorAccount <String>]
 [-SqlServiceAccount <String>] [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>]
 [-DomainFqdn <String>] [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55fd4-107">ID</span><span class="sxs-lookup"><span data-stu-id="55fd4-107">ResourceId</span></span>
```
Update-AzSqlVMGroup [-ResourceId] <String> [-AsJob] [-ClusterOperatorAccount <String>]
 [-SqlServiceAccount <String>] [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>]
 [-DomainFqdn <String>] [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55fd4-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="55fd4-108">DESCRIPTION</span></span>
<span data-ttu-id="55fd4-109">Update-AzSqlVMGroup cmdlet uppdaterar en virtuell SQL-dator grupp.</span><span class="sxs-lookup"><span data-stu-id="55fd4-109">The Update-AzSqlVMGroup cmdlet updates a sql virtual machine group.</span></span>

## <span data-ttu-id="55fd4-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="55fd4-110">EXAMPLES</span></span>

### <span data-ttu-id="55fd4-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="55fd4-111">Example 1</span></span>
```powershell
PS C:\> $tags = @{'key'='value'}
PS C:\> $group = Update-AzSqlVMGroup -InputObject $group -Tags $tags
PS C:\> $group.Tags
Name                           Value
----                           -----
key                            value
```

<span data-ttu-id="55fd4-112">Uppdaterar taggarna för en virtuell SQL-gruppgrupp.</span><span class="sxs-lookup"><span data-stu-id="55fd4-112">Updates the tags of a sql virtual machine group.</span></span>

## <span data-ttu-id="55fd4-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="55fd4-113">PARAMETERS</span></span>

### <span data-ttu-id="55fd4-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="55fd4-114">-AsJob</span></span>
<span data-ttu-id="55fd4-115">Kör cmdleten i bakgrunden.</span><span class="sxs-lookup"><span data-stu-id="55fd4-115">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="55fd4-116">-ClusterBootstrapAccount</span><span class="sxs-lookup"><span data-stu-id="55fd4-116">-ClusterBootstrapAccount</span></span>
<span data-ttu-id="55fd4-117">Namn som används för att skapa kluster</span><span class="sxs-lookup"><span data-stu-id="55fd4-117">Name used for creating cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55fd4-118">-ClusterOperatorAccount</span><span class="sxs-lookup"><span data-stu-id="55fd4-118">-ClusterOperatorAccount</span></span>
<span data-ttu-id="55fd4-119">Namn som används för operativ kluster</span><span class="sxs-lookup"><span data-stu-id="55fd4-119">Name used for operating cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55fd4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55fd4-120">-DefaultProfile</span></span>
<span data-ttu-id="55fd4-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="55fd4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55fd4-122">-DomainFqdn</span><span class="sxs-lookup"><span data-stu-id="55fd4-122">-DomainFqdn</span></span>
<span data-ttu-id="55fd4-123">Fullständigt kvalificerat namn på domänen</span><span class="sxs-lookup"><span data-stu-id="55fd4-123">Fully qualified name of the domain</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55fd4-124">-FileShareWitnessPath</span><span class="sxs-lookup"><span data-stu-id="55fd4-124">-FileShareWitnessPath</span></span>
<span data-ttu-id="55fd4-125">Valfri sökväg för fileshare-vittne</span><span class="sxs-lookup"><span data-stu-id="55fd4-125">Optional path for fileshare witness</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55fd4-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="55fd4-126">-InputObject</span></span>
<span data-ttu-id="55fd4-127">SQL Virtual Machine-objekt.</span><span class="sxs-lookup"><span data-stu-id="55fd4-127">SQL virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel
Parameter Sets: InputObject
Aliases: SqlVMGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55fd4-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="55fd4-128">-Name</span></span>
<span data-ttu-id="55fd4-129">Namn på en virtuell dator i SQL.</span><span class="sxs-lookup"><span data-stu-id="55fd4-129">SQL virtual machine group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: SqlVMGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55fd4-130">-OuPath</span><span class="sxs-lookup"><span data-stu-id="55fd4-130">-OuPath</span></span>
<span data-ttu-id="55fd4-131">Sökväg till Organisationsenhet där noder och kluster visas</span><span class="sxs-lookup"><span data-stu-id="55fd4-131">Organizational Unit path in which the nodes and cluster will be present</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55fd4-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55fd4-132">-ResourceGroupName</span></span>
<span data-ttu-id="55fd4-133">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="55fd4-133">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55fd4-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="55fd4-134">-ResourceId</span></span>
<span data-ttu-id="55fd4-135">Grupp-ID för virtuell dator i SQL.</span><span class="sxs-lookup"><span data-stu-id="55fd4-135">SQL virtual machine group resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: SqlVMGroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55fd4-136">-SqlServiceAccount</span><span class="sxs-lookup"><span data-stu-id="55fd4-136">-SqlServiceAccount</span></span>
<span data-ttu-id="55fd4-137">Det namn som SQL-tjänsten körs på för alla deltagande SQL-datorer i klustret</span><span class="sxs-lookup"><span data-stu-id="55fd4-137">Name under which SQL service will run on all participating SQL virtual machines in the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55fd4-138">-StorageAccountPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="55fd4-138">-StorageAccountPrimaryKey</span></span>
<span data-ttu-id="55fd4-139">Primärt för vittnes lagrings kontot</span><span class="sxs-lookup"><span data-stu-id="55fd4-139">Primary key of the witness storage account</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55fd4-140">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="55fd4-140">-StorageAccountUrl</span></span>
<span data-ttu-id="55fd4-141">Primärt för vittnes lagrings kontot</span><span class="sxs-lookup"><span data-stu-id="55fd4-141">Primary key of the witness storage account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55fd4-142">-Tagg</span><span class="sxs-lookup"><span data-stu-id="55fd4-142">-Tag</span></span>
<span data-ttu-id="55fd4-143">De taggar som ska kopplas till den virtuella SQL-gruppen.</span><span class="sxs-lookup"><span data-stu-id="55fd4-143">The tags to associate with the SQL virtual machine group.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55fd4-144">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="55fd4-144">-Confirm</span></span>
<span data-ttu-id="55fd4-145">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="55fd4-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55fd4-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55fd4-146">-WhatIf</span></span>
<span data-ttu-id="55fd4-147">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="55fd4-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55fd4-148">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="55fd4-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55fd4-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55fd4-149">CommonParameters</span></span>
<span data-ttu-id="55fd4-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55fd4-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55fd4-151">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="55fd4-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55fd4-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="55fd4-152">INPUTS</span></span>

### <span data-ttu-id="55fd4-153">Microsoft. Azure. commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="55fd4-153">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

### <span data-ttu-id="55fd4-154">System. String</span><span class="sxs-lookup"><span data-stu-id="55fd4-154">System.String</span></span>

## <span data-ttu-id="55fd4-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="55fd4-155">OUTPUTS</span></span>

### <span data-ttu-id="55fd4-156">Microsoft. Azure. commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="55fd4-156">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="55fd4-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="55fd4-157">NOTES</span></span>

## <span data-ttu-id="55fd4-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="55fd4-158">RELATED LINKS</span></span>
