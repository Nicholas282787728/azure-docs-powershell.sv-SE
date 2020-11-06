---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: bd4280f87d397afdcab3f77e8305a0c1ff4b0ed2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575574"
---
# <span data-ttu-id="872e5-101">Get-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="872e5-101">Get-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="872e5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="872e5-102">SYNOPSIS</span></span>
<span data-ttu-id="872e5-103">Får ASR-principer.</span><span class="sxs-lookup"><span data-stu-id="872e5-103">Gets ASR replication policies.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="872e5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="872e5-104">SYNTAX</span></span>

### <span data-ttu-id="872e5-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="872e5-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="872e5-106">ByName</span><span class="sxs-lookup"><span data-stu-id="872e5-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrPolicy -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="872e5-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="872e5-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrPolicy -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="872e5-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="872e5-108">DESCRIPTION</span></span>
<span data-ttu-id="872e5-109">Cmdleten **Get-AzureRmRecoveryServicesAsrPolicy** hämtar listan över konfigurerade replikeringsprinciper för Azure Site Recovery eller en speciell replikeringsprincip efter namn.</span><span class="sxs-lookup"><span data-stu-id="872e5-109">The **Get-AzureRmRecoveryServicesAsrPolicy** cmdlet gets the list of configured Azure Site Recovery replication policies or a specific replication policy by name.</span></span>

## <span data-ttu-id="872e5-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="872e5-110">EXAMPLES</span></span>

### <span data-ttu-id="872e5-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="872e5-111">Example 1</span></span>
```
PS C:\> $Policy = Get-AzureRmRecoveryServicesAsrPolicy
```

<span data-ttu-id="872e5-112">Retuns listan över replikeringsprinciper</span><span class="sxs-lookup"><span data-stu-id="872e5-112">Retuns the list of replication policies</span></span>

### <span data-ttu-id="872e5-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="872e5-113">Example 2</span></span>
```
PS C:\>  Get-AzureRmRecoveryServicesAsrPolicy -Name abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="872e5-114">Retuns med namn.</span><span class="sxs-lookup"><span data-stu-id="872e5-114">Retuns replication policy with name.</span></span>

### <span data-ttu-id="872e5-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="872e5-115">Example 3</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrPolicy -FriendlyName abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="872e5-116">Returnerar replikeringsprincipen med angivet eget namn.</span><span class="sxs-lookup"><span data-stu-id="872e5-116">Returns the replication policy with the specified friendly name.</span></span>

## <span data-ttu-id="872e5-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="872e5-117">PARAMETERS</span></span>

### <span data-ttu-id="872e5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="872e5-118">-DefaultProfile</span></span>
<span data-ttu-id="872e5-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="872e5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="872e5-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="872e5-120">-FriendlyName</span></span>
<span data-ttu-id="872e5-121">Anger det egna namnet på ASR-replikeringsprincipen.</span><span class="sxs-lookup"><span data-stu-id="872e5-121">Specifies the friendly name of the ASR replication policy.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="872e5-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="872e5-122">-Name</span></span>
<span data-ttu-id="872e5-123">Anger namnet på auktoriseringsprincipen för automatisk system återställning.</span><span class="sxs-lookup"><span data-stu-id="872e5-123">Specifies the name of the ASR replication policy.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="872e5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="872e5-124">CommonParameters</span></span>
<span data-ttu-id="872e5-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="872e5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="872e5-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="872e5-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="872e5-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="872e5-127">INPUTS</span></span>

### <span data-ttu-id="872e5-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="872e5-128">None</span></span>

## <span data-ttu-id="872e5-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="872e5-129">OUTPUTS</span></span>

### <span data-ttu-id="872e5-130">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRPolicy, Microsoft. Azure. commands. RecoveryServices. SiteRecovery, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="872e5-130">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="872e5-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="872e5-131">NOTES</span></span>

## <span data-ttu-id="872e5-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="872e5-132">RELATED LINKS</span></span>

[<span data-ttu-id="872e5-133">New-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="872e5-133">New-AzureRmRecoveryServicesAsrPolicy</span></span>](./New-AzureRmRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="872e5-134">Remove-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="872e5-134">Remove-AzureRmRecoveryServicesAsrPolicy</span></span>](./Remove-AzureRmRecoveryServicesAsrPolicy.md)
