---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 36b13334c032304ddb61db04c360a1e310ef0876
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090366"
---
# <span data-ttu-id="b6827-101">Remove-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="b6827-101">Remove-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="b6827-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b6827-102">SYNOPSIS</span></span>
<span data-ttu-id="b6827-103">Tar bort den angivna skydds behållaren från dess Fabric.</span><span class="sxs-lookup"><span data-stu-id="b6827-103">Deletes the specified Protection Container from its Fabric.</span></span>

## <span data-ttu-id="b6827-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b6827-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrProtectionContainer -InputObject <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6827-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b6827-105">DESCRIPTION</span></span>
<span data-ttu-id="b6827-106">Remove-AzRecoveryServicesAsrProtectionContainer cmdlet tar bort den angivna Azure Site Recovery-behållaren.</span><span class="sxs-lookup"><span data-stu-id="b6827-106">The Remove-AzRecoveryServicesAsrProtectionContainer cmdlet deletes the specified Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="b6827-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b6827-107">EXAMPLES</span></span>

### <span data-ttu-id="b6827-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b6827-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrProtectionContainer -Name xxxxx  -Fabric $fabric
PS C:\> Remove-AzRecoveryServicesAsrProtectionContainer -InputObject $protectionContainer
```

<span data-ttu-id="b6827-109">Påbörjar borttagning av angiven skydds behållare och returnerar det ASR-jobb som används för att spåra borttagnings åtgärden.</span><span class="sxs-lookup"><span data-stu-id="b6827-109">Starts the deletion of specified protection container and returns the ASR job used to track the remove operation.</span></span>

## <span data-ttu-id="b6827-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b6827-110">PARAMETERS</span></span>

### <span data-ttu-id="b6827-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6827-111">-DefaultProfile</span></span>
<span data-ttu-id="b6827-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b6827-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6827-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b6827-113">-InputObject</span></span>
<span data-ttu-id="b6827-114">Anger skydds behållaren som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="b6827-114">Specifies the protection container to be removed .</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases: ProtectionContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6827-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b6827-115">-Confirm</span></span>
<span data-ttu-id="b6827-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b6827-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6827-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6827-117">-WhatIf</span></span>
<span data-ttu-id="b6827-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b6827-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6827-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b6827-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6827-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6827-120">CommonParameters</span></span>
<span data-ttu-id="b6827-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6827-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6827-122">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b6827-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6827-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b6827-123">INPUTS</span></span>

### <span data-ttu-id="b6827-124">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="b6827-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="b6827-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b6827-125">OUTPUTS</span></span>

### <span data-ttu-id="b6827-126">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="b6827-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="b6827-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b6827-127">NOTES</span></span>

## <span data-ttu-id="b6827-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b6827-128">RELATED LINKS</span></span>
