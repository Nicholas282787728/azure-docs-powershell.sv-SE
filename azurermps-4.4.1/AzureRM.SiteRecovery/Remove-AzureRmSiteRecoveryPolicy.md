---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: C4C624DB-BBE8-4F94-BDC6-C012482F7271
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryPolicy.md
ms.openlocfilehash: 3b01e089271cc131af5a4258c46836a87104ef62
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755913"
---
# <span data-ttu-id="15562-101">Remove-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="15562-101">Remove-AzureRmSiteRecoveryPolicy</span></span>

## <span data-ttu-id="15562-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="15562-102">SYNOPSIS</span></span>
<span data-ttu-id="15562-103">Tar bort en replikeringsprincip för en webbplats återställning.</span><span class="sxs-lookup"><span data-stu-id="15562-103">Removes a Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15562-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="15562-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryPolicy -Policy <ASRPolicy> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="15562-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="15562-105">DESCRIPTION</span></span>
<span data-ttu-id="15562-106">Cmdleten **Remove-AzureRMSiteRecoveryPolicy** tar bort en Azure Site Recovery-replikeringsprincip.</span><span class="sxs-lookup"><span data-stu-id="15562-106">The **Remove-AzureRMSiteRecoveryPolicy** cmdlet removes an Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="15562-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="15562-107">EXAMPLES</span></span>

## <span data-ttu-id="15562-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="15562-108">PARAMETERS</span></span>

### <span data-ttu-id="15562-109">-Princip</span><span class="sxs-lookup"><span data-stu-id="15562-109">-Policy</span></span>
<span data-ttu-id="15562-110">Anger principobjektet för webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="15562-110">Specifies the Site Recovery policy object.</span></span>

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

### <span data-ttu-id="15562-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15562-111">-DefaultProfile</span></span>
<span data-ttu-id="15562-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="15562-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15562-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15562-113">CommonParameters</span></span>
<span data-ttu-id="15562-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15562-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15562-115">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15562-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15562-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="15562-116">INPUTS</span></span>

### <span data-ttu-id="15562-117">ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="15562-117">ASRPolicy</span></span>
<span data-ttu-id="15562-118">Parametern ' policy ' godkänner värdet av typen ' ASRPolicy ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="15562-118">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="15562-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="15562-119">OUTPUTS</span></span>

## <span data-ttu-id="15562-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="15562-120">NOTES</span></span>

## <span data-ttu-id="15562-121">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="15562-121">RELATED LINKS</span></span>

[<span data-ttu-id="15562-122">Get-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="15562-122">Get-AzureRmSiteRecoveryPolicy</span></span>](./Get-AzureRmSiteRecoveryPolicy.md)

[<span data-ttu-id="15562-123">New-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="15562-123">New-AzureRmSiteRecoveryPolicy</span></span>](./New-AzureRmSiteRecoveryPolicy.md)
