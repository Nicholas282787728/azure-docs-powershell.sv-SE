---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azmaintenanceupdate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceUpdate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceUpdate.md
ms.openlocfilehash: d8d3e4df3349acb1340a24362043d32d528fc284
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091949"
---
# <span data-ttu-id="7fece-101">Get-AzMaintenanceUpdate</span><span class="sxs-lookup"><span data-stu-id="7fece-101">Get-AzMaintenanceUpdate</span></span>

## <span data-ttu-id="7fece-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7fece-102">SYNOPSIS</span></span>
<span data-ttu-id="7fece-103">Få väntande underhålls uppdateringar för resursen.</span><span class="sxs-lookup"><span data-stu-id="7fece-103">Get pending maintenance updates to resource.</span></span>

## <span data-ttu-id="7fece-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7fece-104">SYNTAX</span></span>

```
Get-AzMaintenanceUpdate [-ResourceGroupName] <String> [-ProviderName] <String> [-ResourceParentType <String>]
 [-ResourceParentName <String>] [-ResourceType] <String> [-ResourceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7fece-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7fece-105">DESCRIPTION</span></span>
<span data-ttu-id="7fece-106">Få väntande underhålls uppdateringar för resursen.</span><span class="sxs-lookup"><span data-stu-id="7fece-106">Get pending maintenance updates to resource.</span></span>

## <span data-ttu-id="7fece-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7fece-107">EXAMPLES</span></span>

### <span data-ttu-id="7fece-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7fece-108">Example 1</span></span>
```powershell
PS C:\> Get-AzMaintenanceUpdate -ResourceGroupName smdtest$location -ResourceParentType hostGroups -ResourceParentName smddhg$location -ResourceType hosts -ResourceName smddh$location -ProviderName Microsoft.Compute

MaintenanceScope    : Host
ImpactType          : Freeze
Status              : Pending
ImpactDurationInSec : 9
NotBefore           : 1/24/2020 5:11:41 AM
ResourceId          : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2
```

<span data-ttu-id="7fece-109">Få väntande underhålls uppdateringar för resursen.</span><span class="sxs-lookup"><span data-stu-id="7fece-109">Get pending maintenance updates to resource.</span></span>

## <span data-ttu-id="7fece-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7fece-110">PARAMETERS</span></span>

### <span data-ttu-id="7fece-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fece-111">-DefaultProfile</span></span>
<span data-ttu-id="7fece-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7fece-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7fece-113">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="7fece-113">-ProviderName</span></span>
<span data-ttu-id="7fece-114">Namnet på resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="7fece-114">The resource provider Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fece-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fece-115">-ResourceGroupName</span></span>
<span data-ttu-id="7fece-116">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="7fece-116">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fece-117">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="7fece-117">-ResourceName</span></span>
<span data-ttu-id="7fece-118">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="7fece-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fece-119">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="7fece-119">-ResourceParentName</span></span>
<span data-ttu-id="7fece-120">Namnet på den överordnade resursen.</span><span class="sxs-lookup"><span data-stu-id="7fece-120">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fece-121">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="7fece-121">-ResourceParentType</span></span>
<span data-ttu-id="7fece-122">Den överordnade resurs typen.</span><span class="sxs-lookup"><span data-stu-id="7fece-122">The parent resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fece-123">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="7fece-123">-ResourceType</span></span>
<span data-ttu-id="7fece-124">Resurs typen.</span><span class="sxs-lookup"><span data-stu-id="7fece-124">The resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fece-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fece-125">CommonParameters</span></span>
<span data-ttu-id="7fece-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fece-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fece-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7fece-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fece-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7fece-128">INPUTS</span></span>

### <span data-ttu-id="7fece-129">System. String</span><span class="sxs-lookup"><span data-stu-id="7fece-129">System.String</span></span>

## <span data-ttu-id="7fece-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7fece-130">OUTPUTS</span></span>

### <span data-ttu-id="7fece-131">Microsoft. Azure. Management. Maintenance. Models. Update</span><span class="sxs-lookup"><span data-stu-id="7fece-131">Microsoft.Azure.Management.Maintenance.Models.Update</span></span>

## <span data-ttu-id="7fece-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7fece-132">NOTES</span></span>

## <span data-ttu-id="7fece-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7fece-133">RELATED LINKS</span></span>