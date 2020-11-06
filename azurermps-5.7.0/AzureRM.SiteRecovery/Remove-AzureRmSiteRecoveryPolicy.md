---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: C4C624DB-BBE8-4F94-BDC6-C012482F7271
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoverypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryPolicy.md
ms.openlocfilehash: f09ca4bb6c033b954542d6c734b27bf5f2236d87
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573271"
---
# <span data-ttu-id="b6f71-101">Remove-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="b6f71-101">Remove-AzureRmSiteRecoveryPolicy</span></span>

## <span data-ttu-id="b6f71-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b6f71-102">SYNOPSIS</span></span>
<span data-ttu-id="b6f71-103">Tar bort en replikeringsprincip för en webbplats återställning.</span><span class="sxs-lookup"><span data-stu-id="b6f71-103">Removes a Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6f71-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b6f71-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryPolicy -Policy <ASRPolicy> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b6f71-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b6f71-105">DESCRIPTION</span></span>
<span data-ttu-id="b6f71-106">Cmdleten **Remove-AzureRMSiteRecoveryPolicy** tar bort en Azure Site Recovery-replikeringsprincip.</span><span class="sxs-lookup"><span data-stu-id="b6f71-106">The **Remove-AzureRMSiteRecoveryPolicy** cmdlet removes an Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="b6f71-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b6f71-107">EXAMPLES</span></span>

## <span data-ttu-id="b6f71-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b6f71-108">PARAMETERS</span></span>

### <span data-ttu-id="b6f71-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6f71-109">-DefaultProfile</span></span>
<span data-ttu-id="b6f71-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b6f71-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6f71-111">-Princip</span><span class="sxs-lookup"><span data-stu-id="b6f71-111">-Policy</span></span>
<span data-ttu-id="b6f71-112">Anger principobjektet för webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="b6f71-112">Specifies the Site Recovery policy object.</span></span>

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

### <span data-ttu-id="b6f71-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6f71-113">CommonParameters</span></span>
<span data-ttu-id="b6f71-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6f71-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6f71-115">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6f71-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6f71-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b6f71-116">INPUTS</span></span>

### <span data-ttu-id="b6f71-117">ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="b6f71-117">ASRPolicy</span></span>
<span data-ttu-id="b6f71-118">Parametern ' policy ' godkänner värdet av typen ' ASRPolicy ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="b6f71-118">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="b6f71-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b6f71-119">OUTPUTS</span></span>

## <span data-ttu-id="b6f71-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b6f71-120">NOTES</span></span>

## <span data-ttu-id="b6f71-121">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b6f71-121">RELATED LINKS</span></span>

[<span data-ttu-id="b6f71-122">Get-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="b6f71-122">Get-AzureRmSiteRecoveryPolicy</span></span>](./Get-AzureRmSiteRecoveryPolicy.md)

[<span data-ttu-id="b6f71-123">New-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="b6f71-123">New-AzureRmSiteRecoveryPolicy</span></span>](./New-AzureRmSiteRecoveryPolicy.md)
