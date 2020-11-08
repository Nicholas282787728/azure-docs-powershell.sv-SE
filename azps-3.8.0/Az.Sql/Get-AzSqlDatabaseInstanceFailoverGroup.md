---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: bd2a157a1fb05baf0fa6e02b061462718ffad314
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089267"
---
# <span data-ttu-id="58d23-101">Get-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="58d23-101">Get-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="58d23-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="58d23-102">SYNOPSIS</span></span>
<span data-ttu-id="58d23-103">Hämtar eller visar grupper med instansen failover.</span><span class="sxs-lookup"><span data-stu-id="58d23-103">Gets or lists Instance Failover Groups.</span></span>

## <span data-ttu-id="58d23-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="58d23-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseInstanceFailoverGroup [[-Name] <String>] [-ResourceGroupName] <String> [-Location] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58d23-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="58d23-105">DESCRIPTION</span></span>
<span data-ttu-id="58d23-106">Hämtar en specifik failover-grupp eller visar instanserna för redundans i en region under användarens prenumeration.</span><span class="sxs-lookup"><span data-stu-id="58d23-106">Gets a specific Instance Failover Group or lists the Instance Failover Groups in a region under the user's subscription.</span></span>

<span data-ttu-id="58d23-107">Antingen används en region i gruppen för att köra kommandot.</span><span class="sxs-lookup"><span data-stu-id="58d23-107">Either region in the Instance Failover Group may be used to execute the command.</span></span> <span data-ttu-id="58d23-108">De returnerade värdena reflekterar statusen för de hanterade instanserna i det området med avseende på gruppen för förekomster av redundans.</span><span class="sxs-lookup"><span data-stu-id="58d23-108">The returned values will reflect the state of the Managed Instances in that region with respect to the Instance Failover Group.</span></span>

## <span data-ttu-id="58d23-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="58d23-109">EXAMPLES</span></span>

### <span data-ttu-id="58d23-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="58d23-110">Example 1</span></span>
```
PS C:\> $failoverGroups = Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location
Output:
{
    ResourceGroupName                     : rg
    Location                              : East US
    Name                                  : fg
    PartnerResourceGroupName              : rg
    PartnerRegion                         : West US
    PrimaryManagedInstanceName            : managedInstance1
    PartnerManagedInstanceName            : managedInstance2
    ReplicationRole                       : Primary
    ReplicationState                      : CATCH_UP
    ReadWriteFailoverPolicy               : Automatic
    FailoverWithDataLossGracePeriodHours  : 1
    ReadOnlyFailoverPolicy                : Disabled
    Id                                    : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/rg/providers/Microsoft.Sql/locations/eastus/instanceFailoverGroups/fg
}
```

<span data-ttu-id="58d23-111">Visar en lista över alla failover-grupper i regionen</span><span class="sxs-lookup"><span data-stu-id="58d23-111">Lists all Failover Groups in the region</span></span>

### <span data-ttu-id="58d23-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="58d23-112">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg
Output:
ResourceGroupName                     : rg
Location                              : East US
Name                                  : fg
PartnerResourceGroupName              : rg
PartnerRegion                         : West US
PrimaryManagedInstanceName            : managedInstance1
PartnerManagedInstanceName            : managedInstance2
ReplicationRole                       : Primary
ReplicationState                      : CATCH_UP
ReadWriteFailoverPolicy               : Automatic
FailoverWithDataLossGracePeriodHours  : 1
ReadOnlyFailoverPolicy                : Disabled
Id                                    : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/rg/providers/Microsoft.Sql/locations/eastus/instanceFailoverGroups/fg
```

<span data-ttu-id="58d23-113">Skaffa en specifik failover-grupp för förekomst.</span><span class="sxs-lookup"><span data-stu-id="58d23-113">Get a specific Instance Failover Group.</span></span>

## <span data-ttu-id="58d23-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="58d23-114">PARAMETERS</span></span>

### <span data-ttu-id="58d23-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58d23-115">-DefaultProfile</span></span>
<span data-ttu-id="58d23-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="58d23-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58d23-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="58d23-117">-Location</span></span>
<span data-ttu-id="58d23-118">Namnet på det lokala området som du vill hämta instans failover-gruppen från.</span><span class="sxs-lookup"><span data-stu-id="58d23-118">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58d23-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="58d23-119">-Name</span></span>
<span data-ttu-id="58d23-120">Namnet på den instans av instansen som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="58d23-120">The name of the Instance Failover Group to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58d23-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58d23-121">-ResourceGroupName</span></span>
<span data-ttu-id="58d23-122">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="58d23-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58d23-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58d23-123">CommonParameters</span></span>
<span data-ttu-id="58d23-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58d23-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58d23-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="58d23-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58d23-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="58d23-126">INPUTS</span></span>

### <span data-ttu-id="58d23-127">System. String</span><span class="sxs-lookup"><span data-stu-id="58d23-127">System.String</span></span>

## <span data-ttu-id="58d23-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="58d23-128">OUTPUTS</span></span>

### <span data-ttu-id="58d23-129">Microsoft. Azure. commands. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="58d23-129">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="58d23-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="58d23-130">NOTES</span></span>

## <span data-ttu-id="58d23-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="58d23-131">RELATED LINKS</span></span>
