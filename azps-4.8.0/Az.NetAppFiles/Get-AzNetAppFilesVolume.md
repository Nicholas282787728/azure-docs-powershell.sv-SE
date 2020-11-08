---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVolume.md
ms.openlocfilehash: 1a04f128326c0b2259b81d6c58c4bc7b0113e9db
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259506"
---
# <span data-ttu-id="ab8d3-101">Get-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="ab8d3-101">Get-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="ab8d3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ab8d3-102">SYNOPSIS</span></span>
<span data-ttu-id="ab8d3-103">Hämtar information om en Azure NetApp-fil (ANF).</span><span class="sxs-lookup"><span data-stu-id="ab8d3-103">Gets details of an Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="ab8d3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ab8d3-104">SYNTAX</span></span>

### <span data-ttu-id="ab8d3-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ab8d3-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab8d3-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab8d3-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesVolume -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab8d3-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab8d3-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesVolume -PoolObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ab8d3-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ab8d3-108">DESCRIPTION</span></span>
<span data-ttu-id="ab8d3-109">Cmdleten **Get-AzNetAppFilesVolume** hämtar information om en ANF volym.</span><span class="sxs-lookup"><span data-stu-id="ab8d3-109">The **Get-AzNetAppFilesVolume** cmdlet gets details of an ANF volume.</span></span>

## <span data-ttu-id="ab8d3-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ab8d3-110">EXAMPLES</span></span>

### <span data-ttu-id="ab8d3-111">Exempel 1: skaffa en ANF volym</span><span class="sxs-lookup"><span data-stu-id="ab8d3-111">Example 1: Get an ANF volume</span></span>
```
PS C:\>Get-AzNetAppFilesVolume -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume"

Output:

ResourceGroupName : MyRG
Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes
Tags              :
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
CreationToken     :
ServiceLevel      : Premium
UsageThreshold    : 1099511627776
ProvisioningState : Succeeded
SubnetId          : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyRG-vnet/subnets/default
```

<span data-ttu-id="ab8d3-112">Det här kommandot får volymen som heter MyAnfVolume från poolen "MyAnfPool".</span><span class="sxs-lookup"><span data-stu-id="ab8d3-112">This command gets the volume named MyAnfVolume from the pool "MyAnfPool".</span></span> 

## <span data-ttu-id="ab8d3-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ab8d3-113">PARAMETERS</span></span>

### <span data-ttu-id="ab8d3-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ab8d3-114">-AccountName</span></span>
<span data-ttu-id="ab8d3-115">Namnet på ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="ab8d3-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="ab8d3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab8d3-116">-DefaultProfile</span></span>
<span data-ttu-id="ab8d3-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ab8d3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab8d3-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="ab8d3-118">-Name</span></span>
<span data-ttu-id="ab8d3-119">Namnet på ANF-volymen</span><span class="sxs-lookup"><span data-stu-id="ab8d3-119">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: VolumeName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab8d3-120">-PoolName</span><span class="sxs-lookup"><span data-stu-id="ab8d3-120">-PoolName</span></span>
<span data-ttu-id="ab8d3-121">Namnet på ANF-poolen</span><span class="sxs-lookup"><span data-stu-id="ab8d3-121">The name of the ANF pool</span></span>

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

### <span data-ttu-id="ab8d3-122">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="ab8d3-122">-PoolObject</span></span>
<span data-ttu-id="ab8d3-123">Det pool-objekt som innehåller volymen som ska returneras</span><span class="sxs-lookup"><span data-stu-id="ab8d3-123">The pool object containing the volume to return</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ab8d3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab8d3-124">-ResourceGroupName</span></span>
<span data-ttu-id="ab8d3-125">ANF-volymens resurs grupp</span><span class="sxs-lookup"><span data-stu-id="ab8d3-125">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="ab8d3-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ab8d3-126">-ResourceId</span></span>
<span data-ttu-id="ab8d3-127">Resurs-ID för ANF volym</span><span class="sxs-lookup"><span data-stu-id="ab8d3-127">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="ab8d3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab8d3-128">CommonParameters</span></span>
<span data-ttu-id="ab8d3-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab8d3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab8d3-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ab8d3-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab8d3-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ab8d3-131">INPUTS</span></span>

### <span data-ttu-id="ab8d3-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ab8d3-132">System.String</span></span>

### <span data-ttu-id="ab8d3-133">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="ab8d3-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="ab8d3-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ab8d3-134">OUTPUTS</span></span>

### <span data-ttu-id="ab8d3-135">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="ab8d3-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="ab8d3-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ab8d3-136">NOTES</span></span>

## <span data-ttu-id="ab8d3-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ab8d3-137">RELATED LINKS</span></span>
