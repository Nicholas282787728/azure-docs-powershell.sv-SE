---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: B5CA6FD9-49EE-4115-8477-551CE5D8E6CE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: 2365b806bd274bb9cc18f84c83a29423408780d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755631"
---
# <span data-ttu-id="9e3d0-101">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="9e3d0-101">Get-AzureRmSiteRecoveryJob</span></span>

## <span data-ttu-id="9e3d0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9e3d0-102">SYNOPSIS</span></span>
<span data-ttu-id="9e3d0-103">Hämtar åtgärds informationen för det aktuella Site Recovery-valvet.</span><span class="sxs-lookup"><span data-stu-id="9e3d0-103">Gets the operation information for the current Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e3d0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9e3d0-104">SYNTAX</span></span>

### <span data-ttu-id="9e3d0-105">ByParam (standard)</span><span class="sxs-lookup"><span data-stu-id="9e3d0-105">ByParam (Default)</span></span>
```
Get-AzureRmSiteRecoveryJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e3d0-106">ByName</span><span class="sxs-lookup"><span data-stu-id="9e3d0-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e3d0-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="9e3d0-107">ByObject</span></span>
```
Get-AzureRmSiteRecoveryJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e3d0-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9e3d0-108">DESCRIPTION</span></span>
<span data-ttu-id="9e3d0-109">Cmdleten **Get-AzureRmSiteRecoveryJob** får Azure Site Recovery-jobb.</span><span class="sxs-lookup"><span data-stu-id="9e3d0-109">The **Get-AzureRmSiteRecoveryJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="9e3d0-110">Du kan använda denna cmdlet för att Visa åtgärds informationen för det aktuella Site Recovery-valvet.</span><span class="sxs-lookup"><span data-stu-id="9e3d0-110">You can use this cmdlet to view the operation information for the current Site Recovery vault.</span></span>

## <span data-ttu-id="9e3d0-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9e3d0-111">EXAMPLES</span></span>

## <span data-ttu-id="9e3d0-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9e3d0-112">PARAMETERS</span></span>

### <span data-ttu-id="9e3d0-113">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="9e3d0-113">-EndTime</span></span>
<span data-ttu-id="9e3d0-114">Anger slut tiden för jobben.</span><span class="sxs-lookup"><span data-stu-id="9e3d0-114">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="9e3d0-115">Denna cmdlet hämtar alla jobb som startade före angiven tid.</span><span class="sxs-lookup"><span data-stu-id="9e3d0-115">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="9e3d0-116">Om du vill hämta ett **datetime** -objekt för den här parametern använder du Get-Date cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e3d0-116">To obtain a **DateTime** object for this parameter, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="9e3d0-117">Om du vill ha mer information skriver du `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="9e3d0-117">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e3d0-118">-Jobb</span><span class="sxs-lookup"><span data-stu-id="9e3d0-118">-Job</span></span>
<span data-ttu-id="9e3d0-119">Anger återställnings jobbet för webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="9e3d0-119">Specifies the Site Recovery job.</span></span>

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

### <span data-ttu-id="9e3d0-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="9e3d0-120">-Name</span></span>
<span data-ttu-id="9e3d0-121">Anger ett unikt namn som identifierar jobbet.</span><span class="sxs-lookup"><span data-stu-id="9e3d0-121">Specifies a unique name that identifies the job.</span></span>

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

