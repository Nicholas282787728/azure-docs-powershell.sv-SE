---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: c3bd5ecf7e3561be5f9e6b8d990c40281135982c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93927557"
---
# <span data-ttu-id="5e41e-101">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="5e41e-101">Get-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="5e41e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5e41e-102">SYNOPSIS</span></span>
<span data-ttu-id="5e41e-103">Få information om en Azure Site Recovery-Fabric.</span><span class="sxs-lookup"><span data-stu-id="5e41e-103">Get the details of an Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="5e41e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5e41e-104">SYNTAX</span></span>

### <span data-ttu-id="5e41e-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="5e41e-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrFabric [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e41e-106">ByName</span><span class="sxs-lookup"><span data-stu-id="5e41e-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrFabric -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e41e-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="5e41e-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrFabric -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5e41e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5e41e-108">DESCRIPTION</span></span>
<span data-ttu-id="5e41e-109">Cmdleten **Get-AzRecoveryServicesAsrFabric** hämtar egenskaperna för en angiven Azure Site Recovery-infrastruktur eller alla Azure Site Recovery-Fabric i ett valv för återhämtnings tjänst.</span><span class="sxs-lookup"><span data-stu-id="5e41e-109">The **Get-AzRecoveryServicesAsrFabric** cmdlet gets the properties of a specified Azure Site Recovery Fabric or all Azure Site Recovery Fabrics in a Recovery Service vault.</span></span>

## <span data-ttu-id="5e41e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5e41e-110">EXAMPLES</span></span>

### <span data-ttu-id="5e41e-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5e41e-111">Example 1</span></span>
```
PS C:\> $fabrics = Get-AzRecoveryServicesAsrFabric
```

<span data-ttu-id="5e41e-112">Returnerar alla Azure Site Recovery-Fabric i valvet.</span><span class="sxs-lookup"><span data-stu-id="5e41e-112">Returns all the Azure Site Recovery fabrics in the vault.</span></span>

### <span data-ttu-id="5e41e-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="5e41e-113">Example 2</span></span>
```
PS C:\> $fabric = Get-AzRecoveryServicesAsrFabric -Name xxxx

Name                  : xxxx
FriendlyName          : XXXXXXXXXX
ID                    : /Subscriptions/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/XXXXXXXXXXXXX/replicationFabrics/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
FabricType            : VMware
SiteIdentifier        : XXXXXXXXxxxxxxxxxxx
FabricSpecificDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificDetails
```

<span data-ttu-id="5e41e-114">Returnera Azure Site Recovery Fabric med namn xxxx.</span><span class="sxs-lookup"><span data-stu-id="5e41e-114">Return azure site recovery fabric with name xxxx.</span></span>

### <span data-ttu-id="5e41e-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="5e41e-115">Example 3</span></span>
```
PS C:\> $fabric = Get-AzRecoveryServicesAsrFabric -FriendlyName XXXXXXXXXX

Name                  : xxxx
FriendlyName          : XXXXXXXXXX
ID                    : /Subscriptions/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/XXXXXXXXXXXXX/replicationFabrics/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
FabricType            : VMware
SiteIdentifier        : XXXXXXXXxxxxxxxxxxx
FabricSpecificDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificDetails
```

<span data-ttu-id="5e41e-116">Returnera Azure Site Recovery Fabric med vänligt namn xxxx.</span><span class="sxs-lookup"><span data-stu-id="5e41e-116">Return azure site recovery fabric with friendly name xxxx.</span></span>

## <span data-ttu-id="5e41e-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5e41e-117">PARAMETERS</span></span>

### <span data-ttu-id="5e41e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e41e-118">-DefaultProfile</span></span>
<span data-ttu-id="5e41e-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5e41e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e41e-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="5e41e-120">-FriendlyName</span></span>
<span data-ttu-id="5e41e-121">Sök efter ASR-Fabric med eget namn på Fabric.</span><span class="sxs-lookup"><span data-stu-id="5e41e-121">Search for the ASR fabric by the friendly name of the fabric.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e41e-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="5e41e-122">-Name</span></span>
<span data-ttu-id="5e41e-123">Sök efter ASR-Fabric genom namnet på infrastruktur resursen.</span><span class="sxs-lookup"><span data-stu-id="5e41e-123">Search for the ASR fabric by the name of the fabric.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e41e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e41e-124">CommonParameters</span></span>
<span data-ttu-id="5e41e-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e41e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e41e-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5e41e-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e41e-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5e41e-127">INPUTS</span></span>

### <span data-ttu-id="5e41e-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="5e41e-128">None</span></span>

## <span data-ttu-id="5e41e-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5e41e-129">OUTPUTS</span></span>

### <span data-ttu-id="5e41e-130">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="5e41e-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="5e41e-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5e41e-131">NOTES</span></span>

## <span data-ttu-id="5e41e-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5e41e-132">RELATED LINKS</span></span>

[<span data-ttu-id="5e41e-133">New-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="5e41e-133">New-AzRecoveryServicesAsrFabric</span></span>](./New-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="5e41e-134">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="5e41e-134">Remove-AzRecoveryServicesAsrFabric</span></span>](./Remove-AzRecoveryServicesAsrFabric.md)
