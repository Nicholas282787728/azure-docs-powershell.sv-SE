---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: CFEA76B4-684C-4C2A-9806-36DC133AEE80
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/stop-azurermsiterecoveryjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Stop-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Stop-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: 44875207b5a4317b2ceb9a0284a3818a6be36298
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573243"
---
# <span data-ttu-id="467a8-101">Stop-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="467a8-101">Stop-AzureRmSiteRecoveryJob</span></span>

## <span data-ttu-id="467a8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="467a8-102">SYNOPSIS</span></span>
<span data-ttu-id="467a8-103">Stoppar ett återställnings jobb för webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="467a8-103">Stops a Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="467a8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="467a8-104">SYNTAX</span></span>

### <span data-ttu-id="467a8-105">ByObject (standard)</span><span class="sxs-lookup"><span data-stu-id="467a8-105">ByObject (Default)</span></span>
```
Stop-AzureRmSiteRecoveryJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="467a8-106">ByName</span><span class="sxs-lookup"><span data-stu-id="467a8-106">ByName</span></span>
```
Stop-AzureRmSiteRecoveryJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="467a8-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="467a8-107">DESCRIPTION</span></span>
<span data-ttu-id="467a8-108">Cmdleten **Stop-AzureRmSiteRecoveryJob** stoppar ett Azure Site Recovery-jobb.</span><span class="sxs-lookup"><span data-stu-id="467a8-108">The **Stop-AzureRmSiteRecoveryJob** cmdlet stops an Azure Site Recovery job.</span></span>

## <span data-ttu-id="467a8-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="467a8-109">EXAMPLES</span></span>

## <span data-ttu-id="467a8-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="467a8-110">PARAMETERS</span></span>

### <span data-ttu-id="467a8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="467a8-111">-DefaultProfile</span></span>
<span data-ttu-id="467a8-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="467a8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="467a8-113">-Jobb</span><span class="sxs-lookup"><span data-stu-id="467a8-113">-Job</span></span>
<span data-ttu-id="467a8-114">Anger det jobb objekt för webbplats återställning som ska stoppas.</span><span class="sxs-lookup"><span data-stu-id="467a8-114">Specifies the Site Recovery job object to stop.</span></span>

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

### <span data-ttu-id="467a8-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="467a8-115">-Name</span></span>
<span data-ttu-id="467a8-116">Anger det unika namnet på jobbet för webbplats återställning att stoppa.</span><span class="sxs-lookup"><span data-stu-id="467a8-116">Specifies the unique name for the Site Recovery job to stop.</span></span>

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

### <span data-ttu-id="467a8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="467a8-117">CommonParameters</span></span>
<span data-ttu-id="467a8-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="467a8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="467a8-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="467a8-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="467a8-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="467a8-120">INPUTS</span></span>

### <span data-ttu-id="467a8-121">ASRJob</span><span class="sxs-lookup"><span data-stu-id="467a8-121">ASRJob</span></span>
<span data-ttu-id="467a8-122">Parametern ' Job ' godkänner värdet av typen ' ASRJob ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="467a8-122">Parameter 'Job' accepts value of type 'ASRJob' from the pipeline</span></span>

## <span data-ttu-id="467a8-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="467a8-123">OUTPUTS</span></span>

### <span data-ttu-id="467a8-124">Microsoft. Azure. commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="467a8-124">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="467a8-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="467a8-125">NOTES</span></span>

## <span data-ttu-id="467a8-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="467a8-126">RELATED LINKS</span></span>

[<span data-ttu-id="467a8-127">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="467a8-127">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="467a8-128">Restart-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="467a8-128">Restart-AzureRmSiteRecoveryJob</span></span>](./Restart-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="467a8-129">Resume-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="467a8-129">Resume-AzureRmSiteRecoveryJob</span></span>](./Resume-AzureRmSiteRecoveryJob.md)