### <span data-ttu-id="9e3d0-122">-StartTime</span><span class="sxs-lookup"><span data-stu-id="9e3d0-122">-StartTime</span></span>
<span data-ttu-id="9e3d0-123">Anger start tiden för jobben.</span><span class="sxs-lookup"><span data-stu-id="9e3d0-123">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="9e3d0-124">Denna cmdlet hämtar alla jobb som startas efter den angivna tiden.</span><span class="sxs-lookup"><span data-stu-id="9e3d0-124">This cmdlet gets all jobs that started after the specified time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e3d0-125">-State</span><span class="sxs-lookup"><span data-stu-id="9e3d0-125">-State</span></span>
<span data-ttu-id="9e3d0-126">Anger inmatnings läget för ett webbplats återställnings jobb.</span><span class="sxs-lookup"><span data-stu-id="9e3d0-126">Specifies the input state for a Site Recovery job.</span></span>
<span data-ttu-id="9e3d0-127">Denna cmdlet hämtar alla jobb som matchar det angivna tillståndet.</span><span class="sxs-lookup"><span data-stu-id="9e3d0-127">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="9e3d0-128">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="9e3d0-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9e3d0-129">NotStarted</span><span class="sxs-lookup"><span data-stu-id="9e3d0-129">NotStarted</span></span>
- <span data-ttu-id="9e3d0-130">Inaktive</span><span class="sxs-lookup"><span data-stu-id="9e3d0-130">InProgress</span></span>
- <span data-ttu-id="9e3d0-131">Utför</span><span class="sxs-lookup"><span data-stu-id="9e3d0-131">Succeeded</span></span>
- <span data-ttu-id="9e3d0-132">Övrigt</span><span class="sxs-lookup"><span data-stu-id="9e3d0-132">Other</span></span>
- <span data-ttu-id="9e3d0-133">Startade</span><span class="sxs-lookup"><span data-stu-id="9e3d0-133">Failed</span></span>
- <span data-ttu-id="9e3d0-134">Annullerats</span><span class="sxs-lookup"><span data-stu-id="9e3d0-134">Cancelled</span></span>
- <span data-ttu-id="9e3d0-135">Hängande</span><span class="sxs-lookup"><span data-stu-id="9e3d0-135">Suspended</span></span>

```yaml
Type: System.String
Parameter Sets: ByParam
Aliases: 
Accepted values: NotStarted, InProgress, Succeeded, Other, Failed, Cancelled, Suspended

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e3d0-136">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="9e3d0-136">-TargetObjectId</span></span>
<span data-ttu-id="9e3d0-137">Anger ID för det objekt som är inriktat för jobbet.</span><span class="sxs-lookup"><span data-stu-id="9e3d0-137">Specifies the ID of the object targeted by the job.</span></span>

```yaml
Type: System.String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e3d0-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e3d0-138">-DefaultProfile</span></span>
<span data-ttu-id="9e3d0-139">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9e3d0-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e3d0-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e3d0-140">CommonParameters</span></span>
<span data-ttu-id="9e3d0-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e3d0-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e3d0-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e3d0-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e3d0-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9e3d0-143">INPUTS</span></span>

### <span data-ttu-id="9e3d0-144">ASRJob</span><span class="sxs-lookup"><span data-stu-id="9e3d0-144">ASRJob</span></span>
<span data-ttu-id="9e3d0-145">Parametern ' Job ' godkänner värdet av typen ' ASRJob ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="9e3d0-145">Parameter 'Job' accepts value of type 'ASRJob' from the pipeline</span></span>

## <span data-ttu-id="9e3d0-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9e3d0-146">OUTPUTS</span></span>

### <span data-ttu-id="9e3d0-147">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. commands. SiteRecovery. ASRJob]</span><span class="sxs-lookup"><span data-stu-id="9e3d0-147">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRJob]</span></span>

## <span data-ttu-id="9e3d0-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9e3d0-148">NOTES</span></span>

## <span data-ttu-id="9e3d0-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9e3d0-149">RELATED LINKS</span></span>

[<span data-ttu-id="9e3d0-150">Restart-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="9e3d0-150">Restart-AzureRmSiteRecoveryJob</span></span>](./Restart-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="9e3d0-151">Resume-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="9e3d0-151">Resume-AzureRmSiteRecoveryJob</span></span>](./Resume-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="9e3d0-152">Stopp-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="9e3d0-152">Stop-AzureRmSiteRecoveryJob</span></span>](./Stop-AzureRmSiteRecoveryJob.md)
