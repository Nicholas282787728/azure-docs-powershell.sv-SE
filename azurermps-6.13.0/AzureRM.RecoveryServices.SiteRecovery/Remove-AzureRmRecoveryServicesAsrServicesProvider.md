---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 4de1861c3db804e7ffd4371f4e35c241843374cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573947"
---
# <span data-ttu-id="7daee-101">Remove-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="7daee-101">Remove-AzureRmRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="7daee-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7daee-102">SYNOPSIS</span></span>
<span data-ttu-id="7daee-103">Tar bort/avregistrerar den angivna Recovery Services-leverantören för Azure Site Recovery från Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="7daee-103">Deletes/unregister the specified Azure Site Recovery recovery services provider from the recovery services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7daee-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7daee-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7daee-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7daee-105">DESCRIPTION</span></span>
<span data-ttu-id="7daee-106">Cmdleten **Remove-AzureRmRecoveryServicesAsrServicesProvider** tar bort den angivna Azure Site Recovery-leverantören från valvet.</span><span class="sxs-lookup"><span data-stu-id="7daee-106">The **Remove-AzureRmRecoveryServicesAsrServicesProvider** cmdlet removes the specified Azure Site Recovery recovery services provider from the vault.</span></span>

## <span data-ttu-id="7daee-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7daee-107">EXAMPLES</span></span>

### <span data-ttu-id="7daee-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7daee-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrServicesProvider -ServicesProvider $ServicesProvider
```

<span data-ttu-id="7daee-109">Startar borttagning/avregistrering av den angivna Azure Site Recovery Services-leverantören och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="7daee-109">Starts the deletion/unregistration of the specified Azure Site Recovery services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="7daee-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7daee-110">PARAMETERS</span></span>

### <span data-ttu-id="7daee-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7daee-111">-DefaultProfile</span></span>
<span data-ttu-id="7daee-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7daee-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="7daee-113">-Force</span><span class="sxs-lookup"><span data-stu-id="7daee-113">-Force</span></span>
<span data-ttu-id="7daee-114">Tvinga kommandot att köras utan ytterligare en varning.</span><span class="sxs-lookup"><span data-stu-id="7daee-114">Force the command to run without providing an additional warning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7daee-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7daee-115">-InputObject</span></span>
<span data-ttu-id="7daee-116">Indatavärdet till cmdleten: ASR Recovery Services-providern som motsvarar ASR Recovery Services-leverantören som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="7daee-116">The input object to the cmdlet: The ASR recovery services provider object corresponding to the ASR recovery services provider to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: ServicesProvider

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7daee-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7daee-117">-Confirm</span></span>
<span data-ttu-id="7daee-118">Ange om du vill bekräfta.</span><span class="sxs-lookup"><span data-stu-id="7daee-118">Specify if confirmation is required.</span></span> <span data-ttu-id="7daee-119">Ange värdet för parametern Confirm till $false för att hoppa över bekräftelsen.</span><span class="sxs-lookup"><span data-stu-id="7daee-119">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7daee-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7daee-120">-WhatIf</span></span>
<span data-ttu-id="7daee-121">Visar vad som händer om cmdleten körs utan att köra cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7daee-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7daee-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7daee-122">CommonParameters</span></span>
<span data-ttu-id="7daee-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7daee-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7daee-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7daee-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7daee-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7daee-125">INPUTS</span></span>

### <span data-ttu-id="7daee-126">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="7daee-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="7daee-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7daee-127">OUTPUTS</span></span>

### <span data-ttu-id="7daee-128">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob, Microsoft. Azure. commands. RecoveryServices. SiteRecovery, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="7daee-128">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="7daee-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7daee-129">NOTES</span></span>

## <span data-ttu-id="7daee-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7daee-130">RELATED LINKS</span></span>

[<span data-ttu-id="7daee-131">Get-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="7daee-131">Get-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Get-AzureRmRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="7daee-132">Update-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="7daee-132">Update-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Update-AzureRmRecoveryServicesAsrServicesProvider.md)
