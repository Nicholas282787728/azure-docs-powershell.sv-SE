---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 9ff992231e48efdfa9873aae75fc602ccd53a64e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747365"
---
# <span data-ttu-id="c37b5-101">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="c37b5-101">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="c37b5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c37b5-102">SYNOPSIS</span></span>
<span data-ttu-id="c37b5-103">Tar bort den angivna mappningen för Azure Site Recovery-skydd.</span><span class="sxs-lookup"><span data-stu-id="c37b5-103">Deletes the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="c37b5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c37b5-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c37b5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c37b5-105">DESCRIPTION</span></span>
<span data-ttu-id="c37b5-106">Cmdleten **Remove-AzRecoveryServicesAsrProtectionContainerMapping** tar bort den angivna mappningen av Azure Site Recovery-skydd.</span><span class="sxs-lookup"><span data-stu-id="c37b5-106">The **Remove-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet deletes the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="c37b5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c37b5-107">EXAMPLES</span></span>

### <span data-ttu-id="c37b5-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c37b5-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrProtectionContainerMapping -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="c37b5-109">Påbörjar borttagning av angiven skydds behållare och returnerar det ASR-jobb som användes för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="c37b5-109">Starts the deletion of specified protection container mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="c37b5-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c37b5-110">PARAMETERS</span></span>

### <span data-ttu-id="c37b5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c37b5-111">-DefaultProfile</span></span>
<span data-ttu-id="c37b5-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c37b5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="c37b5-113">-Force</span><span class="sxs-lookup"><span data-stu-id="c37b5-113">-Force</span></span>
<span data-ttu-id="c37b5-114">Tvinga kommandot att köras utan ytterligare en varning.</span><span class="sxs-lookup"><span data-stu-id="c37b5-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="c37b5-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c37b5-115">-InputObject</span></span>
<span data-ttu-id="c37b5-116">Indatavärdet till cmdlet: mappnings objekt för ASR-skyddsagenten som motsvarar skydds behållaren som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="c37b5-116">The input object to the cmdlet: the ASR protection container mapping object corresponding to the protection container to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases: ProtectionContainerMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c37b5-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c37b5-117">-Confirm</span></span>
<span data-ttu-id="c37b5-118">Ange om du vill bekräfta.</span><span class="sxs-lookup"><span data-stu-id="c37b5-118">Specify if confirmation is required.</span></span> <span data-ttu-id="c37b5-119">Ange värdet för parametern Confirm till $false för att hoppa över bekräftelsen</span><span class="sxs-lookup"><span data-stu-id="c37b5-119">Set the value of the confirm parameter to $false in order to skip confirmation</span></span>

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

### <span data-ttu-id="c37b5-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c37b5-120">-WhatIf</span></span>
<span data-ttu-id="c37b5-121">Visar vad som händer om cmdleten körs utan att köra cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c37b5-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="c37b5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c37b5-122">CommonParameters</span></span>
<span data-ttu-id="c37b5-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c37b5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c37b5-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c37b5-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c37b5-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c37b5-125">INPUTS</span></span>

### <span data-ttu-id="c37b5-126">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="c37b5-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="c37b5-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c37b5-127">OUTPUTS</span></span>

### <span data-ttu-id="c37b5-128">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="c37b5-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c37b5-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c37b5-129">NOTES</span></span>

## <span data-ttu-id="c37b5-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c37b5-130">RELATED LINKS</span></span>

[<span data-ttu-id="c37b5-131">Get-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="c37b5-131">Get-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="c37b5-132">New-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="c37b5-132">New-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzRecoveryServicesAsrProtectionContainerMapping.md)
