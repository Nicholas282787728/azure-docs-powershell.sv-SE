---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
ms.openlocfilehash: 8f26023224e0f6d4a035f4671db7b45be57a3177
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394648"
---
# <span data-ttu-id="5fefc-101">Update-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="5fefc-101">Update-AzNetAppFilesPool</span></span>

## <span data-ttu-id="5fefc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5fefc-102">SYNOPSIS</span></span>
<span data-ttu-id="5fefc-103">Uppdaterar en ANF-pool (Azure NetApp-filer) i enlighet med de valfria modifierarna.</span><span class="sxs-lookup"><span data-stu-id="5fefc-103">Updates an Azure NetApp Files (ANF) pool according to the optional modifiers provided.</span></span>

## <span data-ttu-id="5fefc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5fefc-104">SYNTAX</span></span>

### <span data-ttu-id="5fefc-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="5fefc-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesPool -ResourceGroupName <String> [-Location <String>] -AccountName <String> -Name <String>
 [-PoolSize <Int64>] [-QosType <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5fefc-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5fefc-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool -Name <String> [-PoolSize <Int64>] [-QosType <String>] [-Tag <Hashtable>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5fefc-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5fefc-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-QosType <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5fefc-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5fefc-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-QosType <String>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5fefc-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5fefc-109">DESCRIPTION</span></span>
<span data-ttu-id="5fefc-110">Cmdleten **Update-AzNetAppFilesPool** ändrar en ANF-pool.</span><span class="sxs-lookup"><span data-stu-id="5fefc-110">The **Update-AzNetAppFilesPool** cmdlet modifies an ANF pool.</span></span>

## <span data-ttu-id="5fefc-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5fefc-111">EXAMPLES</span></span>

### <span data-ttu-id="5fefc-112">Exempel 1: ändra en ANF-pool</span><span class="sxs-lookup"><span data-stu-id="5fefc-112">Example 1: Modify an ANF pool</span></span>
```
PS C:\>Update-AzNetAppFilesPool -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -PoolSize 4398046511104 -QosType "Auto"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool
Name              : MyAnfAccount/MyAnfPool
Type              : Microsoft.NetApp/netAppAccounts/capacityPools
Tags              :
PoolId            : 9fa2ca6d-1e48-4439-30e3-7de056e44e5a
Size              : 4398046511104
ServiceLevel      : Standard
QosType           : Auto
ProvisioningState : Succeeded
```

<span data-ttu-id="5fefc-113">Det här kommandot ändrar ANF-poolen "MyAnfPool" till den angivna storleken och QosType.</span><span class="sxs-lookup"><span data-stu-id="5fefc-113">This command changes the ANF pool "MyAnfPool" to have the given size and QosType.</span></span>

## <span data-ttu-id="5fefc-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5fefc-114">PARAMETERS</span></span>

### <span data-ttu-id="5fefc-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5fefc-115">-AccountName</span></span>
<span data-ttu-id="5fefc-116">Namnet på ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="5fefc-116">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fefc-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="5fefc-117">-AccountObject</span></span>
<span data-ttu-id="5fefc-118">Det konto objekt som innehåller poolen som ska uppdateras</span><span class="sxs-lookup"><span data-stu-id="5fefc-118">The account object containing the pool to update</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5fefc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fefc-119">-DefaultProfile</span></span>
<span data-ttu-id="5fefc-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5fefc-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5fefc-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5fefc-121">-InputObject</span></span>
<span data-ttu-id="5fefc-122">Pool-objekt som ska uppdateras</span><span class="sxs-lookup"><span data-stu-id="5fefc-122">The pool object to update</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5fefc-123">-Plats</span><span class="sxs-lookup"><span data-stu-id="5fefc-123">-Location</span></span>
<span data-ttu-id="5fefc-124">Resursens plats</span><span class="sxs-lookup"><span data-stu-id="5fefc-124">The location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fefc-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="5fefc-125">-Name</span></span>
<span data-ttu-id="5fefc-126">Namnet på ANF-poolen</span><span class="sxs-lookup"><span data-stu-id="5fefc-126">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: PoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fefc-127">-PoolSize</span><span class="sxs-lookup"><span data-stu-id="5fefc-127">-PoolSize</span></span>
<span data-ttu-id="5fefc-128">Storleken på ANF-poolen</span><span class="sxs-lookup"><span data-stu-id="5fefc-128">The size of the ANF pool</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fefc-129">-QosType</span><span class="sxs-lookup"><span data-stu-id="5fefc-129">-QosType</span></span>
<span data-ttu-id="5fefc-130">QoS-typen för poolen.</span><span class="sxs-lookup"><span data-stu-id="5fefc-130">The qos type of the pool.</span></span> <span data-ttu-id="5fefc-131">Möjliga värden är: ' auto ', ' Manual '</span><span class="sxs-lookup"><span data-stu-id="5fefc-131">Possible values include: 'Auto', 'Manual'</span></span>

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

### <span data-ttu-id="5fefc-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fefc-132">-ResourceGroupName</span></span>
<span data-ttu-id="5fefc-133">Resurs gruppen för ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="5fefc-133">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fefc-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5fefc-134">-ResourceId</span></span>
<span data-ttu-id="5fefc-135">Resurs-ID för ANF-poolen</span><span class="sxs-lookup"><span data-stu-id="5fefc-135">The resource id of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fefc-136">-Tagg</span><span class="sxs-lookup"><span data-stu-id="5fefc-136">-Tag</span></span>
<span data-ttu-id="5fefc-137">En hash som representerar resurs koder</span><span class="sxs-lookup"><span data-stu-id="5fefc-137">A hashtable which represents resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fefc-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5fefc-138">-Confirm</span></span>
<span data-ttu-id="5fefc-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5fefc-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5fefc-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fefc-140">-WhatIf</span></span>
<span data-ttu-id="5fefc-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5fefc-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fefc-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5fefc-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5fefc-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fefc-143">CommonParameters</span></span>
<span data-ttu-id="5fefc-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fefc-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fefc-145">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5fefc-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fefc-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5fefc-146">INPUTS</span></span>

### <span data-ttu-id="5fefc-147">System. String</span><span class="sxs-lookup"><span data-stu-id="5fefc-147">System.String</span></span>

### <span data-ttu-id="5fefc-148">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="5fefc-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="5fefc-149">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="5fefc-149">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="5fefc-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5fefc-150">OUTPUTS</span></span>

### <span data-ttu-id="5fefc-151">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="5fefc-151">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="5fefc-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5fefc-152">NOTES</span></span>

## <span data-ttu-id="5fefc-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5fefc-153">RELATED LINKS</span></span>
