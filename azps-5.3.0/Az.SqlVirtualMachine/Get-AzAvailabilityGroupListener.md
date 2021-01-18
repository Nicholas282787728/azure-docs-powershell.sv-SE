---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/get-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzAvailabilityGroupListener.md
ms.openlocfilehash: f1ba6e50c03fffbd4eb6407e90e2a50957806539
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522748"
---
# <span data-ttu-id="ff0b8-101">Get-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="ff0b8-101">Get-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="ff0b8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ff0b8-102">SYNOPSIS</span></span>
<span data-ttu-id="ff0b8-103">Få en eller flera lyssnare för tillgänglighets grupper i en virtuell SQL-dator grupp.</span><span class="sxs-lookup"><span data-stu-id="ff0b8-103">Get one or more Availability Group Listeners in a SQL Virtual Machine Group.</span></span>

## <span data-ttu-id="ff0b8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ff0b8-104">SYNTAX</span></span>

### <span data-ttu-id="ff0b8-105">Namn (standard)</span><span class="sxs-lookup"><span data-stu-id="ff0b8-105">Name (Default)</span></span>
```
Get-AzAvailabilityGroupListener [[-Name] <String>] [-ResourceGroupName] <String> [-SqlVMGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ff0b8-106">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="ff0b8-106">SqlVmGroupObject</span></span>
```
Get-AzAvailabilityGroupListener [[-Name] <String>] [-SqlVMGroupObject] <AzureSqlVMGroupModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ff0b8-107">ID</span><span class="sxs-lookup"><span data-stu-id="ff0b8-107">ResourceId</span></span>
```
Get-AzAvailabilityGroupListener [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ff0b8-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ff0b8-108">DESCRIPTION</span></span>
<span data-ttu-id="ff0b8-109">Get-AzAvailabilityGroupListener får en eller flera tillgänglighets grupp lyssnare från den virtuella SQL-gruppen.</span><span class="sxs-lookup"><span data-stu-id="ff0b8-109">The Get-AzAvailabilityGroupListener gets one or more Availability Group Listener from the SQL Virtual Machine Group.</span></span>

## <span data-ttu-id="ff0b8-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ff0b8-110">EXAMPLES</span></span>

### <span data-ttu-id="ff0b8-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ff0b8-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -Name AgListener01
```

<span data-ttu-id="ff0b8-112">Name ResourceGroupName grupp namn AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="ff0b8-112">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="ff0b8-113">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="ff0b8-113">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="ff0b8-114">Med det här kommandot får du information om tillgänglighets gruppens lyssnar-AgListener01 i gruppen SqlVmGroup01 och resurs grupp för SQL Virtual Machine.</span><span class="sxs-lookup"><span data-stu-id="ff0b8-114">This command gets information about the Availability Group Listener AgListener01 in the SQL Virtual Machine Group SqlVmGroup01 and Resource Group ResourceGroup01.</span></span>

### <span data-ttu-id="ff0b8-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="ff0b8-115">Example 2</span></span>
```powershell
PS C:\> Get-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01
```

<span data-ttu-id="ff0b8-116">Name ResourceGroupName grupp namn AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="ff0b8-116">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="ff0b8-117">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01 AgListener02 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="ff0b8-117">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01 AgListener02 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="ff0b8-118">Med det här kommandot får du information om alla lyssnare för tillgänglighets grupper i gruppen SqlVmGroup01 och resurs grupp för SQL Virtual Machine.</span><span class="sxs-lookup"><span data-stu-id="ff0b8-118">This command gets information about all Availability Group Listeners in the SQL Virtual Machine Group SqlVmGroup01 and Resource Group ResourceGroup01.</span></span>

### <span data-ttu-id="ff0b8-119">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="ff0b8-119">Example 3</span></span>
```powershell
PS C:\> $SqlVmGroupObject = Get-AzSqlVMGroup -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01
PS C:\> Get-AzAvailabilityGroupListener -Name AgListener01 -SqlVMGroupObject $SqlVmGroupObject
```

<span data-ttu-id="ff0b8-120">Name ResourceGroupName grupp namn AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="ff0b8-120">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="ff0b8-121">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="ff0b8-121">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

## <span data-ttu-id="ff0b8-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ff0b8-122">PARAMETERS</span></span>

### <span data-ttu-id="ff0b8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff0b8-123">-DefaultProfile</span></span>
<span data-ttu-id="ff0b8-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ff0b8-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff0b8-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="ff0b8-125">-Name</span></span>
<span data-ttu-id="ff0b8-126">Tillgänglighets gruppens lyssnar namn.</span><span class="sxs-lookup"><span data-stu-id="ff0b8-126">Availability Group Listener name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, SqlVmGroupObject
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff0b8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff0b8-127">-ResourceGroupName</span></span>
<span data-ttu-id="ff0b8-128">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ff0b8-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="ff0b8-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ff0b8-129">-ResourceId</span></span>
<span data-ttu-id="ff0b8-130">Tillgänglighets gruppens resurs-ID</span><span class="sxs-lookup"><span data-stu-id="ff0b8-130">Availability Group Listener Resource Id</span></span>

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

### <span data-ttu-id="ff0b8-131">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="ff0b8-131">-SqlVMGroupName</span></span>
<span data-ttu-id="ff0b8-132">Namn på en virtuell dator i SQL.</span><span class="sxs-lookup"><span data-stu-id="ff0b8-132">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="ff0b8-133">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="ff0b8-133">-SqlVMGroupObject</span></span>
<span data-ttu-id="ff0b8-134">SQL Virtual Machine-gruppobjekt.</span><span class="sxs-lookup"><span data-stu-id="ff0b8-134">SQL virtual machine Group object.</span></span>

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

### <span data-ttu-id="ff0b8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff0b8-135">CommonParameters</span></span>
<span data-ttu-id="ff0b8-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff0b8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff0b8-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ff0b8-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff0b8-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ff0b8-138">INPUTS</span></span>

### <span data-ttu-id="ff0b8-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ff0b8-139">System.String</span></span>

### <span data-ttu-id="ff0b8-140">Microsoft. Azure. commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="ff0b8-140">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="ff0b8-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ff0b8-141">OUTPUTS</span></span>

### <span data-ttu-id="ff0b8-142">Microsoft. Azure. commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="ff0b8-142">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="ff0b8-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ff0b8-143">NOTES</span></span>

## <span data-ttu-id="ff0b8-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ff0b8-144">RELATED LINKS</span></span>
