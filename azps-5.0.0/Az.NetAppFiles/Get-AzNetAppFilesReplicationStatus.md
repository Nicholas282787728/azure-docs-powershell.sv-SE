---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesreplicationstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesReplicationStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesReplicationStatus.md
ms.openlocfilehash: a2345dfe37fd43532739cdfd8000b47fb1e20906
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270840"
---
# <span data-ttu-id="6f74e-101">Get-AzNetAppFilesReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="6f74e-101">Get-AzNetAppFilesReplicationStatus</span></span>

## <span data-ttu-id="6f74e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6f74e-102">SYNOPSIS</span></span>
<span data-ttu-id="6f74e-103">Få statusen för replikeringen</span><span class="sxs-lookup"><span data-stu-id="6f74e-103">Get the status of the replication</span></span>

## <span data-ttu-id="6f74e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6f74e-104">SYNTAX</span></span>

### <span data-ttu-id="6f74e-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="6f74e-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesReplicationStatus -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f74e-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f74e-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesReplicationStatus -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6f74e-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f74e-107">ByObjectParameterSet</span></span>
```
Get-AzNetAppFilesReplicationStatus -InputObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f74e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6f74e-108">DESCRIPTION</span></span>
<span data-ttu-id="6f74e-109">Få statusen för replikeringen</span><span class="sxs-lookup"><span data-stu-id="6f74e-109">Get the status of the replication</span></span>

## <span data-ttu-id="6f74e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6f74e-110">EXAMPLES</span></span>

### <span data-ttu-id="6f74e-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6f74e-111">Example 1</span></span>
```powershell
PS C:\> Get-AnfReplicationStatus -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -PoolName "MyDestinationPool" -VolumeName "MyVol"

Output:

Healthy            : true
RelationshipStatus : Idle
MirrorState        : Mirrored
TotalProgress      : 1024
ErrorMessage       :
```

<span data-ttu-id="6f74e-112">Det här kommandot får statusen för replikering på MyVol</span><span class="sxs-lookup"><span data-stu-id="6f74e-112">This command gets the status of replication on MyVol</span></span>

## <span data-ttu-id="6f74e-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6f74e-113">PARAMETERS</span></span>

### <span data-ttu-id="6f74e-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6f74e-114">-AccountName</span></span>
<span data-ttu-id="6f74e-115">Namnet på ANF-kontot för replikeringens målvolym</span><span class="sxs-lookup"><span data-stu-id="6f74e-115">The name of the ANF account of the replication destination volume</span></span>

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

### <span data-ttu-id="6f74e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f74e-116">-DefaultProfile</span></span>
<span data-ttu-id="6f74e-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6f74e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f74e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6f74e-118">-InputObject</span></span>
<span data-ttu-id="6f74e-119">ANF för att få replikeringsstatus</span><span class="sxs-lookup"><span data-stu-id="6f74e-119">The ANF replication destination volume object to get replication status</span></span>

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

### <span data-ttu-id="6f74e-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="6f74e-120">-Name</span></span>
<span data-ttu-id="6f74e-121">Namnet på ANF</span><span class="sxs-lookup"><span data-stu-id="6f74e-121">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="6f74e-122">-PoolName</span><span class="sxs-lookup"><span data-stu-id="6f74e-122">-PoolName</span></span>
<span data-ttu-id="6f74e-123">Namnet på ANF-poolen för replikeringens målvolym</span><span class="sxs-lookup"><span data-stu-id="6f74e-123">The name of the ANF pool of the replication destination volume</span></span>

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

### <span data-ttu-id="6f74e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f74e-124">-ResourceGroupName</span></span>
<span data-ttu-id="6f74e-125">Resurs gruppen för ANF</span><span class="sxs-lookup"><span data-stu-id="6f74e-125">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="6f74e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6f74e-126">-ResourceId</span></span>
<span data-ttu-id="6f74e-127">Resurs-ID för ANF</span><span class="sxs-lookup"><span data-stu-id="6f74e-127">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="6f74e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f74e-128">CommonParameters</span></span>
<span data-ttu-id="6f74e-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f74e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f74e-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6f74e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f74e-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6f74e-131">INPUTS</span></span>

### <span data-ttu-id="6f74e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="6f74e-132">System.String</span></span>

## <span data-ttu-id="6f74e-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6f74e-133">OUTPUTS</span></span>

### <span data-ttu-id="6f74e-134">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="6f74e-134">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesReplicationStatus</span></span>

## <span data-ttu-id="6f74e-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6f74e-135">NOTES</span></span>

## <span data-ttu-id="6f74e-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6f74e-136">RELATED LINKS</span></span>
