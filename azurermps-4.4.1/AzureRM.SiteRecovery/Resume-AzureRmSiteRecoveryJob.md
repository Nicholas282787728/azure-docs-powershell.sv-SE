---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 3F827EA0-7CF9-49F8-93BB-B15078A8BBB7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Resume-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Resume-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: 5514d7cec58c2ecad7a4b9c79b3d4d2ad77a5ef3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756540"
---
# <span data-ttu-id="0a080-101">Resume-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="0a080-101">Resume-AzureRmSiteRecoveryJob</span></span>

## <span data-ttu-id="0a080-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0a080-102">SYNOPSIS</span></span>
<span data-ttu-id="0a080-103">Återupptar en pausad webbplats återställnings jobb.</span><span class="sxs-lookup"><span data-stu-id="0a080-103">Resumes a suspended Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a080-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0a080-104">SYNTAX</span></span>

### <span data-ttu-id="0a080-105">ByObject (standard)</span><span class="sxs-lookup"><span data-stu-id="0a080-105">ByObject (Default)</span></span>
```
Resume-AzureRmSiteRecoveryJob -Job <ASRJob> [-Comments <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0a080-106">ByName</span><span class="sxs-lookup"><span data-stu-id="0a080-106">ByName</span></span>
```
Resume-AzureRmSiteRecoveryJob -Name <String> [-Comments <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0a080-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0a080-107">DESCRIPTION</span></span>
<span data-ttu-id="0a080-108">Cmdleten **Resume-AzureRmSiteRecoveryJob** återupptar en pausad Azure Site Recovery-jobb.</span><span class="sxs-lookup"><span data-stu-id="0a080-108">The **Resume-AzureRmSiteRecoveryJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="0a080-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0a080-109">EXAMPLES</span></span>

## <span data-ttu-id="0a080-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0a080-110">PARAMETERS</span></span>

### <span data-ttu-id="0a080-111">-Kommentarer</span><span class="sxs-lookup"><span data-stu-id="0a080-111">-Comments</span></span>
<span data-ttu-id="0a080-112">Anger kommentarer för jobb loggen.</span><span class="sxs-lookup"><span data-stu-id="0a080-112">Specifies the comments for the job log.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a080-113">-Jobb</span><span class="sxs-lookup"><span data-stu-id="0a080-113">-Job</span></span>
<span data-ttu-id="0a080-114">Anger jobbobjektet för webbplats återställningen.</span><span class="sxs-lookup"><span data-stu-id="0a080-114">Specifies the Site Recovery job object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRJob
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a080-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="0a080-115">-Name</span></span>
<span data-ttu-id="0a080-116">Anger det unika namnet för jobbet.</span><span class="sxs-lookup"><span data-stu-id="0a080-116">Specifies the unique name for the job.</span></span>

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

### <span data-ttu-id="0a080-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a080-117">-DefaultProfile</span></span>
<span data-ttu-id="0a080-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0a080-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a080-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a080-119">CommonParameters</span></span>
<span data-ttu-id="0a080-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a080-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a080-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a080-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a080-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0a080-122">INPUTS</span></span>

### <span data-ttu-id="0a080-123">ASRJob</span><span class="sxs-lookup"><span data-stu-id="0a080-123">ASRJob</span></span>
<span data-ttu-id="0a080-124">Parametern ' Job ' godkänner värdet av typen ' ASRJob ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="0a080-124">Parameter 'Job' accepts value of type 'ASRJob' from the pipeline</span></span>

## <span data-ttu-id="0a080-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0a080-125">OUTPUTS</span></span>

### <span data-ttu-id="0a080-126">Microsoft. Azure. commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="0a080-126">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="0a080-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0a080-127">NOTES</span></span>

## <span data-ttu-id="0a080-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0a080-128">RELATED LINKS</span></span>

[<span data-ttu-id="0a080-129">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="0a080-129">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="0a080-130">Restart-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="0a080-130">Restart-AzureRmSiteRecoveryJob</span></span>](./Restart-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="0a080-131">Stopp-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="0a080-131">Stop-AzureRmSiteRecoveryJob</span></span>](./Stop-AzureRmSiteRecoveryJob.md)
