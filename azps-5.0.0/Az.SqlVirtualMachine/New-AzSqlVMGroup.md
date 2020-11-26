---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMGroup.md
ms.openlocfilehash: 0cd409f530225b2fadf104f787a1e926b5f8fb16
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322052"
---
# <span data-ttu-id="b624b-101">New-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="b624b-101">New-AzSqlVMGroup</span></span>

## <span data-ttu-id="b624b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b624b-102">SYNOPSIS</span></span>
<span data-ttu-id="b624b-103">Skapar en ny virtuell SQL-dator grupp.</span><span class="sxs-lookup"><span data-stu-id="b624b-103">Creates a new sql virtual machine group.</span></span>

## <span data-ttu-id="b624b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b624b-104">SYNTAX</span></span>

```
New-AzSqlVMGroup [-Location] <String> -Offer <String> -Sku <String> -ClusterOperatorAccount <String>
 -SqlServiceAccount <String> -StorageAccountUrl <String> -StorageAccountPrimaryKey <SecureString>
 -DomainFqdn <String> [-AsJob] [-OuPath <String>] [-FileShareWitnessPath <String>]
 [-ClusterBootstrapAccount <String>] [-Tag <Hashtable>] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b624b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b624b-105">DESCRIPTION</span></span>
<span data-ttu-id="b624b-106">New-AzSqlVMGroup cmdlet skapar en virtuell Azure SQL-dator grupp.</span><span class="sxs-lookup"><span data-stu-id="b624b-106">The New-AzSqlVMGroup cmdlet creates an Azure SQL virtual machine group.</span></span>

## <span data-ttu-id="b624b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b624b-107">EXAMPLES</span></span>

### <span data-ttu-id="b624b-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b624b-108">Example 1</span></span>
```powershell
PS C:\> $secureKey = ConvertTo-SecureString $profile.StorageAccountPrimaryKey -AsPlainText -Force
PS C:\> New-AzSqlVMGroup $resourceGroupName $groupName $location -ClusterOperatorAccount $profile.ClusterOperatorAccount `
>>         -SqlServiceAccount $profile.SqlServiceAccount -StorageAccountUrl $profile.StorageAccountUrl `
>>         -StorageAccountPrimaryKey $secureKey -DomainFqdn $profile.DomainFqdn `
>>         -Offer 'SQL2017-WS2016' -Sku 'Developer'
Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
```

<span data-ttu-id="b624b-109">Skapar en ny virtuell dator grupp för Azure SQL med test-gruppdatorn i resurs gruppen ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="b624b-109">Creates a new Azure SQL virtual machine group with test-group vm in the resource group ResourceGroup01.</span></span>
<span data-ttu-id="b624b-110">$profile är ett objekt av typen Microsoft. Azure. Management. SqlVirtualMachine. Models. WsfcDomainProfile</span><span class="sxs-lookup"><span data-stu-id="b624b-110">$profile is an object of type Microsoft.Azure.Management.SqlVirtualMachine.Models.WsfcDomainProfile</span></span>

## <span data-ttu-id="b624b-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b624b-111">PARAMETERS</span></span>

### <span data-ttu-id="b624b-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b624b-112">-AsJob</span></span>
<span data-ttu-id="b624b-113">Kör cmdleten i bakgrunden.</span><span class="sxs-lookup"><span data-stu-id="b624b-113">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="b624b-114">-ClusterBootstrapAccount</span><span class="sxs-lookup"><span data-stu-id="b624b-114">-ClusterBootstrapAccount</span></span>
<span data-ttu-id="b624b-115">Namn som används för att skapa kluster</span><span class="sxs-lookup"><span data-stu-id="b624b-115">Name used for creating cluster</span></span>

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

### <span data-ttu-id="b624b-116">-ClusterOperatorAccount</span><span class="sxs-lookup"><span data-stu-id="b624b-116">-ClusterOperatorAccount</span></span>
<span data-ttu-id="b624b-117">Namn som används för operativ kluster</span><span class="sxs-lookup"><span data-stu-id="b624b-117">Name used for operating cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b624b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b624b-118">-DefaultProfile</span></span>
<span data-ttu-id="b624b-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b624b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b624b-120">-DomainFqdn</span><span class="sxs-lookup"><span data-stu-id="b624b-120">-DomainFqdn</span></span>
<span data-ttu-id="b624b-121">Fullständigt kvalificerat namn på domänen</span><span class="sxs-lookup"><span data-stu-id="b624b-121">Fully qualified name of the domain</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b624b-122">-FileShareWitnessPath</span><span class="sxs-lookup"><span data-stu-id="b624b-122">-FileShareWitnessPath</span></span>
<span data-ttu-id="b624b-123">Valfri sökväg för fileshare-vittne</span><span class="sxs-lookup"><span data-stu-id="b624b-123">Optional path for fileshare witness</span></span>

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

