---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/update-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVM.md
ms.openlocfilehash: ce700b90194e1cd0fcdf05162696ae980d24ad01
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091913"
---
# <span data-ttu-id="7053f-101">Update-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="7053f-101">Update-AzSqlVM</span></span>

## <span data-ttu-id="7053f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7053f-102">SYNOPSIS</span></span>
<span data-ttu-id="7053f-103">Uppdaterar en virtuell SQL-dator.</span><span class="sxs-lookup"><span data-stu-id="7053f-103">Updates a sql virtual machine.</span></span>

## <span data-ttu-id="7053f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7053f-104">SYNTAX</span></span>

### <span data-ttu-id="7053f-105">NameParamaterList (standard)</span><span class="sxs-lookup"><span data-stu-id="7053f-105">NameParamaterList (Default)</span></span>
```
Update-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-LicenseType <String>] [-Offer <String>]
 [-Sku <String>] [-SqlManagementType <String>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7053f-106">NameInputObject</span><span class="sxs-lookup"><span data-stu-id="7053f-106">NameInputObject</span></span>
```
Update-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-InputObject] <AzureSqlVMModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7053f-107">ResourceIdParamaterList</span><span class="sxs-lookup"><span data-stu-id="7053f-107">ResourceIdParamaterList</span></span>
```
Update-AzSqlVM [-LicenseType <String>] [-Offer <String>] [-Sku <String>] [-SqlManagementType <String>]
 [-Tag <Hashtable>] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7053f-108">ResourceIdInputObject</span><span class="sxs-lookup"><span data-stu-id="7053f-108">ResourceIdInputObject</span></span>
```
Update-AzSqlVM [-InputObject] <AzureSqlVMModel> [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7053f-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7053f-109">DESCRIPTION</span></span>
<span data-ttu-id="7053f-110">Update-AzSqlVM cmdlet uppdaterar en virtuell SQL-dator.</span><span class="sxs-lookup"><span data-stu-id="7053f-110">The Update-AzSqlVM cmdlet updates a sql virtual machine.</span></span>

## <span data-ttu-id="7053f-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7053f-111">EXAMPLES</span></span>

### <span data-ttu-id="7053f-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7053f-112">Example 1</span></span>
```powershell
PS C:\> $tags = @{'key'='value'}
PS C:\> $vm = Update-AzSqlVM -InputObject $vm -Tags $tags
PS C:\> $group.Tags
Name                           Value
----                           -----
key                            value
```

<span data-ttu-id="7053f-113">Uppdaterar taggarna för en virtuell SQL-dator.</span><span class="sxs-lookup"><span data-stu-id="7053f-113">Updates the tags of a sql virtual machine.</span></span>

## <span data-ttu-id="7053f-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7053f-114">PARAMETERS</span></span>

### <span data-ttu-id="7053f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7053f-115">-AsJob</span></span>
<span data-ttu-id="7053f-116">Kör cmdleten i bakgrunden.</span><span class="sxs-lookup"><span data-stu-id="7053f-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="7053f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7053f-117">-DefaultProfile</span></span>
<span data-ttu-id="7053f-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7053f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7053f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7053f-119">-InputObject</span></span>
<span data-ttu-id="7053f-120">SQL Virtual Machine-objekt.</span><span class="sxs-lookup"><span data-stu-id="7053f-120">SQL virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel
Parameter Sets: NameInputObject, ResourceIdInputObject
Aliases: SqlVM

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7053f-121">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="7053f-121">-LicenseType</span></span>
<span data-ttu-id="7053f-122">Licens typ för SQL Virtual Machine.</span><span class="sxs-lookup"><span data-stu-id="7053f-122">SQL virtual machine license type.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList, ResourceIdParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7053f-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="7053f-123">-Name</span></span>
<span data-ttu-id="7053f-124">Namn på SQL-dator.</span><span class="sxs-lookup"><span data-stu-id="7053f-124">SQL virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList, NameInputObject
Aliases: SqlVMName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7053f-125">-Ge</span><span class="sxs-lookup"><span data-stu-id="7053f-125">-Offer</span></span>
<span data-ttu-id="7053f-126">Utbud av virtuell SQL-dator.</span><span class="sxs-lookup"><span data-stu-id="7053f-126">SQL virtual machine offer.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList, ResourceIdParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7053f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7053f-127">-ResourceGroupName</span></span>
<span data-ttu-id="7053f-128">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="7053f-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList, NameInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7053f-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7053f-129">-ResourceId</span></span>
<span data-ttu-id="7053f-130">Resurs-ID för virtuell dator i SQL.</span><span class="sxs-lookup"><span data-stu-id="7053f-130">SQL virtual machine resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParamaterList, ResourceIdInputObject
Aliases: SqlVMId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7053f-131">-SKU</span><span class="sxs-lookup"><span data-stu-id="7053f-131">-Sku</span></span>
<span data-ttu-id="7053f-132">Typ av SQL Virtual Machine-version.</span><span class="sxs-lookup"><span data-stu-id="7053f-132">SQL virtual machine edition type.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList, ResourceIdParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7053f-133">-SqlManagementType</span><span class="sxs-lookup"><span data-stu-id="7053f-133">-SqlManagementType</span></span>
<span data-ttu-id="7053f-134">Hanterings typ för SQL virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="7053f-134">SQL virtual machine management type.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList, ResourceIdParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7053f-135">-Tagg</span><span class="sxs-lookup"><span data-stu-id="7053f-135">-Tag</span></span>
<span data-ttu-id="7053f-136">De taggar som ska kopplas till den virtuella SQL-datorn</span><span class="sxs-lookup"><span data-stu-id="7053f-136">The tags to associate with the SQL virtual machine</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: NameParamaterList, ResourceIdParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7053f-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7053f-137">-Confirm</span></span>
<span data-ttu-id="7053f-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7053f-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7053f-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7053f-139">-WhatIf</span></span>
<span data-ttu-id="7053f-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7053f-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7053f-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7053f-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7053f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7053f-142">CommonParameters</span></span>
<span data-ttu-id="7053f-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7053f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7053f-144">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7053f-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7053f-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7053f-145">INPUTS</span></span>

### <span data-ttu-id="7053f-146">Microsoft. Azure. commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="7053f-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="7053f-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7053f-147">OUTPUTS</span></span>

### <span data-ttu-id="7053f-148">Microsoft. Azure. commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="7053f-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="7053f-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7053f-149">NOTES</span></span>

## <span data-ttu-id="7053f-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7053f-150">RELATED LINKS</span></span>
