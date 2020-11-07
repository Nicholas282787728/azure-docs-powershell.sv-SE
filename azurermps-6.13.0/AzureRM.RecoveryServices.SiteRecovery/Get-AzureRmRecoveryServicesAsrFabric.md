---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrFabric.md
ms.openlocfilehash: db93d022d2abd6d3c6cecfe32b1f82be4483e850
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580019"
---
# <span data-ttu-id="34076-101">Get-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="34076-101">Get-AzureRmRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="34076-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="34076-102">SYNOPSIS</span></span>
<span data-ttu-id="34076-103">Få information om en Azure Site Recovery-Fabric.</span><span class="sxs-lookup"><span data-stu-id="34076-103">Get the details of an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34076-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="34076-104">SYNTAX</span></span>

### <span data-ttu-id="34076-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="34076-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrFabric [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34076-106">ByName</span><span class="sxs-lookup"><span data-stu-id="34076-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrFabric -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="34076-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="34076-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrFabric -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="34076-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="34076-108">DESCRIPTION</span></span>
<span data-ttu-id="34076-109">Cmdleten **Get-AzureRmRecoveryServicesAsrFabric** hämtar egenskaperna för en angiven Azure Site Recovery-infrastruktur eller alla Azure Site Recovery-Fabric i ett valv för återhämtnings tjänst.</span><span class="sxs-lookup"><span data-stu-id="34076-109">The **Get-AzureRmRecoveryServicesAsrFabric** cmdlet gets the properties of a specified Azure Site Recovery Fabric or all Azure Site Recovery Fabrics in a Recovery Service vault.</span></span>

## <span data-ttu-id="34076-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="34076-110">EXAMPLES</span></span>

### <span data-ttu-id="34076-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="34076-111">Example 1</span></span>
```
PS C:\> $fabrics = Get-AzureRmRecoveryServicesAsrFabric
```

<span data-ttu-id="34076-112">Returnerar alla Azure Site Recovery-Fabric i valvet.</span><span class="sxs-lookup"><span data-stu-id="34076-112">Returns all the Azure Site Recovery fabrics in the vault.</span></span>

### <span data-ttu-id="34076-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="34076-113">Example 2</span></span>
```
PS C:\> $fabric = Get-AzureRmRecoveryServicesAsrFabric -Name xxxx

Name                  : xxxx
FriendlyName          : XXXXXXXXXX
ID                    : /Subscriptions/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/XXXXXXXXXXXXX/replicationFabrics/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
FabricType            : VMware
SiteIdentifier        : XXXXXXXXxxxxxxxxxxx
FabricSpecificDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificDetails
```

<span data-ttu-id="34076-114">Returnera Azure Site Recovery Fabric med namn xxxx.</span><span class="sxs-lookup"><span data-stu-id="34076-114">Return azure site recovery fabric with name xxxx.</span></span>

### <span data-ttu-id="34076-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="34076-115">Example 3</span></span>
```
PS C:\> $fabric = Get-AzureRmRecoveryServicesAsrFabric -FriendlyName XXXXXXXXXX

Name                  : xxxx
FriendlyName          : XXXXXXXXXX
ID                    : /Subscriptions/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/XXXXXXXXXXXXX/replicationFabrics/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
FabricType            : VMware
SiteIdentifier        : XXXXXXXXxxxxxxxxxxx
FabricSpecificDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificDetails
```

<span data-ttu-id="34076-116">Returnera Azure Site Recovery Fabric med vänligt namn xxxx.</span><span class="sxs-lookup"><span data-stu-id="34076-116">Return azure site recovery fabric with friendly name xxxx.</span></span>

## <span data-ttu-id="34076-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="34076-117">PARAMETERS</span></span>

### <span data-ttu-id="34076-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34076-118">-DefaultProfile</span></span>
<span data-ttu-id="34076-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="34076-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34076-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="34076-120">-FriendlyName</span></span>
<span data-ttu-id="34076-121">Sök efter ASR-Fabric med eget namn på Fabric.</span><span class="sxs-lookup"><span data-stu-id="34076-121">Search for the ASR fabric by the friendly name of the fabric.</span></span>

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

### <span data-ttu-id="34076-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="34076-122">-Name</span></span>
<span data-ttu-id="34076-123">Sök efter ASR-Fabric genom namnet på infrastruktur resursen.</span><span class="sxs-lookup"><span data-stu-id="34076-123">Search for the ASR fabric by the name of the fabric.</span></span>

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

### <span data-ttu-id="34076-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34076-124">CommonParameters</span></span>
<span data-ttu-id="34076-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34076-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34076-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34076-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34076-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="34076-127">INPUTS</span></span>

### <span data-ttu-id="34076-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="34076-128">None</span></span>

## <span data-ttu-id="34076-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="34076-129">OUTPUTS</span></span>

### <span data-ttu-id="34076-130">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRFabric, Microsoft. Azure. commands. RecoveryServices. SiteRecovery, version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="34076-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="34076-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="34076-131">NOTES</span></span>

## <span data-ttu-id="34076-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="34076-132">RELATED LINKS</span></span>

[<span data-ttu-id="34076-133">New-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="34076-133">New-AzureRmRecoveryServicesAsrFabric</span></span>](./New-AzureRmRecoveryServicesAsrFabric.md)

[<span data-ttu-id="34076-134">Remove-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="34076-134">Remove-AzureRmRecoveryServicesAsrFabric</span></span>](./Remove-AzureRmRecoveryServicesAsrFabric.md)