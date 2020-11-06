---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 5A70AC55-27B4-421E-8EB0-1C7B8DFD3537
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/restart-azurermsiterecoveryjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Restart-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Restart-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: 17486f4a22e488a147fcdd8a8e085c7900fc8147
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573248"
---
# <span data-ttu-id="9538e-101">Restart-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="9538e-101">Restart-AzureRmSiteRecoveryJob</span></span>

## <span data-ttu-id="9538e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9538e-102">SYNOPSIS</span></span>
<span data-ttu-id="9538e-103">Startar om ett Azure Site Recovery-jobb.</span><span class="sxs-lookup"><span data-stu-id="9538e-103">Restarts an Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9538e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9538e-104">SYNTAX</span></span>

### <span data-ttu-id="9538e-105">ByObject (standard)</span><span class="sxs-lookup"><span data-stu-id="9538e-105">ByObject (Default)</span></span>
```
Restart-AzureRmSiteRecoveryJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9538e-106">ByName</span><span class="sxs-lookup"><span data-stu-id="9538e-106">ByName</span></span>
```
Restart-AzureRmSiteRecoveryJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9538e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9538e-107">DESCRIPTION</span></span>
<span data-ttu-id="9538e-108">Cmdleten **restart-AzureRmSiteRecoveryJob** startar om ett Azure Site Recovery-jobb.</span><span class="sxs-lookup"><span data-stu-id="9538e-108">The **Restart-AzureRmSiteRecoveryJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="9538e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9538e-109">EXAMPLES</span></span>

## <span data-ttu-id="9538e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9538e-110">PARAMETERS</span></span>

### <span data-ttu-id="9538e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9538e-111">-DefaultProfile</span></span>
<span data-ttu-id="9538e-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9538e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9538e-113">-Jobb</span><span class="sxs-lookup"><span data-stu-id="9538e-113">-Job</span></span>
<span data-ttu-id="9538e-114">Anger jobbobjektet för webbplats återställningen.</span><span class="sxs-lookup"><span data-stu-id="9538e-114">Specifies the Site Recovery job object.</span></span>

```yaml
Type: ASRJob
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9538e-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="9538e-115">-Name</span></span>
<span data-ttu-id="9538e-116">Anger det unika namnet för jobbet.</span><span class="sxs-lookup"><span data-stu-id="9538e-116">Specifies the unique name for the job.</span></span>

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

### <span data-ttu-id="9538e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9538e-117">CommonParameters</span></span>
<span data-ttu-id="9538e-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9538e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9538e-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9538e-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9538e-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9538e-120">INPUTS</span></span>

### <span data-ttu-id="9538e-121">ASRJob</span><span class="sxs-lookup"><span data-stu-id="9538e-121">ASRJob</span></span>
<span data-ttu-id="9538e-122">Parametern ' Job ' godkänner värdet av typen ' ASRJob ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="9538e-122">Parameter 'Job' accepts value of type 'ASRJob' from the pipeline</span></span>

## <span data-ttu-id="9538e-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9538e-123">OUTPUTS</span></span>

### <span data-ttu-id="9538e-124">Microsoft. Azure. commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="9538e-124">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="9538e-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9538e-125">NOTES</span></span>

## <span data-ttu-id="9538e-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9538e-126">RELATED LINKS</span></span>

[<span data-ttu-id="9538e-127">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="9538e-127">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="9538e-128">Resume-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="9538e-128">Resume-AzureRmSiteRecoveryJob</span></span>](./Resume-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="9538e-129">Stopp-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="9538e-129">Stop-AzureRmSiteRecoveryJob</span></span>](./Stop-AzureRmSiteRecoveryJob.md)
