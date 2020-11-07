---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 20a57bd70c9cf9b1b533e040001afee0cc5809fc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747367"
---
# <span data-ttu-id="c111e-101">Remove-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="c111e-101">Remove-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="c111e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c111e-102">SYNOPSIS</span></span>
<span data-ttu-id="c111e-103">Tar bort den angivna skydds behållaren från dess Fabric.</span><span class="sxs-lookup"><span data-stu-id="c111e-103">Deletes the specified Protection Container from its Fabric.</span></span>

## <span data-ttu-id="c111e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c111e-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrProtectionContainer -InputObject <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c111e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c111e-105">DESCRIPTION</span></span>
<span data-ttu-id="c111e-106">Remove-AzRecoveryServicesAsrProtectionContainer cmdlet tar bort den angivna Azure Site Recovery-behållaren.</span><span class="sxs-lookup"><span data-stu-id="c111e-106">The Remove-AzRecoveryServicesAsrProtectionContainer cmdlet deletes the specified Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="c111e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c111e-107">EXAMPLES</span></span>

### <span data-ttu-id="c111e-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c111e-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrProtectionContainer -Name xxxxx  -Fabric $fabric
PS C:\> Remove-AzRecoveryServicesAsrProtectionContainer -InputObject $protectionContainer
```

<span data-ttu-id="c111e-109">Påbörjar borttagning av angiven skydds behållare och returnerar det ASR-jobb som används för att spåra borttagnings åtgärden.</span><span class="sxs-lookup"><span data-stu-id="c111e-109">Starts the deletion of specified protection container and returns the ASR job used to track the remove operation.</span></span>

## <span data-ttu-id="c111e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c111e-110">PARAMETERS</span></span>

### <span data-ttu-id="c111e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c111e-111">-DefaultProfile</span></span>
<span data-ttu-id="c111e-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c111e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c111e-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c111e-113">-InputObject</span></span>
<span data-ttu-id="c111e-114">Anger skydds behållaren som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="c111e-114">Specifies the protection container to be removed .</span></span>

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

### <span data-ttu-id="c111e-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c111e-115">-Confirm</span></span>
<span data-ttu-id="c111e-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c111e-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c111e-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c111e-117">-WhatIf</span></span>
<span data-ttu-id="c111e-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c111e-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c111e-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c111e-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c111e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c111e-120">CommonParameters</span></span>
<span data-ttu-id="c111e-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c111e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c111e-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c111e-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c111e-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c111e-123">INPUTS</span></span>

### <span data-ttu-id="c111e-124">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="c111e-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="c111e-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c111e-125">OUTPUTS</span></span>

### <span data-ttu-id="c111e-126">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="c111e-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c111e-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c111e-127">NOTES</span></span>

## <span data-ttu-id="c111e-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c111e-128">RELATED LINKS</span></span>