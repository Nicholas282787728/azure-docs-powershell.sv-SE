---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
ms.openlocfilehash: bea1f6d9427d0ed5dca48994d8138f954ed25ecd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93925597"
---
# <span data-ttu-id="c1f0f-101">Update-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="c1f0f-101">Update-AzNetAppFilesPool</span></span>

## <span data-ttu-id="c1f0f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c1f0f-102">SYNOPSIS</span></span>
<span data-ttu-id="c1f0f-103">Uppdaterar en ANF-pool (Azure NetApp-filer) i enlighet med de valfria modifierarna.</span><span class="sxs-lookup"><span data-stu-id="c1f0f-103">Updates an Azure NetApp Files (ANF) pool according to the optional modifiers provided.</span></span>

## <span data-ttu-id="c1f0f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c1f0f-104">SYNTAX</span></span>

### <span data-ttu-id="c1f0f-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="c1f0f-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesPool -ResourceGroupName <String> [-Location <String>] -AccountName <String> -Name <String>
 [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1f0f-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1f0f-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool -Name <String> [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c1f0f-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1f0f-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1f0f-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1f0f-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c1f0f-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c1f0f-109">DESCRIPTION</span></span>
<span data-ttu-id="c1f0f-110">Cmdleten **Update-AzNetAppFilesPool** ändrar en ANF-pool.</span><span class="sxs-lookup"><span data-stu-id="c1f0f-110">The **Update-AzNetAppFilesPool** cmdlet modifies an ANF pool.</span></span>

## <span data-ttu-id="c1f0f-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c1f0f-111">EXAMPLES</span></span>

### <span data-ttu-id="c1f0f-112">Exempel 1: ändra en ANF-pool</span><span class="sxs-lookup"><span data-stu-id="c1f0f-112">Example 1: Modify an ANF pool</span></span>
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

<span data-ttu-id="c1f0f-113">Det här kommandot ändrar ANF-poolen "MyAnfPool" till den angivna storleken och ServiceLevel.</span><span class="sxs-lookup"><span data-stu-id="c1f0f-113">This command changes the ANF pool "MyAnfPool" to have the given size and ServiceLevel.</span></span>

## <span data-ttu-id="c1f0f-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c1f0f-114">PARAMETERS</span></span>

### <span data-ttu-id="c1f0f-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c1f0f-115">-AccountName</span></span>
<span data-ttu-id="c1f0f-116">Namnet på ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="c1f0f-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="c1f0f-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="c1f0f-117">-AccountObject</span></span>
<span data-ttu-id="c1f0f-118">Det konto objekt som innehåller poolen som ska uppdateras</span><span class="sxs-lookup"><span data-stu-id="c1f0f-118">The account object containing the pool to update</span></span>

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

### <span data-ttu-id="c1f0f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1f0f-119">-DefaultProfile</span></span>
<span data-ttu-id="c1f0f-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c1f0f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1f0f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c1f0f-121">-InputObject</span></span>
<span data-ttu-id="c1f0f-122">Pool-objekt som ska uppdateras</span><span class="sxs-lookup"><span data-stu-id="c1f0f-122">The pool object to update</span></span>

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

### <span data-ttu-id="c1f0f-123">-Plats</span><span class="sxs-lookup"><span data-stu-id="c1f0f-123">-Location</span></span>
<span data-ttu-id="c1f0f-124">Resursens plats</span><span class="sxs-lookup"><span data-stu-id="c1f0f-124">The location of the resource</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1f0f-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="c1f0f-125">-Name</span></span>
<span data-ttu-id="c1f0f-126">Namnet på ANF-poolen</span><span class="sxs-lookup"><span data-stu-id="c1f0f-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="c1f0f-127">-PoolSize</span><span class="sxs-lookup"><span data-stu-id="c1f0f-127">-PoolSize</span></span>
<span data-ttu-id="c1f0f-128">Storleken på ANF-poolen</span><span class="sxs-lookup"><span data-stu-id="c1f0f-128">The size of the ANF pool</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1f0f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1f0f-129">-ResourceGroupName</span></span>
<span data-ttu-id="c1f0f-130">Resurs gruppen för ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="c1f0f-130">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="c1f0f-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1f0f-131">-ResourceId</span></span>
<span data-ttu-id="c1f0f-132">Resurs-ID för ANF-poolen</span><span class="sxs-lookup"><span data-stu-id="c1f0f-132">The resource id of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1f0f-133">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="c1f0f-133">-ServiceLevel</span></span>
<span data-ttu-id="c1f0f-134">Tjänst nivå för ANF-poolen</span><span class="sxs-lookup"><span data-stu-id="c1f0f-134">The service level of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1f0f-135">-Tagg</span><span class="sxs-lookup"><span data-stu-id="c1f0f-135">-Tag</span></span>
<span data-ttu-id="c1f0f-136">En hash som representerar resurs koder</span><span class="sxs-lookup"><span data-stu-id="c1f0f-136">A hashtable which represents resource tags</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1f0f-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c1f0f-137">-Confirm</span></span>
<span data-ttu-id="c1f0f-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c1f0f-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1f0f-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1f0f-139">-WhatIf</span></span>
<span data-ttu-id="c1f0f-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c1f0f-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1f0f-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c1f0f-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1f0f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1f0f-142">CommonParameters</span></span>
<span data-ttu-id="c1f0f-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1f0f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="c1f0f-144">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1f0f-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1f0f-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c1f0f-145">INPUTS</span></span>

### <span data-ttu-id="c1f0f-146">System. String</span><span class="sxs-lookup"><span data-stu-id="c1f0f-146">System.String</span></span>

### <span data-ttu-id="c1f0f-147">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="c1f0f-147">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="c1f0f-148">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="c1f0f-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="c1f0f-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c1f0f-149">OUTPUTS</span></span>

### <span data-ttu-id="c1f0f-150">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="c1f0f-150">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="c1f0f-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c1f0f-151">NOTES</span></span>

## <span data-ttu-id="c1f0f-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c1f0f-152">RELATED LINKS</span></span>
