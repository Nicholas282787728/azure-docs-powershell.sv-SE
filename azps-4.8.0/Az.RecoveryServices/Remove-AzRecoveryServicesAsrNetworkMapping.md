---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: ef251bb9d1060e511658f9174cde2c04ab288ed7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94100914"
---
# <span data-ttu-id="c9730-101">Remove-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="c9730-101">Remove-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="c9730-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c9730-102">SYNOPSIS</span></span>
<span data-ttu-id="c9730-103">Tar bort den angivna nätverks mappningen för automatisk system återställning från Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="c9730-103">Deletes the specified ASR network mapping from the Recovery Services vault.</span></span>

## <span data-ttu-id="c9730-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c9730-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9730-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c9730-105">DESCRIPTION</span></span>
<span data-ttu-id="c9730-106">Cmdleten **Remove-AzRecoveryServicesAsrNetworkMapping** tar bort den angivna nätverks mappningen för automatisk system återställning.</span><span class="sxs-lookup"><span data-stu-id="c9730-106">The **Remove-AzRecoveryServicesAsrNetworkMapping** cmdlet deletes the specified ASR network mapping.</span></span>

## <span data-ttu-id="c9730-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c9730-107">EXAMPLES</span></span>

### <span data-ttu-id="c9730-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c9730-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrNetworkMapping -NetworkMapping $networkmapping
```

<span data-ttu-id="c9730-109">Tar bort den angivna nätverks mappningen för automatisk återställning och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="c9730-109">Starts the deletion of specified ASR network mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="c9730-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c9730-110">PARAMETERS</span></span>

### <span data-ttu-id="c9730-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9730-111">-DefaultProfile</span></span>
<span data-ttu-id="c9730-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c9730-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="c9730-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c9730-113">-InputObject</span></span>
<span data-ttu-id="c9730-114">Indatavärdet till cmdlet: det objekt för ASR-nätverket som motsvarar nätverks mappningen för automatisk system återställning.</span><span class="sxs-lookup"><span data-stu-id="c9730-114">The input object to the cmdlet: The ASR network mapping object corresponding to the ASR network mapping to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping
Parameter Sets: (All)
Aliases: NetworkMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9730-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c9730-115">-Confirm</span></span>
<span data-ttu-id="c9730-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c9730-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9730-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9730-117">-WhatIf</span></span>
<span data-ttu-id="c9730-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c9730-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c9730-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c9730-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9730-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9730-120">CommonParameters</span></span>
<span data-ttu-id="c9730-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9730-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9730-122">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c9730-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9730-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c9730-123">INPUTS</span></span>

### <span data-ttu-id="c9730-124">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="c9730-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="c9730-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c9730-125">OUTPUTS</span></span>

### <span data-ttu-id="c9730-126">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="c9730-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c9730-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c9730-127">NOTES</span></span>

## <span data-ttu-id="c9730-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c9730-128">RELATED LINKS</span></span>

[<span data-ttu-id="c9730-129">Get-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="c9730-129">Get-AzRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="c9730-130">New-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="c9730-130">New-AzRecoveryServicesAsrNetworkMapping</span></span>](./New-AzRecoveryServicesAsrNetworkMapping.md)
