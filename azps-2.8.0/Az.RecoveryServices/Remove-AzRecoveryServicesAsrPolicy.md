---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: a358e38dcba9c0f7fb4bae0c1b1af28845a3851b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920212"
---
# <span data-ttu-id="fe529-101">Remove-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="fe529-101">Remove-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="fe529-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fe529-102">SYNOPSIS</span></span>
<span data-ttu-id="fe529-103">Tar bort den angivna principen för automatisk ASR från Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="fe529-103">Deletes the specified ASR replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="fe529-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fe529-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe529-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fe529-105">DESCRIPTION</span></span>
<span data-ttu-id="fe529-106">Cmdleten **Remove-AzRecoveryServicesAsrPolicy** tog bort den angivna Replikeringsprincipen från Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="fe529-106">The **Remove-AzRecoveryServicesAsrPolicy** cmdlet deleted the specified replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="fe529-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fe529-107">EXAMPLES</span></span>

### <span data-ttu-id="fe529-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fe529-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrPolicy -Policy $Policy
```

<span data-ttu-id="fe529-109">Tar bort den angivna replikeringsprincipen och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="fe529-109">Starts the deletion of the specified replication policy and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="fe529-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fe529-110">PARAMETERS</span></span>

### <span data-ttu-id="fe529-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe529-111">-DefaultProfile</span></span>
<span data-ttu-id="fe529-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fe529-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="fe529-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fe529-113">-InputObject</span></span>
<span data-ttu-id="fe529-114">Indatavärdet till cmdleten: objektet ASR-replikeringsprincip som motsvarar den replikeringsprincip som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="fe529-114">The input object to the cmdlet: The ASR replication policy object corresponding to the replication policy to be deleted.</span></span>

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

### <span data-ttu-id="fe529-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fe529-115">-Confirm</span></span>
<span data-ttu-id="fe529-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fe529-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe529-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe529-117">-WhatIf</span></span>
<span data-ttu-id="fe529-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fe529-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fe529-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fe529-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe529-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe529-120">CommonParameters</span></span>
<span data-ttu-id="fe529-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe529-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe529-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe529-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe529-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fe529-123">INPUTS</span></span>

### <span data-ttu-id="fe529-124">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="fe529-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="fe529-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fe529-125">OUTPUTS</span></span>

### <span data-ttu-id="fe529-126">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="fe529-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="fe529-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fe529-127">NOTES</span></span>

## <span data-ttu-id="fe529-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fe529-128">RELATED LINKS</span></span>

[<span data-ttu-id="fe529-129">Get-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="fe529-129">Get-AzRecoveryServicesAsrPolicy</span></span>](./Get-AzRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="fe529-130">New-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="fe529-130">New-AzRecoveryServicesAsrPolicy</span></span>](./New-AzRecoveryServicesAsrPolicy.md)
