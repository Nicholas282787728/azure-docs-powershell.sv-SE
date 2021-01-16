---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesreplicationstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesReplicationStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesReplicationStatus.md
ms.openlocfilehash: e59ce4f5e3b0f1b07744e0754cf0e1cae3de7da6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410811"
---
# <span data-ttu-id="e3361-101">Get-AzNetAppFilesReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="e3361-101">Get-AzNetAppFilesReplicationStatus</span></span>

## <span data-ttu-id="e3361-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e3361-102">SYNOPSIS</span></span>
<span data-ttu-id="e3361-103">Få statusen för replikeringen</span><span class="sxs-lookup"><span data-stu-id="e3361-103">Get the status of the replication</span></span>

## <span data-ttu-id="e3361-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e3361-104">SYNTAX</span></span>

### <span data-ttu-id="e3361-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="e3361-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesReplicationStatus -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3361-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3361-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesReplicationStatus -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e3361-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3361-107">ByObjectParameterSet</span></span>
```
Get-AzNetAppFilesReplicationStatus -InputObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3361-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e3361-108">DESCRIPTION</span></span>
<span data-ttu-id="e3361-109">Få statusen för replikeringen</span><span class="sxs-lookup"><span data-stu-id="e3361-109">Get the status of the replication</span></span>

## <span data-ttu-id="e3361-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e3361-110">EXAMPLES</span></span>

### <span data-ttu-id="e3361-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e3361-111">Example 1</span></span>
```powershell
PS C:\> Get-AnfReplicationStatus -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -PoolName "MyDestinationPool" -VolumeName "MyVol"

Output:

Healthy            : true
RelationshipStatus : Idle
MirrorState        : Mirrored
TotalProgress      : 1024
ErrorMessage       :
```

<span data-ttu-id="e3361-112">Det här kommandot får statusen för replikering på MyVol</span><span class="sxs-lookup"><span data-stu-id="e3361-112">This command gets the status of replication on MyVol</span></span>

## <span data-ttu-id="e3361-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e3361-113">PARAMETERS</span></span>

### <span data-ttu-id="e3361-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e3361-114">-AccountName</span></span>
<span data-ttu-id="e3361-115">Namnet på ANF-kontot för replikeringens målvolym</span><span class="sxs-lookup"><span data-stu-id="e3361-115">The name of the ANF account of the replication destination volume</span></span>

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

### <span data-ttu-id="e3361-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3361-116">-DefaultProfile</span></span>
<span data-ttu-id="e3361-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e3361-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3361-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3361-118">-InputObject</span></span>
<span data-ttu-id="e3361-119">ANF för att få replikeringsstatus</span><span class="sxs-lookup"><span data-stu-id="e3361-119">The ANF replication destination volume object to get replication status</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3361-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="e3361-120">-Name</span></span>
<span data-ttu-id="e3361-121">Namnet på ANF</span><span class="sxs-lookup"><span data-stu-id="e3361-121">The name of the ANF replication destination volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3361-122">-PoolName</span><span class="sxs-lookup"><span data-stu-id="e3361-122">-PoolName</span></span>
<span data-ttu-id="e3361-123">Namnet på ANF-poolen för replikeringens målvolym</span><span class="sxs-lookup"><span data-stu-id="e3361-123">The name of the ANF pool of the replication destination volume</span></span>

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

### <span data-ttu-id="e3361-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3361-124">-ResourceGroupName</span></span>
<span data-ttu-id="e3361-125">Resurs gruppen för ANF</span><span class="sxs-lookup"><span data-stu-id="e3361-125">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="e3361-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3361-126">-ResourceId</span></span>
<span data-ttu-id="e3361-127">Resurs-ID för ANF</span><span class="sxs-lookup"><span data-stu-id="e3361-127">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="e3361-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3361-128">CommonParameters</span></span>
<span data-ttu-id="e3361-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3361-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3361-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e3361-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3361-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e3361-131">INPUTS</span></span>

### <span data-ttu-id="e3361-132">System. String</span><span class="sxs-lookup"><span data-stu-id="e3361-132">System.String</span></span>

### <span data-ttu-id="e3361-133">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="e3361-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="e3361-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e3361-134">OUTPUTS</span></span>

### <span data-ttu-id="e3361-135">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="e3361-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesReplicationStatus</span></span>

## <span data-ttu-id="e3361-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e3361-136">NOTES</span></span>

## <span data-ttu-id="e3361-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e3361-137">RELATED LINKS</span></span>
