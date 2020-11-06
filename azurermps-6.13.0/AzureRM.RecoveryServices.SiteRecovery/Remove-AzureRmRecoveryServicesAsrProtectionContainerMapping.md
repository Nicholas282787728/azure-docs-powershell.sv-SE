---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: f034f91f026538bbae475466fbd9d3afa7067145
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584023"
---
# <span data-ttu-id="48225-101">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="48225-101">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="48225-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="48225-102">SYNOPSIS</span></span>
<span data-ttu-id="48225-103">Tar bort den angivna mappningen för Azure Site Recovery-skydd.</span><span class="sxs-lookup"><span data-stu-id="48225-103">Deletes the specified Azure Site Recovery protection container mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48225-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="48225-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48225-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="48225-105">DESCRIPTION</span></span>
<span data-ttu-id="48225-106">Cmdleten **Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping** tar bort den angivna mappningen av Azure Site Recovery-skydd.</span><span class="sxs-lookup"><span data-stu-id="48225-106">The **Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping** cmdlet deletes the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="48225-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="48225-107">EXAMPLES</span></span>

### <span data-ttu-id="48225-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="48225-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="48225-109">Påbörjar borttagning av angiven skydds behållare och returnerar det ASR-jobb som användes för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="48225-109">Starts the deletion of specified protection container mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="48225-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="48225-110">PARAMETERS</span></span>

### <span data-ttu-id="48225-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48225-111">-DefaultProfile</span></span>
<span data-ttu-id="48225-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="48225-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="48225-113">-Force</span><span class="sxs-lookup"><span data-stu-id="48225-113">-Force</span></span>
<span data-ttu-id="48225-114">Tvinga kommandot att köras utan ytterligare en varning.</span><span class="sxs-lookup"><span data-stu-id="48225-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="48225-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48225-115">-InputObject</span></span>
<span data-ttu-id="48225-116">Indatavärdet till cmdlet: mappnings objekt för ASR-skyddsagenten som motsvarar skydds behållaren som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="48225-116">The input object to the cmdlet: the ASR protection container mapping object corresponding to the protection container to be deleted.</span></span>

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

### <span data-ttu-id="48225-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="48225-117">-Confirm</span></span>
<span data-ttu-id="48225-118">Ange om du vill bekräfta.</span><span class="sxs-lookup"><span data-stu-id="48225-118">Specify if confirmation is required.</span></span> <span data-ttu-id="48225-119">Ange värdet för parametern Confirm till $false för att hoppa över bekräftelsen</span><span class="sxs-lookup"><span data-stu-id="48225-119">Set the value of the confirm parameter to $false in order to skip confirmation</span></span>

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

### <span data-ttu-id="48225-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48225-120">-WhatIf</span></span>
<span data-ttu-id="48225-121">Visar vad som händer om cmdleten körs utan att köra cmdleten.</span><span class="sxs-lookup"><span data-stu-id="48225-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="48225-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48225-122">CommonParameters</span></span>
<span data-ttu-id="48225-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48225-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48225-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48225-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48225-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="48225-125">INPUTS</span></span>

### <span data-ttu-id="48225-126">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="48225-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="48225-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="48225-127">OUTPUTS</span></span>

### <span data-ttu-id="48225-128">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="48225-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="48225-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="48225-129">NOTES</span></span>

## <span data-ttu-id="48225-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="48225-130">RELATED LINKS</span></span>

[<span data-ttu-id="48225-131">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="48225-131">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="48225-132">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="48225-132">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)
