---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 3DDC8DD8-889C-4C76-B32E-3D2C2AD0AC79
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPolicyAssociationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPolicyAssociationJob.md
ms.openlocfilehash: 477f31ea84c5cb3e9c06b79e1ae70f5ae8a93925
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582183"
---
# <span data-ttu-id="b08de-101">Start-AzureRmSiteRecoveryPolicyAssociationJob</span><span class="sxs-lookup"><span data-stu-id="b08de-101">Start-AzureRmSiteRecoveryPolicyAssociationJob</span></span>

## <span data-ttu-id="b08de-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b08de-102">SYNOPSIS</span></span>
<span data-ttu-id="b08de-103">Startar ett projekt för en replikeringsprincip för webbplats återställning.</span><span class="sxs-lookup"><span data-stu-id="b08de-103">Starts a Site Recovery replication policy association job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b08de-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b08de-104">SYNTAX</span></span>

### <span data-ttu-id="b08de-105">EnterpriseToAzure (standard)</span><span class="sxs-lookup"><span data-stu-id="b08de-105">EnterpriseToAzure (Default)</span></span>
```
Start-AzureRmSiteRecoveryPolicyAssociationJob -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b08de-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="b08de-106">EnterpriseToEnterprise</span></span>
```
Start-AzureRmSiteRecoveryPolicyAssociationJob -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b08de-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b08de-107">DESCRIPTION</span></span>
<span data-ttu-id="b08de-108">Cmdleten **Start-AzureRmSiteRecoveryPolicyAssociationJob** initierar ett Associations jobb för att koppla en replikeringsprincip till en Azure Site Recovery Protection-behållare.</span><span class="sxs-lookup"><span data-stu-id="b08de-108">The **Start-AzureRmSiteRecoveryPolicyAssociationJob** cmdlet initiates an association job to associate a replication policy with an Azure Site Recovery protection container.</span></span>

## <span data-ttu-id="b08de-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b08de-109">EXAMPLES</span></span>

## <span data-ttu-id="b08de-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b08de-110">PARAMETERS</span></span>

### <span data-ttu-id="b08de-111">-Princip</span><span class="sxs-lookup"><span data-stu-id="b08de-111">-Policy</span></span>
<span data-ttu-id="b08de-112">Anger principobjektet för webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="b08de-112">Specifies the Site Recovery policy object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b08de-113">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="b08de-113">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="b08de-114">Anger den primära skydds behållaren där inställningarna för skydds profilen ska tillämpas.</span><span class="sxs-lookup"><span data-stu-id="b08de-114">Specifies the primary protection container on which to apply the protection profile settings.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b08de-115">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="b08de-115">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="b08de-116">Anger återställnings skydds behållaren där inställningarna för skydds profilen ska tillämpas.</span><span class="sxs-lookup"><span data-stu-id="b08de-116">Specifies the recovery protection container on which to apply the protection profile settings.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b08de-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b08de-117">-DefaultProfile</span></span>
<span data-ttu-id="b08de-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b08de-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b08de-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b08de-119">CommonParameters</span></span>
<span data-ttu-id="b08de-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b08de-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b08de-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b08de-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b08de-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b08de-122">INPUTS</span></span>

### <span data-ttu-id="b08de-123">ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="b08de-123">ASRPolicy</span></span>
<span data-ttu-id="b08de-124">Parametern ' policy ' godkänner värdet av typen ' ASRPolicy ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="b08de-124">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="b08de-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b08de-125">OUTPUTS</span></span>

### <span data-ttu-id="b08de-126">Microsoft. Azure. commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="b08de-126">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="b08de-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b08de-127">NOTES</span></span>

## <span data-ttu-id="b08de-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b08de-128">RELATED LINKS</span></span>

