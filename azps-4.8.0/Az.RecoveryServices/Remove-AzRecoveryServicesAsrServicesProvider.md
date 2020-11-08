---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 9a9fbf8c25eba6206b3852476b5a72a2f96be423
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260441"
---
# <span data-ttu-id="741c2-101">Remove-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="741c2-101">Remove-AzRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="741c2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="741c2-102">SYNOPSIS</span></span>
<span data-ttu-id="741c2-103">Tar bort/avregistrerar den angivna Recovery Services-leverantören för Azure Site Recovery från Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="741c2-103">Deletes/unregister the specified Azure Site Recovery recovery services provider from the recovery services vault.</span></span>

## <span data-ttu-id="741c2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="741c2-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="741c2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="741c2-105">DESCRIPTION</span></span>
<span data-ttu-id="741c2-106">Cmdleten **Remove-AzRecoveryServicesAsrServicesProvider** tar bort den angivna Azure Site Recovery-leverantören från valvet.</span><span class="sxs-lookup"><span data-stu-id="741c2-106">The **Remove-AzRecoveryServicesAsrServicesProvider** cmdlet removes the specified Azure Site Recovery recovery services provider from the vault.</span></span>

## <span data-ttu-id="741c2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="741c2-107">EXAMPLES</span></span>

### <span data-ttu-id="741c2-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="741c2-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrServicesProvider -ServicesProvider $ServicesProvider
```

<span data-ttu-id="741c2-109">Startar borttagning/avregistrering av den angivna Azure Site Recovery Services-leverantören och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="741c2-109">Starts the deletion/unregistration of the specified Azure Site Recovery services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="741c2-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="741c2-110">PARAMETERS</span></span>

### <span data-ttu-id="741c2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="741c2-111">-DefaultProfile</span></span>
<span data-ttu-id="741c2-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="741c2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="741c2-113">-Force</span><span class="sxs-lookup"><span data-stu-id="741c2-113">-Force</span></span>
<span data-ttu-id="741c2-114">Tvinga kommandot att köras utan ytterligare en varning.</span><span class="sxs-lookup"><span data-stu-id="741c2-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="741c2-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="741c2-115">-InputObject</span></span>
<span data-ttu-id="741c2-116">Indatavärdet till cmdleten: ASR Recovery Services-providern som motsvarar ASR Recovery Services-leverantören som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="741c2-116">The input object to the cmdlet: The ASR recovery services provider object corresponding to the ASR recovery services provider to be deleted.</span></span>

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

### <span data-ttu-id="741c2-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="741c2-117">-Confirm</span></span>
<span data-ttu-id="741c2-118">Ange om du vill bekräfta.</span><span class="sxs-lookup"><span data-stu-id="741c2-118">Specify if confirmation is required.</span></span> <span data-ttu-id="741c2-119">Ange värdet för parametern Confirm till $false för att hoppa över bekräftelsen.</span><span class="sxs-lookup"><span data-stu-id="741c2-119">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="741c2-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="741c2-120">-WhatIf</span></span>
<span data-ttu-id="741c2-121">Visar vad som händer om cmdleten körs utan att köra cmdleten.</span><span class="sxs-lookup"><span data-stu-id="741c2-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="741c2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="741c2-122">CommonParameters</span></span>
<span data-ttu-id="741c2-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="741c2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="741c2-124">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="741c2-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="741c2-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="741c2-125">INPUTS</span></span>

### <span data-ttu-id="741c2-126">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="741c2-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="741c2-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="741c2-127">OUTPUTS</span></span>

### <span data-ttu-id="741c2-128">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="741c2-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="741c2-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="741c2-129">NOTES</span></span>

## <span data-ttu-id="741c2-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="741c2-130">RELATED LINKS</span></span>

[<span data-ttu-id="741c2-131">Get-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="741c2-131">Get-AzRecoveryServicesAsrServicesProvider</span></span>](./Get-AzRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="741c2-132">Update-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="741c2-132">Update-AzRecoveryServicesAsrServicesProvider</span></span>](./Update-AzRecoveryServicesAsrServicesProvider.md)
