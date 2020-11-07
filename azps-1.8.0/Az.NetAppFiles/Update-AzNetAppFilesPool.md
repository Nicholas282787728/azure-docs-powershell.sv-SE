---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
ms.openlocfilehash: 3dd02a2dc0cf7090ba2711b6155d25038397ab9e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753989"
---
# <span data-ttu-id="5d027-101">Update-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="5d027-101">Update-AzNetAppFilesPool</span></span>

## <span data-ttu-id="5d027-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5d027-102">SYNOPSIS</span></span>
<span data-ttu-id="5d027-103">Uppdaterar en ANF-pool (Azure NetApp-filer) med den nya data uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="5d027-103">Updates an Azure NetApp Files (ANF) pool with the new data set.</span></span>

## <span data-ttu-id="5d027-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5d027-104">SYNTAX</span></span>

### <span data-ttu-id="5d027-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="5d027-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesPool -ResourceGroupName <String> -Location <String> -AccountName <String> -Name <String>
 -PoolSize <Int64> -ServiceLevel <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5d027-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d027-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool -Name <String> -PoolSize <Int64> -ServiceLevel <String>
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5d027-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d027-107">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool -PoolSize <Int64> -ServiceLevel <String> -InputObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d027-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5d027-108">DESCRIPTION</span></span>
<span data-ttu-id="5d027-109">Cmdleten **Update-AzNetAppFilesPool** ändrar en ANF-pool.</span><span class="sxs-lookup"><span data-stu-id="5d027-109">The **Update-AzNetAppFilesPool** cmdlet modifies an ANF pool.</span></span>

## <span data-ttu-id="5d027-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5d027-110">EXAMPLES</span></span>

### <span data-ttu-id="5d027-111">Exempel 1: ändra en ANF-pool</span><span class="sxs-lookup"><span data-stu-id="5d027-111">Example 1: Modify an ANF pool</span></span>
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

<span data-ttu-id="5d027-112">Det här kommandot ändrar ANF-poolen "MyAnfPool" till den angivna storleken och ServiceLevel.</span><span class="sxs-lookup"><span data-stu-id="5d027-112">This command changes the ANF pool "MyAnfPool" to have the given size and ServiceLevel.</span></span>

## <span data-ttu-id="5d027-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5d027-113">PARAMETERS</span></span>

### <span data-ttu-id="5d027-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5d027-114">-AccountName</span></span>
<span data-ttu-id="5d027-115">Namnet på ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="5d027-115">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d027-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="5d027-116">-AccountObject</span></span>
<span data-ttu-id="5d027-117">Det konto objekt som innehåller poolen som ska uppdateras</span><span class="sxs-lookup"><span data-stu-id="5d027-117">The account object containing the pool to update</span></span>

```yaml
Type: PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d027-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d027-118">-DefaultProfile</span></span>
<span data-ttu-id="5d027-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5d027-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d027-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5d027-120">-InputObject</span></span>
<span data-ttu-id="5d027-121">Pool-objekt som ska uppdateras</span><span class="sxs-lookup"><span data-stu-id="5d027-121">The pool object to update</span></span>

```yaml
Type: PSNetAppFilesPool
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d027-122">-Plats</span><span class="sxs-lookup"><span data-stu-id="5d027-122">-Location</span></span>
<span data-ttu-id="5d027-123">Resursens plats</span><span class="sxs-lookup"><span data-stu-id="5d027-123">The location of the resource</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d027-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="5d027-124">-Name</span></span>
<span data-ttu-id="5d027-125">Namnet på ANF-poolen</span><span class="sxs-lookup"><span data-stu-id="5d027-125">The name of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: PoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d027-126">-PoolSize</span><span class="sxs-lookup"><span data-stu-id="5d027-126">-PoolSize</span></span>
<span data-ttu-id="5d027-127">Storleken på ANF-poolen</span><span class="sxs-lookup"><span data-stu-id="5d027-127">The size of the ANF pool</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d027-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d027-128">-ResourceGroupName</span></span>
<span data-ttu-id="5d027-129">Resurs gruppen för ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="5d027-129">The resource group of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d027-130">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="5d027-130">-ServiceLevel</span></span>
<span data-ttu-id="5d027-131">Tjänst nivå för ANF-poolen</span><span class="sxs-lookup"><span data-stu-id="5d027-131">The service level of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d027-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5d027-132">-Confirm</span></span>
<span data-ttu-id="5d027-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5d027-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d027-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d027-134">-WhatIf</span></span>
<span data-ttu-id="5d027-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5d027-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d027-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5d027-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d027-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d027-137">CommonParameters</span></span>
<span data-ttu-id="5d027-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d027-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="5d027-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d027-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d027-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5d027-140">INPUTS</span></span>

### <span data-ttu-id="5d027-141">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="5d027-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="5d027-142">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="5d027-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="5d027-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5d027-143">OUTPUTS</span></span>

### <span data-ttu-id="5d027-144">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="5d027-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="5d027-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5d027-145">NOTES</span></span>

## <span data-ttu-id="5d027-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5d027-146">RELATED LINKS</span></span>
