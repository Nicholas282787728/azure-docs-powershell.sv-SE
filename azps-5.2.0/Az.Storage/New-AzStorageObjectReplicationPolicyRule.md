---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/New-azstorageobjectreplicationpolicyrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageObjectReplicationPolicyRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageObjectReplicationPolicyRule.md
ms.openlocfilehash: c8d41300250e41548cf949248b02c819b7da497f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98388779"
---
# <span data-ttu-id="a1214-101">New-AzStorageObjectReplicationPolicyRule</span><span class="sxs-lookup"><span data-stu-id="a1214-101">New-AzStorageObjectReplicationPolicyRule</span></span>

## <span data-ttu-id="a1214-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a1214-102">SYNOPSIS</span></span>
<span data-ttu-id="a1214-103">Skapar en policy för en replikeringsprincip.</span><span class="sxs-lookup"><span data-stu-id="a1214-103">Creates an object replication policy rule.</span></span>

## <span data-ttu-id="a1214-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a1214-104">SYNTAX</span></span>

```
New-AzStorageObjectReplicationPolicyRule -SourceContainer <String> -DestinationContainer <String>
 [-PrefixMatch <String[]>] [-MinCreationTime <DateTime>] [-RuleId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1214-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a1214-105">DESCRIPTION</span></span>
<span data-ttu-id="a1214-106">Cmdleten **Get-AzStorageObjectReplicationPolicy** skapar en regel för en replikeringsprincip, som kommer att användas i Set-AzStorageObjectReplicationPolicy cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1214-106">The **Get-AzStorageObjectReplicationPolicy** cmdlet creates an object replication policy rule, which will be used in Set-AzStorageObjectReplicationPolicy cmdlet.</span></span>

## <span data-ttu-id="a1214-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a1214-107">EXAMPLES</span></span>

### <span data-ttu-id="a1214-108">Exempel 1: skapa en policy för lösenordsreplikeringsprincip med endast käll-och mål konto och visa dess egenskaper</span><span class="sxs-lookup"><span data-stu-id="a1214-108">Example 1: Create an object replication policy rule with only source and destination account, and show its properties</span></span>
```
PS C:\> $rule1 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src1 -DestinationContainer dest1 

PS C:\> $rule1

RuleId SourceContainer DestinationContainer Filters.PrefixMatch Filters.MinCreationTime
------ --------------- -------------------- ------------------- -----------------------
       src1            dest1                {}
```

<span data-ttu-id="a1214-109">Det här kommandot skapar en policy för lösenordsreplikeringsprincip med endast käll-och mål konto och visar dess egenskaper.</span><span class="sxs-lookup"><span data-stu-id="a1214-109">This command creates an object replication policy rule with only source and destination account, and show its properties.</span></span>

### <span data-ttu-id="a1214-110">Exempel 2: skapa en policy för en replikeringsprincip med alla egenskaper och visa dess egenskaper</span><span class="sxs-lookup"><span data-stu-id="a1214-110">Example 2: Create an object replication policy rule with all properties, and show its properties</span></span>
```
PS C:\> $rule2 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src -DestinationContainer dest -MinCreationTime 2019-01-01T16:00:00Z -PrefixMatch a,abc,dd

PS C:\> $rule2

RuleId SourceContainer DestinationContainer Filters.PrefixMatch Filters.MinCreationTime
------ --------------- -------------------- ------------------- -----------------------
       src             dest                 {a, abc, dd}        2019-01-01T16:00:00Z
```

<span data-ttu-id="a1214-111">Det här kommandot en policy regel för en replikeringsprincip med alla egenskaper och visa dess egenskaper.</span><span class="sxs-lookup"><span data-stu-id="a1214-111">This command an object replication policy rule with all properties, and show its properties.</span></span>

## <span data-ttu-id="a1214-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a1214-112">PARAMETERS</span></span>

### <span data-ttu-id="a1214-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1214-113">-DefaultProfile</span></span>
<span data-ttu-id="a1214-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a1214-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1214-115">-DestinationContainer</span><span class="sxs-lookup"><span data-stu-id="a1214-115">-DestinationContainer</span></span>
<span data-ttu-id="a1214-116">Namnet på den mål behållare som ska replikeras till.</span><span class="sxs-lookup"><span data-stu-id="a1214-116">The Destination Container name to replicate to.</span></span>

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

### <span data-ttu-id="a1214-117">-MinCreationTime</span><span class="sxs-lookup"><span data-stu-id="a1214-117">-MinCreationTime</span></span>
<span data-ttu-id="a1214-118">Blobbar skapade efter det att tiden kommer att replikeras till destinationen..</span><span class="sxs-lookup"><span data-stu-id="a1214-118">Blobs created after the time will be replicated to the destination..</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1214-119">-PrefixMatch</span><span class="sxs-lookup"><span data-stu-id="a1214-119">-PrefixMatch</span></span>
<span data-ttu-id="a1214-120">Filtrerar resultaten för att endast replikera blobbar vars namn börjar med det angivna prefixet.</span><span class="sxs-lookup"><span data-stu-id="a1214-120">Filters the results to replicate only blobs whose names begin with the specified prefix.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1214-121">-RuleId</span><span class="sxs-lookup"><span data-stu-id="a1214-121">-RuleId</span></span>
<span data-ttu-id="a1214-122">ID för regel för objekt.</span><span class="sxs-lookup"><span data-stu-id="a1214-122">Object Replication Rule Id.</span></span>

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

### <span data-ttu-id="a1214-123">-SourceContainer</span><span class="sxs-lookup"><span data-stu-id="a1214-123">-SourceContainer</span></span>
<span data-ttu-id="a1214-124">Namnet på den käll behållare som ska replikeras från.</span><span class="sxs-lookup"><span data-stu-id="a1214-124">The Source Container name to replicate from.</span></span>

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

### <span data-ttu-id="a1214-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1214-125">CommonParameters</span></span>
<span data-ttu-id="a1214-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1214-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1214-127">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1214-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1214-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a1214-128">INPUTS</span></span>

### <span data-ttu-id="a1214-129">Ingen</span><span class="sxs-lookup"><span data-stu-id="a1214-129">None</span></span>

## <span data-ttu-id="a1214-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a1214-130">OUTPUTS</span></span>

### <span data-ttu-id="a1214-131">Microsoft. Azure. commands. Management. Storage. Models. PSObjectReplicationPolicyRule</span><span class="sxs-lookup"><span data-stu-id="a1214-131">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicyRule</span></span>

## <span data-ttu-id="a1214-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a1214-132">NOTES</span></span>

## <span data-ttu-id="a1214-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a1214-133">RELATED LINKS</span></span>
