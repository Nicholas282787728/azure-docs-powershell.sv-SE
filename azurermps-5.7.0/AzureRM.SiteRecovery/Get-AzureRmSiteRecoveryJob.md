---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: B5CA6FD9-49EE-4115-8477-551CE5D8E6CE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: dc8a1e6cfe8c3d68af0f8c413a0e96cac9feaee8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579360"
---
# <span data-ttu-id="4726a-101">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="4726a-101">Get-AzureRmSiteRecoveryJob</span></span>

## <span data-ttu-id="4726a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4726a-102">SYNOPSIS</span></span>
<span data-ttu-id="4726a-103">Hämtar åtgärds informationen för det aktuella Site Recovery-valvet.</span><span class="sxs-lookup"><span data-stu-id="4726a-103">Gets the operation information for the current Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4726a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4726a-104">SYNTAX</span></span>

### <span data-ttu-id="4726a-105">ByParam (standard)</span><span class="sxs-lookup"><span data-stu-id="4726a-105">ByParam (Default)</span></span>
```
Get-AzureRmSiteRecoveryJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4726a-106">ByName</span><span class="sxs-lookup"><span data-stu-id="4726a-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4726a-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="4726a-107">ByObject</span></span>
```
Get-AzureRmSiteRecoveryJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4726a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4726a-108">DESCRIPTION</span></span>
<span data-ttu-id="4726a-109">Cmdleten **Get-AzureRmSiteRecoveryJob** får Azure Site Recovery-jobb.</span><span class="sxs-lookup"><span data-stu-id="4726a-109">The **Get-AzureRmSiteRecoveryJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="4726a-110">Du kan använda denna cmdlet för att Visa åtgärds informationen för det aktuella Site Recovery-valvet.</span><span class="sxs-lookup"><span data-stu-id="4726a-110">You can use this cmdlet to view the operation information for the current Site Recovery vault.</span></span>

## <span data-ttu-id="4726a-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4726a-111">EXAMPLES</span></span>

## <span data-ttu-id="4726a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4726a-112">PARAMETERS</span></span>

### <span data-ttu-id="4726a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4726a-113">-DefaultProfile</span></span>
<span data-ttu-id="4726a-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4726a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4726a-115">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="4726a-115">-EndTime</span></span>
<span data-ttu-id="4726a-116">Anger slut tiden för jobben.</span><span class="sxs-lookup"><span data-stu-id="4726a-116">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="4726a-117">Denna cmdlet hämtar alla jobb som startade före angiven tid.</span><span class="sxs-lookup"><span data-stu-id="4726a-117">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="4726a-118">Om du vill hämta ett **datetime** -objekt för den här parametern använder du Get-Date cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4726a-118">To obtain a **DateTime** object for this parameter, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="4726a-119">Om du vill ha mer information skriver du `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="4726a-119">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4726a-120">-Jobb</span><span class="sxs-lookup"><span data-stu-id="4726a-120">-Job</span></span>
<span data-ttu-id="4726a-121">Anger återställnings jobbet för webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="4726a-121">Specifies the Site Recovery job.</span></span>

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

### <span data-ttu-id="4726a-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="4726a-122">-Name</span></span>
<span data-ttu-id="4726a-123">Anger ett unikt namn som identifierar jobbet.</span><span class="sxs-lookup"><span data-stu-id="4726a-123">Specifies a unique name that identifies the job.</span></span>

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

### <span data-ttu-id="4726a-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="4726a-124">-StartTime</span></span>
<span data-ttu-id="4726a-125">Anger start tiden för jobben.</span><span class="sxs-lookup"><span data-stu-id="4726a-125">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="4726a-126">Denna cmdlet hämtar alla jobb som startas efter den angivna tiden.</span><span class="sxs-lookup"><span data-stu-id="4726a-126">This cmdlet gets all jobs that started after the specified time.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4726a-127">-State</span><span class="sxs-lookup"><span data-stu-id="4726a-127">-State</span></span>
<span data-ttu-id="4726a-128">Anger inmatnings läget för ett webbplats återställnings jobb.</span><span class="sxs-lookup"><span data-stu-id="4726a-128">Specifies the input state for a Site Recovery job.</span></span>
<span data-ttu-id="4726a-129">Denna cmdlet hämtar alla jobb som matchar det angivna tillståndet.</span><span class="sxs-lookup"><span data-stu-id="4726a-129">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="4726a-130">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="4726a-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4726a-131">NotStarted</span><span class="sxs-lookup"><span data-stu-id="4726a-131">NotStarted</span></span>
- <span data-ttu-id="4726a-132">Inaktive</span><span class="sxs-lookup"><span data-stu-id="4726a-132">InProgress</span></span>
- <span data-ttu-id="4726a-133">Utför</span><span class="sxs-lookup"><span data-stu-id="4726a-133">Succeeded</span></span>
- <span data-ttu-id="4726a-134">Övrigt</span><span class="sxs-lookup"><span data-stu-id="4726a-134">Other</span></span>
- <span data-ttu-id="4726a-135">Startade</span><span class="sxs-lookup"><span data-stu-id="4726a-135">Failed</span></span>
- <span data-ttu-id="4726a-136">Annullerats</span><span class="sxs-lookup"><span data-stu-id="4726a-136">Cancelled</span></span>
- <span data-ttu-id="4726a-137">Hängande</span><span class="sxs-lookup"><span data-stu-id="4726a-137">Suspended</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 
Accepted values: NotStarted, InProgress, Succeeded, Other, Failed, Cancelled, Suspended

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4726a-138">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="4726a-138">-TargetObjectId</span></span>
<span data-ttu-id="4726a-139">Anger ID för det objekt som är inriktat för jobbet.</span><span class="sxs-lookup"><span data-stu-id="4726a-139">Specifies the ID of the object targeted by the job.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4726a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4726a-140">CommonParameters</span></span>
<span data-ttu-id="4726a-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4726a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4726a-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4726a-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4726a-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4726a-143">INPUTS</span></span>

### <span data-ttu-id="4726a-144">ASRJob</span><span class="sxs-lookup"><span data-stu-id="4726a-144">ASRJob</span></span>
<span data-ttu-id="4726a-145">Parametern ' Job ' godkänner värdet av typen ' ASRJob ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="4726a-145">Parameter 'Job' accepts value of type 'ASRJob' from the pipeline</span></span>

## <span data-ttu-id="4726a-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4726a-146">OUTPUTS</span></span>

### <span data-ttu-id="4726a-147">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. commands. SiteRecovery. ASRJob]</span><span class="sxs-lookup"><span data-stu-id="4726a-147">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRJob]</span></span>

## <span data-ttu-id="4726a-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4726a-148">NOTES</span></span>

## <span data-ttu-id="4726a-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4726a-149">RELATED LINKS</span></span>

[<span data-ttu-id="4726a-150">Restart-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="4726a-150">Restart-AzureRmSiteRecoveryJob</span></span>](./Restart-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="4726a-151">Resume-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="4726a-151">Resume-AzureRmSiteRecoveryJob</span></span>](./Resume-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="4726a-152">Stopp-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="4726a-152">Stop-AzureRmSiteRecoveryJob</span></span>](./Stop-AzureRmSiteRecoveryJob.md)
