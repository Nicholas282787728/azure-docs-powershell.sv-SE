---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 6ff0031c5bb8571c69287968f984565daf58b530
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090367"
---
# <span data-ttu-id="de1fe-101">Remove-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="de1fe-101">Remove-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="de1fe-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="de1fe-102">SYNOPSIS</span></span>
<span data-ttu-id="de1fe-103">Tar bort den angivna principen för automatisk ASR från Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="de1fe-103">Deletes the specified ASR replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="de1fe-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="de1fe-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de1fe-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="de1fe-105">DESCRIPTION</span></span>
<span data-ttu-id="de1fe-106">Cmdleten **Remove-AzRecoveryServicesAsrPolicy** tog bort den angivna Replikeringsprincipen från Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="de1fe-106">The **Remove-AzRecoveryServicesAsrPolicy** cmdlet deleted the specified replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="de1fe-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="de1fe-107">EXAMPLES</span></span>

### <span data-ttu-id="de1fe-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="de1fe-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrPolicy -Policy $Policy
```

<span data-ttu-id="de1fe-109">Tar bort den angivna replikeringsprincipen och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="de1fe-109">Starts the deletion of the specified replication policy and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="de1fe-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="de1fe-110">PARAMETERS</span></span>

### <span data-ttu-id="de1fe-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de1fe-111">-DefaultProfile</span></span>
<span data-ttu-id="de1fe-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="de1fe-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="de1fe-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="de1fe-113">-InputObject</span></span>
<span data-ttu-id="de1fe-114">Indatavärdet till cmdleten: objektet ASR-replikeringsprincip som motsvarar den replikeringsprincip som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="de1fe-114">The input object to the cmdlet: The ASR replication policy object corresponding to the replication policy to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases: Policy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="de1fe-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="de1fe-115">-Confirm</span></span>
<span data-ttu-id="de1fe-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="de1fe-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de1fe-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de1fe-117">-WhatIf</span></span>
<span data-ttu-id="de1fe-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="de1fe-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="de1fe-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="de1fe-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de1fe-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de1fe-120">CommonParameters</span></span>
<span data-ttu-id="de1fe-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de1fe-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de1fe-122">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="de1fe-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de1fe-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="de1fe-123">INPUTS</span></span>

### <span data-ttu-id="de1fe-124">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="de1fe-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="de1fe-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="de1fe-125">OUTPUTS</span></span>

### <span data-ttu-id="de1fe-126">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="de1fe-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="de1fe-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="de1fe-127">NOTES</span></span>

## <span data-ttu-id="de1fe-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="de1fe-128">RELATED LINKS</span></span>

[<span data-ttu-id="de1fe-129">Get-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="de1fe-129">Get-AzRecoveryServicesAsrPolicy</span></span>](./Get-AzRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="de1fe-130">New-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="de1fe-130">New-AzRecoveryServicesAsrPolicy</span></span>](./New-AzRecoveryServicesAsrPolicy.md)