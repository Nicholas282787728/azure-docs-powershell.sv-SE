---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesPool.md
ms.openlocfilehash: fdadfde6c798bf404d1f99dbb1ff2a8109d41f73
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754005"
---
# <span data-ttu-id="0658e-101">New-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="0658e-101">New-AzNetAppFilesPool</span></span>

## <span data-ttu-id="0658e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0658e-102">SYNOPSIS</span></span>
<span data-ttu-id="0658e-103">Skapar en ny ANF-pool (Azure NetApp-filer).</span><span class="sxs-lookup"><span data-stu-id="0658e-103">Creates a new Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="0658e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0658e-104">SYNTAX</span></span>

### <span data-ttu-id="0658e-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="0658e-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesPool -ResourceGroupName <String> -Location <String> -AccountName <String> -Name <String>
 -PoolSize <Int64> -ServiceLevel <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0658e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0658e-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesPool -Name <String> -PoolSize <Int64> -ServiceLevel <String> [-Tag <Hashtable>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0658e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0658e-107">DESCRIPTION</span></span>
<span data-ttu-id="0658e-108">Cmdleten **New-AzNetAppFilesPool** skapar en ANF-pool.</span><span class="sxs-lookup"><span data-stu-id="0658e-108">The **New-AzNetAppFilesPool** cmdlet creates an ANF pool.</span></span>

## <span data-ttu-id="0658e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0658e-109">EXAMPLES</span></span>

### <span data-ttu-id="0658e-110">Exempel 1: skapa en ANF-pool</span><span class="sxs-lookup"><span data-stu-id="0658e-110">Example 1: Create an ANF pool</span></span>
```
PS C:\>New-AzNetAppFilesPool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MyAnfPool" -l "westus2" -PoolSize 4398046511104 -ServiceLevel "Premium"

Output:

Location          : westus2
Id                : /subscriptions/subsID/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool
Name              : MyAnfAccount/MyAnfPool
Type              : Microsoft.NetApp/netAppAccounts/capacityPools
Tags              :
PoolId            : a3a53a09-fd70-37ab-39dc-392a04cba525
Size              : 4398046511104
ServiceLevel      : Premium
ProvisioningState : Succeeded
```

<span data-ttu-id="0658e-111">Det här kommandot skapar den nya ANF-poolen "MyAnfPool" i kontot "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="0658e-111">This command creates the new ANF pool "MyAnfPool" within the account "MyAnfAccount".</span></span>

## <span data-ttu-id="0658e-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0658e-112">PARAMETERS</span></span>

### <span data-ttu-id="0658e-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0658e-113">-AccountName</span></span>
<span data-ttu-id="0658e-114">Namnet på ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="0658e-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="0658e-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="0658e-115">-AccountObject</span></span>
<span data-ttu-id="0658e-116">Kontot för det nya programpoolskontot</span><span class="sxs-lookup"><span data-stu-id="0658e-116">The account for the new pool object</span></span>

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

### <span data-ttu-id="0658e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0658e-117">-DefaultProfile</span></span>
<span data-ttu-id="0658e-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0658e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0658e-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="0658e-119">-Location</span></span>
<span data-ttu-id="0658e-120">Resursens plats</span><span class="sxs-lookup"><span data-stu-id="0658e-120">The location of the resource</span></span>

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

### <span data-ttu-id="0658e-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="0658e-121">-Name</span></span>
<span data-ttu-id="0658e-122">Namnet på ANF-poolen</span><span class="sxs-lookup"><span data-stu-id="0658e-122">The name of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: PoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0658e-123">-PoolSize</span><span class="sxs-lookup"><span data-stu-id="0658e-123">-PoolSize</span></span>
<span data-ttu-id="0658e-124">Storleken på ANF-poolen</span><span class="sxs-lookup"><span data-stu-id="0658e-124">The size of the ANF pool</span></span>

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

### <span data-ttu-id="0658e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0658e-125">-ResourceGroupName</span></span>
<span data-ttu-id="0658e-126">Resurs gruppen för ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="0658e-126">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="0658e-127">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="0658e-127">-ServiceLevel</span></span>
<span data-ttu-id="0658e-128">Tjänst nivå för ANF-poolen</span><span class="sxs-lookup"><span data-stu-id="0658e-128">The service level of the ANF pool</span></span>

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

### <span data-ttu-id="0658e-129">-Tagg</span><span class="sxs-lookup"><span data-stu-id="0658e-129">-Tag</span></span>
<span data-ttu-id="0658e-130">En hash som representerar resurs koder</span><span class="sxs-lookup"><span data-stu-id="0658e-130">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="0658e-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0658e-131">-Confirm</span></span>
<span data-ttu-id="0658e-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0658e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0658e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0658e-133">-WhatIf</span></span>
<span data-ttu-id="0658e-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0658e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0658e-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0658e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0658e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0658e-136">CommonParameters</span></span>
<span data-ttu-id="0658e-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0658e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="0658e-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0658e-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0658e-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0658e-139">INPUTS</span></span>

### <span data-ttu-id="0658e-140">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="0658e-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="0658e-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0658e-141">OUTPUTS</span></span>

### <span data-ttu-id="0658e-142">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="0658e-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="0658e-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0658e-143">NOTES</span></span>

## <span data-ttu-id="0658e-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0658e-144">RELATED LINKS</span></span>