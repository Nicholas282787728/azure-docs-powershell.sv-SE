---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: BDEA3F9D-AC23-402D-BA1F-AC617C7480A1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoverynetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryNetworkMapping.md
ms.openlocfilehash: 481d2d414cde32e9d0b99cedd5b942b7bed9b248
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582943"
---
# <span data-ttu-id="3b474-101">Remove-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="3b474-101">Remove-AzureRmSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="3b474-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3b474-102">SYNOPSIS</span></span>
<span data-ttu-id="3b474-103">Tar bort en nätverks mappning från det aktuella återställnings valvet för webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="3b474-103">Removes a network mapping from the current Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b474-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3b474-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryNetworkMapping -NetworkMapping <ASRNetworkMapping>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b474-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3b474-105">DESCRIPTION</span></span>
<span data-ttu-id="3b474-106">Cmdleten **Remove-AzureRMSiteRecoveryNetworkMapping** tar bort en nätverks mappning från det aktuella Azure Site Recovery-valvet.</span><span class="sxs-lookup"><span data-stu-id="3b474-106">The **Remove-AzureRMSiteRecoveryNetworkMapping** cmdlet removes a network mapping from the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="3b474-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3b474-107">EXAMPLES</span></span>

## <span data-ttu-id="3b474-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3b474-108">PARAMETERS</span></span>

### <span data-ttu-id="3b474-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b474-109">-DefaultProfile</span></span>
<span data-ttu-id="3b474-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3b474-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b474-111">-NetworkMapping</span><span class="sxs-lookup"><span data-stu-id="3b474-111">-NetworkMapping</span></span>
<span data-ttu-id="3b474-112">Anger objektet nätverks mappning.</span><span class="sxs-lookup"><span data-stu-id="3b474-112">Specifies the network mapping object.</span></span>

```yaml
Type: ASRNetworkMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b474-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b474-113">CommonParameters</span></span>
<span data-ttu-id="3b474-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b474-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b474-115">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b474-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b474-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3b474-116">INPUTS</span></span>

### <span data-ttu-id="3b474-117">ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="3b474-117">ASRNetworkMapping</span></span>
<span data-ttu-id="3b474-118">Parametern ' NetworkMapping ' godkänner värdet av typen ' ASRNetworkMapping ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="3b474-118">Parameter 'NetworkMapping' accepts value of type 'ASRNetworkMapping' from the pipeline</span></span>

## <span data-ttu-id="3b474-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3b474-119">OUTPUTS</span></span>

### <span data-ttu-id="3b474-120">Microsoft. Azure. commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="3b474-120">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="3b474-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3b474-121">NOTES</span></span>

## <span data-ttu-id="3b474-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3b474-122">RELATED LINKS</span></span>

[<span data-ttu-id="3b474-123">Get-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="3b474-123">Get-AzureRmSiteRecoveryNetworkMapping</span></span>](./Get-AzureRmSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="3b474-124">New-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="3b474-124">New-AzureRmSiteRecoveryNetworkMapping</span></span>](./New-AzureRmSiteRecoveryNetworkMapping.md)
