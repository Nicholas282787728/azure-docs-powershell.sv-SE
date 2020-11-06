---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 0cc4a1c58349157024f38bce6e5ee2d8bcaa3cd5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584027"
---
# <span data-ttu-id="4b2b4-101">Remove-AzureRmRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="4b2b4-101">Remove-AzureRmRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="4b2b4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4b2b4-102">SYNOPSIS</span></span>
<span data-ttu-id="4b2b4-103">Tar bort den angivna skydds behållaren från dess Fabric.</span><span class="sxs-lookup"><span data-stu-id="4b2b4-103">Deletes the specified Protection Container from its Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b2b4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4b2b4-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrProtectionContainer -InputObject <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b2b4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4b2b4-105">DESCRIPTION</span></span>
<span data-ttu-id="4b2b4-106">Remove-AzureRmRecoveryServicesAsrProtectionContainer cmdlet tar bort den angivna Azure Site Recovery-behållaren.</span><span class="sxs-lookup"><span data-stu-id="4b2b4-106">The Remove-AzureRmRecoveryServicesAsrProtectionContainer cmdlet deletes the specified Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="4b2b4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4b2b4-107">EXAMPLES</span></span>

### <span data-ttu-id="4b2b4-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4b2b4-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrProtectionContainer -Name xxxxx  -Fabric $fabric
PS C:\> Remove-AzureRmRecoveryServicesAsrProtectionContainer -InputObject $protectionContainer
```

<span data-ttu-id="4b2b4-109">Påbörjar borttagning av angiven skydds behållare och returnerar det ASR-jobb som används för att spåra borttagnings åtgärden.</span><span class="sxs-lookup"><span data-stu-id="4b2b4-109">Starts the deletion of specified protection container and returns the ASR job used to track the remove operation.</span></span>

## <span data-ttu-id="4b2b4-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4b2b4-110">PARAMETERS</span></span>

### <span data-ttu-id="4b2b4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b2b4-111">-DefaultProfile</span></span>
<span data-ttu-id="4b2b4-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4b2b4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b2b4-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4b2b4-113">-InputObject</span></span>
<span data-ttu-id="4b2b4-114">Anger skydds behållaren som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="4b2b4-114">Specifies the protection container to be removed .</span></span>

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

### <span data-ttu-id="4b2b4-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4b2b4-115">-Confirm</span></span>
<span data-ttu-id="4b2b4-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4b2b4-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b2b4-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b2b4-117">-WhatIf</span></span>
<span data-ttu-id="4b2b4-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4b2b4-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b2b4-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4b2b4-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b2b4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b2b4-120">CommonParameters</span></span>
<span data-ttu-id="4b2b4-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b2b4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b2b4-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b2b4-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b2b4-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4b2b4-123">INPUTS</span></span>

### <span data-ttu-id="4b2b4-124">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="4b2b4-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="4b2b4-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4b2b4-125">OUTPUTS</span></span>

### <span data-ttu-id="4b2b4-126">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="4b2b4-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="4b2b4-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4b2b4-127">NOTES</span></span>

## <span data-ttu-id="4b2b4-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4b2b4-128">RELATED LINKS</span></span>
