---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: dcc0424cd1d6dbd823793a3dc77e813c6e182176
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757548"
---
# <span data-ttu-id="fd162-101">Remove-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="fd162-101">Remove-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="fd162-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fd162-102">SYNOPSIS</span></span>
<span data-ttu-id="fd162-103">Tar bort den angivna principen för automatisk ASR från Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="fd162-103">Deletes the specified ASR replication policy from the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd162-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fd162-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd162-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fd162-105">DESCRIPTION</span></span>
<span data-ttu-id="fd162-106">Cmdleten **Remove-AzureRmRecoveryServicesAsrPolicy** tog bort den angivna Replikeringsprincipen från Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="fd162-106">The **Remove-AzureRmRecoveryServicesAsrPolicy** cmdlet deleted the specified replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="fd162-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fd162-107">EXAMPLES</span></span>

### <span data-ttu-id="fd162-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fd162-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrPolicy -Policy $Policy
```

<span data-ttu-id="fd162-109">Tar bort den angivna replikeringsprincipen och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="fd162-109">Starts the deletion of the specified replication policy and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="fd162-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fd162-110">PARAMETERS</span></span>

### <span data-ttu-id="fd162-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd162-111">-DefaultProfile</span></span>
<span data-ttu-id="fd162-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fd162-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="fd162-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd162-113">-InputObject</span></span>
<span data-ttu-id="fd162-114">Indatavärdet till cmdleten: objektet ASR-replikeringsprincip som motsvarar den replikeringsprincip som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="fd162-114">The input object to the cmdlet: The ASR replication policy object corresponding to the replication policy to be deleted.</span></span>

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

### <span data-ttu-id="fd162-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fd162-115">-Confirm</span></span>
<span data-ttu-id="fd162-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fd162-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd162-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd162-117">-WhatIf</span></span>
<span data-ttu-id="fd162-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fd162-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fd162-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fd162-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd162-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd162-120">CommonParameters</span></span>
<span data-ttu-id="fd162-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd162-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd162-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd162-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd162-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fd162-123">INPUTS</span></span>

### <span data-ttu-id="fd162-124">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="fd162-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="fd162-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fd162-125">OUTPUTS</span></span>

### <span data-ttu-id="fd162-126">System. Object</span><span class="sxs-lookup"><span data-stu-id="fd162-126">System.Object</span></span>

## <span data-ttu-id="fd162-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fd162-127">NOTES</span></span>

## <span data-ttu-id="fd162-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fd162-128">RELATED LINKS</span></span>

[<span data-ttu-id="fd162-129">Get-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="fd162-129">Get-AzureRmRecoveryServicesAsrPolicy</span></span>](./Get-AzureRmRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="fd162-130">New-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="fd162-130">New-AzureRmRecoveryServicesAsrPolicy</span></span>](./New-AzureRmRecoveryServicesAsrPolicy.md)
