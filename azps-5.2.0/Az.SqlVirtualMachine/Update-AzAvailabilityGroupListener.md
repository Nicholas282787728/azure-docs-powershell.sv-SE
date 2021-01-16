---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/update-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzAvailabilityGroupListener.md
ms.openlocfilehash: 6c44a2fc7193acaadcf24ac311b5eb4b4a00b7d0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394027"
---
# <span data-ttu-id="3f113-101">Update-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="3f113-101">Update-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="3f113-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3f113-102">SYNOPSIS</span></span>
<span data-ttu-id="3f113-103">Uppdaterar tillgänglighets gruppens lyssnare.</span><span class="sxs-lookup"><span data-stu-id="3f113-103">Updates the Availability Group Listener.</span></span>

## <span data-ttu-id="3f113-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3f113-104">SYNTAX</span></span>

### <span data-ttu-id="3f113-105">Namn (standard)</span><span class="sxs-lookup"><span data-stu-id="3f113-105">Name (Default)</span></span>
```
Update-AzAvailabilityGroupListener [-SqlVirtualMachineId <String[]>] [-AsJob] [-ResourceGroupName] <String>
 [-SqlVMGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3f113-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="3f113-106">InputObject</span></span>
```
Update-AzAvailabilityGroupListener [-InputObject] <AzureAvailabilityGroupListenerModel>
 [-SqlVirtualMachineId <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3f113-107">ID</span><span class="sxs-lookup"><span data-stu-id="3f113-107">ResourceId</span></span>
```
Update-AzAvailabilityGroupListener [-ResourceId] <String> [-SqlVirtualMachineId <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f113-108">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="3f113-108">SqlVmGroupObject</span></span>
```
Update-AzAvailabilityGroupListener [-SqlVirtualMachineId <String[]>] [-AsJob]
 [-SqlVMGroupObject] <AzureSqlVMGroupModel> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f113-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3f113-109">DESCRIPTION</span></span>
<span data-ttu-id="3f113-110">Update-AzAvailabilityGroupListener cmdlet uppdaterar en tillgänglighets grupps lyssnare.</span><span class="sxs-lookup"><span data-stu-id="3f113-110">The Update-AzAvailabilityGroupListener cmdlet updates an Availability Group Listener.</span></span>

## <span data-ttu-id="3f113-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3f113-111">EXAMPLES</span></span>

### <span data-ttu-id="3f113-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3f113-112">Example 1</span></span>
```powershell
PS C:\> Update-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -Name AgListener01 -SqlVirtualMachineId $VmResourceId01,$VmResourceId02
```

<span data-ttu-id="3f113-113">Name ResourceGroupName grupp namn AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="3f113-113">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="3f113-114">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="3f113-114">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="3f113-115">Uppdaterar listan med SQL-filer för tillgänglighets gruppen.</span><span class="sxs-lookup"><span data-stu-id="3f113-115">Updates the list SQL Virtual Machines for the Availability Group Listener.</span></span>

## <span data-ttu-id="3f113-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3f113-116">PARAMETERS</span></span>

### <span data-ttu-id="3f113-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3f113-117">-AsJob</span></span>
<span data-ttu-id="3f113-118">Kör cmdleten i bakgrunden.</span><span class="sxs-lookup"><span data-stu-id="3f113-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="3f113-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f113-119">-DefaultProfile</span></span>
<span data-ttu-id="3f113-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3f113-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f113-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f113-121">-InputObject</span></span>
<span data-ttu-id="3f113-122">Tillgänglighets gruppens lyssnar objekt.</span><span class="sxs-lookup"><span data-stu-id="3f113-122">Availability Group Listener object.</span></span>

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

### <span data-ttu-id="3f113-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="3f113-123">-Name</span></span>
<span data-ttu-id="3f113-124">Tillgänglighets gruppens lyssnar namn.</span><span class="sxs-lookup"><span data-stu-id="3f113-124">Availability Group Listener name.</span></span>

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

### <span data-ttu-id="3f113-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f113-125">-ResourceGroupName</span></span>
<span data-ttu-id="3f113-126">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3f113-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="3f113-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f113-127">-ResourceId</span></span>
<span data-ttu-id="3f113-128">Tillgänglighets gruppens resurs-ID</span><span class="sxs-lookup"><span data-stu-id="3f113-128">Availability Group Listener Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: AvailabilityGroupListenerId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f113-129">-SqlVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="3f113-129">-SqlVirtualMachineId</span></span>
<span data-ttu-id="3f113-130">Lista över SQL-resurs-ID: n</span><span class="sxs-lookup"><span data-stu-id="3f113-130">List of Sql VM Resource IDs</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f113-131">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="3f113-131">-SqlVMGroupName</span></span>
<span data-ttu-id="3f113-132">Namn på en virtuell dator i SQL.</span><span class="sxs-lookup"><span data-stu-id="3f113-132">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="3f113-133">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="3f113-133">-SqlVMGroupObject</span></span>
<span data-ttu-id="3f113-134">SQL Virtual Machine-gruppobjekt.</span><span class="sxs-lookup"><span data-stu-id="3f113-134">SQL virtual machine Group object.</span></span>

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

### <span data-ttu-id="3f113-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3f113-135">-Confirm</span></span>
<span data-ttu-id="3f113-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3f113-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f113-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f113-137">-WhatIf</span></span>
<span data-ttu-id="3f113-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3f113-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f113-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3f113-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f113-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f113-140">CommonParameters</span></span>
<span data-ttu-id="3f113-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f113-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f113-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3f113-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f113-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3f113-143">INPUTS</span></span>

### <span data-ttu-id="3f113-144">Microsoft. Azure. commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="3f113-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

### <span data-ttu-id="3f113-145">System. String</span><span class="sxs-lookup"><span data-stu-id="3f113-145">System.String</span></span>

### <span data-ttu-id="3f113-146">Microsoft. Azure. commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="3f113-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="3f113-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3f113-147">OUTPUTS</span></span>

### <span data-ttu-id="3f113-148">Microsoft. Azure. commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="3f113-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="3f113-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3f113-149">NOTES</span></span>

## <span data-ttu-id="3f113-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3f113-150">RELATED LINKS</span></span>
