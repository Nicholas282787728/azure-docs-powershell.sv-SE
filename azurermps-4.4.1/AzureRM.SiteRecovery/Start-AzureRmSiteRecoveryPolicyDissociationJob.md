---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 4F71DC85-B2E0-4E0B-96F6-69D52C577B22
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPolicyDissociationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPolicyDissociationJob.md
ms.openlocfilehash: 7dc64ea2bdbfb5dcbc648143dd094313eb765782
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575796"
---
# <span data-ttu-id="beda7-101">Start-AzureRmSiteRecoveryPolicyDissociationJob</span><span class="sxs-lookup"><span data-stu-id="beda7-101">Start-AzureRmSiteRecoveryPolicyDissociationJob</span></span>

## <span data-ttu-id="beda7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="beda7-102">SYNOPSIS</span></span>
<span data-ttu-id="beda7-103">Startar ett länkat jobb på en replikeringsprincip som är associerad med en behållare för webbplats återställnings skydd.</span><span class="sxs-lookup"><span data-stu-id="beda7-103">Starts a dissociation job on a replication policy associated with a Site Recovery protection container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="beda7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="beda7-104">SYNTAX</span></span>

### <span data-ttu-id="beda7-105">EnterpriseToAzure (standard)</span><span class="sxs-lookup"><span data-stu-id="beda7-105">EnterpriseToAzure (Default)</span></span>
```
Start-AzureRmSiteRecoveryPolicyDissociationJob -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="beda7-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="beda7-106">EnterpriseToEnterprise</span></span>
```
Start-AzureRmSiteRecoveryPolicyDissociationJob -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="beda7-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="beda7-107">DESCRIPTION</span></span>
<span data-ttu-id="beda7-108">Cmdleten **Start-AzureRmSiteRecoveryPolicyDissociationJob** initierar ett länkat jobb på den replikeringsprincip som är kopplad till en Azure Site Recovery-behållare.</span><span class="sxs-lookup"><span data-stu-id="beda7-108">The **Start-AzureRmSiteRecoveryPolicyDissociationJob** cmdlet initiates a dissociation job on the replication policy associated with an Azure Site Recovery protection container.</span></span>

## <span data-ttu-id="beda7-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="beda7-109">EXAMPLES</span></span>

## <span data-ttu-id="beda7-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="beda7-110">PARAMETERS</span></span>

### <span data-ttu-id="beda7-111">-Princip</span><span class="sxs-lookup"><span data-stu-id="beda7-111">-Policy</span></span>
<span data-ttu-id="beda7-112">Anger ett Azure Site Recovery-princip objekt.</span><span class="sxs-lookup"><span data-stu-id="beda7-112">Specifies an Azure Site Recovery policy object.</span></span>

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

### <span data-ttu-id="beda7-113">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="beda7-113">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="beda7-114">Anger en primär skydds behållare.</span><span class="sxs-lookup"><span data-stu-id="beda7-114">Specifies a primary protection container.</span></span>

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

### <span data-ttu-id="beda7-115">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="beda7-115">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="beda7-116">Anger en återställnings skydds behållare.</span><span class="sxs-lookup"><span data-stu-id="beda7-116">Specifies a recovery protection container.</span></span>

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

### <span data-ttu-id="beda7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="beda7-117">-DefaultProfile</span></span>
<span data-ttu-id="beda7-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="beda7-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="beda7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="beda7-119">CommonParameters</span></span>
<span data-ttu-id="beda7-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="beda7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="beda7-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="beda7-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="beda7-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="beda7-122">INPUTS</span></span>

### <span data-ttu-id="beda7-123">ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="beda7-123">ASRPolicy</span></span>
<span data-ttu-id="beda7-124">Parametern ' policy ' godkänner värdet av typen ' ASRPolicy ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="beda7-124">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="beda7-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="beda7-125">OUTPUTS</span></span>

### <span data-ttu-id="beda7-126">Microsoft. Azure. commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="beda7-126">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="beda7-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="beda7-127">NOTES</span></span>

## <span data-ttu-id="beda7-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="beda7-128">RELATED LINKS</span></span>

