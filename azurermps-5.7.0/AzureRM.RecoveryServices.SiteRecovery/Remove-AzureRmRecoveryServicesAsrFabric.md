---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrFabric.md
ms.openlocfilehash: 45979620ea4067af3fc906dfd7348d27b4850f06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579471"
---
# <span data-ttu-id="42c57-101">Remove-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="42c57-101">Remove-AzureRmRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="42c57-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="42c57-102">SYNOPSIS</span></span>
<span data-ttu-id="42c57-103">Tar bort den angivna Azure Site Recovery-Fabric från Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="42c57-103">Deletes the specified Azure Site Recovery Fabric from the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42c57-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="42c57-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrFabric -InputObject <ASRFabric> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42c57-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="42c57-105">DESCRIPTION</span></span>
<span data-ttu-id="42c57-106">Cmdleten **Remove-AzureRmRecoveryServicesAsrFabric** tar bort den angivna Azure Site Recovery-Fabric från Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="42c57-106">The **Remove-AzureRmRecoveryServicesAsrFabric** cmdlet removes the specified Azure Site Recovery fabric from the Recovery services vault.</span></span>

## <span data-ttu-id="42c57-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="42c57-107">EXAMPLES</span></span>

### <span data-ttu-id="42c57-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="42c57-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrFabric -Fabric $Fabric
```

<span data-ttu-id="42c57-109">Börjar ta bort angiven Fabric och returnerar det ASR-jobb som användes för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="42c57-109">Starts the deletion of specified fabric and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="42c57-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="42c57-110">PARAMETERS</span></span>

### <span data-ttu-id="42c57-111">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="42c57-111">-Confirm</span></span>
<span data-ttu-id="42c57-112">Ange om du vill bekräfta.</span><span class="sxs-lookup"><span data-stu-id="42c57-112">Specify if confirmation is required.</span></span> <span data-ttu-id="42c57-113">Ange värdet för parametern Confirm till $false för att hoppa över bekräftelsen.</span><span class="sxs-lookup"><span data-stu-id="42c57-113">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42c57-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42c57-114">-DefaultProfile</span></span>
<span data-ttu-id="42c57-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="42c57-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="42c57-116">-Force</span><span class="sxs-lookup"><span data-stu-id="42c57-116">-Force</span></span>
<span data-ttu-id="42c57-117">Tvinga kommandot att köras utan ytterligare en varning.</span><span class="sxs-lookup"><span data-stu-id="42c57-117">Force the command to run without providing an additional warning.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42c57-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="42c57-118">-InputObject</span></span>
<span data-ttu-id="42c57-119">Indatavärdet till cmdleten: det ASR Fabric-objekt som motsvarar infrastruktur resursen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="42c57-119">The input object to the cmdlet: The ASR fabric object corresponding to the fabric to be deleted.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases: Fabric

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42c57-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42c57-120">-WhatIf</span></span>
<span data-ttu-id="42c57-121">Visar vad som händer om cmdleten körs utan att köra cmdleten.</span><span class="sxs-lookup"><span data-stu-id="42c57-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42c57-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42c57-122">CommonParameters</span></span>
<span data-ttu-id="42c57-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42c57-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42c57-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42c57-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42c57-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="42c57-125">INPUTS</span></span>

### <span data-ttu-id="42c57-126">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="42c57-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="42c57-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="42c57-127">OUTPUTS</span></span>

### <span data-ttu-id="42c57-128">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="42c57-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="42c57-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="42c57-129">NOTES</span></span>

## <span data-ttu-id="42c57-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="42c57-130">RELATED LINKS</span></span>

[<span data-ttu-id="42c57-131">Get-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="42c57-131">Get-AzureRmRecoveryServicesAsrFabric</span></span>](./Get-AzureRmRecoveryServicesAsrFabric.md)

[<span data-ttu-id="42c57-132">New-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="42c57-132">New-AzureRmRecoveryServicesAsrFabric</span></span>](./New-AzureRmRecoveryServicesAsrFabric.md)
