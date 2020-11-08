---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzAvailabilityGroupListener.md
ms.openlocfilehash: af36c7cae36cb3d6bdb9bf2760b9a8299463e877
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94100767"
---
# <span data-ttu-id="d28b0-101">New-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="d28b0-101">New-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="d28b0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d28b0-102">SYNOPSIS</span></span>
<span data-ttu-id="d28b0-103">Skapar en ny lyssnare för tillgänglighets grupp.</span><span class="sxs-lookup"><span data-stu-id="d28b0-103">Creates a new Availability Group Listener.</span></span>

## <span data-ttu-id="d28b0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d28b0-104">SYNTAX</span></span>

### <span data-ttu-id="d28b0-105">Namn (standard)</span><span class="sxs-lookup"><span data-stu-id="d28b0-105">Name (Default)</span></span>
```
New-AzAvailabilityGroupListener -AvailabilityGroupName <String> [-Port <Int32>]
 -LoadBalancerResourceId <String> [-IpAddress <String>] [-SubnetId <String>] -ProbePort <Int32>
 [-PublicIpAddressResourceId <String>] [-AsJob] -SqlVirtualMachineId <String[]> [-ResourceGroupName] <String>
 [-SqlVMGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d28b0-106">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="d28b0-106">SqlVmGroupObject</span></span>
```
New-AzAvailabilityGroupListener -AvailabilityGroupName <String> [-Port <Int32>]
 -LoadBalancerResourceId <String> [-IpAddress <String>] [-SubnetId <String>] -ProbePort <Int32>
 [-PublicIpAddressResourceId <String>] [-AsJob] -SqlVirtualMachineId <String[]>
 [-SqlVMGroupObject] <AzureSqlVMGroupModel> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d28b0-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d28b0-107">DESCRIPTION</span></span>
<span data-ttu-id="d28b0-108">New-AzAvailabilityGroupListener-cmdleten skapar en ny lyssnar grupp.</span><span class="sxs-lookup"><span data-stu-id="d28b0-108">The New-AzAvailabilityGroupListener cmdlet creates a new Availability Group Listener.</span></span>

## <span data-ttu-id="d28b0-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d28b0-109">EXAMPLES</span></span>

### <span data-ttu-id="d28b0-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d28b0-110">Example 1</span></span>
```powershell
PS C:\> New-AzAvailabilityGroupListener -AvailabilityGroupName AvailabilityGroup01 -LoadBalancerResourceId $LoadBalanceResourceId -SubnetId $SubnetId -ProbePort 59999 -SqlVirtualMachineId $VmResourceId1,$VmResourceId2 -Name AgListener01  -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -IpAddress 10.0.0.3
```

<span data-ttu-id="d28b0-111">Name ResourceGroupName grupp namn AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="d28b0-111">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="d28b0-112">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="d28b0-112">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="d28b0-113">Skapar en ny lyssnar AgListener01 för tillgänglighets grupps AvailabilityGroup01 i SQL Virtual Machine Group-SqlVmGroup01.</span><span class="sxs-lookup"><span data-stu-id="d28b0-113">Creates a new Availability Group Listener AgListener01 for the Availability Group AvailabilityGroup01 in SQL Virtual Machine Group SqlVmGroup01.</span></span>

## <span data-ttu-id="d28b0-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d28b0-114">PARAMETERS</span></span>

### <span data-ttu-id="d28b0-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d28b0-115">-AsJob</span></span>
<span data-ttu-id="d28b0-116">Kör cmdleten i bakgrunden.</span><span class="sxs-lookup"><span data-stu-id="d28b0-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="d28b0-117">-AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="d28b0-117">-AvailabilityGroupName</span></span>
<span data-ttu-id="d28b0-118">Tillgänglighets grupp namn.</span><span class="sxs-lookup"><span data-stu-id="d28b0-118">Availability Group name.</span></span>

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

### <span data-ttu-id="d28b0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d28b0-119">-DefaultProfile</span></span>
<span data-ttu-id="d28b0-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d28b0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d28b0-121">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="d28b0-121">-IpAddress</span></span>
<span data-ttu-id="d28b0-122">Privat IP-adress</span><span class="sxs-lookup"><span data-stu-id="d28b0-122">Private Ip Address</span></span>

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