### <span data-ttu-id="b624b-124">-Plats</span><span class="sxs-lookup"><span data-stu-id="b624b-124">-Location</span></span>
<span data-ttu-id="b624b-125">Plats för virtuell dator grupp i SQL.</span><span class="sxs-lookup"><span data-stu-id="b624b-125">SQL virtual machine group location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b624b-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="b624b-126">-Name</span></span>
<span data-ttu-id="b624b-127">Namn på en virtuell dator i SQL.</span><span class="sxs-lookup"><span data-stu-id="b624b-127">SQL virtual machine group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SqlVMGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b624b-128">-Ge</span><span class="sxs-lookup"><span data-stu-id="b624b-128">-Offer</span></span>
<span data-ttu-id="b624b-129">Grupp för virtuell SQL-dator.</span><span class="sxs-lookup"><span data-stu-id="b624b-129">SQL virtual machine group offer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b624b-130">-OuPath</span><span class="sxs-lookup"><span data-stu-id="b624b-130">-OuPath</span></span>
<span data-ttu-id="b624b-131">Sökväg till Organisationsenhet där noder och kluster visas</span><span class="sxs-lookup"><span data-stu-id="b624b-131">Organizational Unit path in which the nodes and cluster will be present</span></span>

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

### <span data-ttu-id="b624b-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b624b-132">-ResourceGroupName</span></span>
<span data-ttu-id="b624b-133">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="b624b-133">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b624b-134">-SKU</span><span class="sxs-lookup"><span data-stu-id="b624b-134">-Sku</span></span>
<span data-ttu-id="b624b-135">Typ av virtuell SQL-dator-grupp.</span><span class="sxs-lookup"><span data-stu-id="b624b-135">SQL virtual machine group edition type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b624b-136">-SqlServiceAccount</span><span class="sxs-lookup"><span data-stu-id="b624b-136">-SqlServiceAccount</span></span>
<span data-ttu-id="b624b-137">Det namn som SQL-tjänsten körs på för alla deltagande SQL-datorer i klustret</span><span class="sxs-lookup"><span data-stu-id="b624b-137">Name under which SQL service will run on all participating SQL virtual machines in the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b624b-138">-StorageAccountPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="b624b-138">-StorageAccountPrimaryKey</span></span>
<span data-ttu-id="b624b-139">Primärt för vittnes lagrings kontot</span><span class="sxs-lookup"><span data-stu-id="b624b-139">Primary key of the witness storage account</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b624b-140">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="b624b-140">-StorageAccountUrl</span></span>
<span data-ttu-id="b624b-141">Primärt för vittnes lagrings kontot</span><span class="sxs-lookup"><span data-stu-id="b624b-141">Primary key of the witness storage account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b624b-142">-Tagg</span><span class="sxs-lookup"><span data-stu-id="b624b-142">-Tag</span></span>
<span data-ttu-id="b624b-143">De taggar som ska kopplas till den virtuella SQL-gruppen.</span><span class="sxs-lookup"><span data-stu-id="b624b-143">The tags to associate with the SQL virtual machine group.</span></span>

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

### <span data-ttu-id="b624b-144">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b624b-144">-Confirm</span></span>
<span data-ttu-id="b624b-145">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b624b-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b624b-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b624b-146">-WhatIf</span></span>
<span data-ttu-id="b624b-147">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b624b-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b624b-148">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b624b-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b624b-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b624b-149">CommonParameters</span></span>
<span data-ttu-id="b624b-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b624b-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b624b-151">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b624b-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b624b-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b624b-152">INPUTS</span></span>

### <span data-ttu-id="b624b-153">System. String</span><span class="sxs-lookup"><span data-stu-id="b624b-153">System.String</span></span>

## <span data-ttu-id="b624b-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b624b-154">OUTPUTS</span></span>

### <span data-ttu-id="b624b-155">Microsoft. Azure. commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="b624b-155">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="b624b-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b624b-156">NOTES</span></span>

## <span data-ttu-id="b624b-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b624b-157">RELATED LINKS</span></span>