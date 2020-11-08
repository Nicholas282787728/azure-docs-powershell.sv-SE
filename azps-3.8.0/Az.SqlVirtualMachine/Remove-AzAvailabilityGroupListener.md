---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/remove-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzAvailabilityGroupListener.md
ms.openlocfilehash: d147fcd53b27031949bf51a33a59a9db86687d57
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93926974"
---
# <span data-ttu-id="c8514-101">Remove-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="c8514-101">Remove-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="c8514-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c8514-102">SYNOPSIS</span></span>
<span data-ttu-id="c8514-103">Tar bort en tillgänglighets grupps lyssnare.</span><span class="sxs-lookup"><span data-stu-id="c8514-103">Deletes an Availability Group Listener.</span></span>

## <span data-ttu-id="c8514-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c8514-104">SYNTAX</span></span>

### <span data-ttu-id="c8514-105">Namn (standard)</span><span class="sxs-lookup"><span data-stu-id="c8514-105">Name (Default)</span></span>
```
Remove-AzAvailabilityGroupListener [-AsJob] [-PassThru] [-ResourceGroupName] <String>
 [-SqlVMGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c8514-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="c8514-106">InputObject</span></span>
```
Remove-AzAvailabilityGroupListener [-InputObject] <AzureAvailabilityGroupListenerModel> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8514-107">ID</span><span class="sxs-lookup"><span data-stu-id="c8514-107">ResourceId</span></span>
```
Remove-AzAvailabilityGroupListener [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8514-108">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="c8514-108">SqlVmGroupObject</span></span>
```
Remove-AzAvailabilityGroupListener [-AsJob] [-PassThru] [-SqlVMGroupObject] <AzureSqlVMGroupModel>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8514-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c8514-109">DESCRIPTION</span></span>
<span data-ttu-id="c8514-110">Remove-AzAvailabilityGroupListener-cmdleten tar bort en tillgänglighets grupp.</span><span class="sxs-lookup"><span data-stu-id="c8514-110">The Remove-AzAvailabilityGroupListener cmdlet deletes an Availability Group Listener.</span></span>

## <span data-ttu-id="c8514-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c8514-111">EXAMPLES</span></span>

### <span data-ttu-id="c8514-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c8514-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -Name AgListener01
```

<span data-ttu-id="c8514-113">Name ResourceGroupName grupp namn AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="c8514-113">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="c8514-114">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="c8514-114">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="c8514-115">Tar bort tillgänglighets gruppens lyssnar-AgListener01 i tillgänglighets gruppen AvailabilityGroup01.</span><span class="sxs-lookup"><span data-stu-id="c8514-115">Deletes the Availability Group Listener AgListener01 in the Availability Group AvailabilityGroup01.</span></span>

## <span data-ttu-id="c8514-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c8514-116">PARAMETERS</span></span>

### <span data-ttu-id="c8514-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c8514-117">-AsJob</span></span>
<span data-ttu-id="c8514-118">Kör cmdleten i bakgrunden.</span><span class="sxs-lookup"><span data-stu-id="c8514-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="c8514-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8514-119">-DefaultProfile</span></span>
<span data-ttu-id="c8514-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c8514-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8514-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c8514-121">-InputObject</span></span>
<span data-ttu-id="c8514-122">Tillgänglighets gruppens lyssnar objekt.</span><span class="sxs-lookup"><span data-stu-id="c8514-122">Availability Group Listener object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c8514-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="c8514-123">-Name</span></span>
<span data-ttu-id="c8514-124">Tillgänglighets gruppens lyssnar namn.</span><span class="sxs-lookup"><span data-stu-id="c8514-124">Availability Group Listener name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, SqlVmGroupObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8514-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c8514-125">-PassThru</span></span>
<span data-ttu-id="c8514-126">Anger om den borttagna resursen ska matas ut i slutet av cmdlet-körningen.</span><span class="sxs-lookup"><span data-stu-id="c8514-126">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="c8514-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8514-127">-ResourceGroupName</span></span>
<span data-ttu-id="c8514-128">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="c8514-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="c8514-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c8514-129">-ResourceId</span></span>
<span data-ttu-id="c8514-130">Tillgänglighets gruppens resurs-ID</span><span class="sxs-lookup"><span data-stu-id="c8514-130">Availability Group Listener Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8514-131">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="c8514-131">-SqlVMGroupName</span></span>
<span data-ttu-id="c8514-132">Namn på en virtuell dator i SQL.</span><span class="sxs-lookup"><span data-stu-id="c8514-132">SQL virtual machine group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: GroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8514-133">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="c8514-133">-SqlVMGroupObject</span></span>
<span data-ttu-id="c8514-134">SQL Virtual Machine-gruppobjekt.</span><span class="sxs-lookup"><span data-stu-id="c8514-134">SQL virtual machine Group object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel
Parameter Sets: SqlVmGroupObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c8514-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c8514-135">-Confirm</span></span>
<span data-ttu-id="c8514-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c8514-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8514-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8514-137">-WhatIf</span></span>
<span data-ttu-id="c8514-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c8514-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8514-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c8514-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8514-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8514-140">CommonParameters</span></span>
<span data-ttu-id="c8514-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8514-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8514-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c8514-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8514-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c8514-143">INPUTS</span></span>

### <span data-ttu-id="c8514-144">Microsoft. Azure. commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="c8514-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

### <span data-ttu-id="c8514-145">System. String</span><span class="sxs-lookup"><span data-stu-id="c8514-145">System.String</span></span>

### <span data-ttu-id="c8514-146">Microsoft. Azure. commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="c8514-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="c8514-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c8514-147">OUTPUTS</span></span>

### <span data-ttu-id="c8514-148">Microsoft. Azure. commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="c8514-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="c8514-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c8514-149">NOTES</span></span>

## <span data-ttu-id="c8514-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c8514-150">RELATED LINKS</span></span>