### <span data-ttu-id="d28b0-123">-LoadBalancerResourceId</span><span class="sxs-lookup"><span data-stu-id="d28b0-123">-LoadBalancerResourceId</span></span>
<span data-ttu-id="d28b0-124">ID för belastnings utjämning</span><span class="sxs-lookup"><span data-stu-id="d28b0-124">Load Balancer Id</span></span>

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

### <span data-ttu-id="d28b0-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="d28b0-125">-Name</span></span>
<span data-ttu-id="d28b0-126">Tillgänglighets gruppens lyssnar namn.</span><span class="sxs-lookup"><span data-stu-id="d28b0-126">Availability Group Listener name.</span></span>

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

### <span data-ttu-id="d28b0-127">-Port</span><span class="sxs-lookup"><span data-stu-id="d28b0-127">-Port</span></span>
<span data-ttu-id="d28b0-128">Port nummer för AG-lyssnare.</span><span class="sxs-lookup"><span data-stu-id="d28b0-128">Port number of AG Listener.</span></span> <span data-ttu-id="d28b0-129">Standardvärdet är 1433.</span><span class="sxs-lookup"><span data-stu-id="d28b0-129">Default Value is 1433.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d28b0-130">-ProbePort</span><span class="sxs-lookup"><span data-stu-id="d28b0-130">-ProbePort</span></span>
<span data-ttu-id="d28b0-131">Avsök port</span><span class="sxs-lookup"><span data-stu-id="d28b0-131">Probe Port</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d28b0-132">-PublicIpAddressResourceId</span><span class="sxs-lookup"><span data-stu-id="d28b0-132">-PublicIpAddressResourceId</span></span>
<span data-ttu-id="d28b0-133">Resurs-ID för offentlig IP-adress</span><span class="sxs-lookup"><span data-stu-id="d28b0-133">Public Ip Address Resource Id</span></span>

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

### <span data-ttu-id="d28b0-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d28b0-134">-ResourceGroupName</span></span>
<span data-ttu-id="d28b0-135">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d28b0-135">The name of the resource group.</span></span>

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

### <span data-ttu-id="d28b0-136">-SqlVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="d28b0-136">-SqlVirtualMachineId</span></span>
<span data-ttu-id="d28b0-137">Lista över SQL-resurs-ID: n</span><span class="sxs-lookup"><span data-stu-id="d28b0-137">List of Sql VM Resource IDs</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d28b0-138">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="d28b0-138">-SqlVMGroupName</span></span>
<span data-ttu-id="d28b0-139">Namn på en virtuell dator i SQL.</span><span class="sxs-lookup"><span data-stu-id="d28b0-139">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="d28b0-140">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="d28b0-140">-SqlVMGroupObject</span></span>
<span data-ttu-id="d28b0-141">SQL Virtual Machine-gruppobjekt.</span><span class="sxs-lookup"><span data-stu-id="d28b0-141">SQL virtual machine Group object.</span></span>

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

### <span data-ttu-id="d28b0-142">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="d28b0-142">-SubnetId</span></span>
<span data-ttu-id="d28b0-143">ID för under nätet</span><span class="sxs-lookup"><span data-stu-id="d28b0-143">Subnet Resource Id</span></span>

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

### <span data-ttu-id="d28b0-144">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d28b0-144">-Confirm</span></span>
<span data-ttu-id="d28b0-145">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d28b0-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d28b0-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d28b0-146">-WhatIf</span></span>
<span data-ttu-id="d28b0-147">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d28b0-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d28b0-148">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d28b0-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d28b0-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d28b0-149">CommonParameters</span></span>
<span data-ttu-id="d28b0-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d28b0-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d28b0-151">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d28b0-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d28b0-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d28b0-152">INPUTS</span></span>

### <span data-ttu-id="d28b0-153">Microsoft. Azure. commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="d28b0-153">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="d28b0-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d28b0-154">OUTPUTS</span></span>

### <span data-ttu-id="d28b0-155">Microsoft. Azure. commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="d28b0-155">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="d28b0-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d28b0-156">NOTES</span></span>

## <span data-ttu-id="d28b0-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d28b0-157">RELATED LINKS</span></span>
