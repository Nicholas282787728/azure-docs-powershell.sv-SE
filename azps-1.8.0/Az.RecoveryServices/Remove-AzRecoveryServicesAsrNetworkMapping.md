---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: e4e6579c330f8ac4189db2ddfc5d3a0578fd07f2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747369"
---
# <span data-ttu-id="377be-101">Remove-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="377be-101">Remove-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="377be-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="377be-102">SYNOPSIS</span></span>
<span data-ttu-id="377be-103">Tar bort den angivna nätverks mappningen för automatisk system återställning från Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="377be-103">Deletes the specified ASR network mapping from the Recovery Services vault.</span></span>

## <span data-ttu-id="377be-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="377be-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="377be-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="377be-105">DESCRIPTION</span></span>
<span data-ttu-id="377be-106">Cmdleten **Remove-AzRecoveryServicesAsrNetworkMapping** tar bort den angivna nätverks mappningen för automatisk system återställning.</span><span class="sxs-lookup"><span data-stu-id="377be-106">The **Remove-AzRecoveryServicesAsrNetworkMapping** cmdlet deletes the specified ASR network mapping.</span></span>

## <span data-ttu-id="377be-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="377be-107">EXAMPLES</span></span>

### <span data-ttu-id="377be-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="377be-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrNetworkMapping -NetworkMapping $networkmapping
```

<span data-ttu-id="377be-109">Tar bort den angivna nätverks mappningen för automatisk återställning och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="377be-109">Starts the deletion of specified ASR network mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="377be-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="377be-110">PARAMETERS</span></span>

### <span data-ttu-id="377be-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="377be-111">-DefaultProfile</span></span>
<span data-ttu-id="377be-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="377be-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="377be-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="377be-113">-InputObject</span></span>
<span data-ttu-id="377be-114">Indatavärdet till cmdlet: det objekt för ASR-nätverket som motsvarar nätverks mappningen för automatisk system återställning.</span><span class="sxs-lookup"><span data-stu-id="377be-114">The input object to the cmdlet: The ASR network mapping object corresponding to the ASR network mapping to be deleted.</span></span>

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

### <span data-ttu-id="377be-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="377be-115">-Confirm</span></span>
<span data-ttu-id="377be-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="377be-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="377be-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="377be-117">-WhatIf</span></span>
<span data-ttu-id="377be-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="377be-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="377be-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="377be-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="377be-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="377be-120">CommonParameters</span></span>
<span data-ttu-id="377be-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="377be-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="377be-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="377be-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="377be-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="377be-123">INPUTS</span></span>

### <span data-ttu-id="377be-124">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="377be-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="377be-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="377be-125">OUTPUTS</span></span>

### <span data-ttu-id="377be-126">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="377be-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="377be-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="377be-127">NOTES</span></span>

## <span data-ttu-id="377be-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="377be-128">RELATED LINKS</span></span>

[<span data-ttu-id="377be-129">Get-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="377be-129">Get-AzRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="377be-130">New-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="377be-130">New-AzRecoveryServicesAsrNetworkMapping</span></span>](./New-AzRecoveryServicesAsrNetworkMapping.md)
