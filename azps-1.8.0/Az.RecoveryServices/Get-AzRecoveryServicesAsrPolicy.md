---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: a25375a565db8d2c69a423aa95033033de3f0f8d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747463"
---
# <span data-ttu-id="ca6fa-101">Get-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="ca6fa-101">Get-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="ca6fa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ca6fa-102">SYNOPSIS</span></span>
<span data-ttu-id="ca6fa-103">Får ASR-principer.</span><span class="sxs-lookup"><span data-stu-id="ca6fa-103">Gets ASR replication policies.</span></span>

## <span data-ttu-id="ca6fa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ca6fa-104">SYNTAX</span></span>

### <span data-ttu-id="ca6fa-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="ca6fa-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca6fa-106">ByName</span><span class="sxs-lookup"><span data-stu-id="ca6fa-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrPolicy -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca6fa-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="ca6fa-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrPolicy -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ca6fa-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ca6fa-108">DESCRIPTION</span></span>
<span data-ttu-id="ca6fa-109">Cmdleten **Get-AzRecoveryServicesAsrPolicy** hämtar listan över konfigurerade replikeringsprinciper för Azure Site Recovery eller en speciell replikeringsprincip efter namn.</span><span class="sxs-lookup"><span data-stu-id="ca6fa-109">The **Get-AzRecoveryServicesAsrPolicy** cmdlet gets the list of configured Azure Site Recovery replication policies or a specific replication policy by name.</span></span>

## <span data-ttu-id="ca6fa-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ca6fa-110">EXAMPLES</span></span>

### <span data-ttu-id="ca6fa-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ca6fa-111">Example 1</span></span>
```
PS C:\> $Policy = Get-AzRecoveryServicesAsrPolicy
```

<span data-ttu-id="ca6fa-112">Retuns listan över replikeringsprinciper</span><span class="sxs-lookup"><span data-stu-id="ca6fa-112">Retuns the list of replication policies</span></span>

### <span data-ttu-id="ca6fa-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="ca6fa-113">Example 2</span></span>
```
PS C:\>  Get-AzRecoveryServicesAsrPolicy -Name abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="ca6fa-114">Retuns med namn.</span><span class="sxs-lookup"><span data-stu-id="ca6fa-114">Retuns replication policy with name.</span></span>

### <span data-ttu-id="ca6fa-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="ca6fa-115">Example 3</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrPolicy -FriendlyName abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="ca6fa-116">Returnerar replikeringsprincipen med angivet eget namn.</span><span class="sxs-lookup"><span data-stu-id="ca6fa-116">Returns the replication policy with the specified friendly name.</span></span>

## <span data-ttu-id="ca6fa-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ca6fa-117">PARAMETERS</span></span>

### <span data-ttu-id="ca6fa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca6fa-118">-DefaultProfile</span></span>
<span data-ttu-id="ca6fa-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ca6fa-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="ca6fa-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="ca6fa-120">-FriendlyName</span></span>
<span data-ttu-id="ca6fa-121">Anger det egna namnet på ASR-replikeringsprincipen.</span><span class="sxs-lookup"><span data-stu-id="ca6fa-121">Specifies the friendly name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="ca6fa-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="ca6fa-122">-Name</span></span>
<span data-ttu-id="ca6fa-123">Anger namnet på auktoriseringsprincipen för automatisk system återställning.</span><span class="sxs-lookup"><span data-stu-id="ca6fa-123">Specifies the name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="ca6fa-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca6fa-124">CommonParameters</span></span>
<span data-ttu-id="ca6fa-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca6fa-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca6fa-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca6fa-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca6fa-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ca6fa-127">INPUTS</span></span>

### <span data-ttu-id="ca6fa-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="ca6fa-128">None</span></span>

## <span data-ttu-id="ca6fa-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ca6fa-129">OUTPUTS</span></span>

### <span data-ttu-id="ca6fa-130">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="ca6fa-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="ca6fa-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ca6fa-131">NOTES</span></span>

## <span data-ttu-id="ca6fa-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ca6fa-132">RELATED LINKS</span></span>

[<span data-ttu-id="ca6fa-133">New-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="ca6fa-133">New-AzRecoveryServicesAsrPolicy</span></span>](./New-AzRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="ca6fa-134">Remove-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="ca6fa-134">Remove-AzRecoveryServicesAsrPolicy</span></span>](./Remove-AzRecoveryServicesAsrPolicy.md)
