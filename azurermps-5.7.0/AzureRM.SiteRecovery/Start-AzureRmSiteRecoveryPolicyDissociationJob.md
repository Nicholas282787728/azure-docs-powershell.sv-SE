---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 4F71DC85-B2E0-4E0B-96F6-69D52C577B22
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/start-azurermsiterecoverypolicydissociationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPolicyDissociationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPolicyDissociationJob.md
ms.openlocfilehash: eb12462b85c4a12416f41f899ebc9b2c46cca465
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581960"
---
# <span data-ttu-id="fbcb5-101">Start-AzureRmSiteRecoveryPolicyDissociationJob</span><span class="sxs-lookup"><span data-stu-id="fbcb5-101">Start-AzureRmSiteRecoveryPolicyDissociationJob</span></span>

## <span data-ttu-id="fbcb5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fbcb5-102">SYNOPSIS</span></span>
<span data-ttu-id="fbcb5-103">Startar ett länkat jobb på en replikeringsprincip som är associerad med en behållare för webbplats återställnings skydd.</span><span class="sxs-lookup"><span data-stu-id="fbcb5-103">Starts a dissociation job on a replication policy associated with a Site Recovery protection container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fbcb5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fbcb5-104">SYNTAX</span></span>

### <span data-ttu-id="fbcb5-105">EnterpriseToAzure (standard)</span><span class="sxs-lookup"><span data-stu-id="fbcb5-105">EnterpriseToAzure (Default)</span></span>
```
Start-AzureRmSiteRecoveryPolicyDissociationJob -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fbcb5-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="fbcb5-106">EnterpriseToEnterprise</span></span>
```
Start-AzureRmSiteRecoveryPolicyDissociationJob -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fbcb5-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fbcb5-107">DESCRIPTION</span></span>
<span data-ttu-id="fbcb5-108">Cmdleten **Start-AzureRmSiteRecoveryPolicyDissociationJob** initierar ett länkat jobb på den replikeringsprincip som är kopplad till en Azure Site Recovery-behållare.</span><span class="sxs-lookup"><span data-stu-id="fbcb5-108">The **Start-AzureRmSiteRecoveryPolicyDissociationJob** cmdlet initiates a dissociation job on the replication policy associated with an Azure Site Recovery protection container.</span></span>

## <span data-ttu-id="fbcb5-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fbcb5-109">EXAMPLES</span></span>

## <span data-ttu-id="fbcb5-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fbcb5-110">PARAMETERS</span></span>

### <span data-ttu-id="fbcb5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbcb5-111">-DefaultProfile</span></span>
<span data-ttu-id="fbcb5-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fbcb5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fbcb5-113">-Princip</span><span class="sxs-lookup"><span data-stu-id="fbcb5-113">-Policy</span></span>
<span data-ttu-id="fbcb5-114">Anger ett Azure Site Recovery-princip objekt.</span><span class="sxs-lookup"><span data-stu-id="fbcb5-114">Specifies an Azure Site Recovery policy object.</span></span>

```yaml
Type: ASRPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fbcb5-115">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="fbcb5-115">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="fbcb5-116">Anger en primär skydds behållare.</span><span class="sxs-lookup"><span data-stu-id="fbcb5-116">Specifies a primary protection container.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbcb5-117">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="fbcb5-117">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="fbcb5-118">Anger en återställnings skydds behållare.</span><span class="sxs-lookup"><span data-stu-id="fbcb5-118">Specifies a recovery protection container.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbcb5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbcb5-119">CommonParameters</span></span>
<span data-ttu-id="fbcb5-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbcb5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbcb5-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbcb5-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbcb5-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fbcb5-122">INPUTS</span></span>

### <span data-ttu-id="fbcb5-123">ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="fbcb5-123">ASRPolicy</span></span>
<span data-ttu-id="fbcb5-124">Parametern ' policy ' godkänner värdet av typen ' ASRPolicy ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="fbcb5-124">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="fbcb5-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fbcb5-125">OUTPUTS</span></span>

### <span data-ttu-id="fbcb5-126">Microsoft. Azure. commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="fbcb5-126">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="fbcb5-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fbcb5-127">NOTES</span></span>

## <span data-ttu-id="fbcb5-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fbcb5-128">RELATED LINKS</span></span>

