---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 133668A0-0D11-4034-A743-4C0D3CE0FAF1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryVaultSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryVaultSettings.md
ms.openlocfilehash: 9c252649ea668e666c98719ab2045e99e729a836
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581255"
---
# <span data-ttu-id="65f0d-101">Set-AzureRmSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="65f0d-101">Set-AzureRmSiteRecoveryVaultSettings</span></span>

## <span data-ttu-id="65f0d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="65f0d-102">SYNOPSIS</span></span>
<span data-ttu-id="65f0d-103">Anger kontext för webbplats återställnings valv för fler åtgärder.</span><span class="sxs-lookup"><span data-stu-id="65f0d-103">Sets the Site Recovery vault context for further operations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65f0d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="65f0d-104">SYNTAX</span></span>

### <span data-ttu-id="65f0d-105">AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="65f0d-105">AzureSiteRecoveryVault</span></span>
```
Set-AzureRmSiteRecoveryVaultSettings -ASRVault <ASRVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="65f0d-106">AzureRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="65f0d-106">AzureRecoveryServicesVault</span></span>
```
Set-AzureRmSiteRecoveryVaultSettings -ARSVault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="65f0d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="65f0d-107">DESCRIPTION</span></span>
<span data-ttu-id="65f0d-108">Cmdleten **set-AzureRmSiteRecoveryVaultSettings** anger kontext för Azure Site Recovery-Valve för fler åtgärder.</span><span class="sxs-lookup"><span data-stu-id="65f0d-108">The **Set-AzureRmSiteRecoveryVaultSettings** cmdlet sets the Azure Site Recovery vault context for further operations.</span></span>
<span data-ttu-id="65f0d-109">Detta gäller inte Recovery Services-valv.</span><span class="sxs-lookup"><span data-stu-id="65f0d-109">This does not apply to recovery services vaults.</span></span>

## <span data-ttu-id="65f0d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="65f0d-110">EXAMPLES</span></span>

## <span data-ttu-id="65f0d-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="65f0d-111">PARAMETERS</span></span>

### <span data-ttu-id="65f0d-112">-ARSVault</span><span class="sxs-lookup"><span data-stu-id="65f0d-112">-ARSVault</span></span>
<span data-ttu-id="65f0d-113">Anger ett **ARSVault** -objekt.</span><span class="sxs-lookup"><span data-stu-id="65f0d-113">Specifies an **ARSVault** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: AzureRecoveryServicesVault
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65f0d-114">-ASRVault</span><span class="sxs-lookup"><span data-stu-id="65f0d-114">-ASRVault</span></span>
<span data-ttu-id="65f0d-115">Anger ett **ASRVault** -objekt.</span><span class="sxs-lookup"><span data-stu-id="65f0d-115">Specifies an **ASRVault** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRVault
Parameter Sets: AzureSiteRecoveryVault
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65f0d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65f0d-116">-DefaultProfile</span></span>
<span data-ttu-id="65f0d-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="65f0d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65f0d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65f0d-118">CommonParameters</span></span>
<span data-ttu-id="65f0d-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65f0d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65f0d-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65f0d-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65f0d-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="65f0d-121">INPUTS</span></span>

### <span data-ttu-id="65f0d-122">ARSVault</span><span class="sxs-lookup"><span data-stu-id="65f0d-122">ARSVault</span></span>
<span data-ttu-id="65f0d-123">Parametern ' ARSVault ' godkänner värdet av typen ' ARSVault ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="65f0d-123">Parameter 'ARSVault' accepts value of type 'ARSVault' from the pipeline</span></span>

### <span data-ttu-id="65f0d-124">ASRVault</span><span class="sxs-lookup"><span data-stu-id="65f0d-124">ASRVault</span></span>
<span data-ttu-id="65f0d-125">Parametern ' ASRVault ' godkänner värdet av typen ' ASRVault ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="65f0d-125">Parameter 'ASRVault' accepts value of type 'ASRVault' from the pipeline</span></span>

## <span data-ttu-id="65f0d-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="65f0d-126">OUTPUTS</span></span>

### <span data-ttu-id="65f0d-127">Microsoft. Azure. commands. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="65f0d-127">Microsoft.Azure.Commands.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="65f0d-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="65f0d-128">NOTES</span></span>

## <span data-ttu-id="65f0d-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="65f0d-129">RELATED LINKS</span></span>

[<span data-ttu-id="65f0d-130">Get-AzureRmSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="65f0d-130">Get-AzureRmSiteRecoveryVaultSettings</span></span>](./Get-AzureRmSiteRecoveryVaultSettings.md)
