---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
ms.openlocfilehash: e63812f1972effd7956911861e5c6e07436fd4c1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272615"
---
# <span data-ttu-id="30847-101">Update-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="30847-101">Update-AzNetAppFilesPool</span></span>

## <span data-ttu-id="30847-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="30847-102">SYNOPSIS</span></span>
<span data-ttu-id="30847-103">Uppdaterar en ANF-pool (Azure NetApp-filer) i enlighet med de valfria modifierarna.</span><span class="sxs-lookup"><span data-stu-id="30847-103">Updates an Azure NetApp Files (ANF) pool according to the optional modifiers provided.</span></span>

## <span data-ttu-id="30847-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="30847-104">SYNTAX</span></span>

### <span data-ttu-id="30847-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="30847-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesPool -ResourceGroupName <String> [-Location <String>] -AccountName <String> -Name <String>
 [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30847-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="30847-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool -Name <String> [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="30847-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="30847-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30847-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="30847-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="30847-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="30847-109">DESCRIPTION</span></span>
<span data-ttu-id="30847-110">Cmdleten **Update-AzNetAppFilesPool** ändrar en ANF-pool.</span><span class="sxs-lookup"><span data-stu-id="30847-110">The **Update-AzNetAppFilesPool** cmdlet modifies an ANF pool.</span></span>

## <span data-ttu-id="30847-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="30847-111">EXAMPLES</span></span>

### <span data-ttu-id="30847-112">Exempel 1: ändra en ANF-pool</span><span class="sxs-lookup"><span data-stu-id="30847-112">Example 1: Modify an ANF pool</span></span>
```
PS C:\>Update-AzNetAppFilesPool -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -PoolSize 4398046511104 -ServiceLevel "Standard"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool
Name              : MyAnfAccount/MyAnfPool
Type              : Microsoft.NetApp/netAppAccounts/capacityPools
Tags              :
PoolId            : 9fa2ca6d-1e48-4439-30e3-7de056e44e5a
Size              : 4398046511104
ServiceLevel      : Standard
ProvisioningState : Succeeded
```

<span data-ttu-id="30847-113">Det här kommandot ändrar ANF-poolen "MyAnfPool" till den angivna storleken och ServiceLevel.</span><span class="sxs-lookup"><span data-stu-id="30847-113">This command changes the ANF pool "MyAnfPool" to have the given size and ServiceLevel.</span></span>

## <span data-ttu-id="30847-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="30847-114">PARAMETERS</span></span>

### <span data-ttu-id="30847-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="30847-115">-AccountName</span></span>
<span data-ttu-id="30847-116">Namnet på ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="30847-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="30847-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="30847-117">-AccountObject</span></span>
<span data-ttu-id="30847-118">Det konto objekt som innehåller poolen som ska uppdateras</span><span class="sxs-lookup"><span data-stu-id="30847-118">The account object containing the pool to update</span></span>

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

### <span data-ttu-id="30847-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30847-119">-DefaultProfile</span></span>
<span data-ttu-id="30847-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="30847-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30847-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="30847-121">-InputObject</span></span>
<span data-ttu-id="30847-122">Pool-objekt som ska uppdateras</span><span class="sxs-lookup"><span data-stu-id="30847-122">The pool object to update</span></span>

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

### <span data-ttu-id="30847-123">-Plats</span><span class="sxs-lookup"><span data-stu-id="30847-123">-Location</span></span>
<span data-ttu-id="30847-124">Resursens plats</span><span class="sxs-lookup"><span data-stu-id="30847-124">The location of the resource</span></span>

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

### <span data-ttu-id="30847-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="30847-125">-Name</span></span>
<span data-ttu-id="30847-126">Namnet på ANF-poolen</span><span class="sxs-lookup"><span data-stu-id="30847-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="30847-127">-PoolSize</span><span class="sxs-lookup"><span data-stu-id="30847-127">-PoolSize</span></span>
<span data-ttu-id="30847-128">Storleken på ANF-poolen</span><span class="sxs-lookup"><span data-stu-id="30847-128">The size of the ANF pool</span></span>

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

### <span data-ttu-id="30847-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30847-129">-ResourceGroupName</span></span>
<span data-ttu-id="30847-130">Resurs gruppen för ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="30847-130">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="30847-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="30847-131">-ResourceId</span></span>
<span data-ttu-id="30847-132">Resurs-ID för ANF-poolen</span><span class="sxs-lookup"><span data-stu-id="30847-132">The resource id of the ANF pool</span></span>

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

### <span data-ttu-id="30847-133">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="30847-133">-ServiceLevel</span></span>
<span data-ttu-id="30847-134">Tjänst nivå för ANF-poolen</span><span class="sxs-lookup"><span data-stu-id="30847-134">The service level of the ANF pool</span></span>

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

### <span data-ttu-id="30847-135">-Tagg</span><span class="sxs-lookup"><span data-stu-id="30847-135">-Tag</span></span>
<span data-ttu-id="30847-136">En hash som representerar resurs koder</span><span class="sxs-lookup"><span data-stu-id="30847-136">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="30847-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="30847-137">-Confirm</span></span>
<span data-ttu-id="30847-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="30847-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30847-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30847-139">-WhatIf</span></span>
<span data-ttu-id="30847-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="30847-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30847-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="30847-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30847-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30847-142">CommonParameters</span></span>
<span data-ttu-id="30847-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30847-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30847-144">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="30847-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30847-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="30847-145">INPUTS</span></span>

### <span data-ttu-id="30847-146">System. String</span><span class="sxs-lookup"><span data-stu-id="30847-146">System.String</span></span>

### <span data-ttu-id="30847-147">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="30847-147">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="30847-148">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="30847-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="30847-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="30847-149">OUTPUTS</span></span>

### <span data-ttu-id="30847-150">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="30847-150">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="30847-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="30847-151">NOTES</span></span>

## <span data-ttu-id="30847-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="30847-152">RELATED LINKS</span></span>